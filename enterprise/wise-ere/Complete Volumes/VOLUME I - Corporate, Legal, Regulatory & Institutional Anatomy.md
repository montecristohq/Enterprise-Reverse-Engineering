# Wise Group plc — VOLUME I: Corporate, Legal, Regulatory & Institutional Anatomy
### An institutional-grade forensic reverse-engineering study | Research cut-off: 8 August 2026

*Evidence labels used throughout: **[CONFIRMED]** = directly supported by reliable/primary evidence; **[COMPANY CLAIM]** = stated by Wise, not independently verified; **[THIRD-PARTY ESTIMATE]**; **[INFERENCE]** = reasoned from multiple facts; **[HYPOTHESIS]**; **[UNKNOWN]**. Volume I only — Volume II is not begun.*

---

## TL;DR
- **Wise is controlled by its founder-CEO and legally engineered around a single UK-authorised e-money institution.** As of the FY2026 reorganisation, the group's ultimate parent is **Wise Group plc, a Jersey-incorporated, UK-tax-resident company** (Nasdaq: WSE; LSE: WISE) that on 8 May 2026 became parent of **Wise Limited (formerly Wise plc)**. Co-founder Kristo Käärmann holds ~18% of the economics but, via nine-vote Class B shares, would command >50% of votes — contractually capped at one vote below 50% while he remains CEO (falling to below 35% if he ceases to be CEO). Real control sits with Käärmann; economic ownership is dispersed across institutions (Baillie Gifford ~10.5% of Class A) and the founders.
- **The regulatory estate is the moat, and one entity is the crown jewel.** Wise operates 80+ licences across dozens of jurisdictions, but the economically decisive permissions are the UK EMI licence held by **Wise Payments Limited** (FCA FRN 900507) and the Belgian payment-institution licence held by **Wise Europe SA** (NBB, No. 0713629988), which passports across the EEA. The rarest asset is direct settlement access to national payment systems (UK Faster Payments/Bank of England RTGS, plus 7 others), where Wise was the first non-bank to obtain several connections.
- **The architecture is under real stress in 2026.** A $4.2m US six-state AML consent order (9 July 2025), a CFPB order (2025), a Belgian criminal money-laundering investigation of Wise Europe SA (>€500m/$569m, disclosed 1 June 2026), the FCA's £350k fine of the CEO (28 Oct 2024), and the OCC's 21 July 2026 denial of Wise's national trust bank charter together reveal that Wise's binding constraint is no longer technology or licensing breadth — it is financial-crime compliance execution at scale.

---

## Key Findings

