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
# Volume III — Data, State, Control & Execution Flows

**Execute Volume III only. Do not begin Volume IV.**

This volume is about runtime truth.

## Research Questions

### 1. Representative Operations
Identify the 5–10 operations that expose the real architecture.

### 2. Happy-Path Execution
For each operation trace input → parsing → validation → authentication/authorization → routing → interpretation → reads → invariant checks → computation → mutation → persistence → side effects/events → response. Identify component, process/thread, state read/written, timing, dependency, and error path at every step.

### 3. State Machines
Build explicit state machines for important entities/workflows: states, transitions, guards, terminal states, invalid transitions, retries, compensations.

### 4. Data Flow
Trace ingress, normalization, validation, transformation, persistence, indexing, projection, export, analytics. Identify lossy transformations.

### 5. Transaction Boundaries
Determine what is atomic, what is not, database/distributed transaction boundaries, commit points, side effects before/after commit, and rollback behavior.

### 6. Ordering and Time
Analyze ordering, timestamps, logical vs wall-clock time, effective vs recorded time, clock assumptions, races, and late-arriving data.

### 7. Concurrency
Determine lock scope, optimistic/pessimistic control, version checks, serialization points, conflict detection, deadlocks, starvation, and concurrent read/write semantics.

### 8. Idempotency
Determine key scope, persistence, retention, payload mismatch behavior, simultaneous duplicates, retries, and exactly-once effect vs delivery semantics.

### 9. Events and Asynchrony
Analyze event generation, transactional coupling, outbox/equivalent, ordering, retries, dead-letter handling, replay, and duplicates.

### 10. Failure Paths
Trace validation errors, storage failures, timeouts, dependency failures, process crashes, response loss, partial success, stale state, and concurrent conflict. State the final system condition after each.

### 11. Recovery and Reconciliation
Analyze incomplete work, divergent state, missing events, duplicate effects, corruption, and external-state mismatch.

### 12. Read Paths
Trace primary reads, indexes, caches, materialized views, projections, stale-read behavior, and query consistency.

### 13. Mutation / Deletion / Immutability
Determine what can change, append-only behavior, corrections, reversals, tombstones, and historical preservation.

## Required Deliverables
1. Operation catalog
2. Sequence diagrams
3. State machines
4. Data-flow diagrams
5. Transaction-boundary map
6. Ordering/time model
7. Concurrency model
8. Idempotency model
9. Event model
10. Failure matrix
11. Recovery/reconciliation model
12. Read/projection model
13. Mutation/immutability model
14. Key unknowns
15. Ten most important findings

## Final Questions
- What is the real commit point?
- What state is authoritative?
- What happens after an ambiguous timeout and retry?
- Where can races occur?
- What operation is hardest to make correct?
- What runtime mechanism most defines the technology?

**Completion test:** A reader must be able to trace the critical operation from input to final durable state and explain important failure cases.
