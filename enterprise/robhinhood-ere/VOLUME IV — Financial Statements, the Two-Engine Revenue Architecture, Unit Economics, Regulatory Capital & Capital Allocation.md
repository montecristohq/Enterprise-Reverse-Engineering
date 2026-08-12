# ROBINHOOD MARKETS, INC. — VOLUME IV: Financial Statements, the Two-Engine Revenue Architecture, Unit Economics, Regulatory Capital & Capital Allocation

*Institutional-grade forensic reverse-engineering study. Fifth subject in the research programme (after Wise plc, Atruvia AG, the DZ BANK Group, Experian plc). Volume IV executed in full; Volume V not begun. All figures US GAAP, USD, 31 December year-end unless stated. Evidence classes: CONFIRMED FACT (default) / COMPANY CLAIM / THIRD-PARTY ESTIMATE / ANALYTICAL INFERENCE / HYPOTHESIS / UNKNOWN.*

## TL;DR
- Robinhood is best characterised as a **structurally improved but still deeply cyclical business currently enjoying an unusually favourable cycle**. FY2025 GAAP net income of $1,883m on total net revenue of $4,473m (up 52% year-over-year) is real, but a material minority of 2024–25 profitability rests on elevated policy rates, a crypto bull run, one-time tax and regulatory-accrual benefits, and a cost base that was cut rather than grown. ANALYTICAL INFERENCE: durable, through-cycle net income is roughly $1.1–1.5bn.
- The two engines are **not genuinely diversifying**. Transaction revenue (PFOF-driven, 59% of FY2025) and net interest revenue (34%) share a common master variable — retail risk appetite. Net interest (margin lending + securities lending) and Gold subscriptions are the highest-quality lines; **crypto transaction revenue is the most fragile** (Q4 2025 crypto revenue fell 38% year-over-year to $221m).
- Growth is **capital-light at the parent but capital-intensive at the broker-dealer**. A growing margin book and NSCC/reserve deposits consume cash, financed largely by customer payables and securities-lending cash collateral. Robinhood Securities LLC held **$3.53bn of net capital at 31 Dec 2025 ($3.16bn above the $373m requirement)**, which — together with the credit-agreement covenants — constrains upstreaming cash to the parent.

## Key Findings
1. **Revenue more than tripled 2022→2025** ($1,358m → $4,473m), but composition changed fundamentally: net interest went from a rate-driven windfall (2022–23) to a balance-driven engine (2024–25), while transaction revenue recovered on crypto and options.
2. **The single most useful number — normalised through-cycle profitability — is materially below the 2025 reported figure.** ANALYTICAL INFERENCE: normalising for rates, the crypto cycle and one-offs, sustainable net income is roughly **$1.1–1.5bn** versus $1,883m reported.
3. **Self-clearing converted settlement risk into a permanent capital charge.** RHS net capital rose from $2.50bn (2022) to $2.54bn (2024) to $3.53bn (2025); the Rule 15c3-3 customer-segregated balance was ~$4.57bn (2024) and ~$4.47bn (2025).
4. **The balance sheet is roughly three-quarters other people's money.** Of $38,137m total assets at end-2025, the margin book ($17,994m), segregated cash, securities borrowed, and fractional shares are customer-related; reported equity is $9,151m, but tangible equity genuinely at the firm's own risk is far smaller.
5. **Incremental margins in 2024–25 were extraordinary and are not repeatable** — revenue grew against a cost base that had been cut (total operating expenses fell from $2,401m in 2023 to $1,897m in 2024 while revenue rose 58%).
6. **Buybacks are so far offsetting dilution, not shrinking the count.** Class A + Class B shares rose in 2025 despite $653m of repurchases, because SBC issuance and RSU settlement outpaced buybacks.

## Details

### IV.1 Multi-Year Financial History (GAAP, USD millions)

