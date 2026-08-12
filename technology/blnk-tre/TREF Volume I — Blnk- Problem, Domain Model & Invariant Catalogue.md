# TREF Volume I — Blnk: Problem, Domain Model & Invariant Catalogue

## §0 — Subject Header

```
Technology:              Blnk — open-source double-entry financial ledger
Technology type:         LEDGER
Primary repository:      https://github.com/blnkfinance/blnk  (ledger core — the subject)
Client SDK:              https://github.com/blnkfinance/blnk-go (Go client; client interface only)
Version / release:       v0.15.0 (Jun 22, 2026) — latest MAJOR release analysed; patch line runs to v0.15.2 (Jul 31, 2026)
Commit / tag:            tag v0.15.0; repository at 604 commits / 54 releases as observed 11 Aug 2026
Official documentation:  docs.blnkfinance.com (Mintlify); README in repo; changelog at /changelog/blnk-core
Source openness:         OPEN SOURCE — Apache License 2.0 (LICENSE.md), "Blnk Core" edition
Deployment model:        BOTH — self-hosted (bring-your-own PostgreSQL) or managed "Blnk Cloud"
Licence / edition:       Apache-2.0 for Core; open-core split — Cloud dashboard/back-office/monitoring is commercial
Research date:           11 August 2026
Study objective:         BUILD EXTRACTION
Configuration:           EXTENDED 7 (Volume VII Security & Threat Model commissioned — ledger holds balances)
```

**Evidence ceiling statement.** Blnk is open source (Apache-2.0), so this study reaches CONFIRMED IMPLEMENTATION on several material claims by naming files, structs and schema behaviour. Where I relied on official documentation without opening the exact source line, I mark DOCUMENTED BEHAVIOR; where the project asserts something in a blog or README, MAINTAINER CLAIM. The single most important source-level fact — that money is carried as Go `*big.Int` — is CONFIRMED at `transaction.go` (root), which imports `math/big` and declares `transactionWorker` with an `amount *big.Int` parameter; the field-level declarations live in `model/transaction.go` and `model/balance.go`, which I could not open directly and therefore mark SOURCE-CODE INFERENCE where cited. **Version is pinned at v0.15.0 and behaviour is not mixed silently across releases.**

---

## TL;DR
- **Blnk exists to give fintech developers a correctness-first, double-entry ledger as a drop-in service** — the "boring but unforgiving" layer (balances, immutable transactions, reconciliation, identity) that every fintech otherwise hand-rolls in an application database and gets wrong. It is Nigerian in origin (founder Jerry Enebeli, ex-Flutterwave/Eyowo/Bloc), which shows in its assumptions: money movement modelled as source→destination flows, multi-currency and crypto precision as first-class, and PostgreSQL-only so an operator can bring their own database.
- **The problem it holds is: never lose or invent money, and always be able to prove how a balance was reached.** Its defining invariants are conservation (every transaction has a source and a destination that move the same precise integer amount), immutability of posted transactions (no updates/deletes; corrections are new transactions), and idempotency (a unique `reference` per transaction, enforced by a DB unique index since v0.13.2).
- **What it promises never to violate:** posted transactions are never mutated or deleted; balances change only through transactions; amounts are stored as arbitrary-precision integers in minor units (never floats); and a duplicate `reference` never produces a second money movement. For the cooperative-society builder, the money representation and the immutability/idempotency model are strong ADOPT candidates; the "balance is a cached running total updated in place" design and the single-Postgres deployment are ADAPT/REJECT candidates examined below.

---

## Key Findings (ten most important)

