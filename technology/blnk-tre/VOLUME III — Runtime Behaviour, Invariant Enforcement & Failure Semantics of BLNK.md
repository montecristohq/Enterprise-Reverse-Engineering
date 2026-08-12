# VOLUME III — Runtime Behaviour, Invariant Enforcement & Failure Semantics of BLNK

```
Technology:              Blnk — open-source double-entry financial ledger
Technology type:         LEDGER
Primary repository:      https://github.com/blnkfinance/blnk
Version / release:       v0.15.0 (22 June 2026) pinned; patch line to v0.15.2 (31 July 2026)
Source openness:         OPEN SOURCE — Apache-2.0 ("Blnk Core")
Research date:           11 August 2026
Study objective:         BUILD EXTRACTION
Configuration:           EXTENDED 7
```

## TL;DR
- **The caller's HTTP response almost never means the money moved.** By default every write returns `QUEUED` with a `_q`-suffixed reference; the real commit point is later, inside an asynq worker that acquires a Redis lock, mutates cached balances, and inserts the row — and even inflight commit/void are queued-by-default since v0.15.0. A cooperative-savings reader must treat 201/200 as "accepted", not "settled".
- **Conservation and precision are strong; concurrency-safety, tenancy and event-durability are weak.** Double-entry conservation (INV-1) and integer-minor-unit precision (INV-7) are enforced structurally/by construction; idempotency (INV-4) and immutability (INV-5/INV-11) are backed by a unique index and a DB immutability trigger. But the single-key Redis lock, webhook-without-outbox, and absent tenancy owner mean INV-9, INV-10 and INV-12 are enforced only by check or by convention — defects a hot cooperative balance will find.
- **The `precise_amount`/balance PostgreSQL column type remains UNKNOWN.** The DDL in the embedded `sql/` dir could not be retrieved by any automated route. Go `*big.Int` plus string-JSON serialization plus the ">15 digit" changelog claim strongly imply unbounded `NUMERIC`, but this is SOURCE-CODE INFERENCE, not confirmed. We keep it UNKNOWN, correcting no earlier volume.

---

## Key Findings

1. **Queue-by-default is the defining mechanism.** `QueueTransaction` (transaction.go) sets `SkipBalanceUpdate=true`, computes `PreciseAmount`, hashes, splits, and enqueues to asynq. The API returns `QUEUED` before any balance moves. A separate worker process later runs `RecordTransaction`, which is where money actually moves. The asynq defaults are named in Blnk's configuration docs: transaction queue `new:transaction`, webhook queue `new:webhook`, index queue `new:index`, inflight-expiry queue `new:inflight-expiry`; number of queues 20, max workers 10, max retries 3, retry delay 5 seconds. [CONFIRMED IMPLEMENTATION — transaction.go `QueueTransaction`, `setTransactionMetadata`, `enqueueTransactions`; DOCUMENTED BEHAVIOR — docs.blnkfinance.com/advanced/configuration]

2. **The real commit point is the worker's `finalizeTransaction` → `persistTransaction`, not the API response.** In the synchronous (`skip_queue`/worker) path, `RecordTransaction` runs under `executeWithLock`: validate → get balances → apply-to-balances in memory → `updateBalances` (persist balances) → `persistTransaction` (insert txn row) → post-actions. Balance write and transaction-row write are **two separate datasource calls**, not one DB transaction, in the code observed. [CONFIRMED IMPLEMENTATION (Aug-2024 fork transaction.go); SOURCE-CODE INFERENCE that v0.15.x preserves the two-call ordering]

3. **Balances are persisted BEFORE the transaction row.** `processBalances` (which calls `updateBalances`) runs before `finalizeTransaction` (which calls `persistTransaction`). A crash between them leaves balances mutated with **no APPLIED transaction row** — a durable, silent partial state. [SOURCE-CODE INFERENCE — transaction.go ordering]

