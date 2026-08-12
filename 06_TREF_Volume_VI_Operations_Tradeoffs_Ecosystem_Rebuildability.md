# TREF VOLUME VI — OPERATIONS, TRADEOFFS, ECOSYSTEM & REBUILDABILITY

**Standalone research prompt. Send together with `TREF_CONVENTIONS.md`, which is binding and is not repeated here.**

Conduct an institutional-grade technical reverse-engineering study.

## Subject header
*Reproduce §0 from the instantiated conventions.*

## This volume
**Owned question:** *What does it cost to run, what was traded away, and could it be rebuilt?*
**Execute Volume VI only.** Do not begin the reconstruction unless explicitly requested.

## Evidence ceiling
*State what the source-openness position permits. Note that operational burden is frequently better evidenced by issue trackers, support forums and practitioner reports than by documentation, which describes the intended experience rather than the actual one.*

## Carried forward
*Restate Volumes I–V — the guarantee ledger, the failure-scenario matrix, the capacity and throughput models, the dependency graph and the rented-versus-owned register.*

## Re-cut *(optional)*

---

### 1. Installation and bootstrap
Prerequisites, initialisation, startup ordering, first-run state. **Establish the time from nothing to a working instance**, and how much of it is automatable.

### 2. Day-two operations
Scaling, monitoring, backups, restores, maintenance, credential and certificate rotation, capacity planning. **These are the operations that consume operator time for the life of the system**, and they are systematically under-documented relative to installation.

### 3. Upgrade and migration
Version upgrades, schema and data migration, rolling upgrades, downtime, rollback, compatibility. **Establish whether rollback is genuinely possible after a schema migration** — frequently it is not, and that asymmetry governs the upgrade risk.

### 4. Troubleshooting
Symptoms, diagnostics, logs, metrics, traces, repair tools, escalation. **Establish what an operator does when the system is in a state the documentation does not describe.**

### 5. Incident response
Detection, triage, containment, recovery, reconciliation, post-mortem. Cross-reference the failure-scenario matrix from Volume V: **for each scenario, what does the operator actually do?**

### 6. Developer experience
Documentation, interface clarity, software development kits, local development, tests, debugging, examples, error messages, learning curve. **Assess error messages specifically** — they are the most-read documentation in any system and the least maintained.

### 7. Operator experience
Deployment burden, configuration, upgrades, monitoring, failure recovery, tuning, staffing. **Estimate the operator effort in people rather than in adjectives**: can one part-time engineer run this, or does it need a team?

### 8. TOTAL COST OF OWNERSHIP
**Build a model, not a list.**

Central processing, memory, storage growth, input-output, bandwidth, database cost, external services, licensing, and **operator labour, which is routinely the largest line and routinely omitted.**

Express it per unit of the throughput measure from Volume V, so the cost can be compared against alternatives and against the value delivered. State the assumptions.

### 9. Governance and maintainership
Owners, maintainers, contribution model, release cadence, **bus factor**, roadmap, sponsor. Establish what happens to the project if its principal sponsor withdraws — a question with recent precedent in several ecosystems.

### 10. Licensing and commercial boundaries
Open source against enterprise, source-available restrictions, cloud-provider restrictions, proprietary features, support terms. **Establish what a commercial user may and may not do**, and whether the licence has changed — a licence change is a strategic act, and the direction of travel matters more than the current terms.

### 11. Ecosystem
Integrations, plugins, software development kits, community, consultants, adjacent tools. **Establish whether the ecosystem is a moat or a liability** — a large plugin ecosystem constrains the project's ability to change.

### 12. Alternatives
Compare credible alternatives on conceptual model, architecture, correctness, performance, operability, ecosystem, licence and complexity. **Give the deepest treatment to the closest structural analogue** and be willing to conclude it is better.

### 13. THE DESIGN-TRADEOFF LEDGER
**For every major design choice: the benefit, the cost, the alternative rejected, and the workloads under which the choice wins or loses.**

A tradeoff stated without its losing case is not a tradeoff; it is marketing. **Name the workload each choice is wrong for.**

### 14. Technical debt and constraints
Legacy areas, known constraints, scaling boundaries, in-flight migrations, deprecated areas, complexity hotspots. **Establish what the maintainers themselves say is wrong**, from issues, proposals and post-mortems.

### 15. THE REBUILDABILITY TEST
List every capability required to recreate a functionally equivalent system. For each, score: **conceptual difficulty · implementation difficulty · correctness difficulty · operational difficulty · time · expertise required · whether a commodity substitute exists.**

Then separate: **what must be built, what can be assembled, and what can simply be bought.** Most systems are far more assemblable than their documentation implies, and the few genuinely hard parts are the whole answer.

### 16. Preserve or redesign
Classify every major design choice: **Preserve · Preserve with modification · Replace · Needs benchmark.**

State the reasoning for each. This section is the bridge to any new implementation and should be written for a builder rather than an analyst.

### 17. Transplant verdicts *(where the objective is build extraction)*
Where §0 declares a build objective, adjudicate each material mechanism **ADOPT · ADAPT · REJECT**, applying the environment question: *did this work because of the mechanism itself, or because of the team size, hardware, traffic profile, operational maturity or surrounding ecosystem?* Strip the environment out, then judge.

State precisely what must change under ADAPT, and the dependency that kills it under REJECT. **A REJECT is as valuable as an ADOPT.**

## Required deliverables
1. Installation map with time-to-working · 2. Day-two operations model · 3. Upgrade and migration model with rollback assessment · 4. Troubleshooting map · 5. Incident-response model cross-referenced to the failure matrix · 6. Developer-experience assessment · 7. Operator-experience assessment with staffing estimate · 8. **Total-cost-of-ownership model per unit of throughput** · 9. Governance map with bus factor · 10. Licensing map with direction of travel · 11. Ecosystem map · 12. Alternatives matrix · 13. **Design-tradeoff ledger with losing cases named** · 14. Technical-debt map · 15. **Rebuildability matrix** · 16. **Preserve-versus-redesign matrix** · 17. Transplant verdicts where applicable · 18. Key unknowns · 19. Ten most important findings

## Final questions
- What is hardest to operate?
- What is most expensive to scale — in machines or in people?
- What is the deepest design tradeoff, and what workload is it wrong for?
- What is hardest to rebuild correctly?
- What could be replaced with commodity infrastructure?
- What should a new implementation preserve, and what should it redesign?

**Completion test:** a reader should understand the production burden, the ecosystem position, the tradeoffs and the realistic cost of recreating the technology — and a builder should know what to keep.
