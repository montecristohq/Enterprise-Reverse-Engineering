# BUILD SPECIFICATION — read this before rendering

This document contains a complete comparative institutional study of approximately **77,600 words**. What follows is a binding specification for how it must be rendered. It is not editorial guidance. Every clause is a requirement.

Render as a **screen document with a persistent sidebar** — not a paginated print document. Use the **Industry** design system: Barlow Condensed for headings, Barlow for body, `ui-monospace` for numerals.

**Palette for this subject.** Warm ink on a bone ground, with a single deep accent — this is a book of argument and law, not a company teardown, and it should not read as a corporate report. Suggested direction: a warm off-white paper (near `#f4f1ea`), a dark warm-grey ink, and a deep oxblood or forest accent for section numerals, evidence labels and figure emphasis. **It must be visibly distinct from the four enterprise studies in this programme**, which run steel-blue (`#5980a6`) and signal-red. Do not reuse either.

---

## 1. PRESERVATION CONTRACT — non-negotiable

**1.1 Every word is retained.** Approximately 77,600 words of body prose. Do not summarise, condense, abridge, truncate, sample or paraphrase any section.

**1.2 Every table renders as a table.** There are approximately **40 tables containing 406 data rows**. Appendices A and B are almost entirely tabular and are the document's lookup instruments — converting them to prose destroys their function. Do not drop columns to make a table fit; see §3.4.

**1.3 Every evidence label is retained in place.** The six long-form labels (CONFIRMED FACT, SCHOLARLY CONSENSUS, CONTESTED IN THE LITERATURE, ANALYTICAL INFERENCE, HYPOTHESIS, UNKNOWN) appear **245 times**; the compressed forms used in Appendices A–C (`[CF] [SC] [CL] [AI] [H] [U]`) appear a further **65 times**. They are load-bearing: this document distinguishes statute from scholarship from inference throughout, and stripping the labels collapses that distinction.

**1.4 Legal citations render intact.** Section symbols, statute names and article references must not break across lines: §43a GenG, §73(3), §27, §33(c), BOFIA 2020 §2(5), CRR Article 29, 12 CFR Part 702 Subpart D, RLRQ c. C-67.3, Loi n° 47-1775.

**1.5 Non-ASCII characters are preserved exactly.** The document carries German (Geschäftsguthaben, Prüfungsverband, Vertreterversammlung, Nachschusspflicht), French (réserve générale impartageable, dévolution désintéressée, parts permanentes, ristournes), Dutch (coöperatie, ledenraad), Yoruba and Hausa (ajo, esusu, adashe), and the currency symbols ₦, €, £, $, KSh, C$. **Verify these survive the render** — a corrupted umlaut or a mangled naira sign is a build failure.

**1.6 No content in a collapsed, hidden or truncated state.**

**Verification:** the output must contain approximately 77,600 words of body prose, approximately 40 tables and 406 data rows.

---

## 2. STRUCTURE CONTRACT

**2.1 Fourteen top-level sections**, each rendering as an `h1` with a section-opening treatment:

1. Front matter (title, what this document is, conventions, contents)
2. Prologue — Why Cooperatives Exist, and Why They Fail
3. Part I — Legal Form and Member Rights
4. Part II — Capital
5. Part III — Governance at Scale
6. Part IV — Shared Infrastructure
7. Part V — The Nigerian Regulatory Path
8. Part VI — What Transplants, and the Design Brief
9. Appendix A — Jurisdiction Matrix
10. Appendix B — Capital-Instruments Catalogue
11. Appendix C — Failure Catalogue
12. Appendix D — Glossary
13. Appendix E — Canonical Figures Register
14. Appendix F — Source Register and Reconciliation

**Do not collapse these into fewer top-level headings.**

**2.2 The Prologue takes a WORD, not a numeral.** Its section opener carries the word *Prologue* set in the numeral's position — same weight, same optical size, no numeral. This is deliberate: the Prologue is different in kind from the numbered Parts, and a numeral would imply otherwise. The appendices take their letters (A–F) in the numeral position.

**2.3 Numerals alternate sides.** Left on Parts I, III, V and Appendices A, C, E; right on Parts II, IV, VI and Appendices B, D, F. The Prologue's word sits left. In the reference build this is `flex-direction:row-reverse` applied via the `data-part` attribute.

