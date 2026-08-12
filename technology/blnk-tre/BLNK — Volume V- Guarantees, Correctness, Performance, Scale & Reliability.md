# BLNK — Volume V: Guarantees, Correctness, Performance, Scale & Reliability

```
Technology:              Blnk — open-source double-entry financial ledger
Technology type:         LEDGER
Primary repository:      https://github.com/blnkfinance/blnk
Version / release:       v0.15.2 (31 July 2026) — supersedes v0.15.0 where they differ
Source openness:         OPEN SOURCE — Apache-2.0 ("Blnk Core")
Research date:           11 August 2026
Study objective:         BUILD EXTRACTION
Configuration:           EXTENDED 7 (Volume VII — Security & Threat Model — commissioned separately)
Volume V question:       What does Blnk genuinely guarantee, and under what conditions do the guarantees hold?
```

---

## TL;DR

- **Strongest guarantee: per-transaction atomicity and value conservation on the main (queued) write path.** Since Volume IV confirmed the single composite datasource write `RecordTransactionWithBalancesAndOutbox(...)` ("persisted atomically"), a posted transaction either moves both balances and records the row, or neither. This is *structural* and CONFIRMED IMPLEMENTATION. **Weakest guarantee: read-your-writes / freshness on the default path (not guaranteed) and tenancy + resource isolation (not enforced at all).** Because the API returns `QUEUED` before money moves, a caller has no guarantee that a subsequent read reflects the transaction until a worker commits — and one noisy cooperative can starve another because there is no per-tenant QoS.
- **Primary scaling bottleneck: the single hot destination balance.** A pooled cooperative contribution account (many members → one account) is a hot balance *by construction*. Every writer to it must acquire the same Redis lock (`internal/redlock` MultiLocker) and pass an optimistic version check; they serialise. **Adding workers does not speed up a contended balance and can worsen contention/retries.** The documented remedies — queueing, coalescing, hot-lane routing, and above all *balance sharding* — manage the symptom; only sharding removes the bottleneck.
- **After saturation Blnk sheds load rather than collapsing.** Since v0.15.2, when Redis memory or pending-task count exceeds limits, new enqueues are rejected with **HTTP 503 / `error_detail.code = QUEUE_BACKPRESSURE`** (backpressure enabled by default). Work already accepted into Redis is retained and drained; nothing already committed is lost. The exposure is that the queue and locks live in Redis, so a Redis loss without persistence loses queued-but-undrained work. **The single most important finding for a savings ledger: a silent balance drift would NOT automatically raise an alarm** — correctness detection (balance reconstruction, hash-chain verification) is entirely opt-in and off by default.

---

## Key Findings

1. **Atomicity is the load-bearing guarantee and it now holds structurally.** Volume III's two-write partial-success hazard is gone: balances are mutated in memory then persisted through one datasource call the source comments describe as *"persisted atomically."* This is the reader's single best reason to trust Blnk with money.

2. **The "up to about 5×" performance claim is a MAINTAINER CLAIM, not a measurement.** The v0.14.0 changelog (Apr 9 2026) states verbatim: *"In internal benchmarks under heavy contention and burst load, processing throughput improved by up to about 5×; your results depend on workload shape, how much traffic overlaps on the same balances, and how you configure the server."* No hardware, dataset size, concurrency level, or measured metric (TPS? p99?) is stated. It fails the volume's stated-conditions test and must be treated as marketing, not evidence.

3. **The money column type remains PERMANENTLY UNKNOWN.** After four volumes and a dedicated extraction subagent, the PostgreSQL DDL in `database/balance.go`, `database/transaction.go`, and `sql/` could not be read (GitHub blob/raw fetches blocked by robots; code-search hits never surfaced). This is now declared permanently unknown for the study. **Consequence for the reader: the representable range of a balance cannot be confirmed.** If the column is `BIGINT`, there is a silent truncation boundary at ±(2⁶³−1) ≈ ±9.22×10¹⁸ minor units that `*big.Int` in Go cannot rescue at the storage layer; if `NUMERIC`, the range is effectively unbounded for financial use. Documentary evidence (docs: *"Balance fields are integers in minor units"*; the `precise_amount` field exists specifically to *"record amounts exceeding 15 digits"* — example `precise_amount: 189207535698279000, precision: 1000000000000000000` for ETH; `precise_amount` handled as a *string* in test mocks) leans toward `NUMERIC`, but this is ANALYTICAL INFERENCE, not confirmed.

4. **Idempotency is defence-in-depth and its storage-layer anchor is named.** The v0.13.2 changelog confirms a unique database index `idx_transactions_reference_unique` on `transactions.reference`. The application `validateTxn` SELECT-then-check is an optimisation over a TOCTOU window; the *real* guarantee is the PostgreSQL `23505` unique-violation caught by `IsDuplicateReferenceError`. Duplicate references are rejected structurally.

5. **Concurrency safety on a single balance is enforced by check, in three layers, none of which is the database transaction isolation level.** Redis distributed lock (serialise) → lock-wait-timeout (absorb brief contention) → optimistic version check on the balance (reject stale writes at write time). The blog states verbatim: *"Blnk still performs an optimistic version check when writing the balance… The version check provides the final database-level protection by rejecting a write if the balance changed after it was read."*

