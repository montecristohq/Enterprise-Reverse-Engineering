# BUILD SPECIFICATION — read this before rendering

This document contains a complete five-volume enterprise study of approximately **41,000 words**. What follows is a binding specification for how it must be rendered. It is not editorial guidance. Every clause is a requirement.

Render as a **screen document with a persistent sidebar** — not a paginated print document. Use the **Industry** design system: Barlow Condensed for headings, Barlow for body, `ui-monospace` for numerals.

**Palette for this subject.** Cool graphite ground with a single high-chroma **signal amber** accent — the colour of a warning indicator on a trading desk. Suggested direction: a near-black cool graphite background, a light warm-grey body text, and amber for section numerals, evidence labels and figure emphasis.

**Two palette prohibitions.** Do not reuse the steel-blue (`#5980a6`) of the Wise, Atruvia and DZ BANK studies, or the signal-red (`#c1352a`) of the Experian study. And **do not use Robinhood's own brand green.** This study is critical of its subject; dressing it in the subject's livery would be a category error.

---

## 1. PRESERVATION CONTRACT — non-negotiable

**1.1 Every word is retained.** Approximately 41,000 words. Do not summarise, condense, abridge, truncate or paraphrase any section.

**1.2 Every table renders as a table.** There are **20 tables containing 215 data rows**. Appendix B (the canonical figures register) and Volume V's moat scorecard and risk register are the document's lookup instruments; converting them to prose destroys their function. Do not drop columns to make a table fit; see §3.4.

**1.3 Every evidence label is retained in place.** The six labels appear **266 times** across the study: CONFIRMED FACT (108), ANALYTICAL INFERENCE (67), COMPANY CLAIM (35), THIRD-PARTY ESTIMATE (23), UNKNOWN (22), HYPOTHESIS (11). They are load-bearing: this study distinguishes filings from company statements from inference throughout, and stripping the labels converts inference into assertion.

**1.4 Financial figures and citations render intact.** Do not break these across lines: `$4,473m`, `$2,522m`, `$1,883m`, `₦`-free but `$3.53bn`, `Rule 15c3-3`, `Rule 606`, `12 CFR Part 702`, `23 NYCRR 500`, `MiFIR (EU) 2024/791`, `$730,165`.

**1.5 No content in a collapsed, hidden or truncated state.**

**Verification:** the output must contain approximately 41,000 words, 20 tables and 215 data rows.

---

## 2. STRUCTURE CONTRACT

**2.1 Eleven top-level sections**, each rendering as an `h1` with a section-opening treatment:

1. Front matter (title, what this document is, conventions, contents)
2. Volume I — Corporate, Legal, Regulatory & Institutional Anatomy
3. Volume II — Product, the Inverted Customer Structure & Value-Flow Architecture
4. Volume III — Operations, Clearing Infrastructure, Technology, Data & Organisational Design
5. Volume IV — Financial Statements, the Two-Engine Revenue Architecture, Unit Economics, Regulatory Capital & Capital Allocation
6. Volume V — Management, Culture, Incentives, Competition, Moat, Risk & Strategic Evolution
7. Part VI — Cross-Volume Synthesis
8. Appendix A — Glossary
9. Appendix B — Canonical Figures Register
10. Appendix C — Enforcement Ledger
11. Appendix D — Source Register and Reconciliation

**Do not collapse these into fewer top-level headings.**

**2.2 Numerals alternate sides.** Left on Volumes I, III, V and Appendices A, C; right on Volumes II, IV, Part VI and Appendices B, D. In the reference build this is `flex-direction:row-reverse` applied via the `data-part` attribute.

**2.3 Heading hierarchy follows the source.** Numbered sections (I.7, II.3, III.12, IV.13, V.9, VI.2, B.4, C.1) are second level; their subsections third level.

**2.4 Table of contents.** Three levels, all eleven top-level sections, every numbered section and every named subsection. The source contains **117 linked entries** and all of them must appear, each linked to a live anchor.

**2.5 Persistent sidebar navigation** across the eleven sections, with a current-section indicator.

**2.6 Anchors on every heading at every level.** Cross-references in the text ("Volume II established…", "see Appendix C", "Appendix D note 1") should be live links where the target is unambiguous.

---

## 3. TYPOGRAPHY AND TABLES

**3.1 Design system: Industry.** Barlow Condensed headings, Barlow body.

**3.2 Palette:** cool graphite ground, light warm-grey body, signal-amber accent. Ensure the accent is legible at 8pt — the evidence labels use it.

