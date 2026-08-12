# EXPERIAN REVERSE-ENGINEERING FORENSIC (EREF) — VOLUME IV
## Financial Statements, Revenue Architecture, Unit Economics & Capital

*Basis convention (binding): Experian reports under IFRS in US dollars with a 31 March year-end. "Benchmark" denotes the company's non-GAAP suite (Benchmark EBIT, Benchmark PBT, Benchmark EBITDA, Benchmark EPS). Every figure below is labelled statutory or Benchmark, and every growth rate is labelled organic / constant-currency (CER) / actual-rate. FY26 = year to 31 March 2026; FY25 = year to 31 March 2025; and so on. Evidence tags: CONFIRMED FACT, COMPANY CLAIM, THIRD-PARTY ESTIMATE, ANALYTICAL INFERENCE, HYPOTHESIS, UNKNOWN. Arithmetic is shown for every derived figure so the reader can audit it.*

---

## TL;DR (the core answer)

- **The 28.6% Benchmark EBIT margin is not made by a free input; it is manufactured by three things: oligopolistic pricing power in a three-firm US bureau market, operating leverage over a largely fixed data-and-compliance platform, and net (agent) revenue recognition on the consumer marketplace. FY26 profitability is *mostly* structural but is flattered by a non-durable US mortgage pricing windfall (mortgage revenue +45% on roughly flat volume) and depressed by cloud dual-run costs that roll off from FY27 — the two roughly offsetting.**
- **The Benchmark presentation is broadly fair on volatile financing items but flattering on the amortisation of acquisition intangibles (US$271m in FY26 and rising every year), which — for a company that acquires continuously — is in substance a permanent cost of strategy excluded from the headline number the market prices.** Thirty years of acquisition created clear value in the core (North America, Latin America and UK cash-generating units have never been impaired) but destroyed roughly US$232m of goodwill at the margin in EMEA/Asia Pacific (US$53m impaired in FY21, US$179m in FY23).
- **The single variable that most determines earnings is US Financial Services inquiry pricing, above all mortgage. Growth is capital-light organically but capital-heavy through M&A (US$792m in FY26) and an 8.6%-of-revenue capex load — so the "capital-light information business" label is only half true.** ROCE of 17.2% comfortably exceeds the ~8–9% cost of capital, and leverage of 1.7x net-debt/EBITDA sits below the 2.0–2.5x target range, leaving ample capacity for both buybacks and deals.

---

## Key Findings

1. **Scale and shape (FY26, CONFIRMED):** statutory revenue US$8,445m (+12% actual); ongoing revenue US$8,425m (+13% actual, +11% CER, +8% organic); Benchmark EBIT from ongoing activities US$2,407m at 28.6% margin; statutory operating profit US$2,045m; Benchmark PBT US$2,212m; statutory PBT US$1,951m (+26%); Benchmark EPS 179.8 US cents (+15% actual); statutory basic EPS 164.5 US cents (+29%); Benchmark operating cash flow US$2,221m at 93% conversion; Benchmark free cash flow US$1,583m; ROCE 17.2%; net debt US$5,179m at 1.7x Benchmark EBITDA.

2. **The margin is a mix story, not an input story.** North America (66.3% of revenue) earns 34.2%; EMEA/Asia Pacific earns 6.7%. The dispersion is driven by fixed-cost absorption, not pricing — the same data/platform cost base spread over vastly different revenue.

3. **The FY26 mortgage windfall is a pricing event, not a franchise event, and it is politically exposed.** FICO's foundational tri-merge score price rose from US$1.80 (late 2022) to US$30 (2026) — a 1,567% increase per the Community Home Lenders of America — and total per-loan credit-report cost rose from about US$50 in 2022 to roughly US$540 in 2026. Experian captured bureau/reseller mark-up on top of the US$4.95 FICO royalty pass-through.

4. **Benchmark-to-statutory gap is persistent and partly structural.** The FY26 bridge from Benchmark PBT US$2,212m to statutory PBT US$1,951m is a US$261m deduction, dominated by acquisition-intangible amortisation (US$271m) — an item that has risen every year (US$174m FY22 → US$211m FY25 → US$271m FY26) because the company acquires every year.

5. **The acquisition programme is value-creating in the core and value-destructive at the edge.** Acquired goodwill has been impaired only twice in ~15 years, both in EMEA/Asia Pacific (US$53m FY21, US$179m FY23); the North America, Latin America and UK cash-generating units have never been impaired.

6. **The regulatory paradox is financial, not merely legal.** The dispute machinery the CFPB alleges is inadequate is deliberately run at very low unit cost (as low as US$0.57 per dispute letter across >12 million disputes a year), and that low cost is itself a contributor to the near-30% margin. Mandated remediation is the single most material adverse contingency, more than any fine.

---

## Details

### IV.1 Multi-Year Financial History

**Statutory revenue (US$m, actual rates) [CONFIRMED — company results; older years via Macrotrends]:** FY19 4,861; FY20 5,179; FY21 5,372; FY22 6,288; FY23 6,619; FY24 7,097; FY25 7,523; FY26 8,445. Compound growth FY19→FY26 ≈ 8.2% p.a. (8,445 / 4,861 = 1.737 over 7 years → 1.737^(1/7) − 1 = 8.2%).

**Statutory profit before tax (US$m) [CONFIRMED]:** FY20 942; FY21 1,077; FY22 1,447; FY23 1,174; FY24 1,551; FY25 1,549; FY26 1,951. The FY23 dip reflects a US$179m EMEA goodwill impairment and adverse financing remeasurements; the FY26 jump reflects revenue growth plus a swing in financing fair-value remeasurements from −US$85m (FY25) to +US$101m (FY26) and lower restructuring.