| Line | 2019 | 2020 | 2021 | 2022 | 2023 | 2024 | 2025 |
|---|---|---|---|---|---|---|---|
| Total net revenue | 277 | 959 | 1,815 | 1,358 | 1,865 | 2,951 | 4,473 |
| — Transaction | ~200 | ~720 | 1,402 | 814 | 785 | 1,647 | 2,628 |
| — Net interest | ~18 | ~28 | 256 | 424 | 929 | 1,109 | 1,514 |
| — Other | ~59 | ~211 | 157 | 120 | 151 | 195 | 331 |
| Total operating expenses | ~385 | ~951 | 3,456 | 2,369 | 2,401 | 1,897 | 2,379 |
| Net income (loss) | (107) | 7 | (3,687) | (1,028) | (541) | 1,411 | 1,883 |
| Diluted EPS ($) | n/a | n/a | (7.49) | (1.17) | (0.61) | 1.56 | 2.05 |
| SBC | small | ~24 | 1,572 | 654 | ~436 | 304 | 305 |
| Adjusted EBITDA (non-GAAP) | (74) | 155 | (89) | (95) | 536 | 1,429 | 2,522 |
| Operating cash flow | — | — | — | — | — | (157) | 1,638 |
| Cash & equivalents | — | — | ~6,300 | ~6,300 | ~4,800 | 4,332 | 4,261 |

2019–2020 sub-line splits are approximate (THIRD-PARTY ESTIMATE from S-1 narrative and Statista compilation of company data); 2021–2025 are CONFIRMED FACT from filings. The 2023 SBC figure ~$436m is approximate.

**Accounting-definition changes to separate from economic change:** (a) Funded Customers include each holder of a joint account from July 2024, RIA/TradePMR customers from Q1 2025, and Bitstamp customers from June 2025 — inflating the metric independent of organic growth; (b) "Total Platform Assets" replaced "Assets Under Custody" in Q1 2025 and adds TradePMR RIA assets *not custodied* by Robinhood; (c) crypto notional and net deposits include Bitstamp from June 2025. Total Platform Assets reached **$324bn at end-2025 (+68% YoY)**; funded customers 27.0m (+7%); ARPU $191 (Q4 2025 annualised, +16% YoY); Gold subscribers 4.2m (+58% YoY, ~15% adoption); Net Deposits $68.1bn full-year.

### IV.2 Engine One — Transaction Revenue

Full-year transaction revenue by asset class (ANALYTICAL INFERENCE from quarterly disclosures; totals reconcile to reported annual figures; individual asset-class annual splits are estimates built from quarterly press-release figures):

| $m | 2024 | 2025 |
|---|---|---|
| Options | ~760 | ~1,123 |
| Cryptocurrencies | ~626 | ~901 |
| Equities | ~177 | ~302 |
| Other (futures, event contracts, instant withdrawals, interchange) | ~84 | ~302 |
| **Total transaction (CONFIRMED)** | **1,647** | **2,628** |

- **Options** is the durable core. 659m contracts in Q4 2025 (+38% YoY, a record); revenue per contract is stable. Recognised when the trade is routed and executed; direct cost is a few cents of exchange/regulatory/clearing fee. Durable and less price-sensitive than crypto.
- **Crypto** is the swing factor. Q4 2025 crypto revenue fell 38% YoY to $221m as prices corrected and Robinhood App crypto notional fell 52% YoY to $34bn. Crypto revenue per $1bn notional fell from ~$5m (Q4 2024) to ~$2.5m (2026) as the fee model and mix shifted (THIRD-PARTY ESTIMATE, CryptoSlate). A crypto winter cuts this line by the majority of its value while leaving net interest intact.
- **Equities** near-doubled in 2025 on volume (Q4 equity notional $710bn, +68% YoY); PFOF on equities is low per dollar.
- **Rate-times-volume decomposition (ANALYTICAL INFERENCE):** most of the 2025 options increase came from *volume*; most of the crypto swing came from *price/notional*. 
- **Concentration and regulatory risk:** PFOF is routed to a small number of wholesale market makers (CONFIRMED FACT from Volume II carried forward); PFOF is banned in the UK and EU, capping the international transaction model.

### IV.3 Engine Two — Net Interest Revenue (seven components, $m)

Robinhood decomposes net interest into seven components in its earnings-presentation bridge (Q4 2025 deck). Full-year figures are the sum of the four disclosed quarters and foot exactly to the reported annual totals:

