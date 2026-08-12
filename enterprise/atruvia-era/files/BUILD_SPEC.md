# BUILD SPECIFICATION — read this before rendering

This document contains a complete institutional research study of approximately **41,000 words**. What follows is a binding specification for how it must be rendered. It is not a suggestion, and it is not editorial guidance. Every clause is a requirement.

This specification exists because two previous renders of this same content produced radically different results: one collapsed eleven top-level sections into a single heading, produced no table of contents and generated no diagrams; the other read the structure correctly. The variance was in interpretation, not in input. This specification removes the interpretation.

---

## 1. PRESERVATION CONTRACT — non-negotiable

**1.1 Every word is retained.** The body content runs to approximately 41,000 words. All of it must appear in the output. Do not summarise, condense, abridge, truncate, sample, paraphrase, or "capture the essence of" any section. If a section seems repetitive, it stays. If a section seems long, it stays. If a table seems dense, it stays.

**1.2 Every table is retained as a table.** There are approximately **53 tables containing over 1,000 rows**. Each must render as an actual table with visible rows and columns. Do not convert tables into prose, bullet lists, or summary callouts. Do not drop columns to make a table fit — see §3.4 for wide-table handling.

**1.3 Every evidence label is retained in place.** The tokens CONFIRMED FACT, COMPANY CLAIM, THIRD-PARTY ESTIMATE, ANALYTICAL INFERENCE, HYPOTHESIS and UNKNOWN appear several hundred times. They are load-bearing: the study's method depends on each claim carrying its confidence level at the point of reading. Never strip them, never move them to a footnote, never consolidate them.

**1.4 Every German term is retained.** Do not translate Gesamtleistung, Betriebsergebnis, Umlage, Vorstand, Aufsichtsrat, Verbund or any other German term in the body. Appendix A is the glossary; the body relies on it.

**1.5 No content may be relegated to a collapsed, hidden, truncated or "read more" state.** All content must be present in the rendered page at full length.

**Verification:** the rendered output must contain approximately 41,000 words of body prose, approximately 53 tables and over 1,000 table rows. If your output falls materially short of these counts, content has been lost and the build has failed.

---

## 2. STRUCTURE CONTRACT — navigation is the priority

This document is a reference work. The reader works through it at a desk over multiple sessions. Navigation is the primary design requirement.

**2.1 Eleven top-level sections.** The document has exactly eleven top-level divisions, each of which must render as an `h1` and receive a section-opening treatment:

1. Front matter (title, how to read, conventions)
2. Part I — Corporate, Legal, Regulatory & Institutional Anatomy
3. Part II — Product, Customer & Service-Delivery Architecture
4. Part III — Operations, Technology, Data & Organisational Infrastructure
5. Part IV — Financial Statements, Revenue Architecture, Unit Economics & Capital
6. Part V — Management, Culture, Competition, Moat, Risk & Strategic Evolution
7. Part VI — Cross-Volume Synthesis
8. Appendix A — Glossary of German Terms
9. Appendix B — Canonical Figures Register
10. Appendix C — Reconciliation of Cross-Volume Discrepancies
11. Appendix D — Source Hierarchy & Evidence Conventions

**Do not collapse these into fewer top-level headings.** A previous render produced a single `h1` for the entire document. That is a build failure.

**2.2 Heading hierarchy must follow the source.** Numbered sections (I.1, II.5, III.12, IV.8, V.16, VI.3 and so on) are second-level. Their subsections are third-level. Do not push second-level sections down to `h4`; do not flatten third-level sections up to `h2`. The source markdown hierarchy is correct — mirror it.

**2.3 Table of contents.** A three-level contents list at the front, covering all eleven top-level sections, every numbered section, and every named subsection. Expect **at least 130 entries**. Each entry links to its target. If page numbers are available in the output medium, include them.

**2.4 Persistent navigation.** Because the document is long, provide a persistent means of moving between the eleven top-level sections without scrolling to the top — a sidebar, a sticky header, or an equivalent. Include a running indicator of which Part the reader is currently in.

