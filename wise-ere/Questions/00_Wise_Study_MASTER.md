# The Wise Enterprise Reverse-Engineering Study

**A forensic institutional teardown of Wise plc / Wise Group plc**

Research cut-off: 8 August 2026
Prepared by: Damascus Research
Volumes I–V complete · Cross-Volume Synthesis included

---

## How to read this document

This study takes Wise apart component by component across five volumes, then reassembles it. Each volume was researched and written as a standalone study; this master edition binds them into one document with a single set of conventions, a canonical figures table, and a synthesis that no individual volume contains.

| Part | Volume | Question it answers |
|---|---|---|
| Front matter | — | Conventions, canonical figures, how to navigate |
| Part I | Corporate, Legal, Regulatory & Institutional Anatomy | Who owns and controls Wise; which entity does what; which regulator supervises which entity |
| Part II | Product, Customer & Money-Movement Architecture | What Wise sells, who buys it, and what physically happens when money moves |
| Part III | Operations, Technology, Data & Organisational Infrastructure | How ~4.7m transactions a day actually get processed safely |
| Part IV | Financial Statements, Revenue Architecture, Unit Economics & Capital | How the economic machine earns, spends and retains money |
| Part V | Management, Culture, Competition, Moat, Risk & Strategic Evolution | Why Wise wins, what is durable, what breaks it, what it becomes |
| Part VI | **Cross-Volume Synthesis** | What the five volumes prove together that none proves alone |
| Appendix A | Canonical Figures Register | The single authoritative value for every material number |
| Appendix B | Reconciliation of Cross-Volume Discrepancies | Where the volumes disagree, and which figure governs |
| Appendix C | Source Hierarchy & Evidence Conventions | How claims were graded |

**Recommended reading order for a first pass:** Part VI (Synthesis) → Appendix A → then Parts II and IV in full. Parts I, III and V are reference-depth.

---

## Conventions governing the whole document

### Evidence classification

Every material claim carries one of six labels. These are not decoration — they are load-bearing, and no inference is silently promoted to fact.

| Label | Meaning |
|---|---|
| **CONFIRMED FACT** | Directly supported by reliable primary evidence |
| **COMPANY CLAIM** | Stated by Wise, not independently verified |
| **THIRD-PARTY ESTIMATE** | Externally reported or estimated |
| **ANALYTICAL INFERENCE** | Reasonably inferred from multiple known facts |
| **HYPOTHESIS** | Possible explanation requiring further evidence |
| **UNKNOWN** | Available evidence is insufficient |

### Reporting-basis convention — read this before any figure

Wise's financial year ends **31 March**. There is a hard basis break in the series:

- **FY2020–FY2025: IFRS, presented in GBP**, reported by Wise plc.
- **FY2026 onward: US GAAP, presented in USD**, reported by Wise Group plc following the 8 May 2026 reorganisation (Jersey-incorporated, UK tax resident; Nasdaq: WSE, LSE: WISE). The former listed parent was renamed Wise Limited.

Three changes happened simultaneously at that break: IFRS → US GAAP, GBP → USD, and the discontinuation of the "underlying income / underlying PBT" alternative performance measures. **These are definitional changes, not economic ones.** The two series are never spliced in this document. Where a figure is quoted, its basis is stated. The bridging source is Wise's "Translation of IFRS financials into US GAAP" RNS of 13 April 2026.

Volumes I, II and III were written primarily against the FY2025 IFRS/GBP base because that was the last fully audited annual report at the time of writing; Volume IV establishes the FY2026 US GAAP/USD base properly. Where the earlier volumes quote £ figures and Volume IV quotes $ figures for the same concept, **Appendix A governs**.

### Currency and rounding

Where both bases are relevant, GBP figures carry the FY and basis inline (e.g. "£145.2bn, FY2025 IFRS"). USD figures default to FY2026 US GAAP. No implied exchange rate is applied across the basis break.

---