**Benchmark EBIT margin (ongoing) [CONFIRMED]:** FY22 ≈26.2%; FY24 27.6%; FY25 28.1%; FY26 28.6%. A steady ~50–90bps annual climb, management-attributed to operating leverage, AI productivity and Consumer Services scaling.

**Benchmark EPS (US cents) [CONFIRMED]:** FY22 124.5; FY24 144.2; FY25 156.9; FY26 179.8. **Statutory basic EPS (US cents):** FY22 127.5; FY25 127.6; FY26 164.5.

**Benchmark EBITDA (US$m) [CONFIRMED, company cash-flow summary]:** FY25 2,630; FY26 3,010 (Benchmark EBIT 2,397 + amortisation/depreciation 613).

**ROCE (post-tax, Benchmark) [CONFIRMED]:** FY24 ~17%; FY25 16.6%; FY26 17.2%. **Net debt/Benchmark EBITDA [CONFIRMED]:** 1.7x in FY24, FY25 and FY26.

**Structural vs presentational:** The 2020–2022 US mortgage boom lifted transactional bureau revenue; the 2023–2025 rate-driven bust cut volumes, but from FY24 Experian offset volume weakness with tri-merge price escalation. Two FY26 presentational changes must be separated from economics: (a) certain Latin America and EMEA/AP B2B lines were reclassified as "exited activities" (US$20m revenue in FY26 vs US$48m in FY25, with a US$10m operating loss removed to arrive at ongoing Benchmark EBIT of US$2,407m vs total US$2,397m); and (b) from 1 April 2025 the B2B line was split into Financial Services and Verticals. Neither changes the underlying economics.

### IV.2 Revenue Taxonomy and Quality

FY26 ongoing revenue US$8,425m [CONFIRMED, Appendix 2]: **B2B US$6,168m** (Financial Services US$4,463m; Verticals US$1,705m) and **Consumer Services US$2,257m**. By region: North America US$5,587m; Latin America US$1,297m; UK & Ireland US$942m; EMEA & Asia Pacific US$599m (sums to 8,425; North America = 5,587/8,425 = 66.3%).

Quality scorecard by stream:
- **Subscription / contracted platform (Ascend, PowerCurve)** — payer: enterprise; trigger: contract; recurring; low cyclicality; highest quality. In FY26 there was a 100% renewal rate among top North America strategic accounts, with durations extended by nearly 10% to over four years and contract values up double digits on average [COMPANY CLAIM]. Over 2,300 client solutions implemented on Ascend; US$2bn of FY26 revenue from "new and scaling products" including Ascend modules and marketplaces [COMPANY CLAIM].
- **Per-inquiry transactional bureau** — payer: lender; trigger: origination/permissible-purpose pull; cyclical; the primary exposure to the US mortgage and consumer-credit cycle.
- **Batch / prescreen** — semi-recurring, tied to marketing spend cycles.
- **Consumer subscription** — recurring but slower ("membership revenue grew modestly" in North America).
- **Marketplace / referral** — performance-based, recognised **net**; now the primary driver of Consumer Services growth (North America marketplace +20%+; UK double-digit every quarter).
- **Experian Health** — recurring, AI-led growth (Patient Access Curator, ~30% denial reduction).
- **Automotive** — grew "well ahead of underlying auto sales"; AutoCheck now exclusive at almost every major US consumer shopping site.
- **Serasa (Brazil)** — consumer marketplace + Limpa Nome (US$19.4bn of debt renegotiated, US$16.1bn written off in FY26; 30m+ agreements renegotiated).
- **illion (ANZ)** — bureau, within EMEA/AP; "near doubling of regional margins."

**Recurring vs transactional [ANALYTICAL INFERENCE]:** roughly two-thirds of group revenue is recurring/contracted or subscription/marketplace-like; the transactional remainder concentrates the cyclical risk in US Financial Services. The FY26 mortgage windfall (see IV.4) is the clearest single example of transactional fragility disguised as growth.

### IV.3 Revenue Recognition and Accounting Judgements

[CONFIRMED, Revenue note]: Per-transaction bureau revenue is recognised at the point of delivery. Hosted software licences are recognised over the service period, creating contract liabilities; on-premise licences are released on delivery completion; support/maintenance is released over the maintenance term. **Consumer Services marketplace and referral revenue is recognised NET** — Experian acts as an agent, recognising only the referral/commission fee, not the gross value of the credit or insurance product placed. This is material: gross presentation would inflate reported revenue and depress the reported margin; net presentation is a structural reason Consumer Services shows a 29.6% Benchmark EBIT margin. The **FICO royalty (US$4.95/score under the mortgage performance model, or US$10 traditional) is a genuine cost of sale / pass-through** [CONFIRMED, FICO]. The accounting judgements that most affect reported results are: (1) the value and economic life of acquisition intangibles (drives the amortisation excluded from Benchmark); (2) the capitalisation and amortisation life of internally generated software (3–10 years, average ~5); and (3) the principal-vs-agent (gross/net) marketplace judgement.

### IV.4 Pricing Economics and the Mortgage Question

**Mechanism:** a conforming mortgage requires a "tri-merge" — a pull from all three bureaus. Per the Community Home Lenders of America (March 2026 white-paper addendum), *"FICO's foundational price for a tri-merge score escalated from $1.80 in late 2022 to $30 today, marking a 1,567% increase,"* while *"total credit report costs associated with closing a conventional loan have risen from about $50 in 2022 to roughly $540 in 2026"* [CONFIRMED, CHLA via HousingWire / NMP]. FICO's own disclosure: the wholesale royalty is US$4.95/score under the performance model (plus a US$33 per-borrower funded-loan fee) or US$10/score traditional; FICO states that *"any amounts charged beyond … FICO's $4.95 per-score royalty … is collected by the credit bureaus or other parties but not by FICO"* [CONFIRMED]. So the escalation captured by Experian is the **bureau mark-up and reseller bundle**, not the FICO royalty.

