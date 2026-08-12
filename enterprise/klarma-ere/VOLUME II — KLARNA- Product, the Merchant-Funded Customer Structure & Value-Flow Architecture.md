# VOLUME II — KLARNA: Product, the Merchant-Funded Customer Structure & Value-Flow Architecture

## TL;DR
- **Klarna's true core product is short-dated merchant-funded credit at the point of sale, and the merchant — not the consumer — is the paying customer.** Klarna monetises primarily by driving GMV for retailers, charging a US merchant discount rate of 3.29–5.99% + $0.30 versus an EU consumer-card interchange cap of 0.3%. In FY2025 Klarna reported GMV of $127.9bn (+22% YoY), total revenue of $3.5bn (+25%), 118 million active consumers (+28%) and 966,000 merchants (+42%) — a ~2.75% take rate — but a net loss of $294.0m (EPS $(0.79)), swinging from a small profit in FY2024.
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