# Part VI — Cross-Volume Synthesis

*This section is new. It exists only in the master edition and draws on all five volumes.*

## VI.1 The unified thesis

Read individually, the five volumes describe five different companies: a licensed multi-entity financial group, a consumer money-transfer app, a microservices platform, a rate-geared balance-sheet business, and a price-led competitor. Read together, they describe one thing.

**Wise rebuilt the settlement layer for retail cross-border payments, and then wrapped licensing, compliance, treasury and distribution around it.** Everything else — the app, the card, the multi-currency account, the interest income, even Wise Platform — is either an input to that rebuild or a way of monetising it.

The single most important sentence in the entire study is the one established in Volume II and confirmed by every subsequent volume: **a Wise "cross-border" transfer is two synchronised domestic payments linked by an internal ledger entry.** Money does not cross a border for the individual customer. It crosses in bulk, periodically, when treasury rebalances a depleted pool. Once that is understood, the licensing architecture (Part I), the direct-rail estate (Part II), the Treasury Ledger (Part III), the ~0.5% take rate (Part IV) and the cost-leadership strategy (Part V) all stop being separate facts and become consequences of one architectural choice made around 2011.

## VI.2 The single causal model

The five volumes collectively evidence one flywheel with two revenue cylinders.

**The cost engine (the primary loop):**

```
Local licences + direct payment-system membership   (Part I)
        ↓
Two synchronised domestic legs + internal netting    (Part II)
        ↓
Real-time double-entry Treasury Ledger + automation  (Part III)
        ↓
Falling unit cost per transaction
        ↓
Deliberate price cut: take rate 0.73% → 0.51%        (Part IV)
        ↓
Customers tell other customers (~70% organic)        (Part V)
        ↓
More volume → deeper netting → lower unit cost  ⟲
```

**The balance engine (the secondary loop, switched on by rates in FY2023):**

```
More volume → more customers hold balances
        ↓
Customer holdings $39.0bn (FY2026)
        ↓
Net interest income + card interchange
        ↓
Funds further price cuts on the primary loop  ⟲
```

The second loop is why roughly half of net revenue is now non-cross-border. It is also, as Volume IV establishes, the lower-quality half: rate-driven, regulatory-contingent, and not durable.

## VI.3 What the volumes prove together that none proves alone

**1. The moat is a stack, and the binding agent is demand, not infrastructure.**

Volume I catalogues 70+ licences. Volume II catalogues 8+ direct rails. Volume III catalogues the ledger and the netting engine. Read separately, each looks like the moat. Read together with Volume V's replication test, the conclusion inverts: **licences, rails and technology are all purchasable with enough time and capital. What is not purchasable is the ~19m organically-acquired customer base and the corridor liquidity depth that only volume creates.** A well-funded rival could buy every input and still face £5–10bn of customer acquisition cost to reach the volume at which netting makes the cost model work. The moat is the demand, and the infrastructure is what converts demand into a cost advantage.

This reframes the conventional read. Licences are the entry ticket, not the moat — a point the OCC proved in July 2026 by denying Wise a charter *despite* its 70+ existing licences.

**2. Reported profitability is being misread, and Wise says so itself.**

Volume IV's most consequential finding is not a number but a mechanism. Wise retains the first 1% of yield on customer balances; above 1%, the framework intends to retain 20% and return 80% to customers. It cannot actually return the full 80% — mainly because UK regulation prevents paying interest on e-money balances, and US customers must opt in. The unreturned portion **accrues to profit by accident**.

The consequence: the FY2026 income-before-tax margin of 26.4% is not the structural margin. The durable figure is the **15–20%** Wise itself guides to. The ~6–10 point gap is a regulatory accident that will close as Wise resolves the barriers — which means margin compression is the *success* case, not the failure case. Any reader treating 26% as the run-rate has misunderstood the business.

**3. The binding constraint flipped in 2024, and it flipped onto the growth path.**