4. **Webhooks fire from a detached goroutine with no outbox on the main path.** `postTransactionActions` launches `go func(){ SendWebhook(...) }()`. There is no transactional coupling: a webhook can be emitted for a state the DB later fails to persist, or lost entirely if the process dies. Volume II found the *lineage* subsystem uses `lineage_outbox.go`; the **main transaction/webhook path does not**. [CONFIRMED IMPLEMENTATION — transaction.go `postTransactionActions`, webhooks.go `SendWebhook`]

5. **Idempotency is a SELECT-then-check race backstopped by a unique index.** `validateTxn` calls `TransactionExistsByRef` and rejects if found — a TOCTOU window. Two identical references racing through the API both pass the check; the DB index `idx_transactions_reference_unique` (v0.13.2) is the real guarantee, converting the loser into an insert error the caller must interpret. [CONFIRMED IMPLEMENTATION — transaction.go `validateTxn`; DOCUMENTED BEHAVIOR — unique index]

6. **The `_q` suffix does NOT weaken caller idempotency.** `validateTxn` checks the caller's original reference before enqueue; the `_q` suffix is applied to the stored/queued record. A caller retrying with the original reference collides correctly at validation and/or at the unique index. [SOURCE-CODE INFERENCE — validateTxn runs on original reference in QueueTransaction]

7. **The distributed lock is keyed on the SOURCE balance only (historically), creating asymmetric protection.** In the Aug-2024 fork, `acquireLock` locked `transaction.Source` with a lock duration that Blnk's configuration docs give as a default of 1800 seconds (30 minutes). v0.15.x changed the inflight-commit lock key to `inflight-commit:%s` (per-transaction). Where the lock is per-source-balance, two transactions crediting the same destination from different sources are **not mutually excluded on the destination** — optimistic `version` is the only backstop there. [CONFIRMED IMPLEMENTATION (fork) `acquireLock`; DOCUMENTED BEHAVIOR (lock duration 1800s); SOURCE-CODE INFERENCE for v0.15.x generalization]

8. **Optimistic `version` is the last line of defence, and its retry behaviour is thin.** Blnk's blog "How Blnk Handles High-Traffic Hot Balances" (17 July 2026) states verbatim: *"Each balance has a version number. A payment remembers the version it read, and its write only succeeds if that version has not changed. If another payment has already updated the balance, the stale write is rejected and must be retried using the new value."* Under a hot cooperative balance the queue serialises work per hot pair (coalescing + hot-lane routing), but a version conflict surfaces as a failed/retried unit, not a silent merge. The same blog specifies the lock-wait behaviour: *"This configuration allows Blnk to wait for up to three seconds when acquiring the required balance locks. It does not delay every transaction by three seconds. A transaction continues as soon as the lock becomes available."* [MAINTAINER CLAIM — hot-balances blog; DOCUMENTED BEHAVIOR]

9. **Backdated transactions do NOT rewrite history or recompute prior balances at runtime.** `effective_date` is stored and used by *historical* balance queries and reconstruction, but a live backdated insert applies to the current cached running balance like any other transaction (it moves `balance` now). Blnk's own migration guidance — set the initial adjustment's `effective_date` before all others — is a workaround precisely because later-applied backdated rows affect the running balance in application order, not effective-date order. [DOCUMENTED BEHAVIOR — migration guide; ANALYTICAL INFERENCE]

10. **Balance reconstruction can silently diverge from the stored balance.** The v0.10.1 "Balance Reconstruction" recomputes balances from transactions and writes a `BLNK_RECONCILIATION_RESULT` into metadata containing `previous_balance`, `recalculated_balance`, and `difference` (the v0.10.1 blog shows a live `"difference":"103842"` recorded in `meta_data`). The difference is recorded in metadata; there is no evidence of an automatic alert/halt when it is non-zero — an operator must inspect it. [DOCUMENTED BEHAVIOR — v0.10.1 blog]

---

## Details

