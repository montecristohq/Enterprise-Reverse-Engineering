# BUILD SPECIFICATION — read this before rendering

This document contains a complete five-volume enterprise study of approximately **38,000 words**. What follows is a binding specification for how it must be rendered. It is not editorial guidance. Every clause is a requirement.

Render as a **screen document with a persistent sidebar** — not a paginated print document. Use the **Industry** design system: Barlow Condensed for headings, Barlow for body, `ui-monospace` for numerals.

**Palette for this subject.** A **bone or paper ground with deep slate text and a single deep-teal accent.** The register should be sober and bank-like rather than fintech-bright: this is a study of a licensed credit institution, and the visual language should say so.

**Three palette prohibitions.** Do not reuse the **steel-blue** (`#5980a6`) of the Wise, Atruvia, DZ BANK and Robinhood studies. Do not reuse the **signal-red** (`#c1352a`) of the Experian study. And **do not use Klarna's brand pink** (`#FFA8CD`) — the study is critical of its subject in places and should not wear the subject's livery, exactly as the Robinhood specification prohibited that company's brand green.

---

## 1. PRESERVATION CONTRACT — non-negotiable

**1.1 Every word is retained.** Approximately 38,000 words. Do not summarise, condense, abridge, truncate or paraphrase any section.

**1.2 Every table renders as a table.** There are **22 tables containing 218 data rows**. Appendix B (the canonical figures register) and Appendix C (the three reporting entities) are the document's lookup instruments; converting them to prose destroys their function. Do not drop columns to make a table fit; see §3.4.

**1.3 Every evidence label is retained in place.** The six labels appear **150 times**: CONFIRMED FACT (77), COMPANY CLAIM (25), UNKNOWN (21), ANALYTICAL INFERENCE (20), THIRD-PARTY ESTIMATE (4), HYPOTHESIS (3). They are load-bearing for a specific reason set out in the front matter: **this subject's own operational claims required correction**, and the labels are how the study separates what Klarna asserts from what is established.

**1.4 Financial figures, currency symbols and citations render intact.** Do not break these across lines: `$13,003m`, `$(273)m`, `$(294)m`, `SEK 92,654m`, `SEK 500m`, `€1.4bn`, `£407m`, `2.74%`, `Directive (EU) 2023/2225`, `dnr 22-11505`, `556737-0431`. The document contains **33 euro signs, 11 pound signs and 22 Swedish characters** (ö, ä, å) — all must survive.

**1.5 No content in a collapsed, hidden or truncated state.**

**Verification:** the output must contain approximately 38,000 words, 22 tables and 218 data rows.

---

## 2. STRUCTURE CONTRACT

**2.1 Eleven top-level sections**, each rendering as an `h1` with a section-opening treatment:

1. Front matter (title, what this document is, conventions, contents)
2. Volume I — Corporate, Legal, Regulatory & Institutional Anatomy
3. Volume II — Product, the Merchant-Funded Customer Structure & Value-Flow Architecture
4. Volume III — Operations, the Decision Engine, Technology, Data, AI & Organisational Design
5. Volume IV — Financial Statements, Revenue Architecture, Credit Economics, Unit Economics, Regulatory Capital & Capital Allocation
6. Volume V — Management, Culture, Incentives, Competition, Moat, Risk & Strategic Evolution
7. Part VI — Cross-Volume Synthesis
8. Appendix A — Glossary
9. Appendix B — Canonical Figures Register
10. Appendix C — The Three Reporting Entities
11. Appendix D — Source Register and Reconciliation

**Do not collapse these into fewer top-level headings.**

**2.2 Numerals alternate sides.** Left on Volumes I, III, V and Appendices A, C; right on Volumes II, IV, Part VI and Appendices B, D.

**2.3 Heading hierarchy follows the source.** Numbered sections (I.7, II.3, III.10, IV.11, V.9, VI.2, B.4, C.3, D.2) are second level; their subsections third level.

**2.4 Table of contents.** Three levels, all eleven top-level sections, every numbered section and every named subsection. The source contains **116 linked entries** and all must appear, each linked to a live anchor.

