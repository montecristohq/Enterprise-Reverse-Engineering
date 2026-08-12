# ATRUVIA AG — Forensic Reverse-Engineering Study
# VOLUME II: Product, Customer & Service-Delivery Architecture

## Preface and Method

Volume I established Atruvia AG's corporate, legal, regulatory and institutional anatomy. Volume II reconstructs what Atruvia actually sells, to whom, why they buy (or are structurally obliged to buy), and precisely what happens operationally, contractually and economically when a member bank — and that bank's end customer — uses an Atruvia system.

A structural framing note governs the whole volume. Atruvia holds no customer money and moves none as principal. It operates the systems through which the member banks move their customers' money. There is therefore no take rate and no safeguarding architecture to analyse; pricing is cost allocation (Umlage/Leistungsentgelte) to owner-members, now transitioning toward usage-based charging. This volume has been re-cut accordingly, replacing money-movement sections with the two-tier customer structure (II.2), the service-delivery flow (II.5) and the cost-allocation architecture (II.8).

**Evidence labels used throughout:** CONFIRMED FACT / COMPANY CLAIM / THIRD-PARTY ESTIMATE / ANALYTICAL INFERENCE / HYPOTHESIS / UNKNOWN.

**A note on disclosure quality (read before the pricing sections):** Atruvia is an unlisted, cooperative-owned AG with no investor relations, no analyst coverage and no product-level revenue reporting. Per-unit prices (cost per account, per workstation, per transaction) and per-bank Atruvia cost lines are **not public**. Where this volume reaches the limit of disclosure it says so and labels the specifics UNKNOWN rather than manufacturing precision.

---

## II.0 Reconciling the Scale Numbers (a prerequisite)

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

## II.1 Product and Service Universe

Atruvia's portfolio is a stack: a mainframe core (agree21) at the bottom; a workstation/omnichannel middle layer; end-customer channels on top; steering/analytics/AI alongside; and a ring of subsidiaries selling adjacent products into the same base. The **Follow-the-Legal-Entity rule** is applied: each product is mapped to its delivering entity.

### The core and platform layer (Atruvia AG)

**agree21 — the Kernbankverfahren (core banking process).** CONFIRMED FACT. The integrated Gesamtbanklösung: account management, payments, lending, securities, plus the steering and channel modules that attach to it. It runs on IBM Z (IMS transaction manager, Db2 database) across four data centres. Named module families: **agree21Finanzen** (steering platform — Accounting, Meldewesen, Controlling on a single data basis), **agree21BAP** (legacy Bankarbeitsplatz), **agree21ECON** (digital end-to-end process modelling for non-standard products), **agree21SecureDocs** (secure data rooms, built on partner DRACOON, superseding agree21Doksharing), **agree21SmartData** (affinity/propensity models), **agree21M365** (managed Microsoft 365). Classification: **core-mandatory**. Historical discipline: agree21 superseded both predecessor cores — "agree" (ex-Fiducia, south) and "bank21" (ex-GAD, north); bank21 is **retired**, agree v1 is **superseded**. Consolidation migration finished 2019–2020 (Volume I).

**BankingWorkspace (BWS) / Bankarbeitsplatz.** CONFIRMED FACT. The new browser-based, role-adaptive employee workspace replacing the closed, inflexible agree21BAP. Vorstandssprecher Ulrich Coenen (Profil, 01/2024): "Der bisherige Bankarbeitsplatz war ein in sich geschlossenes, wenig flexibles System. Der BankingWorkspace hingegen wird … zu einer hochflexiblen, browserbasierten Anwenderoberfläche weiterentwickelt." Coenen confirms a **coexistence phase**: "Die Koexistenzphase von BankingWorkspace und Bankarbeitsplatz wird noch etwas andauern … der aktuelle Zustand ist etwas zäh," with some applications (e.g. CRM) currently maintained twice. Piloting began after successful technical tests in Q4 2022. Classification: **core-mandatory (in transition)**.

**Omnikanalplattform.** CONFIRMED FACT. The multi-tenant (mandantenfähig) platform onto which bank processes are being ported from the core; Atruvia calls it "einer der modernsten und mandantenfähigen Banking-Plattformen in Europa." The BWS is merely "der Zugangsweg der Bankmitarbeitenden zu diesen Prozessen" — the platform is the substance, the workspace the door. ~300 processes from the process map are already available. Vorstand Daniela Bücker's confirmed position (Volume I): the platform/EGP was never limited to agree21, suits integration into arbitrary banking systems, is not restricted to cooperative banks, and porting bank processes from core to platform "will take several more years." Classification: **strategic core**.

### End-customer channels (Atruvia AG)

**OnlineBanking and VR-NetKey.** CONFIRMED FACT. The new OnlineBanking replaced the legacy Fiducia/GAD online environments; private customers migrated through H1 2022. VR-NetKey is the access credential. Classification: **core-mandatory**.

**VR Banking App.** CONFIRMED FACT. The mobile flagship, rebuilt from the ground up, launched "leise" (without a marketing campaign) alongside VR SecureGo plus, developed agile as an MVP and iterated with the banks. It bundles account management, digital cards, Wero, photo-transfer, multibanking, securities/Union-Depot views, and an AI voice assistant. Classification: **core-mandatory + strategic** (the primary digital customer interface). Adoption/competitive data in II.4/II.7.

**VR SecureGo plus.** CONFIRMED FACT. The authentication/authorisation app (push approval, biometrics, up to three devices), separate from the banking app — required to release OnlineBanking, VR Banking App and card transactions, and to activate Wero. Classification: **core-mandatory** (security substrate).

**Wero and the digital card.** CONFIRMED FACT. Wero (the EPI wallet) is integrated into the VR Banking App; transactions execute in real time directly from the Girokonto (account-to-account, no IBAN), with online-payment capability added and card-funding planned. Digital debit/credit cards live in the app for contactless payment. Johannes Stoll leads the "Daily Banking" business field (Volume I). Classification: **defensive + strategic optionality** (a collective answer to PayPal/Apple Pay and to neobank P2P).

### Corporate/business-client software (Atruvia AG) — current vs legacy (Priority verify)