**3.3 Tabular numerals are mandatory** in every table and stat component. Appendix B is a register of governing figures across six years and multiple bases; proportional numerals will misalign it and defeat its purpose.

**3.4 Wide tables.** Appendix B.1 (the six-year financial series), Volume V's moat scorecard and risk register, and Volume III's cost table are wide. Handle in this order: full-bleed or landscape on their own page; horizontal scroll within the container; reduced type size. **Never drop columns.**

**3.5 Evidence labels** as small typographic tags in the accent colour. Give **UNKNOWN** a distinct treatment: it appears 22 times as a deliberate epistemic statement, and Appendix D.4 argues that the one thing an outsider cannot see is internal decision process. The reader should be able to find those admissions by flicking through.

**3.6 Measure** capped at roughly 65–75 characters for body text.

---

## 4. FIGURE MANIFEST — build all fourteen

Fourteen figures are specified below **with their data**. Build every one, numbered, captioned, and placed in the section named. Do not substitute, omit or invent alternatives, and do not replace a specified figure with a table.

### Figure 1 — The Broker-Dealer Stack
**Place in:** Volume I, §I.2 · **Type:** entity diagram by function, not ownership

Robinhood Markets, Inc. (holding company, executes nothing) above: **Robinhood Financial LLC** (introducing broker — customer relationship, order capture; SEC/FINRA/SIPC; exempt from 15c3-3 under (k)(2)(ii)); **Robinhood Securities LLC** (clearing broker — assets, routing, clearing, settlement, margin, securities lending; NSCC/DTC/OCC member); **Robinhood Crypto LLC** (no SIPC, no FDIC); **Robinhood Derivatives LLC** (FCM; CFTC/NFA); Robinhood Money LLC; Robinhood Credit Inc. (via Coastal Community Bank); Robinhood Asset Management LLC; Robinhood U.K. Ltd (FCA); Robinhood Europe UAB (Bank of Lithuania); Bitstamp; TradePMR.

**Caption:** "The parent executes nothing. The customer relationship and the customer's assets sit in two different companies, and only one of them bears settlement risk."

### Figure 2 — What a Customer Actually Owns
**Place in:** Volume I, §I.5 · **Type:** four-column protection matrix

Securities → RHS → Rule 15c3-3 + **SIPC** ($500k, incl. $250k cash) + excess private insurance. Swept cash → partner banks → **FDIC pass-through** ($2.5m individual / $5m joint), **not SIPC**. Spending account → Robinhood Money → FDIC pass-through, not SIPC. **Crypto → RHC → neither SIPC nor FDIC.** Futures → RHD → CFTC segregation, not SIPC.

**Caption:** "One app, four legal regimes. The crypto column is the one customers most reliably misunderstand."

### Figure 3 — The Enforcement Ledger, Plotted
**Place in:** Volume I, §I.11 · **Type:** timeline with penalty magnitude on the vertical

FINRA Dec 2019 $1.25m · SEC Dec 2020 $65m · FINRA Jun 2021 $70m · NYDFS Aug 2022 $30m · Massachusetts 2024 $7.5m · SEC Jan 2025 $45m (**with admissions**) · FINRA Mar 2025 $29.75m. Mark the June 2020 death of Alex Kearns and the January 2021 restrictions as unpriced events on the same axis.

**Caption:** "Eight actions in six years, with conduct in the most recent reaching into 2023 and 2024. The pattern is systemic, not episodic."

### Figure 4 — The Order as Product
**Place in:** Volume II, §II.2 · **Type:** four-payer diagram

Retail user (pays nothing in cash; pays in spread, forgone interest, subscription) → order → **Robinhood** → wholesale market maker (**pays PFOF**). Alongside: Gold subscribers (pay cash), margin and securities-lending borrowers (pay interest), partner banks (pay the sweep spread).

**Caption:** "The user is the product for equities and options, the customer for crypto and margin, and the supplier for cash and lendable stock — simultaneously."

### Figure 5 — Why Uninformed Flow Is Worth Paying For
**Place in:** Volume II, §II.3 · **Type:** mechanism diagram

Retail order (uninformed) → low adverse-selection risk → market maker can internalise and capture the spread safely → pays a rebate to the broker → funds "free" trading. Contrast the institutional path: informed flow → high adverse selection → no rebate. Reference Glosten–Milgrom (1985) and Kyle (1985).

**Caption:** "Retail flow is valuable precisely because it is uninformed. This is the mechanism that makes commission-free trading fundable."

### Figure 6 — The Same $1,000, Two Instruments
**Place in:** Volume II, §II.3 · **Type:** side-by-side comparison