6. **The lock TTL is long enough to be a real correctness risk.** Default `lock_duration` is **1800 seconds**. If a lock expires mid-operation (worker stall, GC pause, slow DB), the *only* serialisation is gone and two writers can proceed concurrently; the optimistic version check is then the last defence against a lost update. v0.15.1 explicitly fixed *"an overflow bug when applying `BLNK_TRANSACTION_LOCK_DURATION`"* — evidence this parameter has been fragile.

7. **Load-shedding is graceful and default-on.** `QUEUE_BACKPRESSURE` (HTTP 503) is the deliberate mechanism, confirmed in the v0.15.2 changelog. Bounded concurrency (`asyncBulkSemaphore=100`, `asyncTxnSemaphore=20`, `balanceMonitorSem=32`) prevents unbounded fan-out inside a node.

8. **Correctness observability is opt-in and would miss a silent drift.** OpenTelemetry/Jaeger/Prometheus cover *availability* and latency; `CountUnchainedTransactions` and `HotpairsContentionTotal` are emitted. But the two instruments that detect a *correctness* failure — balance reconstruction (`BLNK_RUN_RECONCILIATION`) and the hash chain (`verify-chain`) — are manual and off by default. Nothing in the default deployment continuously compares a stored balance against the sum of its transaction history.

9. **Retry amplification is a live risk.** Retries exist at the SDK layer (`WithRetry`), the asynq queue layer, and the application layer simultaneously. Stacked, they can multiply load against an already-contended balance rather than absorbing a transient fault. The documented reconciliation defaults (`max_retries: 3`, `retry_delay: 5`) illustrate the pattern; transaction-queue retry defaults were not independently verifiable.

10. **Durability in the OSS build rests on assumptions Blnk does not itself verify.** Backup is a `pg_dump`→S3 cron calling the `/backup-s3` endpoint, restored with `pg_restore`. There is no built-in WAL archiving / point-in-time recovery in Core; that is a PostgreSQL responsibility the operator must configure. Worst permitted loss is bounded by backup cadence (a daily cron ⇒ up to ~24h RPO) plus any queued-but-undrained Redis work lost on a Redis failure.

---

## Details

### V.1 — The Guarantee Ledger (ranked)

For each guarantee: statement · holds when · fails when · enforcement (structurally / by check / by convention / not enforced, per Volume III, updated for Volume IV) · evidence class.

| Rank | Guarantee | Holds when | Fails / does not hold when | Enforcement | Evidence |
|---|---|---|---|---|---|
| **1 (strongest)** | **Atomicity + conservation** — a posted transaction moves both balances and records the row, or neither; debits equal credits | Main path, single composite write `RecordTransactionWithBalancesAndOutbox` | Multi-leg/bulk flows split across commits; crash *before* the composite write leaves the txn `QUEUED` (see V.16) | **Structurally** (single datasource call, "persisted atomically") | CONFIRMED IMPLEMENTATION (Vol IV) |
| 2 | **Immutability** of posted transactions | Whatever DB protection exists is active | If enforced only in app code and DB is written directly | **By DB protection** (v0.10.1 added "database protections to prevent unauthorized changes to transactions"); trigger definition **UNKNOWN** | DOCUMENTED BEHAVIOR; trigger UNKNOWN |
| 3 | **Idempotency** — a unique `reference` applies once | `reference` supplied and unique | Caller reuses `_q`-suffixed refs carelessly; pre-v0.13.2 deployments | **Structurally** — unique index `idx_transactions_reference_unique` + PG `23505` | CONFIRMED / DOCUMENTED |
| 4 | **Precision integrity** — no float loss in Go | All arithmetic in `*big.Int` | *Storage* range unknown (see V.3); inconsistent per-currency `precision` supplied by caller | **Structurally in Go**; storage **UNKNOWN** | CONFIRMED (Go) / UNKNOWN (DDL) |
| 5 | **Concurrency safety** on one balance | Queue used; lock acquired; version unchanged | Lock lost/expired mid-op (1800s TTL); `skip_queue:true` under contention → "Failed to acquire lock" | **By check** — Redis lock + optimistic version | DOCUMENTED / SOURCE-CODE INFERENCE |
| 6 | **Sufficient funds** unless overdraft | Overdraft not enabled; inflight included (v0.11.0) | `allow_overdraft:true`; TOCTOU if lock lost | **By check** | DOCUMENTED |
| 7 | **Zero / malformed rejected** | Standard path | — (zero-amount dropped before persistence; non-integer precision rejected v0.11.3) | **By check** | CONFIRMED (Vol IV) |
| 8 | **Tamper-evidence** (hash chain) | Chain *enabled* and verified | **Off by default**; lag if `ChainProcessor` stalls | **By convention** (opt-in) | CONFIRMED (Vol IV) |
| **9 (weakest)** | **Consistency / read-your-writes** and **tenancy + resource isolation** | Read-your-writes only with `skip_queue:true`; tenancy only via ledger partition + API-key scope | Default queued path: read after `QUEUED` may not reflect the write; **no per-tenant QoS at all** | **Not guaranteed / not enforced** | DOCUMENTED / ANALYTICAL |

**Ranking rationale.** Blnk is marketed on its strongest properties — "immutable, correct, double-entry" — and those largely hold. It is most likely to be *broken through* its weakest: a caller who assumes read-your-writes on the default queued path, or an operator who assumes tenant isolation that does not exist. For a cooperative ledger, the practical danger is not that a transaction is lost, but that a balance read looks wrong for a window, or that one society's bulk import degrades another's live contributions.