CONFIRMED FACT. Three products, tiered by client size, all maintained by Atruvia and licensed through the customer's own bank:
1. **VR-NetWorld Software** — freelancers, small businesses, associations (current; v8.x, but version 8 "erhält seit 2024 keine Funktions-Updates mehr").
2. **Profi cash** — the SME payments workhorse (current; v13 / v12.99 series 2025–2026; migrates VR-NetWorld data).
3. **GENO cash** — medium/large corporates (current; v4.00.008 SP14 in 2025; already supports instant single orders).

These are Windows desktop/server FinTS/EBICS clients. Economically **optional add-ons** (bank buys licences, resells to corporate customers) but strategically important as SME/Firmenkunden anchors. The **Serviceline** (II.5.E) supports GENO cash, Profi cash, VR-NetWorld Software and BankingManager.

**FinTS/PSD2 interfaces.** CONFIRMED FACT. Atruvia operates the FinTS/HBCI servers (fints1.atruvia.de, fints2.atruvia.de, port 3000) through which both its own corporate software and third-party aggregators (windata, konfipay, ALF-BanCo, GLS eBank, subsembly) access accounts — the PSD2 access layer. Classification: **core-mandatory infrastructure** (regulatorily obligatory).

### Payments and cards

**Payment processing (SEPA, SCT Inst, girocard).** CONFIRMED FACT with a key legal-entity boundary. Atruvia builds and operates the systems in the banks' core through which payments are initiated and posted, but **DZ Bank is the clearing house** ("Clearingstelle für die Abwicklung aller Zahlungen von Volks- und Raiffeisenbanken, die nicht innerhalb einer Bank stattfinden," Handelsblatt). DZ Bank built a new payments platform — jointly owned with Fiducia GAD/Atruvia per Handelsblatt — to carry instant, classic SEPA and cross-border payments. See II.6.

**Card issuing and processing.** CONFIRMED FACT and in transition. Today debit (girocard/Debit) issuing processing sits partly with Atruvia; credit-card processing sits with **VR Payment** (a DZ Bank subsidiary). From **1 January 2027**, under the reorganisation agreed 2 July 2026 (Bundeskartellamt case **B9-75/26, notified 15 July 2026**, product markets "Finanzdienstleistungen, Zahlungsabwicklungsdienste"), Atruvia takes over the **Issuing Processing** division from VR Payment and adds **credit-card processing**, building "eine integrierte, zukunftsfähige Kartenplattform mit einheitlicher Abwicklung von Girokarten, Debitkarten und Kreditkarten auf einer Plattform" (Atruvia PR, 2 July 2026). VR Payment refocuses on Acquiring, POS-Netzbetrieb and merchant/omnichannel payment. **Dr. Christian Marzlin, co-lead partner at legal adviser McDermott Will & Schulte:** "A significant portion of all credit card transactions in Germany is processed through Atruvia's systems. The restructuring of the card business between Atruvia and DZ BANK is therefore of great importance to the German financial and banking sectors." Finanz-Szene (15 May 2026) frames this as VR Payment being "zerschlagen" and Atruvia becoming the "Karten-Powerhouse" (internal project name "Dragon"). Classification: **strategic** — see II.9.

### Steering, analytics and AI

**EGP Gesamtbanksteuerung / agree21Finanzen.** CONFIRMED FACT. The whole-bank steering platform (accounting, regulatory reporting, controlling on one data basis). Bücker: EGP integration is not restricted to agree21 or to cooperative banks. Classification: **core-mandatory** inside GFG; **externally sellable**.

**parcIT: VR-Control and okular.** CONFIRMED FACT. Delivered by subsidiary **parcIT GmbH** (403 employees / €68.9m revenue in the 2022 GB; 478 / €69.8m in the 2023 GB — a growing unit). VR-Control/okular is the risk and steering software family covering customer business, address/market/liquidity risk, whole-bank steering and capital planning, operational risk, plus modules for risk-bearing-capacity (Risikotragfähigkeit), cost management, IFRS accounting and regulatory reporting. "okular-Tools" are bridging/supplementary solutions (RWA optimisation, LSI stress-test templates, IRIS/BETRIS real-estate and participation-risk calculators). LSI stress-test tools are **free for GFG institutions**; external banks pay via a Basis-Abo. Classification: **core-mandatory (steering)** inside GFG; **competitive/externally-sold** outside.

**genoGPT and the AI portfolio.** CONFIRMED FACT. AI has been used at Atruvia since 2017 (fraud detection). A dedicated unit of >70 staff builds process automation (document recognition, photo-transfer), natural-language systems and generative-AI bots. Products: **plainGPT** (a regulatorily safe ChatGPT-based text/image/research tool for bank staff — "eine der steilsten Adoptionskurven"), and its successor **genoGPT** (a "KI-basierte Wissens-, Agenten- und Informationsplattform" that ingests bank-internal documents; runs in a private cloud with no open-internet connection). A customer-facing website chatbot is also offered. A GFG-wide **KI-Kompetenzcenter** was established, with a KI-Strategie permitting decentralised use under central governance aligned to the EU AI Act. Classification: **strategic optionality** (small today, high potential).

**TRUUCO.** CONFIRMED FACT. TRUUCO GmbH (started April 2023) owns the Smart-Data models and the Impulsmanager (incl. Next Best Action), developing data-driven sales with the banks and GFG partners. Classification: **strategic (analytics)**.

### Self-service / ATM estate

CONFIRMED FACT. Atruvia operates ~30,000–34,000 ATMs and self-service terminals ensuring cash supply. During the 9 Nov 2020 outage and the DDoS attacks, terminals were noted as sometimes the only functioning channel ("Versorgung mit Bargeld weiterhin möglich"). Hardware/rollout is tied to subsidiary **Ratiodata**. Classification: **core-mandatory (physical channel)**.

### The subsidiary ring (Follow-the-Legal-Entity)

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

## II.2 The Two-Tier Customer Structure (given unusual weight)

This is the analytical heart of Volume II. Atruvia serves two populations different in kind:

**Tier 1 — the member banks (~670–730 cooperative banks plus ~190 private banks and specials).** They are simultaneously (a) **owners** (99.68% cooperative-held, 91.63% via the three regional Beteiligungs-KGs), (b) **buyers** (they pay the Umlage/Leistungsentgelte), and (c) **governors** (they populate the Aufsichtsrat and the BVR committees that steer the roadmap). This triple identity is the single most important fact about Atruvia's customer structure.

