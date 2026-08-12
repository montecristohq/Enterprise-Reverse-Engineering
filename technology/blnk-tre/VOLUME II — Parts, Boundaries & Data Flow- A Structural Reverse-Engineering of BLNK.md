# VOLUME II — Parts, Boundaries & Data Flow: A Structural Reverse-Engineering of BLNK

```
Technology:              Blnk — open-source double-entry financial ledger
Technology type:         LEDGER
Primary repository:      https://github.com/blnkfinance/blnk  (the ledger core — THIS is the subject)
Client SDK:              https://github.com/blnkfinance/blnk-go  (Go client; client interface contract)
Version / release:       v0.15.0 (22 June 2026) pinned; patch line to v0.15.2 (31 July 2026)
Commit / tag:            tag v0.15.0; ~604 commits / 54 releases observed 11 August 2026
Official documentation:  docs.blnkfinance.com (Mintlify); repository README
Source openness:         OPEN SOURCE — Apache-2.0 ("Blnk Core"); open-core, Blnk Cloud commercial
Deployment model:        BOTH — self-hosted (bring your own PostgreSQL) or managed Blnk Cloud
Research date:           11 August 2026
Study objective:         BUILD EXTRACTION
Configuration:           EXTENDED 7 (Volume VII — Security & Threat Model — commissioned)
```

## TL;DR

- **Blnk is a modular monolith compiled to a single Go binary that runs as two-to-three process roles (API server, worker, one-shot migration) over one shared PostgreSQL source of truth, with Redis (via the `hibiken/asynq` library) owning both the transaction queue and the distributed locks, and Typesense as an optional search projection.** PostgreSQL is the architectural centre of gravity and the single component that is genuinely hard to replace; Redis is on the correctness path (not a cache) because it holds the locks that serialise balance mutation.
- **The confirmed structural facts close most of Volume I's gaps: money moves through `model.Transaction` (fields `PreciseAmount`, `Amount float64`, `Precision float64`) and balances are cached running totals in `model.Balance` with an optimistic-lock `Version` field. But the single most important schema fact — the PostgreSQL column type for `precise_amount` and the balance fields — could NOT be confirmed even with a targeted attempt**, because the repository's `sql/` directory (embedded via `embed.FS` as `SQLFiles` in `blnk.go`) is served only through GitHub tree/raw endpoints that block automated access. Best inference remains NUMERIC (arbitrary precision), strongly supported by the v0.15.0 move to `*big.Int` and the maintainer's own rationale that `precise_amount` was added to "seamlessly manage amounts larger than 15 digits" (Blnk Core v0.10.1 blog) — but it is INFERENCE, not CONFIRMED.
- **For a cooperative-society savings platform: Blnk gives you double-entry integrity, immutability, idempotency and per-transaction hashing, but it provides essentially NO tenant isolation beyond ledger partitioning and API-key scoping** — one PostgreSQL, one Redis, one namespace shared by all societies. Noisy-neighbour and blast-radius risk is real and must be handled by you at the deployment layer, not by Blnk.

## Key Findings

1. **Architectural style is a modular monolith, proven from the layout and the process model, not the README.** The repository is a flat Go package (`package blnk`) at the root with ~40 sibling `.go` files (`transaction.go`, `balance.go`, `queue.go`, `reconciliation.go`, `apikey.go`, `webhooks.go`, `search.go`, `chain_worker.go`, `lineage_*.go`), plus subpackages `api/`, `model/`, `config/`, `database/`, `cmd/`, and `internal/` (with `lock`, `notification`, `pg-backups`, `pg-listener`, `redis-db`, `request`, `apierror`, `cache`). The `docker-compose.yaml` runs the **same image** as both `server` (`blnk migrate up && blnk start`) and `worker` (`blnk workers`) — CONFIRMED single binary, multiple process roles.

2. **PostgreSQL is the source of truth and the hardest-to-replace component.** All authoritative state (ledgers, balances, transactions, identities, API keys, reconciliation) lives in Postgres, accessed through a `database.IDataSource` interface. The schema is embedded in the binary (`var SQLFiles embed.FS` in `blnk.go`) and applied by `blnk migrate up`.

3. **Redis is on the correctness path, not a cache.** The `Queue` type wraps `*asynq.Client` and `*asynq.Inspector` (`github.com/hibiken/asynq`), so Redis is the transaction queue; `internal/lock` provides the distributed lock that serialises balance updates. If Redis is down, queued processing and lock acquisition stop — this is a correctness-and-liveness dependency, not a performance nicety.