### V.2 — Correctness specification (invariants as assertable conditions)

- **INV-1 Conservation:** for every applied txn, `Δsource + Δdestination = 0` in minor units. *Structural.*
- **INV-2 Balances change only via transactions:** no API mutates a balance amount directly; `CreateBalance` starts at 0. *Structural / by check.*
- **INV-3 Derivability:** `balance = Σ(credits) − Σ(debits)` reconstructable from history (`from_source=true`, `BLNK_RUN_RECONCILIATION`). *Structural but only checked on demand.*
- **INV-4 Idempotency:** `COUNT(*) WHERE reference = X ≤ 1`. *Structural (unique index + 23505).*
- **INV-5 Immutability:** an UPDATE/DELETE on an applied txn is rejected. *By DB protection; exact trigger UNKNOWN.*
- **INV-6 Valid transitions:** `QUEUED→APPLIED|REJECTED`, `INFLIGHT→APPLIED|VOID`; no back-transition. *By check.*
- **INV-7 Precision integrity:** amounts stored as integers in minor units; Go arithmetic in `*big.Int`. *Structural in Go; storage range UNKNOWN.*
- **INV-8 Sufficient funds:** `source.balance − amount ≥ −overdraft_limit` unless `allow_overdraft`. Inflight included since v0.11.0. *By check.*
- **INV-9 Concurrency safety:** concurrent writers to one balance serialise; `version` monotonic. *By check.*
- **INV-10 Zero/malformed rejected:** zero-amount dropped; non-integer precision rejected. *By check.*
- **INV-11 Tamper-evidence:** `ComputeChainHash(prev, txn) = stored hash`. *By convention (opt-in).*
- **INV-12 Authorisation/tenancy:** API-key scopes + ledger partitioning only. *By check for authz; tenancy not enforced.*

### V.3 — Numerical and precision semantics

Money is `*big.Int` end-to-end in Go (the lossy `int64(Amount × Precision)` float multiply from the 2024 fork is gone). `precision` converts display units to minor units (e.g. 100 for USD → cents); `precise_amount` exists to carry values *"exceeding 15 digits"* (docs; e.g. `precise_amount: 189207535698279000, precision: 1000000000000000000` for ETH). Balance responses return integers in minor units — docs state verbatim *"Balance fields are integers in minor units"* with `display_amount = balance / precision`.

**Rounding:** distribution across multiple sources/destinations uses rounding support (v0.8.1); `precise_distribution` (v0.12.2) allows exact splits, indicating the default path can round split remainders. Direction of rounding is not documented precisely — treat as UNKNOWN and use `precise_distribution` where exactness matters.

**Inconsistent precision for the same currency:** `precision` is a *per-transaction* parameter applied to the balance. If a caller supplies different `precision` values for the same currency across transactions, the minor-unit interpretation of that balance becomes ambiguous — Blnk does not enforce a single canonical precision per currency. *Caller discipline required.* This is a real hazard for a cooperative mixing, say, `100` and `1000` for the same currency.

**Representable range — the practical consequence of the unresolved DDL:**
- If the balance columns are **NUMERIC**: range is effectively unbounded; `*big.Int` and storage agree. (Documentary evidence leans this way.)
- If they are **BIGINT**: a silent truncation/overflow boundary exists at **±(2⁶³−1) ≈ ±9,223,372,036,854,775,807 minor units** (~±9.22×10¹⁸). At `precision = 10¹⁸` (ETH-style), that is only ~9.2 whole units — a real risk for high-precision assets. Go's `*big.Int` would compute correctly but the write could overflow/truncate at the column.

**Verdict (stated as a range with caveat, as required):** the representable balance range is **either effectively unbounded (NUMERIC) or ±~9.22×10¹⁸ minor units (BIGINT)** and *cannot be resolved from available sources*. A reader building a cooperative ledger in a low-precision fiat currency (USD `precision=100`) is safe under either type up to ~$9.2×10¹⁶ — far beyond any cooperative. A reader handling crypto or very high `precision` **must confirm the column type in their own deployment before trusting large balances.**

### V.4 — Consistency guarantees (in caller terms)

- **Default (queued) path:** the API returns `QUEUED` with a `_q`-suffixed reference *before money moves*. **There is no read-your-writes guarantee.** A read immediately after `QUEUED` may show the pre-transaction balance (queued balances are surfaced separately via `queued_credit_balance` / `queued_debit_balance` and `?with_queued=true`, precisely because the applied balance is not yet updated). The real commit is inside the worker.
- **How long until visible:** bounded by queue drain time, which under contention is bounded by lock-wait + processing per predecessor — i.e. *not a fixed SLA*; it is workload-dependent. A caller must poll `GET /transactions/reference/{ref}_q` or the transaction ID until `status = APPLIED`, or subscribe to the state-change webhook.
- **`skip_queue:true`:** synchronous apply ⇒ read-after-write within the same request path, at the cost of exposing lock-contention failures directly to the caller.
- **Stale reads / replication:** Blnk is single-source-of-truth PostgreSQL; if the operator runs read replicas, replica lag introduces additional staleness Blnk does not manage. Session consistency is not offered.