**Tier 2 — the banks' end customers (tens of millions of German retail and corporate users).** They use Atruvia-built interfaces daily, overwhelmingly **without knowing Atruvia exists**. Their contractual and data relationship is with their local bank, not with Atruvia.

### Who Atruvia designs for when the two conflict

**ANALYTICAL INFERENCE (high confidence):** Atruvia routes requirements almost entirely through Tier 1. The roadmap is set with the banks and the BVR (below), not with end users; end-user needs enter only as mediated by the banks and Atruvia's own UX research. The tell is Kaurin's own framing (II.4/II.7): the competitive battle has shifted "von Features zu persönlicher Relevanz" — an admission that feature parity was built *for the banks' checklist* and that the harder problem (individual end-user relevance) is the current frontier. The structural bias is toward the owner-buyer-governor, not the invisible end user.

### Who sets requirements and through which governance route (Priority Gap 6 — bodies by name)

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

### Who owns the end-customer relationship and data

CONFIRMED FACT (mechanism). The end customer's contract is with the local bank. Under GDPR the **bank is the controller (Verantwortlicher)** and **Atruvia is the processor (Auftragsverarbeiter)** under an Auftragsverarbeitungsvertrag (II.5.B). The Serviceline is "reachable only via the customer's own bank's phone number," deliberately keeping Atruvia invisible and the bank as the face. The end-customer *data* is the bank's; Atruvia processes it on instruction. The "customer-is-also-owner" distortion therefore operates entirely at Tier 1.

### How the customer-is-also-owner identity distorts prioritisation

**ANALYTICAL INFERENCE (high confidence, evidence-backed):**
1. **Consensus over speed.** Because ~700 owner-buyers must be broadly satisfied, standardisation is negotiated ("Standardisierung … keinesfalls als 'kleinsten gemeinsamen Nenner'," Schlächter — a defensive phrasing that concedes the risk exists). Coenen concedes the transition is "etwas zäh."
2. **Underpricing pressure vs investment need.** Owners resist price rises on themselves (II.8) yet demand competitive digital features; the result is chronic under-investment relative to neobanks (Platow: competitors "geben oft ein Vielfaches").
3. **Uniformity over differentiation.** A single multi-tenant platform serves all; individual banks get limited white-labelling (II.7), which suits small banks but frustrates large ones.
4. **The owner's P&L is the customer's cost.** Every euro Atruvia earns is a cost line for its owners, so there is structural pressure to keep margin thin (2022: €8m surplus on €1.4bn) — which starves reinvestment, the exact tension resolved by the 2025 shift to a 4%-of-revenue Zielrendite (II.8).

---

## II.3 Customer Segmentation

### By institution type

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

### By legacy platform (does the north/south divide persist?)

CONFIRMED FACT: the ex-Fiducia (south, "agree") and ex-GAD (north, "bank21") divide has been **eliminated at the core** — all migrated to agree21 by 2019–2020. ANALYTICAL INFERENCE: residual organisational traces persist (two administrative seats, Karlsruhe and Münster), but there is no longer a platform, pricing or service divide by legacy — the single platform is precisely what enables sector-wide rollout (II.9).

### By size

**ANALYTICAL INFERENCE:** the base ranges from a handful of very large Volksbanken (e.g. Frankfurter Volksbank Rhein/Main, Berliner Volksbank — multi-billion balance sheets) to hundreds of small rural Raiffeisenbanken. Roadmap influence correlates with size and Kompetenzteam participation. Large banks are the most likely to chafe at limited white-labelling and to be "nicht alle … zufrieden" with the digital offering (Platow). Small banks are the biggest beneficiaries of scale economics — they could never build MaRisk/BAIT/DORA-compliant IT alone. Price sensitivity is high across the board because IT is a cost line for owner-members.

### By product-adoption depth

ANALYTICAL INFERENCE: adoption depth is the real revenue lever now that the base is saturated. Atruvia is explicitly "die Wertschöpfung vertiefen" — deepening value-add at banks that "ohnehin alle das Core-Banking der Atruvia verwenden" (Finanz-Szene). Depth tiers: (1) core + channels only; (2) + steering (VR-Control) + M365; (3) + BPO (Serviscope/Peras) + analytics (TRUUCO) + AI (genoGPT). The usage-based pricing shift (II.8) is designed to monetise depth.

### The consolidation trend and its consequences

CONFIRMED FACT. Bank mergers requiring technical migration: **42 (2021), 40 (2022), 40–45 registered for 2023**. The cooperative-bank count has fallen from "rund 820" (2022 GB) to "gut 700" / "rund 670" (2025). **Consequence (ANALYTICAL INFERENCE):** the captive base is shrinking in *institution count* but not in *accounts/volume* (accounts rose 89m→91m→97m), because mergers consolidate rather than remove customers. For Atruvia this means (a) fewer, larger, more demanding buyers with more governance weight; (b) recurring migration revenue from consolidations; and (c) growing importance of external wins (II.11) to offset institution shrinkage.

---

## II.4 Jobs to Be Done

### For member banks — candidate jobs tested against evidence

| Candidate job | Verdict | Evidence |
|---|---|---|
| **Remain an independent bank at all** | **PRIMARY JOB** | Without shared IT, a €500m rural Raiffeisenbank could not meet MaRisk/BAIT/DORA or offer a competitive app. UmweltBank's Koppmann: "Wir benötigen … einen starken Partner, der uns das ganze Spektrum an digitalen Lösungen … bietet." |
| **Satisfy MaRisk/BAIT/DORA without building the capability** | Confirmed, major | agree21Finanzen automates Meldewesen; §25b KWG responsibility stays with the bank but execution is Atruvia's (II.5.F). |
| **Compete digitally vs Sparkassen and neobanks** | Confirmed, contested outcome | VR Banking App 84.5 pts vs Sparkassen 92.6 (Capital 2026). |
| **Hold the cost-income ratio down** | Confirmed | Scale economics; but IT cost rises (II.8) push the other way. |
| **Access sector-wide scale economics** | Confirmed, foundational | Single platform, shared development, shared regulatory implementation. |

