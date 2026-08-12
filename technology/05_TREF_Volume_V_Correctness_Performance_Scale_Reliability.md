# TREF VOLUME V — CORRECTNESS, PERFORMANCE, SCALE & RELIABILITY

**Standalone research prompt. Send together with `TREF_CONVENTIONS.md`, which is binding and is not repeated here.**

Conduct an institutional-grade technical reverse-engineering study.

## Subject header
*Reproduce §0 from the instantiated conventions.*

## This volume
**Owned question:** *What does the technology genuinely guarantee, and under what conditions do the guarantees hold?*

*Volume VII, where commissioned, asks the adversarial version: which of these guarantees can be broken deliberately, and by whom.*
**Execute Volume V only.** Do not begin Volume VI.

## Evidence ceiling
*State what the source-openness position permits.*

**And one rule specific to this volume: every performance, scale and security claim made by the project about itself is a MAINTAINER CLAIM until a MEASURED RESULT or CONFIRMED IMPLEMENTATION supersedes it. A benchmark without stated conditions — hardware, workload, dataset, concurrency, configuration — is a MAINTAINER CLAIM, not a measurement.**

## Carried forward
*Restate Volumes I–IV — the invariant catalogue, **the enforcement verification from III.3 and the schema-enforced invariants from IV.5**, the partial-success matrix, the concurrency model and the persistence layer.*

## Re-cut *(optional)*

---

### 1. THE GUARANTEE LEDGER
**Before anything else, state plainly what this technology guarantees.**

For each guarantee: its precise statement; the conditions under which it holds; **the conditions under which it does not**; where it is enforced, using the four-way classification from Volume III; and the evidence class.

Then rank them: **which guarantee is strongest, and which is weakest?** Most technologies are marketed on their strongest and broken through their weakest.

### 2. Correctness specification
Invariants, preconditions, postconditions, valid and invalid states, enforcement layers. Where Volume I catalogued and Volume III verified, this section **specifies**.

### 3. Numerical and precision semantics
Where relevant: integers, decimal, floating point, units, rounding, overflow. **Where money, measurement or accumulation is involved, establish the representation and the rounding rule** — this is a routine source of silent, compounding error.

### 4. Consistency guarantees
Strong, eventual or session consistency; read-after-write; stale reads; replication behaviour. **State the guarantee in terms a caller can rely on**, not in terms of the mechanism.

### 5. Atomicity and isolation
Transaction scope, isolation levels, serialisation points, anomalies prevented and anomalies possible. **Name the anomalies that remain possible** — write skew, lost update, phantom reads — rather than only those prevented.

### 6. Concurrency under stress
Hot keys and entities, lock contention, optimistic conflicts, deadlocks, starvation, fairness. **Establish the behaviour at the contention point rather than in the average case.**

### 7. Latency decomposition
Break latency into parsing, validation, application logic, reads, writes, locking, external calls, serialisation and network. **Establish where the time actually goes** and which component dominates at which percentile.

### 8. Throughput model
The unit of throughput, single-node capacity, scale-out behaviour, saturation point, queueing behaviour beyond saturation. **Establish what happens after saturation** — graceful degradation, collapse, or unbounded queue growth.

### 9. Scalability
Vertical and horizontal scaling, partitioning, sharding, replication, multi-region, coordination overhead. **Identify the primary scaling bottleneck** and the workload shape that reaches it first.

### 10. Capacity model
Central processing, memory, storage, input-output operations, network, connections, lock contention. Build a model a reader could size a deployment from.

### 11. Reliability mechanisms
Retries, timeouts, circuit breakers, failover, health checks, redundancy, graceful degradation. **Establish whether retry policies can amplify a failure** rather than absorb it.

### 12. Durability and recovery
Write-ahead logs, synchronisation assumptions, backup, restore, point-in-time recovery, replication, recovery-point and recovery-time objectives.

**Establish what is lost in the worst permitted case**, and whether the durability guarantee depends on a filesystem or hardware behaviour the project assumes rather than verifies.

### 13. Observability
Logs, metrics, traces, audit logs, service-level objectives and indicators, alerting. **The operative test: could an operator detect a correctness failure — not an availability failure — from what the system emits?** Most systems fail this.

### 14. Resource isolation and noisy neighbours
Resource isolation, quality-of-service controls, and the behaviour of a well-behaved tenant beside a resource-hungry one.

*This is the performance dimension of isolation. **The confidentiality and integrity dimension — whether one tenant can read another — belongs to Volume VII** and should not be attempted here.*

### 15. Security — deferred
**Where Volume VII has been commissioned, the threat model, authentication and authorisation, data protection, tenant confidentiality, abuse and resource exhaustion, and the disclosed-vulnerability record all belong there.** Record here only what the performance and reliability analysis depends on, and refer forward.

**Where Volume VII has *not* been commissioned** — the technology holds no money, credentials or personal data, and is neither internet-facing nor multi-tenant — cover the essentials here: trust boundaries, authentication and authorisation, data protection, and abuse or resource exhaustion. State explicitly that the study made that judgement and why.

### 16. Failure-scenario matrix
Model at minimum: crash during commit; database failover; network partition; disk exhaustion; clock skew; duplicate delivery; partial deployment with mixed versions; corrupt data; hot partition.

For each: what the system does, what state it is left in, whether it self-heals, and how an operator would know.

## Required deliverables
1. **Guarantee ledger, ranked** · 2. Invariant matrix · 3. Precision model · 4. Consistency model · 5. Atomicity and isolation model with remaining anomalies · 6. Concurrency bottleneck map · 7. Latency model · 8. Throughput model with post-saturation behaviour · 9. Scalability model with primary bottleneck · 10. Capacity model · 11. Reliability map with retry-amplification assessment · 12. Backup and recovery model with worst-case loss · 13. **Observability map with the correctness-detection test** · 14. Resource-isolation model · 15. Failure-scenario matrix · 16. Key unknowns · 17. Ten most important findings

*Security deliverables belong to Volume VII where commissioned.*

## Final questions
- What guarantee is strongest? What guarantee is weakest?
- What is the primary scaling bottleneck?
- What happens after saturation?
- What failure mode is most dangerous?
- Could an operator detect a correctness failure from what the system emits?
- Under what workload does the architecture degrade first?

**Completion test:** a reader should be able to state what the technology guarantees, under what conditions the guarantees fail, and how the system behaves under stress and partial failure — distinguishing throughout what is measured from what is claimed. *Whether those guarantees can be broken deliberately is Volume VII's question.*