**Caller rule:** *treat `QUEUED` as "accepted, not yet true." Never render a balance to a member from a read taken immediately after posting; poll for `APPLIED` or use the webhook.*

### V.5 — Atomicity and isolation

- **Scope:** one composite datasource write per transaction ("persisted atomically"); the `BeginTx/Commit/Rollback` envelope was inferred, not read (Vol IV).
- **Serialisation point:** the Redis `MultiLocker` over `[sourceBalanceID, destinationBalanceID]`, deduped when source==destination and **lexicographically sorted** to prevent deadlock. Inflight commits use `inflight-commit:<txnID>`.
- **Isolation level inside the composite write: UNKNOWN.** This matters: if Blnk uses PostgreSQL's default **READ COMMITTED** (likely, since it relies on the Redis lock + optimistic `version` for correctness rather than DB isolation), then the DB alone permits lost updates and read/write skew — the Redis lock is doing the serialisation work. That is safe *while the lock holds*.
- **What the lock actually guarantees:** mutual exclusion over the *pair* of balances, in a global lexicographic order, so no path that uses `MultiLocker` can deadlock with another. The residual risk is any code path that acquires balance locks *outside* the MultiLocker ordering — not observed in extracted source, but not exhaustively proven (test coverage of MultiLocker ordering is UNKNOWN, per Vol IV).
- **Anomalies prevented (lock held):** lost update, write skew, double-spend on a single balance.
- **Anomalies that remain possible:** (a) **lost update if the lock expires mid-operation** (1800s TTL) — then only the optimistic `version` check protects; if the stale writer's version check also races, a lost update is theoretically possible; (b) **read skew / phantoms across multiple balances** read outside a single locked scope (e.g. reporting queries); (c) staleness on the queued path (V.4).

### V.6 — Concurrency under stress (at the contention point, not the average)

The reader's pooled contribution account is an **N→A hot destination** by construction. Behaviour by writer count against one destination:

- **~10 concurrent writers:** queue absorbs them; workers serialise on the destination lock; each waits briefly (lock-wait-timeout, default 3s). Latency to `APPLIED` rises modestly; failures rare. Caller sees `QUEUED` immediately, `APPLIED` shortly after.
- **~100 concurrent writers:** lock queue depth grows; without coalescing, 100 sequential read-lock-write cycles on one balance. **Coalescing** (v0.14+, `BLNK_TRANSACTION_ENABLE_COALESCING`) batches transactions sharing source+destination+currency into one commit, collapsing repeated lookups/commits — highly effective for N→A into one account. **Hot-lane routing** (v0.14+) may activate if this pair shows repeated contention, isolating it from the rest of the queue (`HotpairsContentionTotal` metric increments). Some `skip_queue:true` callers would see "Failed to acquire lock."
- **~1000 concurrent writers:** the single balance is the hard ceiling. Coalescing + hot lane keep it *correct and moving* but throughput on that one balance is bounded by serial commit rate. If Redis memory/pending-task limits are hit, `QUEUE_BACKPRESSURE` (503) sheds new enqueues. The documented, and only real, fix is **balance sharding** (`@Treasury-0..19`), turning one bottleneck into N parallel lanes; the cooperative must then aggregate shards for reporting.

**Fairness/starvation:** the lock is not a fair queue; under sustained contention, no ordering guarantee among waiters. Coalescing changes *which* transactions batch together, not fairness. A relentless hot pair can starve if not hot-lane-isolated.

### V.7 — Latency decomposition (QUEUED vs APPLIED are different numbers)

**API-visible latency (to `QUEUED`)** — the fast path:
parse → authenticate (API-key hash lookup) → validate (incl. `validateTxn` SELECT on reference) → enqueue to Redis. Dominated by the reference-existence SELECT and the Redis enqueue; typically low and roughly flat with load until backpressure.

**End-to-end latency (to `APPLIED`)** — the meaningful number for a member seeing their contribution land:
queue wait (dominant under contention) → lock acquisition (up to lock-wait-timeout) → balance read (`GetBalanceByID` or faster `GetBalanceByIDLite` when `EnableQueuedChecks` off) → in-memory computation (negligible, `big.Int`) → the atomic composite write (DB round-trip, the dominant *fixed* cost) → post-commit side effects (lineage outbox on the write path; **webhooks fire from a detached goroutine, off the critical path and without an outbox**).

- **Low load:** end-to-end ≈ enqueue + one worker pickup + one DB write. The atomic write dominates.
- **p99 under contention on a hot balance:** **queue wait dominates** — it scales with the number of predecessors holding/awaiting the same lock. This is where coalescing pays off (amortises the DB write across a batch).

### V.8 — Throughput model

- **Unit:** applied transactions/second. Coalescing means *ledger rows* and *commits* decouple (many rows, one commit).
- **Single-node capacity:** bounded by (a) worker concurrency (`max_workers` default 10) × per-txn DB write time for *distinct* balances, and (b) serial commit rate for any *single* hot balance.
- **Scale-out:** more workers/nodes help *only for uncontended, distinct balances*. On one hot balance, more workers do **not** help and increase lock churn/retries.
- **Saturation point:** reached first at a single hot balance, or when Redis memory/pending-task limits trip.
- **Post-saturation behaviour: graceful degradation, not collapse.** `QUEUE_BACKPRESSURE` (HTTP 503, default-on since v0.15.2) sheds *new* enqueues when *"Redis memory usage or pending task count exceeds configured limits."* Already-enqueued work is retained and drained. Callers see 503 and must retry with backoff. Nothing accepted is lost — *unless Redis itself is lost* (V.16).
- **The 5× claim, tested:** MAINTAINER CLAIM. Verbatim: throughput *"improved by up to about 5×"* in *"internal benchmarks under heavy contention and burst load"* with results *"depend[ing] on workload shape…"* No hardware, dataset, concurrency, or metric. Do not size a deployment from it.