**2.4 Heading hierarchy follows the source.** Numbered sections (§0.3, I.7, II.6, III.5, IV.4, V.7, VI.5, A.3, B.2, C.4) are second level; their subsections third level. Index every Part to the same depth.

**2.5 Table of contents.** Three levels, all fourteen top-level sections, every numbered section and every named subsection. The source contains **215 linked entries** and all of them must appear, each linked to a live anchor.

**2.6 Persistent sidebar navigation** across the fourteen sections, with a current-section indicator.

**2.7 Anchors on every heading at every level.** Cross-references in the text ("Part II established…", "see Appendix C", "F.2 note 6") should be live links where the target is unambiguous.

---

## 3. TYPOGRAPHY AND TABLES

**3.1 Design system: Industry.** Barlow Condensed headings, Barlow body.

**3.2 Palette:** warm bone ground, warm dark ink, one deep accent. Ensure the accent is legible at 8pt — the evidence labels use it.

**3.3 Tabular numerals are mandatory** in every table and stat component. Appendix E is a register of governing figures across six currencies and four decades; proportional numerals will misalign it and defeat its purpose.

**3.4 Wide tables.** Appendix A's six-jurisdiction matrices, Appendix B's eleven-instrument comparison and Appendix C's case-coding table are wide. Handle in this order: full-bleed or landscape on their own page; horizontal scroll within the container; reduced type size. **Never drop columns and never split a table's columns across stacked halves** — a jurisdiction matrix missing a jurisdiction is worse than useless.

**3.5 Evidence labels** as small typographic tags in the accent colour. Give **UNKNOWN** a distinct treatment: it appears 30 times as a deliberate epistemic statement, not an omission, and the document's credibility depends on the reader seeing it as such.

**3.6 Foreign-language terms** may be set in italic on first appearance within a section, but must not be italicised inside tables where it would disrupt alignment.

**3.7 Measure** capped at roughly 65–75 characters for body text.

---

## 4. FIGURE MANIFEST — build all fourteen

Fourteen figures are specified below **with their data**. Build every one, numbered, captioned, and placed in the section named. Do not substitute, omit or invent alternatives, and do not replace a specified figure with a table.

### Figure 1 — The Cooperative Ownership Test
**Place in:** Prologue §0.2 · **Type:** two-axis diagram

Hansmann's framework: ownership goes to the patron class minimising the sum of **market-contracting costs** (market power, asymmetric information, lock-in, long-term contracting) plus **ownership costs** (monitoring, collective decision-making with heterogeneous preferences, risk-bearing). Show why banking sits in the customer-ownership quadrant.

**Caption:** "Ownership form is predictable from economics, not ideology. Banking sits where customer contracting is costly and customers are homogeneous."

### Figure 2 — Cook's Five Problems
**Place in:** Prologue §0.3 · **Type:** five-panel diagram

Free-rider (common property) · Horizon · Portfolio · Control · Influence costs. Each with its one-line mechanism.

**Caption:** "All five stem from one fact: residual claims that are non-tradable and ill-defined. Fix tradability and you mitigate all five — at a cost in cooperative purity."

### Figure 3 — The Redemption Paradox
**Place in:** Part II, §II.3 · **Type:** circular tension diagram

A member share redeemable at par is attractive to members but is a **liability** under IFRIC 2 and fails CRR Article 29. Make it non-redeemable and it becomes **capital** — but the member loses the right that made membership attractive.

**Caption:** "An instrument is capital to precisely the extent that it is not really the member's to reclaim."

### Figure 4 — The Growth Arithmetic
**Place in:** Part II, §II.2 · **Type:** two-line chart over time

g\* = b × ROE. Plot a cooperative retaining all surplus at 20% ROE from ₦200m against the **₦5bn National MFB wall**. Annotate the crossing at roughly **18 years**. Show an investor-owned rival issuing equity and clearing the wall immediately.

**Caption:** "₦200 million at 20% return on equity reaches ₦5 billion in about eighteen years. The regulatory capital wall cannot be climbed by retained earnings."

### Figure 5 — The Capital–Control Frontier
**Place in:** Part II, §II.7 · **Type:** scatter, X = external capital access, Y = member control retained

Plot all eleven instruments: retained patronage · non-withdrawable shares · permanent shares · subordinated member deposits · subordinated debt · preference shares · institutional protection scheme · **Rabobank Certificates** · investor members · listed vehicle over a mutual base · demutualisation.