4. **The money model is confirmed at the Go struct level.** `model.Transaction` carries `PreciseAmount` (integer minor units — `int64` in the 2024 source, migrated to `*big.Int` by v0.15.0), a convenience `Amount float64`, and `Precision float64`. `model.Balance` carries `Balance`, `CreditBalance`, `DebitBalance`, `InflightBalance`, `InflightCreditBalance`, `InflightDebitBalance` (all integer minor units) plus `Version int64` for optimistic locking and a `CurrencyMultiplier float64` serialised as `precision`. Balance responses do not return precision — CONFIRMED in docs ("Blnk Core does not return precision on balance responses").

5. **The v0.15.0 conservation hardening is visible as a struct-level deletion.** The 2024 source carried a `Rate float64` field and an `ApplyRate()` function on transactions; the carried-forward v0.15.0 note records the removal of `rate`, `currency_multiplier` and `modification_ref` from the transaction path. This is the mechanism by which INV-1 (conservation) was hardened: asymmetric posting was removed, not merely discouraged.

6. **Transaction lifecycle and immutability are structural.** Status constants are `QUEUED`, `SCHEDULED`, `INFLIGHT`, `APPLIED`, `VOID`, `REJECTED` (`transaction.go`). New states are written as new rows linked by `parent_transaction`; the public API exposes `UpdateTransactionStatus` and `VoidInflightTransaction`/`CommitInflightTransaction` but no method that overwrites a posted transaction's amount, source or destination. Docs confirm: "Once recorded, transactions in Blnk cannot be modified or deleted."

7. **Per-transaction hashing is a method on the model; the chain is a separate worker.** `model.Transaction.HashTxn()` computes the SHA-256 hash; `chain_worker.go` (with `chain_worker_test.go`) is the global hash-chain subsystem, and `blnk verify-chain` is the CLI verifier. Tamper-evidence (INV-11) is therefore owned by two components: the model (per-row hash) and the chain worker (linkage).

8. **Idempotency is enforced at two layers.** The application requires a unique `reference` — docs state verbatim: "Blnk implements idempotency by requiring a unique `reference` for every transaction. This reference serves as a transaction identifier, preventing duplicate processing and ensuring consistent outcomes." Since v0.13.2 a database unique index `idx_transactions_reference_unique` backstops it at the storage layer — so a duplicate reference is rejected even under a race that slips past the application check.

9. **Search is optional and is a projection, not a source of truth.** `internal/pg-listener` listens to Postgres change notifications and `TypesenseClient.HandleNotification` pushes them into Typesense collections built by `EnsureCollectionsExist`. Since v0.13.2 a direct-DB filter search path exists, so Typesense can be removed entirely without affecting money movement.

10. **The `blnk-go` client contract encodes the money model correctly but leans on caller discipline.** It exposes `PreciseAmount: big.NewInt(...)` and a separate `Amount`/`Precision`, mirroring the REST surface; the danger it does not remove is that a caller can still send the float `Amount` with a wrong `Precision` and get a silently wrong `precise_amount`.

## Details

### II.1 System boundary; what Blnk Cloud is

**Inside Blnk Core (trusted, in-process):** the HTTP API layer (`api/`, `api/middleware/`, `api/model/`), the transaction engine (`transaction*.go`), the balance engine (`balance.go`, `model/balance.go`), the queue/worker layer (`queue.go`, `transaction_queue.go`, `queue_recovery.go`), the database access layer (`database/`), reconciliation (`reconciliation*.go`), lineage/shadow-ledger (`lineage_*.go`), identity/tokenization (`identity.go`), hashing/chain (`model.HashTxn`, `chain_worker.go`), API-key management (`apikey.go`), webhooks (`webhooks.go`), search (`search.go`), config (`config/`), CLI (`cmd/`), and migrations (`sql/` embedded).

**Outside Blnk Core (trusted infrastructure, separate processes):** PostgreSQL (required), Redis (required), Typesense (optional), Jaeger/OpenTelemetry collector (optional observability). **Untrusted:** all API callers and webhook receivers.

**Control plane vs data plane:** weakly distinguished. Configuration/orchestration (`blnk.json`, `blnk migrate up`) is separable from runtime processing, but there is no separate policy/management service in Core — the API binary is both.

**Blnk Cloud** is the commercial managed plane. Architecturally it is a hosted dashboard/control surface over Core data. The reader-flagged "Query Agent" that connects a managed plane to a self-hosted Core is a read-oriented connector: the docs say "Connect to Blnk Cloud to see your Core data. You can view your transactions, manage identities, create custom reports, invite other team members to collaborate, and perform operations on your Core." Core does not depend on Blnk Cloud in any way — self-hosted Core runs fully standalone. Exactly what the agent can write is not fully documented; treat write scope as UNKNOWN and assume it should be given a scoped, least-privilege API key.

