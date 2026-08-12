# ATRUVIA AG — Enterprise Reverse-Engineering Framework (EREF), VOLUME I: Corporate, Legal, Regulatory & Institutional Anatomy

*Research date: 8 August 2026. Subject legal entity: Atruvia AG, HRB 102381, Amtsgericht Frankfurt am Main; administrative seats Karlsruhe (Fiduciastraße 20, 76227) and Münster (GAD-Str. 2–6, 48163); further offices Munich, Frankfurt, Berlin. VAT ID DE143582320. Share capital €115.8m. Standing house standard applied throughout; evidence labels used for material claims.*

---

## TL;DR
- **Atruvia is a non-listed, non-bank Aktiengesellschaft that is the captive core-banking IT provider for essentially the entire German cooperative banking sector** — the 646 Volksbanken, Raiffeisenbanken, Sparda-Banken, PSD-Banken and other cooperative banks that existed at year-end 2025 (per BVR), plus numerous private banks and the ADAC — and it is owned ~99.7% by cooperative entities, overwhelmingly (91.6% of share capital) through three regional holding KGs pooled into VR-FGI Beteiligungsholding GmbH & Co. KG. **Actual control sits with the member banks acting collectively through this pooling vehicle, not with any single institution; DZ Bank does NOT own a controlling stake.**
- **The single most important current regulatory fact:** on the European Supervisory Authorities' first CTPP list (published 18 November 2025, 19 providers), **Atruvia was NOT designated a Critical ICT Third-Party Provider under DORA — but IBM, on whom Atruvia is deeply dependent (IBM Z mainframes running agree21), WAS.** Atruvia is instead supervised *indirectly*, via the §25b KWG / MaRisk AT 9 outsourcing regime imposed on its bank customers and via direct BaFin §44 KWG inspections (one begun November 2023).
- **The deepest dependency is IBM (a mainframe monoculture); the hardest-to-recreate asset is the agree21 single core platform** running ~800 banks and tens of millions of accounts after the "moon-landing" migration completed in 2019/2020; and **the most misunderstood feature is the customer-owner identity**, which suppresses pricing pressure and external accountability while creating near-insurmountable lock-in.

---