**FY26 outcome:** North America mortgage-profile revenue grew ~45% (management indicated "45% to 50%") on roughly flat volumes — a near-pure pricing effect [CONFIRMED]. This sits inside North America Financial Services (FY26 US$2,363m, +14% total).

**Competitive/regulatory threat:** the FHFA authorised VantageScore 4.0 for conforming mortgages on 8 July 2025 [CONFIRMED]. By the Q1 FY27 update, per CFO Lloyd Pitchford, *"eleven out of the 15 largest mortgage lenders are also using VantageScore 4.0, now reaching close to 30% of the U.S. mortgage market"* [COMPANY CLAIM]. Deep Future Analytics, in its study "Economic Benefits of Score Market Competition for Conforming Mortgages" (Feb 25 2026), estimated *"an estimated $648 million in savings in the first full year"* under full adoption and *"up to $2.5 billion in cumulative cost savings over a five-year period,"* with a March 18 2026 update raising the first-year figure to *"more than $930 million"* [THIRD-PARTY ESTIMATE].

**Scenario read [ANALYTICAL INFERENCE]:** (i) *Price normalisation* would reverse much of the FY26 uplift and is the single biggest threat to the FY26 growth optics; (ii) *volume recovery* would partly offset — management guides modestly lower mortgage volumes into FY27; (iii) *VantageScore share gain* is largely neutral-to-modestly-negative for Experian because Experian sells both scores and the underlying data pull persists regardless of which score is calculated — the economics that shift are chiefly FICO's royalty, not Experian's bureau revenue. The durable risk is political: a per-loan cost of ~US$540 on a government-sponsored mortgage market is an obvious target for the FHFA, the MBA and the CHLA.

**Beyond mortgage:** the same pricing muscle appears in analytics/platform renewals (double-digit contract-value uplifts) and Serasa. Pricing power derives from the difficulty of replicating regulated historical datasets, switching costs once embedded in a client's decisioning workflow, and the three-firm structure of the US bureau market.

### IV.5 The Cost Architecture of a Zero-Input-Cost Business [PRIORITY DEPTH]

FY26 total operating expenses: statutory US$6,400m; Benchmark US$6,052m [CONFIRMED, Group income statement]. The statutory income statement discloses the cost base by nature (US$m, statutory / of which Benchmark):

| Cost category | Statutory | Benchmark | % of revenue (Benchmark) | Variability |
|---|---|---|---|---|
| Labour | 2,731 | 2,686 | 31.8% | Variable → semi-variable |
| Data & IT | 1,625 | 1,625 | 19.2% | Increasingly fixed platform |
| Amortisation & depreciation | 876 | 613 | 7.3% | Fixed |
| Marketing & customer acquisition | 596 | 596 | 7.1% | Variable / discretionary |
| Other operating charges | 572 | 532 | 6.3% | Semi-variable |
| **Total operating expenses** | **6,400** | **6,052** | **71.7%** | |

Rebuilt from first principles into the components the task demands:

- **Labour — US$2,686m (31.8% of revenue) [CONFIRMED].** The largest cost and the swing factor in margin. Management states labour is "over 300 basis points lower than two years ago," attributed to AI (a claimed 10–15% coding-productivity uplift in FY26, 30%+ in select areas). Functionally it spans engineering, data operations, sales, dispute processing and corporate; geographically it is weighted to the US, UK, Brazil and India (India being the lowest-cost engineering/operations hub). Semi-variable: headcount (~25,200 across 33 countries) flexes with volume but slowly.
- **Technology and cloud — the bulk of Data & IT US$1,625m [CONFIRMED].** Includes the 10-year AWS agreement (announced 19 June 2025), the *dual-run* cost of operating legacy data centres alongside cloud during migration, data-centre exit costs, and embedded software amortisation. Cloud migration is "largely completed" in North America and Brazil (ex-Health); dual-run costs "begin to decline" from FY27 — a step-down that management links to ~+50bps of FY27 margin. This is now largely a **fixed platform cost**, which is precisely why incremental revenue drops through at high margin.
- **Data operations and matching [ANALYTICAL INFERENCE, embedded in Data & IT].** The cost of ingesting ~1.3 billion monthly updates and running the matching engine; management claims a 60% reduction in data-processing time from the cloud transformation. Largely fixed/step-fixed.
- **The dispute and consumer-rights machinery [CONFIRMED cost driver; UNKNOWN precise line].** Over 12 million disputes a year, coded into ACDVs and routed via e-OSCAR, at reported vendor economics as low as US$0.57 per dispute letter. Direct cost is trivial relative to revenue; the *risk-adjusted* cost (litigation + the CFPB matter) is disproportionately large. This sits within "Other operating charges."
- **Model development and third-party score royalties [CONFIRMED].** Internal model development is largely capitalised (see IV.9). The **FICO royalty is a genuine variable cost of sale** embedded in Data & IT / cost of sale, rising with mortgage score volume.
- **Consumer acquisition and marketing — US$596m (7.1%) [CONFIRMED].** The cost of acquiring and servicing 215m free members and converting a fraction to paid or marketplace revenue. This is the most discretionary/variable line and is concentrated in Consumer Services.
- **Regulatory, compliance and legal overhead [ANALYTICAL INFERENCE, within Other operating charges + Labour].** The cost of operating simultaneously under FCRA, UK GDPR, LGPD and multiple US state regimes. Not separately disclosed, but the FY26 non-benchmark labour charge of US$45m and non-benchmark other operating charges of US$40m give a sense of the restructuring/one-off overlay.