### II.2 Component inventory (selected; state ownership in bold)

- **HTTP API layer** — `api/`, built on Gin (SOURCE-CODE INFERENCE from Gin routing idioms and the `blnk-go` REST surface). Inputs: REST calls with `X-blnk-key`. Outputs: JSON. **State: none (stateless).** Fails → no ingress; workers keep draining the queue.
- **Transaction engine** — `transaction.go` and siblings (`_execution`, `_inflight`, `_queue`, `_batch_processing`, `_bulk`, `_refunds`, `_rejection`, `_coalescing`, `_queries`). **State: owns transaction rows (write-once).** Core of INV-1/5/6/7/10.
- **Balance engine** — `balance.go`, `model/balance.go`. Methods `CommitInflightCredit/Debit`, `RollbackInflightCredit/Debit`, `UpdateBalances`. **State: owns the cached running-total balance rows + `Version`.** Core of INV-2/3/8/9.
- **Queue/worker** — `queue.go` (`Queue{Client *asynq.Client; Inspector *asynq.Inspector}`), `NumberOfQueues = 20`, queues `new:transaction`, `new:webhoook`, `new:inflight-expiry`. **State: Redis-resident job state + queued balance estimates.** `queue_recovery.go` recovers stuck-QUEUED transactions.
- **Database layer** — `database/`, `database.IDataSource`. **State: gateway to the authoritative store.**
- **Reconciliation** — `reconciliation.go` (+ engine/matching/rules tests). Ingests external files, matches to ledger. **State: reconciliation results in transaction `meta_data`** (e.g. `BLNK_RECONCILIATION_RESULT` with `recalculated_balance`).
- **Lineage / shadow ledger** — `lineage_*.go` (`_allocation`, `_credit`, `_debit`, `_outbox`, `_processing`, `_queries`, `_shadow`, `_worker`). Fund-provenance tracking; `LedgerBalance.GetLineage` surfaces received/spent/available. **State: allocation/lineage rows; uses an outbox pattern.**
- **Identity & tokenization** — `identity.go`, `model/identity.go` (PII fields). **State: identity rows + tokenized PII.**
- **Hashing / chain** — `model.HashTxn()` + `chain_worker.go`. **State: per-row hash + chain linkage.**
- **API-key management** — `apikey.go`. **State: hashed keys + scopes + owner binding.**
- **Webhooks** — `webhooks.go` (`SendWebhook`, `ProcessWebhook` via asynq). **State: none authoritative; delivery via queue.**
- **Search** — `search.go`, `TypesenseClient`; fed by `internal/pg-listener`. **State: Typesense projection (disposable).**
- **Config/CLI/migrations** — `config/`, `cmd/`, `sql/` (embedded `SQLFiles`).
- **Internal shared** — `internal/lock` (distributed lock), `internal/redis-db`, `internal/pg-listener`, `internal/pg-backups`, `internal/notification`, `internal/request`, `internal/apierror`, `internal/cache`.

### II.3 Architectural style — PROVEN

Modular monolith. Evidence: (1) one root Go package with many sibling files sharing internal state through the `Blnk` struct (`NewBlnk(db database.IDataSource)`); (2) one Docker image invoked with different entrypoints (`blnk start` vs `blnk workers` vs `blnk migrate up`); (3) the worker system is in-process asynq consuming from Redis, not a separate service with its own API. A running Blnk is therefore **1 binary in 2 long-lived process roles** (API + worker) plus a **one-shot migration job**. It is event-driven/worker-queue *internally* (asynq over Redis) but monolithic in packaging.

### II.4 Interfaces

