# ROBINHOOD MARKETS, INC. — VOLUME II
## Product, the Inverted Customer Structure & Value-Flow Architecture
### "The Order as Product — Who Actually Pays for Free?"

*Basis note: All figures US GAAP, US dollars, 31 December fiscal year end unless stated. Company operating metrics (Funded Customers, Total Platform Assets, Net Deposits, ARPU, Gold Subscribers) carry Robinhood's own definitions, which have changed over time; changes are flagged. Evidence tags: CONFIRMED FACT / COMPANY CLAIM / THIRD-PARTY ESTIMATE / ANALYTICAL INFERENCE / HYPOTHESIS / UNKNOWN.*

---

## TL;DR

- **Robinhood's true core product is the retail order, and the real paying customer is the wholesale market maker.** Retail users pay almost nothing in visible cash; they pay in execution quality, spread, forgone interest and subscription. The business is a monetisation ladder that escalates users through progressively more profitable and more dangerous products — from commission-free equities up through options, crypto, margin, and event contracts. [CONFIRMED FACT / ANALYTICAL INFERENCE]
- **Two engines now run the company: transaction revenue (PFOF-driven) and net interest revenue.** In FY2025 total net revenue was $4.473bn — transaction-based $2.628bn (59%), net interest $1.514bn (34%), other $0.331bn (7%). Options is the most durable transaction line; crypto is the most volatile; net interest is now a genuine second engine and, as in the Wise study, a transaction business quietly became partly a rate play. [CONFIRMED FACT]
- **"Commission-free" is best understood as a relocation of cost, not an elimination of it** — from a visible per-trade fee to a bundle of invisible costs (spread capture routed via PFOF, forgone interest on swept cash, margin interest, FX and per-contract options economics). The SEC found this relocation cost customers $34.1m even net of commission savings during 2016–2019, but the price-improvement argument for retail internalisation is genuine and must be weighed, not dismissed. [CONFIRMED FACT / ANALYTICAL INFERENCE]

---

## KEY FINDINGS

1. **The order is the product.** Robinhood earns transaction revenue by routing customer orders for options, equities, and (via a fee) crypto to wholesale market makers, who pay for the flow. In FY2021 transaction-based revenue (primarily PFOF) was over 77% of net revenue; by FY2025 it was 59%, reflecting deliberate diversification into net interest and subscription. [CONFIRMED FACT]

2. **Retail flow is valuable because it is uninformed ("non-toxic").** Retail orders carry little adverse-selection risk, so a market maker internalising them earns the spread without being systematically run over by better-informed counterparties. The SEC's Division of Economic and Risk Analysis working paper (Boulton, Shohfi & Walz, January 2025) states plainly that "Uninformed retail order flow, such as that from Robinhood, is particularly valuable to wholesalers due to the limited adverse selection risk." This is the causal mechanism that makes "free" trading fundable. [CONFIRMED FACT — market-microstructure literature]

3. **Options fund the company far more than equities per unit.** Ernst & Spatt (NBER WP 29883, 2022) estimate typical PFOF of ~40 cents per 100-share options trade versus ~20 cents per 100-share equity trade, and show that "a nominal investment of $1,000 in a $5 option would generate a 200-share options order, worth 80 cents in option PFOF… the same nominal investment in options will generate 10 times as much PFOF as the equity investment." Robinhood's own 2019 Rule 606 reports show options PFOF averaged $0.47/contract (Q4 2019) and $0.50/contract (Q2 2019). This asymmetry, plus higher crypto take rates, explains why the escalation ladder points toward more complex products. [THIRD-PARTY ESTIMATE / CONFIRMED FACT]

4. **Net interest revenue is now structural, not incidental.** FY2025 net interest revenue was $1.514bn (34% of net revenue), driven by margin lending (Margin Book $16.8bn at end-2025, +113% YoY), securities lending, cash sweep ($32.8bn), segregated cash and corporate cash. It is rate-sensitive on both sides. [CONFIRMED FACT]

5. **Robinhood Gold is a deposit-gathering and retention device, not primarily a subscription profit centre.** At $5/month, 4.2m subscribers at end-2025 (15%+ attach rate), Gold's real return is measured in the interest, margin, and card economics it unlocks, not in the ~$50m quarterly subscription line. [CONFIRMED FACT / ANALYTICAL INFERENCE]

6. **The escalation ladder is simultaneously the monetisation path and the risk path.** Each rung (options approval, margin, crypto, event contracts) raises revenue per user and the sophistication needed to use it safely — the structural fact behind the FINRA 2021 options-approval findings and the death of Alex Kearns. [CONFIRMED FACT / ANALYTICAL INFERENCE]

---

## DETAILS

### II.1 The Product Universe — by entity

Robinhood Markets, Inc. (RHM) executes nothing itself; every product is delivered through a subsidiary. The following decomposition follows the legal entity, with launch dates, pricing, revenue mechanism, and strategic purpose.

**Commission-free equities and ETFs (Robinhood Financial LLC introduces; Robinhood Securities LLC clears/routes).** Launched December 2014 (public), the founding product. Target customer: first-time and young retail investors. Job-to-be-done: cheap, frictionless market access. Pricing: $0 commission. Revenue mechanism: equity PFOF (spread-based; RHS receives a fixed percentage of the NBBO spread from each wholesaler) plus securities-lending and margin economics on the resulting positions. Direct cost: clearing/settlement, NSCC collateral. Regulatory dependency: SEC/FINRA best-execution (Rule 5310), Rule 605/606 disclosure. Strategic purpose: acquisition and the base of the ladder. [CONFIRMED FACT]

**Options (RHF/RHS).** Launched December 2017. Target: more active retail traders. Pricing: $0 commission per contract. Revenue mechanism: per-contract PFOF — structurally the single most important transaction line. Direct cost: clearing via OCC. Regulatory dependency: options-approval suitability rules (the subject of the June 2021 FINRA action). Strategic purpose: monetisation — the highest-yield mainstream product. [CONFIRMED FACT]

**Cryptocurrencies (Robinhood Crypto LLC).** Launched January 2018 (BTC, ETH first). Target: retail crypto buyers. Pricing: historically "commission-free" with a spread; from 2024 a disclosed fee-based model added. Revenue mechanism: transaction rebates from crypto market makers (e.g., B2C2, Tai Mo Shan) at ~35 bps per dollar of volume, far higher than equities/options per dollar; plus a fee. What the customer owns: a crypto position custodied at RHC — **no SIPC, no FDIC**. Regulatory dependency: state money-transmitter licensing, NYDFS, evolving federal treatment. Strategic purpose: monetisation and TAM expansion; the most cycle-sensitive line. [CONFIRMED FACT]