| Component | 2024 | 2025 | Behaviour |
|---|---|---|---|
| Margin interest | 319 | 573 | Balance-driven (rate × margin book) |
| Securities lending, net | 94 | 190 | Balance/demand-driven |
| Interest on segregated cash/securities & deposits | 261 | 319 | Rate-driven |
| Cash sweep (spread on off-B/S deposits) | 179 | 229 | Spread-driven |
| Interest on corporate cash & investments | 256 | 167 | Rate-driven (fell as Fed cut) |
| Credit card, net | 24 | 64 | Balance-driven |
| Less: interest expense on credit facilities | (24) | (32) | Funding cost |
| Other | 0 | 4 | — |
| **Total net interest revenue (CONFIRMED)** | **1,109** | **1,514** | |

The balance-driven components (margin, securities lending, credit card) grew strongly in 2025 while the rate-driven components (corporate cash, cash sweep spread) fell as the Fed cut — exactly the mix shift the two-engine framing predicts. The **margin book grew 113% YoY to $16.8bn** at end-2025; tiered margin rates ran from 5.0% (up to $50k) to 3.95% ($50m+) as of late 2025 (a floating schedule pegged to the Fed funds upper bound). Implied average yield on the margin book was ~4.89% annualised in Q4 2025 (THIRD-PARTY ESTIMATE derived from disclosed average balance and revenue). **Total securities lending revenue (including interest on cash collateral) reached ~$488m in FY2025**; the "net" line above ($190m) excludes the cash-collateral interest that is reported within the segregated-cash line.

**Rate-sensitivity model (ANALYTICAL INFERENCE, balances constant at end-2025):** with roughly $40–45bn of net rate-sensitive balances (cash sweep, corporate cash, segregated cash), each ±100bp moves net interest revenue by approximately ±$250–350m before balances respond. A −300bp move, balances constant, could cut net interest by roughly $700m–1bn. **How much of 2025 net-interest growth was balance vs rate:** essentially all of the +$405m increase came from *balance growth*, which more than offset a *rate headwind* from Fed cuts — a favourable, but not permanent, offset.

### IV.4 The Interaction of the Two Engines
ANALYTICAL INFERENCE: the engines are **weakly counter-cyclical in rates but strongly pro-cyclical in risk appetite**. Falling rates cut net interest but can support trading volume; a crypto winter cuts transaction revenue but leaves net interest largely intact; a market crash raises volatility/volume short-term but shrinks margin balances and asset values. The common factor across both engines is **retail risk appetite** — so the two-engine structure diversifies *sources* far more than it diversifies *exposure*. The framing-note trap is real: this is more apparent diversification than genuine.

### IV.5 Other Revenue
Gold subscription revenue reached **$50m in Q4 2025 (+56% YoY)**, an annualised run-rate of ~$200m at 4.2m subscribers — genuinely recurring. Other lines: credit-card interchange (offset by rewards expense), proxy/Say Technologies revenue, Bitstamp institutional (a "~$100m or more annualised" business per the CFO in Q3 2025 — COMPANY CLAIM), and TradePMR custody. Gold and credit-card interchange are the most durably recurring; Bitstamp institutional is thin-margin (~5bp on notional).

### IV.6 Cost Architecture (economic drivers, not reporting lines; FY2025 $m)
- **Brokerage & transaction ($211m):** the only genuinely variable-with-trades line; remarkably low precisely because self-clearing pays no third-party clearer (structural fact carried forward from Volume III).
- **Technology & development ($897m):** step-fixed; fell in absolute terms 2021 ($1,234m) → 2024 ($818m) as headcount was cut, then rose modestly in 2025 with platform assets up ~5x over the period.
- **Operations ($130m):** variable with customers/activity.
- **Marketing ($399m):** variable with customer acquisition. **Deposit-match and IRA-match incentives are contra-revenue** (recognised as a reduction to revenue when earned, allocated proportionally across transaction/net-interest/other), *not* marketing expense — a key classification point.
- **G&A ($628m):** largely fixed plus regulatory penalties/accruals.
- **Provision for credit losses ($114m):** variable with margin and credit-card balances; brokerage-related losses relate mainly to fraudulent-deposit transactions and unsecured margin balances (RHF indemnifies RHS for these).