**Central question — if the raw material is free, what determines the margin?** Three levers: (1) **operating leverage** over a fixed data/platform/compliance cost base — the dominant lever, and the reason a pricing windfall drops almost entirely to EBIT; (2) **labour productivity** (the 300bps of labour-cost reduction is the visible margin engine); and (3) **mix** — high-margin North America bureau/platform and net-recognised Consumer marketplace versus sub-scale EMEA/AP. Margin *compresses* if wage inflation outpaces productivity, if cloud dual-run overruns, if compliance/remediation steps up (the CFPB tail), or if mix shifts toward low-margin regions or gross-recognised products.

**Why North America earns 34.2% and EMEA/AP 6.7% — a cost-structure explanation, not a pricing one:** both regions must carry a broadly fixed data-ingestion, matching, platform and compliance stack. North America spreads that stack over US$5,587m of revenue; EMEA/AP spreads a similar-in-kind (if smaller) stack over US$599m. The fixed cost per revenue dollar is therefore an order of magnitude higher in EMEA/AP, which is why integrating illion (adding scale) nearly doubled EMEA/AP margin from 3.4% to 6.7% in a single year.

### IV.6 Unit Economics Across Incompatible Units

All arithmetic shown [ANALYTICAL INFERENCE unless the input is CONFIRMED]:

| Candidate unit | Computation | Result | Verdict |
|---|---|---|---|
| Revenue per employee | 8,445 / 25,200 | **US$335,119** | Useful efficiency gauge; rising with AI |
| Benchmark EBIT per employee | 2,397 / 25,200 | US$95,119 | Confirms high value-add per head |
| Revenue per free member (group) | 8,445 / 215m | US$39 | Misleading |
| Consumer Services revenue per free member | 2,257 / 215m | **US$10.50/member/yr** | Misleading in isolation |
| North America members | — | 85m (+8%) | Asset metric, not revenue metric |
| Revenue per marketplace referral | Confidential fee | **UNKNOWN** | Not publicly derivable |
| Revenue per credit inquiry | Confidential pricing | **UNKNOWN** | Not publicly derivable |

**Which unit governs?** None of the per-member or per-file metrics govern. The economics are governed by (1) the **enterprise B2B relationship** — the renewing, multi-year strategic account with double-digit contract-value uplift and a four-year duration — and (2) the **per-inquiry bureau pull priced to the cycle**. Per-member and per-file metrics mislead because the overwhelming majority of the 215m free members and the hundreds of millions of consumer files generate little or no *direct* revenue. Their value is that they constitute the proprietary data asset and consumer flywheel that (a) makes the B2B data saleable, (b) feeds the marketplace, and (c) makes the whole enterprise strategically defensible. They are the asset, not the unit of sale.

### IV.7 Segment Economics

FY26 Benchmark EBIT and margin (ongoing) [CONFIRMED, income-statement analysis]:

| Segment | Revenue US$m | Benchmark EBIT US$m | Margin |
|---|---|---|---|
| North America | 5,587 | 1,912 | 34.2% |
| Latin America | 1,297 | 399 | 30.8% |
| UK & Ireland | 942 | 220 | 23.4% |
| EMEA & Asia Pacific | 599 | 40 | 6.7% |
| Central corporate costs | — | (164) | — |
| **Ongoing group** | **8,425** | **2,407** | **28.6%** |

By line: B2B US$6,168m at 30.9%; Consumer Services US$2,257m at 29.6% (+220bps YoY, +~500bps over two years). North America margin rose 80bps to 34.2%; Latin America fell 120bps to 30.8% (acquisition dilution from ClearSale/TEx/SalaryFits/CCFacil); UK & Ireland 23.2%→23.4%; EMEA/AP 3.4%→6.7% (illion integration, completed 30 September 2024).

**Is EMEA/AP sub-scale, disadvantaged or being restructured? All three.** It is structurally sub-scale (fixed cost over small revenue); it is being deliberately restructured (the exited-activities re-presentation removed a US$10m-loss tail); and it is being consolidated up via illion. Management's actions signal a decision to reach scale by acquisition in ANZ while exiting the weakest lines elsewhere. **Do headline margins conceal structurally different businesses? Yes** — a dominant ultra-high-margin North America bureau/platform; a high-margin but FX-exposed Brazilian franchise; a mature, low-growth UK; and a still-emerging EMEA/AP. The 28.6% group number is a weighted average of four quite different economic entities.

### IV.8 The Statutory-to-Benchmark Forensic Reconciliation [PRIORITY DEPTH]

FY26 and FY25 bridge, Benchmark PBT → statutory PBT (US$m) [CONFIRMED, income-statement analysis]:

| Reconciling item | FY26 | FY25 | Recurring? |
|---|---|---|---|
| **Benchmark PBT** | **2,212** | **1,926** | — |
| Exceptional items | (20) | (39) | Recurs (restructuring/cloud) |
| Amortisation of acquisition intangibles | (271) | (211) | **Recurs — rising every year** |
| Acquisition & disposal expenses | (59) | (37) | **Recurs — serial acquirer** |
| Adjustment to fair value of contingent consideration | +2 | (1) | Volatile |
| Interest on tax liabilities | (14) | (4) | Recurs |
| Financing fair-value remeasurements | +101 | (85) | Genuinely volatile |
| **Statutory PBT** | **1,951** | **1,549** | — |

Total non-benchmark deduction: US$261m in FY26 (US$377m in FY25). Decomposed further from the company's Appendix 3: exceptional items US$20m; amortisation/impairment of acquisition intangibles US$271m; "other adjustments" −US$30m (a net credit in FY26, driven by the +US$101m financing gain offsetting acquisition expenses and interest-on-tax).

**Amortisation of acquisition intangibles across years (US$m) [CONFIRMED]:** FY22 174; FY25 211; FY26 271. It rises monotonically because Experian completes acquisitions every year, each one creating new customer-relationship and technology intangibles amortised over 2–20 years. This is **not a one-off, non-cash artefact; it is the recurring economic cost of maintaining growth by acquisition.**