**2.5 Persistent sidebar navigation** across the eleven sections, with a current-section indicator. **Build the sidebar from every heading at all three levels, not from the top-level sections alone** — a prior build in this programme shipped with a sidebar of 18 entries where 310 were available, and it made the longest document in the set nearly unnavigable.

**2.6 Anchors on every heading at every level.** Cross-references in the text ("Volume III established…", "see Appendix C", "Appendix D note 1") should be live links where the target is unambiguous.

---

## 3. TYPOGRAPHY AND TABLES

**3.1 Design system: Industry.** Barlow Condensed headings, Barlow body.

**3.2 Palette:** bone or paper ground, deep slate body text, deep-teal accent. Ensure the accent is legible at 8pt — the evidence labels use it.

**3.3 Tabular numerals are mandatory** in every table and stat component. Appendix B is a register of governing figures across three years, three entities and two currencies; proportional numerals will misalign it and defeat its purpose.

**3.4 Wide tables.** Appendix B.1 (the three-year group results), Appendix B.3 (the prudential capital comparison), Volume V's risk register and moat scorecard, and Volume IV's balance-sheet tables are wide. Handle in this order: full-bleed or landscape on their own page; horizontal scroll within the container; reduced type size. **Never drop columns.**

**3.5 Evidence labels** as small typographic tags in the accent colour. Give **UNKNOWN** a distinct treatment: it appears 21 times, and Appendix D.4 argues that the single most important gap in this study — the distributional question about who actually pays consumer fees — is unanswerable from public data. A reader should be able to find those admissions by flicking through.

**3.6 Currency discipline in the type.** Because this study runs in **two currencies across three entities**, set every `SEK` and `$` figure in tabular numerals and never allow a currency symbol to be orphaned from its figure across a line break. This is the single most likely place for a rendering error to create a factual misreading.

**3.7 Measure** capped at roughly 65–75 characters for body text.

---

## 4. FIGURE MANIFEST — build all fourteen

Fourteen figures are specified below **with their data**. Build every one, numbered, captioned, and placed in the section named. Do not substitute, omit or invent alternatives, and do not replace a specified figure with a table.

### Figure 1 — The Bank Inside the Fintech
**Place in:** Volume I, §I.2 · **Type:** entity map by permission and function, not ownership

**Klarna Group plc** (UK holding company, CRN 14467769, NYSE: KLAR — holds no licence, does not lend, takes no deposits, contracts with nobody) above **Klarna Holding AB** (Sweden, the prudential consolidation) above **Klarna Bank AB (publ)** (Sweden, corp. ID 556737-0431 — **the licensed credit institution**, holds the FI licence, takes deposits, lends, bears EEA credit risk). Alongside: EEA branches (including the German branch into which Sofort merged); **Klarna Financial Services UK Ltd** (FCA, FRN 987889); **Klarna Inc.** (Delaware — *not a lender*); and, outside the group in a distinct visual treatment, **WebBank** (Utah industrial bank — the US lender of record). Plus Klarna Australia and PriceRunner.

**Caption:** "The listed parent does nothing. The bank is Swedish. And in the United States, the lender is a company Klarna does not own."

### Figure 2 — Follow the Credit Risk, by Jurisdiction
**Place in:** Volume I, §I.10 · **Type:** two-column comparison

**EEA and UK:** consumer → Klarna Bank AB / KFSUK underwrites → **Klarna is lender of record** → Klarna owns the receivable → **Klarna bears the loss** → funded by insured deposits.
**United States:** consumer → Klarna Inc. underwrites → **WebBank is lender of record and originates** → **Klarna Inc. purchases the receivable** → Klarna bears predominant loss economics → funded by warehouse and forward flow, *not* deposits. Annotate the purpose: **interest-rate exportation** from Utah, avoiding state-by-state lending licences, with associated "true lender" risk.

**Caption:** "The same product, two entirely different legal machines. The US arrangement is the group's largest structural anomaly, and the July 2026 charter application exists to end it."

### Figure 3 — Why Merchants Pay
**Place in:** Volume II, §II.3 · **Type:** mechanism diagram with a scale comparison

