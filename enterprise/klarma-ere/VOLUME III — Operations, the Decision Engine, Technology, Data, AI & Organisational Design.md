# KLARNA — VOLUME III: Operations, the Decision Engine, Technology, Data, AI & Organisational Design

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