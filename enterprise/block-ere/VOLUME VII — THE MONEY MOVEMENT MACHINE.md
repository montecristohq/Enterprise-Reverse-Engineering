# VOLUME VII — THE MONEY MOVEMENT MACHINE
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