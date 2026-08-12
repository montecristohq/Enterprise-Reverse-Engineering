# TREF VOLUME IV — IMPLEMENTATION & INFRASTRUCTURE ANATOMY

**Standalone research prompt. Send together with `TREF_CONVENTIONS.md`, which is binding and is not repeated here.**

Conduct an institutional-grade technical reverse-engineering study.

## Subject header
*Reproduce §0 from the instantiated conventions.*

## This volume
**Owned question:** *What is the technology actually made of, and what was bought rather than built?*
**Execute Volume IV only.** Do not begin Volume V.

## Evidence ceiling — READ FIRST
**This is the volume where source openness binds hardest.**

Where the repository is available, this volume can and should reach CONFIRMED IMPLEMENTATION on most material claims, naming files, functions, tables and clauses so a reader can go and look.

Where it is not, **do not construct an implementation.** State what is known from documentation and observable behaviour, present the plausible alternatives, name which the evidence favours and why, and label the whole ANALYTICAL INFERENCE or HYPOTHESIS. A volume that quietly fills gaps with plausible-sounding architecture is worse than useless, because it is indistinguishable from one that did not.

**State the ceiling in the first paragraph of the output.**

## Carried forward
*Restate Volumes I–III — the domain model and invariant catalogue, the component inventory and dependency graph, and above all **the invariant-enforcement verification from III.3**, which this volume must locate in code.*

## Re-cut *(optional)*

---

### 1. Repository and artefact map
Repositories, packages, modules, binaries, generated code, tests, tools, migrations, deployment files. Establish the shape of the codebase before reading any of it.

### 2. Languages, runtimes and models
Languages, runtimes, versions, concurrency model, memory model, ecosystem choices. **Establish what the concurrency and memory models make easy and what they make dangerous** — most implementation character follows from these two.

### 3. Critical source paths
Trace the critical paths from public interface to persistence, in code. **Name the files and functions.** Where Volume III traced the operation logically, this section traces it literally, and any divergence between the two is a finding.

### 4. Algorithms and data structures
Identify the correctness-critical and performance-critical algorithms and data structures. Analyse complexity, edge cases and the conditions under which each degrades.

### 5. Schema reconstruction
Rebuild the database or storage schema: tables or collections, keys, constraints, indexes, partitions, sequences, views, migrations.

**Establish which invariants are enforced by the schema itself** — a unique constraint, a foreign key, a check — because those are the invariants the system cannot violate, as distinct from those it merely tries not to.

### 6. Persistence layer
Raw queries or object mapping, transactions, connection pools, batching, retries, isolation levels, query patterns. **Establish the isolation level actually used**, not the one available.

### 7. Networking and protocols
Transport, serialisation, compression, timeouts, retries, backpressure, versioning. **Establish the default timeout and retry policy** and whether it can amplify a downstream failure.

### 8. Background work
Workers, schedulers, asynchronous jobs, maintenance, compaction, reconciliation, cleanup. **Establish what happens if each stops running** — background jobs fail silently and their absence is discovered late.

### 9. Configuration surface
Configuration, environment variables, feature flags, secrets, defaults. **Identify the dangerous combinations** — settings that are individually reasonable and jointly catastrophic — and whether anything prevents them.

### 10. Build, test and release
Build, tests, continuous integration, packaging, releases, semantic compatibility, migrations. Establish the release cadence and the compatibility promise.

### 11. TESTS AS EXECUTABLE SPECIFICATION
**A project's test suite states what it believes it guarantees, in executable form, and frequently contradicts its own documentation.**

Mine the tests for: edge cases the documentation omits; invariants asserted nowhere else; concurrency behaviour; historical regressions, which mark where the project has been hurt before; and undocumented contracts.

**Where a test and the documentation disagree, the test is the better evidence** — and the disagreement is a finding.

### 12. Deployment reconstruction
Processes, containers, orchestration, service discovery, load balancing, storage, health checks, autoscaling.

### 13. Infrastructure dependencies and the minimum viable deployment
Map what the technology requires to run at all, and **establish the smallest configuration in which it is genuinely functional** — as distinct from the smallest in which it starts.

### 14. Build, buy or open source
For each material capability, whether the project built it, adopted a library, depends on a service, or reimplemented something available. **Establish what was reimplemented rather than adopted, and why** — that decision usually encodes a constraint the project could not otherwise satisfy.

## Required deliverables
1. Repository map · 2. Language and runtime map with concurrency and memory models · 3. **Critical code paths, named** · 4. Algorithm and data-structure catalogue · 5. **Schema diagram with schema-enforced invariants marked** · 6. Persistence model with actual isolation level · 7. Protocol map with timeout and retry policy · 8. Background-job map with failure consequences · 9. **Configuration map with dangerous combinations** · 10. Build and release pipeline · 11. **Tests-as-specification findings, including documentation contradictions** · 12. Deployment topology · 13. Infrastructure dependency map and minimum viable deployment · 14. Build-versus-buy matrix with reimplementation rationale · 15. Key unknowns · 16. Ten most important findings

## Final questions
- Which implementation choice is most fundamental?
- Which dependency is most operationally important?
- **Where is domain correctness actually enforced — in the schema, in code, or nowhere?**
- What is the performance-critical code path?
- What do the tests guarantee that the documentation does not mention?
- Which implementation details are incidental and which are fundamental?

**Completion test:** a reader should be able to connect the conceptual architecture to concrete code, schema, runtime and deployment mechanisms — and should know which claims rest on source and which on inference.