Deferred payment at checkout → conversion uplift + average-order-value uplift + new-customer acquisition + purchase frequency → incremental merchant revenue → merchant pays **3.29–5.99% + $0.30**. Set against the **EU consumer-card interchange cap of 0.3%** (Regulation (EU) 2015/751) to show the order-of-magnitude difference. Annotate: the fee is priced as a **marketing and conversion service**, not as a payment rail — which is why a merchant tolerates ten to twenty times card interchange.

**Caption:** "Klarna charges roughly twenty times card interchange because it is not selling a payment rail. It is selling completed sales."

### Figure 4 — The Merchant-Funded Structure
**Place in:** Volume II, §II.2 · **Type:** five-payer diagram

**Merchants** (the primary payer — 3.29–5.99%); **consumers** (pay nothing on the core product; pay late fees capped at £5/$7, interest on Fair Financing up to ~34% APR, the Klarna Plus subscription, and FX); **advertisers** (merchants again, paying for placement); **card networks** (interchange, ~1%); **depositors** (supplying funding, receiving a rate below the lending yield). Annotate the verdict: the consumer is **bait** for Pay-in-4 and Pay-in-30, **customer** for Fair Financing, and **supplier** for deposits — often simultaneously.

**Caption:** "The consumer is the bait, not the customer — except on Fair Financing, where the answer flips."

### Figure 5 — The Velocity of the Book
**Place in:** Volume II, §II.6 · **Type:** duration comparison, the study's signature figure

Two horizontal bars on the same time axis. **Klarna: ~40 days**, repeating **~9 times** across a year. **A revolving credit card: ~365 days**, once. Beneath each, the average balance per consumer: **$80** against **~$6,730**. Annotate: the same annual volume, one-ninth the balance sheet.

**Caption:** "This single comparison is why Klarna must not be analysed as a credit card. Everything else in the economics follows from it."

### Figure 6 — The Decision Engine
**Place in:** Volume III, §III.2 · **Type:** process map with a latency budget

Consumer selects Klarna → identification and matching (national identifier where available; device and email where not) → feature retrieval (Kafka event stream → DynamoDB feature store, updated in real time) → **Credit Model** (ML default-probability score) + **Underwriting Policy** (deterministic rules, compliance hard-rejects) → limit assignment → fraud screen → affordability check where regulation requires → approve or decline. Mark the **sub-second latency budget** and annotate what it forecloses: no human review, no document verification, no slow external check.

**Caption:** "Roughly 3.4 million times a day, in under a second, on a population that is substantially thin-file. This is the hardest thing Klarna does."

### Figure 7 — The AI Substitution Episode
**Place in:** Volume III, §III.10 · **Type:** annotated timeline with a correction

December 2023 hiring freeze → 27 February 2024 the joint OpenAI announcement ("2.3 million conversations, two-thirds of chats, **the equivalent work of 700 full-time agents**, resolution time 11 minutes to under 2, a projected $40m profit improvement") → August 2024 the enterprise-software claims → **8 May 2025 the chief executive concedes cost was "a too predominant evaluation factor" and quality suffered** → rehiring of human agents. Beneath, the correction in a distinct treatment: the 700 figure was **avoided outsourced-contractor workload against a base of ~3,000 agents, not 700 redundancies**, and the headcount fall came overwhelmingly from the freeze plus attrition.

**Caption:** "The most instructive operational episode in the study — and the reason every company claim in this document carries a label."

### Figure 8 — The Anti-Money-Laundering Failure
**Place in:** Volume III, §III.8 · **Type:** finding-by-finding post-mortem

The five Finansinspektionen findings (decision of 11 December 2024, dnr 22-11505, period 1 April 2021 – 31 March 2022): no assessment of how products could be abused; the merchant-of-record distribution channel unassessed despite 12.2% of merchant income; 61 police reports unanalysed; **CDD triggered at 60 transactions where the regulator's benchmark is 12**; no model-risk routine. Highlight the decisive finding: **all 100 of the highest-transacting non-KYC consumers made 59 transactions and received no due diligence**, and roughly **70 million of 79 million consumers were classed non-KYC**. Outcome: remark plus **SEK 500m**, about 20% of the statutory ceiling.

