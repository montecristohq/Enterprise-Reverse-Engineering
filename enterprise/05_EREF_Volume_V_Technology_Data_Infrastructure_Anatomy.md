# EREF — Standalone Volume Research Prompt

## Research Target

- **Company:** [COMPANY NAME]
- **Industry / industries:** [INDUSTRY OR LEAVE FOR AGENT TO DETERMINE]
- **Primary geographies:** [GEOGRAPHIES OR LEAVE FOR AGENT TO DETERMINE]
- **Research date:** [CURRENT DATE]
- **Special focus:** [OPTIONAL]

Conduct an **institutional-grade enterprise reverse-engineering study**.

This is not a conventional company profile, SWOT analysis, short equity-research note, or generic strategy exercise.

The objective is to take the enterprise apart component by component until its underlying machinery is understood.

## Non-Negotiable Depth Rule

Depth follows complexity and importance, not an arbitrary page or token budget.

If a subject requires 3 pages, write 3 pages. If it requires 20 pages, write 20 pages. If it requires 50 pages, write 50 pages.

Do not shorten later sections because earlier sections became long. A section ends only when the subject is adequately understood.

> **Completeness before concision.**

If output limits prevent completion, stop at a logical boundary and continue later without compressing the remaining work.

## Evidence Labels

Use:

- **CONFIRMED FACT**
- **COMPANY CLAIM**
- **THIRD-PARTY ESTIMATE**
- **ANALYTICAL INFERENCE**
- **HYPOTHESIS**
- **UNKNOWN**

Never present inference as fact.

## Source Priority

Prioritize annual reports, regulatory/securities filings, investor presentations, earnings materials, official corporate documents, public contracts, official product/service documentation, regulators, registries, court records, patent/trademark databases, procurement records, official technical sources, partner/customer/supplier sources, academic/industry research, reputable journalism, and specialist publications.

Triangulate important findings.

## Universal Questions

For every material component ask:

- **What?**
- **How?**
- **Who?**
- **Where?**
- **When?**
- **Why?**

Then analyze:

- **Structure**
- **Flow**
- **Control**
- **Economics**
- **Risk**

## Mandatory Trace Rules

### Follow the money
Identify whose money it is, which entity controls it, where it resides, when ownership/economic entitlement changes, when revenue is recognized, what costs are deducted, and who bears risk.

### Follow the physical flow
Trace materials, inventory, production, warehousing, logistics, delivery, returns, and service where relevant.

### Follow the data
Trace generation, storage, processing, access, analytics, governance, privacy, and decision use.

### Follow the legal entity
Identify which entity owns assets, signs contracts, employs people, holds licenses, earns revenue, bears liabilities, owns IP, and pays taxes.

### Follow the authority
Identify who can make, approve, block, override, or terminate important decisions.

### Follow the revenue
Customer need → commercial event → pricing → gross transaction/billing → direct costs → recognized revenue → contribution → operating expenses → profit → cash.

## Industry Adaptation

Adapt the framework to the company. Do not force fintech, software, manufacturing, banking, or other sector concepts where they do not apply.

## Anti-Speculation Rule

If evidence is unavailable, state what is known, label inference, preserve uncertainty, and identify evidence needed to resolve it.

---
# Volume V — Technology, Data & Infrastructure Anatomy

**Execute Volume V only. Do not begin Volume VI.**

Primary question:

> **What technological machinery makes the enterprise possible, and which technical capabilities are strategic?**

## V.1 Technology Landscape
Inventory customer-facing applications, core operational systems, ERP, CRM, finance systems, HR systems, data platforms, integration platforms, industrial systems, and internal tools.

## V.2 Core Technology Architecture
Reconstruct major applications, services, APIs, databases, event systems, queues, caches, cloud, data centers, networks, edge/industrial systems, and device/software systems.

## V.3 Critical Systems
Identify systems whose failure would materially impair the enterprise. Rank critical, high, moderate, low.

## V.4 Build vs Buy vs Partner
For each material system classify proprietary/internal, SaaS, commercial software, open source, outsourced, or partner-operated. Explain strategic consequences.

## V.5 Data Architecture
Analyze customer, product, transaction, operational, financial, supplier, behavioral, risk, and R&D data. Trace collection, storage, processing, access, lineage, analytics, governance, privacy, and retention.

## V.6 Analytics & Decision Systems
Analyze BI, forecasting, experimentation, pricing, optimization, risk models, recommendation, and planning.

## V.7 AI / ML
Separate deployed production capability, internal productivity use, experiments, management aspirations, and marketing claims.

## V.8 Integration Architecture
Map APIs, middleware, EDI, events, file transfer, partner interfaces, and legacy bridges.

## V.9 Security
Analyze IAM, privileged access, encryption, key/secrets management, application security, infrastructure security, supply-chain security, security operations, and incident response.

## V.10 Reliability & Business Continuity
Analyze uptime, redundancy, disaster recovery, backups, failover, incident management, and geographic resilience.

## V.11 Technology Organization
Map CTO/CIO, engineering, IT, data, security, infrastructure, architecture, product engineering, and internal systems.

## V.12 Technical Talent
Analyze headcount, geography, skill concentration, contractors, hiring, retention, and key-person dependencies.

## V.13 Technology Economics
Estimate cloud, data center, software licensing, engineering labor, security, vendor, and infrastructure CapEx/Opex.

## V.14 Technology as Moat
For each significant system ask whether it is proprietary, hard to reproduce, cost-reducing, speed-enhancing, quality-enhancing, compliance-enhancing, switching-cost creating, or scale/data compounding.

## V.15 Technical Debt
Identify legacy systems, migration programs, duplicated platforms, integration complexity, obsolete infrastructure, and operational pain.

## V.16 TREF Candidates
Identify technologies that deserve separate **Technology Reverse Engineering Framework (TREF)** analysis.

Rank by business criticality, uniqueness, technical complexity, moat relevance, and replacement difficulty.

## Required Deliverables
1. Technology landscape
2. Core architecture
3. Critical-system ranking
4. Build-vs-buy matrix
5. Data-flow architecture
6. Analytics/AI map
7. Integration map
8. Security architecture
9. Reliability/DR model
10. Technology-org map
11. Technical-talent map
12. Technology-cost model
13. Technology-moat assessment
14. Technical-debt map
15. TREF candidate list
16. Key unknowns
17. Ten most important findings

## Final Questions
- Which system is the technological heart of the enterprise?
- What technology is truly strategic versus commodity?
- Which system is hardest to replace?
- What technical failure would hurt the business most?
- Does technology itself create the moat, or merely enable another moat?
- Which system should receive a full TREF teardown?

**Completion test:** A reader should understand the technical machinery of the enterprise and know which systems deserve deeper reverse engineering.
