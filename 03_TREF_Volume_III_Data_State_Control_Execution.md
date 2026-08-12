# TREF VOLUME III — DATA, STATE, CONTROL & EXECUTION FLOWS

**Standalone research prompt. Send together with `TREF_CONVENTIONS.md`, which is binding and is not repeated here.**

Conduct an institutional-grade technical reverse-engineering study.

## Subject header
*Reproduce §0 from the instantiated conventions.*

## This volume
**Owned question:** *What actually happens at runtime — and what happens when it goes wrong?*
**Execute Volume III only.** Do not begin Volume IV.

**This volume is about runtime truth.** It is where the domain model of Volume I meets the components of Volume II and either survives the contact or does not.

## Evidence ceiling
*State what the source-openness position permits. Runtime behaviour is the hardest thing to establish from documentation alone; where the source is unavailable, most of this volume will be DOCUMENTED BEHAVIOR or ANALYTICAL INFERENCE, and it must say so.*

## Carried forward
*Restate Volumes I–II — the domain model, **the numbered invariant catalogue and its claimed enforcement points**, the component inventory, the state-ownership matrix and the single points of failure.*

## Re-cut *(optional)*

---

### 1. Representative operations
Identify the five to ten operations that expose the real architecture. **Choose operations that cross the most boundaries**, not the most common ones.

### 2. Happy-path execution
For each operation trace: input → parsing → validation → authentication and authorisation → routing → interpretation → reads → invariant checks → computation → mutation → persistence → side effects and events → response.

At every step identify the component, the process or thread, the state read and written, the timing, the dependency and the error path.

### 3. INVARIANT ENFORCEMENT VERIFIED
**For each invariant in Volume I's catalogue, find the runtime point at which it is actually enforced** — the check, the constraint, the lock, the transaction boundary.

Then classify each: **enforced structurally** (a database constraint or type system makes violation impossible); **enforced by check** (code tests it, and the check could be bypassed by another path); **enforced by convention** (nothing tests it); or **not enforced**.

**This is the single most valuable section in the volume.** An invariant claimed in documentation and enforced only by convention is a defect waiting for a concurrent caller.

### 4. State machines
Explicit state machines for important entities and workflows: states, transitions, guards, terminal states, invalid transitions, retries, compensations.

### 5. Data flow
Ingress, normalisation, validation, transformation, persistence, indexing, projection, export, analytics. **Identify every lossy transformation** and what is discarded.

### 6. Transaction boundaries
What is atomic and what is not; database and distributed transaction boundaries; commit points; side effects before and after commit; rollback behaviour.

**State the real commit point** — the moment after which the effect cannot be withdrawn — which is frequently not where the code appears to place it.

### 7. Ordering and time
Ordering guarantees, timestamps, logical against wall-clock time, effective against recorded time, clock assumptions, races, late-arriving data.

### 8. Concurrency
Lock scope, optimistic or pessimistic control, version checks, serialisation points, conflict detection, deadlocks, starvation, concurrent read and write semantics.

### 9. Idempotency
Key scope, persistence, retention, payload-mismatch behaviour, simultaneous duplicates, retries. **Distinguish exactly-once *effect* from exactly-once *delivery*** — systems routinely claim the second and deliver neither.

### 10. Events and asynchrony
Event generation, transactional coupling, outbox or equivalent, ordering, retries, dead-letter handling, replay, duplicates.

### 11. PARTIAL SUCCESS
**The case most studies skip, and the case that most often breaks systems in production.**

Trace every operation that touches more than one system, store or side effect, and establish what happens when some succeed and some do not: which effects persist; whether the system knows it is in a partial state; whether reconciliation is automatic, manual or absent; and **how long the inconsistency can persist before anything notices.**

### 12. Failure paths
Validation errors, storage failures, timeouts, dependency failures, process crashes, response loss, stale state, concurrent conflict. **State the final system condition after each** — not the error returned, but the durable state left behind.

### 13. Recovery and reconciliation
Incomplete work, divergent state, missing events, duplicate effects, corruption, external-state mismatch. **Establish what is self-healing and what requires an operator.**

### 14. Read paths
Primary reads, indexes, caches, materialised views, projections, stale-read behaviour, query consistency. **Establish the maximum staleness a reader can observe** and whether that bound is guaranteed or incidental.

### 15. Mutation, deletion and immutability
What can change; append-only behaviour; corrections; reversals; tombstones; historical preservation. **Establish whether deletion is deletion.**

## Required deliverables
1. Operation catalogue · 2. Sequence diagrams · 3. **Invariant-enforcement verification table with the four-way classification** · 4. State machines · 5. Data-flow diagrams with lossy transformations marked · 6. Transaction-boundary map with the real commit point · 7. Ordering and time model · 8. Concurrency model · 9. Idempotency model · 10. Event model · 11. **Partial-success matrix** · 12. Failure matrix with durable end-states · 13. Recovery and reconciliation model · 14. Read and projection model with staleness bounds · 15. Mutation and immutability model · 16. Key unknowns · 17. Ten most important findings

## Final questions
- What is the real commit point?
- What state is authoritative?
- Which invariants are enforced structurally, and which only by convention?
- What happens after an ambiguous timeout and a retry?
- What happens when half of an operation succeeds?
- Where can races occur? What operation is hardest to make correct?
- What runtime mechanism most defines the technology?

**Completion test:** a reader must be able to trace the critical operation from input to final durable state, explain the important failure cases, and say for each invariant whether the system actually enforces it or merely intends to.