**Futures and options on futures (Robinhood Derivatives LLC, an FCM).** Built on a Marex FCM acquisition (2024); futures launched to customers in early 2025. Revenue: per-contract commissions/fees. Custody: CFTC segregation. Strategic purpose: monetisation and active-trader retention. [CONFIRMED FACT]

**Event / prediction-market contracts (Robinhood Derivatives LLC, via KalshiEX, ForecastEX, and Rothera Exchange).** Launched broadly in 2024–2025. The February 2025 "Pro Football Championship" (Super Bowl) market, launched via Kalshi to roughly 1% of customers, was rolled back at the CFTC's formal request days after launch — the regulator "formally requested that Robinhood Derivatives, LLC 'not permit customers to access' sports event contracts." In 2025 the company processed **over 12 billion event contracts** and, in a January 2026 step, formed a joint venture, Rothera LLC, with Susquehanna International Group that acquired MIAXdx to build a CFTC-licensed exchange/clearinghouse. Revenue: fees per contract (each trades in $0.01 increments up to $1, worth $1 at settlement). Strategic purpose: optionality/new-cohort acquisition; regulatory status contested. [CONFIRMED FACT]

**Fractional shares & recurring investments (RHF/RHS).** Launched 2019–2020. Enables sub-share investing; drives Funded Customer growth and small-deposit gathering. On the balance sheet, user-held fractional shares are a matched asset/repurchase-obligation pair ($3.782bn each at end-2025). Strategic purpose: acquisition/retention. [CONFIRMED FACT]

**Robinhood Gold (Robinhood Gold LLC).** Subscription, $5/month or $50/year. Benefits over time: cash-sweep APY (raised to 5.00% in November 2023; 3.35% by early 2026 as rates fell), 3% IRA match (vs 1% non-Gold), lower/deferred margin (first $1,000 interest-free), larger instant deposits, Nasdaq Level II data, Morningstar research, capped Strategies fees. Revenue: subscription fee plus everything it unlocks. Strategic purpose: retention + deposit gathering. [CONFIRMED FACT]

**Margin lending (RHS).** Interest-bearing loans against margin-enabled accounts. Margin Book reached $16.8bn at end-2025 (+113% YoY), $18.4bn in January 2026. Revenue: margin interest (net interest line). Regulatory dependency: Reg T, margin suitability. Strategic purpose: high-margin monetisation. [CONFIRMED FACT]

**Securities lending / stock lending (RHS).** Two programmes: Margin Securities Lending (RHS lends customer margin securities to third parties) and Fully-Paid Securities Lending (RHS borrows fully-paid customer shares and on-lends; customer receives up to 15% of the weighted-average rebate rate). At end-2024, securities loaned (cash collateral received) stood at $7.463bn, rising to $11.626bn at end-2025. Revenue: securities-lending net (net interest line). Strategic purpose: monetising custody. [CONFIRMED FACT]

**Cash sweep (RHF + partner banks).** Uninvested brokerage cash swept to a network of program banks; FDIC pass-through insurance (**not** SIPC). Cash Sweep balances $32.8bn at end-2025 (+26% YoY). Revenue: net interest spread (bank rate less rate paid to customer). Strategic purpose: deposit gathering and rate monetisation. [CONFIRMED FACT]

**Robinhood Cash Card / spending account (Robinhood Money LLC).** Debit/spending product with round-ups. Revenue: interchange. Strategic purpose: engagement/retention. [CONFIRMED FACT]

**Robinhood Gold Card (Robinhood Credit, Inc.; issued by Coastal Community Bank; Visa network).** Built on the X1 acquisition (~$95m, 2023); launched March 2024, rolled out through 2024–2025. 3% cash back on all categories (5% on travel booked via portal), no annual fee, exclusive to Gold members. Surpassed 1 million customers by mid-2026 (COMPANY CLAIM) with >$17bn annualised purchase volume. Revenue: interchange plus interest on revolving balances (net of financing-partner cost); funded partly via a Credit Card Funding Trust. Strategic purpose: monetisation + Gold attach. [CONFIRMED FACT / COMPANY CLAIM]

**Retirement accounts & IRA match (RHF/RHS).** Traditional and Roth IRAs with 1% match (3% for Gold). Retirement AUC reached $26.5bn at end-2025 (+102% YoY) across ~1.8m funded accounts; customers received over $500m in matches cumulatively. Match funds must vest (Gold held 1 year; funds held 5 years). Strategic purpose: sticky long-term deposit gathering. [CONFIRMED FACT / COMPANY CLAIM]

**Robinhood Strategies (Robinhood Asset Management LLC).** Digital managed-portfolio advisory launched March 2025; low, capped fees ($250 cap for Gold). Over 200,000 Funded Customers and $1.3bn AUM by end-2025. Strategic purpose: wallet-share deepening. [CONFIRMED FACT / COMPANY CLAIM]

**Robinhood Legend (desktop).** Advanced trading desktop launched 2024; surpassed $100m annualised revenue ~18 months post-launch (COMPANY CLAIM). Strategic purpose: active-trader retention/defensive vs incumbents. [COMPANY CLAIM]

**IPO Access.** Retail allocation in IPOs. Strategic purpose: acquisition/engagement. [CONFIRMED FACT]

**24-hour / overnight trading.** Extended-hours equity/ETF trading. Strategic purpose: engagement/defensive. [CONFIRMED FACT]

**Robinhood Banking (Robinhood Money LLC).** Rolling out to Gold Subscribers from late 2025/early 2026; >20,000 customers, ~$300m deposits by 31 January 2026 (COMPANY CLAIM). Strategic purpose: deposit gathering / super-app. [COMPANY CLAIM]

**Robinhood Ventures (Robinhood Ventures Fund I / RVI).** A consolidated investment vehicle (Robinhood held ~52% of RVI as of March 2026). Strategic purpose: optionality/private-market access. [CONFIRMED FACT]

**Tokenised equities in the EU (Robinhood Europe UAB).** "Stock Tokens" launched June 2025 in Cannes; expanded from ~200 to ~2,000 tokens; issued initially on Arbitrum, with a planned "Robinhood Chain" L2. No commission or added spread claimed; dividend support; 24/5. US access blocked pending an SEC regime. Strategic purpose: international TAM/optionality. [CONFIRMED FACT / COMPANY CLAIM]

**Bitstamp institutional services (Bitstamp).** Acquired 2 June 2025 for ~$224m (final consideration after purchase-price adjustments); globally-scaled crypto exchange with retail and institutional customers; ~520k Bitstamp Funded Customers added in Q2 2025. Institutional volumes more than doubled since close. Strategic purpose: global crypto infrastructure. [CONFIRMED FACT]