**2.5 Cross-references are live.** Where the text refers to "Volume I", "Volume III", "§III.8", "Appendix B" or "II.5", link it to the target.

**2.6 Anchors on every heading.** Every heading at every level receives a stable `id` so any section can be linked directly.

---

## 3. TYPOGRAPHY AND TABLES

**3.1 Design system: Industry.** Barlow Condensed for headings, Barlow for body.

**3.2 Palette override.** Use gun-steel as the neutral and gold as the accent, overriding the system defaults. Gold must be darkened sufficiently to remain legible at 8pt on a light background — the evidence labels use the accent and must stay readable.

**3.3 Tabular numerals are mandatory** in every table and in every stat component. This document's core argument rests on comparing figures across columns — Atruvia AG versus Atruvia Group, year against year. Proportional figures will misalign those columns and undermine the content.

**3.4 Wide tables.** Several tables are wide — the risk register, the competitor comparison, the multi-year financial history, the reconciliation appendix. Handle them in this order of preference: (a) let the widest run landscape on their own page or in a full-bleed container; (b) allow horizontal scroll within the table container; (c) reduce type size within the table. **Never drop columns and never split a table's columns across two stacked halves** — the comparison is the content.

**3.5 German hyphenation.** Enable hyphenation with German language rules. The document contains compound nouns of 25+ characters (Digitalisierungsumlage, Bundeseinheitliches Strategieportfolio, Bankaufsichtliche Anforderungen an die IT). Without hyphenation these will punch holes in the measure.

**3.6 Evidence labels.** Render as small typographic tags in the accent colour — visible and findable but quiet enough not to interrupt reading at the density they occur.

**3.7 Measure.** Cap body text at roughly 65–75 characters per line. Tables and figures may exceed this.

---

## 4. FIGURE MANIFEST — build all fifteen

Fifteen figures are specified below **with their data**. Build every one. Do not substitute, omit, or invent alternatives. Do not replace a specified figure with a table — these exist precisely because the underlying tables under-communicate.

Each figure must be numbered (Figure 1 … Figure 15), captioned, and placed in the section named.

---

### Figure 1 — The Ownership Cascade
**Place in:** Part I, section I.3 · **Type:** flow/hierarchy diagram

```
~700 cooperative member banks
        │
        ├── Atruvia Beteiligungs-GmbH & Co. KG Baden-Württemberg (Stuttgart)
        ├── Atruvia Beteiligungs GmbH & Co. KG Nord (Münster)
        └── Bayerische Beteiligungsgesellschaft (BBA, Beilngries) — 14.15%
                        │
                        ▼
        VR-FGI Beteiligungsholding GmbH & Co. KG  ── 91.63% of share capital
                        │
                        ▼
                ATRUVIA AG (HRB 102381)
                Share capital €115.8m
```
**Side panel — full ownership split:** Beteiligungsgesellschaften 91.63% · Primärbanken 6.71% · **DZ Bank 0.35%** · other cooperative entities ~1.0% · private banks 0.32% · **total cooperative 99.68%**

**Callout, prominent:** "DZ Bank holds 0.35%, not 20%. The widely-repeated 20% figure refers to Verimi."

---

### Figure 2 — The Profit Is The Levy
**Place in:** Part IV, section IV.4 · **Type:** dual-series bar or line chart · **This is the single most important figure in the document.**

| Year | Betriebsergebnis (AG) | Digitalisierungsumlage |
|---|---|---|
| 2023 | €40.6m | €30m |
| 2024 | €66.6m | €60m |
| 2025 | €89.0m | €90m |

Two series plotted together on the same axis so the reader sees them tracking. **Caption:** "Strip the levy and the underlying operating result is close to zero."

---

### Figure 3 — The Closing Loop
**Place in:** Part VI, section VI.2 · **Type:** circular causal diagram

