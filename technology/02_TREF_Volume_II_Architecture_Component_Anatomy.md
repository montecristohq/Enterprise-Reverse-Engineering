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
# Volume II — Architecture & Component Anatomy

**Execute Volume II only. Do not begin Volume III.**

## Research Questions

### 1. System Boundary
Define what is inside/outside the system, trusted/untrusted dependencies, required/optional components, control plane, and data plane.

### 2. Component Inventory
Identify modules, services, processes, libraries, workers, schedulers, databases, caches, queues, brokers, APIs, CLIs, SDKs, background jobs, storage systems, and external providers. For each: purpose, inputs, outputs, state ownership, dependencies, failure effect, scaling behavior.

### 3. Architectural Style
Determine whether the system is monolithic, modular, microservice, event-driven, actor-based, layered, plugin-based, peer-to-peer, embedded, distributed-control-plane, or hybrid. Prove the classification.

### 4. Interfaces
Map public/internal APIs, RPC, event schemas, file/wire formats, CLI, plugin interfaces, extension points, versioning, compatibility, authentication, error semantics, and idempotency expectations.

### 5. Dependency Graph
Separate compile-time, runtime, infrastructure, protocol, SaaS, and optional dependencies. Rank criticality and replaceability.

### 6. State Ownership
For each stateful component identify authoritative state, replicas, caches, projections, lifecycle, and consistency model.

### 7. Storage Architecture
Map primary stores, metadata stores, logs, caches, object storage, search indexes, analytical stores, and why each exists.

### 8. Control Plane vs Data Plane
Where applicable, separate configuration/policy/orchestration from high-volume runtime processing.

### 9. Integration Architecture
Analyze push/pull, sync/async, webhooks/events, SDKs, adapters, connectors, import/export, and compatibility boundaries.

### 10. Deployment Topologies
Map local, single-node, clustered, cloud-managed, self-hosted, HA, multi-region, and any topology-specific component changes.

### 11. Multi-Tenancy / Isolation
Analyze namespaces, process/storage isolation, auth boundaries, resource isolation, and noisy-neighbor behavior.

### 12. Architecture Evolution
Use history, design docs, issues, and releases to identify replaced architectures, migrations, and abandoned designs.

## Required Deliverables
1. System context diagram
2. Full component diagram
3. Critical-path architecture
4. Dependency graph
5. Interface map
6. State-ownership matrix
7. Storage architecture
8. Control/data-plane map
9. Integration map
10. Deployment topology map
11. Isolation model
12. Architecture evolution
13. Critical dependencies
14. Key unknowns
15. Ten most important findings

## Final Questions
- Which components are indispensable?
- Which are commodity/replaceable?
- Where is the architectural center of gravity?
- What owns the source of truth?
- Which boundary matters most for correctness?
- What component would be hardest to replace?

**Completion test:** A reader should be able to draw the system architecture from memory and explain why every major component exists.