**Caption:** "No instrument escapes the trade-off; two bend the curve. Non-withdrawable shares improve permanence at zero control cost; the protection scheme relocates capital to the network."

### Figure 6 — The Asset Lock Across Six Jurisdictions
**Place in:** Part I, §I.8 · **Type:** ranked bar with anomaly marked

Quebec (strongest — indivisible *réserve générale*, disinterested devolution) · United States (procedural, via NCUA conversion rules) · Kenya (prudential reserves only) · Netherlands (none) · Nigeria (none) · **Germany (none — the anomaly)**.

**Caption:** "Germany has no statutory asset lock yet almost no demutualisation. The lock is the most direct neutraliser; where it is absent, audit federations and protection schemes must substitute."

### Figure 7 — The Substitute Monitor Ladder
**Place in:** Part III, §III.7 · **Type:** ranked ladder

Germany (compulsory Prüfungsverband + BVR + BaFin) · United States (NCUA + NCUSIF — strong on solvency, absent on member control) · Quebec (AMF) · Netherlands (DNB/ECB) · Kenya (SASRA, with perimeter gaps) · **Nigeria (effectively none)**.

**Caption:** "Where members cannot monitor, someone else must. The quality of that substitute is the best single predictor of whether a cooperative degenerates."

### Figure 8 — Olson's Collapse
**Place in:** Part III, §III.1 · **Type:** decay curve

Individual member's incentive to monitor, of order B/n, plotted against a flat private cost c. Mark Germany's **1,500-member** delegate threshold and, far to the right, Navy Federal at **15.1 million members**.

**Caption:** "The rational member's stake in governance falls as 1/n while the cost of participating does not. Democratic legitimacy is strongest exactly where the capital constraint says you cannot stay."

### Figure 9 — US Credit Union Consolidation
**Place in:** Part III, §III.2 · **Type:** dual-axis chart, 1969–2025

Institutions falling **23,866 → 4,287**; members rising to **144.7 million**; assets to **$2.433 trillion**. Inset: 455 institutions above $1bn hold ~78% of assets.

**Caption:** "Four-fifths of institutions gone, membership at an all-time high. Three-quarters of members now belong to billion-dollar institutions — the migration from high-legitimacy to low-legitimacy scale."

### Figure 10 — The Seven Capture Types
**Place in:** Part III, §III.5 · **Type:** taxonomy diagram

Managerial · Board/insider · Factional (net-saver vs net-borrower) · Staff · Regional · External · **Political** (marked as dominant in Kenya and Nigeria).

**Caption:** "Apathy is the enabling condition; capture is what fills the vacuum. In weak-institution jurisdictions the captor is often political."

### Figure 11 — The Three-Regime Problem
**Place in:** Part V, §V.1 · **Type:** three-column comparison

Cooperative society (state Registrar, NCSA 1993, no prudential capital) · CBN licence (BOFIA 2020, CAMA company, ₦50m–₦5bn) · IMTO (2024 Guidelines, USD 1m, **fintechs barred**).

**Caption:** "Three regimes, three supervisors, three capital requirements. A founder can get the cooperative structure right and still be unable to move money."

### Figure 12 — The Nigerian Capital Ladder
**Place in:** Part V, §V.4 · **Type:** ascending step chart

Super-Agent **₦50m** · PSSP ₦100m · PSS ₦250m · Unit MFB Tier 2 ₦50m / Tier 1 ₦200m · State MFB ₦1bn · MMO ₦2bn · Switching ₦2bn · National MFB ₦5bn · PSB ₦5bn. Mark **only MMO may hold customer funds**.

**Caption:** "Super-Agent at ₦50 million is the cheapest lawful door into the regulated payments chain — and the entry point for remittance payout."

### Figure 13 — The Recommended Two-Tier Architecture
**Place in:** Part VI, §VI.5 · **Type:** entity diagram

**Cooperative society** (members, one-member-one-vote, non-withdrawable shares, indivisible reserve, §27 20% cap) → holds **≥60%** of → **CAMA operating company** (CBN licences, professional management, technology) ← non-voting perpetual subordinated shares held by **outside investors**. Golden share and reserved matters marked on the control line. Reference: Crédit Agricole's SAS Rue La Boétie at **62.45%**; NPF Microfinance Bank at **~62.6%**.