- **REST API** — resources: `/ledgers`, `/balances`, `/balance-monitors`, `/transactions` (+ `/transactions/bulk`, `/transactions/inflight`, `/transactions/refund`, `/transactions/reference/{ref}`, `/transactions/recover?threshold=`), `/identities`, `/reconciliation`, `/search`, `/health`. Auth via `X-blnk-key`. QUEUED transactions get a `_q` reference suffix — docs verbatim: "Blnk appends a `_q` suffix to your original reference after processing a `QUEUED` transaction." No explicit URL version prefix (unversioned; compatibility managed by release).
- **Queue message contract** — `TransactionTypePayload{Data model.Transaction}` enqueued to `new:transaction`; webhook payloads to `new:webhoook`; inflight-expiry to `new:inflight-expiry`.
- **Webhook contract** — `NewWebhook{Event string; Payload interface{}}`; HMAC signing since v0.13.0 (SHA-256 signature in header — DOCUMENTED BEHAVIOR).
- **CLI** — `blnk migrate up`, `blnk start`, `blnk workers`, `blnk verify-chain`, plus collection listing.
- **Config schema** — `blnk.json`: `data_source.dns`, `redis.dns`, `typesense.dns`, `server{port,ssl,domain,ssl_email}`, `notification.slack.webhook_url`, `queue.monitoring_port` (default 5004).
- **`blnk-go` client contract** — `NewClient(baseURL, apiKey, WithTimeout, WithRetry)`; services `Ledger`, `LedgerBalance` (incl. `GetLineage`), `Transaction` (incl. `BulkCommitInflight`, `BulkVoidInflight`), `Identity`, `Reconciliation`, `BalanceMonitor`, `System.health`. Money passed as `PreciseAmount big.NewInt(...)` alongside `Amount`/`Precision`. It mirrors the REST surface faithfully and hides HTTP retry/timeout; the risk it leaves open is the `Amount × Precision` → `precise_amount` conversion, which a caller can still get wrong.

### II.5 Dependency graph (from imports; `go.mod` not opened directly)

- **Runtime/protocol (critical):** `github.com/hibiken/asynq` (Redis queue + locks foundation), `github.com/typesense/typesense-go` (optional search), a PostgreSQL driver (pgx/lib-pq — SOURCE-CODE INFERENCE), Gin (HTTP — INFERENCE), `go.opentelemetry.io/otel` + Jaeger exporter (observability).
- **Compile-time:** Go stdlib `math/big` (money), `crypto/sha256` (hashing), `embed` (schema embedding).
- **Criticality ranking:** PostgreSQL driver > asynq/Redis > Gin > OTel > typesense-go. Replaceability: OTel and Typesense easy; Gin moderate; asynq hard (queue + lock semantics); Postgres driver hard (SQL coupling).

### II.6 Rented vs owned

| Dependency | Owned/Rented | If it disappears | Substitute | Migration cost |
|---|---|---|---|---|
| PostgreSQL | Rented (self-run or managed) | Ledger stops; source of truth gone | None like-for-like | Prohibitive — schema + SQL coupling |
| Redis | Rented | Queue + locks stop; balance mutation halts | Any asynq-compatible Redis | Low if drop-in Redis; high to swap the lib |
| Typesense | Rented (optional) | Search degrades; DB-filter fallback | Direct-DB search (v0.13.2+) | Low |
| asynq (lib) | Owned dep on correctness path | Rewrite queue/lock | River, Machinery, custom | High |
| Blnk Cloud | Rented (optional) | Dashboard only; Core unaffected | Self-host UI | None for Core |

A dependency that cannot be replaced is an architectural feature: **Postgres and the asynq/Redis pairing define Blnk's correctness envelope.**

### II.7 Single points of failure

- **Postgres unavailable:** total halt — no reads, no writes, no balance updates. Not graceful. Recovery: restore/failover Postgres; migrations idempotent.
- **Redis unavailable:** queued-by-default processing stops and locks cannot be acquired, so balance-mutating transactions stall. API may still accept and enqueue-attempt but cannot complete. Blast radius: all money movement. v0.15.2 added a `QUEUE_BACKPRESSURE` 503 so the API sheds load rather than silently backing up.
- **Typesense unavailable:** search only; money movement unaffected (graceful). DB-filter fallback exists.
- **Worker crash mid-transaction:** queue redelivery (asynq) + `queue_recovery.go` recover stuck-QUEUED work — docs: "Blnk now automatically checks for and recovers any transactions stuck in queue... You can also trigger recovery manually with the Queue Recovery endpoint" (`POST /transactions/recover?threshold=5m`, minimum 2 minutes). Per-transaction hash + immutability prevent partial-state corruption because state changes are new rows.

### II.8 State ownership

Authoritative balance lives in **one place: the PostgreSQL `balances` row**, protected by optimistic locking on `Version`. Redis holds *queued balance estimates* (`queued_credit_balance`/`queued_debit_balance`, since v0.8.3) and the *lock* — it is a coordination and estimation store, not an authoritative balance store. This is the one place two components *could appear* to own balance: Redis's queued estimates vs Postgres's committed balance. The design keeps them distinct (estimates are explicitly labelled "queued" and are not the balance), so there is no true dual-ownership — but an operator who reads queued estimates as authoritative would create a correctness illusion. Typesense and the OTel pipeline are pure projections.