1. **Money is an arbitrary-precision integer in minor units, never a float.** `precise_amount` is carried as Go `*big.Int` (CONFIRMED: `transaction.go` imports `math/big`; DOCUMENTED, from Blnk's split-payments blog: "Blnk uses integer amounts with a precision field to avoid floating-point [errors]… precision: 100 means you divide by 100 to get the display amount. 10000 / 100 = $100.00"). A convenience `amount` (float64) is multiplied by a per-transaction `precision` multiplier to derive `precise_amount`. This is the single most consequential and most transferable decision in the system.
2. **`precision` is caller-supplied per transaction, not a property of the currency.** Blnk does not hold a canonical precision per asset; it trusts the caller to pass a consistent `precision` (e.g. 100 for USD, 10^18 for ETH). Balance responses do not even return precision. This is a redefinition trap — an inconsistent precision silently corrupts a balance.
3. **"Balance" in Blnk is a mutable, cached running total, not a derived quantity.** Balances are updated in place through transactions and carry a `version` for optimistic locking. This diverges from the textbook/TigerBeetle model where balance = f(cumulative debits, credits). Blnk keeps `credit_balance` and `debit_balance` alongside a net `balance`, and can *reconstruct* balances from transactions on demand — but the day-to-day balance is a stored mutable field.
4. **Immutability is by convention + DB protections, not a pure append-only log.** Posted transactions "cannot be modified or deleted" (DOCUMENTED), each state transition is a *new* row linked by `parent_transaction`, and v0.10.1 added "database protections to prevent unauthorized changes to transactions and balance snapshots." But the balance row itself is mutated. Immutability therefore applies to the transaction journal, not to balances.
5. **Idempotency hinges entirely on a unique `reference`.** Since v0.13.2 a unique index `idx_transactions_reference_unique` enforces this at the storage layer (DOCUMENTED, breaking change). Before that it was an application-layer check. A duplicate reference is *discarded*, not errored into a second movement.
6. **The inflight (two-phase) transaction is a native primitive.** A transaction with `inflight: true` holds funds (`inflight_debit_balance`) and settles to APPLIED (commit) or VOID. This is Blnk's built-in authorise/settle and escrow mechanism — directly relevant to loans and remittance holds.
7. **The `@`-prefixed internal balance (e.g. `@World`, `@Fees`) is how Blnk represents the outside world and equity/revenue accounts.** These auto-create in the default General Ledger and typically run negative (they are the counter-entry that keeps double-entry balanced). This is Blnk's substitute for a formal chart-of-accounts normality model.
8. **A significant capability was removed in v0.15.0: built-in FX.** The `rate`, `currency_multiplier` and `modification_ref` fields were deleted; "destination credit equals source debit." Blnk retreated from doing currency conversion inside a transaction — a revealing narrowing of scope toward pure value-conservation.
9. **Concurrency correctness rests on Redis distributed locks plus Postgres optimistic locking (`version`).** Under the default queue, transactions serialise per balance; with `skip_queue: true` they take a Redis lock and a versioned DB write. Hot-balance contention is an explicitly acknowledged failure mode.
10. **Blnk is open-core.** Core (ledger, reconciliation, identity, inflight, lineage, hashing) is Apache-2.0 and fully self-hostable on your own Postgres; the commercial line is Blnk Cloud (managed hosting, dashboard, anomaly detection, back-office approvals/monitoring). No ledger correctness feature is paywalled as of v0.15.0.

---

## Details

### I.1 Problem origin

**The problem.** Every fintech product — wallet, neobank, lender, remittance app, savings/contribution scheme — needs an internal source of truth for "who has how much, and how did they get it." Teams routinely build this as a `balances` table in their application database, incrementing and decrementing a number. That approach fails predictably: it loses money to floating-point rounding; double-counts on retries; cannot answer "what was this balance on 3 March"; has no audit trail; and corrupts under concurrency. Blnk's own framing (MAINTAINER CLAIM, Enebeli, "Reimagining Fintech Infrastructure", Mar 5 2025): payments APIs got easy, but ledgers, reconciliation, identity management and compliance "often exist in rigid, legacy systems that are difficult to access, customize, or scale. Developers are forced to either reinvent the wheel or piece together unreliable solutions, slowing down innovation and increasing operational risk." The stated goal is to make a ledger "as simple as signing up for a Stripe API."

**Who experienced it.** Founder Jerry Enebeli spent a decade in African fintech engineering — Backend Engineer at Eyowo (a Nigerian neobank, maintaining banking infrastructure), integration work at Flutterwave (whose own scale, per Y Combinator's company profile, is "close to $20 billion in payments and 100 million transactions across over 33 African countries"), Chief/Head of Product at Bloc (business banking/BaaS), and founder/CEO of Orchestrate (payments orchestration, acquired 2021). Blnk is the generalisation of a ledger he had repeatedly built by hand. (DOCUMENTED, blnkfinance.com/about; LinkedIn.)

**Prior approaches and their inadequacy:**
- *Hand-rolled application-DB ledgers* — fast to start, but no immutability, weak idempotency, float errors, no reconciliation, no history. This is precisely the pain Blnk targets.
- *General-purpose accounting packages (QuickBooks, LedgerSMB, Beancount)* — built for books and reporting at human scale, not high-throughput programmatic money movement via API; no concept of inflight holds, no per-transaction API idempotency.
- *Core-banking systems (Temenos, Finacle, Mambu)* — heavyweight, licensed, closed, hard to customise or self-host; the opposite of "deploy a sandbox in 5 minutes."
- *Other open-source/purpose-built ledgers (TigerBeetle, Formance, Midaz)* — credible, but each makes different tradeoffs (§I.13). At the time Blnk emerged (first release Mar 2024) none combined "single-binary-ish, Postgres-backed, REST-first, batteries-included (reconciliation + identity)" for the developer-first African fintech audience.

**The African/Nigerian context (why a Lagos ledger differs from a Valley one):**
- **Multi-currency and crypto are not edge cases.** Nigerian fintech routinely spans NGN, USD and stablecoins; Blnk treats per-asset precision (including 10^18 for ETH) as first-class rather than assuming two decimal places.
- **High inflation and large nominal values** make >15-digit amounts real, motivating the arbitrary-precision `precise_amount` (added v0.10.1) — a Valley ledger assuming int64 cents would overflow.
- **Bring-your-own-infrastructure and cost sensitivity.** Postgres + Redis + Docker Compose on modest hardware, self-hosted, "100% control on your data" — important where managed-cloud spend and data-residency/regulatory control matter.
- **Reconciliation against many external providers** (agency banking, multiple PSPs across countries) is a headline module, not an afterthought — reflecting the fragmented rails Enebeli integrated across his career at Flutterwave/Orchestrate.

### I.2 Historical evolution (with causes)

Release history is CONFIRMED from the official changelog (`/changelog/blnk-core`) and GitHub releases. Cause attributions are the technical pressure evidenced by the changelog text; where inferred they are marked HYPOTHESIS.

- **v0.5.0 — First release (Mar 25, 2024).** Ledgers, ledger balances, transactions, identities, balance monitoring, General Ledger (chart of accounts), refunds, scheduling. Establishes the core object model.
- **v0.6.0 (Apr 8, 2024).** *Inflight transactions*, *multiple sources/destinations*, *overdrafts*, enhanced concurrency control. Cause: real money flows are two-phase (authorise/settle) and split (fees); wallets need holds — the application-DB model could not.
- **v0.6.1 (Apr 12, 2024).** `precision` becomes a **transaction parameter**; search added; partial inflight commits. Cause: correct per-asset decimal handling; "convert naira to kobo."
- **v0.6.2 (May 3, 2024).** *Rates* (FX between currencies); `inflight_expiry_date`. (Later reversed — see §I.3.)
- **v0.7.0 (Sep 9, 2024).** *Reconciliation* module; `parent_transaction` introduced to link derived transaction states. Cause: audit/traceability and matching external records; the immutable model needs a lineage pointer instead of updates.
- **v0.8.x (Jan–Feb 2025).** `skip_queue` direct processing (0.8.2); configurable insufficient-funds retries and **queued balances** (0.8.3); **balance snapshots & historical balances** (0.8.4); **PII tokenization** (0.8.8). Cause: latency control, point-in-time reporting, and compliance (PII scope reduction).
- **v0.9.0 (Mar 3, 2025).** *Bulk transactions* (atomic or independent) and *backdated transactions* (`effective_date`). Cause: migrations from legacy systems and batch payouts (payroll) need backdating and all-or-nothing batches.
- **v0.10.1 (Mar 22, 2025).** **`precise_amount`** (amounts >15 digits); *granular API keys* (scopes); *overdraft limits*; balance reconstruction; instant reconciliation; DB protections against unauthorized transaction/snapshot changes. Cause: float/precision ceiling and multi-tenant authorisation.
- **v0.11.0 (Aug 27, 2025).** Metadata search; insufficient-balance checks now include inflight. Breaking (Typesense).
- **v0.12.0 (Dec 8, 2025).** **API keys hashed with SHA-256** at rest (breaking). Cause: security hardening.
- **v0.13.0 (Jan 29, 2026).** **Lineage** — fund-source tracking with FIFO/LIFO/proportional debit allocation; webhook HMAC signing. Cause: traceability of *which* funds left a balance.
- **v0.13.2 (Feb 12, 2026).** **Unique DB index on `transactions.reference`** (breaking; upgrade fails on duplicates); DB-level filter search. Cause: harden idempotency at storage, not just application.
- **v0.14.0 (Apr 9, 2026).** Performance release — internal benchmark throughput improved "up to about 5×" under heavy contention (MAINTAINER CLAIM with stated conditions; not independently MEASURED).
- **v0.15.0 (Jun 22–23, 2026).** **Structured API errors (`error_detail.code`)**; **removal of `rate`/`currency_multiplier`/`modification_ref`**; queued inflight commit/void by default; **optional global hash chain** with `blnk verify-chain`. Current major release under study.
- **v0.15.1/0.15.2 (Jul 2026).** Fixes; queue/Typesense memory backpressure (503 `QUEUE_BACKPRESSURE`).

Architectural turning points: (a) shift from application-checked to DB-enforced idempotency (0.13.2); (b) `parent_transaction` lineage (0.7.0) as the backbone of an immutable multi-state model; (c) narrowing away from in-ledger FX (0.15.0).

### I.3 The removal record

- **Built-in FX / `rate` (added v0.6.2 → removed v0.15.0).** For roughly two years a transaction could carry a `rate` to convert between currencies of different balances, plus `currency_multiplier`. In v0.15.0 these were removed: "Request `rate` no longer applies an exchange rate; destination credit equals source debit." **What it reveals:** Blnk chose to make *strict value conservation* (debit amount == credit amount) an inviolable core invariant, and pushed FX out to the caller. A ledger that silently changes the amount between source and destination cannot guarantee conservation; removing FX is the project settling firmly on the conservation invariant as identity. The most informative removal in the record.
- **`modification_ref` (removed v0.15.0).** A field associated with balance/transaction modification bookkeeping. Its removal reinforces the "transactions are not modified" stance — the concept of a modification reference is inconsistent with pure immutability.
- **Synchronous-by-default bulk and inflight commit/void (changed 0.10.5, 0.15.0).** Bulk (0.10.5) and inflight commit/void (0.15.0) moved to queue-by-default; the previous synchronous behaviour is now opt-in via `skip_queue`. **Reveals:** the project settled on asynchronous, queue-serialised processing as the correctness-preserving default under concurrency, treating synchronous processing as the exceptional (low-contention) case.
- **Plaintext/return-on-list API keys (changed 0.12.0).** Keys are no longer retrievable after creation; only a SHA-256 hash is stored. A deliberate withdrawal of convenience for a security guarantee.

### I.4 Actors and users

| Actor | Goal | Trust level | Inputs | Outputs | Failure impact |
|---|---|---|---|---|---|
| **Calling application/service** (fintech backend) | Record money movement, read balances | High — holds API key | REST/SDK calls | Ledger state, webhooks | Incorrect calls → wrong balances; must supply correct `precision`/`reference` |
| **End user (customer)** | Indirect — their wallet is a balance | None (never talks to Blnk directly) | — | — | Sees wrong balance if caller errs |
| **Operator/administrator** | Deploy, configure, back up, scale | Highest — controls Postgres/Redis/config | `blnk.json`, env, `verify-chain` | Running service | DB access = full mutation power (Vol VII) |
| **API key holder (scoped)** | Least-privilege access (e.g. `transactions:write`) | Medium; scopes since v0.10.1; owner-scoped since v0.14.3 | Scoped API calls | — | Over-broad scope = authz breach |
| **External systems (PSPs, banks)** | Provide statements for reconciliation | None | CSV/records uploaded by operator | Match results | Bad data → false mismatches |
| **Maintainers (Blnk Finance LLC)** | Evolve Core; run Cloud | — | Commits, releases | Releases, docs | Breaking changes (several — §I.2) |
| **Blnk Cloud (managed)** | Dashboard, monitoring, back-office | Connects via read "Query Agent" to your Core | Queries | Insights, approvals | Commercial dependency if adopted |

No plugin architecture in Core; extension is by wrapping the REST API in your own services (Watch, a separate DSL repo, handles monitoring rules).

### I.5 Jobs to be done

- **Core jobs (ledger correctness):** create ledgers; create balances; record double-entry transactions (source→destination); maintain running balances (net, credit, debit, inflight, queued); enforce idempotency; immutable transaction journal with lineage.
- **Transaction workflows:** inflight (two-phase) holds with commit/void/partial-commit/expiry; multiple sources/destinations (splits); bulk (atomic or independent); scheduled; backdated (`effective_date`); refunds (idempotent since 0.10.3); overdrafts with `overdraft_limit`.
- **Convenience/reporting:** balance monitors/alerts; balance snapshots & historical balances (point-in-time); queued balances; search (Typesense or direct-DB filter); metadata on any object.
- **Integrations:** reconciliation (batch + instant; matching rules; 1:1/1:many/many:1 strategies); identity management + PII tokenization; webhooks (HMAC-signed since 0.13.0); lineage/fund-source tracking.
- **Administration/ops:** API keys with scopes; health checks; queue monitoring port; Kubernetes manifests; telemetry; optional hash chain + `verify-chain`.
- **Commercial (open-core boundary):** Blnk Cloud — managed hosting, back-office dashboard (create/edit/approve/void from UI), anomaly detection, analytics, team collaboration. **Everything ledger-correctness-related sits on the open (Apache-2.0) side; the paid side is operational convenience and monitoring, not ledger semantics.**

### I.6 Domain glossary (industry-standard vs Blnk-specific; redefinitions flagged)

- **Ledger** — a grouping/namespace for balances (like a "book"). *Blnk-specific usage:* an organisational container, not the classical "book of final entry." A default **General Ledger** is created at install for internal `@` balances. ⚠️ Redefinition-lite: closer to "a partition/tenant."
- **Balance** — a store of value (wallet/account). ⚠️ **Major redefinition:** in Blnk a "balance" is a *stored, mutable, versioned object* with six sub-fields (`balance`, `credit_balance`, `debit_balance`, `inflight_balance`, `inflight_credit_balance`, `inflight_debit_balance`), not a value *derived* from entries. Textbook "balance" = credits − debits computed on demand; Blnk's `balance` is a cached running total (though it can be reconstructed).
- **Account** — Blnk uses **balance** as the primary noun; "account" appears in an SDK helper (`account.go`) and colloquially. Not the primary abstraction.
- **Transaction** — a single money movement from a `source` to a `destination`. ⚠️ Redefinition: classical double-entry treats a "transaction" as a set of balanced journal lines (n debits, n credits); in Blnk it is fundamentally a *one-source-one-destination transfer* (splits fan out into child transactions linked by `parent_transaction`).
- **Entry** — Blnk exposes no separate "journal entry / posting line" object; the debit and credit are implicit in `source`/`destination` and recorded as increments to `credit_balance`/`debit_balance`.
- **Source / Destination** — the balance money leaves / the balance money enters. Both mandatory; a transaction missing either is rejected. *Blnk's engineer-friendly renaming of debit/credit* (compare Formance, which explicitly frames sources/destinations as the engineer's analog of credit/debit).
- **Reference** — a caller-supplied unique string; the idempotency key.
- **Precision** — an integer multiplier (e.g. 100) applied to `amount` to produce integer `precise_amount`. ⚠️ Redefinition: not "number of decimal places" but "the factor mapping display units to minor units"; per-transaction and caller-owned. Blnk docs: "Use the same precision you pass on transactions for each currency (for example, 100 for USD) to convert integers to display amounts: display_amount = balance / precision."
- **Precise amount (`precise_amount`)** — the amount in smallest indivisible units, stored as an arbitrary-precision integer.
- **Inflight** — a held/pending transaction (two-phase). Blnk-specific term for authorise-then-settle.
- **Indicator** — a human-readable alias for an internal balance (e.g. `@World`), auto-registered in the General Ledger when prefixed with `@`.
- **Identity** — a customer/organisation record (with optional PII tokenization) linkable to balances/transactions.
- **Reconciliation** — matching external records to internal transactions via rules/strategies. First-class module.
- **Lineage** — fund-source tracking; which credits funded a later debit, with FIFO/LIFO/proportional allocation (v0.13.0).
- **Version** — a per-balance integer for optimistic concurrency control.
- **Hash** — SHA-256 digest of a transaction's fields; optional global **hash chain** links transactions to detect tampering.
- **Queued balance** — estimated cumulative effect of not-yet-processed queued transactions (`queued_credit_balance`/`queued_debit_balance`); explicitly labelled an estimate.

### I.7 Core abstractions (domain model)

**Ledger** — identity `ldg_<uuid>`; attributes: name, metadata, created_at. Lifecycle: created (default General Ledger auto-created); renamable (0.11.1) without affecting balances; no delete of core ledger. Owns balances. Persistent.

**Balance** — identity `bln_<uuid>`; attributes: the six balance fields (all integers in minor units), `currency`, `ledger_id`, optional `identity_id`, optional `indicator` (for `@` internal balances), `version`, metadata, created_at. ⚠️ Mutability: **mutable in place** (only via transactions; never set directly); starts at 0; cannot be created with a preset amount. Optimistically locked via `version`. Multi-currency: one balance = one currency; multi-currency is multiple balances. Constraint (0.10.5): no duplicate balance with the same indicator+currency.

**Transaction** — identity `txn_<uuid>`; attributes: `amount` (float64, convenience), `precise_amount` (`*big.Int`), `precision` (int64), `currency`, `source`, `destination`, `reference` (unique), `description`, `status`, `hash`, `allow_overdraft`, `overdraft_limit`, `inflight`, `inflight_expiry_date`, `inflight_commit_date`, `scheduled_for`, `effective_date`, `parent_transaction`, metadata, created_at. Lifecycle: QUEUED → {INFLIGHT → {APPLIED|VOID}} | APPLIED | REJECTED. ⚠️ **Immutable once posted**; each state change is a *new* row linked by `parent_transaction`. Money type CONFIRMED as `*big.Int` at `transaction.go`.

**Identity** — `idt_<uuid>`; person/organisation, optional PII tokenization; links to balances/transactions. Deterministic creation supported (0.14.2). Deletable (0.15.0).

**Internal balance** (`@Name`) — a balance owned by the operator's organisation representing the outside world / equity / revenue / fees; auto-created in General Ledger on first `@`-reference. Typically runs negative under overdraft. The counter-entry mechanism.

**Reconciliation, Lineage allocation, Balance snapshot, Balance monitor, API key, Webhook** — supporting abstractions (files `reconciliation.go`, `lineage*.go`, `apikey.go`, `webhooks.go`, `balance_test.go` etc.).

**Money representation (the decision everything rests on).** Numeric model: integer minor units. Wire/compute type: Go `*big.Int` for `precise_amount` and for balance fields (SOURCE-CODE INFERENCE for the balance struct; CONFIRMED that `transaction.go` uses `math/big` and passes `amount *big.Int`). Convenience `amount` is float64 and is *derived*, not authoritative. Precision: caller-supplied per transaction; **balances do not return precision** (docs: "Balance fields are integers in minor units… Blnk Core does not return precision on balance responses… `display_amount = balance / precision`"). Multi-currency: independent per-balance; **no automatic FX** since v0.15.0 (destination credit == source debit). Postgres storage type not opened directly; the >15-digit requirement and `*big.Int` usage make `NUMERIC` the strongly-favoured inference (ANALYTICAL INFERENCE; not confirmed from DDL).

### I.8 THE INVARIANT CATALOGUE

Numbered; each with claimed enforcement point and evidence class. Volumes II–III will locate and verify each.

- **INV-1 — Conservation (source and destination move the same precise amount).** Every transaction has a `source` and a `destination`; the amount debited equals the amount credited. Claimed enforcement: transaction validation (a transaction missing source or destination is *rejected*); reinforced by v0.15.0 removal of `rate` so "destination credit equals source debit." Class: DOCUMENTED BEHAVIOR + FX removal CONFIRMED via changelog. (This is per-transfer equality; NOT a periodic trial-balance across all accounts — see falsification test.)
- **INV-2 — Balances change only through transactions.** "Balance amounts are immutable and can only be updated through transactions. You cannot manually set or alter a balance amount directly." Enforcement: API surface + DB protections (0.10.1). Class: DOCUMENTED BEHAVIOR.
- **INV-3 — Balance derivability / reconstructability.** A balance can be recomputed from its transaction history (`from_source=true`; `BLNK_RUN_RECONCILIATION`). Enforcement: balance reconstruction feature (0.10.1). Class: DOCUMENTED BEHAVIOR. ⚠️ The day-to-day balance is a cached total; derivability is a recovery path, not the primary read.
- **INV-4 — Idempotency / reference uniqueness.** A given `reference` yields exactly one money movement; duplicates are discarded. Enforcement: **unique DB index `idx_transactions_reference_unique`** (v0.13.2) — storage-level; previously application-level. Class: DOCUMENTED BEHAVIOR (index named in changelog → strong CONFIRMED-adjacent).
- **INV-5 — Immutability of posted transactions.** Once QUEUED/APPLIED/committed/voided, a transaction row is not modified or deleted; new states are new rows via `parent_transaction`; status cannot roll back. Enforcement: application + DB protections; lineage pointer. Class: DOCUMENTED BEHAVIOR.
- **INV-6 — Valid state transitions.** Allowed: QUEUED→{INFLIGHT,APPLIED,REJECTED}; INFLIGHT→{APPLIED,VOID}; no reverse transitions. Enforcement: transaction lifecycle engine (`transaction_inflight.go`, `transaction_execution.go`). Class: DOCUMENTED BEHAVIOR.
- **INV-7 — Precision integrity (amounts are integers in minor units).** No float storage; `precise_amount` integer; non-integer precision rejected (0.11.3: "rejects transactions with non-integer precision values"). Enforcement: validation + `*big.Int` type. Class: CONFIRMED (type) + DOCUMENTED (rejection).
- **INV-8 — Sufficient funds unless overdraft permitted.** `available = balance − inflight_debit_balance (− queued_debit)`; if amount exceeds available and `allow_overdraft` is false → REJECTED; with overdraft, cannot exceed `overdraft_limit`. Enforcement: pre-processing balance check (v0.11.0 includes inflight). Class: DOCUMENTED BEHAVIOR.
- **INV-9 — Concurrency safety (no lost updates on a balance).** Per-balance serialisation via Redis distributed lock (skip_queue) and Postgres optimistic locking on `version`; queue path serialises. Enforcement: `queue.go`, Redis lock, versioned write. Class: DOCUMENTED BEHAVIOR + MAINTAINER CLAIM (hot-balances blog).
- **INV-10 — Zero-amount and malformed transactions are not recorded.** Zero-amount transactions are discarded; malformed requests rejected. Enforcement: validation. Class: DOCUMENTED BEHAVIOR.
- **INV-11 — Tamper-evidence (optional).** SHA-256 per-transaction hash; optional global hash chain verified by `blnk verify-chain`. Enforcement: hashing subsystem (opt-in, off by default). Class: DOCUMENTED BEHAVIOR. ⚠️ Off by default → not an active guarantee unless enabled.
- **INV-12 — Authorisation/tenancy (scoped keys).** API keys carry scopes (0.10.1), are owner-bound (0.14.3), and hashed at rest (0.12.0). Enforcement: API key middleware. Class: DOCUMENTED BEHAVIOR. ⚠️ No built-in multi-tenant isolation *between ledgers* beyond key scoping — an operator concern for Vol VII.

An invariant nobody can point to is a HYPOTHESIS: **a global "sum of all balances == 0" trial-balance invariant is NOT enforced by Blnk** — conservation is guaranteed per-transfer (INV-1), and because internal `@World`-type balances absorb the counter-entry, the *system* can be made to sum to zero by convention, but Blnk does not enforce a global zero-sum. Flagged as the primary falsification target (§I.14).

### I.9 Semantics (Blnk meaning vs ordinary meaning)

- **Creation** — POST creates ledger/balance/identity/transaction. A balance is always created at 0 (cannot preset). ⚠️ differs from DB "insert with values."
- **Update** — ledgers can be renamed; metadata can be added to any object; **balances and transactions' financial fields cannot be updated**. "Update" in Blnk means metadata/label, never money.
- **Deletion** — identities and balance monitors can be deleted; **transactions cannot be deleted**; balances are not deletable. ⚠️ Accounting-correct: you never delete a posting.
- **Commit** — settle an INFLIGHT transaction to APPLIED (full or partial); idempotent by transaction_id. Queued by default since 0.15.0.
- **Rollback** — ⚠️ **not a ledger operation.** Statuses cannot roll back. "Rollback" exists only at the internal DB-transaction level. A user-level reversal is a *new* transaction.
- **Void** — cancel an INFLIGHT transaction, releasing held funds (INFLIGHT→VOID). Only inflight can be voided; an APPLIED transaction cannot be voided — you refund/reverse instead.
- **Application (APPLIED)** — funds actually moved and balances updated.
- **Reversal / correction** — ⚠️ **a new transaction**, not an edit. A refund is "a new transaction… needs its own reference" (idempotent since 0.10.3; cannot refund twice). Corrections/backdating use `effective_date`. This is the sharpest accounting-vs-database divergence and the key one for the builder: **you never mutate history; you post a compensating entry.**
- **Version** — optimistic-lock counter on a balance, incremented on each applied change; not a semantic "document version."
- **Timestamp** — `created_at` (system time) vs `effective_date` (financial date, may be backdated; defaults to created_at). ⚠️ Two distinct time axes — a real redefinition trap.
- **Equality / identity** — objects identified by prefixed UUIDs (`txn_`, `bln_`, `ldg_`, `idt_`); a transaction's *idempotent identity* is the `reference`.
- **Ordering** — the `parent_transaction` chain defines lineage order; the queue defines processing order; `effective_date` defines financial order (which can differ from insertion order).
- **Finality** — APPLIED and VOID are terminal; no un-apply. Finality is by forward-only compensating entries.
- **Error** — since v0.15.0 structured `error_detail.code` (e.g. `TXN_NOT_FOUND`, `QUEUE_BACKPRESSURE`); duplicate reference / zero amount → *discarded* (not necessarily an error to the caller); insufficient funds → REJECTED status + webhook.

### I.10 Assumptions (what Blnk assumes the surrounding system provides)

- **Callers supply a correct, consistent `precision` per currency.** Blnk holds no canonical asset precision; an inconsistent precision corrupts balances silently. (Docs warn to "use the highest precision value for all transactions.")
- **Callers supply a unique `reference` per intended movement** and reuse it on retries — the entire idempotency guarantee is delegated to caller discipline (backed by the DB unique index).
- **Callers implement FX themselves** (post-v0.15.0) and record conversions as separate movements/legs.
- **PostgreSQL is available, durable and the source of truth**; the operator brings and secures it. Redis is available for queue + distributed locks.
- **Typesense is available if Typesense search is used** (else direct-DB filter).
- **Clocks are reasonable**; `effective_date` correctness is the caller's responsibility; system uses server time for `created_at`.
- **Concurrency is bounded per balance**; hot balances are the caller's design problem (queue vs skip_queue, coalescing).
- **The caller owns authorisation of *end users*** — Blnk authenticates the *service* (API keys), not customers.
- **Workload is transaction-heavy but each transaction is small**; large fan-outs use bulk/multiple-destinations with caps (10,000 items per bulk request in 0.15.0).

### I.11 Explicit non-goals

- **Not a currency-conversion engine** (explicitly removed FX in v0.15.0). Documented by removal.
- **Not a payments processor / bank connector.** Per the Oncely product listing: "While it doesn't include pre-built payment or bank integrations, its flexible infrastructure enables custom integrations for diverse services, from payment processors to banking systems." You bring the rails.
- **Not a customer-facing auth/identity provider** — identities are records, not a login system.
- **Not a general accounting/reporting suite** (no P&L, tax, GAAP statements out of the box; the General Ledger is a chart-of-accounts container, not a reporting engine).
- **Not a multi-tenant SaaS boundary by itself** — isolation between customers is achieved by ledger partitioning + your own key management (compare TigerBeetle's "ledger per customer" pattern; Blnk expects the same discipline).
- **Not a distributed/HA database** — correctness rests on a single Postgres as source of truth; HA is an operator concern.

Mostly these are *inferred from removals and third-party statements*; Blnk documents them implicitly rather than as a formal "non-goals" list. That itself is a finding: the non-goals must be inferred, so a builder can be misled into expecting FX or bank integrations.

### I.12 Standards and theory

- **Double-entry bookkeeping** — the foundational model. Blnk implements the *reciprocal value movement* core (every transaction = value out of source + value into destination) but **renames debit/credit to source/destination** and does not expose the classical five-account-type/normality model (assets/liabilities/equity/income/expense with debit- or credit-normal behaviour). Compare Formance's explicit formal model (position in chart of accounts + normality + list of debits/credits). Blnk's simplification: normality is emulated by convention using internal `@` balances and overdraft, not by a typed account model.
- **Minor-units integer money (ISO 4217 spirit; crypto satoshi/wei model)** — Blnk follows the industry best practice of integer smallest-units, extended to arbitrary precision via `*big.Int` for crypto-scale magnitudes. Standard, correctly applied.
- **Idempotency keys (Stripe-style)** — the `reference` is a classic idempotency key, now DB-enforced.
- **Two-phase authorise/settle** — inflight mirrors card auth→settlement and escrow; conceptually a hold, not distributed 2PC.
- **Cryptographic hash chaining (SHA-256)** — optional tamper-evidence, borrowing the blockchain "each record commits to prior state" idea, but centralised and opt-in — not a consensus ledger.
- **Deviation to note:** Blnk claims "double-entry" but a builder assuming a *balanced multi-line journal with enforced global trial balance* will be surprised: Blnk enforces per-transfer conservation, not a global debits==credits trial balance across a chart of accounts. This is the deviation most likely to mislead.

### I.13 Competing conceptual models

- **TigerBeetle.** Purpose-built financial DB; accounts + transfers are built-in primitives; amounts are unsigned **128-bit integers** (per its docs: "To maximize precision and efficiency, Account debits/credits and Transfer amounts are unsigned 128-bit integers… map the smallest useful unit of the fractional currency to 1"; its 2023 engineering blog notes they "decided to use 128-bit integers to store all financial amounts and balances, retiring our previous use of 64-bit integers"); accounting rules enforced *in the database* via flags (`debits_must_not_exceed_credits`, `credits_must_not_exceed_debits`, balancing transfers); tracks cumulative posted debits/credits and leaves net balance to the app; ledger-per-asset, transfers only within a ledger. *Buys:* extreme throughput, correctness enforced at the DB, no float. *Costs:* opinionated, no metadata/reconciliation/identity, you build the surrounding service; not REST; harder to query. Blnk trades TigerBeetle's raw speed and in-DB enforcement for developer ergonomics, Postgres familiarity, and batteries-included modules.
- **Formance Ledger.** Programmable, source-available; a DSL (Numscript) to express multi-posting flows; explicit formal double-entry model (normality, chart position). *Buys:* expressive, auditable flows; rigorous model. *Costs:* steeper concept load; DSL to learn. Blnk is more CRUD/REST-simple; Formance is more formally accounting-correct.
- **Midaz (Lerian).** Source-available, cloud-native **microservices** (Onboarding + Transaction services), multi-asset/multi-currency, **n:n transactions**, organisations→ledgers→portfolios→segments→accounts hierarchy, accounting/operation "routes." *Buys:* enterprise hierarchy, n:n richness, plugin ecosystem. *Costs:* heavier to run (microservices) than Blnk's Postgres+Redis. Blnk is simpler/flatter; Midaz is more enterprise-core-banking-shaped — notably *closer* to the cooperative-society platform's eventual shape, and worth the builder's attention as an alternative.
- **Hand-rolled application-DB ledger.** *Buys:* zero new infra, full control. *Costs:* re-implements every invariant badly; this is exactly what Blnk replaces. REJECT for anything holding real member savings.
- **Traditional core-banking ledger (Mambu/Temenos/Finacle).** *Buys:* regulatory features, product engines (loans/deposits) out of the box. *Costs:* cost, closed, slow to change, not founder-ownable. The builder's *destination* is core-banking-shaped, but adopting a closed core violates the "permanently founder-owned" constraint.
- **Event-sourced ledger.** Money as an append-only event log; balances are pure projections. *Buys:* perfect auditability, replay, temporal queries by construction. *Costs:* projection complexity, eventual-consistency reasoning. **Blnk is a hybrid:** immutable transaction journal (event-log-like) + a mutable cached balance projection with optimistic locking — pragmatic, not purely event-sourced.

### I.14 Falsification test

The domain model asserted here — *money as arbitrary-precision integer minor-units; balance as a mutable cached projection reconstructable from an immutable, reference-idempotent, source→destination transaction journal; conservation enforced per-transfer* — would be **proven wrong** if Volumes II–IV find any of:

1. **A code path that stores or arithmetic-processes authoritative money as float64** (not merely the convenience `amount`), i.e. balances or `precise_amount` computed in floating point. Falsifies INV-7 and the money model.
2. **A mutation of a posted transaction row's financial fields** (an UPDATE on amount/source/destination/status that overwrites rather than inserting a new `parent_transaction`-linked row). Falsifies INV-5.
3. **A second money movement produced from a duplicate `reference`** under concurrency (idempotency bypass). Falsifies INV-4.
4. **A transaction whose destination credit differs from its source debit** in v0.15.0+ (surviving FX or asymmetric posting). Falsifies INV-1 (conservation).
5. **A balance write that loses an update under concurrency** despite `version`/lock (a real lost-update on a hot balance). Falsifies INV-9.
6. **Evidence that Blnk enforces a global trial-balance (sum of all balances == 0)** — if found, my claim that conservation is *only* per-transfer is wrong (the more interesting and likely-correct finding is that it does NOT).

Volumes II onward are directed to look specifically for (1), (2) and (4) in `transaction_execution.go`, `transaction_inflight.go`, `balance.go`, and the SQL migrations.

### I.15 Preliminary build-extraction verdicts (ADOPT / ADAPT / REJECT)

Applying the environment question (did it work because of the mechanism, or the environment around it?):

- **Money as `*big.Int` minor-units + integer storage — ADOPT (unconditionally).** Mechanism-intrinsic; independent of Blnk's team/scale. For a Nigerian cooperative platform spanning NGN and possibly USD/stablecoins, arbitrary-precision integers are exactly right. Transferable verbatim.
- **Immutable transaction journal + compensating-entry corrections (no edits/deletes) — ADOPT.** Mechanism-intrinsic and audit-mandatory for member savings/loans. Adopt the "never mutate history; post a reversal" discipline regardless of ledger chosen.
- **Idempotency via unique `reference`, DB-enforced — ADOPT.** Cheap, mechanism-intrinsic, prevents the classic double-credit bug on retries — critical for mobile-money-style unreliable networks in the target market.
- **Inflight two-phase transactions — ADOPT (adapt naming).** Directly models loan disbursement holds, contribution collections pending clearance, and remittance holds. Mechanism-intrinsic.
- **`precision` as a per-transaction, caller-supplied value — ADAPT (change to per-asset canonical precision).** This worked for Blnk because its callers are disciplined developer teams (the *environment*). For a founder-owned core-banking platform with many internal services and cooperative admins, per-transaction precision is a footgun. **Change to:** a currency/asset registry that fixes precision per asset and rejects mismatches — do not inherit the "trust the caller each time" model.
- **Balance as a mutable cached running total — ADAPT.** It works at Blnk's scale with Redis+optimistic locking, but that is partly an *environmental* crutch (their queue/lock infra). For a founder-owned system, keep the cached balance for reads but treat the immutable journal as the sole source of truth and reconcile/reconstruct on a schedule; consider event-sourced projection if audit rigor dominates.
- **Single-PostgreSQL-as-source-of-truth deployment — ADAPT.** Fine to start; but member-savings durability/HA obligations mean you must add replication/backup/DR that Blnk leaves to the operator. Don't inherit the assumption uncritically.
- **In-ledger FX — REJECT (follow Blnk's own removal).** Do not put currency conversion inside a transfer; record conversions as explicit paired movements. Blnk's removal is a lesson learned; adopt the lesson, not the removed feature. A REJECT here is as valuable as an ADOPT.
- **Optional/off-by-default hash chain — ADAPT (turn it on, or design equivalent).** For a system holding member balances, tamper-evidence should be on and monitored, not opt-in.
- **Blnk Cloud (commercial) — REJECT for the core dependency.** The "permanently founder-owned, vendor model" constraint forbids a hard dependency on a third-party managed plane; build your own back-office. Core (Apache-2.0) is compatible with founder ownership; Cloud is not.

### I.16 Volume I reconstruction (synthesis)

**Core abstraction diagram (textual):** Ledger 1—* Balance *—* Transaction (source, destination); Identity *—* Balance; Internal `@`-balance ⊂ Balance in General Ledger; Transaction —parent_transaction→ Transaction (lineage tree). The numbered invariant catalogue (INV-1…INV-12, §I.8) is the spine Volumes II–III will locate and verify.

**Key unknowns:** exact Postgres column types for money (NUMERIC inferred, not confirmed from DDL); exact `model/transaction.go`/`model/balance.go` field declarations; whether any internal path uses float arithmetic on authoritative money; precise semantics of lineage allocation under partial commits; behaviour of the hash chain across backdated inserts; whether a global trial-balance is enforced anywhere (believed not).

**What is Blnk fundamentally?** A correctness-first, Postgres-backed, REST-first double-entry *transfer ledger* — an immutable journal of source→destination money movements with cached, reconstructable balances — packaged so a developer can adopt it without hand-rolling money infrastructure.

**Single most important abstraction:** the **Transaction as an immutable source→destination transfer** (with the `@`-internal-balance as its indispensable counter-entry).

**Invariant that most defines correctness:** **INV-1 conservation** (destination credit == source debit), hardened by the v0.15.0 FX removal — closely coupled with INV-4 idempotency and INV-5 immutability.

**Assumption whose removal would most change the design:** that **the caller supplies correct, consistent per-transaction `precision`** — if Blnk instead owned canonical per-asset precision, the money model and much validation would change shape (and be safer).

**What the project tried and removed, and what it reveals:** it built in-transaction **FX (`rate`)** and then removed it (v0.15.0), revealing that the project ultimately privileged *strict value conservation* over convenience — the clearest signal of what Blnk refuses to violate.

**Deepest conceptual tradeoff:** **cached mutable balance vs pure derived balance.** Blnk keeps a mutable, versioned running balance (fast reads, needs locks/queue for correctness) *and* an immutable journal it can replay — a pragmatic hybrid that buys performance and simplicity at the cost of a second source of truth that must be kept reconciled. For a builder holding members' savings, deciding where to sit on this axis is the central design choice this volume surfaces.

---

## Recommendations

1. **Adopt now, verbatim:** the integer/`*big.Int` minor-units money model; the immutable-journal + compensating-entry correction discipline; DB-enforced idempotency via a unique reference; and inflight two-phase transactions. These are mechanism-intrinsic and directly fit cooperative savings/contributions/loans.
2. **Adapt before adopting:** replace per-transaction caller-supplied `precision` with a **canonical per-asset precision registry** that rejects mismatches; treat the immutable journal (not the cached balance) as the sole source of truth and run scheduled reconstruction/reconciliation; and add replication/backup/DR around Postgres (Blnk assumes you will).
3. **Reject:** in-transaction FX (record conversions as explicit paired movements — follow Blnk's own removal); and any hard dependency on Blnk Cloud (incompatible with permanent founder ownership — build your own back-office on Core, Apache-2.0).
4. **Turn on tamper-evidence** (hash chain) from day one rather than leaving it opt-in.
5. **Benchmarks/thresholds that would change these recommendations:** if Volume III finds a lost-update on hot balances despite `version`/locks (INV-9 fails) → do not inherit the cached-balance design; move to event-sourced projections. If Volume II finds authoritative money handled as float (INV-7 fails) → do not reuse Blnk's arithmetic paths. If member-count/throughput projections exceed what a single Postgres can serve with headroom (sustained hot-balance contention on pooled contribution accounts) → evaluate TigerBeetle for the hot core with Blnk/your-own for metadata. If regulatory audit demands an enforced global trial balance, add that invariant explicitly — Blnk will not give it to you.

## Caveats

- Several claims here are **DOCUMENTED BEHAVIOR** from official docs/changelog, not opened line-by-line in source; the money type is CONFIRMED via `transaction.go`'s `math/big`/`*big.Int` usage, but the exact `model/*.go` field declarations and the Postgres DDL column types were **not** directly read and are marked SOURCE-CODE/ANALYTICAL INFERENCE (NUMERIC for money columns is inferred, not confirmed).
- The "up to about 5×" throughput improvement (v0.14.0) is a **MAINTAINER CLAIM with stated conditions**, not an independently reproduced MEASURED RESULT; the reconciliation "over 95% accuracy" figure is third-party marketing (Oncely product listing: "significantly reducing manual work and achieving over 95% accuracy") and should not be treated as a benchmark.
- Behaviour is pinned to **v0.15.0**; earlier releases differ materially (FX existed pre-0.15.0; idempotency was application-level pre-0.13.2; precise_amount arrived at 0.10.1). Do not mix.
- Testimonial and website copy (blnkfinance.com) are promotional; treated as MAINTAINER CLAIM throughout.
- This is Volume I (domain model only). Component location (Vol II), runtime invariant verification (Vol III), and the security/threat model (Vol VII) are out of scope here and are where several of the above INFERENCE-class claims will be confirmed or falsified.

---

*End of TREF Volume I — Blnk. Volume II (component location) is NOT begun, per scope.*