**True marginal cost (ANALYTICAL INFERENCE):** an incremental *trade* costs only a few cents (exchange/regulatory/clearing fee) — extremely high contribution margin. An incremental *customer* is dominated by marketing and match incentives, so customer acquisition is the real variable cost driver.

### IV.7 Unit Economics
- **Funded customer:** ARPU $191 (Q4 2025 annualised, +16% YoY). Cohort data show older cohorts accumulate assets over time; **average Total Platform Assets per funded customer reached ~$10,500 by Q2 2025** (up from ~$3,800 in Q2 2023). Gold subscribers carry ~5x the assets of an average funded customer (COMPANY CLAIM) — the monetisation flywheel.
- **Per order/contract:** options revenue per contract stable; crypto revenue per $1bn notional roughly halved (see IV.2).
- **Per dollar of platform assets (the most revealing unit):** total monetisation ~1.4% of $324bn platform assets, and rising as balances (margin, sweep, securities lending) monetise — the business increasingly earns on custody, not just on trades.

### IV.8 Income Statement Teardown & Operating Leverage
Incremental margin (Δ operating profit / Δ revenue) was extraordinary in 2024 because operating expenses *fell* while revenue rose — an incremental GAAP operating margin above 100% that quarter/year, which is arithmetically un-repeatable. **GAAP-to-Adjusted-EBITDA reconciliation, FY2025:** net income $1,883m + credit-facility interest $32m + tax $225m + D&A $86m = EBITDA $2,226m; + SBC $305m − $9m unrealised gains on non-marketable securities = **Adjusted EBITDA $2,522m** (56% margin). The SBC add-back is legitimate as non-cash but represents a real economic cost and real dilution; in 2021, SBC ($1,572m) nearly equalled revenue ($1,815m), rendering that year's Adjusted EBITDA almost economically meaningless — the framing-note warning holds. **We believe the GAAP figure, adjusted only for genuine one-offs, is the more honest number; Adjusted EBITDA flatters by ignoring dilution.**

### IV.9 Broker-Dealer Balance Sheet Teardown (end-2025, $m)
**(a) Off balance sheet — customer property:** equities, options and crypto held for customers (the bulk of $324bn Total Platform Assets); **Cash Sweep $32,786m** swept to program banks (Robinhood earns only the net spread).

**(b) On balance sheet but not the firm's economic property:** cash/securities segregated under federal and other regulations $5,749m; **payables to users $11,986m**; **securities loaned $11,626m** (cash collateral received); **fractional-share asset $3,782m and matching repurchase obligation $3,782m** (fully offsetting); **receivables from users (margin book) $17,994m**, collateralised by customer securities with no expected credit loss on fully secured balances.

**(c) The firm's own economic assets/liabilities:** corporate cash $4,261m; deposits with clearing organisations $702m; goodwill $385m and intangibles $168m (Bitstamp, TradePMR, X1); deferred tax assets (post valuation-allowance release); PP&E $154m.

Reported totals: assets $38,137m; liabilities $28,986m; **equity $9,151m** (additional paid-in capital $11,284m less accumulated deficit $2,152m). **ANALYTICAL INFERENCE:** reading gross leverage (~4.2x) as a normal company's would be the first analytical trap — most of the liability side is customer money offset by customer assets. Once customer items are excluded, true firm leverage is modest, and equity principally supports the margin book, clearing/reserve deposits, regulatory net capital and goodwill.

### IV.10 Working Capital & Cash Conversion
Operating cash flow swung from **−$157m (2024) to +$1,638m (2025)**. The margin book consumed **$9,106m** of cash in 2025 (change in receivables from users), financed largely by growth in **payables to users (+$3,423m)** and **securities loaned (+$4,163m)**. Growth is therefore cash-consuming at the broker-dealer level but substantially self-funded by customer balances — a critical distinction, because that financing is not the firm's own capital. Net income to operating-cash-flow divergence is driven by these customer-balance swings, the non-cash deferred-tax benefit, SBC, and provisions.

