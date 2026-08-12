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

