# TREF — Standalone Volume Research Prompt

## Research Target

- **Technology:** [TECHNOLOGY NAME]
- **Technology type:** [DATABASE / LEDGER / PROTOCOL / FRAMEWORK / SERVICE / HARDWARE / OTHER]
- **Version / release / commit:** [VERSION]
- **Official documentation:** [URL]
- **Source repository:** [URL OR NONE]
- **Deployment model:** [SELF-HOSTED / CLOUD / BOTH / UNKNOWN]
- **License / edition:** [IF RELEVANT]
- **Research date:** [CURRENT DATE]
- **Special focus:** [OPTIONAL]

Conduct an **institutional-grade technical reverse-engineering study**. This is not a feature summary, tutorial, review, or generic architecture description. The objective is to understand the technology deeply enough to reconstruct how it works from first principles.

### Evidence labels
Use: **CONFIRMED IMPLEMENTATION**, **DOCUMENTED BEHAVIOR**, **MAINTAINER CLAIM**, **MEASURED RESULT**, **SOURCE-CODE INFERENCE**, **ANALYTICAL INFERENCE**, **HYPOTHESIS**, **UNKNOWN**.

### Depth rule
Depth follows complexity and importance, never an arbitrary length. Do not compress later sections because earlier sections were long. If output limits intervene, stop at a logical boundary and continue without compressing.

> **Completeness before concision.**

### Source priority
Prefer official spec/docs, source code, design docs, ADRs/RFCs, tests, schemas/migrations, changelogs, issues, commit history, engineering posts, official benchmarks, manifests, standards/papers, then reputable independent analysis.

### Mandatory analysis
For each material component ask **What, How, Who/What controls it, Where, When, Why**, then analyze **Structure, Flow, Control, Resource economics, Failure**.

### Mandatory trace rules
- Follow execution from input to durable effects.
- Follow state across client-visible, memory, durable, derived, cached, replicated, and external state.
- Follow failure through retries, timeouts, crashes, duplicates, partial success, and recovery.
- Follow invariants and identify exactly where each is enforced.
- Follow resource usage: CPU, memory, storage, I/O, network, locks, queues, connections, operator effort.
- If implementation is not public, do not invent it; present known facts, alternatives, and uncertainty.

---
# Volume V — Correctness, Performance, Scale, Reliability & Security

**Execute Volume V only. Do not begin Volume VI.**

## Research Questions
1. Create a correctness specification: invariants, preconditions, postconditions, valid/invalid states, enforcement layers.
2. Analyze numerical/precision semantics where relevant: integers, decimal, floating point, units, rounding, overflow.
3. Determine consistency guarantees: strong/eventual/session consistency, read-after-write, stale reads, replication behavior.
4. Analyze atomicity and isolation: transaction scope, isolation levels, serialization points, anomalies prevented/possible.
5. Stress concurrency: hot keys/entities, lock contention, optimistic conflicts, deadlocks, starvation, fairness.
6. Decompose latency into parsing, validation, application logic, reads, writes, locking, external calls, serialization, network.
7. Model throughput: unit of throughput, single-node capacity, scale-out behavior, saturation, queueing.
8. Analyze vertical/horizontal scaling, partitioning, sharding, replication, multi-region, coordination overhead.
9. Build a capacity model using CPU, memory, storage, IOPS, network, DB connections, lock contention.
10. Analyze reliability: retries, timeouts, circuit breakers, failover, health checks, redundancy, graceful degradation.
11. Analyze durability/recovery: WAL/logs, fsync assumptions, backup, restore, PITR, replication, RPO/RTO.
12. Analyze observability: logs, metrics, traces, audit logs, SLOs/SLIs, alerting, ability to diagnose correctness failures.
13. Build a defensive threat model: assets, actors, entry points, trust boundaries, abuse cases. Use STRIDE where helpful.
14. Analyze authentication, authorization, roles/scopes, service identity, tenant boundaries.
15. Analyze data security: encryption, secrets, key management, backups, sensitive logs, retention.
16. Analyze multi-tenant isolation and noisy-neighbor behavior.
17. Analyze misuse/resource exhaustion: duplicates, replay, malformed input, unbounded queries, privilege misuse.
18. Model chaos/failure scenarios: crash during commit, DB failover, network partition, disk exhaustion, clock skew, duplicate delivery, partial deployment, corrupt data, hot partition.

## Required Deliverables
Invariant matrix; precision model; consistency model; atomicity/isolation model; concurrency bottleneck map; latency model; throughput model; scalability model; capacity model; reliability map; backup/recovery model; observability map; threat model; auth/authz model; data-security model; isolation model; abuse-case map; failure-scenario matrix; key unknowns; ten most important findings.

## Final Questions
- What guarantee is strongest?
- What guarantee is weakest?
- What is the primary scaling bottleneck?
- What failure mode is most dangerous?
- What security boundary matters most?
- Under what workload does the architecture degrade first?

**Completion test:** Explain correctness, concurrency, scaling, failure, recovery, observability, and security under hostile conditions.
