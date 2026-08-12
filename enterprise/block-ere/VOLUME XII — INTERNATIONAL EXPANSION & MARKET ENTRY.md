# VOLUME XII — INTERNATIONAL EXPANSION & MARKET ENTRY
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

**Afterpay / Clearpay (acquired, not built).** Block issued 113,617,352 Class A shares with an aggregate fair value of $13.8bn; the deal closed 31 January 2022 (Block FY2022 10-K Note 9; 31 January 2022 8-K). Afterpay brand in the US, Australia, New Zealand and Canada; Clearpay brand in the UK. Clearpay entered the EU in 2021 via the Pagantis acquisition and **exited the EU (wind-down from ~25 August 2025)** while UK/US/AU/NZ continued. ~24m active customers globally; dominant in Australia/NZ (~65% share), ~22% US share. Volume IX's caution stands: $11.72bn goodwill split 50/50 between the Square and Cash App units, never impaired, standalone test impossible. **[CONFIRMED FACT / THIRD-PARTY ESTIMATE on shares]**

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

**(1) Market table:** US (home, full stack), Canada (Oct 2012), Japan (May 2013, SMCC, 3.25%→3.6%), Australia (2016, 1.6%), UK (Mar 2017, Squareup Europe Ltd, FCA FRN 900846, 1.75%), Ireland/France/Spain (2021). Cash App: UK (2018–2024, exited), Verse EU (2020–2023, exited), Australia (cancelled 2024). Afterpay/Clearpay acquired 31 Jan 2022 ($13.8bn stock); Clearpay exited the EU in 2025.

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