Seven nodes in a closed loop:
1. ~700 owner-banks — simultaneously customers, owners and governors
2. Set the roadmap **and** set the levy that funds it (BVR committees, Strategieportfolio, Aufsichtsrat)
3. Atruvia builds once for all (agree21, multi-tenant, IBM Z)
4. Regulatory and technical scale economics — MaRisk, BAIT and DORA implemented once for ~700 institutions
5. Each member bank remains viable when it could not survive alone
6. But the banks consolidate anyway — 40–45 mergers/year; ~820 institutions (2022) → ~670 (2025)
7. Fewer, larger owners → greater bargaining power → greater price resistance → investment squeeze → **back to node 1**

**Caption:** "Atruvia's success dissolves its own customer base."

---

### Figure 4 — Outage Blast Radius, 2018–2026
**Place in:** Part III, section III.12 · **Type:** timeline, markers scaled by banks affected

| Date | Event | Banks affected |
|---|---|---|
| May–Aug 2018 | BaFin §44 special inspection — 15 findings, 3 severe | firmwide |
| 10 Jun 2020 | FinTS/CAMT52 special-character bug | FinTS users |
| 9 Nov 2020 | System-changeover error; Krisenstab convened | **150 of 840** |
| 3 Jun 2021 | DDoS attack, Karlsruhe then Münster | firmwide |
| 29 Nov 2023 | Central fault; transfers and account views down | **up to 520 of ~700** |
| 7 Jul 2026 | Central software error; app and online banking switched off to shed load | **~490** |

**Caption:** "The same failure mode recurs: one central fault, hundreds of banks."

---

### Figure 5 — Atruvia versus Finanz Informatik
**Place in:** Part V, section V.7 · **Type:** paired comparison, bars per metric

| Metric | Atruvia | Finanz Informatik |
|---|---|---|
| Revenue (2024) | ~€2.2bn Group | ~€2.6bn |
| Employees | 10,076 Group / 5,847 AG | 5,037 FTE |
| **Revenue per employee** | **~€218k Group / ~€324k AG** | **~€516k** |
| Accounts | 91–97m | ~114m |
| Technical transactions/yr | ~80bn+ | >205bn |
| Institutions served | ~670–700 cooperative | ~350 Sparkassen |
| Core platform | agree21 | OSPlus |
| DORA CTPP designated | No | No |

**Emphasise the revenue-per-employee row — a 2.4× gap.**

---

### Figure 6 — Where One Euro of Revenue Goes
**Place in:** Part IV, section IV.16 · **Type:** waterfall or stacked bar (AG, FY2025)

| Component | Share of Gesamtleistung |
|---|---|
| Materialaufwand / bought-in services (IBM, nearshore, maintenance) | 41.2% |
| Personalaufwand | 34.1% |
| Abschreibungen | 11.1% |
| Sonstige betriebliche Aufwendungen | 9.7% |
| **Betriebsergebnis** | **4.6%** |

**Caption:** "Bought-in services, not personnel, are the largest cost — Atruvia is a systems integrator riding IBM and nearshore capacity."

---

### Figure 7 — The Technology Stack
**Place in:** Part III, section III.4 · **Type:** layered architecture diagram, five bands

- **Client layer** — VR Banking App · OnlineBanking · BankingWorkspace (Angular) · agree21BAP (legacy) · FinTS/HBCI servers
- **Platform layer** — Omnikanalplattform (multi-tenant, ~300 processes) · agree21ECON · EGP Gesamtbanksteuerung
- **Integration layer** — proprietary API layer · **~1,200 Java microservices on Red Hat OpenShift** · IBM MQ for z/OS
- **Core layer** — **IMS transaction manager + IMS DB · Db2 for z/OS · COBOL estate ~85% Java-enabled via IBM Semeru common runtime (31-bit COBOL ↔ 64-bit Java)**
- **Infrastructure** — **8 × IBM z15 hosting 12 IMS systems (→ z17, deal signed 19 Nov 2025) · four data centres, two each in Karlsruhe and Münster**

**Annotate:** ~80bn technical transactions/year · peaks of 12,000 transactions/second · ~400m Java transactions/day

---

### Figure 8 — The Two-Tier Customer Structure
**Place in:** Part II, section II.2 · **Type:** two-tier diagram