## Key Findings
1. **Origin.** Atruvia traces to the Fiducia Revisions- und Treuhand-Institut AG, founded in Karlsruhe on **13 November 1924**. The Tracxn/PitchBook claim that Atruvia was "founded in 1924 by Martin Beyer" is **erroneous data** — Beyer is a former executive (2013–2025), not a 1924 founder. The modern entity was created by the 2015 merger of Fiducia IT AG (Karlsruhe, south) and GAD eG (Münster, north), renamed Atruvia AG on **1 September 2021**.
2. **Ownership.** 91.63% of Atruvia's €115.8m share capital is held by three regional Beteiligungsgesellschaften pooled through **VR-FGI Beteiligungsholding GmbH & Co. KG**; 6.71% by primary banks directly; ~1% other cooperative entities; 0.32% private banks. Total cooperative ownership 99.68%.
3. **Governance.** German two-tier board; a five-member Vorstand as of January 2026 led by Ulrich Coenen (sole spokesman since July 2025 after Martin Beyer's departure); a **20-member co-determined Aufsichtsrat under the Mitbestimmungsgesetz 1976 (10 shareholder, 10 employee representatives)**, chaired by Daniel Keller.
4. **Regulation.** Not a licensed bank; regulated indirectly through customers' outsourcing obligations (§25b KWG, MaRisk AT 9, BAIT), subject to DORA as an ICT third-party provider (contractually) but **not (yet) as a designated CTPP**, and underwent a BaFin §44 KWG special inspection begun November 2023.
5. **Capability vs dependency.** Atruvia owns and operates the agree21 core platform and its data centres but is strategically dependent on IBM for mainframe hardware/software (a multi-year deal signed **19 November 2025** built on the IBM z17); the subsidiary Ratiodata SE supplies and services the >30,000-device self-service/ATM network.
6. **Payments expansion.** On **2 July 2026** Atruvia agreed to acquire VR Payment's **Issuing-Processing** business (effective 1 January 2027; Bundeskartellamt filing 15 July 2026, case B9-75/26), consolidating debit AND credit card processing under Atruvia and turning it into a card "powerhouse."

---

## Details

### I.1 Origin and Corporate History

**The fragmented origins (1924–2000s).** Two lineages converged into today's Atruvia:

- **Southern lineage (Fiducia).** The Fiducia Revisions- und Treuhand-Institut AG was founded in Karlsruhe on **13 November 1924** [CONFIRMED FACT — Atruvia's own 100-year press release, 11 November 2024]. From 1958 the idea of a shared *Buchungsgemeinschaft* (booking cooperative) emerged among the banks it served; the Zentralkasse südwestdeutscher Volksbanken commissioned Fiducia to build it. By year-end 1963, 67 Volksbanks were partners; 47 staff processed 22 million booking items (against Atruvia's 8.2bn+ today). Fiducia then consolidated regional computing centres through successive mergers: with GRK Genossenschaftliches Rechenzentrum Kassel (1999) and RWG Rechenzentrale Württembergischer Genossenschaften Stuttgart (2001, forming Fiducia AG Karlsruhe/Stuttgart), then with rbg Rechenzentrale Bayerischer Genossenschaften (2003, forming **Fiducia IT AG**). Its core system **agree** (v1.0, 2003) unified the predecessor systems GEBOS (RWG), GENOS (rbg) and RUBIN (GRK), built atop Fiducia's earlier NBS system.
- **Northern lineage (GAD).** The Gesellschaft für automatische Datenverarbeitung (GAD) was founded in Münster on **26 December 1963** as the first cooperative computing centre in north-west Germany, with 23 employees; converted from GmbH to a registered cooperative (eG) in 1966 (30m booking items that year). In 1971 the Rechenzentrale der westdeutschen Volksbanken was absorbed. Its core system **bank21** replaced predecessor BB3 across all GAD member banks by 2007.

**Failed and successful merger (2013–2015).** Earlier merger talks failed (a 2012 attempt "geplatzt," per WirtschaftsWoche). Talks resumed late 2013; the supervisory boards of both firms assented unanimously in early October 2014. The **GAD Generalversammlung approved on 26 November 2014 with 94%**; the **Fiducia extraordinary Hauptversammlung approved on 4 December 2014 with 100%** [CONFIRMED FACT]. The Verschmelzungsvertrag is dated 4 December 2014; the new entity, **Fiducia & GAD IT AG**, was registered at Amtsgericht Frankfurt am Main on 10 June 2015, and the merger became legally effective **1 July 2015** (some sources cite economic effect from 1 January 2015). At formation it had ~5,500–5,600 staff, ~€1.2–1.26bn group revenue, and served all ~1,100 German cooperative banks.

*Structural consequence:* the merger created a two-platform problem (agree south, bank21 north) that dictated the next five years of strategy and created deep path dependency, a north-south organisational fault line, and the dual Karlsruhe/Münster administrative seats that persist today.

**The agree21 migration — "the moon landing" (2016–2020).** Rather than maintain two cores, management chose to consolidate onto **agree21** (based on agree, extended with bank21 components). Series migration of the former GAD banks began February 2017; the series migration completed **9 November 2019**, with all 341 remaining banks (reduced from ~400 by intervening bank mergers) migrated; six special institutions followed through 2020. Scope: ~60,000 bank workstations, 13,000 self-service terminals, ~21.5 million accounts and 22 terabytes of data across 60 series migrations [CONFIRMED FACT — Atruvia press release, 17 February 2020]. Management reported the programme was **delivered on time and on budget**, targeting **~€125m/year in synergies from end-2020** passed to member banks via cost reductions [COMPANY CLAIM — no independent audit of total programme cost or overruns is public; the €125m figure was announced at the 2014/15 merger and repeated at completion]. Contemporary trade press ("Mondlandung"/"the largest cooperative IT transformation of all time") corroborates the scale and on-time completion, but not the cost claim independently.

**Rebrand (2021).** On **1 September 2021** Fiducia & GAD IT AG became **Atruvia AG** (Handelsregister change registered 31 August 2021; Hauptversammlung resolution 30 June 2021). The name was developed by a naming agency; the stated rationale was signalling completion of post-merger integration and a repositioning "from IT service provider to digitalisation partner" [COMPANY CLAIM]. Note the causal chain: the rebrand deliberately followed the migration's completion, so that a single unified platform preceded a single unified brand.

**Strategic programmes since:** the BVR "KundenFokus" verbund project; the EGP Gesamtbanksteuerungssysteme regulatory-software platform (later merged up into Atruvia — the KG was deleted from the register on 19 September 2023 by *Anwachsung*); the M365/Microsoft rollout; a cost-and-efficiency programme; and the "audIT" remediation programme (completed 31 December 2021) that closed out findings from an earlier BaFin process.

**VR Payment acquisition (2026).** On **2 July 2026** Atruvia, DZ Bank and VR Payment announced Atruvia's acquisition of VR Payment's **Issuing-Processing** business, effective **1 January 2027**. The Bundeskartellamt merger-control filing was made **15 July 2026** (case B9-75/26, product markets "Finanzdienstleistungen, Zahlungsabwicklungsdienste") [CONFIRMED FACT]. Atruvia will process debit AND credit cards (credit processing previously sat with VR Payment) on an integrated card platform built with DZ Bank; VR Payment refocuses on acquiring, POS network operation and merchant/omnichannel solutions. Digital Banking board member Željko Kaurin: *"Mit der Bündelung des Issuing Processing führen wir bestehende Stärken in der genossenschaftlichen FinanzGruppe gezielt zusammen."* Legal adviser to Atruvia: McDermott Will & Schulte (Dr. Christian Marzlin, Dr. Philipp Grenzebach). Marzlin (verbatim): *"Ein wesentlicher Teil aller Kreditkartentransaktionen in Deutschland wird über die Systeme von Atruvia abgewickelt … Die Neuordnung des Kartengeschäfts zwischen Atruvia und DZ Bank hat deshalb große Bedeutung für die deutsche Finanz- und Bankenwelt."* Purchase price not disclosed [UNKNOWN]. Rationale: consolidate duplicate structures, integrate account+card at Atruvia, respond to fintech competition and rising payment volumes/regulation.

### I.2 Corporate Group Structure

Atruvia AG is the group parent. Northdata's consolidated filings historically show ~24–31 shareholdings (31 companies in the 2015 consolidated report; ~28 in the 2023 report). Material operating subsidiaries and participations (FY2024 figures from Atruvia's subsidiary report unless noted):

