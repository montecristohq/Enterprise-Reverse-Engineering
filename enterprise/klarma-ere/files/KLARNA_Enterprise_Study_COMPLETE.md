# Klarna

**An Enterprise Reverse-Engineering Study**

Five volumes · Corporate and regulatory anatomy · Product and merchant-funded value flow · Operations and the decision engine · Financial architecture and capital · Strategy and moat

Research cut-off: 11 August 2026
Prepared by: Damascus Research
Sixth subject in the EREF programme, after Wise plc, Atruvia AG, the DZ BANK Group, Experian plc and Robinhood Markets, Inc.

---

## What this document is

A forensic reverse-engineering study of Klarna — the group headed by Klarna Group plc (NYSE: KLAR) and built around its licensed Swedish banking subsidiary, Klarna Bank AB (publ). It is not a company profile, an equity note, or a strategy summary. The objective is to take the enterprise apart until its machinery is understood, then reconstruct it.

The organising question, carried through all five volumes, is the one this programme has now asked of three companies: **when a service is free to the user, who pays?**

Klarna is the third distinct answer. Experian's consumer is the **raw material** — data furnished about them. Robinhood's customer's **order** is the product, bought by a wholesale market maker. **Klarna's consumer is the bait, and the merchant pays for conversion.**

| | Volume | Question it answers |
|---|---|---|
| **I** | Corporate, Legal, Regulatory & Institutional Anatomy | What is Klarna legally, and which entity is the real business? |
| **II** | Product, the Merchant-Funded Customer Structure & Value-Flow Architecture | If the consumer pays nothing, who is the customer? |
| **III** | Operations, the Decision Engine, Technology, Data, AI & Organisational Design | What machinery decides, in a fraction of a second, whether to lend? |
| **IV** | Financial Statements, Revenue Architecture, Credit Economics, Unit Economics, Regulatory Capital & Capital Allocation | Is this business actually profitable, and what does growth cost in capital? |
| **V** | Management, Culture, Incentives, Competition, Moat, Risk & Strategic Evolution | Why does it win, and is the advantage durable? |
| **VI** | Cross-Volume Synthesis | The enterprise as one system |
| **A** | Glossary | The vocabulary of banking regulation, consumer credit and buy-now-pay-later |
| **B** | Canonical Figures Register | The governing value for every material number |
| **C** | The Three Reporting Entities | The basis-discipline guide — read before any financial section |
| **D** | Source Register and Reconciliation | How claims were graded, and where the volumes disagreed |