### V.9 — Scalability

- **Vertical:** helps DB write throughput and Redis memory headroom.
- **Horizontal:** stateless workers scale for distinct-balance workloads; PostgreSQL is the shared source of truth and the eventual write bottleneck; Redis is the shared queue+lock and the eventual coordination bottleneck.
- **Partitioning/sharding:** *ledger partitioning* is the tenancy model; *balance sharding* is the application-level scaling lever for hot balances (Blnk provides the pattern, not automation).
- **Replication / multi-region:** not provided by Core; operator-supplied PostgreSQL/Redis concern.
- **Primary bottleneck:** the single hot balance's serial commit rate; secondarily Redis memory. **Adding workers hurts on a contended balance.**

### V.10 — Capacity model (sized for a real cooperative)

**Scenario:** 5,000 members, monthly contributions into one pooled account (N→A), plus occasional loans/withdrawals.

- **Load shape:** ~5,000 txns/month is trivial in aggregate (~2 txns/min average). The risk is *not* volume — it is the **temporal spike** if contributions are collected on the same day (e.g. payday), producing hundreds of near-simultaneous writes to one pooled balance.
- **Sizing:** a single modest node (a few vCPU, a few GB RAM), one small PostgreSQL instance, and a small Redis suffice for steady state. Connection pool: default worker/DB pool limits (raised in v0.15.0) are ample.
- **Storage growth:** roughly one transaction row + hash + metadata per contribution; ~60k rows/year — negligible. Balance snapshots (`TakeBalanceSnapshots`) add periodic rows for historical queries.
- **Where the first limit appears:** the *contribution-day spike on the single pooled account*. Mitigations, in order: enable the queue (default), enable coalescing (same source→pooled account batches beautifully), enable hot-lane routing, and if spikes still saturate, **shard the pooled account** and aggregate for reporting.
- **Redis memory:** must hold the queue depth of the largest spike; size it for peak pending tasks or `QUEUE_BACKPRESSURE` will 503 legitimate contributions during collection day.

### V.11 — Reliability mechanisms and retry-amplification assessment

- **Timeouts:** lock-wait-timeout (default 3s); SDK client timeout (e.g. `WithTimeout`).
- **Retries at three layers:** SDK (`WithRetry`), asynq queue (documented reconciliation defaults `max_retries:3, retry_delay:5`; transaction-queue defaults not independently verified), and application (`insufficient_fund_retries`/`max_retry_attempts`).
- **Health checks:** `/health` endpoint (auth-bypassed since v0.10.4); queue monitoring port (v0.10.3).
- **Graceful shutdown:** v0.13.0 ensures pending transactions finish before stop.
- **Retry-amplification verdict: YES, it can amplify.** Three independent retry layers stacked over a *contended hot balance* can multiply attempts against the exact resource that is already the bottleneck, converting a transient stall into a sustained retry storm. Idempotency (unique reference) prevents *double application*, so retries are *safe for correctness* — but not *safe for load*. **Recommendation:** disable SDK-level retries for write paths that also retry at the queue layer, and rely on exponential backoff + `QUEUE_BACKPRESSURE` for shedding.

### V.12 — Durability and recovery

- **`internal/pg-backups` / `/backup-s3`:** triggers a `pg_dump`-style backup to S3 (configured via `blnk.json` AWS keys), scheduled by the operator via cron; restore is manual `pg_restore`. This is *logical backup*, not continuous archiving.
- **WAL / PITR:** **not built into Core.** Point-in-time recovery is a PostgreSQL responsibility the operator must configure separately (e.g. pgBackRest + WAL archiving). Blnk Cloud advertises automatic backups and a rollback window (Cloud figures could not be verified against a Blnk-owned source and are excluded).
- **Durability assumption Blnk relies on but does not verify:** that the underlying PostgreSQL is configured with adequate `fsync`/`synchronous_commit` and durable storage, and that Redis persistence (AOF/RDB) is configured if queue loss is unacceptable. Blnk *assumes* these; it does not check them.
- **Worst permitted loss:** bounded by backup cadence for committed data (daily cron ⇒ up to ~24h RPO) **plus** any queued-but-undrained transactions in Redis if Redis is lost without persistence. Because idempotency is by reference, a client that safely retries un-acknowledged posts can recover queue loss without double-applying.
- **RPO/RTO:** not specified by Core; operator-defined. Set them explicitly.

### V.13 — Observability and the correctness-detection verdict