**Exceptional items [CONFIRMED]:** FY22 26; FY25 39; FY26 20. Small but ever-present, dominated by restructuring and cloud-migration costs (FY26 restructuring US$28m, FY25 US$50m). An item labelled "exceptional" that appears every single year is, in substance, an operating cost.

**Financing fair-value remeasurements (+US$101m FY26 vs −US$85m FY25)** are genuinely market-driven (mostly retranslation of Brazilian real intra-group funding — US$82m of the US$87m non-cash financing gain) and are defensibly excluded; their exclusion cuts both ways across years and is not a systematic flatter.

**Verdict — how much is legitimate normalisation vs a serial acquirer excluding its own strategy's cost?** The financing remeasurement exclusion is legitimate. The amortisation of acquisition intangibles (US$271m) and the recurring acquisition/disposal expenses (US$59m) — together US$330m, or ~15% of Benchmark PBT — are, for a perpetual acquirer, a **permanent cost dressed as an adjustment**. Equifax and TransUnion (US GAAP) run analogous adjusted-EBITDA/adjusted-EPS measures that likewise exclude amortisation of acquired intangibles and acquisition costs, so Experian's practice is industry-normal; but "industry-normal" is not the same as "economically neutral," and the market prices Benchmark EPS (179.8c) rather than statutory EPS (164.5c) — a 9.3% premium the reader should keep in view.

### IV.9 Balance Sheet Teardown

At 31 March 2026 (US$m) [CONFIRMED, Group balance sheet]:

| Line | FY26 | FY25 | Note |
|---|---|---|---|
| Goodwill | 7,261 | 6,654 | Dominant asset; residue of 30 years of M&A |
| Other intangible assets | 3,078 | 2,855 | Acquisition intangibles + internally generated software |
| Property, plant & equipment | 337 | 350 | Genuinely asset-light |
| Trade & other receivables (current) | 2,315 | 1,684 | Sharp rise — monitor DSO |
| Cash & equivalents | 328 | 368 | Thin cash; relies on facilities |
| Borrowings (current + non-current) | 5,565 | 5,016 | 900 current + 4,665 non-current |
| Provisions (current + non-current) | 25 | 24 | **No litigation provision evident** |
| Net assets | 5,583 | 5,090 | |
| Capital employed (per Note 5(q)) | 10,720 | 9,732 | Increase "largely acquisition related" |

Retained earnings of US$22,210m are offset by other reserves of −US$18,629m — the accounting residue of the 2006 demerger from GUS. Net current liabilities of US$467m are normal for a business that bills clients in advance and funds itself in the capital markets.

**Software capitalisation (a key accounting-quality question) [CONFIRMED policy; subagent-verified]:** Internally generated software is amortised over 3–10 years (average ~5 years for non-acquisition intangibles); acquisition intangibles over 2–20 years. FY26 "purchase of other intangible assets" (cash flow) was US$677m — the capitalised development spend that builds the platform. The scale of capitalisation (≈8% of revenue) materially supports current-period margin: if this spend were expensed rather than capitalised, Benchmark EBIT would be lower. The split of the US$3,078m "other intangibles" balance between acquisition intangibles and internally generated software is not separately disclosed in the preliminary announcement [UNKNOWN — in the full AR2026 note].

**Receivables:** the jump in current trade and other receivables from US$1,684m to US$2,315m (+37%) outpaces revenue growth (+12%) and warrants monitoring; part is acquisition-related, but rising DSO would be an early quality-of-earnings flag [ANALYTICAL INFERENCE].

### IV.10 Cash Flow and Conversion

FY26 reconciliation (US$m) [CONFIRMED, cash-flow summary]:

| Step | FY26 | FY25 |
|---|---|---|
| Benchmark EBIT | 2,397 | 2,083 |
| + Amortisation & depreciation | 613 | 547 |
| = Benchmark EBITDA | 3,010 | 2,630 |
| + Impairment charged to EBIT | 6 | 15 |
| − Net capital expenditure | (718) | (650) |
| − Increase in working capital | (163) | (54) |
| − Principal lease payments | (48) | (41) |
| ± Associates / share incentives | 134 | 125 |
| = **Benchmark operating cash flow** | **2,221** | **2,025** |
| − Net interest paid | (198) | (165) |
| − Tax paid | (438) | (447) |
| = **Benchmark free cash flow** | **1,583** | **1,411** |

Cash conversion 93% (2,221/2,397). Statutory cash generated from operations was US$2,875m. Capex at 8.6% of revenue (guided toward ~7%) is high for a supposedly asset-light business — the "cost of a free input" is a continuous, large reinvestment in the platform and data that produces it. The cash cost of exceptional/non-benchmark items was only US$34m — cheap. Benchmark measures modestly flatter cash by excluding acquisition-related outflows, but the gap is small; cash generation is genuinely high-quality. After maintaining the platform (~US$677m intangible capex) and funding the dividend (US$590m ordinary paid), roughly US$1bn+ of genuine discretionary cash remains for M&A and buybacks.

### IV.11 Capital Intensity and Return on Capital

ROCE 17.2% = Benchmark EBIT less tax at the Benchmark rate, divided by average capital employed (US$10,720m at year-end; average of ~US$10,226m). Sanity check: Benchmark EBIT US$2,397m × (1 − 25.5%) = US$1,786m; 1,786 / ~10,226 ≈ 17.5% — consistent with the 17.2% reported on the precise averaging basis [ANALYTICAL INFERENCE confirms the disclosed figure].