### II.9 Storage architecture — the money-type question, answered honestly

Tables (reconstructed from models and ID prefixes): `ledgers` (`ldg_`), `balances` (`bln_`), `transactions` (`txn_`), `identities` (`idt_`), `balance_monitors`, plus reconciliation, lineage/allocation, and API-key tables. Confirmed columns on `transactions` (from a repo test's `SELECT`): `transaction_id, parent_transaction, source, reference, amount, precise_amount, precision, rate, currency, destination, description, status, created_at, meta_data, scheduled_for, hash`.

**The Postgres column type for money remains SOURCE-CODE INFERENCE, not CONFIRMED — this is itself a Volume II finding.** A targeted attempt to open the `sql/` directory (embedded as `SQLFiles embed.FS`) failed: GitHub's tree/blob/raw endpoints block automated retrieval, and no search index surfaced the verbatim `CREATE TABLE`. The strongest inference:

- `precise_amount`: **NUMERIC (arbitrary precision)** — supported by the v0.15.0 migration to `*big.Int` (which exceeds BIGINT's 19-digit range) and the maintainer's stated goal, verbatim from the Blnk Core v0.10.1 blog: "We initially introduced precision for developers to handle decimal amounts, but this was capped at a maximum of 15 digits. With this update, we've added a new transaction parameter, precise_amount, enabling developers to seamlessly manage amounts larger than 15 digits in their financial applications." A repo DB test passes `precise_amount` as a string ("100000") and `amount` as a float (1000.0), consistent with NUMERIC and DOUBLE PRECISION respectively.
- Balance money fields (`balance`, `credit_balance`, `debit_balance`, `inflight_*`): integer minor units in Go (`int64`, migrating to big.Int); Postgres type most likely **NUMERIC** to match precise_amount and hold >19-digit values; **BIGINT** cannot be excluded for older columns.
- `version`: integer optimistic-lock counter (BIGINT/INTEGER).
- Whether the DB itself constrains precision, sign or magnitude (CHECK constraints): **UNKNOWN / none found.** Negative balances are explicitly allowed (overdrafts), so a non-negativity CHECK on `balance` is unlikely.

`idx_transactions_reference_unique` (v0.13.2) enforces idempotency at the storage layer; its exact predicate (partial? `CONCURRENTLY`?) is **UNKNOWN**.

### II.10 Control plane vs data plane

Weakly separated. If the management/config surface is unavailable, in-flight money movement continues (workers drain Redis, Postgres commits) because configuration is read at process start from `blnk.json`. There is no runtime policy service whose outage would stop postings. Blnk Cloud's outage has zero effect on Core.

### II.11 Integration architecture

- **Synchronous push:** REST (`X-blnk-key`).
- **Asynchronous:** internal asynq queue; outbound webhooks (HMAC-signed since v0.13.0); balance monitors with callback URLs.
- **Pull:** REST GETs; Search API; historical balance API (`/balances/{id}/at?timestamp=`).
- **File ingestion:** reconciliation upload → matching rules → strategies (one-to-one, one-to-many, many-to-one).
- **Import/export:** bulk transactions with `effective_date` backdating (v0.9.0+), `atomic` and `run_async` flags. Blnk's docs describe the Bulk Transaction API as "process multiple transactions within a single request"; the "1,000–5,000 per batch" figure is a *recommendation* in Blnk's Data Migration guide, not an enforced cap, and no fixed limit is documented.
- **SDKs:** Go (`blnk-go`), TypeScript (`blnk-ts`), Java (`blnk-java`).
- **Compatibility boundary:** unversioned REST; behaviour changes are release-gated (e.g. exchange-rate removal at v0.15.0). This is a real risk — pin the server version.

### II.12 Deployment topologies

- **Local / single-node:** `docker compose up` — services `server`, `worker`, `redis`, `postgres:16`, `typesense:29.0`, `jaeger`.
- **Docker Compose (documented):** server runs `blnk migrate up && blnk start`; worker runs `blnk workers`; shared `blnk.json`. Docs describe Blnk as "a distributed system with three core components: API Server... Worker... Migration Service" plus supporting infra (PostgreSQL, Redis, Typesense, optional Jaeger).
- **Kubernetes:** `infrastructure/k8s-manifests/` in-repo; separate `blnk-infrastructure` repo provides Terraform (AWS/Azure/GCP) + k8s/Helm (community-maintained by contributor iamtito).
- **Managed:** Blnk Cloud.
- **What changes by topology:** Typesense and Jaeger appear/disappear as optional; the migration step is a one-shot job; API and worker scale independently (both stateless w.r.t. authoritative state — state is in Postgres/Redis), so **horizontal scaling of API and workers is supported**, bounded by Postgres write throughput and the Redis lock. Scaling requires a shared Redis and Postgres (no in-memory affinity).

### II.13 Multi-tenancy and isolation — critical for the reader

**Blnk provides NO tenant isolation beyond ledger partitioning and API-key scoping.** There are no per-tenant namespaces, no per-tenant databases, no resource quotas, no noisy-neighbour controls in Core. All cooperative societies would share one Postgres, one Redis queue (20 logical asynq queues, but shared infrastructure), one Typesense index. API keys are SHA-256-hashed at rest (v0.12.0), scoped (e.g. `transactions:write`), and owner-bound (v0.14.3) — that governs *authorisation*, not *isolation*. A heavy batch from one society competes for the same Redis queue and Postgres locks as every other. For members' savings, this means: **Blnk will enforce double-entry, immutability, idempotency and overdraft rules per balance, but it will NOT enforce fairness, blast-radius containment, or data-plane isolation between societies — you must provide that (separate deployments per society or per tier, or strict quotas at your gateway).**

### II.14 Architecture evolution

- **Queue-by-default processing:** transactions are enqueued (`QUEUED` → `_q` suffix) and applied by workers. This decoupled ingestion from accounting, enabling burst absorption — at the cost of eventual-consistency semantics (a caller must poll or await webhook for `APPLIED`). v0.15.2's `QUEUE_BACKPRESSURE` 503 and the queue-recovery endpoint are the maturation of this choice.
- **DB-level unique index (v0.13.2):** moved idempotency from application-only to storage-enforced — closing the race window. This made idempotency robust under concurrency but requires the reference column to be genuinely unique (a constraint on import/replay design).
- **Exchange-rate removal (v0.15.0):** deleted `rate`/`currency_multiplier`/`modification_ref` from the transaction path (the 2024 source's `Rate float64` + `ApplyRate()` are gone). This hardened conservation (INV-1) by making asymmetric posting structurally impossible; the cost is that multi-currency conversion must now be modelled as explicit two-leg transactions.
- **`precise_amount` + `*big.Int` migration:** from `int64` (2024) to arbitrary precision, enabling amounts larger than 15 digits.
- **Direct-DB filter search (v0.13.2):** reduced hard dependence on Typesense.
- **API-key hardening:** hashed at rest (v0.12.0), owner-bound (v0.14.3).

### II.15 INVARIANT LOCATION TABLE — the spine

| # | Invariant | Volume I claimed point | Actual component / file / function | Evidence |
|---|---|---|---|---|
| INV-1 | Conservation (dest credit = src debit) | Transaction engine | `transaction.go` posting + `model.UpdateBalances`; hardened by removal of `Rate`/`ApplyRate` at v0.15.0 | SOURCE-CODE INFERENCE (struct deletion CONFIRMED) |
| INV-2 | Balances change only via transactions | Balance engine | `balance.go` / `model/balance.go`; no public balance-mutation API except via transactions | CONFIRMED (API surface) |
| INV-3 | Balance derivability from history | Transaction history + reconciliation | `transaction_queries.go`, historical balance API, `reconciliation.go` recalculated_balance | DOCUMENTED BEHAVIOR |
| INV-4 | Idempotency (unique reference) | App-level reference | App check ("requiring a unique reference for every transaction") + DB unique index `idx_transactions_reference_unique` (v0.13.2) | CONFIRMED (docs) + INFERENCE (index DDL UNKNOWN) |
| INV-5 | Immutability of posted transactions | Transaction engine | New `parent_transaction`-linked rows; no field-overwrite API; docs "cannot be modified or deleted" | CONFIRMED (API surface + docs) |
| INV-6 | Valid state transitions only | Transaction engine | Status constants + `_inflight`/`_rejection`/`_refunds` handlers | CONFIRMED (constants) |
| INV-7 | Precision integrity (integer minor units) | Money model | `model.Transaction.PreciseAmount` (`big.Int`), `ApplyPrecision` → int64; `math/big` | CONFIRMED (Vol I) + SOURCE-CODE INFERENCE |
| INV-8 | Sufficient funds unless overdraft | Balance engine | `balance.go`: available = `balance − inflight_debit_balance` on source; else `REJECTED` (v0.11.0+); inflight included | DOCUMENTED BEHAVIOR |
| INV-9 | Concurrency safety | Redis lock + PG optimistic lock | `internal/lock` (Redis) + `model.Balance.Version` | CONFIRMED (struct + package) |
| INV-10 | Zero/malformed rejected | Transaction engine | `transaction_rejection.go`; docs: "Zero amounts are not recorded in the Blnk ledger" | DOCUMENTED BEHAVIOR |
| INV-11 | Tamper-evidence | Hash + chain | `model.Transaction.HashTxn()` (SHA-256) + `chain_worker.go` + `blnk verify-chain` | CONFIRMED (method + file) |
| INV-12 | Authorisation & tenancy | API keys | `apikey.go` — hashed (v0.12.0), scoped, owner-bound (v0.14.3); **no tenancy isolation component exists** | CONFIRMED (file) / tenancy UNOWNED |

**No component owns tenant isolation.** INV-12's "tenancy" half is enforced only by convention (ledger partitioning + key scoping), not by an isolation subsystem.

### II.16 Falsification watch

- **Target 1 — authoritative money as float64:** NOT FOUND. Authoritative money is `precise_amount` (`big.Int`/integer minor units); `Amount float64` is a convenience input only, and `ApplyPrecision` returns `int64`. **Volume I money model survives.** (Caveat: not falsified, but not fully closed either — the DB column type is unconfirmed, so a float storage column cannot be 100% ruled out from DDL. Inference strongly against it.)
- **Target 2 — mutation of a posted transaction's financial fields:** NOT FOUND. No API or code path overwrites amount/source/destination/status in place; state changes create new `parent_transaction`-linked rows. **INV-5 survives.**
- **Target 4 — dest credit ≠ src debit in v0.15.0+:** NOT FOUND. The exchange-rate/asymmetric path (`Rate`, `ApplyRate`) was removed at v0.15.0. **INV-1 survives and was structurally hardened.**

No Volume I claim was falsified. The method's honest result is a partial gap, not a contradiction: the schema money type is still inference.

### II.17 Build-extraction verdicts

- **Single-Postgres source of truth — ADOPT.** Works because of the mechanism (one ACID store = one truth), not the environment. Directly transferable to a cooperative-society ledger. Benchmark to change: if write throughput exceeds one Postgres primary's capacity, shard by society/deployment rather than adding balance stores.
- **Redis lock-and-queue (asynq) — ADAPT.** The queue-by-default design is sound, but it makes Redis a correctness dependency. For members' savings, **ADAPT**: run Redis in HA (Sentinel/managed), monitor `QUEUE_BACKPRESSURE`, and decide explicitly whether you want synchronous (inline) posting for small societies to avoid eventual-consistency surprises. What must change: Redis from single-node to HA; add alerting on queue depth and lock wait.
- **Modular-monolith packaging — ADOPT.** The single-binary/multi-role model is simple to operate and scales horizontally on stateless roles. Transferable regardless of team size.
- **Optional-Typesense pattern — ADOPT.** Clean projection with a DB fallback; keep it optional and off unless you need free-text search.
- **API-key scoping model — ADAPT.** Hashed + scoped + owner-bound is good, but it is authorisation, not isolation. **ADAPT for multi-society:** you must add tenant separation above Blnk (deployment-per-society or per-tier, plus gateway quotas). A REJECT of "one shared instance for all societies without quotas" is warranted for real member savings.

### II.18 Reconstruction summary

1. **System context:** Callers → API (X-blnk-key) → Core binary → Postgres (truth) + Redis (queue/lock) + Typesense (optional) + OTel (optional); Blnk Cloud reads Core.
2. **Component diagram:** root `package blnk` + `api/model/config/database/cmd/internal` subpackages; asynq worker in-process.
3. **Critical path:** POST /transactions → enqueue (Redis) → worker acquires lock (internal/lock) → validate → write txn row + update balance (version-checked) → hash → webhook.
4. **Dependency graph:** Postgres driver > asynq/Redis > Gin > OTel > Typesense.
5. **Rented vs owned:** Postgres + asynq/Redis irreplaceable; Typesense/Cloud/OTel disposable.
6. **SPOF map:** Postgres (total), Redis (money-movement), Typesense (search only).
7. **Interface map:** REST (unversioned) + asynq queue + webhooks (HMAC) + CLI + `blnk.json`; `blnk-go` mirrors REST.
8. **State-ownership matrix:** Postgres = authoritative; Redis = locks + queued estimates; Typesense/OTel = projections.
9. **Storage architecture:** tables named; money column type = NUMERIC (INFERENCE, not confirmed — GitHub blocked DDL retrieval).
10. **Control/data plane:** weakly separated; config outage does not stop postings.
11. **Integration map:** sync REST + async queue/webhooks + file reconciliation + bulk import.
12. **Deployment topology:** compose (server/worker/redis/postgres/typesense/jaeger); k8s manifests; Blnk Cloud.
13. **Isolation model:** ledger partitioning + API-key scoping ONLY; no data-plane isolation.
14. **Architecture evolution:** queue-by-default, DB unique index (v0.13.2), rate removal (v0.15.0), big.Int migration, key hardening.
15. **Invariant→component map:** see II.15; tenancy unowned.
16. **Falsification watch:** none falsified; schema money type still inference.
17. **Build-extraction verdicts:** see II.17.
18. **Key unknowns:** exact money column DDL; `idx_transactions_reference_unique` predicate; Blnk Cloud Query Agent write scope; whether any CHECK constraints exist.

**Which components are indispensable and which are commodity?** Indispensable: PostgreSQL and the asynq/Redis queue-and-lock pair. Commodity: Typesense, Jaeger/OTel, Blnk Cloud, the SDKs. **Centre of gravity:** the PostgreSQL source of truth, guarded by optimistic locking on `Version`. **What owns the source of truth:** the `database` layer over one Postgres. **Rented and breaks if gone:** Postgres (total halt) and Redis (money movement halts). **Boundary that matters most for correctness:** the transaction/balance write path where the Redis lock + Postgres `Version` together serialise mutation. **Hardest to replace:** PostgreSQL (schema + SQL coupling), then the asynq/Redis lock-queue semantics.

## Recommendations

1. **Before production for members' savings, confirm the money column DDL yourself.** Clone the repo and open `sql/` (the embedded `SQLFiles`) directly — verify `precise_amount` and every balance field is NUMERIC (or BIGINT) and never `double precision`/`float`. This is the single most important schema fact and Volume II could only infer it. Threshold to proceed: DDL shows an exact-decimal type for all authoritative money columns.
2. **Isolate tenants at the deployment layer.** Because Blnk enforces no data-plane isolation, run **one Blnk deployment (and Postgres/Redis) per society, or per risk tier**, rather than one shared instance. Change this only if you add hard per-tenant quotas at your gateway and accept shared blast radius. Benchmark: if a single society can saturate the Redis queue or Postgres write lock, isolation is mandatory.
3. **Run Redis and Postgres in HA and treat both as correctness infrastructure.** Redis Sentinel/managed + Postgres primary/replica with tested failover. Alert on `QUEUE_BACKPRESSURE` 503s and on queue depth; wire the queue-recovery endpoint (`/transactions/recover`, threshold ≥ 2m) into ops.
4. **Pin the server version and gate upgrades.** The REST surface is unversioned and behaviour changed materially at v0.15.0 (rate removal). Pin to a tested tag; test bulk-import/replay against the DB unique index before upgrading.
5. **Decide sync vs async posting explicitly.** Queue-by-default means `APPLIED` is eventual; for savings, either await the webhook/poll the `_q` reference before confirming to a member, or evaluate inline posting for low-volume societies.
6. **Give Blnk Cloud (if used) a least-privilege, scoped key** and treat the Query Agent's write scope as unknown until verified.

## Caveats

- **The Postgres money column type is INFERENCE, not CONFIRMED.** GitHub tree/blob/raw endpoints blocked automated retrieval of `sql/`, and no index surfaced the verbatim `CREATE TABLE`. NUMERIC is the strongly-supported best inference (big.Int migration + the maintainer's ">15 digit" rationale), but Volume I's gap is only *narrowed*, not fully closed.
- **Several struct-level facts come from the `northstar-pay/nucleus` fork at commit 1cb559337258 (Aug 2024)**, a faithful Blnk mirror that pkg.go.dev had indexed. Where v0.15.0 differs (notably `PreciseAmount int64` → `*big.Int` and the removal of `Rate`), I have stated the release explicitly. Do not read the 2024 struct as the v0.15.0 struct.
- **Gin as the HTTP framework and the exact Postgres driver are SOURCE-CODE INFERENCE**, not opened in `go.mod`.
- **`idx_transactions_reference_unique` predicate, any CHECK constraints, and the Blnk Cloud Query Agent's write scope are UNKNOWN.**
- **HMAC webhook signing (v0.13.0) is DOCUMENTED BEHAVIOR**, not verified in `webhooks.go` source line-by-line.
- Volume III should verify at runtime what this volume located structurally — especially conservation under concurrency, the unique-index race behaviour, and whether queued balance estimates ever diverge from committed balances.