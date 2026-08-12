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
# Volume IV — Implementation & Infrastructure Anatomy

**Execute Volume IV only. Do not begin Volume V.**

## Research Questions
1. Map repositories, packages, modules, binaries, generated code, tests, tools, migrations, and deployment files.
2. Analyze languages, runtimes, versions, concurrency model, memory model, and ecosystem choices.
3. Trace critical source-code paths from public interface to persistence.
4. Identify correctness/performance-critical algorithms and data structures; analyze complexity and edge cases.
5. Reconstruct database/storage schemas: tables/collections, keys, constraints, indexes, partitions, sequences, views, migrations.
6. Analyze persistence: raw SQL/ORM, transactions, connection pools, batching, retries, isolation levels, query patterns.
7. Analyze networking/protocols: HTTP/RPC, serialization, compression, timeouts, retries, backpressure, versioning.
8. Identify workers, schedulers, async jobs, maintenance, compaction, reconciliation, cleanup.
9. Map configuration, environment variables, feature flags, secrets, defaults, and dangerous combinations.
10. Analyze build, tests, CI, packaging, releases, semantic compatibility, and migrations.
11. Reconstruct deployment: processes, containers, orchestration, service discovery, load balancing, storage, health checks, autoscaling.
12. Map infrastructure dependencies and minimum viable infrastructure.
13. Build a build-vs-buy-vs-open-source matrix.
14. Treat tests as executable specification: find edge cases, invariants, concurrency behavior, historical regressions, and undocumented contracts.

## Required Deliverables
Repository map; language/runtime map; critical code paths; algorithm/data-structure catalog; schema diagram; persistence model; protocol map; background-job map; configuration map; build/release pipeline; deployment topology; infrastructure dependency map; build-vs-buy matrix; tests-as-spec findings; key unknowns; ten most important findings.

## Final Questions
- Which implementation choice is most fundamental?
- Which dependency is most operationally important?
- Where is domain correctness actually enforced?
- What is the likely performance-critical code path?
- Which implementation details are incidental and which are fundamental?

**Completion test:** Connect the conceptual architecture to concrete code, schema, runtime, and deployment mechanisms.
