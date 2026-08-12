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
# Volume I — Purpose, Domain & Conceptual Model

**Execute Volume I only. Do not begin Volume II.**

## Research Questions

### 1. Problem Origin
- What problem caused the technology to exist?
- Who experienced it?
- What prior approaches existed?
- What was inadequate about them?
- What constraints shaped the design?

### 2. Historical Evolution
Trace founding/origin, initial release, major conceptual changes, breaking changes, deprecated models, architectural turning points, and current state. For each change, identify the technical pressure that likely caused it.

### 3. Actors and Users
Identify end users, developers, operators, administrators, services, external systems, maintainers, and plugins/extensions. Map goals, permissions, trust level, inputs, outputs, and failure impact.

### 4. Jobs to Be Done
Separate core jobs, convenience features, administration, integrations, operational capabilities, and commercial/enterprise features.

### 5. Domain Glossary
Define every important term precisely. State whether it is industry-standard or project-specific. Resolve ambiguous terminology before deeper analysis.

### 6. Core Abstractions
For each abstraction identify identity, attributes, lifecycle, relationships, mutability, ownership, persistence, and constraints. Build a domain model.

### 7. Invariants
Catalog what must always remain true: uniqueness, conservation, valid transitions, ordering, integrity, authorization, immutability, precision, isolation, or other domain-specific properties. Identify where each invariant is enforced.

### 8. Semantics
Explain the precise meaning of creation, update, deletion, commit, rollback, version, timestamp, equality, identity, ownership, ordering, finality, and error where relevant.

### 9. Assumptions
Identify assumptions about callers, infrastructure, trust, consistency, workload, availability, data size, clock/time, and external dependencies.

### 10. Explicit Non-Goals
Determine what the technology intentionally does not solve.

### 11. Standards and Theory
Identify standards, protocols, academic models, or established theories behind the design. Distinguish standard behavior from proprietary adaptation.

### 12. Competing Conceptual Models
Compare credible alternative abstractions and explain what becomes easier or harder under each.

## Required Deliverables
1. Problem statement
2. Historical evolution
3. Actor map
4. Jobs-to-be-done map
5. Domain glossary
6. Core abstraction diagram
7. Entity/relationship model
8. Invariant catalog
9. Semantic rules
10. Assumption catalog
11. Non-goals
12. Standards map
13. Alternative conceptual models
14. Key unknowns
15. Ten most important findings

## Final Questions
- What is this technology fundamentally?
- What is the single most important abstraction?
- What invariant most defines correctness?
- What assumption would most radically change the design if removed?
- What is the deepest conceptual tradeoff?

**Completion test:** A reader should understand the technology's mental/domain model before discussing implementation.