**Caption:** "Economics to investors, control to members. The lock must be installed before investors hold the economic majority — retrofitting is not available."

### Figure 14 — The Failure Modes, Coded
**Place in:** Appendix C, §C.5 · **Type:** matrix, cases × modes × Cook problems

Seventeen cases against four modes (demutualisation, absorption, degeneration, insolvency) and five Cook problems. Highlight **control** as most frequently implicated, and the three anchor cases: UK building societies, the Co-operative Bank, KUSCCO.

**Caption:** "Control appears most often, and the most destructive cases — KUSCCO, the Co-operative Bank, the US corporates — are control failures, not horizon failures."

---

## 5. STAT TILE MANIFEST — build all twelve

Place the first six in the front matter; distribute the rest at the Part openings indicated.

| # | Value | Label | Place |
|---|---|---|---|
| 1 | **Six** | jurisdictions compared | Front matter |
| 2 | **Five** | of Cook's property-rights problems, not four | Front matter |
| 3 | **Four** | ways a cooperative dies | Front matter |
| 4 | **1889** | the Genossenschaftsgesetz, still in force | Front matter |
| 5 | **~77,600** | words | Front matter |
| 6 | **Ø** | Nigerian cooperatives with a statutory asset lock | Front matter |
| 7 | **1,500** | members — where German law says plenary democracy ends | Part III |
| 8 | **23,866 → 4,287** | US credit unions, 1969 to 2025 | Part III |
| 9 | **KSh 13.3bn** | lost at KUSCCO, outside the supervisory perimeter | Part III |
| 10 | **~18 years** | to grow ₦200m into ₦5bn on retained earnings alone | Part II |
| 11 | **USD 1m** | IMTO minimum capital — and fintechs are barred | Part V |
| 12 | **~62.6%** | of NPF Microfinance Bank held by a cooperative society | Part VI |

---

## 6. KNOWN STRUCTURAL VARIANCE — do not "fix"

The Prologue and Part I use a **TL;DR / Key Findings / Details / Recommendations / Caveats** internal shape, while Parts II–VI use **numbered sections**. This variance is inherited from the commissioning sequence and has been left deliberately: normalising it would require rewriting content. Render both shapes faithfully. Do not restructure either to match the other, and do not add a TL;DR to Parts II–VI to create false symmetry.

---

## 7. ANTI-PATTERNS — build failures to avoid

- **Collapsing the fourteen top-level sections into fewer `h1`s.** Fatal to navigation.
- **Giving the Prologue a numeral.** It takes a word; that is the point.
- **Converting Appendices A or B to prose.** They are lookup instruments; the tables *are* the content.
- **Dropping or softening evidence labels**, particularly UNKNOWN. This document rests substantially on statute and inference across jurisdictions with wildly unequal evidence; removing the labels converts inference into assertion.
- **Corrupting non-ASCII characters.** German, French, Dutch and Yoruba terms and the ₦ symbol appear throughout.
- **Reusing the steel-blue or signal-red palettes** from the enterprise studies. This document is a different kind of thing and should look like one.
- **Treating length as a problem to be solved.** The length is the deliverable.

---

## 8. BUILD CHECKLIST

- [ ] ~77,600 words of body prose present
- [ ] ~40 tables, ~406 data rows, all rendered as tables
- [ ] Fourteen `h1` sections in the correct order
- [ ] Prologue opener carries a **word**, not a numeral; appendices carry letters
- [ ] Numerals alternate — I, III, V, A, C, E left; II, IV, VI, B, D, F right
- [ ] Three-level contents list, 215 entries, zero dead links
- [ ] Persistent sidebar with current-section indicator
- [ ] All fourteen figures built, numbered and captioned
- [ ] All twelve stat tiles placed
- [ ] Evidence labels intact in the accent colour; UNKNOWN distinctly treated
- [ ] Legal citations (§43a, §2(5), CRR Art. 29, 12 CFR 702) unbroken across lines
- [ ] Non-ASCII characters verified — German, French, Dutch, Yoruba, ₦ € £ $ KSh C$
- [ ] Tabular numerals active in all tables and stats
- [ ] Wide tables full-bleed or scrollable, no columns dropped
- [ ] Every heading carries a stable anchor; cross-references linked
- [ ] Warm palette, visibly distinct from the enterprise studies

---

*The specification ends here. The study follows in full.*

---