**What Atruvia says it sells vs what banks are buying.** Atruvia says it sells a "Technologie- und Digitalisierungspartner" relationship. **ANALYTICAL INFERENCE:** what banks actually buy is *the ability to remain independent regulated banks* — a bundle of software + regulatory compliance + scale economics + risk transfer that no single small bank could assemble. The software is the visible product; the licence-to-operate is the real purchase.

### For end customers — the VR Banking App vs Sparkassen and neobanks

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

## II.5 Service-Delivery Flow Reconstruction (replaces money-movement; priority depth)

Six flows, kept strictly separate.

### A. Transaction flow (payments/bookings on behalf of banks)
End customer initiates in a channel → agree21 core (IMS/Db2) validates and posts → interbank leg clears via **DZ Bank** (Clearingstelle) for non-internal payments → counterparty bank. Atruvia is **processor/operator**; the **member bank is the principal**; **DZ Bank is the clearer**; the **Bundesbank/EBA CLEARING** provide settlement rails (TIPS for instant; see II.6). ~9–10bn business bookings/year decompose into ~80bn+ IMS transactions (II.0).

### B. Data flow and GDPR roles
CONFIRMED FACT (mechanism). Customer/account/transaction data and regulatory-reporting data flow between bank and Atruvia data centres. **GDPR: bank = controller; Atruvia = processor** under an Auftragsverarbeitungsvertrag (AVV). Regulatory-reporting data flows outward from agree21Finanzen to the Bundesbank/BaFin **on the bank's behalf and responsibility**. Atruvia's AI products run in a **private cloud with no open-internet connection** to keep processing within the AVV/GDPR perimeter. ANALYTICAL INFERENCE: the AVV + §25b KWG outsourcing contract is the legal spine of the entire relationship (II.5.F).

### C. Software-release flow — how a release reaches ~800 banks (Priority Gap 4)
CONFIRMED FACT (mechanism, reconstructed from the M365 and BankingWorkspace rollouts, which Atruvia documents as templates):
1. **Technical tests** (BankingWorkspace: Q4 2022).
2. **Pilotierung** with a small cohort (M365: 8 pilot banks end-2022; BWS piloting from 2023).
3. **Serienpiloten / Serienfähigkeit** proving mass-rollout capability (M365: 12 pilot banks in 2022, then 44 in 2023 → 56 including Vor- und Serienpiloten).
4. **Serienmigration** in tranches (M365: ~300 banks in 2024).
5. **Bank-side acceptance and change management** — each bank must do MaRisk-conform change assessment "gem. AT 8.2," retest its processes and schedule.
6. **The annual technical year-end close (technischer Jahresabschluss)** is the marquee coordinated release event — "erneut … sehr geräuschlos."
7. **Notification** via SPP/agree21Communitys, LiveTalks, Strategie Hub Regional and the Atruvia Hub.

**ANALYTICAL INFERENCE:** releases are centralised and quasi-mandatory (multi-tenant platform → one code line for all), but *adoption of new optional processes* (of ~300 available) is bank-by-bank. The bank's "acceptance role" is real for change-management/AT 8.2 but does **not** include the right to refuse a core release — a single tenant cannot fork the platform. This is the source of both the sector's rollout speed and its systemic single-point-of-failure risk (II.12).

### D. Money flow (fees from banks to Atruvia)
CONFIRMED FACT (structure; specifics UNKNOWN). Banks pay via the Umlage/Leistungsentgelte model: a **Basispaket** (with a volume element, "Mengenwachstum im Basispaket"), a **Festpreis** component, the infrastructure/Netze/Collaboration/Arbeitsplatz charges, plus the special levies (IT-Sonderumlage, Digitalisierungsumlage). GB2021 revenue split (closest public breakdown): **Erlöse aus Bankverfahren €863.1m** and **Erlöse aus Infrastruktur €227.9m** of €1,496.1m total. Invoicing cadence and per-unit tariffs are **UNKNOWN** (internal Leistungsverzeichnis; confidential). See II.8.

### E. Support and incident flow
CONFIRMED FACT. Tiered:
- **Serviceline** — a qualified *technical end-customer hotline* for OnlineBanking/MobileBanking, GENO cash, Profi cash, VR-NetWorld Software and BankingManager, plus remote-desktop (Fernwartung). Crucially "**only reachable via the telephone number provided by your bank**" — the bank fronts it; Atruvia stays invisible.
- **Bank-facing service desk** for the institutions themselves.
- **Escalation** — during major incidents Atruvia convenes a **Krisenstab** (evidenced 9 Nov 2020) and communicates to banks; banks then communicate to end customers (e.g. 7 July 2026: users warned not to resubmit transfers).
- Status communication during the 7 July 2026 outage was via bank websites and press statements; Atruvia deliberately switched off app/online banking "um die Systeme zu entlasten."

### F. Regulatory-responsibility flow (§25b KWG)
CONFIRMED FACT (mechanism). Under **§25b KWG / MaRisk AT 9 / BAIT**, outsourcing does not transfer regulatory responsibility: the **member bank remains fully responsible** to BaFin; Atruvia executes. This requires (1) a written outsourcing contract with mandated content; (2) the bank's **Auslagerungsregister**; (3) **audit rights** for the bank and BaFin flowing through to Atruvia; (4) exit/contingency provisions, now sharpened by **DORA Article 30** mandatory clauses and exit strategies (II.10). The 2018 BaFin special inspection (triggered via Volksbank Jever) and the **§44 KWG special inspection begun Nov 2023** (Volume I) demonstrate BaFin reaches Atruvia *through* its supervised banks. Atruvia was **not** designated a DORA Critical ICT Third-Party Provider (18 Nov 2025), though IBM was (Volume I) — a material risk observation (II.12).

---

## II.6 Transaction Processing Teardown (priority depth)

Each event: system → legal entity → data → control point → failure mode.

### (1) SEPA credit transfer initiated in the VR Banking App
1. **Initiation** — VR Banking App (Atruvia); **release via VR SecureGo plus** (SCA/PSD2). *Control:* SCA. *Data:* payment instruction, device binding.
2. **Core processing** — agree21 (Atruvia; IMS/Db2) validates balance/limits, debits. *Control:* balance/limit check, fraud screening (AI since 2017). *Failure:* core outage → order stuck (7 July 2026 pattern).
3. **Clearing** — interbank leg via **DZ Bank** (Clearingstelle) → SEPA scheme → creditor bank. *Legal entity:* DZ Bank principal for clearing; customer's bank principal for the payment; Atruvia processor.
4. **Settlement** — via Bundesbank/EBA CLEARING. *Failure:* duplicate-submission risk if users resubmit during an outage (explicit 7 July 2026 warning).