The goodwill-heavy balance sheet (US$7,261m goodwill, US$3,078m other intangibles) depresses reported ROCE. **Return on tangible capital [ANALYTICAL INFERENCE]:** stripping the US$7,261m of goodwill from the US$10,720m capital employed leaves ~US$3.46bn of tangible/working capital; US$1,786m post-tax Benchmark EBIT on that base implies a return above 50%. This is the mechanical signature of a business whose true "capital" is off-balance-sheet data, and whose on-balance-sheet capital is largely the accounting price paid for acquisitions. **Is growth capital-light? Organically, yes; in aggregate, no** — the 8.6% capex ratio plus ~US$800m/yr of M&A mean incremental growth consumes real capital. The "capital-light" label describes the *organic core*, not the *reported enterprise*.

### IV.12 Debt, Funding and Liquidity

Net debt US$5,179m at 31 March 2026 (up from US$4,684m), at 1.7x Benchmark EBITDA — **below the stated 2.0–2.5x target range** [CONFIRMED]. Debt is issued principally through **Experian Finance plc** (a US$6bn Euro Medium-Term Note programme, the former GUS financing vehicle) and **Experian Europe DAC**, both guaranteed by Experian plc [CONFIRMED, Moody's]. Credit ratings: **Baa1 (Moody's) / BBB+ (S&P)**, with a stated policy to maintain "a strong investment grade credit rating (BBB+ / Baa1 or above)" [CONFIRMED]. FY26 net interest US$185m at an average rate of ~3.6% (benefiting from a rate-hedging programme); FY27 guided to US$250–260m (reflecting acquisition financing and Own Up/Konfir, both closed 1 April 2026). Undrawn committed facilities US$2.5bn. **The leverage policy does not currently constrain M&A or buybacks** — running below the bottom of its own range, Experian has explicit headroom, which is why it could simultaneously spend US$792m on acquisitions, pay a US$590m dividend and execute US$725m of buybacks in FY26.

### IV.13 The Litigation and Regulatory Contingency

**CFPB v. Experian Information Solutions, Inc.** (filed 7 January 2025, Central District of California) alleges "sham investigations" of disputes under FCRA. Procedural history [CONFIRMED, CFPB docket/CourtListener]: motion to dismiss granted in part 5 May 2025; amended complaint 6 June 2025; further dismissal 6 August 2025; second amended complaint 22 August 2025; **motion to dismiss denied 22 October 2025**; Experian answered 3 November 2025; the CFPB's motion to strike affirmative defenses was heard 30 January 2026; **jury trial set for 21 September 2026**. Experian calls the suit "completely without merit" and states it does "not expect this to have any material impact on our business" [COMPANY CLAIM].

**Provision status [ANALYTICAL INFERENCE]:** total balance-sheet provisions are only US$18m current + US$7m non-current — consistent with routine matters and indicating **no material provision has been recognised for the CFPB case**, which is standard where an outflow is not assessed as probable and reliably estimable. The full contingent-liabilities note (in AR2026) would carry the qualitative disclosure [not in the preliminary announcement — flagged].

**Historical cost benchmarks [CONFIRMED]:** the 2012/2015 breaches produced a 40-state multistate settlement of **US$13.67m with Experian** (November 2022), alongside a separate **US$2.43m settlement with T-Mobile**; FCRA class actions have settled in the low tens of millions (e.g., Hill-Green "Fraud Shield" ~US$22.45m; a T-Mobile breach class action ~US$22m).

**Outcome model [HYPOTHESIS]:** (i) *Dismissal/settlement with a civil money penalty* — tens of millions, immaterial to a group earning US$2.2bn Benchmark PBT; (ii) *Adverse judgment with a penalty plus redress* — potentially low hundreds of millions, a one-off, still manageable; (iii) **the material scenario — mandated remediation of the dispute system.** Volume III established that the dispute operation is deliberately low-cost (as low as US$0.57 per letter). A court-mandated requirement to conduct substantive, human-reviewed investigations across >12 million disputes a year could raise the run-rate cost by an order of magnitude — the recurring margin risk, not the one-off fine, is the real financial exposure. This is the point where the report's central paradox becomes a P&L line.

### IV.14 Capital Allocation and Return on a Thirty-Year Acquisition Programme [PRIORITY DEPTH]

**Material acquisitions [CONFIRMED]:**

| Deal | Date | Price | Notes |
|---|---|---|---|
| Serasa (initial 65%) | June 2007 | R$2.32bn / US$1.2bn | Transformative Brazil entry |
| Serasa (to 70%) | Oct 2007 | R$138m / US$72m | |
| Serasa (remaining 29.6%, to 99.6%) | Oct 2012 | R$3.1bn / US$1.5bn | Bought out Itaú/Bradesco/Santander/HSBC |
| Tapad | Nov 2020 | ~US$280m | North America digital identity |
| ClearScore | Blocked 2019 | — | CMA prohibited |
| illion | 30 Sept 2024 | A$820m | ANZ bureau; ~A$175m revenue, ~A$65m EBITDA first full year |
| Audigent | Dec 2024 | Undisclosed | AdTech, North America |
| ClearSale | Completed 1 Apr 2025 | up to R$1,905m | Brazil transactional fraud |
| NeuroID | FY25 | Undisclosed | Behavioural fraud, in Ascend |
| KYC360 | Oct 2025 | Undisclosed | UK financial-crime |
| AtData | Oct 2025 | Undisclosed | 10bn+ email addresses |
| Own Up | Post-FY26 (1 Apr 2026) | Undisclosed | US mortgage marketplace |

FY26 acquisition spend US$792m (down from US$1,244m in FY25). Management expects completed acquisitions to contribute ~1% of growth in FY27 and to dilute margin by ~50bps near-term before synergies.

**Goodwill impairment history [CONFIRMED, subagent-verified against AR2022/FY23-FY24 notes]:** Experian **has** impaired acquired goodwill, but only twice in ~15 years and only in the weakest region — **US$53m in FY21 and US$179m in FY23, both in EMEA/Asia Pacific** (accumulated goodwill impairment reached US$246m by 31 March 2023 and was unchanged through FY24). **The North America, Latin America and UK & Ireland cash-generating units have never been impaired.** Separately, US$27m of internally generated software was impaired in FY21 on a technology-estate upgrade. No Tapad-specific write-down has been disclosed (Tapad sits in North America Data, which has never been impaired).