### III.1 Representative operations (boundary-crossing set)
Selected to cross the most boundaries (API ↔ Redis queue ↔ worker ↔ Postgres ↔ webhook/Typesense):
1. Simple queued transaction (`POST /transactions`, default).
2. `skip_queue:true` direct transaction (synchronous, bypasses asynq).
3. Inflight create → commit (two-phase).
4. Inflight create → void.
5. Partial inflight commit (`amount` < original).
6. Multi-destination split (`SplitTransaction`).
7. Bulk transaction `atomic:true`.
8. Refund (`RefundTransaction` → new reversed queued txn).
9. Backdated transaction (`effective_date`).
10. Reconciliation / balance reconstruction run.

### III.2 Happy-path execution — queued vs direct

**Queued (default).** API process: parse → auth (scoped `X-blnk-key`) → `QueueTransaction`: `validateTxn` (reference SELECT) → `setTransactionStatus` (QUEUED/SCHEDULED/INFLIGHT) → `setTransactionMetadata` (`SkipBalanceUpdate=true`, `TransactionID`, `HashTxn`, `PreciseAmount=int64(Amount*Precision)` historically / `*big.Int` in v0.15.x) → `SplitTransaction` → `enqueueTransactions` (asynq `new:transaction`, 20 queues, max 10 workers). **Response returns here: status QUEUED, no money moved.** Worker process later: dequeues → `RecordTransaction` under `executeWithLock` → `validateAndPrepareTransaction` → `processBalances` (`applyTransactionToBalances` in memory → `updateBalances` persists source+destination) → `finalizeTransaction` (`persistTransaction` inserts row, status APPLIED) → `postTransactionActions` (async webhook). **Money moves inside the worker, at `updateBalances`.**

**Direct (`skip_queue:true`).** Same `RecordTransaction` path but executed synchronously in the API request; response returns after `persistTransaction`. This is the only mode where "response received" ≈ "money moved" — and the one that throws `Failed to acquire lock` under contention (after the configured 3-second lock wait elapses).

### III.3 INVARIANT ENFORCEMENT VERIFICATION TABLE

| Inv | Runtime enforcement point (file, function, constraint) | Classification | Evidence | Bypass path |
|---|---|---|---|---|
| INV-1 Conservation | `model.UpdateBalances` applies equal debit to source / credit to destination from one `precise_amount`; double-entry requires both source+destination | **Structural (by construction)** | CONFIRMED IMPL (`applyTransactionToBalances`→`model.UpdateBalances`) | None on write path; a single amount drives both legs |
| INV-2 Balances change only via transactions | All mutation flows through `updateBalances`/`UpdateBalances`; `CreateBalance` starts at 0 | **By check / convention** | CONFIRMED IMPL | Direct DB write; reconstruction overwrites balance |
| INV-3 Derivability from history | Balance Reconstruction recomputes from transactions | **By check** | DOCUMENTED | Cached balance is authoritative day-to-day; drift possible until reconstruction |
| INV-4 Idempotency (unique reference) | `validateTxn` SELECT + DB index `idx_transactions_reference_unique` | **Structural (index) + by check (pre-check)** | CONFIRMED IMPL + DOCUMENTED | Concurrent duplicates pass `validateTxn`; index rejects loser as error |
| INV-5 Immutability of posted txns | New `parent_transaction`-linked rows for every state change; DB immutability trigger on protected fields | **Structural (trigger) + convention (append-only design)** | CONFIRMED IMPL (finalizeCommitment/finalizeVoid create new rows); DOCUMENTED (hash doc "immutability trigger") | Non-protected fields (`description`,`meta_data`) mutable |
| INV-6 Valid state transitions | `fetchAndValidateTransaction` / `fetchAndValidateInflightTransaction` guard status == INFLIGHT; `IsParentTransactionVoid` | **By check** | CONFIRMED IMPL | No DB CHECK on status; guards live only in the two inflight functions |
| INV-7 Precision integrity (integer minor units) | `PreciseAmount` integer; `model.ApplyPrecision`; per-row hash uses float `amount` | **Structural (integer storage) with a lossy ingress** | CONFIRMED IMPL | `int64(Amount*Precision)` truncates float at ingress (see III.5) |
| INV-8 Sufficient funds unless overdraft | Balance check `balance - inflight_debit_balance` since v0.11.0; `allow_overdraft` + overdraft limit | **By check** | DOCUMENTED | Queued estimate vs committed balance gap; overdraft bypasses; check is code not constraint |
| INV-9 Concurrency safety (lock + version) | Redis `redlock` on source balance / per-txn inflight key; optimistic `version` on balance write | **By check** | CONFIRMED IMPL + MAINTAINER CLAIM | Lock keyed on source only → destination collisions rely on version alone; lock is advisory |
| INV-10 Zero/malformed not recorded | Validation rejects zero amount / bad body; discarded (not stored) | **By check** | DOCUMENTED | Convention-level; no DB CHECK(amount>0) confirmed |
| INV-11 Tamper-evidence (`HashTxn` + chain) | `HashTxn` SHA-256 per row (always); optional global hash chain (v0.15.0, off by default); `blnk verify-chain` | **By check (per-row) / structural-if-enabled (chain)** | CONFIRMED IMPL + DOCUMENTED | Per-row hash covers only amount/reference/currency/source/destination; chain disabled by default |
| INV-12 Authorisation & tenancy | Scoped API keys (`transactions:write` etc.) at API middleware | **Auth: by check. Tenancy: NOT ENFORCED (no owner component)** | DOCUMENTED (scopes); Vol II finding | No tenant isolation in data model; keys gate verbs not tenants |