Through roughly 2023, Wise's constraint was infrastructural: get the licence, build the rail, connect the scheme. Volume III and Volume V establish that the constraint is now **compliance credibility** — and that this constraint gates not just remediation but the next strategic move:

| Event | Date | What it blocked |
|---|---|---|
| FCA fine of CEO Käärmann (£350,000) | 28 Oct 2024 | Governance credibility |
| CFPB consent order (reduced to $45,000 + ~$450k redress) | 2025 | Conduct remediation |
| US six-state AML consent order ($4.2m) | 9 Jul 2025 | SAR lookback; 2 years of quarterly reporting |
| Belgian criminal AML investigation (~€500m) | disclosed 1 Jun 2026 | EEA entity exposure; ~20% intraday share fall |
| OCC denial of national trust bank charter | Jul 2026 | **Direct US rails — the single largest remaining cost opportunity** |

The OCC denial is the crux. Wise's remaining large cost inefficiency is the US, where it still reaches rails indirectly through Community Federal Savings Bank. The charter was the fix. The charter was denied on AML grounds. **Compliance failure is therefore not a side-issue; it is directly capping the cost engine that is the entire thesis.**

## VI.4 The central tension

The culture that built the cost advantage is the culture that produced the compliance failures.

Volume III documents autonomous squads, weak code ownership, no dedicated manual QA, 120+ deploys a day. Volume V documents relentless price cuts, ~70% organic growth and an owner-operator CEO on a ~£200k salary. That combination of speed and alignment is precisely what produced a cost base no incumbent could match.

It is also, on the regulators' own findings, what produced late SAR filings, transaction-monitoring data-integrity failures and inadequate independent AML review. Autonomy optimised for velocity collides with financial-crime control, which is inherently centralising and veto-bearing.

**Wise's defining management problem for the next three years is to re-centralise control without killing the engine that made it cheap.** The evidence that it knows this: a Group Chief Compliance Officer hired from Credit Suisse/Goldman in November 2025, FinCrime compliance managers embedded inside product squads, and a claimed third of global staff working on financial crime. The evidence that it is unresolved: the OCC denial in July 2026 and an active Belgian criminal file.

## VI.5 What would falsify the thesis

Specific, checkable markers — stated so this study can be audited against reality rather than re-narrated:

| If this happens | The thesis weakens because |
|---|---|
| Take rate falls below ~0.45% *without* a volume acceleration | Price cuts have stopped buying growth; the flywheel has become value destruction |
| Organic acquisition share falls materially below ~70% | The near-zero-CAC advantage — the least replicable component — is eroding |
| Belgian case results in a criminal conviction or a licence condition on Wise Europe SA | EEA passporting, the second-most-important permission, is impaired |
| A second charter/permission denial after remediation | Compliance is a structural, not fixable, ceiling |
| Wise Platform stalls below ~7% of volume by FY2028 | The infrastructure identity is aspiration, not trajectory |
| Net interest income falls without transaction revenue closing the gap | The balance engine was load-bearing, not supplementary |

## VI.6 What Wise is becoming

Ranked by probability, on the evidence assembled:

| Hypothesis | Probability | Strongest evidence |
|---|---|---|
| International payments network / global financial utility | ~45% | Platform >50% long-term vision; 8+ direct rails; cost-plus infrastructure economics |
| B2B financial infrastructure | ~25% | Platform + Business converging; 85+ partners; competes with Airwallex, Corpay |
| Global multi-currency account | ~20% | ~half of net revenue now non-cross-border; $39bn holdings; $43.6bn card spend |
| Remittance / FX company | ~10% | Still the cash engine, but not the direction of travel |

**Synthesis:** a global payments-infrastructure utility with a consumer and business account front-end that funds it. The account is the customer-acquisition and balance-gathering layer; the network is the asset.

## VI.7 Implications for a multi-jurisdictional fintech build

*This section applies the study to the reader's own context rather than to Wise. It is analytical inference throughout.*