### IV.11 Capital Intensity & Return on Capital
Maintenance capital is trivial: PP&E purchases $15m + capitalised internally-developed software $39m in 2025. The capital that matters is **regulatory and clearing**: RHS net capital $3.53bn, clearing-organisation deposits $702m, and the 15c3-3 reserve. Conventional ROIC is meaningless for a broker-dealer (most of the balance sheet is pass-through customer money); the relevant measures are **return on equity (~21% on end-2025 equity) and return on tangible equity** (higher, given only ~$553m of goodwill+intangibles). Growth is capital-light in software but capital-intensive in regulatory terms — each incremental dollar of margin/balance draws incremental net capital.

### IV.12 Free-Cash-Flow Bridge (FY2025, $m)
Net income 1,883 + D&A 86 + provision for credit losses 114 + SBC 305 + deferred income taxes 181 ± customer-balance changes (large, netting to a use via the margin book offset by payables/securities loaned) = **operating cash flow 1,638**; less capex (PP&E 15 + capitalised software 39 = 54) = **free cash flow ~1,584**. Discretionary uses: buybacks $653m and $437m of taxes paid on net share settlement of RSUs. **Distortions to flag:** SBC is a genuine economic cost despite the non-cash add-back; customer-balance changes flow through operating cash flow but are not the firm's money; the deferred-tax benefit is non-cash. **How much is genuinely available to shareholders after maintaining the business, funding regulatory capital, and funding margin-book growth:** ANALYTICAL INFERENCE ~$1.0–1.4bn through the cycle, well below reported FCF in a peak year.