**TradePMR RIA custody (TradePMR).** Acquired 2025; custodial/portfolio-management platform for RIAs; folded into Funded Customer and Total Platform Assets metrics from Q1 2025. Strategic purpose: new-channel (advisor) TAM. [CONFIRMED FACT]

### II.2 The Inverted Customer Structure

Robinhood has at least four distinct payer classes.

**(1) Retail users** pay almost nothing per trade in visible cash. They pay through: (a) execution quality/spread capture embedded in PFOF routing; (b) the Gold subscription; (c) margin interest; (d) forgone interest on uninvested cash (the sweep spread accrues to Robinhood and its banks); (e) crypto spread/fee; (f) options per-contract economics; (g) indirectly, card interchange. The essential point: **retail users are largely not cash-paying customers of the trading product; they are the source of the product being sold.**

**(2) Wholesale market makers** are the cash-paying customers for the order-flow product. Rule 606 disclosures identify the principal counterparties for equities and options: **Citadel Securities** (the largest venue — roughly 65% of NYSE-listed equity order flow in Q4 2019 and consistently the dominant venue), **Virtu Americas**, **G1 Execution Services (G1X)**, **Two Sigma Securities**, **Wolverine Securities**, and **Jane Street Capital** (appearing in equity routing by 2024). For crypto, wholesalers include **B2C2** and **Tai Mo Shan**. The concentration is high — a handful of wholesalers, dominated by Citadel, buy nearly all the flow. [CONFIRMED FACT]

**(3) Subscription payers** are Gold subscribers (4.2m at end-2025), paying $5/month for a bundle whose real value is the interest and credit economics it unlocks.

**(4) Borrowers and depositors** — margin borrowers (Margin Book $16.8bn), securities-lending borrowers (third parties paying to borrow shares), and the partner banks receiving swept deposits (paying Robinhood a spread) — pay interest that funds the second engine.

**Is the retail user the customer, the product, or both — and does it differ by line?** [ANALYTICAL INFERENCE] For **equities and options**, the retail user is predominantly the *product*: the order is sold to a wholesaler and the user pays no cash. For **crypto**, the user is closer to a *customer* — since 2024 there is an explicit fee and a spread the user bears directly. For **margin, Gold, and the card**, the user is straightforwardly a paying *customer*. For **cash sweep and securities lending**, the user is a *supplier* of raw material (idle cash, lendable shares) that Robinhood monetises with a partner. The single business therefore holds the same person in all three roles simultaneously — product, customer, and supplier — depending on which screen they are on. This is the structural inversion, and it differs from the Experian study: where Experian's consumer is the raw material (data furnished about them), **Robinhood's customer's *order* is the product**.

### II.3 Why Retail Order Flow Is Worth Paying For — the mechanism

The analytical heart of the volume. The chain runs as follows. [CONFIRMED FACT — microstructure literature + SEC DERA working paper]

**What a wholesaler does with a retail order.** A wholesaler (internaliser) receives the routed marketable order and executes it against its own inventory ("internalisation"), typically at a price at or slightly better than the prevailing NBBO ("price improvement"). It captures the difference between what it pays to buy and what it receives to sell — the effective spread — across enormous volume.

**Why retail flow is more valuable than institutional flow — the adverse-selection argument.** Market microstructure since Glosten–Milgrom (1985) and Kyle (1985) models the bid-ask spread as compensation for, among other things, *adverse selection*: the risk that the counterparty knows something the market maker does not. Informed order flow is "toxic" — when an informed trader buys, the price tends to keep rising, and the market maker who sold to them loses. **Retail orders are, on average, uninformed**: a retail buy is as likely to precede a fall as a rise, so it does not systematically pick off the market maker. The SEC DERA working paper (Boulton, Shohfi & Walz, January 2025) states that "Uninformed retail order flow, such as that from Robinhood, is particularly valuable to wholesalers due to the limited adverse selection risk," and describes Robinhood's clientele (citing Fedyk 2023) as "young, small, and relatively inexperienced." Because segmented retail flow is safe to trade against, the wholesaler can quote tighter and still profit — and can afford to pay the broker a rebate (PFOF) for the privilege. Meanwhile, orders internalised off-exchange are hidden (non-displayed) liquidity, leaving the lit exchanges with a higher proportion of informed (toxic) flow and wider spreads — a documented negative externality (Lee and Chung, 2022; Hu and Murphy, 2024).

**How this becomes a rebate, and how rates are set.** For equities, RHS receives "a fixed percentage of the spread between the National Best Bid and National Best Offer for the security at the time of order execution" (Rule 606 language), the same percentage across non-exchange venues. For options, PFOF is set per contract. For crypto, "the transaction price is a fixed percentage of the notional order value." Payments are collected monthly in arrears; the same transaction price is paid by all market makers for a given trade type.

**The price-improvement counter-argument, presented fairly then tested.** Robinhood and wholesalers argue customers receive prices better than the exchange NBBO, made possible only by internalisation, and that zero commissions plus price improvement leave retail better off. This is genuine: internalisers do provide measurable price improvement on many equity orders. But the record is contested. The SEC's December 2020 order (Press Release 2020-321) found that "one of Robinhood's selling points to customers was that trading was 'commission free,' but due in large part to its unusually high payment for order flow rates, Robinhood customers' orders were executed at prices that were inferior to other brokers' prices," depriving customers of **$34.1 million even after taking into account the savings from not paying a commission** (October 2016–June 2019). The order also found that "Robinhood explicitly offered to accept less price improvement for its customers than what the principal trading firms were offering, in exchange for receiving a higher rate of payment for order flow for itself." Robinhood paid $65m to settle, without admitting or denying. The academic evidence is mixed by asset class: Ernst & Spatt (2022) find wholesalers offer smaller spreads than the exchanges in equities but *worse* trading costs in options; Levy (2022) finds price improvement is more pronounced at some brokers (TD Ameritrade) than others (Robinhood). **The honest resolution: PFOF is not self-evidently bad, but the specific charge against Robinhood — that it dialled up its own rebate at the expense of customer price improvement — was upheld and paid for.** [CONFIRMED FACT / ANALYTICAL INFERENCE]