**On sequencing licences.** Wise built UK EMI first, then Belgium for EEA passporting after Brexit forced the split. A build starting from a Lithuanian EMI has the EEA leg first and faces the mirror-image problem: the UK is a separate authorisation, not a passport, and the FCA's post-2023 safeguarding regime is materially more demanding than when Wise was authorised. Budget the UK EMI as a full second application, not an extension.

**On sponsor-bank dependency — the single most transferable lesson.** Wise, at $243.5bn of annual volume, fifteen years old, with 70+ licences and BBB investment-grade ratings, **still cannot get its own US rails.** The OCC denied it in July 2026. If Wise cannot clear that bar, no earlier-stage entrant should model sponsor-bank independence into its plan at all. Architect for sponsor *substitutability* from day one: dual-sponsor from launch if the economics tolerate it, contractual portability of the BIN and ledger, and no product feature that only one sponsor can support. The post-Synapse environment makes this a survival question, not an optimisation.

**On Nigeria.** Wise's NGN history is the most instructive available case study, precisely because Wise kept failing at it: naira payouts launched 2015, suspended 2016, resumed 2017, suspended 2020, USD-to-Nigeria suspended 2022, resumed 2024 only after the CBN's January 2024 directive requiring remittances be paid in naira. Even now NGN is **payout-only** — not a send currency, not a balance currency, no card. The binding constraints were FX scarcity and regulatory reversal, not technology. Any Nigeria phase should assume the corridor will be suspended at least once and should be architected so that a suspension degrades one corridor rather than breaking the product.

**On safeguarding as a financing problem.** Volume IV surfaces the most under-appreciated piece of financial engineering in the study: Wise's **Safeguarding via Comparable Guarantees**, expanded to £845.0m / $1,119.1m backed by investment-grade insurance sureties. Under FCA rules an authorised insurer's guarantee can substitute for holding secure liquid assets — which converts trapped safeguarding cash into deployable operational liquidity. This is only relevant once balances are material, but it is worth knowing it exists before designing the treasury model, because it changes the answer to "how much working capital does the balance book consume."

**On price.** Wise's ~0.5% take rate is survivable only because of direct rails plus netting at $243.5bn of volume. It is a *consequence* of scale, not a strategy available to a new entrant. Competing with Wise on headline price without Wise's cost base is a route to funding customers' transfers out of equity. Compete on segment, corridor depth, UX, or a use case Wise underserves — not on the number.

**On the compliance budget.** Wise states around a third of its global team works on financial crime, and it still drew four enforcement actions in two years. Treat financial-crime headcount as the cost line that scales closest to linearly with customers and jurisdictions — the one genuine diseconomy in an otherwise beautifully scaling model — and staff it ahead of growth rather than behind it. Wise's own experience is that the regulator arrives before the org chart catches up.

## VI.8 Ten cross-volume conclusions

1. Wise is a settlement-layer rebuild wrapped in licences, compliance, treasury and distribution — not a remittance company that scaled.
2. A cross-border transfer is two domestic payments; money crosses borders only in periodic bulk rebalancing.
3. The moat is a stack, and its binding agent is the organically acquired customer base plus netting depth — the only components not purchasable.
4. Licences are the entry ticket, not the moat; the OCC denial proved accumulated licences guarantee nothing.
5. The 26.4% FY2026 margin is inflated by a regulatory accident; the durable structural margin is 15–20%.
6. Roughly half of net revenue is now non-cross-border — and it is the lower-quality, rate-driven half.
7. The binding constraint flipped from infrastructure to compliance credibility in 2024, and now gates the growth path itself.
8. The culture that produced the cost advantage produced the compliance failures; re-centralising control without killing velocity is the defining management problem.
9. Cheaper future rails — stablecoins, Nexus-style interoperability — more likely help Wise than kill it, because the moat is the wrapper, not the rail.
10. Wise is becoming a global payments-infrastructure utility with an account business funding it.

