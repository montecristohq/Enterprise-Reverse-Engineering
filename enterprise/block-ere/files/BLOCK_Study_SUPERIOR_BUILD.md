# BUILD SPECIFICATION — read this before rendering

This document contains a complete fourteen-volume enterprise study of approximately **75,000 words**. What follows is a binding specification for how it must be rendered. It is not editorial guidance. Every clause is a requirement.

Render as a **screen document with a persistent sidebar** — not a paginated print document. Use the **Industry** design system: Barlow Condensed for headings, Barlow for body, `ui-monospace` for numerals.

**Palette for this subject.** A **warm grey ground with a deep ink and a single oxidised-copper accent** — the green-blue of weathered bronze, not bright teal. The register should be that of a long institutional report built to be worked from rather than read once.

**Four palette prohibitions.** Do not reuse the **steel-blue** (`#5980a6`) of the Wise, Atruvia, DZ BANK and Robinhood studies. Do not reuse the **signal-red** (`#c1352a`) of the Experian study. Do not reuse the **bone-and-teal** of the Klarna study. And do not use **Cash App green** or Square's black-and-white brand livery — the study is critical of its subject in several places and should not wear its colours, exactly as the Robinhood and Klarna specifications prohibited theirs.

---

## 1. PRESERVATION CONTRACT — non-negotiable

**1.1 Every word is retained.** Approximately **75,300 words**. Do not summarise, condense, abridge, truncate or paraphrase any section. This is the longest study in the programme after the Cooperative Encyclopedia.

**1.2 Every table renders as a table.** There are **32 tables containing 382 data rows**. Appendix B (canonical figures) and Appendix C (the transplant index) are the document's lookup instruments; converting them to prose destroys their function. Do not drop columns to make a table fit; see §3.4.

**1.3 Every evidence label is retained in place.** The six labels appear **296 times**: CONFIRMED FACT (108), ANALYTICAL INFERENCE (60), COMPANY CLAIM (52), UNKNOWN (48), THIRD-PARTY ESTIMATE (23), HYPOTHESIS (5). They are load-bearing for a stated reason: Volume X found that Block's operational and strategic narrative repeatedly required correction while its audited figures did not, and the labels are how the study keeps those apart.

**1.4 Every transplant verdict is retained and rendered distinctly.** See §4 — this is the document's defining visual system.

**1.5 Financial figures, currency symbols and citations render intact.** Do not break these across lines: `$7,289,018k`, `$13,836,622k`, `$11,719,494k`, `$10.36bn`, `₦50 million`, `₦10,000`, `€280,000`, `£27.92m`, `8,883 BTC`, `CERT 59177`. The document contains **60 naira signs, 5 euro signs and 9 pound signs** — all must survive.

**1.6 No content in a collapsed, hidden or truncated state.**

**Verification:** the output must contain approximately 75,300 words, 32 tables and 382 data rows.

---

## 2. STRUCTURE CONTRACT

**2.1 Twenty top-level sections**, each rendering as an `h1` with a section-opening treatment:

1. Front matter (title, what this document is, conventions, contents)
2. Volume I — Corporate, Legal & Entity Architecture
3. Volume II — The Regulatory Estate & the Bank
4. Volume III — Square: The Seller Ecosystem
5. Volume IV — Cash App: The Consumer Ecosystem
6. Volume V — The Credit Businesses
7. Volume VI — Operations, Technology & Data
8. Volume VII — The Money Movement Machine
9. Volume VIII — Financial Architecture & Segment Economics
10. Volume IX — Capital, Balance Sheet & the Bitcoin Position
11. Volume X — Management, Culture & Governance
12. Volume XI — Competition, Moat & the "One Block" Question
13. Volume XII — International Expansion & Market Entry
14. Volume XIII — The Abandonment Record
15. **Volume XIV — The Transplant Volume**
16. Appendix A — Glossary
17. Appendix B — Canonical Figures Register
18. Appendix C — The Transplant Index
19. Appendix D — Source Register
20. Appendix E — Reconciliation

**Do not collapse these into fewer top-level headings.**

**2.2 Volume XIV receives a distinguished opening.** It is the deliverable, not the fourteenth chapter. Give it a visibly weightier section opener than the other volumes.

**2.3 Numerals alternate sides.** Left on odd-numbered volumes and Appendices A, C, E; right on even-numbered volumes and Appendices B, D.

**2.4 Heading hierarchy follows the source.** Numbered sections (II.7, V.9, VII.9, XI.6, XIV.3) are second level; their subsections third.

**2.5 Table of contents.** Three levels. The source contains **252 linked entries** and all must appear, each linked to a live anchor.

**2.6 Persistent sidebar navigation with a current-section indicator. Build the sidebar from every heading at all three levels, not from the top-level sections alone.** This programme has already shipped one document with an 18-entry sidebar where 310 entries were available, and it made the longest study in the set nearly unnavigable. At 252 entries across 75,000 words this instruction is load-bearing.

**2.7 Anchors on every heading at every level.** Cross-references in the text — and there are many, since fourteen volumes cite each other constantly ("Volume VII established…", "see Appendix E note 1") — should be live links where the target is unambiguous.

---

## 3. TYPOGRAPHY AND TABLES

**3.1 Design system: Industry.** Barlow Condensed headings, Barlow body.

**3.2 Palette:** warm grey ground, deep ink body text, oxidised-copper accent. Ensure the accent is legible at 8pt — the evidence labels use it.

**3.3 Tabular numerals are mandatory** in every table and stat component. Appendix B is a register of governing figures across three years and two currencies; proportional numerals will misalign it and defeat its purpose.

**3.4 Wide tables.** Appendix B.1 (three-year group results), Appendix C (the sixty-one-row transplant index), Volume XIV.3 (three verdict tables), Volume V's product comparison and Volume XI's competitor matrix are all wide. Handle in this order: full-bleed or landscape on their own page; horizontal scroll within the container; reduced type size. **Never drop columns.**

**3.5 Evidence labels** as small typographic tags in the accent colour. Give **UNKNOWN** a distinct treatment — it appears 48 times, and Appendix E.4 argues that the single most important gap in this study is a metric Block has never published. A reader should be able to flick through and find the admissions.

**3.6 Currency discipline.** The study runs in **US dollars and naira**, with euro and sterling appearing in the international volume. Set every figure in tabular numerals and never allow a currency symbol to orphan from its figure across a line break. This is the likeliest place for a rendering error to create a factual misreading.

**3.7 Measure** capped at roughly 65–75 characters for body text.

---

## 4. THE VERDICT SYSTEM — the defining visual element

**This study's distinctive apparatus is not the evidence labels but the transplant verdicts.** ADOPT, ADAPT and REJECT appear throughout all fourteen volumes and constitute the actual deliverable.

**4.1 Three visually distinct states**, used consistently everywhere the words appear as verdicts:
- **ADOPT** — the affirmative state, in the copper accent at full strength.
- **ADAPT** — an intermediate state, visually distinguishable from both others at a glance.
- **REJECT** — a muted or struck state; **not alarm-red**, since a REJECT here is a useful finding rather than a failure.

**4.2 The master verdict table at Volume XIV.3** — three tables totalling sixty-one rows — is the single most important table in the document. Give it full-bleed treatment and apply the three states to every row.

**4.3 Appendix C** repeats all sixty-one as an alphabetical finding aid. Apply the same three states so the two views are visually consistent.

**4.4 The test to design against:** a reader should be able to flick through the document and locate every REJECT in under a minute. If they cannot, the verdict system has failed.

---

## 5. FIGURE MANIFEST — build all thirty

Thirty figures are specified below **with their data**. Build every one, numbered, captioned, and placed in the section named. Do not substitute, omit or invent alternatives, and do not replace a specified figure with a table.

**Three figures carry the study and receive full-page treatment: Figure 11 (the balance sheet in four bands), Figure 7 (the self-liquidating loan), and Figure 13 (one-and-a-half machines).**

### VOLUME I

**Figure 1 — The Three Rings**
*Entity map by regulatory perimeter, not ownership tree.* Ring 1, inside the bank's ring-fence: **Square Financial Services, Inc.** (Utah industrial bank, FDIC CERT 59177) alone. Ring 2, regulated but outside: the 48-plus state money-transmitter entity, the NYDFS BitLicense entity, **Cash App Investing LLC** (SEC/FINRA), **Squareup Europe Ltd** (UK), **Squareup International Limited** (Ireland), the **Afterpay and Clearpay** entities, **Verse Payments Lithuania UAB**. Ring 3, unregulated commercial: **Block, Inc.** (Delaware parent), **TIDAL** (Aspiro AB / TIDAL Music AS / Project Rising LLC), **Proto**, **Spiral**, **Bitkey**, **Square Capital LLC**, **Block XYZ Technology LLC** — **and the bitcoin treasury**.
**Caption:** "One subsidiary is inside the bank's perimeter. The bitcoin sits deliberately outside every ring."

**Figure 2 — The Ring-Fence Machinery**
*The contracts binding Ring 1 to Ring 3.* CALMA (≥20% leverage at all times, signed by SFS, Block **and Jack Dorsey personally**); Parent Company Agreement (FDIC examination reaching into the parent); tax-allocation held in trust; §§23A/23B and Regulation W (10% per affiliate, 20% aggregate, 100–130% collateral); source-of-strength obligation; majority-independent bank board with parent representation capped; a $50m third-party reserve deposit; three-year dividend bar.
**Caption:** "The ring-fence is contractual, not structural — and it binds the founder personally."

### VOLUME II

**Figure 3 — The Licence Ladder** *(infographic)*
*Seven rungs with dates, and the Nigerian equivalent alongside each.* 2009 payment facilitator under JPMorgan Chase / Paymentech → 2013 state money-transmitter licences (48+) plus FinCEN MSB → March 2016 bank-partner lending via **Celtic Bank** → June 2018 **NYDFS BitLicense** → ~2019 **Cash App Investing** broker-dealer → **1 March 2021 Square Financial Services** (applied Sept 2017, refiled Dec 2018, FDIC approval March 2020) → 31 January 2022 **Afterpay**. Alongside: the CBN ladder — Super-Agent ₦50m, PSSP ₦100m, Unit MFB ₦50–200m, State MFB ₦1bn, MMO ₦2bn, National MFB / PSB ₦5bn, IMTO USD 1m.
**Caption:** "Three and a half years and a contested FDIC vote for the sixth rung. Nigeria has no equivalent — but its ladder is shorter."

**Figure 4 — Permits and Forecloses**
*Matrix, seven rungs × six columns:* permits / forbids / capital or bonding / time to obtain / supervisory burden / **what it forecloses**. The last column is the one most analyses omit: the charter brought FDIC examination into the parent, a permanent 20% leverage cage, source-of-strength, and annual business-plan resubmission — none of which renting Celtic's charter carried.
**Caption:** "Every rung permits something and forecloses something. The right-hand column is the one that gets missed."

**Figure 5 — The Enforcement Ledger**
*Dated bar chart, ~$340m total.* CFPB $175m (16 Jan 2025 — $55m penalty + up to $120m redress); 48 state regulators $80m (15 Jan 2025); NYDFS $40m (10 Apr 2025); 46 state AGs $45m (8 Jul 2026); Washington State $20m (8 Jul 2026). Plus the **$240m DOJ reserve**, marked as unresolved.
**Caption:** "The deferred bill for scaling ahead of controls — roughly 3–4% of one year's gross profit for Block, and terminal for anyone smaller."

### VOLUME III

**Figure 6 — The Upmarket Drift**
*Line chart, mid-market GPV share (sellers above $500k annualised):* ~24% (2018) → 34% (Q3 2021) → 41% (Q3 2023) → **45% (Q3 2025)**. Overlay the take rate compressing: ~1.15% → ~1.13% of GPV, drifting 1–2bp a quarter. Annotate the FY2024 hardware loss: **$143.4m revenue against $236.4m cost = −$93.1m**.
**Caption:** "Square was built for the market stall and now earns from the mid-market. The fixed fee is material on a $15 ticket and immaterial on a $500 one."

### VOLUME V

**Figure 7 — The Self-Liquidating Loan** *(signature figure, full page)*
*The mechanism, step by step.* Merchant's daily card sales arrive → **a fixed percentage (the holdback, typically 9–13%) is deducted BEFORE settlement** → the remainder reaches the merchant. Show the state-contingency: slow week, smaller deduction; strong week, faster payoff. Mark the two backstops — **1/18th of principal every 60 days** and an **18-month final maturity** — and the linked-account debit if sales cannot cover the minimum. Annotate: average loan ~$10,000, repaid over ~9–10 months, loss rates ≤4%.
**Caption:** "The lender is first in line on the cash, not a creditor chasing it afterwards. This converts a credit-risk problem into a cash-flow-interception problem — and it is the deepest transferable idea in the study."

**Figure 8 — What Block Sees That a Bureau Does Not**
*Two-column comparison.* Block sees: gross payment volume, transaction frequency, average ticket, seasonality, new-versus-returning mix, revenue trajectory, recency, tenure, product mix, chargebacks, decline rates — and for consumers, inflows, direct-deposit status, balance behaviour. A bureau sees: off-platform obligations and total indebtedness. Annotate the complementarity: **Block cannot see leverage outside its own rail; the bureau cannot see current cash flow.**
**Caption:** "Real-time ability to repay, and the power to intercept it. What Block cannot see is what the borrower owes elsewhere."

**Figure 9 — The Four Credit Products**
*Table-diagram by lender of record.* **Square Loans** ($100–$350,000, factor rate ~1.10–1.16, ~10 months, avg ~$10,000; SFS now, Celtic 2016–2021, Square MCA 2014–2016). **Cash App Borrow** ($20–$500, flat 5% for ~4 weeks, avg <$100; SFS since March 2025, First Electronic before). **Afterpay** (pay-in-4 interest-free, avg ~$79; Pay Monthly 0–35.99% APR via First Electronic). **Square Credit Card** (Celtic Bank under an American Express licence).
**Caption:** "Four products, three lenders of record, and a lender that was not a Block entity for most of the company's history."

### VOLUME VII

**Figure 10 — Who Takes What From $100** *(nine-party trace)*
*A card-present transaction at a Square seller, Free plan, 2.6% + 15¢ = $2.75.* Cardholder pays $100 → **issuing bank** takes interchange ~$1.75–1.80 → **Visa/Mastercard** take assessment ~$0.13–0.16 plus scheme fees → **sponsoring acquirer (JPMorgan Chase)** → **processor (Paymentech)** → **Square as payment facilitator** takes the residual and controls settlement timing → **seller receives $97.25** next business day, or instantly for 1.75%. Annotate: Block's transaction gross profit is **~1.13–1.15% of GPV** — the headline rate is not the margin.
**Caption:** "Nine parties. The headline 2.6% is not Block's margin; roughly 1.15 points is."

**Figure 11 — The Balance Sheet in Four Bands** *(signature figure, full page)*
*31 December 2025, USD thousands.* **Band A — not Block's money:** customer funds 4,771,824; customers payable 6,805,366; settlements receivable 1,359,983. **Band B — the ring-fenced bank:** SFS at ~$1,354m assets, $757m loans, $421m deposits, ≥20% leverage cage. **Band C — the credit book:** loans held for investment 3,382,957 (from 365,062 a year earlier), allowance 382,900, consumer receivables 2,670,322, warehouse facilities 1,364,883. **Band D — the parent's own:** cash 6,564,092, securities ~707k, **bitcoin 777,515**, goodwill 11,849,018, intangibles 1,281,670, deferred tax 1,302,776. Against total equity ~22,169,882 and notes 7,289,018.
**Caption:** "Strip Band A and net corporate debt is about $1.4 billion against $22 billion of equity. Leverage computed on the reported totals is meaningless — this is the most misread balance sheet in the study."

**Figure 12 — Interchange: The Subsidy That Does Not Travel** *(infographic)*
*Six jurisdictions on one scale.* United States small-issuer exempt debit: **~$0.62 per transaction, 1.41% of value, uncapped**. United States large-issuer capped: ~$0.23. EU and UK under the Interchange Fee Regulation: **0.2% debit, 0.3% credit, no small-issuer exemption**. Australia: ~0.2% debit, 0.3% credit. Nigeria: **merchant service charge capped at 0.5% with a ₦10,000 ceiling**, the issuer's slice a fraction of that. Annotate what US interchange funds: free peer-to-peer, free cash-out, cashback, customer acquisition.
**Caption:** "The hidden engine of American consumer fintech. It does not exist in Nigeria — which is why every free feature needs a named paying line."

### VOLUME VI

**Figure 13 — One and a Half Machines** *(signature figure, full page)*
*Shared below, separate above.* **Shared spine:** AWS cloud; a 12-petabyte Databricks platform serving ~70 teams under Unity Catalog; one ML and underwriting engine (Cash App Borrow, Afterpay, Square Loans); shared risk and fraud infrastructure; internal tooling (goose). **Separate above:** Square seller login and Cash App login as distinct accounts; divergent language stacks; separate partner-bank boundary. **And in the gap, marked clearly: NO DEMONSTRATED PERSON-LEVEL CUSTOMER GRAPH.** Show Cash App Pay as a QR and deep-link bridge across the gap, not through it.
**Caption:** "Genuinely shared plumbing. Genuinely separate customers. The gap in the middle is what Volume XI adjudicates."

**Figure 14 — The Headcount Trajectory and the AI Claim**
*Stepped line with annotations.* ~13,000 peak (Q3 2023) → 12,000 cap (Nov 2023) → −1,000 (Jan 2024) → TIDAL and TBD cuts (late 2024) → −931 roles plus ~200 managers (March 2025) → **10,205 FTE at 31 Dec 2025** → **under 6,000** (February 2026 plan, >4,000 cut, ~$852m charges). Beneath, in a distinct treatment: the correction. Mizuho's Dan Dolev — "the vast majority of these cuts were probably not due to AI"; NBER Working Paper 34836 finding ~90% of surveyed executives reported no AI employment effect.
**Caption:** "A multi-year over-hiring correction with an AI narrative attached. The programme reached the same verdict on the same claim at Klarna."

**Figure 15 — The AML Failure, Finding by Finding**
*Five NYDFS and CFPB findings.* A suspicious-activity-report backlog growing **from 18,000 to over 169,000 alerts** (2018–2021); one SAR filed for $1.6m covering 91 subjects, 16,811 accounts and 19,518 transactions; **8,359 accounts opened by a single ring of ~25–30 subjects using falsified information**; bitcoin transfers to terrorism-linked wallets blocked only above 10% exposure; no live customer support from 2016 until February 2021. Outcome: the CFPB order mandating **24-hour live support — telephone ≥12 hours a day, chat ≥18** — as a permanent operating cost.
**Caption:** "Frictionless onboarding, priced. The mandated support floor is the permanent bill for a design choice."

### VOLUME VIII

**Figure 16 — The Segments Diverging**
*Two lines, FY2023–FY2025.* Cash App gross profit 4,323 → 5,239 → **6,340** (+21%). Square 3,130 → 3,600 → **3,940** (+9%). Annotate the two restatements: BNPL moved wholly into Cash App from Q4 2023; the FY2025 re-cut into Commerce Enablement / Financial Solutions / Bitcoin Ecosystem, which cuts across both segments.
**Caption:** "Not converging. Diverging — on growth, margin, capital intensity and cyclicality."

**Figure 17 — Bitcoin Distorts Revenue and Not Gross Profit**
*Paired bars.* FY2024: bitcoin ~$10,358m of $24,121m revenue (**42.3%**) at ~3% margin. FY2025: **$8,503m of $24,194m (~35%)**, revenue down 18% while everything else grew ~14%. Against gross profit, bitcoin is ~4%.
**Caption:** "Anchor on revenue and you misstate this business by roughly a factor of three."

**Figure 18 — Gross Profit per Cash App Active**
*Line, quarterly annualised.* $41 (Q4 2020) → $47 (Q4 2021) → ~$59 (Q4 2022) → ~$67 (Q4 2023) → $75 (Q3 2024) → $76 (Q4 2024) → $81 (Q1 2025) → $87 (Q2 2025) → **$94 (Q3 2025)**. Annotate that actives sat flat at 57m for six consecutive quarters — **the rise is deepening, not user growth.**
**Caption:** "More than doubled while the user count stood still."

**Figure 19 — The Ten-Times Multiple**
*The study's most striking number, given its own figure.* A **primary-banking active** — one who direct-deposits — generates **nearly ten times the gross profit of a peer-to-peer-only active**. Show the funnel: 59m monthly actives → 26m Cash App Card actives (~44%) → **9.3m primary-banking actives (~16%, +22% year on year)** → 2.5m paycheck-deposit actives → 5m Borrow actives.
**Caption:** "Direct deposit is the master conversion event. Everything upstream of it is acquisition; everything downstream is the business."

**Figure 20 — The Loss Line Decomposed**
*Stacked bar, FY2025, $1,337.2m (+68%).* Credit provision on loans held for investment **$561.4m**; provision on Afterpay and BNPL consumer receivables **$333.8m**; transaction, fraud and dispute loss **~$442m** (a reconciliation residual, marked as ANALYTICAL INFERENCE). Verdict beneath: **roughly two-thirds a growth signal** — CECL front-loading on a book that grew ninefold — **and one-third a control signal**.
**Caption:** "Rising provisions on a deliberately growing book are not deteriorating credit. The programme reached the same conclusion at Klarna."

### VOLUME IX

**Figure 21 — The Loan Book's Ninefold Jump**
*Bar with an annotation that matters.* Loans held for investment: $124.0m (2022) → $247.6m (2023) → $365.1m (2024) → **$3,383.0m (2025)**. Allowance: $23.1m → $382.9m. Annotate the cause: **a 1 July 2025 reclassification, not new financing** — Block began retaining Cash App Borrow, Afterpay Post-Purchase and SFS-originated loans rather than selling them.
**Caption:** "Not a financing event. An accounting decision to stop selling the loans — the opposite direction from Klarna."

**Figure 22 — The Capital Structure, Corrected**
*Seven note series.* Senior: $1.0bn 2026, $1.2bn 5.625% 2030, $1.0bn 2031, $2.0bn 6.50% 2032, $1.0bn 6.000% 2033. Convertible: $575m 2026, $575m 0.25% 2027. **Principal $7,350,000k; net carrying $7,289,018k.** Plus a $900m revolver (restated January 2026, undrawn). Mark clearly: **this refutes the "$0 long-term debt" claim — see Appendix E note 1.**
**Caption:** "Seven series, not zero. The single genuine error the assembly caught."

**Figure 23 — Bitcoin as Capital Allocation**
*Two panels.* Left: the position — ~$220m invested 2020–21, cost basis $292.6m, **8,883 BTC worth $777,515k at 31 December 2025**, roughly 0.35% of assets and 3.5% of equity. Right: the earnings volatility under fair-value accounting — FY2024 **+$421m**; FY2025 quarterly **−$93m, +$212m, +$60m, −$234m** for −$56m net; Q1 2026 −$173m.
**Caption:** "It worked in dollars and pollutes the earnings by $200 million a quarter. Small enough not to matter, large enough to distort — and legally impossible for a Nigerian holding company to copy."

**Figure 24 — The Goodwill Mountain**
*Composition and impairments.* Total goodwill $11,849,018k, of which **Afterpay $11,719,494k** — split 50/50 between the Square and Cash App reporting units and therefore **structurally untestable standalone**. Impairments taken: **TIDAL only** — $132.3m (Q4 2023) plus $73.5m (Q4 2024) against original goodwill of ~$197.9m, effectively a complete write-off.
**Caption:** "Never impaired is not the same as value-creating. The 50/50 allocation foreclosed the only honest test."

### VOLUME XII

**Figure 25 — The Natural Experiment** *(infographic, the study's second-most-important)*
*Two columns, one question.* **Square exported:** United States, Canada (Oct 2012), Japan (May 2013), Australia (2016), United Kingdom (Mar 2017), Ireland, France, Spain (2021) — international now **22% of GPV growing 35%** against 8% in the US, with Squareup Europe Ltd profitable (£83.95m turnover, £27.92m net income FY2024). **Cash App did not:** United Kingdom launched 2018 and **shut 15 September 2024**; Australia **cancelled June 2024** before launch; Verse acquired June 2020 and **wound down September 2023**; Clearpay exited the EU **25 August 2023**. Beneath, the weighted explanation: interchange and monetisation model ~50%, incumbency ~25%, free instant rails ~15%, commitment ~10%.
**Caption:** "The same company, the same capital, the same engineers. The seller model travelled and the consumer model did not — and the largest single reason is that one earns a fee it sets and the other earns interchange it does not."

**Figure 26 — Square's Local Pricing**
*Bar chart across eight markets.* United States 2.6% + 15¢; United Kingdom 1.75%; Australia 1.6%; Japan 3.25% at launch, 3.6% now; Ireland, France, Spain with a +1.5% foreign-card surcharge. Annotate: **Square charges less in the capped-interchange markets and is profitable there anyway, because low interchange lowers its cost of goods.**
**Caption:** "Capped interchange starves Cash App and subsidises Square. That asymmetry is the whole finding."

### VOLUME XIII

**Figure 27 — Wallet Against Cash**
*The sharpest natural experiment in Block's own history.* **Square Wallet** (Card Case 2011 → Pay With Square 2012 → discontinued 12 May 2014): hands-free pay-by-name, 75,000 merchants by March 2012, the Starbucks partnership costing **~$71–84.5m in processing losses** across three years, replaced by Square Order which itself died in 10 months. **Square Cash** (launched 15 October 2013): email a recipient, one linked debit card, no merchant required — now **$6.34bn of gross profit.** Beneath: the explanation. Wallet needed two sides to change behaviour simultaneously; Cash needed one user and pulled in the second.
**Caption:** "Two consumer products, months apart, same company. One-sided pairwise value compounds; two-sided behaviour change stalls."

**Figure 28 — The Abandonment Record by Cause**
*Five categories.* **Bought and sold well:** Caviar (2014, $44.3m per filing / ~$90m reported → **$410m**, closed 31 Oct 2019). **Bought and written off:** TIDAL ($237.3m, ~$206m impaired), Verse. **Built and failed:** Square Wallet, Square Order, Cash App UK, Cash App Australia, Clearpay EU, TBD/Web5. **Founder conviction not yet returned:** Proto (Core Scientific paid **$41.9m to exit**), Bitkey, Spiral. **Strategic retreats nobody announced:** the micro-merchant de-prioritisation, the geographic withdrawals, the two-ecosystem structure.
**Caption:** "Block kills cheap things fast and beloved things slowly. The one expensive conviction took three years and two impairments."

### VOLUME XI

**Figure 29 — The Moat Scorecard**
*Horizontal bars, 0–5, deliberately asymmetric.* Settlement control **5** · Seller data and underwriting **5** · Square software switching costs **4** · Square brand and self-serve **4** · Cash App network effects **4** · Primary-banking lock-in **4** · Shared data platform **4** · Banking licence and deposit funding **4** · Cash App Card interchange **3** · Regulatory and compliance capability **2** · Hardware **1** · **Claimed cross-ecosystem synergy 1**.
**Caption:** "Scepticism cutting both ways. Two moats score 5. The synergy the whole strategic narrative rests on scores 1."

### VOLUME XIV

**Figure 30 — The Build Order** *(the deliverable)*
*Six stages with tests, not instructions.* **Stage 0** governance and identity architecture — operator-veto in writing, entity perimeter drawn, one member identity specified, compliance officer appointed. **Stage 1** platform and anchor cooperative — *test: 60–70% of member money movements electronic and on-platform.* **Stage 2** operate under a licensed partner — *test: the fee paid away exceeds what could be earned holding the business.* **Stage 3** credit, collected at source — *test: losses below ceiling for two consecutive cohorts; stop if they double.* **Stage 4** Unit or State microfinance-bank licence, funded from NDIC-insured deposits. **Stage 5** remittance via agency. **Deferred indefinitely:** consumer P2P, hardware, anything sold as instant, speculative crypto, acquisitions.
**Caption:** "Cheap irreversible decisions first; everything purchasable deferred until there is money to purchase it with."

---

## 6. STAT TILE MANIFEST — build all sixteen

| # | Value | Label | Place |
|---|---|---|---|
| 1 | **Fourteen** | volumes, one question: what survives the journey? | Front matter |
| 2 | **61** | transplant verdicts | Front matter |
| 3 | **~75,000** | words | Front matter |
| 4 | **21 / 20 / 20** | ADOPT / ADAPT / REJECT | Front matter |
| 5 | **$10.36bn** | gross profit, FY2025 | Front matter |
| 6 | **Zero** | times Block has published a cross-ecosystem customer figure | Front matter |
| 7 | **$7,289,018k** | of notes — not the "$0" first reported | Volume I |
| 8 | **20%** | the leverage ratio the FDIC imposed on Block's bank | Volume II |
| 9 | **~$340m** | the bill for scaling ahead of compliance | Volume II |
| 10 | **45%** | of Square volume now from mid-market sellers | Volume III |
| 11 | **~10×** | what a direct-depositing customer is worth | Volume IV |
| 12 | **Before** | the borrower is paid — where the repayment is taken | Volume V |
| 13 | **1½** | machines | Volume VI |
| 14 | **0.5% vs 1.41%** | Nigeria's capped merchant charge against US exempt interchange | Volume VII |
| 15 | **8 vs 0** | countries Square exported to, against Cash App | Volume XII |
| 16 | **0.4%** | of Square volume from its biggest cross-ecosystem product | Volume XI |

---

## 7. THE RECONCILIATION — render it visibly

The assembly corrected two genuine errors and resolved five dual-value figures. Four rendering requirements follow.

- **Volume VIII's corrected long-term-debt figure** and **Volume XII's corrected Clearpay date** each carry an inline note ("*corrected on assembly… see Appendix E note 1/2*"). Render these as accent-coloured inline correction marks, not italic text a reader will skim past.
- **Appendix E.2** resolves five figures that have two legitimate values each — Caviar, Afterpay, the bank's balance sheet, the PPP lending and the restructuring charges. Give it a distinct treatment; these are the figures a reader is most likely to mis-cite.
- **Appendix E.3** presents five vintage series that are *not* conflicts. Render them so a reader does not mistake movement for disagreement.
- **Appendix E.4 and E.5** list what remains unknown, including the metric Block has never published and the Nigerian regulatory figures that need re-verification. Make the unresolved status visually obvious.

---

## 8. ANTI-PATTERNS — build failures to avoid

- **Collapsing the twenty top-level sections into fewer `h1`s.** Fatal to navigation at 75,000 words.
- **Building the sidebar from top-level sections only.** This failure has already occurred once in this programme.
- **Rendering ADOPT / ADAPT / REJECT as plain text.** They are the deliverable and need their own visual system.
- **Converting Appendix B or Appendix C to prose.** They are lookup instruments; the tables *are* the content.
- **Treating Volume XIV as the last chapter.** It is the point of the exercise and should open accordingly.
- **Dropping or softening evidence labels**, particularly UNKNOWN and COMPANY CLAIM.
- **Allowing a currency symbol to orphan.** With dollars and naira both in play this creates factual misreadings.
- **Using Cash App green, Square's brand livery, or any prior study's palette.**
- **Treating length as a problem to be solved.** Fourteen volumes is what the transplant question required.

---

## 9. BUILD CHECKLIST

- [ ] ~75,300 words of body prose present
- [ ] 32 tables, 382 data rows, all rendered as tables
- [ ] Twenty `h1` sections in the correct order
- [ ] Volume XIV given a distinguished opening
- [ ] Numerals alternate — odd volumes and A, C, E left; even volumes and B, D right
- [ ] Three-level contents list, 252 entries, zero dead links
- [ ] **Persistent sidebar built from all three heading levels**, with a current-section indicator
- [ ] **ADOPT / ADAPT / REJECT rendered as three distinct states throughout**
- [ ] The sixty-one-row verdict tables at XIV.3 given full-bleed treatment
- [ ] All thirty figures built, numbered and captioned
- [ ] Figures 7, 11 and 13 given full-page treatment
- [ ] All sixteen stat tiles placed
- [ ] Evidence labels intact in the accent colour; UNKNOWN distinctly treated
- [ ] Currency symbols never orphaned; 60 naira, 5 euro, 9 pound characters intact
- [ ] Tabular numerals active in all tables and stats
- [ ] Wide tables full-bleed or scrollable, no columns dropped
- [ ] Every heading carries a stable anchor; cross-volume references linked
- [ ] Both inline corrections rendered visibly
- [ ] Appendix E.2 distinctly treated; E.4 and E.5 visibly unresolved
- [ ] Warm grey and oxidised copper; no brand livery, no prior study's palette

---

*The specification ends here. The study follows in full.*

---

# Block, Inc.

**An Enterprise Reverse-Engineering Study — with a Transplant Objective**

Fourteen volumes · Corporate and regulatory architecture · Two ecosystems · Credit, rails and operations · Financial and capital anatomy · Governance, competition and the abandonment record · The transplant synthesis

Research cut-off: 11 August 2026
Prepared by: Damascus Research
Seventh subject in the EREF programme, after Wise plc, Atruvia AG, the DZ BANK Group, Experian plc, Robinhood Markets, Inc. and Klarna

---

## What this document is, and how it differs from the six before it

A forensic reverse-engineering study of Block, Inc. (NYSE: XYZ, formerly Square, Inc.) — the holding company for the Square seller ecosystem, the Cash App consumer ecosystem, Afterpay, Square Financial Services, TIDAL, Proto and the bitcoin businesses.

**It differs from every prior subject in one decisive respect. This is a playbook extraction, not a neutral teardown.**

The six earlier studies asked how a company works. This one asks a harder question: **which of its mechanisms would survive being rebuilt in a different market, and which depend on institutions that market does not have.** Every volume therefore carries a transplant test and issues verdicts. Sixty-one of them, collected in Volume XIV.

The reader is a founder building a vertically integrated financial services group in Nigeria — a proprietary core-banking platform for cooperative societies, an anchor cooperative society, a remittance capability, and credit as a platform feature. Block was selected because it is the closest existing analogue to that architecture: a technology company that began with merchants nobody would underwrite, built a consumer business alongside, acquired its own bank, and now generates $10.36bn of annual gross profit.

| | Volume | The question it owns |
|---|---|---|
| **I** | Corporate, Legal & Entity Architecture | What is Block legally, and what keeps the bank ring-fenced from a commercial parent? |
| **II** | The Regulatory Estate & the Bank | How does a technology company acquire the right to hold, move and lend money? |
| **III** | Square: The Seller Ecosystem | Why does a small merchant choose Block, and what happens as they grow? |
| **IV** | Cash App: The Consumer Ecosystem | How do you acquire consumers at near-zero cost, and what do they become? |
| **V** | The Credit Businesses | How do you underwrite someone whose only credit file is the flow you already process? |
| **VI** | Operations, Technology & Data | Is it one machine or two? |
| **VII** | The Money Movement Machine | Where does a dollar go, and who takes a cut at each step? |
| **VIII** | Financial Architecture & Segment Economics | What does each ecosystem earn, per seller and per active? |
| **IX** | Capital, Balance Sheet & the Bitcoin Position | What funds this, and has the capital been well allocated? |
| **X** | Management, Culture & Governance | Who decides, and does the company do what it says? |
| **XI** | Competition, Moat & the "One Block" Question | Do the two ecosystems compound, or merely coexist? |
| **XII** | International Expansion & Market Entry | What happened when Block moved its own mechanisms abroad? |
| **XIII** | The Abandonment Record | What did Block try and stop, and why? |
| **XIV** | **The Transplant Volume** | **What survives the journey?** |
| **A** | Glossary | Payments, banking, credit and the vocabulary of two regulatory systems |
| **B** | Canonical Figures Register | The governing value for every material number |
| **C** | The Transplant Index | All sixty-one verdicts, by mechanism |
| **D** | Source Register | What the study rests on, and how claims were graded |
| **E** | Reconciliation | Where the volumes disagreed, and which governs |

**Recommended first pass.** Volume XIV (the synthesis — read it first, not last) → Volume V, section V.2 (flow-based underwriting and settlement-controlled repayment, the mechanism most likely to end up in the reader's build) → Volume VII, section VII.9 (the interchange finding, which reshapes the revenue model) → Volume XI, section XI.6 (the compounding verdict). The remaining volumes are reference-depth.

**A note on what the study concluded.** It did not find a roadmap. It found that Block's *mechanisms* transfer better than expected, its *economics* depend on American institutions that Nigeria lacks, and its *central strategic claim* — that two adjacent ecosystems compound — remains unproven after a decade and effectively unlimited capital. That last finding is uncomfortable, because the reader's architecture rests on the same assumption. It is also the most valuable thing here.

---

## Conventions governing the whole study

### Evidence classification

| Label | Meaning |
|---|---|
| **CONFIRMED FACT** | Directly supported by primary evidence — a filing, a regulatory order, a court opinion, a dated event |
| **COMPANY CLAIM** | Stated by Block but not independently verified. **The default for every operational, cultural and strategic assertion** |
| **THIRD-PARTY ESTIMATE** | Externally reported or estimated; not from filings |
| **ANALYTICAL INFERENCE** | Reasonably inferred from multiple known facts, with the reasoning shown |
| **HYPOTHESIS** | Possible, requiring further evidence |
| **UNKNOWN** | The evidence is insufficient — flagged, not papered over |

**Why the COMPANY CLAIM default is strict here.** Volume X examined four instances in which Block's public account required correction — the artificial-intelligence attribution for a 40% workforce reduction, the "strong product market fit" claim for Proto immediately before its only large customer paid $41.9m to exit, the abandonment framings that concealed competitive defeat, and the contested Cash App user metrics. It reached a settled position that governs the whole study: **the audited financial disclosure is reliable; the operational and strategic narrative is not.** Accept the ledger, test the story.

### Basis discipline

US GAAP, US dollars, 31 December year end, Form 10-K as a domestic filer.

**The series has been restated twice in three years, and a naive multi-year comparison will be wrong.** From Q4 2023 the entire buy-now-pay-later platform was reallocated from a 50/50 Square–Cash App split into Cash App alone. From FY2025 the revenue disclosure was re-cut into **Commerce Enablement, Financial Solutions and the Bitcoin Ecosystem** — categories that cut *across* both reportable segments. Volume XI assessed the second change as "more convenient than incidental," since it obscures precisely the seller-versus-consumer view the compounding question requires.

Non-GAAP measures — Adjusted EBITDA, Adjusted Operating Income, Adjusted Free Cash Flow, and the self-selected "Rule of 40" — are labelled, reconciled where disclosure permits, and never mixed with GAAP figures. **Adjusted Operating Income is the only one that keeps share-based compensation in, and is therefore the only one with full economic content.**

### Follow-the-Gross-Profit — the governing metric rule

Bitcoin sold to Cash App customers is booked as revenue at the **full sale amount**, with the cost of the bitcoin in cost of revenue. Bitcoin was roughly 42.3% of FY2024 revenue and about 35% of FY2025 revenue, at approximately a 3–4% margin.

**Any analysis anchored on revenue will misstate this business by roughly a factor of three.** Every volume anchors on gross profit and separates bitcoin wherever revenue appears.

### Follow-the-Legal-Entity

Block, Inc. is a Delaware commercial holding company that is **not** a bank holding company. Attribute every activity to the entity performing it, and note the parties that are **not** Block: the sponsoring acquirer, the card networks, Marqeta as issuer-processor, and the partner banks — Celtic, First Electronic, Sutton, The Bancorp and Lincoln Savings.

### The Transplant Test — the study's distinctive rule

Every material mechanism is asked the **Guinnane question**, carried from the reader's own prior work on cooperative institutions: *did this work because of the mechanism itself, or because of the institutional environment surrounding it?* Each receives a verdict:

| Verdict | Meaning |
|---|---|
| **ADOPT** | Works on its own logic; survives the move |
| **ADAPT** | The logic transfers but the implementation must change — and the volume states precisely what must change, and to what |
| **REJECT** | Depends on infrastructure, regulation or scale the target market lacks — and the volume names the dependency that kills it |

The American infrastructure stripped out before each verdict: ubiquitous card acceptance and mature interchange; ACH and instant rails; FDIC deposit insurance and the trust it manufactures; near-universal credit files; the Utah industrial-bank charter; deep capital markets for loan sales; and a single currency layered over state regimes.

**A REJECT is as valuable as an ADOPT.** Several are more so.

### Depth follows the subject

Sections are not of equal length. A section ends when its questions are answered.

---

## Contents

- [VOLUME I — Corporate, Legal & Entity Architecture](#volume-i-corporate-legal-entity-architecture)
  - [TL;DR](#tldr)
  - [Key Findings](#key-findings)
  - [Details](#details)
    - [I.1 Origin and corporate history](#i1-origin-and-corporate-history)
    - [I.2 The entity map by regulatory perimeter](#i2-the-entity-map-by-regulatory-perimeter)
    - [I.3 The intercompany architecture (the boundary machinery)](#i3-the-intercompany-architecture-the-boundary-machinery)
    - [I.4 Ownership, control and governance](#i4-ownership-control-and-governance)
    - [I.5 The acquisition record](#i5-the-acquisition-record)
    - [I.6 Litigation, investigations and governance controversies](#i6-litigation-investigations-and-governance-controversies)
    - [I.7 The bitcoin position as a corporate-structure question](#i7-the-bitcoin-position-as-a-corporate-structure-question)
    - [I.8 The transplant verdicts](#i8-the-transplant-verdicts)
    - [I.9 Volume I reconstruction](#i9-volume-i-reconstruction)
  - [Recommendations](#recommendations)
  - [Caveats](#caveats)
- [VOLUME II — The Regulatory Estate & the Bank](#volume-ii-the-regulatory-estate-the-bank)
  - [Block, Inc. (NYSE: XYZ, formerly Square, Inc.) — A Forensic Reverse-Engineering Study](#block-inc-nyse-xyz-formerly-square-inc-a-forensic-reverse-engineering-study)
    - [The Licence Ladder: How a Technology Company Acquired the Right to Hold, Move and Lend Money](#the-licence-ladder-how-a-technology-company-acquired-the-right-to-hold-move-and-lend-money)
  - [TL;DR](#tldr-1)
  - [KEY FINDINGS](#key-findings-1)
  - [DETAILS](#details-1)
    - [II.0 Basis and metric discipline](#ii0-basis-and-metric-discipline)
    - [II.1 The Ladder, Reconstructed (chronological)](#ii1-the-ladder-reconstructed-chronological)
    - [II.2 The Industrial Bank Decision (the pivotal section)](#ii2-the-industrial-bank-decision-the-pivotal-section)
    - [II.3 The Bank-Partner Era and Why It Ended (the section that matters most to the reader)](#ii3-the-bank-partner-era-and-why-it-ended-the-section-that-matters-most-to-the-reader)
    - [II.4 The Enforcement Record as a Cost of the Estate (dated ledger)](#ii4-the-enforcement-record-as-a-cost-of-the-estate-dated-ledger)
    - [II.5 The Cost of the Estate (quantified)](#ii5-the-cost-of-the-estate-quantified)
    - [II.6 What Each Rung Permits and Forecloses (matrix)](#ii6-what-each-rung-permits-and-forecloses-matrix)
    - [II.7 THE TRANSPLANT VERDICTS (with reasoning, against Nigerian conditions)](#ii7-the-transplant-verdicts-with-reasoning-against-nigerian-conditions)
    - [II.8 Volume II Reconstruction](#ii8-volume-ii-reconstruction)
  - [RECOMMENDATIONS](#recommendations-1)
  - [CAVEATS](#caveats-1)
- [VOLUME III — Square: The Seller Ecosystem](#volume-iii-square-the-seller-ecosystem)
    - [A Forensic Reverse-Engineering of Block, Inc. (NYSE: XYZ) — Playbook Extraction for a Nigerian Cooperative-Banking Founder](#a-forensic-reverse-engineering-of-block-inc-nyse-xyz-playbook-extraction-for-a-nigerian-cooperative-banking-founder)
  - [TL;DR](#tldr-2)
  - [Key Findings](#key-findings-2)
  - [Details](#details-2)
    - [III.1 The Seller Universe](#iii1-the-seller-universe)
    - [III.2 The Original Wedge — Hardware, Onboarding, Payment Facilitation](#iii2-the-original-wedge-hardware-onboarding-payment-facilitation)
    - [III.3 The Software Stack (the actual business)](#iii3-the-software-stack-the-actual-business)
    - [III.4 Land-and-Expand and Cohort Economics](#iii4-land-and-expand-and-cohort-economics)
    - [III.5 THE UPMARKET DRIFT (the central re-cut)](#iii5-the-upmarket-drift-the-central-re-cut)
    - [III.6 Retention, Churn and Seller Failure](#iii6-retention-churn-and-seller-failure)
    - [III.7 Acquisition and CAC](#iii7-acquisition-and-cac)
    - [III.8 International Square (seller-side only)](#iii8-international-square-seller-side-only)
    - [III.9 Competitive Position in Seller Payments](#iii9-competitive-position-in-seller-payments)
    - [III.10 THE TRANSPLANT VERDICTS](#iii10-the-transplant-verdicts)
    - [III.11 Volume III Reconstruction](#iii11-volume-iii-reconstruction)
    - [The Answers to the Volume's Owned Question](#the-answers-to-the-volumes-owned-question)
  - [Caveats](#caveats-2)
- [VOLUME IV — Cash App: The Consumer Ecosystem](#volume-iv-cash-app-the-consumer-ecosystem)
    - [A Playbook Extraction for a Nigerian Cooperative-Banking Founder](#a-playbook-extraction-for-a-nigerian-cooperative-banking-founder)
  - [TL;DR](#tldr-3)
  - [Key Findings](#key-findings-3)
  - [Details](#details-3)
    - [IV.1 The Consumer Universe](#iv1-the-consumer-universe)
    - [IV.2 The Acquisition Engine and Its True Net Cost](#iv2-the-acquisition-engine-and-its-true-net-cost)
    - [IV.3 The Product Ladder](#iv3-the-product-ladder)
    - [IV.4 The Conversion Funnel and the BNPL Distortion](#iv4-the-conversion-funnel-and-the-bnpl-distortion)
    - [IV.5 Free P2P: Business or Subsidy?](#iv5-free-p2p-business-or-subsidy)
    - [IV.6 Monetisation Depth and the Banking Ceiling](#iv6-monetisation-depth-and-the-banking-ceiling)
    - [IV.7 The Cost of Frictionless Onboarding](#iv7-the-cost-of-frictionless-onboarding)
    - [The Nigerian Transplant Context](#the-nigerian-transplant-context)
  - [IV.9 The Transplant Verdicts](#iv9-the-transplant-verdicts)
  - [IV.10 Volume IV Reconstruction](#iv10-volume-iv-reconstruction)
  - [Recommendations](#recommendations-2)
  - [Caveats](#caveats-3)
- [VOLUME V — The Credit Businesses](#volume-v-the-credit-businesses)
    - [An Institutional-Grade Forensic Reverse-Engineering Study of Block, Inc. (NYSE: XYZ, formerly Square, Inc.)](#an-institutional-grade-forensic-reverse-engineering-study-of-block-inc-nyse-xyz-formerly-square-inc)
  - [TL;DR](#tldr-4)
  - [Key Findings](#key-findings-4)
  - [Details](#details-4)
    - [V.1 — The Four Credit Products](#v1-the-four-credit-products)
    - [V.2 — The Core Mechanism: Underwriting on Proprietary Payment Flow](#v2-the-core-mechanism-underwriting-on-proprietary-payment-flow)
    - [V.3 — Credit Performance and Loss Experience](#v3-credit-performance-and-loss-experience)
    - [V.4 — Funding the Book](#v4-funding-the-book)
    - [V.5 — The Economics of the Credit Businesses](#v5-the-economics-of-the-credit-businesses)
    - [V.6 — Regulatory Architecture of Lending](#v6-regulatory-architecture-of-lending)
    - [V.7 — The Merchant Cash Advance Question](#v7-the-merchant-cash-advance-question)
    - [V.8 — Failure and Exception Paths](#v8-failure-and-exception-paths)
    - [V.9 — The Transplant Verdicts](#v9-the-transplant-verdicts)
    - [V.10 — Volume V Reconstruction](#v10-volume-v-reconstruction)
  - [Recommendations](#recommendations-3)
  - [Caveats](#caveats-4)
- [VOLUME VI — Operations, Technology & Data](#volume-vi-operations-technology-data)
    - [*A forensic reverse-engineering study — Volume VI of XIV. Basis: US GAAP, US dollars, 31 December year end, Form 10-K, unless stated. Evidence classes: CONFIRMED FACT / COMPANY CLAIM / THIRD-PARTY ESTIMATE / ANALYTICAL INFERENCE / HYPOTHESIS / UNKNOWN.*](#a-forensic-reverse-engineering-study-volume-vi-of-xiv-basis-us-gaap-us-dollars-31-december-year-end-form-10-k-unless-stated-evidence-classes-confirmed-fact-company-claim-third-party-estimate-analytical-inference-hypothesis-unknown)
  - [TL;DR](#tldr-5)
  - [Key Findings](#key-findings-5)
  - [Details](#details-5)
    - [VI.1 The Operating Model](#vi1-the-operating-model)
    - [VI.2 The Shared-Stack Question (Re-cut 1)](#vi2-the-shared-stack-question-re-cut-1)
    - [VI.3 The Risk, Fraud and Financial-Crime Estate — Enforcement Post-Mortem](#vi3-the-risk-fraud-and-financial-crime-estate-enforcement-post-mortem)
    - [VI.4 Customer Support Operations](#vi4-customer-support-operations)
    - [VI.5 Hardware Design, Supply Chain and Manufacturing](#vi5-hardware-design-supply-chain-and-manufacturing)
    - [VI.6 The Data Estate](#vi6-the-data-estate)
    - [VI.7 Engineering Culture and Open Source](#vi7-engineering-culture-and-open-source)
    - [VI.8 The AI Headcount Claim (Re-cut 2)](#vi8-the-ai-headcount-claim-re-cut-2)
    - [VI.9 Operational Resilience](#vi9-operational-resilience)
    - [VI.10 Transplant Verdicts (Nigeria)](#vi10-transplant-verdicts-nigeria)
    - [VI.11 Volume VI Reconstruction](#vi11-volume-vi-reconstruction)
  - [Recommendations](#recommendations-4)
  - [Caveats](#caveats-5)
- [VOLUME VII — The Money Movement Machine](#volume-vii-the-money-movement-machine)
  - [A Forensic Reverse-Engineering of Block, Inc. (NYSE: XYZ, formerly Square, Inc.)](#a-forensic-reverse-engineering-of-block-inc-nyse-xyz-formerly-square-inc)
    - [Where a Dollar Goes Between Payment and Usability — and Who Takes a Cut](#where-a-dollar-goes-between-payment-and-usability-and-who-takes-a-cut)
  - [TL;DR](#tldr-6)
  - [Key Findings](#key-findings-6)
  - [Details](#details-6)
    - [VII.1 The Acquiring Side — a Square card-present transaction, traced end to end](#vii1-the-acquiring-side-a-square-card-present-transaction-traced-end-to-end)
    - [VII.2 The Issuing Side — the reverse flow](#vii2-the-issuing-side-the-reverse-flow)
    - [VII.3 Settlement, Speed and the Price of Time](#vii3-settlement-speed-and-the-price-of-time)
    - [VII.4 Stored Value, Customer Funds and Float](#vii4-stored-value-customer-funds-and-float)
    - [VII.5 The Peer-to-Peer Rail](#vii5-the-peer-to-peer-rail)
    - [VII.6 The Bitcoin Rail](#vii6-the-bitcoin-rail)
    - [VII.7 Network Relationships and Dependency (ranked)](#vii7-network-relationships-and-dependency-ranked)
    - [VII.8 Where the Gross Profit Actually Comes From (decomposition)](#vii8-where-the-gross-profit-actually-comes-from-decomposition)
    - [VII.9 THE TRANSPLANT VERDICTS](#vii9-the-transplant-verdicts)
  - [Recommendations](#recommendations-5)
  - [Caveats](#caveats-6)
  - [Volume VII Reconstruction](#volume-vii-reconstruction)
- [VOLUME VIII — Financial Architecture & Segment Economics](#volume-viii-financial-architecture-segment-economics)
  - [TL;DR](#tldr-7)
  - [Key Findings](#key-findings-7)
  - [Details](#details-7)
    - [VIII.1 Multi-Year Financial History (with restatements flagged)](#viii1-multi-year-financial-history-with-restatements-flagged)
    - [VIII.2 The Two Segment P&Ls (segment-first — the first re-cut)](#viii2-the-two-segment-pls-segment-first-the-first-re-cut)
    - [VIII.3 Gross Profit Decomposition by Strand](#viii3-gross-profit-decomposition-by-strand)
    - [VIII.4 Unit Economics (the transferable core)](#viii4-unit-economics-the-transferable-core)
    - [VIII.5 Cohort Economics and Payback](#viii5-cohort-economics-and-payback)
    - [VIII.6 The Cost Architecture (FY2025, CONFIRMED unless noted)](#viii6-the-cost-architecture-fy2025-confirmed-unless-noted)
    - [VIII.7 Transaction and Loan Losses Decomposed (the third re-cut)](#viii7-transaction-and-loan-losses-decomposed-the-third-re-cut)
    - [VIII.8 Operating Leverage and the Non-GAAP Stack](#viii8-operating-leverage-and-the-non-gaap-stack)
    - [VIII.9 Cash Flow and Its Quality (CONFIRMED)](#viii9-cash-flow-and-its-quality-confirmed)
  - [VIII.10 The Transplant Verdicts (Nigeria)](#viii10-the-transplant-verdicts-nigeria)
  - [Recommendations](#recommendations-6)
  - [Caveats](#caveats-7)
  - [The Ten Most Important Conclusions](#the-ten-most-important-conclusions)
- [VOLUME IX — Capital, Balance Sheet & the Bitcoin Position](#volume-ix-capital-balance-sheet-the-bitcoin-position)
  - [Block, Inc. (NYSE: XYZ, formerly Square, Inc.) — A Forensic Reverse-Engineering Study](#block-inc-nyse-xyz-formerly-square-inc-a-forensic-reverse-engineering-study-1)
  - [TL;DR](#tldr-8)
  - [Key Findings](#key-findings-8)
  - [Details](#details-8)
    - [IX.1 The Hybrid Balance Sheet Teardown — Four Bands (all figures FY2025 10-K, 31 Dec 2025 vs 2024, US GAAP, US$ thousands)](#ix1-the-hybrid-balance-sheet-teardown-four-bands-all-figures-fy2025-10-k-31-dec-2025-vs-2024-us-gaap-us-thousands)
    - [IX.2 Funding the Loan Book](#ix2-funding-the-loan-book)
    - [IX.3 Capital Structure and Its History](#ix3-capital-structure-and-its-history)
    - [IX.4 The Bitcoin Position as Capital Allocation](#ix4-the-bitcoin-position-as-capital-allocation)
    - [IX.5 Goodwill, Intangibles and the Afterpay Verdict](#ix5-goodwill-intangibles-and-the-afterpay-verdict)
    - [IX.6 Capital-Allocation Scorecard](#ix6-capital-allocation-scorecard)
    - [IX.7 Returns on Capital (normalised)](#ix7-returns-on-capital-normalised)
    - [IX.8 Capital Adequacy, Liquidity and Stress](#ix8-capital-adequacy-liquidity-and-stress)
    - [IX.9 The Transplant Verdicts (Nigeria — CBN Financial Holding Company framework)](#ix9-the-transplant-verdicts-nigeria-cbn-financial-holding-company-framework)
    - [IX.10 Volume IX Reconstruction (answers)](#ix10-volume-ix-reconstruction-answers)
  - [Recommendations (for the Nigerian founder)](#recommendations-for-the-nigerian-founder)
  - [Caveats](#caveats-8)
- [VOLUME X — Management, Culture & Governance](#volume-x-management-culture-governance)
  - [Block, Inc. (NYSE: XYZ, formerly Square, Inc.)](#block-inc-nyse-xyz-formerly-square-inc)
  - [TL;DR](#tldr-9)
  - [Key Findings](#key-findings-9)
  - [Details](#details-9)
    - [X.1 Jack Dorsey — decision rights and revealed priorities](#x1-jack-dorsey-decision-rights-and-revealed-priorities)
    - [X.2 The Executive Team and Its Turnover](#x2-the-executive-team-and-its-turnover)
    - [X.3 The Management System](#x3-the-management-system)
    - [X.4 Board and Governance Architecture](#x4-board-and-governance-architecture)
    - [X.5 Compensation and Incentives](#x5-compensation-and-incentives)
    - [X.6 Declared versus Revealed Culture — the credibility verdict](#x6-declared-versus-revealed-culture-the-credibility-verdict)
    - [X.7 The dual-class verdict](#x7-the-dual-class-verdict)
    - [X.8 Transplant verdicts (Nigerian cooperative context)](#x8-transplant-verdicts-nigerian-cooperative-context)
    - [X.9 Reconstruction — the central question answered](#x9-reconstruction-the-central-question-answered)
  - [Recommendations](#recommendations-7)
  - [Caveats](#caveats-9)
- [VOLUME XI — Competition, Moat & the "One Block" Question](#volume-xi-competition-moat-the-one-block-question)
  - [A Forensic Reverse-Engineering of Block, Inc. (NYSE: XYZ, formerly Square, Inc.)](#a-forensic-reverse-engineering-of-block-inc-nyse-xyz-formerly-square-inc-1)
  - [TL;DR](#tldr-10)
  - [Key Findings](#key-findings-10)
  - [Details](#details-10)
    - [XI.1 The Competitive Universe](#xi1-the-competitive-universe)
    - [XI.2 Competitor Teardowns](#xi2-competitor-teardowns)
    - [XI.3 Why Block Wins Where It Wins](#xi3-why-block-wins-where-it-wins)
    - [XI.4 The Moat Scorecard (0–5)](#xi4-the-moat-scorecard-05)
    - [XI.5 The Replication Test](#xi5-the-replication-test)
    - [XI.6 The "One Block" Adjudication](#xi6-the-one-block-adjudication)
    - [XI.7 Porter's Five Forces](#xi7-porters-five-forces)
    - [XI.8 What Could Break Block](#xi8-what-could-break-block)
    - [XI.9 The Transplant Verdicts (Nigerian conditions)](#xi9-the-transplant-verdicts-nigerian-conditions)
  - [XI.10 Volume XI Reconstruction](#xi10-volume-xi-reconstruction)
  - [Recommendations](#recommendations-8)
  - [Caveats](#caveats-10)
- [VOLUME XII — International Expansion & Market Entry](#volume-xii-international-expansion-market-entry)
  - [Block, Inc. (NYSE: XYZ, formerly Square, Inc.) — A Forensic Reverse-Engineering Study](#block-inc-nyse-xyz-formerly-square-inc-a-forensic-reverse-engineering-study-2)
  - [TL;DR](#tldr-11)
  - [Key Findings](#key-findings-11)
  - [Details](#details-11)
    - [XII.1 The Market-by-Market Record (Square)](#xii1-the-market-by-market-record-square)
    - [XII.2 The Cash App International Record](#xii2-the-cash-app-international-record)
    - [XII.3 The Analysis — Why Square Travelled and Cash App Did Not](#xii3-the-analysis-why-square-travelled-and-cash-app-did-not)
    - [XII.4 What Had To Change Per Market](#xii4-what-had-to-change-per-market)
    - [XII.5 The Japan Case](#xii5-the-japan-case)
    - [XII.6 International Economics](#xii6-international-economics)
    - [XII.7 The Competitive Position Abroad](#xii7-the-competitive-position-abroad)
    - [XII.8 The Transplant Verdicts (Nigeria)](#xii8-the-transplant-verdicts-nigeria)
    - [XII.9 Volume XII Reconstruction](#xii9-volume-xii-reconstruction)
  - [Recommendations](#recommendations-9)
  - [Caveats](#caveats-11)
- [VOLUME XIII — The Abandonment Record](#volume-xiii-the-abandonment-record)
  - [A Forensic Reverse-Engineering of Block, Inc. (NYSE: XYZ, formerly Square, Inc.)](#a-forensic-reverse-engineering-of-block-inc-nyse-xyz-formerly-square-inc-2)
  - [TL;DR](#tldr-12)
  - [Key Findings](#key-findings-12)
  - [XIII.1 THE SQUARE WALLET CASE](#xiii1-the-square-wallet-case)
    - [What it was — Card Case → Pay With Square → Square Wallet](#what-it-was-card-case-pay-with-square-square-wallet)
    - [The Starbucks partnership](#the-starbucks-partnership)
    - [The discontinuation and Square Order](#the-discontinuation-and-square-order)
    - [What Square Cash did differently](#what-square-cash-did-differently)
    - [A defensible account of the divergence](#a-defensible-account-of-the-divergence)
  - [XIII.2 THE BOUGHT-AND-SOLD-WELL CATEGORY](#xiii2-the-bought-and-sold-well-category)
    - [Caviar (the one clean win)](#caviar-the-one-clean-win)
  - [XIII.3 THE BOUGHT-AND-WRITTEN-OFF CATEGORY](#xiii3-the-bought-and-written-off-category)
    - [TIDAL (the most expensive failure)](#tidal-the-most-expensive-failure)
    - [Verse](#verse)
  - [XIII.4 THE BUILT-AND-FAILED CATEGORY](#xiii4-the-built-and-failed-category)
  - [XIII.5 THE FOUNDER-CONVICTION CATEGORY](#xiii5-the-founder-conviction-category)
  - [XIII.6 THE STRATEGIC-RETREAT CATEGORY (the abandonments nobody announced)](#xiii6-the-strategic-retreat-category-the-abandonments-nobody-announced)
  - [XIII.7 THE CAPITAL ARITHMETIC](#xiii7-the-capital-arithmetic)
  - [XIII.8 THE PATTERN](#xiii8-the-pattern)
  - [XIII.9 THE TRANSPLANT VERDICTS](#xiii9-the-transplant-verdicts)
  - [XIII.10 VOLUME XIII RECONSTRUCTION](#xiii10-volume-xiii-reconstruction)
  - [Recommendations (staged, with thresholds)](#recommendations-staged-with-thresholds)
  - [Caveats](#caveats-12)
- [VOLUME XIV — The Transplant Volume](#volume-xiv-the-transplant-volume)
  - [The assumed starting position](#the-assumed-starting-position)
  - [XIV.1 What thirteen volumes found](#xiv1-what-thirteen-volumes-found)
  - [XIV.2 The compounding verdict — the spine of this volume](#xiv2-the-compounding-verdict-the-spine-of-this-volume)
    - [What the evidence showed](#what-the-evidence-showed)
    - [The verdict](#the-verdict)
    - [What it means for a four-layer architecture](#what-it-means-for-a-four-layer-architecture)
  - [XIV.3 The master verdict table](#xiv3-the-master-verdict-table)
    - [ADOPT — transfers on its own logic](#adopt-transfers-on-its-own-logic)
    - [ADAPT — the logic transfers, the implementation must change](#adapt-the-logic-transfers-the-implementation-must-change)
    - [REJECT — depends on institutions the target market lacks](#reject-depends-on-institutions-the-target-market-lacks)
  - [XIV.4 The five mechanisms worth the whole study](#xiv4-the-five-mechanisms-worth-the-whole-study)
  - [XIV.5 The five that do not transfer, and why it matters](#xiv5-the-five-that-do-not-transfer-and-why-it-matters)
  - [XIV.6 What Nigeria has that America does not](#xiv6-what-nigeria-has-that-america-does-not)
  - [XIV.7 The build order](#xiv7-the-build-order)
    - [Stage 0 — Before anything is built](#stage-0-before-anything-is-built)
    - [Stage 1 — The platform and the anchor cooperative](#stage-1-the-platform-and-the-anchor-cooperative)
    - [Stage 2 — Partnership, not licence](#stage-2-partnership-not-licence)
    - [Stage 3 — Credit as a platform feature](#stage-3-credit-as-a-platform-feature)
    - [Stage 4 — The deposit licence](#stage-4-the-deposit-licence)
    - [Stage 5 — Remittance](#stage-5-remittance)
    - [Deferred indefinitely](#deferred-indefinitely)
  - [XIV.8 The measurement that decides everything](#xiv8-the-measurement-that-decides-everything)
  - [XIV.9 What this study cannot tell you](#xiv9-what-this-study-cannot-tell-you)
  - [XIV.10 The closing judgement](#xiv10-the-closing-judgement)

---

# VOLUME I — Corporate, Legal & Entity Architecture

## TL;DR
- **Block is legally a Delaware commercial technology holding company (incorporated 2009, IRS EIN 80-0429876) that owns an FDIC-insured Utah industrial bank as one ring-fenced subsidiary among dozens** — the industrial loan company (ILC) charter is the single structural device that lets the commercial parent (bitcoin treasury, mining, music streaming and all) sit outside the Bank Holding Company Act and Federal Reserve consolidated supervision, at the price of a permanent 20% leverage ratio, a Capital and Liquidity Maintenance Agreement, a Parent Company Agreement, and a source-of-strength obligation binding both Block and Jack Dorsey personally.
- **Control is concentrated and separable from ownership:** per Block's 2026 proxy statement, Dorsey holds ~1 million Class A shares (under 1% of that class) and about 47.8 million Class B shares (79.8% of all Class B), giving him about 42.2% of total voting power on a high-single-digit economic stake; the bank (Square Financial Services, Inc.) has its own board and management, deliberately walled off from the parent.
- **For a Nigerian founder the verdict is mostly REJECT/ADAPT:** the ILC escape route has no Nigerian equivalent, so the group cannot escape CBN group supervision; the holdco-over-licensed-subsidiary shape ADAPTS to the CBN Financial Holding Company framework (51% minimum stake, 20% capital buffer); dual-class founder control ADAPTS under CAMA 2020 but collides with CBN fit-and-proper/ownership rules; and the cooperative-society-plus-licensed-bank combination is where **Block offers no precedent at all**.

## Key Findings

**1. What Block is.** Block, Inc. is a Delaware-incorporated, NYSE-listed commercial technology company (Commission File 001-37622). It is *not* a bank holding company and *not* a financial holding company under US law. It is a commercial parent that happens to own a bank. That single legal characterisation is the organising fact of the entire group and the reason its structure is worth studying.

**2. The perimeter, not the ownership tree, is the story.** Block's subsidiaries fall into three rings: (a) *inside* the bank's ring-fence — Square Financial Services, Inc. (SFS), the Utah ILC, supervised by the FDIC and the Utah Department of Financial Institutions; (b) *regulated but outside the bank* — the money-transmitter, broker-dealer, BNPL-lending, e-money and BitLicense entities; and (c) *unregulated commercial* — the parent itself, TIDAL, the bitcoin businesses, and the bitcoin treasury. The bitcoin treasury sits in ring (c), at the consolidated parent level, deliberately outside the bank.

**3. Control is engineered, not earned by ownership.** A dual-class structure (Class B = 10 votes, Class A = 1 vote) gives Dorsey ~42.2% of the vote on a small economic stake. The bank is governed separately.

**4. The structure is accreted at the commercial layer but deliberate at the bank boundary.** The commercial group grew by acquisition and improvisation (Caviar bought then sold, TIDAL impaired, Afterpay bought at the top of the market). But the bank perimeter is a piece of precise, negotiated legal engineering.

## Details

### I.1 Origin and corporate history
- **2009 founding.** Square was founded in February 2009 by Jack Dorsey and Jim McKelvey in San Francisco, after McKelvey lost a glass-art sale because he could not accept a credit card. Incorporated in Delaware in 2009 (IRS EIN 80-0429876). *(CONFIRMED FACT)*
- **November 2015 IPO.** Priced 18 November 2015 at $9.00 per Class A share — below the $11–13 range and ~42% under the prior private round of $15.50. 27,000,000 shares offered (25,650,000 by Square; 1,350,000 by Dorsey's Start Small Foundation), plus a fully-exercised underwriters' option of 4,050,000, for 31,050,000 total; ~$243m raised; implied market cap ~$2.9bn. Lead book-runners Goldman Sachs, Morgan Stanley, J.P. Morgan. First-day close $13.07 (+45%). Offering closed 24 November 2015. *(CONFIRMED FACT)*
- **December 2021 rename.** Legal name changed from Square, Inc. to Block, Inc. on 1 December 2021 (announced), effective on or about 10 December 2021. Ticker stayed "SQ". Stated rationale: "Square" had become synonymous with the seller business; "Block" freed the Square brand for the seller unit and created room for Cash App, TIDAL, TBD and further growth. *(CONFIRMED FACT / COMPANY CLAIM on rationale)*
- **January 2025 ticker change.** Class A common stock began trading as "XYZ" on the NYSE effective 21 January 2025 (ASX CDIs 22 January 2025); the prior "SQ" and "SQ2" symbols were retired. *(CONFIRMED FACT)*
- **Structural takeaway:** none of the renames changed the *legal* architecture. The only structural inflection points were the 2015 IPO (creating the dual-class public company) and the 2021 opening of the bank (creating the ring-fence).

### I.2 The entity map by regulatory perimeter
Block discloses only "major subsidiaries" in Exhibit 21 (Regulation S-K Item 601(b)(21)(ii) lets it omit non-significant ones). The named list has changed materially year to year — itself evidence that the group is fluid at the commercial layer:

- **FY2021 Exhibit 21 (10 entities):** Aspiro AB (Sweden); Project Panther US, LLC (Delaware); Square Canada, Inc. (Canada); Square Capital, LLC (Delaware); Square Financial Services, Inc. (Utah); Square Technologies, Inc. (Canada); Squareup Europe Ltd. (UK); Squareup International Limited (Ireland); Tidal Music AS (Norway); Verse Payments Lithuania UAB (Lithuania).
- **FY2023 Exhibit 21 (14 entities):** the four Afterpay Australian entities (Afterpay Australia Pty Ltd, Afterpay Corporate Services Pty Ltd, Afterpay Holdings Pty Ltd, Afterpay Pty Ltd), Afterpay US, Inc. (Delaware), Aspiro AB (Sweden), Clearpay Finance Limited (UK), Lanai (AU) 1 Pty Ltd, Lanai (US) 1 LLC and Lanai (US) 2 LLC (Delaware), Project Rising, LLC (Delaware — TIDAL's parent), Square Financial Services, Inc. (Utah), Square Technologies, Inc. (Canada), TIDAL Music AS (Norway).
- **FY2024 Exhibit 21 (7 entities):** the Afterpay/Lanai cluster only — SFS was *not* named that year.
- **FY2025 Exhibit 21 (12 entities):** Afterpay Australia Pty Ltd, Afterpay Holdings Pty Ltd, Afterpay Pty Ltd, Afterpay US, Inc. (Delaware), Block XYZ Technology, LLC (Delaware), Lanai (AU) 1 Pty Ltd, Lanai (AU) 2 Pty Ltd, Lanai (US) 1 LLC, Lanai (US) 2 LLC, Square Capital, LLC (Delaware), Square Financial Services, Inc. (Utah), Square Technologies, Inc. (Canada).

Placed by perimeter:

**Ring 1 — inside the bank's ring-fence (FDIC + Utah DFI supervised):**
- **Square Financial Services, Inc.** (Utah industrial bank; FDIC CERT 59177; operational 1 March 2021). The only Block entity inside the insured-depository perimeter.

**Ring 2 — regulated, but outside the bank:**
- Block's US money-transmitter entity (money-transmitter licences in 48+ states plus FinCEN MSB registration) and its **NYDFS BitLicense**-holding crypto entity for Cash App bitcoin.
- **Cash App Investing LLC** — SEC/FINRA broker-dealer.
- **Squareup Europe Ltd.** (UK) and **Squareup International Limited** (Ireland) — non-US regulated payments entities.
- The **Afterpay/Clearpay** lending entities (Australia, US, UK) — consumer-credit regulated in their home jurisdictions.
- **Verse Payments Lithuania UAB** — EU e-money footprint.

**Ring 3 — unregulated commercial:**
- **Block, Inc.** — Delaware parent.
- **TIDAL** (Aspiro AB / TIDAL Music AS / Project Rising, LLC) — music streaming.
- The **bitcoin mining / Proto** hardware business, **Spiral**, **TBD** and **Bitkey**.
- **Square Capital, LLC / Square Technologies, Inc. / Block XYZ Technology, LLC** — technology and servicing entities.
- **The bitcoin treasury** — held at the consolidated parent level (see I.7), *outside* every regulated ring-fence.

### I.3 The intercompany architecture (the boundary machinery)
The FDIC's March 2020 approval imposed a lattice of contracts that is the real ring-fence:
- **Capital and Liquidity Maintenance Agreement (CALMA)** — signed by SFS, Square/Block *and Jack Dorsey personally*. Requires the bank's leverage ratio to be **≥20% at all times**; a third-party line of credit for the bank's benefit acceptable to the FDIC; and a commitment to purchase loans from the bank at the greater of cost or fair value if the FDIC requires. *(CONFIRMED FACT)*
- **Parent Company Agreement (PCA)** — the parent (and Dorsey) consent to FDIC examination of the parent and its subsidiaries; annual reporting on the parent's activities, financial condition, intercompany transactions and risk profile; recordkeeping; and a **source-of-strength** obligation to inject capital or liquidity if the bank falls below thresholds. *(CONFIRMED FACT)*
- **Joint tax-allocation agreement** — the parent holds tax assets generated by the bank *in trust*. *(CONFIRMED FACT)*
- **Sections 23A/23B and Regulation W** — apply to SFS as a state nonmember insured bank via §18(j) of the FDI Act (12 U.S.C. §1828(j)). Covered transactions with any one affiliate are capped at 10% of the bank's capital and surplus (20% in aggregate), with 100–130% collateral requirements, and all affiliate transactions must be on arm's-length terms. The FDIC explicitly noted at approval that "industrial banks are also subject to the provisions of Sections 23A and 23B of the Federal Reserve Act … [which] generally prevents … a bank from subsidizing affiliates by underpricing loans to affiliates." *(CONFIRMED FACT)*
- **Capitalisation:** ~$56m paid-in at opening. Square Financial Services now runs far above minimums — its equity had reached roughly $845m by Q3 2025 (carried from Volume II), and third-party call-report aggregation later shows the bank considerably larger (total assets ~$2.06bn, equity ~$1.35bn, deposits ~$559m, net loans ~$1.29bn, Tier 1 risk-based ~96%). *(THIRD-PARTY ESTIMATE for the later figures; the exact reporting date is unconfirmed — FDIC BankFind for CERT 59177 would be definitive.)*
- **Dividend position:** the FDIC order barred dividends for the first three years of operation without approval ("the Bank shall pay no dividends during the first three years of operations without" prior FDIC approval); SFS became operational 1 March 2021, so that bar lapsed around 1 March 2024. SFS *can* now pay dividends in principle, subject to maintaining the ≥20% leverage ratio and well-capitalised status, but call-report data show a 0% dividend payout — i.e., **no dividends have been paid up to the group**. *(ANALYTICAL INFERENCE that none paid, from a 0% payout ratio; actual payment history UNKNOWN.)* The practical effect: capital flows *into* the bank far more freely than it can flow *out*, and the parent's bitcoin treasury and buybacks are funded from the commercial side, not the bank.

### I.4 Ownership, control and governance
- **Dual-class:** Class A = 1 vote; Class B = 10 votes. The structure sunsets when Class B falls below 5% of combined voting power.
- **Dorsey's position (per the 2026 proxy):** ~1 million Class A shares (<1% of Class A) and ~47.8 million Class B shares (79.8% of Class B), together ~**42.2% of total voting power** on a high-single-digit economic stake. NorthStar Asset Management's shareholder proposals noted that Dorsey and McKelvey "own less than 11% of shares to but control over 48% of the shareholder vote" (2022); the founders' combined vote was reported at ~62% in 2021. McKelvey held 12,259,025 Class B (19.87% of the class; ~10.81% of the vote) in 2022. *(CONFIRMED FACT)*
- **Share counts:** 559,431k Class A + 60,049k Class B (18 Feb 2025); 539,103k Class A + 59,993k Class B (20 Feb 2026) — the Class A count *fell*, reflecting buybacks. *(CONFIRMED FACT)*
- **Shareholder pressure:** NorthStar Asset Management repeatedly proposed collapsing the dual-class structure; the 2021 proposal "garnered support from about 20% of votes cast, per Institutional Shareholder Services," and it was re-proposed 2022–2023, citing Dorsey's crypto focus and the Square→Block rename done "without shareholder input." All failed. Dorsey's cash salary is $2.75. *(CONFIRMED FACT)*
- **The bank's separate governance:** SFS is "an independently governed subsidiary," headquartered in Salt Lake City, with its own board and management — CEO Lewis Goodwin, CFO Brandon Soto (a seven-year tenure; departed to Coastal Community Bank effective 1 October 2025), and Block CFO Amrita Ahuja as Executive Chairwoman of the SFS board (Jacqueline Reses held that role at inception). This separateness is a regulatory requirement, not a courtesy. *(CONFIRMED FACT)*
- **The "Block Heads" reorganisation and headcount cuts:** Dorsey styles himself "Block Head." In November 2023 he imposed a 12,000 headcount cap; ~1,000 roles were cut in January 2024, further cuts hit TIDAL/TBD in late 2024, 931 roles went in March 2025, and on 26 February 2026 — alongside Q4 2025 results — Block announced it would cut **more than 4,000 employees (~40%, nearly half), from over 10,000 to just under 6,000**, citing AI ("we're reducing our organization by nearly half, from over 10,000 people to just under 6,000… A significantly smaller team, using the tools we're building, can do more and do it better"). The FY2025 10-K reports 10,205 full-time employees at 31 December 2025 and a "Workforce Plan" to reduce headcount "by more than 40%," substantially complete by end of Q2 FY2026, with ~$450–500m of charges. Shares rallied ~16% on the day, having been up more than 24% pre-market. **The AI rationale is contested:** Mizuho Americas analyst Dan Dolev told the Wall Street Journal "the vast majority of these cuts were probably not due to AI," and a January 2026 NBER paper (cited by Fortune) found many CEO-attributed AI layoffs were corrections for pandemic-era overhiring. *(CONFIRMED FACT; AI rationale is COMPANY CLAIM and disputed.)*

### I.5 The acquisition record
| Target | Announced / Closed | Consideration | Structure | What it bought | Outcome |
|---|---|---|---|---|---|
| **Caviar** | 2014 / — | Reported ~$90m (securities filing: $44.3m) | Cash | Food-ordering vertical | Sold to DoorDash |
| **Caviar (sale)** | Aug 2019 / 31 Oct 2019 | $410m | Cash + DoorDash preferred stock | Exit non-core vertical | Realised gain |
| **Weebly** | Apr 2018 / 31 May 2018 | ~$365m (cash + stock incl. RSUs) | Cash + stock | Website building / seller omni-channel + recurring subscription revenue | Folded into Square Online |
| **Zesty** | Apr 2018 | Undisclosed | — | Corporate catering tuck-in | Absorbed |
| **Credit Karma Tax** | 2020 | ~$50m | Cash | Free tax-filing → Cash App Taxes | Cash App engagement hook |
| **Verse** | 2020 | Undisclosed | — | European P2P (→ Verse Payments Lithuania) | EU e-money footprint |
| **TIDAL** | 4 Mar 2021 / 30 Apr 2021 | Announced ~$297–306m for ~87.5%; **final $237.3m for 86.23%** | Cash + stock | Music/artist vertical | **$132.3m goodwill impairment (Q4 2023)** |
| **Afterpay** | 1 Aug 2021 / 31 Jan 2022 | **~$29bn announced; $13.8–13.9bn at close** (113,617,352 Class A shares) | All-stock | Global BNPL; seller + Cash App integration | ~$12bn goodwill; AU$1.5bn convertible notes redeemed Mar 2022 |

**Pattern:** Block buys either *time* (Weebly's website tooling, Afterpay's BNPL rails and merchant/consumer base, Credit Karma Tax's filing engine) or *entry into an adjacency it could not credibly build* (TIDAL's artist relationships, Afterpay's Gen-Z installment brand). The record is uneven: Caviar was bought and dumped; TIDAL was impaired by more than half within two years; Afterpay's all-stock structure meant the accounting price ($13.9bn) was less than half the ~$29bn headline because Block's shares fell between signing and closing — a structural feature of paying in your own volatile equity.

### I.6 Litigation, investigations and governance controversies
- **Hindenburg Research, 23 March 2023.** The short-seller report ("Block: How Inflated User Metrics and 'Frictionless' Fraud Facilitation Enabled Insiders To Cash Out Over $1 Billion") alleged inflated Cash App user metrics — "Former employees estimated that 40%-75% of accounts they reviewed were fake, involved in fraud, or were additional accounts tied to a single individual" — lax AML/KYC controls, and that insiders had cashed out over $1bn. Block's shares fell nearly 15% by that Thursday's close. Block called the report "factually inaccurate," said it was "a highly regulated public company … confident in our products, reporting, compliance programs, and controls," and explored legal action. Hindenburg (which disclosed a short position) wound down operations in early 2025. **Assessment:** treated as advocacy. What was *substantiated* by later regulatory findings: the AML/KYC/fraud-controls failures — the CFPB, state money-transmitter regulators, NYDFS and 46 state AGs all found real compliance deficiencies. What was *not* independently established: the specific 40–75% fake-account figure and the deliberate-inflation-to-deceive-investors thesis. What *remains unresolved*: whether metric disclosure was legally misleading (the securities class action is live). *(THIRD-PARTY ESTIMATE / advocacy; regulatory findings are CONFIRMED FACT.)*
- **SEC / DOJ.** Both opened inquiries after the report; the SEC sent a follow-on inquiry in July 2024, then in March 2025 notified Block it had **ended its investigation and "did not intend to recommend an enforcement action."** The DOJ presented "potential terms" in March 2025; Block reserved $240m, disputed "the basis and methodology underlying the DOJ's assessment," made an April counterproposal, and discussions were ongoing as of the May 2025 10-Q. *(CONFIRMED FACT)*
- **Enforcement outcomes (~$340m in 2025–26):** CFPB order up to $175m (16 January 2025 — up to $120m in refunds/redress with a $75m minimum, plus $55m civil penalty); $80m multistate money-transmitter/BSA-AML settlement across 48 states (January 2025); $40m to NYDFS (April 2025, for AML failures, with regulators identifying ~169,000 unprocessed suspicious-activity reports in Block's backlog); $45m to 46 states (Consent Judgment filed 8 July 2026 in the City of Richmond Circuit Court, led by Oregon AG Dan Rayfield and Texas AG Ken Paxton, alleging Electronic Fund Transfer Act / Regulation E violations); $20m to Washington State. *(CONFIRMED FACT)*
- **Securities and derivative suits.** A securities class action (Cohen Milstein / Hagens Berman) alleges Block and executives misled investors about compliance and user metrics; it is ongoing.
- **TIDAL derivative suit.** The City of Coral Springs Police Officers' Pension Plan sued Dorsey and the board over the "terrible business decision" to buy TIDAL (a board meeting convened while Dorsey was "summering with Carter [Jay-Z]"); the suit was **dismissed in May 2023**. *(CONFIRMED FACT)*

**Governance read:** the enforcement record shows the compliance function lagged the growth of Cash App for years — precisely the risk heightened supervision is meant to contain, but Cash App's AML failures sat in the *money-transmitter* entity, not the bank. That is itself a structural lesson: the ring-fence protected the bank; it did nothing to protect the group from the regulated-but-non-bank entity's failures.

### I.7 The bitcoin position as a corporate-structure question
- **Holdings:** 8,038 BTC at end-2022 and end-2023; **8,485 BTC at 31 December 2024** (cost basis $251.5m; fair value $792.3m). Block invested $50m (Q4 2020) and $170m (Q1 2021). *(CONFIRMED FACT)*
- **Accounting:** Block adopted FASB ASU 2023-08 (fair-value measurement of crypto), recording a cumulative-effect adjustment of $30.5m on transition; bitcoin is remeasured to fair value each period within "Other non-current assets." Previously it was an indefinite-lived intangible subject only to impairment write-downs. *(CONFIRMED FACT)*
- **Structural point:** the treasury sits at the **consolidated parent level, outside the bank**. This is exactly how a bank regulator would want it — the FDIC's entire CALMA/PCA apparatus exists to keep the insured bank insulated from the parent's volatile activities. The 20% leverage floor, source-of-strength obligation and 23A/23B limits mean the bank's capital cannot be used to fund, or be impaired by, the parent's bitcoin. There is no public evidence the bitcoin treasury was raised as an obstacle in the charter or supervisory process — because it was structurally quarantined from the bank by design. *(ANALYTICAL INFERENCE; no supervisory objection on record — UNKNOWN whether raised privately.)*

### I.8 The transplant verdicts
- **Holding-company-over-licensed-subsidiary: ADAPT.** The shape transfers, but the CBN Financial Holding Company (FHC) framework is more demanding than the US arrangement. The FHC must be a *non-operating* parent, hold ≥51% of each subsidiary, and hold paid-in capital ≥20% above the sum of subsidiaries' minimum regulatory capital, with excess capital in one subsidiary unable to plug a deficit in another. The silent US feature: Block can own 100% of its bank *and* run unrelated commercial businesses in the same group; Nigeria's draft 2026 FHC rules **prohibit the holdco from owning anything outside financial services** — so a Nigerian founder cannot house a bank and a music-streaming service under one regulated holdco.
- **Escaping consolidated group supervision (the ILC exception): REJECT.** There is no Nigerian route by which a commercial parent escapes CBN group supervision. The reader must accept that the *entire* group — holdco and all subsidiaries — will be consolidated under the CBN, with group capital adequacy, group governance and CBN examination reaching every entity. The silent US feature is the FDIC's ILC carve-out from the BHC Act; nothing analogous exists. Consequence for group shape: the reader cannot keep the technology parent "commercial and unsupervised" the way Block does. The technology platform, if inside the group, is drawn into the perimeter.
- **Ring-fencing a regulated entity from a commercial parent: ADAPT.** Block's instruments (CALMA, PCA, 23A/23B, tax-in-trust, separate bank board, dividend restraint) have direct Nigerian analogues in the draft FHC rules: mandatory operational independence of each subsidiary, arm's-length shared-services with value-for-money audits every two years, intra-group loans to the parent treated as a return of capital (deducted from the bank's CAR), prohibition on the holdco borrowing against subsidiary guarantees, and interlocking-directorship limits (a holdco director may sit on only one subsidiary board; holdco directors ≤20% of any subsidiary board; no cross-attendance of meetings). The reader must **build these ring-fence contracts and governance walls from day one**, not retrofit them.
- **Owning a cooperative society and a licensed entity in one group: REJECT as a Block analogy — the analogy runs out here.** Block never owned an entity registered under a *different body of law* and answering to a *different regulator* from its bank. A Nigerian cooperative society is registered under state cooperative law, governed by a state Director of Cooperatives, and is not a company under CAMA 2020 at all. It cannot be a "51%-owned subsidiary" of an FHC in the ordinary corporate sense, and the CBN's non-operating-holdco, majority-ownership and consolidation logic does not map onto a member-owned cooperative (one-member-one-vote by law). **Block offers no template for this.** What *is* transferable is the generic discipline Block's multi-regulator experience teaches: map each entity to its regulator and its perimeter, keep separate boards, keep intercompany dealings arm's-length and documented, and never assume a control mechanism that works in one perimeter is lawful in another. The reader should treat the cooperative as a *related but non-owned* anchor customer/partner, connected by contract and common founder purpose rather than by equity control.
- **Founder control through dual-class: ADAPT, with a warning.** CAMA 2020 permits different classes of shares, so a dual-class structure is constructible for the holdco and its non-cooperative subsidiaries. But CBN fit-and-proper and significant-shareholder rules require regulatory approval of controllers, and the draft FHC rules require the holdco to be registered as a "person with significant control." Founder voting control is achievable but will be *visible and vetted* by the CBN in a way it is not vetted by the SEC. And a cooperative is one-member-one-vote by law — dual-class control cannot reach it.
- **Holding a volatile asset (e.g., bitcoin) at the parent while owning a licensed subsidiary: REJECT / treat with extreme caution.** A Nigerian regulator would view a holdco holding a volatile speculative asset above a licensed bank with considerable suspicion, and the draft FHC rules' bar on the holdco owning non-financial-services businesses, plus consolidated capital treatment, would likely force any such asset out of the group or heavily penalise it in group capital. Block's ability to hold bitcoin at the parent depends entirely on that parent being *outside* consolidated bank supervision — a condition the reader cannot reproduce.

### I.9 Volume I reconstruction
**(1) Chronology:** 2009 founded (Delaware) → Nov 2015 IPO at $9 → Mar 2016 Celtic Bank lending → Jun 2018 NYDFS BitLicense → Mar 2020 FDIC/Utah conditional bank approval → 1 Mar 2021 SFS operational → 30 Apr 2021 TIDAL closed → 1 Dec 2021 renamed Block → 31 Jan 2022 Afterpay closed → Mar 2023 Hindenburg → Jan 2025 CFPB/multistate settlements + ticker → XYZ → Mar 2025 SEC closes inquiry → Feb 2026 40% workforce cut.
**(2) Entity map:** three rings as in I.2 — SFS alone inside the bank perimeter; the MTL/broker-dealer/BitLicense/BNPL/EU entities regulated-but-outside; the parent, TIDAL, bitcoin businesses and the treasury unregulated-commercial.
**(3) Intercompany architecture:** CALMA + PCA + tax-in-trust + 23A/23B/Reg W + source-of-strength + dividend restraint.
**(4) Ownership/governance:** dual-class; Dorsey ~42.2% vote; separate bank board.
**(5) Acquisition table:** as in I.5.
**(6) Litigation/controls:** Hindenburg (advocacy, partly substantiated); ~$340m enforcement; SEC closed, DOJ ongoing; TIDAL suit dismissed.
**(7) Bitcoin:** 8,485 BTC (end-2024), fair-valued, at the parent, outside the bank.
**(8) Transplant table:** as in I.8.
**(9) Key unknowns:** SFS's precise current balance sheet and reporting date; whether SFS has ever paid a dividend up to Block (evidence says no); the DOJ settlement's final terms; whether the bitcoin treasury was privately raised in supervision.
**(10) Ten conclusions:** (i) Block is a commercial parent that owns a bank, not a bank holding company; (ii) the ILC charter is the load-bearing device; (iii) the bank is one small, heavily-capitalised, walled-off subsidiary; (iv) the ring-fence is contractual (CALMA/PCA) plus statutory (23A/23B); (v) control is dual-class-engineered and separable from ownership; (vi) capital flows into the bank easily and out barely; (vii) the bitcoin treasury is quarantined at the parent by design; (viii) the commercial group is accreted, the bank boundary is deliberate; (ix) acquisitions bought time and adjacencies Block could not build, unevenly; (x) for a Nigerian founder the escape-from-supervision trick does not transfer and the cooperative problem has no Block precedent.

**The central question — deliberate or accreted?** Both, at different layers. The *commercial* group is accreted: renames, a music service bought on a friendship and impaired, a BNPL platform bought at the top in stock, rolling layoffs. The *bank boundary* is deliberate, negotiated legal architecture. A founder building a multi-entity financial group today should **take** the bank-boundary discipline — the ring-fence contracts, the separate board, the source-of-strength commitment, the arm's-length intercompany rules, the perimeter-first mental model — and should **avoid** the accreted commercial sprawl, the volatile asset at the parent (impossible under CBN rules anyway), the friendship-driven acquisition, and the assumption that a control or asset arrangement lawful in one perimeter travels to another. And they must accept at the outset what Block never had to: full group supervision, no commercial escape hatch, and a cooperative anchor that the corporate group cannot own the way Block owns its subsidiaries.

## Recommendations
1. **Adopt a perimeter-first design now.** Before incorporating anything, draw the group as concentric regulatory rings, not an ownership tree. Decide which entity will one day hold the deposit licence and treat everything about that entity — board, capital, intercompany terms — as ring-fenced from day one. *Benchmark to change course:* if the CBN's final 2026 FHC guidelines relax the non-financial-services ownership bar, the technology platform could sit inside the group; if not, keep it outside on a vendor model.
2. **Keep the technology platform founder-owned and outside the FHC.** Because the CBN will consolidate everything inside the holdco and bars non-financial businesses, the permanently founder-owned core-banking platform should sit *outside* the FHC as an arm's-length vendor supplying the group under audited, value-for-money service agreements — mirroring how Block *contracts* for issuer-processing and card rails rather than owning them.
3. **Structure the cooperative as a contractually-linked anchor, not an owned subsidiary.** Since a cooperative cannot be a 51%-owned CAMA subsidiary and answers to a different regulator, connect it by commercial agreement, shared purpose and (where lawful) a management/services contract — not by equity control. Take legal advice on whether any CBN-licensed entity may lend to or transact with the cooperative and on what arm's-length terms.
4. **Build the ring-fence contracts before the licence, not after.** Draft the Nigerian analogues of CALMA/PCA: a capital-and-liquidity support undertaking, arm's-length intercompany service agreements, a tax-sharing agreement, and board-independence rules that satisfy the CBN's interlocking-directorship limits (one subsidiary board per holdco director; ≤20% holdco representation; no cross-attendance).
5. **Plan for the 20% capital buffer as a hard constraint on sequencing.** Because the FHC must hold 20% above the *sum* of all subsidiaries' minimums and cannot net surpluses across subsidiaries, add licensed subsidiaries *sequentially*, not simultaneously, and raise the buffer capital before each new licence. *Benchmark:* do not apply for the deposit licence until the holdco can demonstrate the combined-minimum-plus-20% on a fully-funded basis. Note the draft rules require non-bank promoters to deposit 100% of combined minimum capital plus a 20% mark-up with the CBN upfront.
6. **Keep any volatile treasury asset out of the group entirely.** Unlike Block, the reader has no unsupervised parent to hold it in. If bitcoin or similar exposure is desired, hold it personally or in a vehicle wholly outside the FHC.

## Caveats
- **Basis:** US GAAP, USD, 31 December year-end, Form 10-K, except where third-party call-report data are used for SFS (flagged). Gross profit anchors: $7.505bn (2023), $8.889bn (2024), ~$10.36bn (2025); bitcoin was ~42.3% of 2024 revenue at ~3% margin.
- **SFS balance sheet:** the later figures (≈$2.06bn assets, ≈$1.35bn equity) are third-party aggregations of FDIC call-report data with an unconfirmed reporting date; the ~$845m equity figure (Q3 2025) is carried from Volume II. Reconcile against FDIC BankFind (CERT 59177) before relying on either.
- **Caviar purchase price** conflicts between "reported ~$90m" (press) and $44.3m (securities filing); both are recorded.
- **Nigerian FHC rules** cited are substantially from the CBN's *draft* revised 2026 exposure guidelines (open for comment to 9 July 2026) layered on the extant 2014 framework; final rules may differ, and the 51%/20% figures reflect the reader's stated prior research corroborated by the draft.
- **Hindenburg** is advocacy by an interested short-seller; its specific metrics (including the 40–75% figure) are unverified, though the underlying compliance failures were later confirmed by regulators.
- **DOJ matter** was unresolved as of the last available filing; the final penalty and any admissions are UNKNOWN.
- Where the cooperative-plus-bank question is concerned, **Block offers no precedent**, and this volume declines to manufacture one.

---

# VOLUME II — The Regulatory Estate & the Bank

## Block, Inc. (NYSE: XYZ, formerly Square, Inc.) — A Forensic Reverse-Engineering Study
### The Licence Ladder: How a Technology Company Acquired the Right to Hold, Move and Lend Money

---

## TL;DR

- **Block climbed a seven-rung licence ladder over twelve years — payment facilitator (2009) → state money-transmitter licences + FinCEN MSB registration (2012–13) → bank-partner lending via Celtic Bank (2016) → NYDFS BitLicense (2018) → broker-dealer (Cash App Investing, ~2019) → its own Utah industrial bank (Square Financial Services, 1 March 2021) → Afterpay's BNPL licensing estate (31 January 2022). The single decisive rung was the industrial loan company (ILC) charter, which let Block own an FDIC-insured bank *without* Federal Reserve holding-company supervision — a structural loophole that has no Nigerian equivalent.**
- **The bank-partnership-first sequence ADOPTS to Nigeria and is exactly what the reader should do; the ILC charter REJECTS (no equivalent exists) but its *function* — balance-sheet lending independent of a partner's risk appetite — maps onto a CBN deposit-taking microfinance-bank licence; state-by-state MTL licensing REJECTS as a burden Nigeria's single national CBN regime spares the reader.**
- **The enforcement record is the load-bearing warning: Block paid roughly $340 million in AML, BSA and consumer-protection penalties across 2025–2026 (a $175m CFPB order, an $80m 48-state settlement, a $40m NYDFS penalty, a $45m 46-state settlement and a $20m Washington settlement), all arising because compliance capability did not keep pace with licensing ambition. For a capital-constrained founder this is the central lesson: the ladder is climbable, but "build compliance after scaling" is a privilege of scale, not a template.**

---

## KEY FINDINGS

1. **The ladder is real and sequential, not a checklist.** Each rung changed what Block could *be*: the payment-facilitator model let it onboard millions of sellers without underwriting each as a bank merchant; money-transmitter licences let it hold customer funds; the bank partnership let it lend without a charter; the BitLicense let it sell bitcoin in the largest state; the broker-dealer let it offer equities; the ILC let it originate and *retain* loans and take deposits on its own balance sheet.

2. **The industrial bank is the pivot.** Square applied on 17 September 2017, materially amended the application on 18 December 2018, received FDIC conditional approval on 17–18 March 2020 and a Utah DFI charter, and opened Square Financial Services (SFS) on 1 March 2021 with roughly $56 million of paid-in capital and an extraordinary permanent 20% leverage-ratio requirement — roughly double a normal well-capitalised bank.

3. **Renting a charter (Celtic Bank) worked but capped the economics.** From 2016, Celtic Bank — a Utah ILC — was the lender of record for Square Capital loans; Square purchased the loans within one-to-two business days and sold most to institutional investors. Square bore the credit and balance-sheet risk it retained; Celtic earned fees and was insulated from state usury caps as the bank originator. Block moved off Celtic for business loans in April 2021 once SFS opened.

4. **The charter bought balance-sheet independence.** Owning SFS let Block retain loans as "held for investment," take FDIC-insured deposits (Square Savings exceeded $300m by end-2024), earn the full interest spread rather than a servicing/origination fee, and — from mid-2025 — bring Cash App Borrow and Afterpay lending in-house. SFS equity grew from ~$56m (2021) to roughly $845m (Q3 2025).

5. **The charter also *foreclosed* things.** It brought FDIC and Utah DFI supervision, a Capital and Liquidity Maintenance Agreement (CALMA), a Parent Company Agreement, a source-of-strength obligation on Block and personally on Jack Dorsey, a majority-independent board at the bank, a $50m third-party reserve deposit, a three-year dividend prohibition, and FDIC examination reaching up into the parent. Renting Celtic's charter carried none of this.

6. **The enforcement ledger is large and clustered in 2025–2026,** overwhelmingly about Cash App's AML/BSA and consumer-protection failures during its 2019–2021 hypergrowth — direct evidence that compliance lagged licensing.

7. **The regulatory estate is a modest but rising share of gross profit.** Block's gross profit was $7.505bn (2023), $8.889bn (2024) and ~$10.36bn (2025). The one-time 2025–26 penalties (~$340m) represent roughly 3–4% of a single year's gross profit — absorbable for Block, potentially fatal for a small founder.

---

## DETAILS

### II.0 Basis and metric discipline

Block reports under **US GAAP, in US dollars, with a 31 December year-end, on Form 10-K as a domestic filer.** Segment reporting has changed more than once: through 2023 Block split its BNPL platform 50/50 between Square and Cash App, then from Q4 2023 reported it fully within Cash App ("In the fourth quarter of 2023, we began reporting the financial results of our BNPL platform fully within Cash App, rather than allocating 50% of revenue and gross profit to each of Square and Cash App"); from FY2025 Block re-cut its disclosure into three "revenue categories" — Commerce Enablement, Financial Solutions and the Bitcoin Ecosystem — which together produced $10.4bn of gross profit in 2025. Any figure below is labelled with its basis.

**Follow the gross profit.** Block's headline metric is gross profit, not revenue, by necessity. Bitcoin sold to Cash App customers is booked as revenue at the full sale amount, with the cost of the bitcoin in cost of revenue, so bitcoin inflates total revenue while contributing a razor-thin margin. In 2024 bitcoin revenue was about 42% of Block's ~$24.1bn total net revenue but a trivial share of the $8.889bn gross profit. **Any licensing analysis anchored on revenue would misstate the business by roughly a factor of three.** This volume anchors on gross profit throughout.

**Evidence classification** (CONFIRMED FACT / COMPANY CLAIM / THIRD-PARTY ESTIMATE / ANALYTICAL INFERENCE / HYPOTHESIS / UNKNOWN) is applied to material claims.

### II.1 The Ladder, Reconstructed (chronological)

**Rung 0 — Incorporation and the card reader (2009).** Square, Inc. was formed in 2009 by Jack Dorsey and Jim McKelvey to let small merchants accept card payments via a mobile dongle. (CONFIRMED FACT.)

**Rung 1 — Payment facilitator / aggregator under a sponsoring acquirer (2009–2011).** Square pioneered the "payment facilitator" (PayFac) model: rather than each small merchant obtaining its own merchant account, Square became the master merchant under a sponsoring acquirer and onboarded "sub-merchants" in hours. Square's sponsoring acquirer was **JPMorgan Chase Bank, N.A. / Paymentech, LLC** — Square's Commercial Entity Agreement names "JPMorgan Chase Bank, N.A. (the 'Member')" and "Paymentech, LLC" as the parties governing "the authorization, conveyance and settlement of Transactions utilizing the Square Service." (CONFIRMED FACT.)
- *What it permitted:* accepting and settling card transactions for millions of small sellers without underwriting each as a bank merchant; fast onboarding; portfolio-level risk management.
- *What it forbade / constrained:* the PayFac does not itself hold a banking charter; it is contractually bound to the acquirer's rules, must perform KYC/AML on sub-merchants, bears chargeback and fraud risk, and — under Visa/Mastercard rules — must migrate any sub-merchant exceeding a volume threshold (historically US$1m/year) to a direct merchant agreement. The acquirer, not Square, was the regulated bank in the chain. (CONFIRMED FACT / ANALYTICAL INFERENCE.)

**Rung 2 — State money-transmitter licences + FinCEN MSB registration (~2012–2013 onward).** To hold and move customer funds (particularly as Cash App developed) Square had to license as a money transmitter in essentially every state that requires it. NYDFS records show Block "has been licensed in the State of New York to operate as a money transmission business since 2013." (CONFIRMED FACT.)
- *Scale of the regime:* money transmission is licensed state-by-state — every state except Montana runs its own regime, so the "licence" is really a portfolio of 48-plus licences plus territories (District of Columbia, Puerto Rico, Guam, US Virgin Islands, American Samoa), each with its own net-worth minimum, surety bond, permissible-investment rule, application fee and renewal calendar, most filed through the Nationwide Multistate Licensing System (NMLS). States license more than 700 money transmitters, and 99% of transmission activity is now governed by the state-developed Money Transmission Modernization Act. (CONFIRMED FACT.)
- *Costs:* bonds range from roughly $10,000 to $2 million per state (California can require between $250,000 and $7 million, sized to average daily outstanding transmission obligations); net-worth minimums run from ~$25,000 upward; application fees run from a few hundred to several thousand dollars per state; a full national build "frequently passes seven figures once bonds and legal work are included." (THIRD-PARTY ESTIMATE, licensing practitioners.)
- *FinCEN:* separately and federally, Square registered as a **money services business (MSB)** with FinCEN, triggering Bank Secrecy Act obligations — a written AML program, a designated compliance officer, KYC/customer due diligence, suspicious-activity-report (SAR) and currency-transaction-report filing, and sanctions screening. MSB registration never substitutes for state MTLs; they stack. (CONFIRMED FACT / ANALYTICAL INFERENCE.)

**Rung 3 — The bank-partner lending era: Celtic Bank (2014–2021).** Square Capital launched publicly in May 2014 as a **merchant cash advance (MCA)** product, then converted in March 2016 to fixed-fee **loans originated by Celtic Bank Corporation**, a Utah-chartered industrial bank in Salt Lake City. Celtic was "the lender and originating creditor for the program … using its own funds"; Square Capital, LLC acted as service provider (marketing, application processing, servicing) and **purchased the loans from Celtic**, then sold the majority to third-party institutional investors, retaining a portion. (CONFIRMED FACT, Square 10-K disclosures + loan agreements.) See II.3 for the economics.

**Rung 4 — NYDFS BitLicense for Cash App bitcoin (18 June 2018).** Cash App began offering bitcoin buying/selling in early 2018 but could not serve New York until NYDFS granted Square a **BitLicense on 18 June 2018** — Square was among the first roughly nine firms ever to receive one under the regime introduced in August 2015 (23 NYCRR Part 200), described by industry counsel and by outlets such as *American Banker* as the most demanding state virtual-currency framework in the United States. NYDFS conducted "a comprehensive review of Square's application, including the company's anti-money laundering, anti-fraud, capitalization, consumer protection, and cybersecurity policies." (CONFIRMED FACT / THIRD-PARTY characterization on "hardest".) A prior New York money-transmitter licence did not authorize crypto activity — the BitLicense was a distinct, additional rung.

**Rung 5 — Cash App Investing LLC: broker-dealer (~2019).** Equities trading in Cash App is offered through **Cash App Investing LLC**, a wholly owned Block subsidiary "registered with the Securities and Exchange Commission … as a broker-dealer and … a member of the Financial Industry Regulatory Authority ('FINRA') and the Securities Investor Protection Corporation ('SIPC')" (FINRA CRD #144076). SIPC "protects securities customers of its members up to $500,000 (including $250,000 for claims for cash)." Cash App Investing is an introducing broker; clearing/custody is provided by carrying brokers (transitioning from DriveWealth to Apex Clearing). (CONFIRMED FACT.) Note the careful entity boundary Block draws in its own disclosures: "Cash App and Block are not members of FINRA or SIPC" — only the Cash App Investing subsidiary is.

**Rung 6 — Square Financial Services, Inc.: the Utah industrial bank (opened 1 March 2021).** The pivot. Full analysis in II.2.

**Rung 7 — Afterpay's regulatory estate (acquired 31 January 2022).** Block completed its acquisition of Afterpay Limited on 31 January 2022 (a scheme of arrangement, originally an all-stock deal announced August 2021). Afterpay carried its own US state-lending footprint and regulatory exposure. Notably, California treated BNPL as credit requiring a lender licence: Afterpay had settled with California in 2020, agreeing to pay nearly $1 million in refunds and fines and to obtain a California Financing Law licence. In the US, Block's BNPL loans have been originated through a bank partner (First Electronic Bank, a Utah ILC — the loan agreements name it "as the originator and issuer of your loan") and, from mid-2025, increasingly through SFS. Afterpay also brought CFPB exposure, since the CFPB in 2024 issued an interpretive rule treating BNPL lenders as subject to certain Regulation Z credit-card provisions. (CONFIRMED FACT / ANALYTICAL INFERENCE.)

**International authorizations (established here, developed in the international volume).** Block operates as a licensed money transmitter or equivalent in several non-US jurisdictions and acquired Afterpay's Australian, UK and EU footprint (Afterpay trades as "Clearpay" in the UK/EU). Square's European seller business runs through Squareup Europe Ltd. Precise entity-by-entity international authorizations are UNKNOWN at this volume's evidentiary depth and are deferred to the international-expansion volume.

### II.2 The Industrial Bank Decision (the pivotal section)

**What an industrial bank is, and why Utah.** An industrial bank — or industrial loan company (ILC) — is a state-chartered, FDIC-insured depository that can take deposits, make loans and do essentially everything a commercial bank does, but sits inside a statutory exception in Section 2(c) of the **Bank Holding Company Act (BHCA)**. That exception means the ILC's parent company is **not** deemed a "bank holding company" and is therefore **not subject to consolidated supervision by the Federal Reserve.** This is the entire point: a commercial or technology company can own a full-service FDIC-insured bank without submitting its whole corporate group to Fed holding-company regulation (which would restrict non-banking commercial activities). Utah is the dominant charter state; SFS became the sixteenth FDIC-insured industrial bank operating in Utah, where such banks held $171 billion in total assets as of 31 December 2020. (CONFIRMED FACT.)

**How it differs from a national bank charter.** A national bank (OCC-chartered) or a state member bank forces its parent into the BHCA/Fed holding-company regime, which effectively bars a commercial parent (a technology company selling hardware, running a music-streaming service, mining bitcoin) from owning it, because banking and commerce must be separated. The ILC charter is the only route by which a company like Block — commercial, non-bank, Fed-unsupervised at the group level — can own an FDIC-insured bank. (CONFIRMED FACT / ANALYTICAL INFERENCE.)

**Application and approval history (dated).**
- 17 September 2017 — Square, Inc. submitted its ILC application to the Utah DFI (and a deposit-insurance application to the FDIC).
- The application was withdrawn in mid-2018 (reported as "technical reasons"; COMPANY CLAIM / third-party reporting), then refiled and materially amended on 18 December 2018.
- 17–18 March 2020 — the FDIC Board approved Square's deposit-insurance application (Utah DFI conditional charter approval, Order dated 17 March 2020).
- 1 March 2021 — SFS "received its deposit insurance from the FDIC and charter approval from the Utah Department of Financial Institutions and became operational." (CONFIRMED FACT.)

**Dissent worth recording.** FDIC Director Martin J. Gruenberg opposed Square's application in his 18 March 2020 dissent, arguing it failed the statutory "source of financial strength" test. He stated that Square "has never been profitable since it was formed in 2009" and relies on "a business model that is highly vulnerable to an economic downturn" — conditions he called "reflective of the underlying weakness of the application." He also cited the "extraordinary conditions" in Square's CALMA, including the permanent 20% tier-1 leverage ratio and the reserve deposit. (CONFIRMED FACT: FDIC dissent statement.) This dissent is analytically important: even inside the FDIC, approval was contested and conditioned on unusually heavy parent commitments.

**What the charter permits that the Celtic arrangement did not.**
- **Balance-sheet lending and retention.** Block can originate loans through SFS and hold them "as held for investment," capturing the full interest spread and the full economics of a performing loan, rather than earning a fee for originating on a partner's charter. Square Loans' average loan is approximately $10,000, repaid through a fixed percentage of daily sales.
- **Deposit-taking.** SFS offers FDIC-insured business savings accounts (Square Savings balances "totaled more than $300M" as of 31 December 2024) — a funding source Block could never have as a non-bank.
- **Independence from a partner's risk appetite.** With Celtic, Square was constrained by Celtic's willingness to originate a given product; owning the bank removed that dependency and let Block bring Cash App Borrow (nearly $9 billion of originations in 2024, historic loss rates under 3%) and Afterpay lending in-house from mid-2025.

**What it cost (capital, liquidity, governance, reporting).** The FDIC/Utah conditions are unusually heavy and worth listing in full:
1. Initial paid-in capital of not less than approximately $56 million (per the FDIC and *American Banker*: "Square Financial Services will be required to have an initial capital level of $56 million, with a minimum leverage ratio of 20%" — versus Nelnet Bank's $100m/12% and Varo's 10%).
2. A permanent **leverage ratio of at least 20%** — the CALMA required Square to "maintain the leverage ratio of the proposed bank at least 20 percent at all times," roughly double a normal "well-capitalized" bank — maintained per the FDIC-approved business plan during the first three years and at not less than 20% thereafter.
3. A **Capital and Liquidity Maintenance Agreement (CALMA)** among Block (parent), Jack Dorsey (controlling shareholder), the FDIC and SFS.
4. A **Parent Company Agreement** subjecting Block and its subsidiaries to FDIC reporting and examination and monitoring of affiliate transactions.
5. A statutory **source-of-financial-strength** obligation on Block, with Dorsey personally agreeing to cause Block to perform under the agreements.
6. A **$50 million reserve deposit** at an unaffiliated, third-party insured bank that SFS could draw on if Block failed to provide required funds.
7. A **third-party line of credit** for the benefit of the bank, acceptable to the FDIC.
8. A **parent purchase obligation**: Block must purchase any loan from SFS "at the greater of the cost basis or fair market value, if deemed necessary by the FDIC or the proposed bank."
9. A **majority-independent board** at SFS, with parent-company representation capped (originally 25% in the conditional approval; the FDIC's final rule set the cap at less than 50%), and **no dividends during the first three years** without approval.
10. Operation strictly within the FDIC-approved **business plan**, updated and resubmitted annually to the San Francisco Regional Director.

SFS equity grew from roughly $56m (2021) to about $845m by Q3 2025 (THIRD-PARTY, FDIC call-report-derived aggregator figure).

**The political contest over the ILC charter — current state of play.** The ILC charter is politically contested and periodically at risk of closure. The Independent Community Bankers of America (ICBA), the Bank Policy Institute (BPI) and the Center for Responsible Lending (CRL) have campaigned for years to "close the ILC loophole," arguing it lets commercial and Big Tech firms own FDIC-insured banks while escaping Fed consolidated supervision and mixing banking with commerce (ICBA: the loophole "allows commercial interests to own full-service banks, avoid consolidated supervision, and threaten the financial system," citing the 2008 GMAC failure and its "$17.2 billion taxpayer-funded" rescue). Key milestones: ICBA opposed Walmart's ILC bid (2005); Dodd-Frank imposed a temporary ILC moratorium; the FDIC issued a proposed rule in March 2020 and a **final rule effective 1 April 2021 (Part 354)** codifying parent-company commitments (written agreements, annual subsidiary lists, consent to FDIC examination, tax-allocation and capital/liquidity commitments); the **Close the Shadow Banking Loophole Act (S. 3538)**, introduced by Senators Sherrod Brown and John Kennedy, would force ILC parents into BHCA supervision. As of late 2025 the loophole remains open — the FDIC issued a request for information and ICBA filed a comment on 19 September 2025 urging rejection of pending ILC applications — but no statute has closed it. **Verdict on availability: the route remains legally open but is contested and could narrow; Block's charter, granted before the 2021 rule (which is not retroactive), is grandfathered.** (CONFIRMED FACT.)

**The counterfactual.** Had Block never obtained the charter and remained on Celtic: it would still be earning primarily origination and servicing fees plus gains on loan sales, not the full interest spread; it could not take deposits and would have no FDIC-insured, ~$300m+ low-cost funding base; it would remain hostage to Celtic's risk appetite and pricing for each product; and it could not have internalized Cash App Borrow and Afterpay lending in 2025. It would also, however, have avoided the trapped regulatory capital (now ~$845m of equity locked in SFS at a 20% leverage ratio), the CALMA/source-of-strength drag, and direct FDIC/Utah examination. **Analytical inference: the charter converted Block from a fee-earning loan facilitator into a spread-earning, deposit-funded lender — a categorical change in the lending business model, bought at the price of trapped capital and heavy supervision.**

### II.3 The Bank-Partner Era and Why It Ended (the section that matters most to the reader)

**The mechanics of renting a charter.** From the March 2016 conversion, Celtic Bank was the **lender of record and originating creditor**, using its own funds; the loan agreements are explicitly "a contract between Merchant, Celtic Bank Corporation and Square Capital, LLC." Square Capital purchased the loans from Celtic, obtaining "all rights, title, and interest," and classified them as held for sale, intending to sell the majority to third-party institutional investors on a forward-flow basis, retaining a portion on its own balance sheet. Per Square's own 10-K, loans not sold within one-to-two business days from origination were reclassified as held for investment. (CONFIRMED FACT.)

**Who bore what.** Celtic, as bank originator, earned fees and — critically — as a bank was **not subject to state interest-rate caps**, insulating the product from usury/state-rate litigation. Because Square purchased 100% of the rights and title within days and sold most downstream, the **credit and balance-sheet risk sat with Square and its investors, not Celtic.** The precise Square–Celtic fee split is not publicly disclosed (UNKNOWN). No specific loss-share or repurchase obligation to Celtic is disclosed beyond the standard purchase. (CONFIRMED FACT / UNKNOWN on exact economics.)

**What the arrangement forbade.** Square could not take deposits; could not, of its own right, set the legal terms of the credit (Celtic was the creditor); and depended on Celtic's continued willingness to originate. The structure existed precisely because Square held no banking charter of its own.

**Scale of the rented-charter business.** Square Capital facilitated roughly $450m by early 2016 (still MCA); over $4.0bn cumulatively across 650,000+ loans by end-2018; over $6.3bn across nearly 1 million loans by end-2019; annual business-loan originations of ~$1.6bn (2018), $2.3bn (2019), ~$4.06bn (2022), $4.78bn (2023) and $5.7bn (2024, of which $1.54bn in Q4). Cumulatively Block has cited "more than $32 billion in loans for small businesses" since 2014. During COVID, Square facilitated approximately $857m of Paycheck Protection Program (PPP) loans to over 80,000 small businesses as of 31 December 2020, again with Celtic as issuer (Square later also became a direct PPP lender). (CONFIRMED FACT / THIRD-PARTY deBanked compilations of Block shareholder letters.)

**Why Block moved off it (April 2021).** Block discontinued the Celtic arrangement for business loans once SFS opened, to capture the full economics (spread not fee), gain deposit funding, and control product design and risk independently. The FY2021 filings note Block discontinued a prior arrangement with an industrial-bank partner. (CONFIRMED FACT.) Note the nuance: Celtic and First Electronic Bank continued to originate *some* Block consumer products (the Square credit card, Cash App Borrow, Afterpay-on-Cash-App) even after SFS opened, until Block migrated those to SFS in 2025 — so "moving off" was product-by-product, not a single clean exit. Block received FDIC approval in March 2025 for SFS to offer Cash App Borrow, taking over origination from First Electronic Bank.

**Why this matters most to the reader.** The reader will begin exactly where Square began in 2014–16: holding no licence, partnered with a licensed entity, facilitating a regulated activity performed by someone else's charter. Square's experience shows this is a viable multi-year posture that can scale to billions in volume — but that the *ceiling* of the rented-charter model (fee economics, no deposits, dependence on the partner) is precisely what eventually justifies climbing to an owned charter.

### II.4 The Enforcement Record as a Cost of the Estate (dated ledger)

The material actions cluster in 2025–2026 and concern Cash App. All were entered without Block admitting or denying wrongdoing.

1. **Multistate money-transmitter settlement — 15 January 2025.** Entity: Block, Inc. Regulators: 48 state financial regulators (State Money Transmission Regulators), coordinated through CSBS/MTRA via the Multi-State MSB Examination Taskforce; per the CSBS release, "State regulators in Arkansas, California, Massachusetts, Florida, Maine, Texas, and Washington State led the multistate enforcement effort." Conduct: BSA/AML violations — inadequate customer due diligence, transaction-monitoring and SAR failures — found in a multi-state examination begun 15 May 2023 covering 1 January 2021–31 March 2023. Amount: **$80 million** (assessed as $79,075,000 distributed among participating states). Undertakings: "hire an independent consultant … submit a report to the states within nine months," then "12 months to correct any deficiencies." Liability admitted: no. (CONFIRMED FACT.)

2. **CFPB consent order — 16 January 2025.** Entity: Block, Inc. (Cash App). Conduct: violations of the Consumer Financial Protection Act (unfair practices), the Electronic Fund Transfer Act and Regulation E — woefully incomplete fraud investigations, directing defrauded users to their banks, using the card-network chargeback process as a substitute for statutory dispute resolution, no live customer service for years, and deceptive representations about fraud protection. CFPB Director Rohit Chopra: "Cash App created the conditions for fraud to proliferate on its popular payment platform … Cash App flouted its responsibilities and even burdened local banks with problems that the company caused." Amount: **up to $175 million total — up to $120 million in consumer redress (minimum $75 million) plus a $55 million civil penalty** to the CFPB victims-relief fund. Undertakings: 24-hour live-person customer service (phone ≥12 hrs/day, chat ≥18 hrs/day), full dispute investigation, internal committees, a compliance plan. Redress checks began mailing (via administrator Epiq) on 8 June 2026. Jack Dorsey signed the stipulation to the 75-page consent order. Liability admitted: no. (CONFIRMED FACT.)

3. **NYDFS consent order — 10 April 2025.** Entity: Block, Inc. Regulator: New York Department of Financial Services (under Block's NY money-transmitter licence held since 2013 and BitLicense since 2018). Conduct: "significant failures" in the BSA/AML program during 2019–2021 hypergrowth. Per the consent order, Block "let a backlog of SAR alerts grow from 18,000 to over 169,000" between 2018 and 2021, causing some SARs to be filed over a year late; "restricted" Cash App accounts permitted fiat transactions under a limit without full identity verification (one ring of ~25–30 subjects opened 8,359 accounts using falsified information); sanctions screening was inadequate; and — most strikingly — Block's system "did not trigger blocks on bitcoin transactions involving terrorism-connected wallets until that exposure exceeded 10%," while its vendor did not generate alerts until a recipient wallet had more than 1% exposure. NYDFS stated "Any amount of funds transferred to terrorism-connected wallets is illegal," and Block rated mixer exposure as only "medium" risk. Amount: **$40 million.** Undertakings: engage an independent monitor. Liability admitted: no. (CONFIRMED FACT.)

4. **Multistate consumer-protection settlement (46 states + DC) — 8 July 2026.** Entity: Block, Inc. Regulators: 46 state attorneys general (all except Hawaii, Missouri, South Carolina, Wyoming), led by Oregon and Texas. Conduct: misleading consumers that Cash App was as safe as a bank, failing to protect against fraud and to provide promised fraud protection/dispute resolution; allowing account creation without SSN/DOB and no cap on accounts per person. Oregon AG Dan Rayfield: "Cash App told people their money was safe, and millions of Oregonians and Americans believed them, including a lot of people who didn't have other options." Amount: **$45 million** in civil penalties distributed by population formula (Oregon $3 million; Colorado $1,663,539; Virginia ~$845,500 as examples). This reaffirmed — but did not add to — the CFPB's $75–120m consumer redress. Undertakings: 24-hour phone support, fraud education, maintained dispute processes. Liability admitted: no. (CONFIRMED FACT.)

5. **Washington State settlement — 8 July 2026.** Entity: Block, Inc. Regulator: Washington Attorney General Nick Brown. Conduct: Washington alleged Cash App "processed at least $22 million in fraudulent payments over a five-month span in 2020 using stolen personal information" — pandemic-era unemployment-insurance fraud. Amount: **$20 million.** Liability admitted: no. (CONFIRMED FACT.)

**Earlier/adjacent items.** A 2024 Cash App Investing class action ($15 million) covered 2022–2023 data-security incidents (claim deadline November 2024) — a private action, not a regulator, but part of the cost picture. Afterpay's 2020 California settlement (~$1 million refunds/fines plus obtaining a CFL licence) predates Block's ownership but transferred with the acquisition. (CONFIRMED FACT.)

**What the aggregate reveals.** Every major regulatory action concerns Cash App's AML/BSA and consumer-protection controls during and immediately after its explosive 2019–2021 growth. The regulators' own findings — a SAR backlog that grew from 18,000 to over 169,000 alerts, unverified "restricted" accounts, a 10% terrorism-wallet threshold, no live customer service — are textbook symptoms of a compliance function that did not scale with the product. **Analytical inference: Block's compliance capability materially lagged its licensing ambition, and it paid roughly $340 million in 2025–26 penalties (plus consumer-redress administration, an independent monitor and an independent consultant) to catch up. The licences were obtained; the operational capability to honour their obligations was retrofitted under enforcement pressure.**

### II.5 The Cost of the Estate (quantified)

- **Regulatory capital trapped at SFS:** approximately $56m paid-in at opening (2021), growing to roughly **$845 million of equity by Q3 2025** (THIRD-PARTY, FDIC call-report-derived aggregator estimate), held at a permanent **20% leverage ratio** — i.e., SFS must hold roughly double the capital a normal bank would against the same assets. Plus a $50m reserve deposit and a committed third-party line of credit. This is capital Block cannot freely deploy elsewhere.
- **Loans on Block's balance sheet (consequence of owning the bank):** loans held for investment grew from $124.0m (2022) to $247.6m (2023) to $365.1m (2024); loans held for sale grew from $474.0m (2022) to $775.4m (2023) to $1,111.1m (2024). From 1 July 2025 Block began retaining Cash App Borrow, Afterpay Post-Purchase and SFS-originated loans as held for investment, materially increasing on-balance-sheet lending. The consolidated allowance for credit losses ended 2024 at $201.8m (from $185.3m at end-2023).
- **State MTL bonding and permissible-investment burden:** an estimated seven-figure aggregate of surety bonds and net-worth commitments across 48-plus states and territories (THIRD-PARTY practitioner estimate; Block does not break this out).
- **Enforcement penalties paid (2025–26):** ~$80m + $175m + $40m + $45m + $20m ≈ **$340 million**, plus consumer redress administration, an independent monitor and an independent consultant.
- **Compliance headcount/spend:** UNKNOWN — Block does not disclose a compliance-specific figure. (Context: Block reduced headcount from over 10,000 toward under 6,000 alongside FY2025 results, citing automation/AI; R&D was ~$2.9bn in FY2025; neither is compliance-specific.)
- **As a share of gross profit:** against gross profit of $8.889bn (2024) and ~$10.36bn (2025, up 17% year-over-year, with December 2025 the first month in company history to exceed $1 billion of gross profit), the ~$340m of one-time penalties is roughly 3–4% of a single year's gross profit; trapped SFS capital of ~$845m is under 10% of one year's gross profit. **Analytical inference: the regulatory estate is a meaningful but not existential cost for Block at scale, and the penalty component (a one-time catch-up) should fall as a share of gross profit going forward as remediation completes — but the trapped-capital cost of owning the bank is permanent and rises with the loan book.**

### II.6 What Each Rung Permits and Forecloses (matrix)

| Rung | Permits | Forbids | Capital / bonding | Time to obtain | Supervisory burden | **Forecloses (what gets harder once held)** |
|---|---|---|---|---|---|---|
| **Payment facilitator** (under acquirer) | Onboard/settle for millions of sub-merchants fast | No charter; bound by acquirer & card-network rules; must migrate large sub-merchants to direct agreements | Set by acquirer (reserves, guarantees) | Weeks–months (acquirer sponsorship up to ~6 months) | Card-network + acquirer oversight; PCI-DSS | Ties you to one acquirer's rules and risk appetite; chargeback/fraud liability concentrates in you |
| **State MTL** (×48+ + territories) | Hold and transmit customer funds | Cannot lend or take deposits; permissible-investment rules restrict use of float | Net worth ~$25k+ per state; bonds ~$10k–$7m/state; seven-figure aggregate | Many months to years for full national coverage | Multi-state exams; NMLS reporting; BSA/AML | Every product change must be re-cleared across dozens of regulators; creates 48+ enforcement fronts (as the $80m/$45m settlements show) |
| **FinCEN MSB registration** | Legally operate as MSB federally | Does not substitute for state MTLs | Registration only | Days (registration) | BSA/AML program, SARs, CTRs, sanctions screening; federal exam exposure | Locks in permanent SAR/monitoring obligations that, if under-resourced, become enforcement liabilities |
| **Bank partnership** (Celtic/First Electronic) | Lend without a charter; bank insulated from state usury caps | Cannot take deposits; partner is creditor and sets terms; dependent on partner risk appetite | Partner holds capital; you post reserves/buy loans | Weeks–months to contract | Indirect (partner supervised; you as service provider) | Caps economics at fees/gains-on-sale; partner can constrain or exit; hard to control product design |
| **BitLicense** (NYDFS) | Sell/custody crypto in New York | Tightly conditioned; NY-specific | High application cost; capitalization requirements | Months–year (very stringent) | NYDFS virtual-currency + MT exams | Subjects crypto ops to NY's exacting standard nationwide in practice; adds a distinct enforcement front (contributed to the $40m order) |
| **Broker-dealer** (Cash App Investing) | Offer securities trading | Introducing broker relies on carrying broker; not an adviser | Net-capital rule; SIPC assessments | Months (FINRA membership) | SEC + FINRA + SIPC | Brings FINRA supervision, net-capital constraints, best-execution/Rule 606 obligations onto the group |
| **Industrial bank charter** (SFS) | Balance-sheet lending + retention; FDIC-insured deposits; full spread; product independence | Must operate within FDIC-approved business plan; affiliate-transaction limits; no dividends yr 1–3 without approval | ~$56m initial → ~$845m equity; **20% leverage ratio**; $50m reserve; committed LOC | ~3.5 years (2017 apply → 2021 open) | FDIC + Utah DFI exams reaching into parent; CALMA; Parent Company Agreement; source-of-strength; independent-majority board | **Traps capital at ~2× normal leverage; imposes parent supervision & source-of-strength; personal commitment by controlling shareholder; annual FDIC-approved business plan; politically contested (could narrow)** |

### II.7 THE TRANSPLANT VERDICTS (with reasoning, against Nigerian conditions)

**(a) The bank-partnership-first sequence → ADOPT.** Starting under a licensed entity's charter is the single most transferable mechanism in this volume. It transfers because its logic is institution-agnostic: a technology company performs marketing, onboarding, underwriting-support and servicing while a licensed bank is the creditor/holder of funds. Nigeria's own ladder supports exactly this — the reader's plan (cooperative society → partnership with a licensed entity → Super-Agent → IMTO agency → CBN deposit-taking licence) is structurally identical to Square 2014–2021. *What must be watched (the ADAPT caveat inside the ADOPT):* Celtic's insulation from state usury caps was a US-specific benefit; Nigeria's interest-rate environment and the CBN's consumer-protection rules must be checked so the bank-partner does not simply pass through a rate the reader cannot legally charge. **The institutional feature doing the silent work in the US** was not the partnership itself but (i) a deep forward-flow institutional market that bought Square's loans within days and (ii) bank pre-emption of state rate caps. Nigeria has (i) only thinly — so the reader must fund the book from the cooperative's own deposits or patient capital, not assume a securitization exit.

**(b) The industrial bank charter → REJECT (but map the function).** There is no Nigerian ILC equivalent — no charter that lets a commercial parent own a deposit-taking bank while escaping central-bank holding-company supervision. The specific US feature doing the work is the BHCA Section 2(c) exception, which Nigeria simply does not have. **But the reader must not stop at "reject."** What the charter *bought* Block was three separable things: (1) the right to take insured deposits as funding; (2) the right to retain loans and earn the full spread; (3) independence from a partner's risk appetite. In Nigeria those functions map onto the CBN deposit-taking ladder: a **Unit Microfinance Bank (₦50m–₦200m)** buys local deposit-taking and balance-sheet lending at the lowest capital; a **State Microfinance Bank (₦1bn)** widens geography; a **National Microfinance Bank (₦5bn)** or **Payment Service Bank (₦5bn)** buys national reach. The nearest functional equivalent of "owning the bank" at the lowest capital is therefore the **Unit or State MFB licence**, not a PSB — because the reader's objective is *lending to cooperative members from a deposit base*, which the MFB regime permits and the PSB regime restricts (PSBs generally cannot lend). *Precise transplant:* pursue the MFB licence for the deposit-and-lend function; do not chase a mythical ILC analogue.

**(c) State-by-state money-transmitter licensing → REJECT as a burden; Nigeria's single national regime is materially EASIER.** The US federated MTL regime is a pure cost of American federalism: 48+ separate licences, bonds, net-worth tests and renewal calendars, and — as Block's $80m and $45m settlements show — 48+ enforcement fronts. Nigeria's CBN runs a single national licensing regime (Super-Agent ₦50m, PSSP ₦100m, MMO ₦2bn, PSB ₦5bn). **The institutional feature doing the work in the US is fragmentation, and its absence in Nigeria is a genuine structural advantage for the reader** — one national regulator, one rulebook, one capital test. The reader should treat this as a tailwind, not replicate the US pain. The trade-off: a single regulator is also a single point of failure (one CBN sanction hits everything), so concentration risk replaces fragmentation risk.

**(d) Deposit-taking as a funding strategy → ADAPT (with a hard warning).** Deposit funding transferred brilliantly for Block because US deposits are FDIC-insured to $250,000 and Americans trust non-bank-branded deposit-takers backed by that insurance. Nigeria has the **Nigeria Deposit Insurance Corporation (NDIC)**, but coverage limits are lower, reach is thinner, and public trust in non-bank deposit-takers is materially weaker after repeated failures of unlicensed "wonder banks" and Ponzi schemes. **The silent institutional work in the US was done by FDIC insurance and the trust it manufactures, not by the deposit product itself.** *Precise adaptation:* the reader can use member deposits as a funding base *only* through a properly NDIC-insured MFB licence, and must invest disproportionately in visible trust signals (NDIC signage, transparent audits, cooperative-member governance) to overcome the trust deficit. Do **not** attempt to fund lending from uninsured "savings" held under a cooperative or Super-Agent wrapper — that is precisely the structure Nigerian regulators and the public associate with fraud, and it is the fastest route to a run and a shutdown.

**(e) Building compliance capability after scaling → REJECT as a template for a small founder (it is a privilege of scale).** Block scaled Cash App to 50m+ users first and retrofitted AML/BSA and consumer-protection compliance under ~$340m of enforcement pressure. It survived only because it had the balance sheet to absorb the penalties and the revenue to fund an independent monitor and a compliance rebuild. **A capital-constrained Nigerian founder has no such buffer: a single CBN/NFIU AML sanction or a frozen settlement account can be terminal.** The specific feature doing the work for Block was scale-derived financial resilience, which the reader lacks by definition. *Precise adaptation:* the reader must sequence compliance *ahead of or in lockstep with* growth — a designated compliance officer, a written AML/CFT program, transaction monitoring and CBN/NFIU SAR capability from the first licensed rung — even though this is slower and costlier per user early on. This is the single most important inversion of Block's playbook the reader must make.

### II.8 Volume II Reconstruction

**(1) Chronological licence ladder.** 2009 incorporation & PayFac under JPMorgan/Paymentech → 2013 NY money-transmitter licence (and the broader 48+ state MTL build) + FinCEN MSB registration → May 2014 Square Capital (MCA) → March 2016 Celtic Bank loan origination → June 2018 NYDFS BitLicense → ~2019 Cash App Investing broker-dealer (FINRA/SIPC) → Sept 2017 ILC application, Dec 2018 refiling, March 2020 FDIC approval, **1 March 2021 SFS opens** → 31 January 2022 Afterpay acquisition → 2025 SFS assumes Cash App Borrow/consumer lending.

**(2) Permits-and-forecloses matrix.** See II.6.

**(3) Industrial bank analysis.** See II.2 — the pivot; a grandfathered ILC charter with a permanent 20% leverage ratio, CALMA, Parent Company Agreement and source-of-strength obligation, contested by ICBA/BPI/CRL but not yet closed by Congress.

**(4) Bank-partner economics.** See II.3 — Celtic as lender of record; Square purchased loans within 1–2 days and sold most to investors; Square bore retained credit risk; exact fee split UNKNOWN; discontinued for business loans April 2021.

**(5) Enforcement ledger.** See II.4 — $80m (48-state, Jan 2025), $175m (CFPB, Jan 2025), $40m (NYDFS, Apr 2025), $45m (46-state, Jul 2026), $20m (Washington, Jul 2026).

**(6) Cost of the estate.** See II.5 — ~$845m trapped SFS equity at 20% leverage; ~$340m penalties; seven-figure MTL bonding; compliance spend UNKNOWN; ~3–4% of one year's gross profit in one-time penalties.

**(7) Transplant verdict table.**

| Mechanism | Verdict | Core reasoning |
|---|---|---|
| Bank-partnership-first sequence | **ADOPT** | Institution-agnostic; matches the reader's own plan; watch usury pass-through and absence of a deep loan-buying market |
| Industrial bank charter | **REJECT** (map function to MFB licence) | No BHCA-exception equivalent in Nigeria; function = deposit + retained lending = Unit/State MFB licence |
| State-by-state MTL regime | **REJECT** (Nigeria easier) | US fragmentation is a cost of federalism; CBN's single national regime is a genuine advantage |
| Deposit-taking as funding | **ADAPT** | Works only via NDIC-insured MFB + heavy trust-building; never via uninsured wrappers |
| Compliance-after-scaling | **REJECT** as template | Survivable only with scale-derived financial resilience; reader must sequence compliance first |

**(8) Key unknowns.** Exact Square–Celtic fee economics; Block's compliance headcount/spend; exact FY2025 loans-held-for-investment total and full-year Square Loans origination; precise entity-by-entity international authorizations; the ultimate fate of the ILC loophole in Congress.

**(9) Ten most important conclusions.**
1. The ladder is a strategic sequence, not a checklist — each rung changed what Block could be.
2. The bank-partnership-first posture is viable for years and scales to billions in volume before an owned charter is justified.
3. The ILC charter was the pivot: it converted Block from a fee-earning facilitator into a spread-earning, deposit-funded lender.
4. The charter's price is permanent — trapped capital at a 20% leverage ratio, parent supervision, source-of-strength, and a personal commitment by the controlling shareholder.
5. Owning the bank foreclosed more than renting it: FDIC/Utah exams reach into the parent in ways a partnership never did.
6. The enforcement record proves compliance lagged licensing — every major action is a Cash App AML/consumer-protection failure from the 2019–2021 growth phase.
7. Block absorbed ~$340m in penalties because it had the scale to; a small founder cannot.
8. For Nigeria, the bank-partnership sequence ADOPTS, the ILC charter REJECTS (map to an MFB licence), the federated MTL regime REJECTS (CBN is easier), deposit funding ADAPTS (only via NDIC-insured MFB), and compliance-after-scaling REJECTS as a template.
9. The specific US institutional features doing silent work — the BHCA exception, FDIC insurance and the trust it manufactures, a deep forward-flow loan market, and bank pre-emption of state rate caps — are exactly what Nigeria lacks, and each must be consciously substituted.
10. The single inversion the reader must make is to sequence compliance ahead of scale.

**Which rung mattered most?** The industrial bank charter — it changed the economics of lending categorically. **Which was hardest to obtain?** The same charter (3.5 years, a withdrawal and refiling, a contested FDIC vote, extraordinary conditions) — closely rivalled by the NYDFS BitLicense as the hardest single licence. **Which was most expensive to maintain?** The charter, via ~$845m of trapped capital at a 20% leverage ratio plus source-of-strength — far exceeding the one-time penalties. **What did Block gain by owning a bank that it could not rent?** Insured deposit funding, retention of the full interest spread, and independence from a partner's risk appetite — the ability to build lending as a first-class product rather than a facilitated fee line.

**The central question — is the licence ladder a sequence a small, capital-constrained founder can realistically climb, or a structure only available to a company that has already achieved scale by other means?** The *lower rungs* (cooperative/partnership/agency, and in Nigeria a Unit MFB) are genuinely climbable by a small founder and are the correct starting sequence. The *upper rungs* — an owned, deposit-taking, balance-sheet-lending bank with the capital and compliance apparatus it demands — were in Block's case only reachable *after* Cash App and Square had achieved scale (and profitability) by other means, and only survivable because that scale absorbed ~$340m of enforcement cost. **The honest verdict: the ladder is climbable rung-by-rung, but the top rung is a privilege of prior scale. The reader should climb the lower rungs deliberately, fund lending from insured deposits rather than a securitization market Nigeria lacks, and — the one non-negotiable inversion of Block's playbook — build compliance capability *before* scaling, not after, because unlike Block the reader cannot buy his way out of an enforcement failure.**

---

## RECOMMENDATIONS

1. **Start exactly where Square started, and know the ceiling in advance.** Launch under a licensed partner's charter (the reader's cooperative → partnership → Super-Agent → IMTO-agency plan). Treat this as a multi-year posture, not a stopgap — Square ran it profitably from 2014 to 2021. But model the ceiling now: fee economics, no deposits, dependence on the partner. *Benchmark that changes the plan:* when annual facilitated-loan volume through the partner would generate more net margin if held on your own balance sheet than the fees you pay away, it is time to pursue a CBN deposit-taking licence — model this explicitly each year.

2. **Target a Unit Microfinance Bank licence (₦50m–₦200m) as the functional equivalent of "owning the bank," not a PSB.** The MFB regime buys the two things the ILC charter bought Block — insured deposit funding and retained-spread lending — at the lowest Nigerian capital. A PSB (₦5bn) cannot lend and is the wrong tool for a credit-led cooperative model. *Benchmark:* pursue the MFB licence once the cooperative's member deposit base and loan demand justify the ₦50m+ capital and the compliance overhead.

3. **Fund lending from NDIC-insured deposits, never from uninsured wrappers.** The single biggest silent enabler for Block was FDIC insurance and the trust it manufactured. Replicate the *function* by taking deposits only inside an NDIC-insured MFB and over-investing in visible trust signals. *Threshold that should stop you cold:* if a proposed structure holds member "savings" outside NDIC insurance to fund loans, do not build it — that is the "wonder bank" pattern Nigerian regulators shut down.

4. **Invert Block's compliance sequencing — build it first.** Appoint a compliance officer, write an AML/CFT program, and stand up transaction monitoring and NFIU SAR capability from the first licensed rung. *Benchmark:* compliance headcount and spend should scale with transaction volume from day one, not lag it. This is the one place where copying Block would be fatal.

5. **Exploit Nigeria's single national regime as an advantage.** Do not replicate the US state-by-state pain; the CBN's one national rulebook is a structural tailwind. But hedge the concentration risk of a single regulator by maintaining an unimpeachable examination record — one CBN sanction hits everything.

6. **Sequence the IMTO capability through an agency/partnership, given the USD 1m barrier and the fintech-direct-holding prohibition.** Since Nigeria bars fintechs from holding the IMTO licence directly, the remittance rung must be climbed via partnership — the same rent-the-charter logic as Square/Celtic. Confirm the current CBN IMTO guidelines before committing capital.

---

## CAVEATS

- **Evidence grade.** Charter conditions, capital requirements, enforcement amounts and dates are CONFIRMED against FDIC decision documents and speeches, CSBS/NYDFS/CFPB consent orders and state-AG releases, and Block SEC filings. SFS's ~$845m current equity is a THIRD-PARTY aggregator figure derived from FDIC call reports, not a Block-disclosed consolidated line item — treat as directional. Some origination-volume figures come from deBanked's compilation of Block shareholder letters (reliable but secondary).
- **Unknowns are flagged, not filled.** The exact Square–Celtic fee split, Block's compliance headcount/spend, and precise FY2025 loan-book totals are UNKNOWN and should not be inferred.
- **The ILC loophole is a moving target.** The route remains open as of late 2025 but is under active FDIC and Congressional pressure (ICBA/BPI/CRL campaigns; the Close the Shadow Banking Loophole Act). Block's charter is grandfathered; a new entrant's would not necessarily be. This does not affect the Nigerian transplant (there is no ILC route there anyway) but matters for understanding why the mechanism cannot simply be copied.
- **Transplant verdicts are analytical.** They apply the Guinnane test — mechanism vs. institutional environment — and identify the specific US feature doing silent work in each case, but they are ANALYTICAL INFERENCE, not settled fact, and should be pressure-tested against current CBN and NDIC rules, which change.
- **Nigerian regulatory figures** (capital thresholds for each CBN rung, NDIC coverage, the ~13%-of-adults credit-bureau coverage, the IMTO USD 1m requirement, the fintech-direct-holding prohibition) are drawn from the reader's own brief and general knowledge; verify each against current CBN circulars before acting, as these are periodically revised.

---

# VOLUME III — Square: The Seller Ecosystem

### A Forensic Reverse-Engineering of Block, Inc. (NYSE: XYZ) — Playbook Extraction for a Nigerian Cooperative-Banking Founder

## TL;DR
- **Micro-merchant payments are not a standalone business — they never were.** Square's own history shows the free reader and instant onboarding were a loss-leading acquisition channel (hardware ran a ~$93m gross loss in FY2024) whose economics only close because payments is the *wedge* into two profit engines: high-margin software/integrated payments (~59% of Square gross profit) and settlement-controlled lending/banking (~23%). The "we serve small business" narrative is marketing; the economics increasingly depend on mid-market sellers (>$500k GPV), whose GPV share reached 45% in Q3 2025, up from 41% in Q3 2023 and ~24% in 2018.
- **The upmarket drift was both pulled and pushed** — pulled by larger sellers wanting the product, and pushed by the fixed-fee/cost-to-serve arithmetic that makes the smallest tickets structurally thin. Take rate is compressing (Square transaction gross profit ≈1.13–1.15% of GPV, drifting down ~1–2 bp/quarter) precisely because bigger sellers negotiate lower rates — the signature of the mix shift.
- **The transferable finding for Nigeria: software, not payments, is the business — and the cooperative society is a pre-built payment-facilitator that Square had to manufacture.** Under a 0.5%/₦10,000-capped merchant service charge there is no acquiring spread to fund free hardware, so the free-hardware wedge is REJECT; instant onboarding via aggregation is ADOPT (the cooperative *is* the master-merchant); software-as-margin-engine is ADOPT-with-adaptation; and serving micro-merchants is viable only as a distribution channel for savings, credit and software — never on payment economics alone.

## Key Findings

**1. Who the seller is.** In FY2024 more than 4 million sellers used Square to make 5.2 billion transactions totaling $228bn of Square GPV, across 8 countries (US, Canada, Japan, Australia, UK, Ireland, France, Spain). Square defines seller size by annualized GPV: **small (<$125k), SMB ($125k–$500k), mid-market (>$500k)**. The vertical mix (FY2023 10-K) was food & drink 32%, retail 18%, professional services 11%, beauty & personal care 10%, healthcare & fitness 9%, other 20% — a shift from the 2020 snapshot (food & drink 27%, retail 19%, professional services 15%). Square is the #1 US merchant acquirer by merchant count (~4m).

**2. The wedge is a deliberate loss.** Square began with a free magstripe reader priced below manufacturing cost and a $59 contactless/chip reader; the current hardware line is Reader for magstripe (first one FREE), Reader for contactless and chip ($59), Square Stand ($149), Square Kiosk ($149), Square Terminal ($299), Square Handheld ($399), and Square Register ($799–$899). **Hardware is an acquisition tool, not a profit center**: FY2024 hardware revenue was ~$143.4m against ~$236.4m cost of revenue — a **~$93.1m gross loss** (FY2023 ~$110.5m loss; FY2022 ~$122.6m loss). On Square's Q3 2016 earnings call, then-CFO Sarah Friar told analysts it takes four to five quarters for Square to break even on its hardware sales by monetizing them through payments.

**3. Software is the margin engine.** Square gross profit splits (ex-PPP) into three strands; as of Q1 2024 these were **Software & Integrated Payments ~59%, "Sidecar" (standalone) Payments ~20%, Banking ~23%** (Banking rose from 17% in Q1 2020; Sidecar Payments fell from 34%). Software & integrated payments is the fastest-growing, highest-margin, most genuinely "technology" strand. In Q4 2024, Square gross profit grew 12% year over year (down from 18% a year earlier), driven by software and integrated payments and banking products. Square operates 30+ products across commerce, staff, marketing and banking.

**4. Land-and-expand works and is measurable.** Square Loan borrowers use 3.7 products on average vs 1.5 for non-borrowers; ~38% of Square gross profit in 2021 came from sellers using four or more products; sellers adopting the full software suite post ~9% higher sales. Square Loans repay as a fixed % of daily card sales deducted before settlement — Q4 2024 originations of $1.54bn brought the full-year 2024 total to **$5.7bn** (the largest online business lender deBanked tracks), at an average loan size of nearly $10,000. Square Financial Services (Utah industrial bank, live 1 March 2021) supplies deposits (Square Savings >$300m by end-2024) and now originates loans directly.

**5. The upmarket drift, with data.** Mid-market (>$500k) GPV share: ~20–24% (2018) → 34% (Q3 2021) → 41% (Q3 2023) → 45% (Q3 2025). Larger sellers (>$125k) were 52% of GPV as early as Q3 2018 and ~40% of the seller *base* by Q3 2022 (from 31% in Q3 2020). Block courted them with interchange-plus custom pricing (for sellers >$250k/yr with average ticket >$15), a dedicated field sales force, deeper vertical software, and now 100+ ISO partnerships. The consequence: take-rate compression (transaction gross profit as % of GPV ~1.15% in 2023 → ~1.13–1.14% in 2024, drifting down ~1–2 bp/quarter). Management explicitly calls upmarket mix and hardware costs a "headwind" to gross-profit growth.

**6. Seller mortality is a real exposure but is managed structurally.** Accrued transaction-loss provisions rose sharply in stress (provision $109.4m in 2020 vs $79.4m in 2019 as COVID raised seller failure and non-delivery chargebacks). Square does not hold merchant reserves and sometimes declines to pursue chargebacks for relationship reasons — the price of frictionless onboarding. But settlement-controlled loan repayment (deducting from daily card sales before the seller sees the money) largely insulates the lending book from seller failure, which is why the lending business scales.

## Details

### III.1 The Seller Universe
Square's chief operating decision maker reports two segments — **Square** (formerly "Seller") and **Cash App**. Square sellers "range from sole proprietors to multinational businesses" across the US, Canada, Japan, Australia, the UK, Ireland, France and Spain. FY2024: **>4 million sellers, 5.2 billion transactions, $228bn Square GPV, >800 million payment cards, >300 million buyer profiles.** No customer exceeded 5% of Square GPV in 2022–2024 — a genuinely diversified, long-tail base.

**Size definitions (CONFIRMED FACT, 10-K):** small <$125k annualized GPV; SMB $125k–$500k; **mid-market >$500k.** Note the definition has drifted: in 2018–2019 shareholder letters "larger sellers" meant >$125k; Block now emphasizes the >$500k mid-market band as its growth story.

**Vertical mix (CONFIRMED FACT):** FY2023 — food & drink 32%, retail 18%, professional services 11%, beauty & personal care 10%, healthcare & fitness 9%, other 20%. The 2020 snapshot was food & drink 27%, retail 19%, professional services 15%. **ANALYTICAL INFERENCE:** food & drink's rising share reflects Square for Restaurants pulling the company toward higher-GPV, higher-complexity sellers — the vertical where it competes with Toast.

**UNKNOWN:** the exact FY2024 seller-size band percentages and FY2024 vertical percentages are published only as chart images in the 10-K and could not be extracted as numbers; the directional trend (rising mid-market share) is firmly established from shareholder letters.

### III.2 The Original Wedge — Hardware, Onboarding, Payment Facilitation
Square's founding mechanism (carried forward from Volume II) was operating as a **payment facilitator (payfac) under a sponsoring acquirer** — JPMorgan Chase Bank, N.A. as Member and Paymentech, LLC as processor — aggregating sub-merchants under a master merchant account. This is what allowed **instant onboarding without underwriting each merchant as a bank would.** The risk Square absorbed in exchange: chargeback and fraud exposure it cannot always recover from a closed or bankrupt seller.

**Hardware line and pricing (CONFIRMED FACT, Square hardware pages, 2025–26):**
- **Square Reader for magstripe** — first one FREE (below-cost; the original wedge)
- **Square Reader for contactless and chip** — $59
- **Square Stand** (swiveling iPad POS) — $149
- **Square Kiosk** (self-service iPad) — $149
- **Square Terminal** (all-in-one with receipt printer) — $299
- **Square Handheld** (portable POS, launched 2025) — $399
- **Square Register** (dual-screen standalone) — $799 (a 2nd-generation Register at ~$899 also cited); kits (e.g., Stand Kit $579, Restaurant Stand Kit ~$1,488) bundle drawers/printers.

**Hardware as loss-leader (CONFIRMED FACT):** The FY2021 10-K states plainly: "Hardware is sold primarily as a means to grow our transaction-based revenue and, as a result, generating positive gross margins from hardware sales is not the primary goal." The FY2015 10-K: readers sold "modestly below our manufacturing costs" and "for Square Stand, our production costs substantially exceed our revenue." FY2024: **hardware revenue ~$143.4m, cost ~$236.4m, gross loss ~$93.1m** (a ~65% negative gross margin). Quarterly 2024 losses: Q1 $18m loss on $32m revenue; Q2 $25m loss on $43m revenue (Q3/Q4 not separately disclosed; Block discloses only the full-year total).

**Fraud/loss cost of instant onboarding (CONFIRMED FACT):** The provision for transaction losses ran $79.4m (2019) and spiked to $109.4m (2020) as COVID raised seller-failure and non-delivery chargebacks; accrued transaction losses ended 2020 at $70.6m. The FY2017 10-K acknowledges Square "do[es] not collect and maintain reserves from our sellers to cover these potential losses, and for customer relations purposes we sometimes decline to seek reimbursement." **This is the price of the wedge**: frictionless signup means Square eats a portion of fraud/chargeback loss.

### III.3 The Software Stack (the actual business)
Square monetizes 30+ products via transaction, subscription and service fees. As of October 2025, Square consolidated to **three unified plans across all business types: Free ($0), Plus ($49/mo per location), Premium ($149/mo per location)**, with higher tiers giving lower processing rates (Premium: 2.4% + 15¢ in-person). Legacy per-vertical pricing (e.g., Retail Plus $89/mo, Restaurants Plus $60–69/mo) is being phased out. The material products:

1. **Square Point of Sale** — the core app (free tier), now absorbing the vertical apps.
2. **Square for Restaurants** — table/course/floor management, kitchen display; Free / Plus $49 / Premium $149.
3. **Square for Retail** — inventory, COGS, purchase orders, barcode; Plus historically $89/mo.
4. **Square Appointments** — booking + POS for services/beauty; strong in beauty (high approval among personal-care professionals).
5. **Square Online / eCommerce** — free shoppable website; online rates 3.3% + 30¢ (Free) / 2.9% + 30¢ (paid).
6. **Square Invoices** — digital invoicing; passed >350,000 active sellers and >$5bn GPV as early as 2019.
7. **Square Payroll** — $35/mo base + $6/employee (historically $29 + $5).
8. **Square Marketing** — email/text campaigns, from ~$15/mo.
9. **Square Loyalty** — enrolled buyers >3x more likely to be repeat, spend ~50% more on average.
10. **Square Gift Cards** — buyer acquisition tool.
11. **Square Team Management / Shifts / Payroll / Advanced Access** — staff tooling ($5–6/employee tiers).
12. **Square Messages / Square AI / Square Assistant** — buyer communications and AI-enabled messaging.
13. **Square Banking** — Checking, Savings (1.00% APY via Square Financial Services), Loans, Square Credit Card.
14. **Square Developer / APIs / App Marketplace** — open platform for third-party integrations.
15. **Afterpay via Square** — BNPL at 6% + 30¢; drives demand discovery.

**Software as margin engine (CONFIRMED FACT):** Software & Integrated Payments was **~59% of Square gross profit** (Q1 2024), Banking ~23% and rising, standalone "Sidecar" Payments ~20% and falling. **ANALYTICAL INFERENCE:** software carries near-SaaS gross margins far above the ~1.13% payment take rate, and it is *sticky* — it is the retention mechanism, not the payment rail.

### III.4 Land-and-Expand and Cohort Economics
Block's stated mechanism: acquire on payments (mostly self-serve), then cross-sell software and banking. Evidence:
- **Multi-product = more gross profit:** ~38% of 2021 Square gross profit came from sellers using 4+ products.
- **Lending deepens engagement:** Square Loan borrowers use 3.7 products vs 1.5 for non-borrowers; SaaS attach ~10 points higher; 15% retention improvement for sellers adopting 3+ banking products.
- **Software = more sales:** full-suite adopters post ~9% higher sales.
- **Cohort payback & retention:** Block reports **seller cohort gross-profit retention** (YoY gross-profit growth of a quarterly cohort, ex-hardware/gift cards/Caviar). The 2020 seller cohort was pacing to ~five-quarter payback despite COVID. Square's model is designed so cohorts *expand* in aggregate — Block reported "positive growth in acquisition… and churn of existing sellers remained consistent" through 2024.
- **Upgrade path:** >40% of larger-seller GPV in Q3 2018 came from sellers who *started* as micro-sellers — the land-and-expand thesis in Square's own words.

### III.5 THE UPMARKET DRIFT (the central re-cut)
**The data (CONFIRMED FACT / COMPANY CLAIM):**
- Mid-market (>$500k) GPV share: ~20% (Q1 2018) → 24% (Q4 2018) → 34% (Q3 2021, per Square's Q3 2021 shareholder letter) → 41% (Q3 2023) → **45% (Q3 2025**, following 20% growth in that segment**)**.
- Larger sellers (>$125k) ≈ 52% of GPV in Q3 2018 (up from 48% a year earlier); larger sellers ≈ 40% of the seller *base* by Q3 2022 (from 31% in Q3 2020).
- Mid-market GPV consistently grew ~2x total GPV (e.g., +43% YoY in Q1 2021; +22% in Q1 2026).

**What Block did to court larger sellers:** interchange-plus custom pricing (sellers >$250k/yr, average ticket >$15); a dedicated field sales team (10–20% per-rep productivity gains cited in 2024; sales-led "New Volume Added" +62% YoY in Q4 2025); 100+ ISO partnerships added 2025; deeper vertical software (Restaurants, Retail); and named multi-location wins (Steak Escape, GOLFTEC, Ladurée Canada).

**Consequence for economics:** take rate compresses because larger sellers pay lower rates and negotiate interchange-plus — Square transaction gross profit ≈1.13–1.15% of GPV and drifting down ~1–2 bp/quarter. But **gross profit per seller rises** because larger sellers attach more software and banking. The trade is explicit: thinner payment margin, fatter software/lending margin, higher absolute gross profit per account.

**Was micro-merchant payments ever standalone profitable? The verdict (ANALYTICAL INFERENCE, strongly supported):** No. Consider the arithmetic of the 15¢ fixed fee (raised from 10¢ on 27 March 2025). On a $15 ticket, 2.6% + 15¢ = 54¢ of gross fee, of which interchange/assessments/processing consume the bulk; the residual against cost-to-serve (support, fraud provision, onboarding, the ~$93m hardware subsidy) is thin to negative for the smallest, lowest-frequency sellers. Square itself treats hardware as a loss and payments as a wedge; it reports cohort payback of ~five quarters — meaning a new seller is *underwater for over a year* before sales & marketing is recovered, and that only works if the seller survives and attaches software. **The push (fixed-fee/cost-to-serve math) and the pull (larger sellers wanted the product) are both real, but the push is decisive: micro-merchant payments do not clear cost-to-serve on their own.**

**Was the original constituency abandoned?** Not abandoned — *repriced and de-prioritized.* The March 2025 fixed-fee increase (10¢→15¢) and the Free-plan online rate hike (2.9%→3.3%) fall hardest on small, low-ticket sellers; the free plan's headline processing rates are the highest in Square's lineup. Square retains the micro-merchant as a **top-of-funnel acquisition and optionality play** (some become mid-market), but strategic priority, field sales and product depth now point upmarket. The framing note's first trap — accepting the "we serve small business" narrative — is confirmed: Block *serves* small business but increasingly *earns* from larger sellers.

### III.6 Retention, Churn and Seller Failure
Block reports gross-profit retention by cohort rather than logo churn. It states seller churn "remained consistent with prior periods" through 2024 and that cohorts show positive gross-profit retention in aggregate (negative dollar churn — expansion outweighs loss). **Seller failure exposure:** micro-merchants fail at high rates; Square's transaction-loss provision is the visible cost (spiking in COVID). Crucially, **settlement-controlled loan repayment** (fixed % of daily card sales deducted before settlement, 18-month cap, no new loan while overdue) means Square recovers lending principal from cash flow, not from a solvent balance sheet — so lending is structurally insulated from seller mortality in a way that a conventional term loan is not. **This is the single most important lending-design insight for the Nigerian reader.**

### III.7 Acquisition and CAC
Square's primary channel is **self-serve onboarding** — management calls it "Square's most important customer acquisition channel" and "one of our super powers… many of our competitors don't even offer this." Layered on top: retail distribution of hardware, a direct/field sales force for mid-market, ISO partnerships (100+ by 2025), and app-marketplace integrations. The Square online store drove ~45% of net Square revenue in 2024 (THIRD-PARTY ESTIMATE). **Payback:** ~five quarters for the 2020 seller cohort (COMPANY CLAIM). **ANALYTICAL INFERENCE:** micro-merchant CAC is low (self-serve) but so is gross profit per seller, so payback is long and survival-dependent; mid-market CAC is high (field sales) but justified by multi-product attach and higher GPV.

### III.8 International Square (seller-side only)
Square operates in **8 countries**: US, Canada, Japan (entered May 2013), Australia (2016, launched at 1.9% vs US 2.75%), UK, Ireland, France, Spain (Ireland/France/Spain added 2021). **International = 22% of Square GPV in Q1 2026, up from 18% a year earlier**, growing ~35% YoY (26% constant-currency) vs ~8% US. International gross profit grew 38% YoY in Q1 2024. Products travel unevenly: payments and core POS travel; banking/lending is being localized market-by-market (e.g., a merchant cash advance product launched in Japan). **ANALYTICAL INFERENCE:** international sellers skew toward the same SMB/mid-market profile; international is Square's current growth frontier as US GPV growth slows to single digits.

### III.9 Competitive Position in Seller Payments
- **US POS installed base (THIRD-PARTY ESTIMATE, 2024):** Square ~27–28%, Toast ~24%, Lightspeed ~7–8%, Clover/Fiserv ~5–6%, Shopify a few %, with NCR Voyix and Oracle Micros holding large legacy chain bases.
- **Restaurants (Baird, small-restaurant segment ≈75% of the ~730k US locations):** Square #3 with ~13% share behind the leaders; Toast ~130k–134k locations, Clover ~160k. Toast's direct-sales, restaurant-only model has taken the premium full-service restaurant segment; Clover leverages Fiserv's bank/ISO distribution.
- **eCommerce:** Shopify and Stripe dominate online-first; Square is stronger in omnichannel-from-physical.
- **Where Square wins:** self-serve onboarding, breadth of integrated ecosystem, services/beauty and quick-service verticals, and the banking/lending attach. **Where it has lost ground:** premium full-service restaurants (to Toast) and pure eCommerce (to Shopify/Stripe). This is why Square is racing upmarket and into verticals.

### III.10 THE TRANSPLANT VERDICTS

**(a) Free/subsidised hardware as an acquisition wedge — REJECT (as-is).**
*US institutional feature doing the silent work:* the ~2.6% US acquiring spread, itself resting on high US interchange, funds a ~$93m/yr hardware loss. *Nigeria:* the merchant service charge is capped at **0.5% / ₦10,000**, and all POS hardware is imported (prices doubled 2023–2025 on FX; Moniepoint mPOS ~₦15,500, OPay Mini ~₦8,500, Android units ₦22,500–₦50,000). There is no spread to subsidise free hardware. *What must change if adapting:* recover hardware cost explicitly (sale, lease, or caution-fee deposit — exactly what Moniepoint/OPay already do), or have the cooperative purchase/own terminals and amortise across members. Do **not** import Square's give-it-away model.

**(b) Instant onboarding under a payment-facilitator model — ADOPT (the cooperative is the payfac).**
*US feature doing the silent work:* the master-merchant/sub-merchant aggregation under a sponsoring acquirer, which let Square skip bank-grade underwriting. *Nigeria:* **the cooperative society is itself an aggregation and trust mechanism** — it already knows its members, holds their savings, and can vouch for them. This is precisely the function the payfac master account performed for Square, but *pre-existing and socially collateralised.* The reader does not acquire merchants one at a time; the cooperative delivers them pre-aggregated. *Adaptation:* the core-banking platform onboards members as sub-accounts under the cooperative's institutional relationship with a settlement bank/switch (NIBSS rails), with the cooperative absorbing residual risk the way Square's master account did. **This is the reader's structural advantage over Square.**

**(c) Software as the margin engine rather than payments — ADOPT (this is the thesis).**
*US feature doing the silent work:* payments is a toll, but software (~59% of Square gross profit) is where margin and retention live, because software is priced on value delivered, not on a regulated spread. *Nigeria:* since the acquiring spread is capped at 0.5% and cannot fund the business, **the ONLY way the model works is to monetise software/services, not payments.** A cooperative core-banking platform can charge for exactly the equivalents Square sells: bookkeeping/inventory, payroll/contribution management, loyalty, invoicing, savings-goal tools, and credit-scoring. *Adaptation:* price these as low, naira-denominated subscriptions or bundle them into cooperative membership dues; the payment rail is the wedge and the data source, never the profit center. **This is the single most important transferable finding.**

**(d) Land-and-expand across multiple products — ADAPT.**
*US feature doing the silent work:* each additional product (loans, payroll, banking) carries its own margin, and multi-product sellers churn less (38% of gross profit from 4+-product sellers). *Nigeria:* attach works, but each product's economics are thinner and the member's electronic volume may be a fraction of true (cash) revenue, so payment-linked products under-read the member's real activity. *Adaptation:* sequence the attach around **savings and credit first** (the cooperative's historic strengths and the highest-value products), then layer software; use cooperative-held savings and contribution history — not just electronic GPV — as the underwriting signal, since cash dominates.

**(e) Serving micro-merchants at all — ADOPT, conditionally (and this is the hardest verdict).**
*What Square's experience proves:* micro-merchant *payments* are not standalone viable; they are viable only as an acquisition channel for software and lending. *What must be true for the reader's model to work:* (i) the cooperative must **eliminate per-merchant acquisition cost** (it already has the members — Square's five-quarter payback problem largely disappears); (ii) the model must **monetise savings intermediation and credit**, not payment spread (the cooperative's traditional thrift-and-loan model already does this — members save into a pool, borrow at reasonable rates); (iii) **settlement-controlled repayment** (Square's design) must be replicated — deduct loan repayments from members' inflows/contributions before they hit the member, insulating credit from trader mortality; (iv) software must be cheap to deliver at scale (the proprietary core-banking platform provides this). Given the reader *starts* with the pre-aggregated distribution channel and the savings/credit engine Square had to build from scratch, **the micro-merchant model that failed as standalone payments for Square can work for the reader — but only because payments is the least important part of it.**

### III.11 Volume III Reconstruction

**(1) Seller universe:** >4m sellers, $228bn GPV, 5.2bn transactions (FY2024); size bands small <$125k / SMB $125k–$500k / mid-market >$500k; verticals food & drink 32%, retail 18%, professional services 11%, beauty 10%, healthcare/fitness 9%, other 20% (FY2023); 8 countries, international 22% of GPV (Q1 2026).

**(2) Hardware line & margins:** magstripe Reader FREE, contactless/chip $59, Stand $149, Kiosk $149, Terminal $299, Handheld $399, Register $799–899; FY2024 ~$143.4m revenue / ~$236.4m cost / **~$93.1m gross loss**; explicitly a loss-leader.

**(3) Software stack:** 30+ products; unified Free/$49/$149 plans (Oct 2025); Restaurants, Retail, Appointments, Online, Invoices, Payroll, Marketing, Loyalty, Gift Cards, Team Management, Banking, Developer/APIs, Afterpay. Software & integrated payments ≈59% of Square gross profit.

**(4) Land-and-expand:** 3.7 products/borrower vs 1.5; 38% of GP from 4+-product sellers; ~9% higher sales for full-suite adopters; ~five-quarter cohort payback (2020 cohort).

**(5) Upmarket drift:** mid-market GPV share 24% (2018) → 34% (Q3 2021) → 41% (Q3 2023) → 45% (Q3 2025); take rate 1.15% (2023) → ~1.13–1.14% (2024), compressing ~1–2 bp/quarter.

**(6) Retention/churn:** positive aggregate cohort gross-profit retention; churn "consistent"; lending insulated from seller failure by settlement-controlled repayment; transaction-loss provision $79.4m (2019) → $109.4m (2020).

**(7) Acquisition & payback:** self-serve primary channel; field sales + 100+ ISOs for mid-market; ~five-quarter payback; online store ~45% of net Square revenue (2024, estimate).

**(8) International seller facts:** 8 countries; 22% of GPV, growing ~35% YoY; payments/POS travel, banking localizes.

**(9) Competitive position:** Square ~27–28% of US POS installs (#1 by count), Toast ~24%, Clover ~5–6%; #3 in small restaurants (~13%); losing premium restaurants to Toast, online to Shopify/Stripe.

**(10) Transplant verdict table:**
| Mechanism | Verdict | Silent US institutional feature | Nigerian adaptation |
|---|---|---|---|
| Free/subsidised hardware wedge | **REJECT** | ~2.6% acquiring spread on high US interchange | Recover hardware cost (lease/deposit) or cooperative-owned terminals |
| Instant onboarding via payfac aggregation | **ADOPT** | Master-merchant/sub-merchant under sponsoring acquirer | Cooperative *is* the pre-built payfac; onboard members as sub-accounts on NIBSS rails |
| Software as the margin engine | **ADOPT** | Software priced on value, not regulated spread (~59% of GP) | Charge for core-banking software modules; payments is wedge, not profit |
| Land-and-expand multi-product | **ADAPT** | Each product carries own margin; multi-product reduces churn | Sequence savings/credit first; underwrite on savings history, not electronic GPV |
| Serving micro-merchants | **ADOPT (conditional)** | Micro-payments only viable as acquisition channel | Eliminate CAC via cooperative; monetise savings + credit; settlement-controlled repayment |

**(11) Key unknowns:** exact FY2024 seller-size band and vertical percentages (chart images only); Q3/Q4 2024 individual hardware losses; micro-merchant-specific churn and cost-to-serve; micro-merchant standalone profitability (not disclosed; inferred).

**(12) Ten most important conclusions:**
1. Micro-merchant payments are not standalone profitable; they are an acquisition channel — this is the finding of first importance.
2. Hardware is a deliberate loss (~$93m in FY2024), not a product line.
3. Software & integrated payments (~59% of Square gross profit) is the actual business.
4. Banking/lending (~23%, rising) is the second engine, insulated from seller failure by settlement-controlled repayment.
5. The upmarket drift is both pulled and pushed, but the fixed-fee/cost-to-serve math makes the push decisive.
6. Take rate compresses as the company moves upmarket — the arithmetic signature of the mix shift.
7. Land-and-expand is real and measurable (3.7 products/borrower; 38% of GP from 4+-product sellers).
8. Self-serve onboarding is the low-cost wedge; the payfac model is what makes it possible.
9. Square's original constituency was repriced and de-prioritized, not abandoned.
10. For Nigeria, the cooperative substitutes for mechanisms Square had to build (aggregation, distribution, savings/credit engine) — which is why the model that fails as standalone payments can succeed as cooperative financial services.

### The Answers to the Volume's Owned Question
- **What does a seller actually buy from Square?** Not a card reader — an *operating system* for the business: payment acceptance plus inventory, staff, marketing, banking and credit in one integrated, self-serve, transparent stack.
- **What keeps them?** Software depth and banking/lending attach — the more products, the lower the churn. Payments alone does not retain; the ecosystem does.
- **Which product generates the most gross profit / most retention?** Software & integrated payments generates the most gross profit (~59%); multi-product adoption (especially lending + banking) generates the most retention.
- **What does the move upmarket reveal?** That small-merchant *payment* economics do not clear cost-to-serve — the fixed fee is material on small tickets and immaterial on large ones, so the company must either move upmarket or monetise beyond payments.
- **The central question — is micro-merchant payments viable on its own economics, or only as an acquisition channel?** **Only as an acquisition channel.** The "something else" it acquires customers *for* is twofold: (1) high-margin business software, and (2) settlement-controlled lending and banking. For the Nigerian reader, this is liberating rather than discouraging: the cooperative already owns the distribution channel and the savings/credit engine, so the reader can run the viable half of Square's model (software + savings + credit) without needing the unviable half (payment spread) to work at all.

## Caveats
- **Evidence classification:** Segment gross-profit strand percentages (Software 59% / Banking 23% / Sidecar 20%) are COMPANY CLAIM from shareholder letters and are ex-PPP. Hardware FY2024 figures (~$143.4m rev / ~$236.4m cost / ~$93.1m loss) are CONFIRMED FACT from the 10-K/XBRL. Take-rate ~1.13–1.14% for FY2024 total company is an ANALYTICAL INFERENCE computed from disclosed dollar figures; the verbatim FY2024 full-year Square-segment take rate was not extractable.
- **UNKNOWN:** exact FY2024 seller-size band percentages and FY2024 vertical percentages (published only as chart images); Q3/Q4 2024 individual hardware gross losses (Block discloses only the full-year total); micro-merchant-specific churn rates and cost-to-serve (Block reports cohort gross-profit retention in aggregate, not by size band); micro-merchant standalone profitability is not disclosed by Block and is inferred.
- **Basis discipline:** US GAAP, USD, 31 December year-end. Segment reporting changed: BNPL split 50/50 Square/Cash App through Q3 2023, then fully in Cash App from Q4 2023; from FY2025 Block re-cut disclosure into Commerce Enablement / Financial Solutions / Bitcoin Ecosystem while retaining Square and Cash App as reportable segments. Bitcoin revenue is excluded from all gross-profit anchoring here.
- **Nigerian data:** the 0.5%/₦10,000 MSC cap is from the CBN's revised Guide to Charges (effective 1 May 2026, exposure draft April 2026); POS terminal prices and agent economics are from Nigerian trade press (TechCabal, Nairametrics, Legit.ng) and NIBSS data (8.3m registered terminals as of March 2025; mobile-money operators processed ₦71.5tn in 2024; NIBSS processed ₦1.07 quadrillion across all channels in 2024).
- **Forward-looking items** (2026 guidance, analyst price targets, Toast location projections) are flagged as projections in-text and are not treated as realized results.

---

# VOLUME IV — Cash App: The Consumer Ecosystem

### A Playbook Extraction for a Nigerian Cooperative-Banking Founder

## TL;DR
- **Cash App is not a peer-to-peer business; it is a lending-and-interchange consumer bank that used free P2P transfer as a near-zero-cost customer-acquisition subsidy.** Free P2P earns roughly 8% of Cash App gross profit (THIRD-PARTY ESTIMATE, carried from Volume VII), while "Financial Solutions" — Cash Card interchange, Instant Deposit fees, Borrow and interest — supply the overwhelming majority. The architecture is identical to Square's on the seller side: a free/near-free wedge subsidised by downstream monetisation. This is the architectural insight of the whole study.
- **The transferable half for the reader is the monetisation ladder, not the acquisition engine.** The cooperative already delivers members pre-aggregated, with an existing savings relationship and social collateral — the exact assets Cash App spent a decade and hundreds of millions of marketing dollars manufacturing. The reader should **discard the viral engine** and transplant the deepening ladder — contribution-flow-as-direct-deposit and settlement-gated lending — but **interchange cannot fund it in Nigeria**, so the profit engine must be lending spread, remittance FX and cooperative dues.
- **A Cash App active is worth what it converts into: a primary-banking (direct-deposit) active generates nearly 10x the gross profit of a peer-to-peer-only active** (CONFIRMED, Block Q4 2025). Gross profit per monthly active rose from $41 (Q4 2020) to $94 (Q3 2025), driven by *deepening* plus a deliberate shedding of unmonetisable users (actives sat flat at 57M for six straight quarters), not by headline user growth.

## Key Findings

**1. The consumer universe.** Cash App reached **59 million monthly transacting actives in December 2025** (CONFIRMED, Block Q4 2025 prepared remarks), up from 15M (2018), 36M (2020), 44M (2021), 51M (2022), 56M (2023) and 57M (2024). The user is disproportionately young, lower-income and Black. Per the Pew Research Center (July 2022 survey of 6,034 US adults), "lower-income adults are the most likely to say they use Cash App: About 36% say this, compared with 24% of middle-income and 18% of upper-income adults," and 59% of Black Americans say they ever use Cash App; via Payments Dive, "nearly 40% of 18-to-29-year-olds" used it. **The "underbanked" framing is partly true but overstated.** Per the FDIC 2023 National Survey (released 12 November 2024), only "4.2 percent of U.S. households (representing 5.6 million households) lacked a bank or credit union account," and "two-thirds (66.2 percent) of unbanked households relied entirely on cash" — using *no* payment app at all. Cash App is therefore not primarily an unbanked product; it is a *secondary* account for **banked-but-underserved** lower-income consumers that Block is converting into a primary one.

**2. The acquisition engine.** Customer acquisition cost was about $20 per user in 2019 (CFO Amrita Ahuja, J.P. Morgan conference) and, blended with other marketing, "$10 or less" with "less than one year payback" by the 2022 investor day (COMPANY CLAIM) — versus $250+ for a traditional bank checking customer. The mechanism is the P2P network effect (the shareable $Cashtag, the "pay me back for lunch" loop), a $5 two-sided referral, and cultural marketing (#CashAppFriday giveaways, hip-hop and creator partnerships). Pre-2021 cohorts returned "6x or greater over three years"; 2022–2023 cohorts paced to sub-one-year payback (CONFIRMED, Block). Marketing spend "increased by more than 2x in the second half of 2024 compared to the first half" as Block pivoted toward paid promotion of banking behaviour.

**3. The product ladder (twelve material products).** (1) **P2P transfer** — free; ~8% of gross profit; a subsidy. (2) **Cash App Card** — Visa debit issued by Sutton Bank and The Bancorp Bank, N.A., processed by Marqeta; ~0.9% interchange; **26M actives** of 59M (Dec 2025); Block estimates 21% of all US 18-to-21-year-olds used it in 2024. (3) **Direct deposit / paycheck** — routing/account numbers from Lincoln Savings Bank or Sutton Bank; **2.5M paycheck-deposit actives** (Dec 2024, +25% YoY). (4) **Instant Deposit** — 0.5–1.75%, min $0.25; ~29% of 2023 gross profit (35% ex-BNPL). (5) **Cash App Borrow** — $20–$500, flat 5% (~1.25% weekly late fee), now originated by Square Financial Services (FDIC approval March 2025); part of $18.5bn Q4 2025 consumer-lending origination, Borrow up >3x YoY; loss rates claimed under 3%. (6) **Afterpay Post-Purchase on the Card** — launched Feb 2025, >$3bn origination run-rate by early Oct 2025. (7) **Savings** — up to ~3.25–4.5% APY, premium tiers gated on $300+ monthly deposits (Cash App Green). (8) **Cash App Investing** (Cash App Investing LLC, FINRA/SIPC) — ~4M accounts holding/trading stock as of March 2022 (the only disclosed figure). (9) **Bitcoin** — >10M cumulative buyers by 2022; ~3% margin; ~6–7% of gross profit. (10) **Cash App Pay** — 6M actives (Dec 2024); ~2.9% merchant rate, the highest-monetising flow. (11) **Cash App Taxes** — free; a retention/data tool. (12) **Family/teen and kids' accounts** — 5M+ sponsored teen actives by 2025; managed accounts for children 6–12 launched 2025. Cash App Green is the status tier that bundles the ladder.

**4. The conversion funnel with rates.** 59M monthly actives → **26M Cash App Card actives (~44%)** → **9.3M primary-banking actives (~16%, +22% YoY in Dec 2025)** → **2.5M paycheck-deposit actives** (Dec 2024) → **5M Borrow actives** (Dec 2024). Gross profit per monthly active (annualised, ex-BNPL): **$41 (Q4'20) → $47 (Q4'21) → ~$59 derived (Q4'22) → ~$67 derived (Q4'23) → $75 (Q3'24) → $76 (Q4'24) → $81 (Q1'25) → $87 (Q2'25) → $94 (Q3'25).** The rise is deepening, not user growth — actives were flat at 57M for six consecutive quarters through Q1 2025.

**5. The single most important number.** A primary-banking (direct-deposit) active generates **"nearly 10x the gross profit of peer-to-peer–only actives"** (CONFIRMED, Amrita Ahuja, Block Q4 2025 prepared remarks). At the 2022 investor day Block framed the gap as *inflows* multipliers — direct deposit 6.5x, Borrow 4.5x, bitcoin ~4x, Cash App Card 2x the inflows of a P2P-only active, with a 1.7x monetisation-rate multiplier for multi-product adopters. Note the metric evolved from an inflows multiplier (2022) to a gross-profit multiple (2025); both say the same thing: **direct deposit is the master conversion event.**

**6. Is free P2P a business or a subsidy?** A **subsidy**. It earns ~8% of gross profit; Block loses money on each free withdrawal; and the company built stored balances (2016) and the Cash Card (2017) precisely to recover P2P's cost. This mirrors Volume III's finding on micro-merchant payments exactly — **Block runs the same free-wedge-plus-monetisation-ladder machine on both sides of the house.**

**7. The cost of frictionless onboarding.** Roughly **$340m in 2025–26 penalties**, overwhelmingly for Cash App: a **$175m CFPB order** (16 Jan 2025 — "$120 million to harmed consumers…a minimum amount of $75 million in refunds," plus a $55m penalty; redress checks began mailing 8 June 2026 via Epiq; Director Rohit Chopra: "Cash App created the conditions for fraud to proliferate on its popular payment platform"); **$80m to 48 state regulators**; **$40m to NYDFS** (10 April 2025); **$45m to 46 state AGs**; **$20m to Washington State**. The NYDFS consent order found: "Between 2018 and 2021, Block let a backlog of SAR alerts grow from 18,000 to over 169,000"; a single "SAR was filed for $1.6 million with 91 subjects that were holders of 16,811 accounts with 19,518 transactions"; and "approximately 25-30 subjects…were able to open 8,359 Cash App accounts using falsified information" (a Russian criminal network). Superintendent Adrienne Harris: "The rapid growth of Block's Cash App absent a robust compliance function created risk and vulnerabilities." **This is the deferred bill for frictionless signup — roughly $6 per active (ANALYTICAL INFERENCE, $340m/59M) — causally linked to the restricted-account, no-verification, no-live-support design that made CAC so low.**

**8. Competitive position.** Cash App wins P2P scale, culture and multi-product breadth among lower-income/younger users; **Chime** (~22M+ users) wins primary-banking depth as a purer direct-deposit-and-interchange neobank; **Venmo** (within PayPal) wins social/urban/higher-income; **Zelle** (Early Warning Services, bank-owned) wins bank-to-bank rent-sized transfers and shut its standalone app in April 2025. Cash App's differentiator is the super-app bundle none of the pure-plays match; its strategic pivot is toward older/wealthier and primary-banking users to lift gross profit per active.

## Details

### IV.1 The Consumer Universe
The largest age band is 25–34 (~26%), with 18–24 (~18%) and 35–44 (~24%) close behind; adoption falls sharply above 55. The income skew is decisive and inverts Venmo's more affluent profile. Cash App's own "Expanding Access and Financial Inclusion" white paper cites ~25 million unbanked/underbanked US households as its addressable mission — but the FDIC data show the truly unbanked are a small, largely cash-only population that Cash App does not reach. The honest reading (ANALYTICAL INFERENCE): Cash App serves the **banked-but-underserved** — people with a nominal bank account who transact primarily through a phone — and its "bank our base" strategy is an attempt to become their primary institution. Inflows were **$316bn in FY2025**, ~**$1,410 per active per quarter** in Q4 2025 (+12% YoY), but inflows are heavily skewed toward the direct-depositing minority (the 9.3M primary-banking actives), consistent with the 10x gross-profit gap.

### IV.2 The Acquisition Engine and Its True Net Cost
Reported CAC (~$10–$20) omits the running cost of the free rail — per-transaction costs on every free withdrawal, fraud losses, and (historically absent) support — plus the deferred ~$340m regulatory bill. Netting enforcement against acquisition raises the fully-loaded cost of a frictionlessly-acquired active materially above the celebrated figure. The engine is real and extraordinary; it is also not free once the compliance bill is counted.

### IV.3 The Product Ladder
Gross-profit composition (2023, THIRD-PARTY ESTIMATE via Popular Fintech using Marqeta disclosures): Financial Solutions ~38%; Instant Deposit ~29%; BNPL/Afterpay ~17%; P2P ~8%; Bitcoin markup ~7%. Excluding BNPL, Financial Solutions was ~46% and Instant Deposit ~35% of the ~$3.57bn base. Cash Card volume was ~$140bn in 2023 at ~0.9% interchange. Cash App Pay's ~2.9% merchant rate is 2–3x the monetisation of the Card and is Block's lever to grow gross profit without user growth. Stored customer funds were $1,851m (cash) at year-end 2024, up from $360m in 2023; balances turn over quickly (Volume VII), limiting float income relative to a chartered bank.

### IV.4 The Conversion Funnel and the BNPL Distortion
From Q4 2023 Block reallocated its entire BNPL platform into Cash App (previously split 50/50 with Square), **inflating apparent Cash App growth across the 2023–24 boundary** — BNPL gross profit was ~$298m in Q4 2024 alone. Adjusting for this, the underlying deepening is driven by Borrow (originations >3x YoY in Q4 2025; consumer-lending origination $18.5bn in Q4 2025, +69% YoY) and Card/Afterpay attach. Every annual cohort since 2013 shows positive gross-profit retention; 2024 Cash App retention was above 100%.

### IV.5 Free P2P: Business or Subsidy?
Subsidy, on three facts: ~8% of gross profit; a loss on each free withdrawal; and the deliberate 2016–17 build-out of balances and the Card to recover that cost. This is the same structural pattern Volume III found in micro-merchant payments — the free wedge exists to feed the monetisation ladder.

### IV.6 Monetisation Depth and the Banking Ceiling
Traction: 9.3M primary-banking actives (16% of base, +22% YoY). Ceiling: only ~16% are primary-banking after a decade of effort; balances turn over fast; and switching costs are structurally lower than in the Chase era, so Cash App cannot simply hammer its base with cross-sell as incumbents once did. Block captures the spending-and-small-credit slice of a lower-income consumer's financial life, not the whole of it.

### IV.7 The Cost of Frictionless Onboarding
The causal chain: frictionless signup (restricted accounts, no full verification) → low CAC and rapid growth → AML/fraud failures at scale → a 169,000-alert SAR backlog and mandated 24-hour live support → ~$340m in penalties. The near-zero-CAC economics were partly an accounting illusion that deferred compliance cost into a later, larger bill.

### The Nigerian Transplant Context
- **Interchange:** Nigeria's merchant service charge is capped at **0.5% (₦1,000 cap)** and the issuer's slice is a fraction of that — the US interchange subsidy that funds the Cash Card does not exist (Volume VII's decisive constraint).
- **NIP** already makes interbank transfers real-time and near-free — free-and-instant P2P is not a differentiator.
- **Incumbents:** OPay (~35M+ users), PalmPay (~35M registered users, 15M daily transactions) and Moniepoint already occupy the wallet space. Per Moniepoint's 2025 Year in Review (via TechCabal), it "processed over 14 billion transactions in 2025 worth ₦412 trillion ($294.03 billion)," claiming "eight out of 10 in-person payments in Nigeria."
- **EFInA 2023:** formal financial inclusion 64% (up from 56% in 2020); 26% financially excluded; and financial *health* fell to 16% (from 28% in 2020) — inclusion without resilience.
- **Cooperatives** already run the exact deepening ladder: monthly contributions (commonly ₦5,000–₦10,000), loans to members at ~5–6% (vs ~10% for non-members), and annual dividend/bonus — i.e. pre-aggregated distribution with an existing savings relationship and social collateral.

## IV.9 The Transplant Verdicts

- **Free P2P as an acquisition wedge — REJECT.** The silent US work is done by interchange, which lets Block give P2P away and recover cost on the Card. Nigeria has no interchange to fund the subsidy, NIP already closed the speed/cost gap, and OPay/PalmPay already occupy the space. The wedge has nothing to open.
- **The viral acquisition engine — REJECT / DISCARD (second re-cut, answered plainly).** This is the discardable half. The cooperative delivers members pre-aggregated with a savings relationship and social collateral — the reader already owns the outcome Cash App manufactured over a decade. Building virality would be paying to acquire what you already have.
- **Cash Card / interchange monetisation — ADAPT (heavily).** A card can exist for utility but cannot be the profit engine. What must replace interchange: **lending spread (settlement-gated), remittance FX margin, and cooperative dues/fees.**
- **Direct deposit as the conversion event — ADOPT, as the cooperative contribution flow.** This is the strongest transplant. The recurring, observable **cooperative contribution** is the Nigerian analogue to direct deposit: it signals primary-relationship status *and* underwrites lending. Where members are paid irregularly or in cash, contribution flows (plus agent-collected cash deposits) substitute for the paycheck. Cooperative contribution flows serve the function direct deposit serves for Cash App — the deepest transferable mechanism, consistent with Volume V.
- **Borrow — ADOPT, adapted to settlement control.** Small, short, flat-fee lending gated on observed inflows is what cooperatives already do informally. Automate eligibility on contribution history and control repayment at source (Volume VII: settlement-controlled repayment is the deepest transferable mechanism). The silent US feature is Block's real-time inflow data; the cooperative's contribution ledger is the analogue.
- **Investing and bitcoin — REJECT (for a cooperative).** Given the fiduciary character of a cooperative and Cash App's consumer-protection record, selling volatile, disclaimer-laden bitcoin (~3% margin) to thin-file members is inappropriate. Conservative savings/investment products may fit; speculative crypto does not.

## IV.10 Volume IV Reconstruction
(1) **Consumer universe:** 59M actives; young, lower-income, disproportionately Black and Southern; banked-but-underserved rather than truly unbanked. (2) **Acquisition engine:** ~$10–$20 CAC via the P2P network effect, but true cost inflated by a ~$340m deferred compliance bill. (3) **Product ladder:** twelve products, Financial Solutions dominant, bitcoin large in revenue but trivial in profit. (4) **Funnel:** 59M → 26M Card → 9.3M primary-banking → 2.5M paycheck → 5M Borrow. (5) **P2P verdict:** subsidy, not a business (~8% of gross profit). (6) **Banking ceiling:** ~16% primary-banking penetration is the current ceiling. (7) **Frictionless-onboarding cost:** ~$340m, ~$6/active. (8) **Competition:** super-app breadth vs pure-plays (Chime depth, Venmo social, Zelle bank rails). (9) **Transplant table:** reject the acquisition engine, adopt the deepening ladder, adapt away from interchange. (10) **Key unknowns:** exact P2P running cost; current Cash App Investing actives; Q4 2025 GP-per-active; the precise Nigerian issuer interchange slice. (11) **Ten conclusions** below.

**Ten most important conclusions.** (i) Cash App is a bank wearing a P2P app's clothes. (ii) Free P2P is a customer-acquisition subsidy, not a business. (iii) The same free-wedge/monetisation-ladder architecture runs on both sides of Block — the study's central pattern. (iv) Direct deposit is the master conversion event; a primary-banking active is worth ~10x a P2P-only one. (v) Gross profit per active rose by deepening and by shedding unmonetisable users, not by user growth. (vi) The "underbanked" story is overstated; the real base is banked-but-underserved. (vii) The ~$340m enforcement bill is the deferred, causal cost of frictionless onboarding. (viii) Interchange is the load-bearing US institution that does not exist in Nigeria. (ix) For the reader, the acquisition engine is the discardable half and the monetisation ladder is the transferable half. (x) The cooperative contribution flow is the Nigerian direct deposit — the hinge on which everything else (deepening, lending, retention) turns.

**The central question, answered.** Cash App is **a consumer bank that acquired its customers unusually cheaply, and then spent years discovering that the only way to pay for the free rail was lending and interchange.** It is both readings at once — a free utility that found its business model in Financial Solutions. **The reader should build on the second reading (the monetisation ladder) and discard the first (the acquisition engine), because the cooperative already solves acquisition and Nigeria removes the interchange that made the free rail affordable in the first place.**

## Recommendations
1. **Do not build a viral P2P acquisition engine.** Use the cooperative's pre-aggregated membership. *Threshold that would change this:* only if a non-cooperative, open-market consumer segment becomes strategically essential — and even then, virality is not the tool where NIP and OPay/PalmPay already exist.
2. **Make the cooperative contribution flow the "direct deposit" equivalent** and the master conversion/eligibility signal. Instrument it in the core-banking platform from day one; treat contribution regularity as the primary engagement KPI (the analogue of primary-banking-active penetration).
3. **Build lending as the profit engine, gated on and repaid from contribution/settlement flows** — the transferable Cash App Borrow mechanism minus interchange. *Benchmark:* target Borrow-like sub-3% loss discipline; if early-cohort losses exceed that, tighten eligibility to longer contribution histories before scaling.
4. **Do not rely on interchange.** Model the P&L on lending spread + remittance FX margin + cooperative dues. If a card is offered, treat it as a utility/retention feature, not a revenue centre. *Threshold:* revisit only if Nigerian issuer interchange economics change materially from the current 0.5% MSC regime.
5. **Invest in compliance, KYC and live support up front.** The ~$340m Cash App bill is the price of doing the opposite, and a cooperative's fiduciary character makes frictionless-but-non-compliant onboarding existentially riskier than it was for Block.
6. **Avoid mass-market crypto.** Offer conservative savings and possibly modest investment; reject speculative bitcoin sales to thin-file members.

## Caveats
- The 2023 gross-profit composition percentages are a THIRD-PARTY ESTIMATE (Popular Fintech, using Marqeta disclosures), not a Block disclosure.
- Q4 2022 and Q4 2023 gross-profit-per-active figures (~$59, ~$67) are DERIVED, not Block-stated; the exact Q4 2025 figure was not located (Q3 2025 was $94, +25% YoY).
- Cash App Investing: only the ~4M accounts (March 2022) figure is disclosed; current count is UNKNOWN. Block explicitly does not directly monetise stock investing.
- The bitcoin-buyer count (>10M) is a 2022 figure and has not been updated in filings since.
- The ~$6/active enforcement cost is an ANALYTICAL INFERENCE ($340m ÷ 59M).
- The precise Nigerian issuer interchange slice is UNKNOWN beyond the 0.5% MSC cap; the exact running cost of Cash App's free P2P rail is UNKNOWN (Block does not disclose it).
- Some demographic/usage figures originate from aggregator sites (Backlinko, Electro IQ, Business of Apps, SQ Magazine) of variable reliability; primary Block filings, Pew, FDIC, CFPB and NYDFS sources are preferred and used wherever a claim is load-bearing.

---

# VOLUME V — The Credit Businesses

### An Institutional-Grade Forensic Reverse-Engineering Study of Block, Inc. (NYSE: XYZ, formerly Square, Inc.)
*Playbook extraction for a vertically integrated cooperative-banking group in Nigeria*

## TL;DR
- **Block's central, transferable idea is real and testable:** it underwrites borrowers on the payment flow it already processes rather than a bureau file, and — more importantly — it collects repayment out of that same flow as a fixed percentage of daily sales deducted before the merchant is settled. Disclosed loss rates (≤4% Square Loans since 2016, <3% Cash App Borrow since 2022, ~1% BNPL since 2023) corroborate the claim, but a large part of that performance is a **selection effect**: Block only lends to parties already transacting on its rails, whose money movement it can both see and intercept.
- **The self-liquidating repayment mechanism — not the model — is the deepest transferable idea, and it is also the hardest to transplant to Nigeria.** It works in the US because card acceptance is near-universal, so a Square seller's card flow is a faithful proxy for revenue AND the repayment conduit. In Nigeria, where cash dominates retail, a merchant's electronic flow is only a fraction of true revenue, so both the underwriting signal and the collection lever are weakened. **The verdict is ADAPT, and the specific institutional feature doing the silent work in the US is near-total card penetration.**
- **Flow-based underwriting is a genuine thin-file solution a smaller lender can operate, but only where the lender controls the payment rail and reaches minimum viable scale** — enough transaction history per borrower and a large enough pool to train and calibrate a model. The reader's cooperative-society core-banking platform is a legitimate analogue *if and only if* member contribution flows run through it consistently; the cooperative's member-contribution ledger is the Nigerian equivalent of Cash App direct-deposit inflows and Square GPV.

## Key Findings
1. **Four credit products, three lenders of record.** Square Loans (business), Cash App Borrow (consumer small-dollar), Afterpay (BNPL), and the Square Credit Card. As of the FY2025 10-K, Square Loans, Cash App Borrow and Afterpay Post-Purchase are all being migrated to origination by **Square Financial Services, Inc.** (the Utah industrial bank); the Square Credit Card remains issued by **Celtic Bank Corporation** on the American Express network; Afterpay "Pay Monthly" (interest-bearing) loans are underwritten by **First Electronic Bank**.
2. **The pricing is a flat fee, not an interest rate — deliberately.** Square Loans quote a single fixed dollar fee via a factor rate historically in the range of about 1.10–1.16 (borrow $10,000, repay ~$11,000–$11,600); Cash App Borrow charges a flat 5% finance charge for roughly a four-week loan (~60–65% APR-equivalent at that fee, versus 391% for a typical two-week payday loan per the CFPB) and monetises the merchant at a 3–7% merchant discount rate on the BNPL side.
3. **The core mechanism has two halves that most analysis conflates.** (a) *Underwriting* on real-time transaction data (volume, revenue patterns, customer mix, tenure, decline rates, forecasted income, inflows, direct-deposit status) with offer-driven, pre-approved origination; and (b) *repayment* as an automatic skim off daily processing volume. The second half is the safer, more novel idea.
4. **Disclosed loss performance is strong but selection-inflated.** Block's own figures: Square Loans ≤4% (since 2016), Cash App Borrow <3% (since 2022), BNPL ~1% (since 2023). The population is pre-filtered — Square Loans historically reached only sellers covering ~80% of Square's gross payment volume — so these are not general-population loss rates.
5. **A decisive funding shift happened on 1 July 2025.** Loans held for investment jumped from **$365.1m (year-end 2024) to $3.383bn (year-end 2025)** as Block began retaining Cash App Borrow, Afterpay Post-Purchase and SFS-originated loans; the allowance for credit losses rose from **$23.1m to $382.9m**. This is the *opposite* of Klarna's originate-to-distribute move — Block is internalising the book, funded by SFS deposits.
6. **The merchant-cash-advance-to-loan conversion (March 2016) was a substantive legal restructuring, not cosmetics** — and the reader should understand precisely why Block abandoned the MCA structure that emerging-market lenders often reach for to dodge lending licences.

## Details

### V.1 — The Four Credit Products

**(1) Square Loans (formerly Square Capital) — business credit.**
- **Launch and conversion:** Launched May 2014 as a merchant cash advance (MCA). Square provided roughly $450m in MCA financing between May 2014 and March 2016, including about $400m in 2015 alone. On/around 24–30 March 2016 Square converted the product to fixed-fee **loans originated by Celtic Bank Corporation** (a Utah industrial bank). Square Capital, LLC acted as servicer, purchasing loans within one to two business days and selling most to institutional investors. From April 2021 Block discontinued the Celtic arrangement for business loans; business loans are now originated by **Square Financial Services, Inc.** (operational 1 March 2021).
- **Mechanics and pricing:** Loan offers range from **$100 to $350,000** (some sources cite $300–$250,000 depending on vintage). Pricing is a **single flat fee (factor rate)**, historically about **1.10 to 1.16** — borrow $10,000 at 1.13 and repay $11,300. There is no interest rate and no compounding; the total dollar cost is fixed and disclosed up front. Early repayment does not reduce cost.
- **Repayment:** A **fixed percentage of daily card sales** (the "holdback," commonly cited at 9–13%) is deducted automatically before settlement. There is a **minimum payment obligation of 1/18th of the initial balance every 60 days** and an **18-month maturity backstop** — any remaining balance is due in full at 18 months. Average repayment is roughly 9–10 months. Average loan ≈ **$10,000–$10,208**.
- **Scale:** Origination ~$1.6bn (2018), $2.3bn (2019), $4.06bn (2022), $4.78bn (2023), $5.7bn (2024); cumulative "more than $32 billion" since 2014 (a Q3 2024 shareholder letter separately cites "more than $22 billion in loans globally" — the figures differ by scope and date and should be treated as COMPANY CLAIM; note the apparent inconsistency).
- **Lender of record:** Now **Square Financial Services**; previously **Celtic Bank** (2016–2021); originally Square itself as MCA provider (2014–2016).

**(2) Cash App Borrow — consumer small-dollar credit.**
- **Launch/migration:** Small-dollar short-term consumer loans within Cash App, originated historically through **First Electronic Bank**; in **March 2025 the FDIC approved SFS** to originate and service Borrow, and migration in-house proceeded through 2025.
- **Mechanics and pricing:** Amounts **$20 to $500** (older tiers capped near $200); a **flat 5% finance charge** for roughly a **four-week** term, plus a **1.25% weekly late fee** if overdue. At 5% for four weeks the APR-equivalent is roughly **60–65%** — expensive versus mainstream credit but a fraction of payday-loan cost. For context, the CFPB states that "a loan outstanding for two weeks with a $15 fee per $100 has an Annual Percentage Rate (APR) of 391 percent." Average loan **<$100 (~$87)**, ~one month duration. Repayment is auto-deducted from the Cash App balance and incoming funds. No new loan is allowed while a balance is overdue.
- **Eligibility (flow-based):** Most users qualify by direct-depositing **$300+ in paychecks monthly** into Cash App, or sharing an external account with **$500+ in monthly deposits**, plus Cash App Card usage and maintained balances. Not available in Colorado, Iowa, or Oregon.
- **Scale:** ~**$9bn originated in 2024**, ~5 million actives; cumulatively "nearly $15 billion to more than 9 million active members."
- **Lender of record:** Now **SFS**; previously **First Electronic Bank**.

**(3) Afterpay — buy-now-pay-later.**
- **Acquisition:** Afterpay estate acquired 31 January 2022.
- **Pay-in-4 (classic):** Purchase split into four interest-free instalments over six weeks; 25% down at checkout, three further payments every two weeks. Consumer pays no interest/fees if on time; **late fees up to $8 per missed instalment, total capped at 25% of order value** (US). Merchant pays a **merchant discount rate of ~3–7% plus a fixed per-transaction fee**. Average BNPL loan ≈ **$79**.
- **Pay Monthly:** Longer-term instalment lending for larger purchases, **interest-bearing (APR 0–35.99%)**, underwritten and issued by **First Electronic Bank**.
- **Afterpay Post-Purchase on Cash App Card:** Launched February 2025 — lets Cash App Card users retroactively split past purchases; crossed a **$3bn origination run-rate by early October 2025**, scaling faster than Borrow's early trajectory. Afterpay "Pre-Purchase" launched February 2026; Pay-in-4 for peer-to-peer transactions also launched.
- **Lender of record:** Afterpay entities / SFS for Post-Purchase (migrated in-house mid-2025); First Electronic Bank for Pay Monthly.

**(4) The Square Credit Card and other card credit.**
- **Square Credit Card:** Beta June 2023; **issued by Celtic Bank Corporation pursuant to an American Express licence**, runs on the Amex network. Invite-only for eligible Square sellers; **credit limit scales with Square sales**; no annual or late fees; 1.5% cash back; and — echoing Square Loans — a portion of each day's sales can be assigned toward the balance ("credit that can repay itself"). This is the card-form expression of the same flow-based logic.
- Cash App Card is a **debit** card (Sutton Bank issuer historically), not a credit product, though Afterpay-on-Cash-App-Card now overlays BNPL credit onto it.

### V.2 — The Core Mechanism: Underwriting on Proprietary Payment Flow

**What Block actually sees.** For a Square seller: gross payment volume, transaction frequency, average ticket, seasonality, mix of new versus returning customers, revenue growth trajectory, most-recent-transaction recency, time on platform, product mix, chargebacks and card-decline rates, inventory movements and hiring signals. Block has explicitly cited a **non-traditional signal — whether the business name appears in the owner's email address** — as a default predictor. For a Cash App consumer: inflows, direct-deposit status, transaction patterns, balance behaviour, account tenure, on-time repayment history, and state of residence. In FY2025 Cash App actives brought **$316 billion of inflows** into the app (avg ~$1,410/active/quarter in Q4 2025) — the raw material of consumer underwriting.

**How that becomes a decision.** Block trains machine-learning models on real-time data — reportedly **17 years of historical data plus over a year of randomised test data** — to set eligibility, limits and price. Bureau data is used minimally or not at all for the flagship flows ("no credit check required" for Square Loans; "no credit check" for Cash App Borrow). Origination is **offer-driven, not application-driven**: eligible sellers/consumers are presented a pre-approved amount inside the dashboard/app. Offers are **sized relative to observed volume** — Square uses processing volume, account history and payment frequency to set both the offer and the repayment rate; historically it waited one to two months to observe a business before extending an offer, then compressed that with model improvements to underwrite seasonal, volatile and newer sellers (66% of loans under the expanded model go to sellers with <$25,000 annual GPV; 95% to sellers under $125,000).

**Why flow can beat a bureau file for this population.** A bureau file is lagging, sparse for thin-file borrowers, and silent on current cash flow. Block's argument — that real-time money movement predicts short-duration repayment better than a stale score — is plausible and supported by its loss rates. **But it must be tested against the selection effect:** Block only lends to entities already on its rails (Square Loans historically covered ~80% of Square GPV before the expansion), so the population is pre-filtered for going-concern status and observable revenue. The low loss rates are therefore *partly* a model advantage and *partly* a population advantage. The volume records this as **ANALYTICAL INFERENCE**: the model is good, but a lender lending to "all comers" on the same signals would not replicate these loss rates.

**The self-liquidating repayment mechanism (the single most transferable idea).** Square Loans repay as a **fixed percentage of daily card sales, skimmed automatically before the merchant is settled.** This is structurally different from — and far safer than — invoicing a borrower:
- The lender is *first in line* on the cash, not a creditor chasing payment after the money has reached the borrower.
- Repayment is **state-contingent on revenue**: slow week, smaller deduction; strong week, faster payoff. This aligns debt service with ability to pay and reduces the probability that any single period's obligation exceeds cash generated.
- **Backstops prevent indefinite drift:** a minimum of 1/18th of principal every 60 days, and full balance due at 18 months; if daily sales cannot cover the minimum, Square can debit the linked bank account.
This converts a credit-risk problem into a **cash-flow-interception** problem, which is why loss rates stay low even for thin-file borrowers.

**The lock-in consequence.** Because repayment flows through Square processing, a borrower who stops processing through Square breaks the repayment conduit — payments then fall to the 1/18th minimum debited from a linked bank account, and ultimately the maturity backstop. This ties credit to platform retention: Block reports sellers who took a loan use **3.7 Square products on average versus 1.5** for non-borrowers, SaaS attach rates 10 points higher, and a 15% retention improvement for sellers adopting three or more banking products. Credit is both a product and a **retention flywheel**.

### V.3 — Credit Performance and Loss Experience

**Company-claimed loss rates (COMPANY CLAIM):** BNPL ~1% (since 2023), Cash App Borrow <3% (since 2022), Square Loans ≤4% (since 2016). CFO Amrita Ahuja reiterated Borrow loss rates "below 3%" on the Q3 2025 call. An earlier Harvard case cited a ~4% Square default rate.

**Balance-sheet evidence (CONFIRMED FACT, per 10-Ks):**
- Loans held for investment: $124.0m (2022) → $247.6m (2023) → $365.1m (2024) → **$3.383bn (2025)**.
- Loans held for sale: $474.0m (2022) → $775.4m (2023) → $1,111.1m (2024) → **$783.0m (2025)**.
- Allowance for credit losses on loans held for investment: **$23.1m (2024) → $382.9m (2025)**; FY2025 roll-forward: provisions **$561.4m**, write-offs **$(216.5)m**, recoveries **$14.8m** (net charge-offs ≈ $201.6m).
- Year-end 2025 amortized cost by portfolio segment: Consumer $3,182.6m (allowance $340.1m ≈ 10.7% coverage), Commercial $481.8m (allowance $33.6m ≈ 7.0%), Other $101.4m. **Consumer coverage near 10.7% reflects the short-duration, higher-frequency Borrow book now held on balance sheet.**
- Credit quality: Pass-rated ~$3.4bn; Classified ~$381m at year-end 2025.
- Income-statement line "**Transaction, loan, and consumer receivable losses**": $660.7m (2023) → $794.2m (2024) → **$1,337.2m (2025)** — the near-doubling in 2025 reflects the shift to holding consumer loans.

**Behaviour through cycles.** Through COVID, the MCA/loan book's self-liquidating design meant repayment automatically slowed with sales rather than defaulting outright; PPP (below) absorbed much stress. Through the 2022–2023 rate cycle, Block's short-duration books (Borrow ~21 days, BNPL ~22 days) repriced/turned over fast, insulating them relative to Affirm, whose longer interest-bearing loans were hit hard when funding costs rose.

**Peer benchmarks.** Affirm 30+ day delinquency ~2.4–2.8% (2023–2026) with allowance ~6.0% of loans held for investment (Q1 2026); Klarna reported a 2024 loan-loss rate of 0.47% of GMV on its own methodology but ~5.5% measured as net charge-offs against outstanding balances — a reminder that **denominator choice drives the headline**. US bank credit-card charge-offs ran ~3.4–5.2%. The CFPB's BNPL market monitoring found the share of loans charged off across six large providers (Affirm, Block-owned Afterpay, Klarna, PayPal, Sezzle, Zip) was **2.63% in 2022, falling to 1.83% in 2023** (with earlier readings of 1.83% in 2020 and 2.39% in 2021). Block's ≤4%/<3%/~1% claims are competitive but, like Klarna's, measured against originations rather than average balances, which flatters short-duration products.

**Recoveries.** FY2025 recoveries of $14.8m against $216.5m of write-offs imply a **~7% gross recovery rate** on charged-off loans — low, consistent with unsecured small-dollar lending where the economics rely on loss *avoidance* (flow interception), not collection.

### V.4 — Funding the Book

**The evolution.**
1. **Forward-flow / originate-to-distribute (2016–mid-2025):** Square Capital/Loans sold the **majority of loans to institutional third-party investors on a forward-flow basis** within one to two business days of origination; loans not sold were reclassified held for investment. Block earned a **gain on sale** plus servicing, recycling capital rapidly with minimal balance-sheet commitment. FY2025 still shows **$4.5bn of proceeds from sale of finance receivables and $255.8m of gain on sale** — the sale channel remains large for Square Loans.
2. **Warehouse facilities:** Used for the BNPL portfolio.
3. **Corporate cash:** Bridge funding.
4. **SFS deposits (post-1 March 2021, scaling 2025):** The industrial-bank charter unlocked **deposit funding** — the pivotal structural change from fee-earner to spread-earner. SFS carries a permanent **20% leverage requirement** (roughly double a normal well-capitalised bank) and its equity reached ~$845m by Q3 2025.
5. **The 1 July 2025 shift to held-for-investment:** Block began retaining Cash App Borrow, Afterpay Post-Purchase and SFS-originated loans, driving LHI from $365m to $3.383bn.

**Economics of each mode.** When Block *sells* a loan it books an immediate gain on sale, takes no ongoing credit risk, and frees capital (high turnover, high return on *Block* capital — e.g., Return on Block Capital of 62% for Square Loans, 71% for BNPL as of Q3 2024). When it *holds* a loan it earns the full spread/fee over the loan's life but must fund it (now via deposits), reserve against it (CECL allowance), and bear the credit risk. The shift happened because **deposit funding at SFS is cheaper and stickier than warehouse/forward-flow**, letting Block capture the full economics of Borrow at scale while its short duration keeps balance-sheet intensity manageable.

**Parallel to the Klarna study.** Klarna moved *toward* originate-to-distribute (selling ~$26bn of BNPL loans to Nelnet ahead of its IPO to de-risk the balance sheet). **Block is moving in the opposite direction — internalising its book** — because it has something Klarna lacks: a US industrial-bank charter with deposit-gathering. This is the crucial institutional asymmetry.

### V.5 — The Economics of the Credit Businesses

- **Where lending sits in reporting:** From FY2025 Block re-cut disclosure into three revenue categories. Lending sits mainly in **Financial Solutions** (Cash App Borrow, Square Loans, Square Card, Savings), while **BNPL/Afterpay and Cash App Card sit in Commerce Enablement**. Reportable *segments* remain **Square and Cash App**.
- **Revenue contribution:** Financial Solutions revenue **$4.18bn in 2025, up 28%**, "primarily due to growth in Cash App Borrow volumes." Total gross profit **$10.36bn (2025)** (Cash App segment $6.34bn; Square segment $3.94bn).
- **Per-unit economics (COMPANY CLAIM, Q3 2024 shareholder letter, as of 30 Sep 2024):**

| Metric | Square Loans | Afterpay | Cash App Borrow |
|---|---|---|---|
| Return on Invested Capital | 22% | 34% | 33% |
| Return on Block Capital | 62% | 71% | 33% |
| Duration (days) | 150 | 22 | 21 |
| Annual turnover | 2.4x | 17x | 17x |
| Average loan size | $10,208 | $79 | $87 |

- **Interpretation:** **Afterpay has the best economics on a Return-on-Block-Capital basis (71%)** because it turns capital 17× a year at ~1% loss and is heavily externally funded. Square Loans generate the highest *absolute* gross profit per loan but tie up capital longer (150-day duration, 2.4× turnover). Cash App Borrow's return on *invested* capital (33%) is strong but its Return on *Block* Capital was only 33% while still externally funded — the 2025 in-housing is precisely the move to capture more of that spread.

### V.6 — Regulatory Architecture of Lending

- **State lending licences and bank-partner preemption:** By originating through **Celtic Bank** (and later SFS, both Utah industrial banks) Block relied on **federal bank-partner interest-rate exportation** to preempt state usury/interest-rate caps and avoid a 50-state patchwork of lending licences. The industrial-bank charter internalised this. This is the single most important regulatory enabler of the whole edifice.
- **TILA / Regulation Z:** Applies to consumer credit (Cash App Borrow, Afterpay Pay Monthly). The **CFPB's May 2024 interpretive rule** classified Pay-in-Four BNPL providers as "card issuers" subject to Reg Z dispute/refund and periodic-statement rules — then the CFPB **declined to prioritise enforcement (early 2025) and withdrew the rule on 12 May 2025**. So BNPL's Reg Z status is currently unsettled/de-prioritised (CONFIRMED FACT as of the research date).
- **ECOA / Regulation B (the model-underwriting exposure):** CFPB **Circulars 2022-03 and 2023-03** hold that a creditor using AI/ML "black-box" models must still give declined applicants **specific, accurate principal reasons** for adverse action; model opacity is not a defence. This is the most direct fair-lending constraint on flow-based underwriting.
- **Military Lending Act:** Caps APR at 36% (MAPR) for covered servicemembers — directly relevant to Cash App Borrow's ~65%-APR-equivalent pricing, which must be suppressed or the product withheld for covered borrowers.
- **Fair lending / disparate impact:** Because flow-based models use proxies (transaction patterns, geography, device signals), they carry **disparate-impact exposure** distinct from bureau underwriting — see V.9.
- **SBA / PPP:** Square participated as a PPP lender (below), placing it under SBA program rules.

**Does flow-based underwriting create fair-lending exposure that bureau-based underwriting does not?** **Yes (ANALYTICAL INFERENCE).** Two ways: (1) *adverse-action explainability* — a bureau score maps cleanly to codified reason codes; a 1,400-feature gradient-boosted model on transaction data does not, and the CFPB has explicitly said back-fitting a reason is non-compliant; (2) *proxy discrimination* — transaction-pattern and geographic features can correlate with protected classes, creating disparate impact even without intent. Bureau underwriting has decades of validated reason-code infrastructure; flow underwriting must build that explainability layer from scratch.

### V.7 — The Merchant Cash Advance Question

**The legal distinction.** An MCA is structured as the **purchase of a business's future receivables at a discount**, not a loan. Because it is legally a sale, not credit, it has historically fallen **outside state usury caps and lending-licence requirements** — the very reason emerging-market lenders reach for it. The trade-off: MCAs are lightly regulated, hard to compare on cost, and increasingly subject to **state commercial-financing disclosure laws** (California CFDL/SB 1235, effective 2022; New York CFDL, effective 1 August 2023 — both requiring TILA-like disclosures including an estimated APR for transactions up to $2.5m in NY / $500k thresholds elsewhere; plus registration regimes in Utah and Virginia).

**Why Block converted (March 2016).** Square publicly cited that **structuring the product as a loan would let it grow faster because institutional investors are more familiar with loans** than MCAs — critical because the funding model depended on selling the paper to forward-flow investors. Trade analysis (deBanked) added two more motives: (1) the MCA's near-absent underwriting and one-click process **raised regulatory red flags** (post-San Bernardino scrutiny of easy online credit and AML/terrorism-financing concerns), and the loan structure paired with Celtic Bank added KYC/AML rigor; (2) the **bank-charter model enabled bundling and sale of loans to institutional investors** cleanly. The conversion **cost** Block the licence-free, usury-free freedom of the MCA form; it **bought** investor acceptance, a scalable forward-flow funding market, cleaner regulatory standing, and — ultimately — the path to its own bank charter.

**Why this matters to the reader:** the MCA structure is often proposed in emerging markets precisely to avoid a lending licence. Block, at scale, found the MCA form was a **funding and regulatory dead-end** and deliberately traded it for a licensed structure. A Nigerian builder tempted by a receivables-purchase structure to avoid the MFB licence should note that it forecloses institutional funding and invites eventual reclassification as a loan (courts in NY/CA increasingly reclassify MCAs lacking genuine reconciliation provisions as usurious loans).

### V.8 — Failure and Exception Paths

- **When sales collapse:** The self-liquidating design means the daily deduction shrinks automatically; the loan simply amortises more slowly. There is no fixed instalment to miss. The **1/18th-per-60-days minimum** and **18-month maturity** are the backstops; if daily sales cannot meet the minimum, Square debits the linked bank account/Square balance for the shortfall.
- **No maturity for MCA-style, but a backstop for loans:** The current loan product does have an 18-month final maturity — the key legal feature distinguishing it from a pure MCA.
- **When a borrower leaves the platform:** The repayment conduit breaks; obligation falls to minimum debits and the maturity backstop. This is the lock-in mechanism from the borrower's side.
- **Hardship/forbearance:** Afterpay lets consumers reschedule Pay-in-4 payments up to three times a year and auto-pauses accounts on missed payment; no new loan is allowed with an overdue balance across all products (a structural circuit-breaker against debt spirals).
- **Collections/recovery:** Gross recovery on charge-offs is low (~7% in FY2025), confirming the model relies on loss *prevention* via flow interception, not back-end collection.
- **COVID as a natural stress test:** Square was an SBA PPP lender. Per Square, Inc.'s Q2 2020 shareholder letter, Square Capital "facilitated approximately $873 million in Paycheck Protection Program (PPP) loans, providing access to a financial lifeline to over 80,000 small businesses" (an earlier 10 June 2020 press release cited "more than $820 million…to more than 76,000 small businesses," and the carried-forward Volume II figure was ~$857m; the differences are timing/scope and all are COMPANY CLAIM). This is evidence the flow-based platform could rapidly deploy government-backed credit to thin-file micro-merchants that traditional banks deprioritised.

### V.9 — The Transplant Verdicts

**(A) Underwriting on proprietary payment flow — VERDICT: ADOPT (with data-scale caveat).**
The core idea transfers directly to a platform that processes cooperative transactions. The reader's core-banking platform sees member contributions, withdrawals, loan repayments and internal transfers — a richer, more continuous signal than a Nigerian credit bureau. Bureau coverage is thin: World Bank data recorded private credit bureau coverage of just **7.8% of adults (2017)**, while formal financial inclusion reached **64% in 2023** (EFInA Access to Financial Services survey) — a wide gap that makes bureau-led underwriting unavailable for most of the target population. *Silent institutional feature in the US:* Block owns the rail and sees 100% of on-platform flow. *What must be true in Nigeria:* the cooperative's flows must actually run through the reader's platform (not cash-in-hand), and there must be enough history per member and enough members to train a model.

**(B) Repayment as a fixed percentage of daily processing volume — VERDICT: ADAPT (hardest and most important).**
In the US this works because card acceptance is near-universal, so card flow ≈ true revenue AND is the repayment conduit. **In Nigeria, cash dominates retail, so a merchant's electronic volume is only a fraction of true revenue — the mechanism captures a diluted signal and a diluted collection lever.** *Silent institutional feature:* near-total card penetration. *What must change:* apply the mechanism where the platform genuinely controls the flow — **cooperative member-contribution flows and salary/allowance credits that are inherently electronic and recurring**, not merchant card sales. Repay out of the member's regular contribution deduction (a payroll-style skim at source), which is the true analogue of Square's pre-settlement deduction. For merchant lending specifically, size the loan to *electronic* volume only and treat cash revenue as invisible — never lend against unobservable cash.

**(C) Offer-driven, pre-approved origination — VERDICT: ADOPT.**
Pre-approving from observed data transfers cleanly and is operationally cheap: it requires (i) a clean, continuous transaction ledger per member, (ii) a scoring model, and (iii) an in-app/in-ledger offer surface. It also improves conversion and cuts acquisition cost. *Requirement:* the platform must store and compute on longitudinal member data — a data-engineering, not a licensing, problem.

**(D) Bank-partner-then-own-charter funding sequence — VERDICT: ADAPT.**
Block's sequence (bank partner → own industrial-bank charter) maps onto Nigeria's CBN ladder, but the Nigerian analogue of the charter is a **microfinance-bank (MFB) licence**, which is required for deposit-taking and lending. The reader should **start under an MFB licence directly** (or partner with a licensed MFB) rather than attempt an MCA/receivables dodge. *Silent institutional feature in the US:* the Utah industrial-bank charter's deposit-funding + interest-rate exportation. Nigeria has no interest-rate-exportation analogue; the MFB licence itself confers deposit-taking. Note the MFB microloan caps (Tier 2 Unit <₦500,000 per borrower; other tiers ≤₦1,000,000) and the tiered capital requirements (Tier 2 Unit ₦50m; Tier 1 Unit ₦200m; State ₦1bn; National ₦5bn) constrain product design.

**(E) Selling loans to institutional investors (forward flow) — VERDICT: REJECT (for now) / ADAPT later.**
Block's rapid capital recycling depends on a deep US forward-flow and securitisation market that **does not exist at scale in Nigeria**. *Silent institutional feature:* mature institutional loan-buying market. *What must change:* fund from **member deposits within the MFB** (the reader already plans deposit-taking) — which is, notably, exactly where Block itself moved in 2025. The reader can leapfrog straight to the deposit-funded model Block spent a decade reaching.

**(F) Consumer small-dollar lending on inflow data (the Cash App Borrow model) — VERDICT: ADOPT.**
A cooperative member's **contribution flow is a valid — arguably superior — analogue to Cash App inflows**: it is recurring, predictable, observed at source, and (critically) can be intercepted at source for repayment, exactly like direct-deposit-based Borrow eligibility. This is the reader's strongest transplant. *Silent institutional feature:* Cash App's visibility into direct-deposit inflows. The cooperative sees member contributions even more reliably because membership itself compels them.

### V.10 — Volume V Reconstruction

**(1) Four products by entity and lender of record:** Square Loans (SFS now; Celtic 2016–2021; Square MCA 2014–2016) · Cash App Borrow (SFS now; First Electronic Bank before March 2025) · Afterpay Pay-in-4 & Post-Purchase (Afterpay/SFS in-house from mid-2025) and Pay Monthly (First Electronic Bank) · Square Credit Card (Celtic Bank, Amex network).

**(2) Underwriting-signal map:** Seller — GPV, frequency, average ticket, seasonality, new/returning mix, revenue growth, recency, tenure, product mix, chargebacks, decline rates, plus non-traditional signals (business name in email). Consumer — inflows, direct-deposit status, transaction patterns, balance behaviour, tenure, on-time history, state of residence. Bureau data minimal-to-absent.

**(3) Repayment mechanism:** Fixed % of daily card sales skimmed pre-settlement (holdback ~9–13%); 1/18th minimum per 60 days; 18-month maturity backstop; linked-account debit if sales insufficient. Self-liquidating and revenue-contingent.

**(4) Credit performance across history:** LHI $124m→$247.6m→$365.1m→$3.383bn (2022–2025); allowance $23.1m→$382.9m (2024→2025); FY2025 write-offs $216.5m, recoveries $14.8m; claimed loss rates ≤4% (Square Loans), <3% (Borrow), ~1% (BNPL).

**(5) Funding evolution:** MCA self-funded → forward-flow sale to institutions (2016) → warehouse (BNPL) → SFS deposits (2021→) → held-for-investment internalisation (1 July 2025). FY2025 still $4.5bn proceeds and $255.8m gain on loan sales.

**(6) Credit economics:** Financial Solutions revenue $4.18bn (+28%, Borrow-driven); RoBC 62%/71%/33% (Loans/Afterpay/Borrow); durations 150/22/21 days.

**(7) Regulatory map:** Bank-partner interest-rate exportation → industrial-bank charter; TILA/Reg Z (BNPL interpretive rule issued May 2024, withdrawn May 2025); ECOA/Reg B adverse-action for AI models (Circulars 2022-03, 2023-03); MLA 36% MAPR; fair-lending/disparate-impact; SBA/PPP.

**(8) MCA analysis:** MCA = receivables purchase, licence/usury-free but funding- and regulatory-limited; converted to Celtic-originated loans March 2016 for investor familiarity, funding scalability, and regulatory cleanliness; state disclosure laws (CA 2022, NY 2023) now erode the MCA advantage.

**(9) Failure paths:** Auto-shrinking deductions, minimum + maturity backstops, no new loan with overdue balance, low (~7%) recovery, COVID/PPP stress test (~$873m to 80,000+ businesses).

**(10) Transplant verdict table:**

| Mechanism | Verdict | US institutional feature doing the silent work |
|---|---|---|
| Underwrite on proprietary flow | **ADOPT** | Block owns rail, sees 100% of on-platform flow |
| Repay as % of daily processing | **ADAPT** | Near-universal card acceptance (card ≈ revenue) |
| Offer-driven origination | **ADOPT** | Longitudinal on-platform data |
| Bank-partner→own-charter | **ADAPT** | Industrial-bank charter + rate exportation → use MFB licence |
| Sell loans to institutions | **REJECT/ADAPT** | Deep forward-flow market → fund from deposits |
| Consumer lending on inflows | **ADOPT** | Direct-deposit visibility → member contributions |

**(11) Key unknowns (UNKNOWN):** product-level loss rates broken out in filings (10-K reports Consumer/Commercial/Other, not by product name); exact holdback formula and factor-rate schedule; the precise feature set and weights of the ML models; SFS deposit cost of funds; recovery economics by product; how much of low loss rates is model versus selection (not separable from public data).

**(12) Ten most important conclusions:**
1. The transferable core is *two* mechanisms, not one: underwrite on flow **and** collect out of flow — the collection half is the more novel and safer.
2. The self-liquidating, pre-settlement deduction is the deepest idea and the hardest Nigerian transplant because it depends on electronic-flow penetration.
3. Low loss rates are real but selection-inflated; a lender to all comers would not replicate them.
4. Block deliberately abandoned the MCA structure — the reader should not adopt what Block discarded.
5. The industrial-bank charter (deposit funding + rate exportation) is the silent institutional enabler of the entire US model.
6. Block internalised its loan book in 2025 (opposite of Klarna), because deposit funding beats forward-flow — a model the reader can adopt from day one via an MFB licence.
7. Afterpay has the best capital economics; Square Loans the best absolute per-loan gross profit; Borrow the fastest-growing revenue.
8. Cash App Borrow (consumer inflow lending) is the reader's strongest transplant; member-contribution flow is a superior analogue to direct deposit.
9. Flow-based ML underwriting creates *specific* fair-lending/adverse-action exposure that bureau underwriting does not — build explainability early.
10. Minimum viable scale is set by data, not headcount: you need enough transaction history per borrower and a large enough pool to train and calibrate — achievable for a cooperative platform well below Block's scale, provided flows are electronic and continuous.

**The central question — is flow-based underwriting a genuine thin-file solution a small lender can operate, or does it need platform scale?**
It is genuine and operable at modest scale **conditional on three things**: (i) the lender controls the payment/ledger rail and sees the borrower's flow continuously; (ii) it can *intercept* repayment at source, not merely observe; (iii) it has enough per-borrower history and a large enough pool to calibrate a model. Block's *scale* is not the enabler — its *ownership of the rail and the flow* is. A cooperative core-banking platform satisfies (i) and (ii) structurally and can reach (iii) with a few thousand active members and 6–12 months of continuous ledger history. **Minimum viable scale is therefore a data threshold (roughly: enough members × enough months to make loss rates statistically stable and offers individually sized), not the tens-of-millions of actives Block operates.** The binding constraint in Nigeria is not scale — it is getting member money movement *onto the electronic rail* so it can be both seen and skimmed.

**What Block knows that a bureau does not:** current, real-time cash flow and the ability to intercept it — a forward-looking ability-to-repay signal and a collection lever. **What a bureau knows that Block does not:** the borrower's *off-platform* obligations and total indebtedness — Block sees its own flow but is blind to debts and income elsewhere, so it cannot see leverage or stacking outside its rail. The two are complements; the reader's platform will have Block's advantage and the bureau's blind spot.

## Recommendations
1. **Build the ledger first, lend second.** Before any credit product, ensure member contribution, repayment and transfer flows run *through* the platform electronically and are stored longitudinally. The credit product is worthless without the flow it underwrites and collects from. **Benchmark to change course:** if fewer than ~60–70% of a cooperative's member money movements are electronic and on-platform, defer merchant-style lending and start with contribution-secured consumer loans.
2. **Start with the Cash App Borrow analogue, not the Square Loans analogue.** Lend small, short-duration amounts against member *contribution inflows*, repaid by an at-source deduction from the next contribution — the safest, highest-confidence transplant. Cap first loans small and grow limits with demonstrated repayment, exactly as Borrow does.
3. **Obtain the correct licence; do not use a receivables/MCA dodge.** Secure (or partner for) a CBN microfinance-bank licence for deposit-taking and lending. Block's own history shows the MCA structure is a funding and regulatory dead-end. **Threshold:** if targeting single-state operation, a State MFB licence (₦1bn capital) fits; a Tier-1 Unit (₦200m) suits a single urban cluster pilot.
4. **Fund from member deposits, not forward-flow.** Nigeria lacks a deep loan-purchase market; leapfrog straight to the deposit-funded, held-for-investment model Block reached only in 2025. Manage the deposit-insurance/trust gap explicitly (NDIC coverage, transparent reserves).
5. **Size merchant loans to electronic volume only.** Treat cash revenue as invisible. Never lend against unobservable cash flow; underwrite and collect only against the electronic slice you can both see and skim.
6. **Build adverse-action explainability into the model from day one.** Even absent a Nigerian ECOA analogue, an explainable model (per-feature reason codes) is a prerequisite for fair, defensible, and eventually regulated lending — and avoids the "black-box" trap the CFPB penalises. **Threshold to escalate governance:** once model-declined applicants exceed a few hundred per month, formalise reason-code generation and disparate-impact testing.
7. **Use credit as a retention flywheel deliberately.** Block's data shows borrowers adopt 3.7 products versus 1.5 and retain better. Price and design credit to deepen the cooperative relationship, not as a standalone P&L line.

## Caveats
- **Loss rates are COMPANY CLAIMS measured against originations**, not average balances, and are not broken out by product in filings (the 10-K reports Consumer/Commercial/Other). They flatter short-duration products and cannot be cleanly decomposed into model-skill versus selection-effect from public data.
- **The origination-cumulative and PPP figures conflict** across sources ("more than $32 billion" since 2014 versus "$22 billion globally" in a Q3 2024 letter; PPP ~$873m/80,000 in the Q2 2020 letter versus ~$820m/76,000 in the June 2020 press release versus ~$857m carried forward from Volume II). All are COMPANY CLAIMS with differing scope/date; treat directionally.
- **The BNPL regulatory position is unsettled:** the CFPB's May 2024 interpretive rule was withdrawn in May 2025; future administrations could reverse course.
- **Model internals are UNKNOWN:** feature sets, weights, holdback formulas, and cost of funds are not public.
- **The Nigerian transplant rests on an untested assumption** — that cooperative member flows are and will remain electronic and on-platform. If cash leaks dominate, the entire mechanism degrades. This is the single largest risk to the playbook and must be validated empirically before scaling.
- Figures are drawn from Block filings and shareholder letters current to the FY2025 10-K (filed February 2026); segment/category definitions changed in FY2025 and prior-period comparisons must state their basis.

---

# VOLUME VI — Operations, Technology & Data

### *A forensic reverse-engineering study — Volume VI of XIV. Basis: US GAAP, US dollars, 31 December year end, Form 10-K, unless stated. Evidence classes: CONFIRMED FACT / COMPANY CLAIM / THIRD-PARTY ESTIMATE / ANALYTICAL INFERENCE / HYPOTHESIS / UNKNOWN.*

## TL;DR
- **Square and Cash App run on roughly one-and-a-half machines — not one, and not two.** Block genuinely shares a backend engineering spine, a data platform (Databricks Data Intelligence Platform, 12PB rising to a projected 16PB, ~70 teams under Unity Catalog governance), a risk/fraud infrastructure and one ML/underwriting engine — but the two businesses keep **separate consumer-facing identity systems**: a Square seller login and a Cash App login are distinct accounts, and Block does not publicly demonstrate a person-level customer graph that acts on the knowledge that a Cash App consumer is also a Square seller. Cash App Pay is a QR/deep-link payment bridge, not an identity merger. The lesson for a founder is that platform *unification is hard* — build one shared identity and data spine from day one rather than retrofitting it.
- **The February 2026 "AI cut 40% of staff" claim is substantially overstated and should be treated as narrative, not fact.** The reduction from 10,205 to under 6,000 is the last and largest step of a multi-year over-hiring correction (12,000 cap in Nov 2023; ~1,000 in Jan 2024; TIDAL/TBD cuts late 2024; 931 roles in Mar 2025). Mizuho's Dan Dolev told the *Wall Street Journal* "the vast majority of these cuts were probably not due to AI," and NBER Working Paper No. 34836 (Feb 2026) found ~90% of surveyed executives reported no AI employment impact. Verdict: **AI-assisted, over-hiring-caused.** Analysts should discount Block's operational self-attributions and demand audited production metrics.
- **The enforcement record is the best available technical description of Block's systems — and it shows the shared risk estate failing at Cash App.** ~$340m in 2025–26 penalties, a suspicious-activity-report backlog that grew from ~18,000 to over 169,000 alerts, and a permanent 24-hour live-support obligation are all consequences of scaling a "frictionless" consumer product ahead of controls. Cutting ~40% of staff while under an independent monitor (NYDFS) and independent consultant (multistate) — with a $240m DOJ reserve outstanding — is a real, live control risk.

## Key Findings

**1. The operating model is a federation on a shared platform.** Block is organised as semi-autonomous business units (Square, Cash App, Afterpay, Bitkey/Proto, TIDAL) sitting on shared engineering, data and risk platforms. Since the September 2024 reorganisation it runs functional leads across the whole group: Brian Grassadonia (Ecosystem Lead, "connecting the dots across Square, Cash App, and Proto and our emerging initiatives"), Owen Jennings (Business Lead — product, operations, customer support), Nick Molnar (Sales & Marketing Lead), Thomas Templeton (Hardware), and a Risk Lead who owns risk management, consumer protection, compliance and applied ML and reports directly to the CEO. This replaced the prior model in which Alyssa Henry ran Square and Grassadonia ran Cash App as near-independent CEOs. **CONFIRMED FACT** (Block investor-relations leadership page; Payments Dive; DEF 14A).

**2. What is genuinely SHARED:** cloud (AWS); the data platform (Databricks Data Intelligence Platform — per Databricks' case study quoting Block's Kesting, "Block manages 12PB of data ... and anticipates reaching 16PB by year-end. Approximately 70 different teams across business units, such as TIDAL, Cash App, Square and TBD, and 500 active power users actively utilize the platform," governed centrally by Unity Catalog); the ML/underwriting platform (one engine underwrites Cash App Borrow, Afterpay and Square Loans — Volume V's deepest mechanism); the risk/fraud infrastructure (Cash App Pay uses "the same fraud detection infrastructure ... that monitor[s] millions of daily Square Point of Sale transactions"); internal engineering/AI tooling (goose, Builderbot); and open-source libraries. Risk is a single group-level organisation. **COMPANY CLAIM corroborated by vendor case study and developer docs.**

**3. What is genuinely SEPARATE:** the two consumer-facing identity/account systems. Per Square's own product team (Square Community Q&A, Oct 2023), "**There is no need to connect your Cash App account to Square**" to accept Cash App Pay, and Square Point of Sale and Cash App "operate as completely separate apps." Language stacks diverge by unit (Java/Kotlin at Square; Kotlin/Go at Cash App; Rust/C++ at Bitkey). The partner-bank boundary is deliberately separate — Square Financial Services has its own board (Volume I). **CONFIRMED FACT.**

**4. The customer graph is UNKNOWN at the person level.** Executives describe "combining the two ecosystems" as an ambition they are progressing toward, not an accomplished fact (Dorsey, Q3 2023 shareholder letter: "We finally have line of sight to seeing more of Square within Cash App, and vice versa"). The Databricks case study notes Block uses "identity resolution to gain a comprehensive understanding of customer activities across their diverse services" — but this describes governed data-estate resolution, not a demonstrated, actioned person-level link between a specific Cash App consumer and a specific Square seller. The October 2025 "Neighborhoods" product links sellers and consumers at the network/commerce layer, and Block analyses combined Square + Cash App data at ZIP-code level (2026 Local Economy Report), but there is no public evidence of entity resolution that says "Cash App user A = Square seller B" and acts on it. **UNKNOWN / no public person-level evidence.**

**5. The AI headcount trajectory (full reconstruction).** Peak ~13,000 (Q3 2023) → 12,000 "absolute cap" (Nov 2023, on Dorsey's admission that "the growth of our company has far outpaced the growth of our business and revenue") → ~1,000 cut (~10%, Jan 2024) → TIDAL (~40 people in December) and TBD cuts (late 2024) → 931 roles plus ~200 managers removed (Mar 2025 reorganisation) → **10,205 full-time employees at 31 Dec 2025** (2,472 outside the US) per the FY2025 Form 10-K → **Workforce Plan of >40% (>4,000) announced 26 Feb 2026**, taking headcount to just under 6,000, "substantially complete by the end of the second quarter of fiscal 2026," with **$450–500m of charges** (Q1 2026 reporting later put total restructuring charges at ~$852m). In total more than 7,000 positions were eliminated from peak while gross profit nearly doubled from $7.5bn (2023) to ~$10.4bn (2025). **CONFIRMED FACT** (Form 10-K; Form 8-K; CoinDesk; Fortune; Payments Dive).

**6. What Block's AI actually does.** goose is an open-source, Model-Context-Protocol-first agent framework, released under Apache License 2.0 in January 2025 by Block's Open Source Program Office (built with Anthropic; CTO Dhanji Prasanna framed it as "a framework for new heights of invention and growth") and contributed to the Linux Foundation's Agentic AI Foundation in December 2025; it had over 50,000 GitHub stars and 500+ contributors by Q3 2026. Block claims ~60% of the workforce used goose weekly during rollout (scaled to ~12,000 staff in roughly eight weeks) and eventually 100% AI-tool adoption; production code changes per engineer up more than 2.5x from January to April 2026; non-engineer production code changes up ~60% (April vs January); incident rates after a production code change down over 70% year-over-year in Q1 2026; and Managerbot (Square, ~1m businesses by April 2026) and Money Bot/Moneybot (Cash App, ~1m active users in a single week) each surpassing one million users. **These are COMPANY CLAIMS (shareholder letter, earnings calls) — unaudited.**

## Details

### VI.1 The Operating Model
Block's functions map and attribute as follows. **Engineering/platform:** AWS cloud; microservices architecture (Cash App's "Remodeling Cash App Payments" post documents its Vitess/MySQL scaling and a "Twinlock" mechanism keeping paired double-entry "movements" consistent). **Product:** federated per business unit, coordinated by the Ecosystem and Business Leads. **Risk/fraud/financial crime:** a single group Risk organisation under the Risk Lead reporting to the CEO, with a Head of Risk Analytics & Data Science overseeing "all risk analytics and data science work across Block (including Cash App, Afterpay, and Square)" (Block job spec). **Customer support:** now a group function under the Business Lead, restructured by the CFPB order. **Hardware:** Thomas Templeton leads hardware group-wide (Square devices, Proto, Bitkey). **Data/analytics:** the Databricks platform, ~70 teams, Unity Catalog governance. **Compliance operations:** rebuilt post-enforcement (VI.3). **Corporate:** Amrita Ahuja as COO and CFO. Cost drivers are engineering compensation (historically stock-heavy), transaction/loan/risk losses, and — now permanently — mandated 24-hour support. The dominant failure mode, demonstrated repeatedly, is growth outrunning controls.

### VI.2 The Shared-Stack Question (Re-cut 1)
- **Cloud/infrastructure:** AWS; microservices. COMPANY CLAIM corroborated by engineering blog and job specs.
- **Data platform:** Databricks Data Intelligence Platform, 12PB (projected 16PB), ~70 teams across Square, Cash App, TIDAL, TBD; Unity Catalog for centralized PII governance and "a unified view of their data estate across different business units." **CONFIRMED via Databricks case study (vendor-hosted, quoting Block staff).** This is the strongest evidence of a joined *data* layer — but it is a governed data estate, not a confirmed, actioned person-level customer graph.
- **Identity/customer graph:** SEPARATE at the consumer level (CONFIRMED). Person-level joining across ecosystems: UNKNOWN / no public evidence.
- **Risk/fraud engines:** SHARED (COMPANY CLAIM) — Cash App Pay explicitly reuses Square's fraud infrastructure.
- **ML platform:** SHARED — one underwriting engine across Cash App Borrow, Afterpay, Square Loans.
- **Payment/ledger:** Cash App runs its own P2P double-entry "movements" ledger; Square runs seller settlement. Cash App Pay bridges them via QR/deep-link plus a "grant" token ("linking a Customer to a Merchant"), settling into the seller's Square account as a distinct "Cash App" tender type, treated identically to a card-present transaction. This is a **commercial/payment bridge on top of two stacks**, not deep identity integration. **CONFIRMED via Square/Cash App developer docs and Square product team.**
- **Support tooling:** converging under the Business Lead post-CFPB.

**History:** the separation was **both architectural and organisational.** Grassadonia and Henry ran the two as siloed businesses — Henry's own account: "previously with Square and Cash, I'd say pretty like, actually very, siloed, different businesses with no connections or communication between the two. We were just operating independently." What has been unified since ~2022–2025: the data platform, the risk organisation, the ML/underwriting engine, internal AI tooling, and functional leadership. What has NOT been unified: consumer identity/accounts. Afterpay was explicitly positioned to "build this bridge" between the two — an admission that no native bridge existed.

### VI.3 The Risk, Fraud and Financial-Crime Estate — Enforcement Post-Mortem
The systems: pre-transaction risk scoring (seller and consumer, on the shared risk platform); fraud/account-takeover detection; dispute/chargeback handling; identity verification/CDD; transaction monitoring and SAR filing; sanctions/OFAC screening.

**What failed, when, in which system:**
- **Transaction monitoring / SAR backlog (2018–2021):** the alert backlog grew from ~18,000 (2018) to over 169,000 (2020); some SARs were filed over a year after the triggering alert (Feb 2021–Sep 2022 review). Cause per the NYDFS consent order (10 April 2025, $40m): "Block's inability to predict the impact of Cash App's growing customer base on alert volumes and staffing needs." The order details a single SAR "filed for $1.6 million with 91 subjects that were holders of 16,811 accounts with 19,518 transactions," and a Russian criminal network in which ~25–30 subjects opened 8,359 Cash App accounts using falsified information.
- **Sanctions/crypto screening:** Bitcoin transactions to wallets with under 1% exposure to terrorist-linked wallets did not trigger alerts, and transfers were blocked only once exposure surpassed 10% (NYDFS).
- **KYC/CDD and "frictionless onboarding":** minimal identifiers (phone/email + ZIP, no SSN or bank account) enabled fraud rings; the shareholder suit O'Neill v. Dorsey (Oct 2025) alleges this design inflated user metrics while compliance lagged.
- **Customer service/fraud/disputes (2016–2023):** no live support from 2016 until February 2021 — a number on the cash card triggered only a prerecorded message; scammers posted fake support numbers that drained accounts; Regulation E error-resolution failures. CFPB consent order (16 Jan 2025): up to $175m ($55m civil penalty + up to $120m redress; checks began mailing 8 June 2026).
- **Multistate (48 states, 15 Jan 2025):** $80m; Block agreed to hire an independent consultant to review its BSA/AML program, report within nine months, and correct deficiencies within 12 months of the report (led by AR, CA, FL, ME, MA, TX, WA).

**Total ~$340m across CFPB ($175m), multistate ($80m) and NYDFS ($40m) plus related.** An **independent monitor** (NYDFS) and an **independent consultant** (multistate) are now imposed. A **$240m reserve** for a DOJ inquiry into Cash App compliance and governance was disclosed with Q1 2026 results.

**Who owns risk / can it stop a launch?** The Risk Lead reports directly to the CEO; the September 2024 creation of a chief-risk-officer-type role (responsible for "trust and safety," reporting to Dorsey, requiring "deep regulatory and partnership experience") signals elevation. Whether risk can veto a product launch is **UNKNOWN**, but the "frictionless onboarding" history is strong ANALYTICAL INFERENCE that growth historically outran control.

### VI.4 Customer Support Operations
**Before:** from 2016 until February 2021 Block offered **no live phone support** for Cash App. **After the CFPB order:** Block must run **24-hour customer service — live telephone support at least 12 hours a day and live chat at least 18 hours a day** — and build internal committees covering customer support, fraud prevention and Regulation E compliance, submitting a full compliance plan to the CFPB. This is a **permanent operating-cost obligation** that converts a near-zero-cost-of-acquisition consumer product into one carrying a mandatory always-on support floor. The precise incremental cost is not separately disclosed (**UNKNOWN**), but against 50–58 million Cash App monthly actives it is structurally material and permanent — a direct, quantifiable-in-principle consequence of the original design choice to launch without support.

### VI.5 Hardware Design, Supply Chain and Manufacturing
- **Square hardware:** Reader (from $0 magstripe / $49 chip-contactless), Terminal ($299), Stand ($149), Register ($799), Handheld ($399, introduced 2025). A deliberate loss leader (~$93m loss in FY2024, Volume III) functioning as a seller-acquisition channel. Register is "built entirely by Square."
- **Bitkey:** self-custody multi-signature Bitcoin hardware wallet; began global shipping ~March 2024; Rust/C++.
- **Proto:** bitcoin-mining hardware; developed a **3nm mining ASIC** (following a 5nm prototype), with a full tapeout; first customer **Core Scientific** (~15 EH/s, July 2024), the modular platform co-designed with **ePIC Blockchain Technologies**.
- **Supply chain:** contract-manufactured with FX and tariff exposure on imported components and inventory risk on unsold devices and ASICs. **Strategic coherence with the rest of the group is weak** (ANALYTICAL INFERENCE): Proto and Bitkey serve Dorsey's bitcoin conviction more than the Square/Cash App flywheel, and are a subsidised appendage rather than a margin engine.

### VI.6 The Data Estate
Seller transaction/inventory data (Square), consumer transaction/inflow/behavioural data (Cash App), buyer profiles, and the credit-underwriting feature stores (Volume V) all sit on the shared Databricks platform under Unity Catalog with GDPR/CCPA-oriented governance and PII controls. The estate is **joined at the data-governance and analytics layer** — a "unified view of their data estate" with cross-service "identity resolution" for analytics — and Block acts on combined data at aggregate/ZIP level (Neighborhoods; the 2026 Local Economy Report showing regular customers "shared across 32% of businesses in the same ZIP code"). It is **not demonstrably joined at the person level for operational action.** This is the single most important operational finding for the compounding thesis, and the honest answer is **UNKNOWN / likely not yet fused at the identity level.**

### VI.7 Engineering Culture and Open Source
Square/Block originated widely used libraries — **OkHttp, Okio, Retrofit, Moshi, Wire, SQLDelight, Dagger, Picasso, LeakCanary, Flow, KotlinPoet** — several of which were transferred to the Commonhaus Foundation in 2024. Recent AI tooling: **goose** (agent framework), plus internal **Builderbot, Managerbot and Money Bot**. Engineering is heavily concentrated (a large majority of the pre-cut workforce held technical roles per the human-capital disclosure) and distributed across Oakland (HQ), San Francisco, Atlanta, Melbourne (Cash App's second-largest engineering team) and Dublin. Open-source prominence is genuine evidence of capability — but it must be read against the enforcement record, which shows the *same organisation's* risk systems failing under growth. **Capability in developer tooling did not translate into control maturity** (ANALYTICAL INFERENCE) — precisely the framing-note warning against taking engineering-blog material at face value.

### VI.8 The AI Headcount Claim (Re-cut 2)
**The claim:** Dorsey attributed the >40% cut to AI ("A significantly smaller team, using the tools we're building, can do more and do it better"; "we're not making this decision because we're in trouble").

**The contest:** Mizuho Americas' Dan Dolev told the *Wall Street Journal* (Angel Au-Yeung, "Jack Dorsey's Latest Far-Out Bet: An AI Future With Fewer Employees") that "the vast majority of these cuts were probably not due to AI," citing a "significant amount of bloating." Former Block employee Jason Karsh (on X): "This isn't an AI story. It's organizational bloat wearing an AI costume." **NBER Working Paper No. 34836 (February 2026)** — a survey of ~6,000 C-suite executives across the US, UK, Germany and Australia — found ~90% reported no AI impact on employment and 89% no productivity change, with executives using AI on average about 1.5 hours per week; a corroborating Oxford Economics study reached a similar conclusion. Former Square communications head Aaron Zamost, writing in the *New York Times*: "nobody knows the answer — not even Block itself."

**Decomposition.** The February 2026 cut is the culmination of a multi-year correction that began with the November 2023 12,000 cap. Departments cut in February 2026 included policy and DEI roles — not obviously AI-automatable. The Afterpay integration (effective ~$13.9bn, generating large writedowns) was described by former staff as a "disaster" of "clumsy integration," and TIDAL/TBD were wound down. The genuine AI signal exists (goose adoption; code-velocity metrics), but the *causal* attribution of 4,000 jobs to AI is unproven. The honest split is **prior over-hiring correction + business-line wind-downs (TIDAL/TBD) + Afterpay integration failure + hiring discipline, with AI as an accelerant and a narrative wrapper.**

**Verdict (Klarna methodology applied):** the AI attribution is **substantially overstated.** AI is real and adopted, but it is being used to re-badge a delayed over-hiring correction as a strategic AI transformation because markets reward the latter — shares "soared more than 20% in premarket," rising from $54.53 toward nearly $69 after hours (AP/PBS; one report put extended-trading gains near 30%), on a quarter where Q4 gross profit rose 24% year-over-year.

**What an analyst should do in future:** treat Block's operational self-attributions — especially causal AI claims — as marketing until corroborated by disclosed, audited production metrics; weight the enforcement record and independent analyst commentary above the shareholder letter; and track control metrics (incident rates, SAR timeliness, transaction losses) as the real test of whether a 40%-smaller organisation can operate safely. Note that Mizuho maintained an underweight rating after the announcement, observing that **transaction losses had risen to 18% of gross profit from 11% a year earlier** — a control-quality warning that sits uneasily beside the productivity story.

### VI.9 Operational Resilience
- **Cloud/platform outage at peak retail:** single-cloud (AWS) concentration; microservices limit blast radius; likely recovery in hours; impact = lost GPV and seller trust. Residual risk moderate.
- **Major fraud/ATO event:** the enforcement record marks this as Block's demonstrated weak point; residual risk elevated and now under monitor scrutiny.
- **Loss of issuer-processor (Marqeta) or a partner bank:** high switching cost; Volume VII established Block *rents* these; residual risk material.
- **Hardware supply disruption:** FX/tariff exposure and Proto ASIC inventory risk, but contained to the (loss-making) hardware line.
- **Enforcement escalation:** the $240m DOJ reserve plus existing monitor/consultant obligations mean escalation is live.
- **40% staff removal under monitor obligations:** the standout risk. Cutting nearly half of staff — including policy/compliance-adjacent functions — while an independent monitor and consultant validate remediation is a control risk deserving explicit weight; transaction/loan/risk-loss expense grew 89% year-over-year in Q3 2025 as lending scaled, and rose to 18% of gross profit by early 2026.

### VI.10 Transplant Verdicts (Nigeria)

| Mechanism | Verdict | Reasoning / silent US institutional feature / what must change |
|---|---|---|
| **One shared platform vs. two stacks** | **ADOPT (build one)** | Block spent a decade and vast capital and still has not fully unified identity; retrofitting is the hard part. A single founder should build one shared identity + data + ledger spine from day one for all cooperatives and products. The US "silent worker" is abundant capital that let Block tolerate duplication; the reader cannot. *This is the most directly actionable finding in the volume.* |
| **Unified customer/transaction data estate** | **ADOPT, day one** | Block's estate is joined at governance but not demonstrably at identity; the reader should design person-level entity resolution from the start — what Block had to retrofit. Must comply with the **Nigeria Data Protection Act 2023**: lawful basis and consent for processing, data-subject rights, and data-controller/processor obligations (registration of controllers/processors of major importance, DPO, breach handling). Localise storage given data-residency expectations and naira cost. |
| **Real-time risk/fraud scoring** | **ADAPT** | Buildable by a small team using rules + lightweight ML on proprietary flow (Volume V), but NOT Block's scale ML platform. The US silent feature is deep talent and data volume. Adapt: start with deterministic rules plus settlement-deducted repayment; add ML later; ensure it works offline/over USSD and degrades gracefully. |
| **Owning hardware** | **REJECT as loss leader / ADAPT** | Block loses money on hardware deliberately, subsidised by software margin and capital. The reader cannot subsidise hardware and faces FX-exposed imports. Reject proprietary devices; adapt to BYOD/phone plus USSD and agent-based acceptance. |
| **Sequencing compliance ahead of scale** | **ADOPT (invert Block's playbook)** | Volume II's non-negotiable inversion. Operationally: stand up transaction monitoring and KYC BEFORE onboarding at scale; cap onboarding velocity to alert-processing capacity (Block's 169,000-alert backlog is the anti-pattern); no "frictionless onboarding" without identity verification. The US silent feature is Block's ability to absorb ~$340m in penalties — the reader cannot. |
| **AI as operating leverage for a small team** | **ADAPT (honestly)** | A founder can genuinely automate coding (a goose-style, self-hostable agent), support triage and reconciliation. A founder CANNOT safely automate regulated judgment (SAR decisions, dispute adjudication) given hallucination and oversight needs. Adapt: AI for engineering velocity and drafting; humans on all regulated decisions. |

### VI.11 Volume VI Reconstruction
1. **Operating-model map:** a federation of business units on shared engineering/data/risk platforms, run since 2024 by group functional leads (Ecosystem, Business, Sales & Marketing, Hardware, Risk) plus COO/CFO Ahuja.
2. **Shared vs separate verdict:** shared cloud, data platform, ML/underwriting, risk/fraud engines, internal tooling and open source; separate consumer identity and partner-bank boundary. **~1.5 machines.**
3. **Risk/financial-crime estate + post-mortem:** shared risk platform; catastrophic Cash App AML/monitoring/support failures 2016–2023; ~$340m penalties; independent monitor + consultant; $240m DOJ reserve.
4. **Support model + mandated cost:** from no live support to a permanent 24-hour live-support floor (≥12h phone / ≥18h chat) — a direct, permanent cost consequence of a design choice.
5. **Hardware/supply chain:** Square (deliberate loss), Bitkey, Proto 3nm ASIC (Core Scientific / ePIC); FX/tariff/inventory risk; weak strategic coherence.
6. **Data estate joined?** at the governance/analytics layer, yes; at the person-level identity layer, UNKNOWN / likely not.
7. **Engineering culture/open source:** genuinely strong (OkHttp/Retrofit/Okio/SQLDelight/goose) but not matched by control maturity.
8. **AI headcount verdict:** substantially overstated; an AI-assisted over-hiring correction.
9. **Resilience:** greatest risk is the 40% cut executed under active monitor obligations.
10. **Transplant table:** build one platform, sequence compliance first, reject loss-leader hardware, use AI only for non-regulated work.
11. **Key unknowns:** the person-level customer graph; the precise 24-hour-support cost; whether risk can veto launches; how much of the cut is truly AI-driven; the DOJ outcome.
12. **Ten most important conclusions:** (i) it is ~1.5 machines; (ii) the hardest capability to replicate is the shared ML/underwriting engine on proprietary payment flow; (iii) operating leverage comes from software/integrated-payments margin and the shared platform, not yet from AI; (iv) the enforcement record reveals growth outran controls; (v) identity is the unclosed gap; (vi) hardware is a subsidised appendage; (vii) open-source prowess ≠ control maturity; (viii) the AI narrative is investor-facing; (ix) the 40% cut is a live control risk; (x) for the reader, unify early and sequence compliance first.

**Central question — one machine or two?** Roughly **one-and-a-half.** The infrastructure spine (cloud, data platform, ML/underwriting, risk/fraud engines, internal tooling) is genuinely shared; the customer-facing identities and the two apps remain separate, and a person-level joined customer graph that is acted upon is not demonstrated in the public record. That Block — with a decade of effort and enormous capital — still has not fully fused the two is the single most important lesson for the reader: **platform unification is extremely hard, so build one shared platform with one identity and one data spine from the start rather than accreting several stacks and trying to join them later.**

## Recommendations
1. **Build one platform, one identity, one ledger from day one.** Treat every cooperative and every product (core banking, remittance, credit) as tenants on a single shared core with a single person-level identity graph. Block's failure to fuse identity after a decade is the warning. *Benchmark to change this:* only ever add tenancy/configuration features — never fork into a second stack, no matter how different a new product feels.
2. **Sequence compliance ahead of scale — operationally, not aspirationally.** Stand up transaction monitoring and KYC before onboarding at volume; cap onboarding velocity to your alert-processing capacity; never ship "frictionless onboarding" without identity verification. *Threshold:* if the SAR/alert queue ages beyond a few days, halt onboarding until it clears — the inverse of Block's 169,000-alert backlog.
3. **Reject loss-leader hardware.** Use phones, USSD and agent networks; do not import FX-exposed proprietary devices you cannot subsidise. Revisit only if a hardware line can be sold at positive gross margin.
4. **Use AI for engineering velocity and back-office drafting, not regulated judgment.** Adopt an agentic coding tool (goose is Apache-2.0 and self-hostable); keep humans on SAR, dispute and lending decisions. *Threshold:* automate a regulated decision only once you can evidence audited accuracy above your human baseline and retain a human override.
5. **Design for graceful degradation:** offline/USSD flows, local data residency under the NDPA 2023, and naira-cost-aware cloud choices; assume power and connectivity will fail and make the core work when they do.
6. **Staged next steps:** (a) build the shared identity + ledger core and a rules-based monitoring layer before onboarding the anchor cooperative; (b) add lightweight risk ML and settlement-deducted credit once transaction flow exists (Volume V); (c) layer remittance and multi-cooperative tenancy only after compliance operations are demonstrably keeping pace. *Escalation trigger:* if Nigerian enforcement capacity tightens (as Volume II anticipates), pull compliance hiring forward, not back.

## Caveats
- Engineering-blog, careers-page and vendor case-study material (Databricks, Square Developer, block.xyz) is COMPANY CLAIM / marketing and is treated as such; the CFPB, NYDFS and multistate enforcement documents are the most reliable technical descriptions of Block's internal systems and are mined as engineering evidence.
- The person-level customer graph, the precise incremental cost of 24-hour support, whether risk can veto launches, and the true AI share of the 40% cut are **UNKNOWN** on the public record.
- Post-cut resilience is genuinely uncertain: the AI productivity metrics (2.5x code changes, 100% adoption, incident-rate improvements) are Block's own and unaudited; the DOJ inquiry ($240m reserve) is unresolved; the O'Neill v. Dorsey shareholder suit is pending.
- Reported market reaction varies by source (~16% to ~30%); premarket ~20% and after-hours toward ~$69 from $54.53 are the best-sourced figures.
- Segment/gross-profit figures follow the stated basis (US GAAP, FY end 31 Dec). FY2025 disclosure was re-cut into **Commerce Enablement / Financial Solutions / Bitcoin Ecosystem** while retaining **Square and Cash App** as reportable segments; anchor gross profit $7.505bn (2023), $8.889bn (2024), ~$10.36bn (2025), with Square ~$3.94bn and Cash App ~$6.34bn in 2025.

---

# VOLUME VII — The Money Movement Machine

## A Forensic Reverse-Engineering of Block, Inc. (NYSE: XYZ, formerly Square, Inc.)
### Where a Dollar Goes Between Payment and Usability — and Who Takes a Cut

---

## TL;DR

- **Block is far more toll booth than technology company at the level of raw economics: the single largest source of its $10.36bn full-year 2025 gross profit (up 17% YoY, reported 26 February 2026) is not a proprietary technology but the capture of spreads on American payment rails — merchant-acquiring markup (Square, $3.94bn) and Cash App financial-services monetisation ($6.34bn), of which selling settlement speed (Instant Deposit/Instant Transfer) and earning debit interchange are the two fattest, most defensible strands.** The genuine technology and network assets (the seller operating system, the P2P graph, the self-liquidating loan mechanism) are real but sit on top of, and depend on, rails Block does not own.
- **The most important transplant finding: interchange is the hidden subsidy funding American consumer fintech, and it does not exist in Nigeria.** US small-issuer ("Durbin-exempt") dual-message debit interchange averaged $0.62 per transaction (1.41% of value) in 2023 and is uncapped; Nigeria's regulated merchant service charge is 0.5% capped at ₦10,000, and the issuer's slice of that is a fraction of a percent. A Nigerian founder cannot fund "free" consumer products out of interchange the way Cash App does — something else (lending spread, float, subscription, FX/remittance margin) must pay.
- **Selling settlement speed — Block's most elegant product — largely does NOT transplant to Nigeria.** Block charges 0.5%–1.75% (Cash App) / 1.75% (Square) to give customers instant access to money they already own, a product that exists only because standard US settlement is slow (ACH, 1–3 days). Nigeria's NIBSS Instant Payment (NIP) already makes interbank transfers real-time at a regulated flat fee. **There is almost no "time left to sell." This is the clearest case where Nigeria leapfrogged and the American playbook fails.**

---

## Key Findings

1. **Headline Square pricing is not margin.** Square's current (post-October-2025) US card-present rate is 2.6% + 15¢ on the Free plan (2.5% + 15¢ on Plus, 2.4% + 15¢ on Premium); online 3.3% + 30¢ (Free) / 2.9% + 30¢ (paid); keyed 3.5% + 15¢; ACH 1%. Of a ~2.6% merchant discount rate, roughly 70–80% is interchange paid to the issuer and ~0.13–0.15% is network assessment; Block's transaction-based **gross profit as a percentage of GPV was ~1.15% in 2024** — i.e., Block keeps roughly half the headline rate as revenue and about 1.1–1.2 points as gross profit. **[CONFIRMED FACT / THIRD-PARTY ESTIMATE]**

2. **Block is on both sides of interchange.** As acquirer (Square) it *pays* interchange to issuers; as issuer (Cash App Card, Square debit/credit) it *earns* interchange. The Cash App Card is a Visa debit/prepaid card issued by **Sutton Bank** (and, more recently, **The Bancorp Bank, N.A.**); the Square debit card is issued by Sutton Bank under Mastercard; the Square Credit Card is issued by Celtic Bank under an American Express licence. Because these issuers are all below $10bn in assets, they are **Durbin-exempt** and earn uncapped interchange (~0.9%+ on debit), versus the capped ~$0.23 that binds large banks. **[CONFIRMED FACT]**

3. **Selling time is a top-two Cash App gross-profit engine.** In 2023, Instant Deposit fees were ~29% of Cash App gross profit (35% excluding BNPL) — larger than any single strand except the "Financial Services" bundle. Standard cash-out is free (1–3 business days via ACH); Instant is 0.5%–1.75% (min $0.25) routed over card rails (push-to-card / Visa Direct). The rail costs Block a small network fee; the customer pays for immediacy on money they already own. **[THIRD-PARTY ESTIMATE / ANALYTICAL INFERENCE]**

4. **Float is real but modest and mostly passed to product, not P&L.** Block held **$4.18bn of customer funds (assets underlying customer funds) at year-end 2024** (up from $3.17bn in 2023) and **$5.84bn of customers payable** (2023: $6.80bn). It is restricted from operational use of these funds but may invest a portion in short-term securities; interest earned on customer funds is booked within subscription-and-services revenue and is not separately quantified. Square savings/checking deposits sit partly at **Square Financial Services** (the Utah industrial bank) and partly at Sutton Bank, with FDIC pass-through insurance up to $250,000. **[CONFIRMED FACT]**

5. **Bitcoin is revenue theatre, not a gross-profit engine — and functions today primarily as a traded asset, not a rail.** Bitcoin revenue accounted for 42.3% of Block's total 2024 sales but bitcoin gross profit was only ~6% of Cash App gross profit; the margin is ~3% of bitcoin revenue (e.g., $67m gross profit on $2.61bn revenue in Q2 2024). Lightning Network send/receive exists (capped at $999/7 days, unavailable in New York) but is a small usability feature; management's stablecoin/Lightning-payments ambitions for 2026 are **COMPANY CLAIM**. **[CONFIRMED FACT / COMPANY CLAIM]**

6. **The peer-to-peer rail is free at point of use and paid for by everything downstream.** Cash App P2P is a book transfer within Block when both sides are on Cash App; funding by credit card costs the sender 3%, business-account receipts cost 2.75%, and direct deposit uses real bank rails via **Lincoln Savings Bank (routing 073923033)** or **Sutton Bank (routing 041215663)**. The free P2P rail seeds the network; monetisation comes from Cash Card interchange, Instant Deposit, Borrow, and Cash App Pay. **[CONFIRMED FACT]**

7. **Network and partner dependency is deep and asymmetric.** Block depends on Visa and Mastercard (both as acquirer and issuer), on American Express (Square Credit Card), on its sponsoring acquirer (historically JPMorgan Chase, N.A. as Member and Paymentech, LLC as processor), on issuer-processor Marqeta for Cash App Card, and on partner banks (Sutton, Bancorp, Celtic, Lincoln Savings). The networks can unilaterally change interchange and scheme fees twice a year (April/October). **[CONFIRMED FACT]**

---

## Details

### VII.1 The Acquiring Side — a Square card-present transaction, traced end to end

Trace $100 tapped at a Square seller on a Visa consumer credit card, Free plan (2.6% + 15¢ = $2.75 merchant discount):

**The parties that take a cut, in order:**
1. **The cardholder's issuing bank** (e.g., Chase, Capital One) — receives **interchange**, the largest slice, typically 70–80% of the merchant discount rate; ~$1.75–1.80 on a $100 consumer-credit transaction.
2. **The card network (Visa/Mastercard)** — receives **assessment/scheme fees**, ~0.13–0.14% (~$0.13–0.16), plus per-transaction and (for cross-border) international service/acquirer fees (ISA 0.3–2.3%, IAF 0.45%).
3. **The sponsoring acquirer / Member bank** — historically **JPMorgan Chase Bank, N.A.** as the Visa/Mastercard "Member," governing authorisation, conveyance and settlement.
4. **The acquiring processor** — **Paymentech, LLC**, routing authorisation and clearing.
5. **The payment facilitator — Block itself (Square)** — aggregates the seller under its own master merchant account, takes the residual markup, and (crucially) **controls the settlement step**, deciding when the seller is funded.
6. **The seller** — receives $97.25 the next business day (standard) or instantly for a fee.

Under the FY2025 disclosure, Square is described as acting as **both merchant of record and payment service provider**, maintaining contractual relationships directly with acquiring processors, card networks and other providers. This is the "processing more directly" evolution: Block has progressively moved from pure payment-facilitator-under-a-sponsor toward being the merchant of record, capturing more of the stack and controlling settlement — the foundation of Square Loans' self-liquidating repayment.

**Pricing across channels (current, US):**
- Card-present: 2.6% + 15¢ (Free); 2.5% + 15¢ (Plus, $49/mo); 2.4% + 15¢ (Premium, $149/mo). (Fixed fee rose from 10¢ to 15¢ effective 27 March 2025.)
- Online (website/eCommerce): 3.3% + 30¢ (Free) / 2.9% + 30¢ (paid).
- Keyed / card-on-file: 3.5% + 15¢ (all plans; not discounted).
- Invoices: 3.3% + 30¢ (card) or 1% (ACH, $1 min).
- ACH bank transfer: 1% ($1 min).
- Afterpay via Square: 6% + 30¢.
- Custom/interchange-plus pricing: available to sellers processing >$250,000/yr with average ticket >$15.

**Take rate and its drift:** Total company GPV was $240.8bn in 2024 (Square GPV ~$227.6bn/$228bn); transaction-based **gross profit as a % of GPV was ~1.15% in Q2 2024, down 1bp YoY and 2bp QoQ** — the secular compression as Block's seller mix moves upmarket (bigger sellers negotiate lower rates / interchange-plus, and larger tickets dilute the fixed-fee contribution).

### VII.2 The Issuing Side — the reverse flow

- **Cash App Card:** Visa debit/prepaid, issued by **Sutton Bank** (Member FDIC, Attica, Ohio) and now also **The Bancorp Bank, N.A.**; issuer-processed by **Marqeta**. Block earns interchange on every purchase — estimated ~0.9% on Cash Card spend (analyst estimate, ~$140bn spend in 2023). This is the reverse of the acquiring flow: here Block sits on the issuer side and *collects* the interchange a merchant's acquirer pays.
- **Square debit card:** Mastercard, issued by **Sutton Bank**, issuer-processed by Marqeta; links to Square Checking; earns interchange and offers a 2.75% discount at other Square sellers to keep spend inside the ecosystem.
- **Square Credit Card:** issued by **Celtic Bank** under an **American Express** licence, runs on the Amex network.
- **The Durbin question (economically decisive):** Regulation II caps debit interchange at $0.21 + 0.05% (+$0.01 fraud adjustment) for issuers with ≥$10bn in assets. Per Federal Reserve Board 2024 data (via the Kansas City Fed), the **average exempt dual-message interchange fee rose to $0.62 per transaction in 2023 (up from $0.51 in 2011), or 1.41% of transaction value; single-message exempt fees averaged $0.27** — versus roughly $0.23 for covered (large) issuers. Sutton Bank, Bancorp and Celtic are all well below $10bn, so **Block's card economics ride on the exempt tier** — roughly double to triple the interchange of a big-bank card. Square Financial Services' own asset base (~$845m equity Q3 2025; total assets a few billion) is far below $10bn, so SFS-held deposits are also exempt. **If any issuing partner or SFS were to cross $10bn, per-transaction debit interchange would fall sharply on that portfolio** — a material threat given the exempt premium currently earned. The Fed's October 2023 proposed revision to Regulation II would set the cap at **"$0.144 plus 0.04 percent of the value of the transaction, plus a fraud-prevention adjustment of $0.013"** (i.e., ~17.7¢ on a $50 transaction) — but only for covered issuers; it does not touch exempt issuers directly, though it would widen the exempt advantage. As of the research date the proposal remained pending. **[CONFIRMED FACT / pending]**
- **Interchange as a share of Cash App gross profit:** interchange sits inside "Financial Services" (~38% of Cash App gross profit in 2023, alongside ATM fees, Borrow, interest on customer funds and Cash App Pay). Cash App Card interchange is plausibly Cash App's second-largest single strand after Instant Deposit and has grown with Cash Card actives (26m of 59m users by 2025).

### VII.3 Settlement, Speed and the Price of Time

The settlement-speed menu:
- **Square standard settlement:** next business day, free (funds swept to linked bank via ACH).
- **Square Instant Transfer / Instant Deposit:** 1.75% (min $25 transfer, max $10,000) to a linked debit card or bank, near-instant via push-to-card (Visa Direct / Mastercard Send) rails.
- **Square Checking:** funds available immediately (0% — kept inside the ecosystem, monetised via debit interchange and float).
- **Cash App standard cash-out:** free, 1–3 business days (ACH).
- **Cash App Instant Deposit:** 0.5%–1.75% (min $0.25; some binding terms show 0.5%–2.5%, min $0.25–$1, cap $75) to a linked debit card via push-to-card.
- **Same-day/next-day payroll and disbursement** options exist within Square Payroll and instant-availability features.

**How much gross profit is "selling time"?** Instant Deposit alone was ~29% of Cash App gross profit in 2023 (35% ex-BNPL); at Square, "Banking" (Square Loans + Instant Transfer + Square debit) was a growing double-digit share. The rails cost Block a modest network fee (push-to-card) or near-zero (internal); the customer pays 0.5–1.75% for immediacy. **This is one of Block's most profitable and genuinely innovative products: charging a spread on the time-value of money the customer already owns.**

### VII.4 Stored Value, Customer Funds and Float

- **Where the money sits:** Cash App balances and Square balances are customer funds held by Block but placed at partner banks (Sutton, and via Wells Fargo historically for balance insurance) and, for Square Checking/Savings, at **Square Financial Services** and Sutton Bank.
- **Deposit insurance:** pass-through FDIC insurance up to $250,000 via the partner bank, subject to aggregation and conditions; Block itself is explicitly **not** an FDIC-insured bank.
- **Float economics:** Block is restricted from operational use of customer funds but may invest a portion in short-term marketable debt securities and money-market funds; interest earned is booked in subscription-and-services revenue (FY2024 subscription-and-services revenue $7.16bn). **Year-end 2024 customer funds (assets) were $4.18bn (2023: $3.17bn); customers payable was $5.84bn (2023: $6.80bn).** A notable behavioural fact from AML litigation documents: Cash App customers "do not appear to leave stored balances in Cash App very long," which caps float income — money flows through rather than resting.

### VII.5 The Peer-to-Peer Rail

- **Mechanics:** Cash App P2P between two Cash App users is a **book transfer** within Block's ledger — no interbank movement, instant, free. Movement in/out of the traditional banking system uses ACH (funding from a linked bank, standard cash-out) or push-to-card (Instant).
- **Pricing:** sending/receiving between individuals is free; **credit-card funding costs the sender 3%**; **business-account receipts cost 2.75%**; instant cash-out 0.5–1.75%.
- **Direct deposit / paycheck:** each user gets routing and account numbers belonging to **Lincoln Savings Bank (073923033)** or **Sutton Bank (041215663)**; paychecks arrive via ACH, often up to two days early. Paycheck-deposit actives reached 2.5m in December 2024 (+25% YoY).
- **Economics of a free rail:** P2P itself was only ~8% of Cash App gross profit in 2023. It is a **customer-acquisition and engagement engine** — the free rail seeds the network and the deposit relationship; monetisation comes downstream from Cash Card interchange, Instant Deposit, Borrow and Cash App Pay (2.75–2.9% merchant take, a much higher rate than interchange).

### VII.6 The Bitcoin Rail

- **Trading flow:** Block buys bitcoin from broker-dealers or from Cash App customers and resells to customers at a marginal markup, booking the **full sale amount as revenue** (principal treatment) and the purchase cost as cost of revenue.
- **The true margin:** bitcoin was ~63% of Cash App revenue in 2024 but bitcoin gross profit was only ~6% of Cash App gross profit; company-wide, 42.3% of 2024 revenue at a ~3% gross margin (e.g., $67m GP on $2.61bn revenue, Q2 2024; $205m GP on $9.50bn revenue, FY2023). **Anchoring on revenue overstates the business by roughly 40 points; on gross profit bitcoin is a rounding item.**
- **As a rail:** Lightning Network send/receive is live (QR/link, near-instant, little/no fee, $999/7-day cap, excluded in New York). Today bitcoin functions **primarily as a traded asset, not a payment rail** in Block's economics. Management's 2026 ambitions (stablecoins, Lightning payments auto-converting USD↔BTC, Square merchant BTC acceptance) are **COMPANY CLAIM** and forward-looking.

### VII.7 Network Relationships and Dependency (ranked)

1. **Visa & Mastercard** — highest dependency; Block relies on them as acquirer (Square GPV) AND issuer (Cash App Card = Visa; Square debit = Mastercard) AND for push-to-card rails (Visa Direct/Mastercard Send). Networks unilaterally reset interchange and scheme fees twice yearly; Block is a price-taker.
2. **Partner/issuing banks (Sutton, Bancorp, Celtic, Lincoln Savings)** — high dependency; they hold customer funds, provide FDIC pass-through, and (being sub-$10bn) supply the Durbin-exempt interchange advantage. Concentration on Sutton Bank is notable.
3. **Sponsoring acquirer/processor (JPMorgan Chase, N.A. / Paymentech)** — declining but historically foundational dependency; mitigated as Square becomes merchant of record.
4. **Marqeta (issuer-processor)** — moderate; the 2023 contract renewal cut Marqeta pricing and changed revenue presentation, showing Block's growing leverage.
5. **American Express** — low/contained; only the Square Credit Card.

### VII.8 Where the Gross Profit Actually Comes From (decomposition)

FY2024 gross profit $8.889bn (Cash App $5.24bn; Square $3.6bn). FY2025 $10.36bn (Cash App $6.34bn; Square $3.94bn). Approximate money-movement decomposition (blending Block's 2023 inflows framework and segment disclosures — **THIRD-PARTY ESTIMATE / ANALYTICAL INFERENCE**):

- **Merchant-acquiring spread (Square payments):** largest single money-movement pool (~$2.5–3bn+ of Square GP), but slowest-growing and margin-compressing (~1.15% of GPV).
- **Issuing interchange (Cash App Card + Square cards):** large and growing with Cash Card actives; the reverse-interchange engine; most exposed to Durbin threshold risk.
- **Instant-settlement fees (Instant Deposit/Transfer):** ~29–35% of Cash App GP; high margin; **most defensible in the US, least transplantable.**
- **Float / interest on customer funds:** modest; rate-sensitive; capped by fast balance turnover.
- **Subscription & services / software:** fastest-growing (Square software & integrated payments ~59% of Square GP), highest margin, the most genuine "technology" earnings.
- **Lending (Square Loans, Cash App Borrow, Afterpay):** fast-growing (Borrow origination +3x YoY in Q4 2025); self-liquidating repayment via settlement control.

**Largest:** acquiring spread (Square) + interchange (Cash App) together. **Fastest-growing:** lending and subscription/software; Instant Deposit. **Most vulnerable to regulation:** issuing interchange (Durbin threshold + Reg II revision) and instant-settlement (as instant rails like FedNow/RTP commoditise speed).

### VII.9 THE TRANSPLANT VERDICTS

**(a) Merchant-acquiring take-rate model (2–3% MDR) → ADAPT (heavily).** The US 2.6% MDR is sustainable because US interchange is high (~1.7–2% credit) and card usage is near-universal. In Nigeria the CBN caps the merchant service charge per its **"Guide to Charges by Banks and Other Financial Institutions, 2026" (exposure draft dated 21 April 2026, signed by Director of Financial Policy and Regulation Dr. Rita Sike, effective 1 May 2026): "The MSC payable by a merchant (0.5 per cent), subject to a cap of N10,000, shall be the same irrespective of the technology or payment methods."** Much retail is still cash. *Institutional feature doing the silent work: high US interchange set by the networks.* A Nigerian acquirer cannot earn a 2.6% spread; it must earn thin per-transaction fees at massive volume (the Moniepoint/OPay/PalmPay POS model — ₦79.5tn processed by those operators in 2024) or bundle software. **ADAPT: price at ~0.5% or flat per-transaction, monetise via SaaS, lending and float instead of acquiring spread.**

**(b) Interchange as a subsidy for free consumer products → REJECT (as a funding model).** *This is the single most important finding.* In the US, Durbin-exempt debit interchange (dual-message averaging $0.62/1.41% in 2023, uncapped) silently funds "free" P2P, free standard cash-out, cashback, and customer acquisition. Nigeria has no comparable pool: the issuer's slice of the 0.5% MSC is a fraction of a percent, and the card scheme fee is a fraction of 7.5% of 0.5% (≈0.0375%), capped at ₦75. **There is no interchange subsidy to fund free consumer products in Nigeria.** The reader must fund consumer products from other sources: **lending net-interest margin, FX/remittance spread, float (where regulation permits), subscription/agent-network fees, and value-added services.** Build the model so the "free" hook is paid for by a specific, sized revenue line — never assume interchange will cover it.

**(c) Charging for settlement speed → REJECT (little time left to sell).** Block sells instant access because US standard settlement is slow (ACH 1–3 days). Nigeria's **NIBSS Instant Payment (NIP)** already settles interbank transfers in real time, ubiquitously — NIP processed **N1.07 quadrillion (~$702.6bn) across 962.2m–1.02bn transactions/month in 2024**, at a regulated wholesale processing fee cut to **₦3.75 per transfer effective 1 July 2023** (retail charges ~₦10–₦50). *Institutional feature doing the silent work in the US: the persistence of slow ACH as the default.* In Nigeria that gap is already closed. **REJECT for the interbank case; a narrow ADAPT exists only for niche instant-disbursement or settlement-risk scenarios, which are small.** This is where Nigeria has genuinely leapfrogged the US.

**(d) Float / stored value as a revenue source → ADAPT (with regulatory caution).** Float income depends on (i) balances resting and (ii) the operator being permitted to invest them. Cash App's own experience shows balances turn over fast, capping float. In Nigeria, CBN rules on customer-fund safeguarding (especially for MMOs/PSBs and for a cooperative structure) will constrain investment of customer funds; high policy rates make any permitted float lucrative, but safeguarding rules and the cooperative's fiduciary duties dominate. **ADAPT: treat float as a bonus, not a pillar; segregate and safeguard customer funds rigorously (the most commonly mishandled item for new platforms); confirm exactly what CBN permits the cooperative/PSB to invest in.**

**(e) Controlling settlement to enable flow-based lending repayment → ADOPT (the deepest transferable idea).** Square Loans repay as a fixed % of daily card sales deducted *before* the merchant is settled — only possible because Block controls settlement. In Nigeria the reader must control the equivalent settlement choke-point: the **merchant's POS/acquiring settlement or the NIP collection account** feeding the cooperative member's wallet. If the reader is the core-banking platform AND the settlement processor for its cooperative merchants, it can replicate pre-settlement deduction on NIP/POS inflows. **ADOPT, conditioned on the reader owning the settlement/collections rail for its members — which the vertically integrated design makes feasible.**

**(f) Free P2P as a customer-acquisition engine → ADAPT (funding source differs).** Cash App's free P2P works because interchange funds the subsidy. In Nigeria, NIP transfers are already cheap/instant (so "free P2P" is not a differentiator by itself) AND there is no interchange to fund acquisition. *Institutional feature: interchange-funded acquisition subsidy.* **ADAPT: the acquisition hook cannot be "free transfers" (NIP already commoditised that); it must be a distinctive value proposition (cooperative membership benefits, credit access, savings yield, agent proximity) funded by lending/FX/subscription rather than interchange.**

---

## Recommendations

**Stage 1 — Design the revenue model around the absence of interchange (do this first).** Explicitly size every "free" consumer feature and attach it to a named paying line (lending NIM, FX/remittance spread, subscription, agent fees). Benchmark: if any free feature is implicitly assumed to be "covered by card economics," stop — Nigeria's 0.5%-capped MSC and ~0.0375%/₦75-capped scheme fee will not cover it. Threshold to revisit: only if CBN materially raises the MSC cap or introduces a US-style interchange regime (it tried in 2016 and suspended it in April 2017).

**Stage 2 — Own the settlement/collections choke-point for cooperative members.** This is the transferable core of Block's model. Architect the core-banking platform so member merchant inflows (POS + NIP collections) route through accounts the platform controls, enabling pre-settlement deduction for flow-based loan repayment. Benchmark: you can deduct a fixed % of daily inflows before the member can withdraw. If you cannot control settlement, flow-based lending will not work and you must fall back to conventional underwriting.

**Stage 3 — Do NOT build a "sell instant settlement" product for the interbank case.** NIP has already eliminated the time you would sell. Redirect that product engineering toward services NIP does not provide: reconciliation, working-capital credit, savings yield, and cooperative-specific financial management. Threshold to reconsider: only if a settlement-risk or off-rail scenario emerges where instant certainty commands a fee.

**Stage 4 — Safeguard customer funds as if regulators are watching, because they will be.** Segregate customer funds, obtain the correct CBN licence (Super-Agent / PSSP / PTSP / MMO / PSB as the model requires), and treat float as upside, not budget. Block's 2025 Cash App penalties — a **$175m CFPB order (16 January 2025: up to $120m in consumer redress plus a $55m penalty, per CFPB Director Rohit Chopra); $80m to 48 state financial regulators (15 January 2025, BSA/AML); and $40m to NYDFS (10 April 2025, per Superintendent Adrienne A. Harris)** — were overwhelmingly for AML/consumer-protection failures; the reader's cooperative fiduciary duty raises the stakes further.

**Stage 5 — Use agent-banking + USSD for reach, not cards.** Card interchange economics that anchor US fintech do not exist; Nigeria's growth is in POS agents (₦18.32tn POS volume in 2024) and USSD. Build distribution there, and treat Verve (Interswitch's domestic scheme) as the default card rail for cost reasons where cards are needed.

---

## Caveats

- **Segment restatements:** Block moved BNPL fully into Cash App from Q4 2023 and re-cut disclosure into Commerce Enablement / Financial Solutions / Bitcoin Ecosystem from FY2025 while retaining Square and Cash App as reportable segments. Cross-year comparisons of sub-line contributions are approximate. **THIRD-PARTY ESTIMATE / ANALYTICAL INFERENCE** labels apply to the gross-profit decomposition, which blends Block's 2023 "inflows framework," analyst estimates (interchange ~0.9%; Instant Deposit ~29–35% of Cash App GP), and segment disclosures. Block does not publish a clean gross-profit-by-money-movement-step table.
- **FY2025 balance-sheet detail (customer funds year-end 2025, standalone interest-on-customer-funds) was not verifiable in a primary filing** as of the research date; the $4.18bn/$5.84bn figures are FY2024 year-end. **UNKNOWN:** exact FY2025 customer-funds balance and the standalone dollar figure for interest earned on customer funds (bundled in subscription-and-services revenue).
- **Nigerian interchange:** Nigeria's regulated headline is the 0.5%/₦10,000 MSC; the specific CBN issuer/acquirer/switch interchange *split* within that (from the 2020 Guidelines on Operations of Electronic Payment Channels, Interchange Guidelines section) could not be extracted verbatim and is flagged **UNKNOWN** at the sub-component level. The 2016 interchange-fee circular was **suspended in April 2017**, so Nigeria effectively runs on MSC-based pricing. The ≈0.0375%/₦75-cap figure is a **scheme fee**, adjacent to but not identical with interchange.
- **Forward-looking items** (Block's stablecoin/Lightning 2026 plans; Reg II revision still pending; SFS growth) are labelled COMPANY CLAIM or noted as pending and must not be read as accomplished facts.
- **Push-to-card rail attribution** (Visa Direct vs Mastercard Send vs RTP/FedNow) for each specific Instant product is inferred from product mechanics and network membership; Block does not disclose per-product rail routing.

---

## Volume VII Reconstruction

**(1) End-to-end card transaction map (nine cuts, $100 card-present, Visa consumer credit, Square Free):** Cardholder pays $100 → **Issuer** keeps interchange (~$1.75–1.80) → **Network (Visa)** keeps assessment (~$0.13–0.16) + per-transaction/scheme fees → **Member/sponsor bank (JPMorgan Chase, N.A.)** governs settlement → **Processor (Paymentech, LLC)** clears → **Payment facilitator (Square/Block)** takes residual markup and controls settlement timing → **Seller** receives $97.25 next business day (or instantly, less 1.75%). Additional parties on relevant transactions: **card program manager/issuer-processor** and, cross-border, the **International Service Assessment/International Acquirer Fee** collectors.

**(2) Issuing-side map:** Cash App Card (Visa; Sutton Bank / Bancorp; Marqeta-processed) → Block earns ~0.9% exempt interchange. Square debit (Mastercard; Sutton Bank) → interchange + 2.75% intra-ecosystem discount. Square Credit Card (Amex licence; Celtic Bank) → Amex-network economics.

**(3) Settlement-speed menu:** Square standard (next-day, free); Square Instant (1.75%); Square Checking (immediate, 0%); Cash App standard (1–3 days, free); Cash App Instant (0.5–1.75%, up to 2.5%/cap $75 per binding terms); payroll same-/next-day.

**(4) Customer-funds/float map:** $4.18bn customer-fund assets / $5.84bn customers payable (YE2024) held at Sutton/SFS/partner banks; FDIC pass-through to $250k; interest booked in subscription-and-services; float capped by fast turnover.

**(5) P2P rail:** book transfer within Block (free); credit-card funding 3%; business receipts 2.75%; ACH direct deposit via Lincoln Savings (073923033) / Sutton (041215663).

**(6) Bitcoin rail with true margin:** ~42.3% of 2024 revenue, ~3% margin, ~6% of Cash App GP; Lightning live but a usability feature, not a core rail.

**(7) Network dependency ranking:** Visa/Mastercard > partner/issuing banks > sponsoring acquirer/processor > Marqeta > American Express.

**(8) Gross-profit-by-step decomposition:** acquiring spread + issuing interchange (largest); instant-settlement fees + lending + subscription (fastest-growing); issuing interchange + instant-settlement (most regulation-exposed).

**(9) Transplant verdict table:** MDR model → **ADAPT**; interchange-as-subsidy → **REJECT (as funding model)**; charging for speed → **REJECT**; float → **ADAPT**; settlement-controlled lending → **ADOPT**; free P2P acquisition → **ADAPT**.

**(10) Key unknowns:** FY2025 customer-funds balance; standalone interest-on-customer-funds figure; exact CBN interchange sub-component split; per-product push-to-card rail routing.

**(11) Ten most important conclusions:**
1. Interchange is the hidden American subsidy; it does not exist in Nigeria — the reader's single biggest design constraint.
2. Block's biggest gross-profit pools are acquiring spread + issuing interchange; the fastest-growing are lending and subscription/software.
3. Selling settlement speed is Block's most elegant product and its least transplantable — NIP already closed the gap.
4. The self-liquidating, settlement-controlled loan is the deepest transferable idea — ADOPT if the reader owns the collections rail.
5. Block is a price-taker to Visa/Mastercard on both sides; the networks reset the economics twice a year.
6. The Durbin-exempt status of Block's sub-$10bn issuing partners roughly doubles-to-triples its debit interchange versus big banks — and is its biggest single regulatory exposure.
7. Bitcoin inflates revenue ~42% at ~3% margin and is a traded asset, not a rail, in today's economics.
8. Float is modest and turnover-capped; safeguard it, don't budget on it.
9. Free P2P is an acquisition engine funded by interchange — in Nigeria that funding source is absent, so the hook must change.
10. Net answer: Block is **more toll booth than technology** at the margin — a large, defensible collection of spreads on American rails — with a genuine technology core (seller OS, P2P graph, settlement-controlled lending) that is the part most worth transplanting.

**Central question — how much is technology vs toll booth?** Roughly: the merchant-acquiring spread, the interchange capture, the instant-settlement fee and the float are **toll-booth economics** dependent on American rail characteristics (high interchange, slow ACH); together they are the majority of gross profit. The **subscription/software, the seller operating system, the P2P network graph, and the settlement-controlled self-liquidating loan** are **genuine technology/network assets**. For a Nigerian founder, transplant the technology core and the settlement-controlled lending; do not transplant the toll-booth assumptions — the rails that make them pay do not exist there.

**Which step generates the most gross profit?** Merchant-acquiring spread and Cash App issuing interchange, jointly. **Most defensible?** Instant-settlement fees and the subscription/software layer. **Most exposed to regulatory change?** Issuing interchange (Durbin threshold + Reg II revision). **What Block controls vs rents:** it *controls* settlement timing, the seller OS, the P2P ledger and its lending logic; it *rents* the card networks, the sponsoring acquirer, the issuer-processor and the partner-bank charters — the very things that make the toll-booth economics possible.

---

# VOLUME VIII — Financial Architecture & Segment Economics

---

## TL;DR
- **Cash App is now decisively the better business, and the two economics are DIVERGING, not converging.** In FY2025 (CONFIRMED FACT, Q4 2025 Shareholder Letter, "2025 Highlights"): "Cash App Gross Profit $6.34B +21% YoY Growth… Square Gross Profit $3.94B +9% YoY Growth" against total "$10.36B +17% YoY Growth." Cash App is bigger, faster, higher-margin per user, and increasingly the source of both the group's growth and its credit risk; Square is a slower, more capital-light, more cyclical commerce annuity.
- **The rising loss line is roughly two-thirds a growth signal and one-third a control/design signal.** The FY2025 "transaction, loan, and consumer receivable losses" line of $1,337.2m (up 68% YoY — CONFIRMED, FY2025 10-K: "$1,337,246 [vs] $794,221 … $543,025 … 68%," now "13% of total gross profit" from 9%) is driven mainly by a deliberate ~9x expansion of the on-balance-sheet loan book (loans held for investment $365m→$3.38bn net; provision $561.4m against $216.5m write-offs) — mechanical CECL front-loading on good growth — with a smaller but real fraud/dispute strand that is the deferred cost of frictionless onboarding.
- **For the Nigerian founder the transferable assets are the unit economics, not the financials.** The ~10x primary-banking-active multiple, gross profit as the governing metric, and software-attach as the margin engine ADOPT cleanly; the American interchange subsidy, the deliberate hardware/P2P loss-leader, and the non-GAAP presentation habit must be REJECTED or heavily ADAPTED.

---

## Key Findings

1. **Gross profit, not revenue, is the only honest lens.** FY2025 total net revenue was ~flat at $24.19bn (CONFIRMED, 10-K: 2025 $24,193,683k vs 2024 $24,121,053k), but that masks everything. Bitcoin Ecosystem revenue *fell* $1.85bn (−18%) to $8.50bn while the rest grew ~14% ("Excluding bitcoin ecosystem revenue, total net revenue increased by $1.9 billion, or 14%"). Bitcoin was ~35% of FY2025 revenue at a ~4% gross margin. Anchoring on revenue understates the real business by roughly a factor of three. Gross profit was $10.36bn (+17%).

2. **The FY2025 disclosure re-cut genuinely obscures the segment comparison.** Block now reports revenue/COGS in three categories (Commerce Enablement, Financial Solutions, Bitcoin Ecosystem) that *cut across* the two reportable segments (Square, Cash App). Combined with the Q4 2023 move of the entire BNPL platform from a 50/50 split into Cash App alone, the multi-year series has been restated twice in three years. The three-category cut mixes Square and Cash App inside each line, making a clean segment-strand comparison impossible from the face of the filings.

3. **Cash App and Square are diverging on every axis.** Growth (21% vs 9%), margin trajectory (Financial Solutions GP per active +57% YoY vs Square commerce monetization compressing to 1.18%), capital intensity (Cash App now carries a multi-billion-dollar consumer loan book; Square Loans are largely sold forward), and cyclicality (Cash App tied to consumer inflows and credit; Square tied to SMB card volume).

4. **The loss line decomposes cleanly into growth vs control.** Of the $1,337.2m FY2025 losses: ~$561.4m is credit provision on loans held for investment (overwhelmingly Cash App Borrow newly on the balance sheet), ~$333.8m is credit provision on Afterpay/BNPL consumer receivables, and the ~$442m remainder is transaction/fraud/dispute loss. The step-change from $794.2m is ~90% attributable to the loan book moving onto the balance sheet.

5. **Share-based compensation is large but no longer growing, and adding it back is defensible only partly.** SBC was $1,215.5m in FY2025 (11.7% of gross profit), down from $1,272.6m (2024) and $1,276.1m (2023). It is a real economic cost; Block's Adjusted Operating Income is explicitly "fully burdened by share-based compensation" (Q4 2025 Shareholder Letter, footnote 5) — a credit to disclosure quality — whereas Adjusted EBITDA and the old Adjusted-EPS definition were not (footnote 6: "Beginning in fiscal 2025, we revised our definition of Adjusted Net Income Per Share to include share-based compensation").

---

## Details

### VIII.1 Multi-Year Financial History (with restatements flagged)

**Consolidated (CONFIRMED FACT, Form 10-K / shareholder letters; USD, US GAAP, 31 Dec year-end):**

| Metric ($M unless noted) | 2021 | 2022 | 2023 | 2024 | 2025 |
|---|---|---|---|---|---|
| Total net revenue | 17,661 | 17,532 | 21,916 | 24,121 | 24,194 |
| — of which Bitcoin revenue | ~10,013 | ~7,110 | ~9,498 | 10,358 | 8,503 |
| Gross profit | 4,420 | 5,987 | 7,505 | 8,889 | 10,360 |
| Product development | — | — | — | 2,914 | 2,908 |
| Sales & marketing | — | — | — | 1,984 | 2,273 |
| General & administrative | — | — | — | 2,149 | 1,998 |
| Transaction, loan & receivable losses | — | — | 661 | 794 | 1,337 |
| Amortization of acquired intangibles | — | — | — | 155 | 136 |
| Total operating expenses | — | — | — | 7,997 | 8,652 |
| Operating income (loss) | — | (622) | 259 | 892 | 1,708 |
| Net income (loss) to common | 158 | (541) | 10 | 2,866 | 1,306 |
| Diluted EPS ($) | — | — | 0.02 | 4.56 | 2.10 |
| Adjusted EBITDA | — | 991 | 1,790 | 3,030 | 3,470 |
| Adjusted Operating Income | — | — | ~360 | 1,610 | 2,080 |
| SBC expense | — | — | 1,276 | 1,273 | 1,215 |
| Operating cash flow | — | — | 101 | 1,707 | 2,580 |

**Restatement flags:** (i) **Q4 2023** — entire BNPL platform reallocated from a 50/50 Square/Cash App split into Cash App only, mechanically lifting Cash App's historical growth rate and depressing Square's; (ii) **FY2025** — revenue and cost of revenue re-cut into Commerce Enablement / Financial Solutions / Bitcoin Ecosystem, replacing the prior transaction / subscription-and-services / hardware / bitcoin categories. Net income in 2024 was inflated by ~$1.9bn of one-time tax benefits (valuation-allowance release plus deferred-tax-asset recognition), so the 2024→2025 net-income "decline" is an artifact — operating income actually *rose* 91% ($892.3m→$1,708.4m, CONFIRMED 10-K).

**Operating metrics parallel series (CONFIRMED):**

| Metric | 2023 | 2024 | 2025 |
|---|---|---|---|
| Square GPV ($bn) | ~210 | 227.6 | 250.5 |
| Total GPV incl. Cash App commerce ($bn) | ~228 | 240.8 | ~290 |
| Cash App monthly transacting actives (M, Dec) | 56 | 57 | 59 |
| Cash App inflows ($bn) | 248 | 283 | 316 |
| Square sellers (M) | ~4 | ~4 | 4.5+ |
| Cash App primary-banking actives (M, Dec) | ~6.4 | 7.6 | 9.3 |

### VIII.2 The Two Segment P&Ls (segment-first — the first re-cut)

**Segment gross profit (CONFIRMED, 10-K segment note; on the segment basis, which allocates BNPL to Cash App from Q4 2023):**

| Segment gross profit ($M) | 2022 | 2023 | 2024 | 2025 | 2024→25 growth |
|---|---|---|---|---|---|
| Cash App | 3,245 | 4,323 | 5,239 | ~6,340 | +21% |
| Square | ~2,740 | ~3,130 | ~3,600 | ~3,940 | +9% |
| Corporate/other (TIDAL etc.) | ~0 | ~50 | ~50 | ~80 | — |
| **Total** | **5,987** | **7,505** | **8,889** | **10,360** | **+17%** |

Block discloses segment revenue and segment gross profit but **explicitly does not allocate operating expenses, assets, or operating income to segments** — the CODM (the Block Head and Chairperson, Jack Dorsey) manages to segment *gross profit* only ("The CODM does not evaluate performance or allocate resources based on segment asset data"). Segment operating income is therefore UNKNOWN from disclosure and can only be estimated. ANALYTICAL INFERENCE: because Cash App carries almost the entire consumer loan book and the bulk of transaction-loss/fraud exposure, while Square carries the field sales force and the hardware loss, a rough allocation suggests Cash App's segment operating margin is now structurally higher than Square's, reinforcing divergence.

**Verdict on convergence: DIVERGING.** Cash App is growing ~2.3x faster, is more capital-intensive (loan book), more consumer-cyclical, and less defensible per-product (P2P is a commodity) but more defensible as a bundle (primary-banking lock-in). Square is slower, more capital-light, more defensible per-product (integrated-software switching costs) but exposed to SMB cyclicality and take-rate compression as it moves upmarket.

### VIII.3 Gross Profit Decomposition by Strand

**By the new three-category cut (CONFIRMED, FY2025 quarterly sums from shareholder letter):**
- **Commerce Enablement: ~$6,105m** — the largest strand (Square payments+software+hardware plus Cash App Card/Pay/BNPL/Business). Q4 growth "accelerated to 11%, led by strength in Cash App." Contains both segments.
- **Financial Solutions: ~$3,837m** (Cash App Borrow, Instant Deposit, interest income, Square Loans, banking). **Fastest-growing:** Q4 2025 Shareholder Letter: "Financial Solutions gross profit growth also accelerated to 51% year over year in the fourth quarter, driven by Cash App Consumer Lending."
- **Bitcoin Ecosystem: ~$419m** (~4% of total; buy/sell in Cash App plus Proto/Bitkey hardware). Most volatile — fell 19% in Q1 2025, and in Q2 2026 Bitcoin gross profit fell 31% YoY to $72m, the only category to contract.

**Square strand composition (Volume III carry-forward + FY2025 direction):** Software & integrated payments ~59%, banking & lending ~23% (now the growth driver — the letter states Square gross profit "grew 7.5% year over year… driven primarily by Financial Solutions, most notably Square Loans"), standalone payments ~20%, hardware a deliberate gross loss (FY2024 ~$143m revenue vs ~$236m cost = ~$93m loss).

**Cash App strand composition (2023 THIRD-PARTY ESTIMATE, directional):** Financial Solutions ~38%, Instant Deposit ~29%, BNPL ~17%, P2P ~8%, bitcoin ~6–7%. FY2025 direction: Financial Solutions (Borrow) now the dominant growth engine — Financial Solutions GP per active grew from $9 (Q4'24) to $15 (Q4'25), +57%.

**Highest regulatory exposure:** Financial Solutions (lending — CFPB, state usury, the DOJ inquiry with its ~$240m reserve) and interchange (Cash App Card / Square Card, exposed to Durbin-style caps). Most durable: Square software attach. Most volatile: Bitcoin.

### VIII.4 Unit Economics (the transferable core)

**Per Cash App active (CONFIRMED / ANALYTICAL INFERENCE):**
- Total gross profit per monthly active: ~$107/year (2025: $6.34bn / 59M). Rose from $41 (Q4 2020, annualized) to ~$107.
- Financial Solutions GP per active: $15/quarter in Q4 2025 (+57% YoY, CONFIRMED).
- **A primary-banking active generates nearly 10x the gross profit of a P2P-only active** (COMPANY CLAIM). Verbatim, Q4 2025 Shareholder Letter: "Primary banking actives grew to 9.3 million in December, up from 8.3 million in September. These customers generate nearly 10x the gross profit per active compared to peer-to-peer only actives"; "we added 1 million Primary Banking Actives (PBAs) in December, and accelerated year-over-year growth to 22%." This is the single most important number in the study.
- Inflows per active: $1,410/quarter (Q4 2025), ~$5,356/active/year. Gross-profit take on inflows ≈ 2.0% ($6.34bn / $316bn).

**Per Square seller (ANALYTICAL INFERENCE from CONFIRMED aggregates):**
- GPV per seller: ~$55,700/year ($250.5bn / 4.5M sellers).
- Gross profit per seller: ~$875/year ($3.94bn / 4.5M).
- Blended take rate: 1.57% of GPV; transaction-only ~1.13–1.15%; commerce-enablement-ex-hardware monetization 1.18% in Q4 2025 (compressing as mix moves upmarket — mid-market sellers >$500k GPV were "our fastest-growing segment").

**Per dollar of volume:** Square ~1.57 cents of gross profit per GPV dollar; Cash App commerce monetization rate 1.61% of commerce-enablement volume (Q4 2025); Cash App overall ~2.0 cents per inflow dollar.

**Per dollar of loan originated:** Q4 2025 Shareholder Letter: "We grew consumer lending origination volume 69% year over year in the fourth quarter… Cash App Borrow origination volume grew 223% year over year." FY2025 consumer lending origination ~$53.7bn (+50%). Average Cash App Borrow loan repaid in <4 weeks, average <$100. Square Loans facilitated >$32.8bn cumulatively since 2014, average ~$10,000, repaid ~10 months. Because Borrow loans turn ~13x/year, origination volume vastly exceeds the ~$3.2bn balance held.

### VIII.5 Cohort Economics and Payback
- **Square:** dollar-based net retention (measured in gross profit) exceeded 100%; payback ~5–6 quarters (Volume III / Q4'22 letter, which stated "payback remained six quarters or less"). 44% of Square gross profit came from sellers using 4+ monetized products in 2022 (+15 points vs three years prior) — multi-product attach is the durability mechanism.
- **Cash App:** each recent cohort shows expanding usage and gross-profit contribution; Cash App Green cohorts show "sustained improvements in retention." Borrow actives "bring in 13% more inflows and conduct 6% more transactions than non-Borrow actives" and "generate 10% higher variable profit per active, excluding profit generated from Cash App Borrow."
- **Afterpay:** consumers on the platform >5 years "transact more than 31x per year on average, compared to 4x for those who joined in the past year" — an ~8x frequency expansion by cohort maturity.

**Year 1 / 3 / 5 worth (ANALYTICAL INFERENCE):** a Square seller cohort is worth ~$875/seller in year one and, at >100% net retention, materially more by year three/five as products attach; a Cash App active cohort is worth ~$107/active in year one but converges toward the ~10x primary-banking multiple as inflows and lending attach over three-to-five years.

### VIII.6 The Cost Architecture (FY2025, CONFIRMED unless noted)

| Cost line ($M) | 2024 | 2025 | % chg | Driver classification | Marginal behaviour |
|---|---|---|---|---|---|
| Bitcoin cost of revenue | ~9,900 | ~8,084 | −18% | Variable w/ bitcoin volume | ~96% pass-through |
| Transaction-based costs | — | — | — | Variable w/ GPV | interchange/network fees |
| Hardware cost | 236 | ~ | — | Variable w/ units (deliberate loss) | negative margin |
| Product development | 2,914 | 2,908 | —% | Step-fixed | flat despite growth |
| Sales & marketing | 1,984 | 2,273 | +15% | Semi-variable (P2P/card costs sit here) | rises w/ acquisition |
| General & administrative | 2,149 | 1,998 | −7% | Fixed | driven by lower litigation/regulatory costs vs 2024 |
| Transaction, loan & receivable losses | 794 | 1,337 | +68% | Variable w/ loan book & volume | rises w/ lending scale |
| Amortization of intangibles | 155 | 136 | −12% | Fixed/declining | — |
| SBC (embedded above) | 1,273 | 1,215 | −5% | Non-cash, step-fixed | flat/declining |

**Marginal cost of an incremental gross-profit dollar:** Square's incremental GP dollar is cheap to serve (software is near-zero marginal cost; the binding constraint is customer acquisition). Cash App's incremental GP dollar from Financial Solutions now carries a *credit-loss tax* — every incremental Borrow dollar of gross profit is booked alongside a CECL provision, so the true marginal cost is higher and rises with the loss rate.

### VIII.7 Transaction and Loan Losses Decomposed (the third re-cut)

**The line (CONFIRMED, 10-K):** $660.7m (2023) → $794.2m (2024) → $1,337.2m (2025), i.e. +68% YoY and now "13% of total gross profit" (from 9%).

**Decomposition (CONFIRMED footnote rollforwards + ANALYTICAL INFERENCE for the residual):**
- **Credit provision on loans held for investment: $561.4m** (write-offs $216.5m, recoveries $14.8m; allowance $23.1m → $382.9m). Overwhelmingly Cash App Borrow, newly on the balance sheet — the Consumer/Borrow allowance went from $0 to $340.1m; Square Loans (commercial) allowance was $33.6m.
- **Credit provision on Afterpay/BNPL consumer receivables: $333.8m** (gross receivables $2.91bn; allowance $201.8m → $239.9m; charge-offs and adjustments $302.6m).
- **Transaction/fraud/dispute loss: ~$442m** (reserve-for-transaction-losses provision ~$114.2m plus realized losses; this is the deferred cost of frictionless one-tap onboarding). *This strand is a reconciliation residual (line total minus the two audited credit-provision rollforwards) and is ANALYTICAL INFERENCE.*

**Coverage and charge-off metrics (CONFIRMED):** allowance/loans-held-for-investment = 11.3% net (10.2% gross); LHFI write-off rate ~5.7% of net balance; management states Borrow loss rates "remained in line with historical levels" even as new (higher initial-risk) cohorts scaled.

**Verdict: predominantly a GROWTH signal, with a real but smaller CONTROL/design component.**
- **Growth (~65–70%):** the entire step-change from $794m to $1,337m is explained by the loan book moving on-balance-sheet, forcing CECL to front-load lifetime expected losses at origination on a book growing ~9x. This is exactly the Klarna dynamic — rising provisions with stable underwriting.
- **Credit-quality (small/neutral):** management states Borrow loss rates held to historical levels; a 11.3% coverage ratio on very short-duration (<4-week) loans is conservative, so the balance-sheet snapshot overstates the annualized loss economics.
- **Control/design (~30%):** the ~$442m transaction/fraud strand is the price of the same one-tap onboarding that drives the network — a recurring cost of the design, not a one-off, and the strand the Nigerian reader must underwrite most carefully.

**Square Financial Services (follow-the-legal-entity):** SFS (Utah industrial bank, FDIC-insured since 2021) now carries a materially larger loan book. Latest FFIEC call-report figures (THIRD-PARTY aggregator of FDIC data; exact 31 Dec 2025 reporting date not independently confirmed) indicate roughly $2.0bn total assets, ~$1.29bn net loans, and ~$0.56bn deposits, with SFS holding a portion of the consolidated $3.38bn loans held for investment (the remainder at the parent and in loans held for sale). The 2025 FDIC approval to offer Cash App Borrow nationwide through SFS is what moved the consumer loan book on-balance-sheet and drove the FY2025 provision step-change.

### VIII.8 Operating Leverage and the Non-GAAP Stack

**The stack (CONFIRMED definitions):**
- **Adjusted EBITDA $3.47bn (2025, 33% margin):** adds back SBC, D&A, and bitcoin remeasurement — *not* burdened by SBC, so economically incomplete.
- **Adjusted Operating Income $2.08bn (2025, 20% margin):** explicitly "fully burdened by share-based compensation" (Q4 2025 letter, footnote 5) — the most honest of Block's non-GAAP measures and the one to use.
- **Rule of 40:** Block's self-selected "gross profit growth + Adjusted Operating Income margin." Q4 2025 = 24% + 20% = 44% ("We surpassed Rule of 40 in the fourth quarter"). Self-serving because it pairs a period growth rate with a management-defined margin; scrutinize, do not repeat.
- **Adjusted Diluted EPS:** redefined in FY2025 to *include* SBC (footnote 6) — an improvement.

**Genuine operating leverage:** Gross profit +17% (2025) drove operating income +91% ($892m→$1,708m) — strong incremental flow-through. BUT the improvement is *partly a cost reset*: G&A fell 7%, product development was flat, and the Workforce Plan is a one-time reset, not pure structural automation. Verbatim (Q4 2025 letter, Jack Dorsey): "We're reducing Block by nearly half, from over 10,000 people to just under 6,000, which means that over 4,000 people are being asked to leave or entering into consultation"; the accompanying 8-K cites "$450–$500 million in related charges, primarily in early 2026" (later reported at ~$852m of total restructuring charges). **Verdict: roughly half structural (mix shift toward high-incremental-margin Financial Solutions + flat opex) and half a one-time cost reset.** Q1 2026 already showed the transition cost — a GAAP operating *loss* of $172m even as Adjusted Operating Income hit a record $728m.

**SBC assessment:** $1,215.5m is 11.7% of gross profit and ~0.93x FY2025 GAAP net income to common. Adding it back to reach Adjusted EBITDA produces a number with little economic content for a company still issuing this much equity; adding it back is defensible only in Adjusted Operating Income *because that measure keeps it in*. Buybacks ($2.3bn in 2025) are partly offsetting dilution rather than pure surplus return.

### VIII.9 Cash Flow and Its Quality (CONFIRMED)
- Net income $1.30bn → operating cash flow $2.58bn (2024: $1.71bn; 2023: $0.10bn). Capex ~$155m → simple GAAP FCF proxy ~$2.42bn.
- **Distortions:** (i) the SBC add-back of $1.22bn is non-cash but a real cost — deduct it and "true" FCF is closer to ~$1.2bn; (ii) customer funds and settlements receivable flow through operating cash flow but are not Block's money; (iii) the loan book consumed cash as it grew ~9x, partly funded by warehouse facilities ($1.36bn outstanding at year-end) and SFS deposits, not operating cash; (iv) bitcoin remeasurement (−$55.9m in 2025) is non-cash under the fair-value standard.
- **Cash genuinely available to shareholders (ANALYTICAL INFERENCE):** ~$1.0–1.3bn/year once SBC is treated as the real cost it is and loan-book growth is normalized — materially below the headline ~$2.4bn FCF proxy. Block ended 2025 with $9.2bn total liquidity, **$7,289,018k of notes outstanding across seven series** (*corrected on assembly — this section originally reported "$0 long-term debt"; Volume IX refutes it definitively from Note 14 of the FY2025 10-K. See Appendix E note 1*), and $5.3bn remaining buyback authorization.
- **"Adjusted Free Cash Flow":** Block reports this only in its shareholder letters/earnings releases, not in the audited 10-K; the exact FY2025 figure is UNKNOWN from the 10-K itself.

---

## VIII.10 The Transplant Verdicts (Nigeria)

| Mechanism | Verdict | Reasoning & the silent US institutional feature | What must change (if ADAPT) |
|---|---|---|---|
| **Gross profit as governing metric** | **ADOPT** | Block's revenue is distorted ~3x by bitcoin pass-through; the reader's equivalent distortion is remittance turnover and any FX/crypto pass-through, which inflate "revenue" at ~0% margin. Manage to contribution margin per member, not turnover. | — |
| **Software/integrated services as margin engine** | **ADOPT (with realism)** | Square's ~59% software strand earns near-100% incremental margin because SMBs pay for integrated tooling. Achievable margin is high, but requires real product depth and switching costs. | Build the cooperative core-banking platform as the switching-cost moat; charge SaaS-style per-society fees, not per-transaction only. |
| **Multi-product attach / the ~10x primary-banking multiple** | **ADOPT — the single most important lesson** | A PBA earns ~10x a P2P-only active because payroll inflows + card + lending + savings compound. The cooperative analogue: a member who routes salary/savings, borrows, and transacts through the society is worth many multiples of a dues-only member. Measure it as contribution per fully-attached member vs single-product member. | Define and instrument the "primary-relationship member" from day one; make payroll/inflow capture the north-star metric. |
| **Deliberate loss on an acquisition wedge (hardware, P2P)** | **REJECT / heavily ADAPT** | Block can burn ~$93m on hardware and give P2P away because it has cheap capital and the interchange subsidy funds the network. A capital-constrained Nigerian founder cannot. Minimum viable subsidy: only subsidize the *acquisition action that provably converts to a primary relationship*, capped at a fixed % of expected 12-month member contribution. | Never subsidize hardware; subsidize only onboarding of salary-routing members, funded from lending margin. |
| **Lending as the margin engine + its loss consequences** | **ADAPT — with a hard loss ceiling** | Financial Solutions is Block's fastest-growing strand (+51% in Q4 2025), but it rides US scaffolding absent in Nigeria: FDIC-insured deposit funding, a national credit bureau, CECL discipline, and courts for collections. Block underwrites Borrow to loss rates "in line with historical levels" with 11.3% coverage on <4-week loans. **The reader must underwrite to a loss rate perhaps 2–4x Block's given weaker credit data and collections, and stress-test a doubling: at Block's ~13% loss-to-gross-profit ratio, a doubling of the loss rate would erase roughly a quarter of lending segment gross profit.** | Lend only against observed on-platform cash flows (the Square Loans model — lending against your own payment data); keep tenor ultra-short; fund from member savings, not wholesale debt; hold explicit coverage of 15–20%+. |
| **The non-GAAP presentation habit / Rule of 40** | **REJECT externally; ADAPT one measure internally** | Block's Adjusted EBITDA excludes SBC and flatters the picture; a cooperative's members and regulator (CBN/relevant authority) will and should distrust adjusted metrics. Members are owners and creditors, not equity speculators. | Report audited GAAP/IFRS-equivalent numbers to members and regulator. Internally, one Adjusted-Operating-Income-style measure *that keeps all real costs in* is acceptable for management. |

---

## Recommendations

**Stage 1 (now — instrumentation):** Build the accounting so that gross profit / member contribution is the primary metric from day one, with remittance and any FX pass-through separated exactly as Block separates bitcoin. Define the "primary-relationship member" (salary or savings routed on-platform) and make its count and its contribution-per-member the north-star, targeting the ~10x-attach logic. *Threshold to proceed:* a measurable, widening gap between primary-relationship and single-product member contribution.

**Stage 2 (lending, gated):** Launch credit only against on-platform cash-flow data (the Square Loans / Cash App Borrow model — lend against what you already see), ultra-short tenor, funded from member savings not wholesale debt. Provision conservatively (15–20%+ coverage) and instrument a monthly charge-off and vintage curve before scaling. *Threshold to scale:* observed annualized loss rate below your pre-set ceiling for two consecutive cohorts; *threshold to halt:* loss rate doubling from plan, which on Block's own ratios would erase ~25% of lending gross profit.

**Stage 3 (margin engine):** Reinvest the lending margin into the software/core-banking platform depth that creates cooperative switching costs — the durable, capital-light annuity (Square's software strand), not the payment rails themselves.

**Do not:** subsidize hardware; give away transactional services broadly; or report adjusted metrics to members/regulators. These are affordances of Block's cheap capital and the US interchange subsidy that you do not have.

---

## Caveats
- Block discloses segment *gross profit* only; segment operating income, assets, and true segment margins are UNKNOWN and are estimated here as ANALYTICAL INFERENCE.
- The three-category revenue re-cut (FY2025) and the Q4 2023 BNPL reallocation mean multi-year segment-strand comparisons are not clean; figures pre- and post-restatement are not fully like-for-like.
- The ~$442m transaction/fraud strand of the loss line is a reconciliation residual (income-statement line minus the two audited credit-provision rollforwards) and is ANALYTICAL INFERENCE, not a directly disclosed figure.
- Square Financial Services call-report figures are from third-party aggregators of FFIEC data; the exact 31 Dec 2025 reporting date is not independently confirmed against FDIC BankFind.
- Q1/Q2 2026 figures cited are the most recent reported periods but post-date the FY2025 10-K and reflect the in-progress restructuring.
- Non-GAAP measures (Adjusted EBITDA, Adjusted Operating Income, Rule of 40) are management-defined; the report uses GAAP as the spine and flags each adjustment.

---

## The Ten Most Important Conclusions
1. **Cash App is the better business** — $6.34bn gross profit growing 21% vs Square's $3.94bn growing 9%.
2. **The two economics are DIVERGING**, not converging, on growth, margin, capital intensity, and cyclicality.
3. **Revenue is meaningless here** — bitcoin distorts it ~3x; gross profit is the only spine.
4. **The rising loss line is ~two-thirds growth, one-third control** — the step-change is the loan book moving on-balance-sheet under CECL, not deteriorating underwriting.
5. **The ~10x primary-banking multiple is the whole game** — multi-product attach, not raw active count, drives unit economics.
6. **Square is the durable annuity** — >100% net retention, ~5–6 quarter payback, software switching costs — but capacity-constrained by acquisition and compressing take rate.
7. **Financial Solutions (lending) is the growth engine and the risk engine simultaneously** — +51% in Q4, but each incremental dollar carries a CECL tax.
8. **Operating leverage is real but half one-time** — the +91% operating-income jump is part mix-shift, part a workforce cost reset that produced a GAAP operating loss in Q1 2026.
9. **SBC ($1.22bn, 11.7% of gross profit) is a real cost** — Adjusted Operating Income (which keeps it in) is the honest measure; Adjusted EBITDA and Rule of 40 are not.
10. **The transferable playbook is the unit economics, not the financials** — a Nigerian founder would rather own the Cash App model (bundled consumer relationship, lending as margin engine) but must rebuild it WITHOUT the interchange subsidy, deposit-insurance funding, and credit-bureau scaffolding that silently make it work in the United States — which means building primary-relationship attach first and gating lending hard behind observed on-platform cash flows.

**Central question answered:** Square and Cash App are **diverging into two distinct economic machines** running on one shared infrastructure spine. A founder would rather own **Cash App's economics** — but only after replicating the institutional scaffolding, member by member, that the American environment provides for free.

---

# VOLUME IX — Capital, Balance Sheet & the Bitcoin Position

## Block, Inc. (NYSE: XYZ, formerly Square, Inc.) — A Forensic Reverse-Engineering Study

## TL;DR
- **What funds Block is overwhelmingly its own equity (~$22.2bn) plus $7.29bn of senior and convertible notes — not deposits and not, as Volume VIII feared, "$0 long-term debt."** That carried-forward figure is definitively wrong: Block carries $7,289,018k of notes (net carrying value) across seven series. The single most misunderstood balance-sheet item is *customers payable* ($6.81bn) and *customer funds* ($4.77bn) — several billion dollars of other people's money that make reported leverage meaningless. Stripped of customer money, Block is conservatively financed, with net debt near zero and an investment-grade BBB– rating from Fitch since May 2025.
- **The bitcoin position is a genuine but tiny and quarantined allocation that has paid off in dollar terms and cost almost nothing in capital, yet damages earnings quality.** ~$220m invested in 2020–21 (cost basis now $292.6m for 8,883 investment BTC) is worth $777.5m at end-2025 — a large percentage gain but only ~0.35% of assets and ~3.5% of equity. Under fair-value accounting (ASU 2023-08) it now whips reported net income by hundreds of millions a quarter. **Verdict: founder conviction that happens to have worked, not a disciplined allocation framework — and one the Nigerian reader is legally barred from copying.**
- **Afterpay's $11.72bn of goodwill has never been impaired — but that is an accounting artifact, not vindication.** The goodwill was split 50/50 into the Square and Cash App reporting units, so it can never be tested in isolation; it is shielded by two large, healthy businesses. Against a BNPL operation contributing on the order of $1bn of annual gross profit, the verdict is **too early to judge, leaning value-destructive on price paid** — the honest measure (a standalone impairment test) has been structurally foreclosed.

---

## Key Findings

1. **The "$0 long-term debt" claim is refuted (CONFIRMED, FY2025 10-K).** Note 14 shows $7,350,000k principal / $7,289,018k net carrying value of Notes at 31 December 2025: five senior note series ($1.0bn 2026, $1.2bn 2030, $1.0bn 2031, $2.0bn 2032, $1.0bn 2033) and two convertible series ($575m 2026 convertible, $575m 2027 convertible). This reconciles exactly to the balance sheet's $1,573,259k current portion + $5,715,759k long-term debt.

2. **Band A dominates the liabilities (CONFIRMED, FY2025 10-K).** Customers payable $6,805,366k and customer funds $4,771,824k are money owed to and safeguarded for customers, not corporate leverage. Settlements receivable $1,359,983k is a 1–2 day pass-through from card processors.

3. **The loan book's nine-fold jump was funded by an accounting reclassification, not new borrowing (CONFIRMED).** From 1 July 2025 Block began retaining Cash App Borrow, Afterpay Post-Purchase, and all Square Financial Services-originated loans on balance sheet as held-for-investment, rather than selling them or holding them for sale. This moved billions from "held for sale"/off-balance-sheet-partner status onto the balance sheet — funded principally by the parent's own equity and cash, supplemented by $1.36bn of warehouse facilities and a small SFS deposit base.

4. **Square Financial Services is tiny relative to the book it nominally supports (CONFIRMED, FDIC data).** At 30 September 2025 SFS held total assets of $1,354,373k, loans of $756,584k and deposits of $420,575k — against a group loans-held-for-investment balance of $3.38bn. The trap the framing note warned of is real: **SFS deposits do not fund the loan book; the parent does.**

5. **Bitcoin: 8,883 investment BTC at 31 Dec 2025, cost basis $292.6m, fair value $777,515k** (CONFIRMED); plus ~238 BTC (~$20m) held for operations. FY2025 recorded a net remeasurement *loss* of ~$56m (quarterly: −$93m, +$212m, +$60m, −$234m), versus a +$421m *gain* in FY2024 — illustrating the earnings volatility introduced by fair-value accounting.

6. **Proto's flagship commercial deal collapsed (CONFIRMED, Core Scientific filing).** Core Scientific booked a $41.9m loss to cancel the July 2024 agreement under which Block's Proto team was to supply 15 EH/s of 3nm mining ASICs, as Core pivoted to AI hosting. Core had paid Block/Proto a total of $67.9m for chips since 2024 ($10m July 2024, $21.3m January 2025, $36.6m January 2026).

7. **Afterpay goodwill $11,719,494k, never impaired through FY2025** (CONFIRMED, FY2022/FY2025 10-Ks); total consideration $13,836,622k (essentially all equity, 113,617,352 Class A shares valued at $13,827,929k). Afterpay intangibles at acquisition: customer assets $1,378,000k, technology $239,000k, trade name $386,000k.

8. **TIDAL goodwill is effectively written off (CONFIRMED):** $132m impairment in Q4 2023 plus $73.5m ($73,508k) in Q4 2024, against original TIDAL goodwill of ~$197.9m.

9. **FY2024 net income was inflated by ~$1.9bn of one-time tax benefits** (valuation-allowance release + DTA recognition) plus a $421m bitcoin gain — so the drop from $2,866m (2024) to $1,306m (2025) net income to common is an accounting artifact, not deterioration.

10. **Capital returns are large (CONFIRMED, Form 8-K 19 Nov 2025):** $2.3bn of buybacks in FY2025; the board approved a $5.0bn increase to the existing $4bn program on 19 November 2025, taking total authorization to $9bn, with ~$1.1bn remaining under the prior program at 30 Sept 2025 (~$6.1bn available thereafter). No dividend has ever been paid.

---

## Details

### IX.1 The Hybrid Balance Sheet Teardown — Four Bands (all figures FY2025 10-K, 31 Dec 2025 vs 2024, US GAAP, US$ thousands)

**Total assets $39,549,887; total liabilities $17,380,005; total stockholders' equity ~$22,169,882.**

**Band A — Money that is not Block's:**
- Customer funds: $4,771,824 (2024: $4,182,872) — funds held on behalf of customers, invested in cash and investment-grade securities, restricted to satisfying customer obligations. Block earns float income on these balances (interest income is a growing Financial Solutions line).
- Settlements receivable: $1,359,983 (2024: $1,060,966) — amounts due from card processors, settling in 1–2 days. Concentrated: four processors were ~41%/15%/14%/11% at Q3 2025.
- Customers payable: $6,805,366 (2024: $5,837,152) — Cash App stored balances and Square seller balances owed on demand.
- **Analytical inference:** customers payable ($6.81bn) exceeds the ring-fenced customer-funds asset ($4.77bn) by ~$2bn; the difference is effectively backed by corporate cash and the securities portfolio. This is the safeguarding gap a bank regulator would scrutinise.

**Band B — The regulated bank (Square Financial Services):**
- Utah industrial bank, operational since 1 March 2021; independently governed direct subsidiary; **permanent minimum 20% leverage ratio** imposed by the FDIC (versus ~5% for a normal "well-capitalized" bank), plus a Capital & Liquidity Maintenance Agreement and Parent Company Agreement requiring Block to serve as a source of financial strength. Initial paid-in capital was set at not less than ~$56m.
- At 30 Sept 2025 (FDIC data): total assets $1,354,373k; loans $756,584k; deposits $420,575k. An earlier quarter showed assets of ~$1.69bn / deposits ~$495m — the book is volatile quarter to quarter as loans are originated and sold.
- SFS was barred from paying dividends in its first three years and has paid none to the group (Volume I).
- **Reconciliation to group:** SFS is ~3.4% of group assets. It originates Square Loans (avg ~$10,000) and, since March 2025 FDIC approval, Cash App Borrow (avg <$100, ~1 month). The 20% leverage cage means SFS can support only ~5x its equity in assets — a structural brake on using the bank as the group's lending engine.

**Band C — The credit book and its funding:**
- Loans held for investment, net: $3,382,957 (2024: $365,062) — a 9.3x increase.
- Allowance rose from $23.1m to $382.9m (Volume V, carried forward) — consistent with the shift to expected-credit-loss provisioning on a retained book.
- Consumer receivables, net: $2,670,322 (2024: $2,504,879) — primarily Afterpay receivables.
- Loans held for sale: sit within Other current assets ($3,589,925 total); at Q1 2025 loans held for sale were $1,322,049 (consumer $771,550, commercial $476,687, other $73,812).
- Warehouse funding facilities: current $466,942 + non-current $897,941 = $1,364,883 (~$1.36bn, matches carry-forward).

**Band D — The parent's own commercial assets:**
- Cash and cash equivalents: $6,564,092 (2024: $8,075,247).
- Investments in short-term debt securities: $517,777; long-term debt securities: $188,887.
- Bitcoin investment: $777,515 (2024: $792,282).
- Goodwill: $11,849,018; acquired intangibles, net: $1,281,670.
- Deferred tax assets: $1,302,776 (2024: $1,800,994 — the decline reflects utilisation of the 2024 recognised DTAs).
- Property and equipment, net: $323,375; operating lease ROU assets: $214,929.

**Genuine leverage and returns (ANALYTICAL INFERENCE):** Strip Band A. Real corporate financing is $7.29bn of notes + $1.36bn warehouse = ~$8.65bn against ~$22.17bn equity — ~0.39x. Net of $6.56bn cash + ~$0.71bn securities, **net debt is roughly $1.4bn — Block is barely levered on a corporate basis.** Reported total-liability-to-equity of 0.78x wildly overstates true gearing because ~$6.8bn of "liabilities" is customer money. The correct read: Block is an equity-funded technology company with a small, ring-fenced bank bolted on — a reading corroborated by Fitch's BBB– investment-grade rating (May 2025, affirmed Q3 2025).

### IX.2 Funding the Loan Book

The nine-fold jump is a *classification* event, not a *financing* event. Historically, Square Loans were majority-sold to third-party investors, and Cash App Borrow / Afterpay Post-Purchase loans were originated through an external partner bank and held for sale. From Q2 2025 SFS began originating Cash App Borrow and Afterpay Post-Purchase directly; **from 1 July 2025 essentially all these products, plus loans purchased back from the partner, are retained on balance sheet as held-for-investment.** Cash App Borrow had nearly $9bn of originations in 2024 (via the external partner) with historic loss rates of less than 3% and about 5 million active users; since bringing origination in-house through SFS in March 2025, Borrow originated more than $27bn in loans in the five quarters to Q1 2026, with Q1 2026 risk loss rates of 3.16% for new customers, 3.01% for 7–12-month customers, and 2.67% for customers on platform more than 13 months (per CFO Amrita Ahuja).

Funding sources, in order of magnitude: (1) the parent's own equity and cash — the dominant source; (2) $1.36bn of warehouse facilities with third-party lenders, secured by the loans; (3) SFS's ~$420m deposit base — trivial against a $3.38bn book. There is a whole-loan sale channel (majority of Square Loans still sold to investors) but no public securitisation programme.

**Blended cost of funds vs yield (ANALYTICAL INFERENCE):** With warehouse and note coupons in the 5.6%–6.5% range but most funding being zero-explicit-cost equity, Block's blended funding cost is low; against Cash App Borrow's fee structure (short-duration, high effective APR) and Square Loans, the retained book earns a wide spread — which is precisely why management moved to retain it.

**Direction of travel vs Klarna:** Where the Klarna study found a company moving *toward* originate-to-distribute (selling risk off), **Block is unambiguously moving toward retention** — building an on-balance-sheet credit book to capture spread and recurring revenue, using its own equity as the funding cushion. This is the single biggest capital-allocation shift in the FY2025 accounts.

### IX.3 Capital Structure and Its History

- **2015 IPO** (as Square) at $9/share.
- **Convertible notes:** multiple issues; by end-2025 two remain — 2026 Convertibles $575m and 2027 Convertibles $575m (0.25% coupon on the 2027s). Both are hedged with convertible-note-hedge/warrant structures lifting effective conversion prices from ~$299.13 to ~$368.16 (2026) and ~$414.18 (2027), reducing dilution. Earlier 2025/2026 convertibles were largely retired at or before maturity.
- **Senior notes:** $1.0bn 2026 and $1.0bn 2031; $2.0bn 6.50% due 2032 (May 2024, upsized from $1.5bn); $1.2bn 5.625% due 2030 + $1.0bn 6.000% due 2033 (August 2025, upsized from $1.5bn to $2.2bn, settled 18 Aug 2025).
- **Revolving credit facility:** restated January 2026, increased from $775m to $900m, matures 14 January 2031; no borrowings or letters of credit outstanding as of 14 January 2026.
- **Afterpay equity:** 113,617,352 Class A shares, $13,827,929k (~$13.84bn total consideration).
- **"$0 long-term debt" — RESOLVED:** false. Net carrying $7,289,018k of Notes.
- **Maturity profile:** near-term wall in 2026 ($1.0bn senior + $575m convertible), manageable given $6.56bn cash. **Cost of capital (ANALYTICAL INFERENCE):** blended coupon rising as low-coupon converts are replaced by 5.6%–6.5% senior notes; the Fitch BBB– rating (May 2025, affirmed Q3 2025) lowers Block's marginal cost of debt going forward.

### IX.4 The Bitcoin Position as Capital Allocation

- **Holding:** 8,883 investment BTC (31 Dec 2025), cost basis $292.6m, fair value $777,515k; +398 BTC added in 2025 for $41.1m. Plus ~238 operational BTC (~$20m) to facilitate Cash App transactions. By Q1 2026 the holding was ~9,032 BTC (~$724m).
- **Accounting:** Block early-adopted ASU 2023-08 in Q4 2023 (modified-retrospective, cumulative-effect adjustment to opening retained earnings). Bitcoin is now marked to fair value each reporting date with gains/losses in net income — below operating income, as an investment.
- **Earnings volatility:** FY2024 +$421m gain (incl. +$252m in Q4); FY2025 −$56m net (−$93m, +$212m, +$60m, −$234m by quarter); Q1 2026 −$173m. This single ~$778m asset can swing quarterly GAAP net income by $200m+.
- **Which entity:** the consolidated parent — deliberately quarantined *outside* every regulated ring-fence (Volume I), so a bitcoin drawdown cannot impair SFS's regulatory capital.

**Judgement as allocation:** In dollar terms the bet has worked — ~$220m of 2020–21 purchases (avg cost basis ~$32,939/BTC per BitcoinTreasuries) is worth ~$777m, a large multiple. But three disciplines cut against it: (1) **materiality** — at ~0.35% of assets and ~3.5% of equity it is too small to move enterprise value yet large enough to pollute earnings quality; (2) **opportunity cost** — the same ~$292m cost basis deployed into buybacks in 2020–21 would plausibly have returned similarly, and into the loan book would have compounded at the lending spread with far less earnings noise; (3) **signalling** — holding a volatile asset above an insured bank invites regulatory and covenant scrutiny disproportionate to the sum involved. **Verdict: founder conviction that happened to pay, not a repeatable capital-allocation framework.** It is defensible only because it is small and quarantined.

**Proto and Bitkey:** part of the new "Bitcoin Ecosystem" revenue category (FY2025 re-cut). Proto's 3nm mining-chip programme began Oct 2021 (5nm prototype early 2023); its flagship Core Scientific deal (15 EH/s) collapsed with Core booking a $41.9m loss to cancel the contract and all future equipment deliveries as it pivoted to AI hosting — although Core had by then paid Block/Proto $67.9m in total for chips. Q4 2025 Bitcoin-ecosystem gross profit rose ~10% YoY, partly on Proto hardware shipments. Bitkey is a self-custody wallet. **Verdict: these are R&D-stage capital commitments with no demonstrated return; the lost anchor customer makes Proto the weakest link in the bitcoin thesis.**

### IX.5 Goodwill, Intangibles and the Afterpay Verdict

- **Total goodwill:** $11,966,761 (2022) → $11,919,720 (2023) → $11,417,422 (2024) → $11,849,018 (2025); acquired intangibles, net $1,281,670 (2025). The 2025 rise was foreign-currency translation (+$431,596k), not new acquisitions.
- **Afterpay goodwill $11,719,494k**, allocated 50/50 to the Square and Cash App reporting units; total consideration $13,836,622k (all equity plus $8,693k cash for tax withholding; an additional $66,337k of share value was expensed as post-combination compensation).
- **Impairments to date: only TIDAL** — $132m (Q4 2023) + $73.5m (Q4 2024), essentially writing off TIDAL's ~$197.9m goodwill; TIDAL fair value was estimated via cost and income approaches. The FY2025 annual test (31 Dec 2025) explicitly "concluded no goodwill impairment should be recognized."
- **Afterpay has never been impaired — but cannot be tested alone.** Because its goodwill was split into two large, healthy units (each received ~$5.84bn at Q1 2022), its performance is masked by Square and Cash App. "Never impaired" therefore does not mean "value-creating."
- **BNPL contribution (gross profit):** quarterly run-rate ~$237m (Q1 2025), ~$220–242m (2024 quarters), rising to ~$299m (Q3 2025); BNPL GMV $7.89bn (Q1 2025) → $9.70bn (Q3 2025); cumulative consumer spend through Afterpay ~$72bn since acquisition.

**Afterpay verdict: TOO EARLY TO JUDGE, LEANING VALUE-DESTRUCTIVE ON PRICE.** Block paid $13.84bn (down from ~$29bn announced only because its own stock fell) for a business now generating on the order of $1bn of annual gross profit growing ~20%. On a gross-profit multiple that is not obviously cheap, and the integration was described by former staff as troubled (Volume VIII). The strongest defence is that Afterpay is now the credit rail inside Cash App Card — strategically embedded rather than standalone. The honest scorekeeper — a standalone impairment test — has been structurally foreclosed by the 50/50 allocation.

### IX.6 Capital-Allocation Scorecard
- **2015 IPO** — strategically necessary. VALUE-CREATING.
- **Convertible issuances (low-coupon, hedged)** — cheap capital, dilution managed. VALUE-CREATING.
- **Senior notes 2024–25 (5.6%–6.5%)** — prudent term funding for the retained loan book. STRATEGICALLY NECESSARY.
- **Caviar** (bought ~$90m, sold to DoorDash 2019 ~$410m) — VALUE-CREATING.
- **Weebly, Credit Karma Tax** — small, integrated. NEUTRAL/POSITIVE.
- **TIDAL** (~$237m, goodwill written off) — VALUE-DESTROYING.
- **Afterpay** ($13.84bn) — QUESTIONABLE / TOO EARLY.
- **Bitcoin (~$292m cost)** — QUESTIONABLE (worked, but not framework-driven).
- **Proto/Bitkey** — TOO EARLY, trending negative (Core Scientific exit).
- **Buybacks ($2.3bn FY2025)** — sensible given undervaluation and net-cash balance sheet, but partly offset share-based-compensation dilution ($1,215.5m SBC, Volume VIII).
- **No dividend** — appropriate for the growth/net-cash profile.
- **Net share count:** Class A 542,085k at end-2025 down from 559,606k at end-2024 (Class B ~60,070k → 59,993k); by 20 Feb 2026, 539,103k Class A + 59,993k Class B (CONFIRMED, 10-K cover) — buybacks are shrinking the count net of SBC.

### IX.7 Returns on Capital (normalised)
- **ROE FY2025:** $1,306m / ~$21.7bn avg equity ≈ **~6.0%** (ANALYTICAL INFERENCE).
- **ROE FY2024 reported** ~13.5%, but **normalised** (strip $1.9bn tax benefit and $421m bitcoin gain) ≈ **~2–4%** — worse than 2025. The apparent decline in headline net income masks an underlying *improvement* in operating quality (operating income +91% to $1,708.4m).
- **Return on tangible equity FY2025:** $1,306m / ~$9.0bn tangible equity ≈ **~14.5%** — the gap between ROE and ROTE is entirely the $11.85bn goodwill mountain, most of it Afterpay.
- **ROIC excluding customer funds (ANALYTICAL INFERENCE):** NOPAT ~$1.28bn (operating income less ~25% tax) / (~$22.2bn equity + $7.3bn debt) ≈ **~4.3%** — below any reasonable cost of capital, dragged down by goodwill. On tangible invested capital the figure is materially higher, which is the crux: **Block earns acceptable returns on the capital genuinely at work and poor returns on the capital sunk into Afterpay goodwill.** Management's Investor Day targets (gross profit ~$11.98bn in 2026 and ~$15.8bn by 2028, adjusted operating income $4.6bn by 2028) are COMPANY CLAIMS / forward-looking projections, not results.

### IX.8 Capital Adequacy, Liquidity and Stress
- **Liquidity:** ~$9.2bn total (cash $6.56bn + securities + undrawn $900m revolver). Buyback capacity ~$6.1bn remaining is discretionary and pausable.
- **Claims on liquidity:** restructuring ~$852m (Q1 2026 recorded $495.3m); DOJ reserve $240m (accrued Q1 2026, disclosed as potentially exceedable and material); ~$340m of 2025–26 enforcement penalties (Volume VIII); loan-book growth; the 2026 debt wall (~$1.6bn).
- **SFS regulatory capital:** must hold ≥20% leverage ratio — roughly 4x a normal bank's requirement, so SFS is capital-heavy by design and cannot be levered up to fund group lending.
- **Stress model (loss rate doubles AND bitcoin halves simultaneously):** doubling the FY2025 loss rate adds ~$1.34bn pre-tax to the $1,337.2m already booked; bitcoin halving from $777.5m costs ~$389m. Combined ~$1.7bn pre-tax hit — roughly one year's operating income, absorbable against $22.2bn equity and $9.2bn liquidity, and **the bitcoin leg cannot touch SFS because it is quarantined at the parent.** Block survives comfortably; earnings, not solvency, take the blow.

### IX.9 The Transplant Verdicts (Nigeria — CBN Financial Holding Company framework)

- **Holding customer funds / safeguarding architecture — ADAPT.** Block's float model works because US money-transmitter law and FDIC-adjacent safeguarding are mature. In Nigeria the reader must safeguard e-money/customer balances under CBN rules (segregated trust accounts, no commingling). The silent US institutional feature is deep, liquid, highly rated short-term securities to invest float in; Nigeria's shallower T-bill/OMO market means float income is real but concentration risk is higher. Build segregated safeguarding from day one; do not treat float as free capital.
- **Funding a loan book from deposits inside a licensed subsidiary — ADAPT (via microfinance-bank licence, per Volume V).** Capital arithmetic: under the FHC rule the holdco needs paid-in capital ≥20% above the sum of subsidiary minimums, and a microfinance bank carries its own minimum capital and prudential ratios. **Rule of thumb for the reader: budget roughly ₦1 of the subsidiary's own regulatory capital for every ~₦5–8 of retained lending** (mirroring SFS's ~20% leverage cage, which is stricter than a normal bank precisely because regulators distrust commercial parents owning banks). Do NOT assume the deposit base will fund the book — it won't, just as SFS's $420m doesn't fund Block's $3.38bn.
- **Warehouse and forward-flow funding — REJECT (Volume II: no deep Nigerian market).** Block's warehouses work because US institutional credit buyers and forward-flow counterparties exist. Nigeria lacks them. The reader must instead fund credit from the licensed subsidiary's own capital and deposits, keep the book small relative to capital, and price for the absence of a distribution channel — meaning slower, capital-disciplined growth, not the 9x jump Block executed.
- **Holding a volatile treasury asset at the parent — REJECT (Volume I), and here is the constructive half:** the CBN draft revised guidelines *bar* a financial holding company from owning businesses outside financial services, and the ring-fencing rule means excess capital in one subsidiary cannot plug another's deficit. So the reader legally cannot do what Block does. **What to do with surplus capital instead, in priority order:** (1) hold the mandated ≥20% capital buffer above aggregate subsidiary minimums as genuine, liquid, unencumbered capital — this is not idle, it is the licence to operate; (2) down-stream capital into the credit subsidiary to expand lending at the regulated leverage ceiling, where each naira compounds at the lending spread; (3) build a liquidity reserve in Nigerian government securities to back customer-fund safeguarding and withstand deposit runs; (4) invest in the proprietary core-banking platform and compliance/AML infrastructure — the highest-return "capex" for a regulated group, as Block's own ~$340m of penalties and $240m DOJ reserve show. Surplus capital in a capital-constrained FHC is a *strategic buffer and a lending multiplier*, never a speculative position.
- **Growth by acquisition — REJECT as a default; ADAPT narrowly.** Block's record is uneven at best (Caviar good, TIDAL written off, Afterpay unprovable-and-probably-overpaid). A capital-constrained founder should **build, not buy**, unless an acquisition delivers a *licence*, a *deposit base*, or a *regulated capability* that would take years to build organically — and even then only for cash-and-carry consideration the balance sheet can absorb, never Block-style all-stock deals whose price collapses with the buyer's own multiple (Afterpay's value fell from ~$29bn to $13.84bn between announcement and close for exactly this reason).
- **Share repurchases and equity compensation — REJECT for the cooperative core; ADAPT for any holdco equity.** A cooperative's members are owners of a different kind (patronage, not tradable equity), so buybacks are meaningless and equity comp misaligns with mutual ownership. If the holdco has outside equity investors, modest option pools may be justified, but the reader should avoid Block's ~11.7%-of-gross-profit SBC burn, which quietly offsets its buybacks and would be indefensible in a capital-constrained mutual.

### IX.10 Volume IX Reconstruction (answers)
- **What funds this business?** Equity (~$22.2bn) first; $7.29bn of notes second; warehouse facilities and a tiny deposit base at the margin. Customer money ($6.8bn payable) funds nothing for shareholders — it is a pass-through liability.
- **Most misunderstood balance-sheet item:** customers payable / customer funds — treating them as leverage misreads the whole company.
- **How much capital does growth actually require?** More than it looks: retaining the loan book converts an off-balance-sheet, capital-light model into a capital-hungry one. Each dollar of retained lending needs equity backing (and, at SFS, a punitive 20% leverage cage).
- **What has bitcoin cost or earned?** Earned, on paper: ~$220–293m cost basis now worth ~$724–778m. Cost: earnings-quality volatility of $200m+ a quarter and regulatory optics.
- **Was Afterpay worth it?** Unproven and probably overpaid; the never-impaired goodwill is an artifact of the 50/50 allocation, not evidence of value creation.
- **The central question:** Block's capital allocation is **the work of a founder with unusual latitude (dual-class control) more than a disciplined operator** — bitcoin, Proto, TIDAL and the all-stock Afterpay deal all bear the marks of conviction over discipline; the recent turn to buybacks, term-debt funding, an investment-grade rating and loan-book retention shows a maturing, more disciplined treasury underneath. **What a capital-constrained founder should take from it:** copy the safeguarding rigour, the licence-based bank, and the recent funding discipline; reject the volatile treasury asset (you are legally barred anyway), the acquisition-led growth, and the equity-comp/buyback machinery; and hold surplus capital as a regulated buffer and a lending multiplier, not as a bet.

**Ten most important conclusions:**
1. "$0 long-term debt" is false — Block carries $7,289,018k of notes across seven series.
2. ~$6.8bn of reported liabilities is customer money; true corporate net debt is ~$1.4bn.
3. The loan book's 9x jump was a July-2025 reclassification to held-for-investment, not new financing.
4. SFS ($420m deposits) does not fund the $3.38bn book — the parent's equity does.
5. Bitcoin ($778m) is quarantined at the parent and cannot impair the bank, but pollutes earnings by $200m+ a quarter.
6. Afterpay's $11.72bn goodwill has never been impaired only because it was split 50/50 and can't be tested alone.
7. Only TIDAL goodwill has been impaired ($132m + $73.5m).
8. FY2024 net income was inflated ~$1.9bn by one-time tax benefits — normalise any 2024-spanning ratio.
9. Proto's anchor deal collapsed (Core Scientific $41.9m loss to exit); Proto is the weakest bitcoin bet.
10. Block is barely levered, investment-grade (Fitch BBB–), and buying back stock — a maturing treasury under a founder-driven strategy.

---

## Recommendations (for the Nigerian founder)
1. **Now — safeguard first.** Stand up segregated customer-fund accounts and invest float only in Nigerian government securities; treat float as a liability, never as capital. Benchmark that would change this: a CBN safeguarding rule permitting bank-deposit safeguarding at scale.
2. **Now — size the capital stack to the FHC rule.** Compute paid-in capital as ≥20% above the *sum* of every subsidiary's minimum, and hold it liquid and unencumbered. Do not rely on cross-subsidiary support — it is prohibited.
3. **Stage 1 — build the microfinance-bank subsidiary and lend from its own capital + deposits.** Cap retained lending at roughly 5–8x the subsidiary's regulatory capital. Threshold to accelerate: a durable deposit franchise and demonstrated sub-3% loss rates (Block's Cash App Borrow benchmark).
4. **Stage 2 — reinvest surplus into the platform, compliance, and the lending multiplier, in that order.** Do not acquire unless buying a licence/deposit base for cash. Threshold that would justify an acquisition: a target whose regulated capability would take >3 years to build organically.
5. **Never — no volatile treasury asset, no buybacks, no heavy equity comp.** These are barred, meaningless, or misaligned for a cooperative FHC.

## Caveats
- **Basis/vintage:** all balance-sheet figures are FY2025 10-K (filed 26 Feb 2026, 31 Dec 2025) unless stated; the segment series was re-cut twice (BNPL into Cash App from Q4 2023; the FY2025 Commerce Enablement / Financial Solutions / Bitcoin Ecosystem revenue re-cut). Any 2024-spanning return metric is normalised for the ~$1.9bn one-time tax benefit.
- **SFS figures** are FDIC call-report data via third-party aggregators (Visbanking, BestCashCow, Weiss) at 30 Sept 2025; the exact 31 Dec 2025 call report was not obtained and figures move materially quarter to quarter — **UNKNOWN** at year-end precision.
- **Afterpay intangible useful lives** by class and the standalone net-intangibles line by year were not isolated from the primary filings — **partial UNKNOWN**.
- **Warehouse-facility lenders and terms** are disclosed only in aggregate; individual counterparties and forward-flow buyers are **UNKNOWN** from public filings.
- **Blended cost of funds vs book yield, ROE/ROTE/ROIC and stress outputs** are ANALYTICAL INFERENCES built on disclosed inputs, not company-reported figures.
- **2026/2028 outlook figures** are COMPANY CLAIMS / forward-looking projections from the 19 Nov 2025 Investor Day, not results.
- **Nigeria FHC parameters** (51% minimum stake; 20%-above-subsidiary-minimum capital; ring-fencing; draft bar on non-financial businesses) are as stated in the brief and should be re-verified against the current CBN guideline text before action.

---

# VOLUME X — Management, Culture & Governance

## Block, Inc. (NYSE: XYZ, formerly Square, Inc.)

## TL;DR
- **Block is a founder's vehicle with governance attached, not a well-governed company with an unusual founder.** Jack Dorsey holds roughly 42.2% of voting power on a high-single-digit economic stake, takes a $2.75 salary, and both the failures (TIDAL, TBD, Proto) and the recovery (the 2024 functional reorganisation) trace to his personal conviction. The board has never visibly overruled him; the one committee that reviewed a founder pet project approved what Chancellor Kathaleen McCormick called, "by all accounts, a terrible business decision."
- **The credibility verdict is bifurcated: trust the audited numbers, discount the narrative.** Block's GAAP financials have proved reliable (gross profit $7.505bn in 2023 → $8.889bn in 2024 → $10.36bn in 2025), but its operational and strategic narrative — the AI-driven layoff framing, Proto's "strong product market fit," the "prioritising the United States" abandonment language, and the pre-2023 Cash App user metrics — has repeatedly required correction. An analyst should price the management narrative as promotional and verify it against filings.
- **For the Nigerian reader the transplant lesson is inverted: build the discipline Block could always override.** Because a cooperative runs one-member-one-vote and the founder cannot insulate himself, the reader must institutionalise an operator-veto, an independent risk function with a hard stop over launches, and a genuinely independent licensed-entity board — precisely the disciplines Square Financial Services already carries under FDIC mandate and the Block parent chose to skip.

## Key Findings

1. **Dorsey's control is structural and durable.** Class B shares carry ten votes each; Volume I established Dorsey holds roughly 1 million Class A and about 47.8 million Class B shares (79.8% of all Class B), giving approximately 42.2% of total voting power. Together with co-founder Jim McKelvey, insiders have controlled over 48% of the vote on under 11% of the equity. The dual-class structure sunsets only when Class B falls below 5% of combined voting power — a distant, behaviour-dependent trigger with no calendar date.

2. **The board is ten members, six independent, staggered into three classes.** As of the 2026 proxy: Dorsey (Block Head & Chairperson), Jim McKelvey, Shawn Carter (Jay-Z) and Anthony Eisen are non-independent; Roelof Botha (Lead Independent Director, Sequoia Capital), Amy Brooks (NBA), Randall Garutti (ex-Shake Shack CEO), Mary Meeker (Bond Capital), Paul Deighton and Neha Narula are independent. All three committees — audit and risk, compensation, nominating and corporate governance — are 100% independent; Mary Meeker chairs compensation. Amrita Ahuja, though COO/CFO, is not a main-board director.

3. **No independent director has ever visibly constrained the founder.** The TIDAL transaction committee — reviewing a deal Dorsey conceived while summering with Jay-Z in the Hamptons — learned that TIDAL was failing financially, losing its major contracts, and under criminal investigation, that Carter had personally loaned it $50m, and that Dorsey was the sole management member supporting it, yet approved the acquisition anyway.

4. **Executive power is concentrated in two people.** Below Dorsey, Amrita Ahuja simultaneously holds COO, CFO, Treasurer and "Foundational Lead" titles — overseeing finance, legal, people, policy and communications — and chairs the Square Financial Services bank board. The September 2024 reorganisation dissolved the two-CEO model into functional leads.

5. **The management narrative shows a documented correction pattern** across four incidents that must be assessed as a whole (detailed below): the February 2026 AI-attributed layoffs, Proto's "product market fit" claim, the Hindenburg/Cash App episode, and the abandonment framing Volume XIII flagged.

6. **A materially stricter governance regime already operates inside the group.** Square Financial Services, the Utah-chartered industrial bank, is required by the FDIC to maintain a majority-independent board with parent representation capped at 25%, backed by a Capital and Liquidity Maintenance Agreement and a Parent Company Agreement binding Dorsey personally.

7. **Dual-class collapse proposals failed but drew rising non-insider support.** NorthStar's one-share-one-vote proposal went to a vote twice — 2021 (~19.8% for) and 2022 (~27.9% for) — with ISS recommending FOR in 2022. It has not appeared since; the 2026 ballot instead carried a shareholder proposal for a board-level technology committee, which the board opposed.

## Details

### X.1 Jack Dorsey — decision rights and revealed priorities
Dorsey co-founded Square with Jim McKelvey in 2009 and served as CEO of both Square and Twitter simultaneously from mid-2015 until his November 2021 Twitter departure. That divided-attention period coincided with Block's over-hiring and the two-silo structural error Dorsey later admitted on X: "over-hired during covid because i incorrectly built 2 separate company structures (square & cash app) rather than 1, which we corrected mid 2024." His title is "Block Head"; his cash salary is $2.75; at his own request he receives no equity or bonus.

His revealed priorities skew to conviction bets and open protocols. Since leaving Bluesky's board in 2024 he has directed personal energy to Nostr-based projects — Bitchat (a Bluetooth mesh messenger China ordered pulled from Apple's App Store), the andOtherStuff nonprofit (into which he committed $10m), and Block's own Bitcoin initiatives (Proto mining hardware, the Bitkey wallet). He has publicly predicted Bitcoin will reach $1m by 2030. His communication style is X-first: the 4,000-person layoff was announced through an X post, and Block sourced Q2 2026 earnings-call questions directly from X. In March 2026 he and Botha published "From Hierarchy to Intelligence," a manifesto for an AI-mediated near-flat organisation of roughly 6,000 with only three human roles — individual contributors, Directly Responsible Individuals (DRIs), and player-coaches — and no permanent middle-management layer. Dorsey told Sequoia's "Long Strange Trip" podcast his ideal is all ~6,000 employees reporting directly to him through an "intelligence layer," an idea he conceded is "ridiculous" under a traditional hierarchy. His outside commitments (Nostr, Bitchat, andOtherStuff) are live and material, which is directly relevant to key-person risk.

### X.2 The Executive Team and Its Turnover
Current senior leadership (functional leads, post-September 2024): **Amrita Ahuja** (Foundational Lead / COO / CFO / Treasurer); **Brian Grassadonia** (Ecosystem Lead); **Owen Jennings** (Business Lead, formerly Cash App COO); **Nick Molnar** (Sales & Marketing Lead, Afterpay co-founder); **Thomas Templeton** (Hardware Lead, founded Proto); **Brian Boates** (Risk Lead, formerly SVP machine learning/data science at Cash App); **Chrysty Esperanza** (Counsel Lead); **Robert Andersen** (Principal Designer, employee no. 1); **Brooke Ellis** (Design Lead); **Arnaud Weber** (Engineering Lead since November 2025).

Turnover record: **Alyssa Henry** ran Square as CEO from February 2023, having joined in 2014 from Amazon and Microsoft; she departed effective October 2, 2023, characterising it on X as a retirement after "9+ years." It came days after a two-day Square outage the company said was unrelated, and Dorsey assumed the additional "Square Head" title. Volume VI records Henry's own account that Square and Cash App were "actually very siloed, different businesses with no connections or communication between the two." **Brian Grassadonia**, Cash App's co-creator and former CEO, moved to the cross-cutting Ecosystem Lead role in 2024. **Anthony Eisen** (Afterpay co-founder) co-led Afterpay until November 2024, consulted through the transition, then joined the board in February 2025. **Dhanji Prasanna**, former Technology + Engineering Lead, departed and was succeeded by Weber. The reorganisation eliminated general-manager roles across the company.

Leadership depth is thin and succession planning is not visibly disclosed. Key-person risk is doubly concentrated in Dorsey (strategy, capital, identity) and Ahuja (finance, legal, people, and bank-board chair); the flat-organisation ambition arguably deepens rather than mitigates it.

### X.3 The Management System
Formally, Block runs on functional leads reporting to Dorsey, with Ahuja's "Foundational" group — finance, legal, people, policy, communications — providing the connective tissue that lets functions "speak a common language." Ahuja frames the CFO/COO duality as the tension between "aspiration and discipline." Capital allocation in FY2025 (Volume IX): $2.3bn of buybacks, no dividend, share-based compensation of $1,215.5m (11.7% of gross profit), and the Bitcoin treasury quarantined at the parent. Conviction bets originate with Dorsey, and the record shows neither board nor executives reliably stop them before launch. The shared risk organisation reports to the CEO — a structure that did not prevent the Cash App anti-money-laundering and consumer-protection failures. In practice, power sits with Dorsey on strategy and identity and with Ahuja on execution and finance; there is little evidence of a genuine operator-veto over founder initiatives.

### X.4 Board and Governance Architecture
Ten directors, three staggered classes, six independent, with a Lead Independent Director (Botha, since June 2022). Committees are 100% independent. Governance features include a prohibition on hedging and pledging, clawback policies for Section 16 officers and change-of-control severance, and stock-ownership guidelines. The board opposed the 2026 shareholder proposal for a board-level technology committee, citing existing integrated risk oversight by the full board and the audit and risk committee.

The instructive contrast is **Square Financial Services**. As a condition of FDIC deposit insurance, the industrial bank must maintain a board with a majority of members independent of Block and its affiliates, with parent representation capped at 25%; Dorsey and Block are personally bound by a Capital and Liquidity Maintenance Agreement and a Parent Company Agreement giving the FDIC examination and reporting rights. Ahuja chairs the bank board; Lewis Goodwin is CEO and Brandon Soto CFO. This is a materially stricter regime than the parent's — a licensed entity forced into disciplines the unlicensed parent declined to adopt voluntarily.

Shareholder-proposal record: NorthStar's dual-class collapse proposal ("Change in Stockholder Voting") drew, per Block's Form 8-K Item 5.07 filings, 171,197,461 for vs 694,034,716 against in 2021 (~19.8% of for/against votes) and 260,042,860 for vs 670,888,261 against in 2022 (~27.9%). ISS recommended FOR in 2022, calling the sunset rationale "dubious" and noting a collapse would make Block eligible for the S&P 500. Both figures are heavily suppressed by Dorsey and McKelvey's supervoting shares; a Block-specific non-affiliated support figure is UNKNOWN. The proposal has not returned since 2022. Say-on-pay drew approximately 97% support in 2025.

### X.5 Compensation and Incentives
Dorsey draws a $2.75 salary with no equity and no bonus — but the $2.75 is not the absence of compensation; his incentive is his multibillion-dollar equity stake, making his alignment purely equity-value-based. Ahuja received roughly $15.4m total for FY2024 and about $12.3m for FY2025 (base ~$591k, the balance equity); Grassadonia about $6.46m for FY2025; new Engineering Lead Weber about $22.25m for FY2025, weighted to new-hire equity. Beginning in 2026, Block will introduce an annual cash-incentive bonus for named executive officers with payouts based on company-wide gross-profit and operating-income targets — the first explicit link between pay and gross profit. The system rewards equity-value creation and, newly, gross-profit/operating-income growth; it has not historically rewarded risk-and-compliance outcomes, which is consistent with the enforcement record.

### X.6 Declared versus Revealed Culture — the credibility verdict
Block's declared purpose is "economic empowerment." Tested against behaviour, the four correction incidents form a pattern:

- **The AI headcount attribution.** Dorsey attributed the February 2026 cut of ~4,000 employees (from over 10,000 to under 6,000) to AI. Mizuho Americas analyst Dan Dolev told the Wall Street Journal "the vast majority of these cuts were probably not due to AI"; a former Block employee, Jason Karsh, called it "organizational bloat wearing an AI costume." NBER Working Paper No. 34836 ("Firm Data on AI," February 2026), surveying roughly 6,000 C-suite executives across the US, UK, Germany and Australia, found about 90% reported AI had no effect on employment and 89% no productivity change over the prior three years. Volume VI's verdict — substantially overstated, principally a multi-year over-hiring correction — holds.
- **The Proto claim.** Block's early-2025 shareholder letter described its Bitcoin-mining hardware as having "strong product market fit and a healthy pipeline of demand," and Dorsey said on the Q2 2025 call, "we're gonna have some really happy customers." Per Core Scientific's Q2 2026 regulatory filing, it "entered into a termination and settlement agreement with Block, Inc. and Proto Global LLC to terminate our existing contract and all future delivery obligations of mining equipment thereunder, resulting in a loss of $41.9 million" — abandoning the July 2024 deal for roughly 15 EH/s of 3-nanometre chips, after paying Block $67.9m in total ($10m July 2024, $21.3m January 2025, $36.6m January 2026).
- **The Hindenburg episode (held in all three parts).** Hindenburg's March 2023 report alleged inflated Cash App metrics and lax controls. The SEC closed its inquiry in March 2025 without recommending enforcement. But real compliance failures were confirmed: the CFPB's January 16, 2025 order (Director Rohit Chopra) required a $55m penalty plus up to $120m in consumer redress ($175m total); 48 state regulators imposed an $80m BSA/AML penalty; and NYDFS (Superintendent Adrienne Harris, April 2025) added a separate $40m penalty, identifying 169,000 unprocessed suspicious-activity reports. A securities class action (Gonsalves/O'Neill) survived motions to dismiss in January 2026 and remains live, and a $240m DOJ reserve is outstanding. The honest position holds all three: no SEC action, confirmed regulatory failures, live litigation.
- **The abandonment framing.** Volume XIII found "prioritising the United States" and "shifting resources to higher-return areas" concealed competitive defeat and non-monetisation.

**The settled position: audited financial disclosure is reliable; operational and strategic narrative is not.** An analyst should treat every management statement about strategy, productivity, "product market fit" and abandonment rationale as promotional COMPANY CLAIM requiring independent verification, while continuing to rely on the GAAP financials, which prior volumes have generally found sound. This is promotional exuberance systematically applied — not fraud in the audited numbers, but a narrative that consistently overstates and reframes. That distinction is priceable: discount the story, trust the ledger.

### X.7 The dual-class verdict
What founder control bought: long-horizon patience that turned Cash App from an IPO "footnote" into a $6.34bn-gross-profit business (+21% in 2025); resistance to short-term pressure; and the ability to pivot the company's identity from Square to Block and into Bitcoin. What it cost: the TIDAL transaction — announced at roughly $306m, ultimately $237.3m for an 86.23% stake, of which Block later wrote off $132.3m — approved through a minimal process with no effective independent check; the two-ecosystem structural error that drove the over-hiring; and the Proto and TBD conviction bets Volume XIII catalogued. Chancellor McCormick's full formulation is the governance epitaph: "It seemed, by all accounts, a terrible business decision… a board comprised of a majority of disinterested and independent directors is free to make a terrible business decision without any meaningful threat of liability, so long as the directors approve the action in good faith."

**Verdict for Block specifically: net negative as currently configured.** The same unchecked conviction that built Cash App also produced TIDAL, TBD, Proto and the compliance failures — and the merchant core (Square, $3.94bn gross profit, +9% in 2025), which has essentially no abandonment record, did not require dual-class control to succeed. The calculus would change if the structure carried a time-based sunset, an enhanced-independence process for founder-conflicted transactions (a true special committee with veto power and the will to use it), or a genuine operator-veto. It has none of these; it has a 5%-of-voting-power sunset that may never trigger.

### X.8 Transplant verdicts (Nigerian cooperative context)
- **Founder control without dual-class insulation — ADAPT.** The reader cannot replicate ten-vote shares in a one-member-one-vote cooperative and should not want to. Permanent founder ownership belongs in the *platform-vendor entity* the founder owns, not in the cooperative. Substitute instruments: long-term vendor/licensing contracts, founder-reserved seats on the vendor company's board, and supermajority protections in the vendor entity — never member disenfranchisement in the cooperative. *Guinnane test: dual-class worked for Block because of the surrounding US capital-market environment that priced and tolerated it; that environment does not exist in a Nigerian cooperative, so the mechanism must be re-engineered, not copied.*
- **The operator-veto discipline — ADOPT.** Institutionalise what Block lacked: a written rule that no new product, acquisition or capital commitment above a defined threshold proceeds without documented sign-off from an operator/risk officer empowered to say no, recorded in board minutes. Because the founder cannot override members, this becomes an engineered strength rather than a limitation.
- **Concentrating COO and CFO in one person — REJECT for a capital-constrained founder.** Block can absorb the key-person risk; a Nigerian start-up cannot. Keep finance oversight structurally separate from operational execution to preserve an internal check and reduce single-point failure.
- **Risk leadership reporting to the CEO — REJECT as insufficient.** Block's risk-to-CEO line did not prevent systemic AML failure. The reader must build an independent risk/compliance function reporting to the board (or a board risk committee), with a direct line to the Central Bank of Nigeria relationship — the Square Financial Services model, not the Block-parent model.
- **Communicating through the founder's personal channels — REJECT for the licensed entity.** X-first, founder-voice disclosure is a regulatory hazard for a CBN-licensed entity; all material communications must run through controlled corporate channels with compliance review. Founder personal channels may carry vision, never regulated disclosure.
- **Promotional framing of operational results — REJECT; adopt conservative disclosure.** Cooperative members and the CBN will read "strong product market fit"–style language as a red flag, not a selling point. The reader should adopt understated, verifiable reporting; credibility with members and the regulator is the scarce asset, and it compounds.

### X.9 Reconstruction — the central question answered
- **Who decides?** Dorsey on strategy, identity and capital direction; Ahuja on finance and execution. The board ratifies; it does not constrain.
- **Does the company do what it says?** In its audited numbers, yes. In its strategic and operational narrative, not reliably.
- **What does the structure cost and buy?** It bought Cash App and pivot optionality; it cost TIDAL, TBD, Proto, the two-silo error and a persistent governance discount. Net negative as configured.
- **What is the key-person risk?** Severe and doubly concentrated (Dorsey and Ahuja), and the flat-organisation vision increases it. If Dorsey's attention drifts again — his outside protocol projects are active — there is no evident succession bench.
- **Is Block a well-governed company with an unusual founder, or a founder's vehicle with governance attached?** The latter. The governance apparatus is real on paper — independent committees, a Lead Independent Director, clawbacks, ownership guidelines — but has never demonstrably checked the founder. The only genuinely binding independent governance in the group is the FDIC-imposed regime at the bank.
- **What should a founder with no such insulation take from it?** Engineer the discipline Block could always override. The absence of dual-class insulation is not a handicap but an advantage: it forces the institutional checks — independent board-level risk, an operator-veto, separated finance, controlled disclosure, and conservative narrative — that protect a licensed financial group and that Block's structure allowed it to skip.

## Recommendations
1. **Immediately separate the platform-vendor entity from the cooperative.** Put permanent founder ownership in the vendor company; govern the cooperative one-member-one-vote with arm's-length vendor contracts. *Threshold to revisit:* if members' economic dependence on the vendor exceeds ~50%, add an independent member-representative to the vendor board to police conflicts.
2. **Stand up an independent risk/compliance function before launch, reporting to the board, with a hard veto over product launches.** Model it explicitly on Square Financial Services' majority-independent oversight, not the Block parent. *Threshold:* any product touching customer funds or credit requires documented independent risk sign-off before release.
3. **Do not concentrate COO and CFO in one hire** until the group clears meaningful scale; keep a structural check between finance and operations.
4. **Route all regulated disclosure through controlled corporate channels with compliance review;** reserve founder personal channels for vision only.
5. **Adopt conservative, verifiable public reporting;** treat every superlative as a future liability with members and the CBN.
6. **Write the operator-veto and founder-conflict recusal rules into the constitution and board charter now,** while the founder still controls the drafting — the one moment dual-class founders squander. *Benchmark that would change the posture:* if the group later obtains a deposit-taking licence, upgrade to the full FDIC-style package (majority-independent licensed-entity board, capital-maintenance undertaking, regulator examination consent).

## Caveats
- Named-officer compensation figures for FY2024/FY2025 are drawn from third-party compilations of the proxy (salary.com, Bullfincher) rather than a line-by-line read of the summary compensation table; treat exact dollar figures as THIRD-PARTY ESTIMATE pending the primary table. Dorsey's Block equity value is an ANALYTICAL INFERENCE from his shareholdings and prevailing price, not a disclosed figure.
- The DOJ matter is unresolved; the $240m reserve is a company accrual and the ultimate loss "could be material" per Block's own filings. The securities class action (Gonsalves/O'Neill) survived motions to dismiss in January 2026 and remains live; no liability finding exists.
- Square Financial Services' full current board roster beyond Ahuja (chair), Goodwin (CEO) and Soto (CFO) is not enumerated in the public sources reviewed; the FDIC majority-independent requirement is CONFIRMED but the individual independent directors are UNKNOWN.
- The "42.2% voting power" figure is carried forward from Volume I and reflects a specific filing vintage; it drifts with share issuance and buybacks. No Block-specific "excluding insider shares" support figure for the NorthStar proposals could be located.
- Some 2026 commentary on Block's flat-organisation model (e.g., the "mini-AGI" and all-report-to-Dorsey framing) is stated by Dorsey as ambition, not accomplished fact, and is classified here as COMPANY CLAIM/HYPOTHESIS rather than achieved organisational reality.

---

# VOLUME XI — Competition, Moat & the "One Block" Question

## A Forensic Reverse-Engineering of Block, Inc. (NYSE: XYZ, formerly Square, Inc.)

## TL;DR
- **The verdict is negative, and it is the single most valuable finding in the study: Block's two ecosystems share infrastructure but do not compound at the customer level.** After a decade, near-unlimited capital and an Afterpay acquisition (announced August 2021 at ~$29bn, closing 31 January 2022 at a final consideration of ~$13.9bn after Block's share price fell) explicitly bought to be "the connector," Block has never once published a person-level figure for customers active on both Square and Cash App — and the confirmed absence of that metric, after years of asserting synergy, is itself the answer. The businesses **coexist on one-and-a-half machines; they do not compound into one network.**
- **Where the moats are real they are very real; where the "one Block" synergy is claimed it is largely unbuilt.** Square software stickiness (≈59% of Square gross profit, net revenue retention above 100%), Cash App network effects (a primary-banking active worth ~10x a peer-to-peer-only active), settlement-controlled self-liquidating lending, and the shared data/underwriting spine all score high. Claimed cross-ecosystem synergy scores lowest of the twelve moats. Shopify is the more dangerous long-term analogue and arguably executes the integrated-commerce model better on the merchant side.
- **For the Nigerian reader: build ONE moat first — the merchant/cooperative core with settlement-controlled credit — and treat cross-layer compounding as a bonus to be earned per product, never an architectural assumption.** The cooperative differs from Block in one decisive way (genuine shared member identity), but that difference only compounds if the joined graph is built and acted upon from day one; Block's failure was precisely that it never built the graph.

## Key Findings

1. **Shared infrastructure is real; a shared customer graph is not.** Block's FY2025 10-K (filed 26 February 2026) states the ecosystems "share common infrastructure for payments processing, risk management, identity, and data." That is genuine and produces real cost leverage. But the word "identity" masks the gap: there is a shared *technical* identity/risk layer, not a *joined consumer-and-seller customer graph that is acted upon.* Block has never disclosed a both-sides overlap metric in any filing, shareholder letter, or investor-day deck. This is the analytical heart of the volume.

2. **Afterpay, the testable bridge, has not bridged after four years.** Acquired for a final consideration of ~$13.9bn (Block's FY2022 10-K states the aggregate fair value of shares issued was $13.8bn; the headline ~$29bn was the August 2021 announcement value before Block's stock fell), its $11.72bn of goodwill split 50/50 across the two reporting units (Volume IX), Afterpay was explicitly positioned as "a connector between our Square and Cash App ecosystems." As of FY2025, Block discloses BNPL GMV ($9.70bn in Q3 2025) and BNPL gross profit ($299m in Q3 2025), but **no figure showing Square sellers and Cash App consumers transacting with each other via Afterpay.** The integration that shipped — Afterpay on the Cash App Card (pilot February 2025 in 20 states + DC; expanded February 2026; general availability June 2026) — connects Cash App consumers to *external* merchants, not to Square sellers. It deepened Cash App monetisation; it did not fuse the two networks.

3. **The economics keep diverging, not converging.** FY2025: Cash App gross profit $6.34bn (+21%), Square $3.94bn (+9%). Different growth, margin, capital intensity and cyclicality (Volume VIII). Two businesses under one logo behaving like two businesses.

4. **The company itself concluded the two-company structure failed.** Dorsey's admission (Volume X) — "over-hired during covid because i incorrectly built 2 separate company structures (square & cash app) rather than 1, which we corrected mid 2024" — is corroborated by the July 2024 functional reorganisation (disbanding business-unit reporting lines) and the February 2026 cut from more than 10,000 to fewer than 6,000 staff. Block fixed the *org-chart* duplication; it did not thereby create a *customer* network.

5. **Shopify is the cleaner execution of Block's own model on the merchant side.** Per Shopify's FY2025 10-K: GMV of $378.4bn (+29% year over year), total revenue $11.56bn (+31%), Merchant Solutions $8.804bn (76.2% of revenue, +35%), Shopify Payments at ~62% GMV penetration, and Shopify Capital originating ~$4bn in 2025 off real-time payment data — the same settlement-visibility lending mechanism Square pioneered, executed at larger merchant scale.

6. **Interchange, the load-bearing subsidy (Volume VII), faces live regulatory risk.** On 6 August 2025, Judge Daniel M. Traynor of the US District Court for the District of North Dakota (*Corner Post v. Board of Governors of the Federal Reserve System*) ruled the Court would "vacate Regulation II … because it is contrary to law and was promulgated in excess of the Board's authority" — vacatur stayed pending 8th Circuit appeal; separately, the Fed has proposed tightening the debit cap. Cash App's economics depend on the small-issuer interchange exemption via partner banks — structural today, but exposed to policy change.

## Details

### XI.1 The Competitive Universe

Block competes in no single market; it competes in the union of a merchant-services market and a consumer-fintech market that only Block and PayPal straddle simultaneously. Segmenting by how the customer actually solves the same problem:

- **Integrated POS + vertical software:** Toast, Lightspeed, SpotOn, TouchBistro. They win where the *workflow* (not the payment) is the product — restaurants, hospitality, specialised retail — and attack the highest-value slice of Square's seller base.
- **Payment platforms & acquirers:** Stripe (developer-first online), Adyen (enterprise omnichannel), Fiserv/Clover (bank-distributed SMB), Global Payments/Worldpay (traditional acquiring). They contest the payment rail beneath Square.
- **Commerce platforms with embedded financial services:** Shopify (Payments + Capital + Balance) and Amazon (Lending, Pay). Shopify is the closest structural analogue to Square's own model.
- **Consumer wallets & neobanks:** PayPal/Venmo/Braintree, Chime, Zelle (via Early Warning Services), Varo, Current, and incumbent banks. They contest Cash App.
- **BNPL:** Affirm, Klarna (a prior subject of this programme), PayPal Pay in 4, Sezzle. They contest Afterpay.
- **International & adjacent:** SumUp, Zettle (PayPal), and the Volume XII field.

### XI.2 Competitor Teardowns

**Shopify (deepest treatment — the cleanest test of Square's model).** Target: online-first and omnichannel merchants, from solo DTC to enterprise (Shopify Plus). Product: storefront + payments + capital + balance + shipping + markets. Pricing: subscription tiers ($29–$2,300+/mo) plus a merchant-solutions take; blended take rate ~2.33% on FY2025 GMV (per SEC-filing analysis normalising merchant-solutions revenue over GMV). Unit economics: FY2025 revenue $11.56bn (+31%), free cash flow ~$2.0bn (17% margin), Merchant Solutions 76.2% of revenue and growing faster (+35%) than Subscription (+17%). Capital model: Shopify Capital originated ~$4bn of loans/MCAs in 2025 (portfolio balance grew from $1.22bn to $1.78bn), turning over roughly quarterly, underwritten on real-time Shopify Payments flow — structurally identical to Square's self-liquidating loan. **Verdict: on the merchant side, Shopify executes the integrated commerce-plus-payments-plus-capital stack at larger GMV scale and higher growth than Square, and the volume is willing to say so.** Square's edge is physical/in-person commerce and the sub-$500k local seller; Shopify's edge is online, international and mid-market-plus. Shopify's weakness: no consumer network of its own (Shop Pay is a checkout accelerant, not a Cash App).

**Toast (the vertical specialist that took Square's premium restaurants).** FY2025: ARR crossed $2.0bn (+26%), ~164,000 locations (+30,000 net), first sustained GAAP profitability (Q4 net income $101m). Restaurant-only focus; ~24–24.5% of US POS by merchant count; NRR ~117%; GPV per location far above Square's blended base (Fiserv investor material implies ~$1,189k/location for Toast vs ~$53k for Square). Payments take rate is thin (~49bps) because Toast monetises software and fintech attach. Toast validates Volume III's finding that Square is #3 in small restaurants (~13% share) and loses the premium end to a specialist. Its moat is switching cost: re-training staff and re-integrating kitchen display, payroll and inventory imposes brutal cutover risk.

**Fiserv / Clover (the bank-distributed incumbent).** Clover FY2025 revenue ~$3.3bn (+23% including value-added services), ~910,000 merchants (up from ~700k at end-2023), annualised GPV ~$310–337bn, GPV per location ~$357k — well above Square's blended ~$53k because Clover is distributed through banks and ISOs to established businesses. Payments take rate ~76bps ex-VAS. Clover is the counter-model to Square's self-serve PayFac: it wins through distribution rather than viral self-onboarding, and it is larger in raw GPV. Its weakness is a fragmented, non-cohesive software experience versus Square's integrated design.

**PayPal / Venmo (the only true two-sided comparator).** FY2025: TPV $1.79tn (+7%), 439m active accounts, revenue $33.2bn (+4%), blended transaction take rate ~1.65%. Venmo: 67m monthly active accounts, revenue ~$1.7bn (+20%), TPV +13%, >100m total active accounts. PayPal is the instructive mirror: it too owns a merchant side (Braintree/PayPal checkout, 36m+ merchants) and a consumer side (Venmo) — and it too has struggled to make the two compound, with Venmo monetisation only now scaling. The parallel underlines that two-sided compounding is hard even for the incumbent that has had both sides longest.

**Chime (the consumer pure-play that isolates Cash App's interchange dependency).** FY2025 revenue ~$2.1–2.2bn (+~30%), 8.7m active members, ARPAM ~$251, gross margins above 85%, first GAAP-profitable quarter in Q1 2026. It priced its IPO at $27/share on 11 June 2025, raising $864m at an $11.6bn fully diluted valuation — less than half its $25bn peak private valuation — and closed its debut up 37% at $37.11. Chime's S-1 is explicit: "we have an asset-light, payments-driven revenue model … the substantial majority of our revenue through interchange-based fees … whenever Chime-branded debit and credit cards are used," exploiting the Durbin small-issuer exemption via Bancorp and Stride; its ChimeCore proprietary processor cuts cost-to-serve to roughly one-third that of large banks. Chime is the clean isolate of exactly what Cash App Card economics rest on — proving both the power (85%+ gross margin) and the fragility (interchange-regulation exposure) of the model.

### XI.3 Why Block Wins Where It Wins

Separating structural advantage from management choice from temporary advantage:

- **Self-serve onboarding under the PayFac model (STRUCTURAL, durable).** Square aggregates millions of micro-merchants under its own payment-facilitator umbrella, eliminating per-merchant underwriting friction — why Square is #1 in US POS by merchant count (~27–28%). FY2025: 4.5m sellers, 5.9bn transactions, $250.5bn GPV.
- **Integrated software ecosystem (STRUCTURAL + MANAGEMENT CHOICE).** ~59% of Square gross profit is software and integrated payments (Volume III); more than 30 products; NRR above 100%. Cohesion is a design choice that compounds into switching cost.
- **Settlement control + the self-liquidating loan (STRUCTURAL, deepest transferable mechanism — Volume V).** Block controls settlement and deducts loan repayment at source, collapsing repayment risk. FY2025 Square Loans loss rates <3%; Cash App Borrow ~97% repayment on a base where ~70% of borrowers have FICO <580; more than $200bn cumulative credit provided across Borrow, Afterpay and Square Loans (announced January 2026).
- **Shared data + underwriting engine (STRUCTURAL).** One 12-petabyte Databricks platform serving ~70 teams (Volume VI), one ML/underwriting engine — genuine one-and-a-half-machine leverage, but infrastructure, not customers.
- **Brand & design (MANAGEMENT CHOICE, semi-durable).** Cash App was #1 finance app on Google Play and #3 on iOS by US downloads in 2025.
- **Deposit-funded bank (STRUCTURAL).** Square Financial Services (Utah industrial bank) originated all Cash App Borrow loans in 2025 and more than $20bn cumulatively.
- **Consumer network (STRUCTURAL for Cash App standalone).** 59m monthly actives, 26m Card actives, 9.3m primary-banking actives (+22%), $316bn inflows.
- **Interchange (TEMPORARY / policy-dependent — Volume VII).** The hidden American subsidy; see XI.8.

### XI.4 The Moat Scorecard (0–5)

Scepticism applied discriminatingly, not uniformly.

| # | Moat | Score | Mechanism | Durability / weakening condition |
|---|------|-------|-----------|----------------------------------|
| 1 | Square software switching costs | **4** | Integrated POS/inventory/payroll cutover cost; NRR >100% | Weakens vs. vertical specialists (Toast) at premium end |
| 2 | Square brand & self-serve acquisition | **4** | PayFac viral onboarding; #1 US POS by merchant count | Weakens if CAC rises or Shopify/Stripe undercut online |
| 3 | Seller data + underwriting advantage | **5** | Settlement-visibility underwriting; self-liquidating loans; <3% loss | Weakens only if it loses the payment flow itself |
| 4 | Settlement control | **5** | Owns the ledger; repayment deducted at source | Structural; near-non-replicable without owning the rail |
| 5 | Cash App network effects | **4** | P2P virality; multi-product actives 2–3x LTV | Weakens vs. Venmo/Zelle multi-homing (near-zero switching cost) |
| 6 | Cash App Card + interchange position | **3** | Small-issuer interchange via partner banks | Policy-dependent (Durbin); see XI.8 |
| 7 | Primary-banking lock-in | **4** | Direct deposit → ~10x P2P-only gross profit; 9.3m actives | Durable once the paycheck lands; fragile before it does |
| 8 | Shared data platform | **4** | 12-PB Databricks, one ML engine, ~70 teams | Genuinely real cost leverage; infrastructure not customers |
| 9 | Banking licence + deposit funding | **4** | Utah ILC; funds loan book cheaply | Durable; licence is path-dependent to obtain |
| 10 | Regulatory / compliance capability | **2** | Required to operate | A demonstrated *weakness* — see below |
| 11 | Hardware | **1** | Deliberate loss-leader (Volume III) | Not a moat; a customer-acquisition cost |
| 12 | **Claimed cross-ecosystem synergy** | **1** | Cash App Pay, Afterpay bridge, Neighborhoods | **Largely unbuilt; no both-sides customer metric ever disclosed; Neighborhoods ~$1bn annualised GPV ≈ 0.4% of Square GPV** |

On #10, compliance is an active liability, not a moat: NYDFS Superintendent Adrienne A. Harris announced a $40m penalty on 10 April 2025 for "significant failures in its Bank Secrecy Act/Anti-Money Laundering (AML) compliance program," and a separate $80m CSBS-coordinated action by 48 state regulators (15 January 2025, led by Arkansas, California, Massachusetts, Florida, Maine, Texas and Washington) — the NYDFS consent order citing a ~170,000-alert monitoring backlog and 8,359 Cash App accounts linked to a Russian criminal network. Both settlements require an independent monitor.

**Survives testing:** #3, #4 (score 5); #1, #2, #5, #7, #8, #9 (score 4). **Overrated / fails:** #12 cross-ecosystem synergy (the strategic narrative), #10 compliance (an actual liability), #11 hardware; and #6 interchange is real-but-borrowed.

### XI.5 The Replication Test

| Asset | Difficulty | Classification |
|-------|-----------|----------------|
| Seller base + software attach | Years of self-serve flywheel + product depth | **Buildable with time / difficult** |
| Consumer base + P2P network | Network effects + brand; very hard cold | **Path-dependent** |
| Licence estate + industrial bank | Regulatory time + capital | **Buildable with time (path-dependent)** |
| Settlement control | Requires owning the rail end-to-end | **Effectively non-replicable** without the same architecture |
| Underwriting data | Derives from owning the payment flow | **Path-dependent** (flows from settlement control) |
| Brand | Marketing spend + time | **Buildable with time** |

Hardest to reproduce: **settlement control** and the **underwriting data that flows from it** — the mechanisms Volume V flagged as most transferable to the reader. Easiest to buy: brand/marketing. Notably, *nothing* in the replication list requires the two ecosystems to be joined — reinforcing that the compounding thesis is not where the defensibility lives.

### XI.6 The "One Block" Adjudication

**What would demonstrate genuine compounding:** (1) a joined person-level customer graph that is acted upon; (2) measurable cross-ecosystem customer acquisition (Cash App consumers becoming Square sellers or vice versa, or one side lowering the other's CAC); (3) cross-sell rates across the seller/consumer boundary; (4) shared-infrastructure cost leverage; (5) joint products with material adoption.

**What the record shows:**

- **Cash App Pay at Square sellers:** Launched 2021 as a QR/deep-link bridge (Volume VI). Block reports ~7.3m Cash App Pay actives (Investor Day 2025) but **discloses no Cash App Pay GPV and no Square-vs-non-Square split** — it is folded into "Cash App commerce enablement volume" ($54.7bn in Q4 2025). Not demonstrably material as a bridge.
- **Afterpay as the bridge:** See Finding 2. No seller-to-consumer bridging volume disclosed; the shipped integration points Cash App consumers at external merchants, deepening Cash App monetisation rather than fusing networks. A pilot statistic — "more than three in five customers who have made an Afterpay on Cash App Card transaction have used it at least five times" — measures engagement, not cross-ecosystem bridging.
- **Neighborhoods (the most concrete cross-ecosystem product):** Launched October 2025. Latest disclosed metrics (Q1/Q2 2026 letters): ~100,000 Cash App users following at least one seller (about half were not active on Cash App the prior month — a genuine if tiny acquisition signal); followers reach ~10% of a seller's GPV after ~three quarters; sellers gain ~1,000 followers in year one; followers transacted 50% more often than non-followers; ~$1bn annualised GPV by June 2026 — **which is ~0.4% of Square's $250.5bn annual GPV.** Real, promising, and demonstrably immaterial at current scale. Management calls it "probably the biggest lever we have" — a forward-looking aspiration, not a realised result.
- **A both-sides customer metric:** **Confirmed never disclosed, in any filing, letter or investor-day deck.** Block's retention charts measure engagement *within each ecosystem separately.* A company that has asserted synergy for years and has never published the one number that would prove it is telling the analyst something.
- **Shared-infrastructure cost leverage:** Genuinely real — one cloud/data/ML/risk spine (Volume VI); the February 2026 40% headcount cut and July 2024 functional reorg both harvest duplicated-structure savings.
- **The September 2024 functional reorg:** Block itself concluded the two-company structure had failed and moved to a functional organisation. This fixed *internal* duplication; it did not create a joined *customer* network.

**VERDICT: The two ecosystems COEXIST ON SHARED PLUMBING; they do not COMPOUND AT THE CUSTOMER LEVEL.** Proportionally: infrastructure compounding is real and material; customer compounding is near-zero today (Neighborhoods ≈0.4% of Square GPV; no overlap metric; Afterpay unbridged after four years). This is close to dispositive.

### XI.7 Porter's Five Forces

- **Supplier power — HIGH and structural (Volume VII).** Block *rents* the card networks (Visa/Mastercard set interchange), the sponsoring acquirer, the issuer-processor and the partner-bank charters. Networks hold pricing power over the rail Block cannot own; partner banks and the small-issuer exemption are policy-exposed. This is Block's single greatest structural vulnerability.
- **Buyer power — MODERATE-HIGH on both sides.** Sellers can switch acquirers (mitigated by mid-market software switching costs); consumers can multi-home across Cash App/Venmo/Zelle at near-zero cost (mitigated only by primary-banking direct-deposit lock-in).
- **Threat of new entrants — MODERATE.** PayFac self-serve is now commoditised; the licence estate, settlement control and underwriting data are not.
- **Threat of substitutes — HIGH.** Real-time bank rails (FedNow, Zelle), stablecoins, and platform-embedded finance (Shopify, Amazon) all substitute pieces of Block's stack.
- **Rivalry — HIGH.** Toast (restaurants), Clover (bank-distributed SMB), Shopify (omnichannel/online), Chime/Venmo (consumer). Intense on every front.

### XI.8 What Could Break Block

- **Vertical specialists continuing to take the premium seller segment.** Toast at ~164,000 locations and $2bn ARR, plus SpotOn, keep Square #3 in small restaurants (~13%). Serious and ongoing.
- **A platform (Shopify/Amazon) internalising financial services.** Shopify already does — Capital, Balance, Payments — at larger GMV scale. The most serious long-run threat because it attacks Square's actual model.
- **Interchange regulation.** *Corner Post* (August 2025) vacated Reg II's debit cap (stayed, on appeal; earliest practical effect ~Q3 2026), and the Fed has separately proposed tightening. Cash App Card and Chime-style economics rest on the small-issuer exemption; any erosion hits the load-bearing subsidy.
- **Consumer-credit downturn against the newly retained loan book.** Block now holds more credit risk (Cash App Borrow +223% in Q4 2025; consumer-lending losses +108% YoY GAAP). Loss rates are historically stable (<3%) but untested at this scale through a full downturn.
- **Execution risk of removing 40% of staff while under monitor obligations.** The February 2026 cut to fewer than 6,000, coinciding with independent-monitor AML remediation, is a real operational and regulatory risk. Named analysts (e.g., Mizuho's Dan Dolev) and an NBER analysis argue the "AI" rationale masks a pandemic-overhiring correction.
- **Founder-attention risk (Volume X).** Dorsey's divided attention (Bitcoin, TBD, prior Twitter) and self-admitted structural errors.

### XI.9 The Transplant Verdicts (Nigerian conditions)

*Guinnane question throughout: did this work because of the mechanism, or the institutional environment?*

**(a) The compounding assumption itself — the verdict that matters most.**
Block, with a decade and effectively unlimited capital, did *not* achieve customer-level compounding across two ecosystems it deliberately built to reinforce each other. **For a capital-constrained single founder building four layers in Nigeria, the base-rate expectation must therefore be that the layers will NOT automatically compound at the customer level.** They will share infrastructure if you build one spine — achievable and worth doing. Compounding at the customer level must be *engineered per product and measured*, never assumed. **The reader's cooperative genuinely differs from Block in one decisive respect: cooperative membership is a single shared identity across products, whereas Square and Cash App were separate logins with no joined graph.** That difference is *potentially* decisive — but only if the reader (i) builds one member identity spanning core-banking, remittance and credit from day one, and (ii) actually acts on the joined graph (cross-sell, CAC reduction, shared underwriting). If the cooperative ends up with separate identities per product, the difference is wishful. **ADAPT — the shared-identity advantage is real but conditional on building the graph first, which is exactly what Block failed to do.** *Do differently:* instrument a both-sides overlap metric from launch. If Block's silence teaches one thing, it is that a synergy you cannot measure is a synergy you do not have.

**(b) Shared infrastructure vs. shared customers.**
Block achieved the first and not the second. **Replicate the first deliberately (one core-banking platform, one risk/identity/data spine, one underwriting engine across cooperative, remittance and credit); treat the second as an earned outcome, not a design premise. ADOPT (shared infrastructure); REJECT (assuming shared customers follow automatically).**

**(c) Which moat to build first.**
Build **settlement-controlled credit on the cooperative's own transaction flow** — Volume V's deepest transferable mechanism and the study's most defensible moat (scorecard #3 and #4 both scored 5). In Nigeria, where Moniepoint's dominance was built merchant-first and where collateral-light, transaction-history underwriting already works — per Moniepoint's 2025 Year in Review it "processed ₦412 trillion in transaction value handling more than 14 billion transactions" and now powers "8 out of every 10 in-person payments," while its microfinance subsidiary "disbursed over ₦1 trillion in credit" to ~70,000 businesses that grew more than 36% after accessing it — the anchor cooperative's transaction flow is the reader's equivalent of Square's settlement rail. **ADOPT.** Attach remittance and consumer credit as *platform features* on that flow, not as separate businesses expected to compound by proximity.

**(d) Competing against entrenched incumbents (carried from Volume XII).**
The Nigerian field is not empty: Moniepoint processed ~₦412tn (~$294bn) in 2025 and claims ~80% of in-person payments; OPay (60m+ users) and PalmPay (~35m registered users) own mass-market consumer payments; the CBN is actively imposing boundaries between fintech business lines. **A four-layer group competing head-on for payments will lose to Moniepoint's distribution.** The defensible entry is the **cooperative-society niche** — a genuine shared-identity community the mass-market players do not serve as members — using the cooperative's captive, high-trust membership as the acquisition channel the incumbents lack. **ADAPT — compete on shared member identity in a niche, not on payment ubiquity.**

## XI.10 Volume XI Reconstruction

1. **Competitive universe map** — six categories (integrated POS/vertical software; acquirers; commerce-plus-embedded-finance platforms; consumer wallets/neobanks; BNPL; international), of which only Block and PayPal straddle both the merchant and consumer markets.
2. **Comparison matrix** — Shopify (GMV $378.4bn, +29%; merchant solutions 76.2% of revenue); Toast (164k locations, $2bn ARR, restaurant-only); Clover (910k merchants, ~$3.3bn revenue, bank-distributed); PayPal/Venmo (TPV $1.79tn, two-sided mirror); Chime (8.7m members, interchange-pure). Square: 4.5m sellers, $250.5bn GPV; Cash App: 59m actives.
3. **Why-Block-wins decomposition** — structural (PayFac, settlement control, self-liquidating loan, shared data, bank licence, consumer network) vs. management choice (integrated software, brand) vs. temporary (interchange).
4. **Moat scorecard** — twelve moats; strongest are settlement control and the underwriting advantage (5); weakest are hardware (1) and cross-ecosystem synergy (1); compliance a liability (2).
5. **Replication test** — settlement control effectively non-replicable; consumer network and underwriting data path-dependent; brand and licences buyable/buildable.
6. **The One Block verdict** — COEXIST on shared plumbing; do NOT compound at the customer level. Near-dispositive.
7. **Porter's Five Forces** — supplier power (networks/banks) the dominant structural risk; buyer multi-homing and substitutes both high; rivalry intense.
8. **What could break Block** — Shopify/Amazon embedding finance; vertical specialists; interchange regulation; a credit downturn on the retained book; execution risk of the 40% cut under a monitor; founder attention.
9. **Transplant verdict table** — compounding assumption ADAPT (conditional on building the graph); shared infra ADOPT / shared customers REJECT; settlement-controlled credit ADOPT (build first); incumbents ADAPT (niche on shared identity).
10. **Key unknowns** — Cash App Pay GPV and Square/non-Square split; standalone Afterpay FY2025 GMV; standalone Square Loans and Cash App Borrow dollar originations; any person-level both-sides customer figure (confirmed non-existent).
11. **Ten most important conclusions** — (i) infrastructure compounds, customers do not; (ii) the missing overlap metric is the answer; (iii) Afterpay never bridged; (iv) Neighborhoods is real but ~0.4% of GPV; (v) the strongest moat is settlement-controlled underwriting; (vi) the most overrated is cross-ecosystem synergy; (vii) Shopify executes Square's model better on the merchant side; (viii) interchange is a borrowed, policy-exposed subsidy; (ix) Block itself declared the two-company structure a mistake; (x) for a multi-entity founder, compounding must be engineered and measured, never assumed.

**The strongest moat** is settlement control and the underwriting advantage that flows from it; **the most overrated** is cross-ecosystem synergy. **Hardest to replicate:** settlement control. **Easiest:** brand. **Most dangerous competitor:** Shopify (long-run, structural), with Toast the sharpest near-term threat to premium sellers. **What could make Block obsolete:** the internalisation of financial services by larger commerce platforms combined with erosion of the interchange subsidy. **The central question — do the two ecosystems compound or merely coexist?** They coexist on shared plumbing and do not compound at the customer level. For anyone planning several businesses meant to reinforce one another, the lesson is stark: shared infrastructure is buildable and worth building, but customer-level compounding is a separate, harder achievement that must be designed for, instrumented and proven per product — and if the one large-scale, unlimited-capital attempt could not demonstrate it after a decade, a capital-constrained founder must assume it will not happen by itself.

## Recommendations

**Stage 1 (now — architecture):** Build ONE spine — a single member identity, one core-banking ledger, one risk/underwriting engine — spanning the cooperative, remittance and credit. This is the compounding that is actually achievable (Block proved it). Instrument a both-sides / multi-product-per-member metric from day one. *Threshold to proceed:* you can report, monthly, the share of members active in ≥2 layers.

**Stage 2 (credit as the first moat):** Launch credit deducted at settlement against cooperative cash-flow visibility (the self-liquidating loan). Keep loss rates below 3% before scaling. *Benchmark that changes the plan:* if multi-layer-active members do NOT show lower CAC or higher LTV than single-layer members within three quarters (Block's own Neighborhoods took ~three quarters to reach 10% of a seller's GPV from followers), stop assuming compounding and treat each layer as standalone-viable or cut it.

**Stage 3 (remittance + consumer features):** Add remittance and consumer credit only as features on the existing flow. *Threshold:* each must be standalone-margin-positive; do not cross-subsidise on an unproven synergy assumption.

**Governing rule:** A synergy you cannot measure is a synergy you do not have. Never let the "one group" narrative substitute for a published overlap number — the single discipline Block never adopted.

## Caveats

- **Basis:** US GAAP, USD, 31 December year-end. Gross-profit anchor: $7.505bn (2023), $8.889bn (2024), $10.36bn (2025). The FY2025 re-cut into Commerce Enablement / Financial Solutions / Bitcoin Ecosystem cuts *across* both segments; combined with the Q4 2023 BNPL reallocation into Cash App, this makes the compounding question harder to answer from the face of the filings. **Assessment: the re-cut is more convenient than incidental** — it further obscures a seller-vs-consumer view precisely as the synergy question sharpens — though Block's stated rationale (evolution beyond payments) is defensible and segment (Square/Cash App) reporting is retained.
- **Evidence classification:** Audited financials = CONFIRMED FACT. Cross-ecosystem synergy = COMPANY CLAIM / strategic narrative requiring correction (Volume X). The absence of a both-sides metric = CONFIRMED (verified none exists). Neighborhoods trajectory and Cash App Pay actives = COMPANY CLAIM. Nigerian market figures = THIRD-PARTY ESTIMATE / COMPANY CLAIM (Moniepoint's own Year-in-Review).
- **UNKNOWN:** Cash App Pay GPV and its Square/non-Square split; standalone Afterpay FY2025 GMV; standalone Square Loans and Cash App Borrow dollar originations (reported bundled or as growth rates); any person-level both-sides customer figure (confirmed non-existent).
- Several management statements (Neighborhoods "biggest lever," expectation it drives Cash App actives in the second half of 2026) are forward-looking aspirations, not realised results, and are flagged as such.
- The February 2026 layoffs' "AI" rationale is contested by named analysts; treated here as at least partly a pandemic-overhiring correction.
- On the Afterpay price: the ~$29bn figure widely cited is the August 2021 announcement value; because Block paid in stock and its share price fell before the 31 January 2022 close, the final accounting consideration was ~$13.9bn (Block's FY2022 10-K: $13.8bn aggregate fair value of shares issued). The $11.72bn goodwill figure from Volume IX and the 50/50 split across reporting units are unaffected.

---

# VOLUME XII — International Expansion & Market Entry

## Block, Inc. (NYSE: XYZ, formerly Square, Inc.) — A Forensic Reverse-Engineering Study

## TL;DR
- **Square exported and Cash App did not, and the reason is structural, not accidental: the seller model earns from the merchant fee Square itself sets plus software and hardware, and therefore survives capped interchange, while the consumer model's monetisation ladder depends on uncapped US small-issuer interchange that does not exist in Europe, the UK, Australia or Nigeria. For a Nigerian founder, this is the decisive finding — build the seller/merchant side first.**
- Cash App's only material foreign attempts both failed: the UK (launched 2018, shut 15 September 2024) and Verse in the EU (acquired June 2020, shut September 2023); a planned Australia launch was cancelled in June 2024. Square, by contrast, operates in eight countries with a profitable UK entity, and international is now 22% of Square gross payment volume (up from 18% a year earlier), growing 35% year on year (26% constant currency) versus 8.2% in the US.
- The interchange/monetisation-model factor is the largest single cause but not the whole story; entrenched P2P incumbents (network effects), free instant rails (Faster Payments/SEPA), and product-portability all contributed. Weighted verdict: interchange + monetisation-model ~50%, incumbency/network effects ~25%, free instant rails ~15%, commitment/focus ~10%, with product-portability as the structural umbrella over all four.

## Key Findings

**1. The natural experiment resolves cleanly.** Square is present in the US, Canada, Japan, Australia, the UK, Ireland, France and Spain. Cash App is now a US-only product. Both ran on Block's shared infrastructure spine (Volume VI's "one-and-a-half machines"), so the divergence is not about engineering capacity — it is about which revenue model survives foreign institutional conditions. **[CONFIRMED FACT]**

**2. Square's economics do not depend on interchange; Cash App's do.** Square earns a merchant discount rate (1.75% UK, 1.6% Australia, 3.25% at Japan launch / 3.6% now, 2.6% + $0.15 US) plus software and hardware. That take rate is set by Square, not by the regulated interchange embedded within it. Cash App's gross profit, by Block's own 2023 inflows-framework disclosure, came ~46% from Financial Services (dominated by Cash Card interchange) and ~35% from Instant Deposit fees (excluding BNPL). The Cash Card is issued by Sutton Bank, a sub-$10bn Durbin-exempt issuer earning roughly 0.90% interchange — an order of magnitude above the EU/UK cap of 0.2% debit / 0.3% credit under the Interchange Fee Regulation. **[CONFIRMED FACT / THIRD-PARTY ESTIMATE on the 0.90%]**

**3. Free instant transfer is worthless where the rails are already free and instant.** The UK's Faster Payments and Europe's SEPA Instant provide free bank-to-bank transfers; Venmo, Zelle and Cash App never gained traction outside the US partly because the differentiator (free instant P2P) is a native banking-system feature abroad. This directly corroborates Volume VII's Nigeria judgment: NIBSS Instant Payment already provides this. **[ANALYTICAL INFERENCE, well-supported]**

**4. Square wins where it competes on software and loses where it competes only on price/hardware.** Against SumUp and Zettle in Europe it is a strong but not dominant challenger; its edge is the integrated software ecosystem, not cheap card readers (its 1.75% UK rate is above SumUp's 1.69% and Tyl's 1.39% + 5p). **[CONFIRMED FACT / ANALYTICAL INFERENCE]**

**5. Japan is Block's proof that a cash-dominant market can be entered — but only with a deep local licensed partner, local product fidelity, and delegated local authority.** This is the closest analogue in Block's own record to the Nigerian founder's situation. **[CONFIRMED FACT]**

## Details

### XII.1 The Market-by-Market Record (Square)

- **United States** — home market; launched 2009. Standard rates 2.6% + $0.15 in-person, 3.3% + $0.30 online, 3.5% + $0.15 keyed. Square GPV $250.5bn in 2025; Square segment gross profit $3.94bn (+9%) in 2025. The only market with Square Loans originated through Block's own Utah industrial bank (Square Financial Services), Square banking (checking/savings), and the full Cash App monetisation ladder. **[CONFIRMED FACT / COMPANY CLAIM on GP]**
- **Canada** — entered October 2012 (first market outside the US). In-person rate 2.65%. Square Loans launched later (after US and Australia). Competes against Lightspeed (a Canadian POS incumbent) and banks. Entities: Square Canada, Inc. / Square Technologies, Inc. **[CONFIRMED FACT]**
- **Japan** — launched 23 May 2013, per Square's own press release ("Square Arrives in Japan," May 23, 2013), "with the support and partnership of Sumitomo Mitsui Card Corporation (SMCC)… one simple, low transaction rate of 3.25% per swipe"; TechCrunch confirmed Japan was Square's "first country outside of North America." SMCC was also Square's first foreign investor ($10m, September 2012). Flat 3.6% now. Entity: Square KK / Square Japan. See XII.5. **[CONFIRMED FACT]**
- **Australia** — entered 2016; in-person rate 1.6% (for accounts opened from 30 May 2024) — far below the US 2.75% then / 2.6% now. Square Loans available (issued by Square AU Pty Ltd, ABN 38 167 106 176). Afterpay's home market. RBA reforms cap debit interchange at 8c / 0.2% and consumer credit at 0.3% from 1 October 2026. **[CONFIRMED FACT]**
- **United Kingdom** — launched 28 March 2017 (fifth global market). Entity: Squareup Europe Ltd, FCA-authorised Electronic Money Institution (FRN 900846, authorised 15 March 2018). In-person 1.75%, online 1.4% + 25p (UK cards), +1.5% surcharge for non-UK cards. Square Loans (unregulated) plus Square Cash Advance launched June 2025. Competes against SumUp, Zettle (PayPal), Tyl by NatWest, Stripe, Revolut Business. **[CONFIRMED FACT]**
- **Ireland, France, Spain** — entered 2021. Payment processing live; product suite thinner than US/UK. +1.5% foreign-card surcharge; Ireland adds 23% VAT on the fee. Ireland entity: Squareup International Limited. **[CONFIRMED FACT]**

International reached 22% of total Square GPV (up from 18% a year earlier), with international GPV up 35% YoY (26% constant currency) versus US GPV +8.2%, per Block's Q1 2026 earnings (CFO Amrita Ahuja, prepared remarks: "International GPV grew 35% year over year, or 26% on a constant currency basis"). That implies roughly ~$55bn of international GPV on 2025's $250.5bn base. Hardware is separately certified per market (FCC in the US, RoHS in the EU); a US reader is not approved for use elsewhere. **[COMPANY CLAIM / ANALYTICAL INFERENCE on the ~$55bn]**

**Afterpay / Clearpay (acquired, not built).** Block issued 113,617,352 Class A shares with an aggregate fair value of $13.8bn; the deal closed 31 January 2022 (Block FY2022 10-K Note 9; 31 January 2022 8-K). Afterpay brand in the US, Australia, New Zealand and Canada; Clearpay brand in the UK. Clearpay entered the EU in 2021 via the Pagantis acquisition and **exited the EU (wind-down completed 25 August 2023)** (*corrected on assembly from ~25 August 2025; Volume XIII established the date from contemporaneous City A.M. and FashionNetwork reporting. See Appendix E note 2*) while UK/US/AU/NZ continued. ~24m active customers globally; dominant in Australia/NZ (~65% share), ~22% US share. Volume IX's caution stands: $11.72bn goodwill split 50/50 between the Square and Cash App units, never impaired, standalone test impossible. **[CONFIRMED FACT / THIRD-PARTY ESTIMATE on shares]**

### XII.2 The Cash App International Record

- **United Kingdom.** Launched 2018 (Cash App's first and only built international market). Offered P2P transfer and the Cash Card debit card — but **not** Bitcoin trading or the full US feature set. Estimated ~1.4 million UK users at peak; ~750,000 estimated affected at closure. Announced withdrawal 18 July 2024; shut 15 September 2024. **Stated reason (Block's 18 July 2024 statement, reported by Bloomberg): "In recent months, we have outlined our strategic approach for Cash App, which prioritizes our focus on the United States and deprioritizes global expansion."** Independent reporting attributes the harder cause: per PaymentsIndustryIntelligence, "the app struggled to gain significant traction against local competitors like Revolut and Monzo… even well-funded players face difficulties in scaling operations and achieving profitability." The UK Cash Card could not earn the interchange the US card does. **[COMPANY CLAIM + independent THIRD-PARTY]**
- **Verse (EU).** Spanish-founded P2P app operated by Verse Payments Lithuania UAB (Bank of Lithuania e-money licence, 2019); acquired 15 June 2020 with ~500,000 users and >€100m transferred. The Bank of Lithuania fined Verse Payments Lithuania UAB €280,000 (plus €75,000 on its director) on 10 March 2023 for AML/CTF failures (reported by Forbes as ~$250,000). Shut September 2023, announced on the Q2 2023 earnings call. Jack Dorsey (Q2 2023 call, per Payments Dive): "These required significant investment, and the markets have not seen the growth and profitability we had expected over the past several years… We see an opportunity to shift these resources toward strategic areas that have a higher potential return on investment." CFO Amrita Ahuja said the wind-down "will have an impact on monthly actives going forward, although we do not expect an impact to inflows or gross profit" — i.e., Verse had never monetised. **[CONFIRMED FACT / COMPANY CLAIM]**
- **Australia (Cash App).** A planned launch was **cancelled in June 2024** before going live. **[CONFIRMED FACT]**
- **Current status.** Cash App is US-only. Block has stated no relaunch plans and has "not ruled out" future re-entry, but has committed to a US-focus strategy. **[CONFIRMED FACT / COMPANY CLAIM]**

### XII.3 The Analysis — Why Square Travelled and Cash App Did Not

**Testing the interchange hypothesis (given particular rigour).**
- **US position:** Cash Card issued by Durbin-exempt Sutton Bank; estimated ~0.90% interchange on ~$140bn of 2023 Cash Card spend (Marqeta-derived third-party estimate). Large-issuer regulated debit is ~$0.21 + 0.05% + $0.01; small-issuer exempt cards historically earned far more (~$0.60/transaction average). **[THIRD-PARTY ESTIMATE / CONFIRMED FACT]**
- **EU/UK:** the Interchange Fee Regulation caps consumer debit at 0.2% and credit at 0.3% — roughly one-quarter to one-third of the US exempt rate, with **no small-issuer exemption**. A UK Cash Card cannot earn the US Cash Card's interchange. **[CONFIRMED FACT]**
- **Australia:** debit ~8c / 0.2%, credit 0.3% (0.5% weighted benchmark historically, tightening October 2026). **[CONFIRMED FACT]**
- **Canada:** consumer credit ~0.95%–1.4% (negotiated down), above the EU but below the US exempt rate. **[CONFIRMED FACT]**
- **Japan:** interchange embedded in the ~3.6% merchant discount rate; Square captures the merchant fee. **[CONFIRMED FACT]**
- **Nigeria:** merchant service charge capped at 0.5% (cap ₦10,000 under the 2026 CBN Guide to Charges), the issuer's slice a fraction of that. **[CONFIRMED FACT]**

**Verdict on interchange:** CONFIRMED as the single largest factor for Cash App. Cash App's US monetisation ladder (Cash Card interchange + Instant Deposit, ~46% + ~35% of ex-BNPL gross profit) cannot be reconstructed under capped interchange. But it is **not the whole story** — Verse and Cash App UK also failed for lack of users and engagement, which interchange alone does not explain.

**Why Square survives capped interchange (finding of the first importance).** Square does not earn interchange — it *pays* it as a cost embedded in the merchant discount rate it sets. In the UK, Square charges 1.75% regardless of the 0.2%/0.3% interchange beneath it; its margin is the spread plus software and hardware. Lower European interchange actually *lowers Square's cost of goods sold*. This is precisely why Square is profitable in exactly the capped markets that would starve Cash App. Squareup Europe Ltd reported turnover of £83.95m and net income of £27.92m for FY2024 (up from £64.9m turnover in FY2023) — a profitable European seller business. **[CONFIRMED FACT / ANALYTICAL INFERENCE]**

**Network-effects hypothesis:** PARTLY TRUE. UK P2P ground was held by Revolut, Monzo and bank-native features; Cash App entered late with a weaker proposition (no Bitcoin, thin feature set). Weight ~25%.

**Rails hypothesis:** TRUE and important. Faster Payments (UK) and SEPA Instant (EU) already provide free instant transfer, gutting Cash App's core hook. Venmo and Zelle likewise never left the US. Weight ~15%.

**Product-portability hypothesis:** TRUE and the deep structural reason. A merchant's need (accept payment, run a shop) is jurisdiction-portable; a consumer's financial life is culturally and institutionally specific. This is the umbrella over the other factors.

**Commitment hypothesis:** PARTLY TRUE. Block chose to concentrate rather than keep failing abroad — but the concentration followed the failures rather than pre-empting success. Weight ~10%.

### XII.4 What Had To Change Per Market
- **Pricing:** localised and generally *lower* than the US (UK 1.75%, AU 1.6%) because competition and capped interchange compress rates.
- **Hardware:** per-country certification (FCC/RoHS); readers not cross-approved.
- **Language/currency:** English/French/Japanese/Spanish; local-currency settlement.
- **Local payment methods:** JCB in Japan (Square was slow to support it and lost merchants to Rakuten SmartPay); contactless mandatory in the UK/EU.
- **Licensing:** e-money authorisation (Squareup Europe Ltd, FCA FRN 900846); acquiring via SMCC in Japan; local lending entities (Square AU Pty Ltd).
- **Tax/invoicing:** Japanese paper Ryoshusho ("formal receipt") norms forced Square to build thermal-printer support against HQ resistance; Ireland VAT on fees; Japan's Tax Invoice System.
- **Products that travelled unchanged:** core payments acceptance, Square Point of Sale.
- **Products that required adaptation:** Square Online, Appointments, Restaurants (localised market-by-market; Appointments only US/CA/AU/UK); Square Loans (US, AU, UK, Canada only, via local entities — no Utah-industrial-bank equivalent abroad, per Volume II).
- **Products that never travelled:** the full Cash App monetisation ladder; Square banking (US-only); the industrial-bank charter.

### XII.5 The Japan Case
Japan in 2013 was cash-dominant with low card penetration, expensive locked-in terminals, and a foreign-entrant licensing maze — structurally the closest analogue to Nigeria in Block's record. What Block did:
- **Partnered deeply with SMCC** as acquiring bank (and first foreign investor, $10m). Japanese merchants were onboarded under SMCC's licence umbrella, with fund settlement and risk management leveraging SMCC's existing licences — letting Square launch quickly rather than waiting years for its own approval.
- **Went hyperlocal:** segmented by vertical and neighbourhood (third-wave coffee shops around Omotesando/Aoyama), ran a "Square Week" activation across 70+ boutiques/salons/cafés, and used UNIQLO as a flagship credibility anchor (echoing the Starbucks role in the US).
- **Localised product fidelity:** built thermal-printer/paper-receipt support against HQ resistance; belatedly added JCB (Japan's homegrown card, embedded in points/*poikatsu* loyalty culture) after losing "good merchants by being too slow."
- **Delegated authority:** the 2019 government cashless-rebate program (5% rebates, POS subsidies ahead of the consumption-tax hike and Tokyo Olympics) produced "the closest thing we had to hypergrowth," executed by the local team with SMCC and SMBC bank branches as onboarding centres.
- **Verdict:** it worked — Japan is part of the fast-growing international 22%. But the winning pattern (deep local partner, local product fidelity, delegated authority, patience) is the opposite of a US-playbook copy-paste. Japan-specific GPV/merchant figures are not separately disclosed (**UNKNOWN**).

### XII.6 International Economics
- International ~22% of Square GPV (~$55bn implied on 2025's $250.5bn), growing 35% (26% constant currency) versus 8.2% in the US in Q1 2026; international gross profit grew 38% YoY in Q1 2024. **[COMPANY CLAIM]**
- Squareup Europe Ltd (UK): FY2024 turnover £83.95m, net income £27.92m; FY2023 turnover £64.9m — profitable. Note this single FCA-licensed entity (FRN 900846) housed **both** the UK Square seller business and the former Cash App UK operations, so its turnover is not purely seller revenue. **[CONFIRMED FACT via Companies House aggregators]**
- Whether each international market is profitable on a fully-loaded basis versus subsidised by the US is **NOT DISCLOSED** by Block (**UNKNOWN**); the profitable UK entity and the group's positive operating income ($892m in 2024, up from a $279m loss in 2023) suggest international is not a heavy drag.
- International take rate versus US: **UNKNOWN** as a disclosed blended metric; published per-transaction rates are lower abroad (1.75% UK, 1.6% AU) than the US (2.6% + $0.15).
- Currency: reported growth runs ~9 points above constant currency (35% vs 26% in Q1 2026), so FX has recently flattered reported international growth.

### XII.7 The Competitive Position Abroad
- **Europe (UK/IE/FR/ES):** SumUp (34+ markets, micro-merchant/price leader at 1.69%), Zettle by PayPal (retail features + PayPal/Venmo wallet), Tyl by NatWest (1.39% + 5p), Stripe, Revolut Business, and newer discounters (Lopay). Square is a strong challenger differentiated by software depth, not price — its 1.75% sits above SumUp and Tyl.
- **Canada:** Lightspeed (domestic POS) and banks.
- **Japan/Australia:** local acquirers and banks; PayPal Here (early); Rakuten SmartPay (Japan). Square won on design + next-day deposits + software.
- **P2P (the ground Cash App lost):** Revolut and Monzo (UK); bank-native instant transfer everywhere. Cash App never held ground.
- **Pattern:** Square wins where the contest is software/ecosystem and ties/loses where it is pure price; Cash App loses wherever free instant rails and incumbents already exist.

### XII.8 The Transplant Verdicts (Nigeria)

- **Seller vs consumer — which half to build first: ADOPT the seller-first sequence.** Block's own record shows the seller proposition is jurisdiction-portable and the consumer P2P/monetisation model is not. The silent institutional worker: merchant needs are universal; consumer financial life is culturally specific and interchange-dependent. **Build the merchant/cooperative-acquiring and software side first.**
- **Operating under capped merchant charges: ADAPT.** Block survives EU/UK caps because it earns from the *merchant fee it sets and from software*, not from interchange. Nigeria's 0.5% MSC cap is even tighter than Square's ~1.6–1.75% international merchant discount rate, so the reader **cannot** rely on payment margin alone — margin must come from software, SaaS/subscription, lending and float, exactly as Volume III (software ≈ 59% of Square gross profit) and the monetisation ladder (Volume IV) imply. What must change: do not price the business on transaction take; price it on software and credit.
- **Free instant transfer where rails exist: REJECT.** NIBSS Instant Payment already provides free instant transfer; Block's UK/EU failure with the same value proposition corroborates Volume VII. Do not build the business around free instant transfer as the hook.
- **Entering against entrenched incumbents: ADAPT (enter narrow and deep).** Cash App entered the UK late and broad against Revolut/Monzo and failed. The reader faces OPay (~35m users, ~560,000 agents), PalmPay (~30m registered users) and Moniepoint (dominant in merchant POS, ~1.3m businesses). Lesson from Japan: win a dense, defensible vertical/community first (the anchor cooperative society is exactly this) rather than a broad land-grab against incumbents' agent networks.
- **Cash-dominant market (Japan lesson): ADOPT the partner-led, locally-delegated, high-fidelity model.** Deep licensed local partner, local product fidelity (local payment methods, local receipt/tax norms), patient community-by-community density, and delegated local authority. Do not run it from a foreign playbook.
- **Localisation sequencing for a capital-constrained founder:** first — licensing/partner and core acceptance + the software that creates lock-in; next — credit as a platform feature (using proprietary transaction data, the transferable half per Volume IV); defer — consumer P2P and any "free instant transfer" positioning (rails already provide it); defer — hardware proliferation.

### XII.9 Volume XII Reconstruction

**(1) Market table:** US (home, full stack), Canada (Oct 2012), Japan (May 2013, SMCC, 3.25%→3.6%), Australia (2016, 1.6%), UK (Mar 2017, Squareup Europe Ltd, FCA FRN 900846, 1.75%), Ireland/France/Spain (2021). Cash App: UK (2018–2024, exited), Verse EU (2020–2023, exited), Australia (cancelled 2024). Afterpay/Clearpay acquired 31 Jan 2022 ($13.8bn stock); Clearpay exited the EU in 2023.

**(2) Cash App international record:** total failure abroad — UK shut, Verse shut, Australia cancelled; never monetised abroad.

**(3) Hypothesis verdict with proportions:** interchange/monetisation-model ~50%; incumbency/network effects ~25%; free instant rails ~15%; commitment/focus ~10%. Product-portability is the structural umbrella over all four.

**(4) Localisation map:** pricing (lower abroad), hardware (re-certified), licensing (e-money/acquiring/local lending entities), local payment methods (JCB), tax/invoicing (Ryoshusho, VAT), product depth (thinner abroad).

**(5) Japan case:** entered via SMCC, localised deeply, delegated locally, scaled on the 2019 cashless program — worked.

**(6) International economics:** ~22% of GPV, fastest-growing; UK entity profitable (£27.9m net income FY2024); geographic profitability not disclosed.

**(7) Competitive position:** wins on software (vs SumUp/Zettle/Lightspeed), loses on P2P (vs Revolut/Monzo/bank rails).

**(8) Transplant table:** seller-first ADOPT; capped-MSC ADAPT (monetise software/credit, not transactions); free instant transfer REJECT; incumbents ADAPT (narrow/deep); cash-dominant ADOPT (partner-led/local); sequencing (licence + software → credit → defer P2P/hardware).

**(9) Key unknowns:** per-market profitability; Japan-specific scale; blended international take rate; precise UK Cash App user/revenue figures; the FY2023 profit line of Squareup Europe Ltd.

**(10) Ten most important conclusions:**
1. Square exported because it monetises the merchant fee and software, which are jurisdiction-portable and interchange-independent.
2. Cash App did not export because its monetisation ladder depends on uncapped US small-issuer interchange that no target market permits.
3. Square is profitable *because of* — not despite — capped interchange, since low interchange lowers its cost of goods.
4. The Nigerian 0.5% MSC cap means the reader must monetise software and credit, not the transaction.
5. Free instant transfer is not a differentiator where instant rails exist — proven twice (UK/EU) and applicable to NIBSS.
6. Entering broad against entrenched incumbents fails (Cash App UK); entering narrow and deep works (Square Japan).
7. Cash-dominant markets are winnable only with a deep local licensed partner and local product fidelity.
8. Consumer financial life is culturally specific; merchant needs are universal — build the seller side first.
9. Afterpay was bought, not built; it does not prove Block can *enter* markets, and even it exited the EU.
10. The build sequence should be: licence/partner + acceptance + lock-in software → data-driven credit → (defer) consumer P2P and hardware.

## Recommendations
1. **Build the seller/cooperative-acquiring and core-banking software first.** This is the portable half. Benchmark to change course: if merchant/cooperative software attach and retention are strong, proceed; if you find yourself competing purely on transaction price against OPay/Moniepoint/PalmPay, stop and re-differentiate on software.
2. **Monetise software, subscriptions, credit and float — never the 0.5%-capped transaction.** Threshold: if more than 50% of gross profit is coming from payment take, the model is mispriced for Nigeria.
3. **Launch credit as a platform feature using proprietary transaction data** (the transferable half per Volume IV), not as a standalone lender.
4. **Do not position on "free instant transfer."** NIBSS already provides it; treat instant transfer as table-stakes plumbing, not a wedge.
5. **Enter narrow and deep via the anchor cooperative** (your Japan-style dense community) before any broad consumer push.
6. **Secure a deep local licensed/banking partner early** (the Square–SMCC model) and delegate local authority to the operating team.
7. **Defer** consumer P2P, a Cash-App-style consumer wallet, and hardware proliferation until the seller/credit engine is proven.

## Caveats
- Company statements on the Cash App UK/Verse withdrawals are COMPANY CLAIM ("focus on the US"); independent reporting supplies the harder cause (no traction, no monetisation) — both are presented.
- Per-market and geographic profitability, Japan-specific scale, and a blended international take rate are NOT DISCLOSED (UNKNOWN).
- Squareup Europe Ltd's FY2024 figures (£83.95m turnover, £27.92m net income) are from Companies House data aggregators, not the raw filing pulled directly, and the entity blends Square-seller and former Cash-App-UK activity, so it cannot be read as a pure seller-margin figure.
- Hypothesis weightings are ANALYTICAL INFERENCE, not company disclosure.
- Afterpay/Clearpay footprint is acquired, not organically entered — per the framing note, it should not be read as evidence that Block can itself enter markets.
- All figures are US GAAP / USD / 31 December year-end unless a local entity (GBP) is named; the series reflects the Q4 2023 BNPL reallocation into Cash App and the FY2025 re-cut into Commerce Enablement / Financial Solutions / Bitcoin Ecosystem. Some Australian and Nigerian regulatory figures cited (RBA October 2026 caps; the 2026 CBN Guide to Charges) post-date the reporting periods and are flagged as forward-effective where relevant.

---

# VOLUME XIII — The Abandonment Record

## A Forensic Reverse-Engineering of Block, Inc. (NYSE: XYZ, formerly Square, Inc.)

## TL;DR
- Block's abandonment record contains the sharpest natural experiment in fintech: **Square Wallet** (2011–2014, "pay by name" hands-free checkout) failed completely while **Square Cash** — launched almost simultaneously in October 2013 — became Cash App and now generates **$6.34bn of gross profit (FY2025, +21%), roughly 61% of Block's $10.36bn total, with 59 million monthly actives at year-end 2025**. The difference was not concept quality but structure: Cash App solved a one-sided job (send money to a person) that spread pairwise with zero merchant dependency, while Wallet required merchants *and* consumers to change behaviour simultaneously and never cleared the network-effect threshold.
- Read by cause not date, the record shows Block **bought-and-sold-well once (Caviar, a ~$320m+ gain)**, **bought-and-wrote-off once big (TIDAL, effectively a complete ~$206m goodwill write-off)**, killed several **built products cheaply and fast** (Square Wallet/Order, Cash App UK, Verse, Clearpay EU), and ran a cluster of **founder-conviction crypto bets** (TIDAL, TBD/Web5, Proto mining, Bitkey, the bitcoin treasury) whose *process* — a 35-minute committee, no executive support — was demonstrably weaker than the variance in their outcomes.
- Net capital destroyed by the *abandoned* ventures is modest — the Caviar gain roughly offsets the TIDAL write-off and most other kills were cheap — so the honest verdict for a capital-constrained Nigerian founder is not "Block was reckless" but "Block could afford to be wrong, and you cannot": **adopt the killing-fast discipline, adopt Cash App's tested-behaviour rule, and reject acquisition-led growth and founder-conviction bets that no operator will defend.**

## Key Findings

1. **Square Wallet is the most instructive failure in the record** — a genuinely visionary product killed by a structural flaw, not incompetence. Its successor Square Order was killed even faster (10 months). Cash App, launched in the same window, is now the larger half of Block.
2. **The most expensive single failure was TIDAL** — $237.3m paid for 86.23%, effectively a complete goodwill write-off ($132.3m in 2023 + $73.5m in 2024 = $205.8m), acquired via a process a Delaware judge called "by all accounts, a terrible business decision."
3. **Caviar was a genuinely good trade** — bought 2014 (reported ~$90m; a securities filing shows $44.3m), sold to DoorDash for $410m (closed 31 October 2019). This single disposal roughly offsets the TIDAL destruction.
4. **Block kills built products fast and cheap but held its one expensive conviction (TIDAL) slow** — Order died in 10 months, Cash App Australia before launch, but TIDAL absorbed three-plus years and two impairments before being wound down.
5. **Failures cluster in consumer and founder-driven ventures, not in the merchant core.** Square's seller ecosystem has no comparable abandonment; nearly every kill is a consumer product (Wallet, Cash App UK, Verse) or a Dorsey-conviction bet (TIDAL, TBD, Proto).
6. **The governance structure is directly implicated.** Dorsey controls **42.2% of total voting power** (per Block's 2026 proxy) on a high-single-digit economic stake; the TIDAL acquisition and the crypto pivot both followed founder conviction over operator consensus.
7. **The failure rate is normal-to-low for an acquisitive tech company** — against the widely-cited 70–90% M&A failure rate (HBR, 2011), Block's one clean write-off and one clean win is unremarkable, and its experiments were unusually cheap.

## XIII.1 THE SQUARE WALLET CASE

### What it was — Card Case → Pay With Square → Square Wallet
**[CONFIRMED FACT]** Square launched a consumer app called **Square Card Case** in 2011 (a major hands-free update landed November 2011). The concept was radical: a customer filled a virtual "case" with "cards" for merchants who accepted Square, then **paid by name** — walking into a store, saying their name at the till, with the cashier verifying the customer's photo on the merchant's iPad. The November 2011 update added iOS 5 geofencing, so that within 100 metres of a participating merchant a tab opened automatically; the customer "didn't need to pull the phone out at all."

**[CONFIRMED FACT]** Merchant adoption grew fast: Square reported 20,000 merchants (November 2011), over 40,000 (February 2012), and 75,000 (March 2012), when the app was renamed **Pay With Square**, and later **Square Wallet**. Slate (November 2011) captured the ambition: "you go into a store, choose what you want to buy, and then tell the cashier your name. That's it — you've just paid."

### The Starbucks partnership
**[CONFIRMED FACT]** In August 2012 Starbucks invested $25m in Square (part of a Series D that valued Square at $3.25bn), Square became the exclusive processor of credit/debit payments at 7,000-plus US stores, and Starbucks CEO Howard Schultz joined Square's board (he left about a year later). Dorsey called it "an epic partnership."

**[CONFIRMED FACT — from Square's IPO S-1]** The deal was structurally loss-making. Square disclosed in its 2015 IPO filing that it lost roughly **$71m** processing Starbucks payments over three years; the Seattle Times computed accumulated losses of about **$84.5m**. Year-by-year losses: ~$3m (2012), ~$25m (2013), ~$28m (2014), ~$14m (first half 2015). In 2014 Square earned $123m in Starbucks revenue but paid $151m in card-network fees to process it. The economics failed because Starbucks' average ticket was low (~$5) and interchange on small-ticket card payments exceeds Square's thin processing margin.

**[CONFIRMED FACT]** The partnership unwound as Square approached IPO: exclusivity ended 1 October 2015, Square amended the contract to raise its per-transaction take, and the relationship was set to expire in Q3 2016. Starbucks had already stopped accepting Square Order payments in its stores in 2014.

### The discontinuation and Square Order
**[CONFIRMED FACT]** On 12 May 2014 Square pulled Square Wallet from the app stores and replaced it with **Square Order**, an order-ahead-for-pickup app limited to San Francisco and New York. **[COMPANY CLAIM]** A Square spokesperson said: "we wanted to add more value to the experience of paying with name and the most efficient way to do that was to build a new app on a new and more agile platform." **[ANALYTICAL INFERENCE]** This is a euphemism; independent reporting (Recode: "The grand Square Wallet experiment is over") treated it as an admission that Wallet had failed to gain traction.

**[CONFIRMED FACT]** Square Order was itself killed after just 10 months — Square notified users that orders would stop 20 March 2015. Square had introduced an 8% fee on Order transactions in July 2014 (versus its standard 2.75%), far above order-ahead norms. **[COMPANY CLAIM]** Square said it was "focusing" on other tools including gift cards and Caviar. A Javelin analyst called the shutdown "premature."

### What Square Cash did differently
**[CONFIRMED FACT]** Square Cash launched publicly 15 October 2013 (after an invite-only test in May 2013). The mechanism: email a recipient, CC cash@square.com (later pay@square.com), put the dollar amount in the subject line; each party linked a debit card once, and money moved bank-to-bank. It worked from any email client and had companion iOS/Android apps. It was free, and — critically — required no merchant. Walt Mossberg (AllThingsD) called it "the quickest, simplest method I've seen for sending money from one person to another." **[CONFIRMED FACT]** Square Cash became Cash App, which in FY2025 generated $6.34bn of gross profit (+21%), ~61% of Block's $10.36bn total.

### A defensible account of the divergence
**[ANALYTICAL INFERENCE]** The divergence was not primarily one of concept, execution talent, or timing — both products were visionary, well-built, and early. It was a difference in **network-effect topology and behavioural dependency**:
- **Square Wallet required a two-sided behaviour change simultaneously.** For "pay by name" to be worth using, a critical mass of *merchants* had to enable it *and* a critical mass of *consumers* had to prefer it over a card they already carried. The consumer's marginal benefit was tiny (a few seconds saved); the merchant's friction was real (verify photos, learn a new flow). Neither side reached the threshold where the other's participation became compelling. Contactless/NFC and, ultimately, Apple Pay (announced 2014, at Starbucks in 2016) then commoditised the "phone as payment" idea Wallet was built around.
- **Square Cash solved a one-sided job the user already had.** Sending money to a person has no merchant in the loop; the "network" a sender needed was one other person, pulled in by the transaction itself (viral, pairwise adoption). The benefit over cash, cheques or PayPal's clunkier flow was large and immediate. Cash App's later expansion (Cash Card, direct deposit, bitcoin, stock investing, Borrow) was built on a base of habitual person-to-person use it had already secured.

**[ANALYTICAL INFERENCE]** The lesson: **a consumer financial product that depends on merchants changing behaviour to deliver consumer value will stall; one that delivers standalone value to a single user and spreads pairwise will compound.** Wallet's fatal flaw was designed in from day one.

## XIII.2 THE BOUGHT-AND-SOLD-WELL CATEGORY

### Caviar (the one clean win)
**[CONFIRMED FACT]** Square acquired the food-delivery service Caviar in 2014. The purchase price is reported two ways: press consistently cites ~$90m, but a securities filing shows $44.3m — the discrepancy likely reflects headline (including earnouts/stock) versus GAAP-recognised consideration. Square sold Caviar to DoorDash for **$410m** in cash and DoorDash preferred stock; announced 1 August 2019, closed 31 October 2019. Caviar lead Gokul Rajaram and the team moved to DoorDash. Caviar's sub-brand **Fastbite** was shut in 2016. Square had tried to sell Caviar in 2016 (to Uber, GrubHub, Yelp) for ~$100m and failed to find a buyer at that price; the business "reportedly struggled to turn a profit."

**[COMPANY CLAIM]** Dorsey framed the sale as focus — selling Caviar let Square "increase our focus on and investment in our two large, growing ecosystems — one for businesses and one for individuals." **[ANALYTICAL INFERENCE]** Independent reporting (TechCrunch) is blunter: Square "shed an unprofitable arm that looked less and less core," and DoorDash "turned cash and stock into a bit of growth." The realised gain — roughly $320m on the reported cost basis, or ~$366m on the filing basis, before DoorDash stock movement — makes this the single value-creating exit in the record. **VERDICT: a genuinely good trade; the volume says so plainly.**

## XIII.3 THE BOUGHT-AND-WRITTEN-OFF CATEGORY

### TIDAL (the most expensive failure)
**[CONFIRMED FACT]** Block acquired TIDAL on 30 April 2021; final consideration **$237.3m for 86.23%**, held through **Aspiro AB**, **TIDAL Music AS** and **Project Rising LLC**. Original goodwill ~$197.9m. Jay-Z (Shawn Carter) joined Block's board; the artist shareholder group (Beyoncé, Rihanna and others) retained ~13.2%.

**[CONFIRMED FACT — from the derivative suit]** The acquisition process was extraordinarily thin. Per the May 2023 Delaware Chancery ruling by Chancellor Kathaleen McCormick (dismissing the City of Coral Springs Police Officers' Pension Plan suit): Dorsey proposed the deal on a board video call while vacationing with Jay-Z in the Hamptons in summer 2020; the Transaction Committee's first meeting lasted 35 minutes; no other senior Block executive supported the deal. Per Reuters' account of the ruling, "By 2020, Tidal had signed up 2.1 million paying subscribers, compared with Spotify's 138 million, Apple Music's 60 million and Amazon Music's 55 million," alongside ten consecutive quarters of multimillion-dollar losses and a Norwegian criminal investigation into streaming-fraud allegations. The judge called the deal "by all accounts, a terrible business decision." NYU Stern marketing professor **Scott Galloway** — quoted in the shareholder complaint and reported by Bloomberg Law — called it "a $300 million bar tab to hang out with Jay-Z."

**[CONFIRMED FACT — from 10-K goodwill notes]** Block impaired TIDAL goodwill by **$132,313k in Q4 2023** and a further **$73,508k in Q4 2024** — together $205.8m, effectively wiping out the ~$197.9m original goodwill. In late 2024 Block announced it was "scaling back our investment in TIDAL," eliminated product-management and product-marketing functions, and cut ~40 TIDAL staff in December 2024 (a further ~10% cut followed in 2025). Employees were reportedly instructed not to mention Jay-Z on internal channels (Fortune, November 2024). TIDAL still operates as a slimmed-down service under interim head Jesse Dorogusker, with simplified $11.99 Hi-Fi / $19.99 Hi-Fi Plus tiers and Cash App–powered artist tipping (beta September 2024).

### Verse
**[CONFIRMED FACT]** Block acquired the European P2P app Verse on 15 June 2020 (~500,000 users). **Verse Payments Lithuania UAB** was fined €280,000 by the Bank of Lithuania on 10 March 2023 for anti-money-laundering failures. The Verse brand was wound down September 2023 as part of Block's European retreat. **[COMPANY CLAIM]** The CFO said the wind-down would affect monthly actives but "we do not expect an impact to inflows or gross profit" — **[ANALYTICAL INFERENCE]** i.e., after three years Verse had never monetised. **[COMPANY CLAIM]** Dorsey: these operations "required significant investment, and the markets have not seen the growth and profitability we had expected."

## XIII.4 THE BUILT-AND-FAILED CATEGORY

- **Square Card Case / Pay With Square / Square Wallet** — launched 2011, killed 12 May 2014. Concept: hands-free "pay by name." Cause: two-sided behaviour dependency (see XIII.1).
- **Square Order** — launched 12 May 2014, killed ~20 March 2015 (10 months). Order-ahead pickup; 8% fee. Cause: premature, mispriced, no traction.
- **Square Market** — launched 2013 as a free marketplace/online-store product ("open a store for free," 2.75% per item). Superseded by the **Square Online Store** built on Weebly technology after Square acquired **Weebly for ~$365m** (announced 26 April 2018); the legacy product was migrated and later rebranded "Square Online / websites." Not a hard failure — a quiet absorption.
- **Discontinued hardware** — Block confirms that as of 1 September 2025 software updates were discontinued for older hardware versions, including the 1st-generation Square Reader for contactless and chip and the 1st-generation Square Stand; multiple earlier Reader/Stand/Register generations are retired from sale. Normal product-lifecycle churn, not strategic failure.
- **Cash App United Kingdom** — launched 2018 (Cash App's first international market), shut 15 September 2024. **[COMPANY CLAIM]** Stated reason: prioritising the US ("We're focused on growing within the U.S., not expanding into new markets"). **[ANALYTICAL INFERENCE / independent reporting]** Failed to compete against entrenched Revolut, Monzo and Starling. Housed in **Squareup Europe Ltd**.
- **Cash App Australia** — cancelled June 2024 before launch.
- **Clearpay / Afterpay EU** — Clearpay (Afterpay's EU brand, entered via the 2021 ~$50m Pagantis acquisition) began winding down France, Italy and Spain from 27 June 2023, stopped new customers 3 July 2023, and closed the EU operation from **25 August 2023**. (The carried-forward brief cites "~25 August 2025"; contemporaneous City A.M./FashionNetwork reporting places the closure at 25 August 2023 — flagged as a date conflict.)
- **TBD / Web5** — Block's decentralised-web unit, launched June 2022 (Dorsey called Web5 "likely our most important contribution to the internet"). Staff laid off and the unit wound down entirely November 2024; foundational components contributed to the Decentralized Identity Foundation.
- **Verse** — see XIII.3.

## XIII.5 THE FOUNDER-CONVICTION CATEGORY

**[CONFIRMED FACT]** In the Q3 2024 shareholder letter Block said: "We are scaling back our investment in TIDAL and winding down TBD … This gives us room to invest in our bitcoin mining initiative … and Bitkey, our self-custody wallet for bitcoin."

- **TIDAL** — see XIII.3. Founder conviction over operator consensus; ~$206m written off.
- **TBD / Web5** — wound down November 2024; a pure conviction bet with no revenue model that returned nothing but open-source contributions.
- **Spiral** — Block's open-source bitcoin-development subsidiary (formerly Square Crypto); persists as a cost centre funding bitcoin development with no direct return, by design.
- **Proto (bitcoin mining hardware)** — Block completed a 3-nanometer mining chip design in early 2024 and in July 2024 signed its flagship supply deal with **Core Scientific** (~15 EH/s). Core Scientific **booked a $41.9m loss to terminate** the contract, having paid Block ~$67.9m for chips since 2024 ($10m July 2024, $21.3m January 2025, $36.6m January 2026) before exiting in favour of ~$14bn of AMD AI-colocation leases. Core was Proto's first and only named large customer. **[ANALYTICAL INFERENCE]** The collapse of the flagship customer immediately after launch is a serious product-market-fit warning for a business Block explicitly cited as having "strong product market fit."
- **Bitkey** — self-custody hardware wallet, shipping since March 2024; connects to Cash App and Coinbase. Still live; a conviction bet not yet returned.
- **Bitcoin treasury** — Block held ~8,883 BTC at end-2025 and ~9,000+ BTC by Q1 2026 (corporate), plus ~19,357 BTC for customers (~28,355 BTC total, ~$2.2bn). Under the May 2024 "Bitcoin Blueprint" Block reinvests 10% of monthly bitcoin gross profit into BTC. A conviction bet that has largely worked on outcome (BTC appreciation) but belongs analytically in Volume IX.

**[ANALYTICAL INFERENCE]** The pattern reveals a **systematic process weakness, not merely bad luck**: the conviction bets share a signature — proposed or championed by Dorsey personally, thin or absent operator support, and often no revenue model at inception (TBD, Spiral) or a single unproven customer (Proto). The framing note's trap — scoring these only by outcome — is real: bitcoin worked and TIDAL did not, but *both* were decided by the same weak process. A serious assessment judges the process, and the process was poor in both.

## XIII.6 THE STRATEGIC-RETREAT CATEGORY (the abandonments nobody announced)

- **Micro-merchant de-prioritisation** — Square, which built its brand on micro-merchants and the free card reader, has moved upmarket: GPV from mid-market sellers (those >$500,000 annualised) reached **45% of total GPV** (up from 41% two years earlier), growing ~20–22% year on year. PYMNTS calls this "a move away from Square's original DNA as a small merchant enabler." Nobody announced abandoning micro-merchants; the investment simply migrated.
- **Geographic withdrawals** — Cash App UK (2024), Cash App Australia (cancelled 2024), Verse EU (2023), Clearpay EU (2023). A coherent retreat from international consumer expansion, dressed as "prioritising the US."
- **Lending strategy shift** — Volume IX established the move from originate-to-distribute toward retaining the loan book; Square Financial Services received FDIC approval in March 2025 to originate/service Cash App Borrow loans directly (>$27bn originated in the five quarters since).
- **The two-ecosystem organisational model** — Announced at the Q2 2024 earnings call, Block abandoned its two-independent-ecosystems (Square vs Cash App) structure for a single functional organisation. **[COMPANY CLAIM]** Dorsey later admitted: "over-hired during covid because i incorrectly built 2 separate company structures (square & cash app) rather than 1, which we corrected mid 2024." A rare public admission that a core organising principle was a mistake. It culminated in the February 2026 cut of ~40%+ of the workforce (restructuring charges ~$852m) and Dorsey's stated ambition of a near-flat, AI-mediated organisation.

## XIII.7 THE CAPITAL ARITHMETIC

**[ANALYTICAL INFERENCE — assembled from the confirmed figures above]**

**Capital deployed into subsequently-abandoned ventures (identifiable):**
- TIDAL: $237.3m acquisition consideration.
- Verse: undisclosed (within a ~$253.7m 2021 "other acquisitions" bucket; small) — UNKNOWN precise.
- Starbucks partnership: not an acquisition but a deliberate loss-leader; ~$84.5m accumulated processing losses (net of the $25m investment received, ~$60m net drag).
- Caviar: $44.3m (filing) to ~$90m (reported).
- Clearpay EU (Pagantis): ~$50m.
- Square Wallet / Card Case / Order / TBD / Spiral / Proto R&D: development and operating costs — UNKNOWN, though Proto's chip programme was material.

**Capital recovered:**
- Caviar: $410m (cash + DoorDash preferred) — gain ~$320m (reported basis) to ~$366m (filing basis).
- Starbucks: $25m equity investment received, plus non-cash brand exposure.
- Proto: Block *received* ~$67.9m from Core Scientific (Block was the seller); the $41.9m loss was Core's, not Block's — though Block loses the future revenue stream.

**Write-offs by year (goodwill impairment, TIDAL):** $132.3m (FY2023) + $73.5m (FY2024) = $205.8m.

**Net destruction (abandoned ventures only):** The TIDAL write-off (~$206m) plus the Starbucks net drag (~$60m) plus Clearpay/Verse (tens of millions) is **substantially offset by the ~$320m+ Caviar gain**. On the identifiable items, the abandonment record is close to **net-neutral to modestly value-creating**, before unquantified R&D on Wallet/Order/TBD/Proto. Expressed against gross profit, even the gross TIDAL write-off (~$206m) is **~2% of FY2025 gross profit ($10.36bn)** and a fraction of a percent of capital deployed over the period.

**Critical exclusion:** This excludes **Afterpay**, whose valuation collapsed from a $29bn announced / $13.9bn closing price with Australian writedowns of $12.2bn since 2023. Afterpay is *not* abandoned — it is now core to Cash App's BNPL — so it belongs in Volume IX. Including it would swamp every other number: the abandonment record proper is cheap; the *retained* acquisition (Afterpay) is where the largest paper destruction sits.

**Benchmarking.** **[THIRD-PARTY ESTIMATE]** Against the most-cited finding that the M&A failure rate is "between 70% and 90%" (Clayton Christensen et al., *Harvard Business Review*, March 2011: "companies spend more than $2 trillion on acquisitions every year, yet the M&A failure rate is between 70% and 90%") — corroborated by KPMG's 1999 finding that 83% of deals failed to enhance shareholder value — Block's acquisition record (one clean write-off in TIDAL, one clean win in Caviar, one massively-impaired-but-retained bet in Afterpay) is **normal to unusually disciplined on the abandonment axis**. Comparable tech write-offs dwarf Block's: **HP/Autonomy ($8.8bn, 2012)**, **Microsoft/Nokia ($7.6bn, 2015 — exceeding the purchase price)**, **eBay/Skype ($1.4bn, 2007)**. Academic evidence (Potepa & Thomas, *Journal of Financial Reporting*, 2023) finds 65% of "at-risk" large acquisitions impair within two years — TIDAL is a textbook member of that set. **[ANALYTICAL INFERENCE]** The dominant pattern is **cheap experiments quickly killed** (Wallet, Order, Cash App UK/AU, Verse, Clearpay, TBD), with a single **expensive conviction held too long** (TIDAL). Proto is a partial exception — a conviction bet whose cost is R&D rather than a write-off, and whose flagship customer has now exited.

## XIII.8 THE PATTERN

**[ANALYTICAL INFERENCE]**
- **Fast or slow?** Block kills *built products* fast (Order in 10 months, Cash App Australia before launch, Cash App UK once the US-focus decision was taken) but held its one *acquired conviction* (TIDAL) slow — three-plus years and two impairments before winding down. Cheap things die fast; founder-beloved things die slow.
- **Acquisitions vs built products?** The most expensive failures are acquisitions (TIDAL; and, if counted, Afterpay's paper loss). The built-product failures were comparatively cheap — but failed *more often*.
- **Consumer vs merchant?** Failures cluster overwhelmingly in **consumer** (Wallet, Cash App UK/AU, Verse) and **crypto/founder** (TIDAL, TBD, Proto) products. The **Square merchant core has essentially no abandonment record** — its only "retreat" is the quiet, deliberate, value-accretive move upmarket.
- **Founder vs operator?** Failures cluster in **founder-driven** ventures. The two-ecosystem reorganisation and TIDAL were Dorsey's; both were reversed or written off.
- **Does the company learn?** Partially. Killing Verse and Cash App UK quickly, and admitting the two-ecosystem structure was a mistake, are evidence of learning. But the *same weak conviction-process* recurs (TIDAL → TBD → Proto), suggesting Block learns to *exit* faster than it learns to *not enter*.
- **Governance.** Dorsey's **42.2% voting control** (2026 proxy) on a high-single-digit economic stake is directly implicated. The dual-class structure let a 35-minute committee and a founder's personal enthusiasm commit $237m to TIDAL over unanimous executive scepticism, and let the crypto pivot proceed. Dual-class control is what *permits* the conviction bets; it is also what *insulates* the founder from the discipline that would have caught them. The record is the price of that insulation — a price Block, with $10bn+ of gross profit, can pay.

## XIII.9 THE TRANSPLANT VERDICTS

**1. The consumer-product lesson (Square Wallet vs Square Cash).**
- **Verdict: ADOPT the rule, ADAPT the sequencing.** What distinguishes a working consumer financial product from a failing one is whether it delivers standalone value to a single user and spreads pairwise, versus requiring two sides to change behaviour at once. For the Nigerian cooperative context, a member-to-member transfer / remittance feature (one-sided, pairwise, viral) is the Cash App analogue and should be built first; a "pay by name at the cooperative store" merchant-acceptance play is the Wallet analogue and should be deferred until members *already* transact densely. The Guinnane question: Wallet failed because of the *mechanism* (two-sided dependency), not the environment — so it would fail in Nigeria too. **REJECT merchant-dependent consumer payments as a first move; ADOPT the money-movement primitive.**

**2. Acquisition as a growth strategy for a capital-constrained founder.**
- **Verdict: REJECT.** Volume IX already leaned against it; the abandonment record confirms it. Block's *good* acquisition (Caviar) worked partly because Block could afford to hold an unprofitable asset for five years and wait for a buyer war; its *bad* one (TIDAL) cost $237m it could absorb. A capital-constrained founder has neither the holding power nor the loss-absorption. Mechanism vs environment: acquisition failure is a mechanism problem (integration risk, overpayment) amplified by a capital-constrained environment. **Build, partner, or license; do not acquire.**

**3. Founder-conviction ventures under a cooperative structure.**
- **Verdict: ADOPT strict discipline / REJECT unaccountable conviction.** A cooperative's members are owners of a different kind, and the founder has *no* dual-class insulation — a feature, not a bug. The discipline Block lacked (an operator veto; a revenue model at inception; more than a 35-minute review) must be *institutionalised* in the cooperative's governance precisely because the founder cannot override members. Require every new venture to name (a) the tested user job, (b) the revenue model at inception, and (c) at least one senior operator willing to stake their reputation on it — the TIDAL test Block failed.

**4. Killing fast versus holding on.**
- **Verdict: ADOPT killing fast.** The record teaches that cheap, fast kills (Order, Cash App UK) cost little and that the one slow death (TIDAL) cost the most. A founder with one shot should pre-commit to kill criteria *before* launch (e.g., "if member weekly-active rate is below X% after two quarters, we stop"), and be especially ruthless with anything the founder personally loves — that is exactly what Block held too long.

**5. Building for a market you have not tested.**
- **Verdict: ADOPT a testable discipline.** Cash App UK, Verse and Square Wallet all failed at least partly on untested assumptions about user behaviour (that UK users would switch from Revolut/Monzo; that Verse users would monetise; that consumers would prefer pay-by-name to a card). The catchable discipline: **run a falsifiable behavioural pre-test in the actual target market before committing capital** — a small pilot with real members measuring the specific behaviour the business depends on, with a pre-agreed threshold. Every one of these three failures would have been caught by a cheap pilot with a kill threshold.

## XIII.10 VOLUME XIII RECONSTRUCTION

1. **The Square Wallet case and its verdict.** A visionary two-sided product killed by designed-in network dependency; its simultaneous sibling Square Cash, a one-sided pairwise primitive, became 61% of Block. **Verdict: build the one-sided money primitive; defer merchant-dependent consumer payments.**
2. **The five-category catalogue (in full).**
   - *Bought and sold well:* Caviar (2014, ~$44.3–90m → $410m, 2019); Fastbite shut 2016.
   - *Bought and written off:* TIDAL ($237.3m, $205.8m impaired); Verse (2020, wound down 2023, €280k AML fine).
   - *Built and failed:* Square Card Case/Wallet (2011–2014); Square Order (2014–2015); Square Market (absorbed into Weebly-based Online Store); Cash App UK (2018–2024); Cash App Australia (cancelled 2024); Clearpay EU (2023); TBD/Web5 (2022–2024); legacy hardware retirements.
   - *Founder-conviction:* TIDAL; TBD; Spiral; Proto (Core Scientific $41.9m termination); Bitkey; bitcoin treasury.
   - *Strategic retreats:* micro-merchant de-prioritisation (mid-market now 45% of GPV); international withdrawals; lending shift; abandonment of the two-ecosystem model (2024).
3. **Capital arithmetic.** Gross TIDAL write-off ~$206m ≈ 2% of FY2025 gross profit; roughly offset by the ~$320m+ Caviar gain. Net abandonment destruction is modest; Afterpay's ~$12bn+ paper loss is excluded as *retained*, not abandoned. Failure rate is normal-to-disciplined versus the 70–90% M&A benchmark.
4. **Pattern.** Kills built products fast, held its one founder-conviction acquisition slow; failures cluster in consumer and founder-driven ventures; the merchant core is clean; dual-class control (42.2% of the vote) both enabled the bets and insulated them from discipline.
5. **Transplant verdict table.** Consumer primitive: ADOPT/ADAPT. Acquisition-led growth: REJECT. Unaccountable founder conviction: REJECT; institutionalised discipline: ADOPT. Killing fast: ADOPT. Untested-market building: ADOPT pre-test discipline.
6. **Key unknowns.** Exact Verse purchase price; total Wallet/Order/TBD/Proto R&D spend; Proto's own booked losses on Block's side; precise all-in Starbucks cost; the Clearpay-EU-closure date discrepancy (2023 vs the carried-forward 2025).
7. **Ten most important conclusions.**
   1. The Wallet/Cash divergence is the record's central lesson: one-sided pairwise value beats two-sided behaviour change.
   2. TIDAL is the most expensive failure (~$206m written off) and the most instructive on *process* (35-minute review, no operator support).
   3. Caviar is a genuinely good trade and roughly pays for TIDAL.
   4. Block kills cheap things fast and beloved things slow.
   5. Failures cluster in consumer and founder-driven bets; the merchant core is clean.
   6. The conviction bets share one weak process; bitcoin's success and TIDAL's failure came from the *same* process.
   7. The abandonment record is cheap in absolute terms and disciplined versus benchmarks — but only because Block could afford to be wrong.
   8. Dual-class control both enabled and insulated the failures.
   9. Killing Verse/Cash App UK fast, and admitting the two-ecosystem error, are real evidence of learning to *exit*.
   10. The transplant lesson is asymmetric: a one-shot founder should copy Block's exits and reject Block's entries.

**The central answers.** *What did Block abandon and why?* A consumer wallet (network failure), a music service and a decentralised-web unit and a European P2P app (founder conviction / no monetisation), several international consumer operations (competitive defeat dressed as US focus), and its own two-ecosystem structure (admitted error). *Most expensive?* TIDAL. *Most instructive?* Square Wallet. *Fast or slow?* Fast on cheap built products, slow on the one beloved acquisition. *Governance?* Dual-class control (42.2% of the vote) let founder conviction commit capital over operator scepticism and insulated it from correction. *What should a capital-constrained founder take from a record of failures made by a company that could afford them?* **Copy the exits, not the entries.** Build one-sided, tested, pairwise money primitives; pre-commit kill thresholds; refuse acquisition-led growth; and institutionalise the operator-veto and revenue-at-inception discipline that Block's dual-class insulation let it skip — because you cannot afford a single TIDAL, and Block's own record proves the TIDAL was avoidable at the point of entry, not merely at the point of exit.

## Recommendations (staged, with thresholds)

**Stage 0 — before building anything (now).** Institutionalise, in the cooperative's charter, the three-part venture gate that would have caught TIDAL, Verse and Cash App UK: (a) a named, tested user job; (b) a revenue model at inception; (c) a named senior operator (not the founder) who will stake reputation on it. *Threshold to proceed:* all three present, in writing, reviewed for more than one meeting.

**Stage 1 — the first consumer product.** Build the one-sided money-movement primitive (member-to-member transfer / remittance), not a merchant-acceptance product. *Benchmark that would change this:* only after ≥40–50% of members are transacting weekly should a merchant "pay at the co-op store" feature be attempted — the density Wallet never reached.

**Stage 2 — every subsequent product.** Run a falsifiable in-market behavioural pilot before full capital commitment, with a pre-agreed kill threshold. *Threshold to kill:* if the specific behaviour the business depends on (e.g., repeat weekly use, or paid conversion) misses the pre-set bar after two quarters, stop — as Block did with Order and Cash App UK, not as it did with TIDAL.

**Stage 3 — growth.** Grow by building and partnering, not acquiring. *Benchmark that would change this:* revisit acquisition only if the group has both (i) ≥12 months of loss-absorbing capital buffer and (ii) an integration owner — conditions Block met and you likely will not for years.

**Standing rule.** Apply extra scrutiny, not less, to any venture the founder personally loves. The record's clearest governance lesson is that founder conviction is where the expensive, slow failures live.

## Caveats
- **Stated reasons are COMPANY CLAIM.** "Prioritising the United States" and "shifting resources to higher-return areas" are corporate formulations; independent reporting attributes Cash App UK's failure to Revolut/Monzo/Starling competition and Verse's to non-monetisation.
- **The Clearpay EU closure date conflicts** (contemporaneous reporting: 25 August 2023; carried-forward brief: ~25 August 2025). Flagged, not silently resolved.
- **Several costs are UNKNOWN** — Verse's price, R&D on Wallet/Order/TBD/Proto, Block's own Proto losses, all-in Starbucks cost.
- **Afterpay is deliberately excluded** from the abandonment arithmetic as a retained (not abandoned) asset; its ~$12bn+ paper destruction belongs to Volume IX.
- **The M&A failure-rate benchmark (70–90%) has a definitional range** — "failure" variously means stock decline, missed synergies, or divestiture — so it anchors judgement rather than proving a precise comparison.
- **Caviar's cost basis is genuinely ambiguous** (reported ~$90m vs filing $44.3m); the realised-gain range reflects this, not analyst imprecision.

---

# VOLUME XIV — The Transplant Volume

---

## The assumed starting position

This volume prescribes a sequence, and a sequence needs a starting point. The one assumed here is: **the platform is unbuilt or early; no cooperative society has yet been registered; and available capital is approximately ₦50 million — enough to fund the platform or to buy one Super-Agent licence, but not both.**

If any of that has moved, the sequencing in XIV.7 needs revisiting before it is acted on. A build order derived from the wrong starting position is worse than no build order, because it carries the authority of thirteen volumes behind a false premise.

---

## XIV.1 What thirteen volumes found

Block was selected because it looked like a roadmap: a technology company that started with a card reader for merchants nobody would underwrite, built a consumer product alongside it, acquired its own bank, and now generates $10.36bn of annual gross profit across both. The reader's own architecture — a platform, a cooperative, a remittance capability, credit as a feature — is structurally the same bet.

**The study found that the bet is half right, and that the wrong half is the half most people believe in.**

The mechanisms transfer better than expected. Flow-based underwriting, settlement-controlled repayment, software as the margin engine, and the bank-partnership-first licence sequence are all genuinely portable, and several of them are *easier* in Nigeria than in the United States. That is the good news, and it is substantial.

**What does not transfer is the compounding.** Block spent a decade and effectively unlimited capital trying to make its two ecosystems reinforce each other, bought a $13.84bn company explicitly to bridge them, and — on the evidence of Volume XI — never demonstrated customer-level compounding at all. It achieved shared infrastructure, which is real and valuable. It did not achieve shared customers.

That finding is uncomfortable, because the reader's four-layer architecture rests on precisely the assumption Block could not vindicate. It is also the single most valuable thing in the study, and it arrives early enough to act on.

---

## XIV.2 The compounding verdict — the spine of this volume

### What the evidence showed

Five volumes converged on the same answer from different directions, none of them looking for it:

**Volume VI** examined the machinery and found **roughly one-and-a-half machines**: a genuinely shared spine — one cloud, a twelve-petabyte data platform serving about seventy teams, one machine-learning and underwriting engine, shared risk and fraud infrastructure — sitting beneath **two separate consumer-facing identity systems**. A Square seller login and a Cash App login are different accounts. Cash App Pay, the most-cited integration, turned out to be a QR-and-deep-link payment bridge rather than an identity merger.

**Volume VIII** priced the two businesses separately and found the economics **diverging**, not converging: Cash App gross profit $6.34bn growing 21%, Square $3.94bn growing 9%, with different margins, different capital intensity and different cyclicality.

**Volume XII** found that only one half **exported**. Square operates in eight countries with international at 22% of gross payment volume growing 35%. Cash App withdrew from the United Kingdom, cancelled Australia before launch, and wound down Verse in Europe.

**Volume XIII** found the failures **clustered on one side**: nearly every abandonment is a consumer product or a founder-conviction bet, while the merchant core has essentially no abandonment record at all.

**Volume XI** put the question directly and found the answer in an absence. Block has asserted ecosystem synergy for years. It has **never published a person-level figure for customers active on both sides** — not in a filing, not in a shareholder letter, not in an investor-day deck. Afterpay, acquired for $13.84bn explicitly to be "the connector," has after four years connected Cash App consumers to *external* merchants rather than to Square sellers. Neighborhoods, the most concrete cross-ecosystem product, reached roughly $1bn of annualised gross payment volume — about **0.4% of Square's $250.5bn**.

### The verdict

**Block's two ecosystems coexist on shared plumbing. They do not compound at the customer level.**

Proportionally: infrastructure compounding is real and material; customer compounding is near zero. And Block itself effectively conceded the point — the September 2024 functional reorganisation dissolved the two-company structure, with Dorsey admitting he "incorrectly built 2 separate company structures (square & cash app) rather than 1."

### What it means for a four-layer architecture

The naive reading is that the reader's plan is therefore wrong. That reading is too quick, and the study does not support it.

**There is one structural difference, and it may be decisive.** Block's two ecosystems had no shared identity — a consumer and a seller were different people with different logins and no reason to be linked. **A cooperative member is one person with one membership across every product the group offers.** The identity Block never built is, for the reader, the founding fact of the institution. The cooperative *is* the joined graph.

But that difference is **conditional, not automatic**, and the condition is exactly what Block failed:

- The reader must build **one member identity spanning platform, cooperative, remittance and credit from day one** — not four products that each know a member separately.
- The reader must **act on the joined graph** — cross-sell, underwriting, acquisition cost — rather than merely possess it.
- The reader must **measure it**. Block's silence on the overlap metric is the tell. A synergy you cannot report is a synergy you do not have.

If the reader ends up with separate identities per product, the cooperative advantage evaporates and he will have rebuilt Block's failure with less capital. If he builds the single member spine first, he starts where Block never arrived.

**So the four-layer architecture survives — but as an identity architecture rather than an adjacency architecture.** The layers do not compound because they are adjacent. They compound only if one member identity runs through all of them and the group acts on what that identity reveals.

---

## XIV.3 The master verdict table

Sixty-one adjudications from thirteen volumes. The distribution is close to even thirds, which is itself informative: this is neither a playbook to copy nor a cautionary tale to discard.

**ADOPT 21 · ADAPT 20 · REJECT 20**

### ADOPT — transfers on its own logic

| # | Mechanism | Vol | Note |
|---|---|---|---|
| 1 | Flow-based underwriting on proprietary transaction data | V | The prize; dissolves the thin-file problem |
| 2 | Settlement-controlled repayment (deduct before the borrower is paid) | V, VII | Deepest transferable mechanism in the study |
| 3 | Offer-driven, pre-approved origination | V | Cheap operationally; needs longitudinal data |
| 4 | Consumer lending gated on observed inflows | IV, V | Contribution flow is the analogue |
| 5 | Cooperative contribution flow as the "direct deposit" event | IV | The master conversion signal |
| 6 | Bank-partnership-first licence sequence | II | Square ran it 2014–2021 profitably |
| 7 | Instant onboarding via aggregation | III | **The cooperative *is* the payment facilitator** |
| 8 | Software and integrated services as the margin engine | III, VIII | ~59% of Square gross profit |
| 9 | Build ONE platform, not several | VI | Block's costliest structural error |
| 10 | One unified data estate from day one | VI | Block retrofitted; reader can build it |
| 11 | Gross profit as the governing metric | VIII | Reader's distortion is remittance turnover |
| 12 | Multi-product attach as the unit-economics driver | IV, VIII | The ~10× primary-banking multiple |
| 13 | Sequence compliance ahead of scale | II, VI | The non-negotiable inversion of Block's playbook |
| 14 | Shared infrastructure (not shared customers) | XI | The compounding that is actually achievable |
| 15 | Settlement-controlled credit as the first moat | XI | Scored 5/5 twice on the moat scorecard |
| 16 | Seller/merchant side before consumer side | XII | Square exported; Cash App did not |
| 17 | Partner-led entry in a cash-dominant market | XII | The Japan/SMCC model |
| 18 | Killing fast, with pre-committed thresholds | XIII | Block's exits are better than its entries |
| 19 | Pre-testing behaviour in the actual market | XIII | Would have caught three of Block's failures |
| 20 | The operator-veto discipline | X, XIII | Institutionalise what Block could override |
| 21 | Serving micro-merchants — *conditionally* | III | Only as a channel to savings, credit, software |

### ADAPT — the logic transfers, the implementation must change

| # | Mechanism | Vol | What must change |
|---|---|---|---|
| 22 | Repayment as % of daily processing volume | V | **Hardest verdict.** Cash dominates; apply to contribution flows, not card sales |
| 23 | Merchant-acquiring take-rate model | VII, XII | 0.5% MSC cap vs Square's 1.6–2.6%; monetise software, not transactions |
| 24 | Deposit-taking as a funding strategy | II, IX | Only inside an NDIC-insured MFB; heavy trust-building |
| 25 | Funding a loan book from a licensed subsidiary | V, IX | ~₦1 of regulatory capital per ₦5–8 lent |
| 26 | Holding-company-over-licensed-subsidiary | I | CBN FHC framework: 51% stake, 20% buffer |
| 27 | Ring-fencing a regulated entity | I | Build CALMA/PCA analogues from day one |
| 28 | Customer-fund safeguarding | IX | Segregated, never commingled, never budgeted as capital |
| 29 | Float as a revenue source | VII, IX | A bonus, not a pillar; balances turn over fast |
| 30 | Land-and-expand across products | III, VIII | Sequence savings and credit first, software second |
| 31 | Real-time risk and fraud scoring | VI | Rules first, ML later; must work offline and over USSD |
| 32 | AI as operating leverage | VI | Engineering and drafting only; never regulated judgment |
| 33 | Cash Card and interchange monetisation | IV, VII | Cannot fund the model; utility feature only |
| 34 | Free P2P as an acquisition engine | VII | NIP already commoditised it; the hook must change |
| 35 | Lending as the margin engine | VIII | Underwrite to a loss ceiling 2–4× Block's |
| 36 | Founder control without dual-class insulation | X | Ownership in the vendor entity, not the cooperative |
| 37 | Entering against entrenched incumbents | XII, XI | Narrow and deep, not broad |
| 38 | The compounding assumption itself | XI | Conditional on building the member graph first |
| 39 | Consumer-product design | XIII | One-sided pairwise value, never two-sided behaviour change |
| 40 | Localisation sequencing | XII | Licence and software first; hardware and P2P last |
| 41 | Growth by acquisition | IX, XIII | Only for a licence or deposit base, only for cash |

### REJECT — depends on institutions the target market lacks

| # | Mechanism | Vol | The dependency that kills it |
|---|---|---|---|
| 42 | **Interchange as a subsidy for free consumer products** | VII, XII | **No Nigerian equivalent. The decisive finding** |
| 43 | Selling settlement speed | VII, XII | NIP already closed the gap — Nigeria is ahead |
| 44 | The industrial-bank charter | I, II | No BHCA-exception analogue; map to an MFB licence |
| 45 | Escaping consolidated group supervision | I | CBN will consolidate everything; accept it |
| 46 | Free or subsidised hardware as a wedge | III, VIII | No spread to fund it; hardware is imported |
| 47 | The viral consumer acquisition engine | IV | The cooperative already delivers members |
| 48 | Free P2P transfer as the wedge | IV, VII | Nothing left to open; incumbents hold the ground |
| 49 | Warehouse and forward-flow funding | II, IX | No deep Nigerian loan-buying market |
| 50 | Selling loans to institutional investors | V | Same absence |
| 51 | State-by-state licensing burden | II | Nigeria's single CBN regime is *easier* |
| 52 | Compliance built after scaling | II, VI | Block absorbed ~$340m; the reader cannot |
| 53 | Holding a volatile treasury asset at the parent | I, IX | Barred under the FHC framework |
| 54 | Mass-market crypto and investing products | IV | Inappropriate to a fiduciary cooperative |
| 55 | Owning a cooperative and a bank in one group | I | **Block offers no precedent; the analogy runs out** |
| 56 | Assuming shared customers follow shared infrastructure | XI | The study's central negative finding |
| 57 | Share repurchases and heavy equity compensation | IX, X | Meaningless or misaligned under mutual ownership |
| 58 | The non-GAAP presentation habit | VIII, X | Members and the CBN will read it as a red flag |
| 59 | Combining chief operating and chief financial roles | X | Key-person risk a small group cannot absorb |
| 60 | Risk leadership reporting only to the chief executive | X | It failed at Block; use the SFS board model |
| 61 | Announcing through the founder's personal channels | X | A regulatory hazard for a licensed entity |

---

## XIV.4 The five mechanisms worth the whole study

Stripped of everything else, five things justify the programme.

**One. Underwrite on the flow you already process.** Block does not ask a bureau who a borrower is; it observes what money they actually move. For a market where bureau coverage reaches roughly 13% of adults, this dissolves rather than solves the thin-file problem. The reader's platform will see cooperative member transactions directly. *This is the single most valuable idea in the study.*

**Two. Collect out of that same flow, before the borrower touches it.** Square Loans repay as a fixed percentage of daily card sales, deducted **pre-settlement**. This is the deeper half and the more neglected one. It converts a credit-risk problem into a cash-flow-interception problem, which is why loss rates stay under 3% on a population no bank would underwrite. Volume V found the collection mechanism matters more than the model.

**Three. The aggregation you need already exists.** Square had to *build* the payment-facilitator structure that let it onboard millions of micro-merchants without underwriting each one. A cooperative society **is** that structure — pre-aggregated, socially collateralised, with a savings relationship already running. Block manufactured over a decade what the reader starts with.

**Four. Software is the business; payments is the wedge.** Roughly 59% of Square's gross profit comes from software and integrated services. Under a 0.5% capped merchant service charge this stops being an observation and becomes a constraint: **there is no payment spread to build a business on in Nigeria.** The margin has to come from software, credit and savings intermediation, or it does not come at all.

**Five. Build one platform.** Block's costliest structural error was two company structures where one was needed, and it took a decade and a 40% workforce reduction to correct. The reader can simply not make it.

---

## XIV.5 The five that do not transfer, and why it matters

**One. Interchange.** Uncapped American small-issuer debit interchange averaged about $0.62 per transaction in 2023. That pool silently funds free peer-to-peer transfer, free cash-out, cashback and customer acquisition across American consumer fintech. Nigeria's merchant service charge is capped at 0.5% with a ₦10,000 ceiling, and the issuer's slice is a fraction of a percent.

**Every "free" feature in the reader's plan needs a named paying line.** Not a hope that scale will fix it. A line.

Volume XII then supplied the natural experiment: Cash App entered the United Kingdom and Europe, where the Interchange Fee Regulation caps consumer debit at 0.2%, and withdrew from both. Square, in the same capped markets, is profitable — because Square earns the merchant fee it sets plus software, while Cash App earns interchange it does not control. **The seller model survives capped interchange; the consumer model does not.** That is as close to a controlled experiment as this material offers.

**Two. Settlement speed.** Block's most elegant product charges 0.5–1.75% for instant access to money the customer already owns — a product that exists only because standard American settlement is slow. NIP already makes Nigerian interbank transfers real-time and cheap. **There is almost no time left to sell.** This is Nigeria being ahead, not behind, and the reader should stop looking for the American answer here.

**Three. The industrial bank charter.** The device that let a commercial parent own an insured bank without central-bank group supervision has no Nigerian analogue. What it *bought* — deposit funding, retained lending, independence from a partner's risk appetite — maps onto a microfinance-bank licence. What it *avoided* cannot be avoided: the CBN will consolidate the whole group.

**Four. Compliance after scale.** Block scaled Cash App to tens of millions of users and retrofitted controls under roughly $340m of enforcement pressure, plus a $240m Department of Justice reserve, an independent monitor and an independent consultant. It survived because it had the balance sheet. **A single CBN or NFIU sanction is terminal for a capital-constrained founder.** This is the one place where copying Block would be fatal, and the inversion is non-negotiable.

**Five. The compounding assumption.** Addressed at XIV.2 and running through everything below.

---

## XIV.6 What Nigeria has that America does not

The transplant test is usually assumed to run one way. It does not. Four asymmetries favour the reader, and building as though they do not exist wastes them.

**A single national regulator.** Block maintains forty-eight-plus state money-transmitter licences with separate bonds, net-worth tests and renewal calendars — and paid $80m to forty-eight state regulators and $45m to forty-six state attorneys general in settlements. Nigeria has one CBN rulebook. Volume II's verdict was explicit: this is a **structural advantage**, not a hardship. The trade-off is concentration — one sanction hits everything — so the examination record has to be unimpeachable.

**Instant payment rails that already work.** NIP has been ubiquitous for years, while the United States arrived late via RTP and FedNow and still runs on ACH. Nigeria leapfrogged. The consequence is that a whole category of American fintech product — selling speed — has no market, and the engineering effort should go elsewhere.

**Pre-aggregated distribution with social collateral.** Cash App's near-zero customer acquisition cost is the most admired number in consumer fintech, and it cost roughly $340m in deferred compliance penalties to achieve. The cooperative delivers members already assembled, already saving, already known to one another. **The reader should not build an acquisition engine. He should build the monetisation ladder that sits on top of one.**

**One member identity across every product** — the asset Block never had and could not manufacture. See XIV.2.

---

## XIV.7 The build order

Sequenced by dependency and capital, with tests rather than instructions. The thresholds are the point: each stage states what would tell you to proceed, and what would tell you to stop.

### Stage 0 — Before anything is built

**Governance and identity architecture.** These are cheap now and structurally impossible to retrofit later.

- Write the **operator-veto rule** into the constitution and board charter: no product, capital commitment or partnership above a stated threshold proceeds without documented sign-off from someone empowered to refuse. Volume XIII found Block's failures clustered where nobody could say no; the reader has no dual-class insulation, which is an advantage to be engineered rather than a limitation.
- Fix the **entity perimeter**: the platform stays founder-owned and *outside* the eventual financial holding company, as an arm's-length vendor. The CBN's draft framework bars a holding company from owning non-financial businesses, so a platform inside the group is a structural problem later.
- Specify **one member identity** spanning every product the group will ever offer. This is the decision the entire compounding thesis rests on.
- Appoint a **compliance officer and write the AML/CFT programme before the first member is onboarded.**

*Test to proceed:* the operator-veto rule exists in writing, the perimeter is drawn, and one identity schema covers all four planned layers.

### Stage 1 — The platform and the anchor cooperative

Build the core-banking platform and register the anchor society. Get member contribution, repayment and transfer flows running **electronically and on-platform**, with longitudinal history stored from the first transaction.

*Test to proceed:* **at least 60–70% of member money movements are electronic and on-platform.** Below that, the flow is too thin to underwrite or intercept, and Stage 3 must wait. This is the hardest threshold in the sequence and the one most likely to bind.

*Signal to stop:* if members will not route money through the platform after sustained effort, the flow-based model does not apply and the venture is a software business, not a financial one. Better to learn that at Stage 1 than at Stage 4.

### Stage 2 — Partnership, not licence

Operate under a licensed partner's authority — the Square/Celtic posture, which ran profitably for five years and scaled to billions in volume. Do not chase a licence yet; ₦50 million buys the platform or one Super-Agent licence, not both, and the platform is the appreciating asset.

*Test to proceed to Stage 3:* the fee paid away to the partner exceeds what could be earned holding the same business on your own balance sheet. Model it annually. **That crossover is the signal to pursue a licence — not ambition, not a round number.**

### Stage 3 — Credit as a platform feature

The prize. Lend against observed contribution history; **collect at source, from the contribution before the member receives it.** Start small — the Cash App Borrow analogue, not the Square Loans analogue — and grow limits with demonstrated repayment.

*Test to scale:* observed loss rates hold below your pre-set ceiling for two consecutive cohorts. Underwrite to **2–4× Block's sub-3%**, given weaker collections and thinner data.

*Signal to stop:* losses double from plan. On Block's own ratios that erases roughly a quarter of lending gross profit, and a capital-constrained lender does not get a second cohort to fix it.

### Stage 4 — The deposit licence

Pursue a **Unit or State microfinance-bank licence** — the functional equivalent of what the industrial-bank charter bought Block, at the lowest Nigerian capital. Not a Payment Service Bank: PSBs generally cannot lend, and lending is the point.

Fund the book from **NDIC-insured member deposits**, not from a forward-flow market Nigeria does not have. Note that this is where Block arrived only in 2025, after a decade of selling loans — **the reader can start there.**

*Never:* hold member savings outside deposit insurance to fund lending. That is the structure Nigerian regulators and the public associate with fraud, and it is the fastest route to a run.

### Stage 5 — Remittance

Climb via agency, since the IMTO regime requires USD 1m and bars fintechs from holding the licence directly. Same rent-the-charter logic as Stages 2 and 4. Confirm current CBN guidelines before committing capital.

### Deferred indefinitely

Consumer peer-to-peer as a headline product; proprietary hardware; anything sold as "instant"; speculative crypto; acquisitions.

---

## XIV.8 The measurement that decides everything

One instrument determines whether the four-layer thesis is working, and Block's failure to build it is the study's clearest lesson.

**Report, monthly, the share of members active in two or more layers, and the contribution per member of that group against single-layer members.**

Block asserted ecosystem synergy for years and never published the equivalent number. Volume XI concluded that the absence *was* the answer.

The reader should hold himself to the standard Block avoided:

- If multi-layer members show **materially higher contribution and lower servicing cost** than single-layer members within three quarters, the compounding thesis is live and the architecture is earning its complexity.
- If they do not, **each layer must justify itself standalone** — or be cut. Adjacency alone is not a reason for a layer to exist, and the study demonstrates that at scale.

**A synergy you cannot measure is a synergy you do not have.**

---

## XIV.9 What this study cannot tell you

Fourteen volumes of a foreign company cannot substitute for evidence from the reader's own market, and four things remain genuinely open.

**Whether Nigerian cooperative members will route money electronically at the rate the model requires.** Everything downstream — underwriting, interception, compounding — rests on it, and no amount of American evidence settles it. It is an empirical question answerable only by a pilot.

**Whether a cooperative society and a CBN-licensed entity can sit coherently in one group.** Volume I was explicit that Block offers no precedent: it never owned an entity registered under a different body of law and answering to a different regulator. This needs Nigerian counsel, not analogy.

**Whether the reader's regulatory assumptions still hold.** The CBN's financial-holding-company framework was in draft; capital thresholds, the merchant-service-charge cap and the IMTO regime all move. Every figure in this study touching Nigerian regulation should be re-verified against current circulars before capital is committed.

**Whether the cooperative's shared identity actually delivers what Block's separate logins could not.** This is the load-bearing hypothesis of XIV.2, and it is a hypothesis. It is more plausible than Block's version because the identity genuinely is unified — but plausibility is not evidence, and the measurement at XIV.8 exists precisely to test it rather than assume it.

---

## XIV.10 The closing judgement

Block was worth fourteen volumes, but not for the reason the exercise began.

It is not a roadmap. Its capital allocation was founder-driven and uneven; its governance permitted a $237m acquisition to pass through a thirty-five-minute committee with no executive support; its compliance lagged its licensing by years and roughly $340m; and its central strategic claim — that two ecosystems compound — is unproven after a decade of trying.

**What it is, is the most thoroughly documented natural experiment available** in exactly the transfer the reader is attempting. It ran the seller model and the consumer model side by side and only one exported. It built free peer-to-peer where interchange funds it and withdrew where interchange is capped. It rented a charter for five years before buying one. It scaled first and paid for compliance later, and the bill is public.

The honest summary is this. **The mechanisms transfer; the economics do not; and the compounding has to be built rather than assumed.** Block could afford to be wrong about all three. The reader cannot, which is why the sequence in XIV.7 front-loads the cheap, irreversible decisions — governance, perimeter, identity, compliance — and defers everything that can be bought later with money that does not yet exist.

Copy the exits, not the entries. Build one platform, one identity, one compliance function, and one measurement that would tell you honestly if the whole thesis were failing.

Then find out whether Nigerian cooperative members will put their money through it — because nothing in these fourteen volumes can answer that, and everything depends on it.

---

# APPENDIX A — GLOSSARY

*This study spans American payments, banking regulation, credit accounting and the Nigerian regulatory ladder. Read this before Volumes V, VII or IX.*

## A.1 Payments and the rails

| Term | Meaning |
|---|---|
| **Payment facilitator (PayFac)** | An entity that aggregates many small merchants as "sub-merchants" under its own master merchant account, letting them onboard in hours rather than being underwritten individually. **Square pioneered this; a cooperative society performs the same aggregating function** |
| **Sponsoring acquirer / Member bank** | The licensed bank that ultimately stands behind card acceptance. Historically JPMorgan Chase for Square, with Paymentech processing |
| **Merchant discount rate (MDR)** | The total fee a merchant pays per transaction. Square US: 2.6% + 15¢ card-present. **Nigeria caps the equivalent merchant service charge at 0.5%** |
| **Interchange** | The portion of the merchant fee paid to the cardholder's issuing bank — typically 70–80% of the MDR in the US. **The hidden subsidy funding American consumer fintech** |
| **Durbin Amendment / Regulation II** | Caps US debit interchange for issuers with $10bn or more in assets. Smaller issuers are **exempt** and earn far more — averaging about $0.62 per transaction in 2023. Block's partner banks are all exempt |
| **Interchange Fee Regulation (IFR)** | The EU and UK regime capping consumer debit interchange at 0.2% and credit at 0.3%, with **no small-issuer exemption** |
| **Gross payment volume (GPV)** | Total value of transactions processed. Square: $250.5bn in 2025 |
| **Take rate** | Revenue or gross profit as a percentage of volume. Square transaction gross profit ≈1.13–1.15% of GPV |
| **Push-to-card** | Rails (Visa Direct, Mastercard Send) delivering funds to a debit card in near-real time; how Block provides Instant Deposit |
| **NIBSS Instant Payment (NIP)** | Nigeria's real-time interbank transfer rail, ubiquitous for years and cheap. **Nigeria leapfrogged the United States here** |

## A.2 Banking, licences and regulation

| Term | Meaning |
|---|---|
| **Industrial loan company (ILC) / industrial bank** | A Utah-chartered, FDIC-insured bank whose commercial parent escapes Bank Holding Company Act supervision. **The structural device at the centre of Block's group — with no Nigerian equivalent** |
| **Square Financial Services (SFS)** | Block's Utah industrial bank, operational 1 March 2021, carrying a permanent **20% leverage-ratio requirement** — roughly four times a normal bank's |
| **CALMA / Parent Company Agreement** | The FDIC-imposed Capital and Liquidity Maintenance Agreement and reporting undertaking that ring-fence SFS, binding Block **and Jack Dorsey personally** |
| **Sections 23A / 23B and Regulation W** | Federal limits on transactions between a bank and its affiliates, capping and collateralising intra-group dealings |
| **Money transmitter licence (MTL)** | A state-by-state permission to hold and move customer funds; Block holds 48-plus. **Nigeria's single national CBN regime is materially easier** |
| **Financial Holding Company (FHC) framework** | The CBN regime governing Nigerian groups: minimum 51% subsidiary stakes, paid-in capital at least 20% above the sum of subsidiary minimums, no cross-subsidy of deficits, and — in draft — a bar on owning non-financial businesses |
| **Microfinance bank (MFB) licence** | The Nigerian deposit-taking-and-lending licence. Tiers: Unit (₦50m–₦200m), State (₦1bn), National (₦5bn). **The functional analogue of what the ILC charter bought Block** |
| **Payment Service Bank (PSB)** | A ₦5bn Nigerian licence permitting deposits but generally **not lending** — the wrong tool for a credit-led model |
| **IMTO** | International Money Transfer Operator; the Nigerian remittance licence requiring USD 1m and barring fintechs from holding it directly |
| **NDIC** | The Nigeria Deposit Insurance Corporation — the FDIC analogue, with lower limits and thinner public trust |

## A.3 Credit and its accounting

| Term | Meaning |
|---|---|
| **Flow-based underwriting** | Assessing a borrower on the payment flow the lender already processes rather than a bureau file. **The study's central transferable idea** |
| **Settlement-controlled repayment** | Deducting loan repayment from sales or inflows **before the borrower is paid**. Square Loans take a fixed percentage of daily card sales pre-settlement |
| **Holdback** | That fixed percentage — commonly 9–13% for Square Loans |
| **Factor rate** | A flat multiplier rather than an interest rate: borrow $10,000 at 1.13, repay $11,300. No compounding, no benefit to early repayment |
| **Merchant cash advance (MCA)** | A purchase of future receivables rather than a loan — historically outside usury and licensing rules. **Square used it 2014–2016 and deliberately abandoned it** |
| **CECL** | The US expected-credit-loss standard, front-loading lifetime expected losses at origination. **Why a fast-growing loan book reports rising provisions even when underwriting is stable** |
| **Held for investment vs held for sale** | Whether a loan is retained or sold. Block's shift from selling to retaining, from 1 July 2025, drove loans held for investment from $365.1m to $3.383bn |
| **Forward flow** | An agreement to sell newly originated loans to an investor on a rolling basis. **Nigeria has no deep market for this** |
| **Buy now, pay later (BNPL)** | Short-term instalment credit at checkout — Afterpay in the US, Australia and New Zealand; Clearpay in the UK |

## A.4 Structure and metrics

| Term | Meaning |
|---|---|
| **Gross profit** | Block's headline metric, and the only honest one given the bitcoin revenue distortion |
| **Monthly transacting active** | A Cash App user transacting in a given month — 59 million at December 2025 |
| **Primary-banking active** | A Cash App user who direct-deposits. **Worth nearly ten times a peer-to-peer-only active** — the most striking number in the study |
| **Dual-class structure** | Class A (one vote) and Class B (ten votes), giving Dorsey roughly **42.2% of voting power** on a high-single-digit economic stake |
| **Rule of 40** | Block's self-selected measure combining gross-profit growth with adjusted operating margin. Scrutinise rather than repeat |

---

# APPENDIX B — CANONICAL FIGURES REGISTER

**Where any volume disagrees with this table, this table governs.** Compiled 11 August 2026.

## B.1 Group results — Block, Inc., USD, US GAAP

| USD m | FY2023 | FY2024 | FY2025 |
|---|---|---|---|
| Total net revenue | 21,916 | 24,121 | **24,194** |
| — of which bitcoin | ~9,498 | 10,358 | **8,503** |
| **Gross profit** | **7,505** | **8,889** | **10,360** |
| — Square segment | ~3,130 | ~3,600 | **3,940** |
| — Cash App segment | 4,323 | 5,239 | **6,340** |
| Product development | — | 2,914 | 2,908 |
| Sales & marketing | — | 1,984 | 2,273 |
| General & administrative | — | 2,149 | 1,998 |
| **Transaction, loan & receivable losses** | 661 | 794 | **1,337** |
| Operating income | 259 | 892 | **1,708** |
| Net income to common | 10 | **2,866** | 1,306 |
| Share-based compensation | 1,276 | 1,273 | **1,215** |
| Operating cash flow | 101 | 1,707 | **2,580** |
| Adjusted EBITDA | 1,790 | 3,030 | 3,470 |
| Adjusted Operating Income | ~360 | 1,610 | 2,080 |

**Two warnings on this table.** FY2024 net income was inflated by approximately **$1.9bn of one-time tax benefits** plus a $421m bitcoin gain — the apparent 2024→2025 decline is an artifact, and operating income actually rose 91%. And bitcoin revenue fell 18% in FY2025 while everything else grew about 14%, so total revenue looks flat and is not.

## B.2 Operating metrics — dated, because they move

| Metric | FY2023 | FY2024 | FY2025 |
|---|---|---|---|
| Square GPV ($bn) | ~210 | 227.6 | **250.5** |
| Square sellers (m) | ~4 | ~4 | **4.5+** |
| Cash App monthly actives (m, Dec) | 56 | 57 | **59** |
| Cash App Card actives (m) | — | ~24 | **26** |
| Primary-banking actives (m, Dec) | ~6.4 | 7.6 | **9.3** |
| Cash App inflows ($bn) | 248 | 283 | **316** |
| Gross profit per monthly active ($) | ~67 | 76 | **~107** |

**Mid-market GPV share (sellers above $500k annualised):** ~24% (2018) → 34% (Q3 2021) → 41% (Q3 2023) → **45% (Q3 2025)**.

## B.3 The credit book

| Item | FY2024 | FY2025 |
|---|---|---|
| Loans held for investment, net ($m) | 365.1 | **3,383.0** |
| Allowance for credit losses ($m) | 23.1 | **382.9** |
| Consumer receivables, net ($m) | 2,504.9 | 2,670.3 |
| Provision on loans held for investment ($m) | — | 561.4 |
| Write-offs / recoveries ($m) | — | 216.5 / 14.8 |

Loss rates (COMPANY CLAIM, tested in Volume V): **Square Loans ≤4%** since 2016; **Cash App Borrow <3%** since 2022; **BNPL ~1%** since 2023. Volume VIII decomposed the FY2025 loss line as roughly **two-thirds a growth signal** (CECL front-loading on a book that grew ninefold) **and one-third a control signal**.

## B.4 Capital and the balance sheet (31 December 2025)

| Item | USD |
|---|---|
| Total assets | 39,549,887k |
| Total liabilities | 17,380,005k |
| Total stockholders' equity | ~22,169,882k |
| **Customer funds** (not Block's money) | 4,771,824k |
| **Customers payable** (not Block's money) | 6,805,366k |
| Settlements receivable | 1,359,983k |
| Cash and equivalents | 6,564,092k |
| **Notes outstanding, net carrying** | **7,289,018k** (principal 7,350,000k) |
| Warehouse facilities | 1,364,883k |
| Goodwill | 11,849,018k |
| Acquired intangibles, net | 1,281,670k |
| **Bitcoin (investment)** | **777,515k** (8,883 BTC, cost basis 292.6m) |

**Genuine leverage.** Strip the customer money and real corporate financing is ~$8.65bn against ~$22.17bn of equity — about 0.39×. Net of cash and securities, **net debt is roughly $1.4bn.** Block is barely levered; Fitch rates it BBB–. *See Appendix E note 1 on the "$0 long-term debt" correction.*

## B.5 Square Financial Services — the ring-fenced bank

| Item | Value | Basis |
|---|---|---|
| Opened | **1 March 2021** | FDIC / Utah DFI |
| Initial paid-in capital | ~$56m | FDIC order |
| **Permanent leverage requirement** | **≥20%** | CALMA — roughly 4× a normal bank |
| Equity (Q3 2025) | ~$845m | Call-report derived |
| Total assets / loans / deposits (30 Sep 2025) | $1,354m / $757m / $421m | FDIC call report |
| Dividends paid to group | **None** | Three-year bar lapsed ~March 2024 |

**The trap:** SFS's ~$421m of deposits does not fund a $3.38bn loan book. The parent does.

## B.6 Corporate and enforcement

| Item | Value |
|---|---|
| Founded | 2009, Delaware, by Jack Dorsey and Jim McKelvey |
| IPO | 18 November 2015 at **$9.00**; closed first day at $13.07 |
| Renamed Block | 1 December 2021 (announced); ticker SQ → **XYZ** on 21 January 2025 |
| Dorsey voting power | **~42.2%** on a high-single-digit economic stake |
| Dorsey salary | **$2.75** |
| Workforce | 10,205 FTE at 31 Dec 2025 → **under 6,000** under the February 2026 plan |
| Restructuring charges | $450–500m announced; **~$852m** reported; $495.3m recorded in Q1 2026 |
| **Enforcement, 2025–26** | **~$340m** total |
| — CFPB (16 Jan 2025) | $175m ($55m penalty + up to $120m redress) |
| — 48 state regulators (15 Jan 2025) | $80m |
| — NYDFS (10 Apr 2025) | $40m |
| — 46 state attorneys general (8 Jul 2026) | $45m |
| — Washington State (8 Jul 2026) | $20m |
| DOJ reserve | **$240m**, unresolved |

## B.7 Acquisitions and disposals

| Target | Date | Consideration | Outcome |
|---|---|---|---|
| **Caviar** | 2014 | ~$90m reported / **$44.3m** per filing | **Sold to DoorDash for $410m**, closed 31 Oct 2019 |
| Weebly | closed 31 May 2018 | ~$365m | Absorbed into Square Online |
| Credit Karma Tax | 2020 | ~$50m | Became Cash App Taxes |
| Verse | 15 Jun 2020 | undisclosed | **Wound down September 2023** |
| **TIDAL** | closed 30 Apr 2021 | **$237.3m for 86.23%** | **Goodwill written off: $132.3m (Q4 2023) + $73.5m (Q4 2024)** |
| **Afterpay** | announced 1 Aug 2021, closed 31 Jan 2022 | **~$29bn announced; $13,836,622k at close** (113,617,352 Class A shares) | $11.72bn goodwill, split 50/50, **never impaired and untestable** |

**On the two Afterpay numbers.** Both are correct. The ~$29bn was the August 2021 announcement value; because Block paid in its own stock and its share price fell before closing, the accounting consideration was $13.84bn. The gap is not a discrepancy — it is the structural risk of paying in volatile equity, and Volume XIII treats it as such.

---

# APPENDIX C — THE TRANSPLANT INDEX

All sixty-one verdicts, indexed by mechanism for lookup. **Volume XIV.3 presents them grouped by verdict with full reasoning; this appendix is the alphabetical finding aid.**

| Mechanism | Verdict | Vol |
|---|---|---|
| Acquisition as growth strategy | REJECT | IX, XIII |
| AI as operating leverage | ADAPT | VI |
| Bank-partnership-first sequence | **ADOPT** | II |
| Buybacks and equity compensation | REJECT | IX, X |
| Cash Card / interchange monetisation | ADAPT | IV, VII |
| Charging for settlement speed | **REJECT** | VII, XII |
| Combining COO and CFO roles | REJECT | X |
| Compliance built after scaling | **REJECT** | II, VI |
| Compounding assumption itself | ADAPT (conditional) | XI |
| Consumer lending on observed inflows | **ADOPT** | IV, V |
| Consumer-product design (one-sided value) | ADAPT | XIII |
| Cooperative + licensed bank in one group | REJECT (no precedent) | I |
| Cooperative contribution flow as conversion event | **ADOPT** | IV |
| Customer-fund safeguarding | ADAPT | IX |
| Deposit-taking as funding | ADAPT | II, IX |
| Escaping consolidated supervision | REJECT | I |
| Float as revenue | ADAPT | VII, IX |
| Flow-based underwriting | **ADOPT** | V |
| Founder control without dual-class | ADAPT | X |
| Founder personal channels for disclosure | REJECT | X |
| Free or subsidised hardware wedge | REJECT | III, VIII |
| Free P2P as acquisition wedge | REJECT | IV, VII |
| Gross profit as governing metric | **ADOPT** | VIII |
| Holding-company-over-subsidiary | ADAPT | I |
| Industrial-bank charter | **REJECT** (map to MFB) | I, II |
| Instant onboarding via aggregation | **ADOPT** | III |
| **Interchange as consumer subsidy** | **REJECT** | **VII, XII** |
| Killing fast with pre-set thresholds | **ADOPT** | XIII |
| Land-and-expand attach | ADAPT | III, VIII |
| Lending as margin engine | ADAPT | VIII |
| Localisation sequencing | ADAPT | XII |
| Merchant-acquiring take rate | ADAPT | VII, XII |
| Micro-merchants as a segment | ADOPT (conditional) | III |
| Multi-product attach | **ADOPT** | IV, VIII |
| Non-GAAP presentation habit | REJECT | VIII, X |
| Offer-driven origination | **ADOPT** | V |
| One platform, not several | **ADOPT** | VI |
| Operator-veto discipline | **ADOPT** | X, XIII |
| Owning hardware | REJECT | VI |
| Partner-led entry (cash-dominant market) | **ADOPT** | XII |
| Pre-testing behaviour in market | **ADOPT** | XIII |
| Real-time risk and fraud scoring | ADAPT | VI |
| Repayment as % of daily volume | **ADAPT** (hardest) | V |
| Risk reporting only to the CEO | REJECT | X |
| Ring-fencing a regulated entity | ADAPT | I |
| Selling loans to institutions | REJECT | V, IX |
| Seller side before consumer side | **ADOPT** | XII |
| Settlement-controlled credit as first moat | **ADOPT** | XI |
| Settlement-controlled repayment | **ADOPT** | V, VII |
| Shared infrastructure | **ADOPT** | XI |
| Shared customers assumed to follow | **REJECT** | XI |
| Software as margin engine | **ADOPT** | III, VIII |
| Speculative crypto to members | REJECT | IV |
| State-by-state licensing | REJECT (Nigeria easier) | II |
| Unified data estate from day one | **ADOPT** | VI |
| Viral acquisition engine | REJECT (discard) | IV |
| Volatile treasury asset at parent | REJECT | I, IX |
| Warehouse / forward-flow funding | REJECT | II, IX |
| Compliance sequenced ahead of scale | **ADOPT** | II, VI |
| Entering against entrenched incumbents | ADAPT | XII, XI |
| Unaccountable founder conviction | REJECT | X, XIII |

---

# APPENDIX D — SOURCE REGISTER

## D.1 What the study rests on

**Primary corporate filings.** Block's **Form 10-K** filings for FY2021 through FY2025, with particular weight on Exhibit 21 (subsidiaries), the goodwill and intangibles notes, the loans and allowance roll-forwards, the debt note, the segment note, the customer-funds disclosures and the risk factors; **Form 10-Q** filings; **Form 8-K** filings for acquisitions, disposals, financings, buyback authorisations, the workforce plan and the Item 5.07 voting results; **DEF 14A proxy statements** for board composition, compensation, share structure and shareholder proposals; and **Form 4** filings.

**Banking and prudential records.** FDIC application materials, the conditional approval order and the Capital and Liquidity Maintenance Agreement for Square Financial Services; Utah Department of Financial Institutions records; FDIC call-report data via third-party aggregators, with the reporting date flagged where unconfirmed.

**Enforcement and judicial records.** The **CFPB consent order of 16 January 2025**; the **NYDFS consent order of 10 April 2025**; the **CSBS-coordinated 48-state settlement of 15 January 2025**; the 46-state attorneys general consent judgment of 8 July 2026 and the Washington State settlement; and the **Delaware Court of Chancery opinion** in the TIDAL derivative suit (Chancellor Kathaleen McCormick, May 2023), read throughout as a governance document rather than a legal one.

**Regulatory instruments.** The Bank Holding Company Act Section 2(c) exception; FDIC Part 354; the Federal Reserve's **Regulation II** and the *Corner Post* litigation; the **EU Interchange Fee Regulation** and its UK retained version; Reserve Bank of Australia interchange standards; and on the Nigerian side the **CBN Financial Holding Company framework** including the 2026 draft revisions, the microfinance-bank licensing tiers, the Guide to Charges, the IMTO regime and NIBSS materials.

**Counterparty and competitor filings.** Core Scientific's disclosure of the $41.9m Proto termination; DoorDash on the Caviar acquisition; and Shopify, Toast, Fiserv, PayPal, Affirm, Chime and Lightspeed filings for the comparison matrices, with definitions normalised.

**Contemporaneous reporting**, preferred to retrospective accounts throughout — the Wall Street Journal, Bloomberg, Reuters, American Banker, Payments Dive, PYMNTS, Fortune, TechCrunch, Recode, City A.M. and, for the international volume, Nikkei and the Australian Financial Review.

**Treated as advocacy or claim, and tested.** The Hindenburg Research report of March 2023 and Block's response, both by interested parties; Block's shareholder letters, investor-day materials and engineering blogs; and every management statement about strategy, culture, productivity and product-market fit.

## D.2 Evidential asymmetry

**Block is unusually well documented, and unusually well documented in one direction.** As a domestic filer with fourteen years of public reporting, its financial record is deep. But the material this study needed most — cross-ecosystem customer overlap, per-market profitability, the true composition of the workforce reduction, compliance headcount — is precisely what Block does not disclose.

**The enforcement documents are the best technical evidence available.** The NYDFS and CFPB orders describe Block's internal systems with a specificity no voluntary disclosure matches: the suspicious-activity-report backlog growing from 18,000 to over 169,000 alerts, the 8,359 accounts opened by a single ring, the bitcoin screening thresholds. Volumes IV and VI mine them as engineering documents.

**And one absence carried more weight than any presence.** Block has asserted ecosystem synergy for years and has never published a person-level figure for customers active on both sides. Volume XI concluded that the absence was the answer.

---

# APPENDIX E — RECONCILIATION

Fourteen volumes commissioned sequentially against a moving evidence base, with figures restated twice by the company itself. Eight discrepancies were identified on assembly: **two genuine errors, both corrected at source**; four dual-value figures needing one canonical statement; and two vintage series that are not conflicts at all.

## E.1 Genuine errors — corrected

**Note 1 — long-term debt. CORRECTED.** Volume VIII stated that Block ended 2025 with "$0 long-term debt reported." **This is false.** Volume IX established from Note 14 of the FY2025 Form 10-K that Block carries **$7,350,000k of principal and $7,289,018k of net carrying value across seven series** — five senior note series ($1.0bn 2026, $1.2bn 2030, $1.0bn 2031, $2.0bn 2032, $1.0bn 2033) and two convertible series ($575m 2026, $575m 2027) — reconciling exactly to the balance sheet's $1,573,259k current portion plus $5,715,759k long-term. **Volume IX governs**, and Volume VIII now carries a visible inline correction at the point a reader meets the claim. The error does not affect Volume VIII's analysis, which concerned segment economics, but the figure as stated was wrong.

**Note 2 — the Clearpay European exit. CORRECTED.** Volume XII dated the wind-down to approximately 25 August 2025. Volume XIII, researching the abandonment record directly, established from contemporaneous City A.M. and FashionNetwork reporting that Clearpay stopped taking new customers on 3 July 2023 and **closed the European operation from 25 August 2023** — two years earlier — and flagged the conflict rather than silently resolving it. **Volume XIII governs**; Volume XII is corrected in place.

## E.2 Dual-value figures — one canonical statement each

**Note 3 — the Caviar purchase price.** Press consistently reports approximately $90m; a securities filing shows $44.3m. **Both are recorded throughout and neither is wrong**; the difference most likely reflects headline consideration including earnouts and stock against GAAP-recognised consideration. The sale figure is unambiguous: **$410m**, closed 31 October 2019. Where a single number is needed, use the filing basis and state it.

**Note 4 — the Afterpay consideration.** ~$29bn announced (1 August 2021) against **$13,836,622k at close** (31 January 2022). Not a discrepancy but a structural fact about paying in volatile equity, and Volumes I, IX, XI and XIII all handle it correctly. **Use the closing figure for any economic calculation; cite the announced figure only when discussing the acquisition decision.**

**Note 5 — Square Financial Services' balance sheet.** Three figures circulate: equity of approximately $845m (Q3 2025, carried from Volume II); total assets of approximately $2.06bn with equity of approximately $1.35bn (Volume I, third-party aggregation, date unconfirmed); and total assets of $1,354,373k with loans of $756,584k and deposits of $420,575k (Volume IX, 30 September 2025 call report). **The dated call-report figures govern.** The bank's balance sheet moves materially quarter to quarter as loans are originated and sold, so undated figures should not be used. Volume I's caution to reconcile against FDIC BankFind (CERT 59177) stands.

**Note 6 — Paycheck Protection Program lending.** Three company figures: approximately $820m to more than 76,000 businesses (press release, 10 June 2020); approximately $873m to over 80,000 (Q2 2020 shareholder letter); and approximately $857m carried in Volume II. **All are COMPANY CLAIM at different dates and scopes.** Use the shareholder-letter figure with its date attached, or state the range.

**Note 7 — restructuring charges.** $450–500m announced in the February 2026 Form 8-K; approximately **$852m** reported as the total; $495.3m recorded in Q1 2026. These are an estimate, a total and a period recognition respectively, not competing values. **State which is meant.**

## E.3 Vintage series — not conflicts

**Note 8.** Several figures move because the underlying quantity moved, and should be read as dated series rather than disagreements:

- **Bitcoin holdings:** 8,038 BTC (end-2022 and end-2023) → 8,485 BTC (31 December 2024, fair value $792.3m) → **8,883 investment BTC (31 December 2025, fair value $777,515k, cost basis $292.6m)** → approximately 9,032 (Q1 2026). Add approximately 238 operational BTC and approximately 19,357 customer BTC for the roughly 28,355 total sometimes cited. **Four legitimate numbers depending on date and scope.**
- **Bitcoin as a share of revenue:** ~42.3% (FY2024) → ~35% (FY2025), because bitcoin revenue fell 18% while the rest grew.
- **Square GPV:** ~$210bn (2023) → $227.6bn (2024) → $250.5bn (2025).
- **Headcount:** ~13,000 (peak, Q3 2023) → 12,000 cap (November 2023) → 10,205 (31 December 2025) → **under 6,000** (February 2026 plan).
- **Cash App actives:** 56m (2023) → 57m (2024) → 59m (December 2025).

## E.4 Unknowns carried forward

The study could not resolve, and does not pretend to have resolved:

- **Any person-level figure for customers active on both Square and Cash App.** Confirmed never disclosed. Volume XI treated the absence as evidence.
- Cash App Pay gross payment volume, and its Square versus non-Square split.
- Per-market international profitability, and Japan-specific scale.
- The true composition of the February 2026 workforce reduction, as between artificial-intelligence substitution, over-hiring correction and business-line wind-down. Volume VI judged the AI attribution substantially overstated; the proportions remain UNKNOWN.
- Block's compliance headcount and spend.
- The incremental cost of the CFPB-mandated 24-hour live support.
- Whether risk and compliance now hold a genuine product-launch veto.
- The final terms of the Department of Justice matter, against which $240m is reserved.
- Verse's purchase price, and the development cost of Square Wallet, Square Order, TBD and Proto.
- The individual independent directors of Square Financial Services.

## E.5 A note on the reader's own assumptions

Two figures in this study come from the reader's prior research rather than from primary sources, and are load-bearing for the transplant verdicts: **Nigerian credit-bureau coverage at roughly 13% of adults**, and the **CBN Financial Holding Company capital parameters** (51% minimum stake, 20% buffer above combined subsidiary minimums). Both were corroborated against available material, and the second against the CBN's 2026 draft revisions — but the framework was in draft, and **every Nigerian regulatory figure in this study should be re-verified against current circulars before capital is committed.** Volume XIV states this among its four open questions.