1. **[CONFIRMED]** Founded January 2011 in London as TransferWise by Estonians Taavet Hinrikus (Skype's first employee) and Kristo Käärmann (ex-Deloitte/PwC). The original vehicle was registered by Käärmann in England on 31 March 2010 as "Exchange Solutions," renamed TransferWise (2012) and Wise (Feb 2021).
2. **[CONFIRMED]** Direct listing on the LSE on 7 July 2021: shares opened at 800p and closed at 880p, giving a **£8.75bn (~$12bn) market value** — the first direct listing of a tech company in London and, at the time, the largest such deal. It raised no primary capital; existing holders sold to the market. First trades began at 11:22am BST under ticker WISE.
3. **[CONFIRMED]** On 28 July 2025 shareholders approved moving the primary listing to the US, bundled with a controversial 10-year extension of Class B supervoting rights (previously due to sunset in 2026). Co-founder Hinrikus (via Skaala Investments, ~5%) publicly opposed the bundling as "inappropriate and unfair." The scheme was court-sanctioned 27 April 2026; effective 8 May 2026; Nasdaq trading began 11 May 2026.
4. **[CONFIRMED]** A Jersey topco (Wise Group plc) was inserted via a Part 26 Companies Act 2006 scheme of arrangement, 1:1 share exchange, dual-class structure retained, nominal values redenominated to USD ($0.01 Class A; $0.000000001 Class B). Old Wise plc renamed Wise Limited.
5. **[CONFIRMED]** FY2026 (year to 31 Mar 2026): active customers up 21% to **19 million**; cross-border volume up 31% to **$243.5bn**; net revenue **$2,502.8m** (+19%); **income before tax $660.4m** (26.4% margin); customer holdings **$39bn** (incl. $9bn Wise Assets). Reporting shifted to US GAAP and USD.
6. **[CONFIRMED]** Group held >£1.29bn CET1 capital vs a £219.8m own-funds requirement (FY2025) — a **590.41% surplus buffer**. The binding requirement is the Fixed Overheads Requirement (£219.8m), not the K-factor (£40.0m) or permanent minimum (£6.4m).
7. **[CONFIRMED]** Customer money is **safeguarded (not deposited)**; roughly ~60% in government securities/money-market funds and ~40% cash at banks (e.g., JPMorgan Chase for EU cash; BlackRock and State Street MMFs). Wise earns interest income on safeguarded balances; separately, "Wise Assets" passes MMF returns (managed by BlackRock) to customers.
8. **[CONFIRMED]** Wise depends on **Community Federal Savings Bank (CFSB)** as US card issuer and sponsor bank in states where Wise lacks its own money-transmitter licence — a concentration risk underscored by an OCC AML enforcement action against CFSB.

---

## Details

### I.1 Origin and Corporate Institutional Evolution

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

### I.2 Group Structure (FY2025 consolidation basis; topco changed May 2026)

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

### I.3 Ownership and Share Structure

**Dual-class mechanics:** Class A = 1 vote (listed, tradeable); Class B = 9 votes (non-transferable, unlisted, "golden" supervoting). Each Class B corresponds to a Class A. At the 2021 IPO the largest external holders were Valar Ventures (~10.2%), IA Ventures (~9.6%), Andreessen Horowitz (~9.3%), Baillie Gifford (~4.9%), D1 Capital (~3.9%), IVP (~3.7%); founders held roughly a third combined.

**As of 2026 (post-Nasdaq):** Baillie Gifford filed a Schedule 13G reporting **~10.53% of Class A** (108,011,990 shares; sole voting power over 98,802,398). Käärmann holds ~18% economics; Hinrikus/Skaala ~5%. Total voting rights sit around 2.86–2.95bn depending on issuance date; **Käärmann's votes would exceed 50% but are capped at one vote below 50% while he is CEO** (dropping to below 35% if he ceases to be CEO) — bringing exercisable votes to roughly 2.44bn.

**Economic vs voting divergence — the defining governance fact.** Economic ownership is dispersed and institutional; voting control is founder-concentrated by design. Management cannot realistically be removed against Käärmann's wishes while the cap sits just below 50% and Class B carries 9× votes. This is the trade the market accepted in the July 2025 vote, over the objection of co-founder Hinrikus and initial concern from Glass Lewis and ISS.

### I.4 Governance Architecture

**Board (as of 31 Mar 2025):** David Wells (Chair, ex-Netflix CFO); Kristo Käärmann (CEO); Emmanuel Thomassin (CFO from 1 Oct 2024, after interim Kingsley Kemish and the resignation of Matthew Briers); NEDs Terri Duhon, Clare Gilmartin (Senior Independent Director), Alastair (Alex) Rampell (a16z), Hooi Ling Tan, Ingo Uytdehaage (Audit & Risk Committee Chair), Elizabeth Chambers (Remuneration Committee Chair).

**Committees:** Nomination (Wells), Remuneration (Chambers), Disclosure (Jessica Winter), and a combined Audit & Risk Committee (Uytdehaage). A deep management risk-committee stack sits beneath the board: Group Risk Committee, ALCO, plus Financial Crime, Operational, Regulatory, Credit, Prudential, Market and Liquidity risk committees, and an Emerging Risk Forum, all under a Three-Lines-of-Defence model. Notably, the General Counsel and Chief Risk Officer report to the CTO (not the CEO), and the Global Head of Internal Audit reports to the CFO, with CRO and Internal Audit also reporting jointly to the board for independence.

**Executive pay:** No company-wide annual bonus; heavy equity weighting. The Hybrid LTIP for Executive Directors comprises performance shares (max 325% of salary; measured on relative TSR, volume growth and customer NPS) plus restricted shares (max 325% of salary), with 3-year vesting, 2-year post-vesting holding, and malus/clawback (5 years for EDs, 4 for others). FY2025 aggregate remuneration: Board incl. NEDs £4.65m (9 beneficiaries); Leadership Team (non-board) £9.57m (10); other SMFs/MRTs £2.05m; **total staff remuneration £412.8m across 6,151 beneficiaries.** All permanent staff receive share awards ("Wisers" as owners).

**Revealed priorities (Follow-the-Management).** Capital allocation (≈$470m FY2026 share purchases for the Employee Share Trust plus a planned >$500m programme), relentless direct-rail/licence investment, and continuous price cuts (cross-border take rate fell to ~0.51–0.52%) confirm a genuine volume-and-infrastructure flywheel over near-term margin maximisation — behaviour that matches the stated "mission" rhetoric rather than contradicting it.

### I.5 Legal Architecture

- **Customer contracts by jurisdiction:** UK customers contract with Wise Payments Limited (English law); EEA customers with Wise Europe SA (Belgian law); US customers with Wise US Inc (plus CFSB under a separate Cardholder Agreement); APAC/others with the local licensed entity. The contracting entity is also the entity that owes the customer their balance.
- **Card terms:** In the US, the Wise Multi-Currency Card is issued by CFSB (an FDIC-insured member institution); Wise provides servicing and is a named beneficiary of the agreement. Elsewhere Wise entities issue via card-network membership/BIN sponsorship (Mastercard/Visa).
- **IP / employment / group services:** Software IP is capitalised centrally, though intangibles are modest (£4.0m at FY2025 after most development cost is expensed); the group runs a functional (not divisional) management structure across 30+ offices; intercompany service and cost-allocation arrangements support the licensed entities. Precise transfer-pricing terms are **[UNKNOWN]** from public sources.
- **Litigation/enforcement:** FCA fine of the CEO (£350k, Oct 2024); CFPB order (2025); US six-state AML consent order (Jul 2025); Belgian criminal AML investigation of Wise Europe SA (2026); and a US securities class action (Rosen Law Firm) covering the 11 May–23 Jul 2026 class period, filed after the Belgian disclosure.

**Design logic:** The legal architecture ring-fences each market's customer-money and regulatory liability inside a locally licensed subsidiary while concentrating group capital and technology centrally. This limits contagion (a problem in one market is contained in one entity) but concentrates reputational and financial-crime risk at group level — precisely the fault-line the 2026 Belgian probe exposes.

### I.6 Global Regulatory Map (selected; as of research date)

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

### I.7 Own-Licence vs Partner Dependency Matrix

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

### I.8 Regulation as a Competitive Asset

- **Easy to replicate:** a single MSB registration or one state MTL.
- **Hard but obtainable:** a full EMI (UK) or PI (Belgium) licence with EEA passport; MAS MPI; APRA PPF ADI; Japan Type 1 funds-transfer licence.
- **The real moat — the operating system:** direct settlement participation in national payment systems (being the *first non-bank* into UK FPS, Hungary, and the Japan Zengin/Bank of Japan connection) plus the compliance/treasury operating system to run 80+ licences safely. The 2025–2026 enforcement cluster demonstrates the moat's double edge: the same regulatory density that deters entrants imposes an operating burden that Wise itself has struggled to satisfy. **The moat is real; the operating system to occupy it is the actual bottleneck.**

### I.9 Institutional Dependency Map

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

### I.10 Tax and Intercompany Architecture

- Wise Group plc is **Jersey-incorporated but solely UK tax resident** [CONFIRMED]. This is a listing/redomicile structure for US-market access, not evidence of profit-shifting to a tax haven — profits remain within the UK tax net.
- FY2025 reported PBT was £565m vs underlying PBT £282.1m; a large deferred tax asset (£84.7m at FY2025) is deducted from CET1 because it relies on future profitability. Effective tax rate and granular geographic profit allocation are **[UNKNOWN]** at the level requested; transfer-pricing terms are not public.

### I.11 Corporate and Regulatory Risk

| Risk | Prob. | Severity | Mitigation | Residual |
|---|---|---|---|---|
| AML/sanctions enforcement | High (materialising) | High | Compliance rebuild; SAR lookbacks; ~1/3 staff in financial crime [company claim] | High |
| Belgian criminal probe adverse outcome | Medium | High | Cooperation; localised in Wise Europe SA | Medium-High |
| Partner-bank (CFSB) termination | Low-Med | High | Sought own US charter (denied Jul 2026); alternate sponsors | Medium |
| Licence loss (FCA/NBB) | Low | Severe | Capital surplus (~590%); governance | Low-Med |
| Safeguarding failure | Low | Severe | Segregation; govt securities; new FCA safeguarding rules (May 2026) | Low |
| Governance/founder-control backlash | Medium | Medium | Voting cap; independent NEDs | Medium |
| Capital shortfall | Very low | Severe | £1.29bn CET1 vs £220m requirement | Very low |

### I.12 Reconstruction — Answers to the Completion Test

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

## Recommendations

1. **Treat financial-crime compliance as the gating KPI, not licensing breadth.** The 2025–2026 enforcement cluster (US six-state AML consent order of $4.2m on 9 July 2025; CFPB; Belgian criminal probe; OCC denial citing AML deficiencies) shows the binding constraint. *Benchmark that would change the rating:* an indictment or direct summons of Wise Europe SA in Belgium, or an FCA/NBB remediation escalation, would move the risk rating from High to Severe. Conversely, a clean close of the US SAR lookback (covering closed accounts 1 Mar 2023–1 Mar 2025) and no Belgian charges would de-risk it.
2. **Monitor the CFSB dependency and the second US charter attempt.** If Wise refiles a national trust charter under the GENIUS Act framework and the Fed reopens master-account access for uninsured trusts, US direct-rail independence becomes plausible; continued failure prolongs CFSB concentration risk. *Watch:* Fed's finalised "payment account" policy (proposed May 2026) and any OCC re-engagement.
3. **Track the founder-control cap as the key governance term.** The one-vote-below-50% cap is the single most important governance provision. Any move to remove or extend it, or a Käärmann CEO transition (which drops the cap to below 35%), would materially change the control map and should trigger re-underwriting of governance risk.
4. **Model the rates sensitivity explicitly.** ~$40m of net interest income moves per 25bp of central-bank rate change on ~$26bn of balances — a profitability swing outside management's control and a key variable for any valuation of the FY2027 guidance (net-revenue growth ~mid-15–20% range; income-before-tax margin near the top of 20–25%).

## Caveats
- Some corporate-registry specifics are **[UNKNOWN]** from public sources: the exact Jersey registration number of Wise Group plc; precise transfer-pricing terms; and the granular effective tax rate / geographic profit split.
- The "07209813 vs 13211214" registration-number issue reflects genuine entity-naming complexity (07209813 is Wise Payments Limited's number, also printed on the group MIFIDPRU footer); treat entity-level "Wise" claims with care.
- FY2026 figures are reported on a new US GAAP/USD basis; comparison with prior IFRS/GBP figures requires care. Where this report cites both £ (through FY2025) and $ (FY2026), the currency reflects the reporting basis of the period.
- The Belgian matter is an active criminal investigation of Wise Europe SA with, per Wise, no findings or charges confirmed as of the research date; prosecutors were reported to be finalising a direct summons. Presumption of regularity applies.
- Secondary-source items (e.g., the ~60/40 safeguarding split, some Wise Platform partner counts, "~1/3 of staff in financial crime") are labelled as company claims or third-party estimates and were not all independently reconciled to primary filings.