---

# Appendix A — Canonical Figures Register

**Where any volume disagrees with this table, this table governs.** Basis: FY2026 US GAAP / USD unless stated. FY ends 31 March. As of 8 August 2026.

## Scale and customers

| Figure | Canonical value | Basis | Note |
|---|---|---|---|
| Active customers | **18.9m** | FY2026 | Wise's own release rounds to "19 million"; use 18.9m in tables |
| Personal customers | 14.87m | FY2025 IFRS | FY2026 split not separately disclosed |
| Business customers | 0.697m | FY2025 IFRS | FY2026 split not separately disclosed |
| Cross-border volume | **$243.5bn** | FY2026 | £145.2bn on the FY2025 IFRS base |
| Card spend | **$43.6bn** | FY2026 | Some Wise materials round to $44bn |
| Customer holdings | **$39.0bn** | FY2026 | $30.0bn on balance sheet + ~$9bn Wise Assets |
| Transactions per day | ~4.7m | 2026 | Third-party (American Banker) |

## Financials

| Figure | Canonical value | Basis |
|---|---|---|
| Net revenue | **$2,502.8m** | FY2026 US GAAP |
| Transaction revenue | $1,893.6m | FY2026 |
| — Cross-border | $1,257m | FY2026 |
| — Card | $392m | FY2026 |
| — Other | $245m | FY2026 |
| Interest income on customer balances (gross) | $806.1m | FY2026 |
| Interest paid to customers | $196.9m | FY2026 |
| Income before tax | **$660.4m (26.4% margin)** | FY2026 |
| Net income | $498.7m | FY2026 |
| Total assets | $33,259.8m | 31 Mar 2026 |
| Shareholders' equity | $1,925.2m | 31 Mar 2026 |
| Underlying free cash flow | £332.7m (117.9% conversion) | FY2025 IFRS |
| Rate sensitivity | ~$40m of IBT per 25bp | H1 FY2026 balances |

## Take rate

| Period | Take rate |
|---|---|
| FY2020 | ~0.73% |
| FY2021 | 0.70% |
| FY2022 | 0.63% |
| FY2023 | ~0.69% |
| FY2024 | 0.67% |
| FY2025 (avg) | 0.58% |
| Q4 FY2025 | 0.53% |
| **FY2026 (avg)** | **0.52%** |
| **Q4 FY2026** | **0.51%** |
| Personal Q4 FY2026 | 0.56% |
| Business Q4 FY2026 | 0.39% |

## Regulatory and structural

| Figure | Canonical value | Note |
|---|---|---|
| Licences held | 70+ | Wise statement, FY2025 |
| Direct payment-system connections | **8 live** | Philippines InstaPay was the sixth (FY2025); Brazil Pix and Japan Zengin took it to eight |
| Own funds requirement | £293,376k | FY2026; Fixed Overheads Requirement binding |
| Eligible CET1 capital | £1,409,993k | FY2026; ~481% surplus |
| Safeguarding via Comparable Guarantees | £845.0m / $1,119.1m | 31 Mar 2026; investment-grade insurance sureties |
| Employee Share Trust purchases | ~$470m / 35.9m shares | FY2026 |
| Share buyback | up to £405m | Announced 26 Jun 2026; executing 21 Jul 2026 – 31 Mar 2027 |
| Credit rating | BBB stable (S&P and Fitch) | Published 3 Apr 2025 |

---

# Appendix B — Reconciliation of Cross-Volume Discrepancies

The volumes were written sequentially against a moving evidence base. The following differences are real and are resolved here rather than silently smoothed.

