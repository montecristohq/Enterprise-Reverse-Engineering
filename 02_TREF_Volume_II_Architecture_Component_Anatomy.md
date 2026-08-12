# TREF VOLUME II — ARCHITECTURE & COMPONENT ANATOMY

**Standalone research prompt. Send together with `TREF_CONVENTIONS.md`, which is binding and is not repeated here.**

Conduct an institutional-grade technical reverse-engineering study.

## Subject header
*Reproduce §0 from the instantiated conventions.*

## This volume
**Owned question:** *What are the parts, where do the boundaries fall, and what talks to what?*
**Execute Volume II only.** Do not begin Volume III.

## Evidence ceiling
*State what the source-openness position permits in this volume.*

## Carried forward
*Restate Volume I — the domain model, the core abstractions, **the numbered invariant catalogue**, the assumptions and the falsification test.*

## Re-cut *(optional)*

---

### 1. System boundary
What is inside and outside the system; trusted and untrusted dependencies; required and optional components; control plane and data plane.

### 2. Component inventory
Modules, services, processes, libraries, workers, schedulers, databases, caches, queues, brokers, interfaces, command-line tools, software development kits, background jobs, storage systems, external providers.

For each: purpose, inputs, outputs, state ownership, dependencies, failure effect, scaling behaviour.

### 3. Architectural style
Monolithic, modular, microservice, event-driven, actor-based, layered, plugin-based, peer-to-peer, embedded, distributed-control-plane, or hybrid. **Prove the classification from evidence** rather than asserting it.

### 4. Interfaces
Public and internal interfaces, remote procedure calls, event schemas, file and wire formats, command-line tools, plugin interfaces, extension points, versioning, compatibility, authentication, error semantics, idempotency expectations.

### 5. Dependency graph
Separate compile-time, runtime, infrastructure, protocol, hosted-service and optional dependencies. Rank criticality and replaceability.

### 6. What is rented rather than owned
**Establish which parts of the system the project does not control** — hosted services, proprietary protocols, single-vendor components, upstream projects with divergent governance, licensed technology.

For each: what breaks if it disappears or changes terms, whether a substitute exists, and what the migration would cost. **A dependency that cannot be replaced is an architectural feature, not a footnote.**

### 7. Single points of failure
**Trace every path by which one component's failure halts the system.** For each: the blast radius, whether degradation is graceful, and the recovery path.

### 8. State ownership
For each stateful component: authoritative state, replicas, caches, projections, lifecycle, consistency model. **Where two components could each believe they own the same state, say so** — that ambiguity is where correctness failures live.

### 9. Storage architecture
Primary stores, metadata stores, logs, caches, object storage, search indexes, analytical stores. **Establish why each exists** and what would break if it were consolidated.

### 10. Control plane against data plane
Where applicable, separate configuration, policy and orchestration from high-volume runtime processing. Establish what happens to the data plane when the control plane is unavailable.

### 11. Integration architecture
Push and pull, synchronous and asynchronous, webhooks and events, software development kits, adapters, connectors, import and export, compatibility boundaries.

### 12. Deployment topologies
Local, single-node, clustered, cloud-managed, self-hosted, high-availability, multi-region — and **any component that changes, appears or disappears by topology.**

### 13. Multi-tenancy and isolation
Namespaces, process and storage isolation, authentication boundaries, resource isolation, noisy-neighbour behaviour.

### 14. Architecture evolution
From history, design documents, issues and releases: replaced architectures, migrations, abandoned designs. **Where an architecture was replaced, establish what the replacement made possible and what it cost.**

### 15. Invariant location
**For each invariant in Volume I's catalogue, name the component that owns its enforcement.** Where no component owns it, record that — an invariant enforced nowhere in the architecture is either enforced by convention or not at all.

## Required deliverables
1. System context diagram · 2. Full component diagram · 3. Critical-path architecture · 4. Dependency graph · 5. **Rented-versus-owned register** · 6. **Single-point-of-failure map** · 7. Interface map · 8. State-ownership matrix · 9. Storage architecture · 10. Control and data-plane map · 11. Integration map · 12. Deployment topology map · 13. Isolation model · 14. Architecture evolution · 15. **Invariant-to-component map** · 16. Key unknowns · 17. Ten most important findings

## Final questions
- Which components are indispensable? Which are commodity?
- Where is the architectural centre of gravity?
- What owns the source of truth?
- What is rented rather than owned, and what breaks if it goes?
- Which boundary matters most for correctness?
- Which component would be hardest to replace?

**Completion test:** a reader should be able to draw the architecture from memory, explain why every major component exists, and name the component that enforces each invariant.