### (2) SEPA instant payment (SCT Inst)
ANALYTICAL INFERENCE + CONFIRMED FACT (partial). Wero transactions "werden direkt von Ihrem Girokonto in Echtzeit ausgeführt" (CONFIRMED). Instant SEPA routes through DZ Bank's real-time platform to **TIPS** (the Eurosystem instant-settlement platform referenced in the Bundesbank Verfahrensregeln for SEPA-Echtzeitüberweisungen). GENO cash already supports instant single orders (CONFIRMED). *Control:* the <10-second execution guarantee and recipient-PSP-reachability check. *Failure:* rejection if recipient PSP unreachable or TIPS rejects. **Atruvia's precise SCT Inst reach is UNKNOWN**, but DZ Bank states "alle Zahlungsverkehrskonten im Hause der DZ BANK [sind] für den Empfang von Echtzeit-Zahlungen freigeschaltet."

### (3) girocard point-of-sale transaction
ANALYTICAL INFERENCE + CONFIRMED FACT. Card at terminal → acquirer (**VR Payment** on acceptance) → girocard scheme → **issuer processing** (today partly Atruvia/partly VR Payment) → agree21 posts. *Legal entities:* merchant's bank/VR Payment (acquiring), the scheme, the issuing cooperative bank (principal), Atruvia (issuer processing). *Failure:* card-processing outage → declines. **From 1 Jan 2027** issuer processing (debit **and** credit) consolidates at Atruvia; acquiring/POS stays at VR Payment.

### (4) ATM cash withdrawal
CONFIRMED FACT (partial). Card at one of ~30–34k Atruvia-operated terminals → authorisation via issuer processing → agree21 debit. *Resilience fact:* during 9 Nov 2020 and DDoS incidents, SB-terminals largely kept working when online/app were down ("Bargeldversorgung weiterhin möglich") — ATMs sit on a partly independent path. *Failure:* central-system outages can still propagate to Auszugsdrucker/terminals (reported sporadically 2020).

### (5) Card transaction today vs after the 1 Jan 2027 migration
- **Today:** debit issuer processing at Atruvia; **credit-card processing at VR Payment**; acquiring at VR Payment. Two houses, "Doppelstrukturen."
- **From 1 Jan 2027:** Atruvia runs **unified issuer processing for girocard + debit + credit on one integrated platform**; VR Payment keeps acquiring/POS/omnichannel. Rationale: consolidate double structures, lift synergies, avoid parallel investment; and — decisively for lock-in — "Wenn Konto und Karte bei Atruvia zusammengeführt werden, verbessere das die Verzahnung zentraler Leistungen." *Bundeskartellamt:* B9-75/26, notified 15 July 2026.

