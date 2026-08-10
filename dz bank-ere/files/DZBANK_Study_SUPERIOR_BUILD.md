# BUILD SPECIFICATION — read this before rendering

This document contains a complete institutional research study of approximately **40,300 words**. What follows is a binding specification for how it must be rendered. It is not a suggestion and not editorial guidance. Every clause is a requirement.

Render this study using the scaffolding of the reference build supplied alongside it: a **screen document with a persistent sidebar**, section-opening pages with alternating numerals, stat plates, and drawn figures. Use the **Industry** design system — Barlow Condensed for headings, Barlow for body, with the gun-steel and gold palette overriding the system defaults.

---

## 1. PRESERVATION CONTRACT — non-negotiable

**1.1 Every word is retained.** The body runs to approximately 40,300 words. All of it appears in the output. Do not summarise, condense, abridge, truncate, sample or paraphrase any section. If a section seems repetitive, it stays. If a table seems dense, it stays.

**1.2 Every table renders as a table.** There are approximately **46 tables containing 440 data rows**. Do not convert tables into prose, bullet lists or summary callouts. Do not drop columns to make a table fit — see §3.4.

**1.3 Every evidence label is retained in place.** CONFIRMED FACT, COMPANY CLAIM, THIRD-PARTY ESTIMATE, ANALYTICAL INFERENCE, HYPOTHESIS and UNKNOWN appear several hundred times. They are load-bearing: the study's method depends on each claim carrying its confidence level at the point of reading.

**1.4 Every German term is retained.** Do not translate Förderauftrag, Verbund, Zinsüberschuss, Betriebsergebnis, Sicherungseinrichtung, Bausparkasse, Pfandbrief, Vorstand, Aufsichtsrat or any other German term in the body. Appendix A is the glossary; the body relies on it.

**1.5 No content in a collapsed, hidden or truncated state.**

**Verification:** the output must contain approximately 40,300 words of body prose, approximately 46 tables and 440 data rows.

---

## 2. STRUCTURE CONTRACT

**2.1 Eleven top-level sections**, each rendering as an `h1` with a section-opening treatment:

1. Front matter (title, how to read, conventions)
2. Part I — Corporate, Legal, Regulatory & Institutional Anatomy
3. Part II — Product, Customer, Distribution & Flow Architecture
4. Part III — Operations, Technology, Data, Risk Infrastructure & Organisational Design
5. Part IV — Financial Statements, The Three Economic Engines, Unit Economics & Capital
6. Part V — Management, Culture, Competition, Moat, Risk & Strategic Evolution
7. Part VI — Cross-Volume Synthesis
8. Appendix A — Glossary of German and Regulatory Terms
9. Appendix B — Canonical Figures Register
10. Appendix C — Reconciliation of Cross-Volume Discrepancies
11. Appendix D — Source Hierarchy & Evidence Conventions

**Do not collapse these into fewer top-level headings.**

**2.2 Heading hierarchy follows the source.** Numbered sections (I.1, II.5, III.9, IV.12, V.16, VI.3) are second level; their subsections third level. Do not push second-level sections down, and index every Part to the same depth — do not index one Part more shallowly than the others.

**2.3 Table of contents.** Three levels, covering all eleven top-level sections, every numbered section and every named subsection. Expect **at least 130 entries**, each linked.

**2.4 Persistent navigation** between the eleven top-level sections, with an indicator of the current Part.

**2.5 Cross-references are live.** Link "Volume III", "§IV.12", "Appendix B" and similar to their targets.

**2.6 Anchors on every heading** at every level.

---

## 3. TYPOGRAPHY AND TABLES

**3.1 Design system: Industry.** Barlow Condensed headings, Barlow body.

**3.2 Palette:** gun-steel neutral, gold accent, overriding the system defaults. Darken the gold sufficiently to stay legible at 8pt on light backgrounds — the evidence labels use the accent.

**3.3 Tabular numerals are mandatory** in every table and stat component. This document's central argument rests on comparing figures across perimeters and years; proportional figures will misalign those columns and undermine the content.

**3.4 Wide tables.** The risk register, competitor matrices, multi-year financials and the reconciliation appendix are wide. Handle in this order: full-bleed or landscape on their own page; horizontal scroll within the container; reduced type size. **Never drop columns and never split a table's columns across stacked halves.**

**3.5 German hyphenation enabled.** The document contains compound nouns of 25+ characters (Finanzkonglomerate-Aufsichtsgesetz, Genossenschaftliche FinanzGruppe, Bausparkassengesetz, Beherrschungs- und Gewinnabführungsvertrag).

**3.6 Evidence labels** as small typographic tags in the accent colour.

**3.7 Measure** capped at roughly 65–75 characters for body text.

---

## 4. FIGURE MANIFEST — build all sixteen

Sixteen figures are specified below **with their data**. Build every one, numbered, captioned, and placed in the section named. Do not substitute, omit or invent alternatives, and do not replace a specified figure with a table.

---

### Figure 1 — The Five Perimeters
**Place in:** Front matter, conventions · **Type:** nested boundary diagram

Five nested or adjacent boundaries with scale anchors:
- **DZ BANK AG** — parent only, HGB — operating income €2,835m
- **DZ BANK Group** — IFRS consolidated — ~€661bn assets, €4,282m pre-tax
- **Genossenschaftliche FinanzGruppe** — the whole sector — **€1.68trn assets, €11.6bn pre-tax**
- **CRR prudential scope** — excludes insurance — RWA €148.6bn
- **Solvency II group (R+V)** — own funds €17.05bn, SCR €8.37bn

**Caption:** "The sector is roughly 2.5 times the group's balance sheet and 2.7 times its profit. Conflating them is the most common error in commentary on DZ BANK."

---

### Figure 2 — Ownership Cascade
**Place in:** Part I, section I.3 · **Type:** flow diagram

~645 primary cooperative banks → **94.8%** → DZ BANK AG (HRB 45651, BIC GENODEFF). Side panel: cooperative banks 94.8% · other cooperative enterprises 4.8% · others 0.5%.

**Callout:** "DZ BANK holds ~0.35% of Atruvia, not 20%. The 20% figure refers to Verimi."

---

### Figure 3 — The Three Economic Engines
**Place in:** Part IV, section IV.2 · **Type:** segmented bar, FY2025 pre-tax (€m)

| Segment | Result |
|---|---|
| R+V | 2,144 |
| Union Investment | 1,185 |
| CICB (the bank) | 864 |
| DZ HYP | 338 |
| BSH | 122 |
| DZ PRIVATBANK | 106 |
| TeamBank | −29 |
| VR Smart Finanz | −28 |
| Holding | −335 |
| Other | −85 |

Group total €4,282m. Colour insurance and asset management distinctly and annotate: **~78% of profit**.

**Caption:** "The bank is the third-largest contributor to its own group."

---

### Figure 4 — The Three Capital Regimes Do Not Reconcile
**Place in:** Part IV, section IV.12 · **Type:** three separate gauges, deliberately not summed

- **CET1 18.4%** — banking group only, excludes insurance
- **Solvency II 203.8%** — R+V only
- **FKAG conglomerate 136.1%** — the whole group; thresholds at 100% external, 113% internal, 123% observation

**Caption:** "The conglomerate ratio sums two full requirement stacks with no diversification credit. It, not the CET1, is the binding constraint."

---

### Figure 5 — The Protection Scheme and the Rating
**Place in:** Part I, section I.6 · **Type:** ladder/uplift diagram

Moody's: standalone BCA **baa2** (baa1 from November 2025) → Adjusted BCA **a3** via scheme support → **Aa2** with LGF uplift. Alongside: **S&P A+** equalised to the sector's 'a+' group credit profile, no ALAC uplift. **Fitch AA-/AA** — a single group rating covering DZ BANK and ~700 primary banks. **DBRS AA (low)** — one notch of scheme uplift.

**Caption:** "One to two notches of the rating come from the scheme, not from standalone strength."

---

### Figure 6 — Group Structure
**Place in:** Part I, section I.2 · **Type:** organisational tree with data labels

DZ BANK AG with: R+V (€22.8bn premiums, >18,400 staff, ~26m insured risks) · Union Investment (€534.6bn AuM, 72.37% held) · Bausparkasse Schwäbisch Hall (~7m contracts, 33.3% share) · DZ HYP (€57.6bn portfolio, largest Pfandbrief issuer) · DZ PRIVATBANK (€30.7bn AuM, €181.3bn custody) · TeamBank (€9,132m book, loss-making) · VR Smart Finanz (loss-making) · VR Payment (~248 staff). Mark the two loss-makers visually.

**Side note:** "Münchener Hypothekenbank is an independent cooperative bank OUTSIDE the group — an in-sector competitor."

---

### Figure 7 — Five Supervisory Regimes Plus Conglomerate Supervision
**Place in:** Part I, section I.6 · **Type:** matrix, entity against regime

ECB/SSM banking (DZ BANK AG, DZ HYP) · Solvency II/BaFin (R+V) · KAGB/UCITS/AIFMD (Union Investment) · Bausparkassengesetz (BSH) · CSSF Luxembourg (DZ PRIVATBANK) · **FKAG conglomerate supervision spanning all**. Plus SRB resolution, DORA, GwG, MiFID II as cross-cutting.

---

### Figure 8 — The Manufacture-and-Distribute Chain
**Place in:** Part II, section II.5 · **Type:** six-step flow

Subsidiary manufactures → product enters the Verbund catalogue → **primary bank chooses whether to sell (legally optional)** → adviser sells to end customer → contract sits with the manufacturer → commission flows back to the primary bank, which keeps the relationship and the data.

**Caption:** "No contract compels a primary bank to sell group products. Shelf space is won on merit and roughly €1.57bn a year in commissions."

---

### Figure 9 — FY2025 to FY2026: The Windfall Unwinds
**Place in:** Part IV, section IV.20 · **Type:** bridge/waterfall

Start €4,282m (FY2025) → less the R+V low-claims windfall (~€700–900m) → less trading and market recovery (~€200–300m) → less below-normal loss allowances (~€200m) → **arrive at ~€3.0bn FY2026 guidance**. Show structural earnings power of ~€2.9–3.1bn as the base.

**Caption:** "Management guides down €1.3bn. The combined ratio fell from 94.9% to 86.6% — that does not repeat."

---

### Figure 10 — The Correlation Risk
**Place in:** Part V, section V.16 · **Type:** convergence diagram

A single equity and credit drawdown striking **both** R+V (investment result, Solvency II own funds) **and** Union Investment (AuM-based fees) — together ~78% of group profit — and tightening the FKAG conglomerate ratio.

**Caption:** "Federation across seven operating models gives no protection against the one risk that matters."

---

### Figure 11 — The Distribution Erosion
**Place in:** Part V, section V.14 · **Type:** negative flywheel loop

Branch decline → **R+V referrals fall from ~320,000 to under 200,000 a year** → weaker bancassurance → less commission for primary banks → less incentive to distribute → back to the start. Second loop: consolidation from 672 to ~645 banks → fewer, stronger owners → greater willingness to source externally.

---

### Figure 12 — Payments Scale
**Place in:** Part III, section III.2 · **Type:** column chart

FY2023 **9.9bn** → FY2024 **10.2bn** → FY2025 **11.0bn** transactions on the insourced ZV ON€ platform. Annotate: ~500 people, five years, 100,000+ person-days, >600 banks migrated by end-2024, ~1.8 cents revenue per transaction.

---

### Figure 13 — Competitive Map by Engine
**Place in:** Part V, section V.6 · **Type:** matrix, one row per engine

| Engine | Principal competitors |
|---|---|
| Central institution | Landesbanken (Helaba, LBBW, BayernLB, NORD/LB) |
| Corporate & capital markets | Commerzbank, Deutsche Bank, UniCredit — **and its own owner-banks** |
| Insurance (R+V) | Allianz, Generali, Talanx, Debeka, HUK-Coburg, Provinzial/SV |
| Asset management (Union) | DekaBank, DWS, Amundi — and **BlackRock/iShares, Trade Republic, Scalable** |
| Bauspar (BSH) | LBS, Wüstenrot, Debeka — and Europace/Interhyp platforms |
| Consumer credit (TeamBank) | Santander, TARGOBANK, Check24, Klarna, PayPal |
| Payments | Worldline, Nexi, Adyen, Stripe, S-Payment/Qards — and **Atruvia from 2027** |
| Real estate (DZ HYP) | **Münchener Hypothekenbank** (in-sector), Berlin Hyp, Aareal, pbb |

**Caption:** "There is no single competitor list. Each engine faces a different industry."

---

### Figure 14 — Moat Scorecard: Prevents Exit versus Creates Value
**Place in:** Part V, section V.9 · **Type:** two-axis scatter, X = prevents exit, Y = creates value

| Moat | Prevents exit | Creates value |
|---|---|---|
| Institutional protection scheme | 5 | 5 |
| Central-institution mandate | 5 | 4 |
| Ownership by distributors | 4 | 2 |
| Ecosystem integration (Atruvia rails) | 4 | 3 |
| Payments/clearing platform | 3 | 3 |
| Regulatory capability | 3 | 3 |
| Union Investment AuM annuity | 3 | 4 |
| R+V underwriting scale | 3 | 3 |
| BSH Bauspar share | 4 | 3 |
| DZ HYP Pfandbrief franchise | 3 | 3 |
| Brand and trust | 3 | 3 |

**Caption:** "The protection scheme is the only moat in the top-right corner that does not depend on the owner-banks choosing to distribute."

---

### Figure 15 — Risk Heatmap
**Place in:** Part V, section V.16 · **Type:** probability × severity grid, 15 risks

Correlated equity/credit drawdown (Med/High) · CMDI reform curtailing the IPS (Low/Existential) · Nat-cat year at R+V (High/Med) · German CRE deterioration (Med/Med-High) · Second BayWa (Med/Med) · Member-bank consolidation (High/Med) · Erosion of Verbundtreue (Med/High) · Atruvia dependency and the 2027 migration (Med/Med) · Passive/ETF disruption of Union (High/Med-High) · Branch-decline erosion (High/Med) · Rate normalisation (Med/Low-Med) · Key-person and succession (Med/Med) · Cyber and resilience (Med/High) · Conglomerate capital constraint (Low/High) · Reputational contagion (Med/Med-High).

---

### Figure 16 — What the Group Is Becoming
**Place in:** Part VI, section VI.6 · **Type:** ranked probability bars

Bancassurance and asset-management holding **35%** · Progressively disintermediated at the retail edge **30%** · Unchanged central institution **20%** · National payments infrastructure **8%** · Consolidates with Sparkassen infrastructure **5%** · Restructured after a crisis **2%**.

---

## 5. STAT TILE MANIFEST — build all twelve

Twelve prominent stat components. Place the first six in the front matter; distribute the rest at the Part openings indicated.

| # | Value | Label | Place |
|---|---|---|---|
| 1 | **94.8%** | cooperative-owned | Front matter |
| 2 | **~645** | primary banks served | Front matter |
| 3 | **€661bn** | group total assets | Front matter |
| 4 | **€4,282m** | profit before taxes, FY2025 | Front matter |
| 5 | **~78%** | of profit from insurance and asset management | Front matter |
| 6 | **~33,837** | group employees | Front matter |
| 7 | **€534.6bn** | Union Investment assets under management | Part II |
| 8 | **€22.8bn** | R+V gross written premiums | Part II |
| 9 | **11.0bn** | payment transactions per year | Part III |
| 10 | **18.4% / 203.8% / 136.1%** | CET1 · Solvency II · conglomerate coverage | Part IV |
| 11 | **~1–2 notches** | rating uplift from the protection scheme | Part V |
| 12 | **~€3.0bn** | FY2026 guidance, down from €4,282m | Part VI |

---

## 6. ANTI-PATTERNS — build failures to avoid

- **Collapsing the eleven top-level sections into fewer `h1`s.** Fatal to navigation.
- **Producing no table of contents**, or indexing one Part more shallowly than the others.
- **Generating no diagrams.** Sixteen are specified. Build all sixteen.
- **Rendering fewer table rows than the source contains.**
- **Blending the five perimeters** in any figure or stat tile. Every number carries its perimeter.
- **Treating length as a problem to be solved.** It is not. The length is the deliverable.

---

## 7. BUILD CHECKLIST

- [ ] ~40,300 words of body prose present
- [ ] ~46 tables, ~440 data rows, all rendered as tables
- [ ] Eleven `h1` sections, one per Part and Appendix
- [ ] Three-level contents list, 130+ entries, all linked
- [ ] Persistent navigation between top-level sections
- [ ] All sixteen figures built, numbered and captioned
- [ ] All twelve stat tiles placed
- [ ] Evidence labels intact in the accent colour
- [ ] Tabular numerals active in all tables and stats
- [ ] German hyphenation enabled
- [ ] Wide tables full-bleed or scrollable, no columns dropped
- [ ] Every heading carries a stable anchor
- [ ] Cross-references linked

---

*The specification ends here. The study follows in full.*

---

# The DZ BANK Enterprise Reverse-Engineering Study

**A forensic institutional teardown of DZ BANK AG and the DZ BANK Group — the central institution of the German cooperative banking sector**

Research cut-off: 9 August 2026
Prepared by: Damascus Research
Volumes I–V complete · Cross-Volume Synthesis included

---

## Table of Contents

