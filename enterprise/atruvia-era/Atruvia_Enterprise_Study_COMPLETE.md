# The Atruvia Enterprise Reverse-Engineering Study

**A forensic institutional teardown of Atruvia AG — the captive IT utility of the German cooperative banking sector**

Research cut-off: 8 August 2026
Prepared by: Damascus Research
Volumes I–V complete · Cross-Volume Synthesis included

---

## Table of Contents

- [The Atruvia Enterprise Reverse-Engineering Study](#the-atruvia-enterprise-reverse-engineering-study)
  - [How to read this document](#how-to-read-this-document)
  - [Conventions governing the whole document](#conventions-governing-the-whole-document)
- [Part I — Corporate, Legal, Regulatory & Institutional Anatomy](#part-i-corporate-legal-regulatory-institutional-anatomy)
- [Part II — Product, Customer & Service-Delivery Architecture](#part-ii-product-customer-service-delivery-architecture)
  - [VOLUME II: Product, Customer & Service-Delivery Architecture](#volume-ii-product-customer-service-delivery-architecture)
- [Part III — Operations, Technology, Data & Organisational Infrastructure](#part-iii-operations-technology-data-organisational-infrastructure)
- [Part IV — Financial Statements, Revenue Architecture, Unit Economics & Capital](#part-iv-financial-statements-revenue-architecture-unit-economics-capital)
- [Part V — Management, Culture, Competition, Moat, Risk & Strategic Evolution](#part-v-management-culture-competition-moat-risk-strategic-evolution)
- [Part VI — Cross-Volume Synthesis](#part-vi-cross-volume-synthesis)
  - [VI.1 The category error](#vi1-the-category-error)
  - [VI.2 The single causal model](#vi2-the-single-causal-model)
  - [VI.3 What the volumes prove together that none proves alone](#vi3-what-the-volumes-prove-together-that-none-proves-alone)
  - [VI.4 The central tension](#vi4-the-central-tension)
  - [VI.5 What would falsify the reading](#vi5-what-would-falsify-the-reading)
  - [VI.6 What Atruvia is becoming](#vi6-what-atruvia-is-becoming)
  - [VI.7 Implications for a fintech builder](#vi7-implications-for-a-fintech-builder)
  - [VI.8 Ten cross-volume conclusions](#vi8-ten-cross-volume-conclusions)
- [Appendix A — Glossary of German Terms](#appendix-a-glossary-of-german-terms)
  - [Accounting and financial](#accounting-and-financial)
  - [Pricing and charging](#pricing-and-charging)
  - [Corporate and governance](#corporate-and-governance)
  - [Sector and institutional](#sector-and-institutional)
  - [Technology and operations](#technology-and-operations)
  - [Regulatory](#regulatory)
- [Appendix B — Canonical Figures Register](#appendix-b-canonical-figures-register)
  - [Scale](#scale)
  - [Financials](#financials)
  - [Ownership and structure](#ownership-and-structure)
  - [Technology and regulatory](#technology-and-regulatory)
  - [Benchmark — Finanz Informatik](#benchmark-finanz-informatik)
- [Appendix C — Reconciliation of Cross-Volume Discrepancies](#appendix-c-reconciliation-of-cross-volume-discrepancies)
  - [Perimeter and measurement differences (not errors)](#perimeter-and-measurement-differences-not-errors)
  - [Genuine errors and corrections](#genuine-errors-and-corrections)
  - [Known unknowns carried forward](#known-unknowns-carried-forward)
- [Appendix D — Source Hierarchy & Evidence Conventions](#appendix-d-source-hierarchy-evidence-conventions)

## How to read this document

This study takes Atruvia apart component by component across five volumes, then reassembles it. Each volume was researched and written as a standalone study; this master edition binds them into one document with a single set of conventions, a glossary, a canonical figures register, and a synthesis that no individual volume contains.

| Part | Volume | Question it answers |
|---|---|---|
| Front matter | — | Conventions, glossary, canonical figures, how to navigate |
| Part I | Corporate, Legal, Regulatory & Institutional Anatomy | Who owns and controls Atruvia; how a customer-owned utility is governed and supervised |
| Part II | Product, Customer & Service-Delivery Architecture | What Atruvia sells, to whom, and what a member bank actually buys |
| Part III | Operations, Technology, Data & Organisational Infrastructure | How ~10bn bookings a year are processed on a mainframe core for ~700 banks |
| Part IV | Financial Statements, Revenue Architecture, Unit Economics & Capital | How a cooperative with no equity market funds a permanent investment race |
| Part V | Management, Culture, Competition, Moat, Risk & Strategic Evolution | Why Atruvia persists, what is genuinely defensible, and what it becomes |
| Part VI | **Cross-Volume Synthesis** | What the five volumes prove together that none proves alone |
| Appendix A | Glossary of German Terms | Load-bearing — read before Part IV |
| Appendix B | Canonical Figures Register | The governing value for every material number |
| Appendix C | Reconciliation of Cross-Volume Discrepancies | Where the volumes disagree, and which figure governs |
| Appendix D | Source Hierarchy & Evidence Conventions | How claims were graded |

**Recommended reading order for a first pass:** Appendix A (glossary) → Part VI (Synthesis) → Appendix B → then Parts IV and V in full. Parts I, II and III are reference-depth.

---

## Conventions governing the whole document

### Evidence classification

Every material claim carries one of six labels. These are load-bearing, and no inference is silently promoted to fact.

| Label | Meaning |
|---|---|
| **CONFIRMED FACT** | Directly supported by reliable primary evidence |
| **COMPANY CLAIM** | Stated by Atruvia, not independently verified |
| **THIRD-PARTY ESTIMATE** | Externally reported or estimated |
| **ANALYTICAL INFERENCE** | Reasonably inferred from multiple known facts |
| **HYPOTHESIS** | Possible explanation requiring further evidence |
| **UNKNOWN** | Available evidence is insufficient |

### The governing convention — AG versus Group. Read this before any figure.

Atruvia reports on two bases that secondary sources routinely conflate:

- **Atruvia AG** — the parent company, Einzelabschluss under German HGB. This is the entity that owns agree21, operates the data centres, employs the core workforce and contracts with the member banks.
- **Atruvia Group (Konzern)** — the consolidated group, including Ratiodata SE, parcIT, Peras, Serviscope, BMS Corporate Solutions, GWS, ECON, FORUM, TRUUCO, Accesa/RaRo and Lucke EDV.

The two differ by roughly €600m of revenue and roughly 4,200 employees. **They are never spliced in this document.** Every figure is labelled AG or Group. This is the Atruvia equivalent of a reporting-basis break, and it is the single most common source of error in third-party commentary on the company.

### Accounting basis

Accounts are prepared under **German HGB**, not IFRS. Three consequences matter throughout:

1. **Gesamtleistung is not revenue.** It equals Umsatzerlöse plus aktivierte Eigenleistungen plus inventory change. Margins computed on Gesamtleistung differ from margins computed on Umsatzerlöse.
2. **Betriebsergebnis is not EBIT under IFRS.** It is the HGB operating result, and it is sensitive to development-cost capitalisation and pension provisioning.
3. **Provisions and the pension discount rate** move HGB results in ways an IFRS reader will not expect.

### Language

Primary sources are overwhelmingly German. German terms are retained where translation would lose precision, and are defined in Appendix A. Quotations are given in the original with translation where meaning turns on the wording.

---


---

# Part I — Corporate, Legal, Regulatory & Institutional Anatomy

*Research date: 8 August 2026. Subject legal entity: Atruvia AG, HRB 102381, Amtsgericht Frankfurt am Main; administrative seats Karlsruhe (Fiduciastraße 20, 76227) and Münster (GAD-Str. 2–6, 48163); further offices Munich, Frankfurt, Berlin. VAT ID DE143582320. Share capital €115.8m. Standing house standard applied throughout; evidence labels used for material claims.*

---

### TL;DR
- **Atruvia is a non-listed, non-bank Aktiengesellschaft that is the captive core-banking IT provider for essentially the entire German cooperative banking sector** — the 646 Volksbanken, Raiffeisenbanken, Sparda-Banken, PSD-Banken and other cooperative banks that existed at year-end 2025 (per BVR), plus numerous private banks and the ADAC — and it is owned ~99.7% by cooperative entities, overwhelmingly (91.6% of share capital) through three regional holding KGs pooled into VR-FGI Beteiligungsholding GmbH & Co. KG. **Actual control sits with the member banks acting collectively through this pooling vehicle, not with any single institution; DZ Bank does NOT own a controlling stake.**
- **The single most important current regulatory fact:** on the European Supervisory Authorities' first CTPP list (published 18 November 2025, 19 providers), **Atruvia was NOT designated a Critical ICT Third-Party Provider under DORA — but IBM, on whom Atruvia is deeply dependent (IBM Z mainframes running agree21), WAS.** Atruvia is instead supervised *indirectly*, via the §25b KWG / MaRisk AT 9 outsourcing regime imposed on its bank customers and via direct BaFin §44 KWG inspections (one begun November 2023).
- **The deepest dependency is IBM (a mainframe monoculture); the hardest-to-recreate asset is the agree21 single core platform** running ~800 banks and tens of millions of accounts after the "moon-landing" migration completed in 2019/2020; and **the most misunderstood feature is the customer-owner identity**, which suppresses pricing pressure and external accountability while creating near-insurmountable lock-in.

---

### Key Findings
1. **Origin.** Atruvia traces to the Fiducia Revisions- und Treuhand-Institut AG, founded in Karlsruhe on **13 November 1924**. The Tracxn/PitchBook claim that Atruvia was "founded in 1924 by Martin Beyer" is **erroneous data** — Beyer is a former executive (2013–2025), not a 1924 founder. The modern entity was created by the 2015 merger of Fiducia IT AG (Karlsruhe, south) and GAD eG (Münster, north), renamed Atruvia AG on **1 September 2021**.
2. **Ownership.** 91.63% of Atruvia's €115.8m share capital is held by three regional Beteiligungsgesellschaften pooled through **VR-FGI Beteiligungsholding GmbH & Co. KG**; 6.71% by primary banks directly; ~1% other cooperative entities; 0.32% private banks. Total cooperative ownership 99.68%.
3. **Governance.** German two-tier board; a five-member Vorstand as of January 2026 led by Ulrich Coenen (sole spokesman since July 2025 after Martin Beyer's departure); a **20-member co-determined Aufsichtsrat under the Mitbestimmungsgesetz 1976 (10 shareholder, 10 employee representatives)**, chaired by Daniel Keller.
4. **Regulation.** Not a licensed bank; regulated indirectly through customers' outsourcing obligations (§25b KWG, MaRisk AT 9, BAIT), subject to DORA as an ICT third-party provider (contractually) but **not (yet) as a designated CTPP**, and underwent a BaFin §44 KWG special inspection begun November 2023.
5. **Capability vs dependency.** Atruvia owns and operates the agree21 core platform and its data centres but is strategically dependent on IBM for mainframe hardware/software (a multi-year deal signed **19 November 2025** built on the IBM z17); the subsidiary Ratiodata SE supplies and services the >30,000-device self-service/ATM network.
6. **Payments expansion.** On **2 July 2026** Atruvia agreed to acquire VR Payment's **Issuing-Processing** business (effective 1 January 2027; Bundeskartellamt filing 15 July 2026, case B9-75/26), consolidating debit AND credit card processing under Atruvia and turning it into a card "powerhouse."

---

### Details

#### I.1 Origin and Corporate History

**The fragmented origins (1924–2000s).** Two lineages converged into today's Atruvia:

- **Southern lineage (Fiducia).** The Fiducia Revisions- und Treuhand-Institut AG was founded in Karlsruhe on **13 November 1924** [CONFIRMED FACT — Atruvia's own 100-year press release, 11 November 2024]. From 1958 the idea of a shared *Buchungsgemeinschaft* (booking cooperative) emerged among the banks it served; the Zentralkasse südwestdeutscher Volksbanken commissioned Fiducia to build it. By year-end 1963, 67 Volksbanks were partners; 47 staff processed 22 million booking items (against Atruvia's 8.2bn+ today). Fiducia then consolidated regional computing centres through successive mergers: with GRK Genossenschaftliches Rechenzentrum Kassel (1999) and RWG Rechenzentrale Württembergischer Genossenschaften Stuttgart (2001, forming Fiducia AG Karlsruhe/Stuttgart), then with rbg Rechenzentrale Bayerischer Genossenschaften (2003, forming **Fiducia IT AG**). Its core system **agree** (v1.0, 2003) unified the predecessor systems GEBOS (RWG), GENOS (rbg) and RUBIN (GRK), built atop Fiducia's earlier NBS system.
- **Northern lineage (GAD).** The Gesellschaft für automatische Datenverarbeitung (GAD) was founded in Münster on **26 December 1963** as the first cooperative computing centre in north-west Germany, with 23 employees; converted from GmbH to a registered cooperative (eG) in 1966 (30m booking items that year). In 1971 the Rechenzentrale der westdeutschen Volksbanken was absorbed. Its core system **bank21** replaced predecessor BB3 across all GAD member banks by 2007.

**Failed and successful merger (2013–2015).** Earlier merger talks failed (a 2012 attempt "geplatzt," per WirtschaftsWoche). Talks resumed late 2013; the supervisory boards of both firms assented unanimously in early October 2014. The **GAD Generalversammlung approved on 26 November 2014 with 94%**; the **Fiducia extraordinary Hauptversammlung approved on 4 December 2014 with 100%** [CONFIRMED FACT]. The Verschmelzungsvertrag is dated 4 December 2014; the new entity, **Fiducia & GAD IT AG**, was registered at Amtsgericht Frankfurt am Main on 10 June 2015, and the merger became legally effective **1 July 2015** (some sources cite economic effect from 1 January 2015). At formation it had ~5,500–5,600 staff, ~€1.2–1.26bn group revenue, and served all ~1,100 German cooperative banks.

*Structural consequence:* the merger created a two-platform problem (agree south, bank21 north) that dictated the next five years of strategy and created deep path dependency, a north-south organisational fault line, and the dual Karlsruhe/Münster administrative seats that persist today.

**The agree21 migration — "the moon landing" (2016–2020).** Rather than maintain two cores, management chose to consolidate onto **agree21** (based on agree, extended with bank21 components). Series migration of the former GAD banks began February 2017; the series migration completed **9 November 2019**, with all 341 remaining banks (reduced from ~400 by intervening bank mergers) migrated; six special institutions followed through 2020. Scope: ~60,000 bank workstations, 13,000 self-service terminals, ~21.5 million accounts and 22 terabytes of data across 60 series migrations [CONFIRMED FACT — Atruvia press release, 17 February 2020]. Management reported the programme was **delivered on time and on budget**, targeting **~€125m/year in synergies from end-2020** passed to member banks via cost reductions [COMPANY CLAIM — no independent audit of total programme cost or overruns is public; the €125m figure was announced at the 2014/15 merger and repeated at completion]. Contemporary trade press ("Mondlandung"/"the largest cooperative IT transformation of all time") corroborates the scale and on-time completion, but not the cost claim independently.

**Rebrand (2021).** On **1 September 2021** Fiducia & GAD IT AG became **Atruvia AG** (Handelsregister change registered 31 August 2021; Hauptversammlung resolution 30 June 2021). The name was developed by a naming agency; the stated rationale was signalling completion of post-merger integration and a repositioning "from IT service provider to digitalisation partner" [COMPANY CLAIM]. Note the causal chain: the rebrand deliberately followed the migration's completion, so that a single unified platform preceded a single unified brand.

**Strategic programmes since:** the BVR "KundenFokus" verbund project; the EGP Gesamtbanksteuerungssysteme regulatory-software platform (later merged up into Atruvia — the KG was deleted from the register on 19 September 2023 by *Anwachsung*); the M365/Microsoft rollout; a cost-and-efficiency programme; and the "audIT" remediation programme (completed 31 December 2021) that closed out findings from an earlier BaFin process.

**VR Payment acquisition (2026).** On **2 July 2026** Atruvia, DZ Bank and VR Payment announced Atruvia's acquisition of VR Payment's **Issuing-Processing** business, effective **1 January 2027**. The Bundeskartellamt merger-control filing was made **15 July 2026** (case B9-75/26, product markets "Finanzdienstleistungen, Zahlungsabwicklungsdienste") [CONFIRMED FACT]. Atruvia will process debit AND credit cards (credit processing previously sat with VR Payment) on an integrated card platform built with DZ Bank; VR Payment refocuses on acquiring, POS network operation and merchant/omnichannel solutions. Digital Banking board member Željko Kaurin: *"Mit der Bündelung des Issuing Processing führen wir bestehende Stärken in der genossenschaftlichen FinanzGruppe gezielt zusammen."* Legal adviser to Atruvia: McDermott Will & Schulte (Dr. Christian Marzlin, Dr. Philipp Grenzebach). Marzlin (verbatim): *"Ein wesentlicher Teil aller Kreditkartentransaktionen in Deutschland wird über die Systeme von Atruvia abgewickelt … Die Neuordnung des Kartengeschäfts zwischen Atruvia und DZ Bank hat deshalb große Bedeutung für die deutsche Finanz- und Bankenwelt."* Purchase price not disclosed [UNKNOWN]. Rationale: consolidate duplicate structures, integrate account+card at Atruvia, respond to fintech competition and rising payment volumes/regulation.

#### I.2 Corporate Group Structure

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

#### I.3 Ownership and Control (GIVEN UNUSUAL WEIGHT)

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

#### I.4 Governance Architecture

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

#### I.5 Legal Architecture

- **Who contracts with member banks:** **Atruvia AG**, via framework agreements (Rahmenverträge) covering the Bankverfahren (agree21), data-centre operation and services. Pricing has historically been a base package (Basispaket) plus volume components; the 2024 HV signalled a move toward more "nutzerorientierte Bepreisung." An inflation-linked price increase applied 1 April 2023.
- **Who owns the platform IP:** **Atruvia AG** owns agree21 and the associated trademarks (AGREE, AGREE-BANK, FIDUCIA, PERAS, VR-NetKey, VR-WEB, ZIS, etc., per trademark filings). parcIT owns/develops VR-Control/okular.
- **Who employs staff:** **Atruvia AG** (5,263 at 31 Dec 2023; ~5,300 at end-2024; the "Zahlen und Fakten" page cites ~5,850 for the AG in 2025) plus each subsidiary employs its own (group ~10,076 in 2024).
- **Who bears regulatory liability:** Under **§25b KWG** the *outsourcing bank* retains full regulatory responsibility for outsourced functions; Atruvia is the "Auslagerungsunternehmen." Contracts must give the bank and BaFin audit/inspection and information rights, and DORA (Art. 30) now mandates specific clauses.
- **Key supplier contracts:** IBM (multi-year, signed 19 November 2025); Microsoft M365 (AR-approved 2022).
- **Litigation/enforcement:** a **BaFin §44 KWG special inspection began November 2023** [CONFIRMED FACT — 2023 annual report]; the earlier "audIT" programme (to end-2021) remediated prior findings. No major public litigation identified [UNKNOWN — thin disclosure].

Why the legal architecture is designed this way: a single contracting entity (Atruvia AG) simplifies the ~800 banks' §25b due diligence and the audit-rights architecture; specialised subsidiaries ring-fence distinct labour, tax and regulatory regimes; and the AG form (vs the former GAD eG cooperative form) allows a share-based ownership and pooling structure suited to hundreds of institutional owners.

#### I.6 Regulatory and Supervisory Architecture

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

#### I.7 Own Capability vs Partner Dependency

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

#### I.8 Regulation and Structure as Competitive Position

Atruvia's position is simultaneously a **barrier to entry**, a **strategic asset** and a **constraint**:
- *Captive-ownership lock-in:* member banks own their supplier, so switching means abandoning an asset they own and re-tooling core banking — near-insurmountable. But this is **not** an unqualified "moat": absent competition, pricing discipline is weak, modernisation can be slow, and under-investment risk is real (the multi-year pause on agree21 optimisation/individualisation while the migration ran is illustrative).
- *Regulatory approval burden:* a challenger must reproduce MaRisk/BAIT/DORA-grade operations and pass each bank's §25b due diligence — years of accumulated capability.
- *Operational scale:* safely running core banking for ~800 institutions and tens of millions of accounts is a genuine, hard-to-replicate capability.

Net assessment: the structure produces durability and systemic centrality, but the customer-owner model trades away the pricing discipline and accountability that external competition and external ownership would impose. The right way to score it is not "moat = good" but "moat = durable, with a governance-driven under-investment tax."

#### I.9 Institutional Dependency Map

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

#### I.10 Tax and Intercompany Architecture

Atruvia AG is German tax-resident (Frankfurt registered seat; Karlsruhe/Münster administration), subject to Körperschaftsteuer, Solidaritätszuschlag and Gewerbesteuer. The **GmbH & Co. KG holding vehicles are tax-transparent** for income tax (income attributed to the Kommanditist banks); their purpose is member-governance and interest-pooling with limited liability — the standard German device for pooling many members' interests — **not** tax optimisation. Intercompany relationships: Atruvia charges member banks for services and cost-allocates within the group (e.g. the Ratiodata↔GWS hardware transfer 2024; Accesa/RaRo nearshore services to Atruvia). Effective tax rate and transfer-pricing detail are not individually disclosed [UNKNOWN]. Results: Jahresüberschuss (AG) €7.6m (2022) and €27.8m (2023); operating result (Betriebsergebnis) €40.6m (2023), €66.6m (2024), €89m (2025); AG Gesamtleistung €1,516.3m (2023) with a 2024 plan of €1,636m; **group revenue ~€2.2bn (2024)** with **10,076 group employees, 917 customers, 91m accounts and 9.32bn transactions**; group revenue guided to ~€1.9bn at AG level / higher at group level with €89m operating result for 2025.

#### I.11 Corporate and Regulatory Risk

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

#### I.12 Volume I Reconstruction (Synthesis)

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

### Recommendations
- **For a competitor / cloud-native core challenger:** Do not attack the captive core head-on. Target the edges — digital-banking UX, data analytics, BaaS/ecosystem modules — where fintech displacement is Atruvia's own stated concern. *Benchmark to watch:* any member-bank defection or dual-sourcing of non-core modules would signal a real opening; conversely, deeper IBM entrenchment and the VR Payment integration make the core more, not less, defensible.
- **For a member bank (owner-customer):** Use the pooled governance to push for transparent, usage-based pricing (already signalled at the 2024 HV) and a public modernisation roadmap. *Escalation threshold:* if agree21 modernisation milestones slip, or if IBM-dependency mitigation (OpenShift/hybrid, vendor-independence tooling) stalls, invoke the Aufsichtsrat's Strategy and Technology-&-Architecture committees.
- **For a supervisor (BaFin / Bundesbank):** Treat Atruvia as a *de facto national systemic node* despite its non-CTPP status; ensure §44 inspections and DORA oversight-by-proxy explicitly cover the single-point-of-failure scenario for ~800 banks. *Trigger for direct action:* any material availability incident affecting multiple institutions, or a step-change in cross-border service that could bring Atruvia within the CTPP threshold at the next annual ESA refresh.
- **For an analyst / acquirer of adjacent assets:** Track two clocks — the VR Payment integration (to 1 January 2027, plus cartel clearance in case B9-75/26) and the annual ESA CTPP refresh. CTPP designation would materially raise Atruvia's compliance cost and oversight exposure (up to 1% of worldwide turnover per day of breach for designated providers).

### Caveats
- **Thin disclosure environment:** no listing, no investor relations, no earnings calls, no analyst coverage, no prudential disclosure. Executive compensation, exact effective tax rate, transfer-pricing detail, the VR Payment purchase price, and Atruvia's specific KRITIS registration are **UNKNOWN**.
- **Ownership precision:** only Bavaria's 14.15% indirect stake is individually public; the Baden-Württemberg and Nord KG percentages are not disclosed (the three together = 91.6%). The exact per-share vs per-member voting rule inside the pooling agreement / any formal Konsortialvertrag could not be confirmed from an accessible primary document.
- **Migration cost:** the "on time and on budget" / €125m-synergy figures are company claims; no independent audit of total programme cost or overruns is public.
- **CTPP status is a snapshot:** the ESA list is updated annually; Atruvia's non-designation as of 18 November 2025 could change in future rounds.
- **Customer-count and data variance:** Atruvia/IBM/NetApp sources cite figures ranging from ~800 to ~950 "banks," 81–91m accounts, and four to six data centres, depending on scope (member banks vs all customers) and date; the BVR's 646 is the count of *cooperative banks* at year-end 2025, while Atruvia's ~900+ "Kunden" includes private banks and other entities. Minor discrepancy in the shareholder chart (GB2023 shows 1.3% "sonstige/genossenschaftliche Unternehmen" vs 1.7% in some summaries); the most granular Aug-2026 table resolves the cooperative total to 99.68%.
- Employee and revenue figures vary by scope (AG vs group) and reporting date; "As of" dates are given where material.

*End of Volume I. Volume II (Business Model, Products, Platform Architecture & Economics) not begun, per instruction.*


---

# Part II — Product, Customer & Service-Delivery Architecture

## VOLUME II: Product, Customer & Service-Delivery Architecture

### Preface and Method

Volume I established Atruvia AG's corporate, legal, regulatory and institutional anatomy. Volume II reconstructs what Atruvia actually sells, to whom, why they buy (or are structurally obliged to buy), and precisely what happens operationally, contractually and economically when a member bank — and that bank's end customer — uses an Atruvia system.

A structural framing note governs the whole volume. Atruvia holds no customer money and moves none as principal. It operates the systems through which the member banks move their customers' money. There is therefore no take rate and no safeguarding architecture to analyse; pricing is cost allocation (Umlage/Leistungsentgelte) to owner-members, now transitioning toward usage-based charging. This volume has been re-cut accordingly, replacing money-movement sections with the two-tier customer structure (II.2), the service-delivery flow (II.5) and the cost-allocation architecture (II.8).

**Evidence labels used throughout:** CONFIRMED FACT / COMPANY CLAIM / THIRD-PARTY ESTIMATE / ANALYTICAL INFERENCE / HYPOTHESIS / UNKNOWN.

**A note on disclosure quality (read before the pricing sections):** Atruvia is an unlisted, cooperative-owned AG with no investor relations, no analyst coverage and no product-level revenue reporting. Per-unit prices (cost per account, per workstation, per transaction) and per-bank Atruvia cost lines are **not public**. Where this volume reaches the limit of disclosure it says so and labels the specifics UNKNOWN rather than manufacturing precision.

---

### II.0 Reconciling the Scale Numbers (a prerequisite)

Before decomposing the portfolio, the headline scale figures — which differ across sources — must be reconciled, because several downstream conclusions depend on knowing what each number measures.

| Metric | Figure | Source / date | What it actually measures |
|---|---|---|---|
| Accounts administered | ~91 million (2024); **97 million (2025, GB2025)** | Atruvia GB2024/GB2025; IBM 2025 | Bank customer accounts on agree21. A rising series (89m in 2023) — not a contradiction. |
| Customers (institutions) | 917 (2024); "rund 900"; ">1,000 Finanzinstitute" | Atruvia; private-banking-magazin | Contract-holding institutions incl. ~700–730 cooperative banks plus subsidiaries' clients. The ">1,000" counts all financial institutions served across the group. |
| Cooperative banks served | ~670–730 | Atruvia HV2025 ("rund 670"); Handelsblatt ("gut 700"); GB2022 ("rund 820") | Falling through mergers — see II.3. |
| Banking workstations | ~153,000–169,000 | Wikipedia (169k); IBM Turbonomic (155k); Atruvia 2022 (164k) | Managed Bankarbeitsplätze/seats; range reflects different years. |
| ATMs / self-service terminals | ~30,000–34,000 | IBM (30k+); Wikipedia (34k); Atruvia 2022 (32k) | Self-service estate operated for banks. |
| Data centres | four high-security | Atruvia; IBM | Karlsruhe + Münster core; IBM case study says "four data centers." (Grokipedia's "six" is uncorroborated — treat as erroneous/UNKNOWN.) |

**The two transaction numbers — the key reconciliation (Priority Gap 3):**
- **9.32 billion transactions (2024); ~10 billion (2025, GB2025)** — CONFIRMED FACT, Atruvia's own "Buchungen/Transaktionen" KPI (8.7bn in 2023). This is the **business-event count**: bookings/postings, i.e. customer-visible transactions (transfers, direct debits, card postings).
- **~80 billion core banking transactions/year** — CONFIRMED FACT, IBM case study, "with peaks of 12,000 transactions per second," managed by IBM IMS on Db2 for z/OS. IBM's other pages cite "nearly 100 billion," "87 billion," and "120 billion mainframe transactions" in different years.

**ANALYTICAL INFERENCE (high confidence):** These measure different layers. The ~9–10bn is the *business/booking* layer (what a banker calls a transaction). The 80–120bn is the *technical IMS transaction* layer — each business event decomposes into many machine transactions (authorisation, balance check, posting, mirror-posting, journaling, channel calls). A ratio of roughly 8–13 technical transactions per booking is consistent with a classic IMS/COBOL core wrapped in ~1,200 Java microservices via a proprietary API layer (IBM). The rising IBM figure across years (80→87→100→120bn) reflects the digital-channel explosion: IBM notes "a 12-fold increase in HTTPS requests per user interaction for new online banking apps."

---

### II.1 Product and Service Universe

Atruvia's portfolio is a stack: a mainframe core (agree21) at the bottom; a workstation/omnichannel middle layer; end-customer channels on top; steering/analytics/AI alongside; and a ring of subsidiaries selling adjacent products into the same base. The **Follow-the-Legal-Entity rule** is applied: each product is mapped to its delivering entity.

#### The core and platform layer (Atruvia AG)

**agree21 — the Kernbankverfahren (core banking process).** CONFIRMED FACT. The integrated Gesamtbanklösung: account management, payments, lending, securities, plus the steering and channel modules that attach to it. It runs on IBM Z (IMS transaction manager, Db2 database) across four data centres. Named module families: **agree21Finanzen** (steering platform — Accounting, Meldewesen, Controlling on a single data basis), **agree21BAP** (legacy Bankarbeitsplatz), **agree21ECON** (digital end-to-end process modelling for non-standard products), **agree21SecureDocs** (secure data rooms, built on partner DRACOON, superseding agree21Doksharing), **agree21SmartData** (affinity/propensity models), **agree21M365** (managed Microsoft 365). Classification: **core-mandatory**. Historical discipline: agree21 superseded both predecessor cores — "agree" (ex-Fiducia, south) and "bank21" (ex-GAD, north); bank21 is **retired**, agree v1 is **superseded**. Consolidation migration finished 2019–2020 (Volume I).

**BankingWorkspace (BWS) / Bankarbeitsplatz.** CONFIRMED FACT. The new browser-based, role-adaptive employee workspace replacing the closed, inflexible agree21BAP. Vorstandssprecher Ulrich Coenen (Profil, 01/2024): "Der bisherige Bankarbeitsplatz war ein in sich geschlossenes, wenig flexibles System. Der BankingWorkspace hingegen wird … zu einer hochflexiblen, browserbasierten Anwenderoberfläche weiterentwickelt." Coenen confirms a **coexistence phase**: "Die Koexistenzphase von BankingWorkspace und Bankarbeitsplatz wird noch etwas andauern … der aktuelle Zustand ist etwas zäh," with some applications (e.g. CRM) currently maintained twice. Piloting began after successful technical tests in Q4 2022. Classification: **core-mandatory (in transition)**.

**Omnikanalplattform.** CONFIRMED FACT. The multi-tenant (mandantenfähig) platform onto which bank processes are being ported from the core; Atruvia calls it "einer der modernsten und mandantenfähigen Banking-Plattformen in Europa." The BWS is merely "der Zugangsweg der Bankmitarbeitenden zu diesen Prozessen" — the platform is the substance, the workspace the door. ~300 processes from the process map are already available. Vorstand Daniela Bücker's confirmed position (Volume I): the platform/EGP was never limited to agree21, suits integration into arbitrary banking systems, is not restricted to cooperative banks, and porting bank processes from core to platform "will take several more years." Classification: **strategic core**.

#### End-customer channels (Atruvia AG)

**OnlineBanking and VR-NetKey.** CONFIRMED FACT. The new OnlineBanking replaced the legacy Fiducia/GAD online environments; private customers migrated through H1 2022. VR-NetKey is the access credential. Classification: **core-mandatory**.

**VR Banking App.** CONFIRMED FACT. The mobile flagship, rebuilt from the ground up, launched "leise" (without a marketing campaign) alongside VR SecureGo plus, developed agile as an MVP and iterated with the banks. It bundles account management, digital cards, Wero, photo-transfer, multibanking, securities/Union-Depot views, and an AI voice assistant. Classification: **core-mandatory + strategic** (the primary digital customer interface). Adoption/competitive data in II.4/II.7.

**VR SecureGo plus.** CONFIRMED FACT. The authentication/authorisation app (push approval, biometrics, up to three devices), separate from the banking app — required to release OnlineBanking, VR Banking App and card transactions, and to activate Wero. Classification: **core-mandatory** (security substrate).

**Wero and the digital card.** CONFIRMED FACT. Wero (the EPI wallet) is integrated into the VR Banking App; transactions execute in real time directly from the Girokonto (account-to-account, no IBAN), with online-payment capability added and card-funding planned. Digital debit/credit cards live in the app for contactless payment. Johannes Stoll leads the "Daily Banking" business field (Volume I). Classification: **defensive + strategic optionality** (a collective answer to PayPal/Apple Pay and to neobank P2P).

#### Corporate/business-client software (Atruvia AG) — current vs legacy (Priority verify)

CONFIRMED FACT. Three products, tiered by client size, all maintained by Atruvia and licensed through the customer's own bank:
1. **VR-NetWorld Software** — freelancers, small businesses, associations (current; v8.x, but version 8 "erhält seit 2024 keine Funktions-Updates mehr").
2. **Profi cash** — the SME payments workhorse (current; v13 / v12.99 series 2025–2026; migrates VR-NetWorld data).
3. **GENO cash** — medium/large corporates (current; v4.00.008 SP14 in 2025; already supports instant single orders).

These are Windows desktop/server FinTS/EBICS clients. Economically **optional add-ons** (bank buys licences, resells to corporate customers) but strategically important as SME/Firmenkunden anchors. The **Serviceline** (II.5.E) supports GENO cash, Profi cash, VR-NetWorld Software and BankingManager.

**FinTS/PSD2 interfaces.** CONFIRMED FACT. Atruvia operates the FinTS/HBCI servers (fints1.atruvia.de, fints2.atruvia.de, port 3000) through which both its own corporate software and third-party aggregators (windata, konfipay, ALF-BanCo, GLS eBank, subsembly) access accounts — the PSD2 access layer. Classification: **core-mandatory infrastructure** (regulatorily obligatory).

#### Payments and cards

**Payment processing (SEPA, SCT Inst, girocard).** CONFIRMED FACT with a key legal-entity boundary. Atruvia builds and operates the systems in the banks' core through which payments are initiated and posted, but **DZ Bank is the clearing house** ("Clearingstelle für die Abwicklung aller Zahlungen von Volks- und Raiffeisenbanken, die nicht innerhalb einer Bank stattfinden," Handelsblatt). DZ Bank built a new payments platform — jointly owned with Fiducia GAD/Atruvia per Handelsblatt — to carry instant, classic SEPA and cross-border payments. See II.6.

**Card issuing and processing.** CONFIRMED FACT and in transition. Today debit (girocard/Debit) issuing processing sits partly with Atruvia; credit-card processing sits with **VR Payment** (a DZ Bank subsidiary). From **1 January 2027**, under the reorganisation agreed 2 July 2026 (Bundeskartellamt case **B9-75/26, notified 15 July 2026**, product markets "Finanzdienstleistungen, Zahlungsabwicklungsdienste"), Atruvia takes over the **Issuing Processing** division from VR Payment and adds **credit-card processing**, building "eine integrierte, zukunftsfähige Kartenplattform mit einheitlicher Abwicklung von Girokarten, Debitkarten und Kreditkarten auf einer Plattform" (Atruvia PR, 2 July 2026). VR Payment refocuses on Acquiring, POS-Netzbetrieb and merchant/omnichannel payment. **Dr. Christian Marzlin, co-lead partner at legal adviser McDermott Will & Schulte:** "A significant portion of all credit card transactions in Germany is processed through Atruvia's systems. The restructuring of the card business between Atruvia and DZ BANK is therefore of great importance to the German financial and banking sectors." Finanz-Szene (15 May 2026) frames this as VR Payment being "zerschlagen" and Atruvia becoming the "Karten-Powerhouse" (internal project name "Dragon"). Classification: **strategic** — see II.9.

#### Steering, analytics and AI

**EGP Gesamtbanksteuerung / agree21Finanzen.** CONFIRMED FACT. The whole-bank steering platform (accounting, regulatory reporting, controlling on one data basis). Bücker: EGP integration is not restricted to agree21 or to cooperative banks. Classification: **core-mandatory** inside GFG; **externally sellable**.

**parcIT: VR-Control and okular.** CONFIRMED FACT. Delivered by subsidiary **parcIT GmbH** (403 employees / €68.9m revenue in the 2022 GB; 478 / €69.8m in the 2023 GB — a growing unit). VR-Control/okular is the risk and steering software family covering customer business, address/market/liquidity risk, whole-bank steering and capital planning, operational risk, plus modules for risk-bearing-capacity (Risikotragfähigkeit), cost management, IFRS accounting and regulatory reporting. "okular-Tools" are bridging/supplementary solutions (RWA optimisation, LSI stress-test templates, IRIS/BETRIS real-estate and participation-risk calculators). LSI stress-test tools are **free for GFG institutions**; external banks pay via a Basis-Abo. Classification: **core-mandatory (steering)** inside GFG; **competitive/externally-sold** outside.

**genoGPT and the AI portfolio.** CONFIRMED FACT. AI has been used at Atruvia since 2017 (fraud detection). A dedicated unit of >70 staff builds process automation (document recognition, photo-transfer), natural-language systems and generative-AI bots. Products: **plainGPT** (a regulatorily safe ChatGPT-based text/image/research tool for bank staff — "eine der steilsten Adoptionskurven"), and its successor **genoGPT** (a "KI-basierte Wissens-, Agenten- und Informationsplattform" that ingests bank-internal documents; runs in a private cloud with no open-internet connection). A customer-facing website chatbot is also offered. A GFG-wide **KI-Kompetenzcenter** was established, with a KI-Strategie permitting decentralised use under central governance aligned to the EU AI Act. Classification: **strategic optionality** (small today, high potential).

**TRUUCO.** CONFIRMED FACT. TRUUCO GmbH (started April 2023) owns the Smart-Data models and the Impulsmanager (incl. Next Best Action), developing data-driven sales with the banks and GFG partners. Classification: **strategic (analytics)**.

#### Self-service / ATM estate

CONFIRMED FACT. Atruvia operates ~30,000–34,000 ATMs and self-service terminals ensuring cash supply. During the 9 Nov 2020 outage and the DDoS attacks, terminals were noted as sometimes the only functioning channel ("Versorgung mit Bargeld weiterhin möglich"). Hardware/rollout is tied to subsidiary **Ratiodata**. Classification: **core-mandatory (physical channel)**.

#### The subsidiary ring (Follow-the-Legal-Entity)

| Entity | Product / service | Target | Job-to-be-done | Classification |
|---|---|---|---|---|
| **Ratiodata SE** (€344.5m, Vol I) | Systems house: hardware, managed services, print/output, archiving, self-service device services; nearshore via Accesa/RaRo | Banks + regulated industries | Physical IT + operations | Competitive/externally-sold |
| **parcIT** (€78.6m) | VR-Control/okular risk & steering software | Banks (GFG + external) | Regulatory/risk steering | Core-mandatory (GFG)/competitive |
| **Peras** (€46.7m) | geno.HR — payroll, HR management, time, digital personnel file | Banks | HR BPO/software | Optional add-on |
| **BMS Corporate Solutions** (€52.0m) | Corporate-finance solutions incl. **fincompare** (SME financing marketplace) | Banks + SME | Firmenkunden financing | Strategic optionality |
| **Serviscope** (€28.8m) | BPO; the 116 116 card-blocking hotline; customer-service centre services | Banks | Operational outsourcing | Optional add-on / defensive |
| **GWS** | ERP (industry/trade) | Non-bank cooperatives & SMEs | ERP | Competitive/externally-sold |
| **ECON Application** | No-code process platform | Banks | Digital process building | Optional add-on |
| **FORUM Ges. f. Informationssicherheit** | ForumSuite — InfoSec/GRC | Banks + regulated | InfoSec/compliance | Optional add-on |
| **TRUUCO** | Smart-Data / Impulsmanager | Banks | Data-driven sales | Strategic |
| **Accesa / RaRo** | Nearshore dev, cloud, IT ops/support (Romania) | Internal + banks | Cost-arbitrage delivery | Enabling |
| **Lucke EDV** | Specialist IT | Banks | Niche IT | Optional |

**Serviscope and 116 116 (Priority verify).** CONFIRMED FACT (mechanism). 116 116 is the national card-blocking Sperr-Notruf assigned by the Bundesnetzagentur, operated for the market by the Sperr-Notruf e.V.; cardholders call it to block girocard/credit cards, SIMs, e-ID, online-banking access etc. Serviscope provides BPO including card-blocking/service-centre operations for the cooperative banks; the end-customer nonetheless "nimmt direkt mit dem kartenausgebenden Institut Kontakt auf" for follow-up. ANALYTICAL INFERENCE: Serviscope is the sector's operational hand behind the standardised 116 116 experience for VR-bank cardholders, but the legal card-issuer relationship stays with the bank.

**Verimi (digital-identity JV).** CONFIRMED FACT (Volume I): DZ Bank's ~20% stake is in Verimi, not Atruvia — the frequently-repeated "DZ Bank owns ~20% of Atruvia" claim is erroneous and traces to Verimi. Verimi is a cross-sector German digital-identity platform; the sector's participation is **strategic optionality/defensive**. Product-level Verimi economics are UNKNOWN.

---

### II.2 The Two-Tier Customer Structure (given unusual weight)

This is the analytical heart of Volume II. Atruvia serves two populations different in kind:

**Tier 1 — the member banks (~670–730 cooperative banks plus ~190 private banks and specials).** They are simultaneously (a) **owners** (99.68% cooperative-held, 91.63% via the three regional Beteiligungs-KGs), (b) **buyers** (they pay the Umlage/Leistungsentgelte), and (c) **governors** (they populate the Aufsichtsrat and the BVR committees that steer the roadmap). This triple identity is the single most important fact about Atruvia's customer structure.

**Tier 2 — the banks' end customers (tens of millions of German retail and corporate users).** They use Atruvia-built interfaces daily, overwhelmingly **without knowing Atruvia exists**. Their contractual and data relationship is with their local bank, not with Atruvia.

#### Who Atruvia designs for when the two conflict

**ANALYTICAL INFERENCE (high confidence):** Atruvia routes requirements almost entirely through Tier 1. The roadmap is set with the banks and the BVR (below), not with end users; end-user needs enter only as mediated by the banks and Atruvia's own UX research. The tell is Kaurin's own framing (II.4/II.7): the competitive battle has shifted "von Features zu persönlicher Relevanz" — an admission that feature parity was built *for the banks' checklist* and that the harder problem (individual end-user relevance) is the current frontier. The structural bias is toward the owner-buyer-governor, not the invisible end user.

#### Who sets requirements and through which governance route (Priority Gap 6 — bodies by name)

CONFIRMED FACT — the named mechanism:
- **BVR-Gremien** (Bundesverband der Deutschen Volksbanken und Raiffeisenbanken committees): where Atruvia "stellte … die Kernelemente und Stoßrichtungen der Roadmap … vor." The apex strategic route.
- **Bundeseinheitliches Strategieportfolio (BSP)** — the sector-wide strategy portfolio: "Aktuell enthält das BSP 39 Initiativen – davon 36 mit Bezug zu Atruvia." The concrete prioritisation instrument: 36 of 39 route through Atruvia.
- **Strategie- und Portfolioplattform (SPP)** — the "Bankencommunity" where Atruvia's agile delivery portfolio/roadmap is made transparent to banks.
- **Kompetenzteams / Kompetenzteambanken** — named working groups. Atruvia's Birgit Schlächter (Kernbank expert): the Kompetenzteambanken "lieferten wichtige Impulse und unterstützen die gemeinsamen Zielsetzungen zudem aktiv auch als Mitstreiter in den relevanten Gremien"; bank staff "werden … frühzeitig eingebunden und haben die Möglichkeiten zur Mitgestaltung."
- **Fokusgruppen** (e.g. "Fokusgruppe Business Services" with eleven banks) — product-specific co-creation groups.
- **agree21Communitys** — theme-based online communities channelling operational feedback; one is titled "Kundenformate und Gremien transparent."
- **BVR-Prozesslandkarte** — the process map that is the formal frame ("Ordnungsrahmen dafür ist die BVR-Prozesslandkarte").
- **Strategie Hub Regional / Atruvia Solution Days** — annual regional events (from Sept/Oct 2023) bundling BVR, DZ Bank Gruppe, Atruvia and regional/spartan Verbände.

**How a member bank actually influences the roadmap (mechanism):** (1) collectively via BVR committees that agree the BSP; (2) as a Kompetenzteam/Fokusgruppe co-developer if selected; (3) via SPP/agree21Communitys feedback; (4) through the co-determined Aufsichtsrat (chair Daniel Keller — Volume I) which approves major investment/pricing steps; (5) at the Hauptversammlung. **ANALYTICAL INFERENCE:** individual small banks have negligible direct influence; influence is exercised collectively (BVR) or by invitation (Kompetenzteams). This is majoritarian/consensus governance, not a customer-choice market.

#### Who owns the end-customer relationship and data

CONFIRMED FACT (mechanism). The end customer's contract is with the local bank. Under GDPR the **bank is the controller (Verantwortlicher)** and **Atruvia is the processor (Auftragsverarbeiter)** under an Auftragsverarbeitungsvertrag (II.5.B). The Serviceline is "reachable only via the customer's own bank's phone number," deliberately keeping Atruvia invisible and the bank as the face. The end-customer *data* is the bank's; Atruvia processes it on instruction. The "customer-is-also-owner" distortion therefore operates entirely at Tier 1.

#### How the customer-is-also-owner identity distorts prioritisation

**ANALYTICAL INFERENCE (high confidence, evidence-backed):**
1. **Consensus over speed.** Because ~700 owner-buyers must be broadly satisfied, standardisation is negotiated ("Standardisierung … keinesfalls als 'kleinsten gemeinsamen Nenner'," Schlächter — a defensive phrasing that concedes the risk exists). Coenen concedes the transition is "etwas zäh."
2. **Underpricing pressure vs investment need.** Owners resist price rises on themselves (II.8) yet demand competitive digital features; the result is chronic under-investment relative to neobanks (Platow: competitors "geben oft ein Vielfaches").
3. **Uniformity over differentiation.** A single multi-tenant platform serves all; individual banks get limited white-labelling (II.7), which suits small banks but frustrates large ones.
4. **The owner's P&L is the customer's cost.** Every euro Atruvia earns is a cost line for its owners, so there is structural pressure to keep margin thin (2022: €8m surplus on €1.4bn) — which starves reinvestment, the exact tension resolved by the 2025 shift to a 4%-of-revenue Zielrendite (II.8).

---

### II.3 Customer Segmentation

#### By institution type

| Segment | Examples | Notes |
|---|---|---|
| Volksbanken / Raiffeisenbanken | ~670–730 institutions | The captive core; all use agree21. |
| Sparda-Banken | 11 institutions | All 11 now on/moving to Atruvia (below). |
| PSD-Banken | PSD Bank Nord (first migrated 2008), PSD Bank West etc. | Long-standing cooperative specials. |
| Kirchenbanken | Various | Cooperative specials. |
| Apotheker- und Ärztebank (Apobank) | Apobank | **Left the platform** — migrated to Avaloq (II.10 exit). |
| Private banks | ~190; M.M. Warburg (announced), Bankhaus C.L. Seeliger | Growth segment outside the captive base. |
| Non-cooperative migrations | Bank für Sozialwirtschaft, UmweltBank, National-Bank Essen | Inbound wins (II.11). |
| Non-bank customers | ADAC | IT-outsourcing/other-industry. |

#### By legacy platform (does the north/south divide persist?)

CONFIRMED FACT: the ex-Fiducia (south, "agree") and ex-GAD (north, "bank21") divide has been **eliminated at the core** — all migrated to agree21 by 2019–2020. ANALYTICAL INFERENCE: residual organisational traces persist (two administrative seats, Karlsruhe and Münster), but there is no longer a platform, pricing or service divide by legacy — the single platform is precisely what enables sector-wide rollout (II.9).

#### By size

**ANALYTICAL INFERENCE:** the base ranges from a handful of very large Volksbanken (e.g. Frankfurter Volksbank Rhein/Main, Berliner Volksbank — multi-billion balance sheets) to hundreds of small rural Raiffeisenbanken. Roadmap influence correlates with size and Kompetenzteam participation. Large banks are the most likely to chafe at limited white-labelling and to be "nicht alle … zufrieden" with the digital offering (Platow). Small banks are the biggest beneficiaries of scale economics — they could never build MaRisk/BAIT/DORA-compliant IT alone. Price sensitivity is high across the board because IT is a cost line for owner-members.

#### By product-adoption depth

ANALYTICAL INFERENCE: adoption depth is the real revenue lever now that the base is saturated. Atruvia is explicitly "die Wertschöpfung vertiefen" — deepening value-add at banks that "ohnehin alle das Core-Banking der Atruvia verwenden" (Finanz-Szene). Depth tiers: (1) core + channels only; (2) + steering (VR-Control) + M365; (3) + BPO (Serviscope/Peras) + analytics (TRUUCO) + AI (genoGPT). The usage-based pricing shift (II.8) is designed to monetise depth.

#### The consolidation trend and its consequences

CONFIRMED FACT. Bank mergers requiring technical migration: **42 (2021), 40 (2022), 40–45 registered for 2023**. The cooperative-bank count has fallen from "rund 820" (2022 GB) to "gut 700" / "rund 670" (2025). **Consequence (ANALYTICAL INFERENCE):** the captive base is shrinking in *institution count* but not in *accounts/volume* (accounts rose 89m→91m→97m), because mergers consolidate rather than remove customers. For Atruvia this means (a) fewer, larger, more demanding buyers with more governance weight; (b) recurring migration revenue from consolidations; and (c) growing importance of external wins (II.11) to offset institution shrinkage.

---

### II.4 Jobs to Be Done

#### For member banks — candidate jobs tested against evidence

| Candidate job | Verdict | Evidence |
|---|---|---|
| **Remain an independent bank at all** | **PRIMARY JOB** | Without shared IT, a €500m rural Raiffeisenbank could not meet MaRisk/BAIT/DORA or offer a competitive app. UmweltBank's Koppmann: "Wir benötigen … einen starken Partner, der uns das ganze Spektrum an digitalen Lösungen … bietet." |
| **Satisfy MaRisk/BAIT/DORA without building the capability** | Confirmed, major | agree21Finanzen automates Meldewesen; §25b KWG responsibility stays with the bank but execution is Atruvia's (II.5.F). |
| **Compete digitally vs Sparkassen and neobanks** | Confirmed, contested outcome | VR Banking App 84.5 pts vs Sparkassen 92.6 (Capital 2026). |
| **Hold the cost-income ratio down** | Confirmed | Scale economics; but IT cost rises (II.8) push the other way. |
| **Access sector-wide scale economics** | Confirmed, foundational | Single platform, shared development, shared regulatory implementation. |

**What Atruvia says it sells vs what banks are buying.** Atruvia says it sells a "Technologie- und Digitalisierungspartner" relationship. **ANALYTICAL INFERENCE:** what banks actually buy is *the ability to remain independent regulated banks* — a bundle of software + regulatory compliance + scale economics + risk transfer that no single small bank could assemble. The software is the visible product; the licence-to-operate is the real purchase.

#### For end customers — the VR Banking App vs Sparkassen and neobanks

CONFIRMED FACT (Capital 3/2026 ranking, conducted by the Institut für Vermögensaufbau (IVA) across 33 banking apps):
- **Sparkassen-App: 92.6 points** (1st overall, fifth consecutive win; ~16.6m active users Feb 2024 / ~19.8m active installations per Star Finanz 2026).
- **BW-Mobilbanking: 87.5** (2nd, also Sparkassen-Verbund).
- **C24: 85.5** (top direct/neobank).
- **VR Banking App: 84.5** (assessed in the direct-bank segment).

Kaurin (CONFIRMED FACT): "Der Wettbewerb entscheidet sich nicht mehr an Features – die haben wir in der VR Banking App in großer Breite. Jetzt geht es um persönliche Relevanz." N26/Revolut/bunq/Wise are noted for intuitive onboarding, instant card controls, sub-accounts and multicurrency.

**Adoption figures and the reconciliation the brief demanded:**
- **">12 million downloads and >5 million logins per day"** — CONFIRMED as a COMPANY CLAIM. Margit Messika (Leiterin Geschäftsfeld Omnichannel, Atruvia), Profil interview, 3 June 2025: "Mit mittlerweile über zwölf Millionen Downloads und täglich mehr als fünf Millionen Logins ist die VR Banking App ein zentraler Zugangskanal … geworden." "Downloads" is cumulative installs; "logins per day" is a daily-activity flow.
- **"~991,000 active users, March 2024" (finalarm.de)** — a THIRD-PARTY ESTIMATE that cannot measure the same population as "5 million logins/day." ANALYTICAL INFERENCE: the ~991k figure is almost certainly a single-app-store or single-tool MAU snapshot, not the total user base. The reconciliation: downloads (>12m cumulative) ⊃ active user base (millions) ⊃ daily logins (>5m/day, a flow that can exceed distinct daily users). The finalarm ~991k is not credible as a total and should be treated as a partial/erroneous measurement.

---

### II.5 Service-Delivery Flow Reconstruction (replaces money-movement; priority depth)

Six flows, kept strictly separate.

#### A. Transaction flow (payments/bookings on behalf of banks)
End customer initiates in a channel → agree21 core (IMS/Db2) validates and posts → interbank leg clears via **DZ Bank** (Clearingstelle) for non-internal payments → counterparty bank. Atruvia is **processor/operator**; the **member bank is the principal**; **DZ Bank is the clearer**; the **Bundesbank/EBA CLEARING** provide settlement rails (TIPS for instant; see II.6). ~9–10bn business bookings/year decompose into ~80bn+ IMS transactions (II.0).

#### B. Data flow and GDPR roles
CONFIRMED FACT (mechanism). Customer/account/transaction data and regulatory-reporting data flow between bank and Atruvia data centres. **GDPR: bank = controller; Atruvia = processor** under an Auftragsverarbeitungsvertrag (AVV). Regulatory-reporting data flows outward from agree21Finanzen to the Bundesbank/BaFin **on the bank's behalf and responsibility**. Atruvia's AI products run in a **private cloud with no open-internet connection** to keep processing within the AVV/GDPR perimeter. ANALYTICAL INFERENCE: the AVV + §25b KWG outsourcing contract is the legal spine of the entire relationship (II.5.F).

#### C. Software-release flow — how a release reaches ~800 banks (Priority Gap 4)
CONFIRMED FACT (mechanism, reconstructed from the M365 and BankingWorkspace rollouts, which Atruvia documents as templates):
1. **Technical tests** (BankingWorkspace: Q4 2022).
2. **Pilotierung** with a small cohort (M365: 8 pilot banks end-2022; BWS piloting from 2023).
3. **Serienpiloten / Serienfähigkeit** proving mass-rollout capability (M365: 12 pilot banks in 2022, then 44 in 2023 → 56 including Vor- und Serienpiloten).
4. **Serienmigration** in tranches (M365: ~300 banks in 2024).
5. **Bank-side acceptance and change management** — each bank must do MaRisk-conform change assessment "gem. AT 8.2," retest its processes and schedule.
6. **The annual technical year-end close (technischer Jahresabschluss)** is the marquee coordinated release event — "erneut … sehr geräuschlos."
7. **Notification** via SPP/agree21Communitys, LiveTalks, Strategie Hub Regional and the Atruvia Hub.

**ANALYTICAL INFERENCE:** releases are centralised and quasi-mandatory (multi-tenant platform → one code line for all), but *adoption of new optional processes* (of ~300 available) is bank-by-bank. The bank's "acceptance role" is real for change-management/AT 8.2 but does **not** include the right to refuse a core release — a single tenant cannot fork the platform. This is the source of both the sector's rollout speed and its systemic single-point-of-failure risk (II.12).

#### D. Money flow (fees from banks to Atruvia)
CONFIRMED FACT (structure; specifics UNKNOWN). Banks pay via the Umlage/Leistungsentgelte model: a **Basispaket** (with a volume element, "Mengenwachstum im Basispaket"), a **Festpreis** component, the infrastructure/Netze/Collaboration/Arbeitsplatz charges, plus the special levies (IT-Sonderumlage, Digitalisierungsumlage). GB2021 revenue split (closest public breakdown): **Erlöse aus Bankverfahren €863.1m** and **Erlöse aus Infrastruktur €227.9m** of €1,496.1m total. Invoicing cadence and per-unit tariffs are **UNKNOWN** (internal Leistungsverzeichnis; confidential). See II.8.

#### E. Support and incident flow
CONFIRMED FACT. Tiered:
- **Serviceline** — a qualified *technical end-customer hotline* for OnlineBanking/MobileBanking, GENO cash, Profi cash, VR-NetWorld Software and BankingManager, plus remote-desktop (Fernwartung). Crucially "**only reachable via the telephone number provided by your bank**" — the bank fronts it; Atruvia stays invisible.
- **Bank-facing service desk** for the institutions themselves.
- **Escalation** — during major incidents Atruvia convenes a **Krisenstab** (evidenced 9 Nov 2020) and communicates to banks; banks then communicate to end customers (e.g. 7 July 2026: users warned not to resubmit transfers).
- Status communication during the 7 July 2026 outage was via bank websites and press statements; Atruvia deliberately switched off app/online banking "um die Systeme zu entlasten."

#### F. Regulatory-responsibility flow (§25b KWG)
CONFIRMED FACT (mechanism). Under **§25b KWG / MaRisk AT 9 / BAIT**, outsourcing does not transfer regulatory responsibility: the **member bank remains fully responsible** to BaFin; Atruvia executes. This requires (1) a written outsourcing contract with mandated content; (2) the bank's **Auslagerungsregister**; (3) **audit rights** for the bank and BaFin flowing through to Atruvia; (4) exit/contingency provisions, now sharpened by **DORA Article 30** mandatory clauses and exit strategies (II.10). The 2018 BaFin special inspection (triggered via Volksbank Jever) and the **§44 KWG special inspection begun Nov 2023** (Volume I) demonstrate BaFin reaches Atruvia *through* its supervised banks. Atruvia was **not** designated a DORA Critical ICT Third-Party Provider (18 Nov 2025), though IBM was (Volume I) — a material risk observation (II.12).

---

### II.6 Transaction Processing Teardown (priority depth)

Each event: system → legal entity → data → control point → failure mode.

#### (1) SEPA credit transfer initiated in the VR Banking App
1. **Initiation** — VR Banking App (Atruvia); **release via VR SecureGo plus** (SCA/PSD2). *Control:* SCA. *Data:* payment instruction, device binding.
2. **Core processing** — agree21 (Atruvia; IMS/Db2) validates balance/limits, debits. *Control:* balance/limit check, fraud screening (AI since 2017). *Failure:* core outage → order stuck (7 July 2026 pattern).
3. **Clearing** — interbank leg via **DZ Bank** (Clearingstelle) → SEPA scheme → creditor bank. *Legal entity:* DZ Bank principal for clearing; customer's bank principal for the payment; Atruvia processor.
4. **Settlement** — via Bundesbank/EBA CLEARING. *Failure:* duplicate-submission risk if users resubmit during an outage (explicit 7 July 2026 warning).

#### (2) SEPA instant payment (SCT Inst)
ANALYTICAL INFERENCE + CONFIRMED FACT (partial). Wero transactions "werden direkt von Ihrem Girokonto in Echtzeit ausgeführt" (CONFIRMED). Instant SEPA routes through DZ Bank's real-time platform to **TIPS** (the Eurosystem instant-settlement platform referenced in the Bundesbank Verfahrensregeln for SEPA-Echtzeitüberweisungen). GENO cash already supports instant single orders (CONFIRMED). *Control:* the <10-second execution guarantee and recipient-PSP-reachability check. *Failure:* rejection if recipient PSP unreachable or TIPS rejects. **Atruvia's precise SCT Inst reach is UNKNOWN**, but DZ Bank states "alle Zahlungsverkehrskonten im Hause der DZ BANK [sind] für den Empfang von Echtzeit-Zahlungen freigeschaltet."

#### (3) girocard point-of-sale transaction
ANALYTICAL INFERENCE + CONFIRMED FACT. Card at terminal → acquirer (**VR Payment** on acceptance) → girocard scheme → **issuer processing** (today partly Atruvia/partly VR Payment) → agree21 posts. *Legal entities:* merchant's bank/VR Payment (acquiring), the scheme, the issuing cooperative bank (principal), Atruvia (issuer processing). *Failure:* card-processing outage → declines. **From 1 Jan 2027** issuer processing (debit **and** credit) consolidates at Atruvia; acquiring/POS stays at VR Payment.

#### (4) ATM cash withdrawal
CONFIRMED FACT (partial). Card at one of ~30–34k Atruvia-operated terminals → authorisation via issuer processing → agree21 debit. *Resilience fact:* during 9 Nov 2020 and DDoS incidents, SB-terminals largely kept working when online/app were down ("Bargeldversorgung weiterhin möglich") — ATMs sit on a partly independent path. *Failure:* central-system outages can still propagate to Auszugsdrucker/terminals (reported sporadically 2020).

#### (5) Card transaction today vs after the 1 Jan 2027 migration
- **Today:** debit issuer processing at Atruvia; **credit-card processing at VR Payment**; acquiring at VR Payment. Two houses, "Doppelstrukturen."
- **From 1 Jan 2027:** Atruvia runs **unified issuer processing for girocard + debit + credit on one integrated platform**; VR Payment keeps acquiring/POS/omnichannel. Rationale: consolidate double structures, lift synergies, avoid parallel investment; and — decisively for lock-in — "Wenn Konto und Karte bei Atruvia zusammengeführt werden, verbessere das die Verzahnung zentraler Leistungen." *Bundeskartellamt:* B9-75/26, notified 15 July 2026.

#### (6) Loan application and account opening
CONFIRMED FACT (mechanism). Digital end-to-end strecken via the Omnikanalplattform/agree21ECON (e.g. "Sofortkredit Privatkunde," digital Baufinanzierung with self-service, analytics, document management; "Neukunde (Produktverkauf)" automated customer+account creation). AI document recognition extracts data from IDs/energy certificates/financial documents. *Control:* KYC/credit decisioning (bank's rules). *Legal entity:* bank is lender/principal; Atruvia provides the rails.

#### (7) Branch-counter transaction through the Bankarbeitsplatz
CONFIRMED FACT. Bank employee works in **BankingWorkspace** / legacy **agree21BAP** → agree21 core. *Control:* employee authorisation/role model. *Failure:* during coexistence, some functions (CRM) exist in both → double maintenance, error risk (Coenen's "zäh").

#### (8) Third-party aggregator access via FinTS/PSD2
CONFIRMED FACT. External software (windata, konfipay, ALF-BanCo, GLS eBank, subsembly) connects to fints1/fints2.atruvia.de. *Legal entity:* Atruvia operates the PSD2/FinTS access interface on the bank's behalf; the bank is the ASPSP. *Failure:* FinTS server unreachable → aggregators fail (evidenced 7 July 2026 HBCI/FinTS problems; and the CAMT52 special-character bug of 10 June 2020).

Where internal mechanics are not public they are labelled UNKNOWN (notably exact SCT Inst reach and internal card-platform architecture pre-2027).

---

### II.7 Channel Architecture

| Channel | Operating entity | End-customer experience | Bank configurability / white-labelling | Strategic importance |
|---|---|---|---|---|
| Branch / BankingWorkspace | Atruvia | Advisor-mediated | Role models configurable; process selection (~300 available) | High (efficiency lever) |
| OnlineBanking | Atruvia | Browser banking | Limited; bank branding/skin, product config | Core |
| VR Banking App | Atruvia | Mobile flagship | **Low individual white-labelling** — shared app, bank identity via config | Highest (primary interface) |
| Self-service / ATMs | Atruvia (+ Ratiodata) | Cash/print | Device mix per bank | High (cash + resilience) |
| Call centre / BPO | Serviscope / Serviceline | Phone/remote support | Bank fronts the number | Medium (defensive) |
| Chat / AI assistants | Atruvia (genoGPT/chatbot) | Chatbot on bank site; in-app voice assistant | Bank opts in | Growing |
| Third-party aggregators | Atruvia (FinTS/PSD2) | Customer's chosen app | Regulatorily mandated open access | Obligatory |

**White-labelling — the answer to the brief's question:** ANALYTICAL INFERENCE (high confidence). A member bank can customise **branding, product catalogue, pricing, which optional processes it switches on, and role models** — but it **cannot fork the app or the platform**. The VR Banking App is one shared multi-tenant app; a bank cannot ship a materially different version. This is deliberate (scale economics, single code line, uniform security) and is the deepest source of both efficiency and large-bank frustration.

---

### II.8 Pricing and Cost-Allocation Architecture (priority depth)

#### The structure

CONFIRMED FACT. Banks fund Atruvia through:
1. **Leistungsentgelte / Basispaket** — base service fees with a volume-growth element.
2. **Festpreis** components.
3. **Infrastructure / Netze, Collaboration & Arbeitsplatz** charges.
4. **Special levies:** the **IT-Sonderumlage** and the **Digitalisierungsumlage**.

#### The IT-Sonderumlage and its perpetuation

CONFIRMED FACT (Börsen-Zeitung, "Atruvia will IT-Umlage verstetigen"): the IT-Sonderumlage, resolved ~2018 as a five-year Zukunftsinvestition, "belief sich auf 60 Mill. Euro jährlich" from the cooperative banks — "Weitere 180 Mill. Euro kamen vom Zentralinstitut DZ Bank und rund 200 Mill. Euro von der Rechenzentrale selbst." DER PLATOW Brief: cumulatively "seit 2018 300 Mio. Euro" collected from the Volks- und Raiffeisenbanken. Due to expire end-June 2023, Atruvia sought its **Verstetigung**; the Aufsichtsrat was to decide "bereits Ende April" 2023, with details worked out from summer. Atruvia and BVR declined to comment and left "die Frage nach der Gesamtsumme der heutigen Leistungsentgelte unbeantwortet" — confirming the total Leistungsentgelte figure is deliberately undisclosed.

#### The Digitalisierungsumlage and its tripling

CONFIRMED FACT (DER PLATOW Brief, June 2024): the Digitalisierungsumlage for the Primärinstitute rises "**von zuletzt 30 Mio. Euro über 60 Mio. im laufenden Jahr auf 90 Mio. Euro in 2025**" — a tripling. Being small relative to total revenue, "Ihre Anhebung führt unter dem Strich nur zu einem prozentual einstelligen Preisanstieg." Bank reaction: "Viele Primärbanker stellen immer lauter die Frage, ob das Geld wirklich gut eingesetzt ist … mit dem digitalen Produktangebot … sind längst nicht alle Volksbank-Vorstände zufrieden." And: the price structure "ist ein Thema, über das in den BVR-Führungsgremien nachgedacht wird, auch wenn es noch keine offene Diskussion dazu gibt."

#### The general price increases

CONFIRMED FACT. A **~5% average inflation-driven increase from 1 April 2023** (announced Dec 2022). Börsen-Zeitung: further 2024 increases to give Atruvia "im Schnitt weitere 5% der heutigen Leistungsentgelte der gesamten genossenschaftlichen Organisation" as additional investment.

#### The ~€125m migration synergies "partly taken back"

ANALYTICAL INFERENCE from the record: the agree21 consolidation was sold to banks partly on cost savings; the subsequent tripling of the Digitalisierungsumlage plus perpetuation of the IT-Sonderumlage means the savings are "partly taken back." Mechanism: one-time consolidation synergies were converted into ongoing higher levies to fund the never-ending digital-investment race. (Scenario calculations circulating in the group — Börsen-Zeitung — suggested the sector "im Extremfall" might need €450m–€1bn annually to match European digital front-runners; this is an explicitly hypothetical scenario, **not** a committed figure — HYPOTHESIS.)

#### The shift to nutzenbasierte (usage-based) pricing — announced 2025

CONFIRMED FACT. Vorstandssprecher/CFO Martin Beyer (HV 2025; Atruvia Magazin, 06.05.2025): "Wir reduzieren sukzessive den Anteil der Umlagefinanzierung am Gesamtumsatz durch eine nutzenbasierte Bepreisung. Das heißt für unsere Kunden: Sie bezahlen je nach Mehrwert und Nutzen für unsere Lösungen." Mechanism: "Erlöse werden stärker als heute mit den vorgenannten Indikatoren verknüpft" — revenue tied to digital-usage indicators (Digitalisierungsquote/Nutzungsquote), with "eine spezielle Förderung im Preismodell" rewarding banks that raise digital usage. Phasing is gradual ("sukzessive"); exact indicators and tariffs are **UNKNOWN**.

#### The financial-strategy pivot and dividend question

CONFIRMED FACT. Beyer: "Wir streben eine **Zielrendite von 4 Prozent in Bezug auf den Umsatz** an und steigern nachhaltig das Betriebsergebnis, um ein dauerhaftes Plus für neue Investitionen zu generieren." The stated policy is to **self-fund investment from retained earnings rather than distribute** — investments "künftig aus eigener Kraft." Trajectory: Betriebsergebnis €40.6m (2023) → €66.6m (2024) → €89.0m (2025, Betriebsergebnismarge **4.7%**, exceeding the 4% target). No explicit dividend-per-share policy to owners was found (UNKNOWN). **ANALYTICAL INFERENCE:** returns to owners come primarily as *lower-than-market IT costs and reinvestment*, not as dividends — the cooperative "dividend" is the subsidised platform itself.

#### Actual price levels (Priority Gap 1) — the honest answer

**UNKNOWN / not public.** After targeted search of the Bundesanzeiger, member-bank Geschäftsberichte, BVR and trade press:
- **Per-unit prices** (per account, workstation, transaction) are **not disclosed**; the Leistungsverzeichnis is confidential; Atruvia refused even the aggregate Leistungsentgelte figure to Börsen-Zeitung.
- **Member-bank annual reports do not break out an "Atruvia line."** Atruvia costs sit inside "andere Verwaltungsaufwendungen," with "Datenverarbeitung und Digitalisierung" named only as a qualitative driver (e.g. Frankfurter Volksbank Rhein/Main GB2023: the rise in andere Verwaltungsaufwendungen was driven "unter anderem [durch] gestiegene Aufwendungen in den Bereichen Datenverarbeitung und Digitalisierung"; Berliner Volksbank GB2025: "höhere Kosten für unsere IT-Anwendungen").
- **The only quantified figures are the group-level levies:** IT-Sonderumlage €60m/yr from the banks (+€180m DZ Bank +€200m Atruvia self-funded); €300m cumulative 2018–2023; Digitalisierungsumlage €30m→€60m→€90m (2023–2025); ~5% annual Leistungsentgelte rises; and the GB2021 split (Bankverfahren €863.1m / Infrastruktur €227.9m).
- **A derived proxy** (revenue ÷ accounts) yields roughly €20 per account per year — but this is analyst arithmetic, **not an Atruvia price**, offered only as an order-of-magnitude ANALYTICAL INFERENCE.

#### Governance of pricing and the under-pricing/captive-rent question

**ANALYTICAL INFERENCE (evidence-backed conclusion).** Pricing is *proposed by Atruvia's Vorstand*, *approved by the owner-dominated Aufsichtsrat*, and *contested informally in BVR-Führungsgremien*. There is **no competitive discipline** — the cooperative banks cannot realistically switch (II.10). Two opposing forces result:
- **Toward under-pricing/thin margins:** because every euro is an owner's cost, owners historically squeezed Atruvia to an €8m surplus on €1.4bn (2022) — evidence of *captive under-pricing of Atruvia*, not rent-extraction *by* Atruvia.
- **Toward captive rents:** the absence of exit and of price transparency, plus the ability to perpetuate "temporary" levies and triple the Digitalisierungsumlage with only muted dissent, gives Atruvia real pricing power going forward.

**Conclusion:** historically the owner-customer structure produced **under-pricing** (thin margins, chronic under-investment vs neobanks). The 2025 pivot to a 4% Zielrendite and usage-based pricing is an explicit, governed decision to **move from under-pricing toward sustainable pricing** — converting some latent captive pricing power into reinvestment capacity. Whether this tips into captive rents depends on whether the Aufsichtsrat and BVR hold margins near ~4%. As of 2025, 4.7% suggests the target is being met/slightly exceeded.

---

### II.9 Product Dependency Map

**agree21 is the platform everything attaches to.** Tested rather than assumed:
- **Core → workstation → channels → analytics.** agree21 (core) → BankingWorkspace/BAP (employee) and OnlineBanking/App (customer) → VR-Control/agree21Finanzen (steering) → TRUUCO/SmartData/genoGPT (analytics/AI). Each layer consumes core services via the proprietary API layer (~1,200 microservices, IBM). **Verdict: genuine, tight technical dependency.**
- **Single-platform migration enables sector-wide rollout.** One multi-tenant platform → a release reaches all at once (II.5.C). **Verdict: confirmed — the central economic engine.**
- **Subsidiaries cross-sell into the same base.** Peras (HR), Serviscope (BPO), parcIT (steering), FORUM (InfoSec), TRUUCO (analytics), BMS/fincompare (SME finance) all sell into the captive ~700-bank base. **Verdict: real but uneven** — parcIT/steering is near-mandatory; Peras/Serviscope are optional. The "Wertschöpfung vertiefen" strategy (Finanz-Szene) is precisely about raising attach rates.
- **Does the VR Payment acquisition create a genuine account+debit+credit bundle advantage?** **Verdict: YES (ANALYTICAL INFERENCE, high confidence).** From 1 Jan 2027, unifying account (agree21) + debit + credit + girocard issuer processing on one Atruvia platform (a) deepens lock-in ("Verzahnung zentraler Leistungen"), (b) removes VR Payment's parallel structure, and (c) makes Atruvia the single card-processing point for a large share of German credit-card transactions (Marzlin, McDermott). The most important *new* dependency Atruvia is building.

---

### II.10 Onboarding, Migration and Change

#### When two member banks merge

CONFIRMED FACT (frequency) + ANALYTICAL INFERENCE (process). 40–45 mergers/year require technical migration. The standard process consolidates the two banks' agree21 tenants into one — migrating accounts, products, roles and history to the surviving institution's configuration over a weekend cutover. Because both already run agree21, this is a *tenant merge*, far simpler than an inbound external migration.

#### How a new non-cooperative customer is onboarded (inbound migrations — verified)

CONFIRMED FACT:
- **Bank für Sozialwirtschaft:** contract 8 June 2021, go-live 23 April 2023 (~2-year programme, 200+ bank staff, ten sub-projects), migrating off a self-built SAP-based system in place since 2006, having evaluated SAP HANA as the alternative.
- **UmweltBank:** ~18 months' preparation, go-live October 2023; drivers were growth, changed customer expectations and regulation; chose Atruvia for a "standardisierte und am Markt erprobte" integrated solution.
- **National-Bank Essen:** replaced a system in use since 1996, ~30 applications consolidated, ~two-year project, completed October 2024.
- **M.M. Warburg:** announced; migrating off Sopra Steria's Corbas MBS; the bank's own statement: "das jetzige Kernbanksystem [wird] perspektivisch nicht mehr weiterentwickelt … ein Anbieterwechsel ist also zwangsläufig notwendig."
- **Sparda-Banken:** all 11 now on/moving to Atruvia. Four (Hamburg, Berlin, Hannover, Südwest) already used it; the other seven abandoned a joint Sopra Steria build and switched — Augsburg/Ostbayern first (spring 2024), Sparda-Bank West completing 2025; group fully on Atruvia by 2026. Notably, Verbandschef **Florian Rentsch** conceded that at the four already-migrated Sparda-Banken there had been customer losses "im signifikanten Bereich" during the switch — a rare, named, candid negative data point on migration disruption.
- **Bankhaus C.L. Seeliger:** a further external win (Finanz-Szene).

#### The exit question (Priority Gap 5) — critical

**Has any bank ever left?** CONFIRMED FACT — **YES, one prominent case: the Deutsche Apotheker- und Ärztebank (Apobank)** migrated *away* from Fiducia/GAD to Avaloq over the 2020 Pentecost weekend. It was a **debacle**: transfers and basic services failed, customers were furious, and Apobank-CEO Ulrich Sommer publicly blamed Fiducia GAD for having told the bank only in early 2018 that Avaloq "nicht auf den Hardwaresystemen der Fiducia laufen könne" and that a Mischbetrieb was "nicht erwünscht." This is the exception that proves the rule: the one clear exit was painful and disruptive. Separately, **BMW Bank** and others chose *not* to join Atruvia (going to FIS Kordoba) — but that is *non-adoption*, not exit.

**Is exit practically possible for a cooperative bank?** **ANALYTICAL INFERENCE (high confidence): effectively no.** A Volksbank cannot leave because (1) it is an *owner* of Atruvia; (2) the entire cooperative ecosystem (DZ Bank clearing, Union Investment depots, R+V, VR Payment cards, BVR reporting, Wero) is integrated through agree21; (3) there is no alternative provider offering the cooperative-specific integrated solution; (4) the Apobank precedent shows migration away is high-risk. The switching options that exist (FIS, Avaloq, Sopra Steria) serve *private* banks, and the market trend is *toward* Atruvia (Sparda, UmweltBank, National-Bank, Warburg), not away.

**Contractual notice/exit-support:** standard notice periods and exit-support terms are **UNKNOWN** (contracts confidential), but **DORA Article 30 now mandates exit strategies and exit-support clauses** in ICT outsourcing contracts — so formal exit provisions must exist on paper even though practical exit is near-impossible for cooperative members.

---

### II.11 Non-Cooperative Customers and Third-Party Sales

CONFIRMED FACT. Products sold outside the cooperative sector:
- **Core banking (agree21)** to ~190 private banks and specials, plus new external wins (Bank für Sozialwirtschaft, UmweltBank, National-Bank Essen, M.M. Warburg, Bankhaus C.L. Seeliger, the Sparda group).
- **IT-outsourcing** (mainframe/virtualisation scale) to banks and *other industries* including the **ADAC**.
- **parcIT okular-Tools** to non-GFG banks (via Basis-Abo).
- **Ratiodata** managed services / **GWS** ERP to non-bank customers.

**How much revenue comes from outside the captive base?** **UNKNOWN precisely** — no product- or customer-type split is published. ANALYTICAL INFERENCE: still a **minority** but **the fastest-growing** part. Evidence: Atruvia's 2025 AG revenue growth to knapp €1.9bn (+11.5%) was attributed "hauptsächlich durch neue Kunden" (Atruvia, via IT-Finanzmagazin, HV 2026) — i.e. external wins, since the cooperative base is shrinking in count. GB2021 already noted intensified dialogue with private banks and IT-outsourcing scale effects.

**Genuine growth strategy or marginal by-product?** **Conclusion: a genuine, deliberate growth strategy.** With the cooperative base saturated and consolidating, external migrations + value-deepening are Atruvia's only two organic growth vectors. The active pursuit of Sparda, Warburg, Seeliger and the Bank für Sozialwirtschaft shows a new-logo motion, not opportunism. But the captive base remains the overwhelming majority of revenue.

---

### II.12 Failure and Exception Paths

#### Full outage/incident history (Priority Gap 10)

CONFIRMED FACT — the reconstructed record:

| Date | Event | Scope | What it revealed |
|---|---|---|---|
| **May–Aug 2018** | BaFin §44 special inspection (via Volksbank Jever) | Fiducia & GAD | "Geharnischter Report," ~15 Kritikpunkte: weak Bankensteuerungssystem development, inadequate Berechtigungsmanagement, poor IT-outage precautions. |
| **10 Jun 2020** | FinTS/CAMT52 special-character bug | FinTS umsatz retrieval | Interface fragility; minor. |
| **9 Nov 2020** | System-changeover error | ~150 of 840 banks (NRW/north); online banking + SB-terminals | First big post-merger incident; Krisenstab convened; change-related fragility one year into unified operations. |
| **3 Jun 2021** | DDoS attack | Broad (Hessen/RLP/BW); online + app | External attack; SB-terminals partly usable. |
| **DDoS (Feiertag)** | DDoS on Karlsruhe then Münster data centres | Online banking + banking websites sporadic/unreachable | Both core sites can be targeted; cash supply via SB-terminals maintained. |
| **29 Nov 2023** | Central-system outage | **Up to 520 of ~700** cooperative banks (southern Germany); transfers, account overview, Umsatz display | Largest disclosed blast radius; "Sicherheit der Daten … weiterhin gewährleistet." |
| **7 Jul 2026** | Software error in central systems | **~490 banks** (southern Germany) from ~08:00; app/online switched off to relieve systems; bank websites down 09:47–10:38; resolved 13:20 | App/online *deliberately* switched off; users warned not to resubmit (duplicate risk); FinTS/HBCI also hit. |

**Also relevant (Atruvia-adjacent):** the **Apobank 2020 Avaloq migration debacle**, for which Apobank publicly assigned Fiducia GAD partial blame (II.10).

#### Who owns the problem, and the liability chain

**ANALYTICAL INFERENCE + CONFIRMED FACT (mechanism):**
- **Operationally**, Atruvia owns the fix (Krisenstab, status comms to banks).
- **Regulatorily and toward the end customer**, the **member bank owns the problem** — §25b KWG keeps responsibility with the bank; the end customer's claim is against the bank, not Atruvia. This is why Atruvia stays invisible even during a 520-bank outage.
- **Contractual liability / service credits between Atruvia and banks:** SLAs, availability commitments, service-credit and liability-cap terms are **UNKNOWN** (Priority Gap 2 — contracts confidential). Structurally, MaRisk AT 9 and **DORA Article 30** require the outsourcing contracts to contain service levels, audit rights, incident-reporting and exit clauses — so SLAs must exist, but their figures are not public.
- **Reputational consequence:** falls on the *banks* (their brand fronts the app/website) — a governance lever, since the owner-banks bear the reputational cost of Atruvia's failures, sharpening their interest in resilience.

#### The systemic-risk observation

**ANALYTICAL INFERENCE (important).** The single multi-tenant platform that delivers Atruvia's economics also concentrates risk: one software error took out ~490–520 banks simultaneously (2023, 2026). Atruvia was **not** designated a DORA Critical ICT Third-Party Provider (18 Nov 2025) even though a single incident can disable ~500 German banks — a defensible reading is that the ESAs supervise the *cloud/hardware* layer (IBM designated) while Atruvia is captured indirectly via its banks. A genuine regulatory-perimeter question the report flags rather than resolves.

---

### II.13 Product-Market Evolution

CONFIRMED FACT (trajectory):
- **Booking cooperative → early cores.** Fiducia (founded 1924) and GAD built successive cores across the 1960s–2000s; predecessor systems in the lineage include the batch/booking era, then GEBOS/GENOS/RUBIN/bank21 (north) and NBS/BB3/agree (south).
- **Two platforms (2015 merger):** "agree" (south) and "bank21" (north) coexisted post-merger.
- **agree21 consolidation (to 2019–2020):** all banks onto one core primarily based on agree; **bank21 retired**.
- **Digital channels (2021–):** new OnlineBanking, rebuilt VR Banking App, VR SecureGo plus, Omnikanalplattform, BankingWorkspace.
- **2021 repositioning:** from "IT operator" to "**Digitalisierungspartner**"; rename Fiducia & GAD → **Atruvia** (1 Sep 2021).
- **Expansion into adjacencies:** HR (Peras/geno.HR), BPO (Serviscope), analytics (TRUUCO/SmartData), AI (plainGPT/genoGPT, KI-Kompetenzcenter), and **card processing** (VR Payment issuing from 2027).

**Coherent or accretive drift?** **Conclusion: largely coherent, with two caveats.** The core→channels→steering→analytics→AI stack is a coherent vertical deepening of the same customer. The card-processing move is coherent *bundling*. The genuinely adjacent bets — GWS ERP (non-bank), ADAC-type IT-outsourcing, and parts of the subsidiary ring — are closer to **opportunistic diversification** justified mainly by mainframe scale economics. Net: coherent platform strategy at the centre, mild accretive drift at the edges.

---

### II.14 Volume II Reconstruction

**(1) Full Product/Service Architecture map.** Core (agree21 on IBM Z/IMS/Db2) → Platform (Omnikanalplattform, EGP/agree21Finanzen) → Employee channel (BankingWorkspace/BAP) + Customer channels (OnlineBanking, VR Banking App, VR SecureGo plus, ATMs, FinTS/PSD2) → Payments/cards (SEPA/SCT Inst via DZ Bank; girocard/debit/credit issuer processing → unified at Atruvia from 2027) → Steering/analytics/AI (VR-Control/okular via parcIT; TRUUCO SmartData; genoGPT) → Subsidiary ring (Ratiodata, Peras, Serviscope, BMS/fincompare, FORUM, GWS, ECON, Accesa/RaRo, Lucke).

**(2) Two-Tier Customer Map.** Tier 1: ~670–730 cooperative banks (owner+buyer+governor) + ~190 private banks/specials + non-bank (ADAC). Tier 2: tens of millions of end customers (contract with bank; Atruvia invisible; bank = GDPR controller, Atruvia = processor).

**(3) Customer-Segment Map.** By type (VR / Sparda / PSD / church / Apobank[exited] / private / non-bank); by legacy (north/south — eliminated at core); by size (few large, many small); by adoption depth (core-only → +steering/M365 → +BPO/analytics/AI).

**(4) Jobs-to-Be-Done Matrix.** Banks: remain independent (primary) > regulatory compliance > digital competitiveness > cost-income > scale economics. End customers: reliable daily banking + payments; parity-plus features (84.5 vs 92.6 Sparkassen).

**(5) Service-Delivery Flow Diagram (six flows).** A Transaction (bank principal, Atruvia processor, DZ Bank clearer); B Data (bank controller, Atruvia processor, AVV); C Software-release (pilot→Serienpilot→Serienmigration, AT 8.2 acceptance); D Money (Umlage/Leistungsentgelte, specifics confidential); E Support/incident (Serviceline fronted by bank; Krisenstab); F Regulatory-responsibility (§25b KWG stays with bank; DORA Art. 30 clauses).

**(6) Transaction Processing Maps.** Eight events traced in II.6, each with system/entity/data/control/failure.

**(7) Channel Architecture.** Seven channels; low individual white-labelling; shared multi-tenant app.

**(8) Pricing and Cost-Allocation Model.** Basispaket + Festpreis + infrastructure + IT-Sonderumlage (€60m/yr banks) + Digitalisierungsumlage (€30m→€60m→€90m) → transitioning to nutzenbasierte pricing; 4% Zielrendite (4.7% achieved 2025); self-funding over dividends; per-unit prices UNKNOWN.

**(9) Product Dependency Map.** agree21 as the hub; tight core→layer dependencies; subsidiary attach-rate strategy; VR Payment creating a new account+debit+credit bundle lock-in from 2027.

**(10) Migration/Change Process.** Tenant-merge (bank mergers, 40–45/yr) vs external migration (~18–24 months, e.g. Bank für Sozialwirtschaft, UmweltBank, National-Bank, Sparda). Exit near-impossible; Apobank the sole painful precedent.

**(11) Third-Party Revenue Assessment.** Minority but fastest-growing; 2025 growth "hauptsächlich durch neue Kunden"; deliberate strategy; split UNKNOWN.

**(12) Failure/Exception Map.** 2018 BaFin report; 2020 changeover + DDoS; 2021 DDoS; 2023 (≤520 banks); 2026 (~490 banks). Bank owns regulatory/customer problem; SLAs exist but confidential; systemic single-point-of-failure concentration.

**(13) Product-Market Evolution timeline.** Booking cooperative → GEBOS/GENOS/RUBIN/bank21 & NBS/BB3/agree → agree21 (2019–20) → digital channels (2021) → Digitalisierungspartner + Atruvia rename (2021) → HR/BPO/analytics/AI → card processing (2027).

**(14) Key Unknowns.** Per-unit prices; total Leistungsentgelte per bank; SLA/service-credit/liability-cap figures; contractual exit terms; captive-vs-external revenue split; per-product revenue; exact SCT Inst reach; internal pre-2027 card-platform architecture; Verimi product economics; dividend policy specifics; whether "six data centres" (Grokipedia) is real vs the confirmed "four"; reconciliation of group-revenue figures (see caveat below).

**(15) Ten Most Important Conclusions.**
1. **agree21 is the true core product and the master lock-in** — everything attaches to it and no cooperative bank can leave it.
2. **The real customer is the cooperative sector as an institution**, expressed through ~700 owner-buyer-governor banks; the end customer is a beneficiary, not the customer.
3. **What a member bank actually buys is the ability to remain an independent regulated bank** — software + compliance + scale + risk transfer bundled.
4. **Pricing has historically been under-market (thin margins), not rent-extractive** — the 2025 pivot to a 4% Zielrendite + usage-based pricing deliberately corrects under-investment.
5. **Exit is effectively impossible; the one clear exit (Apobank) was a debacle** — lock-in is near-absolute for members.
6. **A single multi-tenant platform is both the economic engine and the systemic risk** — one error hits ~500 banks (2023, 2026).
7. **The VR Payment card consolidation (2027) is the most important new lock-in** — account+debit+credit on one Atruvia platform.
8. **Governance is majoritarian/consensus via BVR committees, the BSP (36/39 initiatives), Kompetenzteams and the SPP** — individual small banks have negligible direct roadmap power.
9. **The digital offering is competitive but trails the Sparkassen** (VR Banking App 84.5 vs 92.6) — the owner-consensus model is fast to roll out but slow to lead.
10. **External sales are the deliberate growth vector** as the captive base consolidates (40–45 mergers/yr; count 820→~670).

#### The five closing questions answered

- **True core product?** **agree21** — the mainframe core banking process; every other product is an attachment.
- **Strongest lock-in mechanism?** Today: **agree21 + cooperative-ecosystem integration** (ownership + DZ Bank clearing + Union/R+V + BVR reporting). Strengthening fastest: the **unified card platform from 1 Jan 2027**.
- **Best economics?** **The multi-tenant platform releases** (one code line → ~700 banks) and the **near-mandatory steering software (parcIT/VR-Control)** — high attach, low marginal cost. IBM-scale mainframe outsourcing to third parties (incl. ADAC) also earns scale rents.
- **Strategically important despite being small today?** **genoGPT/the AI portfolio** and **Wero** — small revenue now, decisive for future competitiveness and defence against Big Tech/neobanks.
- **Who is the real customer?** **The cooperative sector as an institution** — operationalised as the ~700 member banks that own, pay for and govern Atruvia. The bank's end customer is the user Atruvia designs *for* but never contracts *with*.
- **What precisely does a member bank buy?** Not merely software. It buys **regulatory compliance it need not build, scale economics it could not achieve alone, risk transfer of IT execution (though not of regulatory responsibility), and — decisively — the ability to remain an independent bank at all.** The software is the delivery vehicle; the licence-to-remain-a-bank is the product.

---

#### Data caveat on group-vs-AG revenue (flagged, not silently resolved)
Sources give different revenue bases. **Atruvia AG (parent):** ~€1.4bn (2022), ~€1.5bn (GB2021: €1,496.1m), knapp €1.9bn (2025, +11.5%). **Group/Konzern:** ~€1.77bn (older IBM/press), ~€2.2bn (2024, Volume I), and **€2.5bn per GB2025** (with 97m accounts, ~10bn transactions). Finanz-Szene separately reported a group figure "erstmals mehr als 2 Mrd. Euro … 2,001 Mrd. Euro" with a €50m operating result — likely an interim/rounded or different-perimeter figure. The most authoritative current group number is the **GB2025 figure of €2.5bn**; the €2.0bn and €2.2bn figures are earlier-period or narrower-perimeter and should not be treated as current. This discrepancy is preserved rather than averaged.

*End of Volume II. Volume III not begun, per instruction.*


---

# Part III — Operations, Technology, Data & Organisational Infrastructure

### VOLUME III: Operations, Technology, Data & Organizational Infrastructure

### TL;DR
- **Atruvia's centre of gravity is an IBM Z / IMS / Db2 / COBOL core** (eight IBM z15 systems hosting twelve IMS systems, ~80bn technical transactions/yr, 12,000 tps peaks, ~400m Java transactions/day) wrapped in ~1,200 Java microservices on Red Hat OpenShift. The 19 November 2025 IBM z17 deal re-underwrites this architecture for years — meaning modernisation is being executed as **in-place refactoring, not replacement**.
- **The scarce resource is compute-plus-reliability on four twin-site data centres** (two each in Karlsruhe and Münster). A single central software fault takes ~490–520 of ~700 banks offline simultaneously (proven Nov 2020, Nov 2023, July 2026), yet Atruvia was **NOT** designated a DORA Critical ICT Third-Party Provider while its supplier IBM **was** — a genuine national systemic-supervision gap it shares with Finanz Informatik.
- **Atruvia's advantage is structural (captive ownership) and organisational (repeatable multi-tenant migration at scale) more than purely technological.** The moat is the agree21 multi-tenant core and the industrialised migration machine, not any single piece of software.

### Key Findings
1. The core banking estate is IBM z15 (→ z17) running z/OS, IMS (transaction manager + hierarchical DB) and Db2 for z/OS, with a large COBOL base now ~85% Java-enabled inside IMS via an IBM Semeru common runtime that lets 31-bit COBOL and 64-bit Java interoperate.
2. There are four high-security data centres — "jeweils zwei Rechenzentren in Karlsruhe und Münster" — resolving the four-vs-six ambiguity in favour of four.
3. Fraud detection is in-house AI since 2017: ~0.2–0.3% of transactions flagged, ~20% of flags are false positives, ~80% of unauthorised transactions prevented; banks (not Atruvia) own the regulatory decisions and losses.
4. The recurring outage pattern is a shared-central-path concentration risk; incident response has matured (July 2026 load-shedding) but the architectural root cause persists.
5. Finanz Informatik, the Sparkassen mirror, is larger (~€2.6bn revenue, ~114m accounts, >205bn technical transactions) and also IBM-mainframe-based and also not a DORA CTPP — the in-place-modernisation problem is sector-wide.

### Details

#### III.1 Operating Model
Atruvia is organised as an agile "Spotify-model" organisation. **CONFIRMED FACT** (Atruvia Newwork site; HR-Pioneers conference talk): the top units are **Service-/Geschäftsfelder** (each led by a Feld-Lead with both functional and disciplinary authority); below them sit **Tribes** (grouping squads around a product/service) with a **tandem leadership** split — a **Tribe Lead** (functional leadership, product ownership, budget) and a **People Lead** (disciplinary leadership, people development); **Squads** are the smallest end-to-end delivery units; **Chapters** cross squads within a tribe; **Guilds** span the whole company. A management layer was explicitly removed. Stated drivers (Atruvia HR-Pioneers talk): "Unterschiedlichste Qualitätsprobleme, eine niedrige Mitarbeiterzufriedenheit und vor allem eine geringe Kundenzufriedenheit."

Named units evidenced in job ads and press: Geschäftsfeld **Steuerungsbank** (Tribe Meldewesen), **Omnichannel** (Tribe BankingWorkspace und Vertriebslösungen; Chapter/Squad ContactCenter on Genesys Cloud CX), **Bankbasislösungen** (Tribe Prozessmanagement und Automation), **Daily Banking** (Tribe Bezahllösungen), **Data, Security & Identity** (led by Steffen Unterreiner), Servicefeld **Portfolio Steering and Pricing** (Tribe Pricing and Product Analytics), **Connected Solutions** (Tribe Collaboration Services — SharePoint/M365), and **Procurement** (CPO Regina Krüger-Wendel, ~40 staff in five squads including IT-Services, Business Services and Agiler Projekteinkauf).

| Function | Mandate | Evidence | Leadership |
|---|---|---|---|
| Core banking dev | agree21 IMS/COBOL+Java | CONFIRMED | Vorstand Bücker (Core Banking & Technology) |
| Platform/omnichannel | Omnikanalplattform, BankingWorkspace | CONFIRMED | GF Omnichannel |
| DC & mainframe ops | 4 DCs, IBM Z estate | CONFIRMED | UNKNOWN named lead |
| Release/change mgmt | technischer Jahresabschluss | CONFIRMED (Vol II) | — |
| Payment ops | SEPA, cards, DZ clearing | CONFIRMED | Vorstand Kaurin (Digital Banking) |
| Security (CISO/SOC) | InfoSec, fraud | PARTIAL (audIT; Data/Sec/Identity GF) | S. Unterreiner |
| Compliance/risk | MaRisk/BAIT implementation | CONFIRMED | Vorstand Wiegelmann (Fin/Reg/HR) |
| Data/analytics/AI | Smart Data, plainGPT/genoGPT | CONFIRMED | >70-person AI unit; AI Accelerator |
| Procurement | IT/business sourcing | CONFIRMED | CPO Krüger-Wendel |
| Service desk/Serviceline | end-customer + bank support | CONFIRMED | — |
| Subsidiaries | Ratiodata, parcIT, Peras, etc. | CONFIRMED (Vol I) | — |

Development capacity is augmented via **Accesa/RaRo** in Cluj-Napoca, Romania (see III.5, III.14).

#### III.2 Banking Operations — the processing lifecycle
**CONFIRMED FACT** (IBM case study "Atruvia AG", ibm.com/case-studies/atruvia-ag, May 2022): "eight IBM z15 systems across four data centers that process 80 billion core banking transactions annually, with peaks of 12,000 transactions per second," serving "some 81 million customer accounts." ~85% of core IMS transactions are Java-enabled = ~400 million Java transactions/day. This reconciles with the ~10bn business bookings/yr established in Volume II at a ratio of roughly 8 technical transactions per booking.

**Online/real-time vs batch.** **ANALYTICAL INFERENCE (strongly supported):** agree21 retains a classic mainframe **nightly batch window**. Direct evidence: the Fiducia & GAD "Tailored Fit Pricing" case study states the firm "decreased response times across our production systems by 5 percent and our nightly batch window by 25 percent." IBM's Java-in-IMS study confirms batch jobs run on IBM Z, consolidated from multiple platform schedulers to a single scheduler. A knowledgeable third-party (Borns IT blog) describes a **"frozen zone wg. Jahresabschlussarbeiten und Buchungsschnitt"** (change freeze for year-end close and the booking cut-off) around the year-turn.

**The technischer Jahresabschluss** is the marquee coordinated year-end close/release event (Vol II), planned change-frozen. The 29 December 2025 sector disturbance was attributed by informed commentary to year-turn special processing rather than routine change ("da laufen halt viele Dinge zum Jahreswechsel extra, die sonst nicht laufen").

**Multi-tenancy operations.** ~700 cooperative banks plus Sparda and private banks (and non-bank clients such as the ADAC) run as tenants on one agree21 instance set. The July 2026 (~490 banks) and Nov 2023 (up to 520 banks) incidents demonstrate that a central fault propagates to a large fraction of tenants at once — direct evidence that tenants share central processing paths rather than being fully isolated.

**Abnormal paths / Krisenstab.** **CONFIRMED FACT:** on 9 November 2020 a **system changeover** ("Systemumstellung") error hit 150 of 840/841 banks, disabling online banking and self-service/ATM devices; Fiducia & GAD convened a **Krisenstab** — the documented escalation mechanism for major incidents.

#### III.3 Mainframe Capacity, Compute & Data-Centre Operations (PRIORITY DEPTH)
**Data centres — resolved.** **CONFIRMED FACT:** Atruvia operates **four** high-security data centres — "Wir betreiben jeweils zwei Rechenzentren in Karlsruhe und Münster. Sollte einmal ein Rechenzentrum ausfallen, hat das für unsere Kunden keinerlei Auswirkungen" (Atruvia's own IT-Outsourcing page). The "six" claim is unsupported by primary sources; four is corroborated by IBM ("four data centers") and Wikipedia. The twin-site design implies active-active/hot-standby redundancy within each metro plus cross-metro DR. Karlsruhe↔Münster is ~350 km apart — too far for low-latency synchronous zero-data-loss replication; **ANALYTICAL INFERENCE:** intra-metro pairs are the synchronous/active-active layer, cross-metro is asynchronous DR. No RTO/RPO figures are published — **UNKNOWN**.

**Mainframe estate.** **CONFIRMED FACT** (IBM case study): **eight IBM z15 systems** across the four data centres, and **twelve IMS systems** — verbatim: "Twelve IMS systems with approximately 200 million instructions per processor second (MIPS) support these business-critical transactions." Eight physical z15 machines host twelve logical IMS systems. **Current generation:** the 19 November 2025 Atruvia–IBM agreement commits Atruvia to **IBM z17** (announced April 2025, Telum II processor) "as a cornerstone to support its mission critical operations including the core banking system." The public record jumps z15 (2022 case study) → z17 (2025 deal); a **z16 interim is likely** (z16 was available from 2022) but is not separately documented — label the z16 interim **UNKNOWN**.

**Capacity management.** **CONFIRMED FACT:** peaks of ~12,000 transactions/second (IBM). The Tailored Fit Pricing project was explicitly motivated by workload volatility from PSD2 and instant payments — the goal was to "accommodate new workload peaks in a more cost-effective manner." **IBM Turbonomic** (workload optimisation/automation) and **Apptio** (cost transparency) are named in the November 2025 deal for "vendor independence" and dynamic workload optimisation.

**Cost structure of compute.** **CONFIRMED FACT:** adoption of IBM **Tailored Fit Pricing** — a consumption-based licensing model for IBM Z software replacing the traditional peak-MSU monthly-license-charge (MLC) model. Claimed results: 25% smaller nightly batch window, 5% faster response times. There is also a documented economic incentive to shift Java workloads to **zIIP** specialty processors (lower licensing fees; Java consumes more MIPS than COBOL, but net cost is lower). Internal allocation to member banks has moved to **usage-based (nutzenbasierte) pricing** (Vol II); the precise mechanics are **UNKNOWN**.

**Hybrid-cloud programme.** **CONFIRMED FACT:** **Red Hat OpenShift** hosts the ~1,200 distributed Java microservices and is designated in the Nov 2025 deal as "the basis for hybrid cloud scenarios … flexibility and independence from individual cloud providers." IBM Cognos (bank reporting) and Planning Analytics (Sales Cockpit) run on OpenShift. Data and keys remain "always fully controlled in its own data centers" using **HashiCorp Vault** and IBM storage — i.e., a **sovereign, on-premise-first hybrid cloud**, not a public hyperscaler. At the 2026 Hauptversammlung, hybrid cloud and AI (including "agentische KI") were framed as making VR banks "skalierbar." Energy/cooling/PUE figures are **UNKNOWN**; Nachhaltigkeit is a stated strategic corporate goal.

#### III.4 Technology Architecture (PRIORITY DEPTH)
**Core layer (CONFIRMED, IBM case study):** IBM Z (z15 → z17); z/OS; **IMS** = both transaction manager (IMS TM) and hierarchical database (IMS DB) managing the ~80bn transactions; **Db2 for z/OS** relational store, connected from Java via **JDBC**; a large in-place **COBOL** estate "permanently in evolution" (lines-of-code/age **UNKNOWN**). The **Java-on-Z "common runtime"** is based on **IBM Semeru Runtime Certified Edition for z/OS, Version 11**, co-developed with IBM before general availability. It lets **31-bit COBOL** interoperate with **64-bit Java** inside IMS, invoking **IBM MQ for z/OS** and connecting to Db2 via JDBC. Critically, it removed the per-component "compensation" (rollback) logic previously needed for distributed operations, and enabled colocation (Atruvia reports 3× faster performance for data-intensive apps — "the best I/O is no I/O"). ~85% of core-banking IMS transactions are Java-enabled.

**Integration/API layer:** ~1,200 Java microservices consume core-banking services via a **proprietary API layer** (CONFIRMED), hosted on **Red Hat OpenShift** on x86 Linux (CONFIRMED); IBM MQ confirmed as messaging. Whether z/OS Connect or WebSphere Liberty fronts the mainframe-side APIs is not documented — **UNKNOWN**. A developer "will not know if they are calling Java services or original IMS transactions" (Pascal Meyer, Senior Enterprise Architect, Atruvia).

**Platform layer:** the **Omnikanalplattform** — multi-tenant, ~300 available processes (Vol II); ~45 digital fallabschließende Self-Services live for customers (2024 HV). Process modelling via **agree21ECON** (Vol II) and ADONIS (evidenced in partner process documentation). The BPM/workflow engine name is **UNKNOWN**.

**Client layer:** **BankingWorkspace** is browser-based — **CONFIRMED stack from job ads:** **Angular** (ads reference "Angular ab Version 21"), TypeScript/Web Components, PWA, NGRX, running on OpenShift/Kubernetes, built with GitLab pipelines, Figma for design, Genesys Cloud CX for the contact-centre variant. The legacy **agree21BAP** persists in a coexistence phase; some apps (e.g. CRM) are maintained twice; Coenen: "der aktuelle Zustand ist etwas zäh" (Vol II). The **VR Banking App** framework is **UNKNOWN** from primary sources (job ads reference Angular/Ionic for some apps but not specifically the VR Banking App). **OnlineBanking** and the **FinTS/HBCI servers** are confirmed central services (the June 2020 CAMT52/FinTS special-character bug and the July 2026 FinTS disruption both hit these directly).

**Data layer:** operational stores in Db2/IMS on Z; analytics via **Smart Data**; IBM Cognos on OpenShift for bank reporting. Data lake/warehouse and streaming specifics are **UNKNOWN**.

**Delivery/engineering (job ads — the best window):** **CONFIRMED** tooling — **GitLab** (source control + deployment pipelines), **Jenkins**, **Docker/Kubernetes on OpenShift**, Jira, Confluence, Eclipse/VSCode/IntelliJ; **Java/Spring/Spring Boot** backend, **Angular** frontend; Scrum/Kanban, pair programming and code reviews. Testing a change destined for 700 banks uses the pilot→Serienpilot→Serienmigration ladder (Vol II). Feature-flag specifics are **UNKNOWN**.

**Reliability:** observability/monitoring specifics are not published; incident management runs via Krisenstab; twin-site failover is confirmed at the principle level.

#### III.5 Build vs Buy vs Nearshore
| Capability | Model | Notes |
|---|---|---|
| Core banking (agree21) | **BUILD** | Proprietary IMS/COBOL+Java — the crown jewel |
| Mainframe HW/SW | **BUY (IBM)** | z17, z/OS, IMS, Db2, MQ, Semeru, Turbonomic, Apptio |
| Container platform | **BUY/OSS (Red Hat OpenShift)** | Hybrid-cloud basis |
| Secrets/keys | **BUY (HashiCorp Vault)** | On-prem, self-controlled |
| Productivity | **BUY + managed BUILD (Microsoft M365)** | agree21M365 = managed service on a bought platform |
| Contact centre | **BUY (Genesys Cloud CX)** | Job ads |
| Fraud/AML | **BUILD (in-house AI since 2017)** | Autoencoders/neural nets |
| AI/LLM | **BUY model + BUILD wrapper** | plainGPT is **based on OpenAI models** (Börsen-Zeitung: "Er basiert auf Modellen der ChatGPT-Mutter OpenAI"); genoGPT adds bank-internal knowledge (RAG). The "no open-internet private cloud" is a governance wrapper around a vendor model, not necessarily self-hosted open-weights |
| Reporting/planning | BUY (IBM Cognos, Planning Analytics) | Nov 2025 deal |
| Dev capacity | **NEARSHORE (Accesa/RaRo, Romania)** | Cluj-Napoca |

Regulatory implications: under **DORA Article 30**, member banks' contracts with Atruvia must contain resilience/audit/exit clauses; because **IBM is a designated CTPP** and Atruvia is not, IBM sits under direct ESA oversight while Atruvia is supervised only indirectly via its bank customers (§25b KWG). IBM Z lock-in is deep and deliberately re-committed in November 2025.

#### III.6 Payment Infrastructure Software
**CONFIRMED FACTS:** Atruvia handles SEPA credit transfers, SCT Inst (instant payments were an explicit driver of the Tailored Fit Pricing capacity project), FinTS/HBCI initiation, and card processing. DZ Bank is the clearing/settlement counterpart (Vol I/II). The June 2020 incident (CAMT52 special-character bug) shows the account-statement/reporting path. The 7 July 2026 warning — "Sendet Überweisungen nicht mehrfach ab … Prüft zuerst, ob der Auftrag trotzdem ausgeführt wurde" (NETZWELT Störungskarte, updated 21 July 2026) — is direct evidence that duplicate-submission (idempotency) is a live operational risk under degraded conditions.

**Card platform transformation (CONFIRMED).** Effective **1 January 2027**, Atruvia acquires the **Issuing Processing** business of VR Payment (DZ Bank subsidiary), taking over not only debit-card issuing processing but also **credit-card processing** (previously at VR Payment). Target: a single **integrierte Kartenplattform** unifying Girokarte, Debitkarte and Kreditkarte processing on one platform. VR Payment refocuses on merchant/acquiring/POS-Netzbetrieb. Bundeskartellamt case **B9-75/26**, filed 15 July 2026; reportedly internal name "Projekt Dragon" (unconfirmed). McDermott (adviser) notes "a significant portion of all credit card transactions in Germany is processed through Atruvia's systems." The detailed target state-machine/rail architecture is **UNKNOWN**.

#### III.7 Ledger and Core Banking Data Architecture
**CONFIRMED** at architecture level: balances/postings are held in **Db2 for z/OS** (relational) with transaction management in **IMS**. Beyond this the internal data model is **not public — UNKNOWN**. Specifically unknown: whether tenants are separated by (a) separate databases, (b) separate schemas, or (c) tenant-key partitioning within shared tables. **ANALYTICAL INFERENCE:** the fact that a single central fault simultaneously hits ~490–520 banks argues for **shared logical infrastructure with tenant keys / shared subsystems** rather than 700 physically isolated databases (which would fail bank-by-bank, not en masse). Double-entry structure, pending-vs-settled state, reversal mechanics, and how bank mergers physically consolidate two tenants' ledgers are all **UNKNOWN** — Atruvia has published nothing. To close the gap one would need the agree21 physical data model, the tenant-partitioning key, and the merger-consolidation runbook.

#### III.8 Reconciliation Architecture
Atruvia has published essentially nothing on its internal reconciliation systems — largely **UNKNOWN**. Inferable: reconciliation must occur between the agree21 core and (a) SEPA/SCT Inst rails, (b) card schemes (increasingly in-house post-2027), (c) DZ Bank clearing/settlement, and (d) banks' own regulatory reporting. Regulatory importance: reconciliation breaks feed directly into each member bank's §25b KWG outsourcing liability and MaRisk AT 9 responsibility — the bank, not Atruvia, is the regulated entity that must answer for a settlement mismatch. **ANALYTICAL INFERENCE:** the technischer Jahresabschluss functions partly as a systemwide reconciliation/close checkpoint. A reconciliation failure operationally means blocked/duplicated postings (cf. the July 2026 duplicate-transfer warning), financially means intraday exposure at DZ Bank clearing, and for the member bank means a reportable §25b/MaRisk incident.

#### III.9 Data Architecture and Governance
**CONFIRMED legal structure:** Atruvia is a **GDPR processor (Auftragsverarbeiter)**; each member bank is the **controller (Verantwortlicher)**, bound by an **Auftragsverarbeitungsvertrag (AVV)**. This is the pivotal constraint on any "data flywheel."

**The data-flywheel question (important).** Atruvia's systems see the transaction data of ~97m accounts. Assessed rigorously: as a **processor**, Atruvia may only process personal data on documented controller instructions and for the contracted purpose; it cannot lawfully repurpose cross-tenant personal data for its own commercial benefit without a legal basis. A genuine cross-bank personal-data flywheel is therefore **legally constrained**. However, two legitimate value loops exist and are evidenced: (1) **fraud detection** — models trained across the network on transaction patterns (a permissible security purpose, and one where scale is a real advantage); (2) **Smart Data / analytics products** sold back to banks (each bank exploiting its own data with Atruvia's tooling). **CONFIRMED:** TRUUCO (Vol I) and Smart Data provide model/analytics capability. The strategic asset is thus **network-scale fraud/behavioural modelling and productised analytics**, not a free-floating data monopoly. Technical segregation across ~700 tenants is **UNKNOWN** (see III.7); retention/lineage/access-control specifics are **UNKNOWN**.

#### III.10 Fraud and Financial-Crime Technology
**CONFIRMED FACTS:** Atruvia has used AI/ML for fraud detection since **2017** ("flächendeckend"), positioning itself as a Fraud Detection/Management pioneer. Mechanism (Atruvia Fraud Manager Andreas Hermann, 2022): self-learning algorithms flag suspicious transactions in real time for holding/blocking; **0.2–0.3% of transactions are classified suspicious**; on manual review, **~1 in 5 flags is a false positive** (~80% precision on flags); the solution **"verhindert 80 Prozent aller unberechtigten Transaktionen."** Evolution: decision-tree models are being extended toward **neural networks / autoencoders** that model normal human behaviour to detect anomalies.

**Division of labour (critical).** Atruvia builds and runs the **systems**; the **member bank** retains regulatory responsibility — GwG/KWG obligations, transaction-monitoring calibration, decisions, and filing of Verdachtsmeldungen (SARs) to the FIU. A flagged transaction is reviewed by a **trained bank employee** ("ein geschulter Mitarbeiter"), not auto-rejected. Sanctions/PEP screening and identity/KYC are bank-facing regulated functions supported by Atruvia tooling. **Who bears losses:** ultimately the bank and/or customer per the payment-services liability regime; Atruvia bears the systems-reliability and detection-quality responsibility, not the direct fraud loss. Both rule/threshold scenarios and ML anomaly detection are used.

#### III.11 Security Architecture
**The 2018 BaFin finding and audIT remediation (CONFIRMED, richly sourced).** A BaFin §44 KWG special inspection ran **May–August 2018** (conducted via Volksbank Jever); the report was delivered **spring 2019**: **15 Feststellungen, of which 3 schwerwiegend (severe)**. Fiducia & GAD had pre-emptively launched programme **"audIT"** in autumn 2018 (led by Andreas Abel, head of Risk/Compliance/Security/Legal — "Das war schon wie ein Schlag in die Magengrube"). Documented weak areas: **Berechtigungsmanagement** (access/authorisation management), **IT-Ausfallvorsorge/Notfallmanagement**, Auslagerungsmanagement, Informationssicherheitsmanagement, and the Bankensteuerungssystem. Remediation: **Netzwerksicherheit** was completed; **Berechtigungsmanagement** was hardest — "wesentliche Abarbeitungspunkte" by end-2021 but "restliche Aktivitäten … über 2021 hinaus," with verbund timelines cited toward 2023. Governance fallout: CEO **Klaus-Peter Bruns** and deputy **Carsten Pfläging** departed; a BVR-level Lenkungskreis oversaw progress. (The task instruction's "audIT completed 31 December 2021" should read "material points reached by end-2021, residual work beyond" — the evidence shows Berechtigungsmanagement work extended past 2021.)

**Physical/DC security.** Four Hochsicherheitsrechenzentren; a Baden-Württemberg Sicherheitspreis (2007, silver medal, as Fiducia); Notstrom/battery/aggregate backup proven in a 2007 Durlach 75-minute grid failure (ATMs kept running through the outage).

**Encryption/key management.** IBM Z **pervasive encryption** (from z14/z15) and, on z16/z17, **quantum-safe cryptography** (lattice-based CRYSTALS-Kyber/Dilithium, Crypto Express8S) — the Nov 2025 deal explicitly cites "confidential computing and quantum-safe encryption." Keys held in **HashiCorp Vault**, self-controlled in Atruvia's own data centres.

**DDoS.** **CONFIRMED:** 3 June 2021 and subsequent DDoS attacks on the Karlsruhe then Münster data centres caused multi-hour outages (Finanz-Szene). Specific mitigations adopted are not detailed publicly — **UNKNOWN**.

**Certifications.** Atruvia's specific ISO 27001 / IDW PS 951 / ISAE 3402 scopes and KRITIS/BSI (§8a BSIG) status are **not confirmed in the sources reviewed — UNKNOWN**, though such attestations are the standard basis on which member banks satisfy EBA outsourcing-guideline Rz. 93 and MaRisk AT 9 for a provider of this criticality, and Atruvia almost certainly holds ISAE 3402/IDW PS 951 reports for its customer banks' auditors. This should be verified against Atruvia's Geschäftsbericht/technical annex.

#### III.12 Reliability Engineering (PRIORITY DEPTH) — Incident Post-Mortems
Why Atruvia's reliability bar is exceptional: a single central fault disables ~500 banks at once and is national news. Availability SLOs are not published — **UNKNOWN**. The **batch window** is a hard reliability constraint (a failed batch delays day-start across all tenants). **Duplicate-payment prevention** is a proven live risk (July 2026 warning).

| Date | Scope | Proximate cause | Systemic cause | Aftermath/change |
|---|---|---|---|---|
| May–Aug 2018 | Firmwide | BaFin §44 findings (15/3 severe) | Weak Berechtigungsmanagement, IT-Ausfallvorsorge post-merger | audIT; leadership change; remediation to ~2023 |
| 10 Jun 2020 | FinTS users | CAMT52 special-character bug | Input-validation defect in statement path | Fixed same day |
| 9 Nov 2020 | 150 of 840 banks | Systemumstellung error | Change-execution risk on shared infra; online + SB/ATM hit | Krisenstab; resolved during day |
| 3 Jun 2021+ | Firmwide (KA→MS DCs) | DDoS attack | Internet-facing edge exposure | Mitigations (undisclosed) |
| 29 Nov 2023 | up to 520 of ~700 | Central fault (S. Germany) | Shared central processing path | "Hochdruck" fix; Handelsblatt: "Die Sicherheit der Daten von Kunden ist zu jeder Zeit weiterhin gewährleistet" |
| 7 Jul 2026 | ~490 banks | Central software error from ~08:00 | Shared central path; load amplification | App/online banking switched off to shed load; websites down 09:47–10:38; resolved 13:20; duplicate-transfer warning |

**Pattern assessment.** The recurrence is a **shared-central-path concentration risk**: the same failure mode (a central change or software fault propagating to hundreds of tenants simultaneously) recurs across 2020, 2023 and 2026. The 2018→2020 sequence shows the remediation programme did not prevent a 2020 changeover failure. The **7 July 2026 response is more mature** — deliberate load-shedding (switching off app/online banking to protect the core), explicit user guidance on duplicate prevention, and a bounded recovery timeline (resolved by 13:20) — indicating **improved incident-response playbooks** even as the **underlying architectural concentration risk persists**. Net verdict: **incident-response has improved; the single-central-path vulnerability has not been eliminated** — stasis on the root cause, improvement on mitigation.

#### III.13 Infrastructure Resilience and Concentration Risk
Single points of failure: (1) the **shared agree21 central processing path** (empirically, a ~490–520-bank blast radius); (2) **IBM Z / IBM** as sole core-platform vendor (lock-in re-committed Nov 2025); (3) the internet-facing edge (DDoS-exposed). Geographic redundancy (four DCs, twin metros) does not protect against a **logical/software** fault replicated across sites — which is exactly the recurring failure mode.

**The DORA perimeter gap (systemic question).** **CONFIRMED:** on 18 November 2025 the ESAs (EBA, EIOPA, ESMA) designated **19 CTPPs** under DORA Article 31(9), including **IBM** ("International Business Machines Corporation (IBM)", Lead Overseer EBA), AWS, Microsoft, Google, Oracle, SAP, SWIFT, FIS, Fiserv, Worldline, Temenos, Finastra, Murex, Broadridge, Euroclear, Clearstream, Equinix, Salesforce and SIX. **Atruvia was NOT designated. Finanz Informatik (the Sparkassen equivalent) was also NOT designated** (subagent-confirmed against the list of 19). The Article 31 criteria weight: systemic impact of a failure, systemic importance of dependent entities, **concentration** of reliance, **substitutability**, plus (per commentary) cross-border footprint and EU-wide interconnectedness.

**Analysis:** the methodology favours **cross-border, multi-sector** providers (hyperscalers, global fintech platforms, market infrastructures). Atruvia is **overwhelmingly domestic** (German cooperative banks) — high national concentration, low cross-border footprint — so the criteria capture IBM (Atruvia's global supplier) but not Atruvia itself, even though an Atruvia outage disables a larger share of German retail banking than an isolated IBM outage would. **Verdict: a genuine national systemic-supervision gap exists.** It is only partly mitigated by indirect supervision (§25b KWG via customer banks; BaFin §44 special inspections — one begun November 2023) and by the fact that both large German captive core-banking providers sit outside direct DORA oversight. The counter-argument: because Atruvia is captive and single-country, BaFin already has strong indirect levers and detailed visibility (as the 2018 and 2023 §44 inspections show). But structurally the point stands — no single supervisor holds direct, continuous oversight of an entity whose failure routinely takes ~500 banks offline.

#### III.14 Employee Architecture
**Headcount.** Group ~**10,076 employees (2024)** (Vol I); historically ~8,400 group / ~4,600 AG (2020–21). Geographic distribution: Karlsruhe and Münster (largest — Vorstand, development, sales, customer service), plus Munich/Aschheim, Frankfurt, Berlin (Munich hosts an Innovation space); nearshore in Cluj-Napoca.

**Nearshore (Accesa/RaRo).** **CONFIRMED:** **RaRo (Ratiodata Accesa Romania S.R.L.)** was founded 2020 as a JV — **Ratiodata 74.9% / Accesa 25.1%** — HQ Cluj-Napoca; portfolio = consulting, software development, testing, IT operations support and 24×7 managed services, aimed at regulated sectors. Ratiodata later **acquired the Accesa IT Group** (~**700 IT specialists across ~20 competence centres**), lifting the Ratiodata group to **>2,100 employees across 21 sites** in Germany, Luxembourg, Romania and Switzerland. Compute stays in German data centres; only development/services are performed in Romania. **Why Romania:** a large pool of well-trained STEM/engineering graduates, high English proficiency, German widely studied, EET time zone (1–2h overlap for live stand-ups), and a shared **EU regulatory/legal framework** — important for a regulated-banking supply chain. Named Atruvia collaborators (Accesa site): Lennart Peters (Systems Architect), Enrico Shmal (Tribe Lead), Mathias Glaser (Scrum Master), on a 2.5-year regulatory-delivery partnership.

**COBOL/mainframe skills & demographic risk (important).** **CONFIRMED driver** (IBM case study): "With many COBOL programmers retiring … Atruvia executives decided on a creative approach to application modernization." The Java-in-IMS strategy is explicitly a **skills-continuity hedge** against COBOL retirement, making core-banking work "more familiar to the latest generation of developers." Atruvia is not recruiting a new COBOL generation at scale; it is **wrapping COBOL in Java** so it can hire from the general Java/Spring/Angular talent market (as the job ads confirm). Apprenticeship/dual-study/university-partnership specifics for mainframe engineers are not evidenced in the sources reviewed — **UNKNOWN**.

**Co-determination & brand.** 20-seat co-determined Aufsichtsrat under MitbestG 1976 (Vol I); the transformation removed a management layer and split leadership into People/Tribe leads. Job ads disclose salary bands (e.g. frontend engineer €70,000–€102,000 for a 38h week; fullstack engineer €65,000–€94,000), indicating competitive market-rate compensation — used cautiously as employer-brand evidence. Kununu/Glassdoor sentiment was not systematically assessed here.

#### III.15 Organizational Design
Atruvia is a **matrixed, product-based agile organisation** (Spotify-inspired tribes/squads) sitting inside a **captive customer-owner governance** that heavily constrains autonomy. Decision rights: Tribe Leads hold product ownership and budget; People Leads hold hiring/people authority; risk/compliance veto sits with the Vorstand ressort of Wiegelmann (Finance/Regulation/HR) and the Data/Security/Identity Geschäftsfeld.

**The "neues Betriebsmodell" (CONFIRMED).** Referenced from the 2025 Hauptversammlung and elaborated 2025–26: it is a **strategic-operational framework** for the banks, not merely an internal reorg. Its technological pillars are the **Omnikanalplattform**, **BankingWorkspace**, **OnlineBanking** and the **VR Banking App**, delivering **digitale, fallabschließende Prozesse** (end-to-end digital processes) that "entlasten" bank staff and let banks "flexibel auf unterschiedliche Rahmenbedingungen reagieren." At the 2026 HV it was positioned as the frame within which hybrid cloud + AI (incl. agentic AI) make VR banks "skalierbar."

**Formal vs actual power.** The customer-owner governance (BVR committees, the Bundeseinheitliches Strategieportfolio with 36 of 39 initiatives touching Atruvia, Kompetenzteams, Fokusgruppen, the Strategie- und Portfolioplattform — Vol II) means Atruvia's roadmap is **substantially set by its owners**, not autonomously. Internal agile empowerment is real at delivery level but bounded at portfolio level by the BSP/SPP mechanism.

#### III.16 Product Development and Release System
Roadmapping is driven by the BSP/SPP owner mechanism (Vol II). Agile methods (Scrum/Kanban, pair programming, code reviews) are confirmed in job ads. The **rollout pattern** is the multi-tenant pilot ladder: technical tests → Pilotierung → Serienpiloten/Serienfähigkeit → Serienmigration in tranches → bank-side MaRisk AT 8.2 change assessment, with the **technischer Jahresabschluss** as the marquee coordinated release (Vol II). A new regulation becomes a 700-bank release by: build once centrally, pilot with a small set of banks, prove Serienfähigkeit, then roll out in tranches. Technical-debt management on the COBOL estate is **selective in-place refactoring** ("There is no pressure to modernize just for the sake of modernization" — Thomas Bauer, IT Architect, Atruvia). The genoGPT pilot ("bereits in der Pilotierung mit ersten Banken") shows the same pilot-first cadence for AI features.

#### III.17 Support and Service Operating Model
**CONFIRMED:** the **Serviceline** is a qualified technical **end-customer hotline** for Online-/Mobile-Banking, GENO cash, Profi cash, BankingManager and VR-NetWorld Software, reachable only via the number the bank issues; it offers **Fernwartung** (remote screen-sharing support). The bank-facing service desk and BPO are handled with subsidiaries: **Serviscope** (BPO), **Ratiodata** (field services for the ~30,000+ ATM/self-service-device estate). Contact-centre technology is **Genesys Cloud CX**, with AI-assisted services under development (BankingWorkspace AI-assisted-services roles). Support functions as (a) a **cost centre**, (b) a **trust mechanism** (visible at every outage), (c) a **regulatory function** (complaint handling, fraud-flag review), and (d) a **product-quality feedback loop** into the tribes.

#### III.18 Operating Leverage
| Process | Leverage class | Rationale |
|---|---|---|
| Core banking dev | Sublinear/step-fixed | Build once, serve 700; COBOL estate needs continuous investment |
| Platform/omnichannel | Sublinear | One platform, ~300 processes, all tenants |
| DC ops | Step-fixed | Capacity added in mainframe increments |
| Release mgmt | Sublinear but complex | One build, per-tenant piloting adds coordination cost |
| Service desk | ~Linear | Scales with end-customers/incidents |
| Compliance/regulatory build | Strongly sublinear | One regulation implemented once for all 700 — best leverage point |
| Payment ops | Sublinear, improving w/ in-house cards 2027 | Removes DZ/VR Payment double structures |
| Bank-merger migrations (~40–45/yr) | Repeatable but labour-intensive | Productised but human-heavy |
| Subsidiaries (field) | Linear/labour-bound | Physical device servicing |

**Verdict:** a 700-bank multi-tenant platform DOES produce genuine operating leverage — most powerfully in **regulatory implementation at scale** and platform development (build once, deploy to all). This is visible in the improving margin: Betriebsergebnis rose to **€66.6m for 2024** (per IT-Finanzmagazin, driven by "eigenen Einsparungen sowie dem Betriebsstart neuer Kunden") and to **€89m (4.7% margin) in GB2025** against the **4% Zielrendite**. But **per-tenant complexity absorbs part of the leverage**: coexistence (maintaining CRM and BankingWorkspace twice), 40–45 merger migrations/year, and per-bank piloting are diseconomies. Margin expansion is coming from usage-based pricing plus the internal efficiency programme, not from raw platform scale alone.

#### III.19 Technology and Operations as Competitive Advantage (with Finanz Informatik comparison)
| Advantage | Proprietary? | Hard to reproduce? | Cuts cost? | Regulatory control? | Compounds w/ volume? |
|---|---|---|---|---|---|
| agree21 core (IMS/COBOL+Java) | Yes | Very | Yes (shared) | Yes | Yes |
| Multi-tenant platform | Yes | Very | Yes | Yes | **Yes** |
| Mainframe scale/reliability | No (IBM) | Moderate (capital) | Partly | Yes | Yes |
| **Migration capability** | Yes (process) | **High** | Yes | Yes | **Yes** |
| Regulatory implementation at scale | Yes | High | **Yes** | **Yes** | **Yes** |
| Data/fraud position | Partly | Moderate | Yes | Yes | **Yes** |
| AI (plainGPT/genoGPT) | Wrapper only | Low (OpenAI-based) | Yes | Yes (compliance wrapper) | Partly |
| ATM/SB field operation | Yes (Ratiodata) | Moderate | No (labour) | Yes | No |

**The migration capability is the underrated asset.** Atruvia has migrated dozens of banks (the "Mondlandung" bank21→agree21 consolidation; ~40–45 mergers/year; the Sparda-Banken onboarding from Sopra Steria; the imminent VR Payment card integration) — a **repeatable, industrialised migration machine**, genuinely hard to reproduce and directly relevant to winning new tenants.

**Finanz Informatik comparison (subagent-confirmed, enricher-upgraded).** FI is the structural twin — "Was hier der DSGV ist, ist dort der BVR … was hier die Finanz Informatik ist, ist dort die Atruvia" (Finanz-Szene). FI 2024: **~€2.6bn revenue** — IT-Finanzmagazin: "Der konsolidierte Umsatz stieg 2024 auf rund 2,6 Milliarden Euro – ein Plus von rund 140 Millionen Euro gegenüber dem Vorjahr" (vs Atruvia ~€2.2–2.5bn); **more than 5,000 employees at end-2024**; ~350 Sparkassen plus Landesbanken/Landesbausparkassen; **~114 million accounts**; and **over 205 billion technical transactions per year** (FI/Nutanix press release, end-2024: "Die Finanz Informatik übernimmt den Service für rund 114 Millionen Bankkonten; auf den Rechnern und Systemen werden jährlich über 205 Milliarden technische Transaktionen durchgeführt" — the older career-site figure was ~172bn). Its **34.3m online-banking contracts** and **17.9m active App Sparkasse users** dwarf per-institution digital reach. Core system **OSPlus** is likewise **IBM-mainframe-based** (FI–IBM six-year deal, June 2020) with an IBM/Red Hat hybrid cloud; €328m was invested in OSPlus in 2024. **Neither FI nor Atruvia was designated a DORA CTPP** — confirming the perimeter gap is sector-wide. Strategic read: near-mirror captive monopolies; FI is materially larger and reports a higher transaction count (consistent with its larger account base), but both face the identical structural challenge — an IBM-mainframe core that must be modernised in place. In payments, FI's ecosystem carries extra card muscle (S-Payment; the 2024 Bayern Card-Services/Pluscard merger into "Qards") that the cooperative side is only now assembling via the VR Payment/Atruvia consolidation.

#### III.20 Volume III Reconstruction (condensed)
**(1) Operating model:** Owners (VR banks via VR-FGI Beteiligungsholding) → BVR/BSP-SPP governance → 5-member Vorstand → Geschäfts-/Servicefelder → Tribes (tandem Tribe+People Lead) → Squads → Chapters/Guilds; subsidiaries (Ratiodata, parcIT, Peras, Serviscope, RaRo…). **(2) Banking workflow:** channels → proprietary API layer → ~1,200 Java microservices (OpenShift) → IMS TM on IBM Z → COBOL+Java business logic → Db2 z/OS; nightly batch; technischer Jahresabschluss (change-frozen); failures → Krisenstab. **(3) Compute map:** 4 DCs {KA×2, MS×2}, twin-site active-active + cross-metro DR (~350 km, async inferred); 8×z15 hosting 12 IMS systems (→z17); 80bn tx/yr, 12k tps, ~400m Java tx/day; Turbonomic+Apptio+Tailored Fit Pricing. **(4) Tech stack (layered):** Client (VR Banking App | OnlineBanking | BankingWorkspace-Angular/PWA | agree21BAP legacy | FinTS/HBCI) → Platform (Omnikanalplattform ~300 processes | agree21ECON/ADONIS | Genesys CX) → API/Integration (proprietary API layer | ~1,200 microservices on OpenShift | IBM MQ z/OS | z/OS Connect? UNKNOWN) → Core (IMS TM/DB + Db2 z/OS on IBM Z; COBOL+Java via Semeru 11 common runtime, 31-bit↔64-bit) → Cross-cutting (pervasive + quantum-safe crypto; HashiCorp Vault; Turbonomic/Apptio; GitLab/Jenkins CI/CD). **(5) Payment-state:** initiation → validation → agree21 posting (IMS) → rail selection (SEPA/SCT Inst/card) → DZ clearing → reconciliation; idempotency weak under load; from 2027 in-house integrated card platform. **(6) Ledger:** Db2/IMS; tenant-separation mechanism UNKNOWN (blast radius implies shared subsystems + tenant keys); double-entry/reversal/merger internals UNKNOWN. **(7) Reconciliation:** largely UNKNOWN; spans core↔rails↔card schemes↔DZ↔bank reporting; breaks → member-bank §25b liability. **(8) Data governance:** bank=controller, Atruvia=processor under AVV; no cross-tenant personal-data flywheel; legitimate loops = network fraud modelling + Smart Data. **(9) Fraud workflow:** real-time ML → 0.2–0.3% flagged → auto-hold → human bank review (~20% false positive) → bank decides + files FIU Verdachtsmeldung; ~80% of unauthorised transactions prevented. **(10) Security/reliability:** 4 Hochsicherheits-DCs; pervasive + quantum-safe crypto; Vault; audIT-remediated Berechtigungsmanagement (2018–~2023); DDoS-mitigated edge; Krisenstab; SLOs/RTO/RPO UNKNOWN. **(11) Incidents:** see III.12 table. **(12) Org map:** see (1)/III.1. **(13) Decision rights:** roadmap→owners/BVR; product/budget→Tribe Lead; people/hiring→People Lead; risk/compliance veto→Wiegelmann + Data/Security/Identity GF; escalation→Krisenstab→Vorstand. **(14) Build/buy/nearshore:** see III.5. **(15) Employee map:** ~10,076 group (2024); KA/MS core; RO nearshore (~700 specialists at Accesa/RaRo); Java/Angular hiring replacing COBOL recruitment; €65k–€102k bands. **(16) Operating leverage:** see III.18. **(17) Bottlenecks:** primary = shared central processing path (reliability blast radius) + COBOL-estate change velocity; secondary = coexistence double-maintenance (BankingWorkspace vs agree21BAP) + per-tenant piloting. **(18) Moat:** strongest/most durable = captive ownership (structural), regulatory-implementation-at-scale, industrialised migration machine; weakest/most rented = AI (OpenAI wrapper) and mainframe hardware (IBM). **(19) Key unknowns:** agree21 tenant-separation model; ledger/reconciliation internals; SLOs/RTO/RPO; z16 interim; ISO 27001/ISAE 3402/KRITIS scopes; batch-window duration; VR Banking App framework; internal compute cost allocation; mainframe-training pipeline; DDoS mitigation specifics.

**(20) Ten Most Important Conclusions.**
1. The core is an in-place-refactored IBM Z/IMS/Db2/COBOL estate wrapped in Java + ~1,200 microservices; the Nov 2025 z17 deal re-commits to this architecture for years.
2. Modernisation = selective refactoring (Java-in-IMS), explicitly a COBOL-retirement skills hedge — NOT core replacement.
3. Four twin-site data centres give geographic redundancy but not protection against logical faults replicated across sites — the recurring failure mode.
4. The blast radius (~490–520 banks per central fault) is the defining operational risk; incident response has matured (2026) but the architectural concentration has not been eliminated.
5. Atruvia is a national single point of failure yet sits outside direct DORA oversight while IBM is inside — a real supervision-perimeter gap (shared with Finanz Informatik).
6. As GDPR processor, Atruvia has no lawful cross-tenant personal-data flywheel; its real data edge is network-scale fraud modelling (~80% of unauthorised transactions prevented) and productised analytics.
7. The fraud/AML division of labour is clean: Atruvia builds systems, banks own the regulatory decisions and losses.
8. The strongest moats are structural (captive ownership) and organisational (migration + regulatory-at-scale), not raw technology.
9. Operating leverage is real (margin to 4.7% > 4% target) but partly absorbed by coexistence double-maintenance and per-tenant piloting.
10. Finanz Informatik is a near-mirror (IBM mainframe, ~€2.6bn revenue, >205bn technical transactions, ~114m accounts, not a CTPP) — confirming the cooperative/savings-bank IT duopoly faces an identical in-place-modernisation problem.

**Closing answers.** *Most critical operating subsystem:* the agree21 IMS/Db2 core on IBM Z and its shared central processing path. *Hardest to replicate:* the multi-tenant core plus the industrialised migration machine. *Scales most efficiently:* regulatory implementation and platform development (build once, deploy to 700); *requires headcount to keep growing:* service desk, ATM field services, and per-tenant migrations. *Most dependent on third-party tech:* IBM (Z hardware, z/OS, IMS, Db2, MQ, Turbonomic, Apptio) — a deliberately deepened dependency. *Nature of advantage:* primarily **structural (captive ownership) and organisational**, secondarily regulatory; technology is an enabler, not the moat. ***Central question — can a COBOL/IMS core serving 700 banks be modernised fast enough to stay competitive?*** Evidence FOR: the Java-in-IMS common runtime (85% Java-enabled), OpenShift hybrid cloud, ~1,200 microservices, Angular front-ends and a working AI pipeline show real, low-risk incremental modernisation, funded by an improving margin. Evidence AGAINST: coexistence drag ("etwas zäh"), recurring central outages, a COBOL retirement wave, and an owner-set roadmap that limits autonomy. **Verdict:** Atruvia can modernise fast enough to remain competitive **within its captive market** — its owners are locked in and its only true rival (Finanz Informatik) faces the same constraints — but the in-place-refactor path structurally cannot match a cloud-native challenger's velocity. Its competitiveness is protected by structure, not by technological superiority.

### Recommendations
1. **For member banks / BVR:** press Atruvia to publish availability SLOs, RTO/RPO and a blast-radius-reduction roadmap (tenant isolation / cellular architecture). Benchmark: if central-fault incidents affecting >300 banks recur more than once per 18 months, escalate to a mandated architectural review. The July 2026 incident should trigger this now.
2. **For BaFin / national policy:** treat the DORA CTPP omission of Atruvia (and Finanz Informatik) as a gap to close — via intensified §44/§25b indirect oversight or a national systemic-provider designation; the concentration and substitutability criteria are met domestically even though cross-border footprint is not.
3. **For Atruvia strategy:** prioritise ending the BankingWorkspace/agree21BAP coexistence (the largest self-inflicted diseconomy) and formalise a mainframe-skills pipeline (apprenticeship/dual-study) to de-risk the COBOL retirement wave beyond the Java-in-IMS hedge.
4. **On AI:** given plainGPT's OpenAI dependency, evaluate a self-hosted open-weight fallback to satisfy the "no open-internet" governance claim at the model layer, not just the wrapper.
5. **Change trigger:** if the VR Payment card-platform integration (1 January 2027) slips or causes incidents, re-rate the migration-capability moat downward.

### Caveats
- Several internal mechanisms (ledger model, tenant separation, reconciliation, SLOs, batch-window duration, certification scopes, the z16 interim) are **not published by Atruvia and are labelled UNKNOWN**; this volume deliberately does not invent them.
- The richest technical source (IBM case study) is dated May 2022 and describes the z15 estate; the z17 figures come from the November 2025 deal announcement, so some capacity/machine-count figures may have moved.
- Transaction counts vary by source and year (IBM has cited 80/87/100/120bn for Atruvia); the ~80bn / 12k-tps figures are the 2022 case-study baseline.
- Incident details rely partly on trade press and knowledgeable third-party blogs; where so, this is flagged.
- Finanz Informatik comparison figures carry source spreads reconciled to the most recent official FI/Nutanix press release (end-2024): ~114m accounts and >205bn technical transactions supersede older career-site figures (~111–113m / ~172bn); employees "more than 5,000" (FI legal entity) vs ~6,500 on a broader group basis.


---

# Part IV — Financial Statements, Revenue Architecture, Unit Economics & Capital

### Financial Statements, Revenue Architecture, Unit Economics & Capital

*Reporting perimeters: "AG" = Atruvia AG parent/Einzelabschluss (HGB); "Group" = Atruvia Konzernabschluss (HGB). All figures labelled. German HGB conventions apply (Gesamtleistung, Betriebsergebnis, Materialaufwand incl. bezogene Leistungen). Evidence labels: CONFIRMED FACT / COMPANY CLAIM / THIRD-PARTY ESTIMATE / ANALYTICAL INFERENCE / HYPOTHESIS / UNKNOWN.*

---

### TL;DR (the core answer)

- **Atruvia's real economic engine is a captive, owner-financed core-banking utility whose entire reported operating profit is, to the euro, roughly equal to the digitalisation levy its owner-customers pay.** In FY2025 (AG) the Betriebsergebnis was €89.0m on Gesamtleistung of €1,921.0m (4.63% margin) — and the Digitalisierungsumlage/Zukunftsbanking levy earmarked for that year was ~€90m. Strip the levy and underlying operating profit is approximately zero (ANALYTICAL INFERENCE). The "4% Zielrendite" is therefore best read as a **governance device to legitimise retained earnings for investment**, not a genuine commercial margin.
- **The permanent platform-investment race is funded from four sources in a deliberate sequence: retained earnings (now dressed as the 4% target), earmarked levies (IT-Sonderumlage 2018–2023, then the Digitalisierungsumlage €30m→€60m→€90m), DZ Bank contributions and lending, and — increasingly — supplier/bank financing.** Capex rose from €182.9m (AG, 2023) to €359.1m (AG, 2025), an 18.7% Investitionsquote. The model is sustainable at current ~€350m/yr intensity but would break against the circulating €450m–€1bn sector-investment scenario without a fresh levy or DZ Bank equity/loan injection.
- **The cooperative model does deliver captive-priced IT with near-perfect revenue retention but near-zero pricing power, and it is measurably less capital- and cost-efficient than its Sparkassen twin, Finanz Informatik.** FI turned ~€2.6bn revenue in 2024 with 5,037 employees (Vollzeitäquivalente per FI's Jahresbericht 2024) — ~€516k revenue/employee — and services 114m accounts; Atruvia Group turned ~€2.2bn with 10,076 employees (~€218k/employee) and 91m accounts (Lünendonk-Ranking 2025). Atruvia's headline group figure is dragged down by hardware/field-service (Ratiodata) and BPO (Serviscope) subsidiaries; even AG-only revenue/employee (~€324k) trails FI.

---

### KEY FINDINGS

1. **The profit *is* the levy.** FY2025 AG Betriebsergebnis €89.0m ≈ FY2025 Digitalisierungsumlage ~€90m. FY2024: €66.6m result vs €60m levy. FY2023: €40.6m vs €30m levy. The margin trajectory tracks the levy schedule almost mechanically (ANALYTICAL INFERENCE from CONFIRMED figures).
2. **Bought-in services, not personnel, are now the largest cost.** In FY2025 AG, Materialaufwand/bezogene Leistungen was ~€792.1m (41.2% of Gesamtleistung) versus Personalaufwand €654.1m (34.1%). Atruvia is more a *systems integrator riding IBM and nearshore capacity* than a pure in-house software house (CONFIRMED FACT).
3. **Revenue nearly doubled at AG level in four years without a genuine margin** — Gesamtleistung ~€1,382m (2022) → €1,921m (2025), +39%, driven by new external customers (Sparda group, UmweltBank, Bank für Sozialwirtschaft, National-Bank) and levies, not by pricing power over owners. Per IT-Finanzmagazin's HV coverage, the FY2025 revenue rise of 11.5% to "knapp 1,9 Milliarden Euro" was "hauptsächlich durch neue Kunden."
4. **The 2025 "4.7% margin" looks like a peak, not a plateau.** Management's own FY2026 guidance implies EBIT €77.9m on Gesamtleistung €1,974.6m ≈ 3.9% — i.e. the margin is guided *down* even as revenue rises, undercutting the idea that 4% is now structural (CONFIRMED FACT + ANALYTICAL INFERENCE).
5. **Capital structure is equity-heavy but access-constrained.** Equity €557.0m, EK-quote 38.2% (2025). No Kapitalerhöhung since the 2015 merger; Grundkapital fixed at €115.8m. Debt is a DZ Bank Campus-Karlsruhe loan plus a largely-undrawn credit line; the FY2025 mainframe purchase was funded partly through a ~€145m jump in trade payables (supplier financing) (CONFIRMED FACT).
6. **DZ Bank is a funder, not an owner.** It holds only ~0.35% of shares directly but contributed €180m to the 2018–2023 IT-Sonderumlage, lends against the Karlsruhe campus, and co-finances the VR Payment card reorganisation. The "DZ Bank ~20% of Atruvia" claim remains erroneous (it refers to Verimi/amberra) (CONFIRMED FACT).
7. **The VR Payment issuing-processing acquisition (effective 1 Jan 2027) has no discoverable purchase price** (UNKNOWN); it was announced by Atruvia press release dated 2 July 2026 and filed with the Bundeskartellamt on 15 July 2026 (case B9-75/26, per the Bundeskartellamt Fusionskontrolle listing).
8. **Subsidiary economics are structurally different from the captive core** — Ratiodata (hardware/field service, ~€344.5m, thin margin), Serviscope (BPO), parcIT/FORUM/ECON (software, higher margin), TRUUCO (loss-making smart-data venture, −€7.98m). The captive core cross-subsidises loss-makers like TRUUCO via capital injections (CONFIRMED FACT).

---

### DETAILS

#### IV.1 Multi-Year Financial History

**Table 1 — Atruvia AG (parent, HGB), €m unless stated. Source: Atruvia Geschäftsberichte 2021–2025 (CONFIRMED FACT); FY2024/FY2025 line items from the GB2024 Finanzteil and GB2025 audited accounts (BDO AG, unqualified).**

| Line (AG) | 2021 | 2022 | 2023 | 2024 | 2025 |
|---|---|---|---|---|---|
| Gesamtleistung | ~1,440* | ~1,382* | 1,516.3 | 1,720.0 | 1,921.0 |
| Umsatzerlöse | 1,297.9† | ~1,355* | 1,496.1 | 1,698.3 | 1,894.4 |
| — Bankverfahren (incl. Basispaket) | 863.1‡ | n/d | 765.6 | 831.2 | 908.7 |
| — Infrastruktur / Netze, Collab. & Arbeitsplatz | 227.9‡ | n/d | 298.6 | 326.5 | 357.3 |
| — Einzelprodukte | n/d | n/d | 109.3 | 140.5 | 153.3 |
| — Individualgeschäft & optionale Pakete | n/d | n/d | 133.5 | 146.0 | 146.6 |
| — Andere Umsatzerlöse (incl. levies, migration) | n/d | n/d | 189.0 | 254.1 | 328.4 |
| Aktivierte Eigenleistungen | n/d | n/d | 18.6 | 24.5 | 25.1 |
| Materialaufwand / bezogene Leistungen | n/d | n/d | 648.9 | 731.3 | ~792.1 |
| Personalaufwand | 475.7 | 517.6 | 552.4 | 604.2 | 654.1 |
| Abschreibungen | n/d | n/d | 163.0 | 178.5 | 213.8 |
| Sonstige betr. Aufwendungen | n/d | n/d | 125.5 | 157.6 | 185.9 |
| **Betriebsergebnis (EBIT)** | **18.4** | **11.4** | **40.6** | **66.6** | **89.0** |
| EBIT margin (on Gesamtleistung) | 1.3% | 0.8% | 2.7% | 3.9% | 4.6% |
| EBITDA | n/d | n/d | 203.6 | 245.1 | 302.8 |
| Finanzergebnis | +1.7 | −0.7 | −6.0 | −1.9 | +0.2 |
| Steuern (Ertrag + sonstige) | 10.2 | ~2.7 | 6.8 | 18.4 | 28.7 |
| **Jahresüberschuss** | ~9.9 | **7.6** | **27.8** | **46.3** | **60.5** |
| Bilanzsumme | n/d | 1,052.0 | 1,065.1 | 1,254.7 | 1,435.9 |
| Eigenkapital | n/d | ~448 | 467.3 | 505.0 | 557.0 |
| Eigenkapitalquote | n/d | 41.8% | 43.1% | 39.6% | 38.2% |
| Pensionsrückstellungen | n/d | n/d | 261.7 | 259.6 | 256.6 |
| Verbindlichkeiten ggü. Kreditinstituten | n/d | n/d | 81.8 | 158.3 | ~145.0 |
| Investitionen (capex, immat.+Sach) | n/d | n/d | 182.9 | 208.4 | 359.1 |
| Investitionsquote | n/d | 17.2% | 12.1% | 12.1% | 18.7% |
| Operating cash flow | n/d | n/d | ~230 | 301.1 | 397.2 |
| Employees (year-end) | n/d | n/d | 5,263 | 5,483 | 5,847 |

\* ANALYTICAL INFERENCE: 2023 Gesamtleistung €1,516.3m was +9.7% YoY, implying 2022 ≈ €1,382m. †2021 Umsatzerlöse fell €57.5m YoY per GB2021 (2021 Betriebsergebnis €18.4m; 2022 fell to €11.4m). ‡2021 split (Bankverfahren €863.1m, Infrastruktur €227.9m, weitere GenoFG incl. Zentralbank €167.9m) uses the *pre-2023* taxonomy; the 2023 report re-cut the categories, so pre-2023 and post-2023 splits are **not continuous** (accounting-presentation change, not economic change). n/d = not disclosed in accessible sources.

**Table 2 — Atruvia GROUP (Konzern), €bn / count. Source: Atruvia press/HV releases, Finanz-Szene, Lünendonk (mix of CONFIRMED FACT and THIRD-PARTY ESTIMATE).**

| Group | 2022 | 2023 | 2024 | 2025 |
|---|---|---|---|---|
| Revenue | ~1.82 | ~2.001 | ~2.2 | ~2.5 |
| Operating result | n/d | ~0.050 | n/d | n/d |
| Employees | 9,291 | ~9,500 | 10,076 | n/d |
| Customers | 1,015 | ~866–917 | 917 | ~950+ |
| Accounts (m) | 85 | 89 | 91 | 97 |
| Bookings/transactions (bn) | 8.2 | 8.7 | 9.32 | ~10 |

**Resolving the Finanz-Szene "€2.001bn / €50m" flag:** these are the FY2023 **Group** figures (revenue €2.001bn, +8%; operating result €50m), a *different perimeter* from the FY2023 AG figures (Gesamtleistung €1,516.3m, Betriebsergebnis €40.6m). The two are not contradictory; secondary sources conflate them. The €50m group operating result exceeds the €40.6m AG result because profitable subsidiaries (Ratiodata, parcIT) add ~€10m net (ANALYTICAL INFERENCE).

#### IV.2 Revenue Taxonomy

Economically meaningful AG revenue streams (FY2025 AG, CONFIRMED unless noted):

| Stream | 2025 €m | Payer | Trigger | Pricing basis | Quality |
|---|---|---|---|---|---|
| Bankverfahren (core banking, Basispaket + Festpreis) | 908.7 | Member/other banks | Ongoing service | Per-account/volume + fixed package | Recurring, captive, mandatory |
| Netze, Collaboration & Arbeitsplatz (infrastructure) | 357.3 | Banks | Ongoing | Per-workstation/bandwidth | Recurring, captive |
| Einzelprodukte | 153.3 | Banks | Optional order | Per-product | Recurring/discretionary |
| Individualgeschäft & optionale Pakete | 146.6 | Banks/externals | Project/option | Negotiated | Semi-recurring |
| Andere Umsatzerlöse (levies + migration endabrechnungen + print/output + external) | 328.4 | Banks (levy), new customers (migration) | Levy schedule / project completion | BVR-set levy; project billing | Mixed: levy=mandatory, migration=project |

- **IT-Sonderumlage (2018–2023):** €60m/yr from the primary banks, earmarked for the Digitalisierungsoffensive (BVR-approved June 2018); ended 30 June 2023 (CONFIRMED FACT, Börsen-Zeitung). Per the Atruvia Geschäftsbericht 2023, "nach Auslaufen der Digitalisierungsumlage zum 30. Juni 2023 ... Diese zusätzlichen Mittel haben die Ertragslage positiv beeinflusst."
- **Digitalisierungsumlage / "Zukunftsbanking-Preiskomponente":** introduced 1 July 2023, replacing the Digitalisierungspauschale; scaling €30m (2023) → €60m (2024) → €90m (2025) (COMPANY CLAIM / CONFIRMED via GB2023 narrative + Volume context). Booked within "andere Umsatzerlöse."
- **Migration/project revenue:** endabrechnungen from onboarding external banks and the sector's 40–45 bank mergers/year. Since 2021, 22 institutes migrated or under way to agree21, incl. all 11 Sparda-Banken, Sozialbank Köln, National-Bank Essen, UmweltBank Nürnberg (CONFIRMED FACT, IT-Finanzmagazin).
- **General price increases:** ~5% from 1 April 2023 (inflation-driven); a further ~5% of Leistungsentgelte planned 2024 (CONFIRMED FACT, Börsen-Zeitung/GB2023).
- **Card-processing revenue** grows structurally from 1 Jan 2027 with the VR Payment issuing-processing transfer (debit + credit processing) (CONFIRMED FACT).
- **Subsidiary revenue** (Group, see IV.8): Ratiodata (hardware/field service), parcIT/FORUM/ECON/GWS (software licences), Serviscope/Peras (BPO), Accesa/RaRo (nearshore, largely internal).

**Revenue quality classification:** ~85%+ of AG revenue is recurring and captive; the levy component (~€90m, ~4.7% of revenue) is mandatory but political; migration revenue is project-based and lumpy; external/non-cooperative revenue (private banks, ADAC) carries genuine pricing power but churn risk.

#### IV.3 Revenue Flow by Product (representative traces)

- **(a) A member bank's annual core-banking relationship:** bank pays Basispaket (per-account/volume) + infrastructure (per-workstation) + levy + optional products → recognised across Bankverfahren + Netze + andere Umsatzerlöse. Near-100% pass-through of the underlying platform cost; contribution is thin by design.
- **(b) A bank-merger migration:** two banks combine → one migration project → billed as endabrechnung in "andere Umsatzerlöse"; recurring revenue then *falls* (one customer instead of two) even as accounts are retained — a structural headwind (ANALYTICAL INFERENCE).
- **(c) An external core-banking win (e.g. Sparda-Bank West, ~620,000 customers, €13bn balance sheet, migrated Oct 2025):** multi-year migration project (~300 Atruvia staff involved) → migration revenue, then durable recurring Bankverfahren/infrastructure revenue. This is Atruvia's highest-value growth vector.
- **(d) Ratiodata hardware/field-service engagement:** gross customer payment largely pass-through hardware cost + service margin; low-margin, capital-light but labour-intensive.
- **(e) parcIT software licence:** high-margin, recurring licence + maintenance; VR-Control embedded in agree21.
- **(f) Serviscope BPO contract:** per-process/per-transaction BPO fees; labour-intensive, single-digit EBIT margin.

#### IV.4 THE UMLAGE ECONOMICS AND THE 4% ZIELRENDITE *(priority depth)*

**What the target is.** Vorstandssprecher/CFO Martin Beyer stated Atruvia targets "eine Zielrendite von 4 Prozent in Bezug auf den Umsatz" and, per the Atruvia GB2024 statement, "Unser Ziel: Wir steigern unser Betriebsergebnis, um ein dauerhaftes Plus für neue Investitionen zu schaffen" funded "aus eigener Kraft" (COMPANY CLAIM, HV 2025 / Atruvia Geschäftsbericht). It is measured against revenue, not capital.

**The trajectory (CONFIRMED, AG):**

| Year | Betriebsergebnis €m | Margin (on Gesamtleistung) | Digitalisierungs-levy €m |
|---|---|---|---|
| 2022 | 11.4 | 0.8% | — (Sonderumlage era) |
| 2023 | 40.6 | 2.7% | 30 |
| 2024 | 66.6 | 3.9% | 60 |
| 2025 | 89.0 | 4.6% | 90 |
| 2026 (guidance) | 77.9 | 3.9% | n/d |

Per IT-Finanzmagazin's coverage of the 2026 HV: "Mit 89,0 Millionen Euro liegt das Ergebnis rund ein Drittel über dem des Geschäftsjahres 2024. Die Betriebsergebnismarge liegt bei 4,7 Prozent."

**Why would a customer-owned captive target a positive margin at all?** A supplier owned by its customers is, in theory, indifferent between (i) charging a low price and paying no dividend, and (ii) charging a higher price and returning it as dividend — the owner-customer's net position is identical. Introducing a *deliberate* positive margin only makes economic sense if the surplus is used for something the owners would not otherwise fund voluntarily. That "something" is **permanent platform investment**.

**Central hypothesis (tested):** the 4% Zielrendite is a **governance device to legitimise retained earnings for investment that owners resist funding through explicit levies.** The evidence strongly supports this:
- The FY2025 Betriebsergebnis (€89.0m) is within ~€1m of the FY2025 Digitalisierungslevy (~€90m). In cash terms, **the operating profit is the levy** (ANALYTICAL INFERENCE).
- Management explicitly links the margin to investment funding ("dauerhaftes Plus für neue Investitionen"), not to shareholder return.
- The levy share of revenue is being reduced in favour of "nutzenbasierte Bepreisung" (usage-based pricing) — i.e. the *label* on the money is shifting from an unpopular explicit levy toward embedded usage prices, while the economic function (fund investment from customer cash) is unchanged.

**What happens to the surplus.** It is overwhelmingly retained: Eigenkapital rose from €467.3m (2023) to €557.0m (2025), +€89.7m, almost exactly the cumulative Jahresüberschüsse net of a small dividend. A dividend is paid (the Aufsichtsrat "found the Vorstand's Dividendenvorschlag angemessen" in both 2024 and 2025) but the euro amount is not separately disclosed and is small relative to retained earnings (UNKNOWN exact figure; the FY2025 financing cash outflow of €34.8m includes it alongside debt service).

**Is the target sustainable or flattered?** The FY2026 guidance (margin falling back to ~3.9%) indicates 2025's 4.7% is at or near a cyclical peak, likely flattered by (i) the levy stepping up to €90m and (ii) new-customer migration completions (Sparda group). It is **not yet a structurally self-sustaining 4% margin**; absent the levy, the underlying business runs at roughly break-even (see IV.21). **Verdict: the 4% Zielrendite is economically real as a cash-generation mechanism but is a governance fiction as a "commercial margin" — it is the levy, re-badged.**

#### IV.5 Cost Architecture (AG, FY2025)

| Cost line | €m | % of Gesamtleistung | Behaviour | Driver |
|---|---|---|---|---|
| Materialaufwand / bezogene Leistungen | ~792.1 | 41.2% | Semi-variable | IBM licensing (Tailored Fit Pricing, consumption), Fremdarbeit/nearshore, Miete & Wartung |
| Personalaufwand | 654.1 | 34.1% | Step-fixed | Headcount (5,847), tariff increases, pension provisioning |
| Abschreibungen | 213.8 | 11.1% | Fixed | Capitalised software, mainframes, buildings; incl. €6.5m impairment on decommissioned buildings (2025) |
| Sonstige betr. Aufwendungen | 185.9 | 9.7% | Semi-variable | Energy, travel, consulting, internal applications |
| **Betriebsergebnis** | **89.0** | **4.6%** | Residual | — |

- **Personnel:** cost/employee rose from €104,960 (2023) to €111,870 (2025). The Romanian nearshore shift (Accesa/RaRo, Cluj-Napoca) appears in *bezogene Leistungen* when contracted and migrates to *Personalaufwand* as capacity is internalised — the GB2023/GB2021 narratives repeatedly cite "Wandlung von externen zu internen Kapazitäten," which raises Personalaufwand while restraining Materialaufwand.
- **IBM under Tailored Fit Pricing:** consumption-based licensing converts a step-fixed mainframe cost into a semi-variable one that scales with transaction volume — beneficial as volumes grow but removes the old "peak-MSU" optimisation lever (ANALYTICAL INFERENCE from Volume III + IBM deal).
- **Development capitalisation (HGB):** aktivierte Eigenleistungen were €24.5m (2024) and €25.1m (2025); the GB2023 states development costs were "knapp ein Fünftel der Gesamtkosten" with ~40% of internal staff in development. Capitalising a portion of development flatters current Betriebsergebnis and shifts cost into future Abschreibungen — a material accounting judgement (CONFIRMED FACT).

#### IV.6 Cost per Unit (AG basis; show arithmetic)

Total AG operating cost 2025 = Gesamtleistung − Betriebsergebnis = 1,921.0 − 89.0 = **€1,832.0m**.

- **Cost per account:** €1,832.0m ÷ 97m accounts = **€18.89/account/yr**. Revenue/account = 1,894.4 ÷ 97 = €19.53. *(Accounts are a group operational metric; AG cost is used because AG runs the platform — perimeter caveat.)*
- **Cost per booking:** €1,832.0m ÷ ~10bn bookings = **€0.183/booking**. *If* the ~80bn+ technical-transaction denominator is used, ≈ €0.023/technical transaction (denominator uncertain — flagged).
- **Cost per banking workstation:** infrastructure cost proxy €357.3m revenue ÷ ~160,000 workstations = **€2,233/workstation/yr** (revenue basis; cost basis similar given thin margin).
- **Cost per member-bank relationship:** €1,832.0m ÷ 917 customers = **€2.0m/customer/yr** average (heavily skewed — a large Volksbank consumes many multiples of a small Raiffeisenbank).
- **Cost per employee:** €654.1m Personalaufwand ÷ 5,847 = **€111,870**.

**Where scale economies arise:** single multi-tenant agree21 platform, regulatory "build-once" (MaRisk/DORA implemented once for ~950 banks), mainframe consolidation (eight IBM Z systems, four data centres). **Where they do not:** Ratiodata field service (per-site labour), service desk, per-tenant migrations, and BAP↔BankingWorkspace coexistence double-maintenance.

#### IV.7 Unit Economics

The economically relevant unit is the **member bank** (the contracting, paying, owning entity); the account is the volume driver beneath it. 
- **Revenue per bank (avg):** €1,894.4m ÷ 917 = ~€2.07m. A large Volksbank (~1m accounts) may pay €10m+; a small Raiffeisenbank (~20–30k accounts) perhaps €0.3–0.5m (ANALYTICAL INFERENCE — Atruvia discloses no per-bank pricing).
- **Value of a new external win:** e.g. Sparda-Bank West (~620,000 customers). Migration project revenue (one-off, spread over ~2–3 yrs) plus durable recurring Bankverfahren + infrastructure. Rough estimate: recurring ~€10–20m/yr for a bank of that size (ANALYTICAL INFERENCE, based on ~€19.5 revenue/account × account count).
- **Cost of a bank merger to Atruvia:** a migration project consumes engineering capacity (the Sparda-BW cut-over moved 400GB / 2.4bn records across 612 tables) but *reduces* the recurring customer count — Atruvia earns a one-off fee then loses one relationship's fixed component. Net effect is dilutive to recurring revenue over time, offset only by external wins (ANALYTICAL INFERENCE).

#### IV.8 Segment and Entity Economics *(replaces cohort analysis)*

**Table 3 — Material subsidiaries (FY2024 unless stated). Sources: subsidiary reports, Atruvia Tochterunternehmen GB, Northdata (mix CONFIRMED / COMPANY CLAIM).**

| Entity | Revenue €m | Employees | EBIT/EBT €m | Business | Margin character |
|---|---|---|---|---|---|
| Ratiodata SE | 344.5 (2024) | ~1,426–1,500 | EBT 7.4 (2024) | Hardware, field service, scanning, nearshore | Thin (~2%) |
| parcIT GmbH | 78.6 (2024)* | 507* | ~3+ | Banksteuerung software (VR-Control) | Higher (software) |
| BMS Corporate Solutions | 52.0 | 303 | n/d | Firmenkunden software/consulting | Medium |
| Peras GmbH | 46.7 | 290 | n/d | HR services/payroll BPO | Medium |
| Serviscope AG | 28.8 (task) / Gesamtleistung ~44.0 (2024–25) | 482 | EBIT 3.1 (2024) | BPO/call-centre | Single-digit |
| TRUUCO GmbH | 8.2 (task) / 3.1 (2023) | 51–58 | **−7.98 (2024) / −8.6 (2023)** | Smart-data/analytics | **Loss-making** |
| ECON Application | 4.1 | 35 | 0.3 (2023) | No-code application suite | Small/positive |
| FORUM GmbH | 3.6 | 20 | n/d | Software | Small |
| GWS mbH | n/d | n/d | n/d | Warenwirtschaft (Microsoft Dynamics) | — |
| Accesa/RaRo | n/d (~700 IT specialists) | ~700 | n/d | Nearshore dev (Cluj-Napoca) | Internal cost centre |
| Lucke EDV | n/d | n/d | n/d | EDV | — |

\*parcIT reconciliation flag: GB2022 gave 403 employees/€68.9m; GB2023 478/€69.8m (and a Tochter-page figure of €37.9m/236 for one perimeter); FY2024 €78.6m/507. The jump suggests a change in consolidation/perimeter or a merged unit; the series is **not cleanly continuous** and should not be read as organic growth (ANALYTICAL INFERENCE).

**Cross-subsidy direction:** the captive core (AG) subsidises loss-making strategic ventures — TRUUCO received a capital-reserve injection from Atruvia and a DZ Bank/Atruvia joint strengthening; its ~−€8m annual loss is absorbed at group level. Conversely, the profitable software subsidiaries (parcIT, ECON) modestly *lift* the group margin above the AG margin (the €50m group vs €40.6m AG operating result in 2023). **Headline group margins therefore conceal a break-even captive core, several thin-margin service businesses, a few higher-margin software units, and at least one structural loss-maker.**

#### IV.9 Income Statement Teardown (AG, HGB)

- **Gesamtleistung → Umsatzerlöse reconciliation (2025):** Umsatzerlöse €1,894.4m + aktivierte Eigenleistungen €25.1m + Bestandsveränderung ≈ **Gesamtleistung €1,921.0m**.
- **Betriebsergebnis → Jahresüberschuss (2025):** EBIT €89.0m + Finanzergebnis €0.2m − Steuern (Ertrag €26.9m + sonstige €1.8m) = **Jahresüberschuss €60.5m**.
- **Operating leverage:** modest and asymmetric. From 2023→2025 Gesamtleistung rose €404.7m (+27%) while Betriebsergebnis rose €48.4m — an incremental margin of ~12%. But most of that incremental margin *is* the levy step-up (€30m→€90m = +€60m), so genuine operating leverage from scale is weak (ANALYTICAL INFERENCE).
- **Key accounting judgements:** (i) development-cost capitalisation (~€25m/yr aktivierte Eigenleistungen) flatters EBIT; (ii) pension provisioning is sensitive to the HGB Rechnungszins (the €256–262m Pensionsrückstellungen moved with the discount rate); (iii) levies are booked as ordinary revenue, so they inflate both Umsatzerlöse and Betriebsergebnis one-for-one.

#### IV.10 Balance Sheet Teardown (AG, 31.12.2025)

- **Bilanzsumme €1,435.9m** (+14.5% YoY). **Anlagevermögen ~€1,048.8m**: immaterielle VG (capitalised software) grew sharply (FY2025 immat. capex €286.0m — largely the financed IBM mainframe software purchase); Sachanlagen include the four data centres and the Karlsruhe campus; Finanzanlagen €158.3m (2024) are participations in subsidiaries.
- **Data centres/mainframes: owned, not leased** — the FY2025 report describes *purchasing* mainframe software (financed via trade payables) rather than renting, materially raising Anlagevermögen and Abschreibungen.
- **Eigenkapital €557.0m** = Grundkapital €115.8m + Kapitalrücklage €230.3m + Gewinnrücklagen €100m + Bilanzgewinn. **EK-quote 38.2%** (falling as the balance sheet grows faster than retained earnings).
- **Pensionsrückstellungen €256.6m** — the single largest provision; long-duration, interest-sensitive.
- **Verbindlichkeiten ggü. Kreditinstituten ~€145m** — DZ Bank Campus-Karlsruhe term loan (with SWAP hedge, §254 HGB Bewertungseinheit) + credit line (€160–210m facility, largely undrawn; €25.8m drawn at end-2023, €1.9m Aval at end-2025).
- **Receivables from ~700 member banks:** low credit risk ("geringe Ausfallrisiken," strong cooperative counterparties); a Forderungsmanagementsystem is in place.

#### IV.11 CAPITAL STRUCTURE AND THE COOPERATIVE FINANCING PROBLEM *(priority depth)*

**The structural constraint.** Atruvia cannot issue public equity, is unlisted, cannot raise capital outside the cooperative sector, and its owners are also its price-resisting customers. A cooperative captive facing *permanent* platform-investment demand therefore has only **four funding taps**:
1. **Raise prices on owner-customers** (general increases + usage-based pricing) — politically constrained; owners resist.
2. **Retain earnings** — now institutionalised as the 4% Zielrendite; delivered €89.7m equity growth 2023→2025.
3. **Borrow** — DZ Bank campus loan + credit line + increasingly *supplier/trade financing* (the ~€145m jump in Verb. aus L&L in 2025 to fund the IBM purchase is a form of vendor financing).
4. **Sector-level subsidy** — the IT-Sonderumlage (banks €300m + DZ Bank €180m + Atruvia €200m = ~€680m over 2018–2023) and DZ Bank's ongoing role.

**Has Atruvia ever raised equity from shareholders?** No Kapitalerhöhung is evident since the 2015 merger; Grundkapital is fixed at €115.8m. Capital comes from retained earnings and the Kapitalrücklage, not fresh subscription (CONFIRMED FACT). *(By contrast, subsidiary Serviscope did a Kapitalerhöhung to €1.6m in 2024 — a subsidiary-level, not AG-level, event.)*

**DZ Bank's role as funder (not owner).** DZ Bank holds ~0.35% of shares but: contributed €180m to the 2018–2023 Sonderumlage; provides the campus term loan; and co-finances the VR Payment card reorganisation. Its €180m was a **levy-type sector contribution**, not equity and not a normal customer fee — it functioned as a one-off capital grant to the utility on behalf of the sector (ANALYTICAL INFERENCE). This is why the "DZ Bank ~20% owner" claim is doubly wrong: DZ Bank is a *financier and central institution*, not a material shareholder.

**How large investments are financed:**
- **agree21 modernisation / Omnikanal / BankingWorkspace:** retained earnings + Digitalisierungsumlage (the earmarked levy).
- **IBM z17 multi-year deal (signed 19 Nov 2025):** structured around *purchasing* mainframe software financed through trade payables (+~€145m) rather than pure leasing — a shift from operating expense to capitalised asset + supplier financing.
- **VR Payment issuing-processing (effective 1 Jan 2027):** funding/purchase price UNKNOWN; likely a mix of DZ Bank arrangement and Atruvia balance-sheet capacity.

**Sustainability verdict.** At ~€350m/yr capex and ~€400m/yr operating cash flow, the model is **self-funding at current intensity**. Against the circulating **€450m–€1bn/yr sector-investment scenario (HYPOTHESIS, not a plan)**, retained earnings + current levies would be insufficient by €100–650m/yr, forcing either a new Sonderumlage, a DZ Bank capital injection, or external debt — the last of which is constrained by the falling EK-quote (38.2% and declining).

#### IV.12 The Investment-Funding Mechanism *(replaces interest income)*

**Table 4 — Disclosed investment-funding instruments (CONFIRMED / COMPANY CLAIM):**

| Instrument | Amount | Period | Payer | Nature |
|---|---|---|---|---|
| IT-Sonderumlage (banks) | €60m/yr (~€300m cumulative) | 2018–2023 | Primary banks | Earmarked levy |
| IT-Sonderumlage (DZ Bank) | €180m | 2018–2023 | DZ Bank | Sector capital grant |
| IT-Sonderumlage (self-funded) | ~€200m | 2018–2023 | Atruvia | Retained earnings |
| Digitalisierungsumlage / Zukunftsbanking | €30m→€60m→€90m | 2023→2025 | Banks | Earmarked levy (in revenue) |
| General price increases | ~5% (2023) + ~5% (2024) | ongoing | Banks | Price |
| Retained earnings (4% Zielrendite) | €27.8m→€46.3m→€60.5m Jahresüberschuss | 2023–2025 | Banks (as customers) | Retention |
| DZ Bank campus loan + credit line | ~€145–160m facility | ongoing | DZ Bank | Debt |
| Trade/supplier financing (IBM) | +~€145m payables | 2025 | Vendor | Vendor financing |

**Total annual investment budget:** AG capex €182.9m (2023) → €208.4m (2024) → €359.1m (2025); Investitionsquote 12.1% → 18.7%. The FY2025 jump reflects the IBM mainframe purchase.

**Who ultimately bears each euro?** The banks bear it three ways simultaneously — as **customers** (prices + levy embedded in service fees), as **owners** (foregone dividends via retained earnings), and — for the 2018–2023 tranche — via **DZ Bank on the sector's behalf** (€180m). The design (and the fragility) of the model is that the same party pays in three guises, which blurs accountability and lets Atruvia fund investment without a transparent price signal (ANALYTICAL INFERENCE).

**VR Payment financing (1 Jan 2027):** purchase price **UNKNOWN**; Bundeskartellamt case B9-75/26 filed 15 July 2026; announced 2 July 2026.

#### IV.13 Cash Flow (AG)

**FY2025 cash-flow statement (CONFIRMED):** Operating €397.2m; Investing −€357.5m; Financing −€34.8m; net change in cash +€4.9m; year-end Finanzmittelfonds €108.2m. **FY2024:** Operating €301.1m; Investing −€252.2m; Financing +€80.0m.
- **Non-cash add-backs:** Abschreibungen €213.8m (2025) + provision movements drive the gap between €60.5m net income and €397.2m operating cash flow.
- **Free cash flow:** operating €397.2m − capex €359.1m ≈ **€38m FCF (2025)** — i.e. after maintaining the mainframe estate and funding the platform transition, the business generates only ~€38m of genuinely free cash. This is the *true* discretionary surplus, and it is roughly the size of the dividend + debt service (financing −€34.8m). **The business runs close to cash-neutral after investment** (ANALYTICAL INFERENCE).
- **Working capital:** receivables from ~700 highly-rated cooperative banks; payment terms are short and default risk minimal; the 2025 payables spike is a deliberate financing choice, not stress.

#### IV.14 Capital Intensity

- **Maintenance vs growth capex:** of €359.1m (2025), a large slice is *growth* (IBM z17 software purchase, agree21 modernisation, capitalised development ~€25m); maintenance capex on the eight-system IBM Z estate and data centres is the recurring floor (ANALYTICAL INFERENCE — Atruvia does not split the two).
- **Mainframe refresh:** the z15→z17 transition under the multi-year IBM deal is structured as *purchase + supplier financing + consumption licensing (Tailored Fit Pricing)*, not a clean lease. Cost is not disclosed (UNKNOWN) but the ~€145m payables jump and €286m immat. capex in 2025 bound its scale.
- **Return on incremental capital:** poor by design — €404.7m extra Gesamtleistung (2023→2025) required cumulative capex of ~€750m over the same period for ~€48m extra Betriebsergebnis. The utility is not run to earn a return on capital; it is run to keep the sector's IT current at the lowest sustainable owner cost (ANALYTICAL INFERENCE).

#### IV.15 Capital Allocation

- **Platform:** agree21 modernisation, Omnikanalplattform (productive since 2019), BankingWorkspace (rollout from 2023), AI programme — the dominant use of capital.
- **Acquisitions:** ECON (2023), Accesa IT Group (nearshore), VR Payment issuing-processing (2027). Strategically coherent — each extends the captive value chain (application tooling, nearshore capacity, card processing).
- **Loss-making venture support:** TRUUCO (~−€8m/yr) sustained via capital injections — a strategic bet on data-driven sales, not a disciplined ROIC decision.
- **Portfolio housekeeping:** GWS hardware transferred to Ratiodata (June 2024); EGP merged up into the AG (Sept 2023); ORGA Consulting merged up (2023); Accesa/RaRo moved from Ratiodata to AG (2024). Discipline is improving (consolidating overlaps), but returns are secondary to sector-utility objectives.

#### IV.16 Revenue and Cost Waterfalls

**€1 of Atruvia AG revenue (FY2025, per €1 of Gesamtleistung):**

| Allocation | €/€1 |
|---|---|
| Bought-in services (Material/bezogene Leistungen: IBM, nearshore, maintenance) | 0.412 |
| Personnel | 0.340 |
| Depreciation & amortisation | 0.111 |
| Other operating (energy, travel, consulting) | 0.097 |
| = Total operating cost | 0.960 |
| **Betriebsergebnis** | **0.046** |
| Finance result | +0.000 |
| Tax | −0.015 |
| **Retained (Jahresüberschuss)** | **0.031** |

**One member bank's annual relationship (illustrative, AG):** average customer pays ~€2.07m/yr → ~€0.41 to IBM/nearshore/maintenance, ~€0.34 to Atruvia staff, ~€0.11 to depreciation, ~€0.10 to overhead, ~€0.046 retained for investment (≈€95k of the €2.07m). *(Group and AG are kept separate; this waterfall is AG only.)*

#### IV.17 Economic Driver Tree

The 5–8 variables explaining most outcomes:
1. **Number of member banks × accounts per bank** → Bankverfahren revenue (~€909m). Consolidation shrinks bank count but accounts persist.
2. **Workstations & bandwidth** → infrastructure revenue (~€357m).
3. **Levy level (Digitalisierungsumlage)** → ≈ the entire Betriebsergebnis (~€90m).
4. **External-customer wins (migrations)** → the main revenue-growth lever (+11.5% in 2025).
5. **Personnel headcount & tariff** → €654m cost, largest controllable.
6. **IBM/consumption licensing & nearshore mix** → ~€792m Material line, the largest cost.
7. **Capitalisation rate of development** → shifts cost between current EBIT and future depreciation.
8. **Pension discount rate (HGB Rechnungszins)** → provision and cost volatility.

`Betriebsergebnis ≈ (Bankverfahren + Infrastruktur + Levies + Migration + Options) − (Bought-in services + Personnel + Depreciation + Overhead) → targeted at 4% of revenue, ≈ the levy.`

#### IV.18 Scenario Model (assumptions explicit; directional)

| Scenario | Revenue | Margin | Investment capacity | Capital need |
|---|---|---|---|---|
| **A. Base** (consolidation continues, usage-pricing phases in) | +4–6%/yr | ~4% | Adequate | Neutral |
| **B. Accelerated bank consolidation** (faster drop below ~600 banks) | Flat/soft (fewer fixed-fee relationships) | Squeezed | Reduced | Rising |
| **C. External-win wave** (more Sparda-type migrations) | +8–12%/yr | Lifted (migration fees) | Improved | Neutral/positive |
| **D. €450m–€1bn investment shock** (HYPOTHESIS) | — | Turns negative without new levy | Insufficient by €100–650m/yr | New Sonderumlage or DZ Bank capital required |
| **E. Major operational incident** (liability + remediation) | Flat | Hit by one-offs | Reduced | Rising |
| **F. DORA CTPP designation** (direct oversight cost) | Flat | −0.2–0.5pp compliance cost | Slightly reduced | Modest |
| **G. VR Payment over/under-delivers** | ± card revenue | ± | ± | Integration capex |
| **H. Owner revolt on prices** (Zielrendite → 0) | Flat | ~0% | Collapses | Forces external debt/levy |

#### IV.19 Sensitivity Analysis (most-sensitive variables first)

1. **Levy level** — ~1:1 pass-through to Betriebsergebnis; a €30m levy cut wipes out a third of profit.
2. **Personnel cost/tariff** — €654m base; a 3% tariff rise ≈ €20m, ~22% of EBIT.
3. **IBM/nearshore (Material) cost** — ~€792m base; a 3% move ≈ €24m.
4. **External wins/migration volume** — the growth engine; each large Sparda-scale win adds ~€10–20m recurring.
5. **Bank count** — consolidation erodes the fixed-fee floor.
6. **Pension discount rate** — swings provisions and cost by tens of millions.
7. **Development capitalisation rate** — moves reported EBIT without changing cash.
The economics are **most sensitive to the levy and to personnel/Material costs** — i.e. to political pricing decisions and to input-cost inflation, not to volume.

#### IV.20 Revenue Quality Scorecard

| Stream | Predictability | Recurrence | Retention | Pricing power | Concentration | Cyclicality | Margin | Reg. risk | Overall |
|---|---|---|---|---|---|---|---|---|---|
| Bankverfahren (captive core) | High | High | ~100% | **Very low** | High (sector) | Low | Thin | High (DORA) | **Highest quality by durability, lowest by pricing power** |
| Infrastructure | High | High | High | Low | High | Low | Thin | Medium | High |
| Levies | Medium | Political | n/a | n/a (BVR-set) | High | Low | ≈ pure margin | Medium | Medium |
| Migration/project | Low | Lumpy | n/a | Medium | Medium | Medium | Medium | Low | Medium |
| External/non-coop | Medium | Medium | Churn risk | **Real** | Lower | Medium | Medium | Low | Medium-high |
| Software subs (parcIT/ECON) | High | High | High | Medium | Medium | Low | High | Low | High |
| Hardware/BPO subs | Medium | Medium | Medium | Low | Medium | Medium | Thin | Low | Low |

The defining paradox: **captive revenue has near-perfect retention but near-zero pricing power** (owners resist increases), while **external revenue has real pricing power but real churn risk.**

#### IV.21 Profitability Decomposition

**Is the FY2025 4.7% margin structural or flattered?** Predominantly flattered:
- **Levy contribution:** ~€90m of the €89.0m Betriebsergebnis. Remove it → **underlying operating result ≈ €0** (ANALYTICAL INFERENCE).
- **Migration completions** (Sparda group) added one-off project revenue in 2024–25.
- **Efficiency programme** ("internes Effizienzprogramm") contributed genuine structural savings (management-cited driver of the 2023–24 improvement) — the only *durable* profit component, likely low-double-digit €m.
- **FY2026 guidance margin ~3.9%** confirms the 4.7% is a peak.

**What would the underlying business earn without the levies?** Approximately break-even to slightly positive — consistent with a customer-owned utility priced at cost. The reported profit is, in substance, **investment pre-funding collected from owners and parked in equity**, not a commercial return.

#### IV.22 Economic Value & Owner Returns — Finanz Informatik Benchmark

Atruvia is unlisted; conventional valuation is inapplicable. Its economic value to owners is **cost avoidance** versus (a) each bank building IT independently (impossible at ~950-bank scale) and (b) a commercial vendor's margin. The relevant test is **relative efficiency vs Finanz Informatik**, the near-identical Sparkassen utility. In the Lünendonk-Ranking 2025 of Germany's largest internal IT service providers, FI ranks #2 (revenue €2.6bn, 2024) and Atruvia #3 (€2.2bn, 2024, "erstmals mehr als 10.000 Mitarbeiter").

**Table 5 — Atruvia vs Finanz Informatik (FY2024; CONFIRMED / THIRD-PARTY):**

| Metric | Atruvia (Group) | Finanz Informatik (Group) |
|---|---|---|
| Revenue | ~€2.2bn | ~€2.6bn |
| Employees | 10,076 | 5,037 (FTE) |
| Accounts | 91m | 114m |
| Technical transactions | ~80bn+ (uncertain) | >205bn |
| Platform investment | €208m (AG capex) | €328m (OSPlus Basisangebot) |
| Revenue/employee | ~€218k | ~€516k |
| Revenue/account | ~€24.2 | ~€22.8 |
| Legal form | AG (HGB Kapitalgesellschaft) | GmbH & Co. KG (partnership) |

**Interpretation:** FI is dramatically leaner per employee (€516k vs €218k revenue/employee) because it outsources hardware/field service (no Ratiodata-equivalent inside the perimeter) and runs a larger account base on a single platform (OSPlus). Atruvia's group figure is *structurally* depressed by its ~1,500-strong hardware/field-service arm (Ratiodata) and its BPO/call-centre arm (Serviscope) — a business-mix difference, not pure inefficiency. On revenue/account the two are comparable (~€23–24). **On the like-for-like platform metrics (accounts, transactions per employee, investment intensity), FI is the more efficient operator**, reflecting its larger scale and leaner perimeter (per fi-magazin, FI invested €328m in the OSPlus Basisangebot in 2024, "on premise"). Atruvia's owner-banks nonetheless obtain IT at cost (near-zero margin), which is cheaper than any commercial vendor's marked-up alternative — so the cooperative model delivers cheap IT in *absolute* terms, but not the *cheapest possible* relative to its Sparkassen twin. An owner-bank's stake is economically worth its share of ~€557m equity plus the avoided commercial margin — but is illiquid and non-transferable outside the sector.

#### IV.23 Volume IV Reconstruction — Key Unknowns & Ten Conclusions

**Key Unknowns (labelled UNKNOWN):**
1. VR Payment issuing-processing purchase price.
2. Exact annual dividend €m (small; embedded in financing cash flow).
3. Group (Konzern) FY2025 full P&L/balance sheet (behind Northdata paywall; not in accessible PDFs).
4. IBM z17 total contract value and lease-vs-purchase-vs-consumption split.
5. Per-bank and per-product margins (never disclosed).
6. Precise technical-transaction denominator for cost/transaction.
7. parcIT revenue-series continuity (perimeter changes).

**Ten Most Important Conclusions:**
1. Atruvia's real engine is a **captive cost-recovery utility**, not a profit-maximising firm.
2. **The operating profit ≈ the digitalisation levy** — profitability is levy-driven, not structural.
3. The **4% Zielrendite is a governance device** to legitimise retained-earnings investment funding.
4. **Bought-in services (~€792m) exceed personnel (€654m)** — Atruvia is IBM- and nearshore-dependent.
5. **Growth comes from external wins** (Sparda, UmweltBank, etc.), not owner pricing power.
6. **Free cash flow is thin (~€38m in 2025)** after €359m capex — the utility runs near cash-neutral.
7. **Capital access is the binding constraint**: no equity market, fixed Grundkapital, falling EK-quote (38.2%), reliance on retained earnings + DZ Bank + supplier financing.
8. **The model is sustainable at ~€350m/yr capex but not against the €450m–€1bn sector scenario** without a new levy or DZ Bank capital.
9. **FI is the more efficient twin** on platform metrics; Atruvia's group margins conceal a break-even core, thin-margin services, higher-margin software, and a loss-making venture (TRUUCO).
10. **The variable that matters most is the levy/pricing decision** (political), followed by input-cost inflation — not volume.

**Direct answers to the closing questions:** The economic engine is owner-financed cost recovery. The highest-quality revenue is captive Bankverfahren (retention) — but its pricing power is near-zero; the *best-quality* by margin is software (parcIT/ECON). Profitability is ~100% levy-driven at present. Operating leverage is weak and mostly illusory (levy step-ups, not scale). The 4% Zielrendite is economically meaningful as a cash mechanism but a fiction as a "margin." The investment race is funded by retained earnings + levies + DZ Bank + supplier financing, sustainable only at current intensity. The cooperative model delivers cheap IT absolutely but is less efficient than Finanz Informatik. The single most important variable is the sector's willingness to keep paying the levy/prices.

---

### RECOMMENDATIONS (staged, with thresholds)

**Stage 1 — Immediate analytical positions (now):**
- Treat the reported Betriebsergebnis as **investment pre-funding, not profit**. For any valuation or credit view, model the underlying (ex-levy) operating result at ~break-even.
- **Threshold to revise:** if the Digitalisierungsumlage is withdrawn or capped and Betriebsergebnis holds above €50m, the margin would be proven structural — upgrade the quality assessment.

**Stage 2 — Monitor the funding constraint (next 12–24 months):**
- Track EK-quote (38.2% and falling), Verb. ggü. Kreditinstituten, and trade-payables (supplier financing). 
- **Threshold:** EK-quote below ~30% or a new IT-Sonderumlage announcement would signal the model straining toward the €450m–€1bn scenario.

**Stage 3 — Watch the strategic pivots:**
- VR Payment integration (from 1 Jan 2027) — obtain the purchase price and card-processing revenue run-rate when disclosed.
- Usage-based pricing rollout — measure whether it raises the *effective* price to owners (revenue/account) or merely re-labels the levy.
- FI efficiency gap — if Atruvia's group revenue/employee moves toward FI's, the subsidiary-mix drag is being addressed.
- **Threshold:** a DORA critical-third-party (CTPP) designation would add direct oversight cost and should be priced into the margin outlook.

---

### CAVEATS

- **Perimeter risk is acute:** AG and Group figures are routinely conflated in secondary sources. This report keeps them separate; where Group FY2025 line items were unavailable (Northdata paywall), they are marked UNKNOWN rather than spliced.
- **Levy-to-profit identity is an ANALYTICAL INFERENCE** from the close numerical match (€89.0m EBIT vs ~€90m levy) plus management's explicit investment-funding rationale; the accounts do not separately disclose the levy line.
- **Pre-2015 (Fiducia/GAD) and pre-2023 category splits are not continuous** with the current entity/taxonomy (merger + presentation changes).
- **FI comparison mixes legal forms** (AG vs GmbH & Co. KG) and perimeters; treat efficiency gaps as directional, not precise.
- **Forward figures** (FY2026 guidance €1,974.6m Gesamtleistung / €77.9m EBIT; the €450m–€1bn scenario) are COMPANY CLAIM / HYPOTHESIS, not outcomes.
- **Several FY2025 AG balance-sheet items** (Materialaufwand ~€792.1m; Verb. ggü. Kreditinstituten ~€145m) are derived from disclosed YoY changes rather than read as absolute line items, and are flagged with "~".
- Several subsidiary figures (Serviscope €28.8m vs Gesamtleistung ~€44m; parcIT series) carry unreconciled perimeter discrepancies, flagged in-text.

*End of Volume IV. Volume V not begun, per scope.*


---

# Part V — Management, Culture, Competition, Moat, Risk & Strategic Evolution

### TL;DR
- Atruvia persists not because it is competitively excellent but because it is structurally inescapable: its member banks own it, cannot practically leave it, and route their entire regulated existence through it. The one exit precedent (Apobank→Avaloq, 2020) cost a "mittleren dreistelligen Millionenbetrag" (Finanz-Szene estimated ~€500m all-in), left ~2,500 bugs (500 in the "signifikant" category — a count Apobank disputed as "nicht nachvollziehen"), and collapsed customer satisfaction from 82% to 47% overall — it stands as a cautionary tale, not a template.
- The genuine, hard-to-replicate strengths are industrialised bank migration (60 migration weekends, all 11 Sparda-Banken onboarded, M.M. Warburg incoming) and accumulated regulatory/compliance capability; the rest of the "moat" is lock-in that risks producing under-investment, a thin FY2025 Betriebsergebnis of €89.0m at a 4.7% margin roughly equal to the ~€90m Digitalisierungsumlage, and a repeated outage record (2020 system-changeover, 2021 DDoS, 2023 up-to-520-banks, July 2026 ~490 banks).
- The captive utility model is sustainable for another decade ONLY if the sector resolves the investment-funding question (the circulating €450m–€1bn/yr scenario), contains IBM dependency (deliberately deepened by the 19 November 2025 z17 deal), and manages consolidation of its shrinking owner base — the single most plausible structural endgame is a partial or full consolidation with Finanz Informatik.

### Key Findings

**1. Leadership is a lineage of institutional stewards, not founders — and accountability is real but muffled.** Klaus-Peter Bruns (CEO 2006–2019) architected the 2015 merger and the agree21 "Mondlandung," then departed in the fallout of the 2018 BaFin special inspection (15 findings, 3 severe). Martin Beyer (34 years, spokesman 2019–2025) presided over migration completion, the 2021 rebrand and the pivot to a 4% Zielrendite, then left abruptly in June 2025 amid reported friction with co-CEO Coenen. The 2025–26 Vorstand refresh injected commercial-bank DNA (Kaurin ex-Barclays/ING-DiBa; Wiegelmann ex-BayernLB CFO; Japec ex-Commerzbank) into a cooperative utility — a clear signal of commercialisation and regulatory-hardening intent.

**2. The central question — why banks stay — resolves to "an unavoidable deal that is nonetheless mostly a reasonable one."** Ownership, ecosystem integration (DZ Bank clearing, Union Investment, R+V, VR Payment, BVR reporting all run through agree21), regulatory posture and the absence of a cooperative-specific alternative make staying rational; but the levies, ~5% annual price rises, negligible small-bank influence and outage exposure are the price. Members are not trapped in a bad deal, but they are trapped, and that removes the discipline that would prove it is a good one.

**3. The mainframe is not the bottleneck; investment-funding governance is.** Atruvia modernised COBOL in place (~85% Java-enabled via IBM Semeru) rather than replacing the core — a defensible, path-dependent choice validated by the Apobank and Sparda/Sopra failures. The binding constraint is the sector's willingness to fund the modernisation the front-runners can afford: FY2025 free cash flow was only ~€38m, capex hit €359.1m (18.7% Investitionsquote), and Coenen has openly floated an additional levy for the digital euro alone.

### Details

#### V.1 Institutional Architects and Leadership Lineage (replaces Founder Analysis)

**CONFIRMED FACT.** Atruvia has no founder. Its institutional DNA descends from two lineages: Fiducia (Fiducia Revisions- und Treuhand-Institut AG, founded 13 November 1924, Karlsruhe, "agree" system, south) and GAD eG (founded 26 December 1963, Münster, "bank21," north). The two attempted merger several times and failed; DER PLATOW Brief's characterisation — "Mehr als einmal haben die beiden genossenschaftlichen IT-Dienstleister Fiducia und GAD einen Anlauf zur Fusion genommen, nur um dann kurz vor der Zielgeraden den Deal doch noch platzen zu lassen" — captures the pre-2013 history. The Aufsichtsräte approved the decisive merger 30 September / 1 October 2014; owners approved November–December 2014; it became legally effective 1 July 2015 as Fiducia & GAD IT AG.

**The Bruns era (2006–2019): merger architect and accountability casualty.** Klaus-Peter Bruns led Fiducia from 2006 and, per Aufsichtsrat chair Jürgen Brinkmann, "hat maßgeblich den Zusammenschluss der ehemals zwei IT-Dienstleister Fiducia und GAD 2015 gestaltet." Two path-dependent decisions define his legacy:
- **Choosing agree21 over bank21 (ANALYTICAL INFERENCE: decisive path lock-in).** The merged entity adopted a common core "das im Kern auf agree basiert," extended with bank21 components; all ~400 former GAD banks were migrated onto it by 2019. This meant the *northern* (GAD/Münster) banks bore the migration pain — a political choice that concentrated disruption and set the template for Atruvia's later industrialised migration capability.
- **The captive levy-funded investment model.** The 2015 merger targeted ~€125m/yr in synergies via cost cuts (including ~939 of 5,500 positions removed without layoffs), with Bruns framing the deal's logic bluntly at the 2016 HV: "Unser Zusammenschluss ergibt für unsere Eigentümer nur Sinn, wenn unter dem Strich mehr herauskommt als vorher."

Bruns's departure is the cleanest accountability event in the company's history. He announced in spring 2019 he would not renew beyond 2019; the Börsen-Zeitung reported the Aufsichtsrat was "überrascht" and the step had "persönliche" motives. But the Handelsblatt's December 2019 exposé of the BaFin report drew the causal line explicitly: "Das Ausmaß der Kritik an der Fiducia wirft Fragen nach den Gründen für das Ausscheiden des früheren Vorstandsvorsitzenden Klaus-Peter Bruns und von Vizechef Carsten Pfläging auf." Pfläging left months earlier; Bruns "ist seit Mitte Oktober [2019] ebenfalls nicht mehr bei Fiducia GAD." **ANALYTICAL INFERENCE:** the "persönliche" framing was face-saving; the timing and the severity of the 2018 findings make the departures substantively accountability-driven, even if never formally attributed.

**The Beyer era (2019–2025): stabiliser, rebrand, and the 4% pivot.** Martin Beyer took over as co-spokesman (with Jens-Olaf Bartels) in August 2019 "in einer äußerst schwierigen Phase" (Keller). He was 34 years with the company/predecessors, board from 2013. His tenure delivered: completion of the agree21 series migration (60 migration weekends, ~60,000 bank workstations), the 1 September 2021 rebrand to Atruvia, the agile transformation, and the pivot to treating operating profit as investment fuel. Beyer's own framing of the finance strategy (2024): "Unsere Finanzstrategie basiert darauf, dass wir notwendige Investitionen künftig aus eigener Kraft tätigen. Wir wollen daher unser Betriebsergebnis steigern." His exit on 30 June 2025 was officially "einvernehmlich," but ChannelPartner reported it "erfolgte … aber nicht ganz freiwillig, es hätte 'Verstimmungen' zwischen den beiden Co-CEOs" gegeben. He received the DGRV's Raiffeisen-Schulze-Delitzsch gold medal — a valedictory honour consistent with a managed, dignified exit. **ANALYTICAL INFERENCE:** the combination of "mission accomplished" rhetoric, the gold medal, and the reported friction indicates a board choosing generational renewal and a single clear leader (Coenen) over a co-spokesman structure that had produced tension.

**Beliefs consistently reflected in strategy:** (a) sovereignty/independence ("digitale Souveränität," reinforced in the IBM deal); (b) migration as core competence; (c) modernise-in-place over rip-and-replace; (d) partnership rhetoric ("Digitalisierungspartner"). **Beliefs that changed:** from pure cost-utility (Bruns's synergy logic) toward a commercial, revenue-reinvesting, adjacency-expanding posture (Coenen's "Aktionsradius erweitern").

#### V.2 Current Management Team

**CONFIRMED FACT — the five-member Zielbild Vorstand (complete since 1 January 2026):**

| Member | Ressort | Since | Prior background | Signal |
|---|---|---|---|---|
| Ulrich Coenen (52) | Vorstandssprecher, Corporate Strategy & Development | Board Aug 2020; sole spokesman Jul 2025 | Bereichsvorstand Commerzbank; Geschäftsleitung E-Plus | Commercial-strategic continuity; telco/retail-bank instincts |
| Daniela Bücker | Core Banking & Technology | 2020 | Internal/technology | Technical continuity; platform-architecture voice |
| Julia Japec | Customer Success | 1 May 2025 | ex-Commerzbank | Customer/sales professionalisation |
| Željko Kaurin | Digital Banking | 1 Nov 2025 | ex-COO Barclays Bank Europe; 20+ yrs ING-DiBa | Digital-retail-banking scaling; payments |
| Dr Markus Wiegelmann (56) | Finance, Regulation & HR; Arbeitsdirektor | 1 Jan 2026 | CFO BayernLB (to Jun 2025); began 1998 in Deutsche Bank risk; promovierter Mathematiker | Regulatory/financial hardening |

**The pattern — internal continuity plus senior commercial-bank hires.** Coenen and Bücker anchor institutional memory; Kaurin, Wiegelmann and Japec import large-bank operating experience. Die-privatbank.de read it precisely: "Die neue Mannschaft spiegelt einen Mix aus interner Erfahrung und externen Impulsen wider." **ANALYTICAL INFERENCE:** hiring commercial-bank executives into a cooperative IT utility signals three intentions — (1) to run Atruvia more like a commercial technology firm (Aktionsradius expansion into cards, consulting, brokerage, crypto); (2) to raise regulatory/financial discipline after the 2018 and 2023–25 BaFin episodes (Wiegelmann's mandate explicitly bundles Finance + Regulation); and (3) to speak "die Sprache der Banken" to owner-customers. Wiegelmann's HV framing — "Wir als Atruvia verstehen uns als Innovator, als entscheidenden Motor der Veränderung" — is notably un-utility-like.

**Leadership depth, key-person and succession risk.** **HYPOTHESIS (elevated risk):** a Vorstand in which three of five members have <18 months tenure carries real integration and key-person risk, particularly with a single spokesman (Coenen) concentrating strategic authority. The prior structure lost two members at end-2022 (Frohnhoff, Staff) in a six-to-four reduction and two more in 2025 (Beyer, Teufel) — a high churn rate. **UNKNOWN:** executive compensation is not individually disclosed (unlisted AG); no Zielrendite-linked variable structure is public.

#### V.3 Management System

**Where real decision power sits.** Atruvia runs a two-plane system: an internally agile execution plane (Tribes/Squads) and an externally owner-governed strategy plane (BVR committees). The roadmap is owner-set via the Bundeseinheitliches Strategieportfolio (39 initiatives, 36 touching Atruvia), Kompetenzteams, Fokusgruppen and the Strategie- und Portfolioplattform. Individual small banks have negligible direct roadmap power; power is collective and political.

**Investment approval.** **ANALYTICAL INFERENCE from evidence:** authorising a €359m capex year is not a pure Vorstand decision. The levy/price mechanism runs through the BVR's Ständiger Projekt- und Strategieausschuss (SPSA) and the Aufsichtsrat: the Börsen-Zeitung reported that "der Aufsichtsrat … Ende April [2023] über eine Lösung entscheiden [soll], wie die drohende Abrisskante bei den IT-Investitionen verhindert werden kann," converting the expiring IT-Sonderumlage into a regular price rise. So the true capital-allocation authority is a triangle: Vorstand proposes, Aufsichtsrat approves, BVR committees legitimise the levy on owners.

**The Zielrendite mechanism.** The 4% target is a deliberately modest, utility-style return — Coenen: "Der Konzern solle nicht Gewinnmaximierung betreiben, sondern den Eigentümern ein stabiles Ergebnis und einen gewissen Dividendenbeitrag liefern … Alles, was wir an zusätzlichen Erlösen reinholen, versuchen wir zu reinvestieren." **This is the core of the management system: profit is a means to an investment end, not an end.** The tension is structural — agile internally, consensus-bound externally; the roadmap's velocity is capped by the slowest governance layer, not the fastest squad.

#### V.4 Culture — Declared versus Revealed

**Declared.** Agility, New Work, sovereignty, partnership, cooperative values, "Digitalisierungspartner." The shared-leadership New Work model (People Lead = disziplinarische Führung/Change Enabler; Tribe Lead = fachliche Führung/Product Owner) is publicly documented.

**The stated trigger for transformation (original source located).** The oft-quoted driver — "Unterschiedlichste Qualitätsprobleme, eine niedrige Mitarbeiterzufriedenheit und vor allem eine geringe Kundenzufriedenheit" — originates from an Atruvia self-presentation at the HR Pioneers Agile HR Conference 2023 ("Aufspringen. Anschnallen. Atruvia — Unsere Achterbahnfahrt durch die Agile Transformation"), by People Leads Björn Langer and Marvin Beck with HR consultant Uwe Joas. The same talk states plainly: "Wir haben in unserem neuen Zusammenarbeitsmodell eine Führungsebene herausgenommen und die geteilte Führung umgesetzt." **COMPANY CLAIM (promotional context):** this is the earliest articulation, but it is a conference self-presentation, not an audited report.

**Important distinction (correcting a common conflation).** The "neues Betriebsmodell" (nBM) introduced from 2025 is NOT Atruvia's internal org restructuring — it is a product/process transformation programme *for the member banks*, a Top-Initiative of the BSP led by Margit Messika under Vorständin Japec, targeting "bis 2035 eine Bruttoergebniswirkung von 2,6 Mrd. Euro" and responding to "dem erwarteten Personalrückgang von rund 30 Prozent bis 2030" in the banks. The internal agile model (Spotify-style) is the older ~2020–21 transformation.

**Revealed culture — Declared vs Revealed matrix:**

| Declared value | Revealed behaviour (evidence) | Verdict |
|---|---|---|
| Quality orientation | Repeated outages (2020 system-changeover, 2021 DDoS, 2023 up-to-520-banks, July 2026 ~490 banks); 2018 BaFin: worst grades for QA/testing of VR-Control | Contradiction: quality is aspired to, not consistently delivered |
| Regulatory discipline | 2018 (15 findings, 3 severe) and 2023–25 parcIT findings → bank capital add-ons; audIT programme run 2018–21+ | Improving under pressure; reactive not proactive |
| Employee satisfaction | Kununu 4.3/5, 93% recommend, >1,900 reviews, 5× Top Company; but recurring complaints of "regelmäßige interne Umstrukturierung" and leadership "weiter weg … denn je" | Genuinely strong aggregate; transformation fatigue at the edges |
| Agility/speed | Internal squads agile; roadmap gated by BVR consensus; core rebuild "bis 2030 und länger" | Speed is local, not systemic |
| Transparency | Crisis comms praised in 2021 DDoS; but outage root causes often undisclosed (Nov 2023) | Mixed |
| Tolerance for failure | Accountability exits (Bruns, Pfläging 2019) | Failure has consequences at the top |

**Kununu detail (labelled).** Atruvia's own published aggregates: 4.3/5, 93% Weiterempfehlung, >1,900 reviews; category awards for Gehaltszufriedenheit and Familienfreundlichkeit; Top Female Workplace (Platz 6 Deutschland IT, Platz 3 Baden-Württemberg). Numeric sub-scores per category are not publicly retrievable; Kununu is self-selecting and Atruvia curates republished quotes. Recurring negatives: frequent restructuring, perceived leadership distance, uneven agile maturity, communication gaps. Atruvia's own review-reply concedes: "Atruvia geht seit gut 3 Jahren einen tiefgreifenden Transformationsweg. Diesen mit ca. 5000 Mitarbeitenden gemeinsam zu schaffen ist ein[e Herausforderung]." Engineering salary bands €65,000–€102,000.

#### V.5 Incentive Architecture

No equity, no options, no share-price signal. **What actually motivates behaviour:**
- **Vorstand:** compensation structure UNKNOWN; the Zielrendite (4%) is the visible target, but it is a *floor-style* stability target, not an upside-maximising one. **ANALYTICAL INFERENCE:** absent equity, the dominant incentive is institutional reputation, sector standing (cf. Beyer's gold medal), and the avoidance of BaFin/outage embarrassment. This biases toward risk-aversion and continuity over bold bets — mostly appropriate for critical infrastructure, but a brake on modernisation velocity.
- **Tribe Leads / People Leads:** split leadership deliberately separates delivery (Tribe) from people development (People) — reduces empire-building but, per reviews, can leave staff feeling leadership is "distant."
- **Engineers:** salary-band progression; the risk is that build-once utility work rewards reliability over innovation.
- **"Customer Success" when customers cannot leave:** **the sharpest incentive paradox in the company.** Japec's Customer Success function cannot be disciplined by churn (owners cannot exit). Its incentive must therefore be proxy metrics — Digitalisierungsquote, app ratings, migration satisfaction. **HYPOTHESIS:** these are gameable and softer than real switching pressure, blunting the incentive to improve to a genuinely competitive standard.
- **Compliance/risk:** post-2018, heavily incentivised by BaFin exposure (audIT); commercial vs compliance incentives conflict when speed-to-market meets MaRisk/BAIT — the 2018 and 2023 findings show compliance historically lost until forced.
- **Owner-banks:** as owners they want low levies and dividends; as customers they want investment and reliability. This dual identity blunts the improvement incentive: the same institution that demands modernisation resists paying for it (documented owner "Preisresistenz").

#### V.6 Competitive Universe (re-cut by threat vector)

**A. The structural twin — Finanz Informatik (FI).** Not a customer-competitor but the definitive efficiency benchmark and the counterparty in any sector consolidation. Per FI's Jahresbericht 2024 ("Zukunft. Digital. Machen."): "der konsolidierte Umsatz stieg 2024 auf rund 2,6 Milliarden Euro"; "Mit 649 Neueinstellungen wuchs die Zahl der Beschäftigten (Vollzeitäquivalente) auf 5.037"; "328 Millionen Euro in die Neu- und Weiterentwicklung … OSPlus"; ~114m accounts, >205bn technical transactions, ~350 Sparkassen, IBM-mainframe-based, on-premise; App Sparkasse 17.9m active users. Revenue/employee ~€516k (FI) vs ~€218k (Atruvia Group)/~€324k (Atruvia AG). **The two already co-operate** (joint dual IT-degree with FH Münster from 2026).

**B. Commercial core-banking vendors (contest external wins and defections).** Avaloq (took Apobank), Temenos, Sopra Steria (Corbas MBS — M.M. Warburg migrating *away from it to Atruvia*), FIS/Kordoba, SAP (Fioneer), Finastra; cloud-native challengers Thought Machine (Vault), Mambu (Berlin; multi-unicorn on a ~€5bn valuation; N26/ABN AMRO), 10x Banking, Tuum. **Threat horizon:** low for the captive base; real only at the margins (external banks, private banks). No cloud-native vendor has yet won a German cooperative or savings bank at core-system scale.

**C. The banks' own alternatives.** Build in-house (effectively impossible at single-cooperative-bank scale); consortium build (the seven Sparda-Banken abandoned their Sopra Steria joint build — see V.7/V.10 — and moved to Atruvia); exit the sector. **All three have failed or proven impractical.**

**D. Edge erosion.** BaaS/embedded-finance providers, fintech modules, Big Tech in payments/identity, and neobanks (N26, Trade Republic, Revolut) competing with the member banks themselves — the last is the most insidious because it shrinks Atruvia's customer base indirectly.

**E. Suppliers as competitors.** IBM (could move up the stack via consulting/software), Microsoft/hyperscalers. **ANALYTICAL INFERENCE:** the November 2025 IBM deal both deepens dependency AND buys sovereignty guarantees (HashiCorp Vault, "full control … in its own data centers," quantum-safe encryption) — a deliberate hedge against exactly this risk.

#### V.7 Competitor Teardowns

**Atruvia vs Finanz Informatik:**

| Dimension | Atruvia | Finanz Informatik |
|---|---|---|
| Revenue (2024/25) | AG €1,921m (2025); Group ~€2.5bn | ~€2.6bn (2024) |
| FTE | Group ~10,076; AG 5,847 | 5,037 |
| Accounts | ~97m | ~114m |
| Technical transactions | ~80bn+/yr | >205bn/yr |
| Institutions | ~670–730 coop + others (~950 customers) | ~350 Sparkassen |
| Core platform | agree21 (agree lineage) | OSPlus |
| Core investment | levy + reinvested profit; capex €359.1m (2025) | €328m OSPlus Basisangebot (2024) |
| Revenue/employee | ~€218k Group / ~€324k AG | ~€516k |
| Deployment | on-prem/own DCs | on-prem/own DCs |
| Tech base | IBM Z (z15→z17) | IBM mainframe |
| App | VR BankingApp ("Bestnoten," near-Sparkasse in tests) | App Sparkasse (Capital/Handelsblatt Testsieger; 17.9m active users) |
| Cards | consolidating now via VR Payment (2027) | consolidated 2024 into "Qards" (Bayern Card-Services + Pluscard) |
| Governance | AG, 99.68% coop-owned | GmbH & Co. KG |

**Read:** FI is materially more efficient per head (~2.4× revenue/employee), more transactionally scaled, and roughly 2–3 years ahead on both card consolidation and app-award recognition. Atruvia's app has "aufgeholt … nahe bis zu den Sparkassen" (Coenen) but is "nicht superspitz auf eine junge Zielgruppe ausgelegt." **The efficiency gap is the single most damning comparative datapoint** — though it is partly explained by Atruvia's more fragmented customer base and larger low-margin subsidiary estate (Ratiodata).

**Atruvia vs commercial/cloud-native vendors:**

| Dimension | Atruvia | Avaloq/Temenos | Cloud-native (Thought Machine/Mambu) |
|---|---|---|---|
| Target | captive coop sector | mid/large banks, wealth | digital banks, fintechs |
| Deployment | on-prem, multi-tenant | on-prem/SaaS | cloud-native SaaS |
| Stack | mainframe + Java/OpenShift | modernised legacy/Java | microservices, cloud |
| Migration record | industrialised (60 weekends) | Apobank: debacle | few full-bank cores in DE |
| Regulatory posture | deep German/coop-specific | general | maturing in DE |
| Switching economics | near-prohibitive (owned) | high | lower but unproven at scale |

#### V.8 Why Member Banks Stay — and What That Costs Them

**Decomposition of why a cooperative bank stays:**
1. **Ownership** — it owns the supplier (99.68% coop-owned; ~91.63% via three regional Beteiligungs-KGs pooled through VR-FGI Beteiligungsholding).
2. **Ecosystem integration** — DZ Bank clearing, Union Investment, R+V, VR Payment, BVR reporting all run through agree21. Leaving means rebuilding every one of these interfaces.
3. **Regulatory posture** — Atruvia's compliance IS the bank's compliance under §25b KWG. A commercial vendor shifts that burden onto the bank.
4. **Cost / shared scale** — no single cooperative bank can replicate mainframe-scale economics.
5. **Absence of a cooperative-specific alternative** — no vendor offers the coop-verbund integration out of the box.
6. **The Apobank precedent** — the empirical proof that leaving is ruinous.

**What staying costs (quantified where evidence permits):**
- **Levies:** IT-Sonderumlage 2018–2023 (€60m/yr from banks ≈ €300m cumulative, + €180m DZ Bank + ~€200m self-funded); Digitalisierungsumlage rising, per DER PLATOW Brief, "von zuletzt 30 Mio. Euro über 60 Mio. im laufenden Jahr auf 90 Mio. Euro in 2025" (headline: "Atruvia verdreifacht Digital-Preise für Genossen").
- **Price rises:** ~5% in 2023 and 2024 as "inflationsbedingte Preisanpassung."
- **Constrained influence:** small banks have negligible roadmap power.
- **Outage exposure:** four material events 2020–2026.
- **Modernisation pace:** core rebuild "bis 2030 und länger" (Coenen); the €450m–€1bn/yr scenario to reach European front-runners.

**Judgement.** Members are getting an **unavoidable deal that is nonetheless mostly reasonable** — but reasonableness is unproven precisely because it is untested by exit. The levies buy genuine shared infrastructure and regulatory shelter that no member could build alone; the Apobank case shows the alternative is worse. But the absence of contestability means there is no market discipline confirming the price is fair, and owner price-resistance is simultaneously suppressing the investment members say they want. **This is structural advantage and lock-in delivering genuine — but not demonstrably optimal — value.**

#### V.9 Moat Analysis (reframed: prevents-exit vs creates-value)

| Candidate moat | Score /5 | Prevents exit? | Creates value? | Mechanism & durability |
|---|---|---|---|---|
| Captive ownership | 5 (as lock); 2 (as value) | Yes, absolutely | Only if it disciplines investment — it does not | Structural; durable until sector restructures. **Risk: complacency/under-investment** |
| Ecosystem integration | 4.5 | Yes | Yes — genuine build-once integration | High; replicable only by another verbund |
| Regulatory/compliance capability | 4 | Partly | Yes — real, accumulated, hard to buy | Durable; strengthened by audIT/DORA experience |
| agree21 multi-tenant platform | 3.5 | Yes | Yes but ageing | Path-dependent; modernise-in-place bet |
| Migration capability | 4 | No | **Yes — the most underrated genuine advantage** | Industrialised (60 weekends, 11 Sparda, Warburg); replicable only with scale |
| Scale economics | 3.5 | No | Yes but behind FI | Real but sub-FI efficiency |
| Data position | 2 | No | Constrained by GDPR processor role | Weak as moat |
| Switching costs | 5 (lock); 2 (value) | Yes | Neutral | Very high; Apobank-proven |
| Brand/trust | 3 | Partly | Yes within verbund | Outages erode it |
| Talent | 3 | No | Adequate; nearshore (Cluj ~700) + Kununu strength | Contested by COBOL wave |

**Critical reframe:** the largest "moats" (captive ownership, switching costs) are lock, not value. Scored as competitive strengths they flatter Atruvia; scored honestly they reveal the central risk — **the lock removes the pressure that would otherwise force the value.** The genuine, exit-independent advantages are **migration capability and regulatory capability**; these would survive even in a contestable market.

#### V.10 Replication and Replacement Test

**(a) Replication — rebuild Atruvia from zero:** effectively irreproducible on any reasonable horizon. Recreating a multi-tenant core serving ~950 institutions/97m accounts, four high-security data centres, ~80bn+ transactions/yr, the full verbund-integration layer, and BaFin-tested compliance would require a decade-plus, multi-billion-euro programme, thousands of specialist staff, and — critically — the migration of every institution without catastrophic disruption. Classify: data-centre hardware = purchasable; microservices/app = buildable; verbund integration + migration machinery + regulatory trust = effectively irreproducible/path-dependent.

**(b) Replacement — swap Atruvia for a commercial vendor: the Apobank case study.**
- **What it cost:** Apobank CEO Ulrich Sommer cited a "mittleren dreistelligen Millionenbetrag"; Finanz-Szene estimated ~€500m all-in (with reporting up to ~€807m incl. 2021 and consolidation), plus annual run costs "im zweistelliger Millionenhöhe."
- **How long:** selection from 2015, project from early 2018, go-live Pentecost 2020 (delayed 3 months from a planned 1 March), consolidation into 2021.
- **What went wrong:** "Big Bang" forced because Avaloq could not run on Fiducia hardware ("Mischbetrieb … nicht erwünscht"), so hardware+software switched simultaneously; per inside-it.ch (3 June 2021), Apotheke ad hoc reported "letzten Januar nach wie vor 2500 Bugs gezählt worden seien. 500 davon entfielen auf die Kategorie 2 ('signifikant')" — a figure Apobank disputed ("Die Zahl von 2500 Bugs können wir nicht nachvollziehen"); many subsystems, online banking and the phone system failed; an external call centre was required; the app rated barely above one star. Per Finanz-Szene's customer survey coverage, overall satisfaction fell "von 82% … auf 47%," among self-employed Heilberufler from 80% to 40%, and among Vertriebspartner "von zuvor 78% sogar auf nur noch 27%"; depot-at-competitor share rose 23%→30%. CEO Sommer's later departure was linked "dem Vernehmen nach" to the migration.
- **What it proved:** for a single mid-sized bank, replacement is financially ruinous, operationally hazardous and reputationally scarring. For the *whole cooperative sector* (~950 institutions) it is inconceivable as a coordinated act. **This is the empirical foundation of Atruvia's lock.**

#### V.11 Porter's Five Forces (adapted for a captive utility)

- **Rivalry:** near-zero for the captive base; real but marginal for external wins (Warburg won; private banks contested). **LOW overall.**
- **Supplier power (IBM):** **VERY HIGH and deliberately deepened.** Per the IBM/Atruvia joint release (Frankfurt/Ehningen, 19 November 2025), Atruvia will use "IBM z17 … as a cornerstone" for "mission critical operations including the core banking system." The multi-year z17 agreement (z15→z17; a ~€145m payables jump funded the 2025 mainframe purchase) locks Atruvia's core to IBM Z, z/OS, IMS, Db2. Vorständin Daniela Bücker: "Die Zusammenarbeit mit IBM ermöglicht es uns, in allen Dimensionen der Souveränität zukunftsfähig aufgestellt zu sein: Von Daten über Infrastruktur bis hin zu Cloud, Hersteller- und Innovationssouveränität." The paradox: the deal is *framed* as sovereignty but *is* dependency.
- **Buyer power:** **paradoxical.** Buyers are owners; power is collective and political (BVR/SPSA), not commercial. Individual banks are near-powerless; the collective can set levies and, ultimately, restructure the company.
- **Substitutes:** cloud-native core, BaaS, commercial vendors — **LOW-MODERATE now, rising slowly.** Not yet mature at German-coop scale.
- **New entrants:** near-impossible for the captive core; **real at the module level** (fintech components banks might otherwise buy from Atruvia).

#### V.12 PESTLE (material factors only)

- **Political:** German/EU sovereignty and cloud-independence debates strongly favour a domestically-run, on-prem utility; the cooperative sector's political weight protects it; digital-euro policy imposes cost.
- **Economic:** interest-rate normalisation improved bank profitability (capacity to fund levies); consolidation shrinks the paying base; IT-cost inflation drives the ~5% price rises.
- **Social:** banking-workforce demographics (banks' ~30% headcount decline expected by 2030 — the nBM's raison d'être), the COBOL retirement wave, branch decline, rising digital expectations (especially the under-served young cohort Coenen acknowledges).
- **Technological:** cloud-native core, AI/agentic AI (plainGPT/GenoGPT, "autonomous banking" IBM framing), quantum-safe crypto (in z17 deal), instant payments, EPI/Wero.
- **Legal:** DORA (Atruvia NOT designated a CTPP on the 18 Nov 2025 first list of 19 providers; IBM WAS, Lead Overseer EBA; FI also not designated), MaRisk/BAIT, §25b KWG, GDPR (processor role), EU AI Act, PSD3.
- **Environmental:** data-centre energy and sustainability reporting; the IBM deal foregrounds "sustainable banking."

#### V.13 Strategic Flywheels (positive)

1. **Scale flywheel:** more banks → more scale → build-once economics → lower cost per bank → more attractive to external banks → more scale. **Evidence:** all 11 Sparda-Banken, Warburg incoming, ~5% price rises still tolerable. **Limit:** consolidation shrinks the bank count even as accounts grow; efficiency still trails FI.
2. **Migration flywheel:** migration capability → external wins → scale → better migration capability. **Evidence:** 60 migration weekends, industrialised "Serienmigration," 22 institutions since 2021, 40–45 merger-migrations/yr. **This is Atruvia's strongest genuine flywheel.**
3. **Regulatory build-once flywheel:** compliance built once → attractive to regulated institutions → more scale. **Evidence:** the verbund's regulatory shelter. **Limit:** repeated BaFin findings show the compliance advantage is real but not flawless.

#### V.14 Negative Flywheels

1. **Owner price-resistance → under-investment → falling competitiveness → member banks lose retail customers → consolidation → fewer paying customers → more price pressure.** **Likelihood: HIGH; Severity: HIGH.** Evidence: the €450m–€1bn/yr gap; FY2026 margin guidance falling to ~3.9%; FCF only ~€38m.
2. **Outage → trust damage → regulatory scrutiny → compliance cost → less investment capacity → more fragility.** **Likelihood: MODERATE; Severity: HIGH.** Evidence: 2020/2021/2023/2026 events; 2018 and 2023 BaFin cycles.
3. **COBOL retirement → rising maintenance cost → slower modernisation → widening gap to cloud-native.** **Likelihood: MODERATE; Severity: MODERATE.** Mitigated by Semeru Java-enablement and nearshore build-out.
4. **Consolidation → fewer, larger owners → greater individual bargaining power → pressure on the collective model.** **Likelihood: MODERATE-HIGH; Severity: MODERATE.** A top-ten Volksbank gains leverage the collective model was not designed for.

#### V.15 Theory of Constraints / Strategic Bottleneck

**If everything else improved 50%, the binding constraint is sector investment-funding governance — not the mainframe.** Evidence: the modernisation the front-runners can afford (€450m–€1bn/yr) exceeds what owner-banks will currently fund; FCF is thin (~€38m); the digital euro alone may need "einen zusätzlichen Investitionsbeitrag" (Coenen: "Das ist eine Herausforderung, die lässt sich nicht mal so aus der Portokasse finanzieren"). The COBOL core is a *managed* constraint (Semeru), IBM dependency is *contracted*, talent is *adequate*. The true bottleneck is the political-economic willingness of ~700 owner-customers to fund transformation at competitive speed. **Next bottleneck if solved:** execution capacity/talent to spend that money well (the core rebuild "bis 2030 und länger").

#### V.16 Risk Register (heatmap)

| Risk | Prob | Severity | Detect | Residual | Horizon |
|---|---|---|---|---|---|
| Catastrophic/prolonged outage | Med | Very High | High | High | Ongoing |
| DORA CTPP designation | Low-Med | Med | High | Low-Med | 1–3y |
| Further BaFin enforcement | Med | Med-High | High | Med | Ongoing |
| Cyber/ransomware | Med | Very High | Med | High | Ongoing |
| IBM dependency/price shock | Med | High | High | Med-High | 3–7y |
| COBOL skills wave | Med | Med | High | Med | 3–10y |
| Investment underfunding | High | High | High | High | Ongoing |
| Member-bank consolidation | High | Med | High | Med-High | Ongoing |
| Large bank defection | Low | High | Med | Med | Ongoing |
| VR Payment integration | Med | Med | Med | Med | 2026–27 |
| Key-person (new Vorstand) | Med | Med | Med | Med | 1–3y |
| Loss-making subsidiaries (TRUUCO) | High | Low | High | Low | Ongoing |
| Data protection breach | Low-Med | High | Med | Med | Ongoing |
| Reputational contagion to coop brand | Med | High | Med | Med-High | Ongoing |

**Single points of failure:** the agree21 central platform (proven by the July 2026 event that NETZWELT reported affected "490 Banken," with app/online banking deliberately switched off and, "zwischen 9:47 Uhr und 10:38 Uhr auch die Websites der betroffenen Banken nicht erreichbar") and IBM Z. Both are, by design, concentrated.

#### V.17 Stress Tests

1. **Catastrophic multi-day outage:** immediate loss of banking for a majority of ~700 banks; severe reputational/regulatory fallout; survivable (no exit alternative) but forces emergency BaFin measures and possibly governance change.
2. **DORA CTPP designation:** direct ESA oversight, JET inspections, reporting burden; Coenen already judges DORA effort "unaufwendiger als für unsere Banken" — manageable, reputationally mixed.
3. **Formal BaFin measures after 2023 inspection:** capital add-ons already flowed to primary banks via parcIT; escalation would raise sector cost and pressure the Vorstand.
4. **IBM sharp price rise / mainframe exit:** high cost given the fresh z17 lock; multi-year contract provides medium-term planning security; migration off Z would be a decade-long megaproject.
5. **€450m–€1bn/yr requirement materialises:** forces either much higher levies (owner revolt risk) or restructuring; the defining financial stress test.
6. **Consolidation to <400 banks:** accounts persist but governance concentrates; larger owners gain leverage; collective model strained.
7. **Top-ten Volksbank defects:** symbolic shock; Apobank precedent deters; would trigger a sector crisis of confidence.
8. **Successful ransomware encrypting core:** existential operational event; mitigated by z17 confidential computing/quantum-safe encryption and four DCs; residual risk high.
9. **VR Payment card integration fails/slips:** contained (2026–27), reputational, not existential.
10. **Atruvia–FI merger talks open:** the most consequential structural scenario — see V.20 H3.
11. **Cloud-native vendor wins a German coop/savings bank:** low probability near-term; would be a genuine strategic warning shot.
12. **Multiple simultaneous Vorstand departures:** elevated given three sub-18-month tenures; would stall the Aktionsradius strategy.

#### V.18 What Could Make Atruvia Obsolete?

- **Cloud-native core reaching German-coop maturity:** possible but slow; does not remove the verbund-integration or migration problem. **Atruvia can adopt elements (OpenShift already in stack).**
- **BaaS/modular erosion from the edges:** real and gradual; erodes module revenue, not the regulated core.
- **AI-assisted core-banking replacement dramatically lowering migration cost — THE single most important potential disruptor.** If AI cuts the cost/time/risk of core migration by an order of magnitude, the Apobank deterrent weakens and the lock loosens. **BUT** Atruvia is itself building the AI stack (plainGPT/GenoGPT, "autonomous banking" with IBM) and could use AI to *lower its own* migration and maintenance cost — turning the disruptor into a defensive tool. **Ambiguous: could commoditise the lock OR reinforce it.**
- **Hyperscalers up the stack:** contained by sovereignty politics and the IBM sovereignty framing.
- **Radical consolidation producing build-capable banks:** even the largest coop bank is too small to self-build economically.
- **Sector merger with FI:** not obsolescence but transformation (V.20 H3).

**Verdict:** no single technology makes Atruvia obsolete because the customer problem (regulated, integrated, migrated banking for a whole verbund) persists. The lock could *loosen* if AI collapses migration economics — the one scenario worth watching closely.

#### V.19 Strategic Optionality

| Adjacency | Classification | Rationale |
|---|---|---|
| National card processor post-VR Payment | Plausible → Natural | Deal effective 1 Jan 2027; per McDermott, "a significant portion of all credit card transactions in Germany is processed through Atruvia's systems" |
| Sell platform components/EGP outside sector | Plausible | Bücker's API/technologieoffene-Plattform signal; unproven externally |
| External (non-coop) core-banking sales | Plausible | Warburg, private banks, ADAC; but dilutes coop focus |
| Commercialise AI stack (plainGPT/GenoGPT) | Plausible | Steep internal adoption ("eine der steilsten Adoptionskurven"); EU-hosted; sellable to regulated peers |
| Regulatory/compliance software (parcIT/FORUM) | Natural | Existing products; parcIT's own BaFin findings a caution |
| BPO expansion (Serviscope/Peras) | Natural | Existing, low-margin |
| Consulting JV (Awado/GVB) | Plausible | Under active review, decision autumn 2026 |
| Nearshore as a business (Accesa/RaRo) | Stretch | Internal capability, not a market offering |
| International coop-banking expansion | Strategic fantasy | No evidence, no mandate |
| Merger/deep cooperation with FI | Plausible (sector-level) | Already co-operating on training; the structural endgame |

#### V.20 What Is Atruvia Becoming? (probability-ranked)

- **H1 — remains a captive coop utility, essentially unchanged. ~35%.** For: ownership, Apobank deterrent, sovereignty politics. Against: Coenen's explicit Aktionsradius expansion; commercial-bank Vorstand hires; investment-funding pressure. **Base case with drift.**
- **H5 — progressively disintermediated at the edges while retaining the regulated core. ~25%.** For: BaaS/fintech module erosion, neobank pressure on member banks. Against: Atruvia's platform/API strategy actively defends the edge.
- **H4 — payments/card processor of national significance. ~15%.** For: VR Payment Issuing-Processing (effective 1 Jan 2027), credit-card processing, "Karten-Powerhouse" framing. Against: scope limited to issuing; VR Payment keeps acquiring/POS/Händlergeschäft.
- **H3 — merges/deeply consolidates with Finanz Informatik. ~12% within 10y, rising.** For: identical IBM-mainframe utility models, joint training venture, sector cost logic, sovereignty argument for one national banking-IT champion. Against: deep cultural/ownership rivalry (rot vs blau-orange), governance complexity, competition concerns.
- **H6 — restructured by the sector after an investment/governance crisis. ~10%.** For: the €450m–€1bn funding gap, thin FCF. Against: owners prefer incremental levies to upheaval.
- **H2 — becomes a genuinely commercial open-market core-banking vendor. ~3%.** For: rhetoric. Against: captive identity, no track record of open-market core wins, coop mandate.

#### V.21 Five-Year and Ten-Year Strategic Map

- **Base case (2031):** captive utility with expanded card/consulting/AI adjacencies; margin ~4%; levies persist; agree21 modernised in place; FI gap narrows slowly.
- **Strong execution:** investment-funding resolved; core rebuild on track; app leadership; external wins accumulate; margin stable, competitiveness rising.
- **Investment crisis:** funding gap unresolved; modernisation slips; competitiveness erodes; pressure toward H6.
- **Regulatory shock (DORA CTPP + BaFin measures):** higher compliance cost, reputational damage, governance intervention; survivable.
- **Technology disruption (cloud-native/AI migration maturity):** lock loosens; Atruvia must adopt AI-native migration or cede edge share.
- **Sector consolidation (Atruvia–FI, 2031–2036):** a single German banking-IT utility (>€5bn revenue, ~10,000 FTE, >200m accounts) — the most transformative outcome.
- **Major operational failure:** trust shock; emergency measures; accelerates governance reform.

#### V.22 Sector Misconceptions

1. **"DZ Bank owns ~20% of Atruvia."** FALSE (established). DZ Bank holds ~0.35% directly; the ~20% figure refers to Verimi. Persists via lazy conflation.
2. **"Atruvia is just an IT provider."** Reality: it is the operational nervous system, compliance backbone and increasingly the card/payments and consulting infrastructure of the entire verbund.
3. **"Captive ownership means it is safe."** Reality: captivity prevents exit but risks under-investment; safety is conditional on funding and reliability.
4. **"The reported profit is a commercial margin."** FALSE. FY2025 Betriebsergebnis (€89.0m, 4.7% margin, "rund ein Drittel über dem des Geschäftsjahres 2024") ≈ the ~€90m Digitalisierungsumlage; strip the levy and the underlying result is near zero. Profit is engineered investment fuel, not a market margin.
5. **"The banks could switch if they wanted to."** Reality: Apobank proves switching is ruinous even for one bank; for the sector it is inconceivable.
6. **"The mainframe is a legacy liability."** Partly false: IBM Z delivers the reliability, security and throughput (~80bn+ transactions) the use-case demands; the z17 deal buys quantum-safe crypto and AI acceleration. The liability is skills/cost, not capability.
7. **"Atruvia and FI are basically the same."** Similar structure, but FI is ~2.4× more efficient per head, further ahead on cards and app awards.
8. **"A cooperative cannot be a competitive technology company."** Untested rather than false: Atruvia's migration and compliance capabilities are genuinely competitive; its efficiency and modernisation velocity are not yet.

#### V.23 Management and Capital-Allocation Judgement

| Decision | Verdict | Evidence |
|---|---|---|
| 2015 merger | Value-creating | €125m/yr synergies, single platform |
| agree21 over bank21 | Strategically necessary | Consolidation completed; northern banks bore pain |
| "Mondlandung" migration | Value-creating | Built the migration flywheel |
| Modernise COBOL in place | Strategically necessary | Apobank/Sparda-Sopra failures validate it |
| 2021 rebrand | Questionable/neutral | Cosmetic; limited evidence of value |
| Levy-funded investment model | Strategically necessary but strained | Funds investment; masks near-zero underlying profit |
| 4% Zielrendite | Questionable | Too modest to self-fund the €450m–€1bn gap |
| Agile transformation | Too early to judge | Kununu strong; transformation fatigue evident |
| Response to 2018 BaFin | Value-creating (reactive) | audIT largely delivered by end-2021 |
| Nov 2025 IBM z17 | Strategically necessary; risky | Buys sovereignty features; deepens dependency |
| VR Payment acquisition | Strategically necessary | Consolidates cards; Bundeskartellamt B9-75/26 pending |
| External-customer growth | Too early | Warburg/Sparda wins; dilutes focus |
| Nearshore build-out (Cluj ~700) | Value-creating | Talent/cost hedge |
| Sustained support of loss-making TRUUCO | Questionable | ~−€7.98m; no clear path to value |

#### V.24 Volume V Reconstruction — synthesis answers

- **Why does Atruvia persist?** Because its owners cannot leave it, cannot rebuild it, and cannot find a cooperative-specific alternative — persistence is structural, not competitive.
- **Genuinely defensible vs merely locked in?** Defensible: migration capability, regulatory capability, verbund integration. Locked-in (not defensible on merit): the captive base and switching costs.
- **Hardest to replicate / easiest?** Hardest: verbund integration + migration machinery + regulatory trust (effectively irreproducible). Easiest: data-centre hardware and app front-ends.
- **Current bottleneck:** sector investment-funding governance.
- **Single greatest structural risk:** owner price-resistance driving chronic under-investment while the base consolidates.
- **Most dangerous competitor/force and horizon:** not a vendor but AI-driven collapse of migration economics (5–10y) — the only force that loosens the lock — with sector consolidation/FI as the parallel structural force.
- **Could new technology make Atruvia obsolete or benefit it?** Mostly benefit (it can adopt AI to cut its own migration/maintenance cost); obsolescence only if AI collapses switching costs faster than Atruvia adapts.
- **Are member banks getting a good deal or an unavoidable one?** Unavoidable, and probably reasonable — but unproven because untested by exit.
- **Central question — is the captive cooperative IT utility model sustainable for another decade, or a slow-motion structural trap?** **Sustainable for another decade, but drifting toward a trap unless three things change:** (1) the sector agrees a durable, adequate investment-funding mechanism (beyond ad-hoc levies); (2) reliability and efficiency close the gap to FI and reduce outage frequency; (3) the sector confronts consolidation and the FI question deliberately rather than by drift. If those flip, the model is not just sustainable but potentially the nucleus of a national banking-IT champion. If they do not, captivity slowly converts from shelter into stagnation.

### Recommendations

**For the cooperative sector / BVR (owners):**
1. **Replace ad-hoc levies with a multi-year, committed investment framework** tied to explicit modernisation benchmarks. Threshold to act: FY2026 margin guidance at ~3.9% and FCF ~€38m confirm the current model cannot self-fund the €450m–€1bn scenario. Change trigger: if the digital-euro levy debate produces another one-off rather than a framework, escalate to a structural funding review.
2. **Commission an independent efficiency benchmark against FI** (revenue/employee ~€218k Group vs ~€516k). If the gap does not narrow by 2028, mandate a structural efficiency programme.
3. **Open exploratory, deniable talks on Atruvia–FI cooperation** (beyond the FH Münster training JV) — start with shared procurement/AI/cyber before any core-platform question. Benchmark: any cloud-native win at a German savings or cooperative bank should trigger acceleration.

**For Atruvia management:**
4. **Treat reliability as the first-order KPI.** Four material outages in six years (2020, 2021, 2023, 2026) is the clearest evidence that lock-in has muted quality discipline. Publish outage root-cause transparency to rebuild trust — the undisclosed Nov 2023 cause contrasts poorly with the clearly-communicated 2021 DDoS response.
5. **Use AI on your own cost base first** — migration automation and COBOL-maintenance reduction — to convert the biggest external threat into an internal advantage before competitors do.
6. **De-risk the new Vorstand** with explicit succession/continuity planning given three sub-18-month tenures and a single spokesman.
7. **Resolve TRUUCO and the low-margin subsidiary estate** — either a value path or an exit.

**For individual member banks:**
8. **Stay — but organise collectively.** Exit is irrational (Apobank), but individual banks should use the BVR/SPSA channels to press for the investment-funding framework and reliability benchmarks, since only collective buyer power exists.

### Caveats
- **Executive compensation, internal board deliberations, and per-category Kununu sub-scores are UNKNOWN** and are labelled as such; no personality speculation is offered.
- The **"Treiber" quote** originates from an Atruvia conference self-presentation (HR Pioneers, 2023), not an audited source — reliable for what Atruvia said, promotional in nature.
- **The Nov 2023 outage root cause and any BaFin reaction were not publicly established;** the explicit "fehlerhaftes Software-Update" cause belongs to the December 2021 event. These are distinct events and should not be conflated.
- Several **Finanz-Szene, Börsen-Zeitung and Platow** items are paywalled and were accessed in snippet/summary form.
- The **VR Payment purchase price is UNKNOWN**; the Bundeskartellamt case (B9-75/26, filed 15 July 2026) is pending.
- The **€450m–€1bn/yr investment figure is a circulating sector scenario (HYPOTHESIS), not a plan.**
- Financial figures blend Atruvia AG and Group; where the Coenen interview (Börsen-Zeitung, 16 July 2026) cites Group FY2025 revenue ~€2.5bn, Jahresüberschuss €60.8m and FY2026 EBIT guidance €77.9m (from €118.2m), these are Group figures and differ from the AG figures in Volume IV.


---

# Part VI — Cross-Volume Synthesis

*This section is new. It exists only in the master edition and draws on all five volumes.*

## VI.1 The category error

Read individually, the five volumes describe something that behaves oddly for a company: a firm whose customers own it, whose profit equals a levy it charges those owners, whose strategy is set by a committee of its buyers, and whose customers are legally incapable of leaving.

Read together, they describe something that is **not a company in the ordinary sense at all.**

**Atruvia is a shared organ of the German cooperative banking sector — legally an Aktiengesellschaft, economically a cost pool, politically a committee.** Every analytical instrument that assumes a normal firm produces a category error when applied to it:

| Read as a company | Actually |
|---|---|
| Operating profit | A levy, collected from owners and retained for investment |
| Customers | Owners and governors, who cannot leave |
| Moat | A structural lock that removes competitive discipline |
| Growth | Mostly consolidation and external wins, not owner pricing power |
| Strategy | Set by BVR committees, not by the Vorstand |
| Margin target | A governance device to legitimise retained earnings |

This is not a criticism. It is the correct frame. A cooperative utility optimised for cost recovery and sector survival should not be judged as if it were maximising shareholder value — but it also should not be credited with strengths that are really just the absence of alternatives.

## VI.2 The single causal model

The five volumes evidence one loop, and the loop is closing.

```
~700 owner-banks — simultaneously customers, owners and governors
        ↓  (BVR committees, Bundeseinheitliches Strategieportfolio,
            Kompetenzteams, Aufsichtsrat)
        set the roadmap AND set the levy that funds it
        ↓
Atruvia builds once for all
(agree21, multi-tenant, IBM Z, four data centres)
        ↓
regulatory and technical scale economics
— MaRisk, BAIT and DORA implemented once for ~700 institutions
        ↓
each member bank remains viable when it could not survive alone
        ↓
BUT the banks consolidate anyway (40–45 mergers/year;
   ~820 institutions in 2022 → ~670 by 2025)
        ↓
fewer, larger owners → greater individual bargaining power
   → greater collective price resistance
        ↓
investment squeeze  ⟲
```

**The loop's defining property: Atruvia's success is dissolving its own customer base.** It exists to keep small cooperative banks independent, and it succeeds — but the same digital and regulatory pressures that make Atruvia necessary are the pressures driving those banks to merge. Every year Atruvia does its job well, it has fewer, larger, more demanding owners to answer to.

## VI.3 What the volumes prove together that none proves alone

**1. The investment engine is politically capped, not economically capped.**

Volume IV establishes that the FY2025 AG operating profit of €89.0m is approximately equal to the ~€90m Digitalisierungsumlage — strip the levy and the underlying operating result is close to zero. Volume II establishes that the levy is set politically, through BVR bodies, not commercially. Volume II also documents that owners resist it: "viele Primärbanker stellen immer lauter die Frage, ob das Geld wirklich gut eingesetzt ist."

Chain these three and the central mechanism appears: **Atruvia can invest exactly as much as ~700 owner-banks will vote to pay, and no more.** Not as much as the market demands, not as much as competitors spend, not as much as the technology requires. The €450m–€1bn annual sector-investment scenario circulating in the Verbund is not a budget — it is an estimate of the gap between what is needed and what the political mechanism will fund.

This is the study's most important finding, and no single volume states it, because it requires the financial fact, the governance fact and the sentiment evidence together.

**2. The lock and the blast radius are the same fact viewed from two sides.**

Volume V establishes, through the Apobank case, that leaving is ruinous: a mid-sized bank spent a "mittleren dreistelligen Millionenbetrag" (third-party estimates around €500m), carried hundreds of significant defects, and watched overall customer satisfaction fall from 82% to 47%. Volume III establishes that a single central software fault takes ~490–520 of ~700 banks offline simultaneously — proven twice, in November 2023 and July 2026.

Together: **member banks are captive to a single point of failure they cannot leave.** The concentration that produces the cost advantage produces the systemic risk, and the lock that guarantees the customer base also removes the exit that would otherwise discipline reliability.

Volume I supplies the regulatory coda: Atruvia was **not** designated a DORA Critical ICT Third-Party Provider on the ESAs' first list of 18 November 2025, though **IBM was**. The Article 31 criteria weight cross-border footprint and EU-wide systemic impact; Atruvia is overwhelmingly domestic. So no supervisor holds direct, continuous oversight of an entity whose failure routinely disables around 500 German banks. Finanz Informatik sits in the same gap. **This is a national systemic-supervision blind spot, and it is structural rather than accidental.**

**3. The most criticised strategic choice is the best-evidenced one.**

Volume III documents the decision to modernise the COBOL/IMS core in place — Java-enablement via the IBM Semeru common runtime, ~1,200 microservices on OpenShift around an unreplaced mainframe core — rather than rip and replace. This looks, from outside, like incumbent conservatism.

Volume V supplies the counterfactual evidence: **both attempts at the alternative failed.** Apobank's migration to Avaloq was a public debacle. The seven Sparda-Banken abandoned a joint Sopra Steria build and migrated *to* Atruvia instead. Meanwhile Atruvia has industrialised the opposite capability — 60 migration weekends, 22 institutions since 2021, all eleven Sparda-Banken, M.M. Warburg incoming.

**Modernise-in-place is not timidity; it is the only approach with a track record at this scale in this market.** The genuine risk is not the choice but the pace.

## VI.4 The central tension

The sector built an institution to keep ~700 small banks alive. That institution now needs those banks to fund a permanent technology race that they are, individually, too small to afford — and the act of funding it accelerates the consolidation that removes them.

Every actor is behaving rationally:
- A small Raiffeisenbank resisting a levy increase is protecting a thin margin.
- Atruvia raising the levy is funding the modernisation the banks demand.
- The BVR mediating between them is doing its job.
- Banks merging to gain scale are responding to the same cost pressure.

And the aggregate outcome is a slow squeeze. **This is the defining structural problem of the German cooperative banking sector's IT, and Atruvia is where it becomes visible.**

## VI.5 What would falsify the reading

Specific, checkable markers — stated so the study can be audited against reality rather than re-narrated:

| If this happens | The reading weakens because |
|---|---|
| The sector agrees a multi-year committed investment framework (not another ad-hoc levy) | The political cap on investment has been lifted |
| Atruvia's Betriebsergebnis holds above ~€50m with the Digitalisierungsumlage removed or capped | The margin is structural after all, not levy-equivalence |
| Revenue per employee moves materially toward Finanz Informatik's ~€516k | The efficiency gap was business-mix, not capability |
| A central-fault outage affecting >300 banks does not recur before ~2029 | The blast-radius risk is being architecturally addressed |
| Atruvia is designated a DORA CTPP at a subsequent annual refresh | The supervisory perimeter gap is closing |
| A cloud-native vendor wins a German cooperative or savings bank at core scale | The modernise-in-place bet is losing |
| Atruvia–Finanz Informatik consolidation talks become public | The sector has chosen structural consolidation over parallel funding |

## VI.6 What Atruvia is becoming

Ranked by probability, on the evidence assembled across all five volumes:

| Hypothesis | Probability | Strongest evidence |
|---|---|---|
| Remains a captive cooperative utility, with adjacency drift | ~35% | Ownership, Apobank deterrent, sovereignty politics |
| Progressively disintermediated at the edges, regulated core intact | ~25% | BaaS/fintech module erosion; neobank pressure on member banks |
| Payments and card processor of national significance | ~15% | VR Payment Issuing-Processing from 1 January 2027 |
| Merges or deeply consolidates with Finanz Informatik | ~12% and rising | Identical structures; joint FH Münster training venture; sector cost logic |
| Restructured by the sector after an investment or governance crisis | ~10% | The funding gap; thin free cash flow (~€38m FY2025) |
| Becomes a genuinely commercial open-market vendor | ~3% | Rhetoric only; no open-market core wins |

**Synthesis:** a captive utility drifting toward commercial adjacencies, with sector consolidation — either with Finanz Informatik or through crisis-driven restructuring — as the most consequential live option.

## VI.7 Implications for a fintech builder

*This section applies the study to the reader's own context rather than to Atruvia. Analytical inference throughout.*

**This is what "the incumbent" actually looks like — and it explains your integration timelines.** When a German bank partner takes nine months to expose an API, the reason is usually visible in Volume III: the change must traverse a multi-tenant platform serving hundreds of institutions, pass a MaRisk AT 8.2 change assessment at each one, and land in a release train coordinated across the Verbund. This is not incompetence; it is the arithmetic of building once for 700 banks. Budget integration time against that reality, not against a startup's release cadence.

**Attack the edges, never the core.** Volume V's competitive analysis is unambiguous: no cloud-native vendor has won a German cooperative or savings bank at core-system scale, and the two serious attempts at leaving (Apobank, Sparda/Sopra) failed expensively. But the edges — digital channels, BaaS modules, corporate banking tooling, analytics — are where Atruvia itself identifies erosion risk. That is where a fintech competes with an incumbent utility, and where a partnership is more plausible than displacement.

**The build-once regulatory asymmetry is the harshest number in the study for a startup.** Atruvia implements MaRisk, BAIT and DORA once and amortises it across ~700 institutions and ~97m accounts. You implement the equivalent once, for yourself. That asymmetry is why compliance cost per customer is brutal at small scale and why it improves faster than almost any other line as you grow. Model it as a fixed cost with a very long amortisation runway, not as a variable one.

**DORA Article 31 is worth reading properly if you ever become critical to EU financial entities.** The designation criteria weight cross-border footprint and EU-wide systemic impact heavily. Atruvia — systemically critical to German banking but domestic-only — escaped designation while IBM did not. The practical lesson runs both ways: cross-border scale attracts direct ESA oversight, and single-market concentration can leave a genuine supervisory gap. Know which side of that line your architecture puts you on before regulators decide for you.

**On core systems, the evidence favours in-place modernisation over replacement.** Two well-funded attempts at rip-and-replace failed in this market within five years. If you ever inherit or acquire a core — through an acquisition, a licence deal, or a sponsor-bank arrangement — the Apobank case is the best-documented cautionary evidence available in German banking, and it is worth reading before anyone in the room says "we'll just migrate."

**Finally, a governance lesson that transfers beyond banking.** Atruvia demonstrates what happens when customers, owners and governors are the same people: pricing loses its signal, accountability blurs across three roles, and investment becomes a political negotiation rather than a commercial decision. If you ever structure a shared entity with your own customers — a consortium, a joint venture, a mutualised utility — this study is the cautionary case for separating those three roles explicitly.

## VI.8 Ten cross-volume conclusions

1. Atruvia is a shared organ of the cooperative sector, not a company — reading it as a firm produces category errors at every turn.
2. The reported operating profit is the digitalisation levy; strip the levy and the underlying result is near zero.
3. Investment is politically capped by owner willingness to pay, not economically capped by opportunity.
4. Atruvia's success dissolves its own customer base: it keeps small banks alive while the pressures it addresses drive them to merge.
5. The lock (Apobank-proven) and the blast radius (~490–520 banks per central fault) are the same concentration viewed from two sides.
6. Atruvia is a national systemic node outside direct DORA oversight while its supplier IBM is inside — a structural supervisory gap shared with Finanz Informatik.
7. Modernise-in-place is the best-evidenced strategic choice in the study, validated by the failure of both alternatives; the risk is pace, not direction.
8. The genuine, exit-independent advantages are industrialised migration capability and accumulated regulatory capability — everything else labelled "moat" is lock.
9. Finanz Informatik is materially more efficient per employee, and the gap is only partly explained by business mix.
10. The most consequential live option is sector consolidation — with Finanz Informatik, or through a crisis-driven restructuring.

---

# Appendix A — Glossary of German Terms

*Load-bearing. Read before Part IV.*

## Accounting and financial

| Term | Meaning |
|---|---|
| **Gesamtleistung** | Total output. Umsatzerlöse + aktivierte Eigenleistungen + inventory change. **Not revenue** — margins on this base differ from margins on revenue |
| **Umsatzerlöse** | Revenue proper (sales) |
| **Aktivierte Eigenleistungen** | Capitalised own work — internally developed software capitalised rather than expensed |
| **Betriebsergebnis** | Operating result (≈ EBIT, but on an HGB basis) |
| **Jahresüberschuss** | Net income for the year |
| **Materialaufwand** | Cost of materials and bought-in services — for Atruvia, largely IBM licensing and external/nearshore capacity |
| **Personalaufwand** | Personnel expense |
| **Abschreibungen** | Depreciation and amortisation |
| **Rückstellungen** | Provisions (notably Pensionsrückstellungen — pension provisions) |
| **Eigenkapitalquote** | Equity ratio |
| **Investitionsquote** | Capex as a share of output |
| **Zielrendite** | Target return (Atruvia's stated 4% of revenue) |
| **HGB** | Handelsgesetzbuch — the German Commercial Code; the accounting basis, not IFRS |
| **Kapitalerhöhung** | Capital increase (share issuance) |

## Pricing and charging

| Term | Meaning |
|---|---|
| **Umlage** | A levy or apportionment — a charge allocated across members. Central to Atruvia's economics |
| **IT-Sonderumlage** | The special IT levy, ~€60m/year from member banks 2018–2023 |
| **Digitalisierungsumlage** | The digitalisation levy, €30m → €60m → €90m (2023–2025) |
| **Leistungsentgelte** | Service fees — the base charges for services rendered |
| **Basispaket** | The base package of core services |
| **Nutzenbasierte Bepreisung** | Usage- or benefit-based pricing — the shift announced in 2025 |

## Corporate and governance

| Term | Meaning |
|---|---|
| **Vorstand** | Management board (executive) |
| **Aufsichtsrat** | Supervisory board (non-executive oversight) — German two-tier structure |
| **Hauptversammlung (HV)** | General meeting of shareholders |
| **Mitbestimmung / MitbestG 1976** | Co-determination — employees hold half the supervisory board seats above 2,000 employees |
| **Betriebsrat** | Works council |
| **Beteiligungs-KG** | Participation limited partnership — the vehicles through which member banks hold Atruvia |
| **Handelsregister / HRB** | Commercial register / register number |
| **Bundesanzeiger** | Federal Gazette — where German company accounts are filed publicly |
| **Arbeitsdirektor** | Labour director — a board member with mandatory HR responsibility under co-determination law |

## Sector and institutional

| Term | Meaning |
|---|---|
| **Genossenschaftliche FinanzGruppe (GFG)** | The cooperative financial network — the whole sector |
| **Verbund** | The network/alliance of cooperative institutions |
| **Primärbank** | A primary (local) cooperative bank — a Volksbank or Raiffeisenbank |
| **BVR** | Bundesverband der Deutschen Volksbanken und Raiffeisenbanken — the sector association that sets strategy |
| **DZ Bank** | The central institution of the cooperative sector (clearing, capital markets) — **not a material shareholder of Atruvia** |
| **Bundeseinheitliches Strategieportfolio (BSP)** | The sector-wide strategy portfolio that prioritises initiatives |

## Technology and operations

| Term | Meaning |
|---|---|
| **Kernbankverfahren / Kernbanksystem** | Core banking system — Atruvia's is agree21 |
| **Bankverfahren** | The core banking service line (revenue category) |
| **Bankarbeitsplatz (BAP)** | Bank workstation — the staff-facing application, being replaced by BankingWorkspace |
| **Omnikanalplattform** | Omnichannel platform |
| **Serienmigration** | Series migration — industrialised, tranche-based rollout across many banks |
| **"Mondlandung"** | "Moon landing" — the internal name for the agree21 consolidation migration |
| **Krisenstab** | Crisis team — convened for major incidents |
| **Störung** | Disruption or outage |
| **Rechenzentrum** | Data centre |

## Regulatory

| Term | Meaning |
|---|---|
| **BaFin** | Bundesanstalt für Finanzdienstleistungsaufsicht — the federal financial supervisor |
| **§25b KWG** | The Banking Act provision on outsourcing — regulatory responsibility stays with the outsourcing bank |
| **MaRisk** | Minimum Requirements for Risk Management — including AT 9 on outsourcing and AT 8.2 on changes |
| **BAIT** | Bankaufsichtliche Anforderungen an die IT — supervisory requirements for bank IT |
| **Auslagerung / Auslagerungsregister** | Outsourcing / the register of outsourced functions each bank must maintain |
| **KRITIS** | Critical infrastructure designation under the BSI framework |
| **DORA** | Digital Operational Resilience Act (EU) — including the Critical ICT Third-Party Provider (CTPP) designation regime |
| **Feststellungen** | Findings (from a supervisory inspection) |

---

# Appendix B — Canonical Figures Register

**Where any volume disagrees with this table, this table governs.** Every figure carries its perimeter (AG or Group) and its date. As of 8 August 2026.

## Scale

| Figure | Canonical value | Perimeter / date |
|---|---|---|
| Accounts administered | **97 million** | Group, 2025 (rising series: 85m 2022 → 89m 2023 → 91m 2024 → 97m 2025) |
| Bookings / business transactions | **~10 billion/year** | Group, 2025 (8.2bn 2022 → 8.7bn 2023 → 9.32bn 2024) |
| Technical transactions | **~80bn+/year** | IBM measurement, 2022 baseline — a *different layer* from bookings |
| Customers (institutions) | **~917–950** | Group, 2024–25 (includes private banks and non-banks) |
| Cooperative banks served | **~670–700** | 2025 (falling: ~820 in 2022) |
| Banking workstations | **~153,000–169,000** | Range reflects different years and definitions |
| ATMs / self-service terminals | **~30,000–34,000** | Range reflects different years |
| Data centres | **Four** | Two each in Karlsruhe and Münster (the "six" claim is unsupported) |

## Financials

| Figure | Canonical value | Perimeter / year |
|---|---|---|
| Gesamtleistung | **€1,921.0m** | **AG**, 2025 |
| Umsatzerlöse | €1,894.4m | **AG**, 2025 |
| Revenue | ~€2.5bn | **Group**, 2025 |
| Betriebsergebnis | **€89.0m (4.6–4.7% margin)** | **AG**, 2025 |
| Jahresüberschuss | €60.5m | **AG**, 2025 |
| Digitalisierungsumlage | ~€90m | 2025 (€30m 2023, €60m 2024) |
| Capex (Investitionen) | €359.1m (18.7% Investitionsquote) | **AG**, 2025 |
| Operating cash flow | €397.2m | **AG**, 2025 |
| Free cash flow | ~€38m | **AG**, 2025 (derived: operating less capex) |
| Eigenkapital | €557.0m (EK-quote 38.2%) | **AG**, 2025 |
| Grundkapital | €115.8m | Fixed since the 2015 merger |
| Employees | **5,847 (AG)** / **10,076 (Group)** | AG 2025 / Group 2024 |
| FY2026 guidance | Margin falling to ~3.9% | AG |

## Ownership and structure

| Figure | Canonical value |
|---|---|
| Cooperative ownership | 99.68% |
| Via three regional Beteiligungs-KGs (pooled through VR-FGI) | 91.63% |
| **DZ Bank direct stake** | **~0.35%** — the "~20%" claim is **erroneous** and refers to Verimi |
| Bavarian KG (BBA) indirect stake | 14.15% |
| Registered entity | Atruvia AG, HRB 102381, Amtsgericht Frankfurt am Main |
| Aufsichtsrat | 20 seats, 10 shareholder / 10 employee (MitbestG 1976), chaired by Daniel Keller |
| Auditor | BDO AG Wirtschaftsprüfungsgesellschaft, Hamburg |

## Technology and regulatory

| Figure | Canonical value |
|---|---|
| Mainframe estate | Eight IBM z15 hosting twelve IMS systems (2022 baseline); **z17** under the deal signed 19 November 2025 |
| Peak throughput | ~12,000 transactions/second |
| Java-enabled core transactions | ~85% (via IBM Semeru common runtime) |
| Java microservices | ~1,200 on Red Hat OpenShift |
| DORA CTPP status | **Not designated** (18 November 2025 first list); **IBM was designated**, Lead Overseer EBA |
| BaFin §44 inspections | May–August 2018 (15 findings, 3 severe) and from November 2023 |
| Bank merger migrations | 40–45 per year |

## Benchmark — Finanz Informatik

| Figure | FI | Atruvia |
|---|---|---|
| Revenue | ~€2.6bn (2024) | ~€2.2bn Group (2024) |
| Employees | 5,037 FTE | 10,076 Group / 5,847 AG |
| Accounts | ~114m | 91–97m |
| Technical transactions | >205bn | ~80bn+ |
| Revenue per employee | ~€516k | ~€218k Group / ~€324k AG |
| Core platform | OSPlus | agree21 |
| DORA CTPP | Not designated | Not designated |

---

# Appendix C — Reconciliation of Cross-Volume Discrepancies

The volumes were written sequentially against a moving evidence base, and Atruvia's figures conflict more than most companies' — overwhelmingly for legitimate reasons (different perimeters, different dates, different measurement layers) rather than error. These are resolved here rather than silently smoothed.

## Perimeter and measurement differences (not errors)

| # | Item | Appears as | Resolution |
|---|---|---|---|
| 1 | **Revenue** | AG €1,921.0m Gesamtleistung / AG €1,894.4m Umsatzerlöse / "knapp €1.9bn" / Group ~€2.2bn / Group ~€2.5bn / €2.001bn | **All correct at their perimeter and year.** €2.001bn is the FY2023 *Group* figure; ~€2.2bn is FY2024 Group; ~€2.5bn is FY2025 Group; the €1.9bn figures are AG. Never splice. |
| 2 | **Employees** | 5,263 / 5,483 / 5,847 / 9,291 / 10,076 | AG series (5,263 in 2023 → 5,847 in 2025) versus Group series (9,291 in 2022 → 10,076 in 2024). Both rising. |
| 3 | **Accounts** | 82m / 85m / 89m / 91m / 97m | A **rising series**, not a conflict. 97m is current (2025). The 82m figure is an older third-party citation. |
| 4 | **Cooperative banks** | ~646 / ~670 / "gut 700" / ~730 / ~820 / ~917 customers / >1,000 institutions | Different **populations and dates**. 646 is the BVR's count of cooperative banks at end-2025; ~820 was 2022; ~917 "customers" includes private banks and non-banks; ">1,000 financial institutions" counts the whole group's client base. |
| 5 | **Transactions** | 9.32bn / ~10bn bookings versus 80bn / 87bn / 100bn / 120bn technical | **Different layers.** Bookings are customer-visible business events; IBM's figure counts IMS technical transactions, roughly 8–13 per booking. The IBM number rises across years with digital-channel growth. Non-comparable, not contradictory. |
| 6 | **Serviscope revenue** | €28.8m versus Gesamtleistung ~€44.0m | Revenue versus Gesamtleistung — the HGB distinction again. |
| 7 | **Betriebsergebnis 2025** | AG €89.0m versus Group €118.2m falling to €77.9m guidance | AG versus Group. The Coenen interview figures are Group. |
| 8 | **Finanz Informatik employees** | 5,037 versus ~6,500 | 5,037 is FTE for the FI legal entity (Jahresbericht 2024); ~6,500 is a broader group basis. |
| 9 | **FI technical transactions** | >205bn versus ~172bn | >205bn is the current (end-2024) figure; ~172bn is an older career-site number. |

## Genuine errors and corrections

| # | Item | Status |
|---|---|---|
| 10 | **"DZ Bank owns ~20% of Atruvia"** | **FALSE.** DZ Bank holds ~0.35% directly. The ~20% figure belongs to **Verimi**. This error circulates widely (including on the-playbook.de) and should be expected in further sources. DZ Bank is a *funder* — it contributed €180m to the IT-Sonderumlage and provides the Karlsruhe campus loan — not an owner. |
| 11 | **"Six data centres"** | **Unsupported.** Atruvia's own statement is "jeweils zwei Rechenzentren in Karlsruhe und Münster" — **four**, corroborated by IBM. The "six" claim (Grokipedia) has no primary basis. |
| 12 | **"Founded in 1924 by Martin Beyer"** | **FALSE** (Tracxn/PitchBook). Fiducia was founded 13 November 1924; Martin Beyer was an executive 2013–2025. |
| 13 | **audIT "completed 31 December 2021"** | **Imprecise.** Material remediation points were reached by end-2021, but Berechtigungsmanagement work extended beyond, with Verbund timelines cited toward 2023. Volume III corrected this. |
| 14 | **Outage causes conflated** | The **November 2023** outage root cause was **not publicly disclosed**. The "fehlerhaftes Software-Update" attribution belongs to a **December 2021** event. Distinct incidents — do not merge. Volume V flagged this. |
| 15 | **"neues Betriebsmodell"** | **Two different things.** The internal agile reorganisation (Spotify-model tribes/squads) dates from ~2020–21. The "neues Betriebsmodell" introduced from 2025 is a **product and process programme for the member banks**, targeting a €2.6bn gross earnings effect by 2035. Volume V corrected Volume III's implication. |
| 16 | **parcIT series** | **Discontinuous.** 403 employees/€68.9m (GB2022) → 478/€69.8m (GB2023) → 507/€78.6m (FY2024) reflects a perimeter or consolidation change, not organic growth. Do not read as a trend. |
| 17 | **Mainframe generation** | z15 is the 2022 IBM case-study baseline; **z17** is committed under the November 2025 deal. A z16 interim is likely but **undocumented — UNKNOWN**. |

## Known unknowns carried forward

- VR Payment Issuing-Processing purchase price (Bundeskartellamt case B9-75/26, filed 15 July 2026).
- Executive compensation (unlisted AG — no individual disclosure).
- Per-bank, per-account and per-workstation price levels; only percentage changes are public.
- Contractual SLAs, service credits and liability caps for outages.
- agree21 internal data model and tenant-separation mechanism.
- Reconciliation architecture internals.
- Published availability SLOs, RTO/RPO.
- Group FY2025 full P&L and balance sheet (behind paywall).
- IBM z17 total contract value and lease-versus-purchase split.
- Whether any cooperative bank other than Apobank has attempted exit.
- ISO 27001 / IDW PS 951 / ISAE 3402 certification scopes and KRITIS registration status.

---

# Appendix D — Source Hierarchy & Evidence Conventions

Sources were prioritised in the following order, with primary evidence preferred wherever it existed:

1. **Bundesanzeiger** filings — Atruvia AG Jahresabschlüsse and Konzernabschlüsse, and those of the subsidiaries. German filing law makes these public, giving this study a materially better evidence base than a private company in most jurisdictions would afford.
2. **Atruvia's own Geschäftsberichte** (published as microsites gb2021–gb2025 with Finanzteil PDFs), press releases, Hauptversammlung coverage and technology pages.
3. **Handelsregister filings** via the Unternehmensregister and Northdata (HRB 102381, Amtsgericht Frankfurt am Main).
4. **IBM case studies and press releases** — the richest technical source on the mainframe estate, IMS/Db2, Java-on-Z and the z17 agreement.
5. **BaFin, Bundesbank, BSI and the ESAs** — outsourcing guidance, BAIT, MaRisk, and the DORA CTPP designation lists.
6. **BVR and Genossenschaftliche FinanzGruppe** publications.
7. **German specialist press** — Finanz-Szene, Börsen-Zeitung, DER PLATOW Brief, IT-Finanzmagazin, Handelsblatt, Der Bank Blog, Bankinformation, Computerwoche, heise online, and Verband magazines.
8. **Atruvia job advertisements** — an unusually productive window into the internal stack, naming concrete systems, frameworks and organisational units.
9. **Finanz Informatik** Jahresbericht and press releases for benchmarking.
10. Employee review platforms (Kununu, Glassdoor), used cautiously, labelled, with sample sizes where available.

SEO-oriented aggregators were not relied on where primary evidence existed; where such sources were the only ones available (notably for outage timing and breadth), this is flagged in text. For strategically significant claims, sources were triangulated. Where reputable sources disagreed, the disagreement is identified, dates and perimeters compared, and uncertainty preserved rather than resolved by false precision.

**A note on the prohibition against invented architecture.** Volume III in particular was written under an absolute rule: where Atruvia has published nothing about an internal mechanism, the report says UNKNOWN rather than describing plausible-sounding but unevidenced internals. Several sections are consequently shorter than their headings might suggest. That is deliberate.

---

*End of the Atruvia Enterprise Reverse-Engineering Study.*
