# TREF VOLUME I — PURPOSE, DOMAIN & CONCEPTUAL MODEL

**Standalone research prompt. Send together with `TREF_CONVENTIONS.md`, which is binding and is not repeated here.**

Conduct an institutional-grade technical reverse-engineering study. This is not a feature summary, tutorial, review or generic architecture description. Understand the technology deeply enough to reconstruct how it works from first principles.

## Subject header
*Reproduce §0 from the instantiated conventions — technology, type, version, commit, documentation, repository, deployment model, licence, source openness, objective, research date.*

## This volume
**Owned question:** *Why does this technology exist, what problem does it hold, and what does it promise never to violate?*
**Execute Volume I only.** Do not begin Volume II.

## Evidence ceiling
**State at the outset what the `Source openness` field permits.** Where the source is OPAQUE or DOCUMENTED-ONLY, the highest label reachable in this volume is DOCUMENTED BEHAVIOR, and the study should say so here rather than discovering it at Volume IV.

## Carried forward
**NONE** — this is the first volume.

## Re-cut *(optional)*

---

### 1. Problem origin
What problem caused the technology to exist? Who experienced it? What prior approaches existed, and what was inadequate about them? What constraints — hardware, protocol, regulatory, organisational — shaped the design?

### 2. Historical evolution
Trace origin, initial release, major conceptual changes, breaking changes, deprecated models, architectural turning points, current state. **For each change, identify the technical pressure that caused it**, from design documents, proposals and issue threads where available; mark HYPOTHESIS where not.

### 3. The removal record
**What was built and then taken out?** Removed features, reverted architectures, abandoned proposals, deprecated subsystems, rejected designs that reached implementation.

A project's removals are as informative as its additions and are never presented as such. For each: what it was, why it was removed, and **what the removal reveals about the model the project settled on.**

### 4. Actors and users
End users, developers, operators, administrators, services, external systems, maintainers, plugins and extensions. Map goals, permissions, trust level, inputs, outputs, failure impact.

### 5. Jobs to be done
Separate core jobs, convenience features, administration, integrations, operational capabilities, and commercial or enterprise features.

### 6. Domain glossary
Define every important term precisely. **State whether each is industry-standard or project-specific**, and where a project has redefined a standard term, say so — that redefinition is usually a design decision in disguise. Resolve ambiguous terminology before deeper analysis.

### 7. Core abstractions
For each: identity, attributes, lifecycle, relationships, mutability, ownership, persistence, constraints. Build the domain model.

### 8. THE INVARIANT CATALOGUE
Catalogue what must always remain true: uniqueness, conservation, valid transitions, ordering, integrity, authorisation, immutability, precision, isolation, and any domain-specific property.

**For each invariant, state where it is claimed to be enforced** — which layer, component or constraint. **An invariant nobody can point to is a HYPOTHESIS, not a guarantee.**

*Volume III will verify each enforcement point at runtime. Number them here so it can.*

### 9. Semantics
The precise meaning of creation, update, deletion, commit, rollback, version, timestamp, equality, identity, ownership, ordering, finality and error, where relevant. **Where the project's meaning differs from the ordinary one, that difference is a finding.**

### 10. Assumptions
About callers, infrastructure, trust, consistency, workload, availability, data size, clocks and time, and external dependencies.

### 11. Explicit non-goals
What the technology intentionally does not solve. **A stated non-goal is a design decision and frequently explains an apparent deficiency.**

### 12. Standards and theory
Standards, protocols, academic models or established theories behind the design. **Distinguish standard behaviour from proprietary adaptation** — and where the project deviates from a standard it claims to implement, establish why.

### 13. Competing conceptual models
Credible alternative abstractions, and what becomes easier or harder under each.

### 14. Falsification test
**State what would prove this domain model wrong.** Name the observation, behaviour or code path that, if found, would show the abstractions described here are not the ones the system actually uses. Volumes II–IV should be told to look for it.

## Required deliverables
1. Problem statement · 2. Historical evolution with causes · 3. **Removal record** · 4. Actor map · 5. Jobs-to-be-done map · 6. Domain glossary · 7. Core abstraction diagram · 8. Entity and relationship model · 9. **Numbered invariant catalogue with claimed enforcement points** · 10. Semantic rules · 11. Assumption catalogue · 12. Non-goals · 13. Standards map with deviations · 14. Alternative conceptual models · 15. **Falsification test** · 16. Key unknowns · 17. Ten most important findings

## Final questions
- What is this technology fundamentally?
- What is the single most important abstraction?
- What invariant most defines correctness?
- What assumption would most radically change the design if removed?
- What did the project try and remove, and what does that reveal?
- What is the deepest conceptual tradeoff?

**Completion test:** a reader should understand the technology's domain model before any discussion of implementation — and should know what would prove that understanding wrong.