**The decisive distinctions for a savings cooperative:** INV-1 and INV-7-storage are guarantees; INV-8, INV-9, INV-10, INV-12-tenancy are *hopes* enforced by code paths or absent entirely. A concurrent caller on a hot pooled balance is exactly the actor that reaches balance state without the protection being sufficient.

### III.4 State machines

**Transaction:** `QUEUED`/`SCHEDULED` → (`APPLIED` | `INFLIGHT` | `REJECTED`); `INFLIGHT` → (`APPLIED` via commit | `VOID` via void); `APPLIED`/`VOID`/`REJECTED` terminal. Every transition is a **new row** linked by `parent_transaction` (never an in-place update). Guards: `setTransactionStatus` chooses initial state; `fetchAndValidate*` enforce INFLIGHT precondition. Invalid transitions (e.g., commit of an APPLIED txn) are **prevented by check** ("transaction is not in inflight status"), not by a DB constraint — so an untested code path could reach the same state.

**Balance:** mutable running total; fields move between `balance`, `inflight_balance`, `credit/debit`, `inflight_credit/debit`. Inflight create: `balance`↓, `inflight_balance`↑. Commit: `inflight`→`debit/credit` (`CommitInflightDebit/Credit`). Void: `RollbackInflightDebit/Credit` restores `balance`. `version` increments each write.

### III.5 Data flow & lossy transformations
Ingress float `amount` × caller `precision` → `PreciseAmount`. In the fork this is `int64(transaction.Amount * transaction.Precision)` — a **float64 multiply then integer truncation** (lossy, truncates toward zero; the classic 0.1+0.2 float error can shave a minor unit). v0.15.x accepts `precise_amount` directly as `*big.Int`, letting disciplined callers bypass the float entirely — the recommended path for a savings ledger. The original float `amount` **is preserved** on the row and is what the per-row hash fingerprints. Lossy points: (1) float→int at ingress if `amount` is used; (2) partial-commit remainder `float64(amountLeft)/precision` recomputes a display float; (3) Typesense projection is a lossy read model (see III.14).

### III.6 Transaction boundaries & the real commit point
- **Atomic unit:** the balance write (`UpdateBalances`) and the transaction-row insert (`RecordTransaction`) are issued as **separate datasource calls** in the observed code — not a single DB transaction. Balances are written first.
- **Real commit point:** the moment `updateBalances` durably persists the new balances in the worker. After that the money has moved even if the row insert or webhook later fails.
- **Webhook before durability:** yes — `postTransactionActions` fires asynchronously and is not ordered after a single enclosing commit, so a webhook can precede/contradict durable state.

