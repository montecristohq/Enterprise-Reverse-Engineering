# The Wise Enterprise Reverse-Engineering Study

**A forensic institutional teardown of Wise plc / Wise Group plc**

Research cut-off: 8 August 2026
Prepared by: Damascus Research
Volumes I–V complete · Cross-Volume Synthesis included

---

## Table of Contents

- [The Wise Enterprise Reverse-Engineering Study](#the-wise-enterprise-reverse-engineering-study)
  - [How to read this document](#how-to-read-this-document)
  - [Conventions governing the whole document](#conventions-governing-the-whole-document)
- [Part I — Corporate, Legal, Regulatory & Institutional Anatomy](#part-i-corporate-legal-regulatory-institutional-anatomy)
- [Part II — Product, Customer & Money-Movement Architecture](#part-ii-product-customer-money-movement-architecture)
- [Part III — Operations, Technology, Data & Organisational Infrastructure](#part-iii-operations-technology-data-organisational-infrastructure)
- [Part IV — Financial Statements, Revenue Architecture, Unit Economics & Capital](#part-iv-financial-statements-revenue-architecture-unit-economics-capital)
- [Part V — Management, Culture, Competition, Moat, Risk & Strategic Evolution](#part-v-management-culture-competition-moat-risk-strategic-evolution)
- [Part VI — Cross-Volume Synthesis](#part-vi-cross-volume-synthesis)
  - [VI.1 The unified thesis](#vi1-the-unified-thesis)
  - [VI.2 The single causal model](#vi2-the-single-causal-model)
  - [VI.3 What the volumes prove together that none proves alone](#vi3-what-the-volumes-prove-together-that-none-proves-alone)
  - [VI.4 The central tension](#vi4-the-central-tension)
  - [VI.5 What would falsify the thesis](#vi5-what-would-falsify-the-thesis)
  - [VI.6 What Wise is becoming](#vi6-what-wise-is-becoming)
  - [VI.7 Implications for a multi-jurisdictional fintech build](#vi7-implications-for-a-multi-jurisdictional-fintech-build)
  - [VI.8 Ten cross-volume conclusions](#vi8-ten-cross-volume-conclusions)
- [Appendix A — Canonical Figures Register](#appendix-a-canonical-figures-register)
  - [Scale and customers](#scale-and-customers)
  - [Financials](#financials)
  - [Take rate](#take-rate)
  - [Regulatory and structural](#regulatory-and-structural)
- [Appendix B — Reconciliation of Cross-Volume Discrepancies](#appendix-b-reconciliation-of-cross-volume-discrepancies)
  - [Known unknowns carried forward](#known-unknowns-carried-forward)
- [Appendix C — Source Hierarchy & Evidence Conventions](#appendix-c-source-hierarchy-evidence-conventions)

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


---

# Part I — Corporate, Legal, Regulatory & Institutional Anatomy

#### An institutional-grade forensic reverse-engineering study | Research cut-off: 8 August 2026


---

### TL;DR
- **Wise is controlled by its founder-CEO and legally engineered around a single UK-authorised e-money institution.** As of the FY2026 reorganisation, the group's ultimate parent is **Wise Group plc, a Jersey-incorporated, UK-tax-resident company** (Nasdaq: WSE; LSE: WISE) that on 8 May 2026 became parent of **Wise Limited (formerly Wise plc)**. Co-founder Kristo Käärmann holds ~18% of the economics but, via nine-vote Class B shares, would command >50% of votes — contractually capped at one vote below 50% while he remains CEO (falling to below 35% if he ceases to be CEO). Real control sits with Käärmann; economic ownership is dispersed across institutions (Baillie Gifford ~10.5% of Class A) and the founders.
- **The regulatory estate is the moat, and one entity is the crown jewel.** Wise operates 80+ licences across dozens of jurisdictions, but the economically decisive permissions are the UK EMI licence held by **Wise Payments Limited** (FCA FRN 900507) and the Belgian payment-institution licence held by **Wise Europe SA** (NBB, No. 0713629988), which passports across the EEA. The rarest asset is direct settlement access to national payment systems (UK Faster Payments/Bank of England RTGS, plus 7 others), where Wise was the first non-bank to obtain several connections.
- **The architecture is under real stress in 2026.** A $4.2m US six-state AML consent order (9 July 2025), a CFPB order (2025), a Belgian criminal money-laundering investigation of Wise Europe SA (>€500m/$569m, disclosed 1 June 2026), the FCA's £350k fine of the CEO (28 Oct 2024), and the OCC's 21 July 2026 denial of Wise's national trust bank charter together reveal that Wise's binding constraint is no longer technology or licensing breadth — it is financial-crime compliance execution at scale.

---

### Key Findings

1. **[CONFIRMED]** Founded January 2011 in London as TransferWise by Estonians Taavet Hinrikus (Skype's first employee) and Kristo Käärmann (ex-Deloitte/PwC). The original vehicle was registered by Käärmann in England on 31 March 2010 as "Exchange Solutions," renamed TransferWise (2012) and Wise (Feb 2021).
2. **[CONFIRMED]** Direct listing on the LSE on 7 July 2021: shares opened at 800p and closed at 880p, giving a **£8.75bn (~$12bn) market value** — the first direct listing of a tech company in London and, at the time, the largest such deal. It raised no primary capital; existing holders sold to the market. First trades began at 11:22am BST under ticker WISE.
3. **[CONFIRMED]** On 28 July 2025 shareholders approved moving the primary listing to the US, bundled with a controversial 10-year extension of Class B supervoting rights (previously due to sunset in 2026). Co-founder Hinrikus (via Skaala Investments, ~5%) publicly opposed the bundling as "inappropriate and unfair." The scheme was court-sanctioned 27 April 2026; effective 8 May 2026; Nasdaq trading began 11 May 2026.
4. **[CONFIRMED]** A Jersey topco (Wise Group plc) was inserted via a Part 26 Companies Act 2006 scheme of arrangement, 1:1 share exchange, dual-class structure retained, nominal values redenominated to USD ($0.01 Class A; $0.000000001 Class B). Old Wise plc renamed Wise Limited.
5. **[CONFIRMED]** FY2026 (year to 31 Mar 2026): active customers up 21% to **19 million**; cross-border volume up 31% to **$243.5bn**; net revenue **$2,502.8m** (+19%); **income before tax $660.4m** (26.4% margin); customer holdings **$39bn** (incl. $9bn Wise Assets). Reporting shifted to US GAAP and USD.
6. **[CONFIRMED]** Group held >£1.29bn CET1 capital vs a £219.8m own-funds requirement (FY2025) — a **590.41% surplus buffer**. The binding requirement is the Fixed Overheads Requirement (£219.8m), not the K-factor (£40.0m) or permanent minimum (£6.4m).
7. **[CONFIRMED]** Customer money is **safeguarded (not deposited)**; roughly ~60% in government securities/money-market funds and ~40% cash at banks (e.g., JPMorgan Chase for EU cash; BlackRock and State Street MMFs). Wise earns interest income on safeguarded balances; separately, "Wise Assets" passes MMF returns (managed by BlackRock) to customers.
8. **[CONFIRMED]** Wise depends on **Community Federal Savings Bank (CFSB)** as US card issuer and sponsor bank in states where Wise lacks its own money-transmitter licence — a concentration risk underscored by an OCC AML enforcement action against CFSB.

---

### Details

#### I.1 Origin and Corporate Institutional Evolution

| Date | Event | Structural change / capability gained | New dependency or obligation |
|---|---|---|---|
| 31 Mar 2010 | Käärmann registers "Exchange Solutions" (England) **[CONFIRMED]** | Legal shell created | UK company law |
| Jan 2011 | TransferWise launches; freelance-built MVP **[CONFIRMED]** | P2P currency-matching model (funds don't cross borders) | Needs two-sided currency flow to net |
| Aug 2011 | Seedcamp seed ~$72,000 **[CONFIRMED]** | First external capital | — |
| 2012 | Renamed TransferWise; ~$1.3m seed (IA Ventures, Index, Thiel, Levchin) **[CONFIRMED]** | Core tech build | VC governance |
| May 2013 | $6m Series A led by Valar Ventures (Thiel) **[CONFIRMED]** | Valar becomes long-term anchor investor | — |
| Jun 2014 | $25m Series B (incl. Richard Branson/Virgin) **[CONFIRMED]** | European expansion | — |
| Jan 2015 | $58m Series C led by Andreessen Horowitz **[CONFIRMED]** | a16z anchor | — |
| 2016 | Unicorn status (~$1.1bn); total raised ~$117m **[CONFIRMED]** | Scale | — |
| 2017 | Borderless (multi-currency) account + Mastercard debit launched; profitable since 2017 **[CONFIRMED]** | Shift from pure remittance to account/card | Card-network + sponsor-bank reliance |
| 2018 | First non-bank direct member of UK Faster Payments + Bank of England settlement account **[CONFIRMED]** | Bypasses sponsor banks in GBP; lower cost/faster | Direct BoE settlement obligations |
| Sep 2020 | First EU direct access via Central Bank of Hungary (VIBER/GIRO) **[CONFIRMED]** | Domestic HUF rails | Central-bank participant duties |
| Feb 2021 | Rebrand TransferWise → Wise **[CONFIRMED]** | Broader "money management" positioning | — |
| 7 Jul 2021 | Direct listing on LSE (£8.75bn close) **[CONFIRMED]** | Public currency, broadened ownership, OwnWise customer-shareholder programme | Public-market disclosure; dual-class scrutiny (excluded from FTSE 100 due to dual class) |
| 2022–2025 | Wise Platform scales (Morgan Stanley, Standard Chartered, Nubank, Monzo, N26, Google Pay) **[CONFIRMED]** | B2B2C infrastructure revenue | Partner concentration |
| 28 Oct 2024 | FCA fines CEO Käärmann £350k **[CONFIRMED]** | Governance/reputational | SMCR scrutiny |
| Jan/May 2025 | CFPB consent order (amended to ~$45k civil penalty) **[CONFIRMED]** | US conduct remediation | CFPB oversight |
| 9 Jul 2025 | US six-state AML consent order ($4.2m) **[CONFIRMED]** | Remediation, SAR lookback | State supervision |
| 28 Jul 2025 | Shareholders approve US primary listing + Class B 10-yr extension **[CONFIRMED]** | Path to Nasdaq; founder control extended | Governance controversy |
| 8–11 May 2026 | Jersey topco inserted; Nasdaq primary listing **[CONFIRMED]** | US capital-market access; US GAAP/USD reporting | SEC 20-F regime; securities class action filed |
| 1 Jun 2026 | Belgian AML criminal probe disclosed (>€500m) **[CONFIRMED]** | Share-price shock (down as much as ~20% intraday) | Criminal-law exposure |
| 21–24 Jul 2026 | OCC denies Wise National Trust charter **[CONFIRMED]** | US direct-rail ambition delayed | Continued sponsor-bank reliance |

**Path dependency.** The founders' P2P "netting" insight created a business whose unit economics improve with matched two-way flow and internalisation — which in turn made direct payment-system access (not correspondent banking) the strategic prize. Every later structural choice (own licences over partners; direct rails over sponsors) descends from that original logic. The 2011 idea that "the funds never crossed the borders" is, fifteen years later, still the reason Wise builds direct national-rail connections instead of paying correspondent-bank spreads.

#### I.2 Group Structure (FY2025 consolidation basis; topco changed May 2026)

**Ultimate parent (from 8 May 2026):** Wise Group plc — Jersey plc, solely UK tax resident, Nasdaq/LSE listed (SEC CIK 2099039; Class A ISIN JE00BQKY0816). Beneath it sits **Wise Limited (formerly Wise plc)** and the operating tree. Prior to that, Wise plc (England & Wales) was the listed parent. Court sanction was 27 April 2026; the scheme became effective at 22:00 London time on 8 May 2026; secondary LSE admission and Nasdaq trading commenced 11 May 2026. **[UNKNOWN]:** the exact Jersey company registration number of Wise Group plc.

**Registration-number caution [CONFIRMED / FLAGGED].** Companies House lists **Wise Payments Limited** (the operating EMI) under number **07209813**; the FY2025 MIFIDPRU 8 disclosure footer prints "Wise plc, Registered number: 07209813," which conflates the operating EMI's number. Primary sources indicate the listed holding "Wise plc" was a separate England & Wales company (number **13211214**, originally "456 Newco plc," renamed Wise plc on 17 June 2021). This is a caution against treating any single "Wise" entity as monolithic — the entity behind a given product, balance, or licence matters.

**Economically important entities (from FY2025 MIFIDPRU 8 disclosure; all 100% owned):**

| Entity | Jurisdiction | Function | Regulatory role |
|---|---|---|---|
| Wise Payments Limited | UK | Core online currency exchange / account | FCA EMI, FRN 900507 — the operational heart |
| Wise Europe SA | Belgium | EEA payments | NBB payment institution, No. 0713629988; EEA passport |
| Wise Assets Europe AS | Estonia | Investments (Wise Assets EEA) | EFSA investment firm 4.1-1/174; EEA passport |
| Wise Assets UK Limited | UK | Investments (Wise Assets UK) | FCA MIFIDPRU investment firm, FRN 839689 — triggers consolidated FCA supervision |
| Wise US Inc | USA (Delaware/NY) | US money transmission | FinCEN MSB; 48-state MTLs + 4 territories; CFSB partner elsewhere |
| Wise Australia Pty Ltd | Australia | AU account | ASIC AFSL 513764; APRA ADI (PPF); AUSTRAC |
| Wise Asia-Pacific Pte Ltd | Singapore | APAC account | MAS Major Payment Institution + CMS licence |
| Wise Payments Japan K.K. | Japan | JP transfers | Type 1 & Type 2 funds-transfer licences (FSA / Kanto Local Finance Bureau, reg. 00040) |
| Wise Brasil Corretora / Instituição de Pagamentos | Brazil | FX broker / payments & e-money | Central Bank of Brazil |
| Wise Payments India Pvt Ltd; Vaho Forex Pvt Ltd | India | Inward PA-CB; outward AD-II | RBI |
| Holding cos: Wise Financial Holdings Ltd, Wise Investments Holdings Ltd, Wise Newco Holdings Ltd | UK | Intermediate holding | — |
| Dormant: Wise Switzerland AG, Wise Payments South Africa, Wise Payments Korea, Wise Payments (Thailand), Wise Payments New Zealand, Wise Newco Limited | Various | Placeholder / wind-down / market-entry | — |

**Why functions are separated:** (1) **Regulation/licensing** — each market's law requires a locally licensed entity (dominant driver); (2) **Risk ring-fencing** — safeguarding and customer-money obligations are entity-specific; (3) **Product architecture** — payments (Wise Europe SA) vs investments (Wise Assets Europe AS) split reflects distinct regulatory regimes; (4) **Historical / market-entry** — dormant shells pre-position for expansion or preserve names.

#### I.3 Ownership and Share Structure

**Dual-class mechanics:** Class A = 1 vote (listed, tradeable); Class B = 9 votes (non-transferable, unlisted, "golden" supervoting). Each Class B corresponds to a Class A. At the 2021 IPO the largest external holders were Valar Ventures (~10.2%), IA Ventures (~9.6%), Andreessen Horowitz (~9.3%), Baillie Gifford (~4.9%), D1 Capital (~3.9%), IVP (~3.7%); founders held roughly a third combined.

**As of 2026 (post-Nasdaq):** Baillie Gifford filed a Schedule 13G reporting **~10.53% of Class A** (108,011,990 shares; sole voting power over 98,802,398). Käärmann holds ~18% economics; Hinrikus/Skaala ~5%. Total voting rights sit around 2.86–2.95bn depending on issuance date; **Käärmann's votes would exceed 50% but are capped at one vote below 50% while he is CEO** (dropping to below 35% if he ceases to be CEO) — bringing exercisable votes to roughly 2.44bn.

**Economic vs voting divergence — the defining governance fact.** Economic ownership is dispersed and institutional; voting control is founder-concentrated by design. Management cannot realistically be removed against Käärmann's wishes while the cap sits just below 50% and Class B carries 9× votes. This is the trade the market accepted in the July 2025 vote, over the objection of co-founder Hinrikus and initial concern from Glass Lewis and ISS.

#### I.4 Governance Architecture

**Board (as of 31 Mar 2025):** David Wells (Chair, ex-Netflix CFO); Kristo Käärmann (CEO); Emmanuel Thomassin (CFO from 1 Oct 2024, after interim Kingsley Kemish and the resignation of Matthew Briers); NEDs Terri Duhon, Clare Gilmartin (Senior Independent Director), Alastair (Alex) Rampell (a16z), Hooi Ling Tan, Ingo Uytdehaage (Audit & Risk Committee Chair), Elizabeth Chambers (Remuneration Committee Chair).

**Committees:** Nomination (Wells), Remuneration (Chambers), Disclosure (Jessica Winter), and a combined Audit & Risk Committee (Uytdehaage). A deep management risk-committee stack sits beneath the board: Group Risk Committee, ALCO, plus Financial Crime, Operational, Regulatory, Credit, Prudential, Market and Liquidity risk committees, and an Emerging Risk Forum, all under a Three-Lines-of-Defence model. Notably, the General Counsel and Chief Risk Officer report to the CTO (not the CEO), and the Global Head of Internal Audit reports to the CFO, with CRO and Internal Audit also reporting jointly to the board for independence.

**Executive pay:** No company-wide annual bonus; heavy equity weighting. The Hybrid LTIP for Executive Directors comprises performance shares (max 325% of salary; measured on relative TSR, volume growth and customer NPS) plus restricted shares (max 325% of salary), with 3-year vesting, 2-year post-vesting holding, and malus/clawback (5 years for EDs, 4 for others). FY2025 aggregate remuneration: Board incl. NEDs £4.65m (9 beneficiaries); Leadership Team (non-board) £9.57m (10); other SMFs/MRTs £2.05m; **total staff remuneration £412.8m across 6,151 beneficiaries.** All permanent staff receive share awards ("Wisers" as owners).

**Revealed priorities (Follow-the-Management).** Capital allocation (≈$470m FY2026 share purchases for the Employee Share Trust plus a planned >$500m programme), relentless direct-rail/licence investment, and continuous price cuts (cross-border take rate fell to ~0.51–0.52%) confirm a genuine volume-and-infrastructure flywheel over near-term margin maximisation — behaviour that matches the stated "mission" rhetoric rather than contradicting it.

#### I.5 Legal Architecture

- **Customer contracts by jurisdiction:** UK customers contract with Wise Payments Limited (English law); EEA customers with Wise Europe SA (Belgian law); US customers with Wise US Inc (plus CFSB under a separate Cardholder Agreement); APAC/others with the local licensed entity. The contracting entity is also the entity that owes the customer their balance.
- **Card terms:** In the US, the Wise Multi-Currency Card is issued by CFSB (an FDIC-insured member institution); Wise provides servicing and is a named beneficiary of the agreement. Elsewhere Wise entities issue via card-network membership/BIN sponsorship (Mastercard/Visa).
- **IP / employment / group services:** Software IP is capitalised centrally, though intangibles are modest (£4.0m at FY2025 after most development cost is expensed); the group runs a functional (not divisional) management structure across 30+ offices; intercompany service and cost-allocation arrangements support the licensed entities. Precise transfer-pricing terms are **[UNKNOWN]** from public sources.
- **Litigation/enforcement:** FCA fine of the CEO (£350k, Oct 2024); CFPB order (2025); US six-state AML consent order (Jul 2025); Belgian criminal AML investigation of Wise Europe SA (2026); and a US securities class action (Rosen Law Firm) covering the 11 May–23 Jul 2026 class period, filed after the Belgian disclosure.

**Design logic:** The legal architecture ring-fences each market's customer-money and regulatory liability inside a locally licensed subsidiary while concentrating group capital and technology centrally. This limits contagion (a problem in one market is contained in one entity) but concentrates reputational and financial-crime risk at group level — precisely the fault-line the 2026 Belgian probe exposes.

#### I.6 Global Regulatory Map (selected; as of research date)

| Jurisdiction | Entity | Regulator | Authorisation |
|---|---|---|---|
| UK | Wise Payments Ltd | FCA | Electronic Money Institution, FRN 900507 |
| UK | Wise Assets UK Ltd | FCA | MIFIDPRU investment firm, FRN 839689 |
| EEA (Belgium) | Wise Europe SA | National Bank of Belgium | Payment institution No. 0713629988; EEA passport to 29 states |
| EEA (Estonia) | Wise Assets Europe AS | EFSA | Investment firm licence 4.1-1/174; EEA passport |
| USA | Wise US Inc | FinCEN + state regulators + CFPB | MSB; MTLs in 48 states + 4 territories; CFSB partner elsewhere |
| Canada | Wise Payments Canada Inc | FINTRAC / Bank of Canada / Revenu Québec | MSB M15193392; PSP; Quebec MSB 902804 |
| Australia | Wise Australia Pty Ltd | ASIC / APRA / AUSTRAC | AFSL 513764; ADI (PPF); reporting entity |
| Singapore | Wise Asia-Pacific Pte Ltd | MAS | Major Payment Institution + CMS licence |
| Japan | Wise Payments Japan K.K. | FSA / Kanto Local Finance Bureau | Type 1 & Type 2 funds-transfer licences (reg. 00040) |
| India | Wise Payments India / Vaho Forex | RBI | PA-CB (Inward); AD-II (outward) |
| Brazil | Wise Brasil Corretora / Instituição de Pagamentos | Central Bank of Brazil | FX brokerage; payment institution/e-money |
| New Zealand | Wise Payments NZ Ltd | DIA | AML supervision |
| Hong Kong | Wise Payments Hong Kong Ltd | Customs & Excise (C&ED) | MSO licence 25-03-03263 |
| UAE | Wise Fintech Network LLC | Central Bank of UAE | Stored Value Facility + Retail Payment Services + remittance |
| Malaysia | Wise Payments Malaysia Sdn Bhd | Bank Negara Malaysia | Remittance / money-changing / e-money |
| Philippines | Wise Pilipinas Inc | Bangko Sentral ng Pilipinas | RTC + Type C EMI/MC/FXD + OPS (code 53-0044-00-000) |
| Israel | Wise ILS Ltd | Israel Securities Authority | Payment Services Licence |
| Indonesia | PT Wise Payments Indonesia | Bank Indonesia | Category 3 PSP (remittance) |
| Chile | Wise Chile SpA | UAF | Money Transfer Company |
| Mexico | Wise Pagos Mexico | CNBV / UBVA | Money transmitter, reg. 22578 (authorised Mar 2026) |
| Thailand | Wise Payments (Thailand) Ltd | Bank of Thailand | E-fund transfer / e-money (entity dormant per FY25 list) |

**Customer-money treatment:** none of these are deposit-taking banks; balances are **safeguarded, not covered by deposit-insurance** (FSCS/FDIC do not apply to ordinary balances; limited FDIC pass-through applies only to opted-in US interest via a program bank; the Estonian Guarantee Fund up to €20,000 applies to EEA Assets).

#### I.7 Own-Licence vs Partner Dependency Matrix

| Capability | Structure | Notes |
|---|---|---|
| Account balances / local details | **A. Own** authorisation (EMI/PI/local licences) | Core; safeguarded not deposited |
| GBP domestic transfers | **A. Own** — direct Faster Payments + BoE settlement | First non-bank direct participant (2018) |
| EUR transfers | **A. Own** — Wise Europe SA; SEPA access; direct in Hungary | EEA passport |
| Other direct rails | **A. Own** — 8 live connections (UK FPS, EU SEPA, Hungary, Singapore FAST, Australia NPP, Philippines Pesonet/InstaPay, Brazil Pix, Japan Zengin); Malaysia PayNet added | ~75% of transfers arrive <20s |
| Card issuance (US) | **B. Partner** — CFSB issuer/sponsor | Concentration risk |
| Card issuance (other) | **E. Combination** — network membership + BIN sponsorship | Mastercard/Visa |
| US money transmission (states without own MTL) | **B. Partner** — CFSB | 48 states own; remainder via CFSB |
| FX / matching / netting | **A. Own** — proprietary treasury engine | Core margin driver |
| Interest/returns (Wise Assets) | **D. Outsourced** — BlackRock/State Street MMFs | Wise passes through returns |
| Safeguarding | **E. Combination** — own obligation; cash at JPMorgan + MMFs + govt bonds | ~60/40 split |
| US direct Fed rails | **Blocked** — sought via national trust charter; OCC denied Jul 2026 | Still reliant on partners |

**Why:** Wise builds its own licence/rails where volume justifies the fixed cost and removes correspondent-bank margin and latency (GBP, EUR, and the 8 direct rails). It uses partners where local licensing is uneconomic (US minor states) or structurally required (US card issuance). The national-trust-charter push was an attempt to convert partner dependency into owned US infrastructure; its denial preserves CFSB dependency.

#### I.8 Regulation as a Competitive Asset

- **Easy to replicate:** a single MSB registration or one state MTL.
- **Hard but obtainable:** a full EMI (UK) or PI (Belgium) licence with EEA passport; MAS MPI; APRA PPF ADI; Japan Type 1 funds-transfer licence.
- **The real moat — the operating system:** direct settlement participation in national payment systems (being the *first non-bank* into UK FPS, Hungary, and the Japan Zengin/Bank of Japan connection) plus the compliance/treasury operating system to run 80+ licences safely. The 2025–2026 enforcement cluster demonstrates the moat's double edge: the same regulatory density that deters entrants imposes an operating burden that Wise itself has struggled to satisfy. **The moat is real; the operating system to occupy it is the actual bottleneck.**

#### I.9 Institutional Dependency Map

| Dependency | Function | Substitutability | Criticality |
|---|---|---|---|
| FCA (UK) | Authorises core EMI + consolidated supervision | None | **Critical** |
| National Bank of Belgium | Authorises EEA passport entity | None (short term) | **Critical** |
| Bank of England (RTGS/FPS) | GBP settlement | Low | **Critical** |
| Card networks (Mastercard/Visa) | Card rails | Low | **Critical** |
| CFSB (US sponsor/issuer) | US card + minor-state transmission | Moderate (other sponsors exist) | **High** |
| JPMorgan Chase (safeguarding cash) | Custody of client cash | Moderate (diversifiable) | **High** |
| BlackRock / State Street (MMFs) | Wise Assets returns | Moderate | **Moderate** |
| National payment operators (SEPA, FAST, NPP, Pix, Zengin, etc.) | Direct domestic rails | Low per market | **High** |
| Cloud/infrastructure vendors | Platform hosting | Moderate | **High** |
| Wise Platform partners (Morgan Stanley, Nubank, Standard Chartered, etc.) | B2B revenue | Diversified (85+) | **Moderate** |

**Single points of institutional failure:** loss/restriction of the FCA EMI or NBB PI licence; termination by CFSB before Wise obtains direct US rails; a card-network membership suspension.

#### I.10 Tax and Intercompany Architecture

- Wise Group plc is **Jersey-incorporated but solely UK tax resident** [CONFIRMED]. This is a listing/redomicile structure for US-market access, not evidence of profit-shifting to a tax haven — profits remain within the UK tax net.
- FY2025 reported PBT was £565m vs underlying PBT £282.1m; a large deferred tax asset (£84.7m at FY2025) is deducted from CET1 because it relies on future profitability. Effective tax rate and granular geographic profit allocation are **[UNKNOWN]** at the level requested; transfer-pricing terms are not public.

#### I.11 Corporate and Regulatory Risk

| Risk | Prob. | Severity | Mitigation | Residual |
|---|---|---|---|---|
| AML/sanctions enforcement | High (materialising) | High | Compliance rebuild; SAR lookbacks; ~1/3 staff in financial crime [company claim] | High |
| Belgian criminal probe adverse outcome | Medium | High | Cooperation; localised in Wise Europe SA | Medium-High |
| Partner-bank (CFSB) termination | Low-Med | High | Sought own US charter (denied Jul 2026); alternate sponsors | Medium |
| Licence loss (FCA/NBB) | Low | Severe | Capital surplus (~590%); governance | Low-Med |
| Safeguarding failure | Low | Severe | Segregation; govt securities; new FCA safeguarding rules (May 2026) | Low |
| Governance/founder-control backlash | Medium | Medium | Voting cap; independent NEDs | Medium |
| Capital shortfall | Very low | Severe | £1.29bn CET1 vs £220m requirement | Very low |

#### I.12 Reconstruction — Answers to the Completion Test

- **Who owns Wise:** Dispersed institutions (Baillie Gifford ~10.5% of Class A) + founders (Käärmann ~18%, Hinrikus ~5%) + early VCs (Valar, IA Ventures, a16z) + employees.
- **Who controls Wise:** Käärmann, via 9-vote Class B shares, capped one vote below 50% while CEO.
- **Legal structure:** Jersey topco (Wise Group plc, UK tax resident) → Wise Limited (ex-Wise plc) → licensed operating subsidiaries per market.
- **Which regulators supervise which entities:** FCA (Wise Payments Ltd, Wise Assets UK Ltd + consolidated group); NBB (Wise Europe SA); EFSA (Wise Assets Europe AS); MAS, APRA/ASIC/AUSTRAC, FSA/KLFB, RBI, Central Bank of Brazil, FinCEN + states + CFPB, and others per market.
- **Which licences enable which products:** UK EMI → accounts/transfers/card in UK; Belgian PI + EEA passport → EEA accounts/transfers; EFSA/Wise Assets licences → investment returns; local licences → local products.
- **Partner reliance:** US card + minor-state transmission via CFSB; Wise Assets returns via BlackRock/State Street MMFs.
- **Most strategically important entity:** **Wise Payments Limited** (UK EMI, FRN 900507) — the operational and licensing heart and the anchor of consolidated FCA supervision.
- **Hardest permission to replace:** Direct non-bank settlement access to national payment systems (UK FPS/BoE and the Japan Zengin/Bank of Japan first-mover positions).
- **Greatest dependency:** Core regulators (FCA/NBB) and card networks; among commercial counterparties, CFSB.
- **Where control sits:** With the founder-CEO, by design.
- **Most misunderstood:** That Wise is a "bank." It is not; balances are safeguarded, not insured deposits, and Wise does not lend them out.
- **Longest to rebuild from zero:** The direct payment-system memberships and the multi-jurisdiction compliance/treasury operating system — years, not months.

**Ten most important conclusions:** (1) Control is founder-locked via a sub-50% voting cap. (2) The UK EMI (Wise Payments Ltd) is the indispensable entity. (3) The moat is direct-rail access + the compliance operating system, not licence count. (4) Safeguarding — not deposit insurance — is the customer-money model, and it is widely misunderstood. (5) Interest income on safeguarded balances (~$40m per 25bp) is a large, exogenous profit swing. (6) Financial-crime compliance is now the binding constraint, evidenced by four 2024–2026 enforcement events. (7) The Jersey topco/Nasdaq move is about capital access and US ambition, not tax. (8) CFSB is the sharpest single commercial dependency, and the OCC denial prolongs it. (9) The legal architecture ring-fences market risk but concentrates group-level reputational/criminal risk (Belgium). (10) Capital is not the risk — the ~590% own-funds buffer is enormous; execution and conduct are.

---

### Recommendations

1. **Treat financial-crime compliance as the gating KPI, not licensing breadth.** The 2025–2026 enforcement cluster (US six-state AML consent order of $4.2m on 9 July 2025; CFPB; Belgian criminal probe; OCC denial citing AML deficiencies) shows the binding constraint. *Benchmark that would change the rating:* an indictment or direct summons of Wise Europe SA in Belgium, or an FCA/NBB remediation escalation, would move the risk rating from High to Severe. Conversely, a clean close of the US SAR lookback (covering closed accounts 1 Mar 2023–1 Mar 2025) and no Belgian charges would de-risk it.
2. **Monitor the CFSB dependency and the second US charter attempt.** If Wise refiles a national trust charter under the GENIUS Act framework and the Fed reopens master-account access for uninsured trusts, US direct-rail independence becomes plausible; continued failure prolongs CFSB concentration risk. *Watch:* Fed's finalised "payment account" policy (proposed May 2026) and any OCC re-engagement.
3. **Track the founder-control cap as the key governance term.** The one-vote-below-50% cap is the single most important governance provision. Any move to remove or extend it, or a Käärmann CEO transition (which drops the cap to below 35%), would materially change the control map and should trigger re-underwriting of governance risk.
4. **Model the rates sensitivity explicitly.** ~$40m of net interest income moves per 25bp of central-bank rate change on ~$26bn of balances — a profitability swing outside management's control and a key variable for any valuation of the FY2027 guidance (net-revenue growth ~mid-15–20% range; income-before-tax margin near the top of 20–25%).

### Caveats
- Some corporate-registry specifics are **[UNKNOWN]** from public sources: the exact Jersey registration number of Wise Group plc; precise transfer-pricing terms; and the granular effective tax rate / geographic profit split.
- The "07209813 vs 13211214" registration-number issue reflects genuine entity-naming complexity (07209813 is Wise Payments Limited's number, also printed on the group MIFIDPRU footer); treat entity-level "Wise" claims with care.
- FY2026 figures are reported on a new US GAAP/USD basis; comparison with prior IFRS/GBP figures requires care. Where this report cites both £ (through FY2025) and $ (FY2026), the currency reflects the reporting basis of the period.
- The Belgian matter is an active criminal investigation of Wise Europe SA with, per Wise, no findings or charges confirmed as of the research date; prosecutors were reported to be finalising a direct summons. Presumption of regularity applies.
- Secondary-source items (e.g., the ~60/40 safeguarding split, some Wise Platform partner counts, "~1/3 of staff in financial crime") are labelled as company claims or third-party estimates and were not all independently reconciled to primary filings.


---

# Part II — Product, Customer & Money-Movement Architecture

*Analytical cut-off: 8 August 2026. FY2025 = year ended 31 March 2025 (IFRS, GBP, audited). FY2026 = year ended 31 March 2026 (US GAAP, USD; results released 25 June 2026). Where a base is mixed, it is flagged.*


---

### II.0 Orientation

Wise sells three customer-facing "solutions" built on one shared infrastructure: the **Wise Account** (personal), **Wise Business** (SMEs), and **Wise Platform** (banks/enterprises). [CONFIRMED FACT — FY2025 report] Beneath them sit shared commercial primitives: cross-border transfer, currency conversion, multi-currency balance holding, local account details, the debit card, receiving, interest/Assets, and the API. This volume takes each apart.

Central operating insight, stated up front: **a "cross-border" Wise transfer usually involves no money crossing a border for that specific customer.** Wise holds prefunded local currency pools and local payment-system access at both ends; the sender pays into a Wise account domestically, and Wise pays the recipient from a Wise account domestically in the destination country. The two domestic legs are linked only by an internal ledger entry. Money crosses borders periodically, in bulk, when Wise **rebalances** depleted pools — not per transaction. This is confirmed by Wise's own FY2025 CEO letter, which describes "a new global payments network that directly connects local banks and payment systems at both ends of every transaction, bypassing the traditional correspondent networks used by banks and other payment services, eliminating costly intermediaries and outdated processes." [CONFIRMED FACT]

---

### II.1 Product Universe

#### Product decomposition

| Product / capability | Target customer | Job-to-be-done | Primary legal entity (by region) | Regulatory basis | Pricing mechanism | Revenue type | Classification |
|---|---|---|---|---|---|---|---|
| International transfer | Personal + Business | Move money abroad cheaply/fast | Wise Payments Ltd (UK EMI); Wise Europe SA (BE PI); Wise US Inc (MSB/MTL + CFSB) | E-money / payment institution + MTL | Fixed fee + variable % (from ~0.33%) on converted amount | Cross-border revenue | Monetization / Acquisition |
| Currency conversion (in-account) | Both | Convert held balances | Same as above | EMI/PI | From ~0.33–0.43% conversion fee | Cross-border revenue | Monetization |
| Multi-currency balance | Both | Hold 40+ currencies | Wise Payments Ltd etc. | E-money issuance | Free to hold | Enables interest income | Retention / Infrastructure |
| Local account details | Both | Receive "like a local" | Regional entity | Passported partnerships / direct rail access | Free (personal); one-off setup fee for some business details | Indirect (drives balances) | Acquisition / Retention |
| Wise debit card | Both (US business cards discontinued 2023) | Spend balances globally | Issued by CFSB in US; Mastercard/Visa program elsewhere | Card-scheme licence via issuer | FX conversion fee; ATM fees over allowance | Card & other revenue (interchange + fees) | Monetization / Retention / Data |
| Digital/virtual cards | Both | Online / mobile-wallet spend | Same as card | Same | Free to generate | Interchange | Retention / Data |
| Interest / Assets | Both (30 countries) | Earn yield on idle balances | Wise Assets UK Ltd; Wise Assets Europe AS | Investment-services licences (e.g. AU AFSL) | Annual mgmt fee ~0.27–0.56% | Fee + AUC growth | Retention / Defensive |
| Batch payments | Business | Pay ≤1,000 payees per file | Regional entity | PI/EMI | Per-transfer fee (each leg priced individually) | Cross-border revenue | Monetization / Retention |
| Invoicing / QuickPay (QR) | Business | Get paid | Regional entity | PI/EMI | Free feature | Indirect | Acquisition / Retention |
| Direct debits | Business (US) + EEA | Pay recurring bills | Regional entity | PI/EMI | Standard fees | Retention | Retention |
| Accounting integrations (Xero, QuickBooks, NetSuite) | Business | Reconcile automatically | N/A (software) | N/A | Free | Switching-cost driver | Retention / Defensive |
| API | Business + Platform | Automate payments | Regional entity / partner contract | PI/EMI + partner model | Same transfer fees; integration/licence fees for Platform | Cross-border + Platform | Infrastructure / Strategic optionality |
| Wise Platform | Banks, fintechs, enterprises | Embed cross-border, accounts, cards | Partner contracts with Wise entities | Correspondent / embedded / enterprise models | Cost+margin transaction fee; integration/licence fees | Cross-border (partner volume) | Infrastructure / Strategic optionality |

**Key confirmations:** batch payments up to 1,000 payees/file, each transfer priced individually [CONFIRMED FACT]; US business debit cards discontinued 2023 [CONFIRMED FACT]; card conversion fees "from 0.33%," ATM allowances vary by region (US: free up to $100/2 withdrawals then $1.50 + 2% over $100; AU: free to A$400/month then 2.69% from 1 May 2026; India travel card free to $200) [CONFIRMED FACT — Wise pricing pages]; Assets/Interest live in 30 countries since first UK launch September 2021 [CONFIRMED FACT — FY2025 report].

**Strategic classification logic.** *Acquisition:* international transfer (the original wedge; word-of-mouth driven — Wise's FY2025 report states "In FY2025 our marketing spend was £53.8 million, an increase of 47%, with our Marketing team growing by 30%" [CONFIRMED FACT — Wise FY2025 report]). *Retention:* Wise Account balances, card, Assets, business integrations. *Monetization:* transfer fees, card FX/interchange, interest income. *Infrastructure/optionality:* Wise Platform and the API.

---

### II.2 Customer Segmentation

FY2025 headline: **15.6m active customers** (Personal 14.87m; Business 0.697m). [CONFIRMED FACT] FY2026 (Wise Group plc FY2026 results, 25 June 2026): "support 19 million people and businesses move $243 billion across the world last year… Customer holdings grew 40% in FY26 to $39 billion and card spend grew 37% to $44 billion." [CONFIRMED FACT] Personal was ~73% of volume (£106.4bn of £145.2bn) and Business ~27% (£38.8bn) in FY2025. [CONFIRMED FACT]

| Segment | Geography (typical) | Main use case | Frequency | Product mix | Acquisition | Switching cost | Price sensitivity |
|---|---|---|---|---|---|---|---|
| Migrants / remittance senders | UK/EU/US/AU → India, Philippines, LatAm, Africa | Send money home | High, recurring | Transfer only | Word-of-mouth | Low | High |
| Expats / dual-life | UK-EU, US-anywhere | Hold multiple currencies, local details | Medium | Account + card + transfer | WoM / organic | Medium-high | Medium |
| International workers / digital nomads | Global | Receive salary, spend abroad | High | Account + card + local details | Organic | Medium-high | Medium |
| Travelers | Global (esp. AU, UK, EU) | Spend abroad without FX markup | Bursty | Card + balances | WoM | Low-medium | Medium |
| Freelancers / sole proprietors | India, LatAm, EE Europe, SE Asia | Get paid by foreign clients | Medium-high | Business receive + convert | Organic / marketplace | Medium | Medium |
| SMEs | Global | Pay suppliers/contractors, receive | Medium-high | Business account, batch, cards, API | Organic / referral | High (integrations) | Medium |
| Larger businesses / marketplaces | Global | Mass payouts | High | API, batch | Sales | High | Low-medium |
| Banks / fintechs / enterprises (Platform) | Global | Embed cross-border | Continuous | Platform API / SWIFT | Enterprise sales | Very high | Low |

Personal VPC (volume per customer) Q4 FY2025 = £3,200, +7% YoY. [CONFIRMED FACT — FY2025 report] Business generates far higher volume per customer: ~£55.6k (£38.8bn / 0.697m) vs Personal ~£7.2k. [ANALYTICAL INFERENCE from FY2025 figures]

---

### II.3 Jobs to Be Done (matrix)

| Segment | Trigger | Functional job | Economic job | Emotional/trust job | Workaround | Switch trigger | Repeat reason | Churn reason |
|---|---|---|---|---|---|---|---|---|
| Migrant | Payday / family need | Get NGN/INR/PHP to a bank account | Maximise amount delivered | "Will it arrive safely?" | Bank wire, MoneyGram, hawala | Discovered hidden bank markup | Predictable low cost, speed | Corridor suspended (e.g. NGN history) |
| Expat | Move country / paid in 2 currencies | Hold + convert | Avoid double FX | Bank-like reliability | Two bank accounts | Mid-market rate + card | Balances + card daily use | Wants deposit insurance |
| Freelancer | Foreign client invoice | Receive USD/EUR/GBP locally | Avoid PayPal 3–4% | Legitimacy/compliance (RBI purpose code) | PayPal, Payoneer | Local account details | Reconciliation, low fees | Compliance friction |
| SME | Scaling cross-border payables | Batch-pay suppliers/contractors | FX transparency, treasury control | Audit trail | Bank + spreadsheets | Accounting integration | Switching cost of integrations | Compliance holds; no lending |
| Bank (Platform) | Legacy correspondent too slow/costly | Offer instant cross-border in-app | New fee income, retention | Regulatory comfort | SWIFT correspondent | Wants speed without rebuild | Deep integration | Build own rails |

Usage archetypes to distinguish (per prompt): transfer utility; primary multi-currency account; travel tool; business operating account; cross-border payable/receivable tool; embedded infrastructure. FY2025: ~50% of personal and ~60% of business customers use multiple features — evidence of migration from single-use "transfer utility" to "account." [CONFIRMED FACT — FY2025 report]

---

### II.4 Customer Journey (stage-by-stage)

| Stage | Customer action | Wise system | Entity | Data generated | Compliance obligation | Friction / failure point | Cost / KPI |
|---|---|---|---|---|---|---|---|
| Discovery | Comparison, WoM | Web / pricing calculator | Marketing | Intent, corridor | — | Price disbelief | CAC; WoM % |
| Signup | Create account | Onboarding | Regional entity | PII | KYC prep | Abandonment | Signup conversion |
| Verification | Upload ID | KYC/KYB engine | Regional entity | ID docs, selfie | KYC/AML, CDD | Doc rejection; KYB up to 10 days | Verification pass rate |
| Funding | Pay in | Pay-in rails (FPS, SEPA, ACH, card) | Regional entity | Payment event | Source-of-funds | Funding fails, card decline | Instant-funding % |
| Currency select | Choose corridor | Quote API | Regional entity | Quote | — | Rate confusion | — |
| Conversion | Confirm | FX/pricing engine | Regional entity | Locked rate (30 min) | — | Rate expiry | Take rate |
| Transfer | Submit | Transfer engine | Regional entity | Transfer object | Purpose code (India), sanctions | — | Volume |
| Authorization | — | State machine | Regional entity | State transitions | — | — | — |
| Compliance/fraud | (invisible) | Screening | Regional entity | Screening result | Sanctions, transaction monitoring | Compliance hold | False-positive rate |
| Clearing/settlement | (invisible) | Payout + Treasury Ledger | Regional entity | Ledger postings | Safeguarding | Payout-rail outage | Instant % |
| Beneficiary receipt | Recipient credited | Local-rail payout | Local entity/partner | Confirmation | — | Wrong details, bounce-back | Delivery time |
| Notification | Push/email | Notifications | — | Event | — | — | — |
| Support/exception | Contact support | Support/ops | — | Ticket | — | Manual intervention | Contact rate |
| Repeat/cross-sell | Reuse / adopt card | Growth | — | Behavior | — | — | Retention, feature adoption |

Rate lock: mid-market rate locked at authenticated quote, "typically remains valid for 30 minutes"; if unfunded and the rate moves ≥5% adversely, Wise auto-cancels and refunds. [CONFIRMED FACT — Wise API docs + Help Centre] Instant-delivery KPI: Wise's FY2025 report states "approximately 65% of transactions being completed in under 20 seconds"; this rose to "75% of our Q4 payments globally completed in under 20 seconds" (Wise Group plc FY2026 results, 25 June 2026). [CONFIRMED FACT]

---

### II.5 Money-Flow Reconstruction (six-layer separation)

For each corridor we separate **(A) customer-facing event, (B) actual cash movement, (C) internal ledger movement, (D) banking-system movement, (E) payment-system movement, (F) accounting recognition.**

#### Corridor 1 — EUR → GBP (balanced, both ends direct rail)
- **A:** Sender in Germany pays EUR; recipient in UK gets GBP; sees mid-market rate, upfront fee, often "instant."
- **B:** EUR moves domestically from sender's bank to Wise's EUR account (SEPA / SEPA Instant); GBP moves domestically from Wise's GBP account to the recipient via UK Faster Payments. No EUR or GBP crosses a border for this transaction.
- **C:** Wise Europe SA's EUR pool credited; Wise Payments Ltd's GBP pool debited; internal FX conversion booked at wholesale rate; the two legs linked by a single ledger transaction ID.
- **D:** Wise's EUR safeguarding account (JPMorgan Chase is the named EU-cash bank per Volume I) receives; Wise's GBP account / Bank of England settlement account pays.
- **E:** Inbound SEPA / SEPA Instant; outbound UK Faster Payments (Wise is a direct participant with a Bank of England settlement account).
- **F:** Wise recognises fee revenue on conversion; the spread between the customer mid-market rate and wholesale execution is a treasury item; the customer balance is a liability throughout.
- **Cross-border reality:** ~0% for this transaction; periodic rebalancing only. [ANALYTICAL INFERENCE + CONFIRMED FACT on rail access]

#### Corridor 2 — GBP → USD
Inbound GBP via Faster Payments to Wise UK; outbound USD via US rails (ACH / wire) from Wise US Inc's USD account. Sender-contracting entity = Wise Payments Ltd (UK); payout entity = Wise US Inc. Internal ledger links the legs; the USD pool depletes over time and needs rebalancing.

#### Corridor 3 — USD → EUR
Inbound USD via ACH to Wise US; outbound EUR via SEPA from Wise Europe SA — the reverse of Corridor 1's dollar leg.

#### Corridor 4 — Africa / emerging-market payout (NGN status)
- **NGN caveat (per prompt):** Wise's NGN history is stop-start — naira payouts launched 2015, suspended May 2016, resumed October 2017, suspended 2020, USD-to-Nigeria suspended November 2022, and NGN payouts resumed 2024 after the Central Bank of Nigeria's January 2024 directive requiring remittances be paid in naira (to bank accounts, or cash below the $200 equivalent). As of 2026 Wise supports **sending to Nigeria in NGN** (recipient credited in naira "directly from Wise's local bank account"), but **NGN is not a supported *sending* currency** and Wise does not offer NGN balances/cards to Nigerian-resident users. [CONFIRMED FACT — Wise send-money page + Tekedia / Fintech Magazine Africa] Why NGN is hard: FX scarcity, repeated regulatory reversals, inability to source true mid-market liquidity, and reliance on local partners. [CONFIRMED FACT]
- **Six-layer:** Sender pays USD/GBP/EUR domestically; Wise converts; the NGN payout is made locally through a Nigerian partner/liquidity arrangement to the recipient's bank account. The inbound leg never reaches Nigeria; only the NGN payout is local.

#### Corridor 5 — USD → INR (regulatorily distinctive)
- **Inward to India** runs under RBI's cross-border regime. **Wise Payments India Private Limited** holds RBI **Payment Aggregator – Cross-Border (PA-CB Inward)** authorisation (in-principle June 2025) for business receipts; historically Wise UK worked with **local partner banks in India** — e.g. **IndusInd Bank's "Indus Fast Remit"** platform, integrated via Wise Platform from June 2023 (Wise's first India partner) — to deliver inward remittances with RBI approval. **Vaho Forex Private Limited** holds RBI **Authorised Dealer Category II (AD-II)** for **outward** remittance and forex cards. [CONFIRMED FACT — Wise regulatory page + IndusInd/PRNewswire]
- **Purpose codes:** every inbound INR credit must carry an RBI purpose code (e.g. family maintenance, P0802 software services, P1002 commissions); Wise builds purpose-code selection into the flow. [CONFIRMED FACT — Wise India blog]
- **Payout rails:** INR delivered to bank accounts (including NRE/NRO) or UPI IDs via India's domestic rails (IMPS/NEFT and UPI). [CONFIRMED FACT]
- **Outward from India:** operationalised under AD-II in FY2025, removing the historical ~US$5,000 per-transaction cap; per-transaction limit later ~₹25 lakh (~$30,000) after the June 2025 PA-CB approval; subject to LRS and permitted-purpose constraints (education, travel, medical). [CONFIRMED FACT — FY2025 report + third-party]
- **Six-layer:** Sender in the US pays USD domestically to Wise US; Wise converts USD→INR; the INR payout is made locally in India via partner/rails to the beneficiary. Documentation (purpose code and beneficiary details for inward; LRS declarations for outward) is required.

#### Corridor 6 — Wise Business payment (batch)
An SME uploads a file of ≤1,000 payees; each payment is a discrete transfer object priced individually; funding is one debit from the business's Wise balance; each payout routes to the cheapest local rail. The ledger books each leg; reconciliation is by transfer ID.

#### Corridors 7–9 — card purchase, ATM withdrawal, Wise Platform transaction — see II.11 and II.13.

---

### II.6 Transaction Teardown (representative EUR→GBP, ~18 steps)

1. Sender initiates; the **Quote API** returns a locked mid-market rate + fee (30-min validity). [CONFIRMED FACT]
2. Sender selects recipient; recipient added to quote (fees, delivery estimate, payout network confirmed).
3. Sender funds via SEPA / SEPA Instant into Wise Europe SA's EUR account. Transfer state = `incoming_payment_waiting`. [CONFIRMED FACT — Wise API]
4. Funds arrive; state → `processing`; **the exchange rate locks and the transfer can no longer be cancelled via API.** [CONFIRMED FACT]
5. **KYC status** confirmed (already-verified sender).
6. **Sanctions screening** on sender, recipient, and payment.
7. **Transaction monitoring / fraud scoring** (Wise: "Processing… means we're doing behind-the-scene activities before the money gets sent to the recipient, such as AML, compliance and fraud checks"). [CONFIRMED FACT]
8. On pass, state → `funds_converted` (FX booked source→target). [CONFIRMED FACT]
9. The **Treasury Ledger** posts double-entry: EUR pool +, GBP pool −, at wholesale rate, "calculating our assets and liabilities with unwavering accuracy and in real time" and feeding "trading teams to manage foreign exchange exposure risks and to ensure each entity has enough liquidity." [CONFIRMED FACT — Wise Treasury Ledger engineering job specs]
10. Liquidity check on the GBP pool; payout initiated.
11. Outbound GBP via **UK Faster Payments** from Wise's settlement account. State → `outgoing_payment_sent` — "the final state… it doesn't mean the money has arrived in the recipient's bank account, just that we have sent it from ours." [CONFIRMED FACT]
12. Recipient's bank credits recipient (often <20s).
13. **Notification** to sender and (if email given) recipient.
14. **Reconciliation:** ledger postings matched to bank-statement lines / payment-system position (events reconciled by `occurred_at` since ordering isn't guaranteed). [CONFIRMED FACT]
15. **Fee** recognised as revenue; **FX spread** recognised as treasury income/cost.
16. **Third-party cost:** rail fees (Faster Payments marginal cost is very low), any partner cost.
17. **Failure branches:** `bounced_back` (wrong details) → redelivery or `funds_refunded`; `charged_back` (pay-in problem, "can happen from any other state"); `cancelled` (never funded). Rollback transitions supported. [CONFIRMED FACT]
18. **Counterparty / liquidity risk** borne by Wise on its pools and safeguarding banks; the customer bears authorised push-payment fraud risk.

The full Wise API happy-path state chain is `incoming_payment_waiting → processing → funds_converted → outgoing_payment_sent`, with the unhappy path `outgoing_payment_sent → bounced_back → processing → cancelled → funds_refunded`, plus `charged_back` and `unknown`. [CONFIRMED FACT — Wise API docs]

---

### II.7 Local Payment-Rail Architecture

| Rail | Access type | Entity / mechanism | Significance |
|---|---|---|---|
| UK Faster Payments | **Direct** participant since 2018 — first non-bank, with a Bank of England RTGS settlement account | Wise Payments Ltd | Instant GBP in/out; foundational |
| CHAPS | Indirect / via BoE where needed | Wise Payments Ltd | High-value GBP |
| SEPA / SEPA Instant | Access in EEA | Wise Europe SA | EUR in/out |
| Hungary (MNB instant) | Direct (2020) | Wise Europe SA | First non-bank in HU |
| Singapore FAST | Direct | Wise Asia-Pacific | SGD instant |
| Australia NPP | Direct | Wise Australia | AUD instant |
| Philippines InstaPay / PesoNet | Direct (2024) | Local arrangement | PHP instant — sixth direct connection |
| Brazil Pix | Direct (approval FY2025, live) | Wise Brasil | BRL instant |
| Japan Zengin | Direct (first non-bank approval FY2025) | Wise Payments Japan | JPY |
| Malaysia PayNet | Direct | Local arrangement | MYR |
| US ACH / Fedwire / RTP / FedNow | **Indirect** via CFSB / partner banks | Wise US Inc + CFSB | USD — no direct Fed access |
| India IMPS / NEFT / UPI | **Indirect** via partner banks | Wise India / Vaho / partners | INR payout |
| Canada | Payments Canada member (for the upcoming Real-Time Rail) | Wise entity | Prospective |

**Direct-connection count is a moving target.** The FY2025 report says the Philippines was "our sixth direct integration to date" and that Brazil Pix and Japan Zengin "will increase our direct connections to eight once live"; some marketing materials still cite "5 direct connections." [CONFIRMED FACT — disagreement reflects timing] **Do not infer direct access from the ability to pay a market** — most markets are reached via partners/local pools. [CONFIRMED — prompt discipline]

Faster Payments mechanics: as a directly connected settling participant, Wise holds a Bank of England settlement account and prefunds cash to cover its maximum possible net debit position — which is why it can settle GBP without a sponsor bank and capture the marginal-cost advantage. Wise was the first non-bank PSP granted a BoE RTGS settlement account (2018), a change enabled by the 2017 opening of RTGS to non-banks. [CONFIRMED FACT — Pay.UK / Bank of England / UK Finance / Forbes]

---

### II.8 Wise's Cross-Border Network

**Traditional correspondent banking (baseline):** a payment hops through multiple nostro/vostro-holding banks over SWIFT; each hop adds fees, an FX markup, delay, and opacity. Wise replaces the multi-hop chain with **two synchronized domestic payments** linked by an internal ledger.

**Wise architecture components:** local collection accounts; local payout accounts; prefunded local currency pools; internal matching/netting; treasury rebalancing; residual correspondent usage for thin corridors; direct payment-system connectivity in up to 8 markets; liquidity buffers; safeguarding accounts; operational reconciliation. Wise cites "50+ local liquidity partners" and "90+ banking partners." [CONFIRMED FACT]

**Answers to the prompt's network questions:**
- **What actually crosses a border?** For an individual transaction on a well-covered corridor, essentially nothing — both legs are domestic. Cross-border movement occurs only in periodic bulk **rebalancing**. [ANALYTICAL INFERENCE, strongly supported]
- **When can Wise satisfy both sides from local pools?** When corridor flows are roughly balanced or the target pool has liquidity (GBP-EUR, USD-CAD are near-symmetric). [THIRD-PARTY ESTIMATE]
- **When must funds move internationally?** When a pool is structurally depleted by one-directional flow (e.g. net-outbound remittance corridors), requiring wholesale FX + international funding to top up.
- **What creates rebalancing needs?** Net directional imbalance in a corridor.
- **How does scale affect matching?** Higher volume raises the probability of internal offset and reduces the share of flow needing external FX/rebalancing — a genuine scale economy that lowers unit cost, which Wise recycles into lower prices. Evidence: the take rate fell from 0.67% to 0.53% in Q4 FY2025 (Wise's CEO letter: "this year, our global take rate reduced from 0.67% to 0.53% in Q4 FY2025 — our lowest to date"), then to ~0.52% by Q1 FY2026 and averaged ~52bps for FY2026. [CONFIRMED FACT]
- **Where does Wise still depend on correspondents?** Thin/illiquid or tightly regulated corridors (parts of Africa, some emerging markets), and USD, where it relies on CFSB and partner banks.

---

### II.9 FX Engine

**Five-way rate decomposition (per prompt):**
1. **Reference/mid-market rate** — the midpoint of interbank buy/sell. Wise states it sources this from "multiple independent rate providers," updated in real time during market hours, to 6 significant digits (rounding the 7th digit ≥5 up). [CONFIRMED FACT — Wise Help Centre] Wise does **not** name a specific vendor (Reuters/Bloomberg). [UNKNOWN]
2. **Customer quoted rate** = the mid-market rate (no markup) — Wise's core promise.
3. **Explicit fee** = fixed + variable %, shown upfront.
4. **Wholesale execution rate** — the rate at which Wise actually converts/holds inventory.
5. **Wise's realized economic spread** = the gap between wholesale execution and the customer mid-market rate, plus net treasury gains/losses on inventory.

**Operational meaning of "mid-market rate":** it is not a marketing abstraction but a real, externally verifiable benchmark Wise commits to give customers, monetising via the visible fee rather than a hidden spread. This is the structural reason Wise is cheaper than banks: its cost is the visible fee, whereas banks bury a 2–5% markup in the rate. [CONFIRMED FACT]

**Rate refresh & lock:** the public converter refreshes roughly every 60 seconds; a transaction quote locks for ~30 minutes; a 5% adverse-move safeguard auto-cancels unfunded transfers ("If the mid-market rate drops by 5% or more before we receive your funds, we will automatically cancel and refund your transfer"). The market closes Friday 5pm New York and reopens Monday 9am Auckland. [CONFIRMED FACT — Wise Help Centre]

**Treasury, exposure & hedging:** the Treasury Ledger feeds trading teams that "manage foreign exchange exposure risks" and "ensure each entity has enough liquidity." [CONFIRMED FACT — Wise engineering job specs] Wise's US Form 20-F confirms exposure to FX and interest-rate market risk and mitigation "through financial hedges or collateralization." [CONFIRMED FACT — Wise Group plc 20-F draft] Internal matching/netting reduces net open exposure; residual exposure is short-duration and hedged. [ANALYTICAL INFERENCE] A discrete FX-trading P&L line is not separately disclosed in preliminary results. [UNKNOWN]

---

### II.10 The Wise Account — Legal & Economic Model

**What it legally is:** an **e-money / payment account**, NOT a bank deposit. In the UK the contract is with **Wise Payments Ltd** (FCA-authorised EMI, FRN 900507), governed by English law. [CONFIRMED FACT]

**Why it looks bank-like but isn't:** it offers local account details (IBAN, sort code, US routing/account number), a debit card, direct debits, and multi-currency balances — but Wise **does not lend out** customer money. Instead it **safeguards**: 100% of customer funds held separately from Wise's own money. Wise's own framing: "We don't lend out your money. Banks do… Because we're not lending your money, we handle it differently by safeguarding it." [CONFIRMED FACT]

**Follow-the-money — safeguarding structure:** roughly ~60% in secure liquid assets (government securities/MMFs) and ~40% cash at banks (Volume-I figure). The UK entity's named safeguarding institutions: Barclays Bank PLC (cash + secure liquid assets), Citibank N.A., JPMorgan Chase Bank N.A., Deutsche Bank AG London, Hamburg Commercial Bank, Bank of America. [CONFIRMED FACT — Wise UK safeguarding disclosure] Assets/Interest money (Wise Assets UK Ltd) is held differently as investment products, with distinct FSCS treatment. [CONFIRMED FACT]

**Deposit insurance:** **No FSCS/FDIC deposit insurance** on Wise balances (they are e-money, not deposits). US customers may receive **FDIC pass-through** insurance where funds sit at FDIC-insured partner banks under specific conditions. [CONFIRMED FACT — Wise blogs] On insolvency, safeguarded funds are ring-fenced from Wise's creditors; an administrator returns them to customers, typically over weeks, with no top-up if a shortfall arises inside the pool. [CONFIRMED FACT]

**Customer holdings scale:** £21.5bn customer holdings FY2025 (incl. £4.5bn Assets under custody); Wise states "As of 30 June 2025, our customers are trusting us with the equivalent of 18.1 billion GBP in their Wise accounts." FY2026: $39bn customer holdings, of which ~$9bn in Wise Assets (Volume I). [CONFIRMED FACT]

---

### II.11 Wise Card — Transaction Teardown

**Issuance & network:** In the US the card is issued by **Community Federal Savings Bank (CFSB), member FDIC, under licence from Mastercard International**; you must hold a Wise Account with a ≥$20 balance to obtain a card; the Cardholder Agreement (v2.2, last updated 21 August 2025) is between the customer and CFSB, with Wise providing servicing "on behalf of CFSB." [CONFIRMED FACT] Elsewhere Wise issues via Mastercard/Visa programs through regional BIN sponsorship. [CONFIRMED FACT]

**Processing:** Wise built the **world's first cloud-based card processing** (AWS/Kubernetes microservices), moving processing in-house to shorten the message chain and cut per-transaction cost. Its services cover card ordering, authorization, and scheme settlement; a "Mastercard connector" normalises scheme messages into a unified Wise interface. [CONFIRMED FACT — Wise Engineering; Kravtsov, Weiming, Menon; Sep 2022]

**Authorization + balance-check + conversion waterfall:**
1. Terminal → acquirer → scheme (Mastercard/Visa) → Wise (as processor/issuer via CFSB in the US).
2. Wise checks the available balance in the transaction currency.
3. **Currency selection logic:** if the customer holds enough of the spending currency, no conversion (free). If not, "smart conversion" converts from the balance carrying the **lowest possible fee**, at the mid-market rate. [CONFIRMED FACT — Wise Help/AU blog]
4. Fraud/limit checks; approve/decline flows back to the terminal in seconds.
5. Customers are advised to always pay in the **local currency** to avoid merchant dynamic currency conversion (DCC). Independent research (German consumer group Stiftung Warentest, reported by The Motley Fool) found DCC raised prices "by amounts ranging from 2.6% to 12.0%," with extreme cases to 18%. [THIRD-PARTY — Stiftung Warentest]

**Economics:**
- **Interchange:** merchant-side; flows to the issuer (CFSB) and is shared with Wise — a "card & other" revenue stream. Wise's investor materials confirm revenue "from our account features, such as debit card interchange fees." [CONFIRMED FACT]
- **FX conversion fee:** from 0.33% when the held currency is insufficient.
- **ATM:** region-specific free allowances then percentage fees (US: $1.50 + 2% over $100 / 2 withdrawals; AU: 2.69% over A$400/month from 1 May 2026; India travel card free to $200).
- **Scheme/processor fees:** paid to Mastercard/Visa; reduced by in-house processing.
- **Chargebacks/fraud:** handled via scheme dispute rules; card fraud loss borne partly by Wise/issuer per scheme allocation. [ANALYTICAL INFERENCE]

**Strategic role:** the card is primarily a **retention + balance-usage + data** tool that also monetises via interchange/FX — it converts a transfer utility into a daily-use account. FY2026 card spend grew 37% to $44bn (Wise Group FY2026 results). [CONFIRMED FACT]

---

### II.12 Wise Business

**Segment & onboarding:** SMEs, incorporated freelancers, e-commerce sellers, marketplaces, agencies paying contractors. Onboarding requires KYB (registration docs, directors, 25%+ shareholders); complex structures can take up to 10 business days. [CONFIRMED FACT] A one-off setup fee unlocks "Advanced"/receiving features (e.g. £50 UK, $31 US); no monthly fee. UK pricing was restructured on 26 November 2025 (free "Essential" plan without receiving; paid "Advanced"). [CONFIRMED FACT]

**Features:** multi-currency hold (40+); local details (up to ~9–10 send currencies / 20+ receiving); batch payments (≤1,000); multi-user permissions; business debit/expense cards (not US business); direct debits (US); invoicing; QuickPay QR; accounting integrations (Xero, QuickBooks, NetSuite); API. [CONFIRMED FACT]

**Economics vs Personal:** Business is **structurally superior** on volume per customer (~£55.6k vs £7.2k) and holds large balances (£6.6bn FY2025). But it grows slower in customer count (+11% vs Personal +22% FY2025) and has faced onboarding/compliance friction in Europe (paused registrations at points). Business underlying income was £321.8m FY2025 (~24% of £1,362.3m group underlying income). Higher frequency + accounting integrations create higher switching costs and retention. [CONFIRMED FACT / ANALYTICAL INFERENCE]

---

### II.13 Wise Platform (substantial depth)

**What it is:** Wise's infrastructure-as-a-service offering — banks, fintechs, and enterprises embed Wise's cross-border payments, multi-currency accounts, and card issuing via API or SWIFT. [CONFIRMED FACT]

**Three integration models (Wise docs):**
1. **Embedded** — regulated FIs/fintechs offer Wise inside their own UI; the partner's customers have Wise accounts linked to the partner platform, which transacts on their behalf.
2. **Enterprise** — a business uses the API to move its **own** funds (payroll, vendors); Wise's relationship is with the enterprise only, not its customers/recipients.
3. **Correspondent** — regulated FIs (Tier-1 banks, challengers, EMIs, brokerages) route their customers' cross-border payments through Wise; the partner holds a Wise account; the originators usually "are often not aware that Wise is being used to process their transactions." Includes **Correspondent Services** (launched at Sibos with SWIFT) — banks redirect MT/MX (SWIFT) messages to Wise, which "translate[s] them into a local payout executed on Wise's network." [CONFIRMED FACT — Wise docs]

**KYC ownership:** depends on model — Wise-performed or partner-performed CDD/KYC, defined per integration; regulated partners typically retain CDD. [CONFIRMED FACT — Wise docs]

**Settlement/prefunding:** for correspondent, a settlement journal (a list of transfer IDs) precedes a single bank payment; on linking, transfers move to `processing`; with prefunding, "settlement funds must reach Wise before the payout is initiated to the recipient." Sender-name mismatches on the incoming bank payment may require manual intervention. [CONFIRMED FACT — Wise docs]

**Named public partners (role/date where public):**
- **Correspondent/enterprise banks:** Morgan Stanley (corporate cross-border settlements, Dec 2024), Standard Chartered (SC Remit via Wise Platform API), Raiffeisen Bank International (Central/Eastern Europe), UniCredit, BPCE (France), Shinhan Bank (Korea), IndusInd Bank (India inward, June 2023 — first India partner).
- **Embedded accounts/cards:** Nubank (Brazil — global account + international debit card for premium clients), Bank Mandiri (Indonesia), Mox (Standard Chartered's HK digital bank), Tiger Brokers (Singapore debit card), Interactive Brokers (US), Google Pay, Monzo, N26.
- **Other/SME distribution:** Qonto (France — doubled international-transfer adoption), Swan (embedded international payments across Europe), Allica Bank (UK), Moin (Korea), Brex, Bolt, EQ Bank and Wealthsimple (Canada), Itaú Unibanco (Brazil).
- Wise reported **85+ Platform partners** by the Nubank announcement. [CONFIRMED FACT — Finextra / Wise / press]

**Commercial model (Wise's own words):** "Wise Platform pricing follows a cost+margin framework. Because Wise Platform leverages the exact same underlying payment network and infrastructure built for our direct consumers, the marginal cost of processing partner volumes is extremely low, leading to highly attractive unit economics." Revenue = transaction fees + "potential integration and software licensing fees depending on the partnership structure." [CONFIRMED FACT — Wise investor-topics page]

**Scale:** Wise's H1 FY2026 interim report (6 Nov 2025) states: "around 5% of Wise's cross-border volume is driven by Wise Platform, up from 4% as reported at our Owners' Day… we continue to expect this to increase materially, to around 10% in the medium term, and over 50% in our long-term vision." (FY2025 ≈ 4%, up from 3%.) [CONFIRMED FACT] Implementation is quoted in "weeks or months." [COMPANY CLAIM]

**Strategic verdict:** Platform **does** transform Wise from a consumer fintech into payments infrastructure / a financial network. Because Wise monetises regardless of whether the end customer chooses Wise or a partner wrapper (Monzo and N26 run cross-border on Wise rails), Platform is a **flywheel amplifier**: partner volume lowers network unit cost, which funds lower consumer prices, which drives volume. It is plausibly **more strategically valuable long-term than direct consumer distribution** — Wise's own "over 50% in our long-term vision" target for Platform volume signals this — even though the Personal segment (~78% of revenue/income) dwarfs it today. [ANALYTICAL INFERENCE, well-supported]

---

### II.14 Product Dependency / Flywheel Map

Verified loops:
1. **Transfer → Account → Balances → Card → Frequency → Retention.** Supported: ~50% personal / ~60% business use multiple features; card spend $44bn FY2026; balances £17.1bn FY2025. [CONFIRMED FACT]
2. **Balances → Interest income → Profit → Price cuts → Volume.** Supported: interest income is material (FY2025 "first 1% yield" £150.4m + "above first 1% yield" £443.9m); take rate cut to 0.53% (Q4 FY2025) and ~0.52% (FY2026). [CONFIRMED FACT]
3. **Business → Integrations/API → Switching costs → Retention.** Supported: accounting integrations, batch, permissions. [CONFIRMED FACT]
4. **Infrastructure → Platform partners → Volume → Lower unit cost → Better consumer pricing.** Supported by Wise's cost+margin statement and the take-rate trend. [CONFIRMED FACT / INFERENCE]
5. **Internal matching improves with scale → fewer external FX/rebalancing legs → lower cost.** [ANALYTICAL INFERENCE]

---

### II.15 Product Economics by Use Case

| Use case | Fee mechanism | Direct payment cost | FX cost | Card/network cost | Support/fraud/compliance | Contribution economics | Capital/liquidity need |
|---|---|---|---|---|---|---|---|
| Major-corridor transfer (EUR-GBP) | Fixed + ~0.33–0.43% | Very low (direct rails) | Near-zero (matched) | — | Low (automated) | High margin | Prefunded pools |
| Thin-corridor transfer | Higher variable % | Partner fees | Wholesale FX + rebalancing | — | Higher | Lower margin | Higher buffers |
| Card spend (currency held) | Free | — | 0 | Scheme fee (offset by interchange) | Fraud loss | Interchange-positive | Balance float |
| Card spend (conversion) | 0.33%+ | — | Small | Scheme fee | Fraud | Positive | Float |
| ATM over allowance | $1.50 + 2% (US) | ATM operator | Small | Scheme | Low | Positive | Float |
| Business batch | Per-leg fee | Local rails | Matched/wholesale | — | Medium | High | Pools |
| Platform | Cost+margin txn fee (+ integration/licence) | Shared infra (near-zero marginal) | Matched | Optional card | Partner-shared | "Highly attractive" | Shared |
| Interest/Assets | 0.27–0.56% mgmt fee | — | — | — | Low | Fee + retention | Custody |

FY2025 group economics: underlying income £1,362.3m; underlying gross profit £1,025.1m (75% margin); underlying PBT £282.1m (21% margin); reported PBT £564.8m; profit £416.7m; cost of sales £328.1m. [CONFIRMED FACT — FY2025 report]

---

### II.16 Failure & Exception Paths

| Failure | Owner | Customer experience | Money location | Ledger state | Regulatory obligation | Loss exposure |
|---|---|---|---|---|---|---|
| Failed funding | Wise/customer | Transfer stalls | Never left sender bank | `cancelled` | — | None |
| Rate expiry (unfunded) | Wise | Re-quote | With sender | Refund/cancel | — | None |
| ≥5% adverse move | Wise | Auto-cancel + refund | Returned | `funds_refunded` | — | Wise avoids FX loss |
| Compliance hold | Wise | Balance frozen pending review | In safeguarding | `processing` | AML/sanctions | Reputational |
| Sanctions match | Wise | Blocked/reported | Held | `processing` | Report to authority | Regulatory |
| Fraud suspicion | Wise | Delay/review | Held | `processing` | SAR | Fraud loss |
| Wrong beneficiary details | Customer/Wise | Delay or return | Payout bank / en route | `bounced_back` → redelivery or refund | — | Possible mis-payment |
| Beneficiary bank rejection | Beneficiary bank | Returned | Returned to Wise | `bounced_back` → `funds_refunded` | — | Low |
| Card dispute/chargeback | Issuer/scheme | Provisional credit process | Merchant/issuer | `charged_back` | Scheme rules | Shared |
| Payout-rail outage | Rail/Wise | Delay | In Wise pool | `processing` | — | Operational |
| Insufficient pool liquidity | Wise treasury | Delay | Pool | `processing` | — | Rebalancing cost |

Rollback transitions let transfers return to prior states; events are reconciled by `occurred_at` timestamp since ordering isn't guaranteed. [CONFIRMED FACT — Wise API]

---

### II.17 Volume II Reconstruction

**1. Product architecture:** one infrastructure (licences + banking partners + rail connections + Treasury Ledger + FX engine + card processing) → three solutions (Account, Business, Platform) → shared primitives (transfer, convert, hold, receive, card, interest, API).

**2. Customer-segment map:** see II.2 — remittance senders, expats, workers/nomads, travelers, freelancers, SMEs, larger businesses/marketplaces, Platform FIs.

**3. Jobs-to-be-done matrix:** see II.3.

**4. Customer lifecycle:** see II.4.

**5. End-to-end transfer maps:** see II.5–II.6 (EUR-GBP, GBP-USD, USD-EUR, Nigeria/NGN, USD-INR, business batch).

**6. Money vs ledger vs accounting:** the customer-facing balance (a liability), the internal Treasury Ledger (double-entry, real-time), the bank-account balances (safeguarding + operating), the payment-system position, the settlement obligation, and the GL recognition **do not move simultaneously** — the ledger and customer view update in seconds while actual bank/rail settlement and rebalancing lag. [CONFIRMED FACT]

**7. Local payment-rail map:** see II.7 — up to 8 direct connections; US/India/Nigeria via partners.

**8. Wise network architecture:** local pools + two synchronized domestic legs + periodic rebalancing; see II.8.

**9. FX architecture:** mid-market from multiple independent providers; five-way rate decomposition; matching + short-duration hedging; see II.9.

**10. Wise Account legal/economic model:** e-money, safeguarded, not deposit-insured; see II.10.

**11. Card transaction map:** CFSB-issued (US), cloud processing, conversion waterfall; see II.11.

**12. Wise Business architecture:** see II.12.

**13. Wise Platform architecture:** three models, 85+ partners, cost+margin; see II.13.

**14. Product dependency/flywheel:** see II.14.

**15. Exception/failure map:** see II.16.

**16. Major dependencies:** (i) CFSB for US issuing/USD access (the OCC denied Wise's national trust-bank charter in July 2026 per Volume I, preserving CFSB dependency); (ii) safeguarding banks (Barclays, Citi, JPMorgan, Deutsche, Hamburg Commercial, Bank of America); (iii) Mastercard/Visa schemes; (iv) local rails + 90+ banking partners + 50+ liquidity partners; (v) partner banks in India/Nigeria/US; (vi) 65–70+ regulatory licences; (vii) SWIFT for correspondent Platform; (viii) cloud (AWS).

**17. Key unknowns:** exact FX-trading P&L; precise wholesale-execution mechanics and rate vendor; per-corridor internal-match rates; per-partner Platform revenue; exact interchange split with CFSB; internal reconciliation algorithm details.

**18. Ten most important conclusions:**
1. A Wise "cross-border" transfer is two domestic payments; money crosses borders only in periodic rebalancing.
2. Scale improves internal matching, lowering unit cost — a genuine, self-reinforcing moat, evidenced by the take-rate decline from 0.67% to 0.53% (Q4 FY2025) and ~0.52% (FY2026).
3. The Wise Account (e-money, safeguarded, not deposit-insured) is the retention engine that turned a transfer utility into an account; balances (£17.1bn FY2025 / holdings £21.5bn; $39bn FY2026) now drive material interest income.
4. Interest income on customer balances is a large, rate-sensitive profit contributor — and a strategic vulnerability if rates fall.
5. The card is a retention/data/interchange tool, not primarily a standalone revenue engine; in-house cloud processing lowers its cost.
6. Wise Business has structurally superior unit economics (VPC ~£55.6k) but slower customer growth and heavier compliance friction.
7. Wise Platform is the strongest infrastructure play and likely the highest strategic-optionality product, monetising even when competitors win the end customer.
8. Direct payment-rail membership (especially UK Faster Payments with a BoE settlement account) is the hard-won, hard-to-replicate core of the speed/cost advantage.
9. Emerging-market corridors (NGN, and to a lesser degree INR) remain the fragile edge — regulation and FX liquidity, not technology, are the binding constraints.
10. Wise is best understood as **payments infrastructure with a consumer distribution front-end** — a network, not a remittance app.

**Prompt questions answered:**
- **What part is actually cross-border?** Essentially none for a given transaction on covered corridors; only periodic bulk rebalancing.
- **Central operating insight?** Convert one cross-border payment into two synchronized domestic payments linked by an internal ledger, and net flows at scale.
- **Strongest retention product?** The Wise Account (balances + card + local details + Assets).
- **Strongest infrastructure product?** Wise Platform (and the rail/licence/ledger stack beneath it).
- **Most strategically important despite not being the largest?** Wise Platform.
- **What is Wise?** A cross-border **payments network / infrastructure platform** with multi-currency accounts and a consumer/business distribution layer on top — not merely a remittance product.

---

### Caveats
- FY2026 figures (19m customers; $243bn volume; $39bn holdings; $44bn card spend) are US-GAAP/USD; FY2025 figures are IFRS/GBP audited. Mixing bases requires care.
- Several mechanism details (wholesale FX rate vendor, internal reconciliation algorithm, per-partner Platform economics, the interchange split with CFSB, discrete FX P&L) are not publicly disclosed and are labelled UNKNOWN or ANALYTICAL INFERENCE.
- Rail-connection counts and Platform partner counts are time-sensitive and cited as of FY2025/2026 sources; the "5 vs 6 vs 8 direct connections" discrepancy reflects go-live timing, not conflicting facts.
- The DCC cost range (2.6–12%, up to 18%) is from a Stiftung Warentest study reported by third parties, not a Wise publication.
- The Belgian AML criminal investigation of Wise Europe SA (disclosed 1 June 2026, per Volume I) is regulatory context, not a product mechanism, and is not analysed here.
- This is Volume II only. Volume III is not begun.


---

# Part III — Operations, Technology, Data & Organisational Infrastructure

*An institutional-grade forensic reconstruction of how Wise actually operates at scale. Volumes I (Corporate/Legal/Regulatory/Institutional) and II (Product/Customer/Money-Movement) are treated as established background and are not re-derived. Volume IV is not begun.*

---

### Preface: scope, method, and evidence conventions

This volume reconstructs *how Wise runs at scale* — the software systems, treasury machinery, data platform, financial-crime controls, reliability practices, and organisational design that let **~19 million (18.9m) customers move $243.5bn across borders in FY2026** (year ended 31 March 2026), processing **about 4.7 million transactions a day** [American Banker, 2 June 2026].

Evidence labels: **[CONFIRMED]** (primary/reliable), **[COMPANY CLAIM]** (Wise-stated, not independently verified), **[THIRD-PARTY]** (external report/estimate), **[INFERENCE]** (reasoned from multiple facts), **[HYPOTHESIS]** (plausible, needs evidence), **[UNKNOWN]**. Current-state claims carry "As of [date]" where material.

A structural sourcing note: Wise is unusually transparent about engineering (the Wise Engineering Medium publication; "Tech Stack" posts of 2016/2020/2022/2025; conference talks; detailed job descriptions) but far more opaque about the internal chart-of-accounts, reconciliation break-handling, and treasury execution mechanics. Where Wise has published nothing, this report labels the gap **[UNKNOWN]** rather than inventing architecture, as the research brief requires.

---

### III.1 Operating Model

Wise is best understood as a **regulated payments-network operator wrapped around a software company**. The revealed design doctrine — visible in capital allocation, hiring and org structure — is to *internalise* functions that create cost, speed or regulatory advantage (payment-scheme connectivity, ledgering, treasury, fraud/AML tooling, card processing) and *buy/outsource* commodity capability (CRM/help-desk, cloud primitives, identity-document capture).

#### Function map

| Function | Mandate | Key systems | Automation | Evidence |
|---|---|---|---|---|
| **Product** | Own customer problems by mission team; roadmap | Autonomous teams; A/B experimentation | High | [CONFIRMED] |
| **Engineering** | Build & run >1,000 backend services, 40+ web apps | Java/Kotlin; React/Next.js (CRAB); Kubernetes | High | [CONFIRMED] |
| **Payments Operations** | Process transfers, resolve exceptions, reconcile | Recon tooling; exception queues; 24/7 global ops | Med (manual for breaks) | [CONFIRMED] |
| **Treasury** | Local liquidity, prefunding, FX execution | Treasury Ledger; trading desks | Med-high | [CONFIRMED] |
| **Finance** | Statutory accounts, GL, regulatory capital | US GAAP/USD from FY2026 | Med | [CONFIRMED] |
| **Compliance/AML/Sanctions/Fraud** | KYC/KYB, monitoring, SAR filing, screening | In-house ML (>110 data points) | High + human review | [COMPANY CLAIM]/[CONFIRMED] |
| **Risk** | Three-Lines-of-Defence; risk committees | Group Risk Cttee, ALCO, sub-committees | — | [CONFIRMED] |
| **Customer Support** | Multi-channel service, 4 hubs | Zendesk; LLM-assisted | Rising | [CONFIRMED] |
| **Legal/Reg. Affairs** | Licensing, scheme membership, enforcement | GC reports to CTO | Low | [CONFIRMED] |
| **Wise Platform (BD)** | Enterprise/bank API distribution | REST + OAuth; 40+ currencies | — | [CONFIRMED] |
| **Data** | DBs, streaming, analytics, ML platform | Kafka, Snowflake, Iceberg, SageMaker | High | [CONFIRMED] |
| **Security** | AppSec, infra, PCI-DSS, IR | Bugcrowd; CISO Shan Lee | Med | [CONFIRMED] |
| **Infrastructure/Platform** | CRP, CI/CD, observability | Kubernetes/RKE2/Rancher, Spinnaker, LGTM | High | [CONFIRMED] |
| **Internal Audit** | 3rd-line assurance | Head of IA to CFO + board | — | [CONFIRMED] |

**Headcount context:** Wise reported a monthly-average of **~6,151 employees in FY2025** (aggregate remuneration £412.8m) [CONFIRMED, FY2025 annual report] and **more than 850 engineers as of early 2025** [CONFIRMED, Tech Stack 2025]. A third-party tracker (Revelio Labs) puts total workforce materially higher (~10,332 in 2025) [THIRD-PARTY] — a gap most plausibly explained by contractor/outsourced-support inclusion [HYPOTHESIS], left unreconciled.

**Revealed priority — financial crime is the largest functional concentration.** Wise states that **"around a third of staff is 'dedicated to fighting financial crime'"** [COMPANY CLAIM, verbatim per The Bureau of Investigative Journalism, 1 June 2026]; American Banker (2 June 2026) corroborates that Wise "assigns roughly a third of its global staff" to financial crime and "processes about 4.7 million transactions a day." This is corroborated in direction by Wise's own FDIC submission ("Compliance is one of our largest teams at Wise") and by the density of open FinCrime roles. It is the single clearest quantitative signal of revealed priorities in the operating model.

---

### III.2 Transaction Operations

#### Normal path

Public transfer state machine (Wise API + engineering material):

`incoming_payment_waiting → processing → funds_converted → outgoing_payment_sent`

with terminal/abnormal states `bounced_back`, `charged_back`, `cancelled`, `funds_refunded`, `unknown` [CONFIRMED]. Lifecycle after a customer confirms:

1. **Quote lock** — mid-market rate locked ~30 minutes; 5% adverse-move auto-cancel [CONFIRMED].
2. **Funding** via local rail (Faster Payments, SEPA, ACH via partner bank, card, or existing balance).
3. **Funding confirmation** — `incoming_payment_waiting` clears on receipt into the local collection/safeguarding account.
4. **Compliance checks** — sanctions/PEP screening + risk scoring.
5. **Fraud checks** — ML scoring on device/behavioural/transaction signals.
6. **Conversion** — `processing → funds_converted`; the FX leg is booked internally against a local pool (not necessarily a per-transaction market trade).
7. **Payout** — instruction from the *destination* pool via a domestic rail; `outgoing_payment_sent`.
8. **Beneficiary credit** — for **75% of Q4 FY2026 payments this completed in under 20 seconds** (CEO Kristo Käärmann: *"instant payments, with 75% of our Q4 payments globally completed in under 20 seconds"*, FY2026 results, 25 June 2026) [CONFIRMED].
9. **Reconciliation & recognition** — ledger reconciled to bank/scheme records; revenue and cost of sales recognised.

The architectural key (from Volume II): the cross-border "movement" is usually **local-in / local-out with internal netting** — money paid in stays in-country; a pre-positioned destination pool pays out; treasury rebalances the residual imbalance (§III.3).

#### Abnormal paths

| Path | Owner | Detection | Customer impact | Ledger status | Regulatory dimension | Loss exposure |
|---|---|---|---|---|---|---|
| Failed transfer | Payment Ops | Rail reject | Delay | Held / may roll back | — | Low |
| Returned / beneficiary rejection | Payment Ops | Rail return → `bounced_back` | Delay | Returned to source pool | — | Low |
| Refund | Payment Ops | `funds_refunded` | Money back | Reversal entries | — | FX slippage |
| Chargeback (card-funded) | Payments/Fraud | Scheme dispute → `charged_back` | Clawback | Liability booked | Scheme rules | Moderate (can land on Wise) |
| Sanctions review | Sanctions/Compliance | Screening hit | Hold/freeze | Frozen | Mandatory reporting | Regulatory > financial |
| SAR review | AML | Monitoring alert | Hold, possible closure + SAR | Frozen | SAR duty (31 CFR 1022.320) | Regulatory |
| Account restriction | Fraud/Compliance | Rules/ML | Access limited | Frozen | Consumer-protection tension | — |
| Stale payment | Payment Ops | Ageing in `processing` | Delay | In-transit | — | Operational |
| Reconciliation break | Payment Ops Recon | Recon tooling | Usually invisible | Mismatch flagged | Safeguarding integrity | Potentially high if systemic |
| Settlement mismatch | Treasury/Payment Ops | Ledger vs statement | Invisible | Position discrepancy | Prudential | Scale-dependent |

**Ownership evidence:** Wise's **Payment Operations Reconciliation** teams in Tallinn and Austin "investigate, resolve … and escalate reconciliation discrepancies," "perform month-end close activities and reporting to Finance," and "support building of reconciliation tooling" across "Spend, Treasury, Assets, Wise Platform" [CONFIRMED, Wise job descriptions]. Reconciliation is a first-class, staffed discipline, not an afterthought — a point that matters directly to the enforcement cluster (§III.10).

---

### III.3 Treasury Operations

Treasury is the economic engine that makes "instant and cheap" possible, and Wise invests real internal engineering in it.

#### The Treasury Ledger

At the centre sits the **Treasury Ledger** — a service Wise describes as "the backbone for **calculating our assets and liabilities with unwavering accuracy and in real time**," seamlessly integrating with the full product spectrum [CONFIRMED, Wise job descriptions]. It is a **real-time, double-entry** system that turns product events into actual and forecasted money movements, and its output feeds **trading teams who manage FX exposure and per-entity liquidity, "executing trades in the order of 10s to 100s of millions of pounds"** on the ledger's data [CONFIRMED, "Software Engineer – Treasury Ledger" / "Senior Software Engineer – FX Markets" postings]. Its engineering mandate is "real-time data streaming flows … relied upon for critical downstream processing — such as risk hedging and liquidity management."

#### Treasury operating cycle (reconstructed)

Local pools pre-positioned by corridor → real-time per-entity position calculation → internal netting of opposing flows → imbalance detection → market execution (FX trades of tens-to-hundreds of millions; physical liquidity moves between pools) → scheme prefunding → yield management (MMFs/government securities within safeguarding rules) → reconciliation against bank/scheme records.

#### Safeguarding vs treasury freedom (follow-the-money)

The binding constraint is that most customer money is **safeguarded**, not free corporate cash. As of 31 March 2026, safeguarded customer deposits sat in **highly liquid money market funds ($7,592.1m)**, **investment-grade fixed-income securities — government treasury bonds and highly-rated corporate paper ($4,582.7m)**, cash at banks, and — for UK funds — **Safeguarding via Comparable Guarantees valued at $1,119.1m (£845.0m) backed by nine investment-grade sureties** [CONFIRMED, FY2026 results / Form 20-F]. The MMFs are managed by institutions including **BlackRock** — Wise's own Assets (Interest) customer agreement names the **BlackRock ICS Sterling/Euro Government Liquidity and US Treasury funds**, with **BlackRock Asset Management Ireland Limited** as manager [CONFIRMED, Wise Assets Customer Agreement, 24 Sept 2025]; State Street is also reported [THIRD-PARTY]. Safeguarding rules mean Wise can invest in permitted liquid, low-risk instruments and earn interest, but cannot lend the money out or take meaningful credit/duration risk. This is precisely why Wise is *not* a bank in economic substance despite bank-like balances — and why its national-trust-bank ambition (denied by the OCC in July 2026, §III.10) mattered strategically.

#### Faster Payments prefunding (a concrete liquidity constraint)

As the first non-bank direct participant in UK Faster Payments (2018) with a Bank of England RTGS settlement account, Wise must post **prefunding** into a dedicated BoE account covering its maximum net settlement obligation. Because non-bank PSPs are ineligible for interest-bearing reserves accounts, that prefunding sits in a **"settlement collateralisation account" (own funds)** or **"completion funds account" (client funds)** [CONFIRMED, Bank of England RTGS documentation]. Economic consequence: direct participation buys speed and cost advantage but ties up liquidity (a step-fixed cost of membership) that — for a non-bank — does *not* earn the reserve rate, a subtle drag banks avoid.

#### Interest-rate economics and yield management

Customer holdings reached **$39.0bn in FY2026 (+40%)**: **$30.0bn on-balance-sheet** ($18.8bn Personal / $11.2bn Business) and **$9bn off-balance-sheet Wise Assets** [CONFIRMED, FY2026 results / 6-K]. Wise generated **$806.1m of net interest income (+6% YoY; FY2025 ≈ $758.3m)**, *"made possible by the $39 billion now held in customer accounts, up 40%"* [CONFIRMED, FY2026 results], and **paid $196.9m of interest to customers** [CONFIRMED, FY2026 6-K].

The retention framework is mechanical and P&L-material: the **first 1% of yield** covers Wise Account operating costs; interest **above 1% is split 20% retained / 80% available to customers** [CONFIRMED, Wise "Translation of IFRS financials into US GAAP," 13 April 2026]. Because of (mainly UK) regulatory restrictions, Wise returned only about half of the intended 80% in FY2026, so the unreturned portion "incidentally" flows to profit — producing a **FY2026 income-before-tax margin of 26% (income before tax $660.4m), "slightly above our guided range of 20-25%"** [CONFIRMED, FY2026 results, 25 June 2026], versus a medium-term 15–20% target once full pass-through is achieved.

**Rate sensitivity (verified):** a 25bp simultaneous move in central bank rates changes net interest income / net revenue / income before tax by **approximately $40m per year** (measured on H1 FY2026 balances) — i.e. the figure is **$40m per 25bp in US dollars**, not pounds as sometimes reported secondhand [CONFIRMED, Wise US-GAAP translation, 13 April 2026]. Average gross yield on balances compressed from **~3.9% (FY2025) to ~3.0% (FY2026)** [THIRD-PARTY, investor presentation]. Interest income is thus a genuine but rate-cyclical earnings pillar: a full 100bp of cuts would remove roughly $160m of income on the H1 FY2026 base, partially cushioned because Wise then owes customers less pass-through.

#### Where liquidity binds

Hardest in **imbalanced corridors** (one-directional remittance flows), in **volatile/capital-controlled currencies**, and at **scheme-prefunding step points**. Scale helps (more netting, deeper matching) but does not eliminate corridor imbalance — the fundamental reason Wise still executes hundreds of millions in FX trades.

---

### III.4 Technology Architecture (as of early 2025 unless noted)

#### Client layer
- **Web:** **CRAB** (Wise abstraction over **Next.js**), **40 distinct apps**; **React** components tested with **Storybook** + **Chromatic** visual-regression snapshots [CONFIRMED].
- **iOS:** 250+ Xcode modules migrated Xcodegen→**Tuist**, CocoaPods→**Swift Package Manager**; zero-change build times cut **28s → 2s** [CONFIRMED].
- **Android:** primary repo of 300+ Gradle modules, ~1m LOC; **Jetpack Compose**, **Kotlin 2.x**, Coroutines/Flows, MVVM; exploring **Kotlin Multiplatform** and BFF sharing [CONFIRMED].
- **Auth:** public API uses **REST + OAuth** [CONFIRMED].

#### Backend
- **Over 1,000 services**, primarily **Java and Kotlin** (history: ~50 services in 2016 → ~250 by 2020 → >1,000 by 2025 — a clear monolith-to-microservices trajectory) [CONFIRMED].
- **In-house microservice chassis framework** (shipped as an artifact) pre-configures security, observability, DB access, Kafka [CONFIRMED].
- Standardised builds via in-house **Gradle plugins** across **700+ Java repos**; a language-agnostic automation service performs mass codebase changes and dependency upgrades [CONFIRMED].
- **Envoy** service mesh for service/DB discovery [CONFIRMED].

#### Data (transactional + analytical)
- **Transactional:** **MariaDB** + **PostgreSQL** migrated to **Amazon RDS** (HA via **Patroni**/Postgres and **Orchestrator**/MariaDB); **MongoDB → MongoDB Atlas**; **Redis**; exploring distributed relational DBs [CONFIRMED].
- **Streaming:** **Apache Kafka** processes "billions of messages a day" — async messaging, log collection, streaming aggregations; moved onto Kubernetes with **rack-aware standby replicas**; **complete history retained in compacted Kafka topics**; own streaming engine + custom DSL over **Kafka Streams** and **Flink** [CONFIRMED].
- **Analytics:** **Snowflake** core store + **S3 data lake on Apache Iceberg**; **Trino** query layer (fault-tolerant gateway) over Iceberg/Snowflake/Kafka; **Airflow + dbt-core**; BI via **Looker/Superset**; in-house data-movement service + "Data Archives" (100bn+ records) [CONFIRMED].

#### Infrastructure
- **AWS is the primary cloud** (workloads migrated off on-prem by ~2020); networking centralised via **AWS Transit Gateways**; UK/Hungary/Australia scheme integrations require physical data centres, with **Australia among the first AWS Outpost Servers deployments** [CONFIRMED].
- **Compute Runtime Platform (CRP)** on Kubernetes: **RKE2** bootstrap, **Rancher** state, **Helm** (replacing JSONNET), GitOps via **ArgoCD**, Terraform provisioning; grew from **6 → 20+ clusters**; autoscaling via **VPA** + **KEDA** [CONFIRMED].

#### Delivery
- CI: **CircleCI → GitHub Actions**, ~**500K monthly builds**, ~15% faster via cache pre-population, **SLSA** rollout [CONFIRMED].
- CD: in-house **Octopus → Spinnaker** with **Automated Canary Analysis** (5% traffic, 30-min metric analysis, auto-rollback) that "automatically prevented hundreds of potentially incident-causing deployments" in 2024 [CONFIRMED/COMPANY CLAIM]; historically 120+ production deploys/day and no dedicated manual QA [CONFIRMED, 2020]; **Temporal** automates DB switchovers/recovery tests [CONFIRMED].

#### Reliability/observability
- Full **LGTM stack** — **Loki** (logs), **Grafana** (dashboards), **Tempo** (traces), **Mimir** (metrics, migrated from Thanos); piloting **Pyroscope**; ~**6m metric samples/sec**, **150m active series** for the largest tenant [CONFIRMED].

#### ML platform
- **SageMaker Studio**, **Spark on EMR**, SageMaker **Feature Store**, **MLflow**, in-house prediction service on **Ray Serve**; LLM gateway to **Anthropic (Claude), AWS Bedrock, Google Gemini, OpenAI** + custom **RAG** [CONFIRMED].

---

### III.5 Build vs Buy

| System | Approach | Rationale | Lock-in/risk |
|---|---|---|---|
| Payment routing / scheme connectivity | **Build** + direct membership | Cost, speed, regulatory control, moat | High (the point) |
| Ledger (product + treasury) | **Build** | Real-time correctness, FX/liquidity feed | Proprietary; deep moat |
| FX / treasury execution | **Build** ledger + market counterparties | Netting efficiency | Execution counterparty risk |
| Reconciliation | **Build** tooling + human ops | Safeguarding integrity | Enforcement risk if weak |
| Card processing | **Build** (cloud-first AWS/Kubernetes, Mastercard connector) | World-first cloud card processing | Scheme dependence |
| Compliance/monitoring/fraud | **Build** (in-house ML) | Speed-vs-safety tuning | Enforcement risk (§III.10) |
| Identity doc capture / KYC | **Buy/blend** (Onfido widely used; Wise runs hosted + API KYC) | Commodity capture; decisioning is Wise's | Vendor dependence [INFERENCE] |
| CRM / support desk | **Buy** (Zendesk) | Commodity | Low |
| Data infra | **Buy managed + build glue** (RDS/Snowflake/Atlas/SageMaker) | Reduce toil | Concentration |
| Cloud | **Buy** (AWS) | Elasticity | High concentration |
| Observability | **Buy OSS/managed + self-run** (LGTM) | Cost/control | Medium |
| CI/CD | **Buy + glue** (GitHub Actions/Spinnaker) | Velocity | Medium |
| Security testing | **Buy** (Bugcrowd) | Continuous real-world testing | Low |

Coherent doctrine: **build where correctness, speed, cost-at-scale or regulatory control matter; buy commodity.** The KYC-vendor attribution is [INFERENCE] — Wise runs both hosted and API KYC flows but has not published its current document-capture vendor list.

---

### III.6 Payment Infrastructure Software

- **Idempotency [CONFIRMED]:** create-transfer uses `customerTransactionId`; balance conversions and card orders use an `X-idempotence-uuid` header — the documented duplicate-prevention mechanism at the API boundary.
- **State machine [CONFIRMED]:** explicit lifecycle with rollback transitions; events reconciled by `occurred_at` because ordering is not guaranteed (consistent with Kafka event-driven design).
- **Routing / rail selection [INFERENCE]:** direct-scheme-vs-partner-bank logic is Wise-controlled; the specific routing engine is undocumented.
- **Retries [CONFIRMED pattern]:** event-driven Kafka with idempotent consumers; interview material stresses storing the key with a request hash so retries return the original result.
- **Settlement/treasury handoff, ledger entries, in-line compliance/fraud scoring (Ray Serve), webhooks [CONFIRMED].**

**Confirmed vs inferred boundary:** the *existence and shape* of the state machine, idempotency mechanism, and event-reconciliation-by-timestamp are confirmed; the *internal orchestration engine* (saga/orchestrator vs Kafka choreography) is [HYPOTHESIS] — a StatefulJ-style FSM is documented at Airbnb, not confirmed at Wise.

---

### III.7 Ledger Architecture

[CONFIRMED]: a **real-time double-entry Treasury Ledger**; **event-driven** with **complete history in compacted Kafka topics** (enabling recomputation of aggregations); reconciliation links internal balances to external bank statements via a dedicated Recon function.

Conceptual separation (partly [INFERENCE]): customer-facing balance · product ledger (Spend/Assets/Business/Platform) · payment state (the transfer FSM) · treasury balances (real-time per entity) · bank-account records (safeguarding banks, BoE) · safeguarding records · reconciliation state · general ledger (US GAAP/USD from FY2026).

Prompt questions answered: double-entry — **yes** for the Treasury Ledger [CONFIRMED]; multi-currency per pool [INFERENCE]; pending-vs-settled modelled via the FSM + `occurred_at` [CONFIRMED]; reversals via rollback transitions and `funds_refunded`/`charged_back` [CONFIRMED]; internal chart-of-accounts and fee-recognition schema **[UNKNOWN]** (unpublished).

---

### III.8 Reconciliation Architecture

A **first-class, staffed operational system** (Tallinn, Austin) covering bank-account, payments/transactions, card, customer-balance, safeguarding, treasury and GL reconciliation, plus compensations reconciliation and audit coordination [CONFIRMED, job descriptions]. Specialists "investigate, resolve … and escalate discrepancies in a timely manner," build recon tooling with engineers, and run month-end close.

**Regulatory weight:** the US multistate consent order cited "transaction monitoring **data integrity** issues," and required Wise to "institute a **more robust program to ensure customer information is accurate, complete, valid, and properly reflected in regulatory reporting**" within 90 days, plus **quarterly independent testing of transaction data to verify … internal controls and data integrity** [CONFIRMED, Mass.gov, 9 July 2025]. A reconciliation failure therefore threatens (a) safeguarding integrity, (b) regulatory-reporting accuracy, and (c) in extremis, licence conditions — the regulatory exposure exceeds the direct financial exposure.

---

### III.9 Data Architecture

Ingestion via CDC + in-house data-movement service; storage across RDS/Mongo/Redis (operational), Kafka (streaming/history), Snowflake + S3-Iceberg (analytical); transformation dbt + Airflow; query Trino; BI Looker/Superset; ML SageMaker/EMR/MLflow/Ray Serve [all CONFIRMED]. Wise built an automated **data-inventory + governance portal** (discovery of what data exists, who created it, its category) feeding deletion, privacy and compliance — a direct response to GDPR and the AML data-integrity findings [CONFIRMED].

**Genuine data flywheels (assessed):**
1. **Fraud/AML ML with volume** — [CONFIRMED direction] Wise's FDIC submission: ML "uses **over 110 data points**, with each data point assigned a risk aspect." Real, but the enforcement cluster shows volume outran control quality — the flywheel is genuine yet not self-sufficient.
2. **Routing/liquidity netting** — [INFERENCE] more corridor flow → better netting/forecasting → lower FX cost.
3. **Pricing** — [INFERENCE] elasticity data supports price setting.
4. **Support automation** — [CONFIRMED] LLM QA agent trained on hundreds of cases; ~50% of chat handled by LLMs (FY2026).

Strongest, most durable flywheels: **fraud/AML** and **matching/liquidity**, because both compound with proprietary volume competitors cannot replicate.

---

### III.10 Fraud and Financial-Crime Technology

**Architecture:** in-house **ML for both fraud and AML**; FDIC submission — "over 110 data points," an "advanced **Model Validation Team**," a named **MLRO**, periodic external audits [COMPANY CLAIM/CONFIRMED submission]. Onboarding blends hosted and API KYC/KYB, with vendor-assisted document capture [INFERENCE]. High scores/rule hits route to human review; the consent-order remediation explicitly commits to "ensure adequate levels of personnel and resources … to manage the amount and complexity of case alerts to ensure timely SAR filings" [CONFIRMED] — an admission that alert volume had outpaced human review capacity.

**The enforcement cluster (what the orders actually said):**
- **US multistate consent order (9 July 2025, $4.2m, six states — California, Massachusetts, Minnesota, Nebraska, New York, Texas):** based on a Jan–Feb 2024 exam covering Jul 2022–Sep 2023; Report of Examination (20 Aug 2024) cited failure to provide independent AML review at adequate frequency; **failure to timely file SARs**; **transaction-monitoring data-integrity issues**; **failure to timely correct past deficiencies**; and **Remittance Transfer Rule** violations. Remediation: updated AML/CFT program; **SAR lookback on closed accounts 1 Mar 2023–1 Mar 2025** (customers deactivated, >$2,000 aggregate, no prior SAR); **independent validation** with quarterly testing; **two years of quarterly progress reports**; independent monitor [CONFIRMED, Mass.gov; signed by Wise US President Harsh Sinha].
- **CFPB order (2025):** originally penalised, later **amended down to $45,000** plus ~**$450,000** set aside as consumer redress [CONFIRMED, Banking Dive].
- **OCC denial of national trust-bank charter (July 2026):** the multistate AML action "played a central role"; the OCC concluded the application should not be reconsidered "until Wise has addressed existing deficiencies and built a more robust enterprise-wide compliance program" [CONFIRMED]. Wise subsequently signalled a pivot toward a **GENIUS Act stablecoin framework** application [THIRD-PARTY].
- **Belgian criminal AML investigation of Wise Europe SA (disclosed 1 June 2026):** the Brussels Public Prosecutor's Office says the amount **"would exceed half a billion euros ($582.5m) in suspicious transactions,"** tied to hundreds of criminal files from "more than 30 countries across Europe," with prosecutors "finalising a direct summons before the criminal court" [CONFIRMED, per EPI/Yahoo Finance and TBIJ, 1 June 2026]. Wise's Belgian office handles EEA law-enforcement requests.

**Interpretation:** the controls are technologically sophisticated (in-house ML, model validation) but the enforcement pattern reveals a **speed-vs-safety tension** — Wise's autonomy-and-velocity culture and instant-payment product created growth that outpaced control maturity, particularly in SAR timeliness and data integrity. **Fraud-loss economics:** card chargebacks can fall on Wise; APP scam losses are shaped by the UK reimbursement regime. Wise's specific disclosed fraud-loss figures are **[UNKNOWN]** in the material gathered here and should be sourced from the 20-F risk section for a definitive number.

---

### III.11 Security Architecture

[CONFIRMED]: **PCI-DSS** is a first-order constraint shaping the card platform and Kubernetes controls; **bug bounty via Bugcrowd** (moved from traditional pen-testing to crowdsourced; a private program surfaced a "P1 Business Critical" vulnerability within 24 hours; CISO **Shan Lee**); **SLSA** supply-chain rollout; automated code/documentation quality gates as part of passing financial audits; **OAuth** on the public API; **Envoy** for controlled service-to-service traffic.

[UNKNOWN]/[HYPOTHESIS]: key management (KMS vs HSM), secrets tooling, privileged-access management, and insider-threat controls are not publicly detailed and are not invented here.

Security failures map to (a) direct financial loss (fraud, card e-skimming — the explicit Bugcrowd rationale), (b) regulatory exposure (PCI, data protection), (c) customer trust (the core asset of a money mover), and (d) continuity. Security is treated as business-critical, not IT hygiene.

---

### III.12 Reliability Engineering

**Why the bar exceeds ordinary SaaS:** a failed SaaS request is an inconvenience; a failed Wise operation can mean **money moved but not recorded, recorded but not moved, or moved twice**, and Faster Payments credits are **irrevocable at initiation**. Correctness and durability are financial and sometimes legally irreversible.

[CONFIRMED] practices: **Automated Canary Analysis** (Spinnaker); **Kafka rack-awareness / standby replicas** (Kafka Streams described as "a critical component of Wise's money movement"); DB HA via **Patroni/Orchestrator** and **Temporal**-automated switchovers reducing **RDS maintenance downtime "from 10 minutes to 100 milliseconds"**; **Pod Topology Spread Constraints** across AWS AZs (to avoid losing 2/3 of pods on an AZ failure); LGTM observability.

Hard-question answers: service fails after money moves but before state updates — event history in compacted Kafka topics + reconciliation-by-`occurred_at` allows state to be recomputed and residual breaks caught by the Recon function [CONFIRMED pattern]; runbooks [UNKNOWN]. Late bank settlement — the FSM holds the transfer in-transit; treasury forecasts absorb timing; recon matches on statement arrival [INFERENCE]. Duplicate prevention — idempotency keys + idempotent consumers [CONFIRMED]. **Known-incident catalogue and published SLOs/availability targets are [UNKNOWN]** from the gathered material and are not asserted.

---

### III.13 Infrastructure Resilience

**Concentration risks and single points of failure:**
- **AWS concentration** — near-total, with mitigations *within* AWS (multi-AZ, Transit Gateway, Outposts) rather than multi-cloud; **no public evidence of a multi-cloud posture** [CONFIRMED gap]. This is the most material single point of failure.
- **Payment-scheme / bank dependencies** — direct scheme membership reduces single-correspondent reliance, but each corridor depends on its scheme's availability and on named safeguarding banks (Barclays, Citibank N.A., JPMorgan Chase N.A., Deutsche Bank AG London, Hamburg Commercial Bank, Bank of America — from prior volumes) and, in the US, partner bank CFSB.
- **Card scheme** — Mastercard dependency for card processing.
- **Vendors** — Zendesk, Bugcrowd, Snowflake, MongoDB Atlas, GitHub Actions.
- **Geographic redundancy** — multi-AZ confirmed; multi-region partially evidenced; full DR/BC design **[UNKNOWN]**.

The most material *institutional* dependencies (schemes and safeguarding/partner banks) are simultaneously the **source of the moat** (§III.19).

---

### III.14 Employee Architecture

| Metric | Value | Evidence |
|---|---|---|
| Monthly-average employees FY2025 | ~6,151 (remuneration £412.8m) | [CONFIRMED] |
| Engineers (early 2025) | >850 | [CONFIRMED] |
| Engineer trajectory | ~120 (2016) → 400+ (2019/20) → 850+ (2025) | [CONFIRMED] |
| Total workforce (trackers) | ~7,713 (2024) → ~10,332 (2025) | [THIRD-PARTY, Revelio] |
| Financial-crime share | "around a third of staff" | [COMPANY CLAIM] |
| Transactions/day | ~4.7 million | [THIRD-PARTY, American Banker] |
| Support hubs | Tallinn, Budapest (EMEA); Tampa (Americas); Singapore (APAC) | [CONFIRMED] |
| Other key offices | London HQ, Austin, Tokyo, São Paulo, Brussels | [CONFIRMED] |

**Composition (assessed):** engineering ~14% of the ~6,151 average; financial crime/compliance ~one-third [COMPANY CLAIM]; a large but automation-leveraged support block; a small, high-impact treasury desk; Wise Platform a "start-up within a scale-up." The two largest people investments — **financial crime** and **customer support** — are precisely the functions hardest to fully automate, which shapes operating leverage (§III.18). The Revelio-vs-Wise headcount gap (~10,332 vs ~6,151) is left explicitly unreconciled [UNKNOWN]; contractor/outsourced-support inclusion is the likely but [HYPOTHESIS] explanation.

---

### III.15 Organizational Design

Wise runs a **mission/team-oriented, highly decentralised** model derived from the Spotify "squads/tribes/guilds/chapters" template [CONFIRMED, multiple Wise/TransferWise engineering posts]:
- **Autonomous product teams** ("~46 teams" c.2018; each owns a customer problem; contains engineers, PM, sometimes analyst, designer, plus Operations/CS contacts).
- **Tribes** = alliances of teams in a domain with embedded leadership; **VPs** above tribes.
- **Guilds/Chapters** = cross-team skill communities (iOS, Android, Analytics).
- **Weak code ownership / historically no central architect** — "every engineer is empowered to change any code in any service," owning team advises/reviews.
- **OKRs**; quarterly planning open to all; devolved tool choice.

**Decision rights vs operational power:** product/engineering rights are genuinely devolved (teams pick problems, tools, even currencies to launch — "no-one tells the team what currencies to launch"). **But** the risk/compliance overlay is a formal counterweight: Three-Lines-of-Defence, Group Risk Committee, ALCO and sub-committees, plus (Volume I) GC and CRO reporting to the CTO and Internal Audit to the CFO and jointly to the board. The critical tension the enforcement cluster exposes is that **autonomy optimised for velocity collides with financial-crime control as an inherently centralising, veto-bearing function.** Wise's remediation (independent validation, more personnel for alerts, governance portal) is effectively a **re-centralisation of control**; simultaneously Wise embeds **FinCrime Product Compliance managers inside product/Platform squads** to reconcile autonomy with veto rights by putting compliance SMEs *in* the teams rather than only above them [CONFIRMED, job descriptions].

---

### III.16 Product Development System

[CONFIRMED]: autonomous roadmaps; heavy **A/B testing**; **OKRs**; **continuous delivery** (120+ deploys/day historically; no dedicated manual QA — quality enforced by automated tests, canary analysis, observability); **Storybook/Chromatic** visual regression; 12-language localisation. The balancing mechanism is **standardisation as the enabler of autonomy** — the microservice chassis, standard Gradle/GitHub-Actions plugins, CRP and canary analysis let teams move fast *within* guardrails that bake in security, observability and compliance defaults. Regulatory-product development is increasingly co-owned by embedded FinCrime managers. Technical debt is managed via the language-agnostic automation service that mass-upgrades dependencies across 700+ repos.

---

### III.17 Customer Support Operating Model

[CONFIRMED]: channels are email + Help Centre (Zendesk Support/Guide), phone and chat, all integrated into Zendesk; four hubs — **Tallinn & Budapest** (Europe), **Tampa** (Americas), **Singapore** (APAC); **English plus 11 other languages** (12-language website). Automation: ticket auto-enrichment and routing, self-service deflection, **~50% of chat contacts handled with LLMs (FY2026)**, and a **Credal LLM QA agent** evaluating interactions across **14 Wise-specific criteria** (built because "the volume of customer inquiries was outpacing the company's ability to hire and train"). Escalation routes restricted accounts to fraud/compliance.

Support functions as **four things at once**: a cost centre (attacked with automation), a **trust mechanism** (core to a money mover), a **regulatory function** (complaint handling; the front line for fraud/scam reports feeding SAR processes), and a **product-quality feedback loop** into autonomous teams (CS contacts embedded in teams).

---

### III.18 Operating Leverage

| Function | Scaling | Mechanism |
|---|---|---|
| Engineering / core platform | **Nearly automatic → sublinear** | Fixed R&D amortised over volume; standardisation lowers marginal cost |
| Payments ops (happy path) | **Nearly automatic** | 75% fully automated in <20s |
| Payments ops (exceptions/recon) | **Sublinear, real** | Tooling helps; breaks need humans |
| Treasury | **Sublinear** | Netting improves with scale; desk grows slowly |
| Customer support | **Sublinear (improving)** | LLM automation (~50% chat) breaks linear link |
| Compliance / AML / fraud | **Linear → disproportionate** | Alert volume, SAR duty, jurisdictions, remediation |
| Finance | **Sublinear** | Automated close |
| Legal / regulatory affairs | **Step-fixed / disproportionate** | Each new licence/jurisdiction is lumpy |
| Wise Platform sales | **Linear-ish** | Relationship-driven, long cycles |

**Margin expansion** comes from the technology and payments-operations layers, amplified by treasury netting and support automation — confirmed by FY2026 unit economics (**net revenue $2,502.8m, +19%; average cross-border take rate 0.52%**, down from 0.58%; 75% of payments instant). **Diseconomy threat:** **financial crime/compliance and regulatory affairs**, where the enforcement cluster is direct evidence that complexity can scale *faster* than volume, and where remediation (more personnel, independent validation, two years of quarterly reporting) is a live example of compliance cost rising disproportionately.

---

### III.19 Technology as Competitive Advantage

Scored against six criteria (Proprietary? Hard to reproduce? Cost? Speed/conversion? Regulatory control? Compounds with volume?). ●●● strong, ●● moderate, ● weak.

| Advantage | Prop. | Hard-repro | Cost | Speed | Reg. | Compounds | Verdict |
|---|---|---|---|---|---|---|---|
| Payment routing + direct scheme membership | ●●● | ●●● | ●●● | ●●● | ●●● | ●● | **Deepest moat** — years + regulatory approval; 8+ direct connections |
| Treasury Ledger + netting | ●●● | ●●● | ●●● | ●● | ●●● | ●●● | Core proprietary asset; compounds with volume |
| Automation (happy-path) | ●● | ●● | ●●● | ●●● | ●● | ●● | Strong cost/speed lever |
| Reconciliation | ●● | ●● | ●● | ● | ●●● | ●● | Necessary; must improve (enforcement) |
| FX systems | ●● | ●● | ●●● | ●● | ●● | ●●● | Netting efficiency compounds |
| Fraud/AML ML | ●● | ●● | ●● | ●● | ●●● | ●●● | Real flywheel; control gaps exposed |
| Compliance infra / licences | ●● | ●●● | ● | ● | ●●● | ●● | Accumulated licences = moat; costly |
| Card processing (cloud-first) | ●●● | ●● | ●●● | ●●● | ●● | ●● | World-first cloud card processing |
| API / Wise Platform | ●● | ●● | ●● | ●● | ●●● | ●●● | Distribution moat; embeds Wise in banks |
| Dev productivity (chassis/CI-CD/canary) | ●● | ● | ●●● | ●●● | ● | ●● | Enables velocity; reproducible |
| Reliability | ●● | ●● | ●● | ●●● | ●● | ●● | Table stakes, done well |
| Data | ●● | ●● | ●● | ●● | ●● | ●●● | Compounds; strongest in fraud + matching |

---

### III.20 Volume III Reconstruction

**1. Operating-Model Diagram (textual):** Customer apps (web/iOS/Android) → API/BFF → 1,000+ Java/Kotlin microservices (Kafka-connected) → {transfer FSM, product ledgers, fraud/AML ML on Ray Serve, card platform} → Treasury Ledger (real-time double-entry) → trading desks (FX/liquidity) + payment-scheme connectors → safeguarding banks / BoE RTGS / local pools. Cross-cutting: Reconciliation; Compliance/Risk (3 lines); Support (Zendesk+LLM); Data platform (Snowflake/Iceberg/SageMaker); Observability (LGTM); Security (PCI/Bugcrowd).

**2. Transaction Workflow:** quote-lock → fund → confirm (`incoming_payment_waiting`) → compliance+fraud screen → convert (`processing`→`funds_converted`) → local payout (`outgoing_payment_sent`) → beneficiary credit → reconcile → recognise revenue. Abnormal branches: `bounced_back`, `charged_back`, `cancelled`, `funds_refunded`, sanctions/SAR holds.

**3. Treasury OS:** product events → Treasury Ledger (real-time A/L) → imbalance detection → {internal netting, FX execution 10s–100s £m/trade, pool rebalancing, scheme prefunding} → yield management (MMFs/gov securities within safeguarding rules) → reconciliation.

**4–15.** Technology architecture (§III.4); payment-state architecture (§III.2/6); 8-layer ledger model (§III.7); multi-domain reconciliation (§III.8); Kafka-CDC→Snowflake/Iceberg→Trino→BI/ML data flow (§III.9); ML-score→rules→human-review→SAR fraud/compliance workflow (§III.10); PCI+Bugcrowd+canary+Kafka-rack-awareness+LGTM security/reliability map (§III.11–12); squads/tribes/guilds + risk-committee org and decision-rights map (§III.15); build-vs-buy matrix (§III.5); employee/function map (§III.14); operating-leverage matrix (§III.18).

**16. Operational Bottleneck Analysis (ranked):** (1) **AML alert handling / SAR timeliness** (human-bound, enforcement-critical); (2) **reconciliation breaks** (human-bound, safeguarding-critical); (3) **new-jurisdiction licensing** (step-fixed, lumpy); (4) **corridor liquidity imbalance** (treasury/FX cost); (5) **AWS concentration** (systemic single point of failure).

**17. Technology-Moat Assessment:** durable moats are **direct payment-scheme connectivity + the Treasury Ledger/netting engine + accumulated regulatory licences**, reinforced by the **Wise Platform API** distribution moat. Pure software (CI/CD, observability) is excellent but reproducible — an *enabler*, not the moat.

**18. Key Unknowns:** internal chart-of-accounts/ledger schema; specific current KYC and sanctions/PEP-screening vendors (ComplyAdvantage/World-Check/Napier vs in-house); DR/BC and multi-region failover design; key-management/secrets/PAM specifics; disclosed fraud-loss figures; published SLOs and major-outage catalogue; reconciliation of Wise-reported (~6,151 avg) vs third-party (~10,332) headcount.

**19. Ten Most Important Conclusions:**
1. **The moat is the payments-plus-treasury machine, not the app.** Direct scheme membership + real-time Treasury Ledger + netting is what makes Wise structurally cheaper and faster; software velocity is an enabler.
2. **Local-in/local-out with internal netting** means most "cross-border" transfers never cross a border.
3. **Interest income is a large but rate-cyclical pillar** ($806.1m FY2026; ~$40m per 25bp), governed by a 1%/20%/80% retention framework currently over-earning (26% IBT margin) due to UK pass-through restrictions.
4. **Financial crime is the single largest function** (~one-third of staff, company claim) — the clearest revealed priority and the clearest diseconomy.
5. **The enforcement cluster is an operating-model failure, not just a legal event:** autonomy-and-velocity outran centralising control (SAR timeliness, data integrity).
6. **Reconciliation is a first-class, staffed system** whose failure is primarily a *regulatory* rather than direct-financial risk.
7. **Wise builds where correctness/speed/cost-at-scale/regulatory-control matter and buys commodity** — a disciplined build-vs-buy doctrine.
8. **Operating leverage is strongest in engineering, happy-path payments, treasury and (now) support automation; weakest in compliance and licensing.**
9. **AWS is the dominant single point of failure**; institutional dependencies (schemes, safeguarding/partner banks, Mastercard) are simultaneously moat and risk.
10. **Standardisation is the enabler of autonomy** — chassis, CI/CD, canary analysis and the governance portal let decentralised teams move fast within compliant guardrails; Wise is now *re-centralising* control over risk.

**20. Final answers to the completion questions:**
- **Most critical operating subsystem:** the **Treasury Ledger + payment-scheme connectivity** complex — without it neither instant speed nor low cost survives.
- **Hardest to replicate:** the **combination of direct scheme memberships + accumulated regulatory licences + the netting/treasury engine** — years, capital and regulator trust, not just code.
- **Scales most efficiently:** core engineering, happy-path payment processing, treasury netting, and increasingly LLM-assisted support.
- **Requires human headcount to keep growing:** financial-crime/AML alert handling, reconciliation exceptions, and per-jurisdiction regulatory/licensing work.
- **Most dependent on third parties:** **AWS** (technology) and **payment schemes + safeguarding/partner banks + Mastercard** (institutions).
- **Is technology the moat, or an enabler?** **Technology is primarily an enabler of a broader operating and regulatory moat.** The genuinely defensible assets are the payments-network position, the treasury/netting engine, and the licence stack; Wise's excellent-but-reproducible software is what lets it operate that moat cheaply, fast and at scale.

---

*Volume III ends here at a logical section boundary, with all analytical questions addressed. Volume IV has not been started, per instruction. Material gaps that are discoverable but unresolved are listed explicitly in §III.20(18) as Key Unknowns rather than papered over.*


---

# Part IV — Financial Statements, Revenue Architecture, Unit Economics & Capital

### Wise plc / Wise Group plc — Institutional Forensic Reverse-Engineering Study

**Reporting-basis warning (critical for the entire volume).** FY2020–FY2025 figures are IFRS / GBP, reported by Wise plc (financial year ending 31 March). FY2026 is US GAAP / USD, following the reorganisation completed 8 May 2026 in which the Jersey-incorporated, UK-tax-resident **Wise Group plc** (Nasdaq: WSE; LSE: WISE) became the ultimate holding company and the former listed parent was renamed **Wise Limited**. The conversion involved three simultaneous changes — (i) IFRS → US GAAP, (ii) GBP → USD presentation, and (iii) discontinuation of the earnings-adjusted "underlying basis" alternative performance measure. **This is a reporting-basis change, not an economic change.** The two series are presented separately with the break flagged; they are not spliced. The bridging source is Wise's "Translation of IFRS financials into US GAAP" RNS dated 13 April 2026.

---

### IV.1 Multi-Year Financial History

#### Table 1A — IFRS / GBP series (£m unless stated), FY2020–FY2025 [CONFIRMED FACT]

| Metric | FY2020 | FY2021 | FY2022 | FY2023 | FY2024 | FY2025 |
|---|---|---|---|---|---|---|
| Cross-border volume (£bn) | 42.0 | 54.4 | 76.4 | 104.5 | 118.5 | 145.2 |
| Active customers (annual, m) | ~6.0 | 6.0 | 7.4 | 10.0 | 12.8 | 15.6 |
| — Personal (m) | — | 5.7 | 7.0 | 9.5 | 12.2 | 14.9 |
| — Business (m) | — | 0.3 | 0.4 | 0.52 | 0.63 | 0.70 |
| Customer balances (£bn) | 2.0 | 3.7 | 6.8 | 10.7 | 13.3 | 17.1 |
| Revenue | 302.6 | 421.0 | 559.9 | 846.1 | 1,052.0 | 1,211.9 |
| Underlying income | n/a | n/a | n/a | 964.2 | 1,172.7 | 1,362.3 |
| Underlying interest income (first 1%) | ~3 | ~2 | ~4 | ~50 | 120.7 | 150.4 |
| Gross profit (reported) | 188.1 | 260.5 | 371.9 | 638.2 | 1,092.4 | 1,307.8 |
| Underlying gross profit | — | — | — | ~638 | 852.8 | 1,025.1 |
| Gross margin (reported) | 62% | 62% | 66% | ~75% | ~75% (u: 73%) | ~75% |
| Administrative expenses | 168.8 | 217.5 | 321.4 | ~490 | 615.9 | 768.6 |
| Adjusted EBITDA | 68.2 | 108.7 | 121.4 | 238.6 | — | — |
| Adjusted EBITDA margin | 23% | 26% | 22% | 24.7% | — | — |
| Reported PBT | 20.4 | 41.1 | 43.9 | 146.5 | 481.4 | 564.8 |
| Underlying PBT | — | — | — | ~104 | 241.8 | 282.1 |
| Tax | (5.4) | (10.2) | (11.0) | (32.9) | (126.8) | (148.1) |
| Profit for the year (restated) | 15.0 | 30.9 | 32.9 | 114.1 | 354.6 | 416.7 |
| Basic EPS (p) | 0.95 | 3.31 | 3.40 | 11.53 | 34.20 | 40.37 |
| Diluted EPS (p) | 0.80 | 3.04 | 3.18 | ~11.2 | 33.73 | 39.73 |
| Operating cash flow (gross)¹ | 1,188.4 | 2,073.9 | 3,138.0 | ~2,300 | 3,248.9 | 4,494.4 |
| Underlying/reported FCF | — | 103.9 | 113.3 | ~180 | 247.0 | 332.7 |
| Monthly avg employees | 1,881 | 2,243 | 2,919 | ~4,000 | 5,499 | 6,151 |
| SBC expense | — | — | 42.2 | ~60 | 72.5 | 58.4 |
| Corporate ("own") cash | — | 286.1 | 357.8 | ~700 | 1,061.1 | 1,430.2 |
| Group eligible capital | — | 170.2 | — | — | 870.4 | 1,297.5 |

¹ Operating cash flow is grossly inflated by customer-fund inflows and is **not** shareholder cash.

**Two definitional traps in the early years.** (a) FY2020 profit was **restated** from the originally reported £21.3m to **£15.0m** (a deferred-tax correction on share-based compensation; revenue £302.6m and PBT £20.4m unchanged). (b) At the July 2021 LSE listing the shares were split ~26:1, so FY2021 basic EPS appears as 1.88p on the old share basis and **3.31p** on the new basis. Both are accounting/cosmetic, not economic.

#### Table 1B — US GAAP / USD series ($m), FY2024–FY2026 [CONFIRMED FACT]

| Metric | FY2024 | FY2025 | FY2026 |
|---|---|---|---|
| Active customers (m) | 12.8 | 15.6 | 18.9 |
| Cross-border volume ($bn) | 145.6 | 185.2 | 243.5 |
| Card spend ($bn) | ~23 | 31.9 | 43.6 |
| Customer holdings ($bn) | ~20 | 27.8 | 39.0 |
| Transaction revenue | 1,323.1 | 1,546.3 | 1,893.6 |
| — Cross-border | ~1,060 | ~1,072 | 1,257 |
| — Card | ~245 | ~280 | 392 |
| — Other | ~120 | ~168 | 245 |
| Interest income on customer balances | 610.0 | 758.3 | 806.1 |
| Interest expense on customer liabilities | (157.0) | (205.7) | (196.9) |
| Net revenue | 1,776.1 | 2,098.9 | 2,502.8 |
| Transaction expense | (331.5) | (378.0) | (513.6) |
| Transaction & credit losses | (15.7) | (11.6) | (13.9) |
| Technology & development | (287.6) | (314.1) | (434.3) |
| Servicing | (216.9) | (287.5) | (396.6) |
| Marketing & sales | (79.6) | (106.1) | (171.8) |
| General & administrative | (194.7) | (273.4) | (381.9) |
| Total operating expenses | (1,126.0) | (1,370.7) | (1,912.1) |
| Operating income | 650.1 | 728.2 | 590.7 |
| Other income/(loss), net | 6.6 | (10.7) | 69.7 |
| Income before tax | 656.7 | 717.5 | 660.4 |
| IBT margin | 37.0% | 34.2% | 26.4% |
| Income tax | (155.2) | (167.2) | (161.7) |
| Net income | 501.5 | 550.3 | 498.7 |
| Basic EPS (cents) | 48.57 | 53.31 | 48.92 |
| Diluted EPS (cents) | 47.81 | 52.63 | 48.43 |
| Weighted avg shares — basic (m) | 1,032.6 | 1,032.3 | 1,019.5 |

**Growth rates.** Revenue CAGR FY2020→FY2025 (IFRS): £302.6m → £1,211.9m = **32% p.a.** Underlying-income CAGR FY2023→FY2025 ≈ 19%. Net-revenue growth (US GAAP) FY2024→FY2026 = **19% p.a.** Cross-border volume grew from £42bn (FY2020) to £181.7bn (FY2026, ≈ $243.5bn), a ≈ 28% CAGR. Active-customer CAGR FY2020→FY2026 ≈ 21%.

**Accounting-definition vs genuine economic change.** The single most important *economic* change across the whole series is the FY2023–FY2024 arrival of positive central-bank interest rates, which turned a ~£4m interest line (FY2022) into $806m of gross interest income (FY2026) — the dominant driver of the reported-PBT explosion (from £43.9m in FY2022 to £564.8m in FY2025). The FY2020 restatement, the 2021 share split and the FY2026 IFRS→US GAAP/GBP→USD conversion are all *definitional* and must not be read as economic inflections.

---

### IV.2 Revenue Taxonomy

Wise has nine economically distinct income lines. Under US GAAP these consolidate into two headline categories — **Transaction revenue** and **Net interest income** (interest income on customer balances less interest expense on customer liabilities).

#### Table 2 — Revenue taxonomy [CONFIRMED FACT / ANALYTICAL INFERENCE on splits]

| # | Stream | Payer | Trigger | Pricing basis | FY2026 ($m) | Quality |
|---|---|---|---|---|---|---|
| 1 | Cross-border transfer fee | Sender | Completed transfer | Variable % + fixed | 1,257 (with #2) | Transactional, volume-driven, price-competitive |
| 2 | FX conversion spread | Converting customer | Currency conversion | Mid-market + margin | (in #1) | Transactional |
| 3 | Card interchange + cross-currency | Cardholder / merchant | Card spend | Interchange + FX margin | ~330 of card | Recurring-ish, high-retention |
| 4 | Card issuance / ATM fees | Cardholder | Card order / ATM over-limit | Fixed | ~60 of card | Ancillary |
| 5 | Account / other / domestic fees | Account holder | Domestic txn, opening | Fixed / % | 245 (other) | Growing, higher-margin |
| 6 | Wise Platform (embedded) | Partner (B2B) | Partner-routed txn | Cost + margin (+ integration/licence fees) | (in #1) ~5% vol | Contractual, sticky, scaling |
| 7 | Interest income on customer balances | Wise earns | Holding safeguarded funds | Central-bank rate | 806.1 gross | Balance-driven, rate-sensitive |
| 8 | Wise Assets (custody fee) | Investing customer | AUC holding | % of AUC | (in other) | Recurring, balance-driven |
| 9 | Net interest on corporate investments | Wise earns | Own cash | Rate | ~40 (in other income) | Rate-driven |

**Revenue-quality picture.** Recurring / balance-driven lines (3, 5, 7, 8) now approach half of net revenue: at the FY2026 results (12 months to 31 March 2026) Wise confirmed net revenue rose 19% to $2.50bn "with nearly half coming from non-cross-border revenue." Within transaction revenue, card + other reached 33.6% in FY2026 (card 20.7%, other 12.9%), up from ~24% in FY2024. Cross-border (streams 1–2) remains the largest but slowest-growing and most price-competitive line: FY2024→FY2026 CAGRs are cross-border ~12%, card ~37%, other ~45%.

---

### IV.3 Revenue Flow by Product

#### 3A — Consumer transfer (€1,000, representative) [ANALYTICAL INFERENCE, calibrated to the 52bps FY2026 take rate]
```
Customer sends                         €1,000.00
  Wise fee (~0.52%)                        €5.20   ← gross transaction revenue
  Amount converted at mid-market        €994.80
Third-party / variable direct costs:
  Payout/rail cost (local-out)          ~€1.20   ← declining as direct rails expand
  FX execution / liquidity cost         ~€0.60
  Fraud / compliance variable           ~€0.40
  = Cost of sales (~40% of fee)         ~€2.20
Contribution profit                     ~€3.00   (~58% contribution margin)
Recognition: €5.20 revenue at completion; cash realised same day
```
Wise's reported ~75% underlying gross margin (FY2025) exceeds this per-transfer contribution because the gross-margin denominator (underlying income) includes the first-1% interest income, which carries near-zero direct cost.

#### 3B — Wise Card purchase ($100 abroad)
Wise earns (i) the cross-currency conversion margin (~0.4–0.5%) and (ii) scheme interchange via the issuing entity; direct cost = scheme fees + processor. Card revenue reached **$392m in FY2026 (+40%)**, the fastest-growing transaction line, driven by adoption in the EU, Australia and the UK.

#### 3C — Wise Business payment
Higher average value (business VPC ≈ £62k/yr vs personal ≈ £7.3k/yr), lower take rate (Q4 FY2026 business cross-border **0.39%** vs personal **0.56%**) reflecting volume-tiering, but disproportionate balances ($11.2bn) generating interest income and stickier deposits (payroll, supplier payments, FX hedging).

#### 3D — Wise Platform transaction
A partner (e.g. Morgan Stanley, Standard Chartered, UniCredit, Raiffeisen Bank, MBSB Bank, Capitec) routes an end-customer payment through Wise's rails and licences via API. Commercial model = "cost + margin" transaction fee, plus potential integration and software-licensing fees. ~5% of cross-border volume in FY2026 (up from 4% in FY2025); medium-term target ~10%, long-term vision >50%.

#### 3E — Customer balance / interest income
A customer holding €10,000 has that money safeguarded in cash / MMFs / government bonds earning the central-bank-linked yield (~3.0% average gross FY2026). Wise retains the first 1% (€100/yr) to fund account operating costs; of yield above 1%, the framework aims to retain 20% and return 80%. In practice only about half the 80% is returned (mainly UK regulatory restrictions), so the shortfall accrues incidentally to Wise (see IV.12).

---

### IV.4 Take Rate

#### Table 4 — Cross-border take-rate history [CONFIRMED FACT]

| Period | Cross-border take rate |
|---|---|
| FY2020 | ~0.73% (total); cross-currency n/a |
| FY2021 | 0.70% |
| FY2022 | 0.63% |
| FY2023 | ~0.69% |
| FY2024 | 0.67% |
| FY2025 (avg) | 0.58% |
| Q4 FY2025 | 0.53% |
| FY2026 (avg) | 0.52% |
| Q4 FY2026 | 0.51% |

Quarterly FY2025→FY2026 (US GAAP): 0.64 → 0.59 → 0.56 → 0.53 → 0.52 → 0.52 → 0.52 → 0.51. Personal Q4 FY2026 0.56%; Business Q4 FY2026 0.39%.

**Drivers of compression.** (1) **Deliberate price cuts** funded by unit-cost reductions — the primary driver, and the core of Wise's "Sustainable Efficiency-driven Sales" (SES) flywheel: lower price → more volume/balances → more scale → lower unit cost → lower price. The CFO stated on the FY2026 call that price is "the number one argument for customers to come to us" and the company puts "no floor, any limits" on it. (2) **Mix:** the rise of card-only customers (~3% of active personal in Q1 FY2021 to ~20% in Q4 FY2025) and business volume-tiering mechanically lower the blended cross-border take rate. (3) **Corridor mix** as direct rails cut cost. FY2027 guidance: 1–2bps of quarterly take-rate reduction.

**How low can take rate go?** Cross-border cost of sales is ~40% of the cross-border fee, and direct rails plus internal netting keep cutting the numerator. The strategic point is that Wise no longer needs cross-border take rate to carry group profitability — card, other and interest income now fund ~half of net revenue — so cross-border take rate can plausibly fall toward **~40bps** over the medium term without impairing group margins, provided volume growth (25–31%) continues to reward the cuts. If volume elasticity fails and take rate drops below ~50bps without a volume step-up, that would signal competition overwhelming (rather than enabling) the scale economies.

---

### IV.5 Cost Architecture

#### Table 5 — Cost decomposition, US GAAP ($m) [CONFIRMED FACT + classification INFERENCE]

| Cost bucket | FY2024 | FY2025 | FY2026 | Behaviour |
|---|---|---|---|---|
| Transaction expense | 331.5 | 378.0 | 513.6 | Variable (banking fees, FX, card, product losses) |
| Transaction & credit losses | 15.7 | 11.6 | 13.9 | Volume/risk-sensitive |
| Technology & development | 287.6 | 314.1 | 434.3 | Step-fixed (engineers, cloud, AI) |
| Servicing | 216.9 | 287.5 | 396.6 | Semi-variable (support, payment ops, compliance) |
| Marketing & sales | 79.6 | 106.1 | 171.8 | Discretionary |
| General & administrative | 194.7 | 273.4 | 381.9 | Semi-fixed (finance, legal, offices, D&A, SBC) |

**FY2026 one-off distortions.** Transaction expense rose to 21% of net revenue (from 19%) mainly because of a **~$70m one-off US GAAP FX adjustment on government bonds** (offset in other comprehensive income). Excluding it, transaction cost grew ~17% — below both volume (+31%) and transaction revenue (+22%), evidencing genuine unit-cost decline. Two further one-offs compressed FY2026 margin: **~$45m of Nasdaq-listing core-function costs** and the $70m FX item; excluding these, the operating margin is ~28% vs 26.4% reported.

**Cost classification.**
- **Variable (scale with volume):** banking/rail fees, FX execution, card-scheme fees, product/fraud losses.
- **Semi-variable (scale with customers, sub-linearly):** servicing/support, KYC/onboarding, compliance/manual review.
- **Step-fixed:** engineering (>850 engineers), cloud, data infrastructure.
- **Fixed:** finance, legal, HR, offices, audit, insurance, depreciation.
- **Balance-sensitive:** interest expense to customers; safeguarding/custody operations.

**IFRS admin-expense detail FY2025 (£m):** employee benefits 412.7; consultancy/outsourced 128.1; other admin 78.2; technology 65.9; marketing 53.8; D&A 18.4; PPE impairment 11.5. Employee-benefit split: salaries 290.5; SBC 58.4; social security 41.1; pension 10.2. Monthly average employees 6,151 (Servicing 3,915; Product Development 1,411; Other functions 534; Marketing 291). Under US GAAP, product-engineering costs expensed rose to $226.8m (FY2026) from $164.6m (FY2025); advertising within marketing was $100.5m (FY2026).

---

### IV.6 Cost per Transaction

At ~4.7m transactions/day (~1.7bn/yr) and FY2026 transaction expense of $513.6m, blended direct transaction cost ≈ **$0.30 per transaction** on that gross basis — though this conflates transfers and card taps. On a cross-border-volume basis, cost of sales ≈ 40% of the ~52bps fee ≈ **21bps of volume**. Scale economies arise from five identifiable sources: (1) **direct rail access** — 8+ direct payment-system connections, including Pix (Brazil) and Zengin (Japan) added in FY2026, each cutting correspondent/SWIFT cost on that corridor; (2) **internal matching/netting** via local-in/local-out, so most currency legs never cross a border and Wise pays only domestic rail fees, not correspondent-banking spreads; (3) **automation** of servicing and fraud models; (4) **vendor pricing** improving with volume; (5) **fixed-cost absorption** across a larger base. The principal **diseconomy** is financial-crime/compliance headcount (≈ a third of staff — company claim), which scales closer to linearly with customers and jurisdictions.

---

### IV.7 Unit Economics

#### Table 7 — Unit economics [CONFIRMED inputs; ratios ANALYTICAL INFERENCE]

| Metric | FY2025 | FY2026 |
|---|---|---|
| Active customers (m) | 15.6 | 18.9 |
| Revenue / underlying income per active customer | £87.5 (underlying £1,362m ÷ 15.6m) | ~$132 net revenue/customer |
| Cross-border volume per active customer | £9,309 | ~$12,900 |
| Personal VPC (quarterly) | £3,200 | ~£3,400 |
| Business VPC | ~£55k/yr | ~£62k/yr |
| New customers (first cross-border txn) | 5.9m | 7.0m |
| Marketing spend | £53.8m | $171.8m |
| Blended "CAC" (marketing ÷ new) | ~£9 | ~$25 |

**CAC honesty.** The naïve £53.8m ÷ 5.9m ≈ **£9** blended figure is *not* a true CAC because it spreads paid spend across all new customers, most of whom arrive organically. Word-of-mouth is reported at **~70% of customer growth** (company claim; ~66% in FY2023). The correct framing: paid CAC applies only to the paid-acquired minority (~30%); attributing all marketing to that minority gives paid CAC ≈ £53.8m ÷ (0.30 × 5.9m) ≈ **£30**. Even at £30, against revenue/customer of ~£87 and multi-year retention, payback is well under one year.

**LTV (illustrative, labelled) [HYPOTHESIS — Wise discloses no LTV/retention curves].** Using revenue/active customer ~£87, ~55% blended contribution (transaction + interest), and a 5-year average life with modest revenue retention: LTV ≈ £87 × 0.55 × ~4 (discounted life) ≈ **~£190**. Against paid CAC ~£30, LTV/CAC ≈ **6x**; against blended CAC ~£9, >20x. Sensitivity: at a 3-year life LTV/CAC (paid) ≈ 4x; at 7-year ≈ 8x.

---

### IV.8 Customer Cohort Economics

- **Multi-product adoption:** ~50% of personal and ~60% of business customers use more than one product (FY2025).
- **Card-only cohort:** ~20% of active personal customers (Q4 FY2025), up from ~3% in Q1 FY2021 — low cross-border VPC (£500–£1,000/q) but high card engagement and retention.
- **Balances compound:** customer holdings grew ~5.7x over four years, from £2bn (FY2020) to $39bn (FY2026), evidencing the shift from transactional remittance to a recurring financial account.
- **Business stickiness:** business balances ($11.2bn) fund payroll/supplier/hedging and are stickier than personal.

**Economic character.** Wise is a **hybrid**: (a) transactional remittance at the cross-border core; (b) a recurring financial account (balances + card + interest); (c) an infrastructure usage model (Wise Platform). The trajectory is decisively toward (b) and (c) — balance-driven and recurring lines now fund ~half of net revenue and carry higher retention and margin.

---

### IV.9 Income Statement Teardown (US GAAP, FY2026)

- **Transaction revenue $1,893.6m:** customer-/transaction-driven; recurring at the account level; ~58% contribution; highly scalable.
- **Interest income $806.1m:** balance- and rate-driven; near-zero direct cost; only +6% in FY2026 despite +36% balances, because average gross yield fell 3.9% → 3.0%.
- **Interest expense to customers $196.9m:** balance-/framework-driven; will rise as Wise resolves regulatory barriers to paying the target 80%.
- **Transaction expense $513.6m:** variable; distorted by the $70m one-off FX item.
- **Technology $434.3m, Servicing $396.6m, Marketing $171.8m, G&A $381.9m:** step-fixed / semi-variable / discretionary. Ex-one-offs, operating expenses grew ~17% versus net revenue +19%, so underlying operating leverage is positive but deliberately reinvested.
- **Operating leverage evidence:** IBT margin fell 37% → 34.2% → 26.4% (FY2024→FY2026), but this is **deliberate reinvestment plus rate compression**, not deteriorating economics.

**Statutory vs adjusted.** Under IFRS, "underlying" PBT (revenue + first-1% interest, excluding interest above 1% and benefits paid) versus "reported" PBT differed sharply: FY2025 underlying PBT £282.1m vs reported PBT £564.8m — the £282.7m gap being retained interest above the first 1% not returned to customers. US GAAP abolishes the "underlying" APM; the same economics reappear as the gap between the 15–20% target IBT margin and the 20–25% "over-earning" margin.

---

### IV.10 Balance Sheet Teardown (US GAAP, 31 March 2026, $m) [CONFIRMED FACT]

| Item | FY2026 | FY2025 | Nature |
|---|---|---|---|
| Cash & cash equivalents | 27,802.2 | 18,066.3 | Incl. $14,824.1m safeguarded customer funds |
| Available-for-sale debt securities | 4,582.7 | 6,013.6 | Customer-fund investments |
| Accounts receivable | 391.3 | 347.8 | Settlement in transit |
| Total current assets | 32,980.6 | 24,550.7 | |
| Property, plant & equipment | 189.9 | 150.8 | Offices, equipment |
| Total assets | 33,259.8 | 24,781.1 | |
| Funds payable & due to customers | 30,254.2 | 22,279.9 | Customer liability (Wise Accounts) |
| Short-term debt | 6.0 | 128.4 | RCF |
| Long-term debt | 328.7 | 0.0 | New debt issuance FY2026 |
| Total liabilities | 31,334.6 | 23,043.7 | |
| Treasury stock | (422.8) | (85.0) | Employee Share Trust purchases |
| Retained earnings | 2,111.1 | 1,655.9 | |
| Total shareholders' equity | 1,925.2 | 1,737.4 | |

**Why the balance sheet looks large.** Of $33.3bn total assets, $30.3bn is customer money (funds payable). Shareholder equity is only **$1.9bn**. The balance sheet is inflated by customer funds recognised as both an asset (safeguarded cash/investments) and an offsetting liability (funds due to customers), because Wise concludes it controls the economic benefit of the cash flows and has no enforceable right of set-off. This does **not** represent shareholder capital at risk in a lending sense — Wise does not lend customer money.

---

### IV.11 Customer Funds

#### Table 11 — Safeguarding composition [CONFIRMED FACT]

| Asset class | FY2026 ($m) | FY2025 ($m) |
|---|---|---|
| Cash in segregated safeguarding accounts / term deposits | 14,824.1 | 7,503.0 |
| Money market funds (MMFs) | 7,592.1 | 7,034.4 |
| Investment-grade fixed income (govt/treasury) | 4,582.7 (AFS) | 6,013.6 |
| UK safeguarding via Comparable Guarantee | 1,119.1 (£845.0m) | ~690 (£520.0m) |

**Follow-the-money.** Customer money is legally the customer's; Wise holds it in segregated safeguarding accounts by entity — Wise Payments Ltd (UK: Barclays, Citibank, JPMorgan, Deutsche Bank, Hamburg Commercial Bank, Bank of America), Wise Europe SA (JPMorgan + BlackRock/State Street MMFs, regulated by the National Bank of Belgium), and Wise US Inc (Goldman Sachs Bank USA, JPMorgan). It is **not** covered by FSCS or FDIC deposit insurance (except US interest-opt-in pass-through up to $250k). Wise may **not** lend it and may invest only in permitted liquid assets (US: max 2-year single-bond maturity, ≤1-year portfolio duration). On insolvency, safeguarded funds are ring-fenced for customers.

**The Comparable Guarantee is a liquidity-financing instrument.** Under FCA safeguarding rules Wise may protect UK customer money by holding secure liquid assets **or** by a "comparable guarantee given by authorised insurers." Entered in FY2025 at £520m and expanded to **£845.0m / $1,119.1m** by 31 March 2026, this arrangement lets an authorised insurer guarantee an amount of customer funds, freeing Wise to deploy that customer money into its own customer network for operational liquidity/prefunding rather than parking it in safeguarding accounts. Economically it converts trapped safeguarding cash into working liquidity, substituting an insurance premium for tied-up corporate cash — a genuine financial innovation with direct relevance to capital (IV.14). (Exact surety count and term are disclosed by Wise but were not independently re-confirmed in this review.)

#### Money-flow map (four distinct pools)
```
CUSTOMER MONEY (~$30.3bn)      → segregated safeguarding; customer-owned; Wise earns interest, cannot lend
   ├─ cash in banks   $14.8bn
   ├─ MMFs            $7.6bn
   ├─ IG fixed income $4.6bn
   └─ freed via Comparable Guarantee $1.1bn → operational liquidity
WISE CORPORATE MONEY (~$1.9bn) → shareholder cash; RCF + debt; funds investment/buybacks
REGULATORY CAPITAL (£1.41bn)   → CET1 own funds; must exceed £293.4m requirement
SETTLEMENT LIQUIDITY           → prefunding across direct-rail markets + BoE Faster Payments collateral
```

---

### IV.12 Interest Income

#### Table 12 — Interest income mechanics [CONFIRMED FACT]

| Item | FY2025 (IFRS £m) | FY2026 (US GAAP $m) |
|---|---|---|
| Gross interest income on customer balances | 594.3 | 806.1 |
| — cash at banks | 220.6 | — |
| — money market funds | 202.4 | — |
| — listed bonds | 171.3 | — |
| Interest expense / benefits paid to customers | 161.2 | 196.9 |
| Average gross yield on balances | ~3.9% | ~3.0% |
| Rate sensitivity (per 25bp move) | — | ~$40m/yr |

**The interest framework (mechanism).** Wise retains the **first 1%** of yield on customer balances to fund Wise-Account operating costs. On yield **above 1%**, the framework splits **20% retained / 80% available to customers**. In practice Wise cannot pay the full 80%: in H1 FY2026, of interest above the first 1% yield, 20% intentionally flowed to income before tax, 36% was paid to customers, and **44% (allocated but unpayable, mainly UK regulatory restrictions and US opt-in requirements) incidentally flowed to income before tax.** In FY2025 (IFRS), of £443.9m above the first 1%, the target was retain 20% (£88.9m) / return 80% (£355.0m); Wise actually paid £161.2m (45% of the target) and retained £282.7m — the UK made up two-thirds of the 55% shortfall. FY2025 benefits paid split: EU cashback £121.3m; US interest £38.5m; other £1.4m.

**This is the single largest driver of "over-earning."** The gap between the 15–20% structural IBT-margin target and the 20–25% reported range is almost entirely the unpaid-80% shortfall. It is a **temporary, regulatory-contingent windfall**: as Wise resolves UK regulatory barriers to paying interest, interest expense to customers rises and reported margin converges toward the 15–20% structural target.

#### Rate scenarios
- **High rates (~5% gross yield):** interest income on ~$30bn balances ≈ $1.5bn gross — large windfall.
- **Normalised (~3% — current FY2026):** $806m gross; ~$609m net.
- **Near-zero (~0.5% gross):** on $30bn, gross ≈ $150m; first-1% coverage evaporates; net interest income near zero (see IV.21).

Rate sensitivity: **~$40m of net interest income / net revenue / income before tax per 25bp simultaneous central-bank move** (measured on H1 FY2026 balances). A 200bp cut would remove ~$320m of IBT — roughly half of FY2026 IBT.

---

### IV.13 Cash Flow & Shareholder Free-Cash-Flow Bridge

**Reported operating cash flow is meaningless as shareholder cash.** US GAAP FY2026 net cash from operating activities of $7,553.9m includes **+$6,999.7m of customer-fund inflows** ("funds payable and amounts due to customers"). Strip that and operating cash before customer-fund movement ≈ $554m. Investing activities include ±$9–11bn of AFS purchases/sales (customer-fund reinvestment), netting to +$1,738.5m in FY2026 — again a customer-fund artefact, not corporate investment.

#### Table 13 — Shareholder FCF anchors (IFRS FY2025, £m) [CONFIRMED]

| Line | £m |
|---|---|
| Underlying free cash flow (Wise's definition) | 332.7 |
| UFCF conversion of underlying PBT | 117.9% |
| FY2024 underlying FCF | 247.0 (102.1%) |
| Memo: reported gross operating cash flow (exclude — customer-fund inflated) | 4,494.4 |
| PP&E capex | (34.5) |
| Intangibles capex | (0.9) |

**Wise's definition of underlying free cash flow** is the cash generated by the operating business, stripping out customer-balance/settlement movements and FVOCI investment flows, less corporate capex. It is the cleanest shareholder-cash proxy Wise publishes: FY2025 £332.7m, FY2024 £247.0m (+34.7%), converting at 117.9% and 102.1% of underlying PBT (>100% because SBC is non-cash and capex is minimal). Under US GAAP FY2026, after $473.4m of share repurchases (EST) and ~$21m of capex, the business self-funds all growth investment and share buybacks from internally generated cash.

**Answer — how much cash is genuinely available to shareholders?** Roughly **£330m (FY2025)** / broadly $400–500m (FY2026 underlying) — the underlying-PBT-linked free cash flow, **not** the multi-billion reported operating cash flow. Customer funds and settlement balances are not distributable.

---

### IV.14 Capital Requirements

#### Table 14 — Regulatory capital (MIFIDPRU consolidated, £k) [CONFIRMED FACT]

| Item | FY2025 | FY2026 |
|---|---|---|
| Permanent minimum requirement | 6,400 | 5,081 |
| K-factor requirement | 39,985 | 25,510 |
| Fixed overheads requirement (binding) | 219,764 | 293,376 |
| Own funds requirement (highest of the three) | 219,764 | 293,376 |
| Eligible capital available (CET1) | 1,297,511 | 1,409,993 |
| Excess over requirement | 1,077,747 | 1,116,617 |
| Surplus buffer | 590% | 481% |

**The binding constraint is the Fixed Overheads Requirement** (a quarter of annual fixed overheads), not the K-factor or permanent minimum — the signature of a genuinely capital-light payments model with no material credit or market-risk capital. Wise holds ~4.8–5.9x its regulatory minimum, entirely in CET1.

**Is Wise capital-light? — quantitative answer.** Distinguish two capital types:
1. **Shareholder capital intensity: YES, very light.** The regulatory own-funds requirement of £293.4m (FY2026) sits against $498.7m of annual net income and $1.9bn of equity — the business generates more profit each year than its entire capital requirement. Incremental volume adds negligible regulatory capital (FOR-driven, not volume-driven).
2. **Operational liquidity intensity: MODERATE and rising.** Prefunding across 8+ direct-rail markets, Bank of England Faster Payments settlement collateralisation, and local-pool prefunding tie up operational liquidity that scales with volume and geography. The £845m Comparable Guarantee exists precisely to relieve this — freeing customer funds for operational liquidity so Wise need not tie up as much corporate cash. Geographic expansion (each new direct connection/licence requires local prefunding) is the main driver of incremental liquidity needs.

Net: Wise is capital-light on **shareholder equity** but carries a growing **operational-liquidity** footprint managed via safeguarding-linked financing and a £330m RCF.

---

### IV.15 Capital Allocation

**Revealed priorities (inferred from behaviour, not statements):**
- **Reinvestment first:** committed to ~£2bn over two years across infrastructure, marketing and products; intention to double annual spend on running/growing Wise, including tripling marketing. FY2026 marketing +60% to $172m; technology +38% to $434m.
- **Employee equity:** Employee Share Trust purchases escalated £10m (FY2023) → £68m (FY2024) → £73m (FY2025) → **$470m / 35.9m shares (FY2026)** to eliminate dilution from historic options. Owners Day (3 April 2025) expanded the programme to cover ~25m historic-SBC shares (~2.5% of issued capital).
- **First material buyback:** a buyback of **up to £405m (~$540m)**, announced 26 June 2026 and executed by Goldman Sachs International from 21 July 2026 to 31 March 2027; 40% of shares repurchased are for employee share awards and the remainder held in treasury.
- **No dividend.**
- **Debt:** £330m unsecured multi-currency RCF (December 2024; six lenders — HSBC Innovation Banking, JP Morgan Chase London, NatWest, Citibank London, Barclays, Goldman Sachs Lending Partners; maturity December 2027 + two one-year extension options; SONIA + margin; covenants of max net leverage 3:1 and interest cover ≥ 3.5:1); $328.7m long-term debt issued in FY2026. Investment-grade **BBB (stable) from both S&P and Fitch** (published 3 April 2025).

**Assessment.** Return on incremental capital is high (the business needs almost no incremental equity to grow), the reinvestment runway is long (<5% of consumer and <1% of business cross-border volume penetrated), and shareholder alignment is strong (large EST purchases eliminate dilution; first treasury buyback in FY2027). The discipline risk is that the deliberate margin sacrifice depends on volume elasticity continuing to reward price cuts.

---

### IV.16 Revenue & Cost Waterfalls

#### €1 of Wise net revenue (US GAAP FY2026) [ANALYTICAL INFERENCE from the income statement]
```
€1.00 net revenue
 − €0.205 transaction expense (incl. one-off FX; ~0.18 ex-one-off)
 − €0.006 transaction & credit losses
 − €0.174 technology & development
 − €0.159 servicing
 − €0.069 marketing & sales
 − €0.153 general & administrative
 = €0.236 operating income
 + €0.028 other income (net; incl. one-off gains)
 = €0.264 income before tax
 − €0.065 tax
 = €0.199 net income (retained)
```

#### €1 of customer volume (cross-border) [ANALYTICAL INFERENCE, 52bps take rate]
```
€1.00 sent by customer
 → €0.9948 passes through to the beneficiary (mid-market conversion)
 → €0.0052 gross fee captured by Wise
      − €0.0021 third-party direct cost
      = €0.0031 contribution
 Temporarily: the €1 may rest as a Wise Account balance → earns interest for Wise
 Settlement obligation: Wise must pay out €0.9948 via local rails, often same day
```
Never confuse €1 of volume with the €0.0052 of revenue: volume is ~192x revenue.

---

### IV.17 Economic Driver Tree

```
Active customers (18.9m)
  × transactions & VPC per customer
  = Cross-border volume ($243.5bn)
      × take rate (0.52%)
      = Cross-border revenue ($1,257m)
  + Card spend ($43.6bn) × card yield → Card revenue ($392m)
  + Account/domestic/Assets → Other revenue ($245m)
  = Transaction revenue ($1,893.6m)

Customer balances ($30.0bn on-BS + $9bn AUC)
  × net interest yield (gross ~3.0%, less first-1% & 80% pass-through target)
  = Net interest income ($609.2m net)

Transaction revenue + Net interest income = Net revenue ($2,502.8m)
  − variable transaction cost ($513.6m)
  − servicing/compliance ($396.6m)
  − technology ($434.3m) − marketing ($171.8m) − G&A ($381.9m)
  + other income ($69.7m)
  = Income before tax ($660.4m)
```

**The 8 variables that explain most outcomes:** (1) active-customer growth; (2) cross-border take rate; (3) volume per customer / card spend; (4) customer-balance growth; (5) central-bank interest rates (gross yield); (6) the % of above-1% interest actually paid to customers; (7) servicing + compliance cost per customer; (8) marketing efficiency (organic share).

---

### IV.18 Scenario Model [ANALYTICAL INFERENCE — illustrative, FY2026 US GAAP base]

| Scenario | Customers | Volume | Take rate | Net interest income | Net revenue | IBT margin | FCF |
|---|---|---|---|---|---|---|---|
| **A. Strong growth / normal rates** | +21% | +30% | −1–2bps/q | flat–up | +18–20% | ~24–26% | strong |
| **B. Strong growth / near-zero rates** | +21% | +30% | −1–2bps/q | −$500m+ | +8–10% | ~13–16% | lower |
| **C. Slow growth / normal rates** | +10% | +12% | stable | flat | +8–10% | ~26%+ | strong |
| **D. Severe price competition** | +25% | +35% | −5bps/yr | flat | +12–14% | ~18–20% | resilient |
| **E. Regulatory/compliance cost shock** | +18% | +25% | stable | flat | +15% | −3–5pp (servicing/G&A ↑) | lower |
| **F. Rails become materially cheaper** | +21% | +32% | −3bps (passed on) | flat | +16% | +1–2pp (cost ↓) | higher |
| **G. Wise Platform accelerates** | +21% | +40% (Platform→10%) | blended ↓ | up (balances) | +20%+ | stable–up | strong |
| **H. Consumer slows / business mix improves** | +12% | +18% | business-weighted ↓ | up (business balances) | +14% | stable–up | strong |

**Scenario E is live.** The 2024–2026 enforcement cluster directly raises servicing/compliance cost and is the principal downside to margin:
- **CEO fine:** on 28 October 2024 the FCA fined CEO **Kristo Käärmann £350,000** for breaching Senior Manager Conduct Rule 4 — failing to notify the FCA of a £365,651 HMRC tax penalty.
- **CFPB order:** originally $2m, reduced to a $45,000 penalty plus ~$450k redress.
- **US six-state AML consent order:** a **$4.2m** multistate order (9 July 2025) by California, Massachusetts, Minnesota, Nebraska, New York and Texas money-transmission regulators (each state receiving $700,000), covering the exam period 1 July 2022–30 September 2023, with a SAR lookback and two years of quarterly reporting.
- **Belgian criminal AML investigation:** disclosed via an LSE statement on 1 June 2026 (following the Bureau of Investigative Journalism's "Dirty Payments" report); the Brussels prosecutor is examining ~**€500m ($582.6m)** across hundreds of criminal files from 30+ countries. Prosecutors say the probe is "at an advanced stage and is nearing completion" and are "finalizing a direct summons"; Wise shares fell up to 20%, closing down 8% on disclosure.
- **OCC:** denial of the national trust bank charter (July 2026).

---

### IV.19 Sensitivity Analysis [ANALYTICAL INFERENCE]

| Variable | Change | Approx. IBT impact |
|---|---|---|
| Central-bank rates | ±25bp | ±$40m/yr |
| Central-bank rates | −200bp | ~−$320m (≈ ½ of FY26 IBT) |
| Cross-border take rate | −1bp on $243bn | −$24m revenue |
| Customer balances | +$5bn at 3% gross | +$150m gross interest |
| % of above-1% interest paid | +20pp paid out | −$60–80m IBT (toward target margin) |
| Volume growth | +5pp | +~$95m net revenue |
| Marketing efficiency | organic 70% → 60% | materially higher CAC, lower FCF |

**Most economically sensitive variables:** (1) **interest rates** (largest single swing — ~$40m/25bp); (2) **the unpaid-80% shortfall** (regulatory-contingent; normalising it removes the over-earning); (3) **take-rate vs volume elasticity** (the core flywheel bet).

---

### IV.20 Revenue-Quality & Durability Scorecard [ANALYTICAL INFERENCE]

| Stream | Predictability | Recurrence | Retention | Pricing power | Rate sensitivity | Competition | Margin | Reg. risk | Overall |
|---|---|---|---|---|---|---|---|---|---|
| Cross-border transfer | Med | Med | Med | Low | None | High | Med | Med | **Medium** |
| Card | High | High | High | Med | None | Med | Med-High | Med | **High** |
| Other / account / Assets | High | High | High | Med | Low | Low | High | Med | **High** |
| Wise Platform | High | High | Very high | Med | None | Med | Med | Med | **High (optionality)** |
| Interest income | Low | High | High | None | Very high | None | Very high | High | **Low quality (rate-driven)** |

**Highest-quality revenue:** card + other/account + Wise Platform (recurring, sticky, structurally growing 35–45%). **Lowest-quality:** interest income (highest margin but rate-driven, regulatory-contingent, not durable). The market should capitalise the recurring account/card/Platform lines at a premium and the interest line at a discount.

---

### IV.21 Profitability Decomposition & Near-Zero-Rate Counterfactual

**Decomposition of FY2026 IBT ($660.4m):**
- **Structural transaction economics:** transaction revenue $1,893.6m less attributable operating cost — modestly profitable on its own.
- **Balance/interest effect (rate-driven):** net interest income $609.2m, of which the retained-20% is structural framework but the unpaid-80% shortfall (~$150–200m) is a temporary regulatory windfall.
- **One-offs:** −$45m Nasdaq listing, −$70m FX (offset in OCI), plus one-off gains in other income.

#### Near-zero-rate counterfactual [ANALYTICAL INFERENCE]
Stripping net interest income to a near-zero level (~$50m residual) while retaining transaction economics:
- **FY2026 US GAAP base:** net revenue falls from $2,502.8m to ~$1,944m (transaction revenue $1,893.6m + ~$50m residual NII). Netting the associated disappearance of most customer-interest expense, approximate IBT ≈ **$180–230m, a margin of ~10–12%** vs 26.4% reported. The transaction business remains profitable, but only in the 13–16%/15–20% structural target zone.
- **FY2025 IFRS base:** underlying PBT was £282.1m on underlying income £1,362.3m (which already includes only the first-1% interest). Stripping even the first-1% interest (£150.4m) pulls underlying PBT toward ~£130–150m on revenue £1,211.9m — a **~11–12% margin**, again in the structural target zone.

**Answer:** if rates normalised sharply downward, Wise's underlying operating business would remain profitable at roughly its 13–20% structural target margin, but reported profit would roughly halve. The current 26% margin is materially rate- and regulatory-inflated.

---

### IV.22 Valuation-Relevant Economics

For Wise to compound value over 5–10 years, an investor must believe: (1) **volume elasticity keeps rewarding price cuts** — take rate falling 1–2bps/quarter while volume grows 25–30% (the SES flywheel intact); (2) **the recurring lines (card, account, Platform) keep growing ~35–45%**, structurally replacing rate-driven profit; (3) **Wise Platform scales toward 10%+ of volume**, embedding Wise as infrastructure and creating switching costs; (4) **compliance costs are absorbed** without permanent margin impairment despite the enforcement cluster; (5) **capital-light economics persist** — growth self-funded, minimal net dilution (EST offset), buybacks returning excess. Key risks: sharp rate cuts (halving reported profit), a regulatory cost shock (Scenario E, now live via the Belgian probe), and price competition without a volume payoff. FCF quality is high (underlying FCF converts >100% of underlying PBT), capital intensity is low, and the reinvestment runway is long. The valuation debate reduces to: how much of the 26% margin is durable (answer: ~15–20% structural) and how fast the recurring lines replace the rate windfall.

---

### IV.23 Volume IV Reconstruction — Synthesis

1. **Historical table:** IV.1 (Tables 1A IFRS FY2020–25, 1B US GAAP FY2024–26).
2. **Revenue taxonomy:** nine streams consolidating to transaction revenue + net interest income (IV.2).
3. **Revenue waterfalls by product:** IV.3.
4. **Take-rate history:** 0.73% (FY20) → 0.51% (Q4 FY26) (IV.4).
5. **Cost architecture:** six US GAAP buckets, classified variable→fixed (IV.5).
6. **Cost per transaction:** ~21bps of volume; scale from direct rails + netting (IV.6).
7. **Unit economics:** ~$132 net revenue/customer; paid CAC ~£30, blended ~£9 (IV.7).
8. **Cohort analysis:** hybrid remittance → account → infrastructure (IV.8).
9. **Income-statement teardown:** IV.9.
10. **Balance-sheet teardown:** $33.3bn assets, $30.3bn customer funds, $1.9bn equity (IV.10).
11. **Customer-funds architecture:** four pools; Comparable Guarantee as liquidity financing (IV.11).
12. **Interest-rate sensitivity:** ~$40m/25bp (IV.12, IV.19).
13. **Cash-flow / FCF bridge:** underlying FCF £332.7m FY2025 vs $7.6bn reported operating cash (IV.13).
14. **Capital architecture:** FOR-binding, £1.41bn CET1 vs £293.4m requirement (IV.14).
15. **Capital-allocation assessment:** reinvest-first, EST dilution offset, first £405m buyback (IV.15).
16. **€1 revenue waterfall:** IV.16.
17. **€1 volume waterfall:** IV.16.
18. **Economic driver tree:** IV.17.
19. **Scenario model:** eight scenarios (IV.18).
20. **Sensitivity:** rates > shortfall > elasticity (IV.19).
21. **Revenue-quality scorecard:** card/other/Platform high, interest low (IV.20).
22. **Key unknowns:** below.
23. **Ten most important conclusions:** below.

#### Ten Most Important Conclusions
1. **Wise's real economic engine is a two-cylinder machine:** a scalable transaction business (transaction revenue $1.9bn) plus a rate-driven balance business (net interest income $609m). The first is durable; the second is a partly temporary windfall.
2. **~Half of net revenue is now non-cross-border** (card, other, interest) — Wise has structurally diversified away from single-product remittance.
3. **The 26.4% FY2026 IBT margin is inflated** by ~10pp of rate/regulatory windfall (the unpaid-80% shortfall) plus one-offs; the durable structural margin is ~15–20%.
4. **Take-rate compression is a strategy, not a symptom:** 0.73% → 0.51%, deliberately funded by unit-cost cuts to compound volume (the SES flywheel).
5. **Interest income is the highest-margin but lowest-quality revenue** — rate-sensitive (~$40m/25bp) and regulatory-contingent.
6. **The highest-quality revenue is card + account + Wise Platform** — recurring, sticky, growing 35–45%.
7. **Wise is capital-light on equity but not on operational liquidity;** the £845m Comparable Guarantee is a deliberate instrument to convert trapped safeguarding cash into working liquidity.
8. **Genuine shareholder free cash flow (~£330m FY2025) is a fraction of reported operating cash flow ($7.6bn),** which is dominated by customer-fund inflows.
9. **Operating leverage is real but voluntarily reinvested** — ex-one-offs, opex grew below revenue.
10. **The dominant long-term variable is whether recurring lines replace the rate windfall fast enough** — plus the live tail risk of the 2024–26 enforcement cluster (now including the Belgian criminal AML probe over ~€500m).

#### Final answers to the completion questions
- **Real economic engine:** a scalable cross-border/card/account transaction business plus a rate-geared customer-balance interest business.
- **Highest-quality revenue:** card + other/account + Wise Platform (recurring, sticky).
- **Structural vs rate-driven profitability:** ~15–20% margin is structural; the excess to 26% is a rate/regulatory windfall.
- **Where operating leverage comes from:** sub-linear scaling of servicing/compliance and fixed technology/G&A against volume, plus direct-rail unit-cost reduction and internal netting.
- **How low take rate can fall:** plausibly toward ~40bps cross-border over the medium term, because ~half of net revenue now comes from non-cross-border lines and cost of sales keeps falling.
- **Is Wise capital-light:** yes on shareholder equity (FOR-binding, £293.4m requirement vs $498.7m net income); moderate and rising on operational liquidity.
- **Cleanest shareholder FCF measure:** underlying free cash flow (£332.7m FY2025), not reported operating cash flow.
- **Variable that matters most:** central-bank interest rates in the near term; the pace of recurring-revenue substitution in the long term.

#### Key Unknowns & Evidence Labels
**Company claims (not independently verified):** ~70% word-of-mouth acquisition; ~a third of staff in financial crime; 75% of Q4 FY2026 transfers instant (<20s). **Third-party estimates / analytical inferences (explicitly labelled):** LTV/CAC ratios, cost-per-transaction splits, revenue-stream margin splits, and all scenario/sensitivity outputs. **Unknown:** exact retention/cohort curves, per-corridor economics, the Wise Platform take rate, the timing of UK interest-payment resolution, and the outcome of the Belgian AML investigation. Where reputable sources disagreed (e.g. the FY2020 £21.3m vs restated £15.0m profit; FY2021 EPS on old vs post-split basis), both figures and the reason for the difference are preserved rather than silently reconciled.

*Volume IV ends here. Volume V has not been started.*


---

# Part V — Management, Culture, Competition, Moat, Risk & Strategic Evolution

*Forensic reverse-engineering study — institutional research report. As-of date: 8 August 2026. Evidence labels used throughout: CONFIRMED FACT / COMPANY CLAIM / THIRD-PARTY ESTIMATE / ANALYTICAL INFERENCE / HYPOTHESIS / UNKNOWN. Volumes I–IV are treated as established background; this volume executes Volume V only and does not begin the Cross-Volume Synthesis.*

---

### V.1 Founder Analysis

**Kristo Käärmann (co-founder, CEO)** and **Taavet Hinrikus (co-founder, ex-Chair, now outside critic)** founded TransferWise in January 2011. Käärmann is an ex-Deloitte/PwC management consultant; Hinrikus was Skype's first employee and director of strategy (CONFIRMED). The founding motivation is well-documented and consistent: the pair lost money on GBP/EUR transfers between London and Estonia and built a peer-matching workaround, from which the "money without borders" mission crystallised (CONFIRMED).

**Pricing philosophy — "Mission Zero."** Käärmann has consistently framed the mission as driving the price of moving money toward zero. On the FY2026 results call, CFO Emmanuel Thomassin stated: "Price is the number one argument for customers to come to us and to use us" (CONFIRMED). The take-rate history validates this as a *revealed* rather than merely *stated* philosophy: the average cross-border take rate fell from ~0.73% (FY2020) to 0.52% (FY2026 average) and 0.51% in Q4 FY2026, while cross-border volume compounded to $243.5bn (CONFIRMED, Vol IV). Wise applies a cost-plus approach route by route (COMPANY CLAIM, corroborated by pricing disclosures and the FY2026 call).

**Capital-allocation philosophy — owner-operator alignment.** Käärmann owns ~18% economics but has taken only a ~£200,000 base salary, no bonus and no LTIP for several years (CONFIRMED — data providers show ~£198.7k total, ~93.6% salary; CFO Dive documented his earlier explicit abstention from LTIP and bonus and his request not to have his salary reviewed). His wealth compounds only with the share price. Wise deliberately calls shareholders "Owners," runs an annual Owners Day (notably 3 April 2025), and had never conducted a buyback until FY2026 (CONFIRMED). This is a best-in-class alignment structure.

**Long-term orientation and path dependence.** Three decisions created durable path dependence: (1) building direct payment-system connections rather than renting correspondent rails; (2) the July 2021 LSE direct listing with a dual-class supervoting structure; and (3) the reinvest-the-margin-into-price policy that structurally caps the take rate. Each is difficult to reverse and each shapes the enterprise Wise is becoming.

**Governance controversy — the central founder-influence blemish.** On 28 July 2025 shareholders approved the US primary listing bundled with a 10-year extension of Class B supervoting rights (previously sunsetting July 2026). Hinrikus, acting through Skaala Investments OÜ (5.1% stake), opposed the bundling in a shareholder letter dated 21 July 2025: "It is entirely inappropriate and unfair to wrap these distinct issues together"; he warned that the 10-year extension "significantly exceeds standard practice" and that "Wise owners deserve governance structures that enhance value, not entrench power" (CONFIRMED). Class B holders control more than 90% of votes. The supervoting measure first appeared on page 10 of the proposal — sufficiently obscurely that proxy advisers Glass Lewis and ISS initially overlooked it and issued addenda; PIRC reversed to recommend against (CONFIRMED). Käärmann's votes are contractually capped one vote below 50% while he is CEO, dropping below 35% if he ceases to be CEO (CONFIRMED, per the Total Voting Rights RNS wording). This episode is a genuine contradiction of Wise's "radical transparency" brand and is the strongest evidence that founder control is being entrenched beyond ordinary governance norms (ANALYTICAL INFERENCE).

---

### V.2 Current Management Team

| Executive | Role | Tenure / notes | Prior experience |
|---|---|---|---|
| Kristo Käärmann | Co-founder, CEO, Director | CEO since 2011; ~18% economics (18.31% per data providers); votes capped <50% while CEO | Deloitte, PwC |
| Emmanuel Thomassin | CFO & Director | From 1 Oct 2024 | CFO Delivery Hero (IPO 2017), Team Global, MetaDesign |
| Harsh Sinha | CTO & Wise US President | CTO since May 2015; interim CEO Sep–Dec 2023; board member; signed the US multistate consent order as US President | Director of Product, PayPal; engineering leadership, eBay; MBA, UC Berkeley Haas |
| Nita [Group CCO] | Group Chief Compliance Officer | Joined Nov 2025 | Group CCO Credit Suisse 2022–23; 17 years Goldman Sachs (EMEA/APAC Asset Mgmt CCO) |
| Rohan Basu | Head of Global Operations | ~1.3 years | — |

**Board (as at 31 Mar 2026):** David Wells (Chair, ex-Netflix CFO), Käärmann (CEO), Thomassin (CFO), NEDs Terri Duhon, Clare Gilmartin (SID), Alex Rampell (a16z), Hooi Ling Tan (Grab co-founder), Elizabeth Chambers, and Scott Hill (ex-CFO of Intercontinental Exchange/NYSE). Ingo Uytdehaage stepped down 25 Sep 2025 (CONFIRMED). The Remuneration Committee was renamed the Compensation Committee effective 8 April 2026 following the Nasdaq listing restructuring.

**CFO transition:** Matthew Briers (8-year veteran) resigned; Kingsley Kemish served interim; Thomassin was appointed permanent from 1 October 2024 (CONFIRMED).

**Executive incentive structure (CONFIRMED from FY2026 RNS + MIFIDPRU 8 disclosure):** Executive directors participate in a Hybrid LTIP — performance shares (max 325% of salary; vesting on relative TSR vs the FTSE 250 and volume-growth measures over a 3-year performance period) plus restricted shares (max 325% of salary; vesting in equal annual tranches over three years subject to performance underpins), with a 2-year holding period and malus/clawback for up to five years (four years from grant for ED LTIP per MIFIDPRU 8). Analyst reconstruction indicates NPS thresholds (baseline ~63 for a 25% payout; full 100% only above 70) and a volume-growth threshold above ~13% (THIRD-PARTY ESTIMATE — to be verified against the primary FY2026 remuneration table; the exact FY2026 single-figure totals for Thomassin were NOT retrievable and remain UNKNOWN).

**Is Wise still founder-led? YES, unambiguously (CONFIRMED).** Käärmann has been CEO since inception, holds capped-but-decisive voting control, and the entire pricing/reinvestment strategy directly reflects his stated philosophy. Succession risk is structurally concentrated: the voting cap dropping to below 35% if he ceases to be CEO is a governance cliff that would materially alter control dynamics and potentially expose Wise to takeover.

---

### V.3 Management System

Wise runs an **autonomous-squad model** (tribes/guilds, weak code ownership, no dedicated manual QA, historically 120+ deploys/day) derived from the Spotify template, overlaid with a **Three-Lines-of-Defence risk architecture** (Group Risk Committee, ALCO, plus Financial Crime, Operational, Regulatory, Credit, Prudential, Market and Liquidity risk committees, and an Emerging Risk Forum), with FinCrime Product Compliance managers embedded inside product squads (CONFIRMED, Vol III).

**Revealed operating cadence:** quarterly public "Mission Updates" carry explicit KPIs (instant-transfer %, price/take-rate movements, and even headcount asks). Capital allocation is centralised under Käärmann and Thomassin; product execution is decentralised to squads. Compliance and risk functions hold veto rights via the embedded model and committee structure — but the enforcement cluster (below) demonstrates those vetoes were historically under-resourced relative to commercial growth. Notably, the General Counsel and Chief Risk Officer report to the CTO, and the Head of Internal Audit reports to the CFO with joint board reporting (CONFIRMED, Vol I) — an unusual set of reporting lines that itself raises questions about the independence of the control functions and is consistent with regulators' findings.

---

### V.4 Culture — Declared vs Revealed

**Declared culture:** "Customers > Team > Ego"; money without borders; radical transparency; autonomy; mission-driven frugality (CONFIRMED from company materials and Glassdoor citations of the value).

**Revealed culture (evidence-weighted):**

- **Customer orientation & price discipline — STRONG and genuine.** The relentless take-rate decline (0.73% → 0.52%) is the single strongest revealed-culture signal; management repeatedly chose lower price over higher margin. This is the authentic core of Wise's culture.
- **Autonomy — real but eroding.** Glassdoor (3.6/5 overall, 64% would recommend) consistently praises autonomy, but a growing minority describe "corporatization," "benefit cuts out of the blue," and one review states "there is no autonomy anymore… leads… have literally unlimited control and zero accountability." A classic scale-up tension between the mythologised early culture and a ~6,500-person organisation.
- **Regulatory discipline — WEAK relative to declared standards; this is the central contradiction.** The enforcement cluster reveals a culture that historically prioritised growth and speed over compliance maturity:
  - The **FCA fined Käärmann £350,000 on 27 October 2024** for breaching Senior Manager Conduct Rule 4. FCA joint executive director of enforcement Therese Chambers said: "We, and the public, expect high standards from leaders of financial firms, including being frank and open." The underlying £365,651 HMRC penalty (Feb 2021) was for deliberately failing to notify a capital-gains liability on ~£10m of shares sold in 2017; he was added to HMRC's public tax-defaulters list in September 2021 (CONFIRMED).
  - The **US multistate AML order of $4.2m, paid 9 July 2025** across six states for Bank Secrecy Act/AML/CFT failings (inadequate due diligence and suspicious-activity monitoring, late SAR filing, transaction-monitoring data-integrity issues, and Remittance Transfer Rule violations), later referenced in the OCC's own decision (CONFIRMED).
  - The **Belgian criminal AML investigation of Wise Europe SA**, disclosed 1 June 2026 via The Bureau of Investigative Journalism's "Dirty Payments" report. The Brussels Public Prosecutor's Office is examining "more than half a billion euros" (~$582.5m) in suspicious transactions across 30 European countries tied to fraud, corruption and drug trafficking; the case "originated from the repeated appearance of Wise in hundreds of criminal files received in Belgium… through European Investigation Orders and international letters rogatory," with prosecutors finalising a direct summons to the criminal court. Wise shares fell up to 20% intraday and closed down ~8% (CONFIRMED).
  - The **OCC's denial of Wise's national trust-bank charter (Corporate Decision #1381, dated 21 July 2026)**. Senior Deputy Comptroller Stephen Lybarger wrote that AML/CFT compliance would be lacking "until Wise has addressed existing deficiencies and develops an enhanced enterprise-wide AML/CFT program," and that management "failed to demonstrate sufficient experience with the fiduciary activities of national banks." This was the OCC's first public fintech-charter denial of the current approval cycle (CONFIRMED).
  The gap between "radical transparency" and the CEO's own failure to notify the FCA is a direct, personal declared-vs-revealed contradiction.
- **Transparency — contradicted by the supervoting bundling** (V.1). Hinrikus's critique that the extension was buried undercuts the brand.

---

### V.5 Incentive Architecture

| Group | Primary incentive | Behaviour rewarded | Gaming / conflict risk |
|---|---|---|---|
| Founder/CEO | ~18% equity; ~£200k salary; no LTIP/bonus | Long-term share-price compounding | Very low short-termism; high key-person concentration |
| CFO / EDs | Base + Hybrid LTIP (max 325% performance + 325% restricted); metrics = relative TSR vs FTSE 250, volume growth (~>13% threshold), NPS (~63→25%, >70→100%); 3-yr vest, 2-yr hold, up to 5-yr malus/clawback | Volume growth + customer satisfaction + TSR | Volume-growth metric can reward onboarding speed over KYC rigour — plausibly linked to AML shortfalls (ANALYTICAL INFERENCE) |
| All staff | Universal share awards (FY2025 total staff remuneration £412.8m across 6,151 beneficiaries) | Ownership alignment | Dilution — mitigated by EST purchases ($470m/35.9m shares in FY2026) |
| Compliance / Risk | Salary; embedded in squads | Control-function outcomes | Historically under-resourced vs commercial squads — the core structural conflict |

**Key conflict:** commercial squads incentivised on volume/growth versus compliance squads whose mandate is to add friction. The enforcement cluster is the empirical proof that this conflict was resolved in favour of growth for too long. The hire of a heavyweight Group CCO (ex-Credit Suisse/Goldman) in November 2025 is a revealed-priority correction (ANALYTICAL INFERENCE).

---

### V.6 Competitive Universe

**Cross-border specialists:** Remitly (9.3m active customers at YE2025, $74.9bn send volume, $1.64bn revenue, first full-year GAAP profit of $67.9m, take rate >2%); Western Union (structural decline — FY2025 revenue ~$4.2bn, down ~4–5%, with Consumer Money Transfer ~86–87% of revenue and shrinking; pivoting to digital and stablecoins); MoneyGram (money-transfer fee revenue down ~10% in 2025, all-in on stablecoins); OFX; Intermex (being acquired by Western Union).

**Neobanks / multi-currency accounts:** Revolut (68.3m retail + 767k business customers, $6bn/£4.5bn revenue in 2025, £1.7bn/$2.3bn PBT at a 38% margin, full UK banking licence March 2026, US bank-charter application filed March 2026, licensed bank in 30+ of 40 markets, targeting 100m customers by mid-2027); N26; bunq; Monzo.

**Payment platforms:** PayPal/Xoom (settling cross-border transfers via the PYUSD stablecoin, with Cebuana Lhuillier and Yellow Card as first disbursement partners); Block/Cash App.

**B2B cross-border / treasury:** Airwallex (Sacra estimates ~$1.5bn ARR by May 2026, ~200,000 businesses, ~$300bn annualised volume, ~93% of transactions off SWIFT, valued $6.2bn in May 2025 and reportedly ~$11bn in 2026); Corpay (Corporate Payments revenue ~$481m in Q4 2025, +39%; completed the $2.4bn Alpha acquisition November 2025; Circle stablecoin partnership); Banking Circle; Nium; Thunes; dLocal; Payoneer (being acquired context in a consolidating market).

**Financial infrastructure:** Stripe (owns Bridge, a stablecoin infrastructure business); Adyen; Nuvei.

**Emerging A2A / government infrastructure:** Project Nexus / Nexus Global Payments (BIS Innovation Hub initiative; NGP incorporated in Singapore March 2025; founding members India, Malaysia, the Philippines, Singapore and Thailand; ~2027 go-live target; ECB and Bank Indonesia as special observers; technical operator a PayNet–NETS joint venture).

**Stablecoin / blockchain:** Circle/USDC (~$73bn in circulation, full OCC national trust charter July 2026); Tether/USDT (>$130bn); Bridge (Stripe); PYUSD (PayPal/Paxos); Zerohash; nascent bank consortia.

**Coopetition:** Monzo, N26, Nubank and Google Pay are simultaneously Wise Platform distribution partners *and* competitors — a genuine structural tension Wise must manage, since deepening Platform relationships strengthens rivals' cross-border propositions.

---

### V.7 Competitor Teardowns (Comparison Matrix)

| Metric | **Wise (FY2026)** | Revolut (2025) | Remitly (2025) | Western Union (2025) | Airwallex (2026) | Corpay Cross-Border (2025) |
|---|---|---|---|---|---|---|
| Customers | 18.9–19m active | 68.3m retail + 767k business | 9.3m active | declining base | ~200,000 businesses | Enterprises / FIs |
| Volume | $243.5bn cross-border | $67.5bn balances | $74.9bn send | declining | ~$300bn annualised | — |
| Revenue | $2,502.8m net | $6bn / £4.5bn | $1.64bn | ~$4.2bn | ~$1.5bn ARR | ~$1.9bn segment |
| Profit | $660.4m IBT (26.4%) | £1.7bn PBT (38%) | $67.9m net (first FY) | declining EPS | not disclosed profitable | ~51% EBITDA margin |
| Take rate | 0.52% avg | blended higher | >2% | high (industry ~6.36%) | blended, shifting to cards | — |
| Licensing | 70+ licences, direct rails | bank licences 30+ mkts | MTLs + partners | MTLs + agent network | acquired licences | via acquisitions |
| Model | cost-plus, low margin | diversified (11 product lines >£100m) | FX markup + fees | FX spread + agent commissions | multi-product B2B | corporate payments |
| Moat | direct rails + treasury + cost | brand + breadth + bank licence | brand + corridors + CAC discipline | physical agent network (declining) | B2B infra + card issuing | scale + M&A + relationships |

**Read:** Revolut is larger by customers, revenue and profit but broader and far less cross-border-focused; it is the most dangerous strategic competitor precisely because its £1.7bn PBT and diversified product base let it subsidise FX to attack Wise's core. Remitly is a focused, now-profitable remittance specialist with a higher take rate but ~half Wise's customer count and a paid-acquisition cost base. Western Union is in structural decline, its physical agent moat eroding as mobile money and digital spread. Airwallex is the most dangerous B2B competitor, growing gross profit ~78% and shifting to higher-margin cards. Corpay dominates large-corporate cross-border through scale and acquisitions.

---

### V.8 Why Wise Is Cheaper — Decomposition

The cost advantage is roughly the gap between the industry's ~6.36% global average cost to send remittances (World Bank Remittance Prices Worldwide, Issue 54, September 2025: "the Global Average cost for sending remittances was 6.36 percent"; banks are most expensive at 14.99%, digital-only MTOs at 3.54%) and Wise's ~0.5% take rate. Decomposition:

1. **Direct local rail access / correspondent-banking avoidance — the largest structural driver.** A Wise "cross-border" transfer is two synchronised domestic payments linked by an internal ledger; money crosses borders only in periodic bulk rebalancing. This eliminates 2–4 correspondent intermediaries, each charging fees and FX spreads. Wise holds 8+ direct connections (UK Faster Payments with a Bank of England settlement account, Hungary MNB, Singapore FAST, Australia NPP, Philippines InstaPay/PesoNet, Brazil Pix, Japan Zengin, Malaysia PayNet, plus SEPA/SEPA Instant).
2. **Internal matching / netting — compounds with scale.** With $243.5bn of annual volume, a large share of demand on any corridor nets internally; only the net imbalance requires an actual FX trade and cross-border rebalance. Netting reduces the number, average size and cost of external payments — a genuine scale-driven cost curve.
3. **Treasury scale.** The real-time double-entry Treasury Ledger feeds desks executing FX in the tens-to-hundreds of millions, securing near-institutional pricing and minimising float losses.
4. **Organic acquisition (~70% word-of-mouth — COMPANY CLAIM).** Near-zero customer-acquisition cost on the majority of customers structurally lowers cost per customer versus Remitly's and Western Union's paid-acquisition models.
5. **Automation of support and compliance.** ~50% of chat handled by LLMs in FY2026; cloud-native card processing; ~4.7m transactions/day at low marginal cost.

**Separation of causes:** *Structural cost advantage* (rails, netting, treasury, organic CAC, automation) vs *management choice to price lower* (the cost-plus-target-margin policy that reinvests the ~15–20% over-earn back into price) vs *temporary competitive pricing* (route-specific promotions). The bulk of the gap is structural; the deliberate management choice is what converts that structural advantage into lower *price* rather than higher *margin*. A rival could not simply match Wise's price without first matching its cost base — which is why banks white-label Wise instead.

---

### V.9 Moat Scorecard (0–5)

| Moat | Score | Mechanism / evidence / durability / weakening conditions |
|---|---|---|
| Direct rail connectivity | **4 (Very Strong)** | 8+ direct connections + 70+ licences; first non-bank on UK FPS and Japan Zengin with a BoE settlement account. Replicable only over many years, jurisdiction by jurisdiction. Weakens if Nexus/instant interop commoditises the rails. |
| Treasury / netting scale | **4 (Very Strong)** | Genuinely compounds: more volume → more internal netting → lower unit FX and rebalancing cost. Durable while Wise is the largest independent pure-play. Weakens only if a rival reaches comparable corridor liquidity. |
| Cost position | **4 (Very Strong)** | Downstream of rails + netting + organic CAC; the deepest structural advantage and the source of the price weapon. |
| Regulatory architecture | **3 (Strong)** | 70+ licences are a real barrier, but the enforcement cluster shows regulation is also a liability; the OCC denial proves accumulated licences do NOT guarantee new permissions. Necessary, not sufficient. |
| Brand / trust | **3 (Strong)** | Strong within the cross-border niche; ~70% word-of-mouth. Actively eroded by AML headlines (Belgian probe, OCC denial). |
| Wise Platform switching costs | **3 (Strong)** | 85+ partners; deep API/correspondent integrations become embedded in banks' payment flows and are sticky once live. Still early (~5% of volume). |
| Technology | **3 (Strong)** | >1,000 microservices, world-first cloud card processing, real-time ledger — differentiated but reproducible by a well-funded rival over 2–3 years. |
| Network effects | **2 (Moderate)** | Largely mislabelled scale economies. An additional customer does NOT directly make the network more valuable to others (no genuine two-sided effect); the benefit flows through netting/liquidity, i.e., scale, not network effects. |
| Data / fraud | **2 (Moderate)** | Useful for routing and fraud detection but not unique; AML failures show data ≠ compliance excellence. |
| Customer switching costs (consumer) | **1 (Weak)** | Consumers multi-home; comparison sites drive price shopping; low lock-in beyond the multi-currency account/card habit. |

**Strongest genuine moat: the integrated cost stack (direct rails + netting + treasury + organic acquisition).** Most overrated: licences and "network effects."

---

### V.10 Replication Test (Cost / Time Matrix)

*Scenario: Wise disappears; a well-funded competitor attempts to recreate it.*

| Component | Time | Capital | Difficulty | Verdict |
|---|---|---|---|---|
| UK EMI licence + BoE settlement account + FPS direct participation | 2–4 yrs | ££ | High (regulatory) | Buildable with time |
| Replicate 8 direct rail connections (multi-jurisdiction) | 5–10 yrs | £££ | Very high | Difficult — path-dependent |
| 70+ global licences | 5–10+ yrs | £££ | Very high | Difficult |
| Safeguarding + Comparable Guarantee infrastructure | 2–4 yrs | ££ | Medium-high | Buildable |
| Real-time treasury ledger + FX desks | 2–3 yrs | ££ | High (talent) | Buildable |
| Compliance / fraud at scale | 3–5 yrs | £££ | High | Buildable but slow — Wise itself is still failing to reach the standard |
| Acquire ~19m customers at market CAC | 3–7 yrs | £5–10bn+ | Very high | Effectively irreproducible at comparable cost — Wise's ~70% organic acquisition is the true moat |
| Wise Platform integrations (85+ partners) | 3–5 yrs | ££ | High (trust/sales) | Difficult |
| Net liquidity / netting depth | follows volume | — | — | Irreproducible without first winning the volume |

**Effectively irreproducible at comparable cost/time:** the customer base built via organic word-of-mouth, and the netting/liquidity depth that only volume produces. **Easily purchased:** cloud technology, individual licences (with money), individual bank relationships. This is the crux — money can buy the *inputs* but not the *organically-acquired demand and liquidity network* that make the cost model work.

---

### V.11 Porter's Five Forces (tied to Wise)

- **Rivalry — HIGH and intensifying.** Revolut (broader, more profitable), Airwallex (B2B), Remitly (remittances) and stablecoin entrants. Price competition is the arena Wise deliberately chose; it differentiates on speed, price and transparency. Market growth is high, which moderates rivalry, but the price ceiling keeps pressure on.
- **Supplier power — MODERATE-HIGH.** Partner banks (e.g., CFSB in the US), card networks (Visa), cloud (AWS) and KYC vendors have leverage; direct-rail access reduces bank dependence over time. Critically, **regulators act as institutional gatekeepers** — the OCC denial demonstrates their power over Wise's expansion path.
- **Buyer power — consumer LOW individually but HIGH in aggregate** (price transparency, easy multi-homing); **enterprise/Platform buyers HIGH** (banks negotiate cost-plus terms and can, in principle, insource).
- **Substitutes — RISING.** Stablecoins, Nexus instant interop, open banking and bank modernisation. Analytical view: these threaten the *rails* layer, not necessarily Wise's *compliance/treasury/distribution wrapper*.
- **New entrants — MODERATE.** High barriers (licences, liquidity, trust, CAC), but well-funded fintechs and OCC-chartered stablecoin issuers (Circle) can enter the settlement layer credibly.

---

### V.12 PESTLE (material factors)

- **Political:** sanctions/OFAC compliance; US immigration enforcement depressing Latin American remittance corridors (visibly hurting Western Union and relevant to Wise US); geopolitical fragmentation; state-backed payment initiatives (Nexus, Pix, UPI).
- **Economic:** interest rates (Wise IBT sensitivity ~$40m per 25bp; a return to near-zero rates would remove the bulk of ~$609m net interest income); FX volatility (revenue driver); migration flows; trade and business-activity volumes.
- **Social:** migration, remote work, cross-border families, globalisation, and shifting trust in banks vs fintechs (currently a two-edged factor given AML headlines).
- **Technological:** instant payments, open banking, stablecoins (GENIUS Act, July 2025), AI (support, fraud, and emerging financial agents), digital identity, cloud, cybersecurity.
- **Legal:** payments regulation, AML/BSA (the binding constraint — multistate order, Belgian probe, OCC denial), consumer protection (CFPB Remittance Transfer Rule), safeguarding, competition law, privacy.
- **Environmental:** immaterial to the investment thesis.

---

### V.13 Positive Flywheels

1. **Cost flywheel (PROVEN).** More volume → more netting + lower rail/treasury unit cost → lower price → better proposition → more volume. Evidence: take rate 0.73% → 0.52% while volume compounded to $243.5bn. Limit: price approaches the marginal-cost floor; the first ~1% of yield is retained to cover Wise Account operating costs.
2. **Organic-acquisition flywheel (PROVEN; COMPANY CLAIM ~70% word-of-mouth).** Low price → satisfied customers → referrals → near-zero CAC → more budget available for further price cuts. Failure condition: a trust shock (AML scandal) that breaks word-of-mouth.
3. **Platform flywheel (EARLY).** More volume → scale → lower cost → stronger infrastructure product → more bank partners → more volume. Currently ~5% of cross-border volume; target ~10% medium-term, >50% long-term.
4. **Account-adoption flywheel (EMERGING).** Multi-feature adoption (~50% of personal, ~60% of business customers) → more holdings ($39bn) → more net interest income and card interchange → funds further price cuts. This is why ~50% of net revenue is now non-cross-border.

---

### V.14 Negative Flywheels

1. **Compliance-cost spiral (ACTIVE — most dangerous).** AML failures → enforcement (fines, the Belgian probe, the OCC denial) → mandated remediation + slower/tighter onboarding → higher cost + slower growth → pressure on the price-cut engine. This is the live negative flywheel that most threatens the core thesis.
2. **Price-competition spiral.** Lower take rate → less absolute contribution per transfer → if volume growth ever slows, reinvestment capacity shrinks → weaker advantage.
3. **Scams/fraud spiral.** Losses → tighter controls → more friction → churn.
4. **Complexity/bureaucracy spiral.** Headcount growth → "corporatisation" (Glassdoor) → slower execution, eroding the autonomy advantage that historically powered fast iteration.

---

### V.15 Theory of Constraints / Bottleneck

**Current bottleneck: regulatory/compliance capacity and credibility.** Evidence is direct and recent: the OCC explicitly denied the charter citing unresolved AML deficiencies and management's insufficient national-banking experience; the Belgian criminal probe; and the multistate order's multi-year remediation burden. This single constraint gates US expansion, the trust-bank/stablecoin ambition, and — because banks diligence Wise's compliance before white-labelling — even Wise Platform partnerships. If every other part of Wise improved by 50%, compliance credibility would still cap growth.

**Next bottleneck if solved: Wise Platform enterprise sales + management bandwidth.** Converting the >50%-of-volume vision requires a mature enterprise/bank sales motion and integration capacity, compounded by the key-person concentration on Käärmann.

---

### V.16 Risk Register (Probability × Severity, with detectability, mitigation, residual risk, horizon)

| Risk | Probability | Severity | Detectability | Mitigation | Residual | Horizon |
|---|---|---|---|---|---|---|
| AML/BSA enforcement | High | High | Medium | Remediation; new Group CCO (ex-CS/GS) | High | Now |
| Belgian criminal case | Med-High | Med-High | High | Cooperation; disclosure | Med-High | 0–2 yrs |
| Regulatory expansion blocked (OCC) | Materialised | Medium | High | GENIUS Act refiling | Medium | Now |
| Interest-rate decline | Medium | High (~$40m/25bp) | High | Fee mix, price levers | Medium | 1–3 yrs |
| Take-rate compression | High (guided) | Medium | High | Volume growth, NII, card | Medium | Ongoing |
| Stablecoin/rail disruption | Medium | Medium | Medium | Rail-agnostic stance; GENIUS pivot | Medium | 3–7 yrs |
| Bank-partner loss (e.g., CFSB) | Low-Med | High | Medium | Diversify; direct rails | Medium | 1–3 yrs |
| Cyber / operational incident | Medium | High | Medium | Cloud resilience; monitoring | Medium | Ongoing |
| Key-person (Käärmann) | Low-Med | Very High (votes drop <35%) | High | Board; Sinha as bench | High | Ongoing |
| Governance/dual-class backlash | Medium | Medium | High | — | Medium | Ongoing |
| Competition (Revolut FX subsidy) | Medium | Med-High | High | Cost leadership | Medium | 1–5 yrs |
| FX / treasury / liquidity | Low | High | High | Real-time ledger; ALCO | Low-Med | Ongoing |
| Reputation (AML headlines) | High | Medium | High | PR; remediation | Med-High | Now |

**Single points of failure:** (a) Käärmann — voting cliff plus founder-led strategy continuity; (b) the US banking-access pathway (OCC charter / Fed master account); (c) any single critical partner bank in a major corridor.

---

### V.17 Stress Tests

1. **Rates fall to ~0.** Loses the bulk of ~$609m net interest income; at ~$40m IBT per 25bp, a multi-hundred-million IBT hit. Forces reliance on transaction and card revenue ($1,893.6m transaction revenue). *Survivable*, but reported margin compresses toward the structural 15–20%.
2. **Average transfer prices fall 50%.** Wise's cost-plus model lets it follow prices down further than rivals; accelerates share gains but slows revenue growth. *Survivable*; higher-take-rate competitors (Remitly, WU) suffer disproportionately.
3. **Banks match Wise pricing.** Unlikely at scale — banks' correspondent cost base makes sub-1% cost-plus structurally unprofitable. Would dent Wise's growth but is not sustainable for the banks.
4. **Revolut heavily subsidises cross-border FX.** The most credible competitive threat; Revolut's £1.7bn PBT funds cross-subsidy. Wise's defence is pure-play cost leadership; expect margin pressure and a marketing-spend response (Wise already committed to roughly triple marketing investment).
5. **Stablecoins become mainstream settlement.** Ambiguous — could commoditise the rails (adverse) OR cheapen Wise's own settlement (favourable). Wise's GENIUS-Act pivot positions it to adopt; advantage shifts to the compliance/distribution wrapper.
6. **Governments connect instant-payment systems cheaply (Nexus).** The biggest structural threat to the rail moat, but Nexus provides *connectivity*, not FX conversion, AML, liquidity or UX — Wise could ride Nexus as a participant. APAC-first, ~2027 go-live limits near-term impact.
7. **Loses a major bank.** Short-term corridor disruption; direct rails reduce dependence over time.
8. **Loses direct access to an important rail.** Corridor-specific cost/speed regression plus reputational and competitive damage.
9. **A major regulator restricts Wise.** Already partially materialised (OCC). US growth capped; EU exposure sits with the Belgian case.
10. **Fraud/scam losses double.** Margin and reputation hit; tighter controls raise friction and threaten the word-of-mouth engine.
11. **Customer growth stalls.** Breaks the flywheel; take-rate compression without volume growth would erode absolute contribution.
12. **Business growth disappoints.** Slows the higher-value segment (Business Q4 FY2026 take rate 0.39%) and the account-adoption flywheel.
13. **Wise Platform accelerates dramatically.** The best bull case — moves toward the >50% vision with higher-quality recurring volume and a stronger infrastructure identity.
14. **Founder leadership disappears.** Voting drops below 35%; strategy-continuity risk; potential takeover vulnerability.
15. **Major cyber/operational incident.** In a trust-dependent business, potentially severe and lasting reputational damage.

---

### V.18 What Could Make Wise Obsolete?

For each disruptor: does it remove the customer problem, cut Wise's cost, can Wise adopt it, does the distribution/regulatory layer stay valuable, does it commoditise Wise, or strengthen it?

- **CBDCs:** slow and fragmented; unlikely to solve cross-border FX/compliance soon. Neutral-to-benign.
- **Stablecoins (GENIUS Act):** commoditise settlement rails but not FX conversion, compliance or distribution. Wise can adopt (rail-agnostic; GENIUS refiling). Net effect: reduces Wise's costs more than it destroys Wise — *if* Wise adopts.
- **Instant-payment interop (Nexus):** the sharpest threat to the rail moat, but connectivity ≠ FX + AML + liquidity + UX. Wise can participate. 2027 go-live limits near-term impact.
- **Open banking:** strengthens Wise (cheaper funding, better UX).
- **Bank modernisation:** slow; banks are becoming Wise Platform customers rather than rebuilding.
- **AI financial agents:** could commoditise the *consumer front-end* (agents price-shop across providers) — a real threat to consumer stickiness; benign or positive for the infrastructure layer.
- **Government cross-border infrastructure:** see Nexus.

**Verdict:** Wise's advantage is primarily the licensing/compliance/treasury/distribution wrapper around the rails, not the rails alone. Cheaper rails mostly *help* Wise. The genuine obsolescence risk is a *combination* — Nexus-style interop + stablecoin settlement + AI agents commoditising consumer distribution — playing out over 5–10 years, and only if Wise fails to adopt each.

---

### V.19 Strategic Optionality Matrix

| Adjacency | Classification | Rationale |
|---|---|---|
| Deeper business banking / treasury | Natural | Existing Business account; $39bn holdings; direct overlap with Airwallex |
| AP/AR, invoicing, payroll | Plausible | Fits Business; competitive vs Airwallex, Corpay |
| Enterprise APIs / Wise Platform expansion | Natural | Already core strategy; the >50% vision |
| Card capabilities | Natural | $43.6bn card spend; interchange revenue engine |
| Savings / investment (Assets) | Plausible | Already live; rolled out to Brazil in FY2026 |
| Stablecoin rails / GENIUS issuer | Plausible-to-Stretch | Post-OCC pivot; requires AML remediation first |
| Identity / compliance infrastructure | Stretch | Would monetise a current weakness — implausible near-term |
| Working capital / credit | Stretch | Regulatory/capital burden; off the asset-light model |
| Full consumer bank (à la Revolut) | Strategic fantasy | Contradicts the asset-light, capped-margin identity |

---

### V.20 What Is Wise Becoming? (Probability-ranked hypotheses)

1. **International Payments Network / Global Financial Utility (H3 + H5) — ~45%.** Strongest evidence: the Wise Platform >50% vision, direct rails, "network for the world's money" language, and cost-plus infrastructure economics. Management behaviour (rail-building; Platform wins including UniCredit, Raiffeisen, MBSB and Capitec) confirms the trajectory.
2. **B2B Financial Infrastructure (H4) — ~25%.** Platform + Business converging; competes directly with Airwallex and Corpay.
3. **Global Multi-Currency Account (H2) — ~20%.** ~50% of net revenue is now non-cross-border (NII, card, other); account adoption is rising.
4. **Remittance/FX Company (H1) — ~10%.** Increasingly reductive; still the cash engine but not the direction of travel.

**Synthesis:** Wise is becoming a **global payments-infrastructure utility** with a consumer/business account front-end that funds it — a hybrid of H3, H4 and H5.

---

### V.21 Five-Year and Ten-Year Scenarios

| Scenario | Customers | Take rate | Revenue mix | Margin | Platform share | Moat | Strategic identity |
|---|---|---|---|---|---|---|---|
| **Base case** | compounding ~15–20% | −1–2 bps/qtr | ~50% non-cross-border | 20–25% (over-earn) → 15–20% | ~10% | intact | infrastructure + account |
| **Strong execution** | accelerating | slow decline | balanced across streams | top of 20–25% | >10% | widening | leading global network |
| **Infrastructure winner** | Platform-led | lower blended | Platform-heavy | infrastructure-style | 30–50% | dominant | global financial utility |
| **Commoditised pricing** | high volume, low rate | collapses | NII/card-dependent | compressed | mixed | thinner | low-cost utility |
| **Technology disruption (Nexus/stablecoin)** | pressured | pressured | shifts | lower | adopts rails | narrower | participant, not owner |
| **Regulatory disruption** | US capped | — | — | higher cost | slower | dented | constrained regional player |
| **Competitive consolidation** | share loss | pressured | — | lower | contested | eroded | niche specialist |

---

### V.22 What the Market May Misunderstand

1. **"Wise is just a remittance company."** Reality: ~50% of net revenue is non-cross-border (NII, card, other); it is a payments network plus a multi-currency account. The misconception persists because remittance is the origin story. Implication: the market may under-value the Platform and account optionality.
2. **"Its moat is only low fees."** Reality: low fees are the *output*; the moat is the direct-rail + netting + treasury + organic-CAC cost stack that *produces* them. Copying the price without the cost base is loss-making. Implication: fee cuts are a weapon, not a vulnerability.
3. **"Licences are the moat."** Reality: the OCC denial proves accumulated licences do not guarantee expansion; licences are necessary but not sufficient and can become liabilities. Implication: the regulatory story is more fragile than bulls assume.
4. **"Interest income is the business."** Reality: net interest income (~$609m) is a cyclical tailwind Wise is structurally trying to give back (the intended 80% pass-through); durable margin is 15–20% from transaction economics. Implication: rate-driven earnings are lower-quality than headline margin suggests.
5. **"Banks can copy Wise easily."** Reality: banks' correspondent cost base and legacy technology make cost-plus at ~0.5% structurally unprofitable — which is precisely why 85+ banks white-label Wise Platform instead. Implication: banks are becoming customers, not clones.
6. **"Wise Platform is merely an API product."** Reality: it is a correspondent-banking replacement embedding Wise into banks' payment flows — potentially the majority of future volume. Implication: the Platform is the real long-term equity story.

---

### V.23 Management and Capital-Allocation Judgment

| Decision | Verdict | Evidence |
|---|---|---|
| Relentless price cuts / reinvest margin | Value-creating | Volume and customer compounding; ~70% organic acquisition |
| Direct-rail infrastructure investment | Value-creating | Structural cost moat; unit-cost decline |
| 2021 LSE direct listing | Strategically sound | First UK tech direct listing; no dilution |
| US primary listing (Nasdaq, May 2026) | Too early to judge | Access to deeper capital markets and higher-multiple peers |
| Class B 10-year extension bundling | Questionable | Governance blemish; Hinrikus critique; proxy-adviser concerns; contradicts "radical transparency" |
| Under-investment in compliance (historical) | Value-destroying | Enforcement cluster; OCC denial capped US expansion |
| First buyback (£405m, executed by Goldman Sachs International, 21 Jul 2026–31 Mar 2027) + EST purchases ($470m/35.9m shares FY2026) | Reasonable | Owner-friendly; ~40% of the programme allocated to the EST to offset dilution |
| Wise Platform strategy | Value-creating (early) | 85+ partners; structural optionality toward the network vision |
| Founder low pay / high equity | Value-creating | Best-in-class management alignment |

---

### V.24 Volume V Reconstruction — Consolidated Conclusions

**Ten Most Important Conclusions**
1. Wise wins today on a **structural cost advantage** (direct rails + netting + treasury + ~70% organic CAC), converted into price by a deliberate cost-plus policy.
2. The **strongest moat is the integrated cost stack**, not licences or "network effects."
3. **Most overrated moat: licences and network effects** — the OCC denial and multi-homing consumers expose their limits.
4. **Hardest to replicate:** the organically-acquired ~19m customer base and the netting/liquidity depth that only volume creates.
5. **Easiest to replicate:** the technology stack, individual licences, and individual bank relationships.
6. **Current bottleneck: compliance capacity and credibility** — gating US expansion, the stablecoin ambition, and Platform trust.
7. **Greatest structural risk: the compliance-cost negative flywheel**, intersecting with regulatory expansion denial.
8. **Most dangerous competitor: Revolut** (scale plus profit pools to subsidise FX); **Airwallex** is most dangerous in B2B.
9. **New rails (Nexus/stablecoins) more likely strengthen than obsolete Wise** — provided Wise adopts them; its moat is the wrapper, not the rails.
10. **Wise is becoming a global payments-infrastructure utility** with a consumer/business account funding engine.

**Direct answers to the completion questions**
- *Why does Wise win today?* Lowest structural cost, passed to customers as the lowest price, driving organic volume that lowers cost further — a self-reinforcing cost-and-acquisition flywheel.
- *Strongest moat component?* The direct-rail + netting + treasury cost stack.
- *Most overrated moat?* Licences and claimed network effects.
- *Hardest to replicate?* The organically-acquired customer base and netting depth.
- *Easiest to replicate?* Technology and purchasable licences/bank links.
- *Current bottleneck?* Compliance credibility.
- *Single greatest structural risk?* The AML-enforcement negative flywheel.
- *Most dangerous competitor?* Revolut in consumer/account; Airwallex in B2B.
- *Could new rails make Wise obsolete, or would it benefit?* Net benefit if adopted — the wrapper (licensing, compliance, treasury, distribution), not the rail itself, is the moat.
- *What is Wise ultimately becoming?* A global financial/payments-infrastructure utility (network plus account) — not merely a consumer fintech or a remittance company.

**Key Unknowns**
- Exact FY2026 per-executive single-figure remuneration (particularly for CFO Thomassin) — not retrievable from available sources; requires direct inspection of the FY2026 Form 20-F/UK Annual Report Compensation Report.
- The ultimate outcome and any penalty from the Belgian criminal case against Wise Europe SA.
- The timing and success probability of the GENIUS Act stablecoin-charter refiling, and whether a Fed master account would ultimately be granted.
- Whether Project Nexus achieves meaningful scale beyond its APAC founding members by the ~2027 go-live, and whether Wise participates as a connected institution.

*End of Volume V. The Cross-Volume Synthesis has not been started, per instruction.*


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