**Why options PFOF per contract dwarfs equity PFOF per share, and what it implies.** Ernst & Spatt (2022, NBER WP 29883; published in The Review of Financial Studies, 2026) estimate typical PFOF of **~40 cents per 100-share options trade versus ~20 cents per 100-share equity trade**, and note that on a $0 commission the option pays a broker 100% more than the stock. Their $1,000-nominal illustration is decisive: "a nominal investment of $1,000 in a $25 stock would generate a 40-share equity order, worth 8 cents in equity PFOF, while a nominal investment of $1,000 in a $5 option would generate a 200-share options order, worth 80 cents in option PFOF… the same nominal investment in options will generate 10 times as much PFOF as the equity investment." Robinhood's own historical Rule 606 reports show options PFOF averaged **$0.47 per contract in Q4 2019 and $0.50 in Q2 2019**, and roughly $0.48–$0.60 per contract by venue in 2022. Equity PFOF in Q1 2024 ran ~12–18 cents per hundred shares for non-S&P 500 stocks and ~60–90 cents per hundred shares for S&P 500 market orders (spread-based, hence higher on higher-priced names). Crypto is higher still per dollar (~35 bps vs ~8 bps options, ~0.8 bps equities per Ernst & Spatt/DERA). **Implication: options (and crypto) fund the company; equities are the acquisition loss-leader.** This is precisely why the escalation ladder points users toward more complex products, and why Ernst & Spatt warn that differential PFOF "may tempt" brokers to encourage trading in higher-PFOF assets. [THIRD-PARTY ESTIMATE / CONFIRMED FACT]

### II.4 Transaction Revenue Decomposition

Transaction-based revenue splits into options, equities, cryptocurrencies, and other (futures, event contracts). Reporting history (full-year, $m unless noted): [CONFIRMED FACT except where derived]

- **FY2021:** Total transaction ~$1,400m — options **$689m**, crypto **$419m**, equities **$288m**. Transaction revenue was >77% of net revenue. Crypto's spike was Dogecoin-driven (Dogecoin was over 60% of crypto transactions in Q2 2021).
- **FY2022:** Total ~$814m — approx. options ~$488m, crypto ~$202m, equities ~$115m (derived by summing quarterly disclosures; the FY2022 10-K disaggregation is authoritative). The 25% revenue decline reflected the post-meme, rising-rate bear market.
- **FY2023:** Total $785m — options over $500m (the largest line), crypto and equities smaller. Net interest revenue ($900m+) exceeded transaction revenue for the first time.
- **FY2024:** Total transaction **$1,647m** (+110%). Q4 2024 alone: crypto $358m, options $222m, equities $61m. For the full year crypto was the largest line (~$626m derived; confirm against 10-K), options ~$700m, equities ~$179m.
- **FY2025:** Total transaction **$2,628m** (+60%). Q4 2025: options $314m (+41%), crypto $221m (−38%), equities $94m (+54%), other transaction (event contracts etc.) $147m (+300%+). Event contracts became a material fourth line, with 8.5bn contracts traded in Q4 2025 alone.

**Which line has historically produced the most, and how has it changed?** Options has been the most consistent leader (2021, 2022, 2023, and most of 2024–2025), while crypto is the swing factor: from 30% of transaction revenue in 2021, collapsing in 2022, surging to the top line in late 2024, then falling 38% YoY in Q4 2025. **Crypto revenue correlates strongly with crypto prices (a Bitcoin correlation of ~0.78 in one third-party analysis).** The mix trend is toward diversification: transaction revenue fell from 77% of net revenue (2021) to 59% (2025), and management stated it operates "13 business lines each generating more than $100m in annualized revenue," up from three in 2022 (COMPANY CLAIM). [CONFIRMED FACT / THIRD-PARTY ESTIMATE]

### II.5 Net Interest Revenue — the second engine

