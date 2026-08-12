# VOLUME III — SQUARE: THE SELLER ECOSYSTEM
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