### IV.13 Regulatory Capital & the Cost of Self-Clearing (NEW SECTION)
- **Robinhood Securities LLC (RHS)** — clearing/carrying broker-dealer; **alternative method** (minimum net capital = greater of $0.25m or 2% of aggregate customer debit balances). Net capital: **$2.50bn (2022, req $66m), $2.54bn (2024, req $178m, excess $2.36bn), $3.53bn (2025, req $373m, excess $3.16bn)**. Member's equity $2,790m (2024) → $3,817m (2025). The requirement scales with customer debits (i.e., the margin book), so as balances grow the capital charge rises.
- **Rule 15c3-3 customer reserve:** segregated for customers ~$4,566m (2024) / ~$4,468m (2025); PAB $29m / $18m. RHS became subject to *daily* reserve computation under the December 2024 SEC amendments (threshold $500m average total credits; buffer reduced from 3% to 2% for daily filers).
- **Robinhood Financial LLC (RHF)** — introducing broker; exempt from 15c3-3 under (k)(2)(ii). Member's equity $599m (2024). Critically, **RHF distributed $490m to the parent in 2024** — confirming that the upstreaming channel runs primarily through the introducing broker, because RHS's net-capital rule and credit-agreement covenants constrain its own dividends.
- **Robinhood Derivatives LLC** — FCM, NFA-regulated (minimum adjusted net capital $1m base). Adjusted net capital scaled with event-contract/futures volume: ~$41.7m (Apr 2025) → ~$74.6m (Sep 2025) → **$178.8m (Dec 2025), requirement $10.3m, excess $168.5m**. Segregated customer funds grew alongside (e.g., ~$63m held for U.S. commodity-exchange customers at Sep 2025).
- **Robinhood Crypto LLC** — state money-transmitter licences plus NYDFS BitLicense and FinCEN MSB registration; permissible-investment/like-kind-custody and net-worth/surety requirements vary by state and are **not disclosed at entity level (UNKNOWN in aggregate)**.
- **Committed credit facilities that backstop it all:** RHS 364-day senior secured revolver stepped $2.175bn (Mar 2023) → $2.25bn (Mar 2024, accordion to $3.375bn) → $2.65bn (Mar 2025) → **$3.25bn (Mar 2026, accordion to $4.875bn)**, structured in Tranche A (secured by margin securities, funds margin lending), Tranche B (secured by NSCC deposit-return rights, funds NSCC requirements) and Tranche C (secured by reserve-account funds, funds 15c3-3 reserve). Parent unsecured revolver $1.0bn → $1.125bn.
- **Constraint on upstreaming:** RHS advances/dividends/equity withdrawals require net-capital-rule notification and cannot breach the minimum consolidated tangible net worth, minimum excess net capital, and net-capital-to-aggregate-debits covenants in the credit agreement. Distributable cash therefore flows mainly via RHF.
- **How much capital does a dollar of incremental *volume* require, and what did T+1 change?** ANALYTICAL INFERENCE: the marginal capital per dollar of *trading volume* is **falling**, because T+1 settlement (equities, effective May 2024) halved the settlement window and structurally reduced NSCC VaR-based clearing-fund charges — the very mechanism that produced the ~$3bn deposit demand on 28 January 2021 (of which ~$2.2bn was an "excess capital premium" charge that exceeded RHS's then net capital). But the marginal capital tied to *balances* (margin book, 15c3-3 reserve, net capital = 2% of debits) is **rising** with the balance-sheet-driven model. Net effect: the *settlement-risk* charge is shrinking while the *balance-financing* charge is growing — the cost of self-clearing has shifted from tail-risk collateral to steady-state regulatory capital.

### IV.14 Capital Allocation
- IPO July 2021 raised ~$1.89bn net at $38.00. The ~$3.4bn emergency convertibles raised Jan–Feb 2021 (during the GameStop liquidity event) automatically converted into **137.3m Class A shares** at IPO, with warrants exercisable at $26.60 — a large, non-discretionary dilution event.
- Acquisitions: X1 (~$95m, credit card), Bitstamp (~$200m, crypto exchange), TradePMR (~$300m, RIA custody), and the Marex FCM (now Robinhood Derivatives). Total business-acquisition/asset-acquisition consideration was $399m in 2025.
- Buyback authorisation history: $1.0bn (May 2024), +$500m (April 2025), refreshed to **$1.5bn (March 2026)**. Through Feb 2026, **~$910m of Class A stock (~22m shares at an average $40.64) repurchased**; FY2025 buybacks were $653m (12m shares at $54.30). Timing has been reasonable — heavier buying when the stock was in the $40s.
- No dividend. **Assessment:** disciplined on price, but small in scale relative to SBC-driven issuance; the M&A programme is bolt-on and strategically coherent (crypto, RIA custody, derivatives) rather than transformational.

### IV.15 Return of Capital, Dilution & Share Count
Weighted-average diluted shares were ~906m (2024) and ~919m (2025); end-of-period Class A + Class B rose from ~884.5m to ~901.3m during 2025. Despite $653m of buybacks, the count rose because SBC issuance and RSU settlement (with **$437m paid in withholding taxes on net share settlement** in 2025) outpaced repurchases. **Verdict: buybacks are offsetting, not reducing, dilution.** Management's stated aim of a ~1% annual decline in diluted share count had not yet produced a net reduction on a full-year basis; the "denominator matters" philosophy is directionally right but not yet delivering share-count shrinkage.

### IV.16 One Dollar of Revenue — Two Waterfalls (ANALYTICAL INFERENCE)
- **$1 of transaction revenue:** ~8–10¢ direct brokerage/clearing/exchange/regulatory cost, plus allocations of technology, operations, marketing and G&A, minimal credit loss, then tax — high contribution margin but volatile and cycle-dependent.
- **$1 of net interest revenue:** near-zero direct transaction cost, but it carries a *funding cost* (credit-facility interest) and a *credit-loss provision* (margin and credit-card balances); it is more recurring and balance-driven.
- **Which dollar is worth more:** on a *risk-adjusted, through-cycle* basis the **net-interest dollar is worth more** because it is recurring and less cycle-sensitive; on a *peak-cycle contribution-margin* basis the transaction dollar looks richer. The market's tendency to capitalise peak transaction dollars at a high multiple is the third framing-note trap.

### IV.17 Economic Driver Tree
Funded Customers × assets per customer = Total Platform Assets; Total Platform Assets × monetisation rate (~1.4%) = revenue. Transaction = customers × trades per customer × revenue per trade (with **crypto price as an amplifier**); net interest = interest-earning balances × net spread. **The five variables that explain most financial outcomes:** (1) funded-customer growth; (2) platform assets per customer; (3) crypto price/volume; (4) policy rates; (5) margin-book size. Gold attach rate and PFOF per-unit rates are important secondary levers.

### IV.18 Scenario Model (ANALYTICAL INFERENCE / HYPOTHESIS)
- **(A) Base continuation:** revenue grows mid-teens; margins broadly hold; capital needs scale with the margin book.
- **(B) Crypto winter (crypto revenue −70%):** ~$630m revenue hit (on ~$900m FY2025 crypto base); profit falls sharply, partly cushioned by net interest and options.
- **(C) Rates −300bp:** net interest potentially −$700m–1bn before balance response — the most damaging shock to the *higher-quality* engine.
- **(D) US PFOF ban/material restriction:** strikes options and equities transaction revenue; the most structurally dangerous long-run event because it hits the durable transaction base, not just the cyclical one.
- **(E) Equity bear market:** volumes and asset values fall together; margin book contracts, compounding the net-interest hit.
- **(F) Volatility spike:** volumes up sharply, favourable short-term.
- **(G) Strong execution:** continued product expansion (prediction markets, banking, international, tokenisation) lifts other/transaction revenue.
- **Most dangerous:** a **combined crypto winter + rate cuts + risk-off equity market**, because the two engines' shared driver (retail risk appetite) turns down simultaneously — precisely the correlation the "diversification" story obscures. (The early-2026 crypto and equity sell-off, during which HOOD fell ~55% from its October 2025 high, is a live illustration.)

### IV.19 Sensitivity Analysis
Value creation is most sensitive to, in order: (1) **crypto price/volume** (highest revenue variance); (2) **policy rates** (net interest); (3) **options contract volume**; (4) **margin balances**; (5) **funded-customer growth**. PFOF per-share/per-contract rates, Gold attach rate, and marketing spend are meaningful but second-order. The asymmetry: crypto drives the *upside surprises*, but rates and PFOF regulation drive the *structural downside*.

### IV.20 Revenue-Quality Scorecard & Normalised Profitability
| Line | Predictability | Recurrence | Pricing power | Concentration | Cyclicality | Margin | Capital intensity | Regulatory/disruption risk |
|---|---|---|---|---|---|---|---|---|
| Margin interest | Med-High | High | Med | Low | Med | High | High (net capital) | Med |
| Securities lending | Med | Med-High | Low-Med | Med | Med | High | Med | Med |
| Cash sweep | High | High | Med | Low | Low-Med | High | Low | Med (litigation) |
| Options PFOF | Med | Med | Low | High (wholesalers) | Med-High | High | Low | High (PFOF ban) |
| Crypto transaction | Low | Low | Low | High | Very High | High | Low | High |
| Equities PFOF | Med | Med | Low | High | Med-High | Med | Low | High |
| Gold subscription | High | High | Med-High | Low | Low | High | Low | Low |

**Normalised profitability (the single most useful number; ANALYTICAL INFERENCE):** strip the 2021 convertible-note fair-value charge (~$1.5bn), the 2023 Founders Award Cancellation, and the **2024 $424m benefit** ($369m deferred-tax valuation-allowance release + $55m regulatory-accrual reversal, $0.47 diluted EPS); normalise rates toward a mid-cycle level and the crypto cycle toward trend. Sustainable through-cycle net income is roughly **$1.1–1.5bn** — meaningfully below the $1,883m reported in 2025. This is the number an owner should anchor on.

### IV.21 Valuation-Relevant Economics
Growth durability rests on funded-customer growth and share-of-wallet expansion (retirement, banking, Gold, international). The margin ceiling is genuinely high because incremental transaction costs are trivial and technology is step-fixed. Reinvestment needs are modest in software but regulatory capital scales with balances. FCF quality is good but flattered by the non-cash SBC add-back and by favourable customer-balance timing in peak years. Cyclicality, dilution, and the shared risk-appetite driver are the principal offsets. **What an owner must believe to compound value over 5–10 years:** that retail risk appetite and platform-asset accumulation persist through cycles, that PFOF survives US regulation, that Gold/net-interest/subscription recurring revenue keeps rising as a share of the mix, and that buybacks eventually out-run SBC dilution.

### IV.22 Volume IV Reconstruction — Answers to the Central Questions
- **Real economic engine:** a **retail-risk-appetite monetisation machine** that increasingly earns on *balances* (net interest) as much as on *trades* (PFOF). The self-clearing decision is what lets it capture the balance economics (securities lending, margin, sweep) directly.
- **Highest-quality line:** net interest (margin + securities lending) and Gold subscriptions. **Most fragile:** crypto transaction revenue.
- **Where operating leverage comes from and whether it is durable:** a step-fixed technology/G&A base spread over rising revenue — *structurally durable while revenue grows*, but the specific 2024–25 incremental margins were inflated by a one-time cost reset (headcount cuts correcting admitted 2021 over-hiring) and are **not** repeatable.
- **Capital-light or capital-intensive:** capital-light in software/technology; capital-intensive in the regulatory/clearing capital that scales with the margin book and customer balances.
- **Normalised FCF through the cycle:** ANALYTICAL INFERENCE ~$1.0–1.4bn, materially below the 2025 peak.
- **Most misunderstood balance-sheet item:** the **receivables-from-users/margin book** and the **fractional-share asset + repurchase obligation** — they look like firm assets but are customer-collateralised or fully offset; reading them (or gross leverage) as a normal company's is the central analytical trap.
- **Variable that matters most to long-term earnings power:** **retail risk appetite**, proxied by crypto price and trading volume, with policy rates a close second and US PFOF regulation the key binary risk.
- **Central verdict:** **A structurally improved business that endured a bad cycle, now enjoying an unusually favourable one.** The cost discipline and net-interest scale are durable; the 2024–25 *profit level* is not fully durable. ANALYTICAL INFERENCE: roughly **60–70% of 2024–25 profitability is structural**, with the remainder cyclical (crypto, rates) and one-off (tax/accrual). The business is no longer the cash-burning, dilution-ravaged entity of 2021 — but it is not yet the all-weather compounder its peak-year headline numbers imply.

## Recommendations
1. **Anchor valuation and expectations to normalised earnings (~$1.1–1.5bn), not the 2025 reported $1,883m.** *Threshold to revise upward:* two consecutive years of net-interest growth driven by *balances* (not rates) alongside funded-customer growth above ~8%.
2. **Track crypto revenue and the margin book as the two leading indicators of the shared risk-appetite driver.** *Trigger:* quarterly crypto revenue falling below ~$150m *combined with* a contracting margin book signals both engines turning down together — the most dangerous configuration.
3. **Treat buybacks as dilution-offset, not capital return, until the diluted share count actually falls year-over-year.** *Benchmark:* net diluted share count declining YoY.
4. **Monitor RHS net capital and credit-facility size/utilisation as the true, rising cost of the balance-driven model.** *Trigger:* net capital and facility draws rising faster than revenue means growth is consuming disproportionate regulatory capital and constraining upstreamable cash.
5. **Flag any US PFOF restriction as the single most structurally dangerous event** — it would strike the durable options/equities transaction base, not merely the cyclical crypto line. Watch the SEC/best-execution docket and the ongoing PFOF civil litigation.
6. **Discount peak-cycle Adjusted EBITDA; use GAAP net income adjusted only for genuine one-offs.** SBC of ~$305m is a real cost and a real source of dilution.

## Caveats
- FY2025 figures are company-labelled "preliminary," subject to completion of financial-closing procedures; final audited numbers in the FY2025 Form 10-K (filed Feb 2026) may vary.
- The seven-part net-interest split and the full-year transaction-by-asset-class figures are summed from quarterly disclosures (ANALYTICAL INFERENCE) but reconcile exactly to reported annual totals ($1,109m/$1,514m net interest; $1,647m/$2,628m transaction). Individual asset-class *annual* splits are estimates.
- The 2023 SBC figure and 2019–2020 sub-line splits are approximate (THIRD-PARTY ESTIMATE); treat as directional.
- Normalised-profitability, rate-sensitivity, FCF-availability, and "60–70% structural" ranges are ANALYTICAL INFERENCE with stated assumptions, not company disclosure.
- Robinhood Crypto's aggregate state-by-state money-transmitter net-worth/permissible-investment requirements are not disclosed at entity level (UNKNOWN).
- Margin-rate tiers are a point-in-time schedule (late 2025) that floats with the Fed funds rate, not a full-year average.
- The FY2024 RHS net-capital figure ($2.54bn, excess $2.36bn) is from the FY2024 X-17A-5; the FY2025 figure ($3.53bn, excess $3.16bn) is from the FY2025 X-17A-5 (both CONFIRMED FACT from EDGAR filings, CIK 1699855).