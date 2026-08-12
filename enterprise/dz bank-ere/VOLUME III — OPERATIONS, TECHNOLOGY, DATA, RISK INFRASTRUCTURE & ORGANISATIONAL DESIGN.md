# VOLUME III — OPERATIONS, TECHNOLOGY, DATA, RISK INFRASTRUCTURE & ORGANISATIONAL DESIGN
## The DZ BANK Group as a Federated Operating Model

---

## TL;DR

- **The DZ BANK Group runs not one operating model but at least seven separately licensed operational stacks** federated under a holding company. Only two systems genuinely span the group: the insourced payments/clearing platform ("ZV ON€", completed October 2024, 11.0bn transactions in FY2025) and the financial-conglomerate risk/finance/regulatory-reporting infrastructure required under §25 FKAG. Everything else — insurance policy administration (R+V), fund accounting (Union Investment), Bauspar contract management (BSH), Pfandbrief cover-pool management (DZ HYP), private-bank/fund services (DZ PRIVATBANK) — is run locally on entity-specific technology.
- **The single most systemically important operation is the payments platform.** DZ BANK is the clearing institution for ~640–700 cooperative banks; a failure would halt payments for a large share of German retail banking. DZ BANK deliberately *insourced* this (an in-house build on SAP-based infrastructure, integration by Capco) while Commerzbank *outsourced* to Worldline — the opposite strategic bet. It is both necessary infrastructure and, increasingly, a genuine competitive asset now being commercialised.
- **The federated structure cannot achieve single-institution efficiency, and is not meant to.** Six supervisory regimes (ECB/SSM, BaFin/Solvency II, KAGB/AIFMD, Bausparkassengesetz, CSSF, and FKAG conglomerate supervision) force duplicated control functions, parallel reporting factories and separate technology estates. The group's 49.3% cost/income ratio is good *for a conglomerate*, but the multi-entity/multi-regime design imposes a structural "conglomerate tax" — most visible in the regulatory-reporting burden — that a monoline would avoid. The offset is earnings diversification and a near-captive cooperative distribution channel.

---

## Key Findings

1. **Operating model = holding company with autonomous, separately regulated operating units, plus two shared group-spanning systems.** DZ BANK AG centralises group finance, group risk, group treasury, group compliance and group audit (the FKAG-mandated conglomerate functions). It does NOT centralise the production engines of its subsidiaries. R+V underwrites and settles claims on its own stack in Wiesbaden; Union Investment runs portfolio management on SimCorp; BSH runs a SAP S/4HANA core; DZ HYP runs its own VR-BaufiConnect lending engine; DZ PRIVATBANK runs OLYMPIC/OLYNEXT on IBM i in Luxembourg. This is a hybrid tilted strongly toward **federation**, not shared services.

2. **The Atruvia boundary is the defining structural fact of the group's technology estate.** Atruvia AG is the IT utility for the ~640–700 *primary* cooperative banks — it runs their core banking (agree21/bank21), the VR Banking App, OnlineBanking and the Omnikanalplattform. DZ BANK holds only ~0.35% of Atruvia and does **not** run its own systems on Atruvia. DZ BANK AG runs its own core banking and general ledger on **SAP / S/4HANA** (with SAP Fioneer), its capital-markets stack on **Murex MX.3**, and its payments on the in-house **ZV ON€** platform. From 1 January 2027, card issuing-processing (debit + credit) moves from VR Payment to Atruvia (Bundeskartellamt case B9-75/26, notified 15 July 2026) — meaning DZ BANK will manufacture card products but not control their processing.

3. **Payments scale is confirmed and rising:** 9.9bn transactions (FY2023) → 10.2bn (FY2024) → **11.0bn (FY2025)** on the single ZV ON€ platform. The build took roughly 500 people, five years and over 100,000 person-days, with a budget in the three-digit millions of euros. Migration of more than 600 cooperative banks completed end-2024 without material public incident.

4. **Risk/finance infrastructure is the second group-spanning system and the largest hidden operational cost driver.** The group must consolidate simultaneously under IFRS (group), HGB (parent), and Solvency II (R+V), then compute a financial-conglomerate coverage ratio under Delegated Regulation (EU) 342/2014 in conjunction with Article 49(1) CRR — because the CRR prudential scope *excludes* insurance and Solvency II covers *only* R+V. This produces an annual §25(3)/(4) FKAG report on top of Pillar 3, SREP/ICAAP/ILAAP, SRB resolution planning, DORA, and the CSSF/BaFin/Bundesbank/ESA reporting stack.

5. **The insurance operation (R+V) is the largest earnings contributor and an entirely different operational discipline** — more than 18,400 employees, ~9m customers, ~26m insured risks, gross written premiums €22.8bn (2025). It restructured its board in 2025 to create a dedicated "Operations und IT" division (Klaus Endres, from 1 April 2025), signalling operational-efficiency pressure under the "NextLevel" strategy, which delivered ~€100m of savings in 2025.

---

## Details

### III.1 The Federated Operating Model

**What it is.** The DZ BANK Group is a financial conglomerate: a central cooperative bank (DZ BANK AG), a composite insurer (R+V), an asset manager (Union Investment/UMH), a Bausparkasse (BSH), a Pfandbrief mortgage bank (DZ HYP), a Luxembourg private bank and fund-services house (DZ PRIVATBANK), a consumer lender (TeamBank) and a small-business finance/leasing company (VR Smart Finanz), plus the payments company VR Payment and specialist units. Each material entity is separately licensed and separately supervised.

**Structure — what is centralised vs local.**

```
DZ BANK AG (holding + operating central institution)
│
├─ CENTRALISED AT PARENT (conglomerate functions):
│   • Group Finance (Konzern-Finanzen): IFRS consolidation, group controlling, group prudential
│   • Group Risk (Konzern-Risikocontrolling / Konzern-Risikosteuerung & Services)
│   • Group Treasury (Liquiditätsausgleichsfunktion for the whole GFG)
│   • Group Compliance / AML / Client Lifecycle Management
│   • Group Audit
│   • Transaction Banking (payments, cards oversight, custody/depositary)
│
├─ ENTITY-LOCAL PRODUCTION ENGINES (run by each subsidiary):
│   • R+V — underwriting, claims, actuarial, investment ops, reinsurance (Wiesbaden)
│   • Union Investment — portfolio mgmt, fund accounting, NAV, admin (Frankfurt/Luxembourg)
│   • BSH — Bauspar contract management, credit servicing (Schwäbisch Hall)
│   • DZ HYP — commercial + retail real-estate lending, cover-pool mgmt (Hamburg/Münster)
│   • DZ PRIVATBANK — private banking + fund services (Luxembourg/Zurich/Stuttgart)
│   • TeamBank — consumer-loan underwriting + easyCredit embedded finance (Nuremberg)
│   • VR Smart Finanz — leasing + express-loan (Eschborn)
│   • VR Payment — card acquiring, POS, terminals (Ilvesheim/Frankfurt)
```

**Direction of travel.** The evidence points to *more* federation of production but *more* centralisation of platforms where scale economics dominate. The clearest signals: (a) DZ BANK insourcing payments into one platform for the whole sector; (b) the 2027 consolidation of card issuing-processing into Atruvia (removing it from DZ BANK/VR Payment); (c) R+V's creation of a combined "Operations und IT" board division; (d) BSH's migration to a single SAP S/4HANA core. Each is a "one platform, run it at scale" move — but the platforms sit in *different* legal entities (DZ BANK for payments, Atruvia for cards, R+V for insurance ops), so the group is federating around several scale centres rather than one.

**Governance model classification (ANALYTICAL INFERENCE):** This is a **holding-company model with autonomous operating units and selective shared platforms** — not a true shared-services model. The unifying glue is (i) the FKAG conglomerate risk/finance spine and (ii) supervisory-board interlock (Riese chairs BSH, R+V, TeamBank, Union Investment; Koch chairs DZ HYP, DZ PRIVATBANK, VR Smart Finanz — established in Volume I).

---