**Caption:** "A checkout designed for a sub-second decision had compressed customer due diligence out of the flow entirely."

### Figure 9 — The Two Reporting Bases
**Place in:** Appendix C, §C.2 · **Type:** reconciliation diagram

**Klarna Group plc** (USD, IFRS-IASB, Form 20-F) beside **Klarna Holding AB Consolidated** (SEK, CRR/CRD, Pillar 3), with the four reconciling differences drawn between them: a different parent; intangibles deducted from CET1; subsidiary-issued AT1 and T2 included only up to the bank's minimum; and currency translation. Mark clearly: **capital ratios exist only on the right-hand side.**

**Caption:** "Three entities, two currencies, two frameworks. More errors are made here than anywhere else in reading this company."

### Figure 10 — The IFRS-to-Adjusted Bridge
**Place in:** Volume IV, §IV.8 · **Type:** waterfall, FY2025, USD millions

**Operating loss (230)** → + depreciation, amortisation and impairment **55** → + **share-based payments 157** → + restructuring and IPO costs **~83** → **Adjusted operating profit 65**. Emphasise the share-based-payments bar as the largest single item and annotate it: **a real economic cost borne by shareholders through dilution.**

**Caption:** "The gap between a $65 million profit and a $230 million loss is mostly one line: equity pay that is real."

### Figure 11 — The Capital Cost of a Dollar of GMV
**Place in:** Volume IV, §IV.11 · **Type:** stepped arithmetic, the study's quantitative payoff

Show the working: net receivables **$10.5bn** ÷ GMV **$127.9bn** = **~8%** of annual volume on balance sheet → standardised retail risk weight **75%** → REA per dollar of annual GMV **~8 US cents** → at a CET1 ratio of **15.7%** → **~1.25 US cents of CET1 per dollar of annual GMV** (≈0.7 cents at the regulatory minimum). Set beside a revolving card lender at roughly **nine times** that.

**Caption:** "One and a quarter cents of core equity capital per dollar of annual volume. This is the number the study exists to produce."

### Figure 12 — The Bank Balance Sheet, in Three Bands
**Place in:** Volume IV, §IV.9 · **Type:** three-band stacked diagram, 31 December 2025, USD millions

**Assets 18,797:** cash and central-bank balances 3,803; debt securities 1,518; consumer receivables at amortised cost 10,459 (Pay Later 6,127, Fair Financing 4,332); receivables at FVOCI 386 and FVPL 400; settlement and trade receivables 580; goodwill 685 and intangibles 383; other. **Liabilities 16,113:** **consumer deposits 13,003**; notes payable and borrowings 1,359; payables to merchants 736; other. **Equity 2,684**, with **Additional Tier 1 marked distinctly** — in equity under IFRS, not common equity.

**Caption:** "Ninety per cent of the funding is other people's savings, insured by the Swedish state. That is what makes this a bank."

### Figure 13 — The Moat Scorecard
**Place in:** Volume V, §V.9 · **Type:** scored bar chart, 0–5, deliberately asymmetric

Network effects **4** · Decision engine and repayment data **4** · Banking licence and deposit funding **4** · Scale economies **3** · Trust and brand **3** · Regulatory capability **3** · Cost position **3** · Consumer switching costs **2** · Merchant switching costs **2** · Advertising and comparison assets **2** · **Merchant integration estate 1**.

**Caption:** "Unlike the Robinhood study, the scepticism cuts both ways here. The network effect is genuine. The merchant estate — rented since the 2024 Checkout divestiture — is the weakest claimed moat in the set."

### Figure 14 — Rented Distribution
**Place in:** Volume V, §V.14 · **Type:** before-and-after diagram

**Before (pre-2024):** Klarna → Klarna Checkout → merchant → consumer. Klarna owns the relationship. **After:** Klarna → **Stripe / Adyen as merchant of record** → merchant → consumer. Annotate: a substantial portion of merchant revenue now arrives through an intermediary that can reprice, re-place or replace Klarna. Mark this as the **binding strategic constraint** and the mechanism of the bear case.

**Caption:** "Klarna solved distribution by selling the thing that owned the merchant. That trade is the central strategic question of the study."

