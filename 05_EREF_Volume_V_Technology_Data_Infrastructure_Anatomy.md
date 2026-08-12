# EREF VOLUME V — TECHNOLOGY, DATA & INFRASTRUCTURE ANATOMY

**Standalone research prompt. Send together with `EREF_CONVENTIONS.md`, which is binding and is not repeated here.**

## Subject header
*Reproduce §0 from the instantiated conventions.*

## This volume
**Owned question:** *What technological machinery makes the enterprise possible, and which technical capabilities are strategic?*
**Execute Volume V only.** Do not begin Volume VI.

## Carried forward
*Restate Volumes I–IV — the entity map, the payer inversion, the value flows, and the operating model including any regulated-operations failure.*

## Re-cut *(optional)*

---

## V.1 Technology landscape
Inventory customer-facing applications, core operational systems, enterprise resource planning, customer relationship management, finance, human resources, data platforms, integration platforms, industrial systems, internal tools.

## V.2 Core technology architecture
Reconstruct major applications, services, interfaces, databases, event systems, queues, caches, cloud, data centres, networks, edge and industrial systems, device and software systems.

## V.3 Critical systems
Identify systems whose failure would materially impair the enterprise. Rank critical, high, moderate, low. **Cross-check against the critical operating path from Volume IV** — where the two disagree, that is a finding.

## V.4 SHARED VERSUS SEPARATE *(where the enterprise runs more than one business)*
**Establish what is genuinely one machine and what merely shares a parent.**

For each layer — cloud and infrastructure, data platform, identity, risk and fraud, machine-learning platform, transaction or ledger infrastructure, support tooling — state whether it is shared across the businesses or duplicated per business, and cite the evidence.

**Then answer the harder question separately: is there a joined customer graph?** Does the enterprise know that a customer of one business is also a customer of another, and does anything act on that knowledge?

Shared *infrastructure* and shared *customers* are different achievements, and enterprises routinely claim the second on evidence of the first. **Where no person-level joining is demonstrable, say so** — and record whether the enterprise has ever published a metric that would demonstrate it. An absence, after years of assertion, is itself evidence.

## V.5 Build, buy or partner
For each material system classify as proprietary, software-as-a-service, commercial software, open source, outsourced or partner-operated. **Establish what is rented rather than owned**, and what the enterprise could not rebuild if the vendor withdrew.

## V.6 Data architecture
Customer, product, transaction, operational, financial, supplier, behavioural, risk and research data. Trace collection, storage, processing, access, lineage, analytics, governance, privacy and retention.

**Establish the data rights**: what the enterprise is permitted to do with each class, under whose consent, and whether the permission would survive a change of law.

## V.7 Analytics and decision systems
Business intelligence, forecasting, experimentation, pricing, optimisation, risk models, recommendation, planning.

## V.8 Proprietary decision engines *(where decisions are automated at scale)*
Where the enterprise makes high-volume automated decisions — credit, pricing, routing, matching, moderation, underwriting — reconstruct the engine.

Establish: the inputs and which are proprietary; the feature store and its refresh; the model and policy layers; the **latency budget and what it forecloses**; the decision volume; and the measured outcome quality.

**Then establish what the enterprise knows that an external data provider does not — and what the external provider knows that it does not.** That complementarity is usually the real moat, and its blind spot is usually the real risk.

## V.9 Artificial intelligence and machine learning
**Separate rigorously: deployed production capability · internal productivity use · experiments · management aspiration · marketing claim.**

Where the enterprise attributes a material operational or headcount outcome to artificial intelligence, treat it as COMPANY CLAIM and test it against independent evidence. Two prior studies found identical claims substantially overstated and later qualified by the chief executive.

## V.10 Integration architecture
Interfaces, middleware, electronic data interchange, events, file transfer, partner interfaces, legacy bridges.

## V.11 Security
Identity and access management, privileged access, encryption, key and secrets management, application security, infrastructure security, supply-chain security, security operations, incident response.

## V.12 Reliability and business continuity
Uptime, redundancy, disaster recovery, backups, failover, incident management, geographic resilience.

## V.13 Technology organisation
Chief technology and information officers, engineering, information technology, data, security, infrastructure, architecture, product engineering, internal systems.

## V.14 Technical talent
Headcount, geography, skill concentration, contractors, hiring, retention, key-person dependencies.

## V.15 Technology economics
Cloud, data centre, software licensing, engineering labour, security, vendor costs, infrastructure capital and operating expenditure.

## V.16 Technology as moat
For each significant system ask whether it is proprietary, hard to reproduce, cost-reducing, speed-enhancing, quality-enhancing, compliance-enhancing, switching-cost creating, or scale- and data-compounding.

**Distinguish technology that creates the moat from technology that merely enables one.** Most is the latter.

## V.17 Technical debt
Legacy systems, migration programmes, duplicated platforms, integration complexity, obsolete infrastructure, operational pain. **Where two businesses were merged or acquired, establish what was never integrated.**

## V.18 TREF CANDIDATES *(the formal handoff)*
Identify technologies deserving separate **Technology Reverse-Engineering Framework** analysis.

Rank each on: business criticality · uniqueness · technical complexity · moat relevance · replacement difficulty.

For the highest-ranked, record the header TREF will need: name, type, version where known, documentation, source availability, deployment model, licence. **This list is a deliverable, not a gesture** — it is the bridge between the two frameworks.

## Required deliverables
1. Technology landscape · 2. Core architecture · 3. Critical-system ranking · 4. **Shared-versus-separate assessment and customer-graph verdict** · 5. Build-versus-buy matrix with rented-capability list · 6. Data-flow architecture and data-rights map · 7. Analytics map · 8. **Decision-engine reconstruction** · 9. Artificial-intelligence claims tested · 10. Integration map · 11. Security architecture · 12. Reliability and recovery model · 13. Technology-organisation map · 14. Technical-talent map · 15. Technology-cost model · 16. Technology-moat assessment · 17. Technical-debt map · 18. **Ranked TREF candidate list with headers** · 19. Key unknowns · 20. Ten most important findings

## Final questions
- Which system is the technological heart of the enterprise?
- What is truly strategic and what is commodity?
- Which system is hardest to replace? What is rented rather than owned?
- Is it one machine or several?
- Does technology create the moat, or merely enable one?
- Which system should receive a full TREF teardown?

**Completion test:** a reader should understand the technical machinery, know what is owned against rented, know whether the businesses genuinely share a platform, and know which system deserves deeper reverse engineering.