- **Available:** OpenTelemetry, Jaeger tracing, Prometheus metrics; remote export via `BLNK_CLOUD_DSN` (v0.14.4, redacted); queue monitoring port; `/health`; structured logs (workflow messages moved to `info` in v0.14.5); `system.error` webhooks (incl. duplicate reference); `HotpairsContentionTotal`; `CountUnchainedTransactions` (chain lag).
- **Detects readily:** availability failures, latency, queue depth, lock contention (via hot-pairs metric), chain lag (*if chain enabled*).
- **The operative test — could an operator detect a CORRECTNESS failure (not availability) from what the system emits?** **Largely NO, by default.**
  - **Silent balance drift** (stored balance ≠ Σ history): would *not* raise an alarm unless the operator runs **balance reconstruction** (`BLNK_RUN_RECONCILIATION=SOURCE` / `from_source=true`) and compares — a manual, on-demand action. No continuous reconstruction-diff alarm exists.
  - **Growing chain lag:** *detectable* via `CountUnchainedTransactions` — but only if the hash chain is enabled (off by default) and the metric is alerted on.
  - **Stuck queue:** detectable via queue depth + `RecoverQueuedTransactions`/`GetStuckQueuedTransactions`, but requires the operator to alert on it.
  - **Reconstruction difference:** surfaced only when explicitly requested.
- **Verdict:** the observability stack is a strong *availability*-detection system and a weak *correctness*-detection system out of the box. **For a ledger holding members' savings this is the most important gap after the guarantee ledger.** A drifted balance can sit unnoticed indefinitely.

### V.14 — Resource isolation and noisy neighbours (performance dimension only)

Volume II established there is **no tenant isolation** beyond ledger partitioning and API-key scoping. Performance consequence: workers, the Redis queue, and the PostgreSQL connection pool are **shared**. If cooperative society A runs a bulk import (up to 10,000 items/request per v0.15.0) while society B is taking live member contributions, A's work competes for the same workers, queue capacity, and DB connections. B's contribution latency rises and, if A's burst pushes Redis to its limits, B's enqueues can be rejected with `QUEUE_BACKPRESSURE` (503) — B is penalised for A's behaviour. There is **no per-tenant rate limit or QoS lane** (global rate-limiting exists since v0.7.0, but it is not tenant-aware). Bulk work should be scheduled off-peak and, ideally, run against a separate Blnk deployment per high-volume tenant. *(Confidentiality/integrity of the shared-tenancy model is deferred to Volume VII.)*

### V.15 — Security (deferred)

This volume's analysis depends on two security-adjacent facts, both deferred to Volume VII for adversarial treatment: (1) idempotency and immutability rest on DB constraints/protections whose *bypassability* is a Volume VII question; (2) the Redis lock is the serialisation primitive, and whether it can be *deliberately* subverted (lock theft, TTL manipulation) is a Volume VII question. Here we only note that correctness under *non-adversarial* conditions depends on them holding.

### V.16 — Failure-scenario matrix

| Scenario | What the system does | State left in | Self-heals? | How operator knows |
|---|---|---|---|---|
| **Crash during composite write** | Single atomic write ⇒ commits or rolls back | Txn stays `QUEUED`; no partial balance | Yes — `RecoverQueuedTransactions` re-drives; idempotency prevents double-apply | Stuck-queued metric; `GetStuckQueuedTransactions` |
| **PostgreSQL failover** | Writes fail until new primary; workers error/retry | Consistent (single source of truth) | Yes, once primary returns; queued work drains | Health check, DB errors, queue backlog |
| **Redis failure + restart with queue loss** | Enqueue fails; in-flight locks lost | **Undrained queued txns lost** if no Redis persistence; committed data intact | Partially — clients must re-post (safe via unique reference) | Queue empty/errors; missing `APPLIED` for posted refs |
| **Redis memory exhaustion** | `QUEUE_BACKPRESSURE` 503 on new enqueues | Existing queue drains; new work shed | Yes, as memory frees | 503/`QUEUE_BACKPRESSURE`; Redis mem metric |
| **Network partition worker↔DB** | Worker cannot commit; retries | Txn `QUEUED`; lock may expire | Yes on reconnect | Worker errors; backlog |
| **Disk exhaustion (DB)** | Commits fail | `QUEUED`; no partial | On disk freed | DB errors; health |
| **Clock skew (effective_date, lock TTL)** | `effective_date` may misorder history; **lock TTL may expire early/late** | Possible mis-ordered reporting; **serialisation window lost if TTL early** | No auto-heal for skew | Hard to detect — no clock-skew alarm |
| **Duplicate task delivery (asynq)** | Second delivery hits unique reference ⇒ `23505` | Single application | Yes — idempotent | `system.error` webhook (duplicate reference) |
| **Partial deployment / mixed versions** | Behaviour differences (e.g. pre/post v0.13.2 unique index; v0.15.0 error schema) | Risk of inconsistent enforcement | No | Migration/version checks |
| **Corrupt data** | Detected only if chain enabled or reconstruction run | May persist silently | No | **Only via opt-in reconstruction/verify-chain** |
| **Hot partition (single balance)** | Serialises; coalescing/hot-lane manage; sharding needed | Correct but slow | Partially | `HotpairsContentionTotal`; latency p99 |
| **Lock TTL expires mid-operation** | Serialisation removed; optimistic `version` becomes sole defence | Correct *iff* version check catches the stale writer; else risk of lost update | Version check usually saves it | Not directly alarmed — inferable from drift if reconstruction run |

### V.17 — Build-extraction verdicts