**Has the programme created value above the cost of capital?** [ANALYTICAL INFERENCE, defensible judgement:]
- *Core deals — clearly yes.* Serasa is the paradigm: acquired for a combined ~US$2.8bn across 2007–2012, it anchors a Latin America segment now generating US$1,297m of revenue at a 30.8% margin (~US$399m Benchmark EBIT), and it has never been impaired. North America bolt-ons (Tapad, verification assets, Clarity) feed the 34.2%-margin engine.
- *Edge deals — value-destructive.* The ~US$232m of cumulative EMEA/AP goodwill impairment is the honest scorecard of deals that did not work in structurally sub-scale markets.
- *Aggregate returns exceed the cost of capital:* ROCE of 17.2% versus a ~8–9% WACC, sustained "mid-to-high teens over the past decade" per management, while the base compounds organically at 8%. But the **recurring US$271m amortisation of acquisition intangibles is the perpetual toll** the strategy pays, and the market should treat it as a real (if non-cash) cost of the growth algorithm.

**Buybacks:** US$725m executed in FY26; a new US$1bn programme runs to 30 June 2027; the FY26 closing share count fell to 899m (from ~914m weighted average). Buying back stock at a mid-30s earnings multiple destroys value unless per-share compounding continues at the historical rate — defensible given the growth record, but not risk-free if the mortgage windfall reverses. FY27 guidance assumes WANOS of 880–885m, i.e. continued reduction.

**Overall judgement:** serial acquisition is **both** value-creating strategy in the core **and** growth-maintenance at the edge. It has compounded the franchise, but a meaningful slice of "growth" is the perpetual purchase of the next intangible, whose amortisation is then excluded from the number the market prices.

### IV.15 One Dollar of Group Revenue (FY26, per US$1 of statutory revenue US$8,445m)

| Destination | Cents | Basis |
|---|---|---|
| Labour | 31.8¢ | Benchmark |
| Data & IT (incl. cloud, FICO pass-through) | 19.2¢ | Benchmark |
| Amortisation & depreciation | 7.3¢ | Benchmark |
| Marketing & customer acquisition | 7.1¢ | Benchmark |
| Other operating (compliance, disputes) | 6.3¢ | Benchmark |
| **= Benchmark operating profit** | **~28.4¢** | |
| less amortisation of acquisition intangibles | 3.2¢ | Non-benchmark |
| less other non-benchmark items (net) | ~1.0¢ | |
| **= statutory operating profit** | **24.2¢** | |
| less net finance | 1.2¢ | |
| **= statutory PBT** | **23.1¢** | |
| less tax | 5.2¢ | (22.7% statutory rate) |
| **= retained profit** | **~17.9¢** | |

**B2B vs Consumer Services differ in shape [ANALYTICAL INFERENCE]:** B2B carries the heavier fixed data/platform cost (more of the Data & IT 19.2¢) and little marketing, landing at a 30.9% margin. Consumer Services carries most of the marketing/customer-acquisition load (the bulk of the 7.1¢) but recognises marketplace revenue *net*, which keeps its margin at 29.6% despite the acquisition spend — the net-recognition accounting is what makes a marketing-heavy consumer business look as profitable as the B2B bureau.

### IV.16 Economic Driver Tree

Bureau revenue = files held × permissible-purpose inquiries per file × price per inquiry. FY26 demonstrated the **price** term dominating (mortgage +45% on flat volume). The full frame:

> (files × inquiries/file × price/inquiry) + platform/software subscription + (members × [subscription conversion × ARPU + referrals × fee]) + vertical revenue (Health, Automotive, Marketing) − labour − technology/cloud − data operations − disputes/compliance − FICO royalty − marketing = Benchmark EBIT − amortisation of acquisition intangibles − exceptionals − interest − tax = statutory profit.

**The five variables explaining most outcomes:** (1) US Financial Services inquiry pricing (above all mortgage); (2) US origination volumes; (3) Consumer marketplace referral volume × fee; (4) labour cost as a % of revenue (the productivity lever); (5) cloud dual-run roll-off. Secondary: Brazilian real translation, acquisition-intangible amortisation, net interest.

### IV.17 Scenario and Sensitivity Analysis [ANALYTICAL INFERENCE unless stated]

| Scenario | Revenue by segment | Benchmark EBIT / margin | Statutory profit | Cash / leverage / buyback |
|---|---|---|---|---|
| US mortgage price normalisation | NA Financial Services falls sharply (reverses much of +45%) | Margin dilutive (high-drop-through revenue lost) | Falls | Lower FCF; buyback capacity trimmed |
| US origination downturn | NA transactional down; cushioned by collections/Consumer | Modest drag | Falls | Manageable at 1.7x |
| VantageScore share gain | Broadly neutral (Experian sells both; data pull persists; FICO royalty is pass-through) | Neutral-to-slightly-negative | Neutral | Neutral |
| Adverse CFPB outcome w/ remediation | Revenue unaffected; **cost base steps up** | **Recurring margin drag** | Falls | Reputational; buyback unaffected short-term |
| Material data breach | Revenue tail risk; settlement precedent ~US$14m | One-off | One-off hit | Immaterial financially; reputational tail |
| Legislative removal of data (medical-debt precedent) | File richness erodes → follow-the-data-right risk | Structural drag | Falls | Long-term franchise risk |
| Brazilian FX depreciation | Translates down 30.8%-margin LatAm | Margin/EBIT translation hit | Financing remeasurement swings | Modest |
| Marketing-spend recession | Hits Marketing Services + prescreen | Modest drag | Falls | Manageable |
| Cloud roll-off from FY27 | Neutral to revenue | **+~50bps margin tailwind (CER)** [COMPANY guidance] | Rises | Higher FCF |
| Continued M&A at FY26 rate (~US$800m/yr) | +~1% inorganic revenue | ~50bps near-term dilution; rising amortisation | Amortisation drag rises | Leverage drifts up but within range |