### (6) Loan application and account opening
CONFIRMED FACT (mechanism). Digital end-to-end strecken via the Omnikanalplattform/agree21ECON (e.g. "Sofortkredit Privatkunde," digital Baufinanzierung with self-service, analytics, document management; "Neukunde (Produktverkauf)" automated customer+account creation). AI document recognition extracts data from IDs/energy certificates/financial documents. *Control:* KYC/credit decisioning (bank's rules). *Legal entity:* bank is lender/principal; Atruvia provides the rails.

### (7) Branch-counter transaction through the Bankarbeitsplatz
CONFIRMED FACT. Bank employee works in **BankingWorkspace** / legacy **agree21BAP** → agree21 core. *Control:* employee authorisation/role model. *Failure:* during coexistence, some functions (CRM) exist in both → double maintenance, error risk (Coenen's "zäh").

### (8) Third-party aggregator access via FinTS/PSD2
CONFIRMED FACT. External software (windata, konfipay, ALF-BanCo, GLS eBank, subsembly) connects to fints1/fints2.atruvia.de. *Legal entity:* Atruvia operates the PSD2/FinTS access interface on the bank's behalf; the bank is the ASPSP. *Failure:* FinTS server unreachable → aggregators fail (evidenced 7 July 2026 HBCI/FinTS problems; and the CAMT52 special-character bug of 10 June 2020).

Where internal mechanics are not public they are labelled UNKNOWN (notably exact SCT Inst reach and internal card-platform architecture pre-2027).

---

## II.7 Channel Architecture

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

## II.8 Pricing and Cost-Allocation Architecture (priority depth)

### The structure

CONFIRMED FACT. Banks fund Atruvia through:
1. **Leistungsentgelte / Basispaket** — base service fees with a volume-growth element.
2. **Festpreis** components.
3. **Infrastructure / Netze, Collaboration & Arbeitsplatz** charges.
4. **Special levies:** the **IT-Sonderumlage** and the **Digitalisierungsumlage**.

### The IT-Sonderumlage and its perpetuation

CONFIRMED FACT (Börsen-Zeitung, "Atruvia will IT-Umlage verstetigen"): the IT-Sonderumlage, resolved ~2018 as a five-year Zukunftsinvestition, "belief sich auf 60 Mill. Euro jährlich" from the cooperative banks — "Weitere 180 Mill. Euro kamen vom Zentralinstitut DZ Bank und rund 200 Mill. Euro von der Rechenzentrale selbst." DER PLATOW Brief: cumulatively "seit 2018 300 Mio. Euro" collected from the Volks- und Raiffeisenbanken. Due to expire end-June 2023, Atruvia sought its **Verstetigung**; the Aufsichtsrat was to decide "bereits Ende April" 2023, with details worked out from summer. Atruvia and BVR declined to comment and left "die Frage nach der Gesamtsumme der heutigen Leistungsentgelte unbeantwortet" — confirming the total Leistungsentgelte figure is deliberately undisclosed.

### The Digitalisierungsumlage and its tripling

CONFIRMED FACT (DER PLATOW Brief, June 2024): the Digitalisierungsumlage for the Primärinstitute rises "**von zuletzt 30 Mio. Euro über 60 Mio. im laufenden Jahr auf 90 Mio. Euro in 2025**" — a tripling. Being small relative to total revenue, "Ihre Anhebung führt unter dem Strich nur zu einem prozentual einstelligen Preisanstieg." Bank reaction: "Viele Primärbanker stellen immer lauter die Frage, ob das Geld wirklich gut eingesetzt ist … mit dem digitalen Produktangebot … sind längst nicht alle Volksbank-Vorstände zufrieden." And: the price structure "ist ein Thema, über das in den BVR-Führungsgremien nachgedacht wird, auch wenn es noch keine offene Diskussion dazu gibt."

### The general price increases

CONFIRMED FACT. A **~5% average inflation-driven increase from 1 April 2023** (announced Dec 2022). Börsen-Zeitung: further 2024 increases to give Atruvia "im Schnitt weitere 5% der heutigen Leistungsentgelte der gesamten genossenschaftlichen Organisation" as additional investment.

### The ~€125m migration synergies "partly taken back"

ANALYTICAL INFERENCE from the record: the agree21 consolidation was sold to banks partly on cost savings; the subsequent tripling of the Digitalisierungsumlage plus perpetuation of the IT-Sonderumlage means the savings are "partly taken back." Mechanism: one-time consolidation synergies were converted into ongoing higher levies to fund the never-ending digital-investment race. (Scenario calculations circulating in the group — Börsen-Zeitung — suggested the sector "im Extremfall" might need €450m–€1bn annually to match European digital front-runners; this is an explicitly hypothetical scenario, **not** a committed figure — HYPOTHESIS.)

### The shift to nutzenbasierte (usage-based) pricing — announced 2025

CONFIRMED FACT. Vorstandssprecher/CFO Martin Beyer (HV 2025; Atruvia Magazin, 06.05.2025): "Wir reduzieren sukzessive den Anteil der Umlagefinanzierung am Gesamtumsatz durch eine nutzenbasierte Bepreisung. Das heißt für unsere Kunden: Sie bezahlen je nach Mehrwert und Nutzen für unsere Lösungen." Mechanism: "Erlöse werden stärker als heute mit den vorgenannten Indikatoren verknüpft" — revenue tied to digital-usage indicators (Digitalisierungsquote/Nutzungsquote), with "eine spezielle Förderung im Preismodell" rewarding banks that raise digital usage. Phasing is gradual ("sukzessive"); exact indicators and tariffs are **UNKNOWN**.

### The financial-strategy pivot and dividend question

CONFIRMED FACT. Beyer: "Wir streben eine **Zielrendite von 4 Prozent in Bezug auf den Umsatz** an und steigern nachhaltig das Betriebsergebnis, um ein dauerhaftes Plus für neue Investitionen zu generieren." The stated policy is to **self-fund investment from retained earnings rather than distribute** — investments "künftig aus eigener Kraft." Trajectory: Betriebsergebnis €40.6m (2023) → €66.6m (2024) → €89.0m (2025, Betriebsergebnismarge **4.7%**, exceeding the 4% target). No explicit dividend-per-share policy to owners was found (UNKNOWN). **ANALYTICAL INFERENCE:** returns to owners come primarily as *lower-than-market IT costs and reinvestment*, not as dividends — the cooperative "dividend" is the subsidised platform itself.

### Actual price levels (Priority Gap 1) — the honest answer

**UNKNOWN / not public.** After targeted search of the Bundesanzeiger, member-bank Geschäftsberichte, BVR and trade press:
- **Per-unit prices** (per account, workstation, transaction) are **not disclosed**; the Leistungsverzeichnis is confidential; Atruvia refused even the aggregate Leistungsentgelte figure to Börsen-Zeitung.
- **Member-bank annual reports do not break out an "Atruvia line."** Atruvia costs sit inside "andere Verwaltungsaufwendungen," with "Datenverarbeitung und Digitalisierung" named only as a qualitative driver (e.g. Frankfurter Volksbank Rhein/Main GB2023: the rise in andere Verwaltungsaufwendungen was driven "unter anderem [durch] gestiegene Aufwendungen in den Bereichen Datenverarbeitung und Digitalisierung"; Berliner Volksbank GB2025: "höhere Kosten für unsere IT-Anwendungen").
- **The only quantified figures are the group-level levies:** IT-Sonderumlage €60m/yr from the banks (+€180m DZ Bank +€200m Atruvia self-funded); €300m cumulative 2018–2023; Digitalisierungsumlage €30m→€60m→€90m (2023–2025); ~5% annual Leistungsentgelte rises; and the GB2021 split (Bankverfahren €863.1m / Infrastruktur €227.9m).
- **A derived proxy** (revenue ÷ accounts) yields roughly €20 per account per year — but this is analyst arithmetic, **not an Atruvia price**, offered only as an order-of-magnitude ANALYTICAL INFERENCE.

### Governance of pricing and the under-pricing/captive-rent question

**ANALYTICAL INFERENCE (evidence-backed conclusion).** Pricing is *proposed by Atruvia's Vorstand*, *approved by the owner-dominated Aufsichtsrat*, and *contested informally in BVR-Führungsgremien*. There is **no competitive discipline** — the cooperative banks cannot realistically switch (II.10). Two opposing forces result:
- **Toward under-pricing/thin margins:** because every euro is an owner's cost, owners historically squeezed Atruvia to an €8m surplus on €1.4bn (2022) — evidence of *captive under-pricing of Atruvia*, not rent-extraction *by* Atruvia.
- **Toward captive rents:** the absence of exit and of price transparency, plus the ability to perpetuate "temporary" levies and triple the Digitalisierungsumlage with only muted dissent, gives Atruvia real pricing power going forward.

**Conclusion:** historically the owner-customer structure produced **under-pricing** (thin margins, chronic under-investment vs neobanks). The 2025 pivot to a 4% Zielrendite and usage-based pricing is an explicit, governed decision to **move from under-pricing toward sustainable pricing** — converting some latent captive pricing power into reinvestment capacity. Whether this tips into captive rents depends on whether the Aufsichtsrat and BVR hold margins near ~4%. As of 2025, 4.7% suggests the target is being met/slightly exceeded.

---

## II.9 Product Dependency Map

**agree21 is the platform everything attaches to.** Tested rather than assumed:
- **Core → workstation → channels → analytics.** agree21 (core) → BankingWorkspace/BAP (employee) and OnlineBanking/App (customer) → VR-Control/agree21Finanzen (steering) → TRUUCO/SmartData/genoGPT (analytics/AI). Each layer consumes core services via the proprietary API layer (~1,200 microservices, IBM). **Verdict: genuine, tight technical dependency.**
- **Single-platform migration enables sector-wide rollout.** One multi-tenant platform → a release reaches all at once (II.5.C). **Verdict: confirmed — the central economic engine.**
- **Subsidiaries cross-sell into the same base.** Peras (HR), Serviscope (BPO), parcIT (steering), FORUM (InfoSec), TRUUCO (analytics), BMS/fincompare (SME finance) all sell into the captive ~700-bank base. **Verdict: real but uneven** — parcIT/steering is near-mandatory; Peras/Serviscope are optional. The "Wertschöpfung vertiefen" strategy (Finanz-Szene) is precisely about raising attach rates.
- **Does the VR Payment acquisition create a genuine account+debit+credit bundle advantage?** **Verdict: YES (ANALYTICAL INFERENCE, high confidence).** From 1 Jan 2027, unifying account (agree21) + debit + credit + girocard issuer processing on one Atruvia platform (a) deepens lock-in ("Verzahnung zentraler Leistungen"), (b) removes VR Payment's parallel structure, and (c) makes Atruvia the single card-processing point for a large share of German credit-card transactions (Marzlin, McDermott). The most important *new* dependency Atruvia is building.

---

## II.10 Onboarding, Migration and Change

### When two member banks merge

CONFIRMED FACT (frequency) + ANALYTICAL INFERENCE (process). 40–45 mergers/year require technical migration. The standard process consolidates the two banks' agree21 tenants into one — migrating accounts, products, roles and history to the surviving institution's configuration over a weekend cutover. Because both already run agree21, this is a *tenant merge*, far simpler than an inbound external migration.

### How a new non-cooperative customer is onboarded (inbound migrations — verified)

CONFIRMED FACT:
- **Bank für Sozialwirtschaft:** contract 8 June 2021, go-live 23 April 2023 (~2-year programme, 200+ bank staff, ten sub-projects), migrating off a self-built SAP-based system in place since 2006, having evaluated SAP HANA as the alternative.
- **UmweltBank:** ~18 months' preparation, go-live October 2023; drivers were growth, changed customer expectations and regulation; chose Atruvia for a "standardisierte und am Markt erprobte" integrated solution.
- **National-Bank Essen:** replaced a system in use since 1996, ~30 applications consolidated, ~two-year project, completed October 2024.
- **M.M. Warburg:** announced; migrating off Sopra Steria's Corbas MBS; the bank's own statement: "das jetzige Kernbanksystem [wird] perspektivisch nicht mehr weiterentwickelt … ein Anbieterwechsel ist also zwangsläufig notwendig."
- **Sparda-Banken:** all 11 now on/moving to Atruvia. Four (Hamburg, Berlin, Hannover, Südwest) already used it; the other seven abandoned a joint Sopra Steria build and switched — Augsburg/Ostbayern first (spring 2024), Sparda-Bank West completing 2025; group fully on Atruvia by 2026. Notably, Verbandschef **Florian Rentsch** conceded that at the four already-migrated Sparda-Banken there had been customer losses "im signifikanten Bereich" during the switch — a rare, named, candid negative data point on migration disruption.
- **Bankhaus C.L. Seeliger:** a further external win (Finanz-Szene).

### The exit question (Priority Gap 5) — critical

**Has any bank ever left?** CONFIRMED FACT — **YES, one prominent case: the Deutsche Apotheker- und Ärztebank (Apobank)** migrated *away* from Fiducia/GAD to Avaloq over the 2020 Pentecost weekend. It was a **debacle**: transfers and basic services failed, customers were furious, and Apobank-CEO Ulrich Sommer publicly blamed Fiducia GAD for having told the bank only in early 2018 that Avaloq "nicht auf den Hardwaresystemen der Fiducia laufen könne" and that a Mischbetrieb was "nicht erwünscht." This is the exception that proves the rule: the one clear exit was painful and disruptive. Separately, **BMW Bank** and others chose *not* to join Atruvia (going to FIS Kordoba) — but that is *non-adoption*, not exit.

**Is exit practically possible for a cooperative bank?** **ANALYTICAL INFERENCE (high confidence): effectively no.** A Volksbank cannot leave because (1) it is an *owner* of Atruvia; (2) the entire cooperative ecosystem (DZ Bank clearing, Union Investment depots, R+V, VR Payment cards, BVR reporting, Wero) is integrated through agree21; (3) there is no alternative provider offering the cooperative-specific integrated solution; (4) the Apobank precedent shows migration away is high-risk. The switching options that exist (FIS, Avaloq, Sopra Steria) serve *private* banks, and the market trend is *toward* Atruvia (Sparda, UmweltBank, National-Bank, Warburg), not away.

**Contractual notice/exit-support:** standard notice periods and exit-support terms are **UNKNOWN** (contracts confidential), but **DORA Article 30 now mandates exit strategies and exit-support clauses** in ICT outsourcing contracts — so formal exit provisions must exist on paper even though practical exit is near-impossible for cooperative members.

---

## II.11 Non-Cooperative Customers and Third-Party Sales

CONFIRMED FACT. Products sold outside the cooperative sector:
- **Core banking (agree21)** to ~190 private banks and specials, plus new external wins (Bank für Sozialwirtschaft, UmweltBank, National-Bank Essen, M.M. Warburg, Bankhaus C.L. Seeliger, the Sparda group).
- **IT-outsourcing** (mainframe/virtualisation scale) to banks and *other industries* including the **ADAC**.
- **parcIT okular-Tools** to non-GFG banks (via Basis-Abo).
- **Ratiodata** managed services / **GWS** ERP to non-bank customers.

**How much revenue comes from outside the captive base?** **UNKNOWN precisely** — no product- or customer-type split is published. ANALYTICAL INFERENCE: still a **minority** but **the fastest-growing** part. Evidence: Atruvia's 2025 AG revenue growth to knapp €1.9bn (+11.5%) was attributed "hauptsächlich durch neue Kunden" (Atruvia, via IT-Finanzmagazin, HV 2026) — i.e. external wins, since the cooperative base is shrinking in count. GB2021 already noted intensified dialogue with private banks and IT-outsourcing scale effects.

**Genuine growth strategy or marginal by-product?** **Conclusion: a genuine, deliberate growth strategy.** With the cooperative base saturated and consolidating, external migrations + value-deepening are Atruvia's only two organic growth vectors. The active pursuit of Sparda, Warburg, Seeliger and the Bank für Sozialwirtschaft shows a new-logo motion, not opportunism. But the captive base remains the overwhelming majority of revenue.

---

## II.12 Failure and Exception Paths

### Full outage/incident history (Priority Gap 10)

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

### Who owns the problem, and the liability chain

**ANALYTICAL INFERENCE + CONFIRMED FACT (mechanism):**
- **Operationally**, Atruvia owns the fix (Krisenstab, status comms to banks).
- **Regulatorily and toward the end customer**, the **member bank owns the problem** — §25b KWG keeps responsibility with the bank; the end customer's claim is against the bank, not Atruvia. This is why Atruvia stays invisible even during a 520-bank outage.
- **Contractual liability / service credits between Atruvia and banks:** SLAs, availability commitments, service-credit and liability-cap terms are **UNKNOWN** (Priority Gap 2 — contracts confidential). Structurally, MaRisk AT 9 and **DORA Article 30** require the outsourcing contracts to contain service levels, audit rights, incident-reporting and exit clauses — so SLAs must exist, but their figures are not public.
- **Reputational consequence:** falls on the *banks* (their brand fronts the app/website) — a governance lever, since the owner-banks bear the reputational cost of Atruvia's failures, sharpening their interest in resilience.

### The systemic-risk observation

**ANALYTICAL INFERENCE (important).** The single multi-tenant platform that delivers Atruvia's economics also concentrates risk: one software error took out ~490–520 banks simultaneously (2023, 2026). Atruvia was **not** designated a DORA Critical ICT Third-Party Provider (18 Nov 2025) even though a single incident can disable ~500 German banks — a defensible reading is that the ESAs supervise the *cloud/hardware* layer (IBM designated) while Atruvia is captured indirectly via its banks. A genuine regulatory-perimeter question the report flags rather than resolves.

---

## II.13 Product-Market Evolution

CONFIRMED FACT (trajectory):
- **Booking cooperative → early cores.** Fiducia (founded 1924) and GAD built successive cores across the 1960s–2000s; predecessor systems in the lineage include the batch/booking era, then GEBOS/GENOS/RUBIN/bank21 (north) and NBS/BB3/agree (south).
- **Two platforms (2015 merger):** "agree" (south) and "bank21" (north) coexisted post-merger.
- **agree21 consolidation (to 2019–2020):** all banks onto one core primarily based on agree; **bank21 retired**.
- **Digital channels (2021–):** new OnlineBanking, rebuilt VR Banking App, VR SecureGo plus, Omnikanalplattform, BankingWorkspace.
- **2021 repositioning:** from "IT operator" to "**Digitalisierungspartner**"; rename Fiducia & GAD → **Atruvia** (1 Sep 2021).
- **Expansion into adjacencies:** HR (Peras/geno.HR), BPO (Serviscope), analytics (TRUUCO/SmartData), AI (plainGPT/genoGPT, KI-Kompetenzcenter), and **card processing** (VR Payment issuing from 2027).

**Coherent or accretive drift?** **Conclusion: largely coherent, with two caveats.** The core→channels→steering→analytics→AI stack is a coherent vertical deepening of the same customer. The card-processing move is coherent *bundling*. The genuinely adjacent bets — GWS ERP (non-bank), ADAC-type IT-outsourcing, and parts of the subsidiary ring — are closer to **opportunistic diversification** justified mainly by mainframe scale economics. Net: coherent platform strategy at the centre, mild accretive drift at the edges.

---

## II.14 Volume II Reconstruction

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

### The five closing questions answered

- **True core product?** **agree21** — the mainframe core banking process; every other product is an attachment.
- **Strongest lock-in mechanism?** Today: **agree21 + cooperative-ecosystem integration** (ownership + DZ Bank clearing + Union/R+V + BVR reporting). Strengthening fastest: the **unified card platform from 1 Jan 2027**.
- **Best economics?** **The multi-tenant platform releases** (one code line → ~700 banks) and the **near-mandatory steering software (parcIT/VR-Control)** — high attach, low marginal cost. IBM-scale mainframe outsourcing to third parties (incl. ADAC) also earns scale rents.
- **Strategically important despite being small today?** **genoGPT/the AI portfolio** and **Wero** — small revenue now, decisive for future competitiveness and defence against Big Tech/neobanks.
- **Who is the real customer?** **The cooperative sector as an institution** — operationalised as the ~700 member banks that own, pay for and govern Atruvia. The bank's end customer is the user Atruvia designs *for* but never contracts *with*.
- **What precisely does a member bank buy?** Not merely software. It buys **regulatory compliance it need not build, scale economics it could not achieve alone, risk transfer of IT execution (though not of regulatory responsibility), and — decisively — the ability to remain an independent bank at all.** The software is the delivery vehicle; the licence-to-remain-a-bank is the product.

---

### Data caveat on group-vs-AG revenue (flagged, not silently resolved)
Sources give different revenue bases. **Atruvia AG (parent):** ~€1.4bn (2022), ~€1.5bn (GB2021: €1,496.1m), knapp €1.9bn (2025, +11.5%). **Group/Konzern:** ~€1.77bn (older IBM/press), ~€2.2bn (2024, Volume I), and **€2.5bn per GB2025** (with 97m accounts, ~10bn transactions). Finanz-Szene separately reported a group figure "erstmals mehr als 2 Mrd. Euro … 2,001 Mrd. Euro" with a €50m operating result — likely an interim/rounded or different-perimeter figure. The most authoritative current group number is the **GB2025 figure of €2.5bn**; the €2.0bn and €2.2bn figures are earlier-period or narrower-perimeter and should not be treated as current. This discrepancy is preserved rather than averaged.

*End of Volume II. Volume III not begun, per instruction.*