| Entity | Function | Employees | Revenue (FY2024) | Notes |
|---|---|---|---|---|
| **Ratiodata SE** (Frankfurt/Münster) | Systems house: IT hardware, managed field/campus services, self-service (ATM/SB) systems, scan/document services | 1,426 | €344.5m | Largest subsidiary; >50 yrs; absorbed GWS hardware business June 2024; Beyer was AR chair from July 2024 |
| **parcIT GmbH** (Cologne) | Bank steering & risk software (VR-Control/okular) | 507 | €78.6m | In group since 2009 |
| **BMS Corporate Solutions** | Corporate-client (Firmenkunden) digitalisation, data analytics, fincompare | 303 | €52.0m | Core business field of Atruvia |
| **Peras GmbH** | HR services/payroll (geno.HR), HR BPO | 290 | €46.7m | HR partner |
| **Serviscope AG** | Business process outsourcing (omnichannel, 24/7) for 350+ banks | 451 | €28.8m | Sole owner of SDT since Aug 2024; SERVODATA subsidiary runs the 116 116 card-blocking hotline |
| **Accesa (IT Group GmbH)** (Cluj-Napoca, RO) | Nearshore software development / managed services | 1,090+ | n/a | Spun out of Ratiodata to Atruvia AG eff. 1 Jan 2024 |
| **Ratiodata Romania (RaRo)** | Nearshore | n/a | n/a | Spun out of Ratiodata to Atruvia AG eff. 1 Jan 2024 |
| **ECON Application GmbH** | No-code application/forms software | 35 | €4.1m | Acquired 2023 |
| **FORUM Ges. f. Informationssicherheit** | GRC / DORA / IT-regulatory software (ForumSuite) | 20 | €3.6m | Serves ~700 banks |
| **TRUUCO GmbH** | Data-driven sales AI | 58 | €8.2m | JV with DZ Bank & Bausparkasse Schwäbisch Hall; loss-making (−€7.98m) |
| **GWS mbH** (Münster) | ERP/cloud for wholesale/retail trade | ~670 (mid-2024) | n/a | Now cloud-only after ceding hardware to Ratiodata |

Minority participations/JVs: **Verimi GmbH** (digital identity; after the 2022 yes/Verimi merger, Atruvia + DZ Bank together ~18–20%); **amberra GmbH** (non-core banking ecosystem, with DZ Bank & BVR). Dissolved/merged-up: **EGP Gesamtbanksteuerungssysteme GmbH & Co. KG** (deregistered 19 September 2023).

**Why the entities exist (structure-flow-control-economics-risk):** (a) *historical merger path dependence* (Ratiodata, GWS, GAD-legacy vehicles); (b) *labour-law / tariff separation* (BPO in Serviscope, HR in Peras); (c) *regulatory specialisation* (parcIT for risk models, FORUM for GRC/DORA software); (d) *nearshore cost/skills arbitrage* (Accesa/RaRo in Romania); (e) *tax/holding convenience* (the Verwaltungs-GmbH complementary entities). Entity separation reflects a mix of merger history and functional specialisation far more than tax optimisation. Atruvia is explicitly deduplicating overlapping subsidiary business models (e.g. the June 2024 GWS→Ratiodata hardware transfer) — a control lever the group exercises through its Beteiligungsausschuss.

*Simplified economically-important tree:* **Atruvia AG** → {Ratiodata SE (infrastructure/hardware/SB), parcIT (risk software), BMS CS (corporate banking), Serviscope (BPO), Peras (HR), Accesa/RaRo (nearshore dev)}; the remainder are small software or JV vehicles.

### I.3 Ownership and Control (GIVEN UNUSUAL WEIGHT)

**The cascade.** ~800 member banks → three regional holding KGs → **VR-FGI Beteiligungsholding GmbH & Co. KG** → **Atruvia AG**. Member banks became limited partners (Kommanditisten) of the regional KGs by contributing (*einbringen*) their Atruvia shares; the regional KGs pool their stakes through VR-FGI, which votes the block. Atruvia shares were contributed into VR-FGI on **23 November 2018**.

**The vehicles [CONFIRMED FACT — Handelsregister/Northdata]:**
- **VR-FGI Beteiligungsholding GmbH & Co. KG** — Neu-Isenburg, Amtsgericht Offenbach am Main **HRA 42595**; general partner **VR-FGI Verwaltungs GmbH**. Top pooling vehicle; corporate purpose: acquisition and management of direct and indirect participations in (former) Fiducia & GAD IT AG / Atruvia AG.
- **Atruvia Beteiligungs-GmbH & Co. KG Baden-Württemberg** — Stuttgart, **HRA 720090** (formerly FAG Beteiligungs-GmbH & Co. KG BW); GP now DZA Verwaltungs-GmbH Baden-Württemberg.
- **Atruvia Beteiligungs GmbH & Co. KG Nord** — Münster, **HRA 10029** (formerly GAD Beteiligungs GmbH & Co. KG); GP Atruvia Verwaltungs GmbH Nord (HRB 15398). **DZ Bank AG is listed as a limited partner here.**
- **Bayerische Beteiligungsgesellschaft an der Atruvia AG GmbH & Co. KG (BBA)** — Beilngries, Amtsgericht Ingolstadt **HRA 2070**; GP GVB Verwaltungsgesellschaft mbH (a subsidiary of Genossenschaftsverband Bayern). BBA holds **14.15% of Atruvia's share capital indirectly via VR-FGI** [CONFIRMED FACT — bbakg.de]; founded 22 November 2007; 216 Kommanditisten as of 30 September 2021.