### IV.18 Profitability Decomposition and Normalisation

FY26 Benchmark EBIT US$2,397m decomposes into: (1) **structural earnings power** — the recurring bureau, platform, verticals and Consumer base; (2) **the mortgage pricing windfall** — a boost inside the +45% NA mortgage line, not durable; (3) **cloud dual-run costs still carried** — a self-reversing headwind from FY27; (4) **acquisition contribution** — ~1% of revenue, ~50bps margin-dilutive near-term; (5) **FX** — a 2% Benchmark EPS tailwind in FY26. **Normalised through-cycle Benchmark EBIT margin [HYPOTHESIS]: ~28–29%.** The FY27 guidance (double-digit Benchmark EPS growth, organic revenue 6–8%, ~+50bps margin at CER, capex ~8% trending to 7%, Benchmark tax ~26%) implies management believes the cloud roll-off and AI productivity will more than offset mortgage normalisation — i.e., management itself treats the mortgage windfall as impermanent and is guiding to structural, not windfall, expansion.

---

## Recommendations

**Stage 1 — Underwrite the structural core, discount the windfall (now).** Value Experian on **statutory** and normalised numbers, not on the Benchmark headline: apply at least the US$271m acquisition-intangible amortisation as a real recurring cost, and treat the FY26 mortgage +45% as a one-off pricing event, not a run-rate. Anchor to organic growth of 6–8% and a normalised ~28–29% margin. *Benchmark that would change this view:* if mortgage pricing holds AND VantageScore fails to compress bureau economics through FY27, raise the durable growth assumption.

**Stage 2 — Track five telltales quarterly.** (i) US mortgage-profile revenue growth (watch for the +45% decaying toward volume-led single digits); (ii) VantageScore adoption among top-15 lenders (already ~30% of the market — a share above ~50% would begin to matter); (iii) labour cost as a % of revenue (the 31.8% figure falling further validates the AI thesis; a stall is a margin warning); (iv) the current-receivables trend (the FY26 +37% jump vs +12% revenue is a DSO flag); (v) cloud dual-run roll-off actually landing in the FY27 P&L as guided. *Thresholds:* a labour ratio rising back above ~33%, or receivables growth persistently outpacing revenue by >15pts, would each warrant a quality-of-earnings downgrade.

**Stage 3 — Price the CFPB tail explicitly.** Do not model the CFPB matter as a binary fine. Model the **remediation scenario**: estimate the incremental cost of substantive dispute investigations across >12m disputes/year and haircut the margin accordingly as a low-probability, high-impact recurring cost. *Benchmark:* a summary-judgment or settlement that leaves the low-cost dispute process intact removes most of the downside; any consent order mandating process change is a structural margin event, not a one-off.

**Stage 4 — Judge M&A on the impairment scoreboard, not the pipeline.** Continue to credit core-market bolt-ons (never impaired) but treat further EMEA/AP expansion sceptically given the ~US$232m impairment record there. *Benchmark:* any new goodwill impairment outside EMEA/AP would be a first — and a signal that the acquisition machine is over-reaching into the profitable core.

**Stage 5 — On the buyback, require continued per-share compounding.** The US$1bn programme (to 30 June 2027) creates value only if Benchmark EPS keeps compounding double-digit. *Threshold:* if organic growth slips below ~6% while the mortgage windfall reverses, buying back at a mid-30s multiple becomes value-neutral-to-destructive and cash should tilt back to debt reduction or higher-return M&A.

---

## Caveats

- **The non-GAAP question is unresolved by design.** The market prices Benchmark EPS (179.8c) at a 9.3% premium to statutory (164.5c). This report treats the acquisition-intangible amortisation and recurring acquisition expenses as real economic costs; readers who accept the company's framing will reach a rosier view. The disagreement is analytical, not factual.
- **Pricing opacity forces inference.** Per-inquiry bureau rates and marketplace referral fees are confidential; revenue-per-inquiry and revenue-per-referral are therefore labelled UNKNOWN rather than estimated. Unit economics in IV.6 are derived transparently and flagged as inference.
- **Preliminary-announcement basis.** Figures are from the FY26 results announcement (approved 19 May 2026) and prior-year announcements; the full AR2026 notes (segmental detail, the acquisition-vs-internally-generated split of the US$3,078m intangibles balance, the 31 March 2026 contract-liability/deferred-income balance, and the qualitative contingent-liabilities disclosure) were not all independently accessible and are flagged UNKNOWN where relevant. The FY26 goodwill balance (US$7,261m) and intangibles (US$3,078m) are taken from the published balance sheet; the goodwill *impairment history* (US$53m FY21, US$179m FY23, both EMEA/AP; none in NA/LatAm/UK) is confirmed from the AR2022/FY23/FY24 notes.
- **Forward-looking items are labelled.** FY27 guidance, the cloud dual-run roll-off, the VantageScore savings estimates (Deep Future Analytics US$648m first-year / US$930m updated / US$2.5bn five-year) and all scenario outputs are projections, not realised results, and are tagged COMPANY CLAIM, THIRD-PARTY ESTIMATE, ANALYTICAL INFERENCE or HYPOTHESIS accordingly.
- **Revenue quality is partly a legal question.** Multiple streams depend on legal permissions persisting — FCRA permissible purpose, UK GDPR legitimate interests, LGPD Article 7(X). The medical-debt precedent shows data categories can be removed from the file by legislation or regulation; where that happens, the associated revenue is contingent, not guaranteed.

*Work paused at the completion of Volume IV. Volume V has not been begun.*