| # | Item | Appears as | Resolution |
|---|---|---|---|
| 1 | Active customers | "19m" (Vols II, III) vs "18.9m" (Vols IV, V) | **18.9m.** Wise's release rounds up; the precise figure governs in tables. |
| 2 | Card spend | "$44bn" (Vol II) vs "$43.6bn" (Vols IV, V) | **$43.6bn.** Rounding only. |
| 3 | Direct rail connections | "sixth direct integration" (Vol I, FY2025 language) vs "8+" (Vols II, III) | **8 live.** The "sixth" was Philippines InstaPay at FY2025; Pix and Zengin brought it to eight once live. Both statements are true at their respective dates. |
| 4 | Headcount | 6,151 monthly average / >6,500 at 31 Mar 2025 (Vols III, IV) vs ~10,332 (third-party tracker, Vol III) | **6,151 monthly average FY2025** is the audited figure. The tracker gap is unreconciled and most plausibly reflects contractors and outsourced servicing — labelled UNKNOWN, not resolved. |
| 5 | Wise plc registration number | 07209813 vs 13211214 (Vol I) | **07209813 is Wise Payments Limited**, the operating EMI. The listed holding company was a separate England & Wales entity (13211214, originally "456 Newco plc"). The group MIFIDPRU footer conflates them. |
| 6 | Currency basis | £ figures (Vols I–III) vs $ figures (Vols IV–V) | Not an error. FY2021–25 IFRS/GBP; FY2026 US GAAP/USD. **Never spliced.** See front matter. |
| 7 | "Underlying" measures | Used in Vols I–IV, absent in FY2026 | The underlying income / underlying PBT APMs were discontinued at the US GAAP transition. The same economics reappear as the gap between the 15–20% target margin and the 20–25% reported range. |
| 8 | Interest income framing | "first 1% / above 1%" (IFRS) vs "net interest income" (US GAAP) | Same mechanism, different presentation. Appendix A carries the US GAAP figures. |
| 9 | CFPB penalty | "$2m originally" vs "$45,000" | Both correct: originally $2m, **amended down to $45,000** plus ~$450k redress. |
| 10 | Platform share of volume | "4%" (FY2025) vs "~5%" (H1 FY2026) | Both correct at their dates; **~5%** is current. Targets: ~10% medium-term, >50% long-term vision. |

## Known unknowns carried forward

These were not resolvable from public evidence and are recorded rather than guessed:

- FY2026 per-executive single-figure remuneration (particularly the CFO).
- Wise Group plc's Jersey registration number.
- Internal chart-of-accounts and ledger schema; reconciliation break-handling.
- Current KYC and sanctions-screening vendor stack (build vs buy split).
- Published SLOs, availability targets and major-incident history.
- Per-corridor economics, internal match rates, and the Wise Platform take rate.
- Disclosed fraud-loss figures.
- Outcome of the Belgian criminal investigation into Wise Europe SA.
- Whether a GENIUS Act stablecoin refiling succeeds, and whether a Fed master account follows.

---

# Appendix C — Source Hierarchy & Evidence Conventions

Sources were prioritised in the following order, and primary evidence was preferred wherever it existed:

1. Wise annual reports and regulatory filings (including MIFIDPRU 8 disclosures)
2. SEC filings (Form 20-F, 6-K) and LSE RNS announcements
3. Investor presentations, earnings releases and call transcripts
4. Wise customer agreements, pricing disclosures and product documentation
5. Wise engineering publications, API/Platform documentation, job descriptions and open-source repositories
6. Regulators and central banks — FCA, National Bank of Belgium, Bank of England, OCC, CFPB, FinCEN and US state regulators, MAS, APRA/ASIC/AUSTRAC, RBI, Central Bank of Brazil, Japan FSA
7. Corporate registries, court records and official legal documents
8. Reputable academic research and financial journalism
9. Specialist payments publications

SEO-oriented fintech blogs, comparison sites and affiliate content were not relied on where primary evidence existed. For strategically significant claims, sources were triangulated. Where reputable sources disagreed, the disagreement is identified, dates compared, and uncertainty preserved rather than resolved by false precision.

---

*End of the Wise Enterprise Reverse-Engineering Study.*