**Recommended first pass.** Appendix C (the three reporting entities — without it, the financial sections will mislead) → Volume II, section II.3 (why merchants pay, the mechanism the business rests on) → Volume IV, section IV.11 (the capital cost of a dollar of GMV, the study's quantitative payoff) → Part VI (synthesis). Volumes I, III and the remainder of IV are reference-depth.

**A note on what makes this subject unusual.** Klarna has been a public reporting company only since September 2025, so the disclosure base is thinner than for any previous subject in this programme — this is the shortest of the seven studies, and that is a fact about the evidence rather than about the analysis. Against that, the Swedish supervisory record is unusually candid, and the Finansinspektionen decision of December 2024 provides a level of forensic detail about internal controls that no voluntary disclosure would offer.

---

## Conventions governing the whole study

### Evidence classification

| Label | Meaning |
|---|---|
| **CONFIRMED FACT** | Directly supported by reliable primary evidence — a filing, a supervisory decision, a statute, a dated event |
| **COMPANY CLAIM** | Stated by Klarna but not independently verified. **The default class for every operational, productivity, cultural and "profitability" claim** |
| **THIRD-PARTY ESTIMATE** | Externally reported or estimated; not from filings |
| **ANALYTICAL INFERENCE** | Reasonably inferred from multiple known facts, with the reasoning shown |
| **HYPOTHESIS** | A possible explanation requiring further evidence |
| **UNKNOWN** | The available evidence is insufficient — flagged, not papered over |

**Why the COMPANY CLAIM default is stricter here than in previous studies.** Volume III established that Klarna's celebrated artificial-intelligence narrative was substantially overstated and was later qualified by the chief executive himself. Volume IV established that the headline "adjusted operating profit" excludes real share-based pay. Volume V concluded that management communication is **promotional and narrative-forward, requiring independent correction — but that the audited financials have proved reliable.** The distinction matters: accept the numbers, test the interpretations.

### Basis discipline — the single most important convention in this study

**Three reporting entities and two currencies are in play, and conflating them produces nonsense.** Appendix C sets this out in full. In brief:

| Entity | Currency | Framework | What it reports |
|---|---|---|---|
| **Klarna Group plc** | **USD** | IFRS as issued by the IASB, Form 20-F | The listed group's consolidated results |
| **Klarna Bank AB (publ)** | **SEK** | IFRS-EU + Swedish Annual Accounts Act | The licensed bank's statutory accounts |
| **Klarna Holding AB Consolidated** | **SEK** | CRR/CRD, Pillar 3 | **The only basis on which capital ratios exist** |

Every figure states its entity, currency and framework. Klarna's **non-IFRS measures** — transaction margin dollars, transaction margin, adjusted operating profit and adjusted operating margin — are labelled as such, reconciled where the disclosure permits, and never mixed with IFRS figures in a single comparison.

### Follow-the-Legal-Entity

Klarna Group plc is a non-operating holding company. It does not lend, take deposits, or contract with merchants or consumers. The distinction that matters most:

- **In the EEA and UK, Klarna Bank AB (or its branches, or Klarna Financial Services UK Limited) is the lender of record and holds the credit risk.**
- **In the United States, WebBank — a Utah industrial bank that is not a Klarna entity — originates, and Klarna Inc. purchases the receivables and bears the predominant loss economics.**

That split is the single most important entity fact in the group, and it changes the legal, capital and regulatory answer to almost every question.

### Follow-the-Credit-Risk — the carried rule

This study's distinctive analytical rule, equivalent to Follow-the-Data-Right in the Experian study and Follow-the-Order in the Robinhood study. **Wherever credit is extended, the study establishes who underwrites it, who funds it, who legally owns the receivable, who bears the loss, and how quickly the decision is made.** The rule is developed cumulatively:

- **Volume I** establishes the legal chain — lender of record, receivable ownership, and how it differs by jurisdiction.
- **Volume II** establishes the transaction economics — the merchant fee, the loss rate, and the velocity of the book.
- **Volume III** establishes the machinery — the decision engine, its data, and the sub-second latency budget.
- **Volume IV** establishes the accounting and the capital — IFRS 9 provisioning, CRR risk weights, and what a dollar of volume consumes.
- **Volume V** establishes the strategic durability — whether the arrangement survives regulation, competition and disintermediation.

### Depth follows the subject

Sections are not of equal length. A topic ends when its analytical questions are answered, not when a page count is reached.

---

## Contents

- [VOLUME I — Corporate, Legal, Regulatory & Institutional Anatomy](#volume-i-corporate-legal-regulatory-institutional-anatomy)
  - [Basis Discipline (read first)](#basis-discipline-read-first)
  - [I.1 Origin and Corporate History](#i1-origin-and-corporate-history)
  - [I.2 The Bank Inside the Fintech (RE-CUT — by permission and function)](#i2-the-bank-inside-the-fintech-re-cut-by-permission-and-function)
  - [I.3 Ownership, Share Structure and Control](#i3-ownership-share-structure-and-control)
  - [I.4 Governance and the 2023–2024 Board Dispute](#i4-governance-and-the-20232024-board-dispute)
  - [I.5 Merchant and Consumer Contractual Architecture](#i5-merchant-and-consumer-contractual-architecture)
  - [I.6 The Regulator Inventory](#i6-the-regulator-inventory)
  - [I.7 The Banking Licence Decision (NEW — pivotal)](#i7-the-banking-licence-decision-new-pivotal)
  - [I.8 Funding Structure and Deposits](#i8-funding-structure-and-deposits)
  - [I.9 The Moving Perimeter (NEW)](#i9-the-moving-perimeter-new)
  - [I.10 Follow-the-Credit-Risk by Jurisdiction](#i10-follow-the-credit-risk-by-jurisdiction)
  - [I.11 Enforcement, Supervision and Data Protection (PRIORITY DEPTH)](#i11-enforcement-supervision-and-data-protection-priority-depth)
  - [I.12 Acquisitions and Corporate Development](#i12-acquisitions-and-corporate-development)
  - [I.13 Institutional Dependency Map](#i13-institutional-dependency-map)
  - [I.14 Volume I Reconstruction](#i14-volume-i-reconstruction)
- [VOLUME II — Product, the Merchant-Funded Customer Structure & Value-Flow Architecture](#volume-ii-product-the-merchant-funded-customer-structure-value-flow-architecture)
  - [TL;DR](#tldr)
  - [Key Findings](#key-findings)
  - [Details](#details)
    - [II.1 The Product Universe (by legal entity)](#ii1-the-product-universe-by-legal-entity)
    - [II.2 The Merchant-Funded Customer Structure (THE RE-CUT)](#ii2-the-merchant-funded-customer-structure-the-re-cut)
    - [II.3 Why Merchants Pay (the analytical heart)](#ii3-why-merchants-pay-the-analytical-heart)
    - [II.4 Take Rate and Revenue Decomposition](#ii4-take-rate-and-revenue-decomposition)
    - [II.5 Consumer Economics — what the "free" user actually pays](#ii5-consumer-economics-what-the-free-user-actually-pays)
    - [II.6 The Velocity of the Book (NEW)](#ii6-the-velocity-of-the-book-new)
    - [II.7 The Advertising and Comparison Business](#ii7-the-advertising-and-comparison-business)
    - [II.8 Customer Segmentation and Disclosed Metrics](#ii8-customer-segmentation-and-disclosed-metrics)
    - [II.9 The Escalation Ladder and the Customer Journey](#ii9-the-escalation-ladder-and-the-customer-journey)
    - [II.10 Value-Flow Reconstruction — three transactions](#ii10-value-flow-reconstruction-three-transactions)
    - [II.11 Underwriting and the Decision](#ii11-underwriting-and-the-decision)
    - [II.12 Failure and Exception Paths](#ii12-failure-and-exception-paths)
    - [II.13 Product-Market Evolution (2005 → 2026)](#ii13-product-market-evolution-2005-2026)
  - [Recommendations](#recommendations)
  - [Caveats](#caveats)
  - [Volume II Reconstruction (summary)](#volume-ii-reconstruction-summary)
- [VOLUME III — Operations, the Decision Engine, Technology, Data, AI & Organisational Design](#volume-iii-operations-the-decision-engine-technology-data-ai-organisational-design)
  - [TL;DR](#tldr-1)
  - [Key Findings](#key-findings-1)
  - [Details](#details-1)
    - [III.1 The Operating Model — functions by legal entity](#iii1-the-operating-model-functions-by-legal-entity)
    - [III.2 The Decision Engine (THE CORE)](#iii2-the-decision-engine-the-core)
    - [III.3 Underwriting Data and Model Governance](#iii3-underwriting-data-and-model-governance)
    - [III.4 The Data Architecture and the Purpose-Separation Question](#iii4-the-data-architecture-and-the-purpose-separation-question)
    - [III.5 Technology Architecture](#iii5-technology-architecture)
    - [III.6 Merchant Integration and Distribution Operations](#iii6-merchant-integration-and-distribution-operations)
    - [III.7 Payment Operations, Settlement and Collections](#iii7-payment-operations-settlement-and-collections)
    - [III.8 Financial Crime, AML and Fraud — with the FI post-mortem](#iii8-financial-crime-aml-and-fraud-with-the-fi-post-mortem)
    - [III.9 Customer Service Operations (the pre-AI baseline)](#iii9-customer-service-operations-the-pre-ai-baseline)
    - [III.10 The AI Substitution Episode (assessed)](#iii10-the-ai-substitution-episode-assessed)
    - [III.11 Workforce and Organisational Design](#iii11-workforce-and-organisational-design)
    - [III.12 Operating Leverage — the quantified mechanism](#iii12-operating-leverage-the-quantified-mechanism)
    - [III.13 Bottlenecks and the Theory of Constraints](#iii13-bottlenecks-and-the-theory-of-constraints)
    - [III.14 Operational Resilience (stress tests)](#iii14-operational-resilience-stress-tests)
    - [III.15 Technology and Operations as Moat](#iii15-technology-and-operations-as-moat)
    - [III.16 Volume III Reconstruction — the central question](#iii16-volume-iii-reconstruction-the-central-question)
  - [Recommendations](#recommendations-1)
  - [Caveats](#caveats-1)
- [VOLUME IV — Financial Statements, Revenue Architecture, Credit Economics, Unit Economics, Regulatory Capital & Capital Allocation](#volume-iv-financial-statements-revenue-architecture-credit-economics-unit-economics-regulatory-capital-capital-allocation)
  - [TL;DR](#tldr-2)
  - [Key Findings](#key-findings-2)
  - [Details](#details-2)
    - [IV.1 Multi-Year Financial History](#iv1-multi-year-financial-history)
    - [IV.2 Revenue Architecture](#iv2-revenue-architecture)
    - [IV.3 Net Interest Income and the Deposit Advantage](#iv3-net-interest-income-and-the-deposit-advantage)
    - [IV.4 Cost Architecture (economic drivers)](#iv4-cost-architecture-economic-drivers)
    - [IV.5 Credit Economics in Depth](#iv5-credit-economics-in-depth)
    - [IV.6 Unit Economics](#iv6-unit-economics)
    - [IV.7 Transaction Margin — the company's metric, tested](#iv7-transaction-margin-the-companys-metric-tested)
    - [IV.8 The IFRS-to-Non-IFRS Gap — forensic treatment](#iv8-the-ifrs-to-non-ifrs-gap-forensic-treatment)
    - [IV.9 Bank Balance Sheet Teardown (RE-CUT)](#iv9-bank-balance-sheet-teardown-re-cut)
    - [IV.10 Funding Architecture (all sources traced)](#iv10-funding-architecture-all-sources-traced)
    - [IV.11 The Capital Cost of a Dollar of GMV (NEW SECTION — the payoff)](#iv11-the-capital-cost-of-a-dollar-of-gmv-new-section-the-payoff)
    - [IV.12 Regulatory Capital and the Cost of the Licence](#iv12-regulatory-capital-and-the-cost-of-the-licence)
    - [IV.13 The Originate-to-Distribute Pivot (NEW SECTION)](#iv13-the-originate-to-distribute-pivot-new-section)
    - [IV.14 Cash Flow and the Free-Cash-Flow Question](#iv14-cash-flow-and-the-free-cash-flow-question)
    - [IV.15 Capital Allocation](#iv15-capital-allocation)
    - [IV.16 Dilution and Share Count](#iv16-dilution-and-share-count)
    - [IV.17 One Dollar of GMV — the waterfall](#iv17-one-dollar-of-gmv-the-waterfall)
    - [IV.18 Economic Driver Tree](#iv18-economic-driver-tree)
    - [IV.19 Scenario Model](#iv19-scenario-model)
    - [IV.20 Revenue Quality and Normalised Profitability](#iv20-revenue-quality-and-normalised-profitability)
    - [IV.21 Valuation-Relevant Economics](#iv21-valuation-relevant-economics)
    - [IV.22 Volume IV Reconstruction — Ten Conclusions](#iv22-volume-iv-reconstruction-ten-conclusions)
  - [Recommendations](#recommendations-2)
  - [Caveats](#caveats-2)
- [VOLUME V — Management, Culture, Incentives, Competition, Moat, Risk & Strategic Evolution](#volume-v-management-culture-incentives-competition-moat-risk-strategic-evolution)
  - [TL;DR](#tldr-3)
  - [Key Findings](#key-findings-3)
  - [Details](#details-3)
    - [V.1 The Founders and the Founding Idea](#v1-the-founders-and-the-founding-idea)
    - [V.2 Current Management](#v2-current-management)
    - [V.3 The Management System](#v3-the-management-system)
    - [V.4 Declared versus Revealed Culture, and the Credibility Question (RE-CUT)](#v4-declared-versus-revealed-culture-and-the-credibility-question-re-cut)
    - [V.5 Incentive Architecture](#v5-incentive-architecture)
    - [V.6 The Competitive Universe](#v6-the-competitive-universe)
    - [V.7 Competitor Teardowns](#v7-competitor-teardowns)
    - [V.8 Why Klarna Wins (mechanism decomposition)](#v8-why-klarna-wins-mechanism-decomposition)
    - [V.9 Moat Scorecard (RE-CUT — honestly asymmetric)](#v9-moat-scorecard-re-cut-honestly-asymmetric)
    - [V.10 Replication Test](#v10-replication-test)
    - [V.11 Porter's Five Forces](#v11-porters-five-forces)
    - [V.12 PESTLE](#v12-pestle)
    - [V.13 Strategic Flywheels (genuine)](#v13-strategic-flywheels-genuine)
    - [V.14 Negative Flywheels](#v14-negative-flywheels)
    - [V.15 The Strategic Bottleneck](#v15-the-strategic-bottleneck)
    - [V.16 Risk Register](#v16-risk-register)
    - [V.17 Stress Tests](#v17-stress-tests)
    - [V.18 What Could Make Klarna Obsolete](#v18-what-could-make-klarna-obsolete)
    - [V.19 Strategic Optionality](#v19-strategic-optionality)
    - [V.20 What Is Klarna Actually Becoming (central question — ranked hypotheses)](#v20-what-is-klarna-actually-becoming-central-question-ranked-hypotheses)
    - [V.21 Five- and Ten-Year Strategic Map](#v21-five--and-ten-year-strategic-map)
    - [V.22 What the Market May Misunderstand](#v22-what-the-market-may-misunderstand)
    - [V.23 Management & Capital-Allocation Judgement](#v23-management-capital-allocation-judgement)
    - [V.24 Volume V Reconstruction](#v24-volume-v-reconstruction)
  - [Recommendations](#recommendations-3)
  - [Caveats](#caveats-3)

---

# VOLUME I — Corporate, Legal, Regulatory & Institutional Anatomy

---

## Basis Discipline (read first)

- **Ultimate parent / filer:** Klarna Group plc, incorporated in England and Wales on **7 November 2022** (originally "Klarna UK II PLC," renamed Klarna Group plc on **13 December 2023**), CRN **14467769**, registered at 10 York Road, London SE1 7ND. It lists on the NYSE under "KLAR." **CONFIRMED FACT** (SEC Form F-1).
- **Filing regime:** Klarna Group plc is a **foreign private issuer (FPI)** and filed a **Form F-1** registration statement (not an S-1); it reports on **Form 20-F** (not 10-K). It has elected reduced FPI disclosure. **CONFIRMED FACT** (F-1 cover; group 20-F).
- **Reporting currency:** From the reorganisation, the group presents consolidated financials in **US dollars**. Historically (Klarna Holding AB) the presentation currency was **Swedish krona (SEK)**; the statutory Swedish accounts remain in SEK, and Pillar 3 regulatory figures are prepared in SEK and translated to USD for the prospectus. **CONFIRMED FACT** (F-1).
- **Accounting framework:** **IFRS Accounting Standards as issued by the IASB** for the prospectus consolidated statements; the former Klarna Holding statutory accounts were prepared under **IFRS as adopted by the EU** plus the Swedish Annual Accounts Act. Auditor: **Ernst & Young AB**. No IFRS-to-US-GAAP reconciliation was prepared. **CONFIRMED FACT** (F-1).
- **Financial year end:** **31 December**. **CONFIRMED FACT.**
- **Non-IFRS measures** used by the company: transaction margin dollars, transaction margin, adjusted operating profit/loss, adjusted operating margin. Treated here as **COMPANY CLAIM** and never mixed with statutory figures.

---

## I.1 Origin and Corporate History

**Founding.** Klarna was founded in Stockholm in 2005 by **Sebastian Siemiatkowski**, **Niklas Adalberth** and **Victor Jacobsson**, following participation in the Stockholm School of Economics entrepreneurship competition. The original vehicle was called **Kreditor**; it was renamed **Klarna** in 2010. The founding insight was payment friction and trust at online checkout — letting the consumer receive goods first and pay later, with Klarna assuming the credit and fraud risk on behalf of the merchant. **CONFIRMED FACT.**

**Early funding.** Sequoia Capital first invested in 2010 (Michael Moritz wrote the firm's first cheque), followed by investors including General Atlantic, DST Global, Atomico and later Visa, Permira, Bestseller/Heartland, and others. **CONFIRMED FACT.**

**European expansion via Sofort.** In December 2013 Klarna agreed to acquire the German market leader **Sofort GmbH** (operator of the Sofortüberweisung bank-transfer service) from Reimann Investors for a **reported ~$150 million** (per TechCrunch, 18 December 2013: "Klarna is buying Sofort from their majority shareholder Reimann Investors… we hear the price is around $150 million"). The deal closed in March 2014, financed in part by a **€90m round led by the founders with Sequoia, General Atlantic and Atomico**. The combined entity ("Klarna Group") reached roughly 25 million consumers and ~45,000 merchants across 14 European countries. **CONFIRMED FACT.**

**The banking licence (pivotal).** On **19 June 2017**, after roughly 20 months of process (application filed late 2015), Klarna was granted a **full banking licence** by **Finansinspektionen** (the Swedish FSA). The operating company (incorporated 5 September 2007 as "Kreditor Finans AB," company number 556737-0431) became **Klarna Bank AB (publ)**. See I.7. **CONFIRMED FACT.**

**UK and US launches.** Klarna built a UK presence (accelerated by the 2018 acquisition of Close Brothers Retail Finance) and launched aggressively in the **United States from 2019**, which drove the shift from profitability into investment-stage losses. **CONFIRMED FACT.**

**Valuation cycle.** Klarna's private valuation rose to a **$45.6 billion** peak in a June 2021 round led by SoftBank Vision Fund 2 (after a March 2021 round at $31bn and a 2020 round at $11bn led by Silver Lake). In a July 2022 down round the valuation was cut ~85% to **$6.7 billion**. This is a **financing story**, not a structural one. **CONFIRMED FACT.**

**Restructuring for listing.** In **May 2024** Klarna redomiciled its parent from Sweden to the UK by a share-for-share exchange: shareholders of Klarna Holding AB exchanged their shares for shares in the new English parent, **Klarna Group plc**, which became the ultimate holding company. A **twelve-for-one share split** took effect 6 March 2025. **CONFIRMED FACT** (F-1).

**The NYSE IPO (2025).** Klarna filed its F-1 with the SEC in early September 2025 (having paused an earlier April 2025 attempt amid tariff-driven market volatility). The IPO **priced on 9 September 2025 at $40.00 per share**, above the $35–37 range; trading began **10 September 2025** on the NYSE as "KLAR." The offering was **34,311,274 ordinary shares** — of which the company sold **5,555,556 shares** and selling shareholders sold **28,755,718 shares** (plus a 5,146,691-share over-allotment option granted by selling shareholders). Total gross deal value across all shares was **~$1.37 billion**, of which the great majority (~$1.17 billion) went to selling shareholders. Klarna Group plc's **net proceeds to the company were $169 million** (per Klarna Bank AB's FY2025 Annual Report: "Klarna Group plc raised net proceeds of $169 million through the IPO, net of underwriting discounts and other offering costs of $22.41 million"). The IPO price implied a valuation of **~$15.1 billion**; shares opened at **$52** and closed the first day at **$45.82** (up ~14.6%), implying a first-day market value of roughly **$17.4–17.5bn**. Lead bookrunners: Goldman Sachs, J.P. Morgan, Morgan Stanley. **CONFIRMED FACT.**
- *Post-IPO trajectory (context):* the stock traded well below the IPO price through 2026 (≈$17.66 on 18 June 2026 per one broker note), implying a market cap of roughly $7.4bn as of mid-2026 — above the 2022 private trough but far below the 2021 peak. **THIRD-PARTY ESTIMATE.**

**Structural reading of the history.** Each major event added a *capability* and a *dependency*: Sofort added German scale and open-banking rails but German credit-model exposure (Klarna nearly failed early in Germany); the 2017 banking licence added deposit-funding capability and EEA passporting but imposed CRR/CRD prudential obligations; US launch added the largest revenue market but created dependence on a **US bank partner (WebBank)** because Klarna held no US charter; the 2024 UK redomiciliation and 2025 IPO added public capital and a governance reset but introduced US securities-law and FPI reporting obligations.

---

## I.2 The Bank Inside the Fintech (RE-CUT — by permission and function)

Klarna is not, structurally, a "BNPL app." It is a **licensed Swedish credit institution (bank)** that distributes consumer credit at the point of sale, wrapped in a listed UK holding company, and — in the one market where it lacks a charter (the US) — it rents a charter from a partner bank. Mapped by **regulatory permission and function**:

**Entity map (by function):**

1. **Klarna Group plc** — *UK holding company (England & Wales), CRN 14467769.* Ultimate listed parent (NYSE: KLAR). **Holds no banking licence; does not lend, take deposits, or contract with merchants or consumers.** Its role is capital-raising, group governance and SEC reporting. **CONFIRMED FACT.**
2. **Klarna Holding AB (publ)** — *Sweden, corp. ID 556676-2356, registered Sveavägen 46, Stockholm.* Intermediate holding company and the **prudential consolidation entity** ("Klarna Holding AB Consolidated") for CRR/CRD capital purposes. Owns Klarna Bank AB (95.1% directly / 99.7% indirectly per the 2024 annual report). **CONFIRMED FACT.**
3. **Klarna Bank AB (publ)** — *Sweden, corp. ID 556737-0431, Sveavägen 46, Stockholm.* **THE licensed credit institution.** Holds the Finansinspektionen banking licence; takes deposits; originates and holds consumer credit across the EEA; passports into other EEA states under CRD IV (Directive 2013/36/EU) via branches and cross-border services; participates in the Swedish deposit-guarantee scheme. **This is the real operating business.** Supervised by FI as a "category 2 institution." **CONFIRMED FACT.**
4. **National branches of Klarna Bank AB** — e.g., the **German branch** (into which **Sofort GmbH was merged by cross-border merger completed 17 December 2024**), and other EEA branches. Branches conduct Klarna Bank AB's licensed activities locally under passporting; credit risk sits on Klarna Bank AB's balance sheet. **CONFIRMED FACT** (branch/merger); **ANALYTICAL INFERENCE** (risk location).
5. **Klarna Financial Services UK Limited (KFSUK)** — *UK, FRN 987889.* Dedicated UK entity **authorised and regulated by the FCA**. Following Brexit, Klarna Bank AB operated in the UK under the Temporary Permissions Regime; KFSUK received full FCA authorisation (announced November 2023) covering regulated credit and payment products (term loan, card, one-time card, in-store card, open-banking payments) and was later authorised as an **Electronic Money Institution (EMI)**. From **15 July 2026**, KFSUK is the authorised entity for the now-regulated Deferred Payment Credit (BNPL) products. **CONFIRMED FACT.**
6. **Klarna Inc.** — *Delaware corporation; principal office 800 N. High St., Ste. 400, Columbus, Ohio 43215; NMLS #1353190.* The main US operating entity. **Not a US bank** and **not the lender of record** — it markets and services loans that are **issued by WebBank**, then bears the economics (see I.10). Holds a **California Financing Law license (CFL #60DBO-44020)** and state money-transmitter licenses. **CONFIRMED FACT.**
7. **WebBank** — *Utah-chartered, FDIC-insured industrial bank, Salt Lake City* — **not a Klarna entity**, but the **US lender/originator of record** for Klarna's US financing, one-time card and Klarna Card products (see I.10). **CONFIRMED FACT.**
8. **Klarna Australia Pty Ltd** — Australian operating entity; from **10 June 2025** BNPL providers must hold an **Australian Credit Licence (ACL)** and join AFCA. **CONFIRMED FACT** (regime); **HYPOTHESIS** (exact entity name/ACL number not verified in sources gathered).
9. **Acquired businesses / other entities:** **Sofort GmbH** (Germany, open banking — merged into Klarna Bank AB Dec 2024); **BillPay** (Germany, acquired Feb 2017); **Close Brothers Retail Finance** (UK retail finance, acquired 2018/announced 14 Sept 2018); **Stocard** (Germany, loyalty wallet, acquired July 2021, ~€110m); **PriceRunner** (Sweden/Nordics price comparison, acquisition completed 4 April 2022); plus smaller deals (Cookies, ShopCo, Nuji, Inspirock, APPRL, HERO). **Klarna Germany Holding GmbH** exists as a German holding entity. **CONFIRMED FACT.**

**Who contracts with whom.** In the EEA/UK, **Klarna Bank AB (or its branch / KFSUK)** is the counterparty to both the **merchant agreement** and the **consumer credit agreement**, and holds the receivable and credit risk. In the **US**, the contractual lender to the consumer is **WebBank**, while **Klarna Inc.** contracts with the merchant and purchases/holds the receivable economics. **This split is the single most important entity-attribution fact in the group** and differs fundamentally by jurisdiction. **CONFIRMED FACT / ANALYTICAL INFERENCE.**

---

## I.3 Ownership, Share Structure and Control

**Share structure (created for the listing).** Klarna adopted a **dual/multi-class** structure:
- **Ordinary shares** — one vote each; the class listed on the NYSE; full economic rights.
- **Class B shares** — **ten votes each**, **no dividend/economic rights**; one issued as a bonus to each pre-IPO ordinary share held immediately before the IPO; non-transferable; auto-convert to deferred shares on transfer of the underlying ordinary interest and after 20 years.
- **Class C shares** — issuable only to **Sebastian Siemiatkowski** and related persons for five years post-IPO; **ten votes each** and partial economic rights (half an ordinary share); capped so Class C voting cannot exceed **15%** of pre-IPO voting power.
- **Deferred shares** — no vote, no effective economics.
**CONFIRMED FACT** (F-1).

**Economic vs voting control.** Immediately after the IPO, pre-IPO holders (who received Class B super-voting shares) held **99.09% of voting power**; directors, officers and ≥5% holders and affiliates together held **54.67% of voting power**. Klarna is **not a "controlled company"** under NYSE rules (no single person/group >50%), but the F-1 warns these shareholders "**if they act together, will be able to control our management and affairs**." **CONFIRMED FACT.**

**Major holders (economic, around the IPO):**
- **Sequoia Capital** — largest shareholder, ~**79 million** shares, **just over 20%** (some sources cite ~22–23%); sold ~2m shares in the IPO; ~$500m invested in total; estimated ~7x / ~$3.5bn value at first-day close. **CONFIRMED FACT / THIRD-PARTY ESTIMATE.**
- **Victor Jacobsson** (co-founder, no longer operational) — the founder with the **most shares, ~31.4 million**; retained a large stake (~5–8%) and board influence via a representative. **CONFIRMED FACT.**
- **Sebastian Siemiatkowski** (co-founder, CEO) — ~**25.6 million** shares (~6–8%); **sold none** in the IPO. **CONFIRMED FACT.**
- **Heartland A/S** (family office of Danish billionaire **Anders Holch Povlsen**; first invested 2015/2017) — a **7.86%** passive stake per a Schedule 13G filed November 2025 (**29,652,586 ordinary shares** of **377,489,269 outstanding** as of 4 Nov 2025). **CONFIRMED FACT.**
- **Commonwealth Bank of Australia** — strategic investor (and Australian BNPL partner), ~**19.3 million** shares (~5%). **CONFIRMED FACT.**
- **Niklas Adalberth** (co-founder) — reduced over the years; still ~**under 3 million** shares at IPO. **CONFIRMED FACT.**
- Others with meaningful stakes: **SoftBank Vision Fund 2** (2021 peak round, heavily diluted), **Silver Lake** (2020 and 2022 rounds), **Permira, Atomico, DST Global, Mubadala, BlackRock, CPPIB, Bestseller**. **CONFIRMED FACT / THIRD-PARTY ESTIMATE.**

**Who controls it / can management be removed?** On economics, **no single holder has a majority**; Sequoia is the largest at ~20%. On **voting**, the Class B structure concentrated ~99% of votes in pre-IPO holders, and the CEO holds a bespoke Class C super-voting instrument capped at 15% of pre-IPO voting power. In practice control sits with a **coalition of the founders (Siemiatkowski and Jacobsson interests) and Sequoia**; management cannot easily be removed by public (ordinary) shareholders alone, because ordinary shares carry a small minority of votes. **ANALYTICAL INFERENCE.**

---

## I.4 Governance and the 2023–2024 Board Dispute

**Board and chair.** **Michael (Mike) Moritz** — who wrote Sequoia's first Klarna cheque in 2010 and joined the board that year — became **chairman in 2020** and remained chair after leaving Sequoia in July 2023 (to focus on Sequoia Heritage). He is a close ally of CEO Siemiatkowski (and in March 2026 personally acquired 3,472,845 ordinary shares for ~$49.9m). The board includes Sequoia's **Andrew Reed**, and independents such as **Roger W. Ferguson Jr.** (former TIAA CEO; former Fed Vice-Chair; Alphabet director). Executive directors named in the 2024 Pillar 3 report include Siemiatkowski (CEO), **Camilla Giesecke**, and **David Fock** (chair of the Klarna Bank AB board). **CONFIRMED FACT.**

**The dispute (governance evidence, not gossip).** The conflict had two visible phases and one root cause:
- **Root cause:** a long-running rift between **CEO Siemiatkowski** and co-founder **Victor Jacobsson** (who exited operations but retained a large stake and board influence via representative **Mikael Walther**), over founders' use of pre-emption rights through **SPVs** and over whether to create a **"golden share"** giving certain holders outsized post-IPO influence. **CONFIRMED FACT** (FT, Bloomberg, Sifted reporting).
- **Phase 1 (winter 2023/2024):** **Sequoia** (via board member **Matthew Miller**) sought an **EGM to remove chairman Moritz**. After Siemiatkowski flew to lobby Sequoia, the firm **reversed within days** ("upon a fuller assessment, we've withdrawn our EGM request… We fully support Michael as chairman"), and **Miller was replaced by Andrew Reed** on the board. **CONFIRMED FACT.**
- **Phase 2 (August–October 2024):** the board voted to remove director **Mikael Walther** (Jacobsson's envoy). Walther alleged his removal was **retaliation for questioning a bonus package that could net Siemiatkowski up to $35 billion**; Moritz countered that a law firm had investigated Walther's conduct (alleged holding-up/vetoing of decisions) and the board had lost confidence. On ~24 October 2024, shareholders **removed Walther with ~87% approval**. **CONFIRMED FACT.**

**What it reveals.** Real control sat with the **Siemiatkowski–Moritz–Sequoia axis**; the founder-vs-founder (Siemiatkowski vs Jacobsson) fault line was structural enough to require a bespoke multi-class share design at IPO to lock in founder/allied control. The disclosed **$35bn potential CEO incentive** and the multi-class structure are the two clearest governance-risk signals. **ANALYTICAL INFERENCE.**

---

## I.5 Merchant and Consumer Contractual Architecture

**The "merchant pays, consumer usually doesn't" structure.**
- **Merchant agreement:** Klarna contracts with the merchant to provide checkout financing and assumes the consumer credit and fraud risk; the merchant pays Klarna a **variable fee (up to ~5.99% of order value for BNPL / Pay in 30)** and typically receives payment upfront. **CONFIRMED FACT / COMPANY CLAIM (fee level).**
- **Consumer credit agreement:** the consumer receives short-term, **predominantly interest-free** credit (Klarna states **98% of transactions in the LTM to 30 June 2025 were interest-free**). Per Klarna Group plc's prospectus (424B4): "serving **approximately 111 million active Klarna consumers and approximately 790,000 merchants in 26 countries as of June 30, 2025**, and facilitating **$112 billion of GMV in the last twelve months ended June 30, 2025**." (For context, the group's FY2025 results reported GMV of $127.9bn, revenue of $3.5bn, 118m active consumers and 966,000 merchants — **COMPANY CLAIM**.)
- **Lender of record & receivable ownership:** In the **EEA/UK**, **Klarna Bank AB / KFSUK** is the lender, owns the receivable and bears default loss. In the **US**, **WebBank** is the lender of record and Klarna Inc. takes the economics (see I.10).
- **Legal characterisation by market:** historically **exempt/unregulated** short-term interest-free credit in the UK (outside the Consumer Credit Act) and in much of the EEA and Australia; **regulated consumer credit** where interest-bearing or where new regimes apply. This is changing fast (see I.9): UK DPC regulation from 15 July 2026; EU CCD II application from 20 November 2026; Australia from 10 June 2025.

---

## I.6 The Regulator Inventory

Regulators with authority over part of the group:
1. **Finansinspektionen (FI), Sweden** — home-state **prudential and conduct** supervisor of Klarna Bank AB and of Klarna Holding AB Consolidated (CRR/CRD). Can set Pillar 2 requirements, issue remarks/warnings, impose administrative fines, and ultimately withdraw the banking licence. Also the Swedish AML supervisor. **CONFIRMED FACT.**
2. **European Central Bank / Single Supervisory Mechanism** — **does NOT directly supervise Klarna Bank AB.** Reason: the SSM covers banks in **euro-area / banking-union** states (plus opt-in "close cooperation" states); **Sweden is in the EU but not the euro area and has not joined the banking union**, so prudential supervision stays with FI. **CONFIRMED FACT.**
3. **Riksgälden (Swedish National Debt Office)** — administers the **Swedish deposit guarantee scheme (insättningsgaranti)** in which Klarna Bank AB participates. Coverage ~**SEK 1,050,000** per depositor per bank (the EU-harmonised ~€100,000 under Directive 2014/49/EU); a later 2026 figure of SEK 1,150,000 appears in one distributor sheet (minor discrepancy noted). **CONFIRMED FACT.**
4. **Integritetsskyddsmyndigheten (IMY), the Swedish Authority for Privacy Protection** — lead GDPR supervisor (One-Stop-Shop) for Klarna Bank AB; can issue reprimands and administrative fines (see I.11). Other EEA DPAs (e.g., the German authority) route cross-border complaints to IMY. **CONFIRMED FACT.**
5. **Financial Conduct Authority (FCA), UK** — authorises and supervises **KFSUK** for regulated credit, payments, EMI and (from 15 July 2026) Deferred Payment Credit; enforces financial-promotion rules; the **Financial Ombudsman Service** and **s.75 Consumer Credit Act** protections attach to regulated products. **CONFIRMED FACT.**
6. **US federal:** **Consumer Financial Protection Bureau (CFPB)** — consumer-protection authority over BNPL (interpretive-rule saga, see I.9); **FDIC** — insurer/regulator relevant via **WebBank** and via Klarna's July 2026 industrial-bank application; **Federal Reserve** — not a holding-company supervisor of Klarna given the ILC route. **CONFIRMED FACT.**
7. **US state regulators:** state financial regulators for **money transmission** and lending licences (e.g., California DFPI for the CFL license); **Utah DFI** for WebBank and for the proposed Klarna Bank USA. **CONFIRMED FACT.**
8. **Australian Securities and Investments Commission (ASIC)** — from 10 June 2025 licenses BNPL providers under the National Consumer Credit Protection Act; AFCA membership required. **CONFIRMED FACT.**
9. **Central Bank of Ireland** — conduct-of-business supervision in Ireland for certain Klarna Bank AB activity (per product disclosures). **HYPOTHESIS / limited sourcing.**

---

## I.7 The Banking Licence Decision (NEW — pivotal)

**What happened.** On **19 June 2017**, Finansinspektionen granted Klarna a **full banking (credit-institution) licence**, effective immediately, after a ~20-month process. The entity became **Klarna Bank AB (publ)**. **CONFIRMED FACT.**

**What the licence permits that a payment-institution / consumer-credit licence would not.**
- **Deposit-taking from the public** — the defining permission. This let Klarna fund its lending book with **insured retail deposits** rather than only equity and wholesale money.
- **Full CRD/CRR credit-institution passporting** across the EEA — enabling cross-border lending and branch establishment under a single home-state licence.
- Ability to offer a **broad banking product suite** (savings accounts, cards, balance/current-account-like products) as principal.
**CONFIRMED FACT / ANALYTICAL INFERENCE.**

**What it cost — prudential obligations.**
- **Capital (CRR/CRD).** Klarna is subject to Pillar 1 (credit, CVA, market, operational risk), a **Pillar 2 requirement (P2R)** and **Pillar 2 Guidance**, plus buffers (capital conservation 2.5%, countercyclical, systemic where applicable) and a **leverage-ratio** requirement (Tier 1, min 3%). Per the **2024 Pillar 3 report (Klarna Holding AB Consolidated, in SEK):** CET1 capital SEK 12,970m; Tier 1 SEK 14,623m; total capital SEK 16,503m; total risk exposure amount SEK 77,022m; **CET1 ratio 16.8%, Tier 1 ratio 19.0%, total capital ratio 21.4%** (as of 31 Dec 2024). Total SREP own-funds requirement 9.2%; additional own-funds requirement (P2R) 1.2%. Klarna issued **AT1 and Tier 2** instruments to build an efficient capital stack. **CONFIRMED FACT.**
- **Liquidity:** LCR/HQLA portfolio management, ICLAAP, encumbrance monitoring. **CONFIRMED FACT.**
- **Governance:** three-lines-of-defence model; Audit, Compliance & Risk Committee (ACRC, 9 meetings in 2024); fit-and-proper assessment of board/CEO by FI (new board members/CEO are externally assessed by the SFSA); suitability, remuneration and diversity policies. **CONFIRMED FACT.**
- **Reporting:** annual Pillar 3 disclosures and quarterly capital disclosures; supervisory reporting to FI. **CONFIRMED FACT.**
- **Deposit-guarantee participation:** membership and fees to the Riksgälden-run scheme. **CONFIRMED FACT.**

**EEA passporting position.** Klarna Bank AB provides services in other EEA states by **passporting its licence under CRD IV (Directive 2013/36/EU)**, via **local branches** (e.g., Germany, into which Sofort GmbH merged) and cross-border services; the UK — post-Brexit — required a **separately FCA-authorised entity (KFSUK)** rather than passporting. **CONFIRMED FACT.**

**Analytical verdict — what the licence bought vs cost.** The licence converted Klarna from a payments intermediary into a **deposit-funded lender**. It bought (i) a **structurally cheaper, stickier funding base** (insured deposits vs wholesale), (ii) **EEA-wide distribution** under one licence, and (iii) a **product platform** (cards, savings, accounts). It cost **capital, liquidity, governance and reporting burden** and brought Klarna under FI's full prudential and AML enforcement (the SEK 500m AML fine, I.11, is a direct cost of being a bank). **The strategic point: most BNPL competitors (Affirm, Afterpay/Block, Zip, Sezzle, PayPal's Pay-in-4) are NOT licensed deposit-taking banks in their home markets. This is the single largest structural difference between Klarna and its peer group** — and it is why Klarna could grow Klarna Balance deposits from ~$9.5bn (2024) to ~$14bn (Sept 2025). Would Klarna be *viable* without it? Yes as a BNPL lender (as it is in the US via WebBank), but **not as the "digital bank" it now markets itself to be**; the licence is the foundation of the entire deposit-funded-bank thesis. **ANALYTICAL INFERENCE.**

---

## I.8 Funding Structure and Deposits

- **Retail deposits** are the primary funding source, taken principally in **Germany and Sweden** (Klarna cites "strong consumer demand for savings accounts in Germany and Sweden"), and increasingly via **Klarna Balance** accounts across markets. Per Klarna's January 2026 P2P-launch release: "Since the introduction of Klarna Balance in August 2024, global deposits have almost doubled, from **$9.5bn to $14bn by September 2025**." Earlier reporting cited "$8bn+" of customer deposits. **CONFIRMED FACT / COMPANY CLAIM.**
- **Deposit guarantee:** deposits at Klarna Bank AB are covered by the **Swedish scheme (Riksgälden)** up to ~SEK 1,050,000 (~€100,000). In the **US**, savings are held at **WebBank** (FDIC-insured), **not** at Klarna, at APY starting ~3.28%. **CONFIRMED FACT.**
- **Wholesale / structured funding:** Klarna supplements deposits with securitisation, warehouse and forward-flow arrangements — e.g., a **€1.4bn (~$1.6bn) warehouse facility with Santander** backed by German receivables (2025), and forward-flow / significant-risk-transfer programs (e.g., with Nelnet and Elliott) to offload US credit risk. **CONFIRMED FACT / THIRD-PARTY.**
- **Structural significance:** funding credit with **insured deposits** is cheaper and stickier than the **wholesale/forward-flow** funding on which non-bank BNPL competitors rely; it is a durable cost-of-funds advantage and a moat that regulation tends to widen. **ANALYTICAL INFERENCE.**

---

## I.9 The Moving Perimeter (NEW)

The regulation of Klarna's core product is **being written now**. State of play with dates:

**EU — Consumer Credit Directive II, Directive (EU) 2023/2225 (CCD II).** Published in the Official Journal **30 October 2023**, in force **19 November 2023**. **Transposition deadline 20 November 2025; application from 20 November 2026** (repealing CCD I / 2008/48/EC). CCD II **expands scope to BNPL**, abolishes the old €200 lower limit, raises the upper limit to €100,000, and imposes **creditworthiness assessment**, pre-contractual information (SECCI), and advertising rules. Many member states (e.g., Germany, Netherlands, Belgium, Greece) were **behind the November 2025 transposition deadline**; Germany's draft (Sept 2025) introduces a new point-of-sale financing supervisory regime (AbsFinAG) and a §34k GewO licensing requirement. **CONFIRMED FACT.**

**UK — Deferred Payment Credit (BNPL).** Sequence: **Woolard Review** published **2 February 2021** (26 recommendations; urgent call to bring BNPL into FCA regulation). HM Treasury consultations followed (2021, 2023, and **October 2024** under the new government). Legislation: **Financial Services and Markets Act 2000 (Regulated Activities etc.) (Amendment) Order 2025**, made **14 July 2025** (plus a No.2 Order of 16 June 2025 keeping merchant brokers exempt), bringing third-party **Deferred Payment Credit (DPC)** into the perimeter. The FCA consulted (CP25/23, July 2025) and published final rules in **Policy Statement PS26/1 on 11 February 2026**. **"Regulation day" is 15 July 2026**, from which DPC lending is a regulated activity requiring FCA authorisation or Temporary Permissions Regime (TPR) registration (TPR registration window 15 May–1 July 2026; 6 months thereafter to apply for full authorisation). New protections: affordability checks, FOS access, s.75 CCA protection (£100–£30,000), CRA reporting. For Klarna, **KFSUK (FRN 987889)** is the authorised entity. **CONFIRMED FACT.**

**US — CFPB interpretive rule (rescinded).** The CFPB issued an **interpretive rule (89 FR 47068)** in **May 2024** (effective 30 July 2024) classifying BNPL "digital user account" lenders as **credit-card providers** under TILA/Regulation Z (dispute rights, refunds, periodic statements). The **Financial Technology Association (FTA)** — whose members include **Klarna Bank AB**, Block, PayPal and Zip — sued in **October 2024** (APA challenge). Under new leadership the CFPB signalled in a **26 March 2025** filing it would rescind the rule, said on **6 May 2025** it would not prioritise enforcement, and **withdrew the rule on 12 May 2025**. **Net position: no BNPL-specific federal rule currently in force**, though the NCLC notes courts remain free to apply the 2024 interpretation's reasoning; state lending and money-transmission licensing still applies. **CONFIRMED FACT.**

**Australia.** The **Treasury Laws Amendment (Responsible Buy Now Pay Later and Other Measures) Act 2024** (royal assent 10 December 2024) extended the **National Credit Code** to BNPL. From **10 June 2025** providers (Afterpay, Zip, Klarna, humm) must hold an **Australian Credit Licence** and join AFCA; ASIC's **Regulatory Guide 281** (8 May 2025) sets out modified responsible-lending obligations and fee caps for "low-cost credit contracts." **CONFIRMED FACT.**

**Nordic/Sweden.** Klarna is already a licensed bank performing regulated credit and affordability assessment in its home market; Sweden has restricted the presentation of credit options ahead of debit at checkout. **CONFIRMED FACT (general) / limited specific sourcing.**

**Does BNPL regulation entrench Klarna or constrain it?** **Assessment: on balance it entrenches Klarna.** Klarna already (i) holds a **banking licence** and full prudential/AML/governance apparatus; (ii) performs **affordability/creditworthiness assessment** in regulated markets; (iii) **reports to credit bureaux** in several jurisdictions; and (iv) has compliance, capital and licensing infrastructure that **non-bank competitors must now build**. CCD II, the UK DPC regime and the Australian regime impose **fixed compliance costs that are proportionately far heavier on smaller/non-bank BNPL firms** and raise barriers to entry. The main genuine cost to Klarna is **friction/conversion loss** from mandatory checks and disclosures, and margin pressure where affordability rules bite. **Regulation is therefore more moat than cost for Klarna** — the clearest illustration being that Klarna joined the FTA to *oppose* the CFPB rule, yet is structurally better placed to absorb it than any competitor. **ANALYTICAL INFERENCE.**

---

## I.10 Follow-the-Credit-Risk by Jurisdiction

| Market | Underwriter | Lender of record | Partner bank originates? | Receivable sold? | Who bears loss? | On Klarna balance sheet? | Licence support |
|---|---|---|---|---|---|---|---|
| **Sweden / Nordics** | Klarna Bank AB | **Klarna Bank AB** | No | Generally no (held) | **Klarna Bank AB** | Yes | FI banking licence |
| **Germany** | Klarna Bank AB (German branch) | **Klarna Bank AB** | No | Partly (Santander warehouse; forward-flow) | **Klarna Bank AB** (net of transfers) | Yes | FI licence + CRD passport/branch |
| **Rest of EEA** | Klarna Bank AB | **Klarna Bank AB** | No | Varies | **Klarna Bank AB** | Yes | FI licence + CRD passport |
| **UK** | KFSUK / Klarna Bank AB | **KFSUK** (from regulation) | No | Varies | **Klarna group (KFSUK)** | Yes | FCA authorisation (FRN 987889) |
| **United States** | **Klarna Inc.** (underwriting/servicing) | **WebBank** (Utah ILC) | **Yes — WebBank originates** | **Yes — Klarna Inc. purchases the receivables shortly after origination** | **Klarna** (bears predominant credit risk; offloaded via forward-flow, e.g. Nelnet/Elliott) | Yes (until sold) | WebBank charter + Klarna Inc. CFL / state licences |
| **Australia** | Klarna Australia | Klarna Australia | No | Varies | Klarna group | Yes | ACL (from 10 June 2025) |

**US detail (priority precision).** In the US, **WebBank** — a **Utah-chartered, FDIC-insured industrial bank** — is the **lender/originator of record** for Klarna's financing, one-time card and Klarna Card products ("issued by WebBank"; and per Klarna's Vermont disclosure, "**THIS IS A LOAN SOLICITATION ONLY. KLARNA INC. IS NOT THE LENDER**"). **Klarna Inc. then purchases the receivables from WebBank shortly after origination** and **bears the predominant credit-loss economics** (Klarna's own risk factors state its consumer credit products are "not secured by any collateral, nor… guaranteed or insured by any third party"), which it partly offloads via forward-flow / significant-risk-transfer programs. The purpose of the **bank-partnership ("rent-a-charter") model** is **interest-rate exportation**: because WebBank is a Utah bank, Utah's favourable rate authority is exported to consumers in other states regardless of local usury caps, and Klarna avoids needing a lending licence in every state (Klarna Inc. holds a **California Financing Law license (#60DBO-44020)** and state money-transmitter licences for activities outside the WebBank structure). This model carries **"true lender" / Madden v. Midland** legal risk (a regulator could argue Klarna, bearing the predominant economic interest, is the true lender — as alleged in *Colorado v. Avant/Marlette*). On **6 July 2026**, Klarna applied to the **Utah DFI and FDIC** to establish **Klarna Bank USA**, a Utah-chartered **industrial bank** wholly owned by Klarna Inc. (proposed CEO Gary Harding), which — if approved — would **bring lending in-house and reduce reliance on WebBank** (application pending; not approved; approval can take well over a year). **CONFIRMED FACT.**

---

## I.11 Enforcement, Supervision and Data Protection (PRIORITY DEPTH)

**Enforcement ledger:**

| # | Date | Authority | Entity | Conduct | Outcome / Amount | Admission? |
|---|---|---|---|---|---|---|
| 1 | **11 Dec 2024** | **Finansinspektionen** | **Klarna Bank AB** | AML deficiencies (period 1 Apr 2021–31 Mar 2022): no general risk assessment of how products could be used for ML/TF; inadequate customer due-diligence procedures/guidelines for the invoice product; model-risk gaps | **Remark + administrative fine of SEK 500 million (~$45 million)** (FI: "FI is issuing Klarna Bank AB a remark and an administrative fine of SEK 500 million for violating the anti-money laundering regulations… Klarna's general risk assessment has had significant deficiencies," DG Daniel Barr); FI declined to withdraw authorisation or issue a warning | **No admission of ML**; Klarna framed it as "rule interpretation and application, not actual cases of money laundering" |
| 2 | **28 Mar 2022** | **IMY** (Swedish DPA), One-Stop-Shop | **Klarna Bank AB** | GDPR transparency failures (Arts 5(1)(a), 13, 14) re privacy notices used Mar–Jun 2020 (inadequate information on data processing/rights) | Administrative fine **SEK 7.5 million (~€724k / $733k)** | Contested/appealed |
| 3 | **2023 (lower court)** | Stockholm Administrative Court | Klarna Bank AB | Appeal of #2 | Fine **reduced to SEK 6 million** | — |
| 4 | **11 Mar 2024** | Stockholm Administrative Court of **Appeal** (case 2829-23) | Klarna Bank AB | Final appeal of #2 | Fine **reinstated to SEK 7.5 million** (final) | Liability upheld (narrower than IMY's original view) |
| 5 | **25 Mar 2025** | **IMY** | Klarna Bank AB | GDPR Art 15 access-request handling delay (complaint IMY-2022-10270) | **Reprimand** (minor infringement, recital 148) — no fine | Remedied |
| 6 | **~2022–2023** | IMY / German DPA (OSS) | Klarna Bank AB | Art 15 access-request complaint routed via German DPA | Closed after Klarna complied | Remedied |

**Governance dispute (2023–2024).** Treated in depth in I.4; recorded here as governance evidence: the Miller/Moritz EGM episode (winter 2023/24) and the Walther removal (Oct 2024, ~87% shareholder approval), rooted in the Siemiatkowski–Jacobsson rift and the golden-share/SPV disputes, with the disclosed **$35bn** potential CEO bonus a flashpoint.

**What the aggregate record reveals.** The material record is **one significant prudential/AML fine and a cluster of GDPR transparency/access findings** — serious for a bank of Klarna's size but **not evidence of systemic misconduct or consumer-fraud findings**; FI expressly declined to withdraw the licence or issue a warning and noted "all other major banks have received reprimands" under AML rules. The **control-environment signal is mixed**: rapid growth outran AML and data-transparency controls (both fixed after the fact), consistent with a fast-scaling fintech maturing into bank-grade compliance. The governance disputes are a **larger institutional-risk signal** than the fines. **ANALYTICAL INFERENCE.**

---

## I.12 Acquisitions and Corporate Development

| Date | Target | Country | Consideration | Licence/asset gained | Strategic purpose |
|---|---|---|---|---|---|
| Nov 2016 | Cookies (assets) | Germany | Undisclosed (low) | — | Talent/IP |
| Feb 2017 | **BillPay** | Germany | Undisclosed | ~5,000 merchant partners | German merchant scale |
| Dec 2013 → closed Mar 2014 | **Sofort GmbH** | Germany | **~$150m (~€150m)** | Sofortüberweisung open-banking rails; German market lead | European scale + open banking (merged into Klarna Bank AB Dec 2024) |
| May 2018 | ShopCo (IP + 8 staff) | Germany | < "mid double-digit millions" | Browser tech | Product |
| Sept 2018 (→2019) | **Close Brothers Retail Finance** | UK | Undisclosed | UK retail-finance book & merchants | UK retail-finance expansion (FI approval required) |
| Apr 2020 | Nuji | UK | Undisclosed | — | Shopping/discovery |
| Jul 2021 | **Stocard** | Germany | **~€110m** | Loyalty wallet, ~60m users | Consumer engagement |
| Jul 2021 | APPRL; HERO | Sweden/UK | Undisclosed | Social commerce; virtual shopping | Merchant tools |
| Oct 2021 | Inspirock | US/India | Undisclosed | Trip planning | Travel vertical |
| Nov 2021 → completed 4 Apr 2022 | **PriceRunner** | Sweden/Nordics | Undisclosed (reported ~$1bn) | Price-comparison platform | Comparison shopping / ad revenue |

**What the pattern reveals.** Two phases: **(1) infrastructure/licence acquisitions (2013–2019)** — Sofort, BillPay, Close Brothers Retail Finance — building European payment rails, merchant density and regulated-credit capability; **(2) consumer-engagement/network acquisitions (2020–2022)** — Stocard, PriceRunner, Inspirock, HERO — pivoting toward a **shopping "super-app"/network** ahead of the IPO narrative. The 2013–19 deals were about **becoming a bank and a payments backbone**; the 2020–22 deals were about **owning the consumer relationship**. **ANALYTICAL INFERENCE.**

---

## I.13 Institutional Dependency Map

| Dependency | Rank | Rationale / single point of failure |
|---|---|---|
| **Swedish banking licence (FI)** | **Critical** | The entire deposit-funded-bank model and EEA passporting rest on it; withdrawal (not threatened) would collapse the funding and product thesis |
| **US bank partner (WebBank)** | **Critical (US)** | Sole US lender of record until/unless Klarna Bank USA is approved; loss would halt US lending; mitigated by pending ILC application |
| **Retail depositors / funding markets** | **High** | ~$14bn deposits fund the book; deposit flight or loss of forward-flow/warehouse capacity (Santander, Nelnet, Elliott) would pressure liquidity |
| **Merchant relationships** | **High** | Revenue is merchant-fee driven; concentration risk across ~790k merchants (individually diffuse, but platform/large-merchant churn matters) |
| **Card networks / acquirers (Visa)** | **High** | Klarna Card issued under Visa licence; card rails essential for card products |
| **Credit bureaux / data providers** | **High** | Underwriting and (increasingly mandatory) affordability/CRA reporting depend on bureau data across jurisdictions |
| **Cloud / technology (AWS)** | **High** | Core processing built on AWS; outage/lock-in risk |
| **Regulators (FI, FCA, CFPB, ASIC, IMY)** | **High** | Moving perimeter; adverse rules or enforcement could raise costs, though net-moat as argued |
| **Key individuals (Siemiatkowski; Moritz)** | **Moderate** | Founder-CEO concentration + super-voting shares; succession/governance risk |

**Single points of institutional failure:** the **FI banking licence** and, in the US, the **WebBank relationship**. **ANALYTICAL INFERENCE.**

---

## I.14 Volume I Reconstruction

1. **Entity & Permission Map:** Klarna Group plc (UK holdco, no licence) → Klarna Holding AB (Swedish intermediate holdco, prudential consolidation) → **Klarna Bank AB (publ)** (the licensed bank; EEA branches incl. Germany; UK via KFSUK) and **Klarna Inc.** (US operating co., not a lender; uses WebBank).
2. **Ownership & Voting-Control Map:** Sequoia ~20%+, Jacobsson ~31.4m shares, Siemiatkowski ~25.6m (Class C super-vote), Heartland 7.86%, CBA ~5%; Class B (10 votes, no economics) concentrate ~99% of votes in pre-IPO holders; not a "controlled company," but insiders control if acting together.
3. **Regulator Inventory:** FI (home prudential/AML); ECB/SSM (N/A — Sweden non-euro); Riksgälden (DGS); IMY (GDPR); FCA (UK); CFPB/FDIC/Fed + state regulators (US); ASIC (Australia); CBI (Ireland, conduct).
4. **Banking Licence Analysis:** granted 19 Jun 2017; bought deposit funding + EEA passporting + product platform; cost CRR/CRD capital (CET1 16.8%, total 21.4% at end-2024), liquidity, governance and AML burden. The defining peer differentiator.
5. **Funding Structure:** deposits (~$9.5bn→$14bn) in Sweden/Germany + Klarna Balance; DGS-insured; wholesale/warehouse (Santander €1.4bn) and forward-flow supplement.
6. **Moving-Perimeter Assessment:** EU CCD II (apply 20 Nov 2026); UK DPC (regulation day 15 Jul 2026, PS26/1); US CFPB rule withdrawn 12 May 2025; Australia NCC from 10 Jun 2025 — net **moat > cost** for Klarna.
7. **Credit-Risk-by-Jurisdiction Matrix:** EEA/UK — Klarna is lender and risk-holder; US — **WebBank originates, Klarna Inc. buys receivables and bears loss** (rate exportation via Utah charter).
8. **Enforcement Ledger:** SEK 500m FI AML fine (Dec 2024); SEK 7.5m IMY GDPR fine (2022, reinstated on appeal Mar 2024); 2025 IMY reprimand.
9. **Acquisition Table:** Sofort (2014, ~$150m), BillPay (2017), Close Brothers Retail Finance (2018), Stocard (2021, ~€110m), PriceRunner (2022), and others.
10. **Institutional Dependency Map:** Critical — FI licence and WebBank; High — deposits, merchants, Visa, bureaux, AWS, regulators.
11. **Corporate Chronology:** 2005 founded → 2010 Sequoia/Klarna rename → 2014 Sofort → 2017 banking licence → 2018 Close Brothers RF → 2019 US launch → 2021 $45.6bn peak → 2022 $6.7bn down round → May 2024 UK redomiciliation → Dec 2024 SEK 500m AML fine → Sept 2025 NYSE IPO → Jul 2026 Klarna Bank USA application / UK DPC regulation day.
12. **Key Unknowns:** exact Australian entity name/ACL number; precise F-1 language on US receivable-purchase timing; current statutory SEK DGS cap (1,050,000 vs 1,150,000); precise merchant concentration. (Confirmed: Klarna is a "category 2 institution," NOT an O-SII — Sweden's O-SIIs are only Nordea, Handelsbanken, SEB and Swedbank.)
13. **Ten Most Important Conclusions:** (i) Klarna is legally a **Swedish bank**, not a BNPL app; (ii) the **real business is Klarna Bank AB**; (iii) **control** sits with the Siemiatkowski–Moritz–Sequoia coalition via multi-class shares; (iv) **credit risk sits on Klarna's balance sheet in the EEA/UK but is originated by WebBank in the US**; (v) **FI is the regulator that matters most**; (vi) the **2017 licence** is the pivotal structural decision; (vii) **deposit funding** is a durable cost advantage over non-bank peers; (viii) **BNPL regulation entrenches rather than constrains** Klarna; (ix) the **US arrangement is the group's biggest structural anomaly** and the July 2026 ILC application aims to fix it; (x) the **valuation rollercoaster is financing noise**, not structure.

**Central questions answered.** *What is Klarna, legally?* A licensed Swedish credit institution (Klarna Bank AB) under a UK-listed holding company. *Which entity is the real business?* Klarna Bank AB. *Who controls it?* Founders (Siemiatkowski, Jacobsson interests) and Sequoia, via super-voting shares. *Who bears the credit risk, and does it change by country?* Klarna does — on its own balance sheet in the EEA/UK, but in the US the loan is originated by WebBank and the risk is transferred to Klarna by purchase. *Which regulator matters most?* Finansinspektionen. *What did the banking licence buy and cost?* It bought deposit funding, EEA passporting and a banking product platform; it cost capital, liquidity, governance and AML burden. *Is Klarna a bank that distributes through merchants, or a merchant-services company that owns a bank?* **It is a bank that distributes through merchants** — a deposit-funded Swedish credit institution whose distribution strategy is point-of-sale — **and the coming wave of BNPL regulation entrenches it**, because it already carries the licence, capital and compliance apparatus that its non-bank competitors must now build.

---

*End of Volume I. Volume II (economics of the merchant-pays model, unit economics, funding cost decomposition and credit performance) not begun, per instruction. Where the record is contested (e.g., exact SEK DGS cap; precise US receivable-purchase interval in the F-1; the Australian licensed-entity name), the point is flagged as a Key Unknown rather than resolved by inference.*

---

# VOLUME II — Product, the Merchant-Funded Customer Structure & Value-Flow Architecture

## TL;DR
- **Klarna's true core product is short-dated merchant-funded credit at the point of sale, and the merchant — not the consumer — is the paying customer.** Klarna monetises primarily by driving GMV for retailers, charging a US merchant discount rate of 3.29–5.99% + $0.30 versus an EU consumer-card interchange cap of 0.3%. In FY2025 Klarna reported GMV of $127.9bn (+22% YoY), total revenue of $3.5bn (+25%), 118 million active consumers (+28%) and 966,000 merchants (+42%) — a ~2.75% take rate — but a net loss of **$(273)m** (of which $(294)m attributable to shareholders; EPS $(0.79)) — *corrected on assembly; this section originally gave the attributable figure as the total, see Appendix D note 1*, swinging from a small profit in FY2024.
- **The economics only make sense through the lens of book velocity, not credit-card yield.** Klarna's average receivable duration is ~40 days and 85% of loans are ≤3 months, so the book turns ~9x/year; a 0.44–0.65%-of-GMV loss rate is therefore an order of magnitude different in kind from a revolving card's loss on a year-long balance. Take rate on volume, not yield on assets, is the correct measure of the core product.
- **The consumer is the bait, not the customer, for the core Pay-in-4/Pay-in-30 product — but that flips on the Fair Financing product, where the consumer becomes the principal payer via interest.** The central unresolved question — what share of consumer-fee revenue comes from what share of (likely vulnerable, repeat) users — is **UNKNOWN** from public data and is the crux of the consumer-harm debate.

## Key Findings

1. **Merchant fees are the engine.** In 2024, transaction & service revenue was ~76% of total revenue and interest income ~24%; within transaction & service revenue, merchant fees were ~75%, consumer service revenue (mainly late/reminder fees) ~16%, and advertising ~8%. Roughly two-thirds of total revenue is merchant-side, one-third consumer-side. **CONFIRMED FACT** (Klarna F-1/DRS).

2. **The uplift claims are marketing and only partly corroborated.** Klarna's COMPANY CLAIMs — "40% higher AOV, 20% better conversion, 46% higher purchase frequency" — are not independently reproducible at those magnitudes; independent retailer case studies suggest AOV uplifts nearer 20–35%, and academic work finds BNPL spending is substantially *incremental* (a "liquidity flypaper effect") rather than pure substitution, which validates the merchant's willingness to pay but also grounds the consumer-harm critique.

3. **Take rate (~2.75% FY2025) sits between the pure pay-in-4 model and Affirm's interest-heavy model.** Klarna's ~2.1–2.8% take rate versus Affirm's ~7–9% reflects product mix: Klarna is predominantly 0%-interest short-term credit, Affirm skews to longer interest-bearing loans. Take rate is rising, driven by US mix and Fair Financing.

4. **The escalation ladder is simultaneously the monetisation path and the risk path** — exactly the Robinhood finding. Each rung (Pay-in-30 → Pay-in-4 → Fair Financing → Card → Balance/deposits → Plus) raises revenue per user and raises the consumer's credit exposure. Banking consumers (15.8m, up 101% YoY in Q4 2025) generate $107 revenue/user vs ~$30 for the average consumer.

5. **Advertising is a genuine second, Experian-like inversion but still modest in scale** — $180m in 2024 (6% of revenue), ~$230m estimated 2025, up from $13m in 2020. Klarna sells access to the attention of the consumer it acquired as bait for the merchant, and this creates a real conflict: Klarna both advises consumers where to shop (PriceRunner, app) and is paid by merchants for placement.

## Details

### II.1 The Product Universe (by legal entity)

Klarna's offering must be attributed to the entity that provides it. **In the EEA and UK, Klarna Bank AB (publ) (and Klarna Financial Services UK Ltd) is the lender of record and holds the credit risk. In the US, WebBank (a Utah industrial bank) originates and Klarna Inc. purchases the receivables and bears the predominant credit-loss economics**, offloading much through forward-flow arrangements (Nelnet, Elliott/Värde). Klarna Group plc is the non-operating NYSE-listed holding company.

**Payment products:**
- **Pay in Full / Pay Now** (Sofort direct bank transfer heritage): instant settlement; merchant pays a fee, consumer pays nothing. Job-to-be-done: frictionless checkout. Strategic purpose: acquisition/retention.
- **Pay in 30 days / invoice** (the original 2005 product): consumer receives goods, pays in ≤30 days interest-free. Merchant fee up to ~5.99%. Strategic purpose: conversion uplift; the core "try before you buy" hook, especially in fashion.
- **Pay in 3 / Pay in 4 instalments**: split into 3 (every 30 days) or 4 (every 14 days) interest-free payments. Merchant-funded; consumer pays only late fees. This is the canonical BNPL product.
- **Fair Financing** (longer-term instalment credit, 6–36 months): interest-bearing (0%–~33.99% APR US; up to 21.9% UK representative). Merchant fee lower (up to ~3.29% US). This is where the **consumer becomes the principal payer**. GMV grew 165% YoY in Q4 2025 to $4.5bn; transaction margin over twice the group average.

**Banking / consumer products:**
- **Klarna Card** (physical + virtual Visa): launched UK Jan 2022, relaunched/expanded US July 2025. 4.2m active card users by Q4 2025, up 1.9m QoQ; card volume ~15% of total transactions. Earns interchange (~1% avg, mostly Europe). Strategic purpose: everyday spend, distribution, defensive vs. debit.
- **Klarna Balance** (deposit account, launched Aug 2024) + **savings accounts** (US high-yield ~3.28% APY; new high-yield launched June 2026): deposits grew from ~$9.5bn (2024) to ~$14bn (Sept 2025). Structural funding differentiator; ~90% deposit-funded model.
- **Klarna app**: 47–49m MAU; product discovery, order tracking, returns, budgeting, AI assistant, offers. The monetisation surface for advertising.
- **PriceRunner**: comparison-shopping service acquired 2022; structured product catalogue powering the app's shopping shelf.
- **Klarna Plus**: subscription (~$7.99/mo US) — waived one-time card fees, double rewards, exclusive offers; surpassed 1m members Q3 2025; ~3% of revenue, grew 131% YoY.
- **Cashback & rewards**: consumer incentives to consolidate spend on the network.
- **P2P money transfers**: launched Jan 2026 in 13 European markets; initially Klarna-to-Klarna domestic.
- **KlarnaUSD stablecoin**: announced Nov 2025, launching 2026 (forward-looking).

**Merchant-side integrations:**
- **Klarna Payments** and **Klarna Checkout** (KCO): merchant-side APIs. KCO was sold (relevant to like-for-like adjustments in results).
- **Advertising / merchant marketing services**: sponsored search, affiliate, brand ads.
- **Open banking** (Sofort/Kosma heritage): account information & payment initiation services.

### II.2 The Merchant-Funded Customer Structure (THE RE-CUT)

Klarna has five payer classes:

1. **Merchants (primary payer).** Pay 3.29–5.99% + $0.30 (US) — value-based + fixed pricing varying by vertical and geography; US take rates are higher than Europe. No single merchant is >10% of GMV in any major market. On average 48% of the top 100 merchants in each major market used Klarna, and 66% advertised on the network, in the LTM to mid-2025.
2. **Consumers (mostly pay nothing).** They pay: late fees (£5 UK / $7 US caps, max 25% of order); interest on Fair Financing; Klarna Plus subscription; FX margin on cross-border card use; and one-time card fees (waived for Plus). 98% of transactions were interest-free (LTM to June 2025).
3. **Advertisers** (merchants again, wearing a second hat): pay CPC/affiliate/brand fees for placement in the app and on PriceRunner.
4. **Card networks / interchange**: Klarna earns issuer interchange (~1% avg) on Klarna Card spend.
5. **Depositors and the funding spread**: Klarna earns the net interest between low-cost deposits (~90% deposit-funded) and lending yield.

**Verdict:** For the Pay-in-4/Pay-in-30 core, **the consumer is the bait and the merchant pays for conversion**. For Fair Financing, **the consumer is the customer** (interest payer). For the Card/Balance/deposits, the consumer is a **banking customer** monetised through interchange and funding spread. The answer genuinely differs by product line — which is the whole strategic point of the escalation ladder.

### II.3 Why Merchants Pay (the analytical heart)

**The causal mechanism.** Deferred payment at checkout increases merchant revenue through five channels: (i) conversion-rate uplift / cart-abandonment reduction; (ii) average-order-value uplift; (iii) incremental new-customer acquisition; (iv) higher purchase frequency / repeat; (v) access to younger and thin-file consumers who would not otherwise transact.

**Klarna's own claims (COMPANY CLAIM, to be tested):** "40% higher AOV, 20% better conversion, 46% higher purchase frequency." Stripe (reselling Klarna) claims "as much as 40% of Klarna customers are new to their brand" and "revenue increase by up to 6.6% on Klarna eligible sessions." A published Klarna case study (Rue21) claimed AOV 73% higher than other payment methods. These are marketing figures and are not independently reproducible at those magnitudes.

**Independent / academic test.**
- Independent retailer reviews put AOV uplift nearer **20–35%**, not 40–45%.
- The pivotal academic question is **incremental vs. substitutional**. Di Maggio, Williams & Katz (2022), using transaction-level data on >10m US consumers, find BNPL access **boosts total spending and retail spending** — a "liquidity flypaper effect" whereby retail liquidity "sticks where it hits." Maesen & Ang (2025), using difference-in-differences on a large US retailer, find BNPL adoption raises **purchase incidence and amounts**. This corroborates the merchant's rational willingness to pay: BNPL genuinely creates incremental sales, at least for liquidity-constrained consumers.
- The same literature is the ground of the harm critique: deHaan et al. (2024, *Management Science*, "Buy Now, Pay (Pain?) Later") find first-time BNPL users experience **higher overdraft charges and credit-card interest/late fees** (up to ~$252/year extra banking charges for some subsets). The Central Bank of Ireland (2025) experimentally confirms a "mental-budget" mechanism raising spending.

**Why a merchant pays several per cent when card interchange is capped at 0.3%.** Under the EU Interchange Fee Regulation (Reg. 2015/751, in force since 9 Dec 2015), consumer credit-card interchange is capped at 0.3% and debit at 0.2%. Klarna charges an order of magnitude more (3–6%). The merchant pays the premium because Klarna is **not a payment rail substitute but a marketing/conversion service**: the fee is bundled credit-risk transfer + fraud protection + a demonstrable uplift in completed sales and basket size. If BNPL adds >6% to net revenue (via conversion + AOV), a ~6% fee is rational. This is the same logic by which merchants tolerate Amex's higher fees for a higher-spending cardholder base.

**Competitive dynamic / pricing power.** Klarna's pricing power depends on consumer expectation. Once consumers expect Klarna at checkout (approximately 84% of Swedish adults were active users as of June 2025), a merchant dropping Klarna risks losing conversions — giving Klarna Amex-like "must-accept" leverage in mature markets. But in less-penetrated markets, and where PSPs (Stripe, Adyen) commoditise BNPL access and multiple providers compete, merchant switching costs are low and pricing power is weaker. Net dollar revenue retention of 115% (Q1 2025) indicates merchants are expanding, not fleeing.

### II.4 Take Rate and Revenue Decomposition

**Revenue lines (FY2024, IFRS, USD):**
- Transaction & service revenue ~76% of $2.81bn, of which merchant fees ~75%, consumer service (reminder/late fees) ~16%, advertising ~8%.
- Interest income ~24% (~$675m). Within interest income (2023 detail, USD): Fair Financing $318m, "Snooze" fees $96m, debt securities $75m, incremental merchant fees $19m.
- Advertising: $180m (2024), ~6% of revenue.

**FY2025 (IFRS, USD):** revenue $3.51bn; transaction revenue ~$2.50bn (~71%), interest income ~$937m (~27%), consumer service revenue ~$73m (~2%). Regional: US $1.24bn (35%), Germany $848m (24%), UK $442m (13%), other $976m (28%).

**Take rate = revenue / GMV:** 2.3% (2022) → 2.7% (2024) → ~2.75% (FY2025); Q4 2025 reached 2.80%, the highest to date. Drivers: US mix (higher take rates), Fair Financing growth, and rising consumer-service (late-fee) and advertising revenue. Management itself cautions take rate is "not a particularly important metric" because it is driven by product/geographic mix — a tell that the number is a mix artefact, not a pricing decision.

**Peer comparison (careful — GMV/revenue defined differently):**
- **Affirm**: take rate ~7–9% of GMV (RLTC ~3–4% of GMV), because it is interest-heavy and longer-duration; FY-Q3'26 GMV $11.6bn, revenue $1.04bn (~9%), RLTC 4.31% of GMV.
- **Klarna**: ~2.1–2.8% — lower because predominantly 0% short-term.
- **Afterpay (within Block)**, **PayPal Pay Later**, **Zip**, **Sezzle**: pure pay-in-4 models cluster nearer Klarna's merchant-fee-driven take rate than Affirm's.
The comparison confirms: Klarna's low take rate is a *feature* of the merchant-funded, interest-free model, not weakness.

### II.5 Consumer Economics — what the "free" user actually pays

- **Interest-free proportion:** 98% of transactions interest-free (LTM June 2025); 91% of transactions interest-free Pay Later in 2025 (a different cut).
- **Late fees:** UK up to £5, charged only after 7 days, max 2 per order, capped at 25% of order; US up to $7 after 10 days, capped at 25%; Pay-in-30 has no late fee in the US.
- **Klarna's own transparency (Wikipink, self-reported):** UK 2023 — 60% of purchases paid early, 35% on time, 5% late; 5.18% of orders received a late fee; 4.6% of orders were paid *after* receiving a late fee (i.e., cured); 0.61% referred to an FCA-approved debt collector; default rate 0.4%. US 2023 (Pay in 4) — 31% early, 65% on time, 4% late; 4% of orders received a late fee; 2% referred to a debt collector; "99% Klarna balance repaid," <1% global default. Average UK outstanding balance ~£150 vs ~£1,295 on a credit card.
- **Fair Financing APR:** 0%–~33.99% US; up to 21.9% UK representative.
- **Consumer-fee share of revenue:** consumer service revenue ~16% of transaction & service revenue in 2024 (up from 12% in 2022) — a rising but still minority share; ~2% of total revenue in FY2025.
- **The distributional crux — UNKNOWN.** The question that matters most for consumer-harm — *what share of consumer-fee revenue comes from what share of (likely repeat, subprime) users* — is **not disclosed by Klarna or any regulator**. The CFPB explicitly states it collected only portfolio-level aggregates ("We did not collect data at the loan or account level"). Proxy evidence, from the CFPB report "Consumer Use of Buy Now, Pay Later and Other Unsecured Debt" (Jan 2025): "About 20 percent of borrowers in 2022 were heavy users originating more than one BNPL loan on average each month"; "approximately 63 percent of borrowers originated multiple simultaneous loans at some point during the year, and 33 percent took out loans from multiple BNPL lenders"; and "the majority of consumers who use BNPL (61%) have subprime or deep subprime credit scores" (45% deep subprime, 16% subprime). This strongly *suggests* fee revenue is concentrated among a vulnerable minority, but the direct fee-concentration figure remains unavailable. **What would settle it:** account-level fee-incidence data by user decile, which regulators could compel under the CCD II / FCA regimes. Klarna itself frames late fees as deliberately small: "We charge the lowest late fees we can to ensure they act as a deterrent to missed payments, but that they do not become a large proportion of our income."

### II.6 The Velocity of the Book (NEW)

**Duration by product.** Per the Klarna Bank AB H1-2025 Interim Report: "the average duration of our loans is approximately 40 days and 85% of our loans were three months or less in duration" (the FY2025 annual report updates this to 84%). Average balance per active consumer was **$80** (Pay in Full $0; Pay Later $88; Fair Financing $408) — versus an average balance per US credit card of ~$6,730 (Experian, 2024). Loans to the public were SEK 100.1bn at 30 June 2025 — a snapshot of outstanding loans, not annual originations.

**Turnover.** With ~40-day average duration, the book turns **~9x/year** (365/40 ≈ 9.1). This is the single most important economic fact about Klarna and the reason it must not be analysed as a credit card.

**Why a given loss rate means something completely different.** On a revolving card, a balance sits outstanding for ~a year, so a 5% annual loss rate is 5% of a year-long asset. On Klarna's book, the same dollar of capital funds ~9 loans a year; a **loss of 0.44–0.65% of GMV** (Q3–Q4 2025) is applied to volume that recycles nine times, so the capital at risk per dollar of GMV is tiny and the capital velocity (asset turnover) is ~9x. The correct lens for the core product is therefore **take rate on GMV** (≈2.75%) minus **loss rate on GMV** (≈0.5%) minus funding and servicing on GMV — not net interest margin on assets. As Klarna puts it, the "asset-light balance sheet" "sets us apart from more traditional banks whose longer loan durations tie up capital."

**Credit performance (CONFIRMED FACT, company-reported):**
- Consumer credit losses were **0.47% of GMV in 2024** (Klarna F-1), versus ~3.7% loan-loss-to-loans for Swedish bank peers and 0.77% for US commercial banks (2023) — Klarna's headline underwriting claim.
- Provision for credit losses: 0.56% of GMV (Q2 2025), 0.72% (Q3 2025), 0.65% (Q4 2025), 0.55% (Q1 2026). Realised losses: 0.44–0.45% of GMV.
- Swedish statutory basis (SEK): credit losses net were **0.57% of GMV in H1 2025** (H1 2024: 0.46%) — note the divergence from the USD IFRS group figure and the different basis.
- Absolute losses rose (2024 ~$495m; FY2025 provisions $794m) as Pay Later and Fair Financing scaled, especially in the US.
- Delinquency: BNPL 0.88% (Q2 2025, down from 1.03%); Fair Financing 2.18%.
- **Recoveries via collections:** UK 2023 — 4.6% of orders were paid *after* receiving a late fee (cured), and only 0.61% went to a debt collector; the addition of late fees in 2023–24 drove a 55% improvement in on-time payment and cut UK pay-in-3 collections referrals from 1.95% to 0.84% (Bloomberg, documents seen).

### II.7 The Advertising and Comparison Business

- **Size/growth:** $13m (2020) → $180m (2024, 6% of revenue) → ~$230m estimated 2025 (~7%). Advertising was $184m in the LTM to June 2025.
- **Pricing model:** CPC (pay when a consumer clicks a sponsored placement) plus affiliate (pay on purchase) and brand ads; sponsored search in the app.
- **Reach:** 47–49m app MAU. App users are far more valuable: average active user ~$28/year revenue; shopping+cashback users ~$90.
- **PriceRunner:** acquired 2022; supplies the structured catalogue for the app's shopping shelf and drives high-intent traffic to retailers. On 1 July 2026 the Stockholm Patent and Market Court ordered Google to pay PriceRunner ~14.3bn SEK (~$1.97bn, including ~$500m accrued interest) for preferencing Google Shopping over independent comparison services across the UK, Swedish and Danish markets (2008–2023) — the largest antitrust damages award in Swedish history, though PriceRunner had sought ~$8.3bn and the award is subject to appeal, litigation-funder/investor sharing arrangements and tax.
- **Assessment:** a genuine second business and a real strategic option (a retail-media network on first-party purchase-intent data), but still a modest adjacent line at ~6–7% of revenue — not yet an Amazon/Retail-Media-scale profit centre.
- **The conflict:** Klarna both advises consumers where to shop (comparison, "inspirational catalogue") and is paid by merchants for placement. This is the Experian-style inversion — the consumer acquired as bait is re-monetised by selling their attention — and it embeds an advice/payment conflict that regulators will scrutinise.

### II.8 Customer Segmentation and Disclosed Metrics

- **Active consumers:** 111m (Q2 2025) → 114m (Q3) → 118m (Q4 2025, +28% YoY). US 29m (11% of US adults).
- **Merchants:** 790k (Q2 2025) → 850k (Q3) → 966k (Q4 2025, +42% YoY) → >1m (Q1 2026). (Merchant count = unique brand×market combinations.)
- **GMV:** $105bn (2024) → $127.9bn (FY2025, +22%). ~3.4m transactions/day; >1.45bn transactions in 2025.
- **AOV:** low — average balance per consumer $80; core purchases in the $50–500 band.
- **Transactions per consumer/year:** cohort disclosure shows **3x in year 1 rising to 11x by year 3** (2022 cohort) — clear evidence of deepening engagement.
- **Revenue per consumer:** ~$30 average; banking consumers $107 (Q4 2025); banking consumers 15.8m (up 101% YoY).
- **Demographics (Klarna survey, Q3'23, n=16,370):** 58% female / 42% male; education spread (40% university, 32% secondary, 22% post-secondary); geography spread (42% city, 37% suburb, 21% rural); "representative of the broader population" — Klarna's rebuttal to the "targets the vulnerable" critique.
- **Concentration:** no single merchant >10% of GMV in any major market (GMV diversification); the frequency data imply GMV concentrates in the most engaged consumer cohorts.

### II.9 The Escalation Ladder and the Customer Journey

Lifecycle: **first Pay-in-30 → repeat use → Pay in 4 → Fair Financing → Klarna Card → Klarna Balance/deposits → Klarna Plus subscription**. Each rung raises revenue per user (from ~$30 to $107 for banking consumers; 3x→11x transactions) *and* raises credit exposure and product complexity.

**This is the direct analogue of the Robinhood finding: the ladder is simultaneously the monetisation path and the risk path.** As with Robinhood's options/margin escalation, each rung that lifts Klarna's revenue also increases the consumer's leverage and default risk — Fair Financing carries interest and a 2.18% delinquency rate versus 0.88% for BNPL. The difference from Robinhood: Klarna's underwriting gates each rung, and short duration limits per-transaction exposure. But the structural identity — engagement designed to escalate revenue and exposure together — is the same.

### II.10 Value-Flow Reconstruction — three transactions

**Transaction 1 — €100 Pay-in-30 in Germany (Klarna Bank AB is lender of record):**
- (A) Consumer selects Klarna Pay-in-30 at checkout; approved in seconds.
- (B) Merchant ships goods; Klarna assumes credit + fraud risk.
- (C) Klarna pays merchant ~€94–97 (fee up to 5.99% + fixed) within settlement terms; consumer owes Klarna €100, due in ≤30 days, interest-free.
- (D) Credit risk sits with **Klarna Bank AB**; funded by German/Swedish deposits (~90% deposit-funded).
- (E) Data: transaction, device, behavioural, bureau (SCHUFA), and open-banking signals feed underwriting and the advertising graph.
- (F) Accounting (IFRS): receivable at amortised cost; merchant fee recognised as transaction revenue; ECL provision booked upfront.
- (G) Legal: EEA consumer-credit rules; CCD II applies from 20 Nov 2026.
- **Contribution:** merchant fee ~€3–6, minus ~40 days of funding cost (deposit rate on €100 for ~0.11 years ≈ a few cents to ~€0.10) minus expected loss (~0.5% of GMV ≈ €0.50) minus servicing → positive contribution of roughly €2–5 per €100.

**Transaction 2 — $200 Pay-in-4 in the US (WebBank originates, Klarna Inc. purchases):**
- (A) Consumer selects Pay-in-4; 25% ($50) due at checkout, three payments every 2 weeks.
- (B) Merchant ships; upfront settlement less fee (3.29–5.99% + $0.30).
- (C) **WebBank (Utah industrial bank) is lender of record and originates**; **Klarna Inc. purchases the receivable** and bears predominant loss economics, offloading via forward-flow (Nelnet up to $26bn of Pay-in-4; Elliott/Värde for Financing).
- (D) Credit risk: predominantly Klarna Inc. post-purchase, partially transferred to forward-flow buyers. Funding: wholesale/warehouse (Santander €1.4bn) + forward-flow, *not* US deposits (Klarna cannot yet take US deposits — hence the 6 July 2026 application for Klarna Bank USA).
- (E) Data flow as above (US bureaus: TransUnion/Experian for Financing; Pay-in-4 *not* reported).
- (F) IFRS: some receivables held for sale (originate-to-distribute) → gain on sale (e.g., $57m Q1 2026, ~half from forward flow); merchant fee as transaction revenue.
- (G) Legal: WebBank lender-of-record structure; US state lending law; CFPB TILA interpretive rule applied to Pay-in-4 (2024).
- **Key difference from Germany:** higher take rate, more expensive funding (no deposits), split legal responsibility, and capital-light distribution economics.

**Transaction 3 — a longer-term interest-bearing Fair Financing purchase:**
- (A) Consumer chooses 6–36 month financing; APR 0–~33.99% (US) disclosed upfront; hard credit check.
- (B) Merchant ships; merchant fee *lower* (up to ~3.29%) because the consumer now pays.
- (C) **The consumer is the principal payer** — interest is the main revenue, not the merchant fee.
- (D) Credit risk higher (delinquency 2.18%); funded by deposits (EEA) or forward-flow (US, Elliott).
- (E) Reported to credit bureaus (unlike Pay-in-4).
- (F) IFRS: interest income accrued over term; higher ECL provision; transaction margin >2x group average.
- (G) Legal: fully regulated consumer credit (CCA 1974 UK; TILA US).
- **Economics differ in kind:** this is a yield-on-assets product, closer to a credit card, and is the one product where the "who pays" answer is the consumer.

### II.11 Underwriting and the Decision

Klarna makes a **real-time, fully automated** credit decision per transaction using: its own Klarna transaction/repayment history; merchant data; credit-bureau reports where available; and **open-banking data** on the consumer's current financial position. It underwrites *each transaction* (not a static revolving limit), which lets it start new/thin-file consumers with small exposure and escalate limits with demonstrated repayment — the mechanism by which it underwrites populations with little formal credit history (the hardest problem in credit). Losses of 0.47% of GMV (2024) are the headline evidence it works at scale. Decline rates are not publicly disclosed (**UNKNOWN**). Bureau reporting: UK Pay-in-30/Pay-in-3 reported to Experian & TransUnion since 1 June 2022; US Pay-in-4 *not* reported; US Term Loans reported to TransUnion (and Experian) from 30 Sept 2024.

### II.12 Failure and Exception Paths

- **Returns/partial returns:** Klarna pauses payment on a reported problem; refunds if resolved in the consumer's favour. Merchant-led resolution — "Klarna is unable to override a merchant decision on your dispute."
- **Disputes/chargebacks:** merchant has 21 days to resolve a complaint (7 days for returns); if a merchant fails to refund within 96 hours of agreeing, Klarna performs an automatic chargeback. Double-disputing (Klarna + card issuer) cancels the Klarna dispute.
- **Merchant insolvency:** Klarna, having pre-paid the merchant, bears buyer-protection exposure.
- **Consumer default & collections:** reminders → late fee after 7 (UK) / 10 (US) days → after 4 months (UK) or a 21-day final grace (US), the debt is passed to an FCA-approved / third-party **debt collection agency** and the account is frozen. Only 0.61% of UK orders (2023) reached a collector.
- **Hardship/forbearance:** free due-date extension (10 additional days UK; once per order US; not available on Financing). Uptake not quantified (**UNKNOWN**).
- **Fraud:** Klarna assumes fraud-related dispute liability for merchants; underwriting screens for AML/CTF and abuse.
- **The consumer-harm critique, addressed fairly:** The evidence is genuinely mixed. Against Klarna: deHaan et al. and Di Maggio et al. find BNPL raises overdrafts and total spending; CFPB finds 61% of users subprime and heavy loan-stacking; the Woolard Review (Feb 2021) found "significant potential consumer harm" (more than one in ten users of a major bank already in arrears; a later FCA survey found 44% of frequent users over-indebted in 2022). For Klarna: its own default (0.4% UK) and delinquency (0.88%) rates are low; 95% UK / 96% US paid on time or early; late fees are capped and deliberately small; and some CFPB work found **no long-term negative impact of Pay-in-4 originations on financial distress** and some substitution away from costlier credit. The honest conclusion: BNPL is incremental and does raise spending and short-term distress for liquidity-constrained users, but Klarna's short-duration, capped-fee, gated-underwriting model is materially less punitive than revolving cards — and the unresolved distributional question (II.5) is what separates "moral panic" from "settled case."

### II.13 Product-Market Evolution (2005 → 2026)

Invoice at checkout (2005, Kreditor) → instalments & Klarna Checkout → Sofort/BillPay infrastructure (2014–17) → **Swedish banking licence (2017)** → US launch (2015) & Pay-in-4 → app & shopping (2018) → deposits/bank accounts (Germany 2021) → physical Card (UK 2022) → **PriceRunner & comparison shopping (2022)** → advertising/retail media → **Klarna Balance & deposits at scale (2024)** → Card relaunch, P2P, savings, stablecoin (2025–26).

**The pattern:** the acquisition strategy moved from *infrastructure/licences* (Sofort, BillPay, Close Brothers Retail Finance) to *consumer engagement/network* (Stocard, PriceRunner, Inspirock, HERO) — a deliberate pivot toward owning the consumer relationship. **What it reveals:** Klarna is becoming **a shopping network with a bank balance sheet attached** — not purely a merchant-services company (it now takes deposits and issues cards) nor purely a consumer bank (its economics are still merchant-funded and volume-driven). It is monetising the same consumer three ways: merchant conversion fees, banking spread/interchange, and advertising.

## Recommendations

**For an investor / analyst:**
1. **Model Klarna on take-rate-minus-loss-on-GMV, never on NIM.** Track: take rate (≈2.75%, rising), realised loss/GMV (≈0.45%), funding cost/GMV, and transaction margin/GMV (management target >1.04% of GMV for 2026). Benchmark that would change the thesis: realised losses breaching ~0.8% of GMV sustainably, or take rate falling below ~2.4% (merchant pushback).
2. **Watch the US deposit transition.** The Klarna Bank USA application (6 July 2026) is the single biggest margin lever — replacing wholesale/forward-flow funding with deposits would materially lift US contribution. Benchmark: US funding-cost/GMV converging toward the EEA level.
3. **Treat advertising as optionality, not core.** At ~7% of revenue it is not yet a second engine; re-rate only if it sustains >20% of revenue with retail-media margins.
4. **Demand the distributional disclosure.** The quality of the consumer-fee revenue (II.5) cannot be judged without cohort-level fee data. Until regulators (CCD II, FCA) compel it, discount the "fair to consumers" narrative accordingly.

**For a merchant:**
1. Adopt Klarna where AOV is $50–500 and purchase hesitation is high (fashion, electronics, homeware); measure *incremental* net revenue, not gross uplift, against the 3–6% fee.
2. Negotiate: merchants >$5m annual revenue can reach ~3.29%; do not accept the 5.99% list rate at scale.
3. Reassess annually — the pricing-power asymmetry grows as consumer expectation entrenches; the threshold to drop Klarna is when measured incremental margin < fee.

**For a regulator:**
1. Compel account-level fee-incidence and collections data by user decile — the only way to resolve the harm debate.
2. Scrutinise the advice/payment conflict in the comparison/advertising business.

## Caveats

- **Company figures are COMPANY CLAIM.** Conversion/AOV uplift statistics (40%/20%/46%) are marketing and not independently reproducible; independent estimates are lower (20–35% AOV).
- **Basis discipline:** Group reports in **USD under IFRS as issued by the IASB**, 31 Dec year-end, on Form 20-F as a foreign private issuer. Klarna Bank AB statutory accounts are in **SEK**. The 0.47%-of-GMV loss (IFRS group) and 0.57%-of-GMV credit losses (SEK statutory H1 2025) are on different bases and must not be conflated. Non-IFRS measures (transaction margin dollars, transaction margin, adjusted operating profit/margin) exclude items (notably credit losses in the "before provision" cut and SBC/restructuring) and must not be mixed with IFRS figures — adjusted operating profit was +$181m (2024) while the IFRS operating result was a −$121m loss.
- **The distributional question (II.5) is UNKNOWN** and is the analytical crux; the absence is itself the finding.
- **Decline rate, hardship uptake, and merchant-level GMV concentration** are not disclosed (**UNKNOWN**).
- **Forward-looking items** (Klarna Bank USA licence, KlarnaUSD stablecoin, guidance of >$155bn GMV for 2026, PriceRunner's $1.97bn award subject to appeal) are not settled facts.

## Volume II Reconstruction (summary)

1. **Product architecture by entity:** Pay-in-Full/30/3/4 and Fair Financing, Card, Balance, savings, app, PriceRunner, Plus, P2P, advertising, Payments/Checkout — provided by Klarna Bank AB (EEA/UK lender), Klarna Financial Services UK, Klarna Inc. (US, WebBank lender-of-record), PriceRunner, under non-operating holdco Klarna Group plc.
2. **Five-payer map:** merchants (primary), consumers (late fees/interest/subscription/FX), advertisers, card networks (interchange), depositors (funding spread).
3. **Merchant-uplift mechanism:** conversion + AOV + acquisition + frequency + thin-file access; incremental (not merely substitutional) per academic evidence; priced at 3–6% vs 0.3% interchange because it is a marketing service, not a rail.
4. **Take rate:** ~2.75% FY2025, rising on US/Fair Financing mix; below Affirm (~7–9%) by design.
5. **Consumer cost:** 98% interest-free; capped late fees; Fair Financing up to ~34% APR; distributional concentration UNKNOWN.
6. **Book velocity:** ~40-day duration, ~9x annual turnover; loss ~0.45–0.65% of GMV; analyse on GMV, not assets.
7. **Advertising:** genuine second inversion, ~7% of revenue, real conflict, modest scale.
8. **Metrics series:** 118m consumers, 966k merchants, $127.9bn GMV, 3x→11x transaction cohort curve, $30→$107 revenue/user.
9. **Escalation ladder = monetisation path = risk path** (Robinhood analogue).
10. **Three value-flows:** Germany (Klarna as lender, deposit-funded), US (WebBank + Klarna Inc. + forward-flow), Fair Financing (consumer as payer).
11. **Underwriting:** real-time, per-transaction, open-banking + bureau + behavioural; escalating limits; 0.47% loss/GMV.
12. **Failure map:** merchant-led disputes, capped late fees, 4-month collections path, minimal forbearance disclosure.
13. **Evolution:** invoice → bank → card → shopping network → advertising → deposits at scale = a shopping network with a balance sheet.
14. **Key unknowns:** fee distribution by user; decline rate; hardship uptake; merchant concentration.

**The central answers:**
- **True core product:** short-dated, merchant-funded, interest-free point-of-sale credit that increases merchant conversion.
- **Real customer:** the merchant (for the core product); the consumer becomes the customer only on Fair Financing and banking products.
- **What funds the company:** merchant fees (with interest income the fastest-growing second line and deposits the funding moat).
- **What the consumer pays and can they see it:** mostly nothing explicitly; the real cost is the merchant fee, very likely passed into the price of goods — invisible to the consumer, who pays it whether or not they use Klarna.
- **Highest-quality revenue:** merchant fees (diversified, recurring, volume-linked) and, increasingly, advertising (high margin). **Most fragile:** late-fee/consumer-service revenue (regulatory target under CCD II/FCA) and interest income sensitive to the credit cycle.
- **The central question:** merchant-funded credit is a *better deal than the interest-bearing credit it displaces for the disciplined majority who pay on time* — they get free short-term credit while the merchant bears the cost. But it is **the same cost relocated into the price of goods**: because the merchant fee is embedded in prices, all consumers (including cash/debit payers) subsidise BNPL users, and the liquidity-flypaper effect means the model *sells more*, not just *finances more*. **If merchants ever decide the uplift is not worth the fee — most plausibly if regulation forces affordability checks that cut conversion, or if PSP-commoditised competition collapses pricing — Klarna's core take rate compresses toward interchange levels, and the company's survival then depends on the still-subscale banking and advertising businesses.** That is the fragility beneath a genuinely profitable-in-adjusted-terms, genuinely innovative model.

---

# VOLUME III — Operations, the Decision Engine, Technology, Data, AI & Organisational Design

## TL;DR
- **Klarna's true operating core is a fully automated, per-transaction credit decision made in a fraction of a second, roughly 3.4 million times a day across 26 markets.** The machine is real and technically sophisticated (Kafka event streams → DynamoDB feature store → an ML "Credit Model" plus a rules-based "Underwriting Policy" on AWS), and it is the hardest thing Klarna does and its most durable moat — trained on a proprietary repayment graph (118m consumers, 966k merchants, 2.5bn+ SKU data points) that money alone cannot replicate.
- **The celebrated "AI substitution" story is substantially overstated.** The headline "work of 700 agents" was an avoided-hiring/workload-equivalence claim against an *outsourced* contact-centre base of ~3,000 agents, not 700 redundancies; the halving of headcount (~5,527 → ~2,831) came overwhelmingly from a December 2023 hiring freeze plus natural attrition, not AI-driven layoffs. On 8 May 2025 the CEO publicly conceded cost had been "a too predominant evaluation factor" and quality suffered, and Klarna began rehiring humans. Treat all self-reported operational metrics with corresponding scepticism.
- **The binding constraint on growth is credit quality / loss performance under scaled lending, and the most dangerous single dependency is PSP-mediated distribution (Stripe / Adyen).** The December 2024 SEK 500m AML fine is the best available forensic description of how onboarding actually worked — revealing that ~70m of ~79m consumers were classed "non-KYC," and that the invoice product's due-diligence triggers systematically missed customers who transacted up to 59 times a year.

## Key Findings

**[CONFIRMED FACT]** Klarna Group plc (NYSE: KLAR) reported FY2025 GMV of $127.9bn (+22% YoY), revenue of $3.5bn (+25%), adjusted operating profit of $65m (1.9% adjusted operating margin), 118m active consumers (+28%), and 966,000 merchants (+42%), with basic/diluted EPS of $(0.79). The group reports in USD under IFRS on a 31 December year-end. Non-IFRS measures (transaction margin dollars, adjusted operating profit/margin) are labelled as such throughout.

**[CONFIRMED FACT / COMPANY CLAIM]** The decision engine is per-transaction and real-time. A Klarna senior engineer (Tony Liu) described the architecture publicly at AWS re:Invent 2024 (session FSI319): every purchase gets a fresh underwriting decision built from (a) internal customer features, (b) external credit-reference-agency data, and (c) transaction/basket data, fed into an "Underwriting Policy" (deterministic rules with thresholds, including compliance "hard rejects") and a "Credit Model" (a machine-learning model outputting a default-probability score). This is COMPANY CLAIM as to performance, but CONFIRMED as to architecture (named engineer, named conference, technical detail).

**[COMPANY CLAIM]** Klarna states its US underwriting Gini coefficient rose from 0.36 (2019) to 0.72 (H1 2024), versus a cited VantageScore 4.0 benchmark of ~0.35, and that US credit losses fell from 9.6% (2019) to ~1.1–1.2% (2024). Overall consumer credit losses were 0.47% of GMV in 2024. These are company-reported and not independently audited.

**[CONFIRMED FACT]** On 11 December 2024, Finansinspektionen (FI) issued Klarna Bank AB a remark plus a SEK 500m administrative fine for AML deficiencies over 1 April 2021–31 March 2022 (FI dnr 22-11505). No actual money laundering was found; the case concerns deficient controls.

**[CONFIRMED FACT]** Klarna's workforce fell from ~5,527 (2022) to ~2,907 (2025) per CEO statements; Klarna Group had 2,831 employees at 31 December 2025 (S&P Global Market Intelligence via stockanalysis.com). The reduction came overwhelmingly from a December 2023 hiring freeze plus natural attrition, with departing staff not replaced.

## Details

### III.1 The Operating Model — functions by legal entity

Klarna Group plc is a non-operating UK holding company (NYSE: KLAR). The operating machinery sits in:

- **Klarna Bank AB (publ)** and its EEA branches — the licensed Swedish bank (licence granted 19 June 2017). Performs underwriting, lending (lender of record in the EEA), deposit-taking, collections, financial-crime controls, credit-risk modelling, treasury and capital management. Bears the credit risk in the EEA.
- **Klarna Financial Services UK Limited** (FRN 987889 for regulated consumer credit; 987816 for payment services) — the FCA-authorised UK entity that from ~2025 provides all consumer-facing services in the UK after the Temporary Permissions Regime expired on 31 December. Also authorised as an Electronic Money Institution.
- **Klarna Inc.** — the US operating entity; **WebBank** (a Utah industrial bank) is lender of record for US Pay-in-4, Financing and card products; Klarna Inc. purchases the receivables and bears predominant loss economics. A Klarna Bank USA industrial-bank charter application was filed 6 July 2026.
- **PriceRunner** — comparison-shopping/catalogue asset feeding the product and advertising graph.

Major operating functions and where they sit:
1. **Engineering & platform** (Klarna Bank AB, Stockholm-centric) — builds and runs the transaction pipeline, decision engine, app and merchant APIs on AWS.
2. **Credit risk & decisioning** (Klarna Bank AB) — owns the Underwriting Policy, the Credit Model, limit-setting and the escalation ladder.
3. **Data & analytics** (Klarna Bank AB) — the feature store, the consumer/merchant transaction graph, and model training.
4. **Merchant integration & onboarding** — direct plus PSP-mediated (Stripe, Adyen, Worldpay, Shopify, Salesforce Commerce and others).
5. **Payment operations & settlement** — merchant settlement and consumer collection by card-on-file, direct debit, open-banking initiation and bank transfer.
6. **Collections & recovery** — internal reminder/late-fee sequence, then outsourced to third-party debt-collection agencies.
7. **Customer service** — a hybrid of an OpenAI-based AI assistant plus outsourced human agents (historically Foundever and Accenture).
8. **Financial crime, AML & fraud** (Klarna Bank AB) — CDD, transaction monitoring, sanctions screening, suspicious-activity reporting, and fraud detection.
9. **Compliance & regulatory reporting** — multi-market (Swedish FI, UK FCA, EU, US).
10. **Treasury** — a ~90% deposit-funded model; global deposits almost doubled from $9.5bn to $14bn between the August 2024 launch of Klarna Balance and September 2025.
11. **Corporate functions** — legal, HR, finance (some formerly on Salesforce/Workday; see III.5).

Failure modes cluster in three functions: credit risk (loss-rate drift), financial crime (the demonstrated AML failure), and customer service (the demonstrated AI-quality failure).

### III.2 The Decision Engine (THE CORE)

**What happens between "select Klarna" and approve/decline.** Per the re:Invent 2024 account and the F-1: on checkout the consumer is identified/matched (national identifier where available — e.g. Sweden and Germany; email/phone/device where not). The Underwriting Policy requests a feature set for that consumer. A feature-calculation service reads the current per-order state from DynamoDB (partitioned by Order ID, with a customer_id global secondary index), applies feature definitions from a shared "Business Logic Library," and returns features. The Credit Model scores default probability; the Policy applies thresholds and hard-reject rules; a limit is assigned; fraud screening runs; and — where regulation requires (e.g. UK regulated products) — an affordability assessment can be run, optionally using open-banking data the consumer chooses to share. The response is an approve/decline plus the available payment options.

**Data freshness is the design goal.** Klarna's engineers explicitly rebuilt this system so that internal data updates in real time via Kafka events (a new order tightens the next decision within seconds; a repayment loosens it), while bureau data — "not updated frequently" — forms the slower-moving base layer. This is the operational meaning of "high-frequency underwriting."

**Latency budget.** [THIRD-PARTY / COMPANY CLAIM] American Banker, quoting Forrester principal analyst Alyson Clarke, reported that "Klarna's underwriting software takes in data from more than 100 sources and uses artificial intelligence to make a credit decision in less than a tenth of a second." The same piece quotes Klarna North America CEO Jim Lofgren saying the system uses "more than 180 creditworthiness variables" and "we can do a credit decision in less than 0.4 seconds." The F-1 and the re:Invent talk say "in seconds." ANALYTICAL INFERENCE: the effective budget for the credit-decision microservices is sub-second, constrained by the slowest synchronous call (typically a bureau pull). This forecloses human review, deep document verification, or slow external affordability checks at the moment of checkout — precisely the operational tension the AML fine later exposed (CDD compressed out of the checkout flow). Note a modest reporting discrepancy in scale: Klarna's investor materials state "3.4 million transactions per day" from 118m users (2026), while the F-1 (period ended 30 June 2025) states "approximately 3.0 million transactions made on average per day" from 111m active consumers — the figure grows with volume.

**Three regimes:**
- **Data-rich (Sweden, Germany):** a national identifier plus strong bureau coverage (e.g. UC in Sweden, SCHUFA in Germany) give a reliable external base layer; internal repayment history refines it in real time. Highest-confidence decisions; the invoice product has historically dominated.
- **Data-poor (US Pay-in-4, new markets):** thin/no bureau file; the decision leans on transaction-level signals, device/session data, basket data and Klarna's own accumulating history. Klarna's stated Gini improvement (0.36 → 0.72 in the US) is the claimed payoff of substituting proprietary data for bureau data. Loss rates were far higher early (9.6% in 2019) and were tightened via stricter policy, larger down-payments and risk-based pricing in H2 2022.
- **Genuinely new consumer anywhere:** minimal internal history, so the decision relies on external data (where available), device/behavioural signals and basket, plus a deliberately **small initial spending capacity that escalates with demonstrated repayment**. This "start small, grow with behaviour" ladder is the core risk-control for thin/no-file populations and, per Volume II, is simultaneously the monetisation path.

### III.3 Underwriting Data and Model Governance

**Data sources named in the public record:**
1. First-party Klarna transaction and repayment history (internal customer features: current Klarna debt, lifetime payments, first-order date, any prior lateness).
2. Merchant and basket/SKU data ("more than 2.5 billion SKU-level data points collected in 2024," per the F-1).
3. Device, session and behavioural signals (used especially in thin-file and fraud contexts).
4. Credit-bureau data by market (the slower-refresh base layer).
5. Open-banking account data (consumer-shared, used for real-time affordability especially on UK regulated products).
6. [UNKNOWN] Any consortium/alternative-data sources beyond the above are not clearly disclosed. Klarna's North America CEO's "more than 180 creditworthiness variables" is the most specific public figure on model breadth.

**Model build, validation and governance.** The Credit Model is trained in SageMaker on logged production decisions plus "retrospective calculation" — replaying historical event streams to compute what any feature (even an experimental one) would have been at a past decision point, enabling faster iteration without waiting for data to mature. Governance obligations arise from Klarna's status as a CRR/CRD bank and from the EU AI Act:
- **Capital approach:** [CONFIRMED FACT, Pillar 3 disclosures] Klarna uses the **standardised approach** for credit risk (not internal ratings-based / IRB), with external ratings from Moody's, Fitch and S&P for institutional exposures; the Alternative Standardised Approach for operational risk; and the standardised method for market risk. Credit risk constitutes ~90–95% of Klarna's risk exposure amount. Note the distinction: the standardised approach governs *regulatory capital*, while the ML Credit Model governs the *underwriting decision*. They are separate systems — the sophisticated ML does not (yet) earn Klarna IRB capital treatment, so the balance sheet is capitalised as if underwriting were unremarkable.
- **EU AI Act:** creditworthiness assessment of natural persons is a named **high-risk** use case (Annex III, point 5(b), Regulation (EU) 2024/1689), triggering Articles 8–17 duties (risk management, data governance, technical documentation, human oversight) and, for deployers, an Article 27 fundamental-rights impact assessment; Annex IV technical-documentation obligations become binding from 2 August 2026. Fraud detection is expressly carved out. This is a material forward compliance load on the decision engine.
- **Model risk under AML law:** [CONFIRMED FACT] FI found Klarna had **no model-risk-management routine** for its automated CDD-classification model during the review period — a governance gap that also signals the maturity level of model governance more broadly at the time.

**What is disclosed vs not:** Klarna discloses Gini scores, loss rates and delinquency by product, but not model architecture specifics, full feature lists, drift-monitoring cadence, or segmented performance by cohort. All model-performance claims are COMPANY CLAIM.

### III.4 The Data Architecture and the Purpose-Separation Question

**What Klarna knows:** a consumer transaction graph across 118m consumers and 966k merchants; product/basket data at SKU level; the PriceRunner catalogue; app behavioural data; and an advertising graph monetising consumer intent (the "second Experian-like inversion" identified in Volume II).

**Platform (from engineering publications):** Kafka topics as the event backbone with enforced producer/consumer schema contracts; a DynamoDB-based real-time state/feature store (order-level items); AWS Glue/Spark plus Step Functions for offline/batch processing; S3 for the full event-history lake; SageMaker for training; Redshift for analytics. A "Business Logic Library" unifies feature definitions across the real-time and batch layers. Kiki, the internal assistant, is built on a Neo4j knowledge graph plus OpenAI LLMs.

**The governance constraint (the estate-firewall analogue).** GDPR requires purpose limitation: data gathered for credit assessment cannot be freely repurposed for advertising/personalisation without a lawful basis and transparent disclosure. The Swedish authority (IMY) findings are the key evidence:
- [CONFIRMED FACT] March 2022: IMY fined Klarna SEK 7.5m for breaching transparency/information duties (Articles 5(1)(a), 5.2, 12, 13, 14 GDPR) — the privacy notice failed to clearly state processing purposes, legal bases, recipients, retention, third-country transfers, and the logic of profiling/automated decision-making, including which data types were decisive in a negative decision and the consequences for data subjects.
- [CONFIRMED FACT] On appeal, the Stockholm administrative court (2024) held Klarna had not violated the rules to the full extent IMY claimed and reduced the fine (from ~€730k to ~€600k), upholding transparency findings on the "My Economy" service, retention, third-country transfers and profiling logic, but rejecting the lawfulness/fairness finding.
- [CONFIRMED FACT] March 2025: a further IMY reprimand (IMY-2022-10270) for the handling of an access request.

ANALYTICAL INFERENCE: the IMY record shows Klarna's *disclosure* of purpose separation was deficient, but does not establish that the underlying data uses were unlawful. Whether credit-assessment data and advertising data are genuinely firewalled *inside* Klarna is UNKNOWN from the public record — a material governance gap given the scale of the advertising business.

### III.5 Technology Architecture

Reconstructed from the re:Invent 2024 talk, the Neo4j and OpenAI case studies, and technology reporting:
- **Original → event-driven:** Klarna migrated from batch feature computation (EMR processing daily database dumps) to a real-time, event-sourced architecture on Kafka + DynamoDB, explicitly to fix (i) the absence of producer/consumer data contracts, (ii) costly full-history reprocessing, (iii) divergence between real-time and batch code, and (iv) slow feature experimentation. An incident in which an upstream team changed an internal DB field — unaware the feature system depended on it — and shifted the feature distribution feeding the Underwriting Policy is the corroborated reason for the schema-contract discipline.
- **Cloud posture:** AWS-native (DynamoDB, S3, Glue, EMR, Step Functions, ECS, SageMaker, Redshift). Multi-region arrangements are UNKNOWN in detail.
- **Merchant APIs/SDKs and app:** documented at docs.klarna.com; integrations with PSPs and platforms.
- **Core banking / ledger:** [UNKNOWN] not described publicly in detail.

**The "replaced enterprise SaaS with AI" claim — tested.** [COMPANY CLAIM] On an August 2024 investor call (reported by Seeking Alpha, Inc. and CX Today), CEO Siemiatkowski said Klarna had "just shut down Salesforce" and would shut down Workday "within a few weeks," as part of "internal initiatives that are a combination of AI, standardization and simplification." [THIRD-PARTY, corroborated] Klarna confirmed to Inc. that it removed Workday. **However,** CX Today reported (with a Klarna spokesperson quote) that Klarna did **not** replace these purely with bespoke AI — it combined AI, standardisation and *alternative SaaS*, consolidating providers into "a much more lightweight tech stack." Salesforce CEO Marc Benioff publicly questioned how Klarna could manage employee/financial/customer information after removing these systems. ASSESSMENT: the "AI replaced Salesforce/Workday" framing is partly marketing; the corroborated core is provider consolidation + internal tooling + AI assistance, not a wholesale AI rebuild of ERP/CRM. Kiki (Neo4j + OpenAI) is a corroborated internal knowledge assistant — it answered ~2,000 queries/day and 250,000+ inquiries since its June 2023 launch, with ~85% of staff using it — but it is an internal Q&A assistant, not an ERP replacement.

### III.6 Merchant Integration and Distribution Operations

Klarna acquires and serves merchants two ways: **direct integration** and **PSP/platform-mediated distribution** (Stripe, Adyen, Worldpay, Shopify, Salesforce Commerce, Mollie, Adobe Commerce, WooCommerce).

**The strategic pivot.** In 2024 Klarna **divested Klarna Checkout (KCO)** (reported at ~£407m, to an investor group led by Kamjar Hajabdolahi and BLQ Invest) explicitly to remove the conflict of competing with the PSPs that distribute it. Bloomberg reported Klarna had not actively developed or sold KCO since 2021. Klarna then deepened partnerships: Stripe (businesses in 25 countries can enable Klarna "instantly"; Klarna attributed a doubling of new merchants offering Klarna in Q4 2024 to this) and Adyen (the first global PSP to launch Klarna across all physical terminals worldwide, September 2024). Klarna added more than 100,000 retailers in 2024.

**Operational significance.** [CONFIRMED FACT, per activist analysis of Klarna's own disclosure] PSPs including Adyen and Stripe act as "merchant of record" (MoR) partners, and Klarna "currently derive[s] a substantial portion of [its] merchant revenue" from merchants using those MoRs. This is a structural economic dependency: it accelerates merchant scale but cedes control over pricing dynamics, product placement, integration friction and — critically — direct merchant data and relationship. It is also the same "mor-model" that FI faulted on AML grounds (see III.8), meaning the distribution strategy and the compliance failure share a single architectural feature.

### III.7 Payment Operations, Settlement and Collections

**Settlement:** Klarna pays the merchant (directly, or via the PSP where Klarna is enabled through a distribution partner) and collects from the consumer, taking on the credit risk. Settlement currency and FX are handled by Klarna; where enabled via a PSP, dispute documentation may flow through the PSP.

**Consumer collection & retry:** payments are taken by card-on-file/direct debit on schedule; on a failed attempt Klarna retries; a still-unpaid instalment is added to the next scheduled payment; open-banking initiation and bank transfer are also used. Autopay reduces misses.

**Collections/late-fee sequence (traced):**
- **UK (from 16 March 2023):** a 7-day grace period; a minimum of four "friendly reminders"; then a £5 late fee, capped at 25% of order value and no more than two fees per order. Fees fund the Klarna Customer Recovery Programme, under which Klarna offers to **waive 50% of the balance** of long-overdue customers instead of using a debt-collection agency, blocking further purchases until 50% is paid, after which the debt is considered closed.
- **US:** a one-time flat $7 late fee after ~10 days overdue on Pay in 4.
- **Referral to third-party agencies:** if unpaid after the final reminder due date, the debt is transferred to a debt-collection agency; the consumer may pay Klarna or the agency directly. [UNKNOWN] Specific agency counterparties are not named on Klarna's consumer-facing pages.

**Proportions reaching each stage (UK 2023 self-report, carried from Volumes I/II):** 60% paid early, 35% on time, 5% late; 0.61% referred to a debt collector; 0.4% default. FY-level realised losses were 0.44–0.45% of GMV. Reputational and regulatory exposure concentrate in the collections tail and are heightened by incoming UK FCA regulation of BNPL (from July 2026: affordability checks, clearer terms, enhanced protections).

### III.8 Financial Crime, AML and Fraud — with the FI post-mortem

**Fraud liability (who bears the loss):** [CONFIRMED FACT, Klarna evidence to UK Parliament] For **first-party fraud**, Klarna "bear[s] the brunt of any loss" because it holds the credit risk. For **third-party (impersonation) fraud**, victims in almost all cases pay nothing — the order is cancelled — and Klarna's "Fraud Protection Promise" guarantees the consumer "shall not [be] expect[ed] … to pay for [a] fraudulent purchase." For **merchant disputes/chargebacks**, Klarna runs its own dispute process (not the Visa/Mastercard rails), with strict, largely non-appealable timelines; for many item-not-received and merchant-fault disputes the **merchant carries the loss**, whereas for fraud where Klarna approved the credit decision Klarna typically absorbs liability. Product risk is uneven: short-term Pay-in-4 shows higher chargeback-fraud vulnerability than longer-term Financing, where Klarna assumes more credit risk.

**The FI December 2024 decision as an operational post-mortem (FI dnr 22-11505; investigation 1 April 2021–31 March 2022).** No actual money laundering was established; the case is about deficient controls. FI's five central findings:

1. **The general risk assessment did not assess *how* products could be abused.** Klarna scored inherent and residual risk but never analysed how, for example, the absence of physical customer contact makes its products vulnerable to ML/TF; typologies were copied from national risk reports without linking them to Klarna's business. FI: there were "entirely lacking assessments of in what way the products' and services' characteristics make them vulnerable."
2. **The "mor-model" distribution channel was not risk-assessed.** Klarna contracts only with "merchant-of-record" PSPs (mor-handlare), who hold portfolios of "sub-merchants"; Klarna does CDD only on the mor-handlare, leaving sub-merchant CDD to them. Mor-handlare generated **12.2% of Klarna's merchant income in 2021** (merchant income being 76% of total income). Klarna's own assessment had called this "a special risk … because it means Klarna ends up further away from the sub-merchants," noting funds could flow to/from "sub-merchants that have not been identified and verified" — yet Klarna did not treat it as a distribution channel or analyse the resulting risk. FI called this "particularly remarkable given the extensive sales."
3. **Suspicious-activity reports were not analysed.** Klarna had filed 61 police suspicion reports in the first four months of 2021 but performed no analysis of them in its risk assessment (Klarna admitted this).
4. **CDD for the invoice product missed customers.** Klarna split consumers into **~9m "KYC-consumers"** (CDD collected) and **~70m "non-KYC-consumers"** (none). Escalation to KYC required meeting one of three thresholds, and the invoice product was **not** among the products that auto-trigger KYC. FI's benchmark is that a business relationship (requiring CDD) arises by the 12th transaction in 12 months; Klarna's transaction criterion required **60 transactions**. FI's damning example: "all 100 non-KYC-consumers who made the most transactions during the investigation period made 59 transactions, and the bank took no CDD measures regarding these customers." This is the clearest evidence of how CDD was effectively compressed out of the checkout flow. FI also rejected Klarna's argument that invoice consumers are merely "the customer's customer" (a factoring framing): to use any Klarna method a consumer must register an account and accept a credit agreement, so they are Klarna's customers in the AML sense.
5. **No model-risk-management routine for the automated CDD-classification model** — Klarna conceded it had none; FI held that internal testing could not compensate.

**Sanction reasoning:** FI's escalation ladder runs rectification order → remark → warning → licence withdrawal. FI judged the breaches "not so serious" as to warrant a warning or licence withdrawal and chose a **remark plus fine**. The statutory maximum was the highest of 10% of group turnover (~SEK 2.46bn on 2023 group turnover of SEK 24.64bn), twice the profit from the breach, or €5m. FI set the fine at **SEK 500m (~20% of the ceiling)**, calling it "well-balanced and proportionate," and rejected mitigation both for cooperation ("not more active than can be expected of a company under supervision") and for the 2.5-year handling time ("complex and relatively extensive"). FI noted the deficiencies "potentially could have had" systemic effects but, "as far as Finansinspektionen is aware, have not led to any damage."

**What Klarna changed:** Klarna said it would add abuse-vector analysis to the next general risk assessment and **adjust CDD triggers so that CDD applies once the same person makes 12 transactions in 12 months, with application beginning in Sweden on 1 November 2024** — i.e. aligning to FI's benchmark. Klarna publicly framed the case as one of "rule interpretation and application, and not … actual cases of money laundering." Post-remediation adequacy is not yet independently confirmed.

### III.9 Customer Service Operations (the pre-AI baseline)

[THIRD-PARTY / COMPANY CLAIM] Historically Klarna ran phone/email/chat support via **~3,000 outsourced agents** — the CEO's own figure: "on average, we need 3,000 agents." In late 2023 Klarna had outsourced roughly 750 customer-service roles to **Foundever and Accenture** (per a Sifted investigation cited by Bigeye), and a January 2024 outsourcing transition had already degraded quality *before* the AI launch — a critical confound for any causal reading of III.10. Klarna does **not** directly employ its front-line agents; they are third-party. Channels span 23+ markets and 35+ languages. This is the baseline against which the AI episode must be read.

### III.10 The AI Substitution Episode (assessed)

**Timeline and claims:**
- 2023: Klarna became the first fintech to launch a ChatGPT plugin; the CEO told OpenAI's Sam Altman he wanted Klarna to be ChatGPT's "favourite guinea pig." June 2023: the internal assistant **Kiki** launched (Neo4j + OpenAI). **December 2023: Klarna froze all non-engineer hiring.**
- **27 February 2024:** Klarna and OpenAI announced the customer-service assistant had, in its first month, handled **2.3m conversations** = **two-thirds of chats** = "the equivalent work of **700 full-time agents**"; resolution time cut from **11 minutes to under 2**; a **25% drop in repeat inquiries**; CSAT "on par" with humans; live in 23 markets and 35+ languages; and a **projected $40m profit improvement in 2024**.
- August 2024: Klarna said AI had helped it cut ~1,500 roles and was shutting down Salesforce/Workday (see III.5).
- **8 May 2025 (Bloomberg):** Siemiatkowski conceded: "As cost unfortunately seems to have been a too predominant evaluation factor when organizing this, what you end up having is lower quality," adding that "really investing in the quality of the human support is the way of the future for us." Klarna began **rehiring humans** under an "Uber-type" remote, on-demand model targeting "students, rural populations, and dedicated Klarna users."
- Q3/Nov 2025: Klarna still published rising AI-productivity figures — the assistant "can now do the work of more than 853 full-time agents … up from 700," having "saved the company $60 million" (CX Dive, from the Q3 2025 earnings call) — while headcount reached ~2,907, revenue per employee reached ~$1m (from ~$0.4m two years earlier), and pay for remaining staff rose ~60% (from ~$126k to ~$203k).

**Assessment — what the episode actually demonstrates:**
1. **The "700 agents" figure was never 700 redundancies.** The CEO himself told CBS News the agents are outsourced ("they are not employees"): "the consequence of us launching the technology is we need the equivalent of 700 fewer full-time agents than what we usually use … On average, we need 3,000 agents, now we need a little more than 2,000." That is **avoided contract labour during a growth phase** — a workload-equivalence, not a layoff count.
2. **Headcount halving ≠ AI substitution.** The ~5,527 → ~2,831 fall is overwhelmingly the December 2023 hiring freeze plus attrition (departers not replaced); Klarna itself told Fortune it was "maintaining its policy of not replacing employees who leave." The analytical trap in the framing note is real: a freeze plus natural attrition produces the same headcount curve as AI substitution. Independent survey evidence supports scepticism: Gartner, surveying 321 customer-service leaders in October 2025, found "only 20% of leaders have reduced agent staffing due to AI," with 55% reporting stable staffing while handling higher volumes, and forecast that "by 2027, half of organizations anticipating major AI-driven workforce cuts will abandon those plans." The genuinely AI-attributable headcount reduction at Klarna is therefore **small and not cleanly separable** from the freeze, the pre-existing outsourcing degradation, and normal attrition.
3. **Deflection is not resolution.** The success metrics (handle time, aggregate CSAT) measured speed and average satisfaction, not whether complex problems were actually resolved; quality degraded on complex/emotional tickets in ways the aggregates concealed — the CEO's "lower quality" admission is the confession. Routine queries are high-volume but low-value-at-risk; the tail is where harm in a regulated consumer business concentrates.
4. **Reliability of Klarna's operational claims.** The documented reversal means an analyst should treat Klarna's self-reported operational metrics as **marketing-inflected COMPANY CLAIM** by default and weight them down absent independent corroboration. Klarna published a specific, quantified success narrative that its own CEO materially qualified fourteen months later — the single most instructive fact in this volume about how to read the company.

### III.11 Workforce and Organisational Design

Headcount: ~7,000 (May 2022, pre-layoffs, of which ~700 were then laid off) → ~5,527 (2022 FTE) → ~3,800 (mid-2024) → 2,831 (31 December 2025). The December 2023 hiring freeze applied to non-engineers. Geography is centred on Stockholm, with offices in London, New York and Berlin. Compensation: average pay rose ~60% (from ~$126k in 2022 to ~$203k in 2025), funded by hiring-freeze savings; an equity programme exists, and stock-based compensation is a recurring, dilutive P&L item cited in the 2025 losses. **Revenue per employee** [COMPANY CLAIM — the metric Klarna promotes most aggressively] rose from ~$0.4m (H1 2023) to ~$1.0m (Q2 2025). Basis caveat: this uses Klarna's own employee definition, which **excludes the several thousand outsourced customer-service agents**, so it flatters the ratio relative to a fully-loaded headcount — the metric is sensitive precisely to the definitional choice the company controls.

### III.12 Operating Leverage — the quantified mechanism

Revenue grew 108% since 2022 (per the CEO to analysts) while Klarna kept operating costs roughly flat. FY2024: revenue $2.81bn (+24%), net income +$21m (a 0.7% margin) but a $121m operating loss. FY2025: revenue $3.5bn (+25%), adjusted operating profit $65m (1.9% margin) — but a full-year net loss (EPS $(0.79)); H1 2025 net loss $152m vs $31m in H1 2024; Q3 2025 net loss $95m.

ANALYTICAL INFERENCE: the improvement is a **combination** of (a) genuine automation-driven cost discipline (customer service and marketing-agency spend), and (b) a **one-time cost reset** from the 2022 layoffs plus the December-2023 freeze plus attrition — the latter is not repeatable. The reason 2025 swung back to net losses despite revenue growth is **rising credit-loss provisions** as lending scaled (funding costs also rose 67% YoY in 2024) — i.e. the diseconomy is not in opex automation but in **credit costs**, exactly where the decision engine's quality is tested. Costs that scale with volume: credit losses/provisions, funding costs, and payment-processing/PSP economics. Step-fixed costs: compliance, collections and multi-market regulatory overhead. Fixed costs: core engineering and platform. The genuine operating leverage is real but narrower than the headline "flat costs, doubled revenue" story implies, because the incremental dollar of GMV now carries an incremental provision that is rising.

### III.13 Bottlenecks and the Theory of Constraints

If every other component improved by half, the **binding constraint would remain credit quality / loss performance under scaled growth** — the 2025 return to net losses was driven by loss provisions, not opex. The decision engine is the throughput governor: it must hold losses near ~0.45% of GMV while extending credit to thin/no-file consumers in new markets. **The likely next constraint is regulatory/compliance capacity** — the AML fine, incoming UK FCA BNPL regulation (July 2026), EU AI Act high-risk obligations (Annex IV binding August 2026) and the US industrial-bank application all load the same compliance function. Funding is comfortable (deposit-funded, plus a Nelnet forward-flow of up to $26bn of Pay-in-4 and a Santander €1.4bn warehouse). Merchant acquisition has been *de-constrained* by the PSP pivot — but that trades one constraint for a dependency (III.14).

### III.14 Operational Resilience (stress tests)

- **Credit deterioration:** already partly realised — 2025 provisions pushed the group back to net losses. Response: tighter policy thresholds and risk-based pricing (as in H2 2022). Residual risk: model drift in new/thin-file markets. Recovery is fast because the book is ~40 days' duration and turns ~9× a year, so re-underwriting flows through quickly.
- **Cloud/platform outage at peak trading:** AWS-concentrated; an outage during peak retail would halt decisioning and checkout conversion. Multi-region posture UNKNOWN — a genuine residual risk.
- **Loss of a major PSP channel (Stripe/Adyen):** the most dangerous single dependency, given the "substantial portion of merchant revenue" via MoRs; loss would impair merchant reach and data. Recovery would be slow (re-signing merchants directly).
- **Financial-crime / data-protection escalation:** demonstrated (SEK 500m; the IMY fines). A repeat, or a warning-level sanction, could threaten the licence or the US application. Response is remediation (the 12-transaction CDD trigger from November 2024).
- **Funding/deposit shock:** mitigated by deposit diversification plus forward-flow and warehouse facilities.
- **AI failure in a consumer-facing or decisioning role:** the customer-service episode already demonstrated quality failure and reputational cost. A failure in the *decision engine* (as opposed to customer service) would be far graver — mispricing risk 3.4m times a day — but the engine is rules-plus-ML with hard-reject guardrails, not generative AI, which limits this specific risk.

### III.15 Technology and Operations as Moat

- **Decision engine + accumulated repayment data:** proprietary, learned over time, scale-improving (more transactions → better features → lower losses), and it creates switching costs indirectly (better limits for repeat users). **Money alone cannot replicate the repayment graph** — this is the strongest moat. Verdict: durable.
- **Merchant integration estate:** partly proprietary but increasingly **rented from PSPs** post-KCO divestiture; replicable by well-funded competitors and dependent on Stripe/Adyen goodwill. Verdict: weaker and more contestable.
- **Consumer transaction graph:** proprietary and scale-improving; overlaps the decision-engine moat.
- **AI-native cost structure:** real but overstated and partly a one-time reset; replicable. Verdict: modest.
- **Banking licence + deposits:** genuine and hard to replicate (a licence plus ~90% low-cost deposit funding), a structural advantage over Affirm (bank-partner model, no deposit base), Afterpay (within Block), PayPal (distribution but weaker underwriting depth) and the PSPs (distribution but not lending). Verdict: durable.

Klarna's differentiated combination versus all comparators is **licensed-bank funding plus real-time proprietary underwriting**.

### III.16 Volume III Reconstruction — the central question

**Is Klarna's real operational asset the credit decision engine and the repayment data that trains it, or the merchant integration estate that distributes it — and would either survive without the other?**

VERDICT: the **decision engine and the repayment data that trains it** is the core proprietary asset; the merchant estate is increasingly a **rented distribution layer** (post-KCO divestiture and PSP-dependent). Neither fully survives without the other in the short run — the engine needs transaction flow to learn and to lend against, and the merchant estate needs the engine's approvals to convert intent into revenue. But the relationship is asymmetric: **the engine is the harder to replicate and the more defensible,** because merchant distribution can be re-acquired with money and PSP partnerships, whereas the repayment graph is accumulated only over time and only by bearing real credit risk. If forced to choose, the engine is the asset; the merchant estate is the channel.

Answering the sub-questions directly:
- **Most critical subsystem:** the real-time decision engine.
- **Hardest to replicate:** the accumulated repayment/transaction graph and the models trained on it.
- **Where operating leverage actually comes from:** partly automation, but substantially a one-time cost reset (2022 layoffs + 2023 freeze + attrition) — and it is being eroded on the incremental dollar by rising credit provisions, not by opex.
- **Binding constraint on growth:** credit quality/loss performance; next, compliance capacity.
- **Most dangerous third-party dependency:** PSP-mediated distribution via Stripe and Adyen as merchants of record.
- **The gravest strategic risk:** that the PSP pivot slowly commoditises Klarna into a balance-sheet-and-underwriting utility sitting behind Stripe and Adyen — powerful, but disintermediated from the merchant relationship and its data.

## Recommendations

**For an analyst/investor:**
1. **Weight the decision engine, not the AI-cost narrative.** Track credit-loss/provision trends as a percentage of GMV per market, and the US Gini claim over time; a sustained rise in provisions (as in 2025) is the real risk signal, not customer-service automation metrics. Threshold that would change the view: consumer credit losses sustainably above ~0.6–0.7% of GMV, or a clear deterioration in new-market cohorts.
2. **Discount self-reported operational metrics** (revenue per employee, "work of N agents," AI savings) by default and require independent corroboration; the documented CEO reversal is the justification.
3. **Monitor the PSP dependency** as the most dangerous single point of failure; watch for any disclosure of the share of merchant revenue via Stripe/Adyen MoRs and for changes in those partnerships.
4. **Track the compliance load** as the next constraint: the adequacy of FI remediation, the UK FCA BNPL regime (July 2026), EU AI Act Annex IV (August 2026), and the US industrial-bank application outcome. A second FI escalation or an adverse FCA affordability finding would be materially negative.

**For an operator benchmarking Klarna:**
5. Replicate the event-sourced feature architecture (Kafka schema contracts + a shared business-logic library + retrospective calculation). It is genuinely best-practice and is the corroborated, non-marketing part of the technology story.
6. Do **not** replicate the "AI-first customer service" playbook without a human fallback and without resolution-quality (not deflection) metrics; Klarna's own reversal is the cautionary case.

## Caveats
- Klarna's engineering blog, AI announcements and productivity statistics are **COMPANY CLAIM**; several were later qualified by the CEO. All Gini, loss-rate, revenue-per-employee and "AI savings" figures are self-reported and not independently audited.
- The re:Invent architecture is presented by a Klarna engineer (CONFIRMED as to design, COMPANY CLAIM as to performance); some details (multi-region posture, core ledger) remain UNKNOWN.
- Debt-collection agency counterparties, the precise internal firewalling of credit-assessment vs advertising data, and any consortium/alternative data sources are UNKNOWN from the public record.
- Figures mix IFRS (revenue, net loss, GMV), non-IFRS (adjusted operating profit/margin, transaction margin) and, where noted, SEK statutory figures for Klarna Bank AB and the FI decision; each is labelled at point of use. A minor scale discrepancy exists between IR materials (3.4m transactions/day, 118m users) and the F-1 (≈3.0m/day, 111m users, period ended 30 June 2025), reflecting growth over time.
- The FI decision covers 1 April 2021–31 March 2022; Klarna states remediation began (the 12-transaction CDD trigger from 1 November 2024). Post-remediation adequacy is not yet independently confirmed.

---

# VOLUME IV — Financial Statements, Revenue Architecture, Credit Economics, Unit Economics, Regulatory Capital & Capital Allocation

## TL;DR
- Klarna is a **high-velocity, standardised-approach credit institution** whose ~40-day book turns roughly nine times a year, so a dollar of annual GMV consumes only about **1.0–1.3 US cents of CET1** — roughly one-ninth of a revolving card lender — which is the single most distinctive and under-appreciated economic fact about the business.
- On an **IFRS basis Klarna is not yet profitable at scale**: FY2025 revenue was $3,509m (+25%) but it posted an operating loss of $(230)m and a net loss of $(273)m (of which $(294)m attributable to shareholders, EPS $(0.79)); the $65m "adjusted operating profit" (1.9% margin) excludes $157m of share-based pay and should not be believed as the economic result.
- The **originate-to-distribute pivot** (Nelnet up to $26bn Pay-in-4, Elliott $2bn/$17bn US Financing, Värde $1.7bn SRT, Santander €1.4bn) is simultaneously a capital-efficiency improvement, a genuine risk transfer, and an earnings-quality question: it front-loads gain-on-sale ($73m in Q4 2025 on $1.6bn of loans sold) and reshapes margin, making reported profit progressively harder to read.

## Key Findings
1. **Three reporting entities must never be conflated.** Klarna Group plc (consolidated, USD, IFRS as issued by IASB, 20-F/6-K); Klarna Bank AB (publ) (Swedish statutory, SEK, IFRS-EU + Swedish Annual Accounts Act); and Klarna Holding AB Consolidated (the prudential "consolidated situation," SEK, CRR/CRD Pillar 3). Capital ratios come only from the last.
2. **Revenue is ~71% transaction-and-service, ~29% interest + gain-on-sale.** FY2025: transaction & service $2,500m, interest income $937m, gain on sale of consumer receivables $73m. Merchant fees are the highest-quality line; consumer late/"reminder" fees and gain-on-sale are the most fragile.
3. **The deposit advantage is real and structural.** ~90% deposit-funded; group consumer deposits grew from $9.5bn (Dec 2024) to $13.0bn (+37% YoY, Dec 2025). Prudential deposits from the public reached ~SEK 121.8bn. This is materially cheaper and stickier than the wholesale/forward-flow money on which Affirm and other non-bank BNPL peers rely (Affirm's average cost of funds was ~7.1–7.2% in 2025).
4. **The FY2025 swing into loss is driven by credit-provision timing, not deteriorating underwriting.** Provision for credit losses rose to $794m (from $495m); but realised losses stayed ~0.44–0.45% of GMV, delinquencies improved (BNPL 60+ day 0.89%), and the driver is (a) rapid growth and (b) mix-shift into longer-duration US Fair Financing whose IFRS 9 expected losses are booked upfront while interest income accrues over the loan's life. US provision as a % of GMV actually *fell* from ~3.6% in 2021 to ~0.63% in 2025 even as US GMV grew ~213%.
5. **Capital is scarce at the bank, not the holdco.** Prudential CET1 ratio fell from 16.8% (Dec 2024) to ~15.7% (Dec 2025) even as REA grew from SEK 77.0bn to SEK 92.7bn; upstreaming cash from Klarna Bank AB to Klarna Group plc is constrained by buffers and a Pillar 2 Guidance raised to 5% of REA in September 2025.

## Details

### IV.1 Multi-Year Financial History
**Basis discipline note.** Through FY2021 the group reported as Klarna Holding AB in **SEK, IFRS-EU**. From the 2024 redomiciliation (share-for-share exchange; parent moved to the UK — Klarna Group plc — in May 2024) the listed group reports in **USD, IFRS-IASB**. Klarna Checkout (KCO) was divested in October 2024 (the group's cash-flow shows a **net gain from divestment of $190m** in 2024); all 2024/2025 like-for-like series are KCO-adjusted. These are definitional/accounting changes, not economic ones.

Legacy series (Klarna Holding AB, SEK):
- 2019: GMV SEK 332bn (~$35bn); total net operating income SEK 7.16bn (~$753m); CET1 ratio 28.1%.
- 2020: GMV SEK 484bn (~$53bn, +46%); net operating income SEK 10bn ($1.087bn, +40%); CET1 ratio 29.5%.
- 2021: GMV SEK 689bn; revenue SEK 13.9bn; credit losses SEK 4.6bn; net result SEK (7.1)bn; take rate 2.31%; loss rate 0.67%.
- 2022: GMV SEK 837bn; revenue SEK 19.3bn; credit losses SEK 5.7bn; net result SEK (10.4)bn; take rate 2.31%; loss rate 0.68%. (2022 was the valuation trough — the $800m recap at a $6.7bn valuation, down from the $45.6bn SoftBank peak of June 2021.)

Group series (Klarna Group plc, USD, IFRS):
| USD m | FY2023 | FY2024 | FY2025 |
|---|---|---|---|
| Total revenue | 2,276 | 2,811 | 3,509 |
| — Transaction & service | 1,768 | 2,136 | 2,500 |
| — Interest income | 508 | 675 | 937 |
| — Gain on sale of receivables | — | — | 73 |
| Processing & servicing | (541) | (596) | (809) |
| Provision for credit losses | (353) | (495) | (794) |
| Funding costs | (297) | (503) | (667) |
| Operating loss (IFRS) | (323) | (121) | (230) |
| Net profit/(loss) (total) | (244) | 21 | (273) |
| Attributable to shareholders | (249) | 3 | (294) |
| Basic/diluted EPS ($) | (0.69) | 0.01 | (0.79) |
| GMV ($bn) | 92 | 105 | 127.9 |
| Active consumers (m) | — | 92 | 118 |
| Take rate | ~2.5% | ~2.66% | ~2.74% |

Quarterly FY2025 net result: Q1 $(99)m; Q2 $(53)m; Q3 $(95)m; Q4 $(26)m. Revenue Q1 $701m, Q2 $823m, Q3 $903m, Q4 $1,082m (first billion-dollar quarter). Q1 2026 returned to a $1m net profit on $1.0bn revenue and $68m adjusted operating profit.

### IV.2 Revenue Architecture
FY2025 lines and drivers:
- **Merchant fees** (~57% of total revenue in 2024; the core engine): merchants pay ~3.29%–5.99% + $0.30 per transaction; recognised under IFRS 15 at point of transaction; driver is GMV × merchant take rate; high durability, strong pricing power, low capital intensity — the highest-quality line.
- **Consumer service revenue / late ("reminder"/"snooze") fees** (~16% of transaction-and-service revenue in 2024; ~$254m in 2024): IFRS 15; driver is delinquency incidence; cyclical and regulatory-fragile (CCD II, UK BNPL regime).
- **Interest income** ($937m FY2025, +47% YoY in Q4): earned on Fair Financing (interest-bearing installments up to ~19.99–29% APR) and on the liquidity portfolio; recognised under IFRS 9 effective-interest; the fastest-growing line, driven by Fair Financing GMV (+165% in Q4).
- **Advertising / retail media** ($180m in 2024, ~$230m estimated 2025): high-margin, IFRS 15; strategic optionality (Amazon-style retail media) but small.
- **Interchange** (~$84m in 2024, ~3% of revenue): Klarna Card, ~1% average; embedded in interest income/other; growth optionality as the Card scales (4.2m users, 15% of transactions by Q4 2025).
- **Gain on sale of consumer receivables** ($73m FY2025, all in Q4): IFRS 9 derecognition gain on Fair Financing forward-flow sales; **new, lumpy, and low-quality** as a recurring line.

Regional FY2025: United States $1.24bn, Germany $848m, United Kingdom $442m, other $976m. US grew 58% in Q4 and is now the largest single market. Net dollar revenue retention 115% (Q1 2025). Genuinely recurring revenue is the merchant-fee and interest base; gain-on-sale and late fees are the least durable.

### IV.3 Net Interest Income and the Deposit Advantage
FY2025 interest income $937m; funding costs $667m (of which "interest costs on funding" $132m in Q4 vs a $78m Q4 fair-value adjustment on loans sold/held-for-sale). Klarna's cost of deposits is low: German fixed deposits historically 1.15% (2021) rising to ~2.28% (6-month EUR, 2025); Raisin overnight 0.35% at launch; US savings 3.28% base / up to 3.78% (2026, US, not FDIC-insured directly — via WebBank pass-through). Because ~90% of funding is deposits, blended funding cost is far below the wholesale rates Affirm pays. This is the structural differentiator Volume I identified: Klarna funds a 40-day asset with sub-3% insured retail deposits; a non-bank funds the same asset with high-single-digit wholesale/forward-flow money.

### IV.4 Cost Architecture (economic drivers)
FY2025 operating expenses $3,739m:
- **Variable with GMV:** processing & servicing $809m (payment-network/PSP), funding costs $667m, provision for credit losses $794m. These three ("transaction costs," $2,270m) scale directly with volume and product mix.
- **Step-fixed/fixed:** technology & product development $486m, sales & marketing $414m, customer service & operations $207m, general & administrative $306m, D&A $55m.
- **Non-cash but real:** share-based payments $157m (FY2025 cash-flow add-back).
- **One-offs:** Finansinspektionen fine SEK 500m (~$45–46m, booked 2024) for AML deficiencies over April 2021–March 2022; IPO preparation costs; restructuring/severance.

The true **marginal cost of an incremental dollar of GMV** ≈ processing (~0.63%) + provisions (~0.62%) + funding (~0.52%) = ~1.77% of GMV, against revenue of ~2.74% — a marginal transaction margin of ~0.97% of GMV before any operating cost. AI-driven efficiency cut customer-service cost per transaction ~40% since Q1 2023; headcount down ~49% since 2022 while revenue/employee reached $1.24m.

### IV.5 Credit Economics in Depth
IFRS 9 expected-credit-loss (ECL) with three-stage staging; default at 90+ days past due, debt collection, or fraud. FY2025 provision for credit losses $794m vs realised losses of ~0.44–0.45% of GMV — the gap is the upfront ECL on a fast-growing book. Provision as % of GMV by quarter: Q4'24 0.53%, Q1'25 0.54%, Q2'25 0.56%, Q3'25 0.72%, Q4'25 0.65%. Delinquencies improved: BNPL 60+ day 0.89% (Q2'25, down from 1.03%); Fair Financing 2.23% (down from 2.34%).

Coverage (allowance/gross, Dec 31 2025): Fair Financing $272m / $4,604m = **5.9%**; Pay Later $220m / $6,347m = **3.5%**; total $492m / $10,951m = **4.5%**. By Q1 2026 total allowance for credit losses was 4.6% (Pay Later 3.5%, Fair Financing 6.2%).

**Central credit question — verdict:** the rising provision charge is a function of **growth plus mix-shift toward longer-duration US Fair Financing**, not deteriorating underwriting. The tells: (1) US provision as a % of GMV *fell* from ~3.6% in 2021 to ~0.63% in 2025 even as US GMV grew ~213%; (2) the CFO's own Q4 arithmetic — $2.5bn of US Fair Financing originated in Q4 booked $80m provisions upfront but only $40m revenue, with a further ~$180m of interest income still to come, lifetime net profit unchanged (~$35m in his example), simply spread over time; (3) realised losses and delinquencies are flat-to-improving. This is IFRS 9 timing, not credit deterioration — though it does mean reported profitability understates the through-cycle economics during hyper-growth, and would overstate them if growth stalled.

### IV.6 Unit Economics
- **Per active consumer:** 118m consumers; ARPU ~$30 (trailing). "Banking" consumers (Card/savings/Fair Financing) — 15.8m, +101% — generate $107 revenue each, >3× the base.
- **Per transaction:** 3.4m transactions/day; average order value low; average balance per active consumer $80 (Pay in Full $0, Pay Later $88, Fair Financing $408) vs a US credit-card average of ~$6,730 (Experian, 2024).
- **Cohort curve:** purchase frequency rises from ~2× in year one to ~11–18× by later years (Q1 2019 cohort at 18×). This compounding is the ARPU engine.
- **Per dollar of GMV (most revealing):** revenue ~2.74 cents, transaction margin ~0.97 cents, adjusted operating profit ~0.05 cents, IFRS net loss ~(0.21) cents.

### IV.7 Transaction Margin — the company's metric, tested
Definition: **transaction margin dollars = total revenue − processing & servicing − provision for credit losses − funding costs**; transaction margin = TMD ÷ total revenue. FY2025 TMD ≈ $1,239m (Q1 $271m + Q2 $315m + Q3 $281m + Q4 $372m), a transaction margin of **~35.3%** of revenue (down from the mid-40s in 2024 and 39% in Q1'25 vs 42% a year earlier). The compression is driven by (a) US mix, (b) upfront Fair Financing provisioning, and (c) offloading (Pay Later loans sold below par book an accounting loss in funding costs). Management's 2026 target: TMD >1.04% of GMV. **Assessment:** TMD is a *defensible* gross-margin proxy because — unlike Affirm's earlier framing — it *does* deduct credit losses and funding. But "TMD before provision for credit losses" ($622m in Q4) is a flattering construction that strips the single largest volume-linked cost and should be treated with scepticism, exactly as Volume III's CEO-qualified operational metrics warned.

### IV.8 The IFRS-to-Non-IFRS Gap — forensic treatment
Adjusted operating profit = operating profit/(loss) excluding (i) D&A and impairments, (ii) share-based payments, (iii) severance/restructuring, (iv) IPO-preparation costs. FY2025 bridge (USD m): **Operating loss (230)** + D&A/impairments 55 + share-based payments 157 + restructuring/IPO ~83 = **Adjusted operating profit 65**.
- **D&A ($55m):** partly amortisation of acquired intangibles (Sofort, Close Brothers Retail Finance, Stocard, PriceRunner) — a real economic cost of the acquisition strategy; adding it back is only partly defensible.
- **Share-based payments ($157m):** a **real, dilutive economic cost**; excluding it is the least defensible adjustment and accounts for the bulk of the gap.
- **Restructuring / IPO costs:** genuinely non-recurring; adding back is defensible.

**Which measure this study believes:** the **IFRS operating loss of $(230)m and net loss of $(273)m ($(294)m attributable)**. Adjusted operating profit of $65m materially overstates the economic result because $157m of stock compensation is a real cost borne by shareholders through dilution. The honest read: Klarna is roughly breakeven at the operating line on a through-cycle, growth-normalised basis, but has **not yet earned a clean IFRS profit at scale**.

### IV.9 Bank Balance Sheet Teardown (RE-CUT)
Klarna Group plc consolidated balance sheet, 31 December 2025 (USD m), read as a bank:

**Assets ($18,797m):**
- Cash and cash equivalents (incl. central-bank balances) 3,803
- Debt securities (liquidity portfolio / HQLA) 1,518
- Consumer receivables (amortised cost, net of ECL) 10,459 — Pay Later net 6,127, Fair Financing net 4,332
- Consumer receivables at fair value through OCI (hold-to-collect-and-sell) 386
- Consumer receivables at fair value through P&L (originate-to-sell / **held for sale**) 400
- Settlement and trade receivables 580
- Property & equipment 60
- Goodwill 685 and Intangible assets 383 (from Sofort, Close Brothers Retail Finance, Stocard, PriceRunner)
- Deferred tax assets 36; Other assets 487

**Liabilities ($16,113m):**
- Consumer deposits 13,003 (the dominant funding source, ~90%)
- Notes payable and other borrowings 1,359 (warehouse draws, EMTN senior notes, subordinated)
- Payables to merchants 736; Accounts payable & accrued 655; Other 358; DTL 2

**Equity ($2,684m):**
- Additional paid-in capital 427; Reserves (90); Retained earnings 2,170; NCI 177. (Note the FY2025 reclassification: paid-in capital fell from $4,646m to $427m while the accumulated deficit of $(2,081)m became retained earnings of +$2,170m — a capital-reduction/reorganisation at the IPO, not economic profit.)
- **Additional Tier 1 instruments** (SEK 1,500m Klarna Holding AB, Feb 2024, STIBOR3M+9.5%; SEK 276m Klarna Bank AB, Mar 2022, STIBOR3M+7%) sit in equity under IFRS but are **not common equity** — a key trap.

**Leverage:** a naïve equity/assets ratio of ~14% is meaningless for a bank; the meaningful measure is the **prudential leverage ratio of ~9.4% (Dec 2025)** on the Klarna Holding AB consolidated total exposure of ~SEK 172bn.

**Reconciliation, Group vs prudential consolidation:** the Klarna Holding AB Consolidated ("consolidated situation") is the CRR scope on which Pillar 3 ratios are struck; it differs from Klarna Group plc because (a) the prudential parent is the Swedish Klarna Holding AB, not the UK Klarna Group plc, (b) intangibles are deducted from CET1, (c) AT1/T2 issued by subsidiaries are only included up to the share needed to cover Klarna Bank AB's minimum requirement (Art. 85/87 CRR), and (d) currency is SEK. Prudential deposits from the public (SEK 121.8bn) exceed the Group's USD consumer-deposit figure because of scope and translation.

### IV.10 Funding Architecture (all sources traced)
1. **Retail deposits** (~90%): Sweden and Germany the core savings markets; Swedish deposit-guarantee scheme up to SEK 1,050,000/€100,000 per depositor; growing US "Balance"/savings (WebBank pass-through, not directly FDIC-insured). Group $13.0bn (Dec 2025).
2. **Santander warehouse** (€1.4bn, Aug 2025, sole lender, German receivables; Santander senior-secured, Klarna equity first-loss).
3. **Forward-flow / whole-loan sales** (off-balance-sheet): Nelnet up to $26bn Pay-in-4; Elliott $2bn facility / $17bn US Financing capacity (plus a $6.5bn Fair Financing two-year deal and the Oct 2024 UK portfolio sale freeing ~£30bn capacity); Värde $1.7bn SRT.
4. **Debt securities issued:** EMTN SEK 1.5bn senior unsecured (Jun 2025; SEK 600m due 2027 STIBOR+1.6%, SEK 900m due 2028 STIBOR+1.8%).
5. **Subordinated (Tier 2):** SEK 500m (2023, STIBOR+7.5%), SEK 250m (2023, STIBOR+7.5%), USD 100m (2024, SOFR+7%).
6. **AT1 (equity under IFRS):** SEK 1,500m + SEK 276m.
7. **Common equity.**

Blended cost of funds is low and falling relative to peers because deposits dominate; the deposit base is sticky (guaranteed, app-embedded) but a rapid outflow would force reliance on more expensive warehouse/forward-flow capacity and could pressure the LCR — which, at ~853% (2024) rising to ~1,013% (2025), currently provides enormous headroom.

### IV.11 The Capital Cost of a Dollar of GMV (NEW SECTION — the payoff)
**Working (stated assumptions in brackets):**
- Year-end net receivables $10.5bn on FY2025 GMV of $127.9bn → **net receivables/annual GMV ≈ 8%**. This follows directly from velocity: with ~40-day duration, receivable ≈ GMV × 40/365 ≈ 11% gross, reduced by Pay-in-Full (no receivable) and by offloading to ~8% net.
- Standardised-approach retail risk weight = **75%** (CRR Art. 123); Klarna's disclosed average risk weight has historically been ~75%, and credit risk is ~84–95% of total REA.
- Total prudential REA (Klarna Holding, Dec 2025) SEK 92.7bn ≈ **$10.2bn** (at ~SEK/USD 0.11) on GMV $127.9bn → **REA per $1 of annual GMV ≈ 8 US cents**.
- CET1 held at management's operating ratio (~15.7%): 8¢ × 15.7% ≈ **1.25 US cents of CET1 per $1 of annual GMV**. At the binding regulatory CET1 minimum (~8.7% incl. buffers): ≈ **0.7 cents**.

**Comparison with a revolving card lender:** a credit-card receivable persists ~12 months (book turns ~1×) versus Klarna's ~9× (365/40). For the *same annual volume*, a card lender carries roughly **9× the average balance, ~9× the RWA, and ~9× the CET1**. Klarna's average balance per consumer ($80) versus a US card ($6,730) is the same fact at the consumer level. **This velocity is the core structural advantage.**

**Extensions:**
- **ROE:** because each dollar of CET1 supports ~9× the annual volume of a card book, the *potential* return on equity per unit of capital is far higher — but only if the thin per-dollar margin (net loss today) turns positive.
- **Pay-in-4 vs Financing:** Pay-in-4 (38-day duration) consumes far less capital per dollar of GMV than Fair Financing (180-day duration, ~4.7× longer on book, higher ECL coverage at 5.9%). The originate-to-distribute pivot targets exactly the capital-heavy Financing and the seasonal Pay-in-4 peaks.
- **IRB vs standardised:** Klarna uses the **standardised approach** (75% flat retail RW). Given realised losses <0.5% of GMV and 99% on-time repayment, an internal-ratings-based (IRB) model would likely produce risk weights well below 75%, cutting REA and freeing capital — but IRB approval is costly, slow, and subject to output floors under CRR3/Basel IV (which Klarna says will not materially raise its requirement).

### IV.12 Regulatory Capital and the Cost of the Licence
Klarna Holding AB Consolidated (SEK, prudential):
| | Dec 2024 | Dec 2025 |
|---|---|---|
| CET1 capital (SEK m) | 12,970 | 14,574 |
| Tier 1 (SEK m) | 14,623 | 16,241 |
| Total capital (SEK m) | 16,503 | 17,932 |
| Total REA (SEK m) | 77,022 | 92,654 |
| CET1 ratio | 16.8% | 15.7% |
| Tier 1 ratio | 19.0% | 17.5% |
| Total capital ratio | 21.4% | 19.4% |
| Leverage ratio | 9.9% | 9.4% |
| LCR | 853% | 1,013% |
| NSFR | 178.7% | 192.6% |

Requirement stack (2024): Pillar 1 8.0% + Pillar 2 Requirement 1.2% = total SREP 9.2%; capital conservation buffer 2.5% + countercyclical ~1.0% = combined buffer 3.5%; overall capital requirement 12.6%; **Pillar 2 Guidance 3.5% (2024), raised to 5.0% of REA from September 2025**. Credit risk is standardised (SEK 64.2bn REA in 2024, ~83%; SEK 77.7bn, ~84% in 2025); operational risk uses the Alternative Standardised Approach; note the market-risk REA jump to SEK 5.26bn in 2024 (FX). Leverage minimum 3%; Klarna runs ~3× that.

REA is growing roughly in line with GMV (REA +20% in 2025 vs GMV +22%, off a book being partly offloaded), which — combined with the FY2025 net loss — is why the CET1 ratio slipped despite retained capital. **Upstreaming constraint:** Klarna Group plc is a non-operating holdco; cash reaches it only via dividends/AT1 coupons from Klarna Bank AB, which are constrained by the combined buffer, P2G (now 5%) and the leverage requirement. This is why the IPO raised so little for the company and why distributable capital to public shareholders is, for now, effectively nil.

### IV.13 The Originate-to-Distribute Pivot (NEW SECTION)
**Arrangements:**
- **Nelnet (Aug 14, 2025):** multi-year forward flow, "up to $26 billion in total payment volumes are expected to be sold" of US Pay-in-4 on a rolling basis; **Nelnet assumes the credit risk**, "allowing Klarna to offload liabilities from its balance sheet while retaining full control over loan origination and servicing"; off-balance-sheet. CFO Neglén: "This is a landmark transaction for Klarna in the U.S."
- **Elliott (US Financing):** forward-flow + whole-loan; began Nov 2025 at $1bn, **doubled to $2bn (Mar 2026), 3-year term, supporting up to $17bn** of US Financing; plus a **$6.5bn** two-year Fair Financing deal (back-book + forward flow); plus the Oct 2024 sale of the UK loan portfolio to an Elliott affiliate (~£30bn capacity).
- **Värde (Apr 1, 2026):** a Värde-led consortium "entered into a $1.7 billion Significant Risk Transfer (SRT) transaction," a three-year agreement covering euro-denominated loans; Klarna's sixth and largest SRT, described by CFO Neglén as "our largest and most efficient SRT transaction to date"; frees regulatory capital.
- Combined, these structures support **>$40bn of lending capacity**, dwarfing the on-balance-sheet book.

**Accounting:** receivables originated to sell are classified **at fair value through P&L** ($400m) or **FVOCI** ($386m) and held for sale; sales are derecognised under IFRS 9. **Gain on sale** was **$73m in Q4 2025** (first Fair Financing forward flow, $1.6bn offloaded) and **$57m in Q1 2026** (roughly half from ongoing forward flow, half from a back-book sale). Critically, for **Pay Later** the mechanics invert: Klarna keeps the high-margin merchant fee and sells the receivable *below* originated value, booking an **accounting loss inside funding costs** ($78m in Q4 2025) as it reduces capital/funding — so "gain on sale" understates the true P&L footprint of offloading.

**Assessment — all three at once:**
1. **Capital-efficiency improvement:** yes — moving assets off-balance-sheet reduces REA and CET1 consumption, letting Klarna grow the US without proportional equity.
2. **Risk transfer:** yes — Nelnet and the SRT structures genuinely move credit risk to institutional buyers (Klarna retains servicing and some first-loss/junior positions, so the transfer is partial in warehouse/SRT structures but substantive in forward flow).
3. **Earnings-quality question:** yes and growing — gain-on-sale is lumpy and timing-dependent; the CFO warned gains "will vary with the timing and size" of sales, "creating more reported earnings volatility even if underlying economics remain steady." As offloading scales, reported profit increasingly reflects *when* Klarna chooses to sell, not the period's underwriting.

### IV.14 Cash Flow and the Free-Cash-Flow Question
FY2025 cash flow from operating activities was **$(1,032)m** — but this is a bank distortion, not a signal of distress: it includes a $(2,787)m increase in consumer receivables, a $(378)m + $(413)m increase in FVOCI/FVPL receivables, offset by +$2,148m growth in deposits and a +$794m provision add-back. Share-based payments ($157m) are a non-cash add-back but a real economic cost. Financing activities were +$988m (new share issuance $191m, notes payable +$817m). There is **no ordinary "free cash flow"** for a growing bank: growth in the book consumes cash funded by deposit growth. Genuinely distributable cash to the listed entity is constrained by the prudential upstreaming rules (IV.12) and is currently negligible.

### IV.15 Capital Allocation
- **Private funding & valuation cycle:** ~$3.7bn raised across ~29 rounds; peak $45.6bn (SoftBank, Jun 2021) → trough $6.7bn ($800m recap, Jul 2022) → IPO ~$15.1bn (Sep 2025). A textbook valuation round-trip.
- **2024 redomiciliation** to Klarna Group plc (UK) — enabling a US listing.
- **September 2025 IPO:** priced $40.00 (above the $35–37 range); of the 34.3m shares sold, **only 5m were sold by the company**; **net proceeds to the company were only ~$169m** (per the Klarna Bank AB statutory accounts, net of $22.4m underwriting/offering costs; some press reported a ~$222m gross-of-some-costs figure). The offering was overwhelmingly **secondary** (Sequoia ~23%, plus Silver Lake, BlackRock, Povlsen entities and co-founder Jacobsson selling; CEO Siemiatkowski sold none). **Reading:** the listing's purpose was principally **liquidity for existing holders**, not primary capital — consistent with a company that funds growth via deposits and forward flow, not equity.
- **Acquisitions:** Sofort, BillPay, Close Brothers Retail Finance, Stocard (11m consumers integrated), PriceRunner — the source of the $685m goodwill / $383m intangibles. **Disposal:** Klarna Checkout (Oct 2024, ~$190m net gain).
- **AT1/T2 issuance:** as above, at high floating spreads (STIBOR+7% to +9.5%), reflecting the cost of the licence.
- **No dividend or buyback.**

Discipline is mixed: the AI-driven cost transformation (headcount −49%, revenue/employee $1.24m) is genuinely disciplined; the acquisition programme and the extraordinary private-market valuation cycle were not obviously value-accretive per dollar.

### IV.16 Dilution and Share Count
~378m shares outstanding post-IPO (377.3m at year-end 2025). A multi-class structure was created for the listing; a 12-for-1 share split took effect 6 March 2025. Share-based payments ($157m in FY2025, up from ~$50m+ in 2024) are a persistent dilution source and the single biggest IFRS-to-adjusted gap. With EPS $(0.79), per-share economics remain negative; the SBC run-rate means share count will keep drifting up, a real cost to per-share value that the adjusted metric conceals.

### IV.17 One Dollar of GMV — the waterfall
**Group (FY2025, per $100 of GMV):** revenue $2.74 → less processing $0.63, provisions $0.62, funding $0.52 → **transaction margin $0.97** → less adjusted operating expenses ~$0.92 → **adjusted operating profit ~$0.05** → less D&A ~$0.04, share-based pay ~$0.12, restructuring/IPO → **operating loss ~$(0.18)** → less tax/other → **net loss ~$(0.21)–(0.23)**.

**Pay-in-4 (illustrative):** merchant fee dominates (Klarna keeps it even when the receivable is sold); tiny/no interest; very low funding cost (38-day duration); low ECL; when offloaded, a small accounting loss on the receivable sale but capital freed. Net: thin but positive contribution, extremely capital-light.

**Fair Financing (illustrative):** lower merchant fee but substantial interest income over 180 days; higher funding cost and higher ECL (5.9% coverage) booked upfront; when offloaded, a **gain** on sale (investors pay up for the cash-flowing asset). Net: higher lifetime margin but front-loaded costs — profitable over the loan life, loss-making at origination in a hyper-growth quarter.

The two products' economics differ fundamentally: Pay-in-4 is a **merchant-fee/velocity** business; Fair Financing is an **interest-spread/duration** business.

### IV.18 Economic Driver Tree
Core model: **active consumers (118m) × transactions per consumer (rising 2×→11–18× by cohort age) × average order value = GMV ($127.9bn)**; **GMV × take rate (2.74%) = revenue**; **less loss rate (provision 0.55–0.72% of GMV) × GMV**; **less funding cost (deposit rate × average receivables); less processing (~0.63% of GMV)**; **= transaction margin**; **less step-fixed opex**; **= operating result**. The five variables that explain most outcomes: (1) **book velocity/duration** (drives capital and funding); (2) **US/Fair Financing mix** (drives take rate up, provisions and duration up); (3) **deposit cost** (drives NIM); (4) **provision timing under IFRS 9** (drives reported profit vs economics); (5) **offloading volume** (drives capital, gain-on-sale, and earnings quality).

### IV.19 Scenario Model
- **Base:** GMV >$155bn (2026 guidance), take rate >2.80%, TMD >1.04% of GMV, adjusted operating margin >6.9%; IFRS still near breakeven as SBC persists.
- **Credit downturn:** realised losses rise from ~0.45% toward ~1% of GMV; because the book is short-duration, Klarna can **re-underwrite every transaction** and shrink exposure within ~40 days — the velocity is a defence, but provisions spike and late-fee revenue rises procyclically.
- **Sharp rate cut:** compresses the deposit spread (interest income on liquidity falls, as already seen in Europe), but also lowers funding cost — net NIM effect modest; interest income on Fair Financing is contractual.
- **Regulatory shock (CCD II / UK BNPL affordability checks):** reduces conversion and late-fee revenue; hits the consumer-service line hardest — a genuine threat to a fragile revenue stream.
- **Merchant-fee compression:** the biggest threat to the highest-quality line; even 20–30bps of take-rate erosion would wipe out the thin margin.
- **Strong execution / US growth:** the bull case — US at 58% growth compounding, banking consumers at $107 ARPU.
- **Funding shock (deposit outflow):** LCR headroom (~1,013%) is large, but a run would force reliance on costly warehouse/forward-flow capacity.

**Most dangerous:** a **combination of merchant-fee compression and a credit downturn** — because Klarna's per-dollar margin is already razor-thin (~1 cent of transaction margin), it has almost no buffer to absorb simultaneous revenue and loss shocks. Regulatory affordability rules are the most *likely* structural drag.

### IV.20 Revenue Quality and Normalised Profitability
| Line | Predictability | Recurrence | Pricing power | Cyclicality | Capital intensity | Regulatory risk |
|---|---|---|---|---|---|---|
| Merchant fees | High | High | High | Medium | Low | Low-Med |
| Interest income (Fair Financing) | Medium | High | Medium | High | High | High |
| Consumer/late fees | Low | Medium | Low | High (procyclical) | Low | **High** |
| Advertising | Medium | Medium | Medium | Medium | Low | Low |
| Interchange | Medium | Growing | Low | Low | Low | Medium |
| Gain on sale | **Low** | **Low** | n/a | High | negative | Medium |

**Normalised profitability:** strip the FI fine (~$46m, 2024), IPO costs, and restructuring; normalise credit for the timing mismatch (~$40m Q4 headwind with ~$180m future interest to come) and for the rate cycle. The business is roughly **operating breakeven-to-slightly-positive through the cycle** but **not yet cleanly IFRS-profitable at scale**, because (a) share-based pay (~$157m) is a real recurring cost, and (b) the thin ~1-cent transaction margin leaves little to cover step-fixed technology and G&A. This reconciles the apparent contradiction: adjusted operating profit is positive only because it excludes real costs; the IFRS net loss is the truer picture, with its severity temporarily amplified by IFRS 9 front-loading during hyper-growth.

### IV.21 Valuation-Relevant Economics
- **Growth durability:** high (US 58%, Fair Financing +165%, Card 4.2m users), but decelerating on comps.
- **Margin ceiling:** structurally thin (~1 cent transaction margin per $ GMV); the bull case rests on operating leverage over a fixed cost base plus banking-consumer ARPU ($107 vs $30).
- **Capital intensity:** uniquely low per dollar of GMV (the velocity payoff), and falling further via originate-to-distribute.
- **Cash-flow quality / cyclicality:** bank-style, deposit-funded, procyclical credit.
- **Dilution:** persistent SBC.
- **Optionality:** retail media, Card/interchange, US banking.
- **Long-term ROE:** potentially high *if* the thin per-dollar margin turns durably positive; currently negative.

An owner must believe that (1) merchant-fee take rate holds, (2) US Fair Financing matures into positive lifetime margin faster than provisions front-load, and (3) operating leverage converts ~1 cent of transaction margin into positive IFRS profit at scale.

### IV.22 Volume IV Reconstruction — Ten Conclusions
1. Klarna's **real economic engine** is a two-sided commerce network monetised through **merchant fees on a hyper-velocity, deposit-funded credit book**.
2. The **highest-quality revenue** is merchant fees; the **most fragile** is late/consumer-service fees (regulatory) closely followed by gain-on-sale (lumpy).
3. **Growth requires very little capital** — ~1.0–1.3 cents of CET1 per dollar of annual GMV, roughly one-ninth of a revolving card lender.
4. On an **IFRS basis the business is not yet profitable at scale** (FY2025 net loss $(273)m; $(294)m attributable); adjusted operating profit ($65m) is not the economic result because it excludes $157m of real stock compensation.
5. The **most misunderstood balance-sheet item** is consumer deposits — not ordinary debt but cheap, sticky, insured funding — and, secondarily, the AT1 that sits in equity but is not common equity.
6. The **variable that matters most** to long-term earnings power is **book duration/velocity**, which drives both capital consumption and the ability to re-underwrite in a downturn.
7. **Credit deterioration is not the story**; growth and US/Fair Financing mix-shift under IFRS 9 upfront provisioning are.
8. The **originate-to-distribute pivot** is real capital relief and real risk transfer, but it degrades earnings quality.
9. The **IPO was about liquidity, not capital** (~$169m net to the company) — confirming deposits + forward flow, not equity, fund growth.
10. **Prudential capital, not the reported balance sheet, is the binding constraint**, and it limits what can ever be distributed to public shareholders.

**Central question — verdict:** Klarna is **both**, but weighted toward the optimistic structural case with an unproven margin. It is genuinely a **high-velocity, capital-efficient lender whose ~40-day book is a real structural advantage** — the capital arithmetic in IV.11 is not priced by a market that reads the balance sheet as a corporate. *But* it is **simultaneously a thin-margin credit business whose adjusted profitability disguises the fact that it has not yet earned an IFRS profit at scale.** The velocity advantage is necessary but not sufficient: it lowers the capital and funding cost of a dollar of GMV, yet the ~1-cent transaction margin still has to convert into positive IFRS profit after real stock compensation and step-fixed technology spend. The bull case is that operating leverage and maturing US cohorts close that gap; the bear case is that merchant-fee compression, affordability regulation, or a credit downturn arrive first.

## Recommendations
- **Anchor all analysis to IFRS, not adjusted, figures**, and treat transaction margin as a gross-margin proxy only — never as profit. Benchmark that would change the view: **two consecutive quarters of positive IFRS operating profit** including full SBC.
- **Track five KPIs quarterly:** (1) provision % of GMV vs realised losses (the timing gap); (2) transaction margin % of GMV (target >1.04%); (3) US Fair Financing cohort charge-off curves; (4) gain-on-sale as a share of pre-tax result (earnings-quality flag if >~25%); (5) prudential CET1 ratio vs the ~12.6% overall requirement + 5% P2G.
- **Model capital, not accounting leverage:** use REA/GMV (~8 cents) and CET1/GMV (~1.0–1.3 cents) as the capital-intensity metric; re-run if Klarna pursues IRB approval (would cut REA) or if CRR3 output floors bite.
- **Watch the deposit base and forward-flow renewals** as the true funding story; a deposit outflow or a failure to renew the Nelnet/Elliott/Värde capacity is the fastest route to a growth stall.
- **Discount gain-on-sale from normalised earnings** and add back share-based pay as a real cost when estimating through-cycle profit.

## Caveats
- **Evidence classification:** FY2025 group P&L and balance sheet, the Dec 2024 Pillar 3 capital stack, the funding arrangements, the FI fine, and the IPO mechanics are **CONFIRMED FACT** from primary filings. FY2025 prudential capital figures (CET1 SEK 14,574m, REA SEK 92,654m, CET1 15.7%, LCR 1,013%, NSFR 192.6%) are **CONFIRMED** via Klarna's Pillar 3 2025 / Q1-26 capital supplement (retrieved by a research subagent; internally consistent with the June-2025 interim CET1 of SEK 11,482m and the FY commentary). FY2025 full-year transaction margin dollars (~$1,239m, ~35.3%) and adjusted operating expenses (~$1,174m) are **ANALYTICAL INFERENCE** derived from reported quarterly and full-year figures (they tie out exactly), not printed as standalone annual lines. Note the task brief's assumed Q2/Q3 TMD figures (~$339m/~$291m) were **incorrect**; the reported values are $315m (Q2) and $281m (Q3), which sum with Q1/Q4 to the FY total.
- **Non-IFRS scepticism (per house standard):** Volume III established that management's self-reported operational metrics were later qualified by the CEO; the same scepticism applies here to transaction margin dollars, "TMD before provisions," and adjusted operating profit.
- **Basis risk:** figures move between Klarna Group plc (USD/IFRS), Klarna Bank AB (SEK/statutory) and Klarna Holding AB Consolidated (SEK/prudential); SEK→USD conversions use ~0.11 (2025) and 0.0906964 (31 Dec 2024, the prospectus rate).
- **Data gaps (UNKNOWN):** a precise deposit split by market (Sweden/Germany/other) and by type (demand vs fixed-term) is **not disclosed numerically** for FY2025 (only qualitative Germany/Sweden commentary); the exact IFRS 9 stage-1/2/3 split of loans is not fully public; forward-flow first-loss/retention percentages are not disclosed; the ~$169m vs ~$222m IPO net-proceeds figures reflect different cost bases across sources.
- **Forward-looking items** (2026 guidance of GMV >$155bn, TMD >1.04% of GMV, adjusted operating margin >6.9%, and the ">$40bn lending capacity" and "$26bn"/"$17bn" programme sizes) are **company projections/capacities**, not realised results.

---

# VOLUME V — Management, Culture, Incentives, Competition, Moat, Risk & Strategic Evolution

## TL;DR
- Klarna is, on the balance of evidence, **a genuine two-sided commerce network that owns a real bank** — its deposit funding (91% of the funding base, ~270-day average duration), its short-duration high-velocity book, and its consumer↔merchant network effect are structural and hard to replicate — **but it is simultaneously being pushed toward a commoditised credit-utility role** behind Stripe and Adyen, which now act as merchant of record for a substantial portion of its merchant revenue. Both things are true at once; the strategic question is which vector wins.
- **Management communication should be treated as directionally reliable on audited financials but systematically over-promotional on narrative** — the "work of 700 agents" claim, the framing of the headcount halving, and the reliance on adjusted operating profit ($65m, which excludes $157m of real share-based pay) are promotional exuberance requiring correction, not fraud; the Finansinspektionen AML enforcement is the one item that crosses from spin into a genuine control failure.
- The market's ~$7.5bn valuation (stock ~$20, roughly half the $40 IPO price) plausibly **under-prices the capital efficiency of the short book and the deposit moat while correctly pricing the disintermediation and margin risk** — the single greatest structural risk is payment-service-provider disintermediation, and the most dangerous competitor is not Affirm but the PSPs that distribute Klarna.

## Key Findings
1. **The network effect is real and scores high; the merchant estate scores low.** Klarna's ~119m active consumers and 1.07m merchants (Q1 2026) form a genuine two-sided flywheel, but Volume III's finding holds: since the 2024 Klarna Checkout divestiture, merchant access is increasingly rented through Stripe/Adyen, which act as merchant of record for a "substantial portion" of merchant revenue.
2. **Management credibility is a priceable governance fact, with one exception.** The pattern is promotional-then-corrected: the AI narrative was walked back around 8 May 2025, the headcount halving came overwhelmingly from a hiring freeze and attrition, and non-IFRS "adjusted operating profit" excludes real equity pay. The Finansinspektionen SEK 500m fine (11 December 2024) is the one item that is a substantive control failure, not spin.
3. **The CEO incentive is structured to be worthless unless the stock roughly triples.** The March 2025 grant of 17,505,672 Class C options carries a weighted-average exercise price of ~$91.80 per ordinary-share equivalent — more than double the $40 IPO price and ~4.5x the current ~$20 quote — so it is deeply out of the money and aligns Siemiatkowski to a very high bar.
4. **Take rate tells the whole strategic story.** Klarna's ~2.7% take rate versus Affirm's ~8.9% is not weakness; it reflects a short-duration, merchant-funded, spend-centric model (~$101 average order value) versus Affirm's longer-duration, interest-funded lend-centric model (~$255 AOV). Klarna runs ~3x Affirm's GMV for similar revenue, on roughly one-ninth the capital per dollar of GMV.
5. **The originate-to-distribute pivot is a double-edged sword** — Nelnet (up to $26bn of Pay-in-4), Elliott ($2bn facility supporting up to $17bn of US Financing), and Santander (up to €1.4bn) give capital-light growth capacity, but the resulting gain-on-sale ($57m in Q1 2026) degrades earnings quality and predictability.

## Details

### V.1 The Founders and the Founding Idea
Klarna was founded in Stockholm on 1 July 2005 as **Kreditor Europe AB** by three Stockholm School of Economics students — **Sebastian Siemiatkowski, Niklas Adalberth and Victor Jacobsson**. The founding insight came from Siemiatkowski's experience as a salesperson at a factoring company: merchants wanted guaranteed payment, and consumers wanted to pay only after receiving and being satisfied with goods — a trust gap especially salient in Sweden's mail-order culture. The idea was to insert a middleman who pays the merchant at checkout and collects from the consumer after delivery. The trio pitched at the school's entrepreneurship competition and **finished last**; the judges saw card payments as the future. Angel investor **Jane Walerud** invested roughly SEK 600,000 for about 10% and connected them to the developers who built the first platform. The company rebranded from Kreditor to **Klarna in 2009**.

Operating philosophy (revealed by behaviour; COMPANY CLAIM where stated): high risk tolerance, long-horizon ambition, and a willingness to take publicly uncomfortable decisions (the 2022 layoffs and down round). Siemiatkowski told CNBC (interview October 2024, published 31 March 2025) that he still asks himself "do I still think that Klarna can become the next Google in size, that we can become a hundreds of billions dollar market company, or a trillion dollars… I still am crazy enough to think that's achievable." Siemiatkowski, born 1981 to Polish immigrant parents in Uppsala, has been CEO for the entirety of Klarna's ~20-year existence — an unusually long tenure — and is the company's public face and chief promoter. His communication style (an AI-generated avatar delivering earnings remarks; provocative public statements on AI and jobs) is itself a strategic and governance fact: it drives brand awareness cheaply but repeatedly requires later qualification.

**Current roles/residual influence:** Siemiatkowski remains CEO and holds ~7% economic stake plus enhanced-vote Class C options. **Niklas Adalberth** left operational roles in 2015 to found the Norrsken Foundation; no operational role, residual equity. **Victor Jacobsson** left operations around 2012, holds ~8% (one of the largest holders), is not operationally involved but exerted influence through allied directors — the source of the 2024 boardroom conflict.

### V.2 Current Management
- **Sebastian Siemiatkowski — Co-Founder & CEO** (since 2005/2010). Key-person risk is high: he embodies the brand and strategy. Base salary $3.3m, FY2025 bonus $0.3m, plus Class C options.
- **Niclas Neglén — CFO** (since March 2021; appointed executive director February 2025). Prior: COO/CFO EMEA at HSBC Private Bank; CFO of GE Capital UK — a genuinely heavyweight, bank-grade finance background that lends credibility to the capital-markets execution (forward-flow, significant risk transfer, warehouse funding).
- **Camilla Giesecke — COO.**
- **David Sykes — Chief Commercial Officer** (former Head of Klarna US; former COO of QuadPay).
- **Yaron Shaer — CTO.**
- **David Fock — Chief Product & Design Officer.**
- **Arvind Varadhan — Chief Credit Risk Officer.**
- **Boudien Moerman — Chief Legal Officer.**
- US/compliance leadership is distributed across entities (Klarna Inc. CFO; KFS UK compliance; US compliance directors), consistent with the follow-the-legal-entity structure.

**Leadership depth / turnover:** the C-suite is experienced and stable at the top, but the AI-first culture and headcount reduction (5,527 full-time employees at end-2022 to 3,422 at end-2024, further reduced toward ~2,800 by 2026) create retention pressure lower down, aggravated by equity awards struck well above the current share price. Key-person risk concentrated in Siemiatkowski is the standout.

**Board (post-listing):** Chair **Michael Moritz** (ex-Sequoia, wrote Klarna's first cheque in 2010); **Andrew Reed** (Sequoia); **Lise Kaae** (CEO of Heartland, the Bestseller/Holch Povlsen investment vehicle); **Sarah Smith** (ex-Goldman Sachs); **Markus Villig** (Co-Founder/CEO Bolt, joined February 2025); **Mateusz Staniszewski** (Co-Founder/CEO ElevenLabs, joined May 2025); **Omid Kordestani** (ex-Google/Twitter, chair of the Remuneration & Nomination Committee); plus executives **Siemiatkowski** and **Neglén**. Independence is constrained: the chair is a long-time investor-affiliate, two seats are Sequoia/Heartland investor-linked, and the multi-class structure concentrates control regardless of board composition. The precise count of formally independent directors could not be confirmed from public sources and remains partly UNKNOWN.

### V.3 The Management System
Klarna runs on an **AI-first operating philosophy** enforced from the top: a hiring freeze from late 2023 with an explicit instruction to use AI to fill gaps, an OpenAI-powered assistant launched February 2024, and revenue-per-employee elevated to ~$1.24m (FY2025) and ~$1.4m (Q1 2026), roughly 3.6–4x the 2022 level. Product is organised around three consumer products (Pay Now, Pay Later, Fair Financing) plus the Klarna Card and app, with a "spend-centric not lend-centric" framing.

The critical governance question — **do risk and compliance hold genuine veto rights?** — is answered partly by the record. The Finansinspektionen investigation (period 1 April 2021–31 March 2022) found the general risk assessment "has had significant deficiencies; for example, it has not contained any assessments of how the bank's products and services could be used for money laundering or terrorist financing," and that customer-due-diligence procedures did not capture all situations for the invoice product (fi.se, 11 December 2024). That is evidence that during the examined period, **compliance did not have effective veto over a fast product culture.** ANALYTICAL INFERENCE: the SEK 500m fine, the subsequent US ILC application (which would bring US banking in-house and expand the regulated perimeter), and the CFO's bank-grade profile suggest the control function has been strengthened since — but Volume V cannot confirm from public data that risk now holds a hard veto; this remains partly UNKNOWN.

### V.4 Declared versus Revealed Culture, and the Credibility Question (RE-CUT)
**Declared:** mission to make payments "simple, fair and smart"; consumer-champion positioning (no/low consumer fees, "fair" financing, transparency versus revolving-card debt traps); AI-first productivity leadership.

**Revealed (tested against behaviour and filings):**
- **The AI narrative was overstated and corrected.** The claim originated in the Klarna/OpenAI joint press release of 27 February 2024, which stated the AI assistant "has had 2.3 million conversations, two-thirds of Klarna's customer service chats… is doing the equivalent work of 700 full-time agents… estimated to drive a $40 million USD in profit improvement to Klarna in 2024." Crucially, this described **avoided/outsourced-contractor workload, not 700 redundancies;** the headcount halving came overwhelmingly from a hiring freeze and natural attrition. Around **8 May 2025**, Siemiatkowski conceded to Bloomberg that "as cost unfortunately seems to have been a too predominant evaluation factor when organizing this, what you end up having is lower quality," adding that "it's so critical that you are clear to your customer that there will be always a human if you want" — reopening hiring for premium support. This is the cleanest case of promotional exuberance later qualified.
- **Non-IFRS presentation flatters the result.** "Adjusted operating profit" of $65m (FY2025) excludes $157m of real share-based pay; the IFRS result was an operating loss of $(230)m and a net loss of $(273)m, $(294)m attributable, EPS $(0.79). This is a legal, common, but consequential presentation choice.
- **Enforcement.** The FI **remark + SEK 500m fine (~$45m, 11 December 2024)** for AML deficiencies. Klarna's spokesman Joel Hedin told AFP that "it is important to emphasise that the decision concerns rule interpretation and application and not actual cases of money laundering" — a characterisation that sits against the regulator's own finding of "significant deficiencies." Plus data-protection findings (2022; 2024 on appeal; a 2025 reprimand).
- **Collections/late-fee optics.** Late fees are presented as "reminder" fees ($254m in 2024) and "snooze" fees ($128m) — optically softer, functionally consumer charges.

**Defensible position on credibility:** Klarna management is **promotional and narrative-forward, and its non-IFRS framing and operational claims require independent correction — but the pattern is exuberance and selective emphasis, not misrepresentation of audited numbers.** The hard financials (GMV, revenue, deposits, credit metrics) have proven reliable; the *interpretations* layered on top (AI substitution, "profitability," "owned" merchant relationships) do not. The one item that crosses from spin toward substantive failure is the AML control gap, which was adjudicated by a regulator, not a commentator.

**What an analyst should do with company statements:** accept the audited IFRS figures; discount adjusted/non-IFRS profit measures and add back SBC; treat every strategic, cultural, productivity and "profitability" claim as COMPANY CLAIM to be corroborated against filings and third parties; and weight regulator findings above management characterisations of them.

### V.5 Incentive Architecture
- **CEO Class C options:** 17,505,672 granted 5 March 2025, four-year vesting, 4.5-year term, weighted-average exercise price ~$91.80 per ordinary-share equivalent — deeply out of the money versus the $40 IPO and ~$20 current price, described in the 20-F as "substantially out of the money" with "no value… realizable… unless and until the ordinary share price exceeds the exercise price." The board also amended earlier options into up to 2,941,236 Class C shares. **The "up to $35 billion" figure** that became a governance flashpoint in 2024 was a reported maximum theoretical value of a proposed CEO equity/option programme, contingent on an extreme increase in valuation; what was actually granted is the far more conditional Class C option package above, whose value is zero unless the shares roughly triple. FY2025 CEO cash was modest (salary $3.3m, bonus $0.3m).
- **Multi-class share structure:** ordinary shares (1 vote, full economics); **Class B** (10 votes, no economic rights, held by founders/pre-IPO investors); **Class C** (10 votes, dividends at half the ordinary rate, reserved for Siemiatkowski and related parties), capped so Class C voting cannot exceed 15% of pre-IPO voting rights, with automatic redesignation after 20 years. This protects founder/insider control and insulates long-horizon strategy from public-market pressure — a governance cost that must be priced.
- **Banking-law constraints:** because Klarna Bank AB is an EU credit institution, remuneration is subject to CRD/EBA rules — a 1:1 variable:fixed cap, deferral, malus and clawback on variable pay. This meaningfully limits classic short-term bonus gaming.
- **What the system rewards:** GMV and network growth above all (the metrics the market and merchants reward), then engagement (card, deposits, membership). ANALYTICAL INFERENCE: incentives tilt toward **GMV/growth over near-term reported profitability,** and the upfront-provisioning drag of Fair Financing means growth can suppress reported profit — a tension management manages via originate-to-distribute. Credit quality is protected by the short book (re-underwritten each transaction) and banking-law malus, but the structural pull is toward volume.

### V.6 The Competitive Universe
- **Direct BNPL peers — Affirm, Afterpay/Clearpay (Block), Zip, Sezzle:** solve the same consumer instalment-at-checkout problem; compete for the same merchant integration and consumer mindshare.
- **Payments giants with pay-later — PayPal (Pay in 4), and Apple** (Apple Pay Later, launched March 2023, **discontinued June 2024,** replaced by third-party lenders including Affirm inside Apple Pay — an instructive failure showing even Apple abandoned owning the product).
- **Card networks — Visa, Mastercard:** offer instalment APIs embedded at the network level; can commoditise instalments across every card.
- **PSPs that distribute Klarna — Stripe, Adyen, Shopify, Worldpay:** simultaneously Klarna's distribution and its most dangerous disintermediation risk.
- **Platforms — Amazon, Shopify:** own the merchant relationship and can favour their own or partner financing (Amazon–Affirm renewed to January 2031).
- **Banks/card issuers:** whose revolving credit Klarna displaces at the point of sale.
- **Neobanks — Revolut, N26, Monzo:** compete for the deposit and daily-spend relationship Klarna now targets via card and savings.

### V.7 Competitor Teardowns
**Affirm (cleanest comparator).** FY2025 (year to June 2025): average loans held for investment ~$6.5bn, allowance ~5.6% of loans; RLTC take rate around 4%+ of GMV; funding via warehouse, securitisation and forward flow, with recent ABS spreads under 100bps and weighted-average yields below ~4.6% — but structurally reliant on wholesale/capital-markets funding rather than deposits, with an average cost of funds materially above Klarna's deposit cost (Affirm's average cost of funds ran ~7.1–7.2% in 2025 per Volume IV). ~23m active users vs Klarna's ~119m; ~$255 average order value vs Klarna's ~$101; Amazon renewed to January 2031 (non-exclusive). **Why Affirm's take rate (~8.9%) is ~3x Klarna's (~2.7%):** Affirm is lend-centric — longer-duration, interest-bearing loans on big-ticket items where it captures interest (≈50% of revenue) and merchant-subsidised 0% APR; Klarna is spend-centric — short-duration, mostly interest-free Pay Later funded by merchant fees (interest only ~24% of revenue). The take-rate gap reflects *duration and product mix,* not pricing-power weakness: Klarna earns less per dollar but turns its book ~9x a year on ~one-ninth the capital.

**Block/Afterpay:** Afterpay is a pure short-duration Pay-in-4 network inside Block's two-sided Cash App/Square ecosystem — the closest structural analogue to Klarna's model and a genuine ecosystem threat given Block's own ILC (Square Financial Services).

**PayPal:** vast consumer wallet and merchant base; Pay in 4 is a feature not a business, but distribution reach makes it a persistent low-cost competitor.

**PSPs as distributor-competitors:** Stripe (1m+ businesses can enable Klarna instantly across 25 countries), Adyen (Klarna across ~450,000 terminals; Adyen also acts as an acquiring bank for Klarna). They distribute Klarna today and could disintermediate it tomorrow.

### V.8 Why Klarna Wins (mechanism decomposition)
- **Structural advantages:** (1) the **Swedish banking licence + deposit funding** — 91% deposit-funded, ~270-day average duration, materially cheaper and more stable than wholesale/forward-flow funding; (2) the **velocity of the book** — ~40-day average receivable duration, ~9x annual turns, ~1.0–1.3 US cents of CET1 per dollar of annual GMV; (3) the **two-sided network** of ~119m consumers and 1.07m merchants; (4) the **decision engine + proprietary repayment graph** built over 20 years and ~$0.5tn underwritten.
- **Management choices (contingent):** the originate-to-distribute pivot; the AI-first cost structure; product breadth (card, savings, Fair Financing).
- **Temporary advantages:** brand salience in mature markets (Sweden, Germany, UK); first-mover US scale ahead of the ILC.

### V.9 Moat Scorecard (RE-CUT — honestly asymmetric)
Scored 0–5.
- **Network effects — 4/5.** Mechanism: consumers attract merchants and vice versa; genuine and two-sided. Evidence: ~119m consumers, 1.07m merchants, higher checkout share when placed beside rivals (COMPANY CLAIM). Durability: high but not absolute (multi-homing by both sides). Weakens if: PSPs commoditise placement or a platform (Amazon/Shopify) internalises financing.
- **Decision engine & proprietary repayment data — 4/5.** Mechanism: 20 years / ~$0.5tn of repayment data enables real-time re-underwriting of a short book. Evidence: realised losses ~0.44–0.45% of GMV; fast Fair Financing learning curve. Replicability: low — path-dependent data. Weakens if: open-banking/bureau data commoditises underwriting.
- **Banking licence & deposit funding — 4/5.** Mechanism: cheap, sticky deposits fund originations at peer-level returns. Evidence: 91% deposit-funded, ~270-day duration, ~$12.3bn deposits. Durability: high in EU; US pending ILC. Weakens if: deposit competition raises cost or a run occurs.
- **Scale economies — 3/5.** Real operating leverage (revenue per employee ~$1.4m; opex down 8% since Q4 2022 while revenue +104%), but thin per-dollar margins cap the advantage.
- **Trust / brand — 3/5.** Strong in mature markets, weaker/contested in the US; the AML fine and consumer-harm debate cut against it.
- **Consumer switching costs — 2/5.** App, card and saved credentials create some stickiness, but consumers multi-home across BNPL apps freely.
- **Merchant switching costs — 2/5.** Once, integration was sticky; post-KCO divestiture, PSP intermediation lowers switching costs.
- **Regulatory capability — 3/5.** A licensed bank navigating CCD II/UK/US regimes is a barrier to sub-scale entrants — "more moat than cost" — but the AML fine shows the capability is not yet best-in-class.
- **Cost position — 3/5.** Deposit funding + AI cost base is a genuine relative cost edge versus non-bank BNPL.
- **Advertising / comparison assets — 2/5.** Retail media (~$180m in 2024) and the app are real but sub-scale; PriceRunner is entangled in litigation (Google antitrust case, judgment pending 2026).
- **Merchant integration estate — 1/5 (honestly low).** Per Volume III, increasingly a *rented distribution layer:* PSPs act as merchant of record for a substantial portion of merchant revenue. This is the weakest claimed moat and should not be scored as owned distribution.

**Survives testing:** network effects, repayment-data/decision engine, banking licence/deposit funding. **Does not survive:** merchant integration estate (rented), consumer/merchant switching costs (weak), brand outside mature markets.

### V.10 Replication Test
- **Banking licence / deposit base — difficult (buyable-with-friction).** A charter is obtainable (Affirm and PayPal are pursuing ILCs), but a $12bn+ low-cost deposit base at ~270-day duration is buildable-with-time, not off the shelf.
- **Repayment graph — effectively non-replicable / path-dependent.** 20 years and ~$0.5tn of labelled repayment outcomes cannot be bought.
- **Merchant estate — easy-ish to rent, hard to own.** Any funded entrant can rent PSP distribution — which is precisely why it is a weak moat for Klarna too.
- **Consumer base (~119m) — buildable-with-time but expensive;** Klarna paid for consumer acquisition partly in equity warrants ($233m fair value recognised in Q1 2025).
- **Decision engine — buildable-with-time,** but only as good as the data behind it.
- **Multi-market regulatory estate — difficult; path-dependent.**
- **Brand — buildable-with-time.**

Partial replication attempts: **Affirm** got furthest on US big-ticket lending but with a costlier funding model; **Afterpay** replicated the short-duration network inside Block; **Zip/Sezzle** replicated the product but stalled on scale and profitability; **Apple attempted and abandoned** the product entirely (June 2024) — the strongest evidence that owning BNPL is harder than it looks.

### V.11 Porter's Five Forces
- **Supplier power — HIGH and rising (the central force).** PSPs (Stripe/Adyen) and platforms (Shopify/Amazon) control merchant distribution and act as merchant of record; card networks (Visa/Mastercard) control rails and can embed instalments. This is Klarna's binding external dependency.
- **Buyer power (merchants) — MODERATE-HIGH.** Merchants pay roughly 3.29–5.99% + $0.30 and can drop or de-emphasise the product; conversion uplift is the retention mechanism, but PSP intermediation makes switching easier.
- **Rivalry — HIGH.** Consumer headline price is zero, so competition is on merchant fee, checkout placement and conversion; Affirm, Afterpay, PayPal, Zip and Sezzle all compete hard.
- **Substitutes — HIGH.** Revolving cards, debit, and network-embedded instalments (Visa/Mastercard) all substitute.
- **New entrants — MODERATE (asymmetric).** The banking-licence + data barrier deters sub-scale entrants, but well-capitalised platforms/networks can enter (though Apple's exit shows it is not trivial).

### V.12 PESTLE
- **Political/Regulatory (dominant):** EU **CCD II from 20 November 2026;** UK **Deferred Payment Credit regime, Regulation Day 15 July 2026** (FCA authorisation, affordability/creditworthiness checks, Consumer Duty, Ombudsman access; PS26/1 published 11 February 2026; TPR registration window from 15 May 2026); Australia from 10 June 2025; US CFPB interpretive rule **withdrawn 12 May 2025;** pending **US Utah ILC application (filed 6 July 2026** with the Utah DFI and FDIC to establish Klarna Bank USA, citing $91.3bn in credit extended to Americans since 2019) amid an active political fight over the ILC "loophole" (ICBA opposition; Kennedy/Kim and Warren moratorium proposals). Volume I's assessment — "more moat than cost" — holds for scaled incumbents, since compliance cost is a fixed barrier to sub-scale rivals.
- **Economic:** consumer-credit cycle sensitivity; policy rates drive the deposit spread (a tailwind while rates are elevated and deposits are cheap); retail-spend dependence.
- **Social:** contested consumer-attitude/vulnerability debate (present as unresolved — the distributional question cannot be settled from public data); generational shift toward interest-free instalments and away from revolving cards.
- **Technological:** AI (both cost lever and a source of over-claiming); open banking (could commoditise underwriting); stablecoins (KlarnaUSD, in testing, launch planned 2026); agentic commerce (Klarna's Agentic Product Protocol, December 2025; Visa/Mastercard/OpenAI agentic rails).

### V.13 Strategic Flywheels (genuine)
1. **Two-sided network** — more consumers → more merchants → more consumers. Evidenced by merchant/consumer counts and checkout-share claims.
2. **Cohort-frequency curve** — transactions per consumer rise from ~2 in year one to ~11+ by year three and up to ~18 for the oldest cohorts (COMPANY CLAIM, consistent across disclosures); card users transact ~3x more than non-card users.
3. **Data flywheel** — more transactions → better underwriting → more approvals at stable loss rates (~0.44–0.45%).
4. **Deposit→origination loop** — everyday spend feeds deposits; deposits fund originations at competitive cost ("everyday spend feeds the deposits, deposits fund the originations," CFO, Q1 2026).

### V.14 Negative Flywheels
1. **Regulatory ratchet** — each enforcement action (SEK 500m AML fine; data-protection reprimands) permanently raises the compliance cost base.
2. **Consumer-harm backlash** — feeds regulatory appetite (CCD II, UK DPC).
3. **PSP disintermediation** — Klarna becomes a commoditised credit utility behind Stripe/Adyen (the most dangerous loop).
4. **Credit→funding** — deterioration would raise funding cost and forward-flow pricing.
5. **Depressed share price → equity-retention erosion** — options struck at $91.80 and RSUs above the ~$20 price weaken staff retention and raise cash-comp pressure.

### V.15 The Strategic Bottleneck
**Current bottleneck: distribution control (PSP/platform dependency).** Even if credit, capital and product all improved by half, Klarna's value creation is capped by who controls the merchant relationship and checkout placement — because a substantial portion of merchant revenue flows through PSP merchants of record that can reprice, re-place or disintermediate. **Likely next bottleneck: merchant-fee pricing power** as CCD II/UK affordability rules and network-embedded instalments compress the fee that funds interest-free credit.

### V.16 Risk Register
| # | Risk | Prob | Severity | Detectability | Mitigation | Residual | Horizon |
|---|---|---|---|---|---|---|---|
|1|PSP/platform disintermediation|High|High|Med (channel opacity)|Own card/app, deposits, US ILC|High|1–4y|
|2|Merchant-fee compression|Med-High|High|High|Advertising, card interchange, value-add|Med-High|1–3y|
|3|Consumer-credit downturn|Med|Med-High|High|Short book, re-underwrite, distribute|Med|1–3y|
|4|CCD II / UK DPC tightening|High (certain)|Med|High|Bank-grade compliance, scale barrier|Med (net moat)|2026+|
|5|Further AML/data enforcement|Med|Med|Med|Strengthened controls, CFO|Med|Ongoing|
|6|US ILC application fails/delays|Med|Med|High|WebBank fallback|Med|1–2y|
|7|Deposit outflow/run|Low-Med|High|High|Deposit insurance, diversification|Med|Ongoing|
|8|Forward-flow renewal risk|Med|Med-High|Med|Multiple counterparties (Nelnet/Elliott/Santander/Värde)|Med|1–3y|
|9|Key-person (Siemiatkowski)|Med|High|Low|Deep C-suite, board|High|Ongoing|
|10|Depressed price / equity retention|High (present)|Med|High|Cash comp, new grants|Med-High|Now–2y|
|11|Earnings-quality perception|High|Med|High|Clearer disclosure|Med|Now–2y|
|12|Platform/network competitive entry|Med|High|Med|Network, data, licence|Med-High|2–5y|

### V.17 Stress Tests
- **Merchant fees −50bps:** given a ~2.7% take rate, a direct hit to transaction margin dollars; partly offset by advertising/interchange. Immediate: TMD compression; strategic: accelerates pivot to card/deposits/retail media.
- **Credit downturn doubling loss rates (~0.45%→~0.9% of GMV):** manageable given the short book and originate-to-distribute; provision timing hits reported profit first.
- **Loss of a major PSP channel (e.g., Stripe or Adyen):** severe — a "substantial portion" of merchant revenue is exposed; would validate the disintermediation thesis.
- **Affordability regulation reducing conversion:** lowers GMV growth and merchant ROI; raises churn risk.
- **Deposit run:** funding-cost spike; mitigated by insurance and duration but strategically damaging.
- **Forward-flow non-renewal:** would force loans back on balance sheet, consuming CET1 and slowing US growth.
- **Founder departure:** high narrative/strategic shock given key-person concentration.

### V.18 What Could Make Klarna Obsolete
- **Network-embedded card instalments (Visa/Mastercard) at every checkout:** commoditises the advantage; does not eliminate the customer problem; Klarna can partly adopt but loses differentiation.
- **Platform-native financing (Amazon/Shopify):** strands Klarna's merchant access on those platforms.
- **Regulation making short-term interest-free credit uneconomic:** would erode the core; Klarna's bank/deposit model is more resilient than non-bank peers.
- **Stablecoin/agentic rails bypassing checkout:** Klarna is trying to co-opt this (KlarnaUSD, Agentic Product Protocol) rather than be bypassed.
- **Generational shift away from credit:** slow, uncertain, partially hedged by debit/deposits.
- **Merchants concluding the fee is not worth the uplift:** the existential merchant-side risk; conversion evidence is the defence.

### V.19 Strategic Optionality
- **Retail media/advertising at scale — plausible adjacency** (~$180m in 2024; high-margin; sub-scale).
- **US ILC charter + US deposit-taking — natural adjacency** (filed July 2026; core to the strategy).
- **Card/interchange — natural adjacency** (5m+ card users; membership fees +~600% in the card segment).
- **Savings/wealth — plausible adjacency** (US Klarna Savings launched 2026).
- **KlarnaUSD stablecoin — stretch** (early, competitive, regulatory-dependent).
- **Agentic/AI shopping — plausible-to-stretch** (Agentic Product Protocol; Apple Upgrade leasing July 2026; JPMorgan Payments integration August 2026).
- **Further geographic expansion — natural adjacency but capital-intensive.**

### V.20 What Is Klarna Actually Becoming (central question — ranked hypotheses)
1. **A consumer bank with a shopping/commerce front end (most probable).** Evidence: 91% deposit funding, US ILC application, card/savings/membership growth, "everyday spend feeds deposits, deposits fund originations." Economics: deposit spread + capital-efficient short book. Management behaviour and capital allocation point here.
2. **A two-sided commerce network with a balance sheet (close second, complementary).** The network is genuine; the two hypotheses are not mutually exclusive — the bank monetises the network.
3. **A capital-light originate-to-distribute credit platform (partly true now).** Nelnet/Elliott/Santander/Värde show this operationally, but it is a *funding tactic* within (1), not the end-state.
4. **A commoditised credit utility behind the PSPs (the bear case; real and rising).** Supported by the merchant-of-record dependency; this is what happens if disintermediation wins.
5. **A retail-media business monetising purchase intent (aspirational, sub-scale).**
6. **A diversified everyday-spending super-app (marketing framing, least supported).**

**Verdict:** Klarna is most credibly *becoming a deposit-funded consumer bank that sits on top of a genuine two-sided network* — hypothesis (1)+(2). The decisive contest is between that outcome and hypothesis (4).

### V.21 Five- and Ten-Year Strategic Map
- **Base case:** GMV compounds ~20–30%/yr toward and beyond the ~$155bn 2026 guide; revenue mix tilts toward interest income (Fair Financing/card) and membership/advertising; margins inflect positive (management guides EPS positive by ~FY2027); moat = deposits + data + network.
- **Strong execution:** US ILC granted, deposits scale in the US, card becomes the daily-spend hub, retail media scales — a genuine digital bank re-rates the multiple.
- **Margin compression:** CCD II/UK affordability + fee compression cap TMD; growth continues but profitability lags.
- **Regulatory shock:** harsher affordability/interest-cap rules shrink the interest-free model; bank/deposit resilience limits damage relative to non-bank peers.
- **Disintermediation:** PSP/platform capture pushes Klarna toward a commoditised credit-utility role; take rate and margin erode.
- **Strategic transformation:** agentic/stablecoin rails and AI shopping reposition Klarna as commerce infrastructure — high variance, unproven.

### V.22 What the Market May Misunderstand
1. **"Klarna is a BNPL company" — reality: it is a licensed bank** whose economics run on deposits and a short, high-velocity book. Persists because the US knows it only as BNPL. Implication: mis-comped against non-bank BNPL.
2. **The capital efficiency of the short book (~1.0–1.3¢ CET1 per GMV dollar, ~9x turns) is under-priced.** Persists because reported IFRS losses dominate headlines. Implication: the equity may be cheap on a normalised-returns basis.
3. **"Adjusted operating profit is the economic result" — it is not** ($65m excludes $157m SBC; IFRS net loss $(273)m). Implication: don't capitalise the adjusted number.
4. **"Rising provisions = deteriorating credit" — false;** the charge is IFRS 9 timing on growth and US Fair Financing mix, with realised losses stable at ~0.44–0.45%. Implication: provision growth is a growth signal, not a credit-quality signal.
5. **"The merchant relationship is owned" — it is increasingly rented** through PSP merchants of record. Implication: distribution risk is under-appreciated; this cuts the *other* way from #1–2 (a genuine negative the market may under-price).
6. **"Regulation is a threat" — for scaled Klarna it is largely a moat,** raising fixed compliance costs that deter sub-scale entrants — though the AML fine shows the capability is not yet best-in-class.

### V.23 Management & Capital-Allocation Judgement
- **2017 banking licence — value creating** (the source of the deposit moat).
- **International expansion / US entry — strategically necessary but expensive** (drove the 2022 losses and down round; now the growth engine).
- **Acquisition programme + Klarna Checkout divestiture — mixed/questionable.** KCO divestiture removed PSP friction and added merchants fast, but *created* the rented-distribution dependency — a defensible trade with a dangerous long-tail. PriceRunner acquisition is entangled in litigation.
- **2022 down round ($6.7bn from $45.6bn) — strategically necessary;** imposed cost discipline that made the IPO possible.
- **AI/headcount transformation — value creating operationally, credibility-damaging in communication.**
- **Originate-to-distribute pivot — value creating for growth, quality-degrading for earnings.**
- **Redomiciliation + largely secondary listing — questionable for the company** (only ~$169m net reached Klarna), value-realising for selling holders.
- **Pending US ILC — strategically necessary, too early to judge.**

### V.24 Volume V Reconstruction
**Ten most important conclusions:**
1. Klarna is a bank, not a BNPL lender; its moat is deposits + data + network.
2. The network effect is genuine and asymmetric-high; the merchant estate is genuinely weak (rented).
3. Management is promotional-then-corrected; discount narrative, trust audited numbers, weight regulators.
4. Adjusted operating profit is not the economic result; IFRS shows losses turning to a marginal Q1 2026 profit ($1m net income).
5. The take-rate gap to Affirm reflects model design (spend- vs lend-centric), not weakness.
6. Capital efficiency of the short book is the most under-priced fact.
7. PSP disintermediation is the single greatest structural risk and the binding bottleneck.
8. Originate-to-distribute funds growth but degrades earnings quality.
9. Regulation is net moat for scaled Klarna, net cost for sub-scale rivals.
10. Founder control (multi-class, out-of-money Class C options) is a priceable governance fact, not misconduct.

**Answers to the set questions:**
- **Why Klarna wins today:** cheap sticky deposits + a capital-light, fast-turning book + a genuine two-sided network + 20 years of repayment data.
- **Strongest moat component:** the repayment-data/decision engine married to deposit funding. **Most overrated:** the merchant integration estate (rented).
- **Hardest to replicate:** the repayment graph. **Easiest:** the merchant estate (rentable by anyone).
- **Current bottleneck:** distribution control (PSP/platform dependency). **Next:** merchant-fee pricing power.
- **Greatest structural risk:** PSP/platform disintermediation.
- **Most dangerous competitor/substitute:** not Affirm — the PSPs (Stripe/Adyen) and, secondarily, network-embedded card instalments.
- **What could make it obsolete:** platform-native or network-embedded financing that captures the checkout, combined with regulation that makes interest-free credit uneconomic.
- **Central question:** On balance, Klarna is **building a durable, deposit-funded two-sided commerce network that owns a bank — but it is doing so while renting its merchant distribution, which exposes it to slow commoditisation into a credit utility behind the PSPs.** The durable-bank thesis is currently ahead, but not decisively. The market's ~$7.5bn valuation appears to over-weight the loss-making-fintech framing and the disintermediation risk while under-weighting the deposit moat and capital efficiency — meaning the quote is probably too pessimistic on the structural bank, and roughly right on the strategic vulnerability. The right answer is not yet fully in the price.

## Recommendations
- **For an investor:** treat KLAR as an option on the bank-thesis winning over the utility-thesis. Stage entry against three benchmarks: (1) evidence that direct/owned merchant revenue is growing faster than PSP-intermediated revenue (disintermediation abating); (2) US ILC approval and US deposit growth; (3) sustained IFRS (not adjusted) profitability with SBC added back. Failure on (1) is the thesis-breaker.
- **For an analyst:** rebuild the model on IFRS with SBC included; value the book on normalised return-on-CET1 given ~9x turns, not on headline losses; track take rate, TMD/GMV, deposit cost and the direct-vs-PSP revenue split as the key tells.
- **For a competitor/partner:** the replicable weakness is distribution (rentable); the non-replicable strength is the repayment graph — compete on the former, not the latter.
- **Thresholds that change the call:** a lost major PSP channel or accelerating PSP revenue share → downgrade toward the utility thesis; ILC approval + rising owned-merchant mix + IFRS profitability → upgrade toward the durable-bank thesis.

## Caveats
- Every strategic, cultural, productivity and "profitability" statement from management is treated as COMPANY CLAIM; where it could not be independently corroborated (e.g., checkout-share superiority, exact PSP revenue share, the cohort-frequency curve), it is labelled as such.
- The exact "$35 billion" CEO-incentive figure is a reported maximum theoretical value tied to an extreme valuation outcome; the audited, granted award is the Class C option package (17,505,672 options at ~$91.80), which is what should be priced.
- The consumer-harm/distributional debate is genuinely unresolved and cannot be settled from public data; it is presented as contested, not decided.
- Board-independence classification and the precise count of independent directors could not be fully confirmed from public sources at the time of writing and remain partly UNKNOWN.
- Stock prices and Q1 2026 figures are as reported through mid-2026; the US ILC application (filed 6 July 2026) is pending and its outcome is UNKNOWN. The subagent research budget errored out and could not supplement the governance section; conclusions there rest on the primary filings and reputable journalism gathered directly.

---

# PART VI — CROSS-VOLUME SYNTHESIS

*The five volumes take the enterprise apart. This part reassembles it as one system, and states what the parts together mean that no part means alone.*

## VI.1 The enterprise in one paragraph

Klarna Group plc is a UK-listed holding company that does nothing. Beneath it sits Klarna Bank AB, a Swedish credit institution licensed since June 2017, which takes roughly thirteen billion dollars of insured retail deposits — largely from German and Swedish savers who have never used the shopping product — and lends them, forty days at a time, to consumers at the checkouts of around a million merchants. The consumer usually pays nothing. The merchant pays three to six per cent of the order value, because deferred payment demonstrably increases conversion and basket size. The receivable is extinguished in about forty days and the capital recycles roughly nine times a year. In the United States, where Klarna holds no charter, a Utah industrial bank originates the loan and Klarna buys it back. Increasingly, Klarna does not keep the loan at all — it sells it to Nelnet, Elliott and Värde. **The business is a machine for converting merchant conversion-anxiety into a deposit-funded, hyper-velocity credit book, and its central vulnerability is that it no longer owns the door through which it reaches the merchant.**

## VI.2 The five findings that only appear when the volumes are read together

**One. Klarna is a bank that everyone mistakes for an app.** Volume I established the licence; Volume IV established that ninety per cent of funding is deposits; Volume V established that this is the largest structural difference from every non-bank competitor. Affirm funds itself in wholesale markets at around seven per cent; Klarna funds itself with insured deposits at a fraction of that. **The most consequential fact about this company is a Swedish banking licence granted in 2017, and it is the fact least present in how the company is discussed.**

**Two. Velocity is the whole economic argument.** Volume II found the receivable lasts about forty days. Volume IV converted that into the number that matters: **a dollar of annual gross merchandise volume consumes roughly one to one and a third US cents of core equity capital — about one-ninth of what a revolving card lender needs.** Klarna runs roughly three times Affirm's volume for similar revenue on a fraction of the capital. This is the study's quantitative payoff and, on Volume V's assessment, the thing the market has not priced.

**Three. The low take rate is a design choice, not a weakness.** Klarna earns about 2.74 per cent of volume against Affirm's roughly 8.9 per cent. Read naively, that looks like Klarna is worse at pricing. Read correctly, it reflects two different businesses: Affirm is **lend-centric**, earning interest on long-duration big-ticket loans; Klarna is **spend-centric**, earning merchant fees on short-duration everyday baskets. Neither number can be compared without the duration behind it.

**Four. The merchant relationship is rented, not owned.** Volume III's most uncomfortable finding, followed to its conclusion in Volume V. After the 2024 divestiture of Klarna Checkout, a substantial portion of merchant revenue arrives through payment service providers — Stripe and Adyen — acting as merchant of record. Klarna scaled distribution brilliantly and, in doing so, **placed an intermediary between itself and the customer who actually pays it.** This is the binding strategic constraint.

**Five. The company's own account of itself requires correction, but its numbers do not.** Volume III dismantled the artificial-intelligence substitution story; Volume IV showed the adjusted profit measure excludes a hundred and fifty-seven million dollars of real equity pay; Volume V reached the settled position. **The audited financials have been reliable. The interpretations layered on top have not.** That is a priceable governance fact, and it is different in kind from the anti-money-laundering findings, which were a genuine control failure adjudicated by a regulator rather than a matter of emphasis.

## VI.3 The system diagram, in words

Deposits enter from German and Swedish savers, insured by the Swedish scheme and costing well under three per cent. They fund a book of consumer receivables averaging forty days. A consumer selects Klarna at a checkout; the decision engine reads a feature store updated in real time by transaction events, scores default probability, applies policy rules, and answers in under a second. The merchant is paid immediately, less a fee of three to six per cent. The consumer pays in thirty days, or four instalments, or — increasingly — over six to thirty-six months with interest. Losses run at about 0.45 per cent of volume. The receivable is repaid or sold; either way the capital returns and is lent again, nine times a year. Every repayment feeds the graph that trains the engine. **The flywheel is not network effects in the ordinary sense — it is a data flywheel wrapped inside a two-sided network, funded by a bank.**

## VI.4 Where the machine can break

Ranked by the study's assessment of severity times probability:

1. **Payment-service-provider disintermediation** — the merchant of record sits between Klarna and its paying customer, and can reprice, re-place or replace it.
2. **Merchant-fee compression** — the take rate is 2.74 per cent and the transaction margin about one cent per dollar of volume; there is almost no buffer.
3. **A credit downturn coinciding with fee pressure** — thin margins absorb one shock, not two.
4. **Regulatory tightening** — the Consumer Credit Directive II from November 2026 and the UK regime from July 2026 impose affordability checks that reduce conversion, though on Volume I's assessment they are net moat for a scaled licensed bank.
5. **Network-embedded instalments from Visa and Mastercard**, or platform-native financing from Amazon or Shopify, commoditising the product at the rail or platform layer.

## VI.5 The verdict

Klarna is, on the weight of the evidence, **a genuine deposit-funded consumer bank sitting on top of a real two-sided commerce network — and it is simultaneously being pushed toward a commoditised credit-utility role behind the payment processors that distribute it.** Both are true. The durable-bank thesis is currently ahead, but not decisively, and the contest will be settled by whether owned merchant distribution grows faster than intermediated distribution.

On the market's view: the quote appears to **over-weight the loss-making-fintech framing and under-weight the deposit moat and the capital efficiency**, while pricing the disintermediation risk about right. The market is probably too pessimistic about the bank and roughly correct about the strategic vulnerability.

The one thing that can be said without hedging is this. **The interest-free credit is not free.** The merchant pays for it, and the merchant recovers it in the price of goods — which means it is paid by every customer of that merchant, including those who never use Klarna and those who pay cash. Whether that is a better arrangement than the revolving credit it displaces depends on a distributional question — what share of consumer-fee revenue comes from what share of users — that **cannot be answered from public data**. Volume II identified that gap; no regulator has yet closed it; and until one does, the consumer-harm debate will remain genuinely unresolved rather than settled in either direction.

---

# APPENDIX A — GLOSSARY

*This study spans banking regulation, consumer-credit law, credit-risk accounting and payments. Read this before Volume IV.*

## A.1 The products

| Term | Meaning |
|---|---|
| **Buy now, pay later (BNPL)** | Short-term deferred payment at the point of sale, usually interest-free to the consumer and funded by a merchant fee |
| **Pay in 30 / invoice** | Klarna's original 2005 product: goods first, payment within thirty days, interest-free |
| **Pay in 3 / Pay in 4** | The purchase split into three or four interest-free instalments |
| **Fair Financing** | Klarna's longer-term instalment credit, six to thirty-six months, **interest-bearing** — the product where the consumer, not the merchant, is the principal payer |
| **Klarna Balance** | The deposit account launched August 2024 |
| **Merchant discount rate** | The fee a merchant pays per transaction — for Klarna roughly 3.29% to 5.99% plus a fixed amount, against an EU consumer-card interchange cap of **0.3%** |
| **Gross merchandise volume (GMV)** | The total value of transactions processed. **The denominator that matters for this business** |
| **Take rate** | Revenue divided by GMV. Klarna approximately 2.74%; Affirm approximately 8.9% — a difference of business model, not pricing power |

## A.2 Banking and prudential regulation

| Term | Meaning |
|---|---|
| **Credit institution** | The EU legal term for a bank — an entity authorised to take deposits from the public and grant credit |
| **Finansinspektionen (FI)** | The Swedish Financial Supervisory Authority; Klarna Bank AB's home-state prudential and conduct supervisor, and its anti-money-laundering supervisor |
| **CRR / CRD** | The Capital Requirements Regulation and Directive — the EU implementation of Basel, governing bank capital |
| **CET1** | Common Equity Tier 1 — the highest-quality regulatory capital, essentially common shares and retained earnings |
| **Additional Tier 1 (AT1)** | Perpetual subordinated instruments that count as regulatory capital and **sit in equity under IFRS but are not common equity** — a standard trap when reading a bank balance sheet |
| **Risk exposure amount (REA) / RWA** | Assets weighted by risk; the denominator of a capital ratio |
| **Standardised approach** | The prescribed regulatory formula for risk weights — for retail exposures, a flat **75%**. Klarna uses this rather than internal models |
| **Internal ratings-based (IRB)** | Permission to use a bank's own models to set risk weights; generally produces lower weights for a well-performing book. **Klarna does not have it** |
| **Pillar 2 requirement (P2R) / Pillar 2 guidance (P2G)** | Supervisor-specific capital add-ons above the standard minimum |
| **Leverage ratio** | Tier 1 capital over total exposure, unweighted by risk; a backstop to the risk-weighted ratios |
| **Liquidity coverage ratio (LCR)** | High-quality liquid assets against thirty days of stressed outflows |
| **Passporting** | The right of an EEA-authorised bank to operate across the EEA on its home licence, via branches or cross-border services |
| **Deposit guarantee scheme** | Statutory insurance of retail deposits — in Sweden administered by Riksgälden, up to approximately SEK 1,050,000 (the EU-harmonised €100,000) |
| **Industrial loan company (ILC)** | A Utah-chartered, FDIC-insured bank that may be owned by a commercial parent without Federal Reserve holding-company supervision. **WebBank is one; Klarna applied to establish another in July 2026** |

## A.3 Credit risk and accounting

| Term | Meaning |
|---|---|
| **IFRS 9** | The accounting standard governing financial instruments, including **expected credit loss** provisioning |
| **Expected credit loss (ECL)** | Provisions booked when a loan is made, based on expected future losses, rather than when losses occur. **The reason a fast-growing lender reports losses that a stable one would not** |
| **Staging** | IFRS 9's three-stage model: performing, significantly deteriorated, and credit-impaired |
| **Coverage ratio** | Loss allowance as a percentage of gross receivables |
| **Realised loss** | Losses actually incurred, as distinct from provisions taken in anticipation |
| **Duration** | How long a receivable remains outstanding. **Klarna's average is about forty days; a revolving card balance persists for roughly a year** |
| **Book velocity / turnover** | How many times a year the loan book recycles. Klarna approximately nine times |
| **Lender of record** | The entity legally making the loan — Klarna Bank AB in the EEA, **WebBank in the United States** |
| **Forward flow** | An agreement to sell newly originated receivables to an investor on a rolling basis |
| **Significant risk transfer (SRT)** | A structure transferring credit risk to investors so the originator may reduce regulatory capital |
| **Originate to distribute** | Making loans in order to sell them rather than hold them |
| **Gain on sale** | The accounting profit recognised when a receivable is sold above carrying value; **lumpy, timing-dependent, and a recurring earnings-quality question** |
| **Warehouse facility** | A secured credit line financing receivables pending sale or securitisation |

## A.4 Distribution and regulation of conduct

| Term | Meaning |
|---|---|
| **Payment service provider (PSP)** | A processor connecting merchants to payment methods — Stripe, Adyen, Worldpay |
| **Merchant of record** | The entity legally responsible for a transaction with the consumer. **Where a PSP is merchant of record, Klarna's relationship is with the PSP, not the retailer** |
| **Consumer Credit Directive II (CCD II)** | Directive (EU) 2023/2225, bringing BNPL within EU consumer-credit regulation; applies from **20 November 2026** |
| **Deferred Payment Credit (DPC)** | The UK regulatory term for BNPL; regulated from **15 July 2026** |
| **Woolard Review** | The February 2021 FCA-commissioned review that recommended bringing BNPL into UK regulation |
| **Affordability assessment** | The requirement to check a borrower can repay — the central new obligation under both the EU and UK regimes, and the mechanism by which regulation reduces conversion |
| **Open banking** | Consumer-permissioned access to bank account data, used by Klarna in underwriting where bureau data is thin |

---

# APPENDIX B — CANONICAL FIGURES REGISTER

**Where any volume disagrees with this table, this table governs.** Entity, currency and framework stated on every figure. Compiled 11 August 2026.

## B.1 Group results — Klarna Group plc, USD, IFRS as issued by the IASB

| USD m | FY2023 | FY2024 | FY2025 |
|---|---|---|---|
| Total revenue | 2,276 | 2,811 | **3,509** |
| — Transaction & service | 1,768 | 2,136 | 2,500 |
| — Interest income | 508 | 675 | 937 |
| — Gain on sale of receivables | — | — | 73 |
| Processing & servicing | (541) | (596) | (809) |
| Provision for credit losses | (353) | (495) | (794) |
| Funding costs | (297) | (503) | (667) |
| **Operating profit / (loss), IFRS** | (323) | **(121)** | **(230)** |
| Adjusted operating profit (non-IFRS) | — | 181 | **65** |
| **Net profit / (loss), total group** | (244) | **21** | **(273)** |
| — attributable to shareholders | (249) | 3 | **(294)** |
| Basic and diluted EPS (USD) | (0.69) | 0.01 | **(0.79)** |
| Share-based payments | — | — | **157** |
| GMV (USD bn) | 92 | 105 | **127.9** |
| Take rate | ~2.5% | ~2.66% | **2.74%** |

**On the two net-loss figures.** The total group net loss for FY2025 is **$(273)m**; the loss **attributable to shareholders** is **$(294)m**. The $21m difference is non-controlling interests. *See Appendix D, note 1 — one volume conflates these.*

**Quarterly FY2025 net result:** Q1 $(99)m, Q2 $(53)m, Q3 $(95)m, Q4 $(26)m. Revenue: Q1 $701m, Q2 $823m, Q3 $903m, Q4 $1,082m. **Q1 2026 returned a $1m net profit on $1.0bn of revenue.**

## B.2 Operating metrics — by date, because they move fast

| Date | Active consumers | Merchants | Note |
|---|---|---|---|
| 30 June 2025 | ~111 million | ~790,000 | Prospectus figure, 26 countries, $112bn LTM GMV |
| 31 December 2025 | **118 million** | **966,000** | FY2025 results |
| Q1 2026 | ~119 million | ~1.07 million | Most recent |

All three are correct at their dates; they are a vintage series, not a conflict. Merchant count is measured as unique brand-by-market combinations.

## B.3 The book, credit and capital

| Item | Value | Basis |
|---|---|---|
| Average receivable duration | **~40 days**; 84–85% of loans ≤3 months | Company disclosure |
| Book turnover | **~9× a year** | Derived, 365 ÷ 40 |
| Average balance per active consumer | **$80** (Pay Later $88; Fair Financing $408) | vs ~$6,730 for a US credit card |
| Consumer credit losses | **0.47% of GMV (2024)**; realised **0.44–0.45% (2025)** | Group, IFRS |
| Provisions | 0.55–0.72% of GMV by quarter (2025) | Group, IFRS |
| Delinquency | BNPL 0.88–0.89%; Fair Financing 2.18–2.23% | Group |
| Coverage, 31 Dec 2025 | Total **4.5%** (Pay Later 3.5%, Fair Financing 5.9%) | Group, IFRS |
| **CET1 per $1 of annual GMV** | **~1.0–1.3 US cents** | ANALYTICAL INFERENCE, Volume IV |
| REA per $1 of annual GMV | ~8 US cents | ANALYTICAL INFERENCE |

**Prudential capital — Klarna Holding AB Consolidated, SEK, Pillar 3.** *Capital ratios exist only on this basis.*

| | 31 Dec 2024 | 31 Dec 2025 |
|---|---|---|
| CET1 capital (SEK m) | 12,970 | 14,574 |
| Total risk exposure amount (SEK m) | 77,022 | 92,654 |
| **CET1 ratio** | **16.8%** | **15.7%** |
| Tier 1 ratio | 19.0% | 17.5% |
| Total capital ratio | 21.4% | 19.4% |
| Leverage ratio | 9.9% | 9.4% |
| LCR | 853% | 1,013% |
| NSFR | 178.7% | 192.6% |

Requirement stack (2024): Pillar 1 8.0% + P2R 1.2% = SREP 9.2%; combined buffer 3.5%; overall requirement 12.6%; **P2G raised to 5.0% of REA from September 2025**. Credit risk uses the **standardised approach** (75% retail risk weight) and is roughly 83–84% of REA.

## B.4 Funding

| Item | Value | Basis |
|---|---|---|
| Deposit share of funding | **~90–91%** | Group |
| Consumer deposits, **31 December 2025** | **$13,003m** | Klarna Group plc balance sheet, audited — *the governing figure* |
| Deposits, September 2025 | ~$14bn | Company statement, a different date |
| Deposits, December 2024 | ~$9.5bn | |
| Average deposit duration | ~270 days | |
| Santander warehouse | up to **€1.4bn** | August 2025, German receivables |
| Nelnet forward flow | up to **$26bn** of Pay-in-4 | August 2025; Nelnet assumes credit risk |
| Elliott | **$2bn** facility supporting up to **$17bn** of US Financing | March 2026, three-year |
| Värde-led SRT | **$1.7bn** | April 2026, euro-denominated, three-year |
| Combined lending capacity | **>$40bn** | |

## B.5 Corporate and regulatory

| Item | Value |
|---|---|
| Founded | **1 July 2005**, Stockholm, as **Kreditor Europe AB**, by Siemiatkowski, Adalberth and Jacobsson — *see Appendix D note 4 on the three "Kreditor" entities* |
| Banking licence | Granted by Finansinspektionen **19 June 2017** |
| Licensed bank | **Klarna Bank AB (publ)**, corp. ID 556737-0431 |
| Listed parent | **Klarna Group plc**, England and Wales, CRN 14467769 |
| IPO | Priced **9 September 2025 at $40.00**; overwhelmingly secondary; **net proceeds to the company ~$169m** |
| Share structure | Ordinary (1 vote); Class B (10 votes, no economics); Class C (10 votes, half dividend, CEO only, capped at 15% of pre-IPO voting) |
| CEO incentive granted | **17,505,672 Class C options**, 5 March 2025, weighted-average exercise ~**$91.80** — *see Appendix D note 5 on the "$35 billion" figure* |
| FI sanction | **Remark + SEK 500m** (~$45–46m), **11 December 2024**, AML deficiencies |
| Data protection | SEK 7.5m (IMY, 2022; reinstated on appeal March 2024); reprimand March 2025 |
| US arrangement | **WebBank** originates; Klarna Inc. purchases. ILC application for **Klarna Bank USA** filed **6 July 2026** |
| Regulatory perimeter | CCD II applies **20 Nov 2026**; UK DPC regulation day **15 July 2026**; Australia **10 June 2025**; US CFPB interpretive rule **withdrawn 12 May 2025** |

## B.6 Acquisitions and disposals

| Target | Date | Consideration | Purpose |
|---|---|---|---|
| Sofort GmbH | agreed Dec 2013, closed Mar 2014 | ~$150m | German scale, open-banking rails |
| BillPay | Feb 2017 | undisclosed | German merchants |
| Close Brothers Retail Finance | announced Sept 2018 | undisclosed | UK retail finance |
| Stocard | July 2021 | ~€110m | Loyalty wallet, ~60m users |
| PriceRunner | completed 4 April 2022 | undisclosed (reported ~$1bn) | Comparison shopping |
| **Klarna Checkout — DIVESTED** | October 2024 | reported ~£407m; **$190m net gain** | Removed PSP conflict; **created the rented-distribution dependency** |

---

# APPENDIX C — THE THREE REPORTING ENTITIES

*The basis-discipline guide. More errors are made reading Klarna's numbers than any previous subject in this programme, because three different entities publish three different sets of figures in two currencies under two frameworks. Read this before any financial section.*

## C.1 The three entities

**1. Klarna Group plc — the listed group.**
England and Wales, CRN 14467769, incorporated 7 November 2022 as Klarna UK II PLC and renamed 13 December 2023. Became the ultimate parent by share-for-share exchange in May 2024. Listed on the NYSE as KLAR since 10 September 2025. **Reports in US dollars under IFRS as issued by the IASB**, 31 December year end, on **Form 20-F** as a foreign private issuer with reduced disclosure. Auditor: Ernst & Young AB. No IFRS-to-US-GAAP reconciliation is prepared.

*This is where revenue, GMV, net income, EPS and the consolidated balance sheet come from.*

**2. Klarna Bank AB (publ) — the licensed bank.**
Sweden, corp. ID 556737-0431, Sveavägen 46, Stockholm. Holds the Finansinspektionen banking licence granted 19 June 2017. Takes deposits, originates and holds EEA credit, and passports across the EEA. **Reports in Swedish krona under IFRS as adopted by the EU plus the Swedish Annual Accounts Act.**

*This is where the statutory Swedish accounts, IFRS 9 staging detail, and deposit and lending detail come from.*

**3. Klarna Holding AB Consolidated — the prudential consolidation.**
Sweden, corp. ID 556676-2356. The "consolidated situation" for CRR/CRD purposes. **Reports in Swedish krona on the Pillar 3 basis.**

***This is the only basis on which capital ratios exist.*** Any CET1, Tier 1, total capital, leverage, LCR or NSFR figure comes from here and from nowhere else.

## C.2 Why the three do not reconcile simply

Four reasons the prudential consolidation differs from the listed group:

1. **A different parent.** The prudential parent is Klarna Holding AB in Sweden, not Klarna Group plc in the UK.
2. **Intangibles are deducted from CET1.** The goodwill and intangibles from Sofort, Close Brothers Retail Finance, Stocard and PriceRunner appear as assets in the group accounts but reduce regulatory capital.
3. **Subsidiary-issued capital is only partly included.** Additional Tier 1 and Tier 2 instruments issued by subsidiaries count only up to the share needed to cover the bank's own minimum, under CRR Articles 85 and 87.
4. **Currency.** SEK against USD, with translation at period-end rates.

This is why prudential deposits from the public (approximately SEK 121.8bn) do not equal the group's consumer-deposit line ($13,003m) once converted: scope and translation both differ.

## C.3 The four rules for reading Klarna's numbers

**Rule one. Capital ratios come only from Klarna Holding AB Consolidated.** If a CET1 figure is presented alongside a USD revenue figure without a note, one of them is being misused.

**Rule two. Never mix IFRS and adjusted measures in a comparison.** Adjusted operating profit for FY2025 was $65m; the IFRS operating loss was $(230)m. The bridge is: operating loss $(230)m + depreciation, amortisation and impairment $55m + share-based payments $157m + restructuring and IPO costs ~$83m = $65m. **The largest single item is share-based pay, which is a real economic cost.**

**Rule three. Distinguish the total net loss from the attributable net loss.** FY2025: total $(273)m; attributable to shareholders $(294)m; the difference is non-controlling interests.

**Rule four. Date every operating metric.** Consumers and merchants grew from 111 million and 790,000 at 30 June 2025, to 118 million and 966,000 at 31 December 2025, to roughly 119 million and 1.07 million in Q1 2026. Comparing figures from different quarters without noting the date produces false growth or false stagnation.

## C.4 A worked example of the trap

A reader wishing to compute return on equity might take the group's total equity of $2,684m and the attributable net loss of $(294)m and conclude a return of about negative eleven per cent. That computation is wrong in three ways at once: it uses the attributable rather than the total result against total equity; it includes Additional Tier 1 instruments in the denominator, which sit in equity under IFRS but are not common equity; and it treats a bank in a hyper-growth phase, whose IFRS 9 provisions are front-loaded against interest income that accrues later, as though its reported result were its through-cycle earning power. **All three errors push in the same direction, and together they make a capital-efficient lender look like a failing one.**

---

# APPENDIX D — SOURCE REGISTER AND RECONCILIATION

## D.1 Sources relied upon

**Primary corporate filings.** The Klarna Group plc **Form F-1** registration statement and amendments and the **424B4** prospectus (2025); **Form 20-F** and **Form 6-K** filings; quarterly and full-year earnings releases and investor presentations with their non-IFRS reconciliations; and the announcement of the IPO pricing.

**Banking and prudential records.** **Klarna Bank AB (publ)** annual and interim reports (statutory Swedish accounts, SEK); **Klarna Holding AB Consolidated** annual reports and **Pillar 3 Risk Management and Capital Adequacy** reports for 2024 and 2025; Swedish Companies Registration Office (Bolagsverket) entity data.

**Supervisory and enforcement records.** The **Finansinspektionen decision of 11 December 2024** (dnr 22-11505) imposing a remark and a SEK 500m administrative fine for anti-money-laundering deficiencies — read throughout as an operational document rather than merely a penalty; **Integritetsskyddsmyndigheten** decisions of March 2022 and March 2025 and the Stockholm administrative court judgments on appeal; the **FCA Register** and UK Companies House.

**Regulatory instruments.** **Directive (EU) 2023/2225** (Consumer Credit Directive II); the UK **Financial Services and Markets Act 2000 (Regulated Activities etc.) (Amendment) Order 2025** and FCA **Policy Statement PS26/1** (11 February 2026); the **Woolard Review** (February 2021); the CFPB interpretive rule (89 FR 47068) and its withdrawal on 12 May 2025; the Australian **Treasury Laws Amendment (Responsible Buy Now Pay Later and Other Measures) Act 2024** and ASIC Regulatory Guide 281; the **EU AI Act** (Regulation (EU) 2024/1689) Annex III treatment of creditworthiness assessment; the EU **Interchange Fee Regulation** (Regulation (EU) 2015/751).

**Funding and corporate announcements.** The Nelnet forward-flow announcement (August 2025); the Elliott facility announcements (November 2025 and March 2026); the Värde-led significant risk transfer (April 2026); the Santander structured financing facility (August 2025); the Utah industrial-bank charter application (July 2026).

**Academic and independent research.** Di Maggio, Williams and Katz on BNPL and consumer spending; Maesen and Ang (2025) on purchase incidence; deHaan and others, "Buy Now, Pay (Pain?) Later," *Management Science* (2024); Central Bank of Ireland experimental work (2025); CFPB, "Consumer Use of Buy Now, Pay Later and Other Unsecured Debt" (January 2025).

**Competitor filings.** Affirm, Block (including Afterpay), PayPal, Zip and Sezzle, used for the comparison matrices in Volume V, with definitions of GMV, take rate and loss rate normalised where possible.

**Treated as promotional and tested.** Klarna's engineering publications, artificial-intelligence announcements including the joint OpenAI release of 27 February 2024, investor-day materials, Wikipink self-reported statistics, and all management statements about strategy, culture, productivity and profitability.

## D.2 Reconciliation of cross-volume discrepancies

Five volumes were commissioned sequentially against a moving evidence base. Six discrepancies were identified on assembly: **one is a genuine error**, three are basis or vintage differences, one is a genuine reconciliation that resolves a confusion in the wider commentary, and one is unresolved.

### Genuine error

**Note 1 — the FY2025 net loss. CORRECTED.** Volume II states "a net loss of $294.0m." That is the loss **attributable to shareholders**, not the total group result. Volume IV establishes the correct decomposition, verified on assembly: **total group net loss $(273)m; attributable to shareholders $(294)m; difference $21m of non-controlling interests.** Volume IV governs. The error does not affect Volume II's analysis, which concerns take rate and velocity rather than the loss decomposition, but the figure as stated is wrong and Appendix B records the correct pair.

### Basis and vintage differences — not errors

**Note 2 — consumer deposits.** Four figures appear: approximately $9.5bn (December 2024), approximately $14bn (September 2025), **$13,003m (31 December 2025)** and approximately $12.3bn (Volume V). The first three are the same series at different dates, and **the audited balance-sheet figure at 31 December 2025 — $13,003m — governs** for any balance-sheet purpose. Volume V's approximately $12.3bn is unreconciled to a stated date and should not be used; it may reflect a different scope or an intermediate period. Appendix B records the dated series.

**Note 3 — operating metrics across dates.** Consumers and merchants are reported as 111 million and 790,000 (30 June 2025, prospectus), 118 million and 966,000 (31 December 2025, FY results), and approximately 119 million and 1.07 million (Q1 2026). **These are not in conflict; they are a vintage series**, and Appendix B.2 presents them as such. The same applies to the take rate, reported variously as 2.7%, 2.74% and 2.75%: the precise computation is $3,509m ÷ $127,900m = **2.744%**, and the other figures are roundings of it. Similarly, deposit funding is stated as both 90% and 91% — a rounding, not a disagreement.

**Note 6 — headcount. UNRESOLVED, and flagged within Volume III itself.** The figures do not reconcile across sources or volumes: Volume III gives approximately 5,527 (2022) declining through approximately 3,800 (mid-2024) to **2,831 at 31 December 2025** on an S&P Global Market Intelligence basis, while also citing approximately 2,907 for 2025 from chief-executive statements; Volume V gives 5,527 at end-2022, **3,422 at end-2024**, and approximately 2,800 by 2026. The gaps are almost certainly definitional — full-time employees against total workforce, and whether the several thousand **outsourced** customer-service agents are counted. **No public source reconciles them.** The consequence is that the revenue-per-employee metric, which Klarna promotes heavily, is **sensitive to a definitional choice the company itself controls**, and should be treated as directional rather than precise. The qualitative conclusion — that headcount fell sharply while revenue rose — is robust to the discrepancy.

### Genuine reconciliations produced by the assembly

**Note 4 — the three "Kreditor" entities.** Volume I states that the founding vehicle was called Kreditor and was renamed Klarna in 2010, and separately that the operating company incorporated on 5 September 2007 as "Kreditor Finans AB" became Klarna Bank AB. Volume V states the company was founded on 1 July 2005 as "Kreditor Europe AB" and rebranded to Klarna in 2009. Read together these are not contradictory but describe **three distinct things**, and the assembly resolves them:

1. **Kreditor Europe AB** — the founding company, incorporated 1 July 2005. This is the entity the founders started.
2. **Kreditor Finans AB** — a separate company incorporated 5 September 2007, corp. ID 556737-0431, which later obtained the banking licence and became **Klarna Bank AB (publ)**. This is the entity that is the bank today.
3. **The Klarna rebrand** — dated 2009 in one volume and 2010 in the other. The discrepancy is genuine and unresolved at the level of the exact year; the rebrand occurred at the turn of the decade and nothing in the analysis turns on which side of it.

The practical point for a reader: **the company that was founded in 2005 is not the same legal entity as the bank that holds the licence today**, and conflating them produces an incorrect corporate history.

**Note 5 — the chief executive's incentive.** Volumes I and III refer to a disclosed potential incentive of **up to $35 billion** as a governance flashpoint in the 2024 board dispute. Volume V establishes what was actually granted and the two are different things:

- **The "$35 billion"** was a *reported maximum theoretical value* of a *proposed* equity programme, contingent on an extreme increase in valuation. It is the figure that circulated during the dispute.
- **The granted award** is **17,505,672 Class C options**, granted 5 March 2025, four-year vesting, 4.5-year term, weighted-average exercise price approximately **$91.80** per ordinary-share equivalent — more than twice the $40 IPO price and roughly four and a half times the subsequent market price, and described in the filings as substantially out of the money.

**Volume V governs.** The award that should be priced is the option package, whose value is zero unless the shares roughly triple — a materially different governance fact from the headline figure, and one that cuts in the company's favour.

## D.3 Known unknowns carried forward

- **The distributional question**: what share of consumer-fee revenue comes from what share of users. Identified in Volume II as the crux of the consumer-harm debate and **not answerable from public data**. Regulators could compel account-level fee-incidence data under the CCD II and FCA regimes; none has.
- The precise share of merchant revenue arriving through payment-service-provider merchants of record — disclosed only as "a substantial portion."
- The reconciled full-time employee series (note 6).
- Whether risk and compliance now hold a genuine product-launch veto following the FI findings; internal decision rights are not disclosed.
- The deposit split by market and by type (demand against fixed-term) for FY2025, disclosed only qualitatively.
- Forward-flow first-loss and retention percentages in the Nelnet, Elliott and Värde structures.
- The decline rate of the decision engine, hardship and forbearance uptake, and merchant-level GMV concentration.
- The outcome of the Utah industrial-bank application filed 6 July 2026.
- The aggregate state-by-state money-transmitter requirements applying to the US entities.

## D.4 A note on evidential asymmetry

This subject is the **least documented** of the seven in the programme, and that shapes what the study can and cannot say.

**The supervisory record is the strongest evidence.** The Finansinspektionen decision is unusually candid — it names the customer-due-diligence trigger that was set at sixty transactions where the regulator's benchmark was twelve, and it quantifies the population that fell outside the checks. It provides a level of forensic detail about internal controls that no voluntary disclosure would offer, and Volumes I and III rest substantially on it.

**The financial record is short.** Klarna has been a reporting company only since September 2025 and files as a foreign private issuer with reduced disclosure. The multi-year series is correspondingly thin, the pre-listing years rest on Swedish statutory accounts in a different currency and framework, and there is no IFRS-to-US-GAAP reconciliation.

**The operational record must be handled with unusual care.** Volume III established that the company's most publicised operational claim was substantially overstated and was later qualified by the chief executive. This is the only subject in the programme where the study's method had to include *correcting the subject's own account of itself* as a substantive analytical task rather than an incidental one.

**The gap that matters most is distributional.** Everything about whether this business is good or bad for the consumers who use it turns on a question the public data cannot answer. The study says so plainly rather than resolving it in either direction, and identifies precisely what disclosure would settle it.