Net interest revenue decomposes (Robinhood's own line items) into: (1) interest on corporate cash and investments; (2) **margin interest** paid by customers; (3) interest on segregated cash/securities and deposits with clearing organisations; (4) **cash sweep** (spread on off-balance-sheet swept deposits); (5) **securities lending, net**; (6) credit card, net; less (7) interest expense on credit facilities. [CONFIRMED FACT]

FY2025 net interest revenue was **$1.514bn (+37%)**, 34% of total net revenue, up from ~$900m in 2023. Q4 2025 alone was $411m (+39%), "primarily driven by growth in interest-earning assets and securities lending activity, partially offset by lower short-term interest rates." One third-party analysis attributes ~40% of total revenue to net interest income (margin, securities lending, cash sweep). [CONFIRMED FACT / THIRD-PARTY ESTIMATE]

**Rate sensitivity.** Net interest revenue is a two-sided rate play. When policy rates rose in 2022–2023, the sweep spread and margin/segregated-cash yields expanded, and net interest revenue overtook transaction revenue in 2023. As short rates fell in 2025, Robinhood offset the compression by *growing balances* — margin +113%, securities lending, and interest-earning assets — so net interest revenue still rose 37%. The Gold cash-sweep APY moves with rates (5.00% at the November 2023 peak, 3.35% by early 2026), and the spread Robinhood retains is the difference between the program-bank rate and the customer rate.

**Structural parallel to the Wise study.** [ANALYTICAL INFERENCE] As in the Wise reconstruction — where a cross-border transfer business quietly became substantially a float/rate play — Robinhood's "commission-free" trading business has become, at the margin, an interest-rate business layered on customer balances (cash, margin, lendable securities). The parallel is real but partial: unlike Wise, Robinhood's transaction engine remains the larger line (59% vs 34%), and its interest income is more diversified across margin and lending than pure float. The verdict: **net interest is a genuine, structural second engine and a rate play, but Robinhood is a two-engine company rather than a rate play wearing a transaction disguise.**

### II.6 Robinhood Gold — the subscription layer

Gold costs **$5/month or $50/year** (a $10 annual saving). What the subscriber receives: elevated cash-sweep APY (5.00% at the November 2023 peak; 3.35% early 2026), 3% IRA match vs 1%, first $1,000 of margin interest-free plus a lower Gold margin rate, larger instant deposits (historically up to $50,000), Nasdaq Level II data, Morningstar research, capped Strategies fees, and Gold Card eligibility. [CONFIRMED FACT]

Subscriber trajectory: ~1.9m (mid-2024) → 3.5m (Q2 2025, 13%+ attach) → **4.2m (end-2025, 15%+ attach)** → 4.8m (Q2 2026, COMPANY CLAIM). Gold subscription revenue was ~$50m in Q4 2025 (+56% YoY), inside the "other revenues" line of $96m. [CONFIRMED FACT]

**Unit economics and verdict.** [ANALYTICAL INFERENCE] At $50–60/year per subscriber, 4.2m subscribers imply roughly $210–250m of annual gross subscription revenue — meaningful but small against $4.5bn net revenue. The consumer-facing "worth it" math (independent reviews) shows Gold pays for itself for a user with ~$1,200–2,700 idle cash or an IRA contributor, meaning Robinhood is essentially returning most of the sweep spread and match to the subscriber. **Gold is therefore not primarily a profit centre in its own subscription line; it is a retention and deposit-gathering flywheel** — it raises switching costs, pulls in idle cash (monetised via the sweep), encourages IRA contributions (sticky 5-year-vesting balances), and gates the credit card. Its true return is booked in net interest and card economics, not in "other revenues."

### II.7 Customer Segmentation and Disclosed Metrics

**Definitions (Robinhood's own, with changes flagged):** [CONFIRMED FACT]
- **Funded Customer:** a unique person with ≥1 Robinhood-entity account that, within 45 days, had a positive balance or completed a transaction. Joint-account holders each count (from July 2024); TradePMR RIA customers count from Q1 2025; Bitstamp customers from June 2025.
- **Total Platform Assets** (introduced Q1 2025): fair value of all equities, options, crypto, futures, and cash net of receivables, plus TradePMR-managed non-custodied assets. Formerly the narrower **Assets Under Custody** (which excludes TradePMR non-custodied assets).
- **Net Deposits:** cash deposits and asset transfers plus dividends/interest/staking and promotion incentives, net of withdrawals, margin/lending interest, and Gold fees. Includes Bitstamp from June 2025; excludes TradePMR.
- **ARPU:** total revenue ÷ average Funded Customers, annualised per quarter.
- **Gold Subscribers:** unique persons subscribed and having made ≥1 payment.

**Series:** [CONFIRMED FACT]
- Funded Customers: ~22.5m (2021) → 24.3m (Q3 2024) → 26.5m (Q2 2025) → **27.0m (end-2025)**.
- Total Platform Assets: **$324bn (end-2025, +68% YoY)**; $279bn Q2 2025.
- Net Deposits: **$68.1bn full-year 2025** (35% growth rate); $15.9bn Q4 2025.
- ARPU: **$191 (Q4 2025, +16% YoY)**; $151 (Q2 2025).
- Margin Book $16.8bn; Cash Sweep $32.8bn; Retirement AUC $26.5bn (all end-2025).
- Historic: 18.9m monthly active users at 30 September 2021; MAU/DAU are less consistently disclosed now.

**Demographics.** [THIRD-PARTY ESTIMATE] Median/average age ~31 (2021); most-saturated cohort 27–33; more than one in four first-time investors; predominantly male; average transaction size ~$500 in early 2021. Fedyk (2023) characterises the base as "young, small, and relatively inexperienced."

**Revenue concentration.** [THIRD-PARTY ESTIMATE / ANALYTICAL INFERENCE] Robinhood discloses that it derives transaction-based revenue from a concentrated set of market makers (a credit-risk concentration). On the *customer* side, precise disclosure of what share of revenue comes from the most active options/crypto traders is not published; academic and industry analysis strongly implies heavy concentration in a minority of high-frequency options and crypto traders, given per-unit economics. Barber et al. (2022) estimate ~30% of daily trades across major retail brokers were attributable to Robinhood users; other estimates put Robinhood at up to half of retail flow at times. Treat the specific "X% of revenue from top traders" as **UNKNOWN/estimate** absent company disclosure.

### II.8 The Customer Journey and the Escalation Ladder

The lifecycle — acquisition (referral/free-stock, influencer marketing) → onboarding/identity verification → funding → first trade → **options approval** → margin → crypto → Gold → retirement → credit card — is **simultaneously the monetisation path and the risk-escalation path.** Each rung raises revenue per user (equities ≈ loss-leader; options and crypto ≈ high-yield; margin and card ≈ interest income) and raises the sophistication and risk required to use the product safely. [ANALYTICAL INFERENCE — the volume's central structural claim]

The connection to enforcement is direct. FINRA's June 30, 2021 news release announced it had "fined Robinhood Financial LLC $57 million and ordered the firm to pay approximately $12.6 million in restitution, plus interest… the largest financial penalty ever ordered by FINRA." It found that since December 2017 the firm "relied on algorithms—known at Robinhood as 'option account approval bots'—to approve customers for options trading, with only limited oversight by firm principals," approving "thousands of customers… who either did not satisfy the firm's eligibility criteria or whose accounts contained red flags." One cited case matched **Alexander Kearns**, a 20-year-old of Naperville, Illinois, who died June 12, 2020 after his Robinhood account displayed a negative cash balance of **$730,165** on an options position he believed was capped at under $10,000; a 3:26 a.m. automated email demanded roughly $170,000. FINRA found the displayed balance was inaccurate and the true position value was about half of what was shown; Robinhood settled the family's wrongful-death suit (disclosed in its 2021 IPO filing). **The ladder's design — frictionless escalation into options by algorithm, with a display that could mislead about assignment and margin — is the mechanism that turned a monetisation path into a fatal risk path.** [CONFIRMED FACT / ANALYTICAL INFERENCE]

### II.9 The Interface as Distribution — design, engagement, and suitability

Robinhood's mobile-first, single-screen design removes friction from account opening and trading; historically it deployed **confetti animation** on trades (removed in 2021), **scratch-off free-stock rewards**, streaks, push notifications, and "Top Movers"/popularity lists. These are commercial mechanisms: they increase engagement and trading frequency, which increases order flow and therefore PFOF. [CONFIRMED FACT]

**Peer-reviewed evidence.** Barber, Huang, Odean & Schwarz, "Attention-Induced Trading and Returns: Evidence from Robinhood Users" (The Journal of Finance, Vol. 77, No. 6, December 2022, pp. 3141–3190), documents pronounced herding into attention-grabbing stocks (driven partly by the "Top Mover" list): "Average 20-day abnormal returns are −4.7% for the top stocks purchased each day" — i.e., intense Robinhood buying forecasts negative returns. Robinhood users traded roughly forty times as many shares as Schwab customers per unit of assets. Related work (Eaton et al.; Ozik, Sadka & Shen) uses Robinhood outages and Robintrack data to study the platform's market-quality effects. [CONFIRMED FACT]

**Regulatory response.** The **Massachusetts** Securities Division charged Robinhood in December 2020 under the state fiduciary rule, objecting specifically to confetti, digital scratch tickets, free-stock rewards, push notifications, and "most popular" lists; Robinhood sued to block the rule, lost at the Massachusetts Supreme Judicial Court (2023), and settled in 2024 for **$7.5m**, agreeing (for Massachusetts accounts) to cease celebratory imagery tied to trading frequency, list-based push notifications, and features mimicking games of chance. The consent order noted some customers with no experience averaged at least five trades a day. The **SEC's August 27, 2021 request for information and comment on Digital Engagement Practices** ("DEPs") sought input on gamification, behavioural prompts, and game-like features; Chair Gensler flagged that such prompts "could promote behavior that is not in the interest of the customer, such as excessive trading" and that a PFOF ban was "on the table." **FINRA's March 2025 action** found Robinhood "failed to reasonably supervise and retain social media communications… posted by paid social media influencers," some "promissory or not fair and balanced." [CONFIRMED FACT]

**Honest assessment.** [ANALYTICAL INFERENCE] The design is *both* a legitimate consumer-experience advance (it genuinely lowered barriers and forced industry-wide zero commissions) *and* a suitability problem (the same frictionlessness plus behavioural nudges demonstrably increased trading frequency and attention-driven losses, and the business monetises exactly that frequency). Notably, the Massachusetts settlement did not find that the DEPs themselves violated the rule or that they negatively influenced behaviour — it concerned supervisory controls — so the strongest empirical claims rest on the academic literature, not on an adjudicated finding of harm from the design per se.

### II.10 Value-Flow Reconstruction — three transactions end to end

**Transaction 1 — a commission-free equity purchase of $1,000.**
- (A) *Customer-facing event:* user taps "buy $1,000" of a stock; sees $0 commission and near-instant fill.
- (B) *Order/securities flow:* RHF (introducing broker) accepts the order; RHS (clearing broker) routes it as a non-directed order — "100% of total customer orders were non-directed" — selecting the venue. It goes to a wholesaler (most likely Citadel Securities, historically ~65% of NYSE-listed flow), which internalises against inventory, executing at or slightly better than the NBBO.
- (C) *Money flow:* customer pays $1,000 (plus/minus price improvement). The wholesaler pays RHS a rebate equal to a fixed percentage of the NBBO spread — on a $1,000 order in a mid-priced S&P 500 name, on the order of a fraction of a cent to a few cents per share; Ernst & Spatt's illustration values a $1,000 equity order's PFOF at roughly 8 cents. RHS shares revenue with RHF under a disclosed clearing agreement.
- (D) *Data flow:* the order, its routing, and execution feed Rule 605 (execution quality) and Rule 606 (routing/PFOF) disclosures.
- (E) *Settlement/custody:* trade settles T+1 (post-May 2024; formerly T+2) via NSCC continuous net settlement; shares are held in street name at RHS (the entity that "holds the assets"). NSCC collateral must be posted during the settlement window — the exact mechanism that caused the January 2021 crisis.
- (F) *Accounting:* PFOF recognised as transaction-based revenue at the point the routed order is executed by the market maker; collected monthly in arrears.
- (G) *Legal/regulatory:* RHF owes best execution (FINRA 5310); RHS owes Rule 15c3-3 customer-protection/segregation; SIPC coverage plus excess private insurance applies to the securities.

**Transaction 2 — a single-leg options trade.**
- (A) User buys one option contract, $0 commission.
- (B–C) RHF/RHS route to an options wholesaler (Citadel, Wolverine, G1X historically). Crucially, options PFOF is **per contract** — historically ~$0.47–$0.60 per contract — not spread-percentage. On the $1,000-nominal comparison, an options order can generate ~10× the PFOF of the same-dollar equity order. So the *identical customer intent* ($1,000 exposure) yields dramatically more revenue if expressed in options.
- (D–E) Cleared via OCC; assignment/exercise mechanics apply (the Kearns hazard).
- (F) Recognised per contract at execution.
- (G) Best execution applies but Ernst & Spatt find PFOF is associated with *worse* options prices — the price-improvement defence is weakest here.
- **Why the economics differ so sharply:** per-contract pricing decouples PFOF from notional value, and options' leverage means small nominal outlays produce large contract counts. This is the mathematical core of why the ladder pushes toward options.

**Transaction 3 — a crypto purchase (RHC).**
- (A) User buys crypto; historically "commission-free," now with a disclosed fee plus spread.
- (B) RHC either routes to crypto market makers (B2C2, Tai Mo Shan) or matches orders on an "industry-standard matching engine."
- (C) *Money flow:* the transaction price is "a fixed percentage of the notional order value" — economically a rebate/fee of ~35 bps per dollar of volume, far richer per dollar than equities (~0.8 bps) or options (~8 bps). The user bears this as spread/fee directly.
- (D) **No Rule 606 disclosure applies** — crypto PFOF is opaque (the SEC DERA paper's central critique: crypto PFOF "lacks transparency and generates significantly higher fees").
- (E) *Custody:* the crypto is custodied at RHC. **What the customer actually owns:** a position at RHC with **neither SIPC nor FDIC protection** — legally and economically distinct from the SIPC-covered equity.
- (F) Recognised as transaction revenue at execution.
- (G) State money-transmitter and NYDFS oversight; contested federal securities treatment. **This is the line where the retail user is most clearly a paying customer bearing a visible-but-large cost, yet with the least protection and least disclosure.**

### II.11 Distribution and Acquisition Economics

Acquisition channels: organic/referral (free-stock referral programme — refer a friend, both receive a randomly-valued free share), paid influencer marketing (the subject of the FINRA March 2025 unretained-communications finding), IPO Access as an engagement/acquisition hook, and **1%/2% deposit-match and 3% IRA-match** promotions. [CONFIRMED FACT]

**How the match promotions function economically.** [ANALYTICAL INFERENCE] The matches are a **deposit-gathering subsidy**. Robinhood pays 1–3% upfront (a "deferred customer match incentive" — $185m current + $428m non-current deferred asset at end-2025) to pull in balances that vest over years (Gold held 1 year; funds held 5 years). The return is traced to: (a) net interest on the deposited/transferred balances (sweep, margin collateral, segregated cash); (b) transaction revenue from the trading those balances enable; (c) switching-cost lock-in. In 2025, marketing spend was $399m (+47%) against $68.1bn Net Deposits and 1.8m net new Funded Customers.

**CAC and payback.** [ANALYTICAL INFERENCE / HYPOTHESIS] A crude 2025 implied CAC — $399m marketing ÷ 1.8m net new Funded Customers ≈ **~$220 per net-added funded customer** (an upper bound, since marketing also drives cross-sell to existing users and deposit growth, not just headcount). Against Q4 2025 ARPU of $191 annualised, simple payback is on the order of ~1–1.5 years if retention holds — attractive but sensitive to churn and to the match-vesting clawback (customers forfeit unvested match if they leave early, which protects the subsidy). Treat exact CAC/payback as an inference, not company disclosure.

### II.12 Failure and Exception Paths

- **March 2020 outages.** Platform-wide failures on 2–3 March 2020 during extreme volatility locked customers out; FINRA (2021) found Robinhood failed to supervise the technology behind core services (Jan 2018–Feb 2021), costing certain customers "tens of thousands of dollars." Owner: RHF/RHS; remediation: fines/restitution within the $70m FINRA settlement. [CONFIRMED FACT]
- **January 2021 position-close-only restrictions.** After an NSCC collateral demand (~$3.7bn against ~$700m on hand, later reduced to $1.4bn), Robinhood restricted buying in GameStop/AMC and other names to position-closing-only. Owner: RHS (clearing/self-clearing). Impact: reputational catastrophe + litigation; the direct consequence of self-clearing internalising NSCC settlement risk (Volume I). Robinhood raised ~$3.5bn in emergency capital within days. [CONFIRMED FACT]
- **Collaring of market orders and cancellation (FINRA March 2025).** RHF gave "inaccurate or incomplete disclosures regarding its practice of 'collaring' market orders by converting them to limit orders," causing some orders to be cancelled and re-entered at inferior prices. Remediation: **$3.75m restitution** within the $29.75m settlement ($26m fine + $3.75m restitution). Owner: RHF. [CONFIRMED FACT]
- **Options assignment/exercise errors.** The Kearns display error (misleading negative balance of $730,165; true position value ~half of displayed) — owner RHF; remediation within the $70m 2021 settlement plus product/UX changes. [CONFIRMED FACT]
- **Margin calls / forced liquidation.** Automatic liquidation when margin requirements breach; customer impact is realised losses; legal obligation limited to accurate disclosure (a Kearns failure point). [CONFIRMED FACT]
- **November 2021 data breach.** A November 3, 2021 breach — obtained after an attacker "socially engineered a customer support employee by phone" — exposed email addresses of ~5 million customers and full names of ~2 million more (~7 million total); ~310 had name, date of birth and zip code exposed and ~10 had "more extensive account details revealed." ~117,000 Massachusetts customers were cited in the 2024 consent order. Owner: RHM/RHF; remediation within the Massachusetts settlement and NYDFS oversight. [CONFIRMED FACT]
- **Account takeover / AML failures (FINRA March 2025).** RHF/RHS "failed to establish and implement reasonable anti-money laundering programs," missing suspicious activity and third-party account takeovers, and opened thousands of accounts without adequate identity verification. Owner: RHF/RHS; remediation within the $29.75m settlement. [CONFIRMED FACT]
- **Crypto withdrawal / custody issues.** RHC positions carry neither SIPC nor FDIC; custody risk sits with RHC and the customer. [CONFIRMED FACT]

### II.13 Product-Market Evolution

2014 equities → 2017 options → 2018 crypto → 2019 fractional shares/recurring → 2019–2020 cash management → 2021 IPO Access → 2022 retirement (IRA) → 2023 Gold Card build (X1) / 24-hour trading → 2024 futures (Marex), Gold Card launch, Legend, event contracts → 2025 Strategies, Bitstamp (global crypto), TradePMR (RIA custody), tokenised EU equities, perpetual futures/staking, Banking → 2026 Rothera prediction-market exchange, short selling, money-market funds, agentic (AI) trading. [CONFIRMED FACT]

**The pattern.** [ANALYTICAL INFERENCE] Robinhood is doing **both** things at once, but the dominant motion has shifted. Through ~2022 it primarily *deepened wallet share with the same aging cohort* (the 27–33 first-timers of 2021 acquiring options, margin, retirement, and credit as they matured financially — the "Great Wealth Transfer" framing management now uses). From 2023 it increasingly *acquired new cohorts via new products and channels*: RIAs (TradePMR), institutions (Bitstamp), international retail (EU tokens, UK ISA, Asia acquisitions), and prediction-market/sports-adjacent users (event contracts). The strategy revealed: convert a single-product, cycle-exposed PFOF broker into a diversified, multi-entity "financial super-app" whose revenue is less hostage to any one market cycle — while never abandoning the core insight that the order is the product and engagement is the fuel.

### II.14 Volume II Reconstruction

**(1) Full product architecture by entity** — RHM (holdco, executes nothing) over RHF (customer relationship, best execution), RHS (assets, routing, clearing, margin, securities lending), RHC (crypto, no SIPC/FDIC), RHD (futures + event contracts, CFTC), Robinhood Money (cash card, banking), Robinhood Credit + Coastal Community Bank (Gold Card), Robinhood Asset Management (Strategies), Robinhood Gold LLC (subscription), Robinhood Europe UAB / Robinhood U.K. Ltd (international), Bitstamp (global crypto), TradePMR (RIA custody), RVI (Ventures).

**(2) The four-payer map** — market makers (PFOF, the cash customer for the order product), retail users (product for equities/options; customer for crypto/margin/Gold/card; supplier for sweep/lending), Gold subscribers, and borrowers/depositors/partner banks.

**(3) Order-flow value mechanism** — uninformed retail flow → low adverse selection → wholesaler internalises and earns the spread safely → pays a rebate → funds "free."

**(4) Transaction revenue decomposition** — options the durable leader; crypto the volatile swing line (BTC-correlated); equities the loss-leader; event contracts the emerging fourth line. FY2025 transaction $2.628bn.

**(5) Net interest decomposition and rate sensitivity** — margin + securities lending + cash sweep + segregated/corporate cash + card; FY2025 $1.514bn; two-sided rate play; balance growth offset falling rates in 2025.

**(6) Gold unit economics** — $5/month, 4.2m subscribers, ~$210–250m subscription revenue; a retention/deposit flywheel whose real return is in net interest and card economics.

**(7) Customer metric series** — 27.0m Funded Customers, $324bn Total Platform Assets, $68.1bn FY2025 Net Deposits, $191 ARPU, 4.2m Gold, all end-2025.

**(8) The escalation ladder** — monetisation path = risk path; the volume's central claim; connected to FINRA 2021 and Kearns.

**(9) Three value-flow maps** — equity ($1,000, spread-based PFOF, SIPC, T+1), options (per-contract PFOF ~10× per nominal dollar, OCC, assignment risk), crypto (notional-percentage fee ~35bps, no SIPC/FDIC, opaque, matching engine).

**(10) Acquisition economics** — free-stock referral, influencer marketing, IPO Access, 1–3% match as a deposit subsidy (deferred incentive asset $613m); implied ~$220 CAC, ~1–1.5yr payback (inference).

**(11) Failure map** — March 2020 outages; Jan 2021 PCO/NSCC; collaring (2025); Kearns/options; margin liquidation; Nov 2021 breach; AML/ATO; crypto custody.

**(12) Product evolution timeline** — 2014→2026, from single-product PFOF broker to diversified multi-entity super-app.

**(13) Key unknowns** — exact customer-side revenue concentration (share from top options/crypto traders); precise current-year (2024–25) per-contract options PFOF in company prose; crypto wholesaler concentration; true blended CAC net of cross-sell; the durability of event-contract revenue given contested CFTC status.

**(14) Ten most important conclusions** — (i) the order, not the app, is the product; (ii) the wholesaler, not the user, is the primary cash customer of the flagship business; (iii) retail flow is fundable because it is uninformed; (iv) options and crypto — not equities — fund the company; (v) net interest is now a structural second engine and a rate play; (vi) Gold is a deposit flywheel, not a subscription profit centre; (vii) the escalation ladder is the risk ladder; (viii) the interface is a distribution and frequency-generation mechanism, with peer-reviewed evidence of −4.7% 20-day returns on the most-bought names; (ix) crypto and event contracts are the fragile, contingent lines; (x) "commission-free" is predominantly a relocation of cost into invisibility.

**The central answers.** [ANALYTICAL INFERENCE grounded in CONFIRMED FACT]
- **True core product:** the retail order (a stream of uninformed, low-toxicity order flow), plus the customer balances (cash, margin, lendable shares) that the trading relationship generates.
- **Real customer:** for the flagship equities/options business, the wholesale market maker (Citadel above all). The retail user is the product and the supplier more than the customer — except in crypto, margin, Gold, and the card, where they pay directly.
- **Which product funds the company:** historically options (durable, high per-unit PFOF) and increasingly net interest (margin + lending + sweep); crypto funds it explosively but only in up-cycles; equities barely fund it at all.
- **What the retail user actually pays, and can they see it:** they pay spread/execution quality (invisible, routed through PFOF), forgone interest on idle cash (invisible unless they read the sweep terms), margin and crypto costs (semi-visible), and the Gold fee (visible). Most of the cost is deliberately invisible; Rule 605/606 disclose it in aggregate but not per trade in a form a retail user reads.
- **Highest-quality vs most-fragile revenue line:** highest quality = net interest (recurring, balance-driven, diversified) and options (structurally sticky); most fragile = crypto (cycle- and price-dependent, ~0.78 BTC correlation) and event contracts (regulatorily contingent).
- **The central question — is "commission-free" a genuine reduction in the cost of investing or a relocation of it?** It is **both, but predominantly a relocation.** Robinhood genuinely destroyed the explicit commission and forced the whole industry to zero — a real, permanent consumer gain. But the cost of investing did not vanish; it moved from a visible per-trade fee to a bundle of invisible costs — spread capture monetised via PFOF, forgone interest on swept cash, per-contract options economics, crypto spread, and margin interest — while the interface was engineered to increase the very trading frequency that generates those costs. The SEC's $34.1m finding (inferior prices net of commission savings) is the clean proof that, for a defined period, the relocation left Robinhood's own customers worse off than the visible-fee alternative. The honest verdict: commission-free is a real advance in access and a real reduction in one visible cost, achieved by relocating the true cost of investing into places the customer cannot easily see — and by monetising a ladder that grows more profitable precisely as it grows more dangerous.

---

## RECOMMENDATIONS

**For an analyst/investor evaluating Robinhood:**
1. **Track the transaction/net-interest mix quarterly.** If transaction revenue falls below ~50% of net revenue durably, re-rate Robinhood partly as a rate-sensitive balance-sheet business (Wise parallel). Threshold to watch: net interest revenue growth turning negative in a falling-rate environment *without* offsetting Margin Book/Cash Sweep growth — that would signal the second engine stalling.
2. **Watch options and event-contract volumes, not headline revenue.** Options is the durable funder; a sustained decline in Options Contracts Traded (was 659m in Q4 2025, +38%) is the leading indicator of transaction-revenue quality. Event-contract revenue is high-growth but regulatorily contingent — treat any figure as at-risk until the Rothera/CFTC exchange status is settled.
3. **Monitor crypto as the swing factor.** With ~0.78 BTC correlation, model crypto transaction revenue as a call option on the cycle, not a base case. A 50% crypto drawdown plus 30% equity drawdown would stress nearly half the top line.
4. **Price in regulatory tail risk on PFOF and DEPs.** A US PFOF ban (repeatedly "on the table") or adverse tokenised-equity/event-contract rulings are the binary risks. The UK/EU already ban PFOF, forcing a different (fee/spread) model abroad — a template for what a US ban would do to margins.

**For a regulator/policymaker:**
5. Require **per-asset-class PFOF transparency for crypto** (no Rule 606 equivalent exists) and clearer per-trade cost disclosure to retail — the invisibility of relocated cost is the core consumer-protection gap.
6. Scrutinise the **escalation ladder's suitability**, not just individual features: the monetisation-equals-risk structure is the systemic issue the confetti debate obscured.

**Benchmarks that would change these recommendations:** a durable shift of transaction revenue below 50% of net revenue (re-rate as rate play); a US PFOF ban (structural margin reset); event-contract revenue surviving a full CFTC adjudication (de-risk that line); crypto revenue decoupling from BTC price (upgrade quality).

---

## CAVEATS

- **Full-year 2022 and 2024 asset-class transaction splits are partly derived** by summing quarterly disclosures; the authoritative figures are in the respective 10-K disaggregation tables. FY2021 ($689m options / $419m crypto / $288m equities) and FY2025 totals are firmly sourced.
- **Current-year (2024–25) options PFOF per contract in explicit company prose was not isolated;** the firmest per-contract figures are Robinhood's own 2019 Rule 606 reports ($0.47–$0.50) and 2022 tables (~$0.48–$0.60). The Ernst & Spatt 40¢/20¢ and 10× figures are the authoritative comparative estimates.
- **The options ~8bps / equities ~0.8bps / crypto ~35bps per-dollar triplet** is drawn from the SEC DERA working paper's citation of Ernst & Spatt for options/equities and RHC disclosures for crypto; treat the exact bps as estimates.
- **Customer-side revenue concentration** (share from the most active options/crypto traders) is not disclosed by Robinhood and is treated as UNKNOWN/estimate.
- **CAC and payback are analytical inferences**, not company disclosures, and overstate true per-customer cost because marketing also drives cross-sell and deposit growth.
- **Some 2026 datapoints** (Q2 2026 revenue, Gold Card >1m, agentic trading) are recent company claims/press reporting; treated as COMPANY CLAIM.
- **Third-party revenue-percentage analyses** (e.g., "40% net interest," "90% of transaction revenue is PFOF") are secondary estimates consistent with, but not identical to, Robinhood's GAAP line items.

*End of Volume II. Volume III not commenced, per instruction.*