### III.7 Ordering & time
Ordering is per-application-processing-order, serialised per balance by the lock, not by `effective_date`. `created_at` is wall-clock at enqueue (`time.Now()` in `setTransactionMetadata`). Backdated inserts apply to the *current* running balance; historical/`/at?timestamp=` queries and reconstruction use `effective_date`. **A backdated transaction inserted after later ones does not rewrite history or recompute intervening balances at runtime** — the running balance simply moves now, and the hash chain (if enabled) seals rows in chain sequence, so reordering by effective date is not reflected in the chain. This is the ledger-correctness hazard Volume I flagged: for interest/statement purposes the reader must reconstruct, not trust the live running total.

### III.8 Concurrency at the contention point
Lock scope: per **source balance** (historic) / per-inflight-transaction key (v0.15.x commit), with a default lock duration of 1800 seconds. Deadlock across two balances: the single-key-on-source design means a transaction acquires **one** lock, so classic two-lock deadlock is largely avoided — at the cost of not locking the destination. Hot pooled contribution account (the reader's case): with `skip_queue` it throws `Failed to acquire lock` after the 3-second lock wait; the intended path is the queue, where **coalescing** groups same source+destination+currency work and **hot-lane routing** isolates the hot pair, then optimistic `version` rejects stale writes for retry. Starvation/fairness: asynq gives 20 weighted queues with up to 10 workers; a persistently hot balance can still back up (hence the v0.15.2 `503 QUEUE_BACKPRESSURE`).

### III.9 Idempotency model
Key = caller `reference`, scope = whole ledger, persisted as a unique index, retained for life of the row. Payload-mismatch on a reused reference is **not** reconciled — first write wins, duplicate discarded. Blnk's idempotency blog states verbatim: *"If your app retries with the same reference, Blnk discards the duplicate silently. Alex's balance only moves once, and your ledger stays correct."* Concurrent identical requests: both may pass `validateTxn`; the unique index turns the loser into an **error the caller must interpret**, not a clean success echo. **Exactly-once effect** (balance moves once) is delivered by the index; **exactly-once delivery** (of the API/webhook acknowledgement) is NOT — retries and duplicate webhooks are the caller's responsibility. Rejected vs discarded: REJECTED is stored (insufficient funds etc.); discarded (duplicate/zero) is not. Blnk's guidance for correct retries is explicit: *"Create the reference before any retry logic runs. Build it before you enter the retry loop. If you create it inside the loop, every attempt gets a fresh reference, and Blnk has no way to know they're the same operation."*

### III.10 Events & asynchrony
Main path: `SendWebhook` from a goroutine, no outbox, no transactional coupling, at-most-once-ish with best-effort `NotifyError`. Lineage path: `lineage_outbox.go` (durable outbox) — so the project *knows* the pattern but has not applied it to core webhooks. Ordering across webhooks is not guaranteed; dead-letter/replay for core webhooks is absent on the observed path (asynq's own max-retries 3 / retry-delay 5s governs redelivery of the webhook *task*, not durability against a lost emit).

### III.11 PARTIAL-SUCCESS MATRIX

| Scenario | Effects that persist | System knows? | Auto-heal? | Time-to-notice |
|---|---|---|---|---|
| Multi-dest split, one leg fails | Successful legs persist unless `atomic:true`; with `atomic:true` Blnk "rolls back the entire split" | Only via atomic flag | No (non-atomic) | Until reconciliation |
| Bulk `atomic:false`, some fail | Succeeded entries committed, failed skipped | Partially (per-entry result) | No | Immediate per-entry, but no global rollback |
| Committed to PG, webhook never delivers | Balance moved, row APPLIED, downstream never told | No | No | Until external reconciliation |
| PG write ok, Typesense projection fails | Ledger correct, search stale/missing | pg-listener may log | Eventually (re-index) | Search-only impact |
| Inflight commit updates one balance, fails on other | Possible one-sided balance move (two separate writes) | No | No | Until reconstruction |
| Worker crash after balance update, before APPLIED insert | **Balances moved, no APPLIED row** | No | Queue recovery re-drives the QUEUED parent → risk of double-apply if original balance write already landed | Until reconstruction/audit |

The worker-crash-mid-operation row is the most dangerous: it is a durable, silent, one-sided state, and queue recovery keys off the still-`QUEUED` parent. On the atomic-split guarantee, Blnk's own blog is explicit: *"`atomic: true` means the split succeeds completely or fails completely. If one destination fails, Blnk rolls back the entire split."*

### III.12 Failure matrix — durable end-state

| Failure | Durable DB end-state |
|---|---|
| Validation error | Nothing written (discarded) or REJECTED row |
| Redis unavailable at enqueue | Enqueue fails, `NotifyError`, no txn recorded; caller gets error |
| Redis unavailable mid-op (lock) | `Failed to acquire lock`; balances untouched |
| Postgres unavailable at `updateBalances` | Balances not moved; txn stays QUEUED for recovery |
| Postgres unavailable at `persistTransaction` (after balance write) | **Balances moved, no APPLIED row** |
| API process crash pre-enqueue | Nothing persisted; caller must retry (same reference safe) |
| Worker crash mid-op | See III.11 |
| Response loss (ambiguous timeout) | Effect may or may not have happened; safe retry only via same reference (idempotency) |
| Concurrent version conflict | Stale write rejected; retry |
| Queue backpressure (v0.15.2) | `503 QUEUE_BACKPRESSURE`, nothing enqueued |

### III.13 Recovery & reconciliation
`queue_recovery.go` / `POST /transactions/recover?threshold=` (min 2m, default auto since v0.13.2) scans for transactions stuck in `QUEUED` past the threshold and **re-enqueues** them. Re-driving a transaction whose balance write already succeeded but whose row insert failed **can double-apply** if the worker cannot detect the prior balance mutation — the reference index protects against a duplicate *row*, but a re-driven QUEUED parent generates its own APPLIED child. Self-healing: stuck-queue re-drive, inflight-expiry auto-void. Operator-required: balance reconstruction (`from_source=true` / `BLNK_RUN_RECONCILIATION`), which recomputes from transactions and records `difference` in metadata **without a confirmed automatic alert** — a reconstructed balance can silently differ from the stored balance and only a human reading the metadata would know.

### III.14 Read paths & staleness
Primary reads hit Postgres cached balances (authoritative). Between enqueue and apply, the balance does **not** reflect the pending transaction in `balance`; instead `queued_credit_balance`/`queued_debit_balance` (v0.8.3) expose the pending estimate separately, and available balance = `balance - inflight_debit_balance`. **A caller could act on a queued estimate as though committed** — the estimate is explicitly labelled but nothing prevents misuse, and the gap persists for the full queue latency (unbounded under backpressure). Typesense is an eventually-consistent projection via `pg-listener`; its staleness bound is incidental, not guaranteed. Historical balances via `/balances/{id}/at?timestamp=`.

### III.15 Mutation, deletion, immutability
Transactions: append-only; protected fields guarded by DB immutability trigger + hash; `description`/`meta_data` mutable. Balances: mutable running totals (by design). Identities: became **deletable** in v0.15.0 (`DeleteIdentity`). Deleting an identity attached to a balance: the balance and its transaction history persist (identity link is a reference); the hash chain — which does not fingerprint identity — is unaffected. "Deletion" for transactions is effectively not offered; for identities it is real deletion of the identity record.

### III.16 Falsification watch
- **Target 1 (authoritative money as float64 on the write path):** **PARTIALLY CONFIRMED as a latent hazard.** `setTransactionMetadata` computes `PreciseAmount = int64(Amount * Precision)` — a float64 multiply on the write path when the caller supplies `amount`. `CommitInflightTransaction` took `amount float64` in the fork (now `*big.Int` in v0.15.x). Authoritative storage is integer, but the *conversion* touches float. **This does not falsify Volume I's integer-storage claim, but it qualifies it: the ingress is float-lossy unless the caller sends `precise_amount`.** Volume I's precision claim should be annotated accordingly.
- **Target 2 (mutation of a posted txn's financial fields vs new parent-linked row):** **NOT FOUND / model survives.** `finalizeCommitment` and `finalizeVoidTransaction` always mint a new `TransactionID`/`Reference` and set `ParentTransaction`; the immutability trigger guards protected fields. Immutability holds.
- **Target 4 (destination credit ≠ source debit in v0.15.0+):** **NOT FOUND / model survives.** A single `precise_amount` drives both legs via `model.UpdateBalances`; there is no code path that credits a different amount than it debits. Conservation holds at runtime.

### III.17 Build-extraction verdicts
- **Queue-by-default + eventual-consistency contract — ADOPT (with caller discipline).** Works because of the queue *and* the caller treating QUEUED as non-final. For a savings cooperative, ADOPT but expose settlement status to members only on APPLIED webhooks/polls, never on 201.
- **Redis distributed lock as serialiser — ADAPT.** It works largely because of the deployment (single logical Redis, hot pairs isolated by routing) rather than the mechanism's completeness. **Change:** lock on an ordered pair {source,destination} (or both balances) to close the destination-collision gap, or rely on `version` + retry as the primary guarantee and treat the lock as optimisation.
- **Optimistic `version` — ADOPT.** Correct and environment-independent; make retry counts/limits explicit and surface conflicts to callers.
- **Inflight two-phase model — ADOPT.** Clean commit/void with parent linkage; partial commit supported.
- **`_q` suffix convention — ADOPT.** Does not harm idempotency; keep the caller-reference check ahead of enqueue.
- **Queued-balance-estimate exposure — ADAPT.** Rename/relabel and gate in the API so a queued estimate can never be mistaken for available funds; for members' savings this must be UI-enforced.
- **Webhook without outbox — REJECT (for a money system).** **Change:** add a transactional outbox to the core transaction path (the project already has `lineage_outbox.go` to copy).
- **Two-write (balance then row) non-atomic commit — ADAPT/REJECT.** **Change:** wrap balance update and transaction insert in one DB transaction, or make the worker idempotent against its own partial completion before enabling queue recovery in production.

### III.18 Reconstruction — answers to the volume's closing questions
- **Real commit point:** the worker's durable `updateBalances`, not the API response.
- **Authoritative state:** the Postgres cached balance row (with `version`); Redis is on the correctness path but is queue+lock, not the record; Typesense is a projection.
- **Structural vs convention:** structural = conservation (INV-1), integer storage (INV-7), unique-reference index (INV-4), immutability trigger (INV-5/11 protected fields). Convention/check-only = sufficient funds (INV-8), concurrency (INV-9), zero/malformed (INV-10), tenancy (INV-12).
- **Ambiguous timeout + retry:** safe *only* if the caller reuses the same reference; the index/validate then makes the retry a no-op or a clean error. Any new reference double-applies.
- **Half-success:** the balance-then-row ordering and outbox-less webhook mean half-success leaves durable, silent, one-sided state; reconciliation/reconstruction is the only cure and it does not alert.
- **Where races occur:** `validateTxn` TOCTOU; destination balance under source-only lock; queued-estimate reads; queue-recovery re-drive vs partial completion.
- **Hardest operation to make correct:** the inflight partial commit under concurrency touching two balances via two separate writes — most legs, most state, least atomicity.
- **Runtime mechanism that most defines Blnk:** queue-by-default asynchronous processing with a Redis-lock-serialised, optimistically-versioned balance mutation.

### Ten most important findings (ranked)
1. The real commit point is the worker's durable balance write, not the API response — QUEUED ≠ settled.
2. Balance write and transaction-row insert are two separate writes, balance first — a crash between them leaves durable one-sided state.
3. Core webhooks have no outbox; they can fire before durability or be lost.
4. Idempotency is a TOCTOU pre-check saved only by the unique index; the caller gets an error, not a clean echo, on a concurrent duplicate.
5. The Redis lock is keyed on source only; destination collisions rely on optimistic `version` alone.
6. Float ingress (`int64(amount*precision)`) is lossy; send `precise_amount` as an integer/`*big.Int`.
7. Backdated transactions move the running balance now and do not recompute history; correctness needs reconstruction.
8. Balance reconstruction records a `difference` but does not alert — silent drift is possible.
9. Queue recovery re-drives QUEUED parents and can double-apply after a partial completion.
10. Tenancy (INV-12) is owned by no component; scoped keys gate verbs, not tenants.

## Recommendations
1. **Treat 201/QUEUED as "accepted", settle on APPLIED.** Build member-facing balances off APPLIED webhooks or polled status, never the create response. Benchmark to change: if you enable `skip_queue` for a low-traffic reserve balance, you may treat its synchronous 200 as settled.
2. **Do not expose queued/estimated balances as spendable.** Gate `queued_*` fields server-side. Threshold: only relax if you add hard available-funds checks at spend time.
3. **Send `precise_amount` as an integer/`*big.Int`, never `amount` float.** Eliminates the float-truncation ingress. This is mandatory for members' savings. Also generate each transaction `reference` before the retry loop, not inside it.
4. **Before production: wrap balance-write + row-insert in one DB transaction, and add a core webhook outbox.** Until then, run scheduled balance reconstruction and alert on any non-zero `difference` yourself — Blnk will not.
5. **Close the lock gap on hot pooled accounts.** Either always queue (never `skip_queue`) for contribution accounts, or patch the lock to cover both balances. Benchmark: if `blnk_chain_lag`/queue backlog or `503 QUEUE_BACKPRESSURE` appears, you are at the contention limit.
6. **Enable the global hash chain (`BLNK_TRANSACTION_HASHCHAIN_ENABLED=true`) and schedule `blnk verify-chain`.** It is off by default; for members' money, tamper-evidence should be on.
7. **Build tenancy yourself.** Scoped keys gate verbs, not tenants; enforce per-cooperative isolation in your application layer.

## Caveats
- **`precise_amount` / balance PostgreSQL column type: UNKNOWN.** The embedded `sql/` DDL could not be retrieved by any automated route (GitHub blob/raw blocked by robots; not indexed by search; CDN/sourcegraph not reachable by the tools available). `*big.Int` + string-JSON serialization of balance fields (e.g. `"balance":"40000"`) + the v0.10.1 changelog claim of support for amounts "larger than 15 digits" strongly imply an unbounded `NUMERIC` column in current Blnk; the Aug-2024 `northstar-pay/nucleus` fork used Go `int64` for these fields (implying `BIGINT` at that time). We report NUMERIC as SOURCE-CODE INFERENCE only and correct no earlier volume. To confirm, clone the repo and read `sql/*.sql` plus the `UpdateBalances` SQL directly, or use an authenticated GitHub API call / jsDelivr CDN mirror.
- **Version drift in code reads.** The fully-readable source is the Aug-2024 `northstar-pay/nucleus` fork (a public Apache-2.0 fork of `blnkfinance/blnk`); v0.15.x specifics (big.Int, per-txn inflight lock, coalescing, hot-lane, backpressure, hash chain, immutability trigger, queued inflight commit/void) are corroborated from v0.15.x docs and SDK notes, but individual v0.15.x function bodies (e.g., whether balance+row are now wrapped in one DB transaction) are SOURCE-CODE INFERENCE where marked. If v0.15.x already wraps the two writes atomically, Findings 2–3 and the worst partial-success rows soften — verify against the current `transaction.go` before building.
- **Issue-tracker evidence is thin.** The GitHub issue listing was reachable but individual runtime bug reports (duplicate/stuck/drift) were not retrievable in detail; the partial-success and double-apply hazards are derived from code structure and documented recovery behaviour, not from a confirmed production incident report.
- Blog/README claims are treated as MAINTAINER CLAIM throughout; documentation-vs-source divergences (float ingress vs "integer minor units" marketing; webhook "immutability/idempotency" advice that pushes responsibility to the caller) are reported as findings, not smoothed over.