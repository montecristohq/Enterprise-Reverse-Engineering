# VOLUME XI — COMPETITION, MOAT & THE "ONE BLOCK" QUESTION
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