- [The DZ BANK Enterprise Reverse-Engineering Study](#the-dz-bank-enterprise-reverse-engineering-study)
  - [How to read this document](#how-to-read-this-document)
  - [Conventions governing the whole document](#conventions-governing-the-whole-document)
- [Part I — Corporate, Legal, Regulatory & Institutional Anatomy](#part-i-corporate-legal-regulatory-institutional-anatomy)
- [Part II — Product, Customer, Distribution & Flow Architecture](#part-ii-product-customer-distribution-flow-architecture)
- [Part III — Operations, Technology, Data, Risk Infrastructure & Organisational Design](#part-iii-operations-technology-data-risk-infrastructure-organisational-design)
- [Part IV — Financial Statements, The Three Economic Engines, Unit Economics & Capital](#part-iv-financial-statements-the-three-economic-engines-unit-economics-capital)
- [Part V — Management, Culture, Competition, Moat, Risk & Strategic Evolution](#part-v-management-culture-competition-moat-risk-strategic-evolution)
- [Part VI — Cross-Volume Synthesis](#part-vi-cross-volume-synthesis)
  - [VI.1 The name is the first mistake](#vi1-the-name-is-the-first-mistake)
  - [VI.2 The single causal model — a fortress core and a contested edge](#vi2-the-single-causal-model-a-fortress-core-and-a-contested-edge)
  - [VI.3 What the volumes prove together that none proves alone](#vi3-what-the-volumes-prove-together-that-none-proves-alone)
  - [VI.4 The central tension](#vi4-the-central-tension)
  - [VI.5 What would falsify this reading](#vi5-what-would-falsify-this-reading)
  - [VI.6 What the group is becoming](#vi6-what-the-group-is-becoming)
  - [VI.7 Implications for a fintech builder](#vi7-implications-for-a-fintech-builder)
  - [VI.8 Ten cross-volume conclusions](#vi8-ten-cross-volume-conclusions)
- [Appendix A — Glossary of German and Regulatory Terms](#appendix-a-glossary-of-german-and-regulatory-terms)
  - [Sector and institutional](#sector-and-institutional)
  - [Protection scheme](#protection-scheme)
  - [Accounting and financial](#accounting-and-financial)
  - [Corporate and governance](#corporate-and-governance)
  - [Products](#products)
  - [Regulatory](#regulatory)
- [Appendix B — Canonical Figures Register](#appendix-b-canonical-figures-register)
  - [Group financials — DZ BANK Group (IFRS), FY2025](#group-financials-dz-bank-group-ifrs-fy2025)
  - [Segment pre-tax, FY2025 (€m)](#segment-pre-tax-fy2025-m)
  - [The three capital regimes — never reconcile to one number](#the-three-capital-regimes-never-reconcile-to-one-number)
  - [Ownership and structure](#ownership-and-structure)
  - [Subsidiary scale](#subsidiary-scale)
  - [Operations](#operations)
  - [Ratings and the protection scheme](#ratings-and-the-protection-scheme)
  - [Sector context — Genossenschaftliche FinanzGruppe perimeter, NOT DZ BANK](#sector-context-genossenschaftliche-finanzgruppe-perimeter-not-dz-bank)
- [Appendix C — Reconciliation of Cross-Volume Discrepancies](#appendix-c-reconciliation-of-cross-volume-discrepancies)
  - [Perimeter, date and basis differences — not errors](#perimeter-date-and-basis-differences-not-errors)
  - [Genuine errors and corrections](#genuine-errors-and-corrections)
  - [Known unknowns carried forward](#known-unknowns-carried-forward)
- [Appendix D — Source Hierarchy & Evidence Conventions](#appendix-d-source-hierarchy-evidence-conventions)

## How to read this document

This study takes the DZ BANK Group apart component by component across five volumes, then reassembles it. Each volume was researched and written as a standalone study; this master edition binds them into one document with a single set of conventions, a glossary, a canonical figures register, and a synthesis that no individual volume contains.

| Part | Volume | Question it answers |
|---|---|---|
| Front matter | — | Conventions, glossary, canonical figures, how to navigate |
| Part I | Corporate, Legal, Regulatory & Institutional Anatomy | Who owns and controls the group; how a customer-owned conglomerate is governed across five supervisory regimes |
| Part II | Product, Customer, Distribution & Flow Architecture | What the group manufactures, who sells it, and what each party earns |
| Part III | Operations, Technology, Data, Risk Infrastructure & Organisational Design | How seven regulated operating models run as one federated group |
| Part IV | Financial Statements, Three Economic Engines, Unit Economics & Capital | How three incompatible economic machines and three capital regimes coexist |
| Part V | Management, Culture, Competition, Moat, Risk & Strategic Evolution | Why the group persists, what is genuinely defensible, and what it becomes |
| Part VI | **Cross-Volume Synthesis** | What the five volumes prove together that none proves alone |
| Appendix A | Glossary of German and Regulatory Terms | Load-bearing — read before Part IV |
| Appendix B | Canonical Figures Register | The governing value for every material number, with its perimeter |
| Appendix C | Reconciliation of Cross-Volume Discrepancies | Where the volumes disagree, and which figure governs |
| Appendix D | Source Hierarchy & Evidence Conventions | How claims were graded |

**Recommended reading order for a first pass:** Appendix A (glossary) → the perimeter convention below → Part VI (Synthesis) → Appendix B → then Parts IV and V in full. Parts I, II and III are reference-depth.

---

## Conventions governing the whole document

### Evidence classification

Every material claim carries one of six labels. No inference is silently promoted to fact.

| Label | Meaning |
|---|---|
| **CONFIRMED FACT** | Directly supported by reliable primary evidence |
| **COMPANY CLAIM** | Stated by the group, not independently verified |
| **THIRD-PARTY ESTIMATE** | Externally reported or estimated |
| **ANALYTICAL INFERENCE** | Reasonably inferred from multiple known facts |
| **HYPOTHESIS** | Possible explanation requiring further evidence |
| **UNKNOWN** | Available evidence is insufficient |

### The governing convention — FIVE perimeters. Read this before any figure.

This is the single most important reading instruction in the document, and the most common source of error in third-party commentary on the group. Five distinct perimeters recur throughout, and they are **never** spliced:

| # | Perimeter | What it is | Scale anchor |
|---|---|---|---|
| 1 | **DZ BANK AG** | The parent institution alone, HGB Einzelabschluss | Operating income €2,835m (2025) |
| 2 | **DZ BANK Group / Konzern** | IFRS consolidated, including R+V, Union Investment, BSH, DZ HYP and the rest | ~€661bn assets; €4,282m pre-tax (2025) |
| 3 | **Genossenschaftliche FinanzGruppe** | The **whole cooperative sector**, including the ~645 primary banks — **NOT DZ BANK** | €1.68trn assets; €11.6bn pre-tax (2025) |
| 4 | **Bankenaufsichtlicher Konsolidierungskreis** | CRR prudential scope — **excludes the insurance business** | RWA €148.6bn |
| 5 | **Solvency II group (R+V)** | The insurance perimeter, separately supervised | Own funds €17.05bn; SCR €8.37bn |

Perimeter 3 is quoted as though it were the group more often than any other figure in German banking commentary. It is roughly **2.5 times** the group's balance sheet and **2.7 times** its profit. Every figure in this document carries its perimeter.

### Accounting-basis discipline

The group reports simultaneously under **IFRS** (consolidated group), **HGB** (parent and several subsidiaries) and **Solvency II** (R+V). Three consequences matter throughout:

1. **IFRS 17** applies to insurance from 2023 and fundamentally changed presentation. "Net income from insurance business" is an IFRS 17 construct, **not** premium income, and pre-2023 and post-2023 insurance figures are not comparable without adjustment.
2. **CRR III** took effect on 1 January 2025 and lowered risk-weighted assets, which is the main reason the CET1 ratio rose from 15.8% to 18.4% without a capital raise.
3. **Capital cannot be expressed as one number** — see Appendix B and Part IV.

### Language

Primary sources are overwhelmingly German. German terms are retained where translation would lose precision, and are defined in Appendix A.

---


---

# Part I — Corporate, Legal, Regulatory & Institutional Anatomy

*Enterprise Reverse-Engineering Framework, Subject III. Standalone study; structural contrasts with Wise plc and Atruvia AG noted only where they illuminate DZ BANK. As of August 2026, using FY2025 (31 Dec 2025) results and mid-2026 governance.*

### TL;DR
- **DZ BANK is a customer-owned central institution wrapped inside a bank-plus-insurance financial conglomerate.** As of 31 December 2025, ~94.8% of DZ BANK AG is held by the cooperative banks; the IFRS group (~€661bn total assets, €4.282bn pre-tax profit FY2025) is a BaFin-designated financial conglomerate combining the DZ BANK banking group (under direct ECB supervision) with one of Germany's largest insurers (R+V under Solvency II), an asset manager (Union Investment), a Bausparkasse (Schwäbisch Hall) and Germany's largest Pfandbrief bank (DZ HYP).
- **Actual control sits with the owner-banks, not with Frankfurt management.** Roughly 645 primary cooperative banks (as of end-November 2025) collectively control DZ BANK through the AGM and a supervisory board of owner-bank CEOs, coordinated by the BVR. The single most distinctive institutional feature is the BVR's institutional protection scheme (IPS): no member has failed since 1934, and the scheme delivers the sector's AA-band ratings and a 0% risk weight on intra-network exposures under Article 113(7) CRR.
- **The most misunderstood feature is the perimeter.** DZ BANK AG ≠ DZ BANK Group ≠ Genossenschaftliche FinanzGruppe (~€1.175trn). This report labels every figure by perimeter and corrects the frequently-repeated error that DZ BANK holds ~20% of Atruvia — it holds ~0.35%; the ~20% figure refers to Verimi.

### Key Findings
1. **Product of successive mergers.** DZ BANK AG in its current form dates from the 2001 merger of DG BANK and GZ-Bank; the 2016 absorption of WGZ BANK left a single cooperative central institution for the first time; the 2018 merger of DG HYP and WL BANK created DZ HYP; DVB Bank was wound down and became defunct in 2022.
2. **Ownership is concentrated in the sector itself.** As of 31 December 2025, cooperative banks (direct and indirect) hold 94.8%, other cooperative enterprises 4.8%, and others 0.5% of DZ BANK AG (DZ BANK's own factsheet).
3. **Two-tier governance populated by owner-customers.** The eight-member Vorstand (CEO Dr Cornelius Riese) is supervised by a quasi-parity co-determined Aufsichtsrat chaired by Henning Deneke-Jöhrens, itself dominated by serving cooperative-bank CEOs — the bank's own customers and owners.
4. **Five simultaneous supervisory regimes plus conglomerate supervision.** Banking (ECB/SSM + BaFin/Bundesbank), insurance (Solvency II/BaFin for R+V), funds (KAGB/AIFMD/UCITS for Union Investment), Bausparkassen (BSpKG for Schwäbisch Hall), Luxembourg (CSSF for DZ PRIVATBANK), plus FKAG financial-conglomerate supplementary supervision and SRB resolution planning.
5. **The IPS is the load-bearing wall.** Dual structure: the older BVR-SE (institution protection, since 1934) and the statutory BVR-ISG (deposit guarantee + Article 113(7) IPS since 2015). It underpins the 0% risk-weighting of intra-network exposures and the sector's ratings.
6. **Card business reorganisation underway.** VR Payment's Issuing-Processing division transfers to Atruvia effective 1 January 2027 (Bundeskartellamt case B9-75/26, notified 15 July 2026), concentrating debit and credit card processing at the sector's IT utility while VR Payment refocuses on acquiring/merchant business.

### Details

#### I.1 Origin and Corporate History — Chronological Institutional Evolution

**CONFIRMED FACT.** The cooperative banking movement has two nineteenth-century founders: Hermann Schulze-Delitzsch (urban credit cooperatives, from 1859) and Friedrich Wilhelm Raiffeisen (rural credit unions, 1860s). DZ BANK dates its oldest direct "root" to 1883, when Wilhelm Haas supported the establishment of the **Landwirtschaftliche Genossenschaftsbank AG** in Darmstadt — a central institution owned by the savings-and-loan cooperatives of Hesse, created to perform liquidity compensation and to run payments/collection for the joint procurement of agricultural commodities. It over-extended into non-cooperative business, incurred heavy losses, and was forced to restructure in 1904 — an early demonstration of the recurring hazard when a cooperative central institution strays from its Förderauftrag (a pattern later echoed by DVB Bank).

The **Preußische Central-Genossenschafts-Kasse ("Preußenkasse")** was founded in 1895 as a state central bank for cooperatives. Its lineage ran through the Deutsche Genossenschaftskasse, which the **DG BANK Deutsche Genossenschaftsbank Act of 1975** renamed and expanded into DG BANK, broadening its banking purview. DG BANK opened international offices (New York and Hong Kong) as early as 1976; by 1998 its balance sheet exceeded DM 500 billion. In July 1990 DG BANK took over the central-institution function in the new federal states (former East Germany) as part of a sector-wide solidarity action.

**Progressive consolidation of regional central institutions (Zentralbanken).** Historically the sector ran a three-tier structure (primary banks → regional central banks → national apex) in western/south-western Germany and a two-tier structure in the north, east and south. Regional central institutions merged over decades; SGZ-Bank and GZB-Bank merged in 2000 to form GZ-Bank.

**2001 — DG BANK + GZ-Bank → DZ BANK.** On 24 June 2001 (completed September 2001) DG BANK and GZ-Bank merged to form DZ BANK AG Deutsche Zentral-Genossenschaftsbank, then Germany's sixth-largest bank. *Structural change:* a dominant national apex with a combined product-subsidiary portfolio. *Path dependency:* WGZ BANK (western Germany) remained independent, so the sector retained two competing central institutions for a further fifteen years — a structural inefficiency that shaped the 2016 merger and its constituency politics.

**2016 — DZ BANK + WGZ BANK.** DZ BANK's AGM approved the merger with WGZ BANK (Westdeutsche Genossenschafts-Zentralbank, Düsseldorf) on 22 June 2016 with 99.99% of represented capital (WGZ's AGM: 99.9%); the combined central institution began operating on 1 August 2016. *Structural change:* for the first time a single central institution for the entire sector, completing the transformation to a two-tier structure begun in the 1980s. *New dependency/obligation:* a north (ex-WGZ) / south (ex-DG) constituency division became embedded in the shareholder base and the supervisory board — a fault line still visible in board composition and in the co-CEO arrangement of 2019–2024.

**2018 — DG HYP + WL BANK → DZ HYP.** The two cooperative real-estate banks merged (agreement 20 March 2018; AGMs 25/28 May 2018; Commercial Register entry 27 July 2018, retroactive to 1 January 2018). WL BANK was merged into DG HYP, which was renamed **DZ HYP AG** (AG Hamburg, HRB 5604). *Capability gained:* Germany's largest Pfandbrief issuer (the two issuers had ~€45.3bn of Pfandbriefe outstanding at Q1 2017). *Rationale:* eliminate duplication after the 2016 merger had left two cooperative real-estate banks under one roof — pure post-merger housekeeping.

**DVB Bank — disposal/wind-down.** DVB Bank SE (transport finance: shipping, aviation, land transport, offshore) was crippled by the post-2008 shipping slump — a net loss of €547m and −73% RoE in H1 2017, with H1 provisions of €445m. DZ BANK squeezed out DVB minority shareholders in August 2017 (ending the Frankfurt listing), then wound down and sold in tranches: land transport to Helaba; the aviation-finance portfolio (~€5.6bn) to Japan's MUFG (agreed early 2019); shipping wound down from December 2018. DVB Bank SE became **defunct on 12 August 2022**, merged into DZ BANK. *Capability lost:* a once-top-five global transport-finance franchise. *Lesson embedded:* a non-core, cyclical, US-dollar-funded specialist book is a poor fit inside a cooperative apex — reinforcing the sector's preference for the "one champion per product" architecture.

**2026–2027 — card-business reorganisation.** On 2 July 2026 Atruvia, DZ BANK and VR Payment signed contracts to reorganise the jointly-operated card business effective 1 January 2027: **Atruvia acquires VR Payment's Issuing-Processing division** and will run debit *and* credit card processing on an integrated platform (Giro/debit/credit cards), working closely with DZ BANK; VR Payment refocuses on acquiring, POS network operation and the merchant business. The transaction was notified to the Bundeskartellamt on 15 July 2026 (**case B9-75/26**, "Atruvia AG (D); Erwerb des Issuing Processing Geschäfts von der VR Payment GmbH"). *Structural effect:* effectively a partial break-up of VR Payment and the concentration of card issuing-processing in the sector's IT utility — a significant event because a large share of German credit-card transactions already runs through Atruvia's systems. **COMPANY CLAIM / PENDING:** completion is subject to Bundeskartellamt clearance.

#### I.2 Corporate Group Structure

**Perimeter discipline (CRITICAL).** Three reporting bases must never be conflated:
1. **DZ BANK AG** — the parent institution (HGB Einzelabschluss). AG Frankfurt am Main, HRB 45651; BLZ 500 604 00; BIC GENODEFF; VAT DE114103491.
2. **DZ BANK Group/Konzern** — IFRS consolidated, including R+V, Union Investment (UMH), BSH, DZ HYP, DZ PRIVATBANK, TeamBank, VR Smart Finanz.
3. **Genossenschaftliche FinanzGruppe** — the whole sector including the ~645 primary banks (~€1.175trn total assets) — this is **NOT** DZ BANK and is the single most common source of secondary-source error.

A fourth, distinct perimeter is the **bankenaufsichtlicher Konsolidierungskreis** (CRR prudential scope — the "DZ BANK Institutsgruppe"), which **excludes** the insurance business. That is why R+V is supervised separately under Solvency II and is only captured together with the bank at **financial-conglomerate** level.

**Group headline figures (DZ BANK Group, IFRS, FY2025, CONFIRMED against the 2025 Annual Report):** profit before taxes **€4,282m** (2024: €3,303m); income taxes €1,402m; net profit **€2,880m**; total assets ~**€661bn**; cost/income ratio 49.3%; net interest income €3,839m (−17.8%); net fee & commission income €3,370m (+5.6%); net income from insurance business €2,024m (+76.5%); loss allowances −€653m (2024: −€845m); administrative expenses €4,804m. Long-term ratings: **S&P A+, Moody's Aa2, Fitch AA-/AA**.

**Segment pre-tax earnings contribution (FY2025, €m):** R+V **2,144**; UMH (Union Investment) **1,185**; DZ BANK Central Institution & Corporate Bank (CICB) **864**; DZ HYP **338**; BSH **122**; DZ PRIVATBANK **106**; TeamBank **−29**; VR Smart Finanz **−28**; DZ BANK holding function **−335**; other/consolidation **−85**. **ANALYTICAL INFERENCE:** the group's earnings are dominated by *insurance and asset management*, not by the bank — R+V and UMH together contributed €3.3bn of the €4.28bn pre-tax result, i.e. ~78%. This is the single most important economic fact about the group and reframes DZ BANK as a bancassurance holding whose bank is only one of several profit engines.

**Full material-entity table:**

| Entity | Seat / Register | DZ BANK ownership | Regulator / regime | Primary business | Scale (latest) |
|---|---|---|---|---|---|
| **DZ BANK AG** | Frankfurt; AG Frankfurt HRB 45651 | Parent (94.8% cooperative-owned) | ECB/SSM (Significant Institution) + BaFin/Bundesbank | Central institution, corporate & investment bank, group holding | CICB total assets ~€387.5bn; CICB pre-tax €864m; ~5,981 employees (CICB avg) |
| **R+V Versicherung AG (+ R+V group)** | Wiesbaden | ~96% | BaFin, Solvency II; group supervision | Insurance (life, health, P&C, active reinsurance) | Group premiums €20.9bn (2024, +5.4%); IFRS group pre-tax €1.275bn (2024); SCR ratio 168% (end-2024, ex-transitionals) |
| **Union Asset Management Holding AG (Union Investment)** | Frankfurt | ~93% | BaFin, KAGB / UCITS / AIFMD | Asset management (retail + institutional) | AuM **€534.7bn** (year-end 2025); ~6m investors; ~4,400 staff |
| **Bausparkasse Schwäbisch Hall AG** | Schwäbisch Hall | ~96.8% | BaFin, Bausparkassengesetz | Bausparkasse, home finance | Total assets €82.7bn (2024); CET1 25.4%; Bauspar market share ~35% (largest in Germany); ~7m contracts |
| **DZ HYP AG** | Hamburg & Münster; AG Hamburg HRB 5604 | ~98% | BaFin/ECB, Pfandbrief Act | Commercial real estate & public-sector finance | Germany's largest Pfandbrief issuer; pre-tax €338m (2025) |
| **DZ PRIVATBANK S.A.** | Luxembourg (+ Zurich) | ~92% | CSSF (Luxembourg); FINMA (Switzerland) | Private banking, fund services, FX lending | AuM €30.7bn; AuC €181.3bn; pre-tax €105.5m (2025); >1,200 employees, 8 sites |
| **TeamBank AG (easyCredit / der faire Credit)** | Nuremberg | ~92% | BaFin | Consumer lending; embedded finance | Total assets ~€10.2bn; DE market share 3.9% (2025); Austria 12.3%; pre-tax −€29m (2025) |
| **VR Smart Finanz AG** | Eschborn (ex-VR-Leasing) | ~100% | BaFin (leasing/finance) | SME leasing, hire-purchase, credit | Pre-tax −€28m (2025) |
| **VR Payment GmbH** | Frankfurt | via DZ BANK | ZAG / BaFin (payment services) | Acquiring, POS, merchant business (issuing-processing until 31 Dec 2026) | ~248 employees |
| **DVB Bank SE** | Frankfurt | Defunct 12 Aug 2022 | — | Former transport finance | Wound down |

**Other material / historically significant entities:** ReiseBank AG (cash/FX services), CardProcess (card processing), VR Equitypartner (private equity; booked disposal gains in 2025), VR Factoring GmbH, GENO Broker, DZ Service. Within Union Investment: Union Investment Real Estate GmbH, Union Investment Institutional, Union Investment Luxembourg S.A., Attrax S.A. (Luxembourg fund brokerage/custody) and Quoniam Asset Management. Within R+V: R+V Allgemeine, R+V Lebensversicherung, R+V Krankenversicherung, R+V Re, and the Italian subsidiary Assimoco.

**Why entities are separate (Structure / Control lens).** Regulation is the primary driver: banking, insurance, funds and Bauspar activities must sit in separately-licensed legal entities under distinct supervisory regimes — a Bausparkasse may only conduct Bauspar business under the BSpKG; an insurer cannot hold a banking licence. **Jurisdiction** explains DZ PRIVATBANK (Luxembourg fund-services hub, Swiss private-banking booking centre) and R+V's Italian Assimoco. **Historical merger path-dependence** explains DZ HYP (two banks combined) and the persistence of multiple brands. **Sector-mandate logic** explains the deliberate "one insurer, one asset manager, one Bausparkasse, one consumer lender" architecture: the group runs single sector champions distributed through the primary banks rather than competing internal product factories. **Risk ring-fencing** is a secondary benefit — R+V's insurance risk and DZ HYP's CRE risk are legally contained.

**Simplified economically-important-entities tree.** DZ BANK AG (holding + CICB) → R+V (insurance, ~50% of group profit) → Union Investment/UMH (asset management, ~28%) → DZ HYP (CRE/public finance) → BSH (Bauspar) → DZ PRIVATBANK (private banking) → TeamBank + VR Smart Finanz (consumer/SME credit, currently loss-making) → VR Payment (payments).

#### I.3 Ownership and Control

**Economic ownership (31 Dec 2025, DZ BANK factsheet, CONFIRMED verbatim):** cooperative banks (direct + indirect) **94.8%**; other cooperative enterprises **4.8%**; others **0.5%**. Shares are held directly by primary banks and indirectly through cooperative holding vehicles. **Contrast with Atruvia (EREF Subject II):** Atruvia's control sits in a single pooling vehicle holding 91.63%; DZ BANK's ownership is far more dispersed across the ~645 banks, so no single owner has control — coordination must run through the BVR and the AGM, which makes governance more political and consensus-driven.

**Voting and control (Flow-of-authority lens).** Control is exercised at the Hauptversammlung (AGM); the primary banks collectively elect the shareholder representatives on the Aufsichtsrat, which appoints and can remove the Vorstand and approves strategy. The **BVR** (Bundesverband der Deutschen Volksbanken und Raiffeisenbanken) and the regional Genossenschaftsverbände coordinate the sector's collective interest and audit the primary banks. Economic ownership and voting control are broadly aligned (unlike a listed company with free float): the owners are also the customers and distributors. Management can be removed only by the Aufsichtsrat, which is itself controlled by owner-banks — so ultimate control sits with the membership, not with Frankfurt.

**Conflicts (Control / Economics lens).**
- **Large vs small member banks:** big urban Volksbanken value capital-markets access and corporate-lending capacity; small rural Raiffeisenbanken prioritise cheap standardised services and the protection scheme. Board seats and voting weight mediate this.
- **North (ex-WGZ) vs south (ex-DG):** the 2016 merger embedded a regional-constituency division, still reflected in board composition and in the 2019–2024 co-CEO split.
- **Owner vs competitor (the central tension):** DZ BANK competes with its own owner-banks for corporate/Mittelstand clients. This is managed by the **subsidiarity principle** — DZ BANK is contractually mandated to *support*, not undercut, the primary banks — and by structuring corporate business as **joint/consortium credit ("Metakredit")** where the primary bank retains the client relationship (FY2025 joint-credit volume ~€19.3bn). The friction is nonetheless real and surfaced publicly in 2024–2025, when the BVR openly questioned the apex institution's role in sector "Schieflagen" (e.g. BayWa) on the very day of DZ BANK's results conference.

#### I.4 Governance Architecture (German two-tier model)

**Vorstand (Management Board) — eight members; portfolios as of / effective 1 July 2026 (CONFIRMED, DZ BANK official board page):**

1. **Dr Cornelius Riese — Chief Executive Officer.** Strategy & Group Development (incl. sustainability) – Group; GenoBanks/Verbund; Communications & Marketing; Group Audit; Legal. Chairs the supervisory boards of BSH, R+V, TeamBank and Union Investment. In the Vorstand since March 2013; co-CEO from January 2019; **sole CEO since 1 July 2024**. Background: Accenture strategy consulting, doctorate ("Industrialisierung von Banken"), DG HYP restructuring, then DZ BANK from 2009 (strategy/participations/finance).
2. **Souâd Benkredda — Deputy CEO (from 1 July 2026).** Capital markets (institutional and retail, trading); Group Treasury; Structured Finance; foreign branches/representative offices. On the board since 2022; prior career at Deutsche Bank and Standard Chartered.
3. **Michael Speth — Deputy CEO (from 1 July 2026) / Chief Risk Officer.** Credit; Group Risk Controlling; Group Risk Control & Services.
4. **Stefan Beismann.** Corporate Banking; development/investment-promotion lending. (Succeeded Uwe Berghaus.)
5. **Dr Christian Brauckmann.** IT and Organisation (CIO).
6. **Ulrike Brouzi.** Group Finance (CFO); Bank Finance; Group Financial Services; Compliance; Client Lifecycle Management.
7. **Dr Imke Jacob.** Transaction Banking (Transaction Management, Operations & Custody, Payments & Accounts). Joined from McKinsey (New York partner). (Succeeded Thomas Ullrich.)
8. **Johannes Koch.** Group HR (Arbeitsdirektor) and Strategy for the Central Institution & Corporate Bank; Research & Economics. Chairs the supervisory boards of DZ HYP, DZ PRIVATBANK and VR Smart Finanz. Prior: KfW, Boston Consulting Group.

**The co-CEO history.** From January 2019 DZ BANK ran a Doppelspitze: **Uwe Fröhlich** (former BVR President and Berliner Volksbank board member, responsible for the Verbund- und Geschäftsbank) and **Cornelius Riese** (holding activities). This bound the ex-WGZ/BVR political constituency into management after the 2016 merger. Fröhlich retired on 30 June 2024; Riese became sole CEO on 1 July 2024. The June-2026 appointment of *two* deputy CEOs (Benkredda and Speth) rebalances a now single-headed board without reopening the political Doppelspitze.

**Aufsichtsrat (Supervisory Board).** Chaired by **Henning Deneke-Jöhrens** (board chairman of Volksbank Hildesheim-Lehrte-Pattensen; a northern-German representative; elected chair 30 May 2018, succeeding Helmut Gottschalk who reached the statutory age limit). The board is dominated by serving cooperative-bank management-board chairs (e.g. Timm Häberle, VR-Bank Ludwigsburg; Dr Peter Hanker, Volksbank Mittelhessen; Josef Hodrus, Volksbank Allgäu-Oberschwaben; Sascha Monschauer, VR Bank RheinAhrEifel; Elke Müller-Jordan, Heidenheimer Volksbank), plus **BVR President Marija Kolak**, alongside employee representatives (from DZ BANK, BSH and R+V, and a ver.di official). **Co-determination regime:** given group headcount far above 2,000, DZ BANK falls under the **Mitbestimmungsgesetz 1976** (quasi-parity codetermination), so roughly half the seats are employee representatives, with the chair (a shareholder representative) holding a casting vote.

**Decision-rights map (Control lens).**
- *Capital allocation / risk appetite:* Vorstand proposes, Aufsichtsrat approves the risk-appetite framework; CRO (Speth) and CFO (Brouzi) operationalise.
- *Major investment / acquisitions:* Vorstand decides within thresholds; above thresholds Aufsichtsrat approval required (it can block).
- *Dividends to member banks:* proposed by Vorstand, approved by AGM (dividend €448m / 25 cents per share for 2023–2025).
- *Executive appointment/removal:* sole prerogative of the Aufsichtsrat.
- *Blocking power:* the Aufsichtsrat (owner-banks + employees) can block strategy, acquisitions and appointments.

**Governance paradox (Risk lens).** The supervisory board is populated by the bank's own customers and owners. This maximises network alignment but weakens independent challenge and can import the owner-vs-competitor conflict directly into the boardroom — a structural governance weakness that no amount of committee formalism fully cures.

**Compensation.** Disclosed under the **InstitutsVergV** and CRD remuneration rules in the remuneration report; aggregate Vorstand compensation is published, but individualised variable-pay mechanics and full deferral/malus structures are only partially transparent. **UNKNOWN:** exact individual FY2025 Vorstand pay figures were not retrieved.

#### I.5 Legal Architecture (Follow-the-Legal-Entity lens)

**Verbund relationship.** The legal relationship between DZ BANK and the primary banks rests on the cooperative principles of **subsidiarity, decentralisation and regional market responsibility**, reinforced by **Verbundtreue** (network loyalty). DZ BANK's mandate ("Förderauftrag") is to strengthen the primary banks' competitiveness, not to compete with them for retail customers. There is no single controlling-shareholder agreement in the ordinary corporate sense; coordination is via the AGM, the Aufsichtsrat and BVR governance.

**Intra-group agreements.** DZ BANK AG is the holding company for the specialised institutions. **ANALYTICAL INFERENCE:** because the group holds *majority but not 100%* stakes in R+V (~96%), UMH (~93%), BSH (~96.8%), TeamBank (~92%) and DZ HYP (~98%) — with the minorities largely being primary banks — the scope for full **Beherrschungs- und Gewinnabführungsverträge** (control and profit-transfer agreements) across the whole group is constrained by minority-protection law. **VR Smart Finanz (~100%)** is the clearest candidate for a full control/profit-transfer arrangement. **UNKNOWN:** the precise register of which subsidiaries have BGAVs versus Patronatserklärungen (letters of comfort).

**Clearing / central-institution relationship.** DZ BANK is the cash-clearing, settlement and custody hub for the cooperative banks: it holds their liquidity, provides refinancing, and is their gateway to TARGET2/T2, SEPA and securities settlement. This is the legal-operational core of the "central institution" function and cannot be exited by a primary bank without leaving the network.

**Customer contracts by entity.** Each regulated activity is contracted through its own licensed entity: insurance policies with R+V entities; fund contracts with Union Investment KVGs; Bauspar contracts with BSH; consumer loans with TeamBank; corporate/capital-markets contracts with DZ BANK AG; Pfandbrief/CRE loans with DZ HYP; private-banking mandates with DZ PRIVATBANK S.A. This entity-by-entity contracting is what makes the "one champion per product, distributed by ~645 banks" model legally workable.

**Litigation / enforcement.** Material exposures surfaced through credit events rather than conduct enforcement: **R+V's investment losses on the Signa group** (called a "Fehlinvestition" by Riese) and the group's exposure to **BayWa** (Bavarian agricultural-trading group; DZ BANK and LBBW participated in a rescue package), both of which drove elevated loss allowances in 2023–2024. **UNKNOWN:** any current active regulatory enforcement action against DZ BANK AG specifically.

#### I.6 Regulatory and Supervisory Architecture — Multi-Regime Map (PRIORITY DEPTH)

**(a) Banking — ECB/SSM.** DZ BANK AG is a **Significant Institution** under the SSM, **directly supervised by the ECB**, with BaFin and Bundesbank in national/joint-supervisory-team roles. It is subject to CRR/CRD, annual SREP, Pillar 2 requirements/guidance, capital buffers and MREL.
- **O-SII / A-SRI buffer: 1.00%** of the total risk exposure amount, held in CET1. BaFin/Bundesbank set it under §10g KWG, effective from 1 January 2026 and stable across 2024–2026. BaFin's ranking places DZ BANK below Deutsche Bank (2.00%) and Commerzbank / J.P. Morgan SE (1.25%), level with KfW and Goldman Sachs Bank Europe (1.00%). **DZ BANK has been classified an O-SII by BaFin since 2016** (its own Pillar 3 report).
- **Pillar 2 Requirement (consolidated, ECB-published):** **1.88% (2024), 1.93% (2025), 1.80% (2026)** — the 2026 reduction reflects the latest SREP cycle. No leverage-ratio P2R applies. Under Art. 104a CRD, ≥56.25% must be met in CET1 and ≥75% in Tier 1.
- **Other buffers:** the German **sectoral systemic-risk buffer** on residential-real-estate-secured domestic loans (§10e(1) KWG), set at 2% and **reduced to 1% effective 1 May 2025**; and the domestic **countercyclical buffer** of 0.75% (effective 1 February 2022).
- **Capital & MREL (DZ BANK banking group, 31 Dec 2025):** **CET1 18.4%** (2024: 15.8% — the jump partly reflects CRR III in force from 1 Jan 2025); **Tier 1 20.5%**; **total capital 23.6%**; **leverage 7.0%**; **MREL 40.8% of RWA** and 13.9% of LRE (subordinated MREL 34.1% of RWA); **LCR 156.4%; NSFR 126%**. The 40.8% is the ratio *held*, comfortably above the SRB-set requirement. **UNKNOWN:** precise current MREL *requirement* (%) — a dated third-party (Daiwa, May 2024) cited ~25.1% of RWA, to be verified against table EU KM2 in the FY2025 Pillar 3 report.
- **Resolution:** DZ BANK falls under the SRB/SRMR; it participates annually in preparing the group resolution plan under §40 SAG.

**(b) Insurance — Solvency II.** R+V is supervised by BaFin under Solvency II with its own SCR/MCR, ORSA and group supervision. **SCR ratio 168% at end-2024** (excluding transitional provisions), confirmed by S&P (5 June 2025). R+V is **not** in the CRR prudential scope of the banking group; it enters supervision at the conglomerate level. **Because R+V's rating "automatically follows the network rating," the insurer's A+ (S&P) financial-strength rating is a function of the cooperative network, not standalone underwriting — a direct consequence of the IPS.**

**(c) Asset management — KAGB.** Union Investment's management companies are **Kapitalverwaltungsgesellschaften** under the KAGB, running UCITS funds (UCITS Directive) and AIFs (AIFMD), supervised by BaFin. Luxembourg fund vehicles add CSSF touchpoints via Attrax/Union Investment Luxembourg.

**(d) Building society — Bausparkassengesetz.** Bausparkasse Schwäbisch Hall operates under the **BSpKG** and is supervised by BaFin; its business is legally restricted to Bauspar and related home-finance activities. CET1 ratio 25.4% (2024) — very high, reflecting the low-risk collateralised model.

**(e) Luxembourg — CSSF.** DZ PRIVATBANK S.A. is a Luxembourg credit institution supervised by the **CSSF** (and, as part of a Significant Group, indirectly within the SSM); the Swiss unit is under FINMA.

**(f) Financial conglomerate — FKAG / FiCoD.** BaFin has **classified the DZ BANK Group as a financial conglomerate** under §1(20)/§1(2) FKAG (the German transposition of Directive 2002/87/EC, FiCoD I). DZ BANK publishes an annual FKAG report under §25(3)/(4) FKAG. The conglomerate comprises principally the **DZ BANK Institutsgruppe** (banking) and the **R+V Versicherungsgruppe** (insurance). Supplementary supervision covers **conglomerate solvency** (a Bedeckungssatz computed under Delegated Regulation (EU) 342/2014 in conjunction with Art. 49(1) CRR), **risk concentrations**, **intra-group transactions** and **conglomerate-wide risk management** (drawing on §25a KWG/MaRisk BA for the bank, §26/§27 VAG for the insurer, and §28 KAGB/MaRisk for the funds). **This is the mechanism that captures the banking-plus-insurance combination that the CRR banking scope alone omits** — and it is the reason the group carries a heavier, more fragmented supervisory load than a pure bank of similar size.

**(g) The institutional protection scheme (IPS) — dedicated treatment.** The BVR runs a **dual** protection architecture, jointly the "backbone of the FinanzGruppe's risk management" and monitored by BaFin:
- **BVR-SE (Sicherungseinrichtung):** the older scheme (since 1934), comprising a **Garantiefonds** (guarantee fund) and a **Garantieverbund** (guarantee network). It is an *institution* protection scheme — it protects the member institution *as a whole* (all its liabilities, unlimited in size), not just deposits, by **preventive intervention**: recapitalising, restructuring or merging a troubled member *before* it fails. It is privately financed, with no state support, and **no member has failed since 1934**.
- **BVR Institutssicherung GmbH (BVR-ISG):** since **1 July 2015** the statutory deposit-guarantee scheme recognised under the Einlagensicherungsgesetz (EinSiG §43), and simultaneously an **IPS within the meaning of Article 113(7) CRR**. If BaFin declares a compensation event (§10 EinSiG), BVR-ISG compensates depositors up to **€100,000 per person per institution** (§§5–16 EinSiG). BVR is its sole shareholder.
- **Mechanics & funding (Flow lens).** Members sign a **Beitritts- und Verpflichtungserklärung** binding them to all obligations under the EinSiG and Art. 113(7) CRR. The schemes are funded by member contributions (ex-ante funds plus mutualised, callable commitments). Membership enables a **0% risk weight on intra-scheme exposures under Art. 113(7) CRR**, and the FinanzGruppe reports consolidated regulatory capital using the **extended aggregated calculation under Art. 49(3) in conjunction with Art. 113(7) CRR**. Recognition rests on ongoing BaFin approval.
- **What it means for DZ BANK (Economics / Risk lens).** The IPS is the reason DZ BANK's exposures to primary banks (and vice versa) can be zero-weighted — materially lowering sector-wide RWAs and freeing capital. It is the primary driver of the AA-band external ratings (agencies rate the *network*), which in turn set R+V's and the subsidiaries' ratings. It converts ~645 legally independent banks into a single de facto risk community. **Without it:** each institution would be rated and capitalised standalone; intra-network exposures would attract positive risk weights (a large capital hit sector-wide); funding costs would rise; and the decentralised model would be materially more fragile. The IPS is, in effect, the price of admission for a decentralised cooperative sector to enjoy the ratings and capital efficiency of a single large bank.

**(h) Other regimes.** **DORA** (Digital Operational Resilience Act) applies to DZ BANK and its regulated subsidiaries and governs ICT third-party arrangements — critically the Atruvia relationship, which deepens from 2027. **AML/CFT** under the GwG, BaFin-supervised. **MiFID II** governs the capital-markets/investment-services business. **MREL/TLAC:** DZ BANK is **not** a G-SII, so it faces SRB-set MREL rather than the TLAC minimum reserved for G-SIIs.

**Regulatory matrix (summary):**

| Regime | Lead authority | Perimeter | Key requirement |
|---|---|---|---|
| CRR/CRD banking | ECB/SSM (+ BaFin/Bundesbank) | DZ BANK Institutsgruppe | CET1, P2R 1.80% (2026), O-SII 1.00%, MREL |
| Solvency II | BaFin | R+V group | SCR/MCR, ORSA (SCR 168%) |
| KAGB / UCITS / AIFMD | BaFin | Union Investment KVGs | Fund/manager rules |
| Bausparkassengesetz | BaFin | BSH | Restricted Bauspar activity |
| CSSF | CSSF (Luxembourg) | DZ PRIVATBANK S.A. | Lux banking rules |
| FKAG / FiCoD | BaFin | DZ BANK conglomerate | Conglomerate solvency, concentrations, intra-group |
| SRMR/SAG resolution | SRB | Group | Resolution plan, MREL |
| DGS/IPS | BaFin (BVR-SE/ISG) | FinanzGruppe | Deposit + institution protection |
| DORA / GwG / MiFID II | BaFin/ESMA | Group | Resilience, AML, conduct |

#### I.7 Own Capability vs Partner Dependency

| Capability | Model | Provider | Notes |
|---|---|---|---|
| Core banking IT (primary banks) | Sector partner | **Atruvia AG** | Serves the ~645 primary banks. **DZ BANK holds only ~0.35% of Atruvia directly — NOT ~20% (that figure is Verimi).** |
| DZ BANK's own IT | Mix (own + partners) | DZ BANK IT/Organisation (Brauckmann) | **ANALYTICAL INFERENCE:** DZ BANK runs its own core systems distinct from Atruvia's primary-bank platform; Atruvia is not DZ BANK's core-banking provider. |
| Payments/clearing | Own | DZ BANK Transaction Banking | Central clearer; TARGET2/T2 and SEPA gateway; ~9bn payment transactions/yr. |
| Card issuing-processing | Sector partner (from 2027) | VR Payment → **Atruvia** (1 Jan 2027) | Debit + credit processing consolidated at Atruvia. |
| Card acquiring/merchant | Own | VR Payment | Refocused post-2027; took a stake in Wallee. |
| Securities settlement/custody | Own | DZ BANK | Custodian for the network and institutions (AuD ~€97.4bn). |
| Asset-management operations | Own | Union Investment (+ Attrax, Luxembourg) | |
| Insurance underwriting/claims | Own | R+V (incl. R+V Re) | Active reinsurance in-house. |
| Treasury/funding | Own | DZ BANK Group Treasury | Central group funding; Pfandbrief via DZ HYP. |
| Ratings | Bought | S&P, Moody's, Fitch | Network rating drives subsidiary ratings. |

#### I.8 Regulation and Structure as Competitive Position

- **Central-institution mandate:** effectively **exclusive** — since 2016 there is a single cooperative central institution, a structural monopoly within the sector. Barrier to entry: near-absolute (a competitor cannot conjure ~645 owner-banks).
- **IPS as funding/ratings asset:** a **genuine moat** — AA-band ratings, low funding costs, 0% intra-network risk weights, and depositor confidence that has prevented any visible failure since 1934.
- **Conglomerate structure:** **diversification** (insurance + asset management smoothed the bank's weaker FY2025 net interest income, contributing ~78% of pre-tax profit) but at the **cost** of FKAG supplementary supervision and organisational complexity.
- **Owner-competitor tension:** a **strategic constraint** on how aggressively DZ BANK can pursue corporate clients — a self-imposed ceiling on the corporate bank's growth.
- **Caveat (do not over-score the moat):** captive ownership is not automatically a good outcome. It can dull cost discipline, entrench legacy brands, and slow decisions. The fifteen-year DZ/WGZ duplication, the DVB misadventure, and the persistent losses at TeamBank and VR Smart Finanz show that a protected structure can also shelter underperformance. The moat protects the *system*; it does not guarantee *efficiency*.

#### I.9 Institutional Dependency Map

| Dependency | Criticality | Function | Substitutability | Bargaining power / switching | Failure impact |
|---|---|---|---|---|---|
| Primary cooperative banks (~645) | **Critical** | Owners, funders, distributors, customers | None | They control DZ BANK | Existential |
| BVR & the IPS | **Critical** | Protection, ratings, coordination | None | Mutual | Loss of AA ratings + RWA shock |
| ECB / BaFin / Bundesbank / SRB | **Critical** | Authorisation, capital, resolution | None | One-directional | Licence/operational |
| TARGET2/T2 & Eurosystem | **Critical** | Settlement/liquidity | None | One-directional | Payment gridlock |
| Atruvia | **High** | IT for primary banks; card issuing-processing from 2027 | Very low | Captive sector partner | Sector operational outage |
| Rating agencies | High | Funding access | Low | Moderate | Funding-cost spike |
| Wholesale funding markets | High | Group/DZ HYP funding | Moderate | Market-driven | Liquidity stress |
| EBA CLEARING / SEPA | High | Retail payments | Low | Collective | Payment disruption |
| Reinsurers (for R+V) | Moderate | Risk transfer | Moderate | Market-driven | Earnings volatility |
| Deutsche Kreditwirtschaft / schemes | Moderate | Standards/governance | Low | Collective | Strategic drift |

**Single points of institutional failure:** the **IPS** and **Atruvia**. **Converse — DZ BANK's own systemic importance:** as an O-SII and the settlement/liquidity/custody hub for ~645 banks and ~30m customers, **DZ BANK is itself the single point of failure for the German cooperative sector** and is nationally systemically important — which is precisely why the ECB supervises it directly and why the IPS exists to make its failure unthinkable.

#### I.10 Tax and Intercompany Architecture

**Evidence-limited.** Material entities are German tax-resident except **DZ PRIVATBANK S.A.** (Luxembourg) and the Swiss booking centre. **VR Smart Finanz (~100%)** is the most plausible Organschaft/profit-transfer entity; the majority-but-not-wholly-owned subsidiaries (R+V, UMH, BSH, TeamBank, DZ HYP) limit full tax-grouping because of minority (primary-bank) shareholders. Group income taxes were **€1,402m on €4,282m pre-tax profit in FY2025** (effective rate ~32.7%), consistent with German corporate income tax + solidarity surcharge + trade tax and the partial non-deductibility of certain insurance items — i.e. a *high*, not optimised, effective rate. **ANALYTICAL INFERENCE:** the Luxembourg/Swiss entities exist for fund-services and private-banking *market access*, not tax arbitrage — DZ PRIVATBANK's economic rationale (Luxembourg is Europe's fund-administration hub) precedes any tax consideration. **UNKNOWN:** intercompany service/cost-allocation terms; deferred-tax and uncertain-tax-position detail.

#### I.11 Corporate and Regulatory Risk Register

| Risk | Prob. | Severity | Mitigation | Responsible entity | Residual |
|---|---|---|---|---|---|
| Capital/MREL shortfall | Low | High | 40.8% RWA MREL held; CET1 18.4% | Group Treasury / CFO | Low |
| SREP/P2R escalation | Low-Med | Med | Strong CET1 headroom; P2R fell to 1.80% (2026) | CFO/CRO | Low |
| Conglomerate supervision burden | High (ongoing) | Low-Med | FKAG reporting apparatus | Compliance | Med |
| IPS mutualisation (bear other members' losses) | Med | Med-High | Ex-ante funds; preventive intervention; risk monitoring | BVR-SE / BVR-ISG | Med |
| German CRE concentration (DZ HYP) | Med | High | Pfandbrief cover pools; conservative LTVs | DZ HYP | Med-High |
| R+V investment portfolio / Solvency II sensitivity | Med | High | Diversification; SCR 168%; Signa written down | R+V | Med |
| Interest-rate risk in banking book | Med | Med | ALM/hedging; NII decline already absorbed | Group Treasury | Med |
| Credit concentration (BayWa/Signa-type single names) | Med | Med-High | Loss allowances €653m FY2025; single-name limits | CRO | Med |
| Owner-competitor conflict escalates | Med | Med | Subsidiarity; joint/consortium credit | CEO/Verbund board | Med |
| Member-bank consolidation shrinks owner base | High (structural) | Med | Scale efficiencies; 23 mergers in 2025 alone | BVR/CEO | Med |
| Cyber/operational (DORA) incl. Atruvia concentration | Med | High | DORA programme; resilience testing; step-in rights | CIO | Med-High |
| AML/sanctions enforcement | Low-Med | Med-High | Compliance function; MaRisk | CFO/Compliance | Med |
| Ratings downgrade | Low | High | IPS/network rating anchor | Group Treasury | Low |
| Reputational contagion across the Verbund brand | Med | High | IPS prevents visible failures; shared brand governance | BVR | Med |

#### I.12 Volume I Reconstruction — Synthesis and the Framing Questions

**The twelve reconstructions (1)–(11)** are delivered in the sections above: Corporate Entity Diagram and Simplified Group Structure (I.2); Ownership and Control (I.3); Governance and Decision-Rights Map (I.4); Multi-Regime Regulatory Map and IPS Diagram (I.6); Legal Responsibility Map (I.5); Own-vs-Partner Capability Matrix (I.7); Institutional Dependency Map (I.9); Tax/Intercompany Map (I.10); Chronological Corporate Evolution (I.1); and Structure-as-Competitive-Position (I.8) and the Risk Register (I.11).

**(15) Ten most important conclusions.**
1. The network owns the bank, not the reverse — 94.8% cooperative ownership means control flows *up* from ~645 primary banks.
2. DZ BANK is economically a bancassurance holding: R+V and Union Investment generated ~78% of FY2025 pre-tax profit; the bank itself is a minority contributor.
3. The IPS (Art. 113(7) CRR) is the structural keystone — it delivers 0% intra-network risk weights, AA-band ratings, and a 90-year zero-failure record.
4. Four perimeters (AG / Group / FinanzGruppe / prudential Institutsgruppe) must be kept distinct; secondary sources routinely splice them.
5. DZ BANK carries an unusually heavy supervisory load: five sector regimes *plus* FKAG conglomerate supervision — a real cost of the diversified model.
6. The single-central-institution mandate (post-2016) is a structural monopoly and near-absolute barrier to entry within the sector.
7. Capital is strong and strengthening (CET1 18.4%, up from 15.8%, partly via CRR III), and the 2026 P2R fell to 1.80% — the regulator is comfortable.
8. The owner-competitor conflict is permanent and only *managed*, not resolved — via subsidiarity and consortium credit.
9. The structure shelters underperformers (TeamBank, VR Smart Finanz loss-making; DVB a past failure) — the moat protects the system, not efficiency.
10. Atruvia's role rises sharply from 1 Jan 2027 (card issuing-processing), concentrating operational risk in the sector's IT utility — a new critical dependency.

**Direct answers to the framing questions.**
- **Most strategically important legal entity:** **DZ BANK AG itself** — the exclusive central institution, group holding company, clearer, custodian and funding hub. R+V and Union Investment are the biggest *earners*, but only the AG is *load-bearing* for the network's plumbing.
- **Where actual control sits:** with the ~645 primary cooperative banks collectively, exercised through the AGM and an Aufsichtsrat of owner-bank CEOs, coordinated by the BVR — not with Frankfurt management.
- **Greatest regulatory constraint:** ECB/SSM banking supervision (SREP, P2R, buffers, MREL) layered with **FKAG conglomerate supervision** — the dual banking-plus-insurance perimeter creates the heaviest compliance burden of any EREF subject to date.
- **What the IPS does / life without it:** it mutualises solvency and liquidity so no member fails, delivering 0% intra-network risk weights and AA ratings. Without it, the sector fragments into standalone-rated, standalone-capitalised banks with higher funding costs and far greater fragility — the decentralised model would likely not survive in its current form.
- **Greatest external dependency:** the **Eurosystem/ECB nexus** (direct supervision + TARGET2/T2 settlement + monetary operations). Among sector partners, **Atruvia** rises to near-critical from 2027.
- **Managing owner-vs-competitor conflict:** via the subsidiarity principle, joint/consortium credit that preserves the primary bank's client relationship, and board governance — imperfectly, with periodic public friction (BVR vs DZ BANK over sector Schieflagen).
- **Most misunderstood by outsiders:** the **perimeter confusion** (AG vs Group vs FinanzGruppe) and the myth that DZ BANK "owns" the network — in fact the network owns DZ BANK; plus the false ~20% Atruvia stake (actually ~0.35%; the ~20% is Verimi).
- **What would take longest to rebuild from zero:** the **IPS's ~90-year track record of zero failures** and the trust and ratings it confers. Capital can be raised in months; a credible, tested, unlimited mutual-protection reputation cannot be manufactured — it is the product of nine decades of not failing.

**(14) Key unknowns.** Precise current MREL requirement (%); individual FY2025 Vorstand remuneration; the register of BGAVs/Patronatserklärungen across subsidiaries; intercompany service-pricing and cost-allocation terms; detailed deferred-tax and uncertain-tax-position figures; any active conduct-enforcement actions.

### Recommendations
1. **For an analyst/counterparty:** anchor the credit view on the **network rating and IPS**, not DZ BANK AG's standalone metrics. Monitor BVR-SE/ISG fund adequacy and, above all, any move to change **Article 113(7) CRR** treatment — an EU CMDI (crisis-management/deposit-insurance) reform that removed or diluted IPS privileges would be the single most material negative catalyst for the whole sector. **Threshold:** any EBA/Commission proposal to restrict IPS risk-weighting or force IPS members to co-fund a central EU deposit scheme should trigger a full re-underwrite.
2. **For a competitor:** do not attempt to contest the central-institution mandate directly (structurally impossible). Compete at the **product-factory level** — asset management, consumer credit, payments — where TeamBank (−€29m, losing share to 3.9%) and VR Smart Finanz (−€28m) are visibly under pressure. **Benchmark:** a second consecutive year of TeamBank/VR Smart Finanz losses is the clearest sign of a contestable flank.
3. **For the group itself:** the FY2027 Atruvia card migration concentrates operational risk — DORA-grade resilience, exit and step-in rights should be stress-tested before go-live. As the owner count falls (23 mergers in 2025 alone, to 645 banks), governance weight should shift from constituency politics toward efficiency and independent challenge on the Aufsichtsrat.
4. **Escalation trigger to watch:** a repeat of BayWa/Signa-scale credit events *concurrent* with an R+V investment drawdown would test the P&L and the FKAG conglomerate solvency cover simultaneously — the scenario most likely to force an IPS intervention and the one that would most quickly move the network rating.

### Caveats
- **Perimeter:** figures are labelled AG / Group / FinanzGruppe / banking-group; do not splice. The €1.175trn figure is the **FinanzGruppe**, not DZ BANK. R+V sits outside the CRR banking-group scope and is captured only at conglomerate level.
- **Ownership percentages** in subsidiaries are "rounded" per DZ BANK's own presentation and vary slightly between sources (e.g. BSH cited as both 96.8% and 97.6%; the investors' presentation shows 98%/92%/93%/97%/96%/93%/100% for the subsidiary block); treated as approximate.
- **Bank count:** ~645 institutions as of end-November 2025 (23 mergers recorded in 2025, per consultancy zeb) — DZ BANK's own materials still round to "~700" or occasionally "~800," reflecting different dates; the owner base is shrinking structurally.
- **UNKNOWNs flagged** in I.12 are genuine evidence gaps, labelled rather than estimated.
- **Forward-looking / pending items** — FY2026 group PBT guidance of ~€3bn; the card transfer completing 1 January 2027 subject to Bundeskartellamt clearance (case B9-75/26); R+V's €25bn premium / €1.5bn profit 2030 targets — are **company statements or pending approvals, not accomplished facts**.
- Some scale figures (VR Payment headcount, DZ PRIVATBANK AuM/AuC) derive from company/secondary profiles and may lag the latest year-end.

*End of Volume I. Volume II (business model, product economics, flows and competitive dynamics) not begun, per instruction. Work paused at the natural boundary between institutional anatomy and operating economics.*


---

# Part II — Product, Customer, Distribution & Flow Architecture

### TL;DR
- The DZ BANK Group is best understood not as a bank but as a **captive-but-contestable bancassurance and asset-management manufacturing house** whose value lies overwhelmingly in its subsidiaries: in FY2025 R+V (€2,144m pre-tax) and Union Investment (€1,185m) alone produced ~78% of group pre-tax profit of €4,282m (2024: €3,303m), while the parent bank's own franchise (Central Institution & Corporate Bank, €864m) is secondary. The group manufactures products centrally and distributes them through ~645 legally independent cooperative banks (672 at year-end 2024) it does not control but which collectively own it (94.8%).
- **Distribution is contractually optional, not captive.** Primary banks are free to — and demonstrably do — sell third-party products (documented: Volksbank Mittelhessen brokers Allianz Leben and Generali/Proxalto Leben alongside R+V). The group's dominance rests on Verbundtreue, economic alignment, deep technical embedding in Atruvia's digital rails and habit — not on legal exclusivity. This makes the primary banks the group's customers, distributors, owners and governors simultaneously — a four-role identity that structurally caps how hard the group can push.
- The single most important commercial fact is that **value accrues at the point of customer ownership — the primary banks — not at the manufacturer.** The primary banks earned €6.5bn total net commission income in 2024 (of which payments generates ~€3bn, ≈40%); DZ BANK Group's own net fee and commission income was €3,370m in FY2025. The group is simultaneously a net contributor (commissions + dividends flowing down) and a value-retainer (compounding stock margins kept centrally), and on balance functions as a manufacturing utility for its owners rather than a profit-maximiser against them.

### Key Findings

1. **The two Volume I discrepancies are resolved.** (a) DZ BANK holds **72.37% of Union Asset Management Holding AG** as of 31 December 2025 (CONFIRMED, Union Investment corporate site/Wikipedia: "The primary shareholders in Union Investment are DZ Bank with 72.37%… Other shareholders include BBBank and the credit unions through their membership associations"). The older "54.44% DZ BANK + 17.72% WGZ BANK" figure is the pre-2016 structure; the WGZ stake was absorbed when WGZ BANK merged into DZ BANK in 2016, leaving BBBank and the regional cooperative associations holding the residual ~27.6%. (b) **Münchener Hypothekenbank eG is genuinely outside the DZ BANK Group** — an independent registered cooperative (eG) owned by other cooperative banks and ~60,000 cooperative members, an ECB-supervised Significant Institution, and Germany's 2nd-largest mortgage bank (32.2% of the mortgage-bank segment, 2024). The BVR consolidated accounts explicitly treat it as a "rechtlich selbstständiges, gleichgeordnetes Mutterunternehmen" **alongside** the DZ BANK Konzern, NOT as a DZ BANK subsidiary. It is therefore an in-sector competitor to DZ HYP and BSH for the same home-financing customer — a standing exception that contradicts a strict "one champion per product" reading.

2. **The product universe decomposes into nine principal manufacturers plus specialist units** (full map in Details), for almost all of which the primary bank contracts as intermediary, the group subsidiary manufactures and books the asset/liability, and the commission flows back to the primary bank.

3. **The three-tier customer structure is the defining architecture** and differs fundamentally from a normal bank: in tier one, owners = customers = distributors = governors.

4. **Distribution economics: the manufacturer captures the recurring margin; the distributor captures the commission and owns the relationship and the data.** The clearest published proxy — BVR's "Provisionserträge aus dem Verbundgeschäft" — was €2.8bn in 2021 (+15.6%); this specific line was discontinued in the BVR online Jahresberichte after 2021, but the aggregate primary-bank Provisionsüberschuss was €6.5bn in both 2023 and 2024 (BVR Jahresbericht 2024: "Der Provisionsüberschuss erreichte 2024 insgesamt 6,5 Milliarden Euro beziehungsweise 0,55 Prozent der DBS. Er stieg damit um 3,9 Prozent … der größte Anteil … im Zahlungsverkehr generiert, gefolgt vom Vermittlungs- und Wertpapiergeschäft").

5. **Money movement: DZ BANK is the sector's clearing house**, processing ~9.9bn transactions/year (up from ~7.5bn in 2018), now consolidated onto a single insourced payments platform (migrated 2024), acting as gateway to T2/TARGET2, the SEPA Clearer/EMZ, SCT Inst and the card schemes. Payments has become a genuine profit centre.

6. **The card business is being restructured**: VR Payment's Issuing-Processing division transfers to Atruvia effective 1 January 2027 (Bundeskartellamt case B9-75/26, notified 15 July 2026). Per Atruvia (2 July 2026), Atruvia will assume "neben dem Issuing Processing für Debit auch das Kredit-Processing, das bisher bei der DZ BANK Tochter VR Payment lag," building one integrated platform spanning girocard, debit and credit; VR Payment refocuses on acquiring, POS network operation and merchant business.

7. **Failure paths are real and recent.** BayWa: per Handelsblatt (25 Feb 2025), quoting CEO Cornelius Riese, DZ BANK's loss provisions "mehr als verfünffachte auf 456 Millionen Euro," a "Großteil" BayWa-related. Signa: per CEO Norbert Rollinger (Bilanzpressekonferenz, 3 April 2024), the engagement was "in unserem Jahresabschluss 2023 komplett verarbeitet," a "robuster dreistelliger Millionenbetrag," yet R+V still posted a ~€1bn IFRS result in 2023 on a +€3.5bn investment result. Both show the group and sector bear real losses and that the shared brand transmits reputational damage into the advisory conversation.

### Details

#### II.1 Product Universe — by Manufacturing Entity

The follow-the-legal-entity rule is decisive: for almost every retail product, the **primary bank contracts as intermediary/agent, the group subsidiary is the manufacturer and books the asset/liability and bears the product risk, and the commission flows back to the primary bank**, which keeps the relationship and the data.

**DZ BANK AG — Central Institution & Corporate Bank (CICB) — FY2025 segment €864m pre-tax.** Products: (1) corporate/Mittelstand lending; (2) joint/consortium credit ("Metakredit", ~€19.3bn FY2025) where the primary bank keeps the relationship and DZ BANK supplies balance-sheet capacity; (3) structured, project and export finance; (4) intermediation of KfW and Landesförderinstitut promotional loans; (5) capital markets — DZ BANK is **Germany's market leader in structured retail products (Zertifikate)**, especially Zinsanleihen, ahead of LBBW and DekaBank (Handelsblatt); (6) institutional sales, research, FX, rates, derivatives, CLN/securitisation; (7) Treasury; (8) transaction banking (payments, accounts, cash management, trade finance); (9) depositary/custody (custody assets ~€97.4bn, growing via acquisitions); (10) Verbund-specific services to primary banks (liquidity, refinancing, product supply, risk-taking capacity). Classification: mixed direct/external (capital markets, corporates) and Verbund-exclusive (central-bank services).

**R+V Versicherung — FY2025 segment €2,144m pre-tax (the single largest profit contributor).** Gross written premiums rose to €22.8bn (2024: €20.9bn). Lines: life/pension, health (first time over €1bn), property/casualty, motor, agricultural and credit insurance, occupational pensions, active reinsurance (R+V Re), and the Italian subsidiary Assimoco (which grew strongly). The Volks- und Raiffeisenbanken are the "Hauptvertriebsweg," with R+V field staff (Außendienst) embedded in "mehr als 7.500 Bankstellen"; secondary channels are R+V's own Generalagenturen/Hauptvertretungen, brokers, the Straßenverkehrsgenossenschaften, and (since integrating R+V24 in July 2022) direct. R+V's disclosure that bank-to-insurer referrals ("Überleitungen") fell from up to ~320,000 to under 200,000/year as branch visits declined quantifies the erosion of the traditional handoff — a strategic concern that prompted the "NextLevel" digitalisation programme. Classification: dual-channel, Verbund-led.

**Union Investment (UMH) — FY2025 segment €1,185m pre-tax; AuM €534.7bn year-end 2025.** Retail net inflows €13.5bn (2nd-best year ever, 2024: €12.6bn); institutional net inflows €9.8bn (more than double 2024's €4.7bn); institutional assets €263.8bn; retail assets €270.8bn — a roughly **51/49 retail/institutional split**. Classic fund savings plans passed 4 million (6.55m including Riester/VL). Products: UniFonds retail family, institutional Spezialfonds and mandates, Union Investment Real Estate, Article 8/9 sustainability products, UniProfiRente (Riester), plus Quoniam (quant, ~$22bn) and Attrax. Retail distribution runs through the primary banks and BSH's field force; institutional is won in open competition. Classification: dual (retail Verbund-led; institutional externally competitive).

**Bausparkasse Schwäbisch Hall — FY2025 segment €122m pre-tax (doubled from €64m in 2024).** ~7m customers/contracts (>€328bn Bausparsumme in stock); Bauspar market share 33.3% (unchallenged leader). New Bauspar business normalised to €17.6bn (2024: €28.1bn) after the post-rate-shock surge, but jointly-originated Baufinanzierung new business rose 16% to €15.8bn. Owned 97.6% by DZ BANK, ~2.4% by primary banks; ~6,700–6,800 inside/field staff, whose field force **also distributes Union Investment funds**. Additional units: Schwäbisch Hall Wohnen (subsidiary digital advisory channel), the Baufinex B2B marketplace (JV with Hypoport; >8,000 unbound intermediaries, >560 product partners, transaction volume +~40% to €8.3bn). Classification: Verbund-exclusive core (Bauspar) plus platform extensions.

**DZ HYP — FY2025 segment €338m pre-tax (down from €479m in 2024 on IFRS own-issuance valuation effects; operating business positive).** Corporate (commercial real estate) new business rose to €9.2bn (2024: €7.2bn); retail new business €1.6bn; total financing portfolio stable at ~€57.6bn; risk provisioning an unremarkable €105m. **Germany's largest Pfandbrief issuer** (multiple €1bn benchmarks placed in 2025). Retail residential lending is intermediated by primary banks via the VR-BaufiComfort cooperation model (bank advises; DZ HYP does full credit processing); DZ HYP paid €45.7m (2023: €32.2m) in Vermittlungsleistungen to primary banks in 2024. The group's "subsidiäre Betreuung" of the primary banks is the central element of DZ HYP's model. Classification: dual (direct CRE/public-sector; intermediated retail).

**DZ PRIVATBANK — FY2025 segment €106m pre-tax (2024: €112m; dip from lower rates).** Private-banking AuM rose to €30.7bn (2024: €26.1bn), >60% in pure discretionary mandates; AuC ~€181.3bn. Model: HNW clients referred by primary banks under a joint-sales cooperation ("Verbundvertrieb statt teurem Standalone-Private-Banking"); the BVR anchored Private Banking as a distinct group business field, seeing "erhebliches Ertragspotenzial." Also: Luxembourg fund services/depositary and foreign-currency lending. Note the Asset Servicing headwind — Flossbach von Storch (>€50bn) departed as a custody client, hitting the FY2025 comparison. Zuwendungsfreie Provisionen paid to primary banks exceeded €130m (up >50% since 2019). Classification: dual (Verbund-referred private banking; third-party Lux fund services).

**TeamBank (easyCredit) — FY2025 segment −€29m pre-tax (a loss).** ~1.067m customers (2024: 1.071m); loan book €9,132m (−3.7%); German market share 3.9% (second consecutive slight decline); Austrian ("der faire Credit") 12.3%. Products: easyCredit and "der faire Credit" instalment loans, plus easyCredit-Ratenkauf/-Rechnung embedded/POS finance (financing €200–10,000; from July 2025 also invoice), with a uniform Ratenkauf rate of 12.99% eff. p.a. regardless of term or credit score; >2,500 cooperative corporate/multichannel merchant partners; 94% of partner banks connected. TeamBank takes the default risk on Ratenkauf. Classification: dual (Verbund consumer lending + externally competitive embedded finance).

**VR Smart Finanz — FY2025 segment −€28m pre-tax (a loss; company-reported EGT −€28.3m, prior year −€23.4m).** Total new business €1.18bn (−4.5%); object finance (leasing/hire-purchase) €547m (−10%); Unternehmerkredit (VR Smart flexibel express loan + VR Smart basis) €636m (+1%); portfolio €3.12bn; ~113,000 customers; cost/income 78.6%. Positioned as "subsidiärer Partner für einfachste Mittelstandslösungen," sold via the cooperative online platforms. Classification: Verbund-exclusive SME finance.

**VR Payment — ~248 employees.** Merchant acquiring, POS network operation, omnichannel/e-commerce payment, and card issuing-processing (until 31 December 2026, then to Atruvia). Classification: Verbund infrastructure + externally competitive acquiring.

**Others:** ReiseBank (cash/FX/precious metals/international cash transfer); CardProcess; VR Equitypartner (PE/mezzanine); VR Factoring; GENO Broker (online brokerage). Classification: mostly Verbund niche.

#### II.2 The Three-Tier Customer Structure (unusual weight)

**Tier (a): the ~645 primary cooperative banks (672 at year-end 2024; ~23–25 mergers/year).** They are simultaneously **owners** (94.8%), **customers** (buying liquidity, refinancing, risk capacity, product supply, transaction infrastructure), **distributors** (selling group products to their own customers and earning commission), and **governors** (populating the Aufsichtsrat, controlling the AGM, and — via the BVR — setting sector strategy). This four-in-one identity is the central structural fact. When the manufacturer's interest (maximise product margin) conflicts with the distributor-owner's interest (maximise retained commission and protect the local relationship), governance is stacked toward the primary banks because they own and govern the manufacturer. This is precisely why the group operates under a **Förderauftrag** — a mandate to strengthen the primary banks' competitiveness — rather than a mandate to maximise its own profit against them. The spread of institutions is wide: average balance sheet ~€1.8bn but median only €0.78bn, ranging from ~€37m (smallest) to ~€52bn (largest) — so "the primary bank" is not a homogeneous counterparty.

**Tier (b): the primary banks' >30m end customers.** They buy R+V policies, UniFonds, Schwäbisch Hall Bauspar contracts, TeamBank loans and DZ HYP mortgages — largely without knowing DZ BANK exists. The manufacturer books the contract; the local bank owns the relationship and the data. This is the crux of the group's economics: it manufactures for customers it does not own and cannot see directly.

**Tier (c): direct clients of DZ BANK AG and subsidiaries** — corporates, institutional investors, other banks/insurers, third-party fund-services clients. This is the genuinely contestable, market-priced business (capital markets, Union institutional mandates, DZ HYP direct CRE, DZ PRIVATBANK Luxembourg fund services, TeamBank external embedded finance).

**Product governance (who sets requirements).** The BVR is the sector's strategic apex and holds — unusually, and more than the DSGV does on the Sparkassen side — genuine "strategische Führungskompetenz," setting sector strategy across five defined fields (Finanzmarktstabilität, Zahlungsverkehr, Wettbewerb, Nachhaltigkeit, Wohlstandssicherung). Product entry into the Verbund catalogue and cross-subsidiary arbitration run through BVR committees and Fachräte and the group's product-governance processes. The manufacturers hold the product economics, but the primary banks — through the BVR and the Aufsichtsrat — hold the ultimate go/no-go on what the network pushes. (ANALYTICAL INFERENCE where specific committee names are not individually published; the BVR's strategic-leadership role and the Fachrat structure are CONFIRMED.)

#### II.3 Customer Segmentation

**Tier (a) primary banks:** by size (large urban Volksbanken with tens of billions in assets vs small rural Raiffeisenbanken under €100m); by region (the persistent ex-DG south vs ex-WGZ north constituency); by product-adoption depth; and by whether they are net placers or net takers of liquidity with DZ BANK. Roughly one in ten also runs a Warengeschäft (commodity trading) — 49 institutions in 2024 (2023: 55) — the sub-segment most directly exposed to BayWa-type agricultural-commodity risk. **Tier (b) end customers:** retail; private banking/HNW (DZ PRIVATBANK); self-employed/Mittelstand (VR Smart Finanz, CICB); agricultural (R+V, the Warengeschäft banks); public sector (DZ HYP). **Tier (c) direct clients:** large corporates; institutional investors (Union €263.8bn institutional); other financial institutions (Zertifikate buyers, custody clients); international clients through foreign branches. Earnings-driver mapping: R+V and Union dominate group profit (~78%); CICB drives corporate/capital-markets earnings; BSH/DZ HYP the housing chain; TeamBank/VR Smart Finanz are currently loss-making.

#### II.4 Jobs to Be Done

For a **primary bank**: "give me products I cannot manufacture" (all subsidiaries); "give me liquidity/refinancing and risk-taking capacity" (CICB, Metakredit ~€19.3bn); "give me capital-markets access" (CICB); "give me payment/settlement infrastructure" (DZ BANK clearing, ~9.9bn transactions); "let me stay a full-service bank at small scale" — the meta-job the entire group exists to serve. For **end customers**: Bauspar = disciplined home-savings plus rate insurance; UniFonds savings plan = automated long-horizon wealth-building; R+V policy = risk protection; easyCredit = fair, transparent instalment liquidity. Competitive substitutes: DekaBank/LBS/Provinzial-SV (the near-identical Sparkassen manufacture-and-distribute model — the single most useful benchmark) and direct players ING, DWS, Allianz, Check24/Smava. For **direct clients**: cooperative-sector reach, Pfandbrief funding depth, strong ratings (S&P A+, Moody's Aa2, Fitch AA-) and a non-listed, stable counterparty.

#### II.5 The Distribution Model and Its Economics (priority depth)

**The manufacture-and-distribute chain (6 steps):** (1) a subsidiary manufactures the product; (2) it enters the Verbund catalogue; (3) each primary bank independently decides whether to sell it; (4) the bank's adviser sells to the end customer; (5) the contract sits with the manufacturing entity, which books the asset/liability and bears the product risk; (6) commission flows back to the primary bank, which keeps the relationship and the data.

**Is distribution exclusive or optional? — OPTIONAL. This is the single most important commercial finding of the volume.** A primary bank is NOT contractually obliged to sell only group products. Documented evidence: Volksbank Mittelhessen operates as a tied insurance agent (gebundener Versicherungsvertreter, §34d Abs. 7 Nr. 1 GewO) on the basis of R+V products, **but its own mandatory disclosure states it simultaneously brokers Allianz Lebensversicherung and Generali/Proxalto Leben** and receives commission from each. German case law (BGH, 30 January 2014, I ZR 19/13) confirms that tied agents may sell third-party products complementing the principal's range. The commercial implication is profound: the group must compete for shelf space inside its own network. Its dominance therefore rests on Verbundtreue (loyalty norms), economic alignment (the banks own the manufacturers and share the upside), deep technical embedding in Atruvia's rails, and inertia — not on captivity. Where a competing product is materially better or better-remunerated, a primary bank can and sometimes does place it. Münchener Hyp's independent existence as an in-sector mortgage alternative is the structural proof.

**The commission economics.** The clearest published measure of what the primary banks earn from distributing group products is the BVR series "Provisionserträge der Genossenschaftsbanken aus dem Verbundgeschäft," which was **€2.8bn in 2021 (+15.6%)** against off-balance-sheet customer volume of €588bn (investments €473bn, credit €115bn). CAVEAT: this specific line was not carried forward in the same wording in the BVR online Jahresberichte for 2022–2024; it may survive only in the downloadable statistical annex. The available proxy is the aggregate primary-bank Provisionsüberschuss: €6.5bn in 2023 (0.56% of average total assets, +4.3%) and €6.5bn again in 2024 (0.55%, +3.9%), with payments the largest component (~€3bn) and the Vermittlungs-/Wertpapiergeschäft (brokering Verbund products) the second. Set against DZ BANK Group's own net fee and commission income of €3,370m (FY2025), the two sides are of comparable magnitude: **the network captures roughly as much in distribution commission as the manufacturer captures in total net fees.** Value is split — the manufacturer captures the recurring management/underwriting margin (which compounds on stock: Union's €534.7bn AuM, R+V's premium base), while the distributor captures the up-front and trailing commission plus, crucially, the relationship and the data. (ANALYTICAL INFERENCE: because the ~€2.8bn Verbund figure and the €6.5bn aggregate overlap but are not on identical perimeters, they should not be summed.)

**Verbund-internal competition** is real and only partly managed: Union Investment vs R+V for the same savings euro; BSH vs DZ HYP vs the independent Münchener Hyp for the same home-financing customer; TeamBank vs the primary bank's own overdraft for consumer credit. The "one champion per product" principle mitigates but does not eliminate this, and Münchener Hyp's independence is a permanent exception.

#### II.6 Money Movement and Clearing

DZ BANK is the sector's cash-clearing, settlement and gateway institution, handling ~9.9bn transactions/year (up from ~7.5bn in 2018), now consolidated onto a single **insourced** platform (migration completed 2024, deliberately one year later than planned to absorb T2 consolidation, ISO 20022 and SEPA changes). The company contrasts its insourcing approach with Commerzbank's outsourcing. Flows kept analytically separate:

(a) **Payments/clearing** — gateway to T2/TARGET2 for large-value interbank settlement (staggered pricing, ~€0.80/transaction at low volume), the SEPA Clearer/EMZ for retail bulk (~€0.0025 per transaction in bulk files of up to 100,000), SCT Inst, and the card schemes. (b) **Liquidity** — primary banks' surplus deposits placed with, and refinancing drawn from, DZ BANK, which manages the resulting balance sheet. (c) **Securities settlement/custody** (~€97.4bn custody). (d) **Risk transfer** — Metakredit ~€19.3bn, syndication, risk participation. (e) **Commissions/revenue-share** back to primary banks. (f) **Capital and dividends** up to the owner-banks. Payments is now an explicit profit centre: ~€3bn of the primary banks' commission income (≈40% of their commission earnings) is payments-related, up from ~€1.8bn a decade earlier.

**Representative end-to-end flows.** A *SEPA credit transfer* initiated at a Volksbank routes through Atruvia's core system → DZ BANK as the bank's clearer → the SEPA Clearer/EMZ (near-zero marginal cost) → beneficiary bank; DZ BANK earns a thin per-transaction fee, the primary bank books account/payment commission, DZ BANK holds settlement risk intraday, the primary bank holds the regulatory customer relationship. A *SEPA instant payment* routes in real time via the RT1/TIPS rails with DZ BANK as gateway. A *girocard/credit-card transaction* today runs acquiring via VR Payment and issuing-processing via VR Payment (credit) / Atruvia (debit); **from 1 January 2027 all issuing-processing consolidates at Atruvia** and VR Payment retains acquiring/POS/merchant. A *corporate loan* jointly originated by a primary bank and DZ BANK (Metakredit) leaves the relationship and covenant with the primary bank while DZ BANK books its participation and shares the credit risk. A *Union fund purchase* is advised and booked by the primary bank as intermediary, the fund sits at Union, Union earns the management fee and pays the bank trailing commission. An *R+V policy sale* is written by R+V, contracted with the customer via the tied-agent bank, with R+V bearing underwriting risk and paying the bank acquisition/renewal commission.

A critical control fact: **DZ BANK holds only ~0.35% of Atruvia** (the ~20% figure sometimes cited refers to Verimi and is erroneous). The sector's primary digital rail — the VR Banking App, OnlineBanking, the BankingWorkspace and the Omnikanalplattform (live since 2019) — is controlled by Atruvia, not DZ BANK. The group manufactures the products but does not own the increasingly dominant digital channel through which they are sold, and from 2027 will not own card issuing-processing either.

#### II.7 Channel Architecture (all channels mapped)

(1) **Primary-bank branch network** (~7,000 Bankstellen) — the dominant channel; not DZ-controlled. (2) **Primary-bank digital channels on Atruvia's platform** (VR Banking App — one of the best-rated German banking apps at 4.5/4.7 stars, increasingly a sales channel via "Produktabschlussstrecken") — Atruvia-controlled. (3) **Subsidiary-direct digital** (easyCredit embedded finance, Union online, R+V direct, GENO Broker) — DZ-group-controlled. (4) **BSH's and R+V's own field forces** (R+V embedded in bank branches; BSH field force also sells Union funds). (5) **DZ BANK AG direct corporate/institutional coverage.** (6) **Foreign branches/representative offices.** (7) **Broker/intermediary channels** (Baufinex; R+V brokers). (8) **Third-party/embedded distribution outside the sector** (easyCredit-Ratenkauf merchants; Atruvia itself now serving non-cooperative clients such as Bankhaus C.L. Seeliger and ADAC). Strategic importance is shifting from (1) toward (2), which raises the Atruvia channel-control question.

#### II.8 Pricing and Revenue Architecture; net extractor or contributor?

Pricing to **tier (a)** primary banks blends cost-plus/subsidised central-bank services (liquidity, refinancing, product supply) with market-based capital-markets pricing. To **tier (b)** end customers, retail product pricing is largely set by the **manufacturer** (easyCredit's uniform 12.99% Ratenkauf rate; BSH tariffs; Union fund fees), with the distributor earning commission. To **tier (c)** direct clients, full market pricing applies. The **Förderauftrag** means DZ BANK is expected to operate for its owners' benefit rather than to maximise profit against them.

**Testing the "captive supplier's profit is a levy in disguise" hypothesis** (carried from the Atruvia finding): DZ BANK pays dividends up to the owner-banks AND pays them distribution commissions, while retaining product margins centrally. On balance the group is best read as a **net contributor / manufacturing utility at the flow level**: the €6.5bn of commission income the primary banks earn (a large share Verbund-derived) plus the dividend stream materially exceeds what a stand-alone profit-maximiser would return, and the stated mandate constrains extraction. **However, at the stock level the group is a value-retainer**: the manufacturers keep the compounding AuM/premium margins the primary banks never see. So the correct characterisation is nuanced — a contributor on annual flows, a retainer of durable franchise value. Unlike the pure-levy Atruvia case, DZ BANK's reported profit is not simply a disguised charge on the owners, because most of it is generated in genuinely external markets (insurance underwriting, capital markets, institutional asset management) rather than extracted from the network.

#### II.9 Product Dependency and Cross-Sell Map

Prerequisite/anchor: the current account at the primary bank, with DZ BANK payment services behind it. From there: savings → Union funds; home → BSH Bauspar + DZ HYP mortgage; protection → R+V; consumer credit → TeamBank; SME → VR Smart Finanz + VR Payment. Highest-margin (stock-compounding): Union AuM and R+V life/health. Retention products: current account and Bauspar (long contractual life). Current loss leaders: TeamBank and VR Smart Finanz (both loss-making FY2025). The binding constraint on cross-sell is that the **primary bank owns the relationship and the data**, so group-wide cross-sell depends on the bank's willingness and on Atruvia's Smart-Data tools (Truuco, the DZ BANK/Atruvia JV founded November 2022) rather than on manufacturer initiative. The fall in R+V referrals from ~320,000 to <200,000/year is the sharpest available evidence that the traditional cross-sell handoff is weakening as footfall declines — which is precisely why the group is investing in data-driven omnichannel cross-sell.

#### II.11 The Non-Cooperative Business

Genuinely competitive revenue: DZ BANK AG direct corporate/Mittelstand lending and capital-markets/Zertifikate sold to non-cooperative institutions (market leader in Zertifikate); Union Investment institutional mandates (€263.8bn; net inflows doubled to €9.8bn in 2025) won in open competition; R+V non-Verbund distribution (brokers; Assimoco/Italy; the CCB and ICCREA bancassurance partnerships in Italy); DZ HYP direct CRE and public-sector lending; DZ PRIVATBANK Luxembourg third-party fund services; TeamBank external embedded finance (>2,500 merchant partners). The owner-competitor conflict is managed by the joint/consortium-credit convention (the primary bank keeps the corporate relationship even when DZ BANK provides the balance sheet), but friction surfaced publicly in 2024–2025 (BVR vs DZ BANK over sector Schieflagen including BayWa; R+V's Signa losses). The non-cooperative business is a deliberate growth strategy in institutional asset management, custody and capital markets, and more of a by-product in retail lines. (Exact Verbund vs non-Verbund revenue split is UNKNOWN at group level — not disclosed.)

#### II.12 Failure and Exception Paths

- **Credit event on a joint/consortium loan — BayWa (documented):** per Handelsblatt (25 Feb 2025) quoting CEO Cornelius Riese, DZ BANK's loss provisions "mehr als verfünffachte auf 456 Millionen Euro," a "Großteil" BayWa-related. The Bavarian cooperative banks hold ~one-third of BayWa via their BRB vehicle and had already written down 60% of a €220m Schuldscheindarlehen (€132m) in the 2024 accounts, with further write-downs to potential total loss flagged by the GVB; DZ BANK and HVB were negotiating a standstill to autumn 2026. Loss borne by the lending banks and DZ BANK; end customers unaffected; reputational damage to the shared brand and a governance flashpoint between the sector and DZ BANK.
- **Investment loss at R+V — Signa (documented):** fully written off in the 2023 accounts as a "robuster dreistelliger Millionenbetrag" (CEO Rollinger: "in unserem Jahresabschluss 2023 komplett verarbeitet"), yet R+V still posted a ~€1bn IFRS result on a +€3.5bn investment result. Loss borne by R+V's balance sheet; policyholders unaffected — but Rollinger acknowledged the topic recurs in customer advisory conversations, direct evidence that shared-brand reputational risk transmits to the sales front line.
- **Payment/clearing outage:** DZ BANK owns the problem as central clearer; the consolidation onto one insourced platform raises single-point concentration risk against the efficiency gain.
- **Mis-selling / claims / fund liquidity / primary bank in difficulty:** the BVR's dual protection scheme (Sicherungseinrichtung des BVR + BVR Institutssicherung GmbH) backstops a primary bank in difficulty, funded sector-wide and focused on prevention of Schieflagen. This mutualisation of failure is the ultimate reason distribution loyalty holds: the banks are bound together by a shared safety net, which reinforces Verbundtreue even though product distribution itself is legally optional.

#### II.13 Product-Market Evolution (timeline)

2001 DG BANK/GZ-Bank merger → DZ BANK; 2016 WGZ BANK merger (also absorbing WGZ's Union stake); 2018 DZ HYP formed from DG HYP + WL BANK; 2019 Atruvia Omnikanalplattform live; **12 August 2022 DVB Bank defunct** (exit from non-core, non-Verbund product lines — the clearest signal of the "one champion per product" discipline); November 2022 DZ BANK/Atruvia Smart-Data JV (Truuco, live April 2023); 2023 growth of insurance + asset management to ~78% of group profit; 2024 payments consolidated onto one platform; 2 July 2026 card-business reorganisation announced (issuing-processing to Atruvia from 1 January 2027); ongoing strategy programmes "Verbund First 4.0" (DZ BANK), "NextLevel" (R+V), "#Fokus100" (BSH), "Fit for Future" (UMH), "Strategie 2028" (TeamBank), "DZ PRIVATBANK 2030." Direction of travel under the current Vorstand (sole CEO Cornelius Riese since 1 July 2024): consolidate infrastructure, deepen the Verbund distribution rail digitally, and lean on insurance and asset management as the profit engine.

#### II.14 Volume II Reconstruction

**(1) Product architecture by manufacturer:** CICB (corporate/capital-markets/transaction/central-bank); R+V (insurance/reinsurance); Union (funds/mandates); BSH (Bauspar/Baufi); DZ HYP (CRE/public/Pfandbrief); DZ PRIVATBANK (wealth/Lux fund services); TeamBank (consumer/embedded credit); VR Smart Finanz (SME leasing/loans); VR Payment (acquiring/POS/issuing to 2026); specialists (ReiseBank, CardProcess, VR Equitypartner, VR Factoring, GENO Broker).

**(2) Three-tier customer map:** (a) ~645–672 primary banks = owners+customers+distributors+governors; (b) >30m end customers owned by the primary banks; (c) direct corporate/institutional/third-party clients.

**(3) Customer-segment map:** primary banks by size/region/product-depth/liquidity-position (incl. 49 Warengeschäft banks); end customers by retail/HNW/Mittelstand/agricultural/public; direct clients by corporate/institutional/FI/international.

**(4) Jobs-to-be-done:** primary banks buy manufacturing, liquidity, risk capacity, capital-markets access and payment infrastructure to remain full-service at small scale; end customers buy home-savings, wealth-building, protection and liquidity.

**(5) Manufacture-and-distribute chain:** manufacture → catalogue → optional bank adoption → adviser sale → contract with manufacturer → commission to bank (bank keeps relationship + data).

**(6) Commission/revenue-share economics:** €2.8bn Verbund commission (2021, last confirmed) within €6.5bn aggregate primary-bank Provisionsüberschuss (2023 & 2024); vs DZ BANK Group net fee income €3,370m (FY2025). Manufacturer keeps stock margin; distributor keeps flow commission + relationship.

**(7) Money-movement/clearing flows:** ~9.9bn transactions/year via one insourced platform; T2/SEPA/SCT Inst/cards; liquidity, custody, risk-transfer, commissions and dividends as separate flows; card issuing-processing to Atruvia 2027.

**(8) Channel architecture:** 8 channels; shift from branch to Atruvia digital rail (which DZ BANK does not control).

**(9) Pricing by tier:** subsidised/cost-plus + market to primary banks; manufacturer-set retail pricing; market pricing to direct clients.

**(10) Product dependency/cross-sell:** current account anchor → funds/home/protection/credit; Union & R+V highest-margin; cross-sell gated by primary banks' relationship ownership.

**(11) Verbund vs non-Verbund:** growing genuine external business in institutional AM, custody, capital markets, Italy; exact split UNKNOWN.

**(12) Failure/exception map:** BayWa (€456m provisions), Signa (three-digit-million write-off), clearing concentration, IPS mutualisation.

**(13) Product-market evolution:** consolidation to one-champion, DVB exit, insurance/AM ascendancy, digital distribution, payments/card restructuring.

**(14) Key unknowns:** per-product commission rates and revenue splits; exact Verbund vs non-Verbund revenue split; R+V in-branch Außendienst headcount; number of cooperative banks connected to VR Smart Finanz; the post-2021 Verbundgeschäft commission series.

**(15) Ten most important conclusions:**
1. Value lives in the subsidiaries (R+V + Union = ~78% of profit); the parent bank is a utility.
2. Distribution is legally optional — the group competes for its own shelf space.
3. The primary banks own the relationship and the data; the group manufactures blind to the end customer.
4. The manufacturer keeps the compounding stock margin; the distributor keeps the flow commission.
5. Best economics: Union Investment (asset-light, compounding fees) and R+V life/health.
6. Worst economics: TeamBank and VR Smart Finanz (both loss-making FY2025).
7. Strategically most important despite not being the largest: payments/transaction banking — the infrastructural glue and now a profit centre feeding ~40% of the primary banks' commission.
8. The owner-competitor conflict is resolved by the Förderauftrag plus the joint-credit convention, but friction is real (BayWa).
9. The group does not control its own primary digital channel (Atruvia, ~0.35% stake) — a growing strategic vulnerability.
10. Münchener Hyp's independence is a permanent breach in the "one champion per product" ideal.

**Central question — is DZ BANK Group a bank, a bancassurance manufacturer, a distribution utility, or a holding company?** It is primarily a **holding company whose value lies in its subsidiaries, operating as a bancassurance/asset-management manufacturer for a distribution network it does not control and cannot compel.** It is a bank only in the narrow CICB/clearing sense. The defining tension — manufacturing for owners who are also its distributors and governors — means it behaves less like a profit-maximising financial conglomerate and more like a **member-serving manufacturing-and-infrastructure utility** whose profitability is a means to the Förderauftrag, not the end.

### Recommendations

1. **Value the group sum-of-the-parts, leading with the subsidiaries.** R+V and Union Investment are the crown jewels; the parent bank is a utility. Any analysis that leads with "the bank" misreads the entity. Threshold to revisit: if R+V + UMH fall below ~60% of group pre-tax profit for two consecutive years.
2. **Monitor distribution loyalty, not distribution contracts.** Because distribution is legally optional, the leading indicator of group health is the primary banks' continued willingness to sell group products. Track the aggregate primary-bank Provisionsüberschuss and (if republished) the Verbundgeschäft commission line; a sustained fall in the Vermittlungs-/Wertpapier component alongside rising third-party placement would signal shelf-space erosion.
3. **Treat the Atruvia channel-control question as the top strategic risk.** The group manufactures products but does not control the digital rail (VR Banking App) or, from 2027, card issuing-processing. Watch whether Atruvia begins onboarding non-Verbund product manufacturers into the app's Abschlussstrecken — that would directly threaten the group's captive shelf.
4. **Put TeamBank and VR Smart Finanz on watch.** Two consecutive loss years plus declining market share (TeamBank 3.9%) raise the question of whether they remain "champions" or become DVB-style disposal candidates. Trigger: a third loss year or a strategic review announcement.
5. **Price the shared-brand reputational channel.** BayWa and Signa show that sector-level events transmit into the advisory conversation and into DZ BANK's own P&L. Any single-name exposure large enough to require sector IPS discussion should be treated as a group-brand event, not merely a balance-sheet event.

### Caveats

- **Product-level economics remain the hard limit.** Commission rates, revenue splits with primary banks and per-product margins are largely unpublished. The €2.8bn Verbundgeschäft commission figure is 2021 and the specific line appears discontinued in the BVR online Jahresberichte thereafter; the €6.5bn aggregate Provisionsüberschuss (2023 and 2024) is a broader proxy that includes non-Verbund commission. The two are on different perimeters and must not be summed. Where exact splits are unavailable they are labelled UNKNOWN rather than estimated.
- The precise headcount of R+V Außendienst staff working inside bank branches is not disclosed (only "7,500+ Bankstellen served"); the exact number of cooperative banks connected to VR Smart Finanz is not in the primary 2025 source.
- The "subsidiäre Betreuung" model is confirmed for DZ HYP generally but not quoted verbatim in 2025 releases.
- Segment pre-tax figures are IFRS group-segment values; several subsidiary press releases quote HGB or sub-group numbers on slightly different perimeters, labelled where they diverge (e.g. R+V group IFRS pre-tax ~€2.22bn vs DZ BANK segment €2,144m; BSH €122m IFRS). The four perimeters (DZ BANK AG / DZ BANK Group IFRS / Genossenschaftliche FinanzGruppe ~€1.175trn / CRR prudential scope) are kept distinct throughout; product volumes routinely quoted at sector level (Bauspar contracts, insured risks, >30m customers) belong to the FinanzGruppe, not the DZ BANK Group.
- Forward-looking items (2026 guidance ~€3.0bn group pre-tax; DZ HYP's expected lower 2026 distributable result) are management projections, not facts.
- This is Volume II (Product, Customer, Distribution & Flow). Detailed financial analysis (margins, capital, per-segment profitability decomposition) belongs to Volume IV and is deliberately not attempted here.


---

# Part III — Operations, Technology, Data, Risk Infrastructure & Organisational Design

### The DZ BANK Group as a Federated Operating Model

---

### TL;DR

- **The DZ BANK Group runs not one operating model but at least seven separately licensed operational stacks** federated under a holding company. Only two systems genuinely span the group: the insourced payments/clearing platform ("ZV ON€", completed October 2024, 11.0bn transactions in FY2025) and the financial-conglomerate risk/finance/regulatory-reporting infrastructure required under §25 FKAG. Everything else — insurance policy administration (R+V), fund accounting (Union Investment), Bauspar contract management (BSH), Pfandbrief cover-pool management (DZ HYP), private-bank/fund services (DZ PRIVATBANK) — is run locally on entity-specific technology.
- **The single most systemically important operation is the payments platform.** DZ BANK is the clearing institution for ~640–700 cooperative banks; a failure would halt payments for a large share of German retail banking. DZ BANK deliberately *insourced* this (an in-house build on SAP-based infrastructure, integration by Capco) while Commerzbank *outsourced* to Worldline — the opposite strategic bet. It is both necessary infrastructure and, increasingly, a genuine competitive asset now being commercialised.
- **The federated structure cannot achieve single-institution efficiency, and is not meant to.** Six supervisory regimes (ECB/SSM, BaFin/Solvency II, KAGB/AIFMD, Bausparkassengesetz, CSSF, and FKAG conglomerate supervision) force duplicated control functions, parallel reporting factories and separate technology estates. The group's 49.3% cost/income ratio is good *for a conglomerate*, but the multi-entity/multi-regime design imposes a structural "conglomerate tax" — most visible in the regulatory-reporting burden — that a monoline would avoid. The offset is earnings diversification and a near-captive cooperative distribution channel.

---

### Key Findings

1. **Operating model = holding company with autonomous, separately regulated operating units, plus two shared group-spanning systems.** DZ BANK AG centralises group finance, group risk, group treasury, group compliance and group audit (the FKAG-mandated conglomerate functions). It does NOT centralise the production engines of its subsidiaries. R+V underwrites and settles claims on its own stack in Wiesbaden; Union Investment runs portfolio management on SimCorp; BSH runs a SAP S/4HANA core; DZ HYP runs its own VR-BaufiConnect lending engine; DZ PRIVATBANK runs OLYMPIC/OLYNEXT on IBM i in Luxembourg. This is a hybrid tilted strongly toward **federation**, not shared services.

2. **The Atruvia boundary is the defining structural fact of the group's technology estate.** Atruvia AG is the IT utility for the ~640–700 *primary* cooperative banks — it runs their core banking (agree21/bank21), the VR Banking App, OnlineBanking and the Omnikanalplattform. DZ BANK holds only ~0.35% of Atruvia and does **not** run its own systems on Atruvia. DZ BANK AG runs its own core banking and general ledger on **SAP / S/4HANA** (with SAP Fioneer), its capital-markets stack on **Murex MX.3**, and its payments on the in-house **ZV ON€** platform. From 1 January 2027, card issuing-processing (debit + credit) moves from VR Payment to Atruvia (Bundeskartellamt case B9-75/26, notified 15 July 2026) — meaning DZ BANK will manufacture card products but not control their processing.

3. **Payments scale is confirmed and rising:** 9.9bn transactions (FY2023) → 10.2bn (FY2024) → **11.0bn (FY2025)** on the single ZV ON€ platform. The build took roughly 500 people, five years and over 100,000 person-days, with a budget in the three-digit millions of euros. Migration of more than 600 cooperative banks completed end-2024 without material public incident.

4. **Risk/finance infrastructure is the second group-spanning system and the largest hidden operational cost driver.** The group must consolidate simultaneously under IFRS (group), HGB (parent), and Solvency II (R+V), then compute a financial-conglomerate coverage ratio under Delegated Regulation (EU) 342/2014 in conjunction with Article 49(1) CRR — because the CRR prudential scope *excludes* insurance and Solvency II covers *only* R+V. This produces an annual §25(3)/(4) FKAG report on top of Pillar 3, SREP/ICAAP/ILAAP, SRB resolution planning, DORA, and the CSSF/BaFin/Bundesbank/ESA reporting stack.

5. **The insurance operation (R+V) is the largest earnings contributor and an entirely different operational discipline** — more than 18,400 employees, ~9m customers, ~26m insured risks, gross written premiums €22.8bn (2025). It restructured its board in 2025 to create a dedicated "Operations und IT" division (Klaus Endres, from 1 April 2025), signalling operational-efficiency pressure under the "NextLevel" strategy, which delivered ~€100m of savings in 2025.

---

### Details

#### III.1 The Federated Operating Model

**What it is.** The DZ BANK Group is a financial conglomerate: a central cooperative bank (DZ BANK AG), a composite insurer (R+V), an asset manager (Union Investment/UMH), a Bausparkasse (BSH), a Pfandbrief mortgage bank (DZ HYP), a Luxembourg private bank and fund-services house (DZ PRIVATBANK), a consumer lender (TeamBank) and a small-business finance/leasing company (VR Smart Finanz), plus the payments company VR Payment and specialist units. Each material entity is separately licensed and separately supervised.

**Structure — what is centralised vs local.**

```
DZ BANK AG (holding + operating central institution)
│
├─ CENTRALISED AT PARENT (conglomerate functions):
│   • Group Finance (Konzern-Finanzen): IFRS consolidation, group controlling, group prudential
│   • Group Risk (Konzern-Risikocontrolling / Konzern-Risikosteuerung & Services)
│   • Group Treasury (Liquiditätsausgleichsfunktion for the whole GFG)
│   • Group Compliance / AML / Client Lifecycle Management
│   • Group Audit
│   • Transaction Banking (payments, cards oversight, custody/depositary)
│
├─ ENTITY-LOCAL PRODUCTION ENGINES (run by each subsidiary):
│   • R+V — underwriting, claims, actuarial, investment ops, reinsurance (Wiesbaden)
│   • Union Investment — portfolio mgmt, fund accounting, NAV, admin (Frankfurt/Luxembourg)
│   • BSH — Bauspar contract management, credit servicing (Schwäbisch Hall)
│   • DZ HYP — commercial + retail real-estate lending, cover-pool mgmt (Hamburg/Münster)
│   • DZ PRIVATBANK — private banking + fund services (Luxembourg/Zurich/Stuttgart)
│   • TeamBank — consumer-loan underwriting + easyCredit embedded finance (Nuremberg)
│   • VR Smart Finanz — leasing + express-loan (Eschborn)
│   • VR Payment — card acquiring, POS, terminals (Ilvesheim/Frankfurt)
```

**Direction of travel.** The evidence points to *more* federation of production but *more* centralisation of platforms where scale economics dominate. The clearest signals: (a) DZ BANK insourcing payments into one platform for the whole sector; (b) the 2027 consolidation of card issuing-processing into Atruvia (removing it from DZ BANK/VR Payment); (c) R+V's creation of a combined "Operations und IT" board division; (d) BSH's migration to a single SAP S/4HANA core. Each is a "one platform, run it at scale" move — but the platforms sit in *different* legal entities (DZ BANK for payments, Atruvia for cards, R+V for insurance ops), so the group is federating around several scale centres rather than one.

**Governance model classification (ANALYTICAL INFERENCE):** This is a **holding-company model with autonomous operating units and selective shared platforms** — not a true shared-services model. The unifying glue is (i) the FKAG conglomerate risk/finance spine and (ii) supervisory-board interlock (Riese chairs BSH, R+V, TeamBank, Union Investment; Koch chairs DZ HYP, DZ PRIVATBANK, VR Smart Finanz — established in Volume I).

---

#### III.2 Payments, Clearing and Settlement Operations — PRIORITY DEPTH

**The single most systemically important operation in the group.**

##### The insourced platform: "ZV ON€"

- **What it is (CONFIRMED FACT):** DZ BANK's 2024 annual report (DZ BANK AG, HGB accounts, filed to the Bundestag Lobbyregister) states: *"Durch das Projekt „ZV ON€" wurde der gesamte Zahlungsverkehr der Genossenschaftlichen FinanzGruppe auf eine leistungsfähige In-House-Plattform vereint."* It is an **in-house build**, not a packaged vendor product — evolved from the legacy WGZ Bank in-house payments platform inherited in the 2016 merger.
- **Who built it (CONFIRMED FACT):** ~500 people, five years, over 100,000 person-days, per DZ BANK payments head Matthias Ehringer via Payment & Banking: *"Insgesamt etwa 500 Mitarbeiter:innen, fünf Jahre und über 100.000 Arbeitstage brauchte es."* The project effectively began with the 2016 WGZ Bank merger. Systems-integration and IT-strategy partner: **Capco**, whose own case study puts its scope from April 2019 to end-2024, comprising "fünf großen ZV-Migrationen," "97 einzelne Go-Live Events," "63 Projektdrehbücher mit bis zu 1.281 Einzelaktivitäten," and the migration of "Mehr als 600 Banken sowie tausende Firmenkunden." Budget: three-digit-million euros (DZ BANK Group report 2024). Atruvia contributed to the target-picture design.
- **What it replaced:** A split estate — the historical DZ BANK side had partly used Equens/equensWorldline (DZ BANK's payments-processing subsidiary was carved out in 2003 into the Transaktionsinstitut, merged into Equens in 2006; DZ BANK sold its residual equensWorldline stake to Worldline effective 30 September 2019), while the smaller WGZ Bank side processed in-house. The merger forced a single target.
- **Why insourcing (COMPANY CLAIM, Thomas Ullrich, then-Vorstand, Börsen-Zeitung):** *"Während die Commerzbank beim Zahlungsverkehr einen Outsourcing-Ansatz verfolgt, betreibt die DZ Bank ein Insourcing."* The stated rationale (Ehringer): development cost is high but long-term cheaper than per-transaction fees to an external clearing/authorisation provider, given the sector's volume. Strategic goal: become a payment provider not just for the ~700 cooperative institutes but for banks outside the sector, and monetise ("versilbern") the platform.
- **Why delayed one year:** Migration was planned to 2023 but pushed to end-2024 to absorb T2/TARGET2 consolidation, ISO 20022 migration and SEPA-standard changes concurrently.

##### Processing scale and profile

| Metric | FY2023 | FY2024 | FY2025 |
|---|---|---|---|
| Payment transactions (ZV ON€) | 9.9bn | 10.2bn | **11.0bn** |
| H1 transactions | 4.8→5.1bn | 5.1bn | 5.3bn |
| Credit-card transactions | 365.9m | 457.1m | +23% YoY |
| Cards issued | 6.7m | 7.2m | +11% card sales |
| Depositary/custody fund volume | €332.5bn | €369.9bn | €380.7bn |

(CONFIRMED FACT, DZ BANK preliminary-results releases 2024–2026.) Note the definitional perimeter: the figure counts *processed payment transactions on the ZV ON€ platform for the cooperative FinanzGruppe* — i.e. bulk SEPA credit transfers, direct debits, instant payments and cross-border/SWIFT, plus card-scheme messages. It is a throughput count, not a value figure. DZ BANK targets up to **one-third of all German payment traffic** running across the platform.

**Split (ANALYTICAL INFERENCE — the group does not publish a clean breakdown):** The overwhelming majority of the 11.0bn are SEPA bulk (SCT + SDD) processed through the Bundesbank SEPA-Clearer/EMZ; card transactions are a separately-reported and much smaller count (hundreds of millions); instant payments a fast-growing minority; high-value/SWIFT a small count but high value. HYPOTHESIS: SCT+SDD >80% of volume.

##### Rails and gateways (CONFIRMED FACT, from product pages + sector structure)

- **T2/TARGET2:** DZ BANK is a direct T2 participant and settlement-account holder; it provides indirect access and settlement for cooperative banks.
- **SEPA-Clearer/EMZ (Deutsche Bundesbank):** the bulk-file rail; bulk files up to 100,000 items, ~€0.0025/transaction (established Vol II).
- **EBA CLEARING:** STEP2 (bulk SEPA) and RT1 (instant); DZ BANK is a participant.
- **TIPS:** the Eurosystem instant-settlement layer used for SCT Inst.
- **Card schemes:** DZ BANK is a scheme member of Visa and Mastercard; also engaged in EPI/Wero (P2P live July 2024).

##### EU Instant Payments Regulation compliance (CONFIRMED FACT)

The IPR ((EU) 2024/886) imposed: receive instant payments by **9 January 2025**; send instant payments plus Verification of Payee (VoP) by **9 October 2025**; removal of the €100,000 scheme cap. DZ BANK met the deadlines on time — notable given how few European banks were technically ready. Per the Capgemini Research Institute's *World Payments Report 2025* (10 September 2024), *"only 13% of European banks can claim a strong technology foundation for instant payments"* — i.e. roughly 87% lacked a robust instant-payments tech base (EU 13% vs Asia-Pacific 30%, Americas 26%). Ullrich publicly argued for removing the €100,000 cap and for allowing premium pricing on large instant transactions — a revenue concern given the IPR bars charging more for instant than standard SCT.

##### The card operation, pre- and post-1 January 2027 (CONFIRMED FACT)

- **Today:** VR Payment (a DZ BANK subsidiary, ~248 employees, revenue over €200m) is the cooperative sector's full-service acquirer — POS network operation, terminals, card acceptance, e-commerce, plus **issuing-processing** for debit and credit. DZ BANK is the card-issuing bank/scheme member.
- **From 1 January 2027:** Atruvia acquires VR Payment's **issuing-processing** business (Bundeskartellamt B9-75/26, notified 15 July 2026; announced 2 July 2026). Atruvia will run debit + credit issuing-processing on one **integrated card platform** (girocard/debit/credit unified). VR Payment refocuses on **acquiring, POS-network operation and omnichannel merchant solutions**. Dr Imke Jacob (DZ BANK Vorstand Transaction Banking) chairs VR Payment's supervisory board and co-leads the realignment.
- **Operational risk of the migration (ANALYTICAL INFERENCE):** Moving live issuing-processing for a large share of German credit-card transactions onto Atruvia's platform is a high-stakes cutover. Legal counsel (McDermott) publicly noted *"Ein wesentlicher Teil aller Kreditkartentransaktionen in Deutschland wird über die Systeme von Atruvia abgewickelt."* Concentration risk rises: card processing joins core banking under one utility that DZ BANK barely owns.

##### Securities settlement and custody (CONFIRMED FACT)

DZ BANK is the **third-largest depositary (Verwahrstelle) in Germany**, fund volume €380.7bn at end-2025, grown partly by acquisition (e.g. the apoBank depositary business). It connects to Clearstream/T2S for settlement. The Luxembourg fund-services operations sit at Attrax (Union Investment group) and DZ PRIVATBANK/IPConcept. DZ BANK also operates a crypto-securities registrar / crypto-custody capability for institutional clients and is active in DLT-based (blockchain) bond issuance and custody.

**Collateral operations (CONFIRMED FACT, Murex):** DZ BANK processes ~1,400 collateral calls per day across more than 5,400 collateral agreements on Murex MX.3 for Collateral Management (Rüdiger Welsch, head of operations IT, DZ BANK) — one of the largest MX.3 platforms in Central Europe.

---

#### III.3 Treasury, Liquidity and Balance-Sheet Operations

**Mandate (CONFIRMED FACT):** DZ BANK's Konzern-Treasury performs the **Liquiditätsausgleichsfunktion** for the entire Genossenschaftliche FinanzGruppe — the daily netting of surplus and deficit liquidity across the cooperative banks — and secures access to money/capital markets and central-bank liquidity. It is the competence centre for unsecured and secured funding.

**How surplus deposits are managed:** The ~640–700 primary banks are structurally deposit-rich (retail funding exceeds local lending). They place surplus liquidity with DZ BANK (the Depot-A relationship), which aggregates and reinvests it and provides refinancing to deficit institutions. DZ BANK thus intermediates the sector's internal balance sheet.

**Systems supporting the primary banks (CONFIRMED FACT):** DZ BANK offers GENO-SAVE and EGon to the cooperative banks for own-account business (Eigengeschäft), regulatory reporting (Meldewesen) and accounting — i.e. DZ BANK is a *provider of treasury/reporting tooling* to the primary banks, not just their counterparty.

**Funding/issuance:** DZ BANK optimises its own funding via securities issuance placed through its own sales and via intermediaries to institutional clients (insurers, funds) in Germany and abroad. DZ HYP runs the Pfandbrief funding operation (incl. Green Pfandbriefe). Under "Verbund First 4.0," DZ BANK expanded a dedicated "Treasury/Refinanzierung" work package.

**ALM relevance:** Net interest income fell 17.8% in FY2025 (established), making interest-rate-risk management and ALM operationally central. Treasury *economics* belong to Volume IV; here the point is operational: intraday liquidity, collateral mobilisation with the Eurosystem (managed on Murex MX.3), and the settlement-account plumbing into T2.

---

#### III.4 Technology Architecture — PRIORITY DEPTH, MOST EVIDENCE-CONSTRAINED

##### DZ BANK AG's own core systems (CONFIRMED FACT — resolved)

The open question "who provides DZ BANK's own core banking?" is now answered from DZ BANK's own careers/technology page:

> *"Unter allen deutschen Banken haben wir in der DZ BANK die meisten SAP-Anwendungen im Banking im Einsatz und dabei bauen wir komplett auf S/4 HANA. Angefangen vom SAP Business Partner über das gesamte SAP Core Banking bis zur Aufbereitung und Analyse im SAP BW oder in SAP BO nutzen wir Software vom Marktführer aus Walldorf."*

- **Core banking + general ledger/finance:** **SAP**, standardising on **S/4HANA** (mid-migration from SAP R/3), plus **SAP Fioneer**. SAP BW/BO for analytics/reporting. DZ BANK describes itself as the most SAP-intensive bank in Germany and a "Fast Follower."
- **Capital markets / trading:** **Murex MX.3** (front-to-back, collateral, securities finance) — confirmed by Murex case studies and a third-party integrator noting data feeds "aus dem DZ BANK-Handelssystem Murex."
- **Payments:** in-house **ZV ON€** (see III.2).
- **Integration backbone (CONFIRMED FACT, DZ BANK IT careers):** an **EAI (Enterprise Application Integration) platform** — "eine der größten Plattformen ihrer Art im D-A-CH Raum," with ~500 internal/external applications exchanging data; job scheduling via **Automic Automation Engine**; IT-cost transparency via **Apptio**.

##### Data centres and infrastructure (CONFIRMED FACT, DZ BANK IT careers)

> *"Unsere Systeme betreiben wir selbst in den besten Rechenzentren Frankfurts sowie bei zwei der großen Cloud-Hyperscalern."*

- On-prem data centres in Frankfurt (self-operated); classic virtualised Linux/Windows server estate.
- **Two hyperscalers** used (unnamed publicly); container technologies; a "Virtual Hybrid IT-Infrastructure" model integrating cloud into the on-prem estate. Mainframe/batch legacy retained as an "efficient booking machine in the background" (DZ BANK Innovation LAB, 2020: "intelligenter Rück- und Umbau" of legacy core systems).

##### Subsidiary technology estates

| Entity | Core / production systems | Evidence class |
|---|---|---|
| **R+V** | Bespoke software for the insurance core (Beratung, Verkauf, Bestandsführung, Schaden) **plus** standard software from **Salesforce, SAP, Microsoft, IBM**; new "Operations und IT" board division from April 2025; VR/3D-scan claims tooling ("AssureXR" w/ Fraunhofer IGD) | CONFIRMED (CIO.de; R+V PR) |
| **Union Investment** | **SimCorp** (portfolio/investment management; SimCorp partnership with Quoniam confirmed 2024); **Attrax S.A.** Luxembourg fund-services/brokerage platform (transfer agent, fund administration) | CONFIRMED (SimCorp; Attrax) |
| **BSH** | **SAP S/4HANA** core banking ("NEXT" migration; role-model SAP real-estate-credit standard; migration tooling by paricon; programme support by Wavestone); Bauspar processing being migrated onto SAP progressively | CONFIRMED (Wavestone; paricon; Bank Blog) |
| **DZ HYP** | **VR-BaufiConnect** proprietary processing software behind VR-BaufiComfort; connected to Genopace, Baufinex, Europace and Atruvia Omnikanalplattform; "FK Digital" for corporate-credit digitalisation | CONFIRMED (Börsen-Zeitung; DZ HYP) |
| **DZ PRIVATBANK** | **OLYMPIC / OLYNEXT** core banking (ERI Bancaire) on **IBM Power / IBM i (OS/400)**; Oracle PL/SQL + APEX application landscape; SAP BusinessObjects/Crystal Reports/Tableau for reporting; fund-admin/NAV/TA product **not publicly named** | CONFIRMED core (job ads); fund-admin UNKNOWN |
| **TeamBank** | easyCredit consumer-loan platform + **easyCredit-Ratenkauf / -Rechnung** embedded-finance APIs; merchant plugins (open-source on GitHub, Vue.js transaction manager); CTO Reinhold Rehbichler; more than 2,500 merchant partners | CONFIRMED (TeamBank; GitHub) |
| **VR Payment** | Acquiring/POS/terminal platform; issuing-processing (moving to Atruvia 2027); stake in Wallee | CONFIRMED |
| **VR Smart Finanz** | Leasing + express-loan ("VR Smart flexibel") digital processing | THIN — little published |

##### Engineering practice (CONFIRMED FACT)

DZ BANK IT publicly emphasises agile transformation, container/cloud CI-CD, and dual-study (Wirtschaftsinformatik/Softwaretechnologie) talent pipelines. R+V transformed its IT into an agile organisation under former CIO Tillmann Lukosch (2018–2025). TeamBank publishes open-source merchant SDKs. **Where nothing is published:** the group does not disclose detailed SLOs, deployment frequencies, or internal architecture beyond the above — marked UNKNOWN.

---

#### III.5 Build, Buy, Outsource and the Atruvia Boundary

| Capability | Sourcing model | Owner/vendor | Reasoning |
|---|---|---|---|
| Primary-bank core banking + digital channels | **Utility (sector utility)** | **Atruvia** (DZ BANK ~0.35%) | Sector-wide scale; not DZ BANK's to control |
| DZ BANK AG core banking / GL | **Buy + heavy config** | **SAP S/4HANA / Fioneer** | Standard bank-in-a-box; deep SAP investment |
| Capital-markets front-to-back | **Buy** | **Murex MX.3** | Industry standard; one of largest MX.3 in C. Europe |
| Payments processing | **Insourced / build** | **ZV ON€ (in-house)**, Capco integration | Volume economics; strategic control; monetisation |
| Card issuing-processing | **Moving to utility (2027)** | VR Payment → **Atruvia** | Scale consolidation; loss of DZ BANK control |
| Card acquiring / POS | **In-house subsidiary** | **VR Payment** | Merchant-side differentiation |
| Securities settlement/custody | **Build + market infra** | DZ BANK depositary + **Clearstream/T2S** | 3rd-largest German depositary; scale |
| Insurance policy admin/claims | **Build + buy** | R+V bespoke + SAP/Salesforce/IBM | Insurance is a distinct discipline |
| Fund administration/depositary | **Build (entity-local)** | Union Investment + **Attrax**; DZ PRIVATBANK + **IPConcept/OLYMPIC** | Luxembourg regulatory + scale |
| Risk & regulatory reporting | **Build (group)** | DZ BANK Konzern-Finanzen/-Risiko on SAP + EAI | Conglomerate-specific |
| Data & analytics (next-best-action) | **JV** | **Truuco** (DZ BANK/Atruvia JV, live April 2023) | Access to primary-bank data |
| Cloud & infra | **Hybrid** | Own Frankfurt DCs + 2 hyperscalers | Sovereignty + scalability |

**The Atruvia boundary — assessment.** DZ BANK **manufactures** products (payments rails, funds, insurance, loans, cards) but does **not** control the primary banks' digital channel (Atruvia), and from 2027 will **not** control card issuing-processing (Atruvia). This is a structural asymmetry: the group's route to ~30m end customers runs through software it barely owns.

- **Operational control:** Weakened on the customer-facing edge; strong on the manufacturing core (payments, custody, capital markets, insurance, funds).
- **Cost:** Atruvia's utility model spreads IT cost across ~640–700 banks — cheaper than DZ BANK could achieve alone for channel/core — but DZ BANK cannot capture that margin.
- **Strategic optionality:** Reduced. If Atruvia's roadmap diverges from DZ BANK's product ambitions (Wero, Request-to-Pay, digital euro), DZ BANK must negotiate rather than direct. The Truuco JV is the mechanism to regain some data/analytics leverage.
- **Direction (ANALYTICAL INFERENCE):** The group is becoming *more* dependent on Atruvia (channels + core + cards from 2027), not less. This is the single biggest third-party-dependency question in the group.

---

#### III.6 Insurance Operations (R+V) — real depth

**Scale (CONFIRMED FACT):** more than 18,400 employees; ~9m customers; ~26m insured risks; gross written premiums €22.8bn (2025); record 2024/2025 group results; the largest segment pre-tax contributor (€2,144m in FY2025).

**Lines:** life, health, property/casualty, motor, accident, legal-protection, credit/surety, and a large agricultural book (R+V is the cooperative sector's agricultural insurer). Composite structure across multiple legal entities: R+V Lebensversicherung AG, R+V Krankenversicherung AG, R+V Allgemeine Versicherung AG, R+V Direktversicherung, KRAVAG (transport/motor for the haulage sector), plus R+V Versicherung AG as group parent and central reinsurer.

**Underwriting & claims operations:** Distribution runs primarily through **more than 13,000 cooperative bank branches** plus R+V's own Außendienst (general agencies and Hauptvertretungen). Claims automation is a "NextLevel" priority — R+V reports two-digit-million-euro savings from AI in advisory, underwriting and fraud detection, and is piloting 3D-scan/VR claims capture ("AssureXR" with Fraunhofer IGD) to cut manual steps in property-damage adjustment.

**Reinsurance (CONFIRMED FACT, SFCR):** R+V Versicherung AG is the **central reinsurer** of the group's primary insurers and independently writes worldwide non-life reinsurance from Wiesbaden (2024 gross written premiums €4,106m at the AG level). This makes R+V one of the few bank-owned groups running a genuine reinsurance operation.

**Investment operation:** R+V runs the group's second-largest balance sheet after the bank; its capital-investment result (R+V Lebensversicherung ordinary investment income above €1.6bn per year) is managed via a Finance/Risk board division (created autumn 2024) and an investment committee. **Signa exposure** was fully written off in R+V's 2023 accounts. R+V CEO Norbert Rollinger stated on 3 April 2024: *"Wir haben das Signa-Engagement in unserem Jahresabschluss 2023 komplett verarbeitet."* The widely-quoted characterisation "robuster dreistelliger Millionenbetrag" in fact originated not with Rollinger but with DZ BANK Co-CEO / R+V supervisory-board chair Cornelius Riese (per procontra). Either way, the episode illustrates how single-name real-estate/private-market exposures are managed through reserving and write-down rather than group contagion.

**Solvency II operations (CONFIRMED FACT):** R+V produces annual SFCRs per legal entity, runs ORSA, and applies transitional measures (§352 VAG Rückstellungstransitional) and the volatility adjustment on the life book. SCR coverage was 168% at end-2024. R+V has a *modified* risk-governance structure reflecting its Solvency II (not CRR) regime — explicitly noted in the group risk report.

**Board restructuring (CONFIRMED FACT):** From 1 April 2025, R+V created a combined **"Operations und IT"** division (Klaus Endres), integrating the former "IT, Digitalisierung und Prozesse" division — a clear operational-efficiency signal. "NextLevel" is a five-year strategy to 2030; an efficiency programme delivered ~€100m savings in 2025.

---

#### III.7 Asset-Management Operations (Union Investment) — depth

**Scale:** AuM €534.7bn (retail €270.8bn / institutional €263.8bn); ~4,400 staff; segment pre-tax €1,185m FY2025.

**Portfolio management & trading (CONFIRMED FACT):** Union Investment runs **SimCorp** for investment management; its quant subsidiary **Quoniam** signed a SimCorp partnership in 2024 (AI/ML/big-data systematic investing on SimCorp's platform plus research-cloud). This places Union Investment on the same class of front-to-back IBOR platform used by other large European managers.

**Fund administration & NAV / depositary:** Fund administration and NAV production for the Luxembourg range run through **Union Investment Luxembourg S.A.** (35+ years, one of the most experienced Luxembourg ManCos) and **Attrax Financial Services S.A.** (CSSF-regulated, §24-1/24-2; a "one-stop" fund brokerage, administration and transfer-agency house). The depositary function for German funds is provided by DZ BANK's depositary (see III.2).

**Sustainability data / SFDR classification (CONFIRMED FACT):** Article 8/9 assets reached €153.7bn at end-2025 (from €146.6bn end-2024); an internal "sustainable minimum-standards" figure is separately reported (€127.1bn end-2024). This is a substantial data-operations burden — SFDR classification requires per-instrument ESG data pipelines.

**Distribution operations:** Retail distribution runs through the primary cooperative banks (and BSH's field force for building-society-linked products); institutional client servicing is direct. Programme: "Fit for Future" (efficiency/operating-model).

---

#### III.8 Credit, Lending and Real-Estate Operations

**DZ BANK corporate credit & Metakredit (CONFIRMED FACT):** DZ BANK acts *subsidiarily* to the primary banks in corporate lending, and runs the consortium/joint-credit ("Metakredit") model (~€19.3bn, established Vol II) in which DZ BANK and primary banks share exposures. Corporate-credit digitalisation runs under a dedicated programme.

**DZ HYP VR-BaufiComfort — how it works operationally (CONFIRMED FACT):** This is the clearest example of *manufacturing/distribution division of labour* in the group. In the retail model:
1. The Volksbank/Raiffeisenbank adviser handles **customer advice** on the Verbund platforms **Genopace** and **Baufinex** (and, from 2024, Atruvia's Omnikanalplattform).
2. **Without needing a framework contract with DZ HYP**, the adviser submits the application; DZ HYP then **takes over the entire process from application onward** — credit check, approval, and all downstream steps through to disbursement.
3. The technical backbone is DZ HYP's proprietary **VR-BaufiConnect** software, enabling media-break-free data processing from the sales systems and standardised/automated flows that can produce a **credit decision plus contract within 24 hours**. (Context: Bundesbank reported private-construction new business +21.4% to €240.9bn in 2025.)

**Pfandbrief cover-pool management:** DZ HYP manages its Pfandbrief cover pools and reporting (incl. Green Pfandbrief framework), financing portfolio ~€57.6bn (established). VR WERT provides property valuations/appraisals.

**BSH Bauspar contract administration (CONFIRMED FACT):** ~7m contracts on the new **SAP S/4HANA** core ("NEXT" programme; migration tooling by paricon; Wavestone support) — a "role-model" SAP real-estate-credit migration in Germany. The **Baufinex** B2B marketplace (JV with Hypoport) carries more than 8,000 intermediaries and more than 560 product partners; transaction volume +~40% to €8.3bn (established).

**TeamBank easyCredit-Ratenkauf merchant integration (CONFIRMED FACT):** easyCredit-Ratenkauf (€200–€10,000) and easyCredit-Rechnung (€50–€5,000) are embedded-finance/BNPL products with instant online credit checks; TeamBank bears the default risk and pays merchants within ~3 days. Integration via store plugins (JTL, PlentyONE, e-vendo, modified, etc.) and a Vue.js merchant "Transaction Manager" (open-source on GitHub). More than 2,500 cooperative-sector merchant partners; run as a "hochverfügbares System." Loan book €9,132m; ~1.067m customers (established).

**VR Smart Finanz:** leasing and express small-business loans ("VR Smart flexibel"), cost/income 78.6% (established) — the least-automated, thinnest-margin operation; little technology detail published (UNKNOWN).

---

#### III.9 Risk, Finance and Regulatory-Reporting Infrastructure — PRIORITY DEPTH

**The second genuinely group-spanning system.**

**The conglomerate aggregation problem (CONFIRMED FACT):** The DZ BANK financial conglomerate = **DZ BANK Institutsgruppe (CRR scope, excludes insurance) + R+V (Solvency II)**. Because no single prudential regime covers both, the group computes a **financial-conglomerate coverage ratio (Bedeckungssatz)** under **Delegated Regulation (EU) 342/2014 in conjunction with Article 49(1) CRR** — the quotient of (sum of eligible own funds) over (sum of solvency requirements) across banking and insurance. BaFin is the conglomerate supervisor (FKAG, in force since 4 July 2013, transposing Directive 2011/89/EU).

- **Coverage at end-2024:** exceeded the external minimum of 100.0%, the internal minimum threshold of 113.0%, and the internal observation threshold.
- **Historical anchor:** end-2020 eligible own funds €35,805m vs requirements €24,516m = 146.0% coverage.
- **Economic vs normative:** the conglomerate coverage and economic capital adequacy are both anchored on Solvency II-style market-consistent valuation (marktnahe Bewertung), so the CRR III transition does not disturb the market-value basis.

**Risk governance (CONFIRMED FACT):** Three-lines-of-defence model; R+V runs a *modified* governance reflecting Solvency II. Central units: **Konzern-Risikocontrolling, Konzern-Risikosteuerung & Services, Konzern-Finanzen**. Group-wide risk reporting across all material risk types is built on prescribed minimum standards and harmonised methods; each Steuerungseinheit's risk-controlling ensures transparency and method currency against DZ BANK-allocated risk capital. Compliance framework reviewed annually; R+V may deviate where special/insurance law requires (documented).

**The reporting factory (ANALYTICAL INFERENCE + CONFIRMED components):** DZ BANK must simultaneously satisfy:
- **ECB/SSM** (banking; P2R 1.80% for 2026, O-SII buffer 1.00%) — SREP, ICAAP, ILAAP, COREP/FINREP, stress tests (the EBA 2025 test confirmed CET1 of 17.9% at H1 2025).
- **BaFin** — conglomerate supervision (§25 FKAG report, around 15 May annually), plus national reporting.
- **Bundesbank** — payment-system and statistical reporting.
- **Solvency II** (R+V) — SFCRs, RSR, ORSA, QRTs.
- **KAGB/UCITS/AIFMD** (Union Investment) — CSSF (Luxembourg) + BaFin.
- **CSSF** — DZ PRIVATBANK, Attrax, IPConcept.
- **SRB** — resolution planning (MREL, resolution reporting).
- **DORA, GwG/AML, MiFID II** — cross-cutting.
- **CRR III** in force from 1 January 2025 (output floor, RWA changes) — a driver of CET1 rising from 15.8% to 18.4%.

Group finance consolidates under **IFRS (group), HGB (parent) and Solvency II (R+V) simultaneously** — three accounting/valuation bases running in parallel on the SAP/BW estate. This triple-basis consolidation is the core operational cost driver of the conglomerate structure.

---

#### III.10 Data Architecture and Governance

**The central tension (ANALYTICAL INFERENCE, well-grounded):** The **primary banks own the end-customer relationship and data** (they are the account-holding institutions on Atruvia's core). DZ BANK Group manufactures products but does not own the customer. So how does it get the data to manufacture, price and cross-sell?

- **Truuco (CONFIRMED FACT):** the DZ BANK/Atruvia JV (founded November 2022, live April 2023) provides Smart-Data and next-best-action capability *to the primary banks*. It is the mechanism by which product-relevant signals flow — but the analytics run *for* the primary banks, whose data governance and customer consent gate the flow. Truuco is effectively the group's attempt to build a data capability *on top of* Atruvia's data estate without owning it.
- **GDPR controller/processor allocation (ANALYTICAL INFERENCE):** The primary bank is controller for its customers; Atruvia is processor for core/channel; DZ BANK entities are controllers for their own manufactured products (a fund investor, an insurance policyholder, a Bauspar contract holder become customers of the respective subsidiary). This creates a **fragmented controllership map** — no single group entity is controller for the ~30m end customers.
- **Data warehousing/analytics:** DZ BANK runs SAP BW/BO for finance/risk; a Financial Data Warehouse integrates trading data from Murex. R+V, Union Investment (SFDR ESG data pipelines) and BSH run their own analytics estates. AI/ML: R+V (underwriting/fraud/advisory), Union Investment/Quoniam (systematic investing), DZ BANK (generative-AI work package under Verbund First 4.0).

**Does a group-wide data flywheel exist? (HYPOTHESIS / ANALYTICAL INFERENCE):** No — not a true group flywheel. The relationship-ownership structure of the cooperative model *structurally prevents* a single group data asset. The group has *entity-level* flywheels (Union Investment's fund data, R+V's claims/actuarial data, TeamBank's credit-decision data, DZ BANK's payments data) and a *federated* signal-sharing layer (Truuco), but not the unified customer-360 that an integrated bank or a fintech would build. This is the sharpest data question in the group, and the answer is: the cooperative structure trades data-integration upside for local relationship ownership.

---

#### III.11 Cyber, Security and Operational Resilience

**DORA implementation (ANALYTICAL INFERENCE + CONFIRMED regime):** DORA applies across the whole multi-entity, multi-regime group from January 2025. The operational challenge is acute precisely because the group spans banking, insurance and asset-management regimes — the ICT third-party register and critical-third-party identification must span DZ BANK AG, R+V (insurance), Union Investment (AIFMD), and the Luxembourg CSSF entities.

**Critical third parties (ANALYTICAL INFERENCE, well-grounded):**
- **Atruvia** — channels/core for the primary banks; cards from 2027 (the dominant CTP).
- **SAP / SAP Fioneer** — DZ BANK core banking/GL.
- **Murex** — capital markets.
- **ERI Bancaire (OLYMPIC)** — DZ PRIVATBANK core.
- **SimCorp** — Union Investment.
- **IBM** — DZ PRIVATBANK infrastructure (IBM Power/i); R+V software stack.
- **Hyperscalers** (two, unnamed publicly) — DZ BANK cloud.
- **Deutsche Bundesbank (SEPA-Clearer/EMZ, T2), EBA CLEARING (STEP2/RT1), Clearstream/T2S** — market infrastructures.
- **Worldline/equensWorldline** — legacy/residual.

**Concentration risk from single-platform payments (ANALYTICAL INFERENCE):** Consolidating 11bn transactions onto one ZV ON€ platform creates a single point of failure for a large share of German retail payments. DZ BANK's own project lead acknowledged: *"Bei einem Problem im Rahmen der Migration des SEPA-ZV hätte der Zahlungsverkehr in ganz Europa zum Stillstand kommen können."* The mitigation is the platform's design for high availability and the deliberately "geräuschlos" (noiseless) migration, but the structural concentration is real and rising.

**Operational-risk framework:** Managed within the group risk architecture (Pillar 1 op-risk capital under CRR; op-risk is a named risk type in the group risk report). R+V carries op-risk under Solvency II SCR.

**Published incidents:** No major public outage of DZ BANK's own ZV ON€ platform has been reported (the migration was completed without material public disruption). See III.12 for the sector's Atruvia incident record.

---

#### III.12 Reliability Engineering and Failure Paths

**Why reliability requirements exceed ordinary enterprise IT:** A clearing failure at DZ BANK would halt payments for a large share of German retail banking (target ~one-third of German traffic). This is systemic infrastructure, not a single bank's back office.

**Availability/SLOs:** DZ BANK does not publish formal SLOs. The design intent is 24/7/365 for instant payments (IPR mandate: settle within 10 seconds). TeamBank describes easyCredit-Ratenkauf as a "hochverfügbares System." Beyond this, published SLOs are UNKNOWN.

**Batch/settlement window as constraint (ANALYTICAL INFERENCE):** Bulk SEPA still runs on batch cycles into the Bundesbank EMZ/SEPA-Clearer with defined cut-offs; instant payments run real-time on TIPS/RT1. The coexistence of batch (legacy mainframe "booking machine") and real-time rails is the core reliability-engineering constraint. Year-end/long-weekend "frozen zones" (no changes during accounting close) are standard sector practice.

**Duplicate-payment prevention:** A named risk during instant/real-time processing; consumer guidance during the July 2026 Atruvia outage explicitly warned users not to re-submit transfers to avoid duplicates — illustrating the failure mode.

**The Atruvia incident record (CONFIRMED FACT) — the relevant contrast:**
- **November 2023:** A central Atruvia software fault caused online-banking/app disruption; per Handelsblatt, *"Potenziell seien bis zu 520 Geldhäuser betroffen … Insgesamt gibt es gut 700 Genossenschaftsbanken, für die Atruvia IT-Dienstleistungen erbringt"* — Volks- und Raiffeisenbanken in southern Germany, with customers unable to make transfers and account information returning error codes.
- **21 July 2026:** Another central-systems fault; per Netzwelt (updated 21 July 2026, 15:28), app and online banking were temporarily shut down to relieve systems and *"waren zwischen 9:47 Uhr und 10:38 Uhr auch die Websites der betroffenen Banken nicht erreichbar"*, with roughly 490 banks affected and the root cause in Atruvia's central systems.

**Assessment — does DZ BANK's ZV ON€ carry comparable concentration risk? (ANALYTICAL INFERENCE):** *Different layer, similar systemic shape.* Atruvia's outages hit the **channel/core** layer (customers can't see or initiate), but payments already submitted still clear. A ZV ON€ failure would hit the **clearing/settlement** layer — potentially more systemic, because it would stop settlement across banks, not just one bank's channel. The two are complementary single-points-of-failure in the cooperative sector: Atruvia = channel/core concentration; DZ BANK ZV ON€ = clearing concentration. Both are consequences of the sector's centralise-for-scale logic. DZ BANK's clean migration record is reassuring, but the tail risk is larger than Atruvia's channel outages.

---

#### III.13 Employee Architecture

| Entity | Headcount | Location(s) |
|---|---|---|
| DZ BANK AG / CICB | ~5,981 avg (CICB segment) | Frankfurt HQ + 12 domestic branches; NY, HK, Singapore, London, etc. |
| **R+V** | **more than 18,400** | Wiesbaden (HQ) + Außendienst nationwide |
| Union Investment | ~4,400 | Frankfurt; Luxembourg; Quoniam (Frankfurt) |
| BSH | ~6,700 (of which ~3,200–3,300 field, ~3,300 office) | Schwäbisch Hall |
| DZ HYP | (mid-size; not separately headlined) | Hamburg + Münster (dual HQ) |
| DZ PRIVATBANK | more than 1,200 across 8 sites | Luxembourg, Zurich, Stuttgart + German locations |
| TeamBank | (mid-size) | Nuremberg; Vienna (Austria) |
| VR Smart Finanz | (small) | Eschborn |
| VR Payment | ~248 | Ilvesheim/Frankfurt |
| **Group total (2024, company/Wikipedia)** | **~33,837** | — |

(CONFIRMED FACT where sourced; note the order-of-magnitude point: R+V alone is more than half the group headcount, so "group employees" (~34k) and "DZ BANK AG employees" (~6k) must never be conflated.)

**Skills position (CONFIRMED FACT):** DZ BANK runs dual-study IT pipelines (Fachinformatik, Wirtschaftsinformatik, Softwaretechnologie) and markets SAP/S4HANA, cloud, Murex and agile skills. R+V and Union Investment compete for actuarial and quant/IT talent respectively. IT and actuarial talent are the constrained skills (ANALYTICAL INFERENCE from job-ad volume and the R+V/UMH efficiency programmes).

**Co-determination (ANALYTICAL INFERENCE):** As large German AGs, DZ BANK AG, R+V and the major subsidiaries operate under the Mitbestimmungsgesetz 1976 (parity supervisory boards) with active works councils; Johannes Koch is Arbeitsdirektor at DZ BANK (established Vol I). The Verdi warning-strike at equensWorldline illustrates the sector's active labour relations.

---

#### III.14 Organisational Design and Decision Rights

**Holding relationship & board interlock (CONFIRMED FACT, Vol I):** DZ BANK Vorstand members chair the subsidiary supervisory boards — **Riese chairs BSH, R+V, TeamBank, Union Investment; Koch chairs DZ HYP, DZ PRIVATBANK, VR Smart Finanz**. This is the primary mechanism of group control over legally autonomous, separately regulated subsidiaries.

**The four strategic business fields vs legal entities:** The four fields — Privatkundengeschäft, Firmenkundengeschäft, Kapitalmarktgeschäft, Transaction Banking — are *market-facing constructs* that cut across legal entities. Transaction Banking (Dr Imke Jacob) maps mostly to DZ BANK AG + VR Payment; Privatkundengeschäft spans BSH, Union Investment retail, TeamBank, R+V retail and DZ PRIVATBANK; Kapitalmarktgeschäft is DZ BANK AG. The matrix (business field × legal entity × supervisory regime) is the group's core organisational complexity.

**Where real operational power sits (ANALYTICAL INFERENCE):** Formal power sits with each subsidiary's own board (each is separately licensed and its board bears regulatory responsibility). *Actual* influence sits with the DZ BANK Vorstand via (a) supervisory-board chairs, (b) the group risk-capital allocation (each Steuerungseinheit operates within DZ BANK-allocated risk capital), and (c) group treasury's control of sector liquidity. So subsidiaries are operationally autonomous but capital- and liquidity-dependent on the centre — a classic "loose-tight" federation.

---

#### III.15 Operating Leverage and Cost Architecture

Administrative expenses €4,804m in FY2025; cost/income 49.3% (established).

| Process | Leverage class | Rationale |
|---|---|---|
| Payments processing (ZV ON€) | **Nearly automatic / strongly sublinear** | 7.5bn→11bn transactions on one platform; marginal cost ≈ €0.0025/transaction; adding volume barely adds cost |
| Securities settlement/custody | **Sublinear** | €332bn→€380bn AuC with scale platform; headcount grows far slower than assets |
| Card acquiring/processing | **Sublinear** (→ step-fixed at 2027 migration) | Scale platform; the Atruvia migration is a step-fixed reset |
| Fund administration (Attrax/UI Lux) | **Sublinear** | NAV production scales with automation, not fund count linearly |
| Insurance claims | **Linear → sublinear** (as automation rises) | Claims volume tracks policies; AI/3D-scan pushing toward sublinear |
| Insurance underwriting (life/health) | **Linear/step-fixed** | Actuarial + advisory headcount-bound |
| Credit processing (DZ HYP VR-BaufiComfort) | **Sublinear** | VR-BaufiConnect automates; 24-hour decisions; volume-sensitive |
| Regulatory reporting (conglomerate) | **Disproportionate / step-fixed** | Each new regime/rule adds fixed cost regardless of volume — the "conglomerate tax" |
| IT development | **Step-fixed** | Platform builds (ZV ON€: 100k+ person-days) are lumpy |
| Distribution support (primary banks) | **Sublinear** | Shared Verbund tooling amortised across ~640–700 banks |

**Where duplication/diseconomy lives (ANALYTICAL INFERENCE):** The multi-entity/multi-regime structure forces **parallel control functions** — each regulated entity needs its own risk, compliance, actuarial/finance, audit and DORA/ICT functions, on top of the group functions. The regulatory-reporting factory (triple accounting basis + six regimes) is the clearest *disproportionate* cost: it grows with regulatory complexity, not with revenue. A monoline of the same size would carry one regime and one reporting stack. **Quantification is not publicly disclosed**, but the structural logic is unambiguous: the conglomerate pays a control/reporting premium in exchange for diversification.

---

#### III.16 Operations and Technology as Competitive Advantage

Scoring each on: Proprietary / Hard-to-reproduce / Cost-reducing / Quality-improving / Regulatory-control-improving / Compounds-with-volume.

| Operational asset | Prop. | Hard | Cost↓ | Qual↑ | Reg↑ | Compounds | Verdict |
|---|---|---|---|---|---|---|---|
| **ZV ON€ payments/clearing platform** | ✔ | ✔✔ | ✔✔ | ✔ | ✔ | ✔✔ | **Genuine moat** — proprietary, sector-critical, volume-compounding, now being commercialised |
| Securities/custody scale (3rd-largest DE) | ~ | ✔ | ✔ | ✔ | ✔ | ✔ | Strong scale asset; not unique |
| Insurance underwriting/claims (R+V) | ✔ | ✔ | ✔ | ✔ | ✔ | ~ | Strong but discipline-specific; reproducible by any large insurer |
| Fund-administration scale (UI/Attrax) | ~ | ✔ | ✔ | ✔ | ✔ | ✔ | Scale asset; SimCorp is bought, not proprietary |
| Regulatory-reporting machine | ✔ | ✔✔ | ✗ | ✔ | ✔✔ | ✗ | Hard to reproduce but a *cost*, not a revenue moat — a licence to operate |
| **Cooperative distribution interface** | ✔✔ | ✔✔ | ✔ | ✔ | ~ | ✔ | **Structural moat** — ~640–700 banks, ~30m customers, near-captive; but channel controlled by Atruvia |

**Comparison with the Sparkassen equivalent (CONFIRMED FACT / ANALYTICAL INFERENCE):** The two three-tier sectors are near-mirrors: BVR↔DSGV; DZ BANK↔Landesbanken; Atruvia↔**Finanz Informatik (FI)**; Union Investment↔**DekaBank**. Differences that sharpen the analysis:
- **IT utility:** FI (Sparkassen) runs on OSPlus; Atruvia on agree21/bank21 — both single-core utilities serving hundreds of institutions. Comparable concentration.
- **Payments/cards:** The Sparkassen have the Deutscher Sparkassenverlag/S-Payment and, from 2024, merged Bayern Card Services + PLuscard into **"Qards"** — a card-processing heavyweight. The cooperative side has *no direct equivalent* to the DSV; the 2027 Atruvia card consolidation is partly a catch-up to Qards.
- **Central institution:** The Sparkassen have *multiple* Landesbanken (fragmented); the cooperatives have *one* DZ BANK (consolidated since the 2016 WGZ merger) — a structural efficiency advantage for the cooperatives at the central-institution layer.
- **Asset management:** Union Investment (€534.7bn) vs DekaBank — comparable scale; both sector-captive distribution.

**The DZ BANK payments platform: genuine competitive asset or merely necessary infrastructure? (ANALYTICAL CONCLUSION):** *Both, but tipping toward asset.* It is necessary infrastructure (someone must clear the sector's payments). But the deliberate insourcing decision, the plan to sell processing to banks outside the sector, the on-time IPR compliance when only ~13% of European banks had a strong instant-payments technology foundation, and the ~€3bn of the primary banks' ~€6.5bn commission income that payments now generates, together make it a genuine, hard-to-reproduce, volume-compounding asset — provided DZ BANK can actually win external clients (unproven; COMPANY CLAIM/aspiration, not yet demonstrated at scale).

---

#### III.17 Volume III Reconstruction

**(1) Federated Operating-Model Diagram** — see III.1.

**(2) Payments & Clearing Architecture:**
```
Primary banks (agree21/Atruvia) ──files──▶ DZ BANK ZV ON€ platform ──▶ rails:
   • Bundesbank SEPA-Clearer/EMZ (bulk SCT/SDD)
   • EBA CLEARING STEP2 (bulk) / RT1 (instant)
   • TIPS (instant settlement, central-bank money)
   • T2/TARGET2 (high-value/settlement)
   • Visa/Mastercard (cards; issuing-processing → Atruvia 2027)
   • SWIFT (cross-border)
Custody: DZ BANK depositary ──▶ Clearstream/T2S
```

**(3) Treasury/Liquidity Map:** Primary banks' surplus deposits ▶ DZ BANK Konzern-Treasury (Liquiditätsausgleich) ▶ money/capital markets + Eurosystem; DZ HYP Pfandbrief funding; own issuance to institutionals. Collateral on Murex MX.3 (~1,400 calls/day, >5,400 agreements).

**(4) Technology Architecture by entity** — see III.4 table.

**(5) Build/Buy/Outsource + Atruvia boundary** — see III.5 table.

**(6) Insurance Ops Map** — R+V: >13,000 bank branches + Außendienst ▶ underwriting ▶ claims (AI/3D-scan) ▶ investment ops + R+V Re reinsurance ▶ Solvency II/SFCR/ORSA.

**(7) Asset-Mgmt Ops Map** — SimCorp front-to-back ▶ UI Lux/Attrax fund admin/NAV/TA ▶ DZ BANK depositary ▶ SFDR ESG data pipelines.

**(8) Credit/Real-Estate Ops Map** — DZ HYP VR-BaufiConnect (advice at primary bank, processing at DZ HYP); BSH SAP S/4HANA + Baufinex; TeamBank easyCredit APIs.

**(9) Risk/Finance/Reg-Reporting Architecture** — FKAG conglomerate coverage (Reg 342/2014 + Art 49(1) CRR); triple consolidation (IFRS/HGB/Solvency II); six-regime reporting factory.

**(10) Data Governance Model** — fragmented controllership; primary banks own customer; Truuco JV signal-sharing; no group flywheel.

**(11) Security/Resilience Map** — DORA across regimes; CTPs led by Atruvia, SAP, Murex, IBM, ERI, hyperscalers, Bundesbank/EBA CLEARING/Clearstream.

**(12) Incident Record:**

| Date | System | Scope | Cause | Lesson |
|---|---|---|---|---|
| Nov 2023 | Atruvia core/channel | up to 520 of ~700 banks | central software fault | channel concentration |
| 21 Jul 2026 | Atruvia core/channel | ~490 banks (09:47–10:38) | central-systems fault | channel concentration; duplicate-payment risk |
| End-2024 | DZ BANK ZV ON€ migration | >600 banks migrated | (planned) | clean cutover, no material outage |
| (ongoing) | equensWorldline | Verdi warning strikes | labour | legacy vendor instability |

**(13) Employee & Entity Map** — see III.13.

**(14) Decision-Rights Map** — supervisory-board interlock + risk-capital allocation + treasury control = loose-tight federation.

**(15) Operating-Leverage Matrix** — see III.15.

**(16) Operations Moat Assessment** — see III.16.

**(17) Key Unknowns:**
- DZ PRIVATBANK's specific fund-admin/NAV/transfer-agency software product (UNKNOWN — not published; only OLYMPIC/OLYNEXT core confirmed).
- DZ BANK's formal availability SLOs and DR/RTO/RPO targets (UNKNOWN).
- The precise SCT/SDD/instant/card/high-value split of the 11.0bn (UNKNOWN — only card sub-count published).
- Whether Cofinpro (vs the confirmed Capco) had a role in ZV ON€ (UNKNOWN).
- The two named hyperscalers DZ BANK uses (UNKNOWN — described only as "two of the big hyperscalers").
- Quantified cost of the conglomerate/multi-regime duplication (UNKNOWN — not disclosed).
- VR Smart Finanz technology stack (thin/UNKNOWN).

**(18) Ten Most Important Conclusions:**
1. Two systems truly span the group — ZV ON€ payments and the FKAG risk/finance spine; everything else is entity-local.
2. DZ BANK AG runs its *own* SAP S/4HANA core + Murex + ZV ON€ — it is NOT an Atruvia customer for its own systems; Atruvia serves the primary banks.
3. Payments is the most systemically critical operation and a genuine, hard-to-reproduce, volume-compounding asset — the group bet against the outsourcing trend and won on resilience (on-time IPR while only ~13% of European banks had a strong instant-payments tech base).
4. The group is becoming *more* dependent on Atruvia (channels + core + cards from 2027), an entity it owns ~0.35% of — the biggest third-party-dependency question.
5. The conglomerate must consolidate under three accounting bases (IFRS/HGB/Solvency II) and report to six regimes — a disproportionate, volume-insensitive "conglomerate tax."
6. R+V is the largest earnings contributor and a wholly different operational discipline (incl. a real reinsurance operation); its 2025 board restructuring signals efficiency pressure.
7. The cooperative model structurally prevents a single group data flywheel — the primary banks own the customer; Truuco is a federated work-around.
8. Operating leverage is excellent in payments/custody/fund-admin (sublinear) but poor in regulatory reporting (disproportionate) and headcount-bound in insurance underwriting.
9. The Sparkassen mirror (FI/Deka/Qards) shows the cooperatives are ahead at the *central-institution* layer (one DZ BANK vs many Landesbanken) but were behind in *card processing* until the 2027 Atruvia consolidation.
10. A federated group under six regimes **cannot** match a single integrated institution's operational efficiency — the structure costs a permanent control/reporting premium and forgoes a unified data asset; it buys diversification, a near-captive channel, and per-platform scale in exchange.

**Answers to the closing questions:**
- **Most critical subsystem to the group and to German banking:** the ZV ON€ payments/clearing platform (systemic for a large share of German payments) — with the FKAG risk spine most critical to the *group's* licence to operate.
- **Hardest to replicate:** the cooperative distribution interface + the ZV ON€ clearing role (both structural, decades in the making).
- **Scales best:** payments, custody and fund administration (sublinear/near-automatic). **Requires headcount to keep growing:** insurance underwriting/claims and regulatory reporting.
- **Most dependent on third parties/institutions:** Atruvia (channels/core/cards), then SAP, Murex, ERI, IBM, SimCorp and the market infrastructures (Bundesbank, EBA CLEARING, Clearstream).
- **Does federation create advantage or duplication:** both — advantage via diversification, per-platform scale and near-captive distribution; duplication via parallel control/reporting functions across six regimes.
- **Payments platform — asset or infrastructure:** necessary infrastructure that has been engineered into a genuine competitive asset, contingent on winning external clients.
- **Central question — can a federated group under six regimes match a single integrated institution's efficiency:** **No.** It carries a permanent structural premium (triple accounting basis, six-regime reporting factory, duplicated control functions, no unified data asset). What that structure *costs* is a control/reporting/coordination overhead that a monoline avoids; what it *buys* is earnings diversification (R+V's €2.1bn cushioning bank-cycle troughs), a near-captive ~30m-customer channel, and scale platforms (payments, custody, funds) each run at sector scale. The 49.3% cost/income ratio shows the trade is being managed well — but the conglomerate tax is real and permanent.

---

### Recommendations

**For an analyst/counterparty assessing the group:**
1. **Treat ZV ON€ concentration as the top operational-risk item.** Benchmark: any published ZV ON€ outage affecting settlement (not just channel) would be a materially worse signal than an Atruvia channel outage. Watch for DZ BANK disclosing formal availability SLOs or a DR site — continued absence is a (mild) red flag.
2. **Track the 1 January 2027 Atruvia card-processing cutover as a discrete event risk.** Benchmark: a clean cutover (as with ZV ON€ in 2024) confirms the sector's migration competence; any disruption to credit-card processing would be systemic given Atruvia processes "a significant portion of all German credit-card transactions." Re-rate operational risk if the cutover slips or fails.
3. **Model the conglomerate-reporting cost as a permanent fixed overhead**, not a variable cost — it will rise with each new regime (DORA, CRR III phase-ins, Solvency II review) regardless of revenue. Benchmark: cost/income drifting above ~52–53% without a revenue explanation would suggest the regulatory/control base is outpacing operating leverage.
4. **Monitor whether DZ BANK wins external (non-cooperative) payments clients.** This is the swing factor that converts ZV ON€ from "necessary cost" to "growth asset." Benchmark: named external bank clients on ZV ON€ would validate the "payment provider for banks outside the sector" thesis (currently aspiration).

**For the group itself (implied by the analysis):**
5. Reduce Atruvia single-point-of-failure exposure at the channel layer (the 2023/2026 outages are a pattern, not one-offs) — but this is largely outside DZ BANK's control given ~0.35% ownership; the lever is governance influence and the Truuco data layer.
6. Publish more operational transparency (SLOs, DR posture, the payments split) — the current opacity forces analysts to infer, which understates a genuinely strong payments operation.

**Thresholds that would change these recommendations:** a ZV ON€ settlement-layer outage; a failed/delayed 2027 card cutover; cost/income breaching ~53%; or, positively, the signing of named external ZV ON€ clients or the publication of formal resilience SLOs.

---

### Caveats

- **Evidence asymmetry:** As warned, DZ BANK publishes far less about internals than a fintech would. The richest technology evidence came from job advertisements (DZ BANK IT careers: EAI, Automic, Apptio, SAP S/4HANA, hyperscalers; DZ PRIVATBANK: OLYMPIC/OLYNEXT on IBM i), vendor case studies (Murex MX.3; SimCorp/Quoniam; Wavestone/paricon for BSH SAP; Capco for ZV ON€) and specialist press. These are reliable but not audited disclosures.
- **The payments split (SCT/SDD/instant/card/high-value) is inferred, not published** — only the card sub-count is disclosed.
- **"ZV ON€" is confirmed as an in-house build; no underlying commercial payments engine is named** — do not attribute a specific vendor product to it. Capco is confirmed as integration partner (scope April 2019–end-2024, 97 go-live events, >600 banks migrated); Cofinpro's involvement is unconfirmed.
- **DZ PRIVATBANK's fund-administration/NAV/transfer-agency software product is UNKNOWN** — only the OLYMPIC/OLYNEXT core-banking system (ERI Bancaire, on IBM Power/i) is confirmed, from the bank's own IT recruitment postings.
- **The Signa write-off characterisation was mis-attributed in the carried-forward context.** R+V CEO Rollinger's own 3 April 2024 statement was that the Signa engagement was fully processed in the 2023 accounts; the phrase "robuster dreistelliger Millionenbetrag" traces to DZ BANK Co-CEO Cornelius Riese, not Rollinger. Both confirm a full write-off in FY2023.
- **Headcount figures mix reporting bases** (segment averages vs entity totals vs group). The ~33,837 group figure (2024) and R+V's more-than-18,400 are from company/Wikipedia sources; treat the group total as approximate and never conflate perimeters (DZ BANK AG ~6k vs group ~34k).
- **Forward-looking items** (2027 card migration, external ZV ON€ client ambitions, "NextLevel"/"Fit for Future" savings targets) are plans/claims, not accomplished facts, and are labelled as such.
- **Perimeter discipline:** figures are for the DZ BANK Group (IFRS) or the named entity; the ~€1.175trn Genossenschaftliche FinanzGruppe aggregate is the *sector*, NOT DZ BANK; the CRR prudential scope excludes insurance; and the erroneous "DZ BANK holds ~20% of Atruvia" claim must not be propagated (it holds ~0.35%; the ~20% figure refers to Verimi).

---

*End of Volume III. Work paused at a logical boundary; Volume IV (economics, capital, profitability, strategy) not begun, per scope.*


---

# Part IV — Financial Statements, The Three Economic Engines, Unit Economics & Capital

### TL;DR
- The DZ BANK Group's real economic engine in FY2025 was **insurance** (R+V, €2,144m segment pre-tax, ~50% of group) and **asset management** (Union Investment, €1,185m, ~28%) — together ~78% of a €4,282m pre-tax result — **not** the eponymous bank; but roughly €1.0–1.3bn of that result was a non-repeating low-claims/market windfall, which is exactly why management guides FY2026 down to **around €3.0bn** (CEO Cornelius Riese: "we are unlikely to see a repetition of the one-off items that had a positive effect in 2025, particularly in the insurance segment … we anticipate a profit before taxes for 2026 of around €3.0 billion").
- The group runs three incompatible capital regimes that do not reconcile to one number: CRR/CRD (CET1 18.4%, RWA €148.6bn, banking only), Solvency II (R+V own funds €17.05bn / SCR €8.37bn = 203.8% preliminary end-2025), and the FKAG conglomerate coverage (136.1% end-2024, €37.45bn own funds / €27.52bn requirements) that arithmetically sums the two and gives no diversification credit.
- Conventional ROE/valuation is category-inappropriate: DZ BANK is unlisted, 94.8% cooperatively owned, and runs a Förderauftrag. The owner-banks extract value mainly through distribution commissions and subsidised Verbund services, not the €448m dividend (15.6% payout). CET1 far above requirements reflects the conglomerate deduction logic and cooperative prudence, not productive over-capitalisation.

### Key Findings

1. **FY2025 group pre-tax profit was €4,282m (net €2,880m), up 29.6%** — but the headline masks three moving parts pulling in opposite directions. Net interest income fell 17.8% to €3,839m while the trading result swung from −€842m to +€281m; these are two halves of the same accounting artefact (2024 NII was inflated by valuation effects with a countervailing trading loss). Net income from insurance rose 76.5% to €2,024m on an exceptionally benign claims year.

2. **The three engines are genuinely incompatible machines.** Banking (CICB, DZ HYP, BSH, DZ PRIVATBANK, TeamBank, VR Smart Finanz) is measured in NII, fees and RWA; insurance (R+V) in premiums, combined ratio and the IFRS 17 contractual service margin (R+V's "Vertragliche Servicemarge"/VSM, €6.68bn at YE2025); asset management (Union Investment, €534.6bn AuM) in basis-point margin (~45.7bps). No single revenue narrative can hold all three.

3. **Insurance is the highest-quality-in-scale but most cyclical engine.** R+V's segment pre-tax of €2,144m (group perimeter) / €2,221m (R+V's own IFRS group) rode a P&C combined ratio that fell from 94.9% to 86.6% and a reinsurance combined ratio from 82.5% to 58.9% — a once-in-several-years low-claims outcome. The investment result actually fell (Kapitalanlageergebnis −54.5% to €2,368m), so the profit surge is underwriting-driven, not investment-driven, and not an IFRS 17 presentation illusion.

4. **Asset management is the highest-quality recurring engine.** Union Investment earned €1,185m pre-tax on €534.6bn AuM at a ~53% cost/income ratio — essentially an annuity on the primary banks' distribution reach — but its margin is thin (~45.7bps of AuM) and market-dependent.

5. **The banking engine is the lowest-return, highest-capital-intensity engine** and exists substantially to serve the Förderauftrag: it consumes essentially all of the group's €148.6bn RWA, produced CICB pre-tax of €864m, and carries two structural loss-makers (TeamBank −€29m, VR Smart Finanz −€28m).

6. **Capital cannot be expressed as one number.** CET1 18.4% (banking, up from 15.8% mainly on CRR III lowering RWA); R+V SCR 203.8%; conglomerate 136.1%. The conglomerate ratio sits far below the banking CET1 headroom because it sums two full requirement stacks and strips diversification.

7. **The FY2026 ~€3.0bn guidance is realistic-to-slightly-conservative**, implying ~€1.3bn of non-repeating 2025 result — overwhelmingly the R+V low-claims windfall plus normalising loss allowances and trading.

### Details

#### IV.1 Multi-Year Financial History

**Perimeter warning.** Four perimeters recur below and must never be blended: **(1) DZ BANK AG** (HGB parent); **(2) DZ BANK Group/Konzern** (IFRS, ~€661bn); **(3) Genossenschaftliche FinanzGruppe** (the whole sector — €1.68trn total assets and, per BVR President Marija Kolak on 15 July 2026, a consolidated pre-tax profit of €11.6bn in 2025, €7.4bn net after €4.2bn income taxes, cost/income 58.3% — this is NOT DZ BANK and is the most commonly misquoted figure); **(4) bankenaufsichtlicher Konsolidierungskreis** (CRR scope, RWA €148.6bn, EXCLUDES insurance). A fifth, the **Solvency II group** for R+V, is used only in IV.5/IV.12.

**Table 1 — DZ BANK Group (IFRS), €m [CONFIRMED, company disclosure, preliminary FY2025]**

| Line | FY2024 | FY2025 | Δ% |
|---|---|---|---|
| Net interest income | 4,670 | 3,839 | −17.8 |
| Net fee & commission income | 3,191 | 3,370 | +5.6 |
| Trading result | −842 | 281 | >100 |
| Gains/losses on investments | 65 | 105 | +61.5 |
| Other valuation result (fin. instr.) | 229 | −127 | >100 |
| Result from derecognition (AC) | 40 | 28 | −30.0 |
| Net income from insurance business | 1,147 | 2,024 | +76.5 |
| Loss allowances | −845 | −653 | −22.7 |
| Administrative expenses | −4,552 | −4,804 | +5.5 |
| Other operating result | 200 | 219 | +9.5 |
| **Profit before taxes** | **3,303** | **4,282** | **+29.6** |
| Income taxes | −913 | −1,402 | +53.6 |
| **Net profit** | **2,390** | **2,880** | **+20.5** |
| Total assets (€bn) | ~660 | ~661 (H1 2025: 666) | ~flat |
| CET1 ratio (%) | 15.8 | 18.4 | +2.6pp |
| Leverage ratio (%) | 6.6 | 7.0 | +0.4pp |
| Cost/income ratio (%) | 52.3 | 49.3 | −3.0pp |
| Dividend (€m) | 448 | 448 (proposed) | flat |

Longer-run context [CONFIRMED]: pre-tax profit was €3.2bn (2023) and €3.3bn (2024). The FY2023 introduction of IFRS 17 makes the "net income from insurance business" line non-comparable to any pre-2023 premium-based presentation; pre- and post-2023 insurance figures must never be compared without adjustment.

**Table 2 — DZ BANK AG (HGB parent, standalone), €m [CONFIRMED]**

| Line | FY2024 | FY2025 |
|---|---|---|
| Zinsüberschuss (incl. participation income) | 1,653 | 1,487 |
| Operating income (operative Erträge) | 2,704 | 2,835 |
| Administrative expenses | −1,662 | −1,762 |
| Cost/income ratio (%) | 61.5 | 62.2 |
| Betriebsergebnis vor Risikovorsorge | 1,042 | 1,073* |
| Risikovorsorge | n/a | −106 |
| Betriebsergebnis | 519 | 967 |

*derived (2,835 − 1,762 = 1,073). The AG's cost/income ratio (62.2%) is far worse than the group's (49.3%) — because the AG carries the central-institution and holding cost base without the high-margin insurance and asset-management subsidiaries. This is the clearest single demonstration that the "bank" and the "group" are different economic objects.

#### IV.2 The Three Economic Engines

**Engine 1 — Banking.** Segments and FY2025 pre-tax: CICB (Verbund- und Geschäftsbank) €864m; DZ HYP €338m; BSH €122m; DZ PRIVATBANK €106m; TeamBank −€29m; VR Smart Finanz −€28m. Aggregate banking pre-tax ≈ €1,373m before the holding function (−€335m) and consolidation (−€85m). Revenue drivers: net interest income (deposit-taking from owner-banks, lending to corporates), fees (transaction banking, capital markets), trading. Capital: this engine consumes essentially all of the group's €148.6bn RWA. Cyclicality: moderate; highly sensitive to the rate cycle and to corporate credit.

**Why NII fell 17.8%.** The €831m fall in NII (€4,670m→€3,839m) is largely mirrored by the €1,123m improvement in trading (−€842m→+€281m). DZ BANK states plainly that 2024 NII was "unusually high due to accounting-related effects that had a positive impact on net interest income but a countervailing negative impact on gains and losses on trading activities" [COMPANY CLAIM, corroborated by the offsetting swings]. ANALYTICAL INFERENCE: the genuine economic decline in NII is far smaller than 17.8%; combined NII+trading rose from €3,828m to €4,120m (+7.6%).

**Engine 2 — Insurance (R+V).** IFRS 17 basis (group segment presentation): insurance service result (versicherungstechnisches Ergebnis) €2,597m (2024: €1,371m); investment & other insurance result €2,368m (2024: €5,210m, −54.5%); insurance finance expense (versicherungstechnisches Finanzergebnis) −€2,853m (2024: −€5,351m). The net income from insurance business line reported at group level was €2,024m; R+V's segment pre-tax €2,144m. Gross written premiums €22.8bn (+9.1%): Leben/Kranken €10.8bn, Schaden/Unfall €8.5bn, assumed reinsurance €3.4bn. R+V's own IFRS group reported €2,221m pre-tax, €1,455m net, 17.9% RoE, €12.4bn equity. The contractual service margin (VSM) rose to €6,680m (2024: €6,035m) — the store of unearned future profit; that it grew means new-business value more than replaced the amortised release (a positive quality signal).

**Engine 3 — Asset management (Union Investment/UMH).** AuM €534.6bn (2024: €504.7bn; 2023: €455.2bn), a record high ("neuer Höchststand"), split retail €270.8bn / institutional €263.8bn. Total net inflows €23.3bn (2024: €17.3bn): retail €13.5bn (second-best in the company's history), institutional €9.8bn (more than doubled from €4.7bn). Fund savings plans surpassed 4 million (6.55m including Riester/VL). Segment revenue is dominated by net commission income of €2,377m. **Basis-point margin (derived):** €2,377m ÷ average AuM ((504.7+534.6)/2 = €519.65bn) = **45.7bps** [ANALYTICAL INFERENCE]. Cost/income: administrative expenses €1,352m ÷ operating income (~€2,536m) = **~53%**. Pre-tax margin ~46.7% of revenue. Performance-related management fees are volatile: in FY2023 UMH's success-fee income was only €12.3m [CONFIRMED, UMH GB2023]. Pre-tax fell 4.5% to €1,185m (2024: €1,241m; 2023: €974m) despite record AuM because 2024 benefited from positive valuation effects (Sonstiges Bewertungsergebnis €85m vs €19m in 2025); CEO Hans Joachim Reinke called it a "robustes Ergebnis."

**Interaction / correlation risk.** The insurance and asset-management engines share one systematic exposure: equity and credit markets. A drawdown simultaneously lowers Union AuM (and thus fee income) and R+V's investment result and Solvency II own funds. This is the group's single most important correlation risk (modelled in IV.19).

#### IV.3 Revenue Architecture and Quality
Recurring, high-quality streams: Union Investment management fees (annuity on €534.6bn AuM); BSH and DZ HYP net interest (spread businesses); R+V premium/underwriting. Market-dependent/lower-quality: trading result, performance fees, investment result within insurance, own-issuance valuation effects. Of the FY2025 €4,282m, ANALYTICAL INFERENCE puts ~€2.9–3.1bn as structural earnings power and ~€1.2–1.4bn as a rate-cycle/low-claims/market windfall — consistent with management's ~€3.0bn FY2026 guide and with Riese's statement that 2025's one-off items, "particularly in the insurance segment," are unlikely to repeat.

#### IV.4 Banking Economics in Detail
CICB: NII €1,487m, fees €691m, trading €452m, loss allowances −€241m (down from −€457m, which had carried BayWa), CIR 58.0%. Corporate loan commitments +8% to €97.4bn; joint/consortium credit (Metakredit) €19.3bn; renewable-energy lending +21% to €9.7bn. DZ HYP: NII €819m, portfolio €57.6bn, loss allowances €105m, but pre-tax fell to €338m because own-issuance valuation effects (Sonstiges Bewertungsergebnis) hit −€138m. BSH: NII €684m (+27.4%), pre-tax €122m (+90.6%), Bauspar new business fell to €17.6bn, market share 33.3%. The Metakredit model: DZ BANK supplies balance sheet and RWA while the primary bank retains the customer relationship — a Förderauftrag mechanism, not a profit-maximising one.

#### IV.5 Insurance Economics in Detail (R+V)
Combined ratios [CONFIRMED, DZ BANK segment disclosure, net EOM basis]: P&C 86.6% (2024: 94.9%); assumed reinsurance 58.9% (2024: 82.5%). On an HGB basis R+V reports motor combined ratio improved to 96% (from 103%). Segment pre-tax by line: Schaden/Unfall €979m (from €407m); Leben/Kranken €452m (from €479m); assumed reinsurance €713m (from €355m). Investments €127bn (IFRS Kapitalanlagen €101.3bn plus €26.8bn unit-linked). Portfolio ~84% FVOCI, debt-heavy (~€90.8bn fixed income); equities ~€5.1bn; investment property €3.5bn. Solvency II (R+V "Versicherungsgruppe", preliminary/unaudited, end-2025): own funds €17,053m, SCR €8,368m, ratio **203.8%** (end-2024 restated to 172.5% from the 168% originally cited); the §352 VAG Rückstellungstransitional now has **zero** effect (revaluation to null at 1 Jan 2024); the volatility adjustment is applied for individual life/health entities. Economic (internal) capital adequacy 335.9% at end-2025. VSM €6,680m; VSM release €378m (life/health) + €254m (reinsurance) + €19m (P&C); risk-adjustment release €70m (life/health) + €48m (reinsurance). Of R+V's €2,144m, the overwhelming majority is underwriting (insurance service result €2,597m) rather than investment, which fell — confirming the profit surge is genuine underwriting, not accounting.

#### IV.6 Asset-Management Economics (Union Investment) with peer benchmark
UMH €1,185m pre-tax on €534.6bn AuM. Margin ~45.7bps; cost/income ~53%. Benchmark [THIRD-PARTY, CONFIRMED]: DWS reported a FY2025 cost-income ratio of **58.0%** (improved 7.6pp vs FY2024; net income €928m, revenues €3,155m) — UMH's ~53% is thus meaningfully more efficient than its largest listed German peer, reflecting the captive Volksbanken distribution which lowers acquisition cost but requires trailer commissions paid to the primary banks (a Verbund cost, discussed in IV.16). Net flow quality is high — ratierliches Sparen (regular savings plans, now >4m contracts) provides sticky retail inflows and Riester leadership.

#### IV.7 Cost Architecture
Group administrative expenses €4,804m (+5.5%), driven by investment in personnel and IT. By segment: UMH €1,352m; CICB €1,526m; holding €213m; DZ PRIVATBANK €320m; BSH €527m; DZ HYP €256m; TeamBank €279m; VR Smart Finanz €82m. Group employees ~33,837 (R+V alone >18,400). Cost per employee (crude, group admin ÷ headcount) ≈ €142,000 — but this blends insurance and bank cost structures and is not a clean unit. The "conglomerate tax" (parallel CRR + Solvency II + FKAG reporting, three audit/accounting bases) is real but not separately quantified by the company — label **UNKNOWN**.

#### IV.8 Unit Economics Across Incompatible Units [ANALYTICAL INFERENCE, arithmetic shown]
- **Per member bank** (~645 institutions): pre-tax €4,282m ÷ 645 = **€6.64m**; net €2,880m ÷ 645 = **€4.47m**.
- **Per euro of AuM** (Union): **45.7bps** revenue margin (€2,377m ÷ €519.65bn average AuM).
- **Per payment transaction** (11.0bn): if VR Payment revenue is ~€200m, ~**1.8 cents** per transaction — a critical figure showing the payments business is a scale/utility play, not a margin play.
- **Per euro of RWA** (€148.6bn, banking only): banking-attributable pre-tax ÷ RWA ≈ **~0.9%** (using ~€1.37bn banking segment pre-tax) — the insurance and AM engines earn outside RWA entirely.
- **Per employee**: net €2,880m ÷ 33,837 = **€85,120**.
- **Governing unit:** none of the conventional bank units governs. **The member bank is the true unit of account** — the group exists to serve ~645 owners; every other metric (per customer, per transaction, per euro RWA) misleads because the group neither owns the 30m+ end customers nor optimises RWA return.

#### IV.9 Segment and Entity Economics — all nine
R+V €2,144m; UMH €1,185m; CICB €864m; DZ HYP €338m; BSH €122m; DZ PRIVATBANK €106m; TeamBank −€29m; VR Smart Finanz −€28m; holding function −€335m; other/consolidation −€85m. The two loss-makers are consumer/SME credit units hit by rising loss allowances in a weak economy (TeamBank risk provision −€233m; VR Smart Finanz −€51m). The holding function −€335m comprises negative NII (−€122m, funding/AT1 costs) and administrative expenses (−€213m) for group-level commercial-law, tax and prudential-supervision functions. These are structurally different businesses; the loss-makers are tolerated because they serve the Förderauftrag (consumer and SME credit reach for the Volksbanken) — a clear case of Förderauftrag cross-subsidy.

#### IV.10 Income Statement Teardown
Effective tax rate **32.7%** (€1,402m ÷ €4,282m) — high, reflecting German corporate + trade tax and non-deductible items. Key accounting judgements: IFRS 17 measurement models (all three used — general measurement model, premium allocation approach, variable fee approach, with usage varying by segment); IFRS 9 ECL staging (loss allowances €653m); fair-value trading; and own-issuance valuation effects that depressed DZ HYP (−€138m) and helped CICB.

#### IV.11 Balance Sheet Teardown
Total assets ~€661bn. Dominant lines: loans to banks (primary-bank placements), loans to customers, insurance investments (~€101bn) and unit-linked assets (~€27bn), the trading portfolio, Pfandbrief-backed lending at DZ HYP, deposits from banks (structural funding core), insurance contract liabilities under IFRS 17 (Deckungsrückstellung €101,089m including the €6,680m VSM), debt certificates including Pfandbriefe, subordinated capital, and equity. Asset encumbrance arises from DZ HYP Pfandbrief issuance and from cover-pool eligibility of claims against sector members.

#### IV.12 The Three Capital Regimes — Reconciliation
(a) **CRR/CRD banking group** [CONFIRMED, Pillar 3]: CET1 18.4% (Q3 2025: 18.10%), Tier 1 20.5%, total 23.6%, leverage 7.0%. Total risk exposure amount (RWA) €148,617m at 30 Sept 2025 (down from €162,563m at end-2024 and €151,425m at H1 2025 — CRR III lowered RWA, the main reason CET1 rose from 15.8% to 18.4%). CET1 capital ~€26,905m. Requirement stack: P2R 1.80% (2026), capital conservation buffer 2.5%, O-SII 1.00% (from 1 Jan 2026), CCyB 0.75%, sectoral SyRB on residential real estate reduced to 1% (from 1 May 2025). MREL 40.8% of RWA (subordinated 34.1%), 13.9% of leverage exposure.
(b) **Solvency II (R+V, preliminary)**: own funds €17,053m, SCR €8,368m, ratio 203.8%.
(c) **FKAG conglomerate** [CONFIRMED, §25(3)/(4) FKAG report]: end-2024 own funds €37,450m ÷ requirements €27,522m = **136.1%** (down from 152.5% end-2023, reduced mainly by the R+V transitional revaluation to zero and higher requirements); H1 2025 rose to 142.2% (own funds +€1,396m, requirements −€204m). External minimum 100%, internal minimum 113%, internal observation threshold 123% (raised from 121%). Computed under Delegated Regulation (EU) 342/2014 with Article 49(1) CRR.
**Why they don't reconcile:** the conglomerate ratio sums a banking requirement (Pillar 1 + buffers on RWA) and an insurance requirement (SCR) and divides into summed own funds, giving no credit for cross-sector diversification. So an 18.4% banking CET1 (huge headroom) coexists with a 136.1% conglomerate ratio (comfortable but not lavish) — because the same capital cannot be counted twice and the deductions bite. **No single "group solvency number" exists; anyone quoting one is conflating perimeters.** The internal 113% threshold implies management runs the conglomerate with a deliberately modest ~23-point buffer to the observation threshold, signalling disciplined but not excessive risk appetite at the whole-group level even as the banking CET1 looks lavish.

#### IV.13 Funding, Liquidity, Rating
Funding core: deposits from the primary banks (structural, cheap, sticky); DZ HYP covered bonds/Pfandbriefe; senior preferred/non-preferred; AT1/T2; central-bank access (incl. $15bn US CP programme, NY Fed access). LCR 156.4%, NSFR 126% — conservative. **Rating drivers:** S&P A+ is anchored on the 'a+' group credit profile of the cooperative sector and its protection scheme (S&P adds no ALAC uplift because sector support is deemed "the strongest support element" and a bail-in "highly unlikely"). Moody's Aa2: DZ BANK's standalone Baseline Credit Assessment is baa2, lifted to an **a3 Adjusted BCA** by "a very high probability of cross-sector support from Genossenschaftliche FinanzGruppe" through the institutional protection scheme — i.e. roughly two notches of the rating derive from scheme membership, not standalone strength [CONFIRMED, Moody's]. This is the single most important qualitative fact about the group's funding cost: the AA-band rating is substantially a sector-solidarity rating, not a standalone one.

#### IV.14 Cash Flow, Dividend, Retention
Dividend €448m (25 cents/share) proposed for FY2025, the third consecutive year at that level (the payout also carries a variable 3-cent component dependent on business performance); payout **15.6%** of €2,880m net. Retention is high because (i) the owner-banks want the central institution strongly capitalised as their risk backstop, (ii) the conglomerate ratio (136.1%) is the binding constraint, not the banking CET1, and (iii) CRR III/Solvency II reviews create prudent capital targets. Retained earnings build conglomerate own funds.

#### IV.15 Capital Allocation
Deployments: organic growth (renewable-energy lending +21% to €9.7bn; corporate credit +8%); the ZV ON€ payments platform (three-digit-million build); depositary-business acquisitions (AuD €380.7bn, third-largest in Germany); the disposal of VR Payment's issuing-processing to Atruvia effective 1 Jan 2027; support for loss-making TeamBank/VR Smart Finanz; and high retention. Discipline is evident (exiting sub-scale payments processing, consolidating depositary, participation in Wallee) but returns on the payments build are not yet separately disclosed — **UNKNOWN**. Note: DZ BANK holds ~0.35% of Atruvia (the ~20% figure that circulates refers to Verimi).

#### IV.16 Return to Whom, and For What Purpose
Nominal group RoE for reference: net €2,880m ÷ equity (~€28–29bn) ≈ **~10%** [ANALYTICAL INFERENCE] — respectable but not the governing metric. The economic value to owner-banks flows in several forms: (1) the **€448m dividend** (small); (2) **distribution commissions** paid by the group's product factories to the primary banks for selling funds, insurance and Bauspar — Verbund commission income was €2.8bn in 2021 (last year BVR published that specific line), within total primary-bank net commission income that reached €9.5bn (BVR consolidated 2024); (3) **subsidised/cost-based central services** (payments, custody, liquidity); (4) **risk capacity** via Metakredit (€19.3bn); (5) **protection-scheme membership** underpinning every member's rating. On the central question — is CET1 18.4% over-capitalisation? — the answer is **no, it is not productively deployable "excess"**: the binding constraint is the 136.1% conglomerate ratio, and cooperative owners rationally prefer a fortress balance sheet at their central institution to a higher dividend. The owner-banks are better off with the current low-price/high-service/high-retention model than with a higher payout; the true "return" is the competitiveness the Verbund confers on 645 local banks, not a per-share yield.

#### IV.17 One Euro of Group Revenue [ANALYTICAL INFERENCE]
Because the three engines have fundamentally different shapes, a single group waterfall misleads and is therefore presented separately. For the **bank**, of €1 of income: ~€0.49–0.58 admin cost (group CIR 49.3%; AG 62.2%), a material slice to loss allowances, then tax and residual retention. For the **asset manager**: ~€0.53 cost, negligible loss allowance, ~€0.47 pre-tax margin. For the **insurer**: the dominant outflow is insurance service expenses/claims, and the CSM/VSM defers profit to future periods rather than releasing it with the premium. These three euros cannot be meaningfully summed.

#### IV.18 Economic Driver Tree — the variables that matter most
1. **R+V combined ratio** (nat-cat/claims frequency) — the single largest swing factor in 2025 (P&C 94.9%→86.6%, reinsurance 82.5%→58.9%).
2. **Equity/credit market level** — drives both Union AuM fees and R+V's investment result and Solvency II own funds (correlated).
3. **Union Investment AuM × ~45.7bps margin.**
4. **The rate cycle / deposit beta** on primary-bank placements (NII).
5. **Corporate credit losses** (BayWa-type single names).
6. **Own-issuance IFRS valuation effects** (DZ HYP/CICB noise).
7. **Loss-allowance level** (€653m vs €845m).
8. **Member-bank count** (~645, consolidating) — the ultimate demand base.

#### IV.19 Scenario and Sensitivity Analysis [ANALYTICAL INFERENCE / HYPOTHESIS]
- **Rate normalisation** (further NII compression): modest, ~€100–200m pre-tax drag, partly offset by trading normalisation.
- **Equity drawdown (the key correlation risk):** a 20% equity fall could cut Union fee revenue by ~€150–250m annualised AND simultaneously reduce R+V's investment result and Solvency II own funds — plausibly €500m-plus combined pre-tax, and a Solvency II ratio move of tens of points.
- **German CRE deterioration (DZ HYP):** loss allowances could multiply from €105m; pre-tax €338m is exposed.
- **BayWa-scale single name:** ~€450m loss-provision precedent; directly reduces CICB pre-tax.
- **Nat-cat year at R+V:** reverses the 2025 windfall — a combined ratio back to the mid-90s would remove ~€600–900m of the 2025 uplift. **This is the core of the FY2026 guide-down.**
- **Accelerated primary-bank consolidation:** shrinks the owner base but not necessarily Verbund volume (mergers consolidate rather than eliminate customers).
- **Capital-regime shock:** a further R+V transitional recalculation or a Solvency II review would hit the conglomerate ratio (136.1%) faster than the banking CET1.

#### IV.20 Profitability Decomposition and Normalisation [ANALYTICAL INFERENCE]
FY2025 €4,282m ≈ structural ~€2.9–3.1bn + R+V low-claims windfall ~€0.7–0.9bn + trading/market recovery ~€0.2–0.3bn + below-normal loss allowances ~€0.2bn. Normalised full-cycle group pre-tax ≈ **€3.0–3.3bn**, reconciling closely with management's ~€3.0bn FY2026 guide. The guide is realistic and arguably mildly conservative if markets hold and claims normalise only partway.

### Volume IV Reconstruction — Answers to the Central Questions
- **What is the real economic engine?** The **member bank relationship monetised through three product factories** — insurance and asset management (78% of profit) are the earnings engines, banking is the Förderauftrag utility. The "bank" is the smallest profit contributor relative to its capital and cost.
- **Highest quality / most fragile engine?** Highest recurring quality: **Union Investment** (sticky retail AuM, ~53% CIR, thin but durable margin). Most fragile/cyclical: **R+V underwriting**, whose 2025 result depended on an exceptionally benign claims year that will not repeat.
- **How much of FY2025 is structural?** ~€2.9–3.1bn of €4,282m; ~€1.2–1.4bn was windfall.
- **Why guide FY2026 down ~€1.3bn?** Because the R+V low-claims windfall, subdued loss allowances and trading recovery all normalise.
- **Over-capitalised?** No in economic terms: the binding constraint is the conglomerate ratio (136.1%), not the banking CET1 (18.4%); cooperative owners want the fortress.
- **What does an owner-bank receive, and is it adequate?** ~€6.64m of pre-tax profit attribution plus distribution commissions, cost-based services, risk capacity and scheme protection. Adequate for a Förderauftrag institution — the return is competitiveness, not yield.
- **Single most determinative variable:** the **R+V combined ratio**, closely followed by equity-market level (the correlated hit to both R+V and Union).
- **The central question — can a group be a bank, insurer and asset manager under three capital regimes without comparable capital or earnings to any single-regime peer, and what is that worth to its owners?** Yes it can, and DZ BANK is the proof: no single capital number or peer multiple describes it, which is precisely why it is unlisted and why ROE is category-inappropriate. Its worth to the owners is **not a valuation but a function** — a diversified, protection-scheme-backstopped, cost-efficient central utility that lets 645 small cooperative banks offer full-service finance they could never build alone. The diversification that defeats single-regime comparison is exactly the source of the value.

### Recommendations
1. **Analyse the group as a holding company owning three regulated monoline-equivalents, never as a bank.** Value/assess R+V on Solvency II + IFRS 17 CSM, Union Investment on AuM × bps (benchmark ~45.7bps and ~53% CIR against DWS's 58.0%), and only the banking stub on RWA return. Blending produces nonsense.
2. **Treat the FY2026 ~€3.0bn guide as the normalised anchor, not the €4.28bn print.** A repeat above €3.5bn would require another benign claims year — if R+V's combined ratio stays below ~90%, revise upward; if a nat-cat pushes it above ~97%, the guide is at risk.
3. **Watch the conglomerate coverage ratio (136.1% end-2024 → 142.2% H1 2025), not the CET1 headline, as the binding capital constraint.** A move toward the 123% observation threshold — most likely via a Solvency II shock at R+V or a further transitional revaluation — is the real capital risk. CET1 at 18.4% is not spendable "excess."
4. **Monitor the single correlation risk — a simultaneous equity/credit drawdown — above all idiosyncratic risks.** It is the only event that hits two of the three engines at once.
5. **For the owner-banks: the current low-price/high-retention model is defensible.** Pressing for a materially higher dividend would weaken the central institution they rely on as a risk backstop; the greater value lever is continued distribution-commission flow and cost-based services, not the €448m dividend.

### Caveats
- FY2025 group figures are on a **preliminary basis** (Bilanzpressekonferenz 3 March 2026); the audited annual report was scheduled for 31 March 2026.
- R+V Solvency II figures (own funds €17,053m, SCR €8,368m, 203.8%) are **explicitly preliminary and unaudited** and may be revised after a scheduled Q2 2026 recalculation; the end-2024 ratio was restated from 168% to 172.5%. The regulatory "R+V Versicherung AG Versicherungsgruppe" (Solvency II) perimeter differs slightly from the IFRS "R+V Konzern" consolidation perimeter, which is why R+V's own IFRS group pre-tax (€2,221m) differs from the DZ BANK segment figure (€2,144m).
- The FKAG conglomerate coverage of 136.1% is the **end-2024** figure (H1 2025: 142.2%); the end-2025 conglomerate ratio was not yet published at the time of writing — **UNKNOWN**.
- Basis-point margins, cost/income ratios, unit-economics and normalisation splits are **ANALYTICAL INFERENCE** with arithmetic shown; per-product margins, internal transfer pricing, the precise VR Payment revenue-per-transaction, the "conglomerate tax," the ZV ON€ return, the ZZR position (an HGB single-entity concept not disclosed in R+V's IFRS group report), and the fully itemised CSM/VSM roll-forward (new-business vs interest-accretion split) and risk-adjustment closing balance remain **UNKNOWN**.
- Sector context (Genossenschaftliche FinanzGruppe: €11.6bn pre-tax, €1.68trn assets, 2025) must never be confused with the DZ BANK Group (€4,282m pre-tax, €661bn assets). Work paused at the completion of Volume IV; Volume V not begun.


---

# Part V — Management, Culture, Competition, Moat, Risk & Strategic Evolution

*Institutional-grade forensic reverse-engineering study. Perimeter discipline enforced throughout: **DZ BANK AG** (parent, HGB) ≠ **DZ BANK Group** (IFRS, ~€661bn total assets, pre-tax €4,282m FY2025) ≠ **Genossenschaftliche FinanzGruppe** (the whole sector — €1.68trn total assets, €11.6bn sector pre-tax profit 2025 per BVR President Marija Kolak, 15 July 2026) ≠ **CRR prudential scope** (excludes insurance). Evidence tags: CONFIRMED FACT / COMPANY CLAIM / THIRD-PARTY ESTIMATE / ANALYTICAL INFERENCE / HYPOTHESIS / UNKNOWN. Volume V only; no cross-volume synthesis.*

---

### V.1 Institutional Architects and the Merger Lineage (replaces Founder Analysis)

DZ BANK has no founder. It is the terminal product of a century-long consolidation of regional cooperative central institutions (Zentralbanken) into a single Spitzeninstitut, and its strategic character was set not by an entrepreneur but by a succession of merger architects and post-merger integrators.

**The 2001 DG BANK/GZ-Bank merger** created "DZ BANK" (Deutsche Zentral-Genossenschaftsbank) as the dominant but not yet sole central institution. **The 2016 WGZ BANK merger** (legally effective 1 August 2016) is the defining structural event: for the first time it left a single cooperative central institution serving the whole sector. (CONFIRMED FACT — DZ BANK's AGM approved the merger on 22 June 2016 with 99.99% of represented capital; WGZ's AGM approved with 99.9%; the combined institution began operations 1 August 2016.)

**Wolfgang Kirsch** (CEO 15 September 2006 – 31 December 2018) is the architect of the modern group. A former Deutsche Bank corporate/investment banker (1981–2002), he presided over the WGZ merger and framed it explicitly as completing "the consolidation process within the superstructure of our banking group." (CONFIRMED FACT, DZ BANK press statement, 22 June 2016.) His stated doctrine — that the cooperative sector's future advantages would be "Präsenz in der Fläche und Dezentralität" (presence across the territory and decentralisation) combined with the ability to "work in networks" (CONFIRMED FACT, Kirsch essay, DZ BANK Innovation LAB, 14 November 2016) — is the belief system that still governs the group. Kirsch also inherited the group's most damaging legacy asset, the transport-finance house **DVB Bank**.

**The Fröhlich/Riese co-CEO era (January 2019 – June 2024).** The Doppelspitze pairing **Uwe Fröhlich** — a former BVR President, i.e. the political voice of the primary banks — with **Cornelius Riese** — a career DZ BANK strategist (joined 2009, Vorstand from 2013 for finance/strategy/controlling) — is itself the clearest single piece of evidence about the group's governance settlement after the WGZ merger. (ANALYTICAL INFERENCE, high confidence.) The pairing was a political treaty: one CEO represented the owners' collective political interest (Verbund), one the institution's own strategic and capital-market management. That the "owner-politician" seat was retired in 2024 and not refilled — leaving the "institution-strategist" in sole command — is a meaningful shift of power toward the central institution and away from pure Verbund-representation.

**Riese's sole leadership (from 1 July 2024).** Riese (b. 20 February 1975, Heidelberg; Diplom-Kaufmann Mannheim; Dr rer. pol. TU Chemnitz; McKinsey internship background) became sole CEO on 1 July 2024 when Fröhlich retired. (CONFIRMED FACT.) On ~27 February 2026 the Aufsichtsrat appointed **Souâd Benkredda** (capital markets, group treasury, structured finance, foreign branches) and **Michael Speth** (risk: credit, group risk controlling, risk steering & services) as **deputy CEOs effective 1 July 2026**, with functional responsibilities unchanged. (CONFIRMED FACT.) This restores collective leadership without recreating the owner/institution treaty: both deputies are functional-domain executives, not BVR politicians — reinforcing the inference that the centre of gravity has moved to the institution.

**Path-dependent beliefs reflected in decisions (not speeches):**
- **Insource, don't outsource, core infrastructure.** The payments-platform insourcing (ZV ON€) runs against the industry outsourcing trend and reveals a belief that transaction infrastructure is strategic and must be sector-owned.
- **Exit non-core rather than defend it.** The DVB wind-down (aviation portfolio sold to Mitsubishi UFJ in 2019; entity defunct 12 August 2022) shows willingness to kill a chronic loss-maker — a discipline notably NOT applied to TeamBank and VR Smart Finanz, which are Verbund-serving.
- **Retain capital, pay little.** The persistent ~15.6% payout / high-retention policy reflects a belief that the group's job is to build sector resilience, not to distribute.
- **Tolerate strategic losses where they serve the Verbund.** Sustained support for loss-making TeamBank and VR Smart Finanz is a Förderauftrag decision, not a profit decision.

---

### V.2 Current Management Team

Eight-member Vorstand (CONFIRMED FACT, DZ BANK confirmation statement dated 12 February 2026).

| Member | Domain | Background | Signal |
|---|---|---|---|
| **Dr Cornelius Riese** | CEO; Strategy & Group Development (incl. sustainability), GenoBanken/Verbund, Communications, Group Audit, Legal | DZ BANK strategist since 2009; Vorstand since 2013 | Institution-strategist in sole command; chairs 4 subsidiary supervisory boards |
| **Souâd Benkredda** | Capital markets, group treasury, structured finance, foreign branches; Deputy CEO from 1 July 2026 | Deutsche Bank (from 2001), Standard Chartered; DZ BANK Vorstand from 1 Sept 2022; first woman on the DZ BANK Vorstand | Capital-markets engine strategically central; external-hire pedigree |
| **Michael Speth** | Risk (credit, group risk controlling, risk steering & services); Deputy CEO from 1 July 2026 | WGZ BANK Vorstand 2010–2016 (head of Finance) | WGZ continuity; risk elevated to co-equal status post-BayWa |
| **Dr Christian Brauckmann** | CIO / IT & Operations | Ex-WGZ; long-tenured | Owns the insourcing bet |
| **Ulrike Brouzi** | CFO | — | — |
| **Johannes Koch** | Verbund- und Geschäftsbank & assigned subsidiaries; Arbeitsdirektor | Generalbevollmächtigter from 1 March 2023, Vorstand from Jan 2024 | Chairs DZ HYP, DZ PRIVATBANK, VR Smart Finanz supervisory boards |
| **Dr Imke Jacob** | Transaction Banking | Ex-McKinsey | Consulting-to-transaction-banking hire signals industrialisation agenda |
| **Stefan Beismann** | (listed on the Vorstand) | — | — |

**Appointment-pattern reading (ANALYTICAL INFERENCE):** recent hires skew external, capital-markets and consulting (Benkredda ex-DB/Standard Chartered; Jacob ex-McKinsey) rather than career Verbund insiders — signalling a team optimising for institutional competitiveness and industrialisation, anchored by WGZ-continuity insiders (Speth, Brauckmann) who hold the merger settlement together.

**Concentration of oversight (flagged risk).** Riese personally chairs the supervisory boards of BSH, R+V, TeamBank and Union Investment (via Union Asset Management Holding). (CONFIRMED FACT.) These four subsidiaries generate the overwhelming majority of group profit. The CEO therefore both runs the parent and chairs oversight of the entities producing ~78% of group earnings — efficient for coherence, but it concentrates key-person risk and blurs the separation of management and supervision at group level. (ANALYTICAL INFERENCE.)

**Executive compensation:** disclosed only in aggregate under InstitutsVergV. Individual figures = **UNKNOWN**.

---

### V.3 Management System and Governance in Practice

The group runs seven-plus regulated operating models, each answering to a different regime: DZ BANK AG and DZ HYP under CRR/ECB-SSM banking supervision; R+V under Solvency II (BaFin insurance); Union Investment under KAGB fund supervision; BSH under the Bausparkassengesetz; TeamBank/VR Smart Finanz under CRR consumer-credit banking; DZ PRIVATBANK under Luxembourg + German banking supervision; plus **financial-conglomerate (FKAG) supervision** binding insurance and banking together.

**Where real power sits — three centres in tension:**
1. **The Vorstand** (institutional management) — sets group strategy and capital allocation, and controls subsidiaries by chairing their supervisory boards.
2. **The Aufsichtsrat**, chaired by **Henning Deneke-Jöhrens** (a serving cooperative-bank CEO, Volksbank Hildesheim-Lehrte-Pattensen), dominated by serving owner-bank CEOs, with **BVR President Marija Kolak** a member. Mitbestimmungsgesetz 1976 applies.
3. **The BVR** — the sector association, which runs the protection scheme (Sicherungseinrichtung) and holds intervention rights over individual banks.

**Coherent strategy or negotiated compromise?** Structurally, a negotiated compromise. The owners are simultaneously customers, distributors, governors (via the Aufsichtsrat) and — through the BVR — guarantors. The 2024–2025 public friction is the tell: at the exact moment of the DZ BANK Bilanzpressekonferenz (March 2025), Kolak publicly questioned DZ BANK's role in the sector Schieflagen, stating it "must not happen that a bank which has already taken on many risks and is under observation by the protection scheme procures additional liquidity — and thereby the potential for even more risk — via DZ BANK." (CONFIRMED FACT, Handelsblatt interview reported by Börsen-Zeitung.) Riese rebutted that liquidity is "as a rule not the problem but the problem-solver" and said he "cannot follow the narrative that DZ BANK drove individual institutions into crisis by providing liquidity." (CONFIRMED FACT.) The backdrop: three cooperative banks entered the Sicherungseinrichtung in 2024 — VR-Bank Bad Salzungen Schmalkalden, Volksbank Dortmund-Nordwest and Volksbank Düsseldorf Neuss — at reported costs of roughly €280m, €134m and €70m respectively (THIRD-PARTY ESTIMATE, Börsen-Zeitung; the BVR does not confirm figures). This is a live boundary dispute over who controls and who is accountable — the clearest available evidence that group strategy is produced through negotiation, not command. In response the BVR tightened intervention rights and is drafting a Vorstands- und Aufsichtsratskodex.

---

### V.4 Culture — Declared versus Revealed

| Declared value | Revealed behaviour | Verdict |
|---|---|---|
| Förderauftrag — serve the primary banks | Sustained support for loss-making TeamBank/VR Smart Finanz; Union Investment paid the Verbund ~€1.57bn in distribution commissions in 2024 and "a tick higher" in 2025 (CONFIRMED FACT, Reinke, Platow) | **Consistent** — the group genuinely subsidises Verbund service |
| Conservative, risk-disciplined | BayWa provisioning "mehr als verfünffachte auf 456 Millionen Euro"; Signa fully written off at R+V FY2023; but the BVR publicly argued DZ BANK's liquidity provision enabled risk build-up | **Mostly consistent, contested** |
| Long-termism | ~15.6% dividend payout, high retention, five-year subsidiary strategies (NextLevel to 2030, #Fokus100, DZ PRIVATBANK 2030, Strategie 2028, Fit for Future at UMH) | **Consistent** |
| Engineering/operational orientation | Payments insourcing (ZV ON€) built with ~500 people, ~5 years, 100,000+ person-days, three-digit-million budget, >600 banks migrated; own SAP S/4HANA + Murex MX.3 | **Consistent — genuine build culture** |
| Decisiveness / speed | Doppelspitze politics; negotiated governance; BVR friction | **Contradiction** — decision-making is slow and consensual by design |

**Contradiction identified:** the group declares customer-centric agility (R+V's NextLevel explicitly promises "mehr Tempo") yet its governance is deliberately consensual and slow. The revealed culture is that of a patient, engineering-led, risk-conservative utility that subsidises its owners — not the agile competitor the strategy documents describe. Employee-review evidence is not load-bearing here and is used only illustratively.

---

### V.5 Incentive Architecture

No share price, no equity compensation. What actually drives behaviour:
- **InstitutsVergV** caps and defers variable pay and constrains risk-taking incentives — pushing behaviour toward stability over profit maximisation.
- **The Förderauftrag** is the stated objective function: strengthen the primary banks' competitiveness, not maximise own profit. It is genuinely binding — it justifies loss-making units and the low payout.
- **Subsidiary CEOs** report to supervisory boards chaired by the group CEO — aligning them tightly to group strategy but concentrating patronage and reducing independent challenge.
- **Owner-bank representatives on the Aufsichtsrat** face a four-way conflict: customers (buy), distributors (sell), governors (oversee) and — collectively via the BVR — guarantors. Individually each bank has little power; collectively decisive political power — and the legal right to source externally.
- **The primary banks** choose whether to sell group products; the incentive is commission income plus Verbundtreue, NOT legal exclusivity. Union's ~€1.57bn+ of distribution commissions to the banks is the economic glue.

**What the system rewards:** sector stability, cross-selling into the Verbund, capital retention. **What can be gamed:** referral counts, product-shelf metrics, the boundary between "group profit" and "commission paid back to owners." **Where incentives conflict:** the group wants to retain capital and manufacture at scale; large owner-banks increasingly want the best product and price, from inside or outside. **Net:** the absence of a share price makes the group MORE long-term oriented than a listed peer (no EPS pressure, no buyback-driven de-equitisation — a practice Riese has publicly criticised as a crisis indicator) but LESS disciplined on returns in the units the Förderauftrag protects.

---

### V.6 Competitive Universe — PER ENGINE

#### (a) As a central institution
Structural analogues, not competitors for the same owners: the Landesbanken — **Helaba, LBBW, BayernLB, NORD/LB**. The cooperative sector's single central institution is a structural advantage over the Sparkassen sector's fragmented, still-consolidating Landesbank layer: one balance sheet, one strategy, one rating anchor, versus several. (ANALYTICAL INFERENCE, high confidence.) At the central-institution layer DZ BANK effectively has no direct competitor — its "competition" is the counterfactual of the primary banks self-organising or defecting, which is near-impossible (V.10/V.11).

#### (b) As a corporate and capital-markets bank
| Competitor | Overlap | DZ BANK position |
|---|---|---|
| Commerzbank | Mittelstand, corporates | Comparable scale; now itself an M&A target (UniCredit) |
| Deutsche Bank | Large corporates, capital markets | DB larger in global IB |
| UniCredit/HypoVereinsbank | Mittelstand, corporates | Cross-border reach |
| Landesbanken (esp. LBBW, Helaba) | Corporates, Schuldschein | Peer |
| **Its own owner-banks** | Mittelstand lending | **Structural tension** — subsidiarity forbids cannibalising them |
| **Structured products / Zertifikate** | Retail structured products | **DZ BANK is the German market leader**, ahead of LBBW and DekaBank |

#### (c) As an insurer (R+V)
Allianz leads life at ~24%; R+V is Germany's #2 P&C insurer (~6.4% share, 2022 KIVI). The öffentliche/Sparkassen insurance bloc (**Provinzial/VKB/SV**) is #2 overall at ~10.8%. Germany's three bancassurance blocs — (1) öffentliche Versicherer + Sparkassen, (2) R+V + Volksbanken/Raiffeisenbanken, (3) Allianz + Commerzbank/Dresdner — together held roughly 75% of new business (THIRD-PARTY ESTIMATE). **R+V's edge over Provinzial/VKB:** the öffentliche Versicherer are bound by the Regionalprinzip (geographically fragmented), whereas R+V is a single national insurer behind a single national bank network. **FY2025:** gross premiums +8.6% to €22.8bn (from €21.0bn; domestic primary business +9.3% to €17.5bn), CEO Norbert Rollinger targeting €25bn by 2030 under NextLevel; combined ratio improved to 86.6%; group IFRS pre-tax roughly doubled to €2.2bn; Solvency II rose from 168% to 204% (preliminary). R+V's weakness: bank-to-insurer referrals fell from ~320,000 to under 200,000/year as branch footfall declined.

#### (d) As an asset manager (Union Investment)
| Competitor | Type | Note |
|---|---|---|
| **DekaBank** | Sparkassen-captive mirror | AuM ~€452bn end-2025; the closest structural analogue |
| DWS | Listed (Deutsche Bank) | Cost/income 58.0% vs Union ~53% |
| Allianz Global Investors, Amundi | Active managers | Scale peers |
| **BlackRock/iShares, Vanguard, Xtrackers** | Passive/ETF | Structural margin threat |
| **Trade Republic, Scalable Capital** | Neobrokers | Bypass bank branches entirely |

Union FY2025: AuM €534.6bn (record; 2024: €504.7bn), net inflows €23.3bn (2024: €17.3bn) split retail €13.5bn ("zweitbestes Absatzergebnis in der 70-jährigen Unternehmensgeschichte") and institutional €9.8bn (doubled from €4.7bn), operating result €1,185m (2024: €1,241m), cost/income ~53%. Union has explicitly declined to offer passive ETFs (CONFIRMED FACT) — a bet on active management plus the captive savings-plan base (fund savings plans above 4 million). **The neobroker threat is now large and fast:** Trade Republic crossed 10 million customers in 2026, up from ~8 million at its Poland launch in September 2025, with €150bn AuM across 18 countries and ~one-third of customers outside Germany; co-founder Christian Hecker states "70% of Trade Republic customers are first-time investors" — i.e. it is capturing the next generation of savers before a Volksbank branch ever sees them.

#### (e) As a Bausparkasse (BSH)
Competitors: **LBS** (Sparkassen), **Wüstenrot**, **Debeka Bausparkasse**; plus platform intermediaries **Hypoport/Europace** and **Interhyp** disintermediating the advice layer. BSH is the unchallenged leader — 33.3% Bauspar market share (management cites ~34–35% on an "eingelöstes Neugeschäft" basis), ~7m contracts, FY2025 pre-tax €122m (doubled again), Baufinanzierung new business €15.8bn (+16%). BSH's own counter to platform disintermediation is **BAUFINEX** (its cooperative broker marketplace: €16.8bn transaction volume in 2025, +26.8%, 560 product providers) — building the platform rather than only being disintermediated by one.

#### (f) As a consumer lender (TeamBank)
Competitors: **Santander Consumer Bank, TARGOBANK, ING**; comparison platforms **Check24, Smava**; BNPL **Klarna, PayPal, Ratepay**. TeamBank FY2025: loan book €9,132m (−3.7%), ~1.067m customers, new business −9.4%, pre-tax **−€29m** (2024: +€23m), German Ratenkredit share ~3.9% and falling (Austrian "faire Credit" share 12.3%). **Why the share falls (ANALYTICAL INFERENCE):** (1) TeamBank sells only through cooperative branches whose footfall is declining, while rivals run direct + platform origination; (2) comparison platforms commoditise price, and easyCredit is a premium-priced "faire" product; (3) BNPL captures the small-ticket point-of-sale credit that used to seed instalment loans; (4) the 2025 consumer recession forced deliberate risk-tightening. The classic Ratenkredit was retired end-June 2025 and replaced (Strategie 2028) with a flexible individual credit line — a bet that product modernisation plus embedded finance (easyCredit-Ratenkauf, ~2,500 merchants) can arrest the decline.

#### (g) As a payments processor (ZV ON€ and VR Payment)
Competitors: **Worldline/equensWorldline, Nexi, Adyen, Stripe**; the Sparkassen's **S-Payment** and the 2024 **"Qards"** merger (Bayern Card-Services + PLuscard); and, decisively, **Atruvia**, which takes card issuing-processing from 1 January 2027. Context: Worldline is Europe's largest merchant acquirer by revenue but in deep distress — shares are down more than 96% from a peak above €20bn in mid-2021 (all-time-high close €98.40 on 6 Jan 2021 vs a 2025 year-close near €3.80); Nexi's strongest 2025 growth market was Germany; Adyen and Stripe are the high-growth gateway-acquirers. DZ BANK processed ~11.0bn transactions on ZV ON€ in FY2025. The 2027 restructuring splits the value chain: Atruvia takes issuing-processing (debit + credit) onto an integrated card platform; VR Payment keeps and expands merchant acquiring + POS network. (CONFIRMED FACT; Bundeskartellamt case B9-75/26 notified 15 July 2026.) Consequence: the group will manufacture card products without controlling their processing.

#### (h) As a real-estate lender (DZ HYP)
Competitors: **Münchener Hypothekenbank** (in-sector, independent cooperative — the proof that partial substitution is possible), **Berlin Hyp, Aareal, pbb**. DZ HYP is Germany's largest mortgage-Pfandbrief issuer; portfolio ~€57.6bn, FY2025 pre-tax €338m. MünchenerHyp is #2 with a mortgage book of ~€46bn (end-June 2025), 79% residential.

#### Cross-cutting threats
Neobanks/neobrokers erode the primary banks themselves (shrinking DZ BANK's distribution base); embedded finance moves credit to the point of sale; the digital euro threatens payment economics. Each attacks the **distribution premise** on which the whole group rests.

---

### V.7 Competitor Teardowns

**DekaBank (closest structural mirror).** Sparkassen-owned central securities house. AuM ~€452bn end-2025 vs Union €534.6bn; wirtschaftliches Ergebnis €962.9m in 2025 (from €892.2m, +7.9%), a sales record of €40.9bn (+40%), >6m securities accounts, CET1 (CRR III) 21.2% (2024: 19.8%), dividend €400m (+€100m). Deka guides **conservatively to >€700m for 2026** — the same "peak-year, expect reversion" honesty Riese shows for the group. Same manufacture-and-distribute, sector-captive model; same branch-distribution reliance; Deka is more certificate-heavy (Deka-Zertifikate €22.2bn). Union out-scales Deka in AuM and runs a lower cost/income (~53%).

**Landesbanken collectively.** The Sparkassen sector's fragmented central-institution layer. Advantage DZ BANK: one consolidated central institution with a single group rating vs four+ separately managed and rated institutions — the single clearest structural win of the cooperative architecture over the Sparkassen architecture. (ANALYTICAL INFERENCE, high confidence.)

**DWS.** Listed benchmark; cost/income 58.0% vs Union ~53%. Union is more efficient but unlisted (no market discipline, no equity currency for M&A).

**Allianz / Provinzial-SV.** Allianz is the scale and profitability benchmark R+V cannot match on size; Provinzial/SV/VKB is the direct bancassurance mirror, constrained by the Regionalprinzip where R+V is national.

**Sparkassen-Finanzgruppe as systemic rival.** Almost identical three-tier architecture: DSGV≈BVR, Landesbanken≈DZ BANK, Finanz Informatik≈Atruvia, Deka≈Union, öffentliche Versicherer≈R+V, LBS≈BSH. Larger in aggregate (~€2.5trn sector assets vs cooperative €1.68trn). Key difference: public-law owners bound by the Regionalprinzip and a fragmented central-bank layer, versus private-law owners and a unified central institution.

---

### V.8 Why the Group Wins — and Where It Does Not

**Decomposition of the win mechanism:**
1. **Institutional protection scheme → rating uplift → cheap funding → cheap products** (master mechanism; quantified in V.9).
2. **Exclusive central-institution mandate** — a natural monopoly at the wholesale layer; unreplicable by a new entrant.
3. **Manufacture-and-distribute reach** across ~645 banks and 30m+ end customers — scale that lowers unit cost.
4. **Payments/clearing scale** — ~11.0bn transactions; Germany's third-largest depositary (€380.7bn).
5. **Three-engine diversification** — banking + insurance + asset management (uncorrelated on paper; but see V.16).
6. **Captive-adjacent (not captive) distribution** — a cost advantage only while the banks choose to sell.

**Structural vs choice vs temporary:** #1–#2 are structural (regulatory/legal); #3–#5 are management-built scale (choice, in principle replicable by the Sparkassen); #6 is temporary and eroding. The FY2025 profit windfall (R+V combined ratio 86.6% vs 94.9%) is purely temporary — Riese guides FY2026 to ~€3.0bn precisely because the benign claims year will not repeat: "Gleichwohl wäre ein Ergebnis in dieser Höhe ohne begünstigende Faktoren, insbesondere bei der R+V Versicherung, nicht möglich gewesen."

**Where it does NOT win:** TeamBank (share 3.9% and falling, loss-making); VR Smart Finanz (loss-making, cost/income 78.6%); R+V referrals (−38%); branch-based distribution generally.

---

### V.9 Moat Analysis — REFRAMED AS CONTESTED

Scoring 0–5, separating (a) *prevents exit/substitution* from (b) *creates value*.

| Candidate moat | Prevents exit | Creates value | Verdict |
|---|---|---|---|
| Institutional protection scheme (IPS) | 5 | 5 | **Genuine moat** — the one moat independent of the banks' choice to distribute |
| Central-institution mandate | 5 | 4 | Structural monopoly; genuine |
| Ownership by distributors | 4 | 2 | Prevents exit, but does NOT by itself create product value |
| Ecosystem/technical integration (Atruvia rails) | 4 | 3 | Sticky, but DZ BANK holds only ~0.35% of Atruvia |
| Payments/clearing platform | 3 | 3 | Scale value; issuing-processing leaves for Atruvia in 2027 |
| Regulatory/conglomerate-supervision capability | 3 | 3 | Real barrier to entry; costly to replicate |
| Union Investment AuM annuity | 3 | 4 | High-quality fee stream; threatened by passive/neobrokers |
| R+V underwriting scale | 3 | 3 | #2 national; sub-Allianz |
| BSH 33.3% Bauspar share | 4 | 3 | Dominant niche; Bauspar itself is structurally challenged |
| DZ HYP Pfandbrief franchise | 3 | 3 | Largest issuer; MünchenerHyp proves substitutability |
| Brand/trust within the Verbund | 3 | 3 | Real but shared and contestable |

**The contested core.** Because distribution is legally optional (documented: Volksbank Mittelhessen brokers Allianz Leben and Generali/Proxalto alongside R+V), **network ownership must NOT be scored as a value-creating moat without asking whether the group wins shelf space on merit.** The evidence that it largely does: Union achieved record inflows (€23.3bn) and paid the banks ~€1.57bn+ in commissions in 2025 (they keep selling because it pays and the product performs); R+V grew premiums +8.6% to €22.8bn; BSH held 33.3%. The shelf-space contest is currently being won — but on merit and economics, not legal lock-in.

**Which moats survive if Verbundtreue weakened:** the IPS and the central-institution mandate survive (legal/structural). The manufacture-and-distribute reach, the R+V referral flow, the Union commission engine and the BSH share would all erode — they depend on the banks' continued *choice* to distribute. **This is the fault line of the whole edifice.**

---

### V.10 Replication and Substitution Test

**(a) Replication (rebuild from scratch):** effectively impossible. One would need the central-institution clearing role and ~11bn-transaction platform; the IPS with its legal mutual-liability web and regulatory approvals; seven+ regulated licences across four supervisory regimes; €534.6bn of AuM; an insurer with ~26m insured risks and €6.68bn contractual service margin; and a distribution relationship with ~645 independent banks that must *choose* to participate. The last cannot be bought at any price — it must be earned politically over decades.

**(b) Substitution (replace piecemeal):** already partially possible TODAY. The banks can and do buy insurance from Allianz/Generali; funds could migrate to BlackRock/ETFs; payments could go to Worldline; mortgages already go partly to **Münchener Hypothekenbank** — an independent cooperative mortgage bank OUTSIDE the group whose very existence proves at least one product line is substitutable within the sector. Consumer credit is already substitutable (Santander/BNPL).

**Irreplaceable vs substitutable:** irreplaceable = central-institution clearing + the IPS + the conglomerate-supervision apparatus. Substitutable = funds, insurance, consumer credit, mortgages, payments-processing (already leaving to Atruvia). **The wholesale/regulated core is a fortress; the retail product edges are contestable commodities.**

---

### V.11 Porter's Five Forces (adapted for a cooperative conglomerate)

- **Rivalry:** varies enormously by engine — near-zero at the central-institution layer, brutal in consumer credit and ETFs, moderate in insurance/asset management. The group is insulated where it is regulated and exposed where it is retail.
- **Supplier power:** HIGH and rising for **Atruvia** (the sector IT monopoly; DZ BANK holds only ~0.35% — a customer-adjacent counterparty, not a controller) and for SAP/Murex/IBM and the market infrastructures. The 2027 card migration hands Atruvia more of the payments value chain. (ANALYTICAL INFERENCE.)
- **Buyer power (paradoxical):** buyers ARE the owners and governors. Individually a single Volksbank has little power; collectively, via the BVR and Aufsichtsrat, decisive political power — and the legal right to source externally. Consolidation converts many weak individual buyers into fewer strong ones (V.14).
- **Substitutes:** passive/ETFs, BNPL, embedded finance, neobrokers, platform mortgage intermediaries (Europace/Interhyp/Baufinex). All attack the retail edges.
- **New entrants:** near-impossible at the central-institution/IPS layer; easy at the product-module layer (a neobroker needs no licence web to steal an ETF saver).

**Verdict:** a fortress at the wholesale core and a contested incumbent at the retail edge — and the two are linked, because the retail edge is where the owners' customer base is eroding.

---

### V.12 PESTLE (material factors only)

- **Political:** German banking-policy debate; EU banking-union completion; sovereignty/consolidation debate (Riese sees "gewisse Sinnhaftigkeit" in a UniCredit/Commerzbank tie-up); BVR–DZ BANK governance friction.
- **Economic:** rate normalisation (the FY2025 −17.8% NII drop was largely an accounting artefact offset by trading swinging from −€842m to +€281m); German stagnation (DZ BANK economists ~1.0–1.2% 2026 GDP); real-estate cycle (DZ HYP, BSH); the BayWa-type Mittelstand/agricultural credit cycle.
- **Social:** branch decline and the collapse in R+V referrals (~320k→<200k); demographic change; migration of savings to ETFs/neobrokers.
- **Technological:** AI (all subsidiary strategies cite it); the digital euro; instant payments; tokenisation/DLT bond issuance; embedded finance.
- **Legal (decisive):** CRR III (cut RWA to €148.6bn, lifting CET1 to 18.4%); Solvency II review; DORA; and above all the **EU CMDI package** touching the IPS and Article 113(7) CRR.
- **Environmental:** green Pfandbriefe (DZ HYP and MünchenerHyp both active); EU taxonomy (Union Article 8/9 assets €153.7bn); climate underwriting risk at R+V (the benign 2025 nat-cat year flattered results — reversion is the risk).

**CMDI status (CONFIRMED FACT — the single most consequential legal factor, and it broke the group's way):** Council and Parliament reached political agreement on 25 June 2025; the Council formally adopted the CMDI package in first reading on 5 March 2026. Critically, the agreed text "introduces specific provisions to preserve a functioning framework for institutional protection schemes (IPSs) to implement preventive measures," and the DGSD continues to "take into account the mandate of an IPS that fulfils the requirements of Article 113(7) CRR." The German government reportedly protested the Commission's original points; the final text is materially more protective of IPSs than the 2023 proposal. **Interpretation:** the tail risk to Article 113(7) treatment did NOT crystallise in this round — a major positive for the group's rating architecture. The ECB continues to press (via its Guide on options and discretions, and MEP correspondence dated 2 September 2025) for a segregated ex-ante IPS fund as a condition of the 0% risk-weight — a slow-burn constraint, not an existential threat.

---

### V.13 Strategic Flywheels (validated)

1. **Manufacture-at-scale loop (VALIDATED):** primary banks distribute → group manufactures at scale → lower unit cost + commission income → banks compete better and earn commission → more distribution. Evidence: Union's ~€1.57bn+ commissions to banks; record inflows. **Failure condition:** banks source externally, or the customer base shrinks.
2. **Protection-scheme funding loop (VALIDATED, strongest):** IPS → rating uplift → cheaper funding → cheaper products → stronger sector → stronger scheme. Evidence: the rating architecture (V.9/V.24). **Failure condition:** CMDI/Art. 113(7) reform (did not crystallise) or a support event large enough to strain the scheme.
3. **Payments-scale loop (WEAKENING):** payments scale → lower cost per transaction → more sector volume → more scale. **Failure condition:** the 2027 hand-off of issuing-processing to Atruvia removes part of this loop from DZ BANK's control.

---

### V.14 Negative Flywheels

1. **Branch decline → fewer referrals → weaker bancassurance (DOCUMENTED):** ~320k → <200k referrals/year → weaker R+V retail → less commission for banks → less incentive to distribute. The most concretely evidenced negative loop.
2. **Consolidation → fewer, larger owners → more bargaining power + more willingness to source externally → weaker Verbundtreue → contested shelf space.** Owner base fell from 672 (end-2024) to ~645, shrinking 23–25 mergers/year.
3. **Passive/ETF + neobroker growth → retail fund-margin compression at Union → the group's highest-quality earnings stream erodes.** Union's refusal to offer ETFs concentrates this risk.
4. **Loss-making subsidiaries → capital drag → less investment capacity.** TeamBank −€29m, VR Smart Finanz −€28m, holding −€335m FY2025.

---

### V.15 Theory of Constraints / Strategic Bottleneck

If every other part improved 50%, the binding constraint is **the willingness and capacity of the shrinking, consolidating primary-bank base to keep distributing group products through a declining branch channel.** Everything else — capital, manufacturing scale, product quality — is downstream of distribution. Evidence: the documented referral collapse; the consolidation trend; the legal optionality of distribution; TeamBank's share loss.

**Next bottleneck if distribution were solved:** the **conglomerate capital ratio (FKAG 136.1% end-2024, 142.2% H1 2025)** — not the banking CET1 (18.4%) — because insurance + asset management dominate earnings and the conglomerate ratio is what actually binds. A correlated market drawdown that hits R+V own funds and Union AuM simultaneously would tighten this ratio directly.

---

### V.16 Risk Register — PRIORITY DEPTH

| # | Risk | Prob | Severity | Detectability | Horizon | Residual |
|---|---|---|---|---|---|---|
| **1** | **Correlated equity/credit drawdown hitting R+V + Union simultaneously** | Med | **High** | High | 0–3y | **The only event that damages two of three engines at once.** R+V investment result + Solvency II own funds AND Union AuM fees fall together. Buffers: R+V SAA/hedging, VSM €6.68bn, Solvency II 204%; residual HIGH |
| **2** | **CMDI/deposit-insurance reform curtailing IPS Art. 113(7) treatment** | **Low (post-2026)** | **Existential** | High | 3–7y | Underpins 0% intra-network risk-weighting AND ~1–2 rating notches. 2025–26 CMDI round PRESERVED IPS treatment; residual now LOW but permanent tail |
| 3 | Nat-cat year reversing R+V combined-ratio windfall | High | Med | Med | 0–2y | 2025's 86.6% CR is unrepeatable; guidance reflects this |
| 4 | German CRE deterioration at DZ HYP | Med | Med-High | Med | 0–3y | €57.6bn book; Pfandbrief-covered |
| 5 | Second BayWa (single-name Mittelstand) | Med | Med | Low | 0–3y | Provisioning "verfünffachte auf 456 Mio"; sector-shared |
| 6 | Member-bank consolidation shrinking owner base | High (certain) | Med | High | ongoing | 23–25/yr; erodes distribution |
| 7 | Erosion of Verbundtreue / loss of shelf space | Med | High | Med | 2–7y | Legally optional distribution |
| 8 | Atruvia dependency + 2027 card migration | Med | Med | High | 2027 | Execution + supplier-power risk |
| 9 | Passive/ETF disruption of Union | High | Med-High | High | ongoing | Highest-quality earnings at risk |
| 10 | Branch-decline erosion of bancassurance | High (certain) | Med | High | ongoing | Documented referral collapse |
| 11 | Rate normalisation compressing NII | Med | Low-Med | High | 0–2y | Offset by trading/insurance |
| 12 | Key-person/succession on recently reconstituted Vorstand | Med | Med | Med | 0–3y | Riese chairs 4 boards; two new deputies from 1 July 2026 |
| 13 | Cyber / operational resilience | Med | High | Low | ongoing | DORA; own S/4HANA+Murex |
| 14 | Conglomerate capital constraint (136–142%) | Low | High | High | ongoing | The true binding constraint |
| 15 | Reputational contagion across shared Verbund brand | Med | Med-High | Low | ongoing | Schieflagen; BVR friction |

---

### V.17 Stress Tests (strategic)

1. **20–30% equity drawdown + spread widening:** hits R+V investment result (already fell 54.5% to €2,368m in 2025) and Solvency II own funds (204% buffer absorbs much) AND Union AuM fees together. CET1 largely unaffected (insurance out of CRR scope), but the **conglomerate ratio tightens materially** — the scenario that hits the binding constraint. Survivable; earnings reset lower 1–2 years.
2. **Major nat-cat year at R+V:** combined ratio reverts toward/above 100%; segment pre-tax could fall from €2,144m toward or below €1bn; group toward the low end of the €2.5–3.0bn "natural" range. Reinsurance mitigates the tail.
3. **CMDI reform removing IPS privileges (did NOT occur in 2025–26):** would raise intra-network risk weights from 0% and cut ~1–2 rating notches, raising funding cost sector-wide. Existential-adjacent; low probability post-2026.
4. **German CRE crisis:** DZ HYP losses; Pfandbrief cover protects investors; segment pre-tax compresses from €338m.
5. **Second BayWa:** another ~€400–450m provision; absorbable at group level, sector-shared via BRB-type vehicles.
6. **Consolidation to <400 primary banks:** fewer, larger, more demanding owners; accelerates external sourcing; strategic more than financial threat.
7. **A large primary bank publicly sourcing insurance/funds outside the Verbund:** reputationally and economically corrosive; the Volksbank Mittelhessen precedent shows it already happens at the margin.
8. **2027 Atruvia card migration failing:** operational disruption across >600 banks; the VR Payment split adds execution risk.
9. **Sustained ETF/neobroker shift halving Union retail net inflows:** retail from €13.5bn toward ~€6–7bn; slow degradation of the highest-quality earnings stream.
10. **Ratings downgrade:** most likely trigger is IPS/scheme weakening, not standalone deterioration (since ~1–2 notches are scheme-derived).
11. **Multiple simultaneous Vorstand departures:** elevated by Riese's four-board concentration; mitigated by the 1 July 2026 deputy appointments.
12. **Digital-euro rollout displacing payment revenue:** slow-burn; erodes ZV ON€/VR Payment economics; timing uncertain.

---

### V.18 What Could Make the Group Obsolete?

| Disruption | Removes customer problem? | Can group adopt? | Assets still useful? | Strands capital? |
|---|---|---|---|---|
| Terminal branch-distribution decline | No (advice demand persists) | Partially (omnichannel) | Yes | Some |
| Passive/neobroker commoditisation of retail AM | No | Reluctantly (Union refuses ETFs) | Partly | Union franchise value |
| Embedded finance/BNPL displacing consumer credit | Partly | Yes (easyCredit-Ratenkauf) | TeamBank licence | Yes if unadapted |
| Digital euro disintermediating payments | Partly | Must (sector infra) | ZV ON€ partly | Payments capex |
| Platform mortgage intermediaries | No (funding still needed) | Yes (BAUFINEX) | Pfandbrief franchise | No |
| **Primary-bank consolidation into self-manufacturers** | **Yes** | No | Central role redundant | **Yes — the true obsolescence path** |
| Merger of cooperative + Sparkassen infrastructure | Reshapes, not removes | Politically hard | Yes | Possibly |

**Verdict:** technology alone does not make the group obsolete — it can adopt most disruptions and its regulated core stays useful. The one genuine obsolescence path is **owner-side**: consolidation into primary banks large enough to self-manufacture, plus eroding Verbundtreue, hollowing the central factory from within.

---

### V.19 Strategic Optionality

| Option | Classification |
|---|---|
| Sell ZV ON€ payments processing to non-cooperative banks | **Plausible adjacency** (stated ambition; 2027 Atruvia hand-off complicates) |
| Expand Union institutional business beyond the Verbund | **Natural adjacency** (institutional inflows doubled to €9.8bn in 2025) |
| R+V international (Assimoco/Italy; CCB/ICCREA partnerships) | **Plausible adjacency** |
| DZ PRIVATBANK third-party Luxembourg fund services | **Natural adjacency** (Frankfurt HQ from Jan 2026; Luxembourg fund-servicing retained) |
| Grow custody/depositary by acquisition | **Natural adjacency** (already #3 at €380.7bn) |
| Consolidation with a Landesbank | **Stretch** (cross-pillar, political) |
| Atruvia–Finanz Informatik merger | **Strategic fantasy** (the 2027 card deal shows deeper Atruvia dependence, not convergence) |
| Tokenisation / digital-asset custody | **Plausible adjacency** |
| Become a pure holding, divest the banking stub | **Stretch/fantasy** — contradicts the central-institution mandate that is the group's reason to exist |

---

### V.20 What Is the Group Becoming? (ranked)

| Hypothesis | Probability | Evidence for | Evidence against |
|---|---|---|---|
| **H2: bancassurance + AM holding, bank a minority utility** | **~35%** | ~78% of pre-tax profit from insurance + AM; only ~27% from the banking business (Finanz-Szene) | Central-institution mandate is legally core; cannot divest the bank |
| **H4: progressively disintermediated at retail edges, regulated wholesale core retained** | **~30%** | TeamBank share loss; referral collapse; ETF/neobroker threat; 2027 processing hand-off | Union/R+V/BSH still winning shelf space on merit |
| **H1: unchanged central institution + product factory** | **~20%** | Structural inertia; IPS intact post-CMDI; owners won't dismantle | Distribution premise eroding |
| **H3: national payments/transaction-banking infra beyond the sector** | **~8%** | ZV ON€ ambition; Jacob hire | 2027 Atruvia hand-off removes issuing-processing |
| **H5: consolidates with Sparkassen infra or a Landesbank** | **~5%** | Sector-consolidation logic | Cross-pillar politics near-prohibitive |
| **H6: restructured after a capital/credit/governance crisis** | **~2%** | BayWa/Signa; BVR friction | Strong buffers; IPS |

**Most likely trajectory (ANALYTICAL INFERENCE):** a blend of H2 and H4 — the group increasingly IS an insurance-and-asset-management holding wrapped around a regulated wholesale core, while its retail product edges are slowly contested. The bank does not disappear; it becomes the smaller, utility-like anchor of a group whose value is manufactured by R+V and Union.

---

### V.21 Five- and Ten-Year Strategic Map

- **Base case:** group pre-tax reverts to the €2.5–3.0bn "natural" range (FY2026 guidance ~€3.0bn); R+V and Union remain ~75–80% of profit; owner base drifts below ~600 then ~550; CET1 stays high, the conglomerate ratio the binding constraint; moat intact at core, contested at edge.
- **Strong execution:** Union institutional scaling + BAUFINEX + payments repositioning + R+V NextLevel (€25bn premium target by 2030) lift the natural range; cost/income holds near 49%.
- **Market shock:** correlated drawdown compresses R+V + Union together; conglomerate ratio tightens; earnings reset 1–2 years; survivable.
- **Regulatory shock (CMDI/IPS reform):** low probability post-2026 but the one scenario that threatens the identity via funding cost + rating.
- **Technology disruption:** ETF/neobroker + digital euro slowly erode retail AM and payments; the group adapts at lower margin.
- **Sector consolidation:** <400 banks; shelf-space contest intensifies; central factory hollows if Verbundtreue weakens.
- **Major credit/operational failure:** BayWa-scale repeat or Atruvia migration failure; reputational; financially absorbable.

---

### V.22 What the Market and Sector May Misunderstand

1. **"DZ BANK is a bank."** Reality: ~78% of FY2025 pre-tax profit is insurance + asset management; Finanz-Szene calculates only ~27% from the banking business. Persists because of the name and balance sheet. Implication: value and risk-manage it as a conglomerate; the conglomerate ratio, not CET1, is the constraint.
2. **"The FinanzGruppe's €1.68trn / €11.6bn are DZ BANK figures."** Reality: those are SECTOR figures (per BVR President Kolak, 15 July 2026); the DZ BANK Group is ~€661bn / €4,282m pre-tax FY2025. The most commonly misquoted numbers in the sector.
3. **"The primary banks are captive distributors."** Reality: distribution is legally optional; Volksbank Mittelhessen already brokers Allianz Leben and Generali/Proxalto alongside R+V. Shelf space is contested and won on merit.
4. **"18.4% CET1 means over-capitalised."** Reality: the binding constraint is the FKAG conglomerate ratio (136.1% end-2024 / 142.2% H1 2025) against a 100% external minimum, 113% internal minimum and 123% observation threshold — not CET1.
5. **"The AA rating reflects standalone strength."** Reality: the scheme provides material uplift (V.9/V.24); the standalone assessment is investment-grade but below the supported rating.
6. **"DZ BANK controls the cooperative sector's IT."** Reality: DZ BANK holds ~0.35% of Atruvia; the ~20% figure that circulates refers to Verimi. The 2027 card deal shows DZ BANK is a customer-side counterparty to Atruvia, not its controller.
7. **"The FY2025 €4.28bn is the run-rate."** Reality: guidance is ~€3.0bn; Riese: a result of that size "wäre ohne begünstigende Faktoren, insbesondere bei der R+V Versicherung, nicht möglich gewesen."

---

### V.23 Management and Capital-Allocation Judgement

| Decision | Verdict | Evidence |
|---|---|---|
| 2016 WGZ merger | **Value-creating / strategically necessary** | Created the single cooperative central institution |
| DVB wind-down | **Value-creating** | Killed a chronic loss-maker; aviation sold to MUFG 2019; defunct 2022 |
| 2018 DZ HYP formation (DG HYP + WL BANK) | **Value-creating** | Germany's largest Pfandbrief issuer; €338m FY2025 |
| Payments insourcing (ZV ON€) | **Strategically necessary; too early to fully judge** | ~11bn tx; 2027 issuing-processing exit qualifies the ROI |
| VR Payment issuing-processing → Atruvia (2027) | **Questionable / strategically rational** | Concentrates card processing sector-wide but increases Atruvia supplier power over DZ BANK |
| Depositary acquisitions | **Value-creating** | #3 at €380.7bn |
| Sustained support for TeamBank / VR Smart Finanz | **Questionable on returns; consistent with Förderauftrag** | −€29m / −€28m FY2025; share falling |
| High-retention, low-payout capital policy | **Value-creating for sector resilience** | ~15.6% payout; builds conglomerate buffer |
| Response to BayWa/Signa | **Strategically necessary** | Provisioned/written off; but BVR publicly contested DZ BANK's role |
| Current Vorstand appointment pattern | **Too early to judge; directionally sound** | External capital-markets/consulting hires + WGZ continuity |

---

### V.24 Volume V Reconstruction — synthesis and closing questions

#### The rating architecture (integrated primary-source evidence — the quantified moat)

The single most important fact underpinning the group's moat is how rating agencies treat the institutional protection scheme:

- **Moody's (Aa2, stable).** Pre-November 2025, DZ BANK's standalone Baseline Credit Assessment was **baa2** and its Adjusted BCA **a3** — **two notches of uplift** from "a very high probability of cross-sector support from Genossenschaftliche FinanzGruppe" via the institutional protection scheme (Moody's Credit Opinion, 28 May 2025: the a3 Adjusted BCA "results in two notches of rating uplift from DZ BANK's baa2 BCA"). In the 18–20 November 2025 methodology-driven action on ~69 Western European banking groups, Moody's **upgraded the BCA one notch (to baa1) while affirming the Adjusted BCA at a3**, compressing the affiliate-support uplift to **one notch**; the final Aa2 rating (Adjusted BCA a3 + three notches of Advanced LGF uplift) was unchanged. The BCA upgrade "predominantly considers the improved assessment of the bank's funding position, taking into account its access to stable funding from the cooperative sector." (Note: the post-November-2025 "baa1" label is inferred from a one-notch upgrade, not a captured verbatim quote — to confirm against the next Credit Opinion.)
- **S&P (A+, stable).** S&P **equalises DZ BANK with the 'a+' group credit profile** on "core group status," adds **zero ALAC uplift**, calls "group support… the strongest support element," and deems a bail-in "highly unlikely… would imply solidarity within the sector had ceased." The rating is thus not merely uplifted by the scheme — it *is* the scheme's group credit profile.
- **Fitch (AA-/F1+; senior preferred AA).** Fitch assigns a **single group rating** to Genossenschaftliche FinanzGruppe (Viability Rating 'aa-'), covering DZ BANK and ~700 primary banks together; DZ BANK is not rated standalone but carries the group viability rating, with senior preferred/deposits notched **+1 to AA** for resolution-buffer protection (reaffirmed 20/21 January 2026).
- **Morningstar DBRS (context): AA (low)**, with an explicit **one-notch uplift** from the A (high) Intrinsic Assessment driven by the BVR protection scheme (SA1, 30 October 2024).

**Bottom line on the moat:** across the agencies, the cooperative scheme is worth on the order of **one to two notches of rating**, and at S&P and Fitch it is the very basis of the rating (equalised to / anchored on the group). The moat is real, quantified and — uniquely — the ONE moat that does not depend on the primary banks choosing to distribute.

#### Closing questions

**Why does the group persist, and would it be created today?** It persists because the IPS + central-institution mandate make it a regulatory fortress with a rating the sector cannot replicate individually, and because it genuinely subsidises its owners (Förderauftrag). Would it be created today? The wholesale/IPS core — yes. The sprawling manufacture-and-distribute conglomerate spanning insurance, asset management, Bauspar, consumer credit and payments — **probably not in this exact form**; a green-field designer would likely *buy* several retail product modules (funds, consumer credit, payments-processing) rather than own them — exactly as the substitution analysis and the 2027 Atruvia hand-off already imply.

**Defensible vs merely structurally protected:** genuinely defensible = the IPS rating uplift, the central-institution clearing role, Union's active-AM scale and efficiency, R+V's national bancassurance reach vs the region-bound öffentliche Versicherer, BSH's Bauspar dominance. Merely structurally protected = the loss-making Verbund-service units and the assumption of captive distribution.

**Hardest vs easiest to replicate:** hardest = the IPS, the central-institution role, the ~645-bank distribution relationship (unbuyable). Easiest = the retail product modules — several already substitutable today (MünchenerHyp proves it).

**Current bottleneck:** the willingness/capacity of a shrinking, consolidating, branch-declining primary-bank base to keep distributing on merit. **Next bottleneck if solved:** the conglomerate capital ratio under a correlated market drawdown.

**Single greatest structural risk:** the correlated equity/credit drawdown that simultaneously hits R+V (investment result + Solvency II own funds) and Union (AuM fees) — the only event that damages two of three engines at once and tightens the binding conglomerate ratio. The CMDI/IPS tail risk is more severe if it crystallises but is now low-probability, having been substantially preserved in the 2025–26 CMDI outcome.

**Most dangerous competitor/force, and horizon:** over 0–3 years, benign-year reversion and correlated-market risk; over 3–10 years, the **structural erosion of branch distribution combined with neobroker/ETF disintermediation of the retail edge and owner-bank consolidation** — a slow negative flywheel, not a single rival. Trade Republic/Scalable and BlackRock/iShares are the sharpest individual embodiments.

**Could it be made obsolete, or would it adapt?** It would adapt to technology; the genuine obsolescence path is owner-side (consolidation into self-manufacturers + eroding Verbundtreue).

**Are the owner-banks well served?** On current evidence, yes — Union pays them ~€1.57bn+ in commissions, R+V and BSH give them competitive products, and the IPS gives their depositors a AA-rated safety net. But they are served by a structure whose distribution premise is quietly eroding beneath it.

**The central question — durable structure or mid-twentieth-century architecture?** Verdict: the **regulated wholesale core (central institution + IPS) is durable for the next decade and beyond** — a genuine, quantified, near-unreplicable moat. The **manufacture-and-distribute retail superstructure is a mid-twentieth-century architecture whose distribution premise is eroding** — legally optional distribution, a shrinking owner base, collapsing referrals and neobroker/ETF disintermediation all pull in one direction. The group is durable; the *conglomerate form* is contingent on continuing to win shelf space on merit. It is doing so today. The decade ahead is a race between the compounding value of the fortress core and the compounding erosion of the distribution edge.

#### Key Unknowns
- Individual executive compensation (InstitutsVergV aggregate only) — **UNKNOWN**.
- Exact post-November-2025 Moody's DZ BANK standalone BCA label ("baa1" is inferred) — **to confirm against the next Credit Opinion**.
- Internal board deliberations, strategy documents, and the precise economics of the VR Payment/Atruvia transaction — **UNKNOWN**.
- Final FY2025 R+V Solvency II (204% preliminary) and year-end 2025 conglomerate ratio — preliminary/H1 figures used.

#### Ten Most Important Conclusions
1. The group is ~78% insurance + asset management by profit; it is a conglomerate, not a bank (~27% banking).
2. The IPS is the master moat — worth ~1–2 rating notches, the basis of S&P's and Fitch's ratings — and the only moat independent of the banks' choice to distribute.
3. Distribution is legally optional and contested; the retail moat must be re-won every year on merit (and currently is).
4. The binding capital constraint is the FKAG conglomerate ratio (~136–142%), not the 18.4% CET1.
5. The FY2025 €4.28bn is a windfall; ~€3.0bn is the run-rate — an unusually honest management guide.
6. The single greatest structural risk is a correlated equity/credit drawdown hitting R+V and Union together.
7. The CMDI 2025–26 outcome preserved Article 113(7)/IPS treatment — the sector's biggest legal tail risk did not crystallise.
8. The strategic bottleneck is the shrinking, branch-declining, consolidating owner-distribution base (672 end-2024 → ~645; 23–25 mergers/year).
9. Management follows the Förderauftrag in revealed behaviour (subsidised units, low payout, commissions to owners), not just speeches — but governance is a negotiated compromise, evidenced by the 2024–25 BVR friction.
10. The wholesale core is durable for the decade; the conglomerate superstructure is a legacy architecture whose distribution premise is eroding — a durable group in a contingent form.

*Volume V complete. No cross-volume synthesis undertaken, per scope.*


---

# Part VI — Cross-Volume Synthesis

*This section is new. It exists only in the master edition and draws on all five volumes.*

## VI.1 The name is the first mistake

Almost every error made about this institution follows from its name.

**DZ BANK is not, in economic substance, a bank.** In FY2025 the group earned €4,282m before tax, of which R+V (insurance) contributed €2,144m and Union Investment (asset management) €1,185m — together roughly **78%**. The Central Institution and Corporate Bank segment, the part that actually is a bank, contributed €864m. Finanz-Szene put it more bluntly: only about **27%** of the record result came from the banking business.

Reading the group as a bank produces a chain of category errors:

| Read as a bank | Actually |
|---|---|
| CET1 18.4% means large capital headroom | The binding constraint is the FKAG conglomerate ratio at 136.1% |
| Its competitors are Commerzbank and the Landesbanken | Its competitors are Allianz, DWS, BlackRock, Santander and Worldline — different firms in every engine |
| Net interest income falling 17.8% is a serious problem | Largely an accounting artefact, offset by trading swinging from −€842m to +€281m |
| Return on equity is the governing metric | It is unlisted, cooperatively owned, and runs a Förderauftrag |
| The FY2025 result is the run-rate | Guidance for FY2026 is ~€3.0bn |

The correct frame is a **financial conglomerate under FKAG supervision**: a banking group and a Solvency II insurance group bound together by a supplementary capital regime, with an asset manager and a Bausparkasse alongside — wrapped around a regulated central-institution core.

## VI.2 The single causal model — a fortress core and a contested edge

```
        INSTITUTIONAL PROTECTION SCHEME (BVR-SE / BVR-ISG)
                            │
        Article 113(7) CRR → 0% intra-network risk weight
        + 1–2 notches of rating uplift (S&P equalises to the
          group; Fitch rates the sector, not the bank)
                            ↓
              cheap, stable funding at AA-band
                            ↓
    ┌───────────── THE FORTRESS CORE ─────────────┐
    │  Central-institution mandate (exclusive)     │
    │  Clearing: ~11.0bn payments/yr               │
    │  Liquidity management for the whole sector   │
    │  Conglomerate-supervision capability         │
    └──────────────────────────────────────────────┘
                            ↓
    products manufactured centrally by R+V, Union,
    BSH, DZ HYP, TeamBank, VR Smart Finanz
                            ↓
    ┌──────────── THE CONTESTED EDGE ─────────────┐
    │  ~645 primary banks CHOOSE whether to sell   │
    │  (distribution is LEGALLY OPTIONAL)          │
    │  Won today on merit + ~€1.57bn+ commissions  │
    └──────────────────────────────────────────────┘
                            ↓
              30m+ end customers, owned by
              the primary banks — not the group
                            ↓
    ┌─────────── THE EROSION ──────────────────────┐
    │  Branch decline → R+V referrals 320k → <200k │
    │  Consolidation → 672 (2024) → ~645 banks     │
    │  ETF/neobrokers capture first-time savers    │
    │    before a branch ever sees them            │
    └──────────────────────────────────────────────┘
                            ⟲ back to distribution
```

**The defining property: the core and the edge have opposite dynamics.** The wholesale core is getting stronger — CRR III lifted capital, the 2025–26 CMDI package preserved the IPS, the payments platform consolidated. The retail edge is getting weaker — referrals down 38%, TeamBank's share falling, branch footfall in structural decline. The group's earnings come overwhelmingly from the edge; its durability comes overwhelmingly from the core.

## VI.3 What the volumes prove together that none proves alone

**1. The only moat independent of owner choice is the protection scheme.**

Volume I established the mechanism: the BVR's Sicherungseinrichtung and BVR-ISG constitute an institutional protection scheme recognised under Article 113(7) CRR, permitting a 0% risk weight on intra-network exposures, with no member bank having failed since 1934. Volume V quantified its worth: Moody's lifts the standalone Baseline Credit Assessment by one to two notches to an a3 Adjusted BCA; S&P equalises DZ BANK to the sector's 'a+' group credit profile and adds no ALAC uplift because sector support is "the strongest support element"; Fitch does not rate DZ BANK standalone at all, assigning a single group rating covering the bank and ~700 primary banks together.

Volume II established the countervailing fact: **distribution is legally optional.** Volksbank Mittelhessen operates as a tied R+V agent while simultaneously brokering Allianz Leben and Generali/Proxalto, and German case law permits it.

Chain these and the structure appears: **every advantage the group has except the protection scheme and the central-institution mandate depends on ~645 independent banks continuing to choose to sell its products.** The scheme is the one asset that does not.

**2. The binding capital constraint is not the one anyone looks at.**

Volume I established why the CRR prudential scope excludes insurance. Volume IV established the consequence: three capital regimes that cannot be reconciled to a single number — CET1 18.4% (banking only), Solvency II 203.8% (R+V only), and the FKAG conglomerate coverage at 136.1% (end-2024) rising to 142.2% (H1 2025). The conglomerate ratio arithmetically sums two full requirement stacks and gives **no credit for cross-sector diversification**, which is why a banking CET1 that looks lavish coexists with a conglomerate ratio that is merely comfortable.

**Anyone reading 18.4% as deployable headroom has misread the group.** The internal thresholds — 113% minimum, 123% observation — are where management actually operates.

**3. Federation gives no protection against the one risk that matters.**

Volume III established that the group runs seven separate operating models with separate technology estates, separate regulators and separate production engines — a genuinely federated structure. Volume IV established that R+V and Union Investment together are ~78% of profit. Volume V established that both are exposed to the same variable: equity and credit markets. A drawdown reduces Union's AuM-based fees and R+V's investment result and Solvency II own funds **simultaneously**, and tightens the conglomerate ratio directly.

**Operational federation delivers no diversification against the correlated market risk that dominates the group's earnings.** The diversification is real against idiosyncratic risk — a BayWa credit event, a nat-cat year — and largely illusory against systematic risk.

**4. The group does not control its own distribution rail, and is becoming more dependent on it.**

Volume III established that DZ BANK runs its own SAP S/4HANA core and Murex — it is not an Atruvia customer for its own systems. But Volume II established that the growing retail channel is the VR Banking App, which Atruvia controls; Volume I and Volume V established that **DZ BANK holds approximately 0.35% of Atruvia** (the widely-repeated ~20% figure refers to Verimi); and from 1 January 2027 card issuing-processing transfers from VR Payment to Atruvia.

**The group manufactures products, and is progressively ceding control of the rails through which they reach customers, to an entity it barely owns.**

## VI.4 The central tension

The DZ BANK Group exists so that roughly 645 small cooperative banks can remain independent full-service institutions. It succeeds at that. But its own economics now depend on those banks' branch networks — and branch-based distribution is precisely what is being disrupted.

Every actor is behaving rationally. A primary bank closing branches is responding to cost pressure. A saver opening a Trade Republic account rather than visiting a Volksbank is responding to convenience and price. Union Investment declining to launch ETFs is protecting a margin its owners depend on. R+V investing in digital referral tools is doing what it can.

And the aggregate outcome is that the manufacturing superstructure is optimised for a distribution channel in secular decline. **The fortress core cannot save the contested edge, because the edge is where the earnings are.**

## VI.5 What would falsify this reading

Specific, checkable markers, so the study can be audited against reality:

| If this happens | The reading weakens because |
|---|---|
| Group pre-tax holds above ~€3.5bn for two consecutive years without a benign claims year | The FY2025 result was less of a windfall than assessed |
| R+V bank referrals stabilise or recover above ~250,000/year | The distribution erosion is cyclical, not structural |
| Union Investment's retail net inflows hold above ~€12bn while ETF share keeps rising | The active/captive model is more resilient than assessed |
| A future CMDI or Basel review curtails Article 113(7) IPS treatment | The fortress core is less secure than assessed — this is the tail risk |
| TeamBank's German market share stabilises above ~3.9% | The retail-edge erosion is arrestable |
| The conglomerate ratio moves toward the 123% observation threshold | Capital, not distribution, becomes the binding constraint sooner |
| A top-20 primary bank publicly sources insurance or funds outside the Verbund | Shelf-space erosion has moved from marginal to material |
| The 2027 Atruvia card migration completes cleanly and DZ BANK wins external ZV ON€ clients | The payments platform is a genuine growth asset, not just infrastructure |

## VI.6 What the group is becoming

Ranked by probability on the evidence assembled across all five volumes:

| Hypothesis | Probability | Strongest evidence |
|---|---|---|
| Bancassurance and asset-management holding, bank a minority utility | ~35% | ~78% of pre-tax profit already from insurance and AM |
| Progressively disintermediated at the retail edge, regulated core retained | ~30% | Referral collapse; TeamBank share loss; ETF and neobroker growth |
| Unchanged central institution and product factory | ~20% | Structural inertia; IPS preserved in the 2025–26 CMDI outcome |
| National payments and transaction-banking infrastructure beyond the sector | ~8% | ZV ON€ ambition; but issuing-processing leaves for Atruvia in 2027 |
| Consolidates with Sparkassen infrastructure or a Landesbank | ~5% | Sector logic; cross-pillar politics near-prohibitive |
| Restructured after a capital, credit or governance crisis | ~2% | BayWa and Signa; strong buffers argue against |

**Synthesis:** a blend of the first two. The group is already, in substance, an insurance-and-asset-management holding wrapped around a regulated wholesale core, and its retail edges are slowly being contested. The bank does not disappear; it becomes the smaller, utility-like anchor of a group whose value is manufactured elsewhere.

## VI.7 Implications for a fintech builder

*This section applies the study to the reader's own context rather than to DZ BANK. Analytical inference throughout.*

**The protection scheme explains why German cooperative deposits are so hard to compete with.** A Volksbank's depositor is protected by a scheme that has not let a member fail since 1934, and its funding carries an AA-band rating it did not earn standalone. If your model depends on attracting German retail deposits away from cooperative or savings banks on safety grounds, that argument does not work. Compete on product, convenience and price — not on security.

**The distribution premise is the opening, and someone is already through it.** The single most actionable finding in this study is that R+V's bank referrals fell from roughly 320,000 to under 200,000 a year, while Trade Republic passed ten million customers with 70% of them first-time investors. The incumbent's manufacturing scale is intact; its route to the next generation of customers is not. Whatever you are building, the question worth asking is whether it reaches a customer before a branch does.

**Understand what a bank partner's capital constraint actually is.** If you partner with a European bancassurance group, its willingness to deploy balance sheet is not governed by the CET1 ratio in its press release. For a conglomerate it may be the FKAG-equivalent coverage ratio; for a monoline it may be MREL or the leverage ratio. Ask which constraint binds before assuming headroom exists.

**"Optional distribution" is a business model, not a weakness — but it must be re-won annually.** DZ BANK's manufacturers keep their shelf space by paying roughly €1.57bn a year in commissions and by performing. If you are building a product distributed through partners you do not own, that is the discipline: no contract makes them sell it, and the commission is the price of the relationship, not the reward for it.

**Insurance and asset management are where the money is, not payments.** This is worth internalising against fintech convention. In the largest cooperative financial group in Germany, payments processes 11 billion transactions a year and earns roughly 1.8 cents each; asset management earns 45.7 basis points on €534.6bn without touching a payment. Payments buys the customer relationship. Manufacturing monetises it.

**Finally, on conglomerates.** This study is a detailed demonstration that combining banking, insurance and asset management produces genuine earnings diversification against idiosyncratic shocks and almost none against systematic ones — while imposing a permanent, volume-insensitive supervisory cost. If you are ever tempted to add a regulated business line to another regulated business line, read Part IV first.

## VI.8 Ten cross-volume conclusions

1. DZ BANK is a financial conglomerate, not a bank — roughly 78% of profit comes from insurance and asset management.
2. The institutional protection scheme is the master moat, worth one to two rating notches, and the only advantage independent of the owner-banks' choice to distribute.
3. Distribution is legally optional; shelf space is contested and must be re-won every year on merit and commission.
4. The binding capital constraint is the FKAG conglomerate ratio at ~136–142%, not the 18.4% CET1.
5. Federation across seven operating models gives no protection against the correlated equity and credit risk that dominates group earnings.
6. The FY2025 result of €4,282m was a windfall; management guides FY2026 to approximately €3.0bn.
7. The group is becoming more dependent on Atruvia — an entity it holds approximately 0.35% of — as channels and card processing consolidate there.
8. The wholesale core is strengthening while the retail edge erodes; the earnings sit at the edge.
9. The 2025–26 CMDI package preserved Article 113(7) IPS treatment — the sector's largest legal tail risk did not crystallise this round.
10. The group exists to keep small banks independent, and its economics depend on the branch networks that digital distribution is dismantling.

---

# Appendix A — Glossary of German and Regulatory Terms

*Load-bearing. Read before Part IV.*

## Sector and institutional

| Term | Meaning |
|---|---|
| **Genossenschaftliche FinanzGruppe (GFG)** | The whole German cooperative financial network — the ~645 primary banks plus DZ BANK Group and associated institutions. **Not** the DZ BANK Group |
| **Zentralinstitut / Spitzeninstitut** | Central institution — DZ BANK's role as the apex bank for the sector |
| **Primärbank** | A primary (local) cooperative bank: a Volksbank or Raiffeisenbank |
| **Verbund** | The network or alliance of cooperative institutions |
| **Verbundtreue** | Network loyalty — the informal norm that binds primary banks to Verbund products |
| **Förderauftrag** | Statutory promotional mandate — DZ BANK exists to strengthen the primary banks' competitiveness, not to maximise its own profit |
| **Subsidiaritätsprinzip** | Subsidiarity — the central institution supports rather than competes with the primary banks |
| **BVR** | Bundesverband der Deutschen Volksbanken und Raiffeisenbanken — the sector association |
| **Metakredit** | Joint or consortium credit, where DZ BANK supplies balance sheet while the primary bank keeps the customer relationship |

## Protection scheme

| Term | Meaning |
|---|---|
| **Sicherungseinrichtung (BVR-SE)** | The BVR's institutional protection scheme, operating since 1934; protects the institution as a whole, not merely deposits, through preventive intervention |
| **BVR Institutssicherung GmbH (BVR-ISG)** | The statutory deposit-guarantee scheme since 1 July 2015, and simultaneously an IPS under Article 113(7) CRR |
| **Institutional Protection Scheme (IPS)** | The recognised arrangement permitting a 0% risk weight on intra-network exposures under Article 113(7) CRR |
| **Schieflage** | A distressed situation at a member institution, potentially triggering scheme intervention |

## Accounting and financial

| Term | Meaning |
|---|---|
| **Zinsüberschuss** | Net interest income |
| **Provisionsüberschuss** | Net fee and commission income |
| **Betriebsergebnis** | Operating result |
| **Jahresüberschuss** | Net income for the year |
| **Verwaltungsaufwendungen** | Administrative expenses |
| **Risikovorsorge** | Loss allowances / credit-risk provisioning |
| **Bilanzsumme** | Total assets |
| **Einzelabschluss / Konzernabschluss** | Parent-only accounts / consolidated group accounts |
| **HGB** | Handelsgesetzbuch — the German Commercial Code; the parent's accounting basis |
| **Vertragliche Servicemarge (VSM) / CSM** | Contractual service margin — under IFRS 17, the store of unearned future insurance profit |
| **Kapitalanlageergebnis** | Investment result |
| **Zinszusatzreserve (ZZR)** | Additional interest reserve in German life insurance (an HGB concept) |

## Corporate and governance

| Term | Meaning |
|---|---|
| **Vorstand** | Management board (executive) |
| **Aufsichtsrat** | Supervisory board (non-executive) — German two-tier structure |
| **Doppelspitze** | A co-CEO arrangement; DZ BANK ran one from 2019 to 2024 |
| **Arbeitsdirektor** | Labour director — a board member with mandatory HR responsibility under co-determination |
| **Mitbestimmungsgesetz 1976** | The co-determination law giving employees half the supervisory-board seats above 2,000 employees |
| **Hauptversammlung** | General meeting of shareholders |
| **Beherrschungs- und Gewinnabführungsvertrag (BGAV)** | Control and profit-transfer agreement between parent and subsidiary |
| **Patronatserklärung** | Letter of comfort |
| **Organschaft** | Tax grouping between parent and subsidiary |

## Products

| Term | Meaning |
|---|---|
| **Bausparkasse / Bausparvertrag** | Building society / building-savings contract combining savings with a rate-locked loan entitlement |
| **Bausparsumme** | The total contract value of a Bauspar agreement |
| **Baufinanzierung** | Residential construction or purchase finance |
| **Pfandbrief** | German covered bond, backed by a segregated cover pool under the Pfandbriefgesetz |
| **Zertifikate** | Structured retail investment products — DZ BANK is the German market leader |
| **Ratenkredit** | Instalment consumer loan |
| **Depot A / Depot B** | A bank's own-account securities portfolio / customer securities accounts |
| **Warengeschäft** | Commodity trading business, run by roughly one in ten cooperative banks |

## Regulatory

| Term | Meaning |
|---|---|
| **BaFin** | Bundesanstalt für Finanzdienstleistungsaufsicht — the federal financial supervisor |
| **SSM** | Single Supervisory Mechanism — DZ BANK is directly supervised by the ECB as a Significant Institution |
| **CRR / CRD** | Capital Requirements Regulation and Directive; **CRR III** applies from 1 January 2025 |
| **SREP / P2R** | Supervisory Review and Evaluation Process / Pillar 2 Requirement (1.80% for 2026) |
| **O-SII / A-SRI** | Other Systemically Important Institution buffer (1.00% from 1 January 2026) |
| **MREL** | Minimum Requirement for Own Funds and Eligible Liabilities |
| **LCR / NSFR** | Liquidity Coverage Ratio / Net Stable Funding Ratio |
| **Solvency II / SCR / ORSA / SFCR** | The insurance prudential regime; Solvency Capital Requirement; Own Risk and Solvency Assessment; Solvency and Financial Condition Report |
| **FKAG / FiCoD** | Finanzkonglomerate-Aufsichtsgesetz — German financial-conglomerate supervision law transposing the EU directive; requires an annual §25(3)/(4) report |
| **KAGB / UCITS / AIFMD** | The German investment code and the EU fund directives governing Union Investment |
| **Bausparkassengesetz (BSpKG)** | The law restricting Bausparkasse activity |
| **CSSF** | The Luxembourg financial supervisor, for DZ PRIVATBANK |
| **SRB / SRMR** | Single Resolution Board and Regulation — resolution planning |
| **CMDI** | The EU Crisis Management and Deposit Insurance package; the 2025–26 outcome preserved IPS treatment |
| **DORA** | Digital Operational Resilience Act |
| **InstitutsVergV** | The German remuneration ordinance for financial institutions |

---

# Appendix B — Canonical Figures Register

**Where any volume disagrees with this table, this table governs.** Every figure carries its perimeter and date. As of 9 August 2026.

## Group financials — DZ BANK Group (IFRS), FY2025

| Figure | Canonical value |
|---|---|
| Profit before taxes | **€4,282m** (2024: €3,303m) |
| Income taxes | €1,402m (effective rate ~32.7%) |
| Net profit | €2,880m |
| Total assets | ~**€661bn** |
| Cost/income ratio | 49.3% |
| Net interest income | €3,839m (−17.8%, largely an accounting artefact) |
| Net fee and commission income | €3,370m |
| Trading result | +€281m (2024: −€842m) |
| Net income from insurance business | €2,024m (IFRS 17 basis) |
| Loss allowances | −€653m (2024: −€845m) |
| Administrative expenses | €4,804m |
| Dividend | €448m (25 cents/share; ~15.6% payout) |
| **FY2026 guidance** | **approximately €3.0bn pre-tax** |

## Segment pre-tax, FY2025 (€m)

| Segment | Result |
|---|---|
| R+V | **2,144** |
| Union Investment (UMH) | **1,185** |
| Central Institution & Corporate Bank (CICB) | 864 |
| DZ HYP | 338 |
| Bausparkasse Schwäbisch Hall | 122 |
| DZ PRIVATBANK | 106 |
| TeamBank | −29 |
| VR Smart Finanz | −28 |
| Holding function | −335 |
| Other / consolidation | −85 |
| **Insurance + asset management share** | **~78%** |

## The three capital regimes — never reconcile to one number

| Regime | Perimeter | Value |
|---|---|---|
| **CET1** | Banking group (CRR, excludes insurance) | **18.4%** (2024: 15.8%; CRR III lowered RWA to €148.6bn) |
| Tier 1 / total capital / leverage | Banking group | 20.5% / 23.6% / 7.0% |
| MREL | Banking group | 40.8% of RWA |
| LCR / NSFR | Banking group | 156.4% / 126% |
| P2R (2026) / O-SII buffer | Banking group | 1.80% / 1.00% |
| **Solvency II ratio** | R+V group | **203.8%** (preliminary end-2025; end-2024 restated to 172.5%) |
| **FKAG conglomerate coverage** | Whole conglomerate | **136.1%** (end-2024); 142.2% (H1 2025) |
| FKAG thresholds | Whole conglomerate | 100% external minimum · 113% internal minimum · 123% observation |

## Ownership and structure

| Figure | Canonical value |
|---|---|
| Cooperative bank ownership | **94.8%** (other cooperative enterprises 4.8%; others 0.5%), 31 Dec 2025 |
| Primary cooperative banks | **~645** (672 at end-2024; 23–25 mergers/year) |
| Registered entity | DZ BANK AG, HRB 45651, Amtsgericht Frankfurt am Main; BIC GENODEFF |
| **Stake in Atruvia** | **~0.35%** — the "~20%" claim is **erroneous** and refers to Verimi |
| Union Asset Management Holding stake | **72.37%** (BBBank and the regional cooperative associations hold the residual) |
| Group employees | ~**33,837** (2024), of which R+V alone >18,400 |

## Subsidiary scale

| Entity | Key figures |
|---|---|
| **R+V** | Gross written premiums €22.8bn (2025, +8.6%); ~9m customers; ~26m insured risks; >18,400 employees; combined ratio 86.6% (2024: 94.9%); CSM/VSM €6,680m |
| **Union Investment** | AuM €534.6bn; retail €270.8bn / institutional €263.8bn; net inflows €23.3bn; margin ~45.7bps; cost/income ~53%; Article 8/9 assets €153.7bn |
| **Bausparkasse Schwäbisch Hall** | ~7m contracts; Bauspar market share 33.3%; Baufinanzierung new business €15.8bn (+16%) |
| **DZ HYP** | Portfolio ~€57.6bn; Germany's largest Pfandbrief issuer; corporate new business €9.2bn |
| **DZ PRIVATBANK** | AuM €30.7bn; assets under custody €181.3bn; >1,200 employees |
| **TeamBank** | ~1.067m customers; loan book €9,132m; German market share 3.9% and falling |
| **VR Smart Finanz** | New business €1.18bn; portfolio €3.12bn; cost/income 78.6% |
| **VR Payment** | ~248 employees; revenue >€200m; issuing-processing to Atruvia 1 Jan 2027 |

## Operations

| Figure | Canonical value |
|---|---|
| Payment transactions | **11.0bn** (FY2025); 10.2bn (2024); 9.9bn (2023) |
| Payments platform | ZV ON€, insourced, migration completed 2024 (~500 people, ~5 years, 100,000+ person-days, >600 banks) |
| Depositary / custody | €380.7bn — Germany's third largest |
| Joint/consortium credit (Metakredit) | ~€19.3bn |
| Own core systems | SAP S/4HANA + Murex MX.3 — **not** Atruvia |

## Ratings and the protection scheme

| Figure | Canonical value |
|---|---|
| S&P | **A+** — equalised to the sector's 'a+' group credit profile; no ALAC uplift |
| Moody's | **Aa2** — Adjusted BCA a3; standalone BCA baa2, upgraded to baa1 in November 2025 |
| Fitch | **AA-/AA** — a single group rating covering DZ BANK and ~700 primary banks |
| Morningstar DBRS | AA (low) — one notch of uplift from the protection scheme |
| **Rating uplift attributable to the IPS** | **~1–2 notches** |

## Sector context — Genossenschaftliche FinanzGruppe perimeter, NOT DZ BANK

| Figure | Canonical value |
|---|---|
| Sector total assets | **€1.68trn** (2025) |
| Sector pre-tax profit | **€11.6bn** (2025); €7.4bn net after €4.2bn taxes |
| Sector cost/income ratio | 58.3% |
| Primary banks' net commission income | €6.5bn (2024), ~€3bn of it from payments |
| End customers | 30m+ |

---

# Appendix C — Reconciliation of Cross-Volume Discrepancies

The volumes were written sequentially against a moving evidence base, and DZ BANK's figures conflict for two reasons that must be kept apart: **perimeter and date differences**, which are legitimate, and **genuine errors**, which are not.

## Perimeter, date and basis differences — not errors

| # | Item | Appears as | Resolution |
|---|---|---|---|
| 1 | **Genossenschaftliche FinanzGruppe scale** | €1.175trn (Volumes I–III) versus €1.68trn (Volumes IV–V) | **Different years and measures.** The earlier figure is the primary banks' aggregate balance sheet as reported for 2022; €1.68trn is the sector total for 2025 per BVR President Kolak on 15 July 2026. Neither is the DZ BANK Group (~€661bn). |
| 2 | **Sector pre-tax profit** | €9.5bn (2024) versus €11.6bn (2025) | Different years, both sector perimeter — not the group's €4,282m. |
| 3 | **Primary bank count** | ~645 / 672 / ~700 / "rund 800" | A **falling series** measured at different dates: ~800 in older sources, 672 at end-2024, ~645 by late 2025, with ~700 used loosely by DZ BANK and Fitch for the rating perimeter. |
| 4 | **R+V gross written premiums** | €20.9bn versus €22.8bn | 2024 versus 2025. The 2025 figure is +8.6%. |
| 5 | **R+V pre-tax result** | €2,144m versus €2,221m | **DZ BANK segment perimeter versus R+V's own IFRS group perimeter.** Both correct; do not use interchangeably. |
| 6 | **R+V Solvency II ratio** | 168% → 172.5% → 203.8% | 168% was the originally-published end-2024 figure, later **restated to 172.5%**; 203.8% is preliminary end-2025. The restatement follows the §352 VAG transitional revaluing to zero. |
| 7 | **FKAG conglomerate coverage** | ">100%, >113% internal" (Volume I) versus 136.1% / 142.2% (Volume IV) | Volume I reported the thresholds; Volume IV obtained the actual ratios. **136.1% at end-2024, 142.2% at H1 2025 governs.** |
| 8 | **Payment transactions** | 9.9bn / 10.2bn / 11.0bn | A rising series: FY2023 / FY2024 / FY2025. |
| 9 | **CET1 ratio** | 15.8% versus 18.4% | 2024 versus 2025. The rise is **mainly CRR III lowering RWA**, not a capital raise. |
| 10 | **Net interest income −17.8%** | Presented as a decline | Largely an **accounting artefact**: 2024 NII was inflated by valuation effects with a countervailing trading loss. NII plus trading rose 7.6%. |
| 11 | **Union Investment AuM** | €534.7bn versus €534.6bn | Rounding between sources; €534.6bn is the later figure. |
| 12 | **BSH ownership** | 96.8% versus 97.6% | Both appear in group materials; treat as approximate. |
| 13 | **BSH Bauspar market share** | 33.3% versus ~34–35% | Different measurement bases — total contracts versus "eingelöstes Neugeschäft." |
| 14 | **Moody's standalone BCA** | baa2 versus baa1 | **baa2 before November 2025; upgraded one notch to baa1** in the methodology-driven action of 18–20 November 2025, with the Adjusted BCA affirmed at a3 — so the scheme uplift compressed from two notches to one while the Aa2 rating was unchanged. |

## Genuine errors and corrections

| # | Item | Status |
|---|---|---|
| 15 | **"DZ BANK holds ~20% of Atruvia"** | **FALSE.** DZ BANK holds approximately **0.35%**. The ~20% figure belongs to **Verimi**. This error circulates widely and should be expected in further sources. DZ BANK is a *customer-side counterparty* to Atruvia, not its controller. |
| 16 | **Union Investment stake "~93%"** | **Superseded.** Volume I carried ~93%; Volume II established **72.37%** as of 31 December 2025, with BBBank and the regional cooperative associations holding the residual ~27.6%. The higher figure reflects the pre-2016 structure in which WGZ BANK held 17.72% alongside DZ BANK's 54.44%; the WGZ stake was absorbed in the 2016 merger. |
| 17 | **Münchener Hypothekenbank treated as a group entity** | **FALSE.** It is an **independent cooperative mortgage bank outside the DZ BANK Group**, ECB-supervised, and therefore an in-sector competitor to DZ HYP and BSH. The BVR consolidated accounts treat it as a "rechtlich selbstständiges, gleichgeordnetes Mutterunternehmen" alongside the DZ BANK Konzern. Its existence is the standing exception to any strict "one champion per product" reading. |
| 18 | **The Signa write-off quotation** | **Mis-attributed in an earlier volume.** R+V CEO Norbert Rollinger stated on 3 April 2024 that the Signa engagement was fully processed in the 2023 accounts. The phrase "robuster dreistelliger Millionenbetrag" traces to **DZ BANK CEO Cornelius Riese**, not Rollinger. Both confirm a full FY2023 write-off. |
| 19 | **R+V bank distribution reach** | **Two figures appear:** "more than 7,500 Bankstellen" (Volume II) and "more than 13,000 cooperative bank branches" (Volume V). These are **not reconciled**. The lower figure likely counts branches with embedded R+V field staff; the higher counts all cooperative branches through which R+V products are available. Treat both as approximate and do not sum or average. **UNRESOLVED.** |

## Known unknowns carried forward

- Individual executive compensation (InstitutsVergV discloses aggregate only).
- Per-product commission rates and the precise Verbund versus non-Verbund revenue split.
- The register of control and profit-transfer agreements (BGAVs) across subsidiaries.
- Intercompany service pricing and cost-allocation terms.
- The quantified cost of the multi-regime "conglomerate tax."
- DZ PRIVATBANK's fund-administration and transfer-agency software product.
- Formal availability SLOs, RTO and RPO for the ZV ON€ platform.
- The VR Payment issuing-processing transaction price and the year-end 2025 conglomerate ratio.
- Precise post-November-2025 Moody's BCA label (baa1 is inferred from a one-notch upgrade).
- The reconciliation of the 7,500 versus 13,000 branch-reach figures.

---

# Appendix D — Source Hierarchy & Evidence Conventions

Sources were prioritised as follows, with primary evidence preferred wherever it existed:

1. **DZ BANK Geschäftsberichte and Konzernabschlüsse** (IFRS consolidated and HGB parent), half-year reports, the Risikobericht, and the **Offenlegungsbericht / Pillar 3 disclosure** — collectively a materially richer evidence base than either prior EREF subject afforded.
2. **The §25(3)/(4) FKAG conglomerate report** — the sole public source for the conglomerate coverage ratio, and therefore for the group's binding capital constraint.
3. **Subsidiary annual reports and, for R+V, the Solvency and Financial Condition Report (SFCR)** — the SFCR is unusually informative on insurance operations, own funds and sensitivities.
4. **Rating agency reports** — Moody's, S&P, Fitch and Morningstar DBRS — which are more explicit than any company disclosure about the institutional protection scheme's contribution to the rating and about group-support assumptions.
5. **ECB, BaFin, Bundesbank, EBA and the SRB** — SREP and Pillar 2 publications, buffer decisions, stress-test results and resolution material.
6. **BVR** publications, the consolidated financial statements of the Genossenschaftliche FinanzGruppe, and statements by BVR President Marija Kolak.
7. **Bundesanzeiger** filings and **Handelsregister** records for material entities.
8. **German specialist press** — Börsen-Zeitung, Handelsblatt, Finanz-Szene, DER PLATOW Brief, procontra, Versicherungswirtschaft and FONDS professionell — which carry executive interviews and sector reporting unavailable elsewhere.
9. **EU policy material on the CMDI package**, decisive for the institutional protection scheme's future treatment.
10. Competitor and benchmark material: DekaBank, DWS, Allianz, Provinzial/SV, LBS, Wüstenrot, Santander Consumer Bank, Worldline, Nexi, Münchener Hypothekenbank and the Sparkassen-Finanzgruppe.

SEO-oriented aggregators were not relied on where primary evidence existed. For strategically significant claims, sources were triangulated. Where reputable sources disagreed, the disagreement is identified, perimeters and dates compared, and uncertainty preserved rather than resolved by false precision.

**A note on the prohibition against invented architecture.** Volume III in particular was written under an absolute rule: where the group has published nothing about an internal mechanism, the report says UNKNOWN rather than describing plausible-sounding but unevidenced internals. A bank of this size discloses far less about its systems than a fintech does, and several sections are consequently shorter than their headings might suggest. That is deliberate.

---

*End of the DZ BANK Enterprise Reverse-Engineering Study.*