### III.2 Payments, Clearing and Settlement Operations — PRIORITY DEPTH

**The single most systemically important operation in the group.**

#### The insourced platform: "ZV ON€"

- **What it is (CONFIRMED FACT):** DZ BANK's 2024 annual report (DZ BANK AG, HGB accounts, filed to the Bundestag Lobbyregister) states: *"Durch das Projekt „ZV ON€" wurde der gesamte Zahlungsverkehr der Genossenschaftlichen FinanzGruppe auf eine leistungsfähige In-House-Plattform vereint."* It is an **in-house build**, not a packaged vendor product — evolved from the legacy WGZ Bank in-house payments platform inherited in the 2016 merger.
- **Who built it (CONFIRMED FACT):** ~500 people, five years, over 100,000 person-days, per DZ BANK payments head Matthias Ehringer via Payment & Banking: *"Insgesamt etwa 500 Mitarbeiter:innen, fünf Jahre und über 100.000 Arbeitstage brauchte es."* The project effectively began with the 2016 WGZ Bank merger. Systems-integration and IT-strategy partner: **Capco**, whose own case study puts its scope from April 2019 to end-2024, comprising "fünf großen ZV-Migrationen," "97 einzelne Go-Live Events," "63 Projektdrehbücher mit bis zu 1.281 Einzelaktivitäten," and the migration of "Mehr als 600 Banken sowie tausende Firmenkunden." Budget: three-digit-million euros (DZ BANK Group report 2024). Atruvia contributed to the target-picture design.
- **What it replaced:** A split estate — the historical DZ BANK side had partly used Equens/equensWorldline (DZ BANK's payments-processing subsidiary was carved out in 2003 into the Transaktionsinstitut, merged into Equens in 2006; DZ BANK sold its residual equensWorldline stake to Worldline effective 30 September 2019), while the smaller WGZ Bank side processed in-house. The merger forced a single target.
- **Why insourcing (COMPANY CLAIM, Thomas Ullrich, then-Vorstand, Börsen-Zeitung):** *"Während die Commerzbank beim Zahlungsverkehr einen Outsourcing-Ansatz verfolgt, betreibt die DZ Bank ein Insourcing."* The stated rationale (Ehringer): development cost is high but long-term cheaper than per-transaction fees to an external clearing/authorisation provider, given the sector's volume. Strategic goal: become a payment provider not just for the ~700 cooperative institutes but for banks outside the sector, and monetise ("versilbern") the platform.
- **Why delayed one year:** Migration was planned to 2023 but pushed to end-2024 to absorb T2/TARGET2 consolidation, ISO 20022 migration and SEPA-standard changes concurrently.

#### Processing scale and profile

| Metric | FY2023 | FY2024 | FY2025 |
|---|---|---|---|
| Payment transactions (ZV ON€) | 9.9bn | 10.2bn | **11.0bn** |
| H1 transactions | 4.8→5.1bn | 5.1bn | 5.3bn |
| Credit-card transactions | 365.9m | 457.1m | +23% YoY |
| Cards issued | 6.7m | 7.2m | +11% card sales |
| Depositary/custody fund volume | €332.5bn | €369.9bn | €380.7bn |

(CONFIRMED FACT, DZ BANK preliminary-results releases 2024–2026.) Note the definitional perimeter: the figure counts *processed payment transactions on the ZV ON€ platform for the cooperative FinanzGruppe* — i.e. bulk SEPA credit transfers, direct debits, instant payments and cross-border/SWIFT, plus card-scheme messages. It is a throughput count, not a value figure. DZ BANK targets up to **one-third of all German payment traffic** running across the platform.

**Split (ANALYTICAL INFERENCE — the group does not publish a clean breakdown):** The overwhelming majority of the 11.0bn are SEPA bulk (SCT + SDD) processed through the Bundesbank SEPA-Clearer/EMZ; card transactions are a separately-reported and much smaller count (hundreds of millions); instant payments a fast-growing minority; high-value/SWIFT a small count but high value. HYPOTHESIS: SCT+SDD >80% of volume.

#### Rails and gateways (CONFIRMED FACT, from product pages + sector structure)

- **T2/TARGET2:** DZ BANK is a direct T2 participant and settlement-account holder; it provides indirect access and settlement for cooperative banks.
- **SEPA-Clearer/EMZ (Deutsche Bundesbank):** the bulk-file rail; bulk files up to 100,000 items, ~€0.0025/transaction (established Vol II).
- **EBA CLEARING:** STEP2 (bulk SEPA) and RT1 (instant); DZ BANK is a participant.
- **TIPS:** the Eurosystem instant-settlement layer used for SCT Inst.
- **Card schemes:** DZ BANK is a scheme member of Visa and Mastercard; also engaged in EPI/Wero (P2P live July 2024).

#### EU Instant Payments Regulation compliance (CONFIRMED FACT)

The IPR ((EU) 2024/886) imposed: receive instant payments by **9 January 2025**; send instant payments plus Verification of Payee (VoP) by **9 October 2025**; removal of the €100,000 scheme cap. DZ BANK met the deadlines on time — notable given how few European banks were technically ready. Per the Capgemini Research Institute's *World Payments Report 2025* (10 September 2024), *"only 13% of European banks can claim a strong technology foundation for instant payments"* — i.e. roughly 87% lacked a robust instant-payments tech base (EU 13% vs Asia-Pacific 30%, Americas 26%). Ullrich publicly argued for removing the €100,000 cap and for allowing premium pricing on large instant transactions — a revenue concern given the IPR bars charging more for instant than standard SCT.

#### The card operation, pre- and post-1 January 2027 (CONFIRMED FACT)

- **Today:** VR Payment (a DZ BANK subsidiary, ~248 employees, revenue over €200m) is the cooperative sector's full-service acquirer — POS network operation, terminals, card acceptance, e-commerce, plus **issuing-processing** for debit and credit. DZ BANK is the card-issuing bank/scheme member.
- **From 1 January 2027:** Atruvia acquires VR Payment's **issuing-processing** business (Bundeskartellamt B9-75/26, notified 15 July 2026; announced 2 July 2026). Atruvia will run debit + credit issuing-processing on one **integrated card platform** (girocard/debit/credit unified). VR Payment refocuses on **acquiring, POS-network operation and omnichannel merchant solutions**. Dr Imke Jacob (DZ BANK Vorstand Transaction Banking) chairs VR Payment's supervisory board and co-leads the realignment.
- **Operational risk of the migration (ANALYTICAL INFERENCE):** Moving live issuing-processing for a large share of German credit-card transactions onto Atruvia's platform is a high-stakes cutover. Legal counsel (McDermott) publicly noted *"Ein wesentlicher Teil aller Kreditkartentransaktionen in Deutschland wird über die Systeme von Atruvia abgewickelt."* Concentration risk rises: card processing joins core banking under one utility that DZ BANK barely owns.

#### Securities settlement and custody (CONFIRMED FACT)

DZ BANK is the **third-largest depositary (Verwahrstelle) in Germany**, fund volume €380.7bn at end-2025, grown partly by acquisition (e.g. the apoBank depositary business). It connects to Clearstream/T2S for settlement. The Luxembourg fund-services operations sit at Attrax (Union Investment group) and DZ PRIVATBANK/IPConcept. DZ BANK also operates a crypto-securities registrar / crypto-custody capability for institutional clients and is active in DLT-based (blockchain) bond issuance and custody.

**Collateral operations (CONFIRMED FACT, Murex):** DZ BANK processes ~1,400 collateral calls per day across more than 5,400 collateral agreements on Murex MX.3 for Collateral Management (Rüdiger Welsch, head of operations IT, DZ BANK) — one of the largest MX.3 platforms in Central Europe.

---

### III.3 Treasury, Liquidity and Balance-Sheet Operations

**Mandate (CONFIRMED FACT):** DZ BANK's Konzern-Treasury performs the **Liquiditätsausgleichsfunktion** for the entire Genossenschaftliche FinanzGruppe — the daily netting of surplus and deficit liquidity across the cooperative banks — and secures access to money/capital markets and central-bank liquidity. It is the competence centre for unsecured and secured funding.

**How surplus deposits are managed:** The ~640–700 primary banks are structurally deposit-rich (retail funding exceeds local lending). They place surplus liquidity with DZ BANK (the Depot-A relationship), which aggregates and reinvests it and provides refinancing to deficit institutions. DZ BANK thus intermediates the sector's internal balance sheet.

**Systems supporting the primary banks (CONFIRMED FACT):** DZ BANK offers GENO-SAVE and EGon to the cooperative banks for own-account business (Eigengeschäft), regulatory reporting (Meldewesen) and accounting — i.e. DZ BANK is a *provider of treasury/reporting tooling* to the primary banks, not just their counterparty.

**Funding/issuance:** DZ BANK optimises its own funding via securities issuance placed through its own sales and via intermediaries to institutional clients (insurers, funds) in Germany and abroad. DZ HYP runs the Pfandbrief funding operation (incl. Green Pfandbriefe). Under "Verbund First 4.0," DZ BANK expanded a dedicated "Treasury/Refinanzierung" work package.

**ALM relevance:** Net interest income fell 17.8% in FY2025 (established), making interest-rate-risk management and ALM operationally central. Treasury *economics* belong to Volume IV; here the point is operational: intraday liquidity, collateral mobilisation with the Eurosystem (managed on Murex MX.3), and the settlement-account plumbing into T2.

---

### III.4 Technology Architecture — PRIORITY DEPTH, MOST EVIDENCE-CONSTRAINED

#### DZ BANK AG's own core systems (CONFIRMED FACT — resolved)

The open question "who provides DZ BANK's own core banking?" is now answered from DZ BANK's own careers/technology page:

> *"Unter allen deutschen Banken haben wir in der DZ BANK die meisten SAP-Anwendungen im Banking im Einsatz und dabei bauen wir komplett auf S/4 HANA. Angefangen vom SAP Business Partner über das gesamte SAP Core Banking bis zur Aufbereitung und Analyse im SAP BW oder in SAP BO nutzen wir Software vom Marktführer aus Walldorf."*

- **Core banking + general ledger/finance:** **SAP**, standardising on **S/4HANA** (mid-migration from SAP R/3), plus **SAP Fioneer**. SAP BW/BO for analytics/reporting. DZ BANK describes itself as the most SAP-intensive bank in Germany and a "Fast Follower."
- **Capital markets / trading:** **Murex MX.3** (front-to-back, collateral, securities finance) — confirmed by Murex case studies and a third-party integrator noting data feeds "aus dem DZ BANK-Handelssystem Murex."
- **Payments:** in-house **ZV ON€** (see III.2).
- **Integration backbone (CONFIRMED FACT, DZ BANK IT careers):** an **EAI (Enterprise Application Integration) platform** — "eine der größten Plattformen ihrer Art im D-A-CH Raum," with ~500 internal/external applications exchanging data; job scheduling via **Automic Automation Engine**; IT-cost transparency via **Apptio**.

#### Data centres and infrastructure (CONFIRMED FACT, DZ BANK IT careers)

> *"Unsere Systeme betreiben wir selbst in den besten Rechenzentren Frankfurts sowie bei zwei der großen Cloud-Hyperscalern."*

- On-prem data centres in Frankfurt (self-operated); classic virtualised Linux/Windows server estate.
- **Two hyperscalers** used (unnamed publicly); container technologies; a "Virtual Hybrid IT-Infrastructure" model integrating cloud into the on-prem estate. Mainframe/batch legacy retained as an "efficient booking machine in the background" (DZ BANK Innovation LAB, 2020: "intelligenter Rück- und Umbau" of legacy core systems).

#### Subsidiary technology estates

| Entity | Core / production systems | Evidence class |
|---|---|---|
| **R+V** | Bespoke software for the insurance core (Beratung, Verkauf, Bestandsführung, Schaden) **plus** standard software from **Salesforce, SAP, Microsoft, IBM**; new "Operations und IT" board division from April 2025; VR/3D-scan claims tooling ("AssureXR" w/ Fraunhofer IGD) | CONFIRMED (CIO.de; R+V PR) |
| **Union Investment** | **SimCorp** (portfolio/investment management; SimCorp partnership with Quoniam confirmed 2024); **Attrax S.A.** Luxembourg fund-services/brokerage platform (transfer agent, fund administration) | CONFIRMED (SimCorp; Attrax) |
| **BSH** | **SAP S/4HANA** core banking ("NEXT" migration; role-model SAP real-estate-credit standard; migration tooling by paricon; programme support by Wavestone); Bauspar processing being migrated onto SAP progressively | CONFIRMED (Wavestone; paricon; Bank Blog) |
| **DZ HYP** | **VR-BaufiConnect** proprietary processing software behind VR-BaufiComfort; connected to Genopace, Baufinex, Europace and Atruvia Omnikanalplattform; "FK Digital" for corporate-credit digitalisation | CONFIRMED (Börsen-Zeitung; DZ HYP) |
| **DZ PRIVATBANK** | **OLYMPIC / OLYNEXT** core banking (ERI Bancaire) on **IBM Power / IBM i (OS/400)**; Oracle PL/SQL + APEX application landscape; SAP BusinessObjects/Crystal Reports/Tableau for reporting; fund-admin/NAV/TA product **not publicly named** | CONFIRMED core (job ads); fund-admin UNKNOWN |
| **TeamBank** | easyCredit consumer-loan platform + **easyCredit-Ratenkauf / -Rechnung** embedded-finance APIs; merchant plugins (open-source on GitHub, Vue.js transaction manager); CTO Reinhold Rehbichler; more than 2,500 merchant partners | CONFIRMED (TeamBank; GitHub) |
| **VR Payment** | Acquiring/POS/terminal platform; issuing-processing (moving to Atruvia 2027); stake in Wallee | CONFIRMED |
| **VR Smart Finanz** | Leasing + express-loan ("VR Smart flexibel") digital processing | THIN — little published |

#### Engineering practice (CONFIRMED FACT)

DZ BANK IT publicly emphasises agile transformation, container/cloud CI-CD, and dual-study (Wirtschaftsinformatik/Softwaretechnologie) talent pipelines. R+V transformed its IT into an agile organisation under former CIO Tillmann Lukosch (2018–2025). TeamBank publishes open-source merchant SDKs. **Where nothing is published:** the group does not disclose detailed SLOs, deployment frequencies, or internal architecture beyond the above — marked UNKNOWN.

---

### III.5 Build, Buy, Outsource and the Atruvia Boundary

| Capability | Sourcing model | Owner/vendor | Reasoning |
|---|---|---|---|
| Primary-bank core banking + digital channels | **Utility (sector utility)** | **Atruvia** (DZ BANK ~0.35%) | Sector-wide scale; not DZ BANK's to control |
| DZ BANK AG core banking / GL | **Buy + heavy config** | **SAP S/4HANA / Fioneer** | Standard bank-in-a-box; deep SAP investment |
| Capital-markets front-to-back | **Buy** | **Murex MX.3** | Industry standard; one of largest MX.3 in C. Europe |
| Payments processing | **Insourced / build** | **ZV ON€ (in-house)**, Capco integration | Volume economics; strategic control; monetisation |
| Card issuing-processing | **Moving to utility (2027)** | VR Payment → **Atruvia** | Scale consolidation; loss of DZ BANK control |
| Card acquiring / POS | **In-house subsidiary** | **VR Payment** | Merchant-side differentiation |
| Securities settlement/custody | **Build + market infra** | DZ BANK depositary + **Clearstream/T2S** | 3rd-largest German depositary; scale |
| Insurance policy admin/claims | **Build + buy** | R+V bespoke + SAP/Salesforce/IBM | Insurance is a distinct discipline |
| Fund administration/depositary | **Build (entity-local)** | Union Investment + **Attrax**; DZ PRIVATBANK + **IPConcept/OLYMPIC** | Luxembourg regulatory + scale |
| Risk & regulatory reporting | **Build (group)** | DZ BANK Konzern-Finanzen/-Risiko on SAP + EAI | Conglomerate-specific |
| Data & analytics (next-best-action) | **JV** | **Truuco** (DZ BANK/Atruvia JV, live April 2023) | Access to primary-bank data |
| Cloud & infra | **Hybrid** | Own Frankfurt DCs + 2 hyperscalers | Sovereignty + scalability |

**The Atruvia boundary — assessment.** DZ BANK **manufactures** products (payments rails, funds, insurance, loans, cards) but does **not** control the primary banks' digital channel (Atruvia), and from 2027 will **not** control card issuing-processing (Atruvia). This is a structural asymmetry: the group's route to ~30m end customers runs through software it barely owns.

- **Operational control:** Weakened on the customer-facing edge; strong on the manufacturing core (payments, custody, capital markets, insurance, funds).
- **Cost:** Atruvia's utility model spreads IT cost across ~640–700 banks — cheaper than DZ BANK could achieve alone for channel/core — but DZ BANK cannot capture that margin.
- **Strategic optionality:** Reduced. If Atruvia's roadmap diverges from DZ BANK's product ambitions (Wero, Request-to-Pay, digital euro), DZ BANK must negotiate rather than direct. The Truuco JV is the mechanism to regain some data/analytics leverage.
- **Direction (ANALYTICAL INFERENCE):** The group is becoming *more* dependent on Atruvia (channels + core + cards from 2027), not less. This is the single biggest third-party-dependency question in the group.

---

### III.6 Insurance Operations (R+V) — real depth

**Scale (CONFIRMED FACT):** more than 18,400 employees; ~9m customers; ~26m insured risks; gross written premiums €22.8bn (2025); record 2024/2025 group results; the largest segment pre-tax contributor (€2,144m in FY2025).

**Lines:** life, health, property/casualty, motor, accident, legal-protection, credit/surety, and a large agricultural book (R+V is the cooperative sector's agricultural insurer). Composite structure across multiple legal entities: R+V Lebensversicherung AG, R+V Krankenversicherung AG, R+V Allgemeine Versicherung AG, R+V Direktversicherung, KRAVAG (transport/motor for the haulage sector), plus R+V Versicherung AG as group parent and central reinsurer.

**Underwriting & claims operations:** Distribution runs primarily through **more than 13,000 cooperative bank branches** plus R+V's own Außendienst (general agencies and Hauptvertretungen). Claims automation is a "NextLevel" priority — R+V reports two-digit-million-euro savings from AI in advisory, underwriting and fraud detection, and is piloting 3D-scan/VR claims capture ("AssureXR" with Fraunhofer IGD) to cut manual steps in property-damage adjustment.

**Reinsurance (CONFIRMED FACT, SFCR):** R+V Versicherung AG is the **central reinsurer** of the group's primary insurers and independently writes worldwide non-life reinsurance from Wiesbaden (2024 gross written premiums €4,106m at the AG level). This makes R+V one of the few bank-owned groups running a genuine reinsurance operation.

**Investment operation:** R+V runs the group's second-largest balance sheet after the bank; its capital-investment result (R+V Lebensversicherung ordinary investment income above €1.6bn per year) is managed via a Finance/Risk board division (created autumn 2024) and an investment committee. **Signa exposure** was fully written off in R+V's 2023 accounts. R+V CEO Norbert Rollinger stated on 3 April 2024: *"Wir haben das Signa-Engagement in unserem Jahresabschluss 2023 komplett verarbeitet."* The widely-quoted characterisation "robuster dreistelliger Millionenbetrag" in fact originated not with Rollinger but with DZ BANK Co-CEO / R+V supervisory-board chair Cornelius Riese (per procontra). Either way, the episode illustrates how single-name real-estate/private-market exposures are managed through reserving and write-down rather than group contagion.

**Solvency II operations (CONFIRMED FACT):** R+V produces annual SFCRs per legal entity, runs ORSA, and applies transitional measures (§352 VAG Rückstellungstransitional) and the volatility adjustment on the life book. SCR coverage was 168% at end-2024. R+V has a *modified* risk-governance structure reflecting its Solvency II (not CRR) regime — explicitly noted in the group risk report.

**Board restructuring (CONFIRMED FACT):** From 1 April 2025, R+V created a combined **"Operations und IT"** division (Klaus Endres), integrating the former "IT, Digitalisierung und Prozesse" division — a clear operational-efficiency signal. "NextLevel" is a five-year strategy to 2030; an efficiency programme delivered ~€100m savings in 2025.

---

### III.7 Asset-Management Operations (Union Investment) — depth

**Scale:** AuM €534.7bn (retail €270.8bn / institutional €263.8bn); ~4,400 staff; segment pre-tax €1,185m FY2025.

**Portfolio management & trading (CONFIRMED FACT):** Union Investment runs **SimCorp** for investment management; its quant subsidiary **Quoniam** signed a SimCorp partnership in 2024 (AI/ML/big-data systematic investing on SimCorp's platform plus research-cloud). This places Union Investment on the same class of front-to-back IBOR platform used by other large European managers.

**Fund administration & NAV / depositary:** Fund administration and NAV production for the Luxembourg range run through **Union Investment Luxembourg S.A.** (35+ years, one of the most experienced Luxembourg ManCos) and **Attrax Financial Services S.A.** (CSSF-regulated, §24-1/24-2; a "one-stop" fund brokerage, administration and transfer-agency house). The depositary function for German funds is provided by DZ BANK's depositary (see III.2).

**Sustainability data / SFDR classification (CONFIRMED FACT):** Article 8/9 assets reached €153.7bn at end-2025 (from €146.6bn end-2024); an internal "sustainable minimum-standards" figure is separately reported (€127.1bn end-2024). This is a substantial data-operations burden — SFDR classification requires per-instrument ESG data pipelines.

**Distribution operations:** Retail distribution runs through the primary cooperative banks (and BSH's field force for building-society-linked products); institutional client servicing is direct. Programme: "Fit for Future" (efficiency/operating-model).

---

### III.8 Credit, Lending and Real-Estate Operations

**DZ BANK corporate credit & Metakredit (CONFIRMED FACT):** DZ BANK acts *subsidiarily* to the primary banks in corporate lending, and runs the consortium/joint-credit ("Metakredit") model (~€19.3bn, established Vol II) in which DZ BANK and primary banks share exposures. Corporate-credit digitalisation runs under a dedicated programme.

**DZ HYP VR-BaufiComfort — how it works operationally (CONFIRMED FACT):** This is the clearest example of *manufacturing/distribution division of labour* in the group. In the retail model:
1. The Volksbank/Raiffeisenbank adviser handles **customer advice** on the Verbund platforms **Genopace** and **Baufinex** (and, from 2024, Atruvia's Omnikanalplattform).
2. **Without needing a framework contract with DZ HYP**, the adviser submits the application; DZ HYP then **takes over the entire process from application onward** — credit check, approval, and all downstream steps through to disbursement.
3. The technical backbone is DZ HYP's proprietary **VR-BaufiConnect** software, enabling media-break-free data processing from the sales systems and standardised/automated flows that can produce a **credit decision plus contract within 24 hours**. (Context: Bundesbank reported private-construction new business +21.4% to €240.9bn in 2025.)

**Pfandbrief cover-pool management:** DZ HYP manages its Pfandbrief cover pools and reporting (incl. Green Pfandbrief framework), financing portfolio ~€57.6bn (established). VR WERT provides property valuations/appraisals.

**BSH Bauspar contract administration (CONFIRMED FACT):** ~7m contracts on the new **SAP S/4HANA** core ("NEXT" programme; migration tooling by paricon; Wavestone support) — a "role-model" SAP real-estate-credit migration in Germany. The **Baufinex** B2B marketplace (JV with Hypoport) carries more than 8,000 intermediaries and more than 560 product partners; transaction volume +~40% to €8.3bn (established).

**TeamBank easyCredit-Ratenkauf merchant integration (CONFIRMED FACT):** easyCredit-Ratenkauf (€200–€10,000) and easyCredit-Rechnung (€50–€5,000) are embedded-finance/BNPL products with instant online credit checks; TeamBank bears the default risk and pays merchants within ~3 days. Integration via store plugins (JTL, PlentyONE, e-vendo, modified, etc.) and a Vue.js merchant "Transaction Manager" (open-source on GitHub). More than 2,500 cooperative-sector merchant partners; run as a "hochverfügbares System." Loan book €9,132m; ~1.067m customers (established).

**VR Smart Finanz:** leasing and express small-business loans ("VR Smart flexibel"), cost/income 78.6% (established) — the least-automated, thinnest-margin operation; little technology detail published (UNKNOWN).

---

### III.9 Risk, Finance and Regulatory-Reporting Infrastructure — PRIORITY DEPTH

**The second genuinely group-spanning system.**

**The conglomerate aggregation problem (CONFIRMED FACT):** The DZ BANK financial conglomerate = **DZ BANK Institutsgruppe (CRR scope, excludes insurance) + R+V (Solvency II)**. Because no single prudential regime covers both, the group computes a **financial-conglomerate coverage ratio (Bedeckungssatz)** under **Delegated Regulation (EU) 342/2014 in conjunction with Article 49(1) CRR** — the quotient of (sum of eligible own funds) over (sum of solvency requirements) across banking and insurance. BaFin is the conglomerate supervisor (FKAG, in force since 4 July 2013, transposing Directive 2011/89/EU).

- **Coverage at end-2024:** exceeded the external minimum of 100.0%, the internal minimum threshold of 113.0%, and the internal observation threshold.
- **Historical anchor:** end-2020 eligible own funds €35,805m vs requirements €24,516m = 146.0% coverage.
- **Economic vs normative:** the conglomerate coverage and economic capital adequacy are both anchored on Solvency II-style market-consistent valuation (marktnahe Bewertung), so the CRR III transition does not disturb the market-value basis.

**Risk governance (CONFIRMED FACT):** Three-lines-of-defence model; R+V runs a *modified* governance reflecting Solvency II. Central units: **Konzern-Risikocontrolling, Konzern-Risikosteuerung & Services, Konzern-Finanzen**. Group-wide risk reporting across all material risk types is built on prescribed minimum standards and harmonised methods; each Steuerungseinheit's risk-controlling ensures transparency and method currency against DZ BANK-allocated risk capital. Compliance framework reviewed annually; R+V may deviate where special/insurance law requires (documented).

**The reporting factory (ANALYTICAL INFERENCE + CONFIRMED components):** DZ BANK must simultaneously satisfy:
- **ECB/SSM** (banking; P2R 1.80% for 2026, O-SII buffer 1.00%) — SREP, ICAAP, ILAAP, COREP/FINREP, stress tests (the EBA 2025 test confirmed CET1 of 17.9% at H1 2025).
- **BaFin** — conglomerate supervision (§25 FKAG report, around 15 May annually), plus national reporting.
- **Bundesbank** — payment-system and statistical reporting.
- **Solvency II** (R+V) — SFCRs, RSR, ORSA, QRTs.
- **KAGB/UCITS/AIFMD** (Union Investment) — CSSF (Luxembourg) + BaFin.
- **CSSF** — DZ PRIVATBANK, Attrax, IPConcept.
- **SRB** — resolution planning (MREL, resolution reporting).
- **DORA, GwG/AML, MiFID II** — cross-cutting.
- **CRR III** in force from 1 January 2025 (output floor, RWA changes) — a driver of CET1 rising from 15.8% to 18.4%.

Group finance consolidates under **IFRS (group), HGB (parent) and Solvency II (R+V) simultaneously** — three accounting/valuation bases running in parallel on the SAP/BW estate. This triple-basis consolidation is the core operational cost driver of the conglomerate structure.

---

### III.10 Data Architecture and Governance

**The central tension (ANALYTICAL INFERENCE, well-grounded):** The **primary banks own the end-customer relationship and data** (they are the account-holding institutions on Atruvia's core). DZ BANK Group manufactures products but does not own the customer. So how does it get the data to manufacture, price and cross-sell?

- **Truuco (CONFIRMED FACT):** the DZ BANK/Atruvia JV (founded November 2022, live April 2023) provides Smart-Data and next-best-action capability *to the primary banks*. It is the mechanism by which product-relevant signals flow — but the analytics run *for* the primary banks, whose data governance and customer consent gate the flow. Truuco is effectively the group's attempt to build a data capability *on top of* Atruvia's data estate without owning it.
- **GDPR controller/processor allocation (ANALYTICAL INFERENCE):** The primary bank is controller for its customers; Atruvia is processor for core/channel; DZ BANK entities are controllers for their own manufactured products (a fund investor, an insurance policyholder, a Bauspar contract holder become customers of the respective subsidiary). This creates a **fragmented controllership map** — no single group entity is controller for the ~30m end customers.
- **Data warehousing/analytics:** DZ BANK runs SAP BW/BO for finance/risk; a Financial Data Warehouse integrates trading data from Murex. R+V, Union Investment (SFDR ESG data pipelines) and BSH run their own analytics estates. AI/ML: R+V (underwriting/fraud/advisory), Union Investment/Quoniam (systematic investing), DZ BANK (generative-AI work package under Verbund First 4.0).

**Does a group-wide data flywheel exist? (HYPOTHESIS / ANALYTICAL INFERENCE):** No — not a true group flywheel. The relationship-ownership structure of the cooperative model *structurally prevents* a single group data asset. The group has *entity-level* flywheels (Union Investment's fund data, R+V's claims/actuarial data, TeamBank's credit-decision data, DZ BANK's payments data) and a *federated* signal-sharing layer (Truuco), but not the unified customer-360 that an integrated bank or a fintech would build. This is the sharpest data question in the group, and the answer is: the cooperative structure trades data-integration upside for local relationship ownership.

---

### III.11 Cyber, Security and Operational Resilience

**DORA implementation (ANALYTICAL INFERENCE + CONFIRMED regime):** DORA applies across the whole multi-entity, multi-regime group from January 2025. The operational challenge is acute precisely because the group spans banking, insurance and asset-management regimes — the ICT third-party register and critical-third-party identification must span DZ BANK AG, R+V (insurance), Union Investment (AIFMD), and the Luxembourg CSSF entities.

**Critical third parties (ANALYTICAL INFERENCE, well-grounded):**
- **Atruvia** — channels/core for the primary banks; cards from 2027 (the dominant CTP).
- **SAP / SAP Fioneer** — DZ BANK core banking/GL.
- **Murex** — capital markets.
- **ERI Bancaire (OLYMPIC)** — DZ PRIVATBANK core.
- **SimCorp** — Union Investment.
- **IBM** — DZ PRIVATBANK infrastructure (IBM Power/i); R+V software stack.
- **Hyperscalers** (two, unnamed publicly) — DZ BANK cloud.
- **Deutsche Bundesbank (SEPA-Clearer/EMZ, T2), EBA CLEARING (STEP2/RT1), Clearstream/T2S** — market infrastructures.
- **Worldline/equensWorldline** — legacy/residual.

**Concentration risk from single-platform payments (ANALYTICAL INFERENCE):** Consolidating 11bn transactions onto one ZV ON€ platform creates a single point of failure for a large share of German retail payments. DZ BANK's own project lead acknowledged: *"Bei einem Problem im Rahmen der Migration des SEPA-ZV hätte der Zahlungsverkehr in ganz Europa zum Stillstand kommen können."* The mitigation is the platform's design for high availability and the deliberately "geräuschlos" (noiseless) migration, but the structural concentration is real and rising.

**Operational-risk framework:** Managed within the group risk architecture (Pillar 1 op-risk capital under CRR; op-risk is a named risk type in the group risk report). R+V carries op-risk under Solvency II SCR.

**Published incidents:** No major public outage of DZ BANK's own ZV ON€ platform has been reported (the migration was completed without material public disruption). See III.12 for the sector's Atruvia incident record.

---

### III.12 Reliability Engineering and Failure Paths

**Why reliability requirements exceed ordinary enterprise IT:** A clearing failure at DZ BANK would halt payments for a large share of German retail banking (target ~one-third of German traffic). This is systemic infrastructure, not a single bank's back office.

**Availability/SLOs:** DZ BANK does not publish formal SLOs. The design intent is 24/7/365 for instant payments (IPR mandate: settle within 10 seconds). TeamBank describes easyCredit-Ratenkauf as a "hochverfügbares System." Beyond this, published SLOs are UNKNOWN.

**Batch/settlement window as constraint (ANALYTICAL INFERENCE):** Bulk SEPA still runs on batch cycles into the Bundesbank EMZ/SEPA-Clearer with defined cut-offs; instant payments run real-time on TIPS/RT1. The coexistence of batch (legacy mainframe "booking machine") and real-time rails is the core reliability-engineering constraint. Year-end/long-weekend "frozen zones" (no changes during accounting close) are standard sector practice.

**Duplicate-payment prevention:** A named risk during instant/real-time processing; consumer guidance during the July 2026 Atruvia outage explicitly warned users not to re-submit transfers to avoid duplicates — illustrating the failure mode.

**The Atruvia incident record (CONFIRMED FACT) — the relevant contrast:**
- **November 2023:** A central Atruvia software fault caused online-banking/app disruption; per Handelsblatt, *"Potenziell seien bis zu 520 Geldhäuser betroffen … Insgesamt gibt es gut 700 Genossenschaftsbanken, für die Atruvia IT-Dienstleistungen erbringt"* — Volks- und Raiffeisenbanken in southern Germany, with customers unable to make transfers and account information returning error codes.
- **21 July 2026:** Another central-systems fault; per Netzwelt (updated 21 July 2026, 15:28), app and online banking were temporarily shut down to relieve systems and *"waren zwischen 9:47 Uhr und 10:38 Uhr auch die Websites der betroffenen Banken nicht erreichbar"*, with roughly 490 banks affected and the root cause in Atruvia's central systems.

**Assessment — does DZ BANK's ZV ON€ carry comparable concentration risk? (ANALYTICAL INFERENCE):** *Different layer, similar systemic shape.* Atruvia's outages hit the **channel/core** layer (customers can't see or initiate), but payments already submitted still clear. A ZV ON€ failure would hit the **clearing/settlement** layer — potentially more systemic, because it would stop settlement across banks, not just one bank's channel. The two are complementary single-points-of-failure in the cooperative sector: Atruvia = channel/core concentration; DZ BANK ZV ON€ = clearing concentration. Both are consequences of the sector's centralise-for-scale logic. DZ BANK's clean migration record is reassuring, but the tail risk is larger than Atruvia's channel outages.

---

### III.13 Employee Architecture

| Entity | Headcount | Location(s) |
|---|---|---|
| DZ BANK AG / CICB | ~5,981 avg (CICB segment) | Frankfurt HQ + 12 domestic branches; NY, HK, Singapore, London, etc. |
| **R+V** | **more than 18,400** | Wiesbaden (HQ) + Außendienst nationwide |
| Union Investment | ~4,400 | Frankfurt; Luxembourg; Quoniam (Frankfurt) |
| BSH | ~6,700 (of which ~3,200–3,300 field, ~3,300 office) | Schwäbisch Hall |
| DZ HYP | (mid-size; not separately headlined) | Hamburg + Münster (dual HQ) |
| DZ PRIVATBANK | more than 1,200 across 8 sites | Luxembourg, Zurich, Stuttgart + German locations |
| TeamBank | (mid-size) | Nuremberg; Vienna (Austria) |
| VR Smart Finanz | (small) | Eschborn |
| VR Payment | ~248 | Ilvesheim/Frankfurt |
| **Group total (2024, company/Wikipedia)** | **~33,837** | — |

(CONFIRMED FACT where sourced; note the order-of-magnitude point: R+V alone is more than half the group headcount, so "group employees" (~34k) and "DZ BANK AG employees" (~6k) must never be conflated.)

**Skills position (CONFIRMED FACT):** DZ BANK runs dual-study IT pipelines (Fachinformatik, Wirtschaftsinformatik, Softwaretechnologie) and markets SAP/S4HANA, cloud, Murex and agile skills. R+V and Union Investment compete for actuarial and quant/IT talent respectively. IT and actuarial talent are the constrained skills (ANALYTICAL INFERENCE from job-ad volume and the R+V/UMH efficiency programmes).

**Co-determination (ANALYTICAL INFERENCE):** As large German AGs, DZ BANK AG, R+V and the major subsidiaries operate under the Mitbestimmungsgesetz 1976 (parity supervisory boards) with active works councils; Johannes Koch is Arbeitsdirektor at DZ BANK (established Vol I). The Verdi warning-strike at equensWorldline illustrates the sector's active labour relations.

---

### III.14 Organisational Design and Decision Rights

**Holding relationship & board interlock (CONFIRMED FACT, Vol I):** DZ BANK Vorstand members chair the subsidiary supervisory boards — **Riese chairs BSH, R+V, TeamBank, Union Investment; Koch chairs DZ HYP, DZ PRIVATBANK, VR Smart Finanz**. This is the primary mechanism of group control over legally autonomous, separately regulated subsidiaries.

**The four strategic business fields vs legal entities:** The four fields — Privatkundengeschäft, Firmenkundengeschäft, Kapitalmarktgeschäft, Transaction Banking — are *market-facing constructs* that cut across legal entities. Transaction Banking (Dr Imke Jacob) maps mostly to DZ BANK AG + VR Payment; Privatkundengeschäft spans BSH, Union Investment retail, TeamBank, R+V retail and DZ PRIVATBANK; Kapitalmarktgeschäft is DZ BANK AG. The matrix (business field × legal entity × supervisory regime) is the group's core organisational complexity.

**Where real operational power sits (ANALYTICAL INFERENCE):** Formal power sits with each subsidiary's own board (each is separately licensed and its board bears regulatory responsibility). *Actual* influence sits with the DZ BANK Vorstand via (a) supervisory-board chairs, (b) the group risk-capital allocation (each Steuerungseinheit operates within DZ BANK-allocated risk capital), and (c) group treasury's control of sector liquidity. So subsidiaries are operationally autonomous but capital- and liquidity-dependent on the centre — a classic "loose-tight" federation.

---

### III.15 Operating Leverage and Cost Architecture

Administrative expenses €4,804m in FY2025; cost/income 49.3% (established).

| Process | Leverage class | Rationale |
|---|---|---|
| Payments processing (ZV ON€) | **Nearly automatic / strongly sublinear** | 7.5bn→11bn transactions on one platform; marginal cost ≈ €0.0025/transaction; adding volume barely adds cost |
| Securities settlement/custody | **Sublinear** | €332bn→€380bn AuC with scale platform; headcount grows far slower than assets |
| Card acquiring/processing | **Sublinear** (→ step-fixed at 2027 migration) | Scale platform; the Atruvia migration is a step-fixed reset |
| Fund administration (Attrax/UI Lux) | **Sublinear** | NAV production scales with automation, not fund count linearly |
| Insurance claims | **Linear → sublinear** (as automation rises) | Claims volume tracks policies; AI/3D-scan pushing toward sublinear |
| Insurance underwriting (life/health) | **Linear/step-fixed** | Actuarial + advisory headcount-bound |
| Credit processing (DZ HYP VR-BaufiComfort) | **Sublinear** | VR-BaufiConnect automates; 24-hour decisions; volume-sensitive |
| Regulatory reporting (conglomerate) | **Disproportionate / step-fixed** | Each new regime/rule adds fixed cost regardless of volume — the "conglomerate tax" |
| IT development | **Step-fixed** | Platform builds (ZV ON€: 100k+ person-days) are lumpy |
| Distribution support (primary banks) | **Sublinear** | Shared Verbund tooling amortised across ~640–700 banks |

**Where duplication/diseconomy lives (ANALYTICAL INFERENCE):** The multi-entity/multi-regime structure forces **parallel control functions** — each regulated entity needs its own risk, compliance, actuarial/finance, audit and DORA/ICT functions, on top of the group functions. The regulatory-reporting factory (triple accounting basis + six regimes) is the clearest *disproportionate* cost: it grows with regulatory complexity, not with revenue. A monoline of the same size would carry one regime and one reporting stack. **Quantification is not publicly disclosed**, but the structural logic is unambiguous: the conglomerate pays a control/reporting premium in exchange for diversification.

---

### III.16 Operations and Technology as Competitive Advantage

Scoring each on: Proprietary / Hard-to-reproduce / Cost-reducing / Quality-improving / Regulatory-control-improving / Compounds-with-volume.

| Operational asset | Prop. | Hard | Cost↓ | Qual↑ | Reg↑ | Compounds | Verdict |
|---|---|---|---|---|---|---|---|
| **ZV ON€ payments/clearing platform** | ✔ | ✔✔ | ✔✔ | ✔ | ✔ | ✔✔ | **Genuine moat** — proprietary, sector-critical, volume-compounding, now being commercialised |
| Securities/custody scale (3rd-largest DE) | ~ | ✔ | ✔ | ✔ | ✔ | ✔ | Strong scale asset; not unique |
| Insurance underwriting/claims (R+V) | ✔ | ✔ | ✔ | ✔ | ✔ | ~ | Strong but discipline-specific; reproducible by any large insurer |
| Fund-administration scale (UI/Attrax) | ~ | ✔ | ✔ | ✔ | ✔ | ✔ | Scale asset; SimCorp is bought, not proprietary |
| Regulatory-reporting machine | ✔ | ✔✔ | ✗ | ✔ | ✔✔ | ✗ | Hard to reproduce but a *cost*, not a revenue moat — a licence to operate |
| **Cooperative distribution interface** | ✔✔ | ✔✔ | ✔ | ✔ | ~ | ✔ | **Structural moat** — ~640–700 banks, ~30m customers, near-captive; but channel controlled by Atruvia |

**Comparison with the Sparkassen equivalent (CONFIRMED FACT / ANALYTICAL INFERENCE):** The two three-tier sectors are near-mirrors: BVR↔DSGV; DZ BANK↔Landesbanken; Atruvia↔**Finanz Informatik (FI)**; Union Investment↔**DekaBank**. Differences that sharpen the analysis:
- **IT utility:** FI (Sparkassen) runs on OSPlus; Atruvia on agree21/bank21 — both single-core utilities serving hundreds of institutions. Comparable concentration.
- **Payments/cards:** The Sparkassen have the Deutscher Sparkassenverlag/S-Payment and, from 2024, merged Bayern Card Services + PLuscard into **"Qards"** — a card-processing heavyweight. The cooperative side has *no direct equivalent* to the DSV; the 2027 Atruvia card consolidation is partly a catch-up to Qards.
- **Central institution:** The Sparkassen have *multiple* Landesbanken (fragmented); the cooperatives have *one* DZ BANK (consolidated since the 2016 WGZ merger) — a structural efficiency advantage for the cooperatives at the central-institution layer.
- **Asset management:** Union Investment (€534.7bn) vs DekaBank — comparable scale; both sector-captive distribution.

**The DZ BANK payments platform: genuine competitive asset or merely necessary infrastructure? (ANALYTICAL CONCLUSION):** *Both, but tipping toward asset.* It is necessary infrastructure (someone must clear the sector's payments). But the deliberate insourcing decision, the plan to sell processing to banks outside the sector, the on-time IPR compliance when only ~13% of European banks had a strong instant-payments technology foundation, and the ~€3bn of the primary banks' ~€6.5bn commission income that payments now generates, together make it a genuine, hard-to-reproduce, volume-compounding asset — provided DZ BANK can actually win external clients (unproven; COMPANY CLAIM/aspiration, not yet demonstrated at scale).

---

### III.17 Volume III Reconstruction

**(1) Federated Operating-Model Diagram** — see III.1.

**(2) Payments & Clearing Architecture:**
```
Primary banks (agree21/Atruvia) ──files──▶ DZ BANK ZV ON€ platform ──▶ rails:
   • Bundesbank SEPA-Clearer/EMZ (bulk SCT/SDD)
   • EBA CLEARING STEP2 (bulk) / RT1 (instant)
   • TIPS (instant settlement, central-bank money)
   • T2/TARGET2 (high-value/settlement)
   • Visa/Mastercard (cards; issuing-processing → Atruvia 2027)
   • SWIFT (cross-border)
Custody: DZ BANK depositary ──▶ Clearstream/T2S
```

**(3) Treasury/Liquidity Map:** Primary banks' surplus deposits ▶ DZ BANK Konzern-Treasury (Liquiditätsausgleich) ▶ money/capital markets + Eurosystem; DZ HYP Pfandbrief funding; own issuance to institutionals. Collateral on Murex MX.3 (~1,400 calls/day, >5,400 agreements).

**(4) Technology Architecture by entity** — see III.4 table.

**(5) Build/Buy/Outsource + Atruvia boundary** — see III.5 table.

**(6) Insurance Ops Map** — R+V: >13,000 bank branches + Außendienst ▶ underwriting ▶ claims (AI/3D-scan) ▶ investment ops + R+V Re reinsurance ▶ Solvency II/SFCR/ORSA.

**(7) Asset-Mgmt Ops Map** — SimCorp front-to-back ▶ UI Lux/Attrax fund admin/NAV/TA ▶ DZ BANK depositary ▶ SFDR ESG data pipelines.

**(8) Credit/Real-Estate Ops Map** — DZ HYP VR-BaufiConnect (advice at primary bank, processing at DZ HYP); BSH SAP S/4HANA + Baufinex; TeamBank easyCredit APIs.

**(9) Risk/Finance/Reg-Reporting Architecture** — FKAG conglomerate coverage (Reg 342/2014 + Art 49(1) CRR); triple consolidation (IFRS/HGB/Solvency II); six-regime reporting factory.

**(10) Data Governance Model** — fragmented controllership; primary banks own customer; Truuco JV signal-sharing; no group flywheel.

**(11) Security/Resilience Map** — DORA across regimes; CTPs led by Atruvia, SAP, Murex, IBM, ERI, hyperscalers, Bundesbank/EBA CLEARING/Clearstream.

**(12) Incident Record:**

| Date | System | Scope | Cause | Lesson |
|---|---|---|---|---|
| Nov 2023 | Atruvia core/channel | up to 520 of ~700 banks | central software fault | channel concentration |
| 21 Jul 2026 | Atruvia core/channel | ~490 banks (09:47–10:38) | central-systems fault | channel concentration; duplicate-payment risk |
| End-2024 | DZ BANK ZV ON€ migration | >600 banks migrated | (planned) | clean cutover, no material outage |
| (ongoing) | equensWorldline | Verdi warning strikes | labour | legacy vendor instability |

**(13) Employee & Entity Map** — see III.13.

**(14) Decision-Rights Map** — supervisory-board interlock + risk-capital allocation + treasury control = loose-tight federation.

**(15) Operating-Leverage Matrix** — see III.15.

**(16) Operations Moat Assessment** — see III.16.

**(17) Key Unknowns:**
- DZ PRIVATBANK's specific fund-admin/NAV/transfer-agency software product (UNKNOWN — not published; only OLYMPIC/OLYNEXT core confirmed).
- DZ BANK's formal availability SLOs and DR/RTO/RPO targets (UNKNOWN).
- The precise SCT/SDD/instant/card/high-value split of the 11.0bn (UNKNOWN — only card sub-count published).
- Whether Cofinpro (vs the confirmed Capco) had a role in ZV ON€ (UNKNOWN).
- The two named hyperscalers DZ BANK uses (UNKNOWN — described only as "two of the big hyperscalers").
- Quantified cost of the conglomerate/multi-regime duplication (UNKNOWN — not disclosed).
- VR Smart Finanz technology stack (thin/UNKNOWN).

**(18) Ten Most Important Conclusions:**
1. Two systems truly span the group — ZV ON€ payments and the FKAG risk/finance spine; everything else is entity-local.
2. DZ BANK AG runs its *own* SAP S/4HANA core + Murex + ZV ON€ — it is NOT an Atruvia customer for its own systems; Atruvia serves the primary banks.
3. Payments is the most systemically critical operation and a genuine, hard-to-reproduce, volume-compounding asset — the group bet against the outsourcing trend and won on resilience (on-time IPR while only ~13% of European banks had a strong instant-payments tech base).
4. The group is becoming *more* dependent on Atruvia (channels + core + cards from 2027), an entity it owns ~0.35% of — the biggest third-party-dependency question.
5. The conglomerate must consolidate under three accounting bases (IFRS/HGB/Solvency II) and report to six regimes — a disproportionate, volume-insensitive "conglomerate tax."
6. R+V is the largest earnings contributor and a wholly different operational discipline (incl. a real reinsurance operation); its 2025 board restructuring signals efficiency pressure.
7. The cooperative model structurally prevents a single group data flywheel — the primary banks own the customer; Truuco is a federated work-around.
8. Operating leverage is excellent in payments/custody/fund-admin (sublinear) but poor in regulatory reporting (disproportionate) and headcount-bound in insurance underwriting.
9. The Sparkassen mirror (FI/Deka/Qards) shows the cooperatives are ahead at the *central-institution* layer (one DZ BANK vs many Landesbanken) but were behind in *card processing* until the 2027 Atruvia consolidation.
10. A federated group under six regimes **cannot** match a single integrated institution's operational efficiency — the structure costs a permanent control/reporting premium and forgoes a unified data asset; it buys diversification, a near-captive channel, and per-platform scale in exchange.

**Answers to the closing questions:**
- **Most critical subsystem to the group and to German banking:** the ZV ON€ payments/clearing platform (systemic for a large share of German payments) — with the FKAG risk spine most critical to the *group's* licence to operate.
- **Hardest to replicate:** the cooperative distribution interface + the ZV ON€ clearing role (both structural, decades in the making).
- **Scales best:** payments, custody and fund administration (sublinear/near-automatic). **Requires headcount to keep growing:** insurance underwriting/claims and regulatory reporting.
- **Most dependent on third parties/institutions:** Atruvia (channels/core/cards), then SAP, Murex, ERI, IBM, SimCorp and the market infrastructures (Bundesbank, EBA CLEARING, Clearstream).
- **Does federation create advantage or duplication:** both — advantage via diversification, per-platform scale and near-captive distribution; duplication via parallel control/reporting functions across six regimes.
- **Payments platform — asset or infrastructure:** necessary infrastructure that has been engineered into a genuine competitive asset, contingent on winning external clients.
- **Central question — can a federated group under six regimes match a single integrated institution's efficiency:** **No.** It carries a permanent structural premium (triple accounting basis, six-regime reporting factory, duplicated control functions, no unified data asset). What that structure *costs* is a control/reporting/coordination overhead that a monoline avoids; what it *buys* is earnings diversification (R+V's €2.1bn cushioning bank-cycle troughs), a near-captive ~30m-customer channel, and scale platforms (payments, custody, funds) each run at sector scale. The 49.3% cost/income ratio shows the trade is being managed well — but the conglomerate tax is real and permanent.

---

## Recommendations

**For an analyst/counterparty assessing the group:**
1. **Treat ZV ON€ concentration as the top operational-risk item.** Benchmark: any published ZV ON€ outage affecting settlement (not just channel) would be a materially worse signal than an Atruvia channel outage. Watch for DZ BANK disclosing formal availability SLOs or a DR site — continued absence is a (mild) red flag.
2. **Track the 1 January 2027 Atruvia card-processing cutover as a discrete event risk.** Benchmark: a clean cutover (as with ZV ON€ in 2024) confirms the sector's migration competence; any disruption to credit-card processing would be systemic given Atruvia processes "a significant portion of all German credit-card transactions." Re-rate operational risk if the cutover slips or fails.
3. **Model the conglomerate-reporting cost as a permanent fixed overhead**, not a variable cost — it will rise with each new regime (DORA, CRR III phase-ins, Solvency II review) regardless of revenue. Benchmark: cost/income drifting above ~52–53% without a revenue explanation would suggest the regulatory/control base is outpacing operating leverage.
4. **Monitor whether DZ BANK wins external (non-cooperative) payments clients.** This is the swing factor that converts ZV ON€ from "necessary cost" to "growth asset." Benchmark: named external bank clients on ZV ON€ would validate the "payment provider for banks outside the sector" thesis (currently aspiration).

**For the group itself (implied by the analysis):**
5. Reduce Atruvia single-point-of-failure exposure at the channel layer (the 2023/2026 outages are a pattern, not one-offs) — but this is largely outside DZ BANK's control given ~0.35% ownership; the lever is governance influence and the Truuco data layer.
6. Publish more operational transparency (SLOs, DR posture, the payments split) — the current opacity forces analysts to infer, which understates a genuinely strong payments operation.

**Thresholds that would change these recommendations:** a ZV ON€ settlement-layer outage; a failed/delayed 2027 card cutover; cost/income breaching ~53%; or, positively, the signing of named external ZV ON€ clients or the publication of formal resilience SLOs.

---

## Caveats

- **Evidence asymmetry:** As warned, DZ BANK publishes far less about internals than a fintech would. The richest technology evidence came from job advertisements (DZ BANK IT careers: EAI, Automic, Apptio, SAP S/4HANA, hyperscalers; DZ PRIVATBANK: OLYMPIC/OLYNEXT on IBM i), vendor case studies (Murex MX.3; SimCorp/Quoniam; Wavestone/paricon for BSH SAP; Capco for ZV ON€) and specialist press. These are reliable but not audited disclosures.
- **The payments split (SCT/SDD/instant/card/high-value) is inferred, not published** — only the card sub-count is disclosed.
- **"ZV ON€" is confirmed as an in-house build; no underlying commercial payments engine is named** — do not attribute a specific vendor product to it. Capco is confirmed as integration partner (scope April 2019–end-2024, 97 go-live events, >600 banks migrated); Cofinpro's involvement is unconfirmed.
- **DZ PRIVATBANK's fund-administration/NAV/transfer-agency software product is UNKNOWN** — only the OLYMPIC/OLYNEXT core-banking system (ERI Bancaire, on IBM Power/i) is confirmed, from the bank's own IT recruitment postings.
- **The Signa write-off characterisation was mis-attributed in the carried-forward context.** R+V CEO Rollinger's own 3 April 2024 statement was that the Signa engagement was fully processed in the 2023 accounts; the phrase "robuster dreistelliger Millionenbetrag" traces to DZ BANK Co-CEO Cornelius Riese, not Rollinger. Both confirm a full write-off in FY2023.
- **Headcount figures mix reporting bases** (segment averages vs entity totals vs group). The ~33,837 group figure (2024) and R+V's more-than-18,400 are from company/Wikipedia sources; treat the group total as approximate and never conflate perimeters (DZ BANK AG ~6k vs group ~34k).
- **Forward-looking items** (2027 card migration, external ZV ON€ client ambitions, "NextLevel"/"Fit for Future" savings targets) are plans/claims, not accomplished facts, and are labelled as such.
- **Perimeter discipline:** figures are for the DZ BANK Group (IFRS) or the named entity; the ~€1.175trn Genossenschaftliche FinanzGruppe aggregate is the *sector*, NOT DZ BANK; the CRR prudential scope excludes insurance; and the erroneous "DZ BANK holds ~20% of Atruvia" claim must not be propagated (it holds ~0.35%; the ~20% figure refers to Verimi).

---

*End of Volume III. Work paused at a logical boundary; Volume IV (economics, capital, profitability, strategy) not begun, per scope.*