| Mechanism | Verdict | Environment vs mechanism |
|---|---|---|
| **Atomic composite write** | **ADOPT** | Works because of the *mechanism* (single datasource call). Portable. The single most valuable thing to copy. |
| **`redlock` MultiLocker (sorted, deduped)** | **ADOPT** | Mechanism-driven deadlock-freedom via lexicographic ordering. But it depends on Redis availability and TTL discipline — adopt *with* a short, monitored TTL, not 1800s. |
| **Optimistic version check** | **ADOPT** | Correct last-line defence; cheap. Essential precisely because the DB isolation level is not doing the work. |
| **Coalescing / hot-lane routing** | **ADAPT** | Works because of *workload shape* (repeated same-pair traffic). Great for N→A contributions; useless for dispersed traffic. Adopt only if your workload has hot pairs. |
| **Queue backpressure (503)** | **ADAPT** | Mechanism is sound; thresholds are environment-specific. Adopt with Redis sized for peak. |
| **Hash chain as correctness instrument** | **ADOPT-BUT-ENABLE** | Off by default = not a guarantee. For savings, enable it and alert on `CountUnchainedTransactions`. |
| **Balance snapshots** | **ADOPT** | Enables historical queries and faster reconstruction; storage cost modest. |
| **Observability stack as correctness detector** | **REJECT AS-IS** | Detects availability, not silent drift. Must be *supplemented* with a scheduled reconstruction-diff job that alarms on any `stored ≠ reconstructed`. Without that, the environment (a vigilant operator) is doing the work, not the mechanism. |
| **Long lock TTL (1800s default)** | **REJECT (retune)** | A 1800s TTL turns a stalled worker into a serialisation gap. Set it just above worst-case commit time and monitor. |
| **Stacked SDK+queue+app retries** | **REJECT AS-IS** | Amplifies load on the exact bottleneck. Consolidate to one retry layer with backoff. |

### V.18 — Volume V reconstruction

1. **Guarantee ledger, ranked:** atomicity+conservation (strongest, structural) → immutability → idempotency → precision (Go) → concurrency safety → sufficient funds → zero/malformed → tamper-evidence (opt-in) → consistency/read-your-writes & tenancy/resource isolation (weakest).
2. **Invariant spec:** INV-1..12 restated as assertable conditions (V.2); INV-5/7-storage/isolation-level remain UNKNOWN.
3. **Precision model:** `*big.Int` in Go, integer minor units in storage; representable range = *unbounded (NUMERIC) or ±~9.22×10¹⁸ minor units (BIGINT)* — unresolved; safe for fiat cooperatives, risky for high-precision assets.
4. **Consistency model:** no read-your-writes on the queued default; `skip_queue:true` for synchronous read-after-write; poll for `APPLIED`.
5. **Atomicity/isolation model:** one atomic composite write; Redis MultiLock serialises; DB isolation level UNKNOWN (likely READ COMMITTED, compensated by lock+version); remaining anomalies = lost update if lock expires, cross-balance read skew, queued staleness.
6. **Concurrency at the contention point:** single balance serialises; coalescing/hot-lane help at 100s; sharding required at 1000s; adding workers does not help a hot balance.
7. **Latency model:** QUEUED (fast, ~flat) ≠ APPLIED (queue wait dominates under contention; atomic write dominates at low load).
8. **Throughput model:** unit = applied txns/s; ceiling = single hot balance serial commit rate; post-saturation = graceful shedding via `QUEUE_BACKPRESSURE` 503, no loss unless Redis lost.
9. **Scalability model:** stateless workers scale for distinct balances; primary bottleneck = single hot balance, then Redis memory.
10. **Capacity model:** a 5,000-member cooperative is trivial in aggregate; the first limit is the contribution-day spike on one pooled account; fix with coalescing then sharding; size Redis for peak.
11. **Reliability map:** three retry layers → amplification risk; idempotency keeps retries correctness-safe but not load-safe; consolidate retries.
12. **Durability/recovery:** logical backup to S3 + manual restore; no built-in PITR; worst loss ≈ backup cadence (~24h daily) + Redis queue loss; depends on unverified PG/Redis durability config.
13. **Observability map + correctness verdict:** strong availability detection; **weak correctness detection — silent balance drift would not raise an alarm by default.**
14. **Resource-isolation model:** no per-tenant QoS; a bulk import degrades a neighbour's live contributions and can trigger their 503s.
15. **Failure-scenario matrix:** see V.16 — most scenarios self-heal via idempotent recovery; the un-self-healing ones are corrupt/silent-drift data and clock skew.
16. **Build-extraction verdicts:** ADOPT the atomic write, MultiLock, version check, snapshots; ADAPT coalescing/hot-lane/backpressure; ADOPT-BUT-ENABLE the hash chain; REJECT-as-is the default observability-as-correctness-detector, the 1800s lock TTL, and stacked retries.
17. **Key unknowns:** money column type (NUMERIC vs BIGINT) — **permanently UNKNOWN**; CHECK constraints; immutability trigger definition & violation behaviour; DB isolation level inside the composite write; test coverage of concurrent duplicate references, MultiLock ordering, partial-failure rollback, and the trigger; transaction-queue retry defaults; rounding direction.
18. **Ten most important findings:** see Key Findings above.