$1,000 into a $25 stock → a 40-share order → roughly **8 cents** of equity PFOF. $1,000 into a $5 option → a 200-share (2-contract) order → roughly **80 cents** of options PFOF. Annotate: **roughly 10× for the same customer outlay.** Robinhood's own Rule 606 reports show options PFOF averaging $0.47–$0.50 per contract in 2019.

**Caption:** "Identical customer intent, ten times the revenue. This single ratio explains the direction of the entire product roadmap."

### Figure 7 — The Escalation Ladder
**Place in:** Volume II, §II.8 · **Type:** ascending ladder, twin-axis

Rungs: sign-up → funding → first equity trade → **options approval** → margin → crypto → Gold → retirement → credit card → futures and event contracts. Plot revenue-per-user rising against sophistication-required rising. Mark the options rung where the FINRA 2021 approval-bot findings and the Kearns case sit.

**Caption:** "The monetisation path and the risk path are the same path. Each rung earns more and demands more."

### Figure 8 — The Order-to-Settlement Machine
**Place in:** Volume III, §III.2 · **Type:** thirteen-step process map

Order capture (RHF) → pre-trade risk and buying-power check → collaring → smart order routing (RHS) → execution at wholesaler → drop copy → allocation to the customer ledger → tape and CAT reporting → submission to NSCC → **continuous net settlement** → settlement at DTC (T+1) → custody in street name → corporate actions. Mark the failure mode at each step from the enforcement record.

**Caption:** "Thirteen steps from a tap to a settled position. The enforcement record describes a failure at nine of them."

### Figure 9 — The Collateral Machine, 28 January 2021
**Place in:** Volume III, §III.3 · **Type:** waterfall across a single morning

Previous day's requirement $696m → **5:11 a.m. automated notice: ~$3bn deficit** (VaR ~$1.3bn + **ECP >$2.2bn**) → ~9:00 a.m. ECP waived → gross requirement ~$1.4bn → **net deposit ~$700m**. Annotate: the ECP formula was publicly available and had not been modelled.

**Caption:** "A published charge the firm had never modelled produced a demand it could not meet. The reconciled chain is at Appendix B.4."

### Figure 10 — Operating Leverage, Quantified
**Place in:** Volume III, §III.12 · **Type:** indexed multi-line chart, 2021–2025

Revenue 1,815 → 4,473 (rising). Technology & development 1,234 → 897 (**falling**). Operations 368 → 130 (**falling sharply**). Brokerage & transaction 158 → 211 (barely moving). Total operating expenses 3,456 → 2,379.

**Caption:** "Technology spend fell in absolute terms while platform assets grew roughly fivefold. Roughly two-thirds of that is structural leverage; the rest is the correction of admitted over-hiring."

### Figure 11 — The Two Engines
**Place in:** Volume IV, §IV.4 · **Type:** dual-stream diagram with a shared driver

Engine one: retail risk appetite → trades → PFOF → **transaction revenue $2,628m (59%)**. Engine two: retail risk appetite → balances (margin $16.8bn, sweep $32.8bn, lending $11.6bn) → **net interest revenue $1,514m (34%)**. Draw the shared input prominently.

**Caption:** "Two revenue streams, one master variable. The diversification is of sources, not of exposure."

### Figure 12 — The Broker-Dealer Balance Sheet
**Place in:** Volume IV, §IV.9 · **Type:** three-band stacked diagram, end-2025

Band one, **off balance sheet**: customer securities, options and crypto (the bulk of $324bn); cash sweep $32,786m. Band two, **on balance sheet but not the firm's property**: margin receivables $17,994m; payables to users $11,986m; securities loaned $11,626m; segregated cash $5,749m; fractional shares $3,782m matched by an identical repurchase obligation. Band three, **the firm's own**: corporate cash $4,261m; clearing deposits $702m; goodwill $385m; intangibles $168m. Totals: assets $38,137m, liabilities $28,986m, **equity $9,151m**.

**Caption:** "Roughly three-quarters is other people's money. Computing leverage on the reported totals is the first analytical trap."

### Figure 13 — The Moat Scorecard
**Place in:** Volume V, §V.9 · **Type:** scored bar chart, 0–5

Regulatory assets and multi-entity capability **4** · Proprietary technology and self-clearing **4** · Scale economies **3** · Distribution **3** · Installed base **3** · Cost position **3** · Brand **2** · Ecosystem **2** · Learning curves **2** · Network effects **1** · Trust **1** · **Switching costs 1** · Data **1**.

