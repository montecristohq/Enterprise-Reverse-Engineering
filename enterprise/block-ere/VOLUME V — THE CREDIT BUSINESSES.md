# VOLUME V — THE CREDIT BUSINESSES
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