**Direct answers to the volume's closing questions:**
- **Strongest guarantee?** Per-transaction atomicity + conservation on the main write path (structural, CONFIRMED).
- **Weakest guarantee?** Read-your-writes on the default queued path (not guaranteed) and tenancy/resource isolation (not enforced).
- **Primary scaling bottleneck?** The single hot destination balance's serial commit rate (then Redis memory).
- **What happens after saturation?** Graceful load-shedding via `QUEUE_BACKPRESSURE` (HTTP 503, default-on); accepted work is retained and drained; nothing committed is lost unless Redis itself is lost.
- **Could an operator detect a correctness failure from what the system emits?** Not by default — silent balance drift would go unnoticed unless balance reconstruction and/or the hash chain are explicitly enabled and alerted on.
- **Under what workload does the architecture degrade first?** A spike of concurrent writes to a single hot balance (the pooled cooperative contribution account on collection day) — long before raw aggregate volume matters.

---

## Recommendations

**Stage 0 — Before trusting Blnk with savings (do now):**
1. **Confirm the money column type in your own deployment.** Run `\d balances` / `\d transactions` (or inspect the migration SQL you deploy) and record whether balance/`precise_amount` columns are `NUMERIC` or `BIGINT`. *Threshold to change plan:* if `BIGINT` and you use `precision ≥ 10⁶`, cap or reject balances approaching ±9×10¹⁸ minor units, or migrate the column to `NUMERIC`.
2. **Stand up a scheduled correctness alarm.** Nightly, reconstruct every balance from history (`from_source=true`) and alert on any `stored ≠ reconstructed`. This is the single most important operational control and Blnk does not provide it by default.
3. **Enable the hash chain** and alert when `CountUnchainedTransactions` exceeds a small threshold.

**Stage 1 — Configuration hardening:**
4. **Retune `lock_duration`** from 1800s to just above your worst-case commit latency (seconds, not minutes); monitor for lock-expiry-driven retries.
5. **Consolidate retries** to one layer (prefer queue-layer with exponential backoff); disable SDK write-path retries to avoid amplification.
6. **Size Redis for peak queue depth** and enable Redis persistence (AOF) if losing queued-but-undrained contributions is unacceptable. *Threshold:* if `QUEUE_BACKPRESSURE` 503s appear during normal collection days, add Redis memory or shard load.
7. **Configure PostgreSQL PITR** (WAL archiving, e.g. pgBackRest) — do not rely on the daily `pg_dump`→S3 alone. Set an explicit RPO/RTO.

**Stage 2 — Workload shaping for the cooperative pattern:**
8. **Keep `skip_queue:false`** (default) for member contributions; enable **coalescing** (`BLNK_TRANSACTION_ENABLE_COALESCING=true`) — it is ideal for N→A into one pooled account.
9. **Enable hot-lane routing** (`BLNK_QUEUE_ENABLE_HOT_LANE=true`).
10. If contribution-day spikes still saturate one account, **shard the pooled balance** (`@Pool-0..N`) and aggregate for reporting. *Threshold:* shard when p99 time-to-`APPLIED` on collection day exceeds your member-experience budget or lock-contention metrics climb.
11. **Isolate high-volume tenants:** schedule bulk imports off-peak, and run a separate Blnk deployment per society that regularly does bulk work — there is no per-tenant QoS.

**Stage 3 — Caller discipline (bake into your app):**
12. **Never render a balance from a read taken immediately after `QUEUED`.** Poll `reference+_q`/txn ID for `APPLIED` or use the state-change webhook.
13. **Fix a single canonical `precision` per currency** in your application and never vary it.
14. **Use `precise_amount` / `precise_distribution`** for any high-precision or split amounts to avoid rounding ambiguity.

---

## Caveats

- **Money column type, CHECK constraints, the `reference` unique-index DDL, and the immutability trigger are PERMANENTLY UNKNOWN for this study.** The `sql/` DDL defeated four volumes; GitHub blob/raw access was robots-blocked and code-search hits never surfaced. The **named** index `idx_transactions_reference_unique` and the *existence* of immutability protections and an optimistic `version` are confirmed from the changelog and blog, but their exact SQL text and violation behaviour are not. The representable-range conclusion is therefore stated as a range with a caveat, not a fact.
- **The PostgreSQL isolation level inside the composite write is inferred (likely READ COMMITTED), not read.** If it is stronger, some anomalies noted as "possible" would be additionally guarded at the DB layer.
- **The "up to ~5×" throughput figure is a MAINTAINER CLAIM** with no stated conditions; treat it as marketing. No independent MEASURED RESULT (hardware, dataset, concurrency, metric) was found.
- **No independent benchmark of Blnk under contention was located.** All performance behaviour described is derived from source-code mechanisms, the changelog, and the official hot-balances documentation/blog — not from a controlled measurement.
- **Blnk Cloud figures** (99.9% SLA, 7-day rollback, 7-day backup) appear on marketing pages but could not be verified against a durable, Blnk-owned technical source and are excluded from the reliability conclusions for Core.
- **Transaction-queue retry defaults** (as distinct from the reconciliation `max_retries:3, retry_delay:5`) were not independently verifiable; the retry-amplification assessment stands on the *existence* of three retry layers, which is confirmed.
- **Security/adversarial dimensions are deliberately excluded** and deferred to Volume VII; where correctness depends on a mechanism holding (idempotency constraint, Redis lock), only the non-adversarial case is treated here.