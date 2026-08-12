# VOLUME XIII — THE ABANDONMENT RECORD
## A Forensic Reverse-Engineering of Block, Inc. (NYSE: XYZ, formerly Square, Inc.)

## TL;DR
- Block's abandonment record contains the sharpest natural experiment in fintech: **Square Wallet** (2011–2014, "pay by name" hands-free checkout) failed completely while **Square Cash** — launched almost simultaneously in October 2013 — became Cash App and now generates **$6.34bn of gross profit (FY2025, +21%), roughly 61% of Block's $10.36bn total, with 59 million monthly actives at year-end 2025**. The difference was not concept quality but structure: Cash App solved a one-sided job (send money to a person) that spread pairwise with zero merchant dependency, while Wallet required merchants *and* consumers to change behaviour simultaneously and never cleared the network-effect threshold.
- Read by cause not date, the record shows Block **bought-and-sold-well once (Caviar, a ~$320m+ gain)**, **bought-and-wrote-off once big (TIDAL, effectively a complete ~$206m goodwill write-off)**, killed several **built products cheaply and fast** (Square Wallet/Order, Cash App UK, Verse, Clearpay EU), and ran a cluster of **founder-conviction crypto bets** (TIDAL, TBD/Web5, Proto mining, Bitkey, the bitcoin treasury) whose *process* — a 35-minute committee, no executive support — was demonstrably weaker than the variance in their outcomes.
- Net capital destroyed by the *abandoned* ventures is modest — the Caviar gain roughly offsets the TIDAL write-off and most other kills were cheap — so the honest verdict for a capital-constrained Nigerian founder is not "Block was reckless" but "Block could afford to be wrong, and you cannot": **adopt the killing-fast discipline, adopt Cash App's tested-behaviour rule, and reject acquisition-led growth and founder-conviction bets that no operator will defend.**

## Key Findings