**Economic ownership (Atruvia's most recent published "Nominalkapital in %" table, as of Aug 2026):** Beteiligungsgesellschaften **91.63%**; Primärbanken **6.71%**; Zentralbank (DZ Bank) **0.35%**; other cooperative entities ~1.0% combined (sonstige genossenschaftliche Gesellschaften 0.86%, gewerbliche Warengenossenschaften 0.13%, etc.); Privatbanken **0.32%**. **Total cooperative 99.68%.** Share capital €115.8m [CONFIRMED FACT].

**Separating economic ownership from voting control.** Economic ownership is highly fragmented across ~800 banks. Voting control, however, is *concentrated by the pooling structure*: VR-FGI votes ~91.6% of the shares as a single block, and the three regional KGs coordinate through it. BBA's own guidelines describe the arrangement as bundling member interests "in one company" and state that "die Bündelung der Aktionärsinteressen setzt Konsens über die gemeinsamen strategischen Ziele voraus" ("bundling of shareholder interests presupposes consensus on common strategic goals").

**Who actually controls Atruvia?** The member banks collectively, acting through the pooling vehicles and BVR-coordinated cooperative-sector consensus. No single member bank has a controlling stake; the largest disclosed block is Bavaria's 14.15%. **DZ Bank — the sector's central institution — does NOT control Atruvia; the widely-cited "DZ Bank ~20%" figure refers to Verimi, not Atruvia** [ANALYTICAL INFERENCE, corroborated: DZ Bank appears only as a minor LP in the Nord KG and holds ~0.35% "Zentralbank" directly]. Management can be removed by the Aufsichtsrat, whose shareholder bench is elected by the Hauptversammlung (i.e. ultimately the member banks via VR-FGI). A coordinated bloc of member banks could therefore force strategic change — but the pooling structure and consensus requirement make unilateral action by any faction difficult.

**Conflicts (the analytically interesting core):**
- *North (ex-GAD) vs South (ex-Fiducia):* institutionalised in the separate Nord vs Baden-Württemberg/Bayern KGs and the dual seats. The agree21 decision (the south's platform prevailed; bank21 was retired) was a durable source of northern grievance.
- *Large vs small banks:* large banks want bespoke functionality and faster modernisation; small banks want low, stable, standardised pricing. The pooled, capital-weighted-within-KG structure protects the collective, though the exact per-share vs per-member voting rule within the pool could not be confirmed from an accessible primary document [UNKNOWN].
- *Owner vs customer — THE central governance fact.* Member banks are simultaneously shareholders (wanting dividends and low investment) and customers (wanting low prices and high service). This dual identity suppresses arm's-length pricing pressure, mutes accountability (no external shareholders demanding returns; no analysts; no listing), and can produce under-investment — but it also aligns the supplier's incentives with the sector's survival and guarantees captive demand. The consequences run through pricing (historically cost-plus "Basispaket"; a shift to usage-based pricing was signalled in 2024), investment (large programmes require member consensus), and accountability (discipline comes from internal governance, not markets).

### I.4 Governance Architecture

**Vorstand (management board) — 5 members; "Zielbild" complete as of 1 January 2026:**

| Member | Ressort | Since | Prior experience |
|---|---|---|---|
| **Ulrich Coenen** (Vorstandssprecher) | Corporate Strategy & Development | co-spokesman from 2021; **sole spokesman from July 2025** | long-serving Fiducia/F&G executive |
| **Daniela Bücker** | Core Banking & Technology | 2020 | technical continuity |
| **Julia Japec** | Customer Success (sales) | 1 May 2025 (succeeded Ralf Teufel) | joined from Commerzbank 2022 |
| **Željko Kaurin** | Digital Banking | 1 November 2025 | ex-COO Barclays Bank Europe; 20+ yrs ING-DiBa |
| **Dr. Markus Wiegelmann** | Finance, Regulation & HR (Arbeitsdirektor) | 1 January 2026 | ex-CFO/COO BayernLB; began at Deutsche Bank risk 1998 |

*Departures:* **Martin Beyer** (Vorstandssprecher; 34 years at the company/predecessors; board from 2013; spokesman from 2019) left **30 June 2025** ("Mission erfüllt"; awarded the Raiffeisen-Schulze-Delitzsch gold medal); **Ralf W. A. Teufel** (Client Services) left in 2025 (declined renewal, decided end-2024) — confirming Northdata's record of his departure; Birgit Frohnhoff and Jörg Staff departed end-2022 in the six-to-four board reduction. The 2025–26 turnover is a deliberate generational refresh combining internal continuity (Bücker) with external bank expertise (Kaurin, Wiegelmann).

**Aufsichtsrat (supervisory board) — 20 seats, fully co-determined [CONFIRMED FACT].** Atruvia's 2025 Hauptversammlung invitation states the board is composed "gemäß §§ 96 Abs. 1, 101 AktG, § 7 Abs. 1 Satz 2, Satz 1 Nr. 3 Mitbestimmungsgesetz i.V.m. Ziff. 10.1 der Satzung … aus zwanzig Mitgliedern, zehn Vertretern der Anteilseigner und zehn Vertretern der Arbeitnehmer." This confirms the **Mitbestimmungsgesetz 1976** applies (near-parity; triggered above 2,000 employees), with the chair holding a casting second vote in deadlock (§29 MitbestG) and a Vermittlungsausschuss for appointments. Employees hold **10 of 20 seats**; the Betriebsrat/works council drives the employee-side election. Chair: **Daniel Keller** (Deputy CEO, Berliner Volksbank; AR member since June 2020; chair from June 2024, succeeding **Jürgen Brinkmann**). Shareholder representatives elected in 2023 include Kurt Abele, Johannes Karl Herzog and Tanja Müller-Ziegler (replacing Wolfgang Altmüller, Dr. Andreas Martin, Joachim Straub). Committees: Prüfungsausschuss (audit), Strategieausschuss, Ausschuss für Vorstandsangelegenheiten, Vermittlungsausschuss, Beteiligungsausschuss, and (from 1 January 2024) an Ausschuss für Technologie und Architektur.

**Decision rights (control map).** The Vorstand runs operations and proposes strategy, capital allocation, major platform investment, acquisitions and pricing to member banks. The Aufsichtsrat approves major investments, acquisitions (e.g. ECON 2023, the Ratiodata restructurings, supplier contracts including Microsoft and IBM), board appointments and remuneration, the financial plan and the "Finanzierung der weiteren Digitalisierung." The Hauptversammlung (member banks via VR-FGI) elects the shareholder AR bench, approves the dividend, and discharges the boards (both discharged at the 2026 HV "mit sehr guten Ergebnissen"). Auditor: **BDO AG Wirtschaftsprüfungsgesellschaft, Hamburg** (unqualified opinions 2023).

**Executive compensation:** not individually disclosed (no listed-company disclosure regime). The Ausschuss für Vorstandsangelegenheiten handles Vorstand contracts, Tantiemen (bonuses) and targets; specific figures are [UNKNOWN].

### I.5 Legal Architecture

- **Who contracts with member banks:** **Atruvia AG**, via framework agreements (Rahmenverträge) covering the Bankverfahren (agree21), data-centre operation and services. Pricing has historically been a base package (Basispaket) plus volume components; the 2024 HV signalled a move toward more "nutzerorientierte Bepreisung." An inflation-linked price increase applied 1 April 2023.
- **Who owns the platform IP:** **Atruvia AG** owns agree21 and the associated trademarks (AGREE, AGREE-BANK, FIDUCIA, PERAS, VR-NetKey, VR-WEB, ZIS, etc., per trademark filings). parcIT owns/develops VR-Control/okular.
- **Who employs staff:** **Atruvia AG** (5,263 at 31 Dec 2023; ~5,300 at end-2024; the "Zahlen und Fakten" page cites ~5,850 for the AG in 2025) plus each subsidiary employs its own (group ~10,076 in 2024).
- **Who bears regulatory liability:** Under **§25b KWG** the *outsourcing bank* retains full regulatory responsibility for outsourced functions; Atruvia is the "Auslagerungsunternehmen." Contracts must give the bank and BaFin audit/inspection and information rights, and DORA (Art. 30) now mandates specific clauses.
- **Key supplier contracts:** IBM (multi-year, signed 19 November 2025); Microsoft M365 (AR-approved 2022).
- **Litigation/enforcement:** a **BaFin §44 KWG special inspection began November 2023** [CONFIRMED FACT — 2023 annual report]; the earlier "audIT" programme (to end-2021) remediated prior findings. No major public litigation identified [UNKNOWN — thin disclosure].

Why the legal architecture is designed this way: a single contracting entity (Atruvia AG) simplifies the ~800 banks' §25b due diligence and the audit-rights architecture; specialised subsidiaries ring-fence distinct labour, tax and regulatory regimes; and the AG form (vs the former GAD eG cooperative form) allows a share-based ownership and pooling structure suited to hundreds of institutional owners.

### I.6 Regulatory and Supervisory Architecture

Atruvia is **not a licensed credit institution.** It is supervised principally *indirectly*, through the outsourcing obligations of its bank customers, plus direct BaFin inspection powers and (contractually) DORA.

- **§25b KWG + MaRisk AT 9:** the outsourcing banks remain fully responsible; they must maintain outsourcing registers, risk assessments, exit strategies and audit rights over Atruvia. Because ~800 banks outsource core banking to one provider, Atruvia sits at the centre of the sector's outsourcing-risk map.
- **BAIT (and its KRITIS module, since 2018):** bank IT requirements flow to Atruvia through customer contracts; the BAIT KRITIS module permits the §8a/§39 BSIG nachweis to be delivered within the annual audit.
- **BaFin §44 KWG:** BaFin can and does inspect banks' outsourced IT providers directly; the November 2023 inspection is the concrete instance.
- **DORA (Regulation (EU) 2022/2554):** in force from 17 January 2025. **CRITICAL FINDING: on the ESAs' first CTPP list published 18 November 2025 (19 providers), Atruvia was NOT designated a Critical ICT Third-Party Provider. IBM WAS designated (Lead Overseer: EBA), as were AWS, Microsoft, Google Cloud, Oracle, SAP, Deutsche Telekom, SWIFT, Worldline, Temenos, Equinix and others** [CONFIRMED FACT — EBA/ESMA/EIOPA joint announcement, 18 November 2025]. *Why not Atruvia?* The DORA methodology (Art. 31) weights *cross-border footprint* (services in 3+ member states), *systemic impact across the EU*, and *substitutability*; Atruvia is overwhelmingly domestic (Germany-only) and intra-sector in character, which likely kept it below the CTPP threshold even though it is systemically central *within Germany* [ANALYTICAL INFERENCE]. The list is updated annually, so future designation is plausible but not imminent. Meanwhile Atruvia still bears full DORA obligations as an ordinary ICT third-party provider (mandatory contractual clauses, incident support, testing participation, exit facilitation) — but escapes the direct ESA oversight, oversight fees, on-site inspection powers, binding recommendations, and the power to require financial entities to suspend/terminate services that CTPP status carries. Designated CTPPs face periodic penalty payments of **up to 1% of average daily worldwide turnover** per day of breach (Art. 35(6)) — a burden IBM now carries and Atruvia does not.
- **KRITIS / BSI-KritisV:** finance/insurance is a KRITIS sector and Atruvia's data centres/processing almost certainly exceed thresholds; since 17 January 2025, DORA-regulated entities are exempt from the parallel §32 BSIG incident-reporting duty (DORA reports are routed BaFin→BSI) [ANALYTICAL INFERENCE — Atruvia's specific KRITIS registration is not individually public].
- **NIS2:** German transposition (BSIG recast, in force late 2025) treats DORA-regulated financial entities as lex specialis, reducing double reporting.
- **Bundesbank/ECB:** interest arises from payment-system and (post-VR Payment) card-processing volumes; Atruvia itself is not directly ECB-supervised.
- **Certifications/audits:** Atruvia states ISO 27001, high availability and high security standards; service-organisation reporting (IDW PS 951 / ISAE 3402) is standard for such providers [COMPANY CLAIM — specific certificate scopes not fully public].

**Does the competitor face the same burden?** Yes — **Finanz Informatik** (the Sparkassen equivalent; Atruvia and Finanz Informatik top the Lünendonk ranking of German internal IT service providers) faces the identical §25b/MaRisk/BAIT/DORA regime and is similarly domestic; neither appears on the CTPP list. Accumulated regulatory capability is thus both a running cost and a barrier to entry: a challenger would have to reproduce a decade of MaRisk/BAIT/DORA-compliant operations to be credible.

### I.7 Own Capability vs Partner Dependency

| Capability | Model | Detail |
|---|---|---|
| Core platform (agree21) | **Own** | Atruvia-owned IP; IMS/COBOL back end, Java-enabled ~85% of transactions |
| Mainframe hardware/software | **Buy — deep dependency on IBM** | Historically 8× IBM z15 across four data centres; ~80bn core-banking transactions/yr, peaks 12,000 tps; IBM IMS transaction manager + Db2 for z/OS; migrating to **IBM z17** under the Nov 2025 deal; Red Hat OpenShift for hybrid cloud; IBM Turbonomic (workload optimisation) and Apptio (cost transparency) for vendor-independence |
| Data centres | **Own/operate** | Four data centres (Karlsruhe, Münster and others) |
| Cloud / sovereignty | **Hybrid** | OpenShift for multi-cloud independence; GWS provides cloud; "sovereignty" framed by Atruvia (Bücker) across data, infrastructure, cloud, vendor and innovation dimensions |
| ATM / self-service (>30,000 devices) | **Subsidiary (Ratiodata)** | Ratiodata supplies, rolls out and services SB systems nationwide; processing runs on IBM Z |
| Card issuing / processing | **Building — via VR Payment acquisition** | Debit today; debit + credit from 1 Jan 2027 |
| Identity / authentication | **Own + JV** | VR SecureGo (authentication app) operated by Atruvia; Verimi JV for broader digital identity |

**IBM dependency assessment (mechanism):** this is a mainframe monoculture. Switching cost is prohibitive (the IMS/COBOL/Db2 estate carries ~80bn+ transactions/yr), giving IBM strong bargaining power; the multi-year deal secures continuity but entrenches the dependency. IBM's own quote frames Atruvia's use of the z17 "as a cornerstone to support its mission-critical operations including the core banking system." Resilience is high operationally (mature, hardened platform) but *concentration risk is severe.* A second-order mitigant: IBM's CTPP designation places IBM under direct EU oversight, marginally strengthening Atruvia's resilience story without Atruvia bearing the compliance cost.

### I.8 Regulation and Structure as Competitive Position

Atruvia's position is simultaneously a **barrier to entry**, a **strategic asset** and a **constraint**:
- *Captive-ownership lock-in:* member banks own their supplier, so switching means abandoning an asset they own and re-tooling core banking — near-insurmountable. But this is **not** an unqualified "moat": absent competition, pricing discipline is weak, modernisation can be slow, and under-investment risk is real (the multi-year pause on agree21 optimisation/individualisation while the migration ran is illustrative).
- *Regulatory approval burden:* a challenger must reproduce MaRisk/BAIT/DORA-grade operations and pass each bank's §25b due diligence — years of accumulated capability.
- *Operational scale:* safely running core banking for ~800 institutions and tens of millions of accounts is a genuine, hard-to-replicate capability.

Net assessment: the structure produces durability and systemic centrality, but the customer-owner model trades away the pricing discipline and accountability that external competition and external ownership would impose. The right way to score it is not "moat = good" but "moat = durable, with a governance-driven under-investment tax."

### I.9 Institutional Dependency Map

| Institution | Function | Criticality | Substitutability | Their bargaining power | Switching difficulty | Failure impact |
|---|---|---|---|---|---|---|
| **IBM** | Mainframe HW/SW (Z, IMS, Db2) | **Critical** | Very low | Very high | Extreme | Core banking halts |
| **Member banks (owners + customers)** | Capital + revenue | **Critical** | None | Collective/high | n/a | Existential both ways |
| **BVR** | Sector coordination/strategy | High | Low | Moderate | n/a | Strategic drift |
| **DZ Bank / GFG** (Union Investment, R+V, Schwäbisch Hall, VR Payment) | Central bank + product/payment partners | High | Low | Moderate | High | Product/payment disruption |
| **BaFin / Bundesbank / ESAs** | Supervision | High | None | High | n/a | Enforcement/restrictions |
| **Deutsche Kreditwirtschaft / girocard** | Payment scheme infrastructure | High | Low | Moderate | High | Card/payment disruption |
| **Card schemes (Visa/Mastercard)** | Card rails | High (rising post-VR Payment) | Low | High | High | Card processing disruption |
| **SCHUFA / data providers** | Credit data | Moderate | Moderate | Moderate | Moderate | Lending friction |
| **Ratiodata (internal)** | Hardware / SB services | High | Moderate | Low (owned) | Moderate | ATM/branch hardware |
| **COBOL/mainframe labour market** | Scarce skills | High | Low | High (scarcity) | n/a | Maintenance risk |
| **Microsoft** | M365 / productivity | Moderate | Moderate | High | Moderate | Office disruption |

**Single point of institutional failure — both directions.** Atruvia depends on IBM and on its member banks; but the systemic headline is the converse: **Atruvia is itself a single point of failure for the German cooperative banking sector** — the 646 cooperative banks counted by the BVR at year-end 2025, plus ~250 further private banks and the ADAC, and tens of millions of accounts. An extended Atruvia outage would incapacitate a large share of German retail banking. This is precisely the concentration DORA is meant to police — yet Atruvia's domestic profile kept it off the CTPP list, arguably leaving a *national* systemic-risk supervisory gap even as *cross-border* providers (IBM, the hyperscalers) are captured.

### I.10 Tax and Intercompany Architecture

Atruvia AG is German tax-resident (Frankfurt registered seat; Karlsruhe/Münster administration), subject to Körperschaftsteuer, Solidaritätszuschlag and Gewerbesteuer. The **GmbH & Co. KG holding vehicles are tax-transparent** for income tax (income attributed to the Kommanditist banks); their purpose is member-governance and interest-pooling with limited liability — the standard German device for pooling many members' interests — **not** tax optimisation. Intercompany relationships: Atruvia charges member banks for services and cost-allocates within the group (e.g. the Ratiodata↔GWS hardware transfer 2024; Accesa/RaRo nearshore services to Atruvia). Effective tax rate and transfer-pricing detail are not individually disclosed [UNKNOWN]. Results: Jahresüberschuss (AG) €7.6m (2022) and €27.8m (2023); operating result (Betriebsergebnis) €40.6m (2023), €66.6m (2024), €89m (2025); AG Gesamtleistung €1,516.3m (2023) with a 2024 plan of €1,636m; **group revenue ~€2.2bn (2024)** with **10,076 group employees, 917 customers, 91m accounts and 9.32bn transactions**; group revenue guided to ~€1.9bn at AG level / higher at group level with €89m operating result for 2025.

### I.11 Corporate and Regulatory Risk

| Risk | Prob. | Severity | Mitigation | Responsible function | Residual |
|---|---|---|---|---|---|
| DORA CTPP designation (future) | Moderate | Moderate | DORA compliance already built; domestic profile keeps it below threshold | Finance, Regulation & HR | Moderate |
| Concentration / systemic outage | Low | Extreme | Four data centres, HA, BCM, testing | Core Banking & Technology | High |
| Core-platform modernisation risk | Moderate | High | Incremental Java refactor of IMS/COBOL; IBM deal | Core Banking & Technology | Moderate |
| COBOL/mainframe skills attrition | High | High | Java-enablement (85%), nearshore Accesa/RaRo | Core Banking & Technology | High |
| Cyber / ransomware | Moderate | Extreme | ISO 27001, quantum-safe crypto (z17), SecureGo | CISO / Technology | High |
| IBM supplier concentration | High (exposure) | Extreme | Multi-year deal, OpenShift, Turbonomic/Apptio | Vorstand | High |
| Governance failure (owner-customer conflict) | Moderate | Moderate | Pooling/consensus, AR committees | Aufsichtsrat | Moderate |
| Member-bank consolidation shrinking owner base | High (ongoing) | Moderate | Scale economics still favour Atruvia | BVR / Vorstand | Moderate |
| Fintech/BaaS edge displacement | Moderate | Moderate | Digital Banking ressort, ecosystem JVs | Digital Banking | Moderate |
| GDPR/BDSG exposure | Moderate | Moderate | Certifications, DPO | Legal / DPO | Moderate |
| VR Payment integration risk | Moderate | Moderate | Phased to 1 Jan 2027; McDermott advised; cartel filing pending | Digital Banking | Moderate |

### I.12 Volume I Reconstruction (Synthesis)

**Chronological corporate evolution:** 1924 Fiducia (Karlsruhe) → 1963 GAD (Münster) and the Fiducia Buchungsgemeinschaft → 1999–2003 Fiducia consolidations (GRK, RWG, rbg) + agree v1.0 → 2007 bank21 across GAD → 2012 failed merger → Oct–Dec 2014 approvals (GAD 94%, Fiducia 100%) → **1 July 2015 Fiducia & GAD IT AG** → 2017–2019 agree21 series migration → 2020 migration complete (~€125m synergy target) → **1 Sep 2021 rebrand to Atruvia** → 2023 EGP merged up, BaFin §44 inspection begins, Accesa/RaRo restructured to the AG → **19 Nov 2025 IBM multi-year deal (z17)** → **18 Nov 2025 ESAs CTPP list (Atruvia not designated; IBM designated)** → 1 Jan 2026 Vorstand "Zielbild" complete → **2 Jul 2026 VR Payment Issuing-Processing acquisition** (effective 1 Jan 2027; cartel filing 15 Jul 2026).

**Corporate entity diagram (control flow):** ~800 member banks → {BW-KG (Stuttgart, HRA 720090), Nord-KG (Münster, HRA 10029), Bayern-BBA (Beilngries, HRA 2070; 14.15%)} → VR-FGI Beteiligungsholding (Neu-Isenburg, HRA 42595; ~91.6% block) → **Atruvia AG (HRB 102381)** → {Ratiodata SE, parcIT, BMS CS, Peras, Serviscope, Accesa/RaRo, ECON, FORUM, TRUUCO, GWS} + minority JVs {Verimi, amberra}.

**Regulatory/supervisory map:** BaFin (§25b, §44 KWG; MaRisk AT 9; BAIT) supervises the *banks*, reaching Atruvia through their outsourcing duties and direct inspection; ESAs (DORA) capture IBM as CTPP but not Atruvia; BSI (KRITIS/BSIG) and NIS2 apply with DORA as lex specialis; Bundesbank/ECB interest via payments.

**Legal responsibility map:** Atruvia AG contracts with banks, owns agree21 IP, employs core staff, is the "Auslagerungsunternehmen"; the *banks* retain regulatory liability; parcIT/others own their niche IP.

**Answers to the mandated questions:**
- **Most strategically important legal entity:** Atruvia AG itself (owns agree21 IP, holds the bank contracts and the outsourcing relationship, employs the core staff). Among the ownership vehicles, **VR-FGI Beteiligungsholding GmbH & Co. KG** is the control linchpin.
- **Where actual control sits:** with the member banks collectively, exercised through VR-FGI's pooled ~91.6% vote and BVR-coordinated consensus — not with DZ Bank or any single bank.
- **Greatest external dependency:** **IBM** (mainframe monoculture).
- **Hardest-to-recreate asset:** the **agree21 single core platform** running ~800 banks and tens of millions of accounts on IBM Z — a decade-plus, "moon-landing"-scale build plus the regulatory operating capability around it.
- **Most misunderstood by outsiders:** the **customer-owner identity** (and the false belief that DZ Bank controls Atruvia). Ownership is captive and pooled, not centralised.
- **What would take longest to rebuild from zero:** not the software licences or data centres, but (a) the migrated, cleansed data and battle-tested agree21 operating processes, and (b) the accumulated MaRisk/BAIT/DORA regulatory operating capability and the sector's trust — a decade-scale endeavour.

**Ten most important conclusions:**
1. Atruvia is systemically central to German cooperative banking yet escaped DORA CTPP designation because it is domestic, not cross-border — a potential supervisory blind spot for *national* systemic risk.
2. Control is genuinely collective (VR-FGI pooling), making Atruvia unusually accountable to its customers-as-owners but structurally weak on external pricing discipline.
3. DZ Bank does not control Atruvia; the "~20%" figure is Verimi, not Atruvia.
4. IBM is the deepest single dependency; the Nov 2025 z17 deal entrenches rather than reduces it.
5. agree21 is the crown jewel and the single largest concentration risk simultaneously.
6. The 20-seat, MitbestG-1976 co-determined board gives employees 10 of 20 seats — significant for a workforce-heavy IT business (Wiegelmann is Arbeitsdirektor).
7. The 2025–26 Vorstand turnover (Beyer/Teufel out; Kaurin, Japec, Wiegelmann in) is a deliberate generational-plus-external-expertise refresh.
8. The VR Payment acquisition materially expands Atruvia into credit-card processing, raising card-scheme exposure and integration risk (subject to Bundeskartellamt clearance).
9. Disclosure is thin (no listing, no IR, no analyst coverage) — several economic/tax specifics are genuinely UNKNOWN.
10. The captive model is durable but structurally prone to under-investment and slow modernisation absent competitive pressure.

---

## Recommendations
- **For a competitor / cloud-native core challenger:** Do not attack the captive core head-on. Target the edges — digital-banking UX, data analytics, BaaS/ecosystem modules — where fintech displacement is Atruvia's own stated concern. *Benchmark to watch:* any member-bank defection or dual-sourcing of non-core modules would signal a real opening; conversely, deeper IBM entrenchment and the VR Payment integration make the core more, not less, defensible.
- **For a member bank (owner-customer):** Use the pooled governance to push for transparent, usage-based pricing (already signalled at the 2024 HV) and a public modernisation roadmap. *Escalation threshold:* if agree21 modernisation milestones slip, or if IBM-dependency mitigation (OpenShift/hybrid, vendor-independence tooling) stalls, invoke the Aufsichtsrat's Strategy and Technology-&-Architecture committees.
- **For a supervisor (BaFin / Bundesbank):** Treat Atruvia as a *de facto national systemic node* despite its non-CTPP status; ensure §44 inspections and DORA oversight-by-proxy explicitly cover the single-point-of-failure scenario for ~800 banks. *Trigger for direct action:* any material availability incident affecting multiple institutions, or a step-change in cross-border service that could bring Atruvia within the CTPP threshold at the next annual ESA refresh.
- **For an analyst / acquirer of adjacent assets:** Track two clocks — the VR Payment integration (to 1 January 2027, plus cartel clearance in case B9-75/26) and the annual ESA CTPP refresh. CTPP designation would materially raise Atruvia's compliance cost and oversight exposure (up to 1% of worldwide turnover per day of breach for designated providers).

## Caveats
- **Thin disclosure environment:** no listing, no investor relations, no earnings calls, no analyst coverage, no prudential disclosure. Executive compensation, exact effective tax rate, transfer-pricing detail, the VR Payment purchase price, and Atruvia's specific KRITIS registration are **UNKNOWN**.
- **Ownership precision:** only Bavaria's 14.15% indirect stake is individually public; the Baden-Württemberg and Nord KG percentages are not disclosed (the three together = 91.6%). The exact per-share vs per-member voting rule inside the pooling agreement / any formal Konsortialvertrag could not be confirmed from an accessible primary document.
- **Migration cost:** the "on time and on budget" / €125m-synergy figures are company claims; no independent audit of total programme cost or overruns is public.
- **CTPP status is a snapshot:** the ESA list is updated annually; Atruvia's non-designation as of 18 November 2025 could change in future rounds.
- **Customer-count and data variance:** Atruvia/IBM/NetApp sources cite figures ranging from ~800 to ~950 "banks," 81–91m accounts, and four to six data centres, depending on scope (member banks vs all customers) and date; the BVR's 646 is the count of *cooperative banks* at year-end 2025, while Atruvia's ~900+ "Kunden" includes private banks and other entities. Minor discrepancy in the shareholder chart (GB2023 shows 1.3% "sonstige/genossenschaftliche Unternehmen" vs 1.7% in some summaries); the most granular Aug-2026 table resolves the cooperative total to 99.68%.
- Employee and revenue figures vary by scope (AG vs group) and reporting date; "As of" dates are given where material.

*End of Volume I. Volume II (Business Model, Products, Platform Architecture & Economics) not begun, per instruction.*