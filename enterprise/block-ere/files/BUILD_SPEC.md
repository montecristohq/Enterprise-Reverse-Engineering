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

