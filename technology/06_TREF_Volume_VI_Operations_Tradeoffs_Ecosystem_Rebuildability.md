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
# Volume VI — Operations, Tradeoffs, Ecosystem & Rebuildability

**Execute Volume VI only. Do not begin the final Technology Reconstruction unless explicitly requested.**

## Research Questions
1. Installation/bootstrap: prerequisites, initialization, startup ordering, first-run state.
2. Day-2 operations: scaling, monitoring, backups, restores, maintenance, credentials/certificates, capacity planning.
3. Upgrade/migration: version upgrades, schema/data migration, rolling upgrades, downtime, rollback, compatibility.
4. Troubleshooting: symptoms, diagnostics, logs, metrics, traces, repair tools, escalation.
5. Incident response: detection, triage, containment, recovery, reconciliation, postmortem.
6. Developer experience: docs, API clarity, SDKs, local development, tests, debugging, examples, errors, learning curve.
7. Operator experience: deployment burden, configuration, upgrades, monitoring, failure recovery, tuning, staffing.
8. Resource economics: CPU, memory, storage growth, IOPS, bandwidth, DB cost, external services, licensing, operator labor.
9. Governance/maintainership: owners, maintainers, contribution model, release cadence, bus factor, roadmap, sponsor.
10. Licensing/commercial boundaries: OSS vs enterprise, source-available restrictions, cloud restrictions, proprietary features, support.
11. Ecosystem: integrations, plugins, SDKs, community, consultants, adjacent tools.
12. Alternatives: compare conceptual models, architecture, correctness, performance, operability, ecosystem, license, complexity.
13. Build a design-tradeoff ledger. For every major choice state benefit, cost, rejected alternative, workloads where it wins/loses.
14. Identify technical debt, known constraints, scaling boundaries, migration projects, deprecated areas, complexity hotspots.
15. Rebuildability test: list every capability needed to recreate the system and score conceptual, implementation, correctness, operational difficulty, time, expertise, and commodity substitutes.
16. Preserve-vs-redesign: classify every major design choice as Preserve / Preserve with modification / Replace / Needs benchmark.

## Required Deliverables
Installation map; day-2 operations model; upgrade/migration model; troubleshooting map; incident-response model; developer/operator experience assessments; resource-cost model; governance map; licensing map; ecosystem map; alternatives matrix; design-tradeoff ledger; technical-debt map; rebuildability matrix; preserve-vs-redesign matrix; key unknowns; ten most important findings.

## Final Questions
- What is hardest to operate?
- What is most expensive to scale?
- What is the deepest design tradeoff?
- What is hardest to rebuild correctly?
- What could be replaced with commodity infrastructure?
- What should a new implementation preserve or redesign?

**Completion test:** Explain the production burden, ecosystem position, tradeoffs, and realistic cost of recreating the technology.