1. **Square Wallet is the most instructive failure in the record** — a genuinely visionary product killed by a structural flaw, not incompetence. Its successor Square Order was killed even faster (10 months). Cash App, launched in the same window, is now the larger half of Block.
2. **The most expensive single failure was TIDAL** — $237.3m paid for 86.23%, effectively a complete goodwill write-off ($132.3m in 2023 + $73.5m in 2024 = $205.8m), acquired via a process a Delaware judge called "by all accounts, a terrible business decision."
3. **Caviar was a genuinely good trade** — bought 2014 (reported ~$90m; a securities filing shows $44.3m), sold to DoorDash for $410m (closed 31 October 2019). This single disposal roughly offsets the TIDAL destruction.
4. **Block kills built products fast and cheap but held its one expensive conviction (TIDAL) slow** — Order died in 10 months, Cash App Australia before launch, but TIDAL absorbed three-plus years and two impairments before being wound down.
5. **Failures cluster in consumer and founder-driven ventures, not in the merchant core.** Square's seller ecosystem has no comparable abandonment; nearly every kill is a consumer product (Wallet, Cash App UK, Verse) or a Dorsey-conviction bet (TIDAL, TBD, Proto).
6. **The governance structure is directly implicated.** Dorsey controls **42.2% of total voting power** (per Block's 2026 proxy) on a high-single-digit economic stake; the TIDAL acquisition and the crypto pivot both followed founder conviction over operator consensus.
7. **The failure rate is normal-to-low for an acquisitive tech company** — against the widely-cited 70–90% M&A failure rate (HBR, 2011), Block's one clean write-off and one clean win is unremarkable, and its experiments were unusually cheap.

## XIII.1 THE SQUARE WALLET CASE

### What it was — Card Case → Pay With Square → Square Wallet
**[CONFIRMED FACT]** Square launched a consumer app called **Square Card Case** in 2011 (a major hands-free update landed November 2011). The concept was radical: a customer filled a virtual "case" with "cards" for merchants who accepted Square, then **paid by name** — walking into a store, saying their name at the till, with the cashier verifying the customer's photo on the merchant's iPad. The November 2011 update added iOS 5 geofencing, so that within 100 metres of a participating merchant a tab opened automatically; the customer "didn't need to pull the phone out at all."

**[CONFIRMED FACT]** Merchant adoption grew fast: Square reported 20,000 merchants (November 2011), over 40,000 (February 2012), and 75,000 (March 2012), when the app was renamed **Pay With Square**, and later **Square Wallet**. Slate (November 2011) captured the ambition: "you go into a store, choose what you want to buy, and then tell the cashier your name. That's it — you've just paid."

### The Starbucks partnership
**[CONFIRMED FACT]** In August 2012 Starbucks invested $25m in Square (part of a Series D that valued Square at $3.25bn), Square became the exclusive processor of credit/debit payments at 7,000-plus US stores, and Starbucks CEO Howard Schultz joined Square's board (he left about a year later). Dorsey called it "an epic partnership."

**[CONFIRMED FACT — from Square's IPO S-1]** The deal was structurally loss-making. Square disclosed in its 2015 IPO filing that it lost roughly **$71m** processing Starbucks payments over three years; the Seattle Times computed accumulated losses of about **$84.5m**. Year-by-year losses: ~$3m (2012), ~$25m (2013), ~$28m (2014), ~$14m (first half 2015). In 2014 Square earned $123m in Starbucks revenue but paid $151m in card-network fees to process it. The economics failed because Starbucks' average ticket was low (~$5) and interchange on small-ticket card payments exceeds Square's thin processing margin.

**[CONFIRMED FACT]** The partnership unwound as Square approached IPO: exclusivity ended 1 October 2015, Square amended the contract to raise its per-transaction take, and the relationship was set to expire in Q3 2016. Starbucks had already stopped accepting Square Order payments in its stores in 2014.

### The discontinuation and Square Order
**[CONFIRMED FACT]** On 12 May 2014 Square pulled Square Wallet from the app stores and replaced it with **Square Order**, an order-ahead-for-pickup app limited to San Francisco and New York. **[COMPANY CLAIM]** A Square spokesperson said: "we wanted to add more value to the experience of paying with name and the most efficient way to do that was to build a new app on a new and more agile platform." **[ANALYTICAL INFERENCE]** This is a euphemism; independent reporting (Recode: "The grand Square Wallet experiment is over") treated it as an admission that Wallet had failed to gain traction.

**[CONFIRMED FACT]** Square Order was itself killed after just 10 months — Square notified users that orders would stop 20 March 2015. Square had introduced an 8% fee on Order transactions in July 2014 (versus its standard 2.75%), far above order-ahead norms. **[COMPANY CLAIM]** Square said it was "focusing" on other tools including gift cards and Caviar. A Javelin analyst called the shutdown "premature."

### What Square Cash did differently
**[CONFIRMED FACT]** Square Cash launched publicly 15 October 2013 (after an invite-only test in May 2013). The mechanism: email a recipient, CC cash@square.com (later pay@square.com), put the dollar amount in the subject line; each party linked a debit card once, and money moved bank-to-bank. It worked from any email client and had companion iOS/Android apps. It was free, and — critically — required no merchant. Walt Mossberg (AllThingsD) called it "the quickest, simplest method I've seen for sending money from one person to another." **[CONFIRMED FACT]** Square Cash became Cash App, which in FY2025 generated $6.34bn of gross profit (+21%), ~61% of Block's $10.36bn total.

### A defensible account of the divergence
**[ANALYTICAL INFERENCE]** The divergence was not primarily one of concept, execution talent, or timing — both products were visionary, well-built, and early. It was a difference in **network-effect topology and behavioural dependency**:
- **Square Wallet required a two-sided behaviour change simultaneously.** For "pay by name" to be worth using, a critical mass of *merchants* had to enable it *and* a critical mass of *consumers* had to prefer it over a card they already carried. The consumer's marginal benefit was tiny (a few seconds saved); the merchant's friction was real (verify photos, learn a new flow). Neither side reached the threshold where the other's participation became compelling. Contactless/NFC and, ultimately, Apple Pay (announced 2014, at Starbucks in 2016) then commoditised the "phone as payment" idea Wallet was built around.
- **Square Cash solved a one-sided job the user already had.** Sending money to a person has no merchant in the loop; the "network" a sender needed was one other person, pulled in by the transaction itself (viral, pairwise adoption). The benefit over cash, cheques or PayPal's clunkier flow was large and immediate. Cash App's later expansion (Cash Card, direct deposit, bitcoin, stock investing, Borrow) was built on a base of habitual person-to-person use it had already secured.

**[ANALYTICAL INFERENCE]** The lesson: **a consumer financial product that depends on merchants changing behaviour to deliver consumer value will stall; one that delivers standalone value to a single user and spreads pairwise will compound.** Wallet's fatal flaw was designed in from day one.

## XIII.2 THE BOUGHT-AND-SOLD-WELL CATEGORY

### Caviar (the one clean win)
**[CONFIRMED FACT]** Square acquired the food-delivery service Caviar in 2014. The purchase price is reported two ways: press consistently cites ~$90m, but a securities filing shows $44.3m — the discrepancy likely reflects headline (including earnouts/stock) versus GAAP-recognised consideration. Square sold Caviar to DoorDash for **$410m** in cash and DoorDash preferred stock; announced 1 August 2019, closed 31 October 2019. Caviar lead Gokul Rajaram and the team moved to DoorDash. Caviar's sub-brand **Fastbite** was shut in 2016. Square had tried to sell Caviar in 2016 (to Uber, GrubHub, Yelp) for ~$100m and failed to find a buyer at that price; the business "reportedly struggled to turn a profit."

**[COMPANY CLAIM]** Dorsey framed the sale as focus — selling Caviar let Square "increase our focus on and investment in our two large, growing ecosystems — one for businesses and one for individuals." **[ANALYTICAL INFERENCE]** Independent reporting (TechCrunch) is blunter: Square "shed an unprofitable arm that looked less and less core," and DoorDash "turned cash and stock into a bit of growth." The realised gain — roughly $320m on the reported cost basis, or ~$366m on the filing basis, before DoorDash stock movement — makes this the single value-creating exit in the record. **VERDICT: a genuinely good trade; the volume says so plainly.**

## XIII.3 THE BOUGHT-AND-WRITTEN-OFF CATEGORY

### TIDAL (the most expensive failure)
**[CONFIRMED FACT]** Block acquired TIDAL on 30 April 2021; final consideration **$237.3m for 86.23%**, held through **Aspiro AB**, **TIDAL Music AS** and **Project Rising LLC**. Original goodwill ~$197.9m. Jay-Z (Shawn Carter) joined Block's board; the artist shareholder group (Beyoncé, Rihanna and others) retained ~13.2%.

**[CONFIRMED FACT — from the derivative suit]** The acquisition process was extraordinarily thin. Per the May 2023 Delaware Chancery ruling by Chancellor Kathaleen McCormick (dismissing the City of Coral Springs Police Officers' Pension Plan suit): Dorsey proposed the deal on a board video call while vacationing with Jay-Z in the Hamptons in summer 2020; the Transaction Committee's first meeting lasted 35 minutes; no other senior Block executive supported the deal. Per Reuters' account of the ruling, "By 2020, Tidal had signed up 2.1 million paying subscribers, compared with Spotify's 138 million, Apple Music's 60 million and Amazon Music's 55 million," alongside ten consecutive quarters of multimillion-dollar losses and a Norwegian criminal investigation into streaming-fraud allegations. The judge called the deal "by all accounts, a terrible business decision." NYU Stern marketing professor **Scott Galloway** — quoted in the shareholder complaint and reported by Bloomberg Law — called it "a $300 million bar tab to hang out with Jay-Z."

**[CONFIRMED FACT — from 10-K goodwill notes]** Block impaired TIDAL goodwill by **$132,313k in Q4 2023** and a further **$73,508k in Q4 2024** — together $205.8m, effectively wiping out the ~$197.9m original goodwill. In late 2024 Block announced it was "scaling back our investment in TIDAL," eliminated product-management and product-marketing functions, and cut ~40 TIDAL staff in December 2024 (a further ~10% cut followed in 2025). Employees were reportedly instructed not to mention Jay-Z on internal channels (Fortune, November 2024). TIDAL still operates as a slimmed-down service under interim head Jesse Dorogusker, with simplified $11.99 Hi-Fi / $19.99 Hi-Fi Plus tiers and Cash App–powered artist tipping (beta September 2024).

### Verse
**[CONFIRMED FACT]** Block acquired the European P2P app Verse on 15 June 2020 (~500,000 users). **Verse Payments Lithuania UAB** was fined €280,000 by the Bank of Lithuania on 10 March 2023 for anti-money-laundering failures. The Verse brand was wound down September 2023 as part of Block's European retreat. **[COMPANY CLAIM]** The CFO said the wind-down would affect monthly actives but "we do not expect an impact to inflows or gross profit" — **[ANALYTICAL INFERENCE]** i.e., after three years Verse had never monetised. **[COMPANY CLAIM]** Dorsey: these operations "required significant investment, and the markets have not seen the growth and profitability we had expected."

## XIII.4 THE BUILT-AND-FAILED CATEGORY

- **Square Card Case / Pay With Square / Square Wallet** — launched 2011, killed 12 May 2014. Concept: hands-free "pay by name." Cause: two-sided behaviour dependency (see XIII.1).
- **Square Order** — launched 12 May 2014, killed ~20 March 2015 (10 months). Order-ahead pickup; 8% fee. Cause: premature, mispriced, no traction.
- **Square Market** — launched 2013 as a free marketplace/online-store product ("open a store for free," 2.75% per item). Superseded by the **Square Online Store** built on Weebly technology after Square acquired **Weebly for ~$365m** (announced 26 April 2018); the legacy product was migrated and later rebranded "Square Online / websites." Not a hard failure — a quiet absorption.
- **Discontinued hardware** — Block confirms that as of 1 September 2025 software updates were discontinued for older hardware versions, including the 1st-generation Square Reader for contactless and chip and the 1st-generation Square Stand; multiple earlier Reader/Stand/Register generations are retired from sale. Normal product-lifecycle churn, not strategic failure.
- **Cash App United Kingdom** — launched 2018 (Cash App's first international market), shut 15 September 2024. **[COMPANY CLAIM]** Stated reason: prioritising the US ("We're focused on growing within the U.S., not expanding into new markets"). **[ANALYTICAL INFERENCE / independent reporting]** Failed to compete against entrenched Revolut, Monzo and Starling. Housed in **Squareup Europe Ltd**.
- **Cash App Australia** — cancelled June 2024 before launch.
- **Clearpay / Afterpay EU** — Clearpay (Afterpay's EU brand, entered via the 2021 ~$50m Pagantis acquisition) began winding down France, Italy and Spain from 27 June 2023, stopped new customers 3 July 2023, and closed the EU operation from **25 August 2023**. (The carried-forward brief cites "~25 August 2025"; contemporaneous City A.M./FashionNetwork reporting places the closure at 25 August 2023 — flagged as a date conflict.)
- **TBD / Web5** — Block's decentralised-web unit, launched June 2022 (Dorsey called Web5 "likely our most important contribution to the internet"). Staff laid off and the unit wound down entirely November 2024; foundational components contributed to the Decentralized Identity Foundation.
- **Verse** — see XIII.3.

## XIII.5 THE FOUNDER-CONVICTION CATEGORY

**[CONFIRMED FACT]** In the Q3 2024 shareholder letter Block said: "We are scaling back our investment in TIDAL and winding down TBD … This gives us room to invest in our bitcoin mining initiative … and Bitkey, our self-custody wallet for bitcoin."

- **TIDAL** — see XIII.3. Founder conviction over operator consensus; ~$206m written off.
- **TBD / Web5** — wound down November 2024; a pure conviction bet with no revenue model that returned nothing but open-source contributions.
- **Spiral** — Block's open-source bitcoin-development subsidiary (formerly Square Crypto); persists as a cost centre funding bitcoin development with no direct return, by design.
- **Proto (bitcoin mining hardware)** — Block completed a 3-nanometer mining chip design in early 2024 and in July 2024 signed its flagship supply deal with **Core Scientific** (~15 EH/s). Core Scientific **booked a $41.9m loss to terminate** the contract, having paid Block ~$67.9m for chips since 2024 ($10m July 2024, $21.3m January 2025, $36.6m January 2026) before exiting in favour of ~$14bn of AMD AI-colocation leases. Core was Proto's first and only named large customer. **[ANALYTICAL INFERENCE]** The collapse of the flagship customer immediately after launch is a serious product-market-fit warning for a business Block explicitly cited as having "strong product market fit."
- **Bitkey** — self-custody hardware wallet, shipping since March 2024; connects to Cash App and Coinbase. Still live; a conviction bet not yet returned.
- **Bitcoin treasury** — Block held ~8,883 BTC at end-2025 and ~9,000+ BTC by Q1 2026 (corporate), plus ~19,357 BTC for customers (~28,355 BTC total, ~$2.2bn). Under the May 2024 "Bitcoin Blueprint" Block reinvests 10% of monthly bitcoin gross profit into BTC. A conviction bet that has largely worked on outcome (BTC appreciation) but belongs analytically in Volume IX.

**[ANALYTICAL INFERENCE]** The pattern reveals a **systematic process weakness, not merely bad luck**: the conviction bets share a signature — proposed or championed by Dorsey personally, thin or absent operator support, and often no revenue model at inception (TBD, Spiral) or a single unproven customer (Proto). The framing note's trap — scoring these only by outcome — is real: bitcoin worked and TIDAL did not, but *both* were decided by the same weak process. A serious assessment judges the process, and the process was poor in both.

## XIII.6 THE STRATEGIC-RETREAT CATEGORY (the abandonments nobody announced)

- **Micro-merchant de-prioritisation** — Square, which built its brand on micro-merchants and the free card reader, has moved upmarket: GPV from mid-market sellers (those >$500,000 annualised) reached **45% of total GPV** (up from 41% two years earlier), growing ~20–22% year on year. PYMNTS calls this "a move away from Square's original DNA as a small merchant enabler." Nobody announced abandoning micro-merchants; the investment simply migrated.
- **Geographic withdrawals** — Cash App UK (2024), Cash App Australia (cancelled 2024), Verse EU (2023), Clearpay EU (2023). A coherent retreat from international consumer expansion, dressed as "prioritising the US."
- **Lending strategy shift** — Volume IX established the move from originate-to-distribute toward retaining the loan book; Square Financial Services received FDIC approval in March 2025 to originate/service Cash App Borrow loans directly (>$27bn originated in the five quarters since).
- **The two-ecosystem organisational model** — Announced at the Q2 2024 earnings call, Block abandoned its two-independent-ecosystems (Square vs Cash App) structure for a single functional organisation. **[COMPANY CLAIM]** Dorsey later admitted: "over-hired during covid because i incorrectly built 2 separate company structures (square & cash app) rather than 1, which we corrected mid 2024." A rare public admission that a core organising principle was a mistake. It culminated in the February 2026 cut of ~40%+ of the workforce (restructuring charges ~$852m) and Dorsey's stated ambition of a near-flat, AI-mediated organisation.

## XIII.7 THE CAPITAL ARITHMETIC

**[ANALYTICAL INFERENCE — assembled from the confirmed figures above]**

**Capital deployed into subsequently-abandoned ventures (identifiable):**
- TIDAL: $237.3m acquisition consideration.
- Verse: undisclosed (within a ~$253.7m 2021 "other acquisitions" bucket; small) — UNKNOWN precise.
- Starbucks partnership: not an acquisition but a deliberate loss-leader; ~$84.5m accumulated processing losses (net of the $25m investment received, ~$60m net drag).
- Caviar: $44.3m (filing) to ~$90m (reported).
- Clearpay EU (Pagantis): ~$50m.
- Square Wallet / Card Case / Order / TBD / Spiral / Proto R&D: development and operating costs — UNKNOWN, though Proto's chip programme was material.

**Capital recovered:**
- Caviar: $410m (cash + DoorDash preferred) — gain ~$320m (reported basis) to ~$366m (filing basis).
- Starbucks: $25m equity investment received, plus non-cash brand exposure.
- Proto: Block *received* ~$67.9m from Core Scientific (Block was the seller); the $41.9m loss was Core's, not Block's — though Block loses the future revenue stream.

**Write-offs by year (goodwill impairment, TIDAL):** $132.3m (FY2023) + $73.5m (FY2024) = $205.8m.

**Net destruction (abandoned ventures only):** The TIDAL write-off (~$206m) plus the Starbucks net drag (~$60m) plus Clearpay/Verse (tens of millions) is **substantially offset by the ~$320m+ Caviar gain**. On the identifiable items, the abandonment record is close to **net-neutral to modestly value-creating**, before unquantified R&D on Wallet/Order/TBD/Proto. Expressed against gross profit, even the gross TIDAL write-off (~$206m) is **~2% of FY2025 gross profit ($10.36bn)** and a fraction of a percent of capital deployed over the period.

**Critical exclusion:** This excludes **Afterpay**, whose valuation collapsed from a $29bn announced / $13.9bn closing price with Australian writedowns of $12.2bn since 2023. Afterpay is *not* abandoned — it is now core to Cash App's BNPL — so it belongs in Volume IX. Including it would swamp every other number: the abandonment record proper is cheap; the *retained* acquisition (Afterpay) is where the largest paper destruction sits.

**Benchmarking.** **[THIRD-PARTY ESTIMATE]** Against the most-cited finding that the M&A failure rate is "between 70% and 90%" (Clayton Christensen et al., *Harvard Business Review*, March 2011: "companies spend more than $2 trillion on acquisitions every year, yet the M&A failure rate is between 70% and 90%") — corroborated by KPMG's 1999 finding that 83% of deals failed to enhance shareholder value — Block's acquisition record (one clean write-off in TIDAL, one clean win in Caviar, one massively-impaired-but-retained bet in Afterpay) is **normal to unusually disciplined on the abandonment axis**. Comparable tech write-offs dwarf Block's: **HP/Autonomy ($8.8bn, 2012)**, **Microsoft/Nokia ($7.6bn, 2015 — exceeding the purchase price)**, **eBay/Skype ($1.4bn, 2007)**. Academic evidence (Potepa & Thomas, *Journal of Financial Reporting*, 2023) finds 65% of "at-risk" large acquisitions impair within two years — TIDAL is a textbook member of that set. **[ANALYTICAL INFERENCE]** The dominant pattern is **cheap experiments quickly killed** (Wallet, Order, Cash App UK/AU, Verse, Clearpay, TBD), with a single **expensive conviction held too long** (TIDAL). Proto is a partial exception — a conviction bet whose cost is R&D rather than a write-off, and whose flagship customer has now exited.

## XIII.8 THE PATTERN

**[ANALYTICAL INFERENCE]**
- **Fast or slow?** Block kills *built products* fast (Order in 10 months, Cash App Australia before launch, Cash App UK once the US-focus decision was taken) but held its one *acquired conviction* (TIDAL) slow — three-plus years and two impairments before winding down. Cheap things die fast; founder-beloved things die slow.
- **Acquisitions vs built products?** The most expensive failures are acquisitions (TIDAL; and, if counted, Afterpay's paper loss). The built-product failures were comparatively cheap — but failed *more often*.
- **Consumer vs merchant?** Failures cluster overwhelmingly in **consumer** (Wallet, Cash App UK/AU, Verse) and **crypto/founder** (TIDAL, TBD, Proto) products. The **Square merchant core has essentially no abandonment record** — its only "retreat" is the quiet, deliberate, value-accretive move upmarket.
- **Founder vs operator?** Failures cluster in **founder-driven** ventures. The two-ecosystem reorganisation and TIDAL were Dorsey's; both were reversed or written off.
- **Does the company learn?** Partially. Killing Verse and Cash App UK quickly, and admitting the two-ecosystem structure was a mistake, are evidence of learning. But the *same weak conviction-process* recurs (TIDAL → TBD → Proto), suggesting Block learns to *exit* faster than it learns to *not enter*.
- **Governance.** Dorsey's **42.2% voting control** (2026 proxy) on a high-single-digit economic stake is directly implicated. The dual-class structure let a 35-minute committee and a founder's personal enthusiasm commit $237m to TIDAL over unanimous executive scepticism, and let the crypto pivot proceed. Dual-class control is what *permits* the conviction bets; it is also what *insulates* the founder from the discipline that would have caught them. The record is the price of that insulation — a price Block, with $10bn+ of gross profit, can pay.

## XIII.9 THE TRANSPLANT VERDICTS

**1. The consumer-product lesson (Square Wallet vs Square Cash).**
- **Verdict: ADOPT the rule, ADAPT the sequencing.** What distinguishes a working consumer financial product from a failing one is whether it delivers standalone value to a single user and spreads pairwise, versus requiring two sides to change behaviour at once. For the Nigerian cooperative context, a member-to-member transfer / remittance feature (one-sided, pairwise, viral) is the Cash App analogue and should be built first; a "pay by name at the cooperative store" merchant-acceptance play is the Wallet analogue and should be deferred until members *already* transact densely. The Guinnane question: Wallet failed because of the *mechanism* (two-sided dependency), not the environment — so it would fail in Nigeria too. **REJECT merchant-dependent consumer payments as a first move; ADOPT the money-movement primitive.**

**2. Acquisition as a growth strategy for a capital-constrained founder.**
- **Verdict: REJECT.** Volume IX already leaned against it; the abandonment record confirms it. Block's *good* acquisition (Caviar) worked partly because Block could afford to hold an unprofitable asset for five years and wait for a buyer war; its *bad* one (TIDAL) cost $237m it could absorb. A capital-constrained founder has neither the holding power nor the loss-absorption. Mechanism vs environment: acquisition failure is a mechanism problem (integration risk, overpayment) amplified by a capital-constrained environment. **Build, partner, or license; do not acquire.**

**3. Founder-conviction ventures under a cooperative structure.**
- **Verdict: ADOPT strict discipline / REJECT unaccountable conviction.** A cooperative's members are owners of a different kind, and the founder has *no* dual-class insulation — a feature, not a bug. The discipline Block lacked (an operator veto; a revenue model at inception; more than a 35-minute review) must be *institutionalised* in the cooperative's governance precisely because the founder cannot override members. Require every new venture to name (a) the tested user job, (b) the revenue model at inception, and (c) at least one senior operator willing to stake their reputation on it — the TIDAL test Block failed.

**4. Killing fast versus holding on.**
- **Verdict: ADOPT killing fast.** The record teaches that cheap, fast kills (Order, Cash App UK) cost little and that the one slow death (TIDAL) cost the most. A founder with one shot should pre-commit to kill criteria *before* launch (e.g., "if member weekly-active rate is below X% after two quarters, we stop"), and be especially ruthless with anything the founder personally loves — that is exactly what Block held too long.

**5. Building for a market you have not tested.**
- **Verdict: ADOPT a testable discipline.** Cash App UK, Verse and Square Wallet all failed at least partly on untested assumptions about user behaviour (that UK users would switch from Revolut/Monzo; that Verse users would monetise; that consumers would prefer pay-by-name to a card). The catchable discipline: **run a falsifiable behavioural pre-test in the actual target market before committing capital** — a small pilot with real members measuring the specific behaviour the business depends on, with a pre-agreed threshold. Every one of these three failures would have been caught by a cheap pilot with a kill threshold.

## XIII.10 VOLUME XIII RECONSTRUCTION

1. **The Square Wallet case and its verdict.** A visionary two-sided product killed by designed-in network dependency; its simultaneous sibling Square Cash, a one-sided pairwise primitive, became 61% of Block. **Verdict: build the one-sided money primitive; defer merchant-dependent consumer payments.**
2. **The five-category catalogue (in full).**
   - *Bought and sold well:* Caviar (2014, ~$44.3–90m → $410m, 2019); Fastbite shut 2016.
   - *Bought and written off:* TIDAL ($237.3m, $205.8m impaired); Verse (2020, wound down 2023, €280k AML fine).
   - *Built and failed:* Square Card Case/Wallet (2011–2014); Square Order (2014–2015); Square Market (absorbed into Weebly-based Online Store); Cash App UK (2018–2024); Cash App Australia (cancelled 2024); Clearpay EU (2023); TBD/Web5 (2022–2024); legacy hardware retirements.
   - *Founder-conviction:* TIDAL; TBD; Spiral; Proto (Core Scientific $41.9m termination); Bitkey; bitcoin treasury.
   - *Strategic retreats:* micro-merchant de-prioritisation (mid-market now 45% of GPV); international withdrawals; lending shift; abandonment of the two-ecosystem model (2024).
3. **Capital arithmetic.** Gross TIDAL write-off ~$206m ≈ 2% of FY2025 gross profit; roughly offset by the ~$320m+ Caviar gain. Net abandonment destruction is modest; Afterpay's ~$12bn+ paper loss is excluded as *retained*, not abandoned. Failure rate is normal-to-disciplined versus the 70–90% M&A benchmark.
4. **Pattern.** Kills built products fast, held its one founder-conviction acquisition slow; failures cluster in consumer and founder-driven ventures; the merchant core is clean; dual-class control (42.2% of the vote) both enabled the bets and insulated them from discipline.
5. **Transplant verdict table.** Consumer primitive: ADOPT/ADAPT. Acquisition-led growth: REJECT. Unaccountable founder conviction: REJECT; institutionalised discipline: ADOPT. Killing fast: ADOPT. Untested-market building: ADOPT pre-test discipline.
6. **Key unknowns.** Exact Verse purchase price; total Wallet/Order/TBD/Proto R&D spend; Proto's own booked losses on Block's side; precise all-in Starbucks cost; the Clearpay-EU-closure date discrepancy (2023 vs the carried-forward 2025).
7. **Ten most important conclusions.**
   1. The Wallet/Cash divergence is the record's central lesson: one-sided pairwise value beats two-sided behaviour change.
   2. TIDAL is the most expensive failure (~$206m written off) and the most instructive on *process* (35-minute review, no operator support).
   3. Caviar is a genuinely good trade and roughly pays for TIDAL.
   4. Block kills cheap things fast and beloved things slow.
   5. Failures cluster in consumer and founder-driven bets; the merchant core is clean.
   6. The conviction bets share one weak process; bitcoin's success and TIDAL's failure came from the *same* process.
   7. The abandonment record is cheap in absolute terms and disciplined versus benchmarks — but only because Block could afford to be wrong.
   8. Dual-class control both enabled and insulated the failures.
   9. Killing Verse/Cash App UK fast, and admitting the two-ecosystem error, are real evidence of learning to *exit*.
   10. The transplant lesson is asymmetric: a one-shot founder should copy Block's exits and reject Block's entries.

**The central answers.** *What did Block abandon and why?* A consumer wallet (network failure), a music service and a decentralised-web unit and a European P2P app (founder conviction / no monetisation), several international consumer operations (competitive defeat dressed as US focus), and its own two-ecosystem structure (admitted error). *Most expensive?* TIDAL. *Most instructive?* Square Wallet. *Fast or slow?* Fast on cheap built products, slow on the one beloved acquisition. *Governance?* Dual-class control (42.2% of the vote) let founder conviction commit capital over operator scepticism and insulated it from correction. *What should a capital-constrained founder take from a record of failures made by a company that could afford them?* **Copy the exits, not the entries.** Build one-sided, tested, pairwise money primitives; pre-commit kill thresholds; refuse acquisition-led growth; and institutionalise the operator-veto and revenue-at-inception discipline that Block's dual-class insulation let it skip — because you cannot afford a single TIDAL, and Block's own record proves the TIDAL was avoidable at the point of entry, not merely at the point of exit.

## Recommendations (staged, with thresholds)

**Stage 0 — before building anything (now).** Institutionalise, in the cooperative's charter, the three-part venture gate that would have caught TIDAL, Verse and Cash App UK: (a) a named, tested user job; (b) a revenue model at inception; (c) a named senior operator (not the founder) who will stake reputation on it. *Threshold to proceed:* all three present, in writing, reviewed for more than one meeting.

**Stage 1 — the first consumer product.** Build the one-sided money-movement primitive (member-to-member transfer / remittance), not a merchant-acceptance product. *Benchmark that would change this:* only after ≥40–50% of members are transacting weekly should a merchant "pay at the co-op store" feature be attempted — the density Wallet never reached.

**Stage 2 — every subsequent product.** Run a falsifiable in-market behavioural pilot before full capital commitment, with a pre-agreed kill threshold. *Threshold to kill:* if the specific behaviour the business depends on (e.g., repeat weekly use, or paid conversion) misses the pre-set bar after two quarters, stop — as Block did with Order and Cash App UK, not as it did with TIDAL.

**Stage 3 — growth.** Grow by building and partnering, not acquiring. *Benchmark that would change this:* revisit acquisition only if the group has both (i) ≥12 months of loss-absorbing capital buffer and (ii) an integration owner — conditions Block met and you likely will not for years.

**Standing rule.** Apply extra scrutiny, not less, to any venture the founder personally loves. The record's clearest governance lesson is that founder conviction is where the expensive, slow failures live.

## Caveats
- **Stated reasons are COMPANY CLAIM.** "Prioritising the United States" and "shifting resources to higher-return areas" are corporate formulations; independent reporting attributes Cash App UK's failure to Revolut/Monzo/Starling competition and Verse's to non-monetisation.
- **The Clearpay EU closure date conflicts** (contemporaneous reporting: 25 August 2023; carried-forward brief: ~25 August 2025). Flagged, not silently resolved.
- **Several costs are UNKNOWN** — Verse's price, R&D on Wallet/Order/TBD/Proto, Block's own Proto losses, all-in Starbucks cost.
- **Afterpay is deliberately excluded** from the abandonment arithmetic as a retained (not abandoned) asset; its ~$12bn+ paper destruction belongs to Volume IX.
- **The M&A failure-rate benchmark (70–90%) has a definitional range** — "failure" variously means stock decline, missed synergies, or divestiture — so it anchors judgement rather than proving a precise comparison.
- **Caviar's cost basis is genuinely ambiguous** (reported ~$90m vs filing $44.3m); the realised-gain range reflects this, not analyst imprecision.