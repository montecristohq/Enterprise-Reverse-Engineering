# VOLUME IV — KLARNA: Financial Statements, Revenue Architecture, Credit Economics, Unit Economics, Regulatory Capital & Capital Allocation

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