**Caption:** "Five of the moats most commonly credited to Robinhood — network effects, brand, trust, switching costs and data — do not survive testing. ACATS makes account transfer straightforward."

### Figure 14 — The Cohort-Ageing Flywheel
**Place in:** Volume V, §V.13 · **Type:** circular flywheel with the key series inset

Young customers acquired cheaply → deposit and trade → **assets accumulate** → net interest and more products → higher retention and assets per customer → more of the same. Inset the governing series: average platform assets per funded customer rising toward roughly **$12,000** at end-2025 ($324bn ÷ 27.0m).

**Caption:** "The only credible path from cyclical business to durable institution — and the one series that would prove it is working."

---

## 5. STAT TILE MANIFEST — build all fourteen

Place the first six in the front matter; distribute the rest at the volume openings indicated.

| # | Value | Label | Place |
|---|---|---|---|
| 1 | **$0** | commission on a trade | Front matter |
| 2 | **27.0m** | funded customers | Front matter |
| 3 | **$324bn** | total platform assets | Front matter |
| 4 | **Five** | volumes, one question: who pays? | Front matter |
| 5 | **8** | material enforcement actions, 2019–2025 | Front matter |
| 6 | **~41,000** | words | Front matter |
| 7 | **$34.1m** | of customer harm found by the SEC, net of commission savings | Volume I |
| 8 | **10×** | the PFOF on an option versus the same dollar in stock | Volume II |
| 9 | **$730,165** | the balance Robinhood displayed to Alex Kearns | Volume II |
| 10 | **~$3bn** | the collateral demand at 5:11 a.m. on 28 January 2021 | Volume III |
| 11 | **14 million** | accounts approved by an automated identity check with red flags | Volume III |
| 12 | **$1.1–1.5bn** | normalised through-cycle net income, against $1,883m reported | Volume IV |
| 13 | **59% / 34%** | transaction and net interest share of FY2025 revenue | Volume IV |
| 14 | **1 / 5** | switching-costs moat score, out of five | Volume V |

---

## 6. THE RECONCILIATION — render it visibly

This assembly corrected one genuine error and reconciled four apparent conflicts across the five volumes. Two rendering requirements follow.

- **The corrected figure in Volume V** carries an inline note ("*corrected on assembly… see Appendix D note 1*"). Render that note visibly — an accent-coloured inline correction mark, not plain italic text a reader will skim past.
- **Appendix B.4** (the January 2021 reconciled chain) should render as a prominent stepped table or waterfall, because the apparent inconsistency between the $3bn, $3.7bn, $1.4bn and $700m figures has caused genuine confusion in the wider commentary, and this table resolves it.

---

## 7. ANTI-PATTERNS — build failures to avoid

- **Collapsing the eleven top-level sections into fewer `h1`s.** Fatal to navigation.
- **Converting Appendix B or the moat scorecard to prose.** They are lookup instruments; the tables *are* the content.
- **Dropping or softening evidence labels**, particularly UNKNOWN. This study rests substantially on inference from a rich but incomplete record; removing the labels converts inference into assertion.
- **Using Robinhood's brand green.** The study is critical of its subject and should not wear its livery.
- **Reusing the steel-blue or signal-red palettes** from the earlier studies.
- **Rendering the enforcement ledger as a mere list.** It is the behavioural evidence base of Volume V's culture analysis and should read as such.
- **Treating length as a problem to be solved.** The length is the deliverable.

---

## 8. BUILD CHECKLIST

- [ ] ~41,000 words of body prose present
- [ ] 20 tables, 215 data rows, all rendered as tables
- [ ] Eleven `h1` sections in the correct order
- [ ] Numerals alternate — I, III, V, A, C left; II, IV, VI, B, D right
- [ ] Three-level contents list, 117 entries, zero dead links
- [ ] Persistent sidebar with current-section indicator
- [ ] All fourteen figures built, numbered and captioned
- [ ] All fourteen stat tiles placed
- [ ] Evidence labels intact in the accent colour; UNKNOWN distinctly treated
- [ ] Financial figures and rule citations unbroken across lines
- [ ] Tabular numerals active in all tables and stats
- [ ] Wide tables full-bleed or scrollable, no columns dropped
- [ ] Every heading carries a stable anchor; cross-references linked
- [ ] Inline correction in Volume V rendered visibly
- [ ] Appendix B.4 rendered as a stepped table or waterfall
- [ ] Graphite-and-amber palette; no brand green, no steel-blue, no signal-red

---

*The specification ends here. The study follows in full.*

---