---

## 5. STAT TILE MANIFEST — build all fourteen

Place the first six in the front matter; distribute the rest at the volume openings indicated.

| # | Value | Label | Place |
|---|---|---|---|
| 1 | **~40 days** | the life of a Klarna loan | Front matter |
| 2 | **9×** | times the book turns each year | Front matter |
| 3 | **118m / 966k** | consumers and merchants, end-2025 | Front matter |
| 4 | **Three** | reporting entities, two currencies | Front matter |
| 5 | **Five** | volumes, one question: who pays? | Front matter |
| 6 | **~38,000** | words | Front matter |
| 7 | **19 June 2017** | the day Klarna became a bank | Volume I |
| 8 | **20×** | Klarna's merchant fee against card interchange | Volume II |
| 9 | **$80** | average balance per consumer, against ~$6,730 on a card | Volume II |
| 10 | **60 vs 12** | the transaction trigger for due diligence, against the regulator's benchmark | Volume III |
| 11 | **700** | agents the AI was said to replace — none of them employees | Volume III |
| 12 | **1.25¢** | of core equity capital per dollar of annual volume | Volume IV |
| 13 | **$65m / $(230)m** | adjusted profit against IFRS operating loss | Volume IV |
| 14 | **1 / 5** | the merchant-estate moat score | Volume V |

---

## 6. THE RECONCILIATION — render it visibly

This assembly corrected one genuine error, resolved two confusions and left one unresolved. Three rendering requirements follow.

- **The corrected figure in Volume II** carries an inline note ("*corrected on assembly… see Appendix D note 1*"). Render that visibly — an accent-coloured inline correction mark, not italic text a reader will skim.
- **Appendix D notes 4 and 5** are genuine reconciliations rather than error corrections — the three "Kreditor" entities, and the difference between the reported "$35 billion" and the option package actually granted. Give both a distinct treatment; they resolve confusions present in the wider commentary on this company.
- **Appendix D note 6 (headcount) is unresolved.** Render it so that its unresolved status is visually obvious rather than reading as though it had been settled.

---

## 7. ANTI-PATTERNS — build failures to avoid

- **Collapsing the eleven top-level sections into fewer `h1`s.** Fatal to navigation.
- **Building the sidebar from top-level sections only.** This failure has already occurred once in this programme; do not repeat it.
- **Converting Appendix B or Appendix C to prose.** They are lookup instruments; the tables *are* the content.
- **Dropping or softening evidence labels**, particularly UNKNOWN and COMPANY CLAIM. This study's method includes correcting the subject's own account of itself, and the labels are how that is done.
- **Allowing a currency symbol to orphan from its figure.** With SEK and USD both in play, this creates factual misreadings.
- **Using Klarna's brand pink**, or reusing the steel-blue or signal-red palettes from earlier studies.
- **Treating length as a problem to be solved.** This is the shortest study in the programme because the disclosure base is thin, not because the subject is simple.

---

## 8. BUILD CHECKLIST

- [ ] ~38,000 words of body prose present
- [ ] 22 tables, 218 data rows, all rendered as tables
- [ ] Eleven `h1` sections in the correct order
- [ ] Numerals alternate — I, III, V, A, C left; II, IV, VI, B, D right
- [ ] Three-level contents list, 116 entries, zero dead links
- [ ] **Persistent sidebar built from all three heading levels**, with a current-section indicator
- [ ] All fourteen figures built, numbered and captioned
- [ ] All fourteen stat tiles placed
- [ ] Evidence labels intact in the accent colour; UNKNOWN distinctly treated
- [ ] Currency symbols never orphaned; 33 euro, 11 pound, 22 Swedish characters intact
- [ ] Tabular numerals active in all tables and stats
- [ ] Wide tables full-bleed or scrollable, no columns dropped
- [ ] Every heading carries a stable anchor; cross-references linked
- [ ] Inline correction in Volume II rendered visibly
- [ ] Appendix D notes 4 and 5 given a distinct treatment; note 6 visibly unresolved
- [ ] Bone-and-teal palette; no brand pink, no steel-blue, no signal-red

---

*The specification ends here. The study follows in full.*

---