- **Tier 1 — Member banks (~670–730 cooperative, plus private banks and non-banks; ~917–950 customers).** Show them wearing three hats simultaneously: **OWNER** · **BUYER** · **GOVERNOR**.
- **Tier 2 — End customers.** Tens of millions of German retail and corporate banking users. ~97m accounts. Label: "do not know Atruvia exists."
- Show the contractual line running end customer → member bank, and the GDPR relationship: **bank = controller, Atruvia = processor.**

**Caption:** "Funded by banks, judged by consumers."

---

### Figure 9 — The Corporate Group
**Place in:** Part I, section I.2 · **Type:** organisational tree with data labels

**Atruvia AG** (5,847 employees AG, 2025) with subsidiaries:

| Entity | Revenue | Employees | Business |
|---|---|---|---|
| Ratiodata SE | €344.5m | ~1,426 | Hardware, field service, self-service estate |
| parcIT GmbH | €78.6m | 507 | Risk & bank-steering software (VR-Control) |
| BMS Corporate Solutions | €52.0m | 303 | Corporate-client solutions, fincompare |
| Peras GmbH | €46.7m | 290 | HR services, payroll |
| Serviscope AG | €28.8m | 451 | BPO, 116 116 card-blocking hotline |
| TRUUCO GmbH | €8.2m | 58 | Smart data — **loss-making, −€7.98m** |
| ECON Application | €4.1m | 35 | No-code platform |
| FORUM GmbH | €3.6m | 20 | InfoSec/GRC software |
| GWS mbH | — | ~670 | ERP for trade |
| Accesa / RaRo | — | ~700 | Nearshore development, Cluj-Napoca |

Mark TRUUCO visually as the loss-maker.

---

### Figure 10 — Consolidation: Fewer Banks, More Accounts
**Place in:** Part II, section II.3 · **Type:** dual-axis chart — declining bars, rising line

| Year | Cooperative banks | Accounts |
|---|---|---|
| 2022 | ~820 | 85m |
| 2023 | ~700 | 89m |
| 2024 | ~700 | 91m |
| 2025 | ~670 | 97m |

Annotate: **40–45 merger migrations per year.** **Caption:** "The owner base shrinks while the workload grows."

---

### Figure 11 — Moat Scorecard: Lock versus Value
**Place in:** Part V, section V.9 · **Type:** two-axis scatter or paired-bar matrix. **X = prevents exit. Y = creates value.**

| Moat | Prevents exit | Creates value |
|---|---|---|
| Captive ownership | 5 | 2 |
| Switching costs | 5 | 2 |
| Ecosystem integration | 4.5 | 4.5 |
| Regulatory capability | 4 | 4 |
| **Migration capability** | **0** | **4** |
| agree21 platform | 3.5 | 3.5 |
| Scale economics | 3 | 3.5 |
| Brand/trust | 3 | 3 |
| Data position | 2 | 2 |

**Caption:** "The largest moats are lock, not value. The genuine advantages — migration and regulatory capability — would survive in a contestable market."

---

### Figure 12 — Risk Heatmap
**Place in:** Part V, section V.16 · **Type:** probability × severity grid, 14 plotted risks

Catastrophic/prolonged outage (Med/Very High) · Cyber and ransomware (Med/Very High) · Investment underfunding (High/High) · IBM dependency and price shock (Med/High) · Further BaFin enforcement (Med/Med-High) · Member-bank consolidation (High/Med) · Reputational contagion (Med/High) · COBOL skills wave (Med/Med) · VR Payment integration (Med/Med) · Key-person, new Vorstand (Med/Med) · DORA CTPP designation (Low-Med/Med) · Data protection breach (Low-Med/High) · Large bank defection (Low/High) · Loss-making subsidiaries (High/Low)

---

### Figure 13 — Capex against Free Cash Flow
**Place in:** Part IV, section IV.13 · **Type:** bar chart with FCF overlay

| Year | Capex (AG) | Investitionsquote |
|---|---|---|
| 2023 | €182.9m | 12.1% |
| 2024 | €208.4m | 12.1% |
| 2025 | **€359.1m** | **18.7%** |

Overlay FY2025: operating cash flow €397.2m − capex €359.1m = **free cash flow ~€38m**.

**Caption:** "After maintaining the mainframe estate, the business runs close to cash-neutral."

---

### Figure 14 — The DORA Supervisory Perimeter
**Place in:** Part I, section I.6 · **Type:** boundary/Venn diagram

Inside the perimeter (designated Critical ICT Third-Party Providers, ESA list of 18 November 2025): **IBM** (Lead Overseer: EBA), AWS, Microsoft, Google Cloud, Oracle, SAP, SWIFT and others — 19 in total.

Outside: **Atruvia** and **Finanz Informatik** — despite a single fault at Atruvia disabling ~490–520 German banks.

**Caption:** "Atruvia's supplier is directly supervised. Atruvia is not."

---

### Figure 15 — Migration Track Record
**Place in:** Part V, section V.9 · **Type:** timeline

2015 merger of Fiducia and GAD · 2017–2019 agree21 "Mondlandung" series migration, 60 migration weekends · 2019 series phase complete, 9 November · 2021–2026: 22 institutions migrated or under way, including all 11 Sparda-Banken, Bank für Sozialwirtschaft, UmweltBank, National-Bank Essen, with M.M. Warburg announced · ongoing: 40–45 merger migrations per year

**Counterpoint panel — the alternative:** Apobank migrated *away* to Avaloq in 2020. Cost a mid-three-digit-million euro sum (third-party estimates ~€500m); customer satisfaction fell from 82% to 47%.

---

## 5. STAT TILE MANIFEST — build all twelve

Twelve prominent stat components. Place the first six in the front matter as an opening summary; distribute the remainder at the openings of the Parts indicated.

| # | Value | Label | Place |
|---|---|---|---|
| 1 | **99.68%** | cooperative-owned | Front matter |
| 2 | **~700** | member banks served | Front matter |
| 3 | **97m** | accounts administered | Front matter |
| 4 | **~10bn** | bookings per year | Front matter |
| 5 | **€2.5bn** | Group revenue, 2025 | Front matter |
| 6 | **10,076** | employees, Group | Front matter |
| 7 | **€89.0m** | Betriebsergebnis, AG 2025 — 4.6% margin | Part IV |
| 8 | **~€90m** | Digitalisierungsumlage, 2025 | Part IV |
| 9 | **~490–520** | banks offline per central fault | Part III |
| 10 | **8 × IBM z15 → z17** | mainframes, four data centres | Part III |
| 11 | **~€218k vs ~€516k** | revenue per employee: Atruvia vs Finanz Informatik | Part V |
| 12 | **40–45** | bank merger migrations per year | Part II |

---

## 6. ANTI-PATTERNS — previous build failures to avoid

Each of these occurred in an earlier render of this exact content:

- **Collapsing all eleven top-level sections into a single `h1`.** Fatal to navigation.
- **Producing no table of contents.** In a 41,000-word reference document this is a build failure.
- **Generating zero diagrams.** Fifteen are specified in §4. Build all fifteen.
- **Pushing numbered sections down to `h4`** so real sections sit four levels deep while trivial ones sit at `h2`.
- **Rendering fewer table rows than the source contains.** Row counts must match.
- **Treating length as a problem to be solved.** It is not. The length is the deliverable.

---

## 7. BUILD CHECKLIST

Before returning output, confirm:

- [ ] ~41,000 words of body prose present
- [ ] ~53 tables, 1,000+ rows, all rendered as tables
- [ ] Eleven `h1` sections, one per Part and Appendix
- [ ] Three-level contents list, 130+ entries, all linked
- [ ] Persistent navigation between top-level sections
- [ ] All fifteen figures built, numbered and captioned
- [ ] All twelve stat tiles placed
- [ ] Evidence labels intact throughout, in the accent colour
- [ ] Tabular numerals active in all tables and stats
- [ ] German hyphenation enabled
- [ ] Wide tables landscape or scrollable, no columns dropped
- [ ] Every heading carries a stable anchor
- [ ] Cross-references linked

---

*The specification ends here. The study follows in full.*

---

