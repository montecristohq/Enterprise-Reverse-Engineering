# The Experian Enterprise Reverse-Engineering Study

**A forensic institutional teardown of Experian plc — the information utility whose raw material is contributed free by the customers who then buy it back**

Research cut-off: 9 August 2026
Prepared by: Damascus Research
Volumes I–V complete · Cross-Volume Synthesis included

---

## Table of Contents

- [The Experian Enterprise Reverse-Engineering Study](#the-experian-enterprise-reverse-engineering-study)
  - [How to read this document](#how-to-read-this-document)
  - [Conventions governing the whole document](#conventions-governing-the-whole-document)
- [Part I — Corporate, Legal, Regulatory & Institutional Anatomy](#part-i-corporate-legal-regulatory-institutional-anatomy)
- [Part II — Product, the Three-Sided Customer Structure & the Inverted Value Flow](#part-ii-product-the-three-sided-customer-structure-the-inverted-value-flow)
- [Part III — Operations, Identity Infrastructure, Data, Technology & Organisational Design](#part-iii-operations-identity-infrastructure-data-technology-organisational-design)
- [Part IV — Financial Statements, Revenue Architecture, Unit Economics & Capital](#part-iv-financial-statements-revenue-architecture-unit-economics-capital)
- [Part V — Management, Culture, Competition, Moat, Risk & Strategic Evolution](#part-v-management-culture-competition-moat-risk-strategic-evolution)
  - [VOLUME V — Management, Culture, Competition, Moat, Risk & Strategic Evolution](#volume-v-management-culture-competition-moat-risk-strategic-evolution)
- [Part VI — Cross-Volume Synthesis](#part-vi-cross-volume-synthesis)
  - [VI.1 What Experian actually owns](#vi1-what-experian-actually-owns)
  - [VI.2 The single causal model](#vi2-the-single-causal-model)
  - [VI.3 What the volumes prove together that none proves alone](#vi3-what-the-volumes-prove-together-that-none-proves-alone)
  - [VI.4 The central tension](#vi4-the-central-tension)
  - [VI.5 What would falsify this reading](#vi5-what-would-falsify-this-reading)
  - [VI.6 What Experian is becoming](#vi6-what-experian-is-becoming)
  - [VI.7 Implications for a fintech builder](#vi7-implications-for-a-fintech-builder)
  - [VI.8 Ten cross-volume conclusions](#vi8-ten-cross-volume-conclusions)
- [Appendix A — Glossary of Regulatory and Technical Terms](#appendix-a-glossary-of-regulatory-and-technical-terms)
  - [US regulatory](#us-regulatory)
  - [UK and EU regulatory](#uk-and-eu-regulatory)
  - [Brazil](#brazil)
  - [Industry mechanics](#industry-mechanics)
  - [Products and platforms](#products-and-platforms)
  - [Financial](#financial)
- [Appendix B — Canonical Figures Register](#appendix-b-canonical-figures-register)
  - [Group financials — FY26 (year to 31 March 2026)](#group-financials-fy26-year-to-31-march-2026)
  - [Revenue architecture](#revenue-architecture)
  - [Cost architecture (Benchmark, % of revenue)](#cost-architecture-benchmark-of-revenue)
  - [Balance sheet and capital](#balance-sheet-and-capital)
  - [Corporate](#corporate)
  - [Operational scale](#operational-scale)
  - [Pricing and the mortgage chain](#pricing-and-the-mortgage-chain)
  - [Litigation and regulation](#litigation-and-regulation)
- [Appendix C — Reconciliation of Cross-Volume Discrepancies](#appendix-c-reconciliation-of-cross-volume-discrepancies)
  - [Basis, date and vintage differences — not errors](#basis-date-and-vintage-differences-not-errors)
  - [Genuine errors, corrections and supersessions](#genuine-errors-corrections-and-supersessions)
  - [Known unknowns carried forward](#known-unknowns-carried-forward)
- [Appendix D — Source Hierarchy & Evidence Conventions](#appendix-d-source-hierarchy-evidence-conventions)

## How to read this document

This study takes Experian apart component by component across five volumes, then reassembles it. Each volume was researched and written as a standalone study; this master edition binds them into one document with a single set of conventions, a glossary, a canonical figures register, and a synthesis that no individual volume contains.

| Part | Volume | Question it answers |
|---|---|---|
| Front matter | — | Conventions, glossary, canonical figures, how to navigate |
| Part I | Corporate, Legal, Regulatory & Institutional Anatomy | Who owns it, which entity holds which database under which permission, and how a data business is regulated across incompatible jurisdictions |
| Part II | Product, the Three-Sided Customer Structure & the Inverted Value Flow | What it sells, to whom, and how a free input becomes paid output |
| Part III | Operations, Identity Infrastructure, Data, Technology & Organisational Design | How records are matched to people, and what happens when that fails |
| Part IV | Financial Statements, Revenue Architecture, Unit Economics & Capital | Where a 28.6% margin comes from when the raw material costs nothing |
| Part V | Management, Culture, Competition, Moat, Risk & Strategic Evolution | Why it wins, what could break it, and what it becomes |
| Part VI | **Cross-Volume Synthesis** | What the five volumes prove together that none proves alone |
| Appendix A | Glossary of Regulatory and Technical Terms | Load-bearing — read before Part II |
| Appendix B | Canonical Figures Register | The governing value for every material number, with its basis |
| Appendix C | Reconciliation of Cross-Volume Discrepancies | Where the volumes disagree, and which figure governs |
| Appendix D | Source Hierarchy & Evidence Conventions | How claims were graded |

**Recommended reading order for a first pass:** Appendix A (glossary) → the conventions below → Part VI (Synthesis) → Appendix B → then Parts II and V in full. Parts I, III and IV are reference-depth.

---

## Conventions governing the whole document

### Evidence classification

Every material claim carries one of six labels. No inference is silently promoted to fact.

| Label | Meaning |
|---|---|
| **CONFIRMED FACT** | Directly supported by reliable primary evidence |
| **COMPANY CLAIM** | Stated by Experian, not independently verified |
| **THIRD-PARTY ESTIMATE** | Externally reported or estimated |
| **ANALYTICAL INFERENCE** | Reasonably inferred from multiple known facts |
| **HYPOTHESIS** | Possible explanation requiring further evidence |
| **UNKNOWN** | Available evidence is insufficient |

### The governing convention — statutory versus Benchmark. Read this before any figure.

Experian reports under **IFRS in US dollars** with a **31 March financial year end**, and presents a parallel suite of non-GAAP **Benchmark** measures. The two sets are different numbers, and the market prices the Benchmark ones. Four rules apply throughout:

1. **Never mix statutory and Benchmark measures in one comparison.** FY26 statutory profit before tax was US$1,951m; Benchmark profit before tax was US$2,212m. Statutory basic EPS was 164.5 US cents; Benchmark EPS was 179.8. The gap is not noise — it is the subject of Part IV's forensic reconciliation.
2. **Always state whether a growth rate is organic, constant-currency or actual-rate.** FY26 ongoing revenue grew 8% organic, 11% at constant currency and 13% at actual rates. All three are true; they are not interchangeable.
3. **Distinguish total revenue from ongoing-activities revenue.** Statutory revenue was US$8,445m; ongoing revenue US$8,425m, after certain Latin America and EMEA/Asia Pacific B2B lines were re-presented as exited from FY26.
4. **The financial year ends 31 March.** FY26 is the year to 31 March 2026. Competitor comparisons against Equifax and TransUnion (December year ends) are therefore three months offset.

### The second governing convention — Follow-the-Data-Right

This study applies a rule with no analogue in the three prior subjects. **Experian does not own most of the data it holds.** Wherever data is discussed, the study establishes who contributed it, under what statutory and contractual permission, who the controller is, and what the permission allows.

The consequence for every reader: **revenue in this business is contingent on legal permissions persisting.** A product lawful as a marketing audience may be unlawful as a credit decision. A data category present in the file today can be legislated out of it tomorrow — as medical debt demonstrates. Revenue quality here is partly a legal question, not only a commercial one.

### Language

Regulatory acronyms are retained rather than translated, and defined in Appendix A. The study spans US, UK and Brazilian regimes that use different vocabulary for the same concepts; Appendix A maps them.

---


---

# Part I — Corporate, Legal, Regulatory & Institutional Anatomy

### VOLUME I — Corporate, Legal, Regulatory & Institutional Anatomy
*Prepared as of 9 August 2026. Reporting basis: IFRS, US dollars, 31 March financial year-end. Non-GAAP measures (Benchmark PBT/EBIT/EPS, organic revenue growth) are labelled wherever used and never mixed with statutory figures in the same comparison.*

---

### TL;DR
- Experian plc is a **Jersey-incorporated, Irish-tax-resident, Dublin-headquartered, London-listed** information utility whose single most valuable and most misunderstood asset is not data it owns but the **legally-sanctioned aggregation of data contributed for free by its own customers** under reciprocity rules and statutory permission — a position that would take a new entrant a decade to replicate and, in the UK, is close to legally impossible to build from zero.
- The group is a **listed information utility with no controlling shareholder** (largest holder BlackRock ~5.9%); real control sits with a dispersed institutional register and the executive team, while the single most strategically decisive legal entity is **Experian Information Solutions, Inc.** (an Ohio corporation), the US FCRA bureau that generates the majority of group profit.
- Regulation is simultaneously Experian's **deepest moat and its largest tail risk**: the FCRA/CFPB, UK GDPR/ICO/FCA and Brazilian LGPD/Cadastro Positivo/Banco Central regimes are mutually incompatible, and the live **CFPB "sham investigations" lawsuit (7 January 2025)**, the 2015 breach settlements and the multi-year ICO litigation demonstrate that the enforcement surface is structural rather than incidental.

---

### Key Findings

1. **The three-way corporate split is confirmed by primary sources.** The FY26 results announcement (20 May 2026) states verbatim that Experian plc "is incorporated and registered in Jersey as a public company limited by shares and is resident in Ireland. The Company's registered office is at 22 Grenville Street, St Helier, Jersey, JE4 8PX, Channel Islands." Corporate headquarters are in Dublin (2 Cumberland Place, Fenian Street, D02 HY05); operational hubs are Nottingham (The Sir John Peace Building, NG80 1ZZ), Costa Mesa (California) and São Paulo. **The user's summary was correct** — with one nuance: the *registered office* is in Jersey, while Dublin is the *corporate HQ* and tax residence.

2. **The finance entity is the ghost of GUS.** Experian Finance plc (UK company 00146575, incorporated 17 March 1917) is the same legal person that was "The Great Universal Stores PLC" (1917–2001) and then "GUS plc" (2001–2006) — the retailer parent, repurposed after the 2006 demerger as the group's principal bond-issuing vehicle. This is a striking path-dependency: the retailer did not spin its credit department out into a fresh shell; the credit department kept the retailer's 108-year-old corporate shell as its treasury.

3. **Scale (FY26, year to 31 March 2026, primary source Experian FY26 announcement).** Statutory revenue US$8,445m (up 12%); Benchmark EBIT from ongoing activities US$2,407m at a 28.6% margin (up 50bps at actual rates); Benchmark EPS 179.8 US cents (up 15% at actual rates); statutory profit before tax US$1,951m (up 26% from US$1,549m in FY25); Benchmark tax rate 25.5%; post-tax ROCE 17.2%; net debt/Benchmark EBITDA 1.7x. North America delivered ~two-thirds of group revenue; Consumer Services now serves "over 215 million free members globally."

4. **The data-rights architecture is the institutional heart.** Experian largely does *not* own the raw data. It holds it under statutory permission (FCRA in the US; "protection of credit" under LGPD Article 7(X) and the Cadastro Positivo law in Brazil) and under contractual reciprocity (the SCOR Principles of Reciprocity in the UK). What Experian owns outright is the *aggregation*, the *derived attributes and bureau scores*, the *models* and the *identity-matching graph*.

5. **The enforcement record is extensive and continuing** (see enforcement table in I.6), spanning a 2017 CFPB consent order (US$3m), the 2015 T-Mobile breach settlements (~US$16m across the coalition), the ICO litigation (2020–2024, largely won by Experian), the abandoned ClearScore merger (CMA, 2018–19) and the live CFPB dispute-handling lawsuit (2025).

---

### Details

#### I.1 Origin and Corporate History — Chronological Institutional Evolution

Experian's institutional lineage is a fusion of two utterly different corporate cultures: a British mail-order retailer's in-house credit-checking department (CCN) and an American aerospace conglomerate's data division (TRW). The path dependencies created in 1996 and 2006 still define the group.

| Date | Event | Structural / capability consequence |
|---|---|---|
| 1826 onward | London/Manchester merchants exchange credit information (the Manchester Guardian Society lineage often cited) | Deep cultural root of reciprocal data-sharing in the UK |
| 1964 | Credit Data Corporation founded (Detroit) | US consumer-bureau lineage begins |
| 1968 | TRW Inc. acquires Credit Data Corp → TRW Information Systems & Services | US national scale under an aerospace/electronics parent |
| 1980 | Great Universal Stores (GUS) launches **CCN Systems** in Nottingham (John Peace) | UK credit-checking arm of a mail-order retailer — the true corporate root of today's plc |
| Sep–Nov 1996 | TRW IS&S spun out (backed by **Bain Capital** and **Thomas H. Lee**); renamed **Experian**; within weeks GUS buys it for ~US$1.7bn and merges it with CCN | Transatlantic bureau created; "Experian" brand adopted; dual HQ Nottingham/Orange County. The PE backers reportedly tripled their money within weeks |
| 10 Oct 2006 | Demerger from GUS; LSE listing (initial price ~£5.60); Home Retail Group separated in parallel | Independent FTSE 100 company. **The old GUS plc shell becomes Experian Finance plc**; Don Robert CEO, John Peace Chair |
| Jun 2007 | Acquires initial 65% of **Serasa** (Brazil) for R$2.32bn (~US$1.2bn) from a consortium of banks (Bradesco, Itaú, Unibanco, ABN Amro, Santander, HSBC); to 70% by Oct 2007 | Entry into the dominant Brazilian bureau; put/call options over the minority created |
| 2008 | Listed parent renamed from "Experian Group Limited" to "Experian plc" | Naming trap: a UK subsidiary is *also* called Experian Group Limited |
| Oct–Nov 2012 | Acquires further 29.6% of Serasa for R$3.1bn (~US$1.5bn) → **99.6%**; cumulative spend R$5.6bn (~8.5x EBITDA). BIU (Itaú/Bradesco) classified as related party under the Listing Rules | Serasa becomes near-wholly-owned; negative-data agreements extended and positive-data commitments secured for when Cadastro Positivo became operational |
| Sept 2015 | **T-Mobile/Experian breach** (~15 million consumers) disclosed | Largest breach event; multi-state AG and class litigation |
| Mar 2018–Feb 2019 | Attempted acquisition of **ClearScore** (legal target: Credit Laser Holdings Ltd) for ~£275m; CMA Phase 2; parties abandon; **CMA cancels the reference 27 Feb 2019** | Competition authority signals it will protect free credit-checking competition (see I.8) |
| Nov 2020 | Acquires **Tapad** (US digital identity) for ~US$280m from Telenor | Cross-device digital identity graph |
| Oct 2020 → Apr 2024 | ICO enforcement notice → FTT → Upper Tribunal (see I.6) | Data-broking legal-basis fight, ultimately won by Experian |
| 2024 | Acquires **illion** (Australia/NZ, ~A$820m), **NeuroID** (behavioural fraud, Aug 2024), **Audigent** (ad identity, Dec 2024) | APAC bureau scale; fraud/identity build-out |
| 7 Jan 2025 | **CFPB sues Experian** ("sham investigations") in C.D. Cal. | Live FCRA/CFPA litigation |
| 1 Apr 2025 | Completes **ClearSale** (Brazil transactional fraud) for up to R$1,905m (~US$350m) | Extends ID&F suite in Brazil |
| Oct 2025 | Acquires **KYC360/KYC Global Technologies** (UK/Ireland RegTech), **AtData** (email identity, 10bn+ addresses), **Own Up** (US mortgage marketplace) | Compliance, identity and consumer-marketplace expansion |

**Divestitures / transitions:** From FY26 the group re-presented certain Latin America and EMEA/Asia-Pacific B2B lines as "exited business activities," and largely completed its cloud migration in North America and Brazil (ex-Health). Note that "Compuscan" (a South African bureau acquired 2019) and "Tapad" were both genuine Experian acquisitions; there is no evidence any of ClearSale, NeuroID, Compuscan or Tapad were subsequently divested — they were retained and integrated.

#### I.2 Corporate Group Structure

**Verified entity chain (primary registry data, corroborated via UK Companies House and the group's debt disclosures):**

- **Experian plc** — listed parent (LSE: EXPN). Jersey company; registered office 22 Grenville Street, St Helier, JE4 8PX; tax-resident Ireland; corporate HQ Dublin. **Ultimate guarantor of all group debt.**
- **Experian Finance plc** — UK company **00146575** (incorporated 17 Mar 1917; formerly The Great Universal Stores PLC → GUS plc). Group financing / debt-issuing entity; principal issuer under the US$6bn EMTN programme.
- **Experian Group Limited** — UK company **03720393** (inc. 1999). UK holding company. *Distinct* from the pre-2008 name of the listed parent — a genuine trap for outsiders.
- **Experian Holdings Limited** — UK company **03478895** (inc. 1997). UK holding company (its officers are registered at the Dublin corporate HQ address).
- **Experian (UK) Finance Limited** — UK company **07553817**. Intra-group finance entity that distributes part of the plc dividend via Income Access Share arrangements.
- **Experian Limited** — UK operating company **00653331** (inc. 22 Mar 1960); Nottingham; **FCA-authorised**; operates the UK CAIS bureau and consumer brands (CreditExpert, CreditMatcher).
- **Experian Holdings, Inc.** — US intermediate holding company (state of incorporation **likely Delaware — UNVERIFIED**). Named alongside the operating entities in the 2017 CFPB consent order.
- **Experian Information Solutions, Inc.** — **Ohio corporation** (inc. 25 Sep 1996), the FCRA credit-reporting bureau; principal operations Allen, Texas and Costa Mesa, California; descended from TRW. **The single most strategically important operating entity** and the named defendant in the 2025 CFPB suit.
- **Experian Services Corp.** — Delaware corporation (shared services; LEI 635400L5ZONXBLQZQM08).
- **ConsumerInfo.com, Inc.** (dba **Experian Consumer Services**) — California company (domicile high-probability, **not SoS-confirmed**); the direct-to-consumer membership / Experian.com / Experian Boost business; Costa Mesa. Acquired by Experian in 2002.
- **Experian Marketing Solutions, LLC** — Delaware LLC; marketing-data / identity business (the entity behind the ICO matter's US-facing analogue; the ICO case itself concerned the UK arm within Experian Limited).
- **Experian Health, Inc.** — US healthcare payments/eligibility business (state of incorporation **UNKNOWN**; Tennessee or Delaware plausible given the Passport Health/MedeAnalytics heritage).
- **Experian Europe DAC** (Ireland) and **Experian Finance US, Inc.** — additional EMTN issuers.
- **Serasa S.A.** ("Serasa Experian") — Brazilian *sociedade anônima*; ~**99.6%** Experian-owned (last publicly verified figure, 2012); São Carlos / São Paulo; **Banco Central-accredited** Cadastro Positivo database manager (GBD) since 11 Oct 2019. CNPJ **UNKNOWN**.

**Why each material entity exists (causal taxonomy):**
- *Regulation:* Experian Information Solutions Inc. must be a US person to be an FCRA consumer reporting agency; Experian Limited must be FCA-authorised; Serasa must be a Banco Central-accredited GBD.
- *Tax / financing:* Experian Finance plc, Experian Europe DAC, Experian Finance US Inc. and Experian (UK) Finance Limited exist to issue/route debt and dividends efficiently across the Jersey/Ireland/UK/US perimeter.
- *Historical acquisition path:* Serasa S.A. persists as an intact Brazilian entity; the GUS shell survives as Experian Finance plc.
- *Liability ring-fencing:* separating the FCRA bureau (Experian Information Solutions) from the D2C consumer entity (ConsumerInfo.com), from marketing (Experian Marketing Solutions) and from Health isolates distinct litigation and regulatory exposures.

#### I.3 Ownership and Share Structure

Experian is a FTSE 100 constituent (ticker EXPN) with **ordinary shares on a one-share-one-vote basis, no dual-class or golden shares, and no controlling shareholder.** As most recently disclosed, the largest holders are global asset managers: **BlackRock ~5.9%**, with **The Vanguard Group** and **Massachusetts Financial Services** roughly level at ~5.1% each; Norges Bank Investment Management and Capital Group are also significant. The top ~25 shareholders together hold less than half the register, indicating a long tail of smaller holders. There is an OTC ADR/depositary programme (EXPGY/EXPGF). The group runs continuous buybacks (**US$725m executed in FY26**, plus a new **US$1bn programme announced May 2026 valid to 30 June 2027**) alongside a progressive dividend (FY26 total **69.25 US cents**, +11%).

**Economic and voting ownership do not diverge.** Control is contestable in principle: management can be removed by ordinary shareholder resolution, and there is no defensive bloc or family stake. In practice, control rests with the executive team, legitimised by a dispersed long-only institutional base that has historically backed the "Experian Way" strategy; there has been no public activist campaign. This is a materially different control structure from EREF Subjects II and III (Atruvia and DZ BANK), which are captive/cooperatively-owned — Experian is genuinely widely-held.

#### I.4 Governance Architecture

- **Chair:** Mike Rogers (independent NED from 1 July 2017; Chair from 24 July 2019). He has confirmed retirement at the AGM on **22 July 2026** after nine years. **Adam Crozier** was named as incoming Chair (announced April 2026); the succession was led by Senior Independent Director **Alison Brittain**.
- **CEO:** Brian Cassin. **CFO:** Lloyd Pitchford. Both remained in post through 2026.
- **Committees:** Audit; Remuneration (**Kathleen DeRose** appointed chair from the July 2025 AGM); Nomination and Corporate Governance (chaired by the Chair).
- **Analytically significant governance gap:** there is **no dedicated board-level data-ethics/privacy committee.** For an enterprise whose entire franchise is the lawful processing of personal data across incompatible regimes, the absence of a standalone data/privacy board committee — with data-use decisions instead handled through management and the audit/risk apparatus — is a notable structural feature and, in this analyst's assessment, a governance weakness relative to the risk profile.
- The **UK Corporate Governance Code** applies despite Jersey incorporation. Executive pay is performance-linked to Benchmark EPS, organic revenue growth, ROCE and relative TSR.
- **Decision-rights map:** capital allocation and M&A → Board on management recommendation; data-use policy and permissible-use changes → management-led with board/risk oversight (no dedicated committee); new-jurisdiction entry → management/regional presidents with board sign-off on material commitments; pricing → business-line management; regulatory-enforcement response → CEO/CFO/General Counsel plus the relevant regional president and legal entity.

#### I.5 Legal Architecture

**Data furnisher agreements.** In the **UK**, lenders furnish account and performance data into closed user groups (Experian's **CAIS** database) under the **Principles of Reciprocity** administered by SCOR; access is conditioned on contribution — "you only get out what you put in." Over 350 million records relating to ~400 institutions are shared industry-wide. In the **US**, furnishing is voluntary but governed by FCRA §623 furnisher-accuracy duties and the CDIA **Metro 2** reporting format; network effects produce near-universal participation. In **Brazil**, furnishing of *negative* data is governed by the Consumer Defence Code, and of *positive* data by the Cadastro Positivo law (LC 166/2019), under which furnishers have a **statutory duty** to transmit data to accredited GBDs. The precise commercial terms of individual furnisher contracts are private and **UNKNOWN**.

**Scoring IP — FICO and VantageScore.** Experian distributes **FICO** scores licensed from Fair Isaac *and* co-owns **VantageScore Solutions, LLC** (formed 2006) equally with Equifax and TransUnion — a cooperative venture between three direct competitors to challenge FICO's incumbency. After the **FHFA authorised VantageScore 4.0 for Fannie Mae/Freddie Mac conforming mortgages on 8 July 2025** (FHFA projected "Up to Five Million Prospective New Buyers to Qualify"), FICO's VP/GM of B2B scores Julie May attacked the arrangement, stating "there can be zero meaningful competition in the conforming mortgage market until the credit bureaus divest their ownership in VantageScore," and FICO characterised the bureau-owned venture as "a de facto monopoly." This is a live competition-law flashpoint embedded in Experian's own IP portfolio.

**Litigation is structural, not incidental.** As a CRA, Experian Information Solutions, Inc. is a routine FCRA defendant in individual and class actions over accuracy, tradeline reinsertion, mixed files and dispute handling. The headline current matter is the **CFPB "sham investigations" suit** (see I.6).

**Legal-responsibility mapping (Follow-the-Legal-Entity):** FCRA bureau liability → Experian Information Solutions, Inc. (Ohio); UK data-protection and FCA liability → Experian Limited (Nottingham); Brazilian LGPD/Cadastro Positivo liability → Serasa S.A.; D2C consumer liability → ConsumerInfo.com, Inc.; group debt liability → issued by Experian Finance plc and guaranteed by Experian plc.

#### I.6 Regulatory and Data-Protection Architecture — PRIORITY DEPTH

**United States.** The **Fair Credit Reporting Act (FCRA, 15 U.S.C. §1681)** is foundational: permissible purpose, accuracy and reinvestigation duties (§611), furnisher duties (§623), adverse-action notices, consumer file access and security freezes. Since the **CFPB larger-participant rule (issued 16 July 2012, effective 30 September 2012)**, the big-three bureaux are federally supervised; the CFPB may seek restitution, disgorgement and civil penalties (historically up to ~US$1m/day for knowing violations). The **FTC** retains authority; **state AGs** and state statutes (California **CCPA/CPRA** and comparable laws) add a fragmenting overlay, together with state credit-freeze and (state-level) medical-debt rules. The **Gramm-Leach-Bliley Act** governs safeguarding.

*Enforcement trajectory has sharply reversed under the current federal administration.* In 2025 the CFPB **dismissed six credit-reporting enforcement actions** initiated 2021–2024, withdrew the interpretive rulemaking that would have classified data brokers as CRAs, and **joined industry in vacating the medical-debt rule** (the US District Court for the Eastern District of Texas vacated it on **11 July 2025** in *Cornerstone Credit Union League v. CFPB*, finding it exceeded the Bureau's authority and that the FCRA expressly permits use of coded medical-debt information — and that FCRA generally preempts contrary state laws). Crucially for Experian, however, the **"sham investigations" lawsuit remained on foot**: filed **7 January 2025** in the Central District of California against Experian Information Solutions, Inc., with then-Director Rohit Chopra stating, "When consumers disputed errors on their credit reports, Experian conducted sham investigations rather than properly reviewing the disputes as required by federal law." Experian called the suit "completely without merit." The tension is analytically important: rising consumer complaint volumes (the CFPB reported credit-reporting complaint submissions climbing from ~70,000 to over 460,000 per month between January 2023 and October 2025) coincide with a deregulatory enforcement posture — meaning the *class-action* channel, not the regulator, is now the principal FCRA enforcement mechanism.

**United Kingdom.** **UK GDPR + the Data Protection Act 2018**, enforced by the **ICO**; the **FCA** authorises CRAs. The ICO issued an **enforcement notice against Experian Limited on 27 October 2020** over Experian Marketing Services' processing of the data of "approximately 51 million UK adults" for direct marketing without adequate transparency/consent (Commissioner Elizabeth Denham: "Our investigation uncovered data protection failings that likely affected millions of adults in the UK"). Experian appealed. The **First-tier Tribunal (20 February 2023) substantially overturned** the notice, replacing it with a far narrower "Substitute Enforcement Notice," holding that legitimate interests could lawfully ground less-intrusive marketing and that Experian's CRAIN transparency notice was largely adequate — while agreeing Experian had unlawfully failed to notify ~5.3 million individuals whose public-source data it processed. The **Upper Tribunal dismissed the ICO's appeal on 23 April 2024**, and the ICO **declined to appeal further (May 2024)**. Net outcome: **Experian won decisively.** This is a landmark data-broking precedent and a rare, complete regulatory defeat for the ICO.

Separately, the **FCA Credit Information Market Study (CIMS)**: launched 2019 (following the Woolard Review), paused for COVID, interim report November 2022, **final report 3 December 2023 (MS19/1)**. The FCA found the existing self-governance body, **SCOR (the Steering Committee on Reciprocity), "too narrow" and "not fit for purpose"** and proposed replacing it with a broader, more accountable **Credit Reporting Governance Body (CRGB)**, supported by mandatory reporting requirements and a new common data format. An Interim Working Group was convened; the CRGB has since been incorporated; and the FCA published implementation consultation **CP26/7 in February 2026**. This is the single most consequential *structural* regulatory intervention for Experian's UK moat (see I.8).

**Brazil.** Serasa operates under the **LGPD** — with credit processing grounded in **Article 7(X), "protection of credit"** — the **Consumer Defence Code (Lei 8.078/90)** for negative data, and the **Cadastro Positivo law (Lei 12.414/2011, amended by LC 166/2019)**, which converted the positive registry from opt-in to automatic (opt-out) inclusion. Serasa estimated the positive registry could benefit ~137 million Brazilians (88.5% of adults). Serasa was **accredited by Banco Central do Brasil on 11 October 2019** as a positive-registry database manager (GBD); the **ANPD** is the data-protection authority; Banco Central supervises the positive-registry infrastructure.

**EU and other markets.** GDPR governs EMEA bureaux; APAC now includes illion (Australia/NZ). Experian has been rationalising smaller B2B operations in Latin America and EMEA/APAC (re-presented as exited activities in FY25–26).

**Cross-cutting.** AML/KYC identity-verification services (reinforced by the KYC360 acquisition) bring Experian into financial-crime regulation as a service provider; the decisioning/analytics businesses generally do not require separate licensing beyond the underlying data permissions.

**Enforcement & litigation table:**

| Date | Regulator/forum | Allegation | Outcome / penalty | Operating consequence |
|---|---|---|---|---|
| Mar 2017 | CFPB | Deceptive marketing of "educational" credit scores; ads shown before free-report disclosure (FCRA) | Consent order; **US$3m** civil penalty; prescribed disclosures | Changed D2C score-marketing practices |
| Sept 2015 → Nov 2022 | 40-state AG coalition | 2015 breach of ~15m T-Mobile applicants (Sept 2013–Sept 2015) | **US$12.67m** (Experian) + US$2.43m (T-Mobile); combined >US$16m; 5 years' credit monitoring; security undertakings | Data-security remediation; vendor oversight |
| 2019 | US class action (C.D. Cal.) | Same 2015 breach | Settlement incl. extended monitoring | — |
| Oct 2020 → Apr 2024 | ICO → FTT → Upper Tribunal | Unlawful data-broking / marketing use of ~51m adults' data | ICO notice **substantially overturned**; Experian wins; narrow residual notice on ~5.3m notifications | Marketing data-basis reforms; ceased consent-reliant suppliers |
| Jul 2018 → Feb 2019 | CMA | Anti-competitive acquisition of ClearScore | Parties abandoned; **CMA cancelled reference 27 Feb 2019** | Merger did not proceed |
| 7 Jan 2025 → (live) | CFPB (C.D. Cal.) | "Sham" dispute investigations; improper reinsertion; FCRA §611/§623 + CFPA unfair practices | **Litigation ongoing** as of mid-2026; Experian contests | Potential precedent on dispute-handling |

#### I.7 The Data-Rights Architecture — PRIORITY DEPTH (the institutional heart)

**Who contributes.** Banks, card issuers, telecoms, utilities, retailers, and public-record sources (electoral roll, county-court judgments, insolvency registers). Experian Information Solutions describes its US database as representing ~245 million credit-active consumers with ~1.3 billion updates flowing monthly.

**Why they contribute for free, and what they get.** In the **UK**, contribution is the *price of access*: SCOR's Principles of Reciprocity bind furnishers into closed user groups, and a lender that ceases contributing loses access to the equivalent shared data. Reciprocity is enforced contractually and by industry compliance exercises (SCOR-mandated questionnaires). In **Brazil**, positive-data furnishing is a *legal duty* under LC 166/2019 for accredited GBDs. In the **US**, furnishing is nominally voluntary but Metro 2 conventions and competitive parity produce near-universal participation. The consideration is symmetrical information: each furnisher gets a market-wide view of borrower behaviour it could never assemble alone.

**Legal basis to hold data, by jurisdiction.** US = FCRA statutory permissible-purpose regime; UK = UK GDPR **legitimate interests (Art. 6(1)(f))** for the bureau, with the **CRAIN** (Credit Reference Agency Information Notice) as the transparency mechanism — a basis the Tribunal litigation substantially validated for bureau (and less-intrusive marketing) processing; Brazil = LGPD Art. 7(X) plus the credit-specific statutes.

**Controller vs processor.** For the bureau databases Experian is a **data controller** (confirmed in the ICO Tribunal proceedings — the Tribunal agreed Experian was a controller regardless of whether it was labelled a "data broker"). For certain client-hosted decisioning/processing it acts as a processor; the marketing business is controller for its own compiled data.

**Consumer rights and the operating obligations they create.** Access; dispute/correction (FCRA §611 reinvestigation; UK GDPR Art. 16; Cadastro Positivo correction within 10 days); freeze/opt-out; and deletion where permitted. These rights generate enormous operating load — the entire CFPB 2025 suit is about the *dispute/reinvestigation* obligation, which is the single most operationally demanding consumer right for a bureau.

**What happens if a furnisher leaves.** Forward data flow stops; historical contributed data may generally be retained subject to statutory retention limits (e.g., ~6 years for UK defaults; FCRA §605 time-limits in the US). Precise contractual reversion/deletion terms are **UNKNOWN** (private contracts).

**Public-record vs furnished data.** Yes — these sit on a *different* legal footing. Public-record and electoral-roll data are collected under separate statutory/public-interest bases (the ICO case turned partly on the ~5.3m individuals whose *public-source* data Experian had not adequately notified), distinct from the reciprocity-governed furnished data.

**The central institutional question — what does Experian actually own?** Not the raw furnished data (held under permission). It owns: (a) the **aggregated database as a compiled work**; (b) the **derived attributes and bureau scores** it computes; (c) the **models** (and its one-third of VantageScore Solutions); and (d) the **identity-matching / linkage graph**. In one line: **Experian owns the refinery and the refined product, not the crude oil.** This is the deepest structural truth of the enterprise and is nowhere stated so plainly in its own disclosure.

#### I.8 Regulation as Barrier, Cost and Moat

Regulation functions as a genuine moat through three distinct mechanisms:

1. **FCRA/permissible-purpose compliance capability is genuinely hard to replicate.** The accuracy, reinvestigation, adverse-action and freeze machinery is expensive, litigation-tested and slow to build; it is a de facto licence to operate that a new entrant cannot shortcut. (The very existence of the CFPB dispute-handling suit shows how demanding — and how central — this capability is.)

2. **The reciprocity principle operates as a legally-sanctioned exclusion mechanism.** A new bureau cannot obtain contributed data without already having contributors — a chicken-and-egg barrier. The FCA examined this directly in CIMS and concluded SCOR was not fit for purpose *precisely because* it could entrench incumbents; the proposed CRGB and common data format are explicitly designed to lower this barrier. This is the clearest case in the study of a moat that is simultaneously a regulatory target.

3. **The CMA's readiness to block Experian/ClearScore reveals the enforcement geometry.** Competition authorities police the *consumer-facing* layer (free credit-checking, comparison platforms) aggressively while leaving the *underlying bureau oligopoly* largely intact — because the bureau layer's barriers are seen as structural/data-driven rather than merger-driven. The lesson: Experian will be blocked from consolidating the consumer layer, but its core bureau position is not currently contestable by a challenger.

**Assessment:** the regulatory moat is real and durable, but it is a **double-edged asset** — the same regulatory density that excludes entrants is the largest source of enforcement, litigation and legislative tail risk. It is best characterised not as pure incumbency advantage but as a *legally-constructed network barrier* that regulators can, and in the UK are actively trying to, dismantle at the margin.

#### I.9 Institutional Dependency Map

| Dependency | Function | Criticality | Substitutability | Concentration / bargaining power | Failure impact |
|---|---|---|---|---|---|
| Data furnishers (collectively) | Supply raw data | **Critical** | Very low collectively; high individually | Diffuse across ~hundreds of institutions; no single furnisher decisive, but the largest banks have real leverage | Coordinated withdrawal / reciprocity breakdown = existential |
| FCRA / regulatory licence to operate | Right to run a bureau | **Critical** | None | Regulator holds all power | Loss = existential |
| FICO | Score licensor **and** rival | High | Partial (VantageScore) | FICO strong in mortgage; frenemy dynamic | Margin/pricing pressure |
| VantageScore JV | Bureau-owned score | Moderate–High | n/a (co-owned) | Shared 1/3 control with Equifax/TransUnion | Competition-law exposure ("de facto monopoly" charge) |
| Cloud infrastructure | Compute/storage | High | Moderate | Migration substantially complete FY26 | Outage / cost shock |
| Public-record sources | Data inputs | Moderate | Low | Government-controlled | Coverage/quality gaps |
| Industry bodies (SCOR→CRGB, CDIA) | Governance of reciprocity | High | None | Being restructured by FCA | Access-rule change dilutes moat |
| Lenders/networks as customers | Revenue | High | Moderate | Concentrated top accounts (100% NA renewal in FY26 at higher values) | Revenue concentration risk |

**Single points of institutional failure:** (1) the integrity of the reciprocity/contributed-data network; (2) the FCRA licence/reputation of Experian Information Solutions, Inc.; (3) a catastrophic breach of the core bureau database (as opposed to the peripheral 2015 T-Mobile segment).

#### I.10 Tax and Intercompany Architecture

**Jersey incorporation** (no corporate income tax; company-law flexibility) combined with **Irish tax residence** (management and control exercised from Dublin) produces a group tax charge that the company states is "influenced by the nature of its income and expenditure and prevailing Irish and Jersey tax laws." The **Benchmark tax rate was 25.5% in FY26** (FY25: 25.3%), with FY27 guided to ~26% — i.e., a *rising*, mid-20s effective rate, which argues *against* reading the Jersey/Ireland structure as aggressive tax minimisation. Group debt is issued through Experian Finance plc (the old GUS shell), Experian Europe DAC and Experian Finance US, Inc., all **guaranteed by Experian plc**; brand, models and data are licensed intra-group with attendant transfer pricing. The most defensible interpretation is that the Jersey/Ireland/UK/US split is an **artefact of the 2006 demerger and the group's international footprint** — a legacy of listing a Jersey-incorporated vehicle while running the business from Dublin, Nottingham and Costa Mesa — rather than a tax-optimisation construct. No material disclosed tax dispute was identified in this review (UNKNOWN if any minor uncertain positions exist).

#### I.11 Corporate, Regulatory and Legal Risk Register

| Risk | Probability | Severity | Responsible entity | Mitigation | Residual |
|---|---|---|---|---|---|
| Major breach of **core** bureau database | Low–Medium | Very high | Experian Information Solutions / group | Post-2015 security investment; cloud migration; monitoring | High |
| CFPB FCRA action (**live**) | Occurring | Medium–high | Experian Information Solutions | Litigation defence; process reform | Medium |
| FCRA class-action exposure | High (continuous) | Medium | Experian Information Solutions | Reserves; dispute-process controls | Medium–High (now the primary enforcement channel given CFPB retreat) |
| ICO/EU data-protection enforcement | Low (post-2024 win) | Medium | Experian Limited | CRAIN transparency; legitimate-interests framework validated | Low–Medium |
| Adverse legislation removing data from the file (e.g., medical-debt-type exclusions) | Medium | Medium–high | Group | Diversification; lobbying; the 2025 vacatur reduced near-term US risk | Medium |
| SCOR→CRGB restructuring diluting reciprocity moat | Occurring | Medium | Experian Limited | Engagement with FCA/CRGB/IWG | Medium |
| LGPD/ANPD or Banco Central enforcement | Low–Medium | Medium | Serasa S.A. | Compliance programme; Central Bank accreditation | Medium |
| Structural **B2B–D2C conflict** | Standing | Reputational | Group | Entity separation; "financial-health" narrative | Medium |
| US state-privacy fragmentation | High | Medium | US entities | Compliance overhead; FCRA-preemption arguments | Medium |
| Furnisher withdrawal / reciprocity failure | Low | Very high | Group | Legal duties (Brazil); network lock-in (UK/US) | Medium |
| Reputational damage impairing D2C trust | Medium | Medium | ConsumerInfo.com | Brand/security investment | Medium |

**The breach history in full.** The **2015 T-Mobile incident** is the defining event: an unauthorised actor accessed an Experian network segment holding personal data (names, addresses, dates of birth, SSNs, government IDs) of **~15 million** T-Mobile postpaid/device-financing applicants from September 2013 to September 2015. A **40-state AG coalition** settled in November 2022 for **~US$12.67m from Experian** plus US$2.43m from T-Mobile (combined >US$16m), with five years' extended credit monitoring and security undertakings; a 2019 consumer class action had earlier settled with two years' monitoring. Critically, **neither Experian's core consumer-credit database nor T-Mobile's own systems were compromised** — the breach was of a client-processing segment, which is why it did not become an Equifax-scale existential event. Some settlements reference companion 2012 incidents.

**The B2B vs D2C tension.** Experian sells consumer data to lenders (B2B, principally via Experian Information Solutions) *and* sells credit monitoring and identity protection to consumers (D2C, via ConsumerInfo.com — over 215 million free members globally, monetised through premium subscriptions and marketplace referrals). This is a genuine structural conflict — the company profits from the market whose risks it then sells consumers protection against — managed through legal-entity separation and a "help consumers improve their financial health" narrative. It is a standing reputational risk that would be amplified by any future breach or adverse enforcement.

#### I.12 Volume I Reconstruction

**(1) Corporate Entity Diagram (economically-important core):**
Experian plc (Jersey/Ireland, listed, guarantor) → [Experian Finance plc (UK, ex-GUS, debt) | Experian Group Limited / Experian Holdings Limited (UK holdcos) | Experian Holdings, Inc. (US holdco)] → operating layer: Experian Limited (UK bureau, FCA) · Experian Information Solutions, Inc. (US FCRA bureau, Ohio) · ConsumerInfo.com, Inc. (US D2C, CA) · Experian Marketing Solutions, LLC (US, DE) · Experian Health, Inc. (US) · Serasa S.A. (Brazil, ~99.6%).

**(2) Simplified group structure:** one listed Jersey parent; a thin band of UK/US/Irish holding and finance entities; a set of ring-fenced national operating bureaux and product companies.

**(3) Ownership and control:** widely held, one-share-one-vote, no controlling shareholder; largest holder BlackRock ~5.9%; control effectively with management + dispersed institutions; removable by ordinary vote.

**(4) Governance/decision-rights:** Board (Chair Rogers→Crozier 2026; CEO Cassin; CFO Pitchford) with Audit/Remuneration/Nomination committees; **no dedicated data/privacy committee**; capital allocation and M&A at Board; data-use at management.

**(5) Multi-jurisdiction regulatory map:** US (FCRA + CFPB larger-participant + FTC + state AGs/CCPA/GLBA); UK (UK GDPR/DPA 2018 + ICO + FCA/CIMS + SCOR→CRGB); Brazil (LGPD + Cadastro Positivo + Banco Central + ANPD); EU/APAC (GDPR; illion in AU/NZ).

**(6) Data-rights architecture:** contributed data held under statutory permission (FCRA/LGPD) and contractual reciprocity (SCOR); Experian is controller of the bureau databases; owns the aggregation, attributes, scores and models — not the raw data.

**(7) Enforcement/litigation table:** see I.6 (2017 CFPB US$3m; 2015 breach ~US$16m; ICO 2020–24 Experian win; CMA/ClearScore abandoned 2019; CFPB 2025 live).

**(8) Legal-responsibility map:** FCRA → Experian Information Solutions; UK data/FCA → Experian Limited; Brazil → Serasa S.A.; D2C → ConsumerInfo.com; debt → Experian Finance plc / Experian plc guarantee.

**(9) Institutional dependency map:** furnishers (Critical); FCRA licence (Critical); FICO/VantageScore (High); cloud (High); industry bodies (High).

**(10) Tax/intercompany map:** Jersey inc. + Irish residence; debt via Experian Finance plc/Europe DAC/US Inc. under Experian plc guarantee; ~25.5% Benchmark tax rate, rising.

**(11) Chronological corporate evolution:** 1980 CCN → 1996 TRW merger/Experian brand → 2006 demerger (GUS shell → Experian Finance plc) → 2007/2012 Serasa → 2020–25 identity/fraud/APAC build-out.

**(12) Regulation-as-moat assessment:** real and durable but double-edged; reciprocity is a legally-constructed network barrier the FCA is actively trying to loosen.

**(13) Top corporate/legal/regulatory risks:** core-database breach; live CFPB suit; FCRA class actions (now the primary enforcement channel); reciprocity restructuring; B2B–D2C conflict.

**(14) Key unknowns:** individual furnisher contract terms; Serasa's exact current ownership % and CNPJ; states of incorporation of Experian Holdings Inc., ConsumerInfo.com and Experian Health; any minor uncertain tax positions.

**(15) Ten most important conclusions:**
1. Experian is a listed information utility, not a data owner — it holds others' data under permission and owns the aggregation.
2. The Jersey-inc./Irish-resident/Dublin-HQ/Nottingham+Costa Mesa split is confirmed and foundational; the operational centre of gravity is North America.
3. Experian Finance plc *is* the old GUS/Great Universal Stores shell — the retailer's corpse is the group treasury.
4. The most strategically important entity is Experian Information Solutions, Inc. (Ohio), the US FCRA bureau and profit centre.
5. Control is genuinely contestable in law but practically management-led over a dispersed institutional register; no controlling bloc.
6. The reciprocity principle is both moat and regulatory accident — and the FCA is dismantling its governance (SCOR→CRGB).
7. Regulation is Experian's deepest barrier to entry and its largest tail risk simultaneously.
8. The CFPB's 2025 enforcement retreat shifts FCRA enforcement onto the class-action channel — raising, not lowering, private litigation salience.
9. Experian largely *won* its ICO fight — a rare, complete data-broking regulatory defeat for the regulator — validating legitimate interests for bureau/marketing processing.
10. The B2B–D2C conflict (selling data to lenders and protection to consumers) is a permanent, managed reputational fault line.

**Direct answers to the closing questions:**
- **Most strategically important legal entity:** Experian Information Solutions, Inc. (Ohio) — the US FCRA bureau generating the majority of group profit.
- **Where actual control sits:** with executive management, legitimised by a dispersed long-only institutional register; no controlling shareholder; removable by ordinary vote.
- **Greatest constraint / greatest protection:** the FCRA/CFPB regime is both — the largest single constraint (litigation, dispute-handling burden) and, via the barrier to entry, the greatest protection.
- **What Experian actually owns:** the refinery and refined product — the aggregated database as a compiled work, derived attributes and scores, the models (and its third of VantageScore) and the identity graph — not the raw furnished data.
- **Most dangerous dependency:** the integrity of collective furnisher participation / reciprocity.
- **Reciprocity — moat or accident?** Both: a self-regulatory settlement that hardened into a legally-sanctioned entry barrier, now being restructured by the FCA.
- **Most misunderstood by outsiders:** the belief that Experian "owns your data"; in law it holds others' data under permission and owns the aggregation and models.
- **What a well-funded entrant could and could not build today:** it could build the data centre, cloud stack and even the scoring models within a few years; it could *not* quickly assemble the contributed-data network under reciprocity (near-impossible in the UK without a regulatory mandate) or the litigation-tested FCRA-compliance apparatus. The legally-permissioned data network — not the technology — is what takes longest and is, in the UK, effectively legally impossible to replicate from zero.

---

### Recommendations
1. **Track the CFPB *Experian* litigation (C.D. Cal., filed 7 Jan 2025) as the near-term binary.** An adverse judgment or settlement would set FCRA dispute-handling precedent for the whole industry and invite copy-cat class actions; a dismissal (plausible given the CFPB's 2025 posture reversal) would materially de-risk the sector. *Threshold that changes the view:* any dispositive ruling or a settlement figure disclosed as material.
2. **Watch the SCOR→CRGB transition and FCA CP26/7 (2026).** Mandatory reporting and a common data format could erode the reciprocity moat. *Benchmark to monitor:* whether the CRGB opens data access to thin-contribution new entrants — the single most important indicator of moat durability in the UK.
3. **Monitor VantageScore 4.0 conforming-mortgage adoption post-FHFA (8 Jul 2025).** A genuine shift in scoring economics and a competition-law flashpoint (FICO's "de facto monopoly" charge). *Threshold:* any DOJ/FTC or private antitrust action targeting bureau ownership of VantageScore.
4. **For counterparty due diligence, always contract with the correct legal entity:** FCRA obligations attach to Experian Information Solutions, Inc. (Ohio); UK data/FCA obligations to Experian Limited; Brazilian obligations to Serasa S.A.; debt exposure to Experian Finance plc under the Experian plc guarantee. Do not treat "Experian" as a single contracting counterparty.
5. **For Volume II (do not begin here):** carry forward the unresolved entity-registration items and the furnisher-contract terms as the priority primary-source targets (Irish CRO, Ohio SoS, California SoS, Serasa CNPJ via Receita Federal).

### Caveats
- Individual **furnisher contract terms**, **Serasa's exact current ownership percentage and CNPJ**, and the **states of incorporation of Experian Holdings Inc., ConsumerInfo.com and Experian Health** are **UNKNOWN/UNVERIFIED** from public sources and are labelled as such above; the 99.6% Serasa figure is the last publicly verified level (2012) and may since be higher.
- Financial figures are FY26 (year to 31 March 2026) on the bases labelled; **statutory and Benchmark measures are not mixed** in any single comparison.
- The **US CFPB enforcement posture is in flux** as of mid-2026; statements about 2025 dismissals and the medical-debt-rule vacatur reflect actions taken in 2025 and remain subject to appeal and legislative change.
- Some corporate-history dating (e.g., the exact 1996 sequencing of the TRW spin-out and GUS purchase, and pre-1980 pre-history) relies on secondary business-history sources and is corroborated where possible against Experian's own "Our history" disclosure; the PE-backer detail (Bain Capital, Thomas H. Lee) is from a reputable company-history source rather than a primary filing.
- This is a standalone Volume I on Experian; structural contrasts with EREF Subjects I–III (Wise, Atruvia, DZ BANK) are noted only where analytically useful. **Volume II has not been started.**


---

# Part II — Product, the Three-Sided Customer Structure & the Inverted Value Flow

### Product, the Three-Sided Customer Structure & the Inverted Value Flow

*Basis discipline: Experian reports under IFRS in US dollars with a 31 March financial year end. FY26 = year ended 31 March 2026. Benchmark and statutory figures are labelled throughout and never mixed. "Ongoing activities" excludes the B2B lines re-presented as exited from FY26. Evidence tags: CONFIRMED FACT / COMPANY CLAIM / THIRD-PARTY ESTIMATE / ANALYTICAL INFERENCE / UNKNOWN.*

---

### TL;DR
- **Experian's true core product is not data but a permissioned network position no single participant could occupy alone.** It sits between ~245m credit-active US consumers, ~400 UK institutions, and ~100m Brazilians, receives its raw material free from the same institutions that later buy the finished product back, and monetises the resulting aggregation, identity graph, derived attributes and models. In FY26 it converted **US$8,425m** of ongoing revenue into a **28.6% Benchmark EBIT margin** off a core input carrying essentially zero procurement cost.
- **The three-sided customer structure is real and concentrated.** A large bank is simultaneously a **data furnisher** (supplies data free), a **data buyer** (pays per pull for reports/scores/attributes/decisioning) and a **marketplace advertiser** (pays to be shown to pre-qualified consumers). Reciprocity — you can only draw out what you contribute — is the disciplining mechanism that both locks furnishers in and caps Experian's raw-material bargaining exposure.
- **The consumer is monetised three ways at once (B2B data sale, D2C subscription, marketplace referral) and is both customer and product.** The marketplace has overtaken subscriptions as the primary consumer growth driver, which sharpens rather than resolves the conflict of interest. The live CFPB "sham investigations" suit (filed 7 January 2025; motion to dismiss denied 22 October 2025; discovery ongoing) targets exactly the dispute machinery that is both Experian's largest consumer-facing cost and its principal legal exposure.

---

### Key Findings

1. **FY26 revenue architecture (Benchmark, ongoing, US$m) [CONFIRMED FACT]:** B2B **US$6,168m** (Financial Services **US$4,463m** + Verticals **US$1,705m**) and Consumer Services **US$2,257m**, for **US$8,425m** total. By region: North America **US$5,587m**, Latin America **US$1,297m**, UK & Ireland **US$942m**, EMEA & Asia Pacific **US$599m**. North America is **66.3%** of ongoing revenue (5,587/8,425).
2. **Margin geography [CONFIRMED FACT]:** Benchmark EBIT by region — North America **US$1,912m (34.2% margin)**, Latin America **US$399m (30.8%)**, UK & Ireland **US$220m (23.4%)**, EMEA/AP **US$40m (6.7%)**, less **US$164m** central costs = **US$2,407m (28.6%)**. By line: B2B **US$1,903m (30.9%)**, Consumer Services **US$668m (29.6%)**. North America is where the free-input-to-margin conversion is most complete.
3. **The inverted value flow is the central mechanism [ANALYTICAL INFERENCE from confirmed mechanics]:** the furnisher reports at its own cost under Metro 2 (US) / CAIS (UK) and receives no cash; the same or another lender later pays per pull. COGS is therefore not raw material but matching/identity resolution, database operations, model development, compliance and — materially — dispute handling.
4. **Triple monetisation confirmed by the company's own model page [CONFIRMED FACT]:** Consumer Services revenue is generated through "Premium subscriptions," "Marketplace referral and performance-based fees," "Financial product origination partnerships" and "Value-added protection services." Management stated marketplace (credit cards, personal loans, insurance) was a key driver of FY26 consumer growth.
5. **Pricing power sits with Experian on the buy side but is capped by reciprocity and, in mortgage, complicated by FICO.** Per the Community Home Lenders of America (CHLA), via HousingWire (April 2026), *"total credit report costs associated with closing a conventional loan have risen from about $50 in 2022 to roughly $540 in 2026,"* while *"the base price charged by FICO for a tri-merge credit report has increased from $1.80 in late 2022 to $30 in 2026 — a more than 1,500% increase over four years."* FICO's wholesale royalty is **US$4.95/score** and, per FICO EVP Jim Wehmann, *"all amounts above $4.95 per score are collected and retained by the credit bureaus or their tri-merge resellers—not FICO"* (the traditional wholesale channel still averages ~US$10/score). Experian's own mortgage revenue grew **45% in FY26 on roughly flat volumes** — a pure pricing effect.
6. **The consumer product is a genuine business but the "financial health" framing does not survive contact with the mechanics.** The consumer whose data is sold has no contract with the buyer and receives no payment; per Experian's own Boost page *"most people get an instant increase in their FICO® Score by an average of 13 points"* — but only under the FICO Score 8 model and only to the Experian file, which many mortgage/auto models do not use.
7. **Serasa is a national platform in its own right [CONFIRMED FACT]:** ~100m Brazilians in its base, ~75.7m negativados (March 2025), and Limpa Nome renegotiated **US$19.4bn** of consumer debt in FY26 across a creditor-paid marketplace of 2,200+ partner companies; the consumer pays nothing and Serasa is paid by creditors on recovery — the exact fee rate is UNKNOWN.

---

### Details

#### II.1 Product Universe — decomposed by manufacturing entity and legal basis

Experian's portfolio is best understood as concentric rings around a single regulated asset — the bureau file — with each outer ring progressively less regulated and more contestable. Each family below is tagged by manufacturing legal entity, legal basis and classification (regulated-bureau / adjacent-analytics / marketing / consumer-subscription / marketplace / infrastructure).

**A. Core bureau (B2B) — regulated-bureau.** Manufactured by **Experian Information Solutions, Inc.** (US, the FCRA "consumer reporting agency" and the group's principal profit centre) and **Experian Limited** (UK, FCA-authorised, operating the CAIS bureau). Products: consumer credit reports; credit scores (FICO under distribution licence; VantageScore as co-owner); bureau attributes and trended data (2,100+ credit attributes on Ascend; ~6,000 predictive attributes when cashflow data is blended, per FY26 disclosure, enabling *"up to a 25% uplift in predictive performance when combined with traditional credit data"*); prescreen / pre-qualification files; account review and portfolio monitoring; collections triggers; alerts. Legal basis: FCRA "permissible purpose" (US); UK GDPR Article 6(1)(f) legitimate interests with CRAIN transparency (UK); LGPD Art. 7(X) + Cadastro Positivo law (Brazil). Job: assess and monitor borrowers. Pricing: per-inquiry, tiered by volume (largely confidential — UNKNOWN at list). This is the prerequisite product on which everything else depends.

**B. Analytics and decisioning — adjacent-analytics/infrastructure.** Manufactured through **Experian Software Solutions (ESS)** and regional decision-analytics entities. The **Ascend** family — Ascend Platform (**2,300+ client solutions implemented, 37 product capabilities provisioned globally** per FY26), Ascend Intelligence Services (custom AI/ML model build), Ascend Ops, the Ascend Sandbox — plus **PowerCurve** decisioning software (originations, customer management, collections; now interoperating with Ascend and carrying the "Experian Assistant" GenAI / AIVA layer). Legal basis: contractual (software/SaaS licensing); where bureau data flows through, FCRA/GDPR bases attach. Job: let a mid-market lender deploy models that only the top banks could previously afford; the company claims model build cut "from months to days." Pricing: subscription/platform + consumption (confidential — UNKNOWN). Classification: infrastructure that is bureau-dependent for data but is itself a software business.

**C. Fraud and identity — adjacent-analytics.** **CrossCore** (identity/fraud orchestration platform), **Precise ID** (identity verification and fraud scoring), device intelligence, **NeuroID** (behavioural analytics — keystroke/mouse/typing cadence, acquired 2024), **ClearSale** (Brazil transactional/e-commerce fraud, completed 1 April 2025), **KYC360** (UK/Ireland RegTech/AML, October 2025), and **AtData** (email identity, 10bn+ addresses, October 2025). Legal basis: fraud-prevention legitimate interest / substantial public interest; not a consumer-report use unless a bureau pull is involved. Job: verify identity and stop fraud at onboarding and transaction. Experian claims its identity/fraud solutions helped clients avoid ~US$15bn in fraud losses globally in a year [COMPANY CLAIM]. Pricing: per-transaction/per-check.

**D. Marketing services — marketing.** Manufactured by **Experian Marketing Solutions, LLC** (US) and Experian Limited's marketing unit (UK). Assets: audience segmentation (ConsumerView-type products), identity resolution via the **Experian Graph** (signal-agnostic, supporting UID2/ID5), **Tapad** (cross-device probabilistic graph, ~US$280m, 2020), **Audigent** (data curation/SmartPMPs, December 2024) and **AtData** (email). Clean-room / data-collaboration ("Consumer Sync"). **Critical legal distinction:** marketing use is *not* permitted under FCRA permissible purpose and *not* under the credit-bureau data-sharing reciprocity; in the UK it runs on UK GDPR legitimate interests for the marketing data set specifically — **the precise point litigated in the ICO case**. The ICO's October 2020 enforcement notice attacked exactly this "invisible processing"; the First-tier Tribunal (20 February 2023) and Upper Tribunal (23 April 2024) largely upheld Experian, confirming legitimate interests can support large-scale direct-marketing processing — but also that data originally collected on a *consent* basis cannot be "flipped" to legitimate interests. The FTT found the Information Commissioner *"did not properly appreciate the limited extent to which CRA data was used."* Classification: marketing; must be firewalled from the credit file.

**E. Experian Health — infrastructure (healthcare RCM).** Manufactured by **Experian Health, Inc.** Patient identity, insurance eligibility verification, claims management (ClaimSource), denials prediction (AI Advantage), Patient Access Curator (PAC, ~30% average denial reduction claimed), collections optimisation, patient payment estimates. Company metrics [COMPANY CLAIM]: US$4.9bn annual collections facilitated, 2,700 payer connections, 175m claims processed, US$3.2bn+ annual eligibility transactions cleared. **Why a credit bureau owns this:** the shared asset is *identity resolution and data-matching infrastructure*, not credit data — Experian is applying the same matching/attribute engine to a different data domain (payer coverage) where it does not share the consumer credit file. This is infrastructure reuse, not credit-data cross-use.

**F. Automotive — adjacent-analytics/marketing.** **AutoCheck** vehicle history (per FY26, now *"the exclusive vehicle history report provider across almost every major consumer shopping site in the USA"*), plus automotive credit, value-recovery and marketing data. Legal basis: mixed (public/DMV records, FCRA where credit is involved).

**G. Business information — regulated/adjacent.** Commercial credit reports, small-business risk scores, commercial bureau (US/UK/Brazil/illion). Legal basis: commercial data is largely outside FCRA/consumer-GDPR constraints (business data), though sole-trader data blurs the line.

**H. Direct-to-consumer — consumer-subscription + marketplace.** Manufactured by **ConsumerInfo.com, Inc. dba Experian Consumer Services** (US, Costa Mesa) and Experian Limited (UK). Free membership (215m+ globally); premium subscriptions — CreditWorks Premium (**US$24.99/mo** after a US$4.99 first month) and IdentityWorks Premium (**US$24.99/mo**) / Family (**US$34.99/mo**), including tri-bureau monitoring, dark-web scanning, up to **US$1m** identity-theft insurance and CreditLock; **Experian Boost** (free; adds utility/telecom/rent/streaming payments to the Experian file, ~13-point average FICO Score 8 uplift); **Experian Go** (credit-invisible file establishment; 15,000+ in pilot); the **marketplace** (credit cards, personal loans, insurance via Gabi, and now mortgage via **Own Up**); and in the UK **CreditExpert** (paid) and **CreditMatcher** (free marketplace). Legal basis: direct consumer contract (subscription T&Cs); marketplace referrals on consumer consent. Classification: subscription + marketplace.

**I. Serasa Experian consumer (Brazil) — consumer-subscription + marketplace.** Manufactured by **Serasa S.A.** (~99.6% owned). The five distinct consumer products: (1) **Serasa Score** (0–1,000; Cadastro Positivo data carries ~55% of the calculation weight per Serasa); (2) **Limpa Nome** (debt-renegotiation marketplace — see II.6); (3) **Serasa Premium** (CPF monitoring, consultation-blocking, alerts); (4) **Serasa Cadastro Positivo** (the positive-registry enrolment and management, Banco Central-accredited since 11 October 2019); (5) the **Serasa app / eCred marketplace** (credit matching). Legal basis: LGPD Art. 7(X) + Cadastro Positivo law (Lei Complementar nº 166/2019, automatic inclusion). Scale: ~100m Brazilians in base [THIRD-PARTY ESTIMATE, Exame].

**J. illion (Australia/NZ) — regulated-bureau + adjacent.** Consumer and commercial credit registries; **BankStatements** (bank-transaction retrieval, 47m+ transactions weekly from 2.7m+ individuals, 5,000+ customers incl. 750+ lenders); Open Data Solutions (CDR/open-banking, 140+ AU banks, 20+ NZ); illion Decisioning; Authenticate (fraud); Company360 (commercial). Acquired 2024 (~A$820m). Legal basis: Australian Privacy Act / CDR; NZ equivalents.

#### II.2 The Three-Sided Customer Structure (replaces segmentation) — PRIORITY

The defining feature of Experian's counterparty base is **role superimposition**: the same institution frequently occupies all three roles at once.

**(a) Data furnishers** — banks, card issuers, auto lenders, telecoms, utilities, retailers, debt collectors, and public-record sources. They supply account and performance data at their own cost (Metro 2 in the US, CAIS in the UK) and receive *no cash*. What they receive instead is **reciprocal access**: under the SCOR Principles of Reciprocity (UK) — being replaced by the new Credit Reporting Governance Body following the FCA Credit Information Market Study, with implementation consultation CP26/7 (February 2026) — a furnisher can only *draw out* the data categories it *contributes*. In the US the discipline is contractual and regulatory rather than a single reciprocity code, but the economic effect is the same. Concentration: the furnisher base is broad (US ~1.3bn updates monthly; UK ~350m records across ~400 institutions industry-wide), so no single furnisher is individually decisive — this diffusion is precisely what protects Experian from raw-material hold-up [ANALYTICAL INFERENCE].

**(b) Data buyers** — lenders, insurers, telecoms, landlords, employers (where FCRA-permitted), healthcare providers, government, debt collectors and fintechs. Financial Services (US$4,463m, just over half of group revenue) is the dominant buying vertical. A large share of the buying base is *also* furnishing — the essential overlap. Contract structure: enterprise master agreements with permissible-purpose certification, per-inquiry pricing with volume tiers, multi-year terms (North America FY26: **100% renewal** among top strategic financial-services accounts, contract durations extended ~10% to over four years, contract values up double-digits — CONFIRMED FACT).

**(c) Marketplace advertisers** — lenders and insurers who pay Experian (via performance/referral fees) to be shown to consumers Experian has pre-qualified using bureau data. This is the newest role and, per management, the primary driver of FY26 consumer-services growth.

**Consequences — where bargaining power actually sits.** When a bank is supplier, customer and advertiser simultaneously, the relationship is a repeated, multi-dimensional game rather than a simple buy/sell. Experian's pricing power on the *buy* side is real (evidenced by the 45% mortgage-revenue jump on flat volume and double-digit renewal uplifts) because (i) the tri-merge structure forces lenders to buy from all three bureaus — they cannot substitute one for another — and (ii) switching costs are high (integration, model re-validation). But that power is **capped by reciprocity**: Experian cannot squeeze a furnisher so hard that it degrades or withdraws its data contribution, because the contribution is what makes the file saleable to everyone else. Reciprocity therefore functions as an implicit price-discipline mechanism — the network only works if the largest contributors stay in, so their effective "payment" (free data) is protected by their strategic indispensability. **Analytical inference:** the true locus of power is the *network itself*; neither Experian nor any single bank controls it, which is why the answer to "who has pricing power when the buyer is also the supplier" is "the network position, arbitrated by the reciprocity rules."

#### II.3 Jobs to Be Done

**Lenders:** assess new applicants; monitor existing books (account review); find and pre-qualify prospects (prescreen); comply with affordability/creditworthiness rules (UK Consumer Duty, US ability-to-repay); detect fraud and verify identity; price risk. What they are *actually* buying is not "data" but **a defensible, auditable, regulator-acceptable basis for a lending decision** — the permission and the explainability as much as the number.

**Consumers:** understand and improve a score; access credit; protect against identity theft; find a better product; in Brazil, clear a default and exit the *negativado* state. **Conflict:** the consumer's job ("get me approved / clear my name / pay less") is partly *adverse* to the lender's job ("price my risk accurately / decline me if risky"). Experian sells to both sides of this conflict — the same bureau file that helps a lender decline a consumer is sold back to that consumer as "monitoring," and then the consumer is referred back to lenders for a fee.

**Other buyers:** insurers (risk-based pricing, where permitted); telecoms (thin-file onboarding decisions); employers (FCRA-permitted background/employment screening); healthcare providers (identity and coverage, via Experian Health — *not* credit data); landlords (tenant screening).

#### II.4 The Customer Journey — traced separately

**B2B:** prospect → contract and permissible-purpose certification → technical integration (API/platform onboarding; the highest switching-cost step) → first inquiry → ongoing usage and cross-sell (bureau → attributes → scores → Ascend → fraud) → renewal. FY26 evidenced very high stickiness: 100% North America strategic renewal, longer durations, higher values, and Ascend embedded across the largest institutions (a multi-year ServiceNow partnership, using Model Context Protocol, extends reach beyond financial services). Sales cycle for enterprise is long (months to quarters); integration burden and model-revalidation cost create the switching moat.

**Consumer:** acquisition (free sign-up, often via Boost or a free-score offer) → identity verification (Go uses government ID + selfie) → free score/report and alerts → engagement (EVA virtual assistant, ~3.5m engagements since launch) → **either** upgrade to premium subscription **or** monetisation via marketplace referral. **Funnel economics [ANALYTICAL INFERENCE; company does not disclose paid-conversion rates]:** with 215m free members and Consumer Services revenue of US$2,257m, blended annual revenue per free member is ~US$10.5 (2,257 ÷ 215) — but this is dominated by a small paid/marketplace-active cohort; the vast majority of free members generate little or no direct revenue and exist as *marketplace inventory* and *consented-data supply*. This is the clearest evidence that the free member is the product, not the customer.

#### II.5 The Inverted Value Flow (replaces money-movement) — PRIORITY

Trace one unit of data:

- **(a) Data inflow:** Lender A reports Consumer X's account + performance to Experian under Metro 2 (US) / CAIS (UK), *at Lender A's own cost*, receiving no cash. Permission: statutory + reciprocity.
- **(b) Processing:** Experian matches the record to X's identity (the hard, value-adding step), appends it to the file, derives attributes and trended variables, and computes scores (FICO/VantageScore). **This is where Experian's proprietary ownership begins** — it does not own the raw tradeline, but it owns the aggregation, the attributes, the identity graph and the models. (FY26: *"Over 90% of our revenue is derived from proprietary data."*)
- **(c) Data outflow:** Lender B (or Lender A) pulls a report/score on X and **pays per pull**.
- **(d) Money flow:** cash flows *only* at outflow. There is **no procurement cost for the core input** — the defining inversion. The furnisher's "payment" is reciprocal access, an in-kind exchange that never touches the P&L as a cost of goods.
- **(e) Permission flow:** each pull requires a permissible purpose (US FCRA) or a lawful basis (UK GDPR), certified by the puller; Experian polices this contractually and via audit.
- **(f) Liability flow:** if the data is wrong, the **furnisher** is liable under FCRA §623 (accuracy of what it reports and its duty to investigate) and the **bureau** under FCRA §611 (its own reinvestigation duty). Liability is *joint and split* — the crux of the CFPB case (II.6/II.12).

**The central economic question — if the raw material is free, what is COGS and where is the margin?** Since there is no raw-material cost, gross margin is a function of the cost of *manufacturing the file and defending it*. Decomposition of the cost base [ANALYTICAL INFERENCE; Experian does not publish a COGS bridge]:
1. **Matching and identity resolution** — the single most value-additive cost; bad matching creates mixed files and litigation.
2. **Database operations / cloud** — now largely migrated to cloud (North America and Brazil substantially complete ex-Health), with dual-run costs falling from FY27, i.e. this cost is declining.
3. **Model development** — FICO royalties (a *pass-through cost* on score sales — US$4.95/score wholesale in mortgage) plus internal VantageScore/attribute R&D.
4. **Compliance and dispute handling** — the FCRA §611 reinvestigation machinery; both a legal obligation and, per the CFPB suit, a contested cost centre. **Analytical inference: dispute handling is a material share of the consumer-facing cost base** — the CFPB alleges Experian under-invests in it precisely because it is a cost with no direct revenue.
5. **Distribution** — API/platform, resellers, sales.

FY26 group labour cost was **32% of revenue** (over 300bps lower than two years earlier, per management — a productivity/AI effect). The 28.6% group Benchmark EBIT margin (34.2% in North America) is therefore best read as: **a near-zero-input-cost information asset, taxed mainly by the cost of accuracy, compliance, labour and distribution.** The margin comes from the *network position and the derived IP*, not from any transformation of purchased inputs.

#### II.6 Transaction Teardown

**US credit-card application:** Applicant applies → issuer pulls Experian report + score under permissible purpose "credit transaction initiated by the consumer" → decision → if declined, FCRA adverse-action notice citing the CRA and key factors → a **hard inquiry** is recorded on the file (a data artefact that itself slightly lowers the score). System: Experian Information Solutions, Inc. Failure mode: wrong-person match, stale tradeline, or an inquiry the consumer disputes.

**UK affordability assessment:** Lender combines CAIS bureau data with Open Banking transaction data (categorised income/expenditure) to satisfy Consumer Duty affordability. Entity: Experian Limited. Legal basis: legitimate interests + consumer consent for Open Banking. Failure mode: mis-categorised transactions producing a false affordability read.

**Prescreen / pre-qualification campaign:** Lender specifies criteria → Experian returns a list of pre-qualified consumers (permissible purpose: "firm offer of credit") → the firm-offer-of-credit obligation attaches (the lender must honour the offer to those who meet the pre-set criteria). This is the B2B twin of the consumer marketplace.

**Consumer dispute (the CFPB transaction):** Consumer disputes a tradeline → Experian must, under FCRA §611, conduct a reasonable reinvestigation within 30 days → it forwards the dispute to the furnisher, which must investigate under §623 → outcome reported back. **What the CFPB (complaint filed 7 January 2025, C.D. Cal., against Experian Information Solutions, Inc.) alleges Experian does wrong:** (i) *"sham investigations"* — faulty intake that does not accurately convey all relevant dispute information to the furnisher, and failure to pass consumer-submitted documentation to furnishers; (ii) *uncritical deference* — routinely accepting the furnisher's response *"even when that response was improbable or illogical on its face,"* or when Experian has other information suggesting the furnisher is unreliable; (iii) *defective result notices* — sending consumers notices that are *"confusing, ambiguous, incorrect, or internally inconsistent"*; (iv) *improper reinsertion* — failing to implement basic matching tools, so a previously deleted inaccurate tradeline reappears under a new furnisher's name. Director Rohit Chopra: *"When consumers disputed errors on their credit reports, Experian conducted sham investigations rather than properly reviewing the disputes as required by federal law."* The CFPB pleads both FCRA violations and the CFPA prohibition on unfair acts/practices, and seeks injunctive relief, redress and a civil money penalty. **Case status:** the court **denied Experian's motion to dismiss the second amended complaint on 22 October 2025**; Experian answered on 3 November 2025; **discovery is ongoing**. Experian calls the suit "without merit." **This is the failure path that is simultaneously a legal duty, a cost centre and live federal litigation.**

**Limpa Nome renegotiation (Brazil):** Consumer checks CPF free on the Serasa app/site/WhatsApp → sees discounted settlement offers (up to 90%, up to 99% during the Feirão) from 2,200+ creditors → selects and pays via Pix/boleto (Serasa intermediates payment through its payment institution, PagueVeloz) → creditor requests removal of the negativação within five business days. **Who pays Experian and how much:** the *consumer pays nothing* to Serasa (only the negotiated debt to the creditor); Serasa is paid by the **creditor** on a credit-recovery basis (the platform is marketed to creditors as turning *"inadimplência into receita"*). The **exact commission/success-fee rate is not publicly disclosed — UNKNOWN.** Scale [CONFIRMED FACT / COMPANY CLAIM]: *"Limpa Nome, our debt renegotiation business, continues to help millions of consumers, with US$19.4bn of consumer debt renegotiated in FY26"*; Experian's financial-health page states 14 million people in Brazil used the portal to renegotiate ~US$19.5bn in FY26; 30m+ credit agreements renegotiated in Latin America in the year; 600m+ debts listed.

**Marketplace referral (US):** Consumer sees a pre-qualified card/loan/insurance/mortgage offer (No Ding Decline avoids a hard-inquiry ding on decline) → clicks → applies → is approved → the lender pays Experian a **referral/performance/origination fee**. Recognition is on a net basis at the qualifying event (application/approval/origination depending on contract). Exact per-referral economics: **UNKNOWN** (commercially confidential); structurally these are CPA or revenue-share fees.

#### II.7 Distribution Architecture

Routes to counterparty: (1) **direct enterprise sales** to large lenders (highest value, Experian controls the relationship, deepest data access, strategic); (2) **mid-market / small-business** channels (Ascend democratises analytics down-market); (3) **API / developer self-service**; (4) **resellers and mortgage tri-merge resellers** (Experian shares the relationship and margin, but tri-merge resellers are a control choke-point in mortgage); (5) **platform partnerships** — loan-origination systems, core-banking providers, POS/BNPL, and the new ServiceNow and TazWorks integrations (embeds Experian inside others' workflows, high strategic value, medium relationship control); (6) **consumer app/web**; (7) **affiliate / comparison-site** partnerships (consumer marketplace demand); (8) **embedded distribution** inside client products (a *"significant new multi-year partnership with a leading USA bank"* will extend Experian premium credit/identity capabilities into the bank's own customer base from FY27 — Partner Solutions).

#### II.8 Pricing Architecture

- **Per-inquiry report/score pricing:** volume-tiered, confidential. UNKNOWN at list level.
- **US mortgage tri-merge — the clearest public window.** FICO wholesale royalty US$4.95/score (mortgage originations, from 2025; a per-score channel still averages ~US$10/score to lenders). Per CHLA/HousingWire, total per-loan credit-report cost rose from *"about $50 in 2022 to roughly $540 in 2026,"* and the FICO tri-merge base price from *"$1.80 in late 2022 to $30 in 2026 — a more than 1,500% increase."* **What this means for Experian's margin on a score sale:** FICO's US$4.95 is a pass-through cost; *"all amounts above $4.95 per score are collected and retained by the credit bureaus or their tri-merge resellers—not FICO"* (Jim Wehmann, FICO). So the recent mortgage price escalation is retained largely by the bureaus/resellers, not FICO — consistent with Experian's 45% FY26 mortgage-revenue growth on flat volume.
- **Ascend / PowerCurve:** platform subscription + consumption. UNKNOWN specifics.
- **Consumer subscription:** US CreditWorks Premium US$24.99/mo (US$4.99 first month); IdentityWorks Premium US$24.99/mo, Family US$34.99/mo. UK CreditExpert paid; CreditMatcher free.
- **Marketplace:** CPA / revenue-share, per-approval or per-origination. UNKNOWN rates.
- **Serasa:** consumer Score/Limpa Nome free; Serasa Premium subscription (BRL, undisclosed USD); creditor-paid recovery fees on Limpa Nome (undisclosed).
- **Pricing-power verdict:** on the buy side Experian has structural power (tri-merge non-substitutability + switching costs), tempered by reciprocity on the supply side and by FICO's royalty capture on scores.

#### II.9 Product Dependency and Cross-Sell Map

- **Prerequisite:** the bureau file underpins scores, attributes, prescreen, monitoring, the consumer product and the marketplace pre-qualification.
- **Highest margin:** North America B2B bureau/attributes (34.2% regional EBIT margin; B2B line 30.9%).
- **Retention products:** Ascend/PowerCurve (embedded, high switching cost) and enterprise master contracts.
- **Loss leaders / acquisition:** free membership, Boost, Go, free Serasa Score — they acquire the consumer and generate consented data and marketplace inventory.
- **Identity graph** underpins *both* fraud (CrossCore/Precise ID/NeuroID) and marketing (Graph/Tapad/Audigent/AtData) — a genuine shared asset.
- **Survival test if the bureau file were removed:** Experian Health (payer/identity infrastructure), Automotive/AutoCheck (DMV/vehicle data), Marketing Services (independent identity graph and third-party data), illion BankStatements/Open Data, and much of the fraud stack would survive as standalone businesses. Scores, attributes, prescreen, monitoring, and marketplace pre-qualification would **collapse** — they are bureau-file-derivative. **Conclusion:** roughly the Verticals (US$1,705m) and parts of fraud/identity are bureau-independent; the Financial Services core (US$4,463m) and most of Consumer Services are not.

#### II.10 Customer Economics and the Triple Monetisation of the Consumer — PRIORITY

**Per-unit economics (arithmetic shown; all analytical inference unless labelled):**
- Blended revenue per free member = US$2,257m Consumer Services ÷ 215m members = **~US$10.5/member/yr** (mixes free and paid; a small cohort carries it).
- A single US premium subscriber at CreditWorks Premium US$24.99/mo = **~US$300/yr** gross — i.e. one paid subscriber ≈ ~28 average members.
- B2B revenue per pull: UNKNOWN at list, but the group monetises ~1.3bn US updates monthly on the supply side and sells pulls on the demand side; Financial Services US$4,463m spread across the buying base implies large enterprise ARPU (UNKNOWN precise).

**The triple monetisation of one consumer, X:**
1. **B2B data sale:** every time a lender/insurer/landlord pulls X's report or score, Experian is paid. X has *no contract with the buyer and receives no payment.*
2. **D2C subscription:** Experian sells X monitoring/identity protection (up to US$300+/yr) — protecting X from the very data ecosystem Experian operates.
3. **Marketplace referral:** Experian sends X back to a lender and is paid a referral/origination fee — now the *primary* consumer growth driver.

**Which is largest?** At the group level, B2B (US$6,168m) dwarfs Consumer Services (US$2,257m); within Consumer Services, management states the *marketplace* has overtaken subscriptions as the growth driver. So for the *institution*, the B2B sale of the consumer's data is by far the largest monetisation; for the *consumer-facing segment*, marketplace referral is now ascendant.

**Is this a conflict of interest? Test, don't adopt the framing.** Experian frames all three as *"helping consumers improve their financial health."* The mechanics say otherwise in specific, testable ways:
- The subscription sells protection against risks (identity theft, errors) that arise *from the credit-reporting system itself* — a system Experian co-operates and profits from. A consumer advocate would call this selling the cure for a disease you help spread. On the record: **Chi Chi Wu, senior attorney at the National Consumer Law Center**, stated (January 2025): *"For decades, Experian and others have conducted terrible and perfunctory so-called investigations when consumers tried to fix errors on their credit reports – 'sham' is exactly right."*
- The marketplace referral aligns Experian's revenue with *placement*, not necessarily with the *best consumer outcome*: Experian is paid when X takes a product, creating an incentive to surface remunerative offers. "No Ding Decline" genuinely improves consumer experience, but it also increases application throughput (and thus referral revenue).
- The B2B sale monetises X's data without X's payment or direct consent to the specific buyer — lawful under FCRA/GDPR/LGPD, but the consumer is unambiguously the *product* in this leg.
- **A regulator's view is already on the record:** the CFPB's suit implies the consumer-protection machinery (disputes) is under-resourced relative to the revenue the data generates. The absence (per Volume I) of any board-level data-ethics/privacy committee is a governance gap directly relevant to managing this three-way conflict.

**Verdict:** the consumer is *both* customer and product, and the roles can coexist legally but not frictionlessly; the "financial health" narrative is partially true (Boost, Go, Limpa Nome do help some consumers) and partially a re-description of monetisation.

#### II.11 Capacity and Supply Constraints

The binding constraint is **data coverage and freshness**, not compute. US file coverage ~245m credit-active consumers, but ~28m "credit invisible" + ~21m "unscorable" thin-file (Experian research) — a coverage gap Experian addresses with **Boost** (alternative/positive data to the Experian file), **Go** (file establishment), rental/utility reporting, cashflow attributes (~6,000 predictive attributes from transaction data), and, in Brazil, the **Cadastro Positivo** (which structurally converted a negative-only system into a positive-history system, ~55% of Serasa Score weight). Freshness: ~1.3bn US updates monthly; recency depends on furnisher reporting cadence (typically monthly). Furnisher-participation completeness varies by category — full for banks/cards, thinner for rent/utilities, which is exactly why Boost exists. Coverage gaps constrain the *addressable lending population* and hence B2B volume; closing them (alternative data) is both a growth lever and a financial-inclusion claim.

#### II.12 Failure and Exception Paths

- **Inaccurate tradeline:** owner = furnisher (§623) + bureau (§611); deadline 30 days; remedy = reinvestigation. Litigation exposure high (FCRA statutory damages).
- **Mixed file** (two consumers merged): the most damaging error; owner = bureau (matching failure); driver of the highest-severity FCRA suits.
- **Identity theft / fraudulent accounts:** consumer files dispute + fraud alert/freeze; bureau must block; Experian's own fraud stack is sold to prevent this on the B2B side.
- **Disputed item:** the §611 path the CFPB attacks.
- **Security freeze blocking a legitimate pull:** consumer-controlled; friction but consumer-protective.
- **Contested adverse-action decision:** consumer routes via dispute; lender relies on FCRA safe-harbour if it used the report properly.
- **Reinserted-after-deletion data:** a *specific CFPB allegation* — Experian allegedly fails to match new reporting against previously deleted items, so errors reappear under a new furnisher name.
- **Breach:** notification duties; Experian's own Partner Solutions data-breach contracts (two large ones winding down in FY26) show it monetises *others'* breaches.
- **Furnisher supplying systematically bad data:** bureau's duty to consider furnisher unreliability — the CFPB says Experian ignores "improbable or illogical" furnisher responses.

**This section is disproportionately important because dispute handling is simultaneously the largest consumer-facing cost, the core consumer-protection obligation, and the subject of live federal litigation.** Credit/consumer-reporting complaints are the single largest category in the CFPB complaint database — accounting for roughly 80% of all complaints in recent years — with the most common sub-issue being incorrect information on a report. The 2012–2013 FTC Section 319 FACTA accuracy study found that roughly one in five consumers had an error corrected after dispute on at least one of their three reports, 26% reported a potential material error and filed a dispute (half of whom saw a score change), and ~5% had errors serious enough to raise the cost of credit — the empirical backdrop against which the CFPB's "sham investigations" theory is being litigated.

#### II.13 Product-Market Evolution

From a credit-checking bureau, Experian moved: → decisioning/analytics (PowerCurve, then cloud-native Ascend) → direct-to-consumer (driven by free-score consumer demand, breach-response contracts, and the realisation that the consumer relationship is both a data source and a marketplace funnel) → fraud/identity build-out (CrossCore, NeuroID, ClearSale, KYC360, AtData — a response to digital-first fraud and to the fact that identity is the connective tissue across all products) → marketing-services expansion (Tapad/Audigent/AtData) and its **regulatory collision** (the ICO case) → healthcare adjacency (infrastructure reuse) → marketplace/lead-generation (the highest-growth consumer model, extended into mortgage via Own Up and insurance via Gabi) → recent identity/RegTech/mortgage-marketplace M&A (FY26 acquisitions totalling US$792m). **Assessment:** the expansion is *coherent around one axis — identity and permissioned data* — rather than accretive drift. The through-line is: own the identity graph, then apply it to every domain where matching a person to a record has value (credit, fraud, marketing, health, automotive, and now agentic-commerce via "Experian Agent Trust"). The marketing collision is the exception that proves the rule: it is the one domain where the permission does *not* travel with the data, which is why it drew enforcement. Management claims *"over US$15bn of AI-enabled addressable market opportunities"* across Health, agentic commerce, Ascend expansion and embedded consumer marketplaces [COMPANY CLAIM — forward-looking, not realised].

#### II.14 Volume II Reconstruction

**(1) Full Product Architecture by entity and legal basis** — see II.1 (families A–J; Experian Information Solutions Inc. = US bureau/FCRA; Experian Limited = UK bureau/UK GDPR; ConsumerInfo.com dba Experian Consumer Services = US D2C; Experian Marketing Solutions LLC = marketing/legitimate interests; Experian Health Inc. = RCM/infrastructure; Serasa S.A. = Brazil/LGPD+Cadastro Positivo; illion = ANZ/Privacy Act+CDR).

**(2) Three-Sided Customer Map** — furnisher (free-in, reciprocal access) / buyer (per-pull cash) / marketplace advertiser (referral fee); one institution occupies all three; reciprocity arbitrates power (II.2).

**(3) Customer-Segment Map** — Financial Services (US$4,463m) dominant; Verticals (US$1,705m: Automotive, Health, Marketing Services) bureau-independent; Consumer Services (US$2,257m) subscription + marketplace.

**(4) Jobs-to-Be-Done Matrix** — lenders buy an auditable decision basis; consumers buy access/protection/clearance; other buyers buy identity/coverage/risk (II.3).

**(5) B2B and Consumer Journeys** — enterprise integration → renewal (100% NA); consumer free sign-up → subscription *or* marketplace (II.4).

**(6) Inverted Value-Flow Diagram** — free inflow → matching/attributes/scores (value creation + IP ownership) → paid outflow; split §623/§611 liability (II.5).

**(7) Transaction Teardowns** — US card app; UK affordability; prescreen; the CFPB dispute; Limpa Nome; marketplace referral (II.6).

**(8) Distribution Architecture** — eight routes, enterprise-direct highest value, embedded/Partner Solutions rising (II.7).

**(9) Pricing Architecture** — buy-side power tempered by reciprocity and FICO royalty capture; most rates UNKNOWN; mortgage tri-merge the public window (II.8).

**(10) Product Dependency Map** — bureau file is prerequisite; Verticals + fraud/identity survive its removal; Financial Services core + Consumer Services collapse (II.9).

**(11) Triple-Monetisation Analysis** — B2B data sale (largest, institution-wide) > marketplace referral (rising, consumer-segment) ≈ subscription; consumer is both customer and product; conflict real, lawful, frictional (II.10).

**(12) Capacity and Coverage Map** — coverage/freshness the binding constraint; ~49m thin/invisible in US addressed by Boost/Go/alt-data; Cadastro Positivo in Brazil (II.11).

**(13) Failure/Exception Map** — mixed files and reinsertion are the highest-severity paths; dispute handling is duty, cost and litigation at once (II.12).

**(14) Product-Market Evolution** — coherent expansion along the identity/permissioned-data axis; marketing the one domain where permission doesn't travel (II.13).

**(15) Key Unknowns** — per-inquiry and score list prices; Ascend/PowerCurve pricing; marketplace CPA/revenue-share rates; Limpa Nome creditor take-rate; the paid-conversion rate of the 215m free base; the split of Consumer Services between subscription and marketplace; Own Up deal value (undisclosed); the eventual CFPB outcome and any mandated dispute-system remediation cost.

**(16) Ten Most Important Conclusions:**
1. The product sold is a **network position plus derived IP**, not raw data — the data is borrowed, the aggregation and models are owned.
2. The **inverted value flow** (free input from the same parties who buy the output) is the enterprise's defining economic mechanism and the source of its structurally high margin.
3. **Reciprocity is the true moat and the true price-discipline** — it locks furnishers in and simultaneously prevents Experian from over-charging its own suppliers.
4. **Pricing power is real but asymmetric** — strong on the buy side (tri-merge non-substitutability), constrained on the supply side (reciprocity) and shared with FICO on scores.
5. The **consumer is monetised three times** and is unambiguously the product in the largest (B2B) leg; the "financial health" framing is a partial truth layered over monetisation.
6. **Marketplace referral has overtaken subscription** as the consumer growth engine, widening the conflict-of-interest surface and shifting revenue quality toward transactional.
7. **Dispute handling is the fault line** — the largest consumer-facing cost, the core legal duty, and the subject of live CFPB litigation that survived a motion to dismiss (October 2025).
8. **The bureau file is load-bearing** — remove it and Financial Services and most of Consumer Services collapse, while Verticals (Health, Automotive, Marketing) and much of fraud/identity survive as independent businesses.
9. **The expansion is coherent** around identity/permissioned data; the marketing-services collision (ICO) is the diagnostic exception because permission does not travel with marketing data.
10. **Serasa is a distinct, systemically important consumer platform** (~100m base, US$19.4bn renegotiated) with economics (Limpa Nome take-rate) that Experian does not disclose.

**The central question answered — what is a credit bureau actually selling?** Not data (it doesn't own the crude data), not merely a permission, and not simply a decision. It is selling **access to a network position that no participant could occupy alone** — a shared, reciprocally-funded utility whose value is precisely that it aggregates what no single bank would share bilaterally, wraps it in statutory permission and explainability, and rents that position to every side of the market, including back to the consumers who are its raw material. The most valuable relationship is the enterprise financial-services buyer that is also a furnisher (highest revenue, highest stickiness); the most fragile is the **consumer relationship**, because it rests on a "financial health" narrative that the dispute-handling litigation and the triple-monetisation mechanics are actively straining.

### Recommendations (for an analyst / investor / counterparty using this teardown)

1. **Treat the bureau file as the crown jewel and reciprocity as the moat.** Monitor the UK Credit Reporting Governance Body transition (CP26/7, February 2026) closely — any weakening of reciprocity or mandated data-portability is the single biggest structural risk to the free-input economics. *Threshold that would change the view:* a regulatory move to compel data sharing on non-reciprocal terms, or to cap per-pull pricing.
2. **Price the CFPB suit as a cost-structure signal, not just a legal contingency.** With the motion to dismiss denied and discovery under way, a consent order mandating specific matching/reinvestigation systems would convert a variable legal risk into a fixed cost and compress the consumer-facing margin. *Threshold:* any settlement/consent order specifying dispute-system remediation.
3. **Watch the marketplace mix.** As marketplace referral overtakes subscriptions, revenue quality shifts from recurring to transactional/cyclical and the conflict surface widens. *Benchmark:* disclosure of the marketplace-vs-subscription split within Consumer Services would materially improve the segment's valuability.
4. **Value Serasa as a separate platform.** ~100m base, US$19.4bn renegotiated, strong LatAm consumer growth — but the Limpa Nome creditor take-rate is undisclosed; press for it. *Threshold:* any disclosure of Limpa Nome revenue or take-rate.
5. **Stress-test the mortgage pricing tailwind.** The 45%-on-flat-volume mortgage effect is a pricing windfall vulnerable to (a) VantageScore 4.0 competition compressing score margins (FHFA authorised VantageScore 4.0 for GSE conforming mortgages, 8 July 2025) and (b) political pressure (CHLA/MBA) on tri-merge costs. *Benchmark:* GSE adoption pace of VantageScore 4.0 and any FICO Mortgage Direct License disintermediation of bureau markups.

### Caveats

- **Pricing opacity is pervasive.** Per-inquiry rates, enterprise contract terms, marketplace CPA/revenue-share and Serasa's creditor fee are commercially confidential and labelled UNKNOWN; where per-member arithmetic is shown it is explicitly analytical inference, not disclosed unit economics.
- **Segment figures** are Benchmark, ongoing-activities, from the FY26 results announcement/annual report; they exclude exited B2B lines and should not be compared to prior-year statutory numbers without re-presentation. Regional revenue sums (5,587 + 1,297 + 942 + 599 = 8,425) reconcile to ongoing total; statutory revenue is US$8,445m.
- **Some third-party consumer-subscription aggregator pages** show inconsistent tier names/prices; figures are anchored to Experian's own disclosures where possible and ranges are flagged.
- **The ICO, CFPB, tribunal, CHLA and NCLC characterisations** are allegations/findings/estimates as stated by the respective bodies; the CFPB matter is unresolved and Experian contests it; the CHLA per-loan cost figures are a trade-association estimate disputed in part by FICO.
- **Forward-looking company statements** (AI-enabled addressable market, FY27 Partner Solutions ramp, cost savings from FY27) are labelled COMPANY CLAIM and are not treated as realised results.
- The **"financial health" framing has been tested against mechanics rather than adopted**; readers who disagree with that analytical stance should weight the company's narrative more heavily.

*End of Volume II. Volume III not commenced, per scope.*


---

# Part III — Operations, Identity Infrastructure, Data, Technology & Organisational Design

### Operations, Identity Infrastructure, Data, Technology & Organisational Design

*Evidence classification used throughout:* **CONFIRMED FACT / COMPANY CLAIM / THIRD-PARTY ESTIMATE / ANALYTICAL INFERENCE / HYPOTHESIS / UNKNOWN.** Where Experian has published nothing about an internal mechanism, this volume writes UNKNOWN rather than inventing plausible architecture. Litigation filings and the CFPB complaint are used as the richest public window into the matching and dispute systems, with allegations labelled as allegations.

---

#### III.0 Framing and the central finding

The central question this volume must answer is whether identity resolution is a solved engineering problem that Experian executes well, or an irreducibly error-prone process whose failures are the unavoidable cost of the bureau model. On the evidence: **it is the latter — but with a solvable excess margin that Experian has under-invested in closing.** Matching roughly 1.3 billion monthly record updates to the right person among ~245 million consumers, with no universal identifier and with furnisher-supplied identity data of variable quality, is mathematically guaranteed to produce a non-zero rate of mixed and fragmented files. That floor is structural. But the *height* of the floor is a policy choice — where the match threshold sits, whether reinsertion guards exist, how much discretion a dispute agent is given — and the CFPB's January 2025 complaint alleges Experian set those choices to minimise cost rather than maximise accuracy.

Company disclosure on internal systems is thin; adversarial sources (the CFPB complaint, FCRA litigation, NCLC research) are the richest window. This volume leans on them heavily.

---

#### III.1 Operating Model

**Structure.** Experian is organised as a four-region reporting matrix (North America; Latin America; UK & Ireland; EMEA/Asia Pacific) overlaid on global business lines (B2B — Financial Services and Verticals; Consumer Services). CONFIRMED FACT: the FY26 Annual Report states Experian "operate[s] across four geographic regions, which allows us to tailor our products to local market needs while sharing innovation globally." Headcount is roughly 25,200–25,346 across 32–33 countries (COMPANY CLAIM: "a team of 25,200 people across 33 countries"; THIRD-PARTY ESTIMATE: Revelio Labs, 25,346 as of March 2026). Corporate HQ is Dublin; operational hubs are Nottingham, Costa Mesa and São Paulo.

The major operating functions, mapped:

| Function | Mandate | Key systems | Legal entity (US) | Automation/offshore |
|---|---|---|---|---|
| Data acquisition & furnisher mgmt | Onboard/certify furnishers, ingest Metro 2 | Metro 2 intake, DataArc 360 | Experian Information Solutions, Inc. (EIS) | High automation |
| Ingestion & data ops | Validate, normalise, QC ~1.3bn updates/mo | File One pipeline | EIS | High automation |
| Identity resolution | Attach records to correct file | "Find Consumer" search-and-match | EIS | Fully automated |
| Database operations | Maintain core files | File One (US); CAIS (UK) | EIS / Experian Ltd | Automated |
| Analytics & model dev | Build attributes, scores, models | Ascend, Ascend Intelligence Services | EIS / Experian Software Solutions | AI-augmented |
| Product/platform eng | Build Ascend, APIs | AWS cloud stack | Group | Cloud-native |
| Consumer operation | Serve 215m+ free members | Experian app, EVA, Boost | ConsumerInfo.com dba Experian Consumer Services | High automation |
| Dispute/consumer-rights | FCRA §611 reinvestigation | e-OSCAR, Online Dispute Center | EIS | Highly automated + offshore |
| Security | Protect the estate | zero-trust program | Group | — |
| Compliance/permissible-purpose | Police access | subscriber vetting | EIS | Mixed |
| Sales & client integration | Onboard enterprise clients | PowerCurve, Ascend Sandbox | Regional | Manual-heavy |

**Regional operational reality vs. reporting geography.** ANALYTICAL INFERENCE: the four regions are P&L constructs; operational reality is more concentrated. The US bureau (EIS, an Ohio corporation) is the principal profit centre and runs the File One estate. Technology and analytics are increasingly centralised and cloud-based; India (Hyderabad; Experian Credit Information Co. of India, ~490 people per Revelio in the India credit entity, with a larger broader India technology footprint) is a significant technology and operations centre. Dispute processing is widely reported to rely on low-cost offshore vendors (see III.9).

---

#### III.2 Data Ingestion and Furnisher Operations (replaces Transaction Processing)

**Scale and cadence.** CONFIRMED FACT (CFPB 2012 white paper, corroborated by Vol I/II figures): the NCRAs each maintain files on 200m+ adults and receive data from ~10,000 furnishers, who provide information on **over 1.3 billion consumer credit accounts (tradelines) monthly**. Most furnishing is monthly and highly concentrated: "The 10 largest institutions furnishing credit information to each of the NCRAs account for more than half of all accounts," and retail and network-branded revolving cards are "nearly 60% of all trade lines" (CFPB 2012).

**The Metro 2 format.** CONFIRMED FACT: Metro 2 is the fixed-format data specification maintained by the CDIA's Metro 2 Task Force (Equifax, Experian, Innovis, TransUnion) and published in the annually-updated Credit Reporting Resource Guide (CRRG). It standardises identity fields (name, address, SSN, DOB) and account fields (balance, status, payment history, dates). Access to the format is restricted to furnishers, their processors and CRAs. Furnisher accuracy liability flows through FCRA §623 and Regulation V (12 CFR §1022.42), which requires furnishers to maintain "reasonable written policies and procedures regarding the accuracy and integrity" of furnished data. Experian sells furnishers a compliance tool, DataArc 360, with "over 130 pre-built rules" to validate a Metro 2 file before submission (COMPANY CLAIM, Experian/Edq).

**Onboarding, validation, screening.** CONFIRMED FACT (CFPB 2012): "before accepting information from data furnishers, [the NCRAs] perform certain background and quality control checks on would-be-furnishers," and "when data files are received, the NCRAs also perform quality checks prior to adding the data to credit files." The specific number, sequence and thresholds of Experian's internal validation stages are **UNKNOWN** (not published). What is known: Metro 2 is internally consistent by design — the format is engineered so certain field combinations cannot lawfully coexist, so structurally invalid combinations can be detected at intake.

**Bad-furnisher detection.** Adversarial framing (CFPB allegation): Experian "routinely and uncritically accepts the original furnisher's response … even when that response was improbable or illogical on its face, or when Experian has other information available that suggests the furnisher is unreliable." This implies furnisher-reliability signals exist internally but are not consistently acted upon. Whether Experian systematically suppresses a chronically-erring furnisher's feed is **UNKNOWN**.

**Public records and the National Consumer Assistance Plan (NCAP).** CONFIRMED FACT: NCAP — a settlement with 31+ state AGs, announced March 2015, phased through 2018 — imposed minimum PII standards (name, address, and SSN or DOB) and a minimum 90-day refresh on civil public records. Effective 1 July 2017 it removed **all civil judgments and roughly half of tax liens**; by April 2018 all tax liens were removed; bankruptcies remained. Experian's own analysis projected ~96% of civil-judgment data would fail the new PII standard. CONFIRMED FACT (CFPB): pre-NCAP, ~6% of consumers had a judgment or lien; post-implementation, ~1.4% had a tax lien and none had civil judgments, yet the CFPB found "removal of public records has little effect on consumers' credit scores." Phase 2 restricted medical-debt reporting (180-day delay; paid medical debt removed).

**UK CAIS.** CONFIRMED FACT: Experian Limited (FCA-authorised) operates CAIS (Credit Account Information Sharing), which shares 350m+ records across ~400 institutions on a reciprocity / closed-user-group basis (data-in for data-out). Detailed CAIS validation architecture is not publicly detailed — partially **UNKNOWN**.

**Serasa (Brazil).** CONFIRMED FACT: Serasa S.A. operates the Brazilian bureau covering ~100m Brazilians; positive-data sharing operates under the Cadastro Positivo regime (Lei 12.414 as amended by LC 166/2019), which shifted to an opt-out (automatic inclusion) model. Serasa's internal ingestion pipeline specifics are **UNKNOWN**.

**illion (Australia/NZ).** CONFIRMED FACT: illion's BankStatements retrieves 47m+ transactions weekly from 2.7m+ individuals for 5,000+ customers via open-banking / bank-statement retrieval — a real-time, consent-based ingestion model distinct from the monthly batch bureau feed.

**Rejection/exception rates: UNKNOWN.** No public figure quantifies the proportion of records rejected or held in exception at Experian intake.

---

#### III.3 Identity Resolution and Matching (replaces Treasury) — PRIORITY DEPTH

This is the enterprise's core operation. Everything downstream — scores, reports, decisions, disputes — depends on attaching each furnished record to exactly the right consumer.

**The engine.** CONFIRMED FACT (primary source, Experian 2003 filing to the Administrative Office of the U.S. Courts): "Experian has developed a complex 'search and match' system … called 'Find Consumer.' … 'Find Consumer' locates the consumer's record in our database and a credit report can be returned in 1.8 seconds. 'Find Consumer' relies on identification information provided on the input data … Name, address and SSN are used to search our database to identify all possible candidate consumers. After all matches are found, a complex and extensive series of edits are performed using various matrixes." The core database is **File One** (COMPANY CLAIM: "Experian's File One℠ database of more than 245 million credit-active consumers"). Social Search / SSN-search logic "match[es] and retrieve[s] consumers associated with the same Social Security number."

**File architecture.** CONFIRMED FACT (CFPB 2012): the NCRAs use differing data architectures. "At least one NCRA organizes its database like a traditional flat filing system so that each consumer is linked to one file. Consumers' files are distinguished through matching logic using a consumer's personal identifiers such as name, address, SSN, and date of birth. Multiple or fragmented files can occur for a single person when information is reported with different identifying information." Which architecture is Experian's specifically is not disclosed there — the flat-file attribution to Experian is **HYPOTHESIS**.

**Identifiers and technique.** CONFIRMED FACT: matching uses name (and prior names), current/former addresses, SSN (including partial-SSN matching), DOB and phone. The literature distinguishes deterministic matching (exact or exact-partial, e.g. last-four SSN, with support for transpositions/typos) from probabilistic matching (a match probability from degree of similarity). Experian's exact confidence thresholds and the deterministic/probabilistic blend are **UNKNOWN** (proprietary), but the "candidate set then matrix of edits" description in the Find Consumer filing indicates a two-stage retrieve-then-score design consistent with rule-based deterministic linkage plus tolerance edits.

**The two-sided error problem.**
- **Over-matching → mixed file.** Two consumers' data merged. This is the single most damaging bureau error and the source of the largest FCRA verdicts. CONFIRMED FACT (NCLC *Automated Injustice*, citing *Apodaca v. Discover Fin. Servs.*): bureaus "have been known to mismerge files when the consumers' names are similar and they share seven of nine digits in their SSN." NCLC's recommended fix — "merely requiring an eight of nine SSN match and a flag if that match isn't perfect" — shows the threshold is a tunable policy dial, not a physical constant.
- **Under-matching → fragmented file.** History splits across two files, suppressing score or rendering a consumer unscorable. CONFIRMED FACT (CFPB "Data Point: Credit Invisibles," 5 May 2015): "As of 2010, 26 million consumers in the United States were credit invisible, representing about 11 percent of the adult population. An additional 19 million consumers, or 8.3 percent of the adult population, had credit records that were treated as unscorable" (9.9m insufficient + 9.6m stale). (Vol I/II's ~28m/~21m are the later-vintage figures; the 26m/19m are the CFPB's foundational 2015 measurement.)

**Incentive asymmetry.** ANALYTICAL INFERENCE: the two errors are not symmetric in who bears the cost. A mixed file that inserts *bad* data harms the consumer (who is not the paying customer) and helps no lender; a loose threshold that maximises "hits" on a lender's inquiry improves the bureau's fill/match rate — a metric lenders value. The commercial pressure therefore tilts toward looser matching, which produces mixed files. This asymmetry, not incompetence, is the structural driver.

**Scale of the problem.** CONFIRMED FACT (FTC "Report to Congress Under Section 319 of the FACT Act," Fifth Interim Report, December 2012; n=1,001 randomly selected participants): "26 percent of consumers reported a potential material error … and half of these consumers experienced a change in their credit score. For five percent of consumers, the error … could lead to them paying more." 21% had a modification after dispute; the FTC's most conservative measure found 9.7% had at least one confirmed material error, and 2.2% of all reports had a material error affecting the price of credit. Common contributing factors: common names, Jr./Sr. suffix confusion, family members at one address, transposed SSN digits, thin files. A 2021 academic study (arXiv 2105.07554) illustrates real-world noise: an Infutor→TransUnion match of 80m submitted individuals returned 49m matched — a ~61% match rate under controlled conditions.

**The identity graph beyond credit — and the legal firewalls.** The same matching competence powers:
- **Fraud/identity:** CrossCore (cloud orchestration platform, launched 2016), Precise ID (US identity verification/KBA), FraudNet, Hunter, Prove-ID; plus acquired assets (Ekata/Identity Network via a Mastercard partnership).
- **Marketing:** the Experian Graph and Tapad. CONFIRMED FACT (Experian PLC, completed 19 November 2020): Experian acquired "100% of Tapad from Telenor for a cash consideration of around US$280m," with forecast revenue of US$55m for the 12 months to 31 December 2020, placed in its North America Data segment (Telenor had itself bought Tapad for US$360m in January 2016). Plus AtData/Audigent-type email and audience assets.
- **Healthcare:** Experian Health patient-identity resolution.

**FOLLOW-THE-DATA-RIGHT — the firewalls.** CONFIRMED legal constraint: FCRA data assembled for a permissible purpose (credit) may not lawfully be repurposed into a marketing audience, and marketing/consumer data may not enter a credit-eligibility decision (which would make the marketing dataset a "consumer report" and its user subject to FCRA). Operational capability (one matching engine can link across all estates) and legal permission (the estates must be firewalled) are separate constraints. ANALYTICAL INFERENCE: the technical unity of the identity graph is precisely why the legal segregation must be enforced at the data-governance and access-control layer, not at the algorithm layer — the algorithm does not "know" which estate it is serving.

**The CFPB's matching allegation (reinsertion).** CONFIRMED FACT (CFPB complaint, ¶¶91–97): "Experian has failed to implement basic matching tools that prevent or greatly reduce the likelihood of reinsertion by a new furnisher of a previously deleted tradeline. For example, Experian has not implemented procedures to compare dates of first delinquencies, recent credit balance amounts, high credit balances, or the names of original creditors, to ascertain whether a newly reported tradeline constitutes a reinsertion." IMPLICATION for architecture: the same debt resold to a new debt buyer arrives with a *new* furnisher identity and is treated by the matching engine as a new record with no dedupe against the *deleted* record's substantive fields. This is an allegation, not a proven fact; it implies matching keys on furnisher+account identity rather than on the underlying debt's economic fingerprint.

---

#### III.4 Database and Platform Architecture

**Core databases.** File One (US consumer file, EIS); CAIS (UK, Experian Limited); Serasa's Brazilian databases; illion's Australian/NZ databases. Detailed schemas are not public.

**Cloud position — now precisely establishable.** CONFIRMED FACT: on **19 June 2025** Experian and AWS announced a **10-year strategic agreement** naming AWS as Experian's "preferred cloud" and strategic partner for generative AI. Quantified claims from Experian CTO Rodrigo Rodrigues (COMPANY CLAIM): "By moving to AWS, we've reduced our data processing time by 60%, improved our ability to launch new products from months to weeks, and can now analyze credit data in real-time." The migration involves "migrating off mainframe computers and moving multiple on-premises servers to the cloud" and developing "more than 100 generative AI use-cases." This corroborates the Vol I/II position that North America and Brazil cloud migration was substantially complete by FY26 (Health excepted), with dual-run costs expected to fall from FY27.

**Ascend.** CONFIRMED FACT: the Experian Ascend Platform is cloud-native, available in North America, Brazil and the UK, unifying data, analytics, credit decisioning and fraud in a single interface; Ascend Ops handles model registration/test/deploy/monitor across cloud environments; Ascend Sandbox provisions a data sandbox that reduces model build "from months to hours" (COMPANY CLAIM). A Forrester Total Economic Impact study (Experian-commissioned) claimed 183% ROI / US$13.3m NPV for a composite organisation. Carry-forward: 2,300+ client solutions, 37 product capabilities, 2,100+ attributes rising to ~6,000 with cashflow/transaction blending.

**Storage/streaming/serving.** Specific named components (Kafka/Confluent, Kubernetes, Snowflake, Databricks) are **UNKNOWN** for Experian by name; the confirmed stack is AWS-centric with generative AI on AWS. Health remains on legacy infrastructure (Vol I/II).

**Benchmark.** Equifax completed a ~US$1.5bn–US$3bn cloud transformation on **Google Cloud Platform**, built around a "single data fabric" that unifies 100+ data sources and explicitly enhances "the keying and linking of our data assets … identity resolution and fraud prevention" — a materially different architectural choice (GCP + single data fabric) from Experian's AWS-centric, platform-led (Ascend) approach.

---

#### III.5 Decisioning and Delivery Operations

**Real-time pull.** CONFIRMED FACT (Experian's own historical figure): a credit report can be returned in ~1.8 seconds via Find Consumer. Real-time API delivery is the norm for point-of-sale/online decisions.

**Batch.** Prescreen and portfolio review run as batch jobs against the file; monthly furnisher updates are the dominant batch ingestion window.

**Tri-merge (US mortgage).** CONFIRMED FACT: mortgage lenders pull all three bureaus via a mortgage reseller; the reseller sends simultaneous inquiries to Experian, Equifax and TransUnion, each independently retrieves its file and computes a score, and the reseller merges them, dedupes tradelines and applies the "middle score" convention. A tri-merge can cost ~US$200+ as of early 2026 (THIRD-PARTY). Resellers are a distinct channel/tier layered on top of the bureau.

**Deployment models.** PowerCurve (decisioning software, on-prem/hosted/cloud variants) and Ascend Sandbox provisioning. Enterprise onboarding is manual-heavy; switching costs are high because integrations, attribute definitions and model recalibration are lender-specific — a source of stickiness (see III.15).

---

#### III.6 The Consumer Operation

CONFIRMED FACT: 215m+ free members globally; the app is used by ~85m consumers worldwide (SiliconANGLE/company). Registration/identity verification includes Experian Go (government ID + selfie for thin/no-file consumers). Free-report obligations run through FCRA and the AnnualCreditReport.com joint venture with Equifax and TransUnion. Security freezes, fraud alerts and locks are offered; Boost links bank accounts (open banking / permissioned data) to add positive telecom/utility/rent data, and the next-generation EVA (2026) now recognises everyday spending via connected accounts. Marketplace pre-qualification monetises the free base by routing pre-qualified offers (revenue is lead-gen/affiliate — the "inverted value flow" of Vol II).

**Cost of the free tier.** ANALYTICAL INFERENCE: the free tier's marginal cost is low (cloud-served self-service + AI assistant EVA displacing human support) and is cross-subsidised by marketplace and premium conversion; the 300bps labour-cost reduction (Vol I/II) is partly attributable to AI-driven consumer self-service. Exact unit economics are **UNKNOWN**.

---

#### III.7 Model Development, Governance and the Explainability Constraint — NEW SECTION, PRIORITY DEPTH

**How models are built.** Attribute engineering on the 2,100+ / ~6,000-attribute libraries; Ascend Intelligence Services for custom model build; Ascend Ops for deploy/monitor with drift detection.

**Adverse-action reason codes — the binding constraint.** CONFIRMED FACT: under ECOA/Regulation B and FCRA, a declined consumer must be told the principal reasons for the adverse action; when a credit score drives the decision, the key factors that adversely affected the score must be disclosed. FinRegLab (independent) calls this "the most technically difficult explainability challenge for lenders using machine learning underwriting models." CONFIRMED FACT: Experian holds patents (e.g., US 11,922,495; US 12,050,975; US 12,321,826) on generating adverse-action reason codes from complex ML models using SHAP (Shapley additive explanations) and grouped partial-dependence plots. Experian markets "patent-pending ML explainability … generate adverse action codes directly from the model."

**Does this prohibit opaque models in credit?** ANALYTICAL INFERENCE, well-supported: effectively yes for the decision itself. A fully opaque model that cannot yield stable, defensible principal-reason codes is, in Experian's own words, "effectively … unusable" in a credit decision. The industry response is not "don't use ML" but "use ML techniques constrained to remain explainable" (monotonic gradient-boosted trees + post-hoc SHAP reason codes). The constraint shapes *which* ML is deployable in-decision, not whether ML is used.

**Fair lending / disparate impact.** CONFIRMED FACT: ECOA/Reg B prohibit use of protected characteristics and their proxies; Experian markets fairness-aware training and disparate-impact testing. The precise internal testing regime is partly **UNKNOWN**.

**Model risk management (SR 11-7).** CONFIRMED FACT: because Experian models are deployed inside supervised banks, they inherit bank MRM expectations (Fed/OCC SR 11-7). Experian launched **Experian Assistant for Model Risk Management** (31 July 2025, powered by ValidMind), claiming it can "reduce internal approval times by up to 70%" by automating model documentation, validation and monitoring for US and UK regulatory requirements; it won a 2026 BIG Innovation Award.

**Generative and agentic AI — productivity vs. decision.** This is the crucial distinction:
- **Productivity / model-development side (no explainability constraint on the credit decision):** Experian Assistant (launched Money20/20, 28 October 2024) compresses model build "from months to days—or even hours"; built in nine months; ~100 genAI use-cases developed with AWS; internal genAI for coding assistance. The 300bps labour-cost reduction (Vol I/II) sits substantially here.
- **Consumer side:** EVA (Experian Virtual Assistant), an LLM-based financial copilot for ~85m app users; "We treat generative AI outputs with the same rigor as credit data" (Jack Yu, Experian).
- **Agentic:** Experian launched an "Agent Operating System" and an "Agent Trust" ecosystem (2026), positioning for agentic commerce.
- **In the credit decision itself:** generative AI is *not* used to make the eligibility decision — that remains the domain of explainable, reason-code-producing models. ANALYTICAL INFERENCE: genAI accelerates the *building and documenting* of decision models and the *serving* of consumer guidance, but the adverse-action requirement fences it out of the decision boundary.

**Relationship to FICO/VantageScore.** CONFIRMED FACT (Vol I/II): Experian distributes FICO under licence (US$4.95 wholesale mortgage royalty) and co-owns VantageScore equally with Equifax and TransUnion. Experian's own attributes/scores compete alongside these distributed third-party scores — Experian is simultaneously a distributor of others' models and a builder of its own.

---

#### III.8 Security Architecture

**History and posture.** CONFIRMED FACT: the 2015 T-Mobile breach exposed ~15m consumers. Per Experian North America's 1 October 2015 statement and T-Mobile CEO John Legere's letter, the hacker "acquired the records of approximately 15 million people, including new applicants requiring a credit check for service or device financing from September 1, 2013 through September 16, 2015"; Experian confirmed neither its consumer credit database nor T-Mobile's network was breached (Experian held the data to process T-Mobile credit applications). It settled November 2022 with a 40-state AG coalition: **US$12.67m from Experian** (plus a separate T-Mobile settlement; combined >US$15–16m). The Experian settlement mandated a comprehensive information-security program incorporating **zero-trust principles**, data minimisation (specifically reducing SSN use as an identifier), executive-level reporting, encryption, segmentation, patch management, intrusion detection, firewalls, access controls, logging/monitoring, penetration testing and risk assessments.

**The 2017 Equifax effect.** CONFIRMED FACT: the Equifax breach affected 147 million consumers (per the 2019 FTC/CFPB settlement record) and triggered a ~US$1.5–3bn Equifax cloud-plus-security transformation, resetting industry expectations. ANALYTICAL INFERENCE: it raised the disclosure and board-attention bar for all three bureaus; Experian's zero-trust settlement terms and AWS security emphasis reflect the post-2017 environment. NOTE (Vol I/II): Experian has **no dedicated board-level data-ethics/privacy committee** — a governance gap against the salience of this risk.

**Permissible-purpose enforcement.** CONFIRMED vector: the largest practical breach vector for a bureau is not perimeter compromise but *credentialled access misuse* — legitimate subscribers (or fraudsters posing as them) pulling reports without permissible purpose. Experian's 2012-era incident (an identity thief posing as a private investigator to abuse an Experian subsidiary's services) exemplifies this; the 2022 settlement addressed subscriber due diligence.

**Named CISO / certifications.** The current group CISO is **UNKNOWN** — Experian does not prominently publish the name (contrast Equifax's very public CISO Jamil Farshchi). Certifications (ISO 27001, SOC 2, PCI DSS) are held across various products but the precise scopes are **UNKNOWN** at this granularity.

**Concentration risk.** ANALYTICAL INFERENCE: holding files on ~245m US consumers in one estate is systemic concentration; the commercial irony is that Experian sells identity-protection products whose demand rises with breaches (including, historically, its own and competitors'). This is a genuine conflict-of-interest tension the company does not resolve structurally.

---

#### III.9 The Dispute and Consumer-Rights Production Line — PRIORITY DEPTH

**Volume.** CONFIRMED FACT (CFPB complaint ¶33): "Experian typically processes over a million consumer disputes per month" — i.e. **>12m disputes/year at Experian alone**. Channels: mail, phone, website ("Online Dispute Center") and mobile app. Industry baseline (CFPB 2012): ~8m consumer dispute contacts in 2011 generating 32–38m disputed items across the three bureaus; no official updated cross-bureau total has replaced this figure (the CFPB now reports *complaints*, not disputes — 4.8m credit-reporting complaints Jan 2024–Jun 2025, ~3.9m about the big three).

**The process (all steps).**
1. **Intake:** consumer submits via mail/phone/online/app.
2. **Coding:** CONFIRMED FACT — a bureau agent reads the submission and converts it into an **ACDV (Automated Credit Dispute Verification)**, "a one-page form" carrying identity fields plus the tradeline "as currently reported," a **three-digit dispute code** and "sometimes a short free-form description" (CFPB ¶29). The bureau does *not* forward the consumer's actual letter/documents by default. (Example specificity from the Second Amended Complaint: for an online "account paid in full" dispute Experian assigns code **106** rather than the more precise code **010** "Settlement or partial payments accepted," because its Online Dispute Center does not permit the more precise code.)
3. **Internal update vs. transmission:** CONFIRMED FACT (CFPB ¶36) — "Experian resolves a minority of disputes via an internal update. If Experian does not make an internal update, it prepares an ACDV to transmit to the furnisher through e-OSCAR."
4. **Transmission via e-OSCAR:** CONFIRMED FACT — e-OSCAR is the web-based system jointly operated by Equifax, Experian, Innovis and TransUnion; "the ACDV is typically the only way CRAs and furnishers communicate during a reinvestigation" (¶32). Historically the NCRAs forward explanatory text in only a minority of cases (26% in the 2012 data) and generally do not forward consumer documentation.
5. **Furnisher investigation (§623):** furnisher reviews its own records and returns the ACDV with a **two-digit response code** (verify/modify/delete).
6. **Bureau determination:** Experian updates the file per the furnisher response.
7. **Consumer result notice:** CONFIRMED FACT (CFPB allegation) — notices are alleged to be "confusing, ambiguous, incorrect, or internally inconsistent."

**The 30-day clock.** CONFIRMED FACT: FCRA §611 requires reinvestigation within 30 days (extendable to 45 in limited cases). Operational implication: the clock forces industrialisation — high volume × hard deadline × no revenue = pressure toward maximal automation and minimal per-dispute labour.

**Automation and offshoring.** CONFIRMED FACT (NCLC *Automated Injustice*): bureaus limit the role of dispute handlers — "or of the foreign workers employed by their offshore vendors — to little more than selecting … two or three digit codes. Workers do not examine documents, contact consumers by phone or email, or exercise any form of human discretion." NCLC also documented that "one credit bureau has reduced the amount it pays to its vendor that handles disputes to a mere US$0.57 per dispute letter." IMPORTANT: the CFPB complaint itself does **not** name any offshore vendor or country and does not state a seconds-per-dispute figure — those specifics come from NCLC and prior litigation, not this case. Per-dispute agent time in seconds is **UNKNOWN** from primary sources.

**The CFPB's operational allegations, decomposed.** CONFIRMED FACT (allegations): (a) faulty intake that fails to convey all relevant dispute information to the furnisher; (b) failure to pass consumer documentation to furnishers (despite a company policy requiring agents to attach it — "in some cases its agents fail to do so," ¶36); (c) uncritical acceptance of furnisher responses "even when … improbable or illogical on its face"; (d) confusing result notices; (e) reinsertion of previously-deleted tradelines for want of "basic matching tools." Hard numbers pleaded: **>2 million disputes** not forwarded to furnishers within five business days (January 2018–October 2021); **>100,000 disputed tradelines** deleted rather than reinvestigated within 30 days (February 2019–February 2020), some later reinserted; **>1,700 consumer files** left inaccurately reflecting joint-user status (June–December 2020). These are allegations; discovery is ongoing. Procedural posture (CONFIRMED FACT): original complaint filed 7 January 2025; a portion dismissed as time-barred (the "Discrete Violations," Jan 2018–Oct 2021) on 5 May 2025; second amended complaint 22 August 2025; **motion to dismiss denied 22 October 2025**; Experian answered 3 November 2025; CFPB motion to strike affirmative defenses granted in part 26 January 2026; discovery ongoing as of March 2026.

**Cost and incentive.** ANALYTICAL INFERENCE: disputes generate no revenue; the consumer is not the paying customer; the 30-day clock is fixed. The rational cost-minimising design is exactly what critics describe — code the dispute into two/three digits, forward via e-OSCAR, accept the furnisher's response, notify. At roughly US$0.57–a-few-dollars per dispute × >12m/year, the operation might cost on the order of low tens of millions of dollars annually (ANALYTICAL INFERENCE; not disclosed) — trivial against US$8,445m revenue, which is precisely the problem the CFPB alleges: the operation is *cheap by design*.

**Independent assessment.** Both framings are claims to be tested. The company's "we resolve the vast majority promptly" is true on throughput but silent on *quality*; the plaintiff-bar/NCLC "sham" framing is well-evidenced on mechanics (code-and-forward, no document review) but the legal question — whether that constitutes an unreasonable investigation under §611 — is what the litigation will decide. On the mechanics, the evidence supports the critics: a system that by default does not transmit the consumer's documents or free-text to the furnisher, and that accepts furnisher verification as dispositive, cannot conduct a substantive investigation of a factual dispute that the furnisher's own records may have caused.

---

#### III.10 Data Governance and Retention

| Jurisdiction | Core retention rule | Entity |
|---|---|---|
| US | FCRA §605: most adverse items 7 years; Chapter 7 bankruptcy 10 years; inquiries ~2 years | EIS |
| UK | ~6-year default retention of account data post-closure | Experian Limited |
| Brazil | Cadastro Positivo / LGPD-governed retention | Serasa S.A. |
| EU/EMEA | GDPR-governed | regional entities |

CONFIRMED FACT: NCAP removed civil judgments/most tax liens and delayed/limited medical-debt reporting. Consumer opt-outs include the prescreen opt-out (FCRA §604(e)/§615(d), via OptOutPrescreen.com, jointly operated). Controller/processor allocation: in the T-Mobile matter Experian acted as a processor for T-Mobile's data — a reminder that the same firm is controller of its bureau file but processor for client-held data, a distinction that matters for breach liability. Cross-border flows between US, UK, EU and Brazil rely on GDPR transfer mechanisms (SCCs / UK IDTA) and intragroup agreements; document-level specifics are **UNKNOWN**.

---

#### III.11 Reliability Engineering

Availability expectations for a real-time credit-decision API are effectively "always on" — a bureau outage stops lending decisions economy-wide. CONFIRMED FACT: Experian claims post-AWS improvements in "performance, security and reliability" and 60% faster data processing. Published SLAs, DR/RTO/RPO targets, the exact monthly batch window, and peak-capacity plans (month-end, tax season, Black Friday, prescreen campaigns) are **UNKNOWN** (not disclosed). No major public Experian bureau outage is established in this research. ANALYTICAL INFERENCE: a week-long Experian outage would be severe but not total — mortgage tri-merge would degrade to bi-merge, and many lenders could fail over to Equifax/TransUnion; the bureau oligopoly's redundancy is itself a systemic backstop. The segments most exposed are those Experian dominates (certain prescreen, auto and Experian-exclusive attribute/fraud services) and mortgage (where all three are required).

---

#### III.12 Employee Architecture

CONFIRMED FACT / THIRD-PARTY: ~25,200 (company) to 25,346 (Revelio, March 2026) employees across 32–33 countries; up ~10.8% since 2023 (Revelio) but down ~0.3% YoY in 2026. Major sites: Nottingham, Costa Mesa, Allen (Texas), São Paulo, Dublin and Hyderabad (India). The US is the single largest workforce share. Offshore/nearshore footprint concentrates technology (India) and dispute processing (offshore vendors, per NCLC). Attrition, union/works-council presence and skills mix are partly **UNKNOWN**; Revelio reports employee sentiment "neutral but improving."

**The 300bps labour-cost reduction.** CONFIRMED FACT (Vol I/II): labour cost fell to 32% of revenue, >300bps lower than two years earlier. ANALYTICAL INFERENCE: with headcount roughly flat-to-modestly-up while revenue grew 13% in FY26, the ratio decline is predominantly **operating leverage + mix shift + AI-driven productivity**, not headcount cuts. Revenue grew faster than heads; AI (Experian Assistant internally, EVA in consumer, genAI coding) raised output per head. This is genuine productivity, not workforce reduction.

---

#### III.13 Organisational Design and Decision Rights

The group is a **matrix**: four regional P&Ls × global business lines × a global product/technology organisation. CONFIRMED FACT: the FY26 report frames the four-region structure as "tailor[ing] products to local market needs while sharing innovation globally." Real operational power sits with (a) North America / EIS (the profit centre and File One owner) and (b) the global software/platform organisation (Ascend, Experian Software Solutions under Alex Lintner; AI under regional GMs such as Shri Santhanam in North America; COO Craig Boundy group-wide). CONFIRMED FACT (Vol I/II): there is **no dedicated board data-ethics/privacy committee** — meaning the highest-stakes decision (how data is used and how tightly it is matched/governed) is made in management, not at board-committee level. ANALYTICAL INFERENCE: the consumer (ConsumerInfo.com) and B2B (EIS) organisations share the same underlying File One data but are legally and commercially separated by permissible-purpose firewalls; tension between them is resolved operationally, not by a standing governance body.

---

#### III.14 Operating Leverage

| Process | Leverage class | Rationale |
|---|---|---|
| Data ingestion | Nearly automatic / sublinear | Batch Metro 2 intake scales with automation; marginal cost per record tiny |
| Identity matching | Nearly automatic | Find Consumer runs at ~1.8s/query; compute scales cheaply on cloud |
| Report delivery | Nearly automatic | API/cloud; marginal cost ≈ compute |
| Attribute computation | Sublinear | Precomputed/cloud; amortised across all clients |
| Model development | Step-fixed → falling | AI (Experian Assistant) converts months→hours; big fixed skill base, falling marginal |
| Dispute handling | **Linear-to-disproportionate** | Volume-driven labour + legal/litigation exposure; the one genuinely cost-growing, risk-laden process |
| Consumer membership servicing | Sublinear | Self-service + EVA displace human cost |
| Client integration | Step-fixed / linear | Manual, bespoke; grows with client count |
| Marketplace | Nearly automatic | Lead-routing scales with traffic |

**Where the 28.6% Benchmark EBIT margin comes from, operationally:** the near-zero marginal cost of matching and delivering a report against proprietary data already collected (90%+ of revenue is proprietary-data-derived), amplified by cloud (60% faster processing; dual-run costs falling from FY27) and AI productivity. Margin is highest where data is reused most (North America, 34.2% Benchmark EBIT margin) and lowest where the model is people/build-heavy or sub-scale (EMEA/AP, 6.7%).

**Is the dispute operation the one genuinely disproportionate cost?** ANALYTICAL INFERENCE: yes — not in raw dollars (it is cheap per unit) but in *risk-adjusted* cost. It is the only major process where volume, a hard legal deadline, litigation exposure and regulatory enforcement compound. The CFPB suit converts a low-dollar operation into a potentially high-dollar liability. It is the margin's structural soft spot.

---

#### III.15 Operations and Technology as Competitive Advantage

Scoring each asset (P=proprietary, HR=hard-to-reproduce, CR=cost-reducing, QI=quality-improving, RS=regulator-satisfying, C=compounds-with-volume):

| Asset | P | HR | CR | QI | RS | C | Verdict |
|---|---|---|---|---|---|---|---|
| Identity graph / matching engine | ✓ | ✓ | ✓ | ~ | ~ | ✓ | Core moat; QI is the weak axis (mixed files) |
| Ingestion scale + furnisher relationships | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ | Deepest moat — reciprocity (data-in-for-data-out) is self-reinforcing |
| Attribute library (2,100→6,000) | ✓ | ✓ | — | ✓ | ~ | ✓ | Strong; differentiator vs. raw data |
| Ascend platform | ~ | ~ | ✓ | ✓ | ✓ | ✓ | Strong but replicable (Equifax Ignite, TU equivalents) |
| Fraud stack (CrossCore/Precise ID) | ✓ | ~ | ✓ | ✓ | ✓ | ✓ | Strong; open-orchestration model invites partners |
| Dispute infrastructure | — | — | ✓ | ✗ | ✗ | ✗ | **Not a moat — a liability;** shared e-OSCAR, QI/RS negative |

**Comparison with Equifax and TransUnion.** Equifax completed a heavily-publicised ~US$1.5–3bn GCP transformation with a single data fabric and public CISO leadership; it is arguably ahead on the *narrative* of security-and-cloud remediation (forced by 2017). Experian's differentiator is the **Ascend platform-led commercial model** on AWS and its consumer franchise (215m+ members). TransUnion is the smallest of the three and the closest operational comparator on the bureau core. The three share e-OSCAR, Metro 2 and the tri-merge plumbing — meaning the *dispute and format infrastructure is an industry commons, not a competitive differentiator for any of them*.

---

#### III.16 Volume III Reconstruction

**(1) Operating-Model Diagram (text).** Furnishers (~10,000) → [Metro 2 batch, ~1.3bn/mo] → Ingestion/validation (DataArc-style QC) → **Find Consumer matching → File One (245m)** → {Report delivery API (~1.8s) | Attribute computation (2,100→6,000) | Scores: FICO/VantageScore/Experian} → Clients (lenders via API/batch/PowerCurve/Ascend; mortgage via reseller tri-merge). Parallel firewalled estates: Fraud (CrossCore/Precise ID) · Marketing (Experian Graph/Tapad) · Health (patient identity). Consumer loop: ConsumerInfo.com (215m members, EVA, Boost, Marketplace) ↔ File One (permissible-purpose gated). Dispute loop: Consumer → Online Dispute Center/mail/phone → ACDV → e-OSCAR → Furnisher §623 → determination → notice.

**(2) Ingestion Pipeline.** Furnisher certification → Metro 2 submission (monthly) → format/structural validation → identity/quality checks → matching → file update → exception queue (rate UNKNOWN).

**(3) Identity-Resolution Architecture.** Input identity (name/address/SSN/DOB/phone) → candidate retrieval → matrix of edits/tolerance rules (deterministic + probabilistic blend, thresholds UNKNOWN) → attach to file OR create new OR flag fragment. Failure modes: over-match→mixed file (7-of-9 SSN heuristic implicated historically); under-match→fragment/unscorable.

**(4) Database/Platform.** File One (US, EIS) · CAIS (UK) · Serasa DBs · illion DBs; all US/Brazil (ex-Health) on AWS (10-yr deal, June 2025); Ascend cloud-native; Health on legacy.

**(5) Delivery/Integration Map.** Real-time API · batch prescreen/portfolio · tri-merge via resellers · PowerCurve · Ascend Sandbox. High switching costs.

**(6) Consumer Operation Map.** Registration/Experian Go (ID+selfie) · AnnualCreditReport.com JV · freezes/alerts/locks · Boost (open banking) · EVA (LLM) · Marketplace pre-qual.

**(7) Model Governance/Explainability.** Explainable ML (monotonic GBMs + SHAP reason codes; patents 11,922,495 / 12,050,975 / 12,321,826) in-decision; genAI (Experian Assistant, EVA, Agent OS) for build/serve/support, fenced out of the decision; SR 11-7 MRM (Experian Assistant for MRM, ValidMind, "up to 70%" faster approvals).

**(8) Security Map.** Zero-trust program (2022 settlement-mandated) · SSN-minimisation · encryption/segmentation between estates · permissible-purpose access control as top vector · concentration risk on 245m files · no board data committee · CISO name UNKNOWN.

**(9) Dispute Production Line.** >1m/mo (>12m/yr) → ACDV (3-digit code) → e-OSCAR → §623 furnisher → determination → notice; documents not forwarded by default; offshore/automated; CFPB "sham" allegations (>2m not forwarded in 5 days; >100k deleted-not-investigated; reinsertion for want of matching tools).

**(10) Data Governance/Retention Matrix.** (See III.10 table.)

**(11) Reliability Assessment.** "Always-on" expectation; SLAs/DR UNKNOWN; oligopoly failover cushions a single-bureau outage; mortgage most exposed.

**(12) Employee/Site Map.** ~25,200–25,346; Costa Mesa/Nottingham/Allen/São Paulo/Dublin/Hyderabad; US largest; offshore for tech + disputes; 300bps labour-ratio fall = productivity/mix, not cuts.

**(13) Decision-Rights Map.** Matrix; power in NA/EIS + global software/AI org; data-use decided in management, not board committee.

**(14) Operating-Leverage Matrix.** (See III.14 table.) Margin from data reuse at near-zero marginal cost; dispute = the disproportionate risk-adjusted cost.

**(15) Operations Moat Assessment.** (See III.15 table.) Deepest moat = ingestion scale/furnisher reciprocity; weakest link = dispute infra (a shared liability).

**(16) Key Unknowns.** Match thresholds/architecture specifics; internal validation stage count; rejection/exception rates; dispute per-unit cost and offshore-vendor identity; CISO name; SLA/DR targets; certification scopes; cross-border transfer mechanisms at document level.

**(17) Ten Most Important Conclusions.**
1. Identity resolution is the enterprise's core operation and its origin of worst failures; it is *irreducibly* error-prone, but the error rate is a tunable policy choice Experian has under-optimised for accuracy.
2. The match-threshold incentive is asymmetric: looser matching raises fill/match rates lenders value while the cost of mixed files lands on non-paying consumers — a structural bias toward over-matching.
3. Ingestion scale plus furnisher reciprocity (data-in-for-data-out) is the deepest, most compounding moat — harder to replicate than any algorithm.
4. The dispute operation is a regulated industrial line built to minimise cost, not maximise substantive investigation; its default of not forwarding consumer documents is the mechanical heart of the CFPB case.
5. The dispute operation is the margin's soft spot — cheap per unit, disproportionate in risk-adjusted cost, now crystallised by live federal litigation.
6. The explainability constraint does not stop AI in credit — it channels it: explainable ML in the decision, generative/agentic AI in build/serve/support.
7. The 300bps labour-cost fall is genuine productivity and operating leverage (revenue +13%, heads roughly flat), aided by AI — not headcount reduction.
8. Cloud is now decisively AWS (10-year deal, June 2025) with claimed 60% faster processing — a different bet from Equifax's GCP single-data-fabric.
9. The identity graph is technically unified across credit/fraud/marketing/health, so the legal firewalls must be enforced at governance/access layers, not in the algorithm — a permanent control burden.
10. A one-week Experian outage would badly disrupt but not halt US lending: mortgage degrades to bi-merge and many lenders fail over to the other two bureaus — the oligopoly is its own backstop.

---

### TL;DR
- **Identity resolution is Experian's true core operation and its greatest fragility.** Attaching ~1.3bn monthly records to ~245m consumers via the "Find Consumer" engine into the File One database is irreducibly error-prone (the FTC's 2012 §319 study found 26% of consumers reported a potential material error and ~5% had errors that could raise their cost of credit); the *baseline* error rate is structural, but the *excess* rate — mixed files from loose matching and reinsertion of deleted tradelines — is an avoidable, cost-driven policy choice, now the subject of the CFPB's live suit (motion to dismiss denied 22 October 2025, discovery ongoing).
- **The dispute production line is a deliberately cheap, highly-automated, partly-offshored operation** handling >1m disputes/month at Experian alone, coding each into a three-digit ACDV, routing it through the shared e-OSCAR system to the furnisher, and by default *not* forwarding the consumer's documents — the mechanical heart of the CFPB's "sham investigations" allegation and the margin's structural soft spot (disproportionate in risk-adjusted, not dollar, terms).
- **The 28.6% margin comes from reusing already-collected proprietary data at near-zero marginal cost**, now amplified by a 10-year AWS cloud deal (June 2025; claimed 60% faster processing) and AI productivity (Experian Assistant, EVA); explainability (adverse-action reason codes via patented SHAP-based methods) bars opaque models from the *decision* but leaves generative/agentic AI free to accelerate model-building, servicing and documentation — where the 300bps labour-cost fall actually originates.

### Key Findings
- **Cloud is AWS.** CONFIRMED: 10-year "preferred cloud" + genAI partnership announced 19 June 2025; migration off mainframes; "reduced data processing time by 60%"; 100+ genAI use-cases. Equifax, by contrast, built its post-breach single data fabric on Google Cloud (~US$1.5–3bn).
- **Matching thresholds are tunable and cost-biased.** The 7-of-9-SSN mismerge heuristic (NCLC/*Apodaca*) and the CFPB's reinsertion allegation (no comparison of first-delinquency date, balances or original creditor) both show accuracy is limited by policy, not physics.
- **The dispute operation's economics explain its quality.** No revenue, a fixed 30-day clock, and reported vendor costs as low as US$0.57/dispute letter (NCLC) drive a code-and-forward design with minimal human discretion.
- **Explainability channels rather than blocks AI.** Patented reason-code generation (US 11,922,495 / 12,050,975 / 12,321,826) keeps decision models explainable; genAI is deployed in development, MRM (Experian Assistant for MRM, "up to 70%" faster approvals) and consumer servicing (EVA, ~85m users).
- **Governance gap.** No dedicated board data-ethics/privacy committee and an unnamed public CISO, against a 245m-file concentration risk and a 2022 zero-trust settlement.

### Details
Full mechanism-level analysis is in sections III.1–III.16 above, covering the operating model; the Metro 2 ingestion pipeline and NCAP public-record purge; the Find Consumer / File One matching engine and the mixed-file/fragmented-file error economics; the AWS/Ascend platform stack; delivery, tri-merge and consumer operations; the model-governance/explainability regime; the security posture and its litigation history; the e-OSCAR dispute production line and the CFPB's pleaded numbers; retention and cross-border governance; reliability; the workforce and the 300bps labour-cost analysis; decision rights; the operating-leverage classification; and the moat assessment versus Equifax and TransUnion.

### Recommendations
For a reader assessing Experian operationally (investor, regulator, counterparty), staged actions and the thresholds that would change them:
1. **Track the CFPB case as the single most material operational-risk item.** Benchmark: an adverse ruling or consent order requiring routine transmission of consumer documents/free-text and substantive human review would raise the dispute operation's unit cost by an order of magnitude and set an industry precedent binding Equifax and TransUnion too. A settlement without operational mandates would confirm the status quo.
2. **Watch for disclosure of matching-quality metrics.** Benchmark: if Experian (or a court in discovery) publishes mixed-file rates or tightens SSN-match thresholds (e.g., to 8-of-9 with a flag), that signals genuine accuracy investment; continued silence signals the cost-minimising equilibrium persists.
3. **Monitor cloud dual-run cost roll-off from FY27** as the near-term margin catalyst; benchmark against the claimed 60% processing-time reduction translating into disclosed cost savings.
4. **Distinguish AI productivity from AI decisioning in all company claims.** Treat genAI margin claims as real (build/serve/support) but treat any suggestion of genAI *in the credit decision* skeptically — the explainability constraint makes it unlikely and, if true, a regulatory red flag.
5. **Press for the CISO identity, certification scopes and DR/SLA disclosure** — their absence is itself a governance signal given the concentration risk.

### Caveats
- Experian publishes very little about internal systems; many architectural specifics (validation stage counts, match thresholds, rejection/exception rates, dispute unit cost, offshore-vendor identity, CISO name, SLA/DR targets, certification scopes, cross-border transfer instruments) are **UNKNOWN** and are labelled as such rather than invented.
- The CFPB's operational descriptions are **allegations** subject to ongoing litigation; the pleaded numbers (>2m disputes not forwarded in five days; >100k deleted-not-investigated; >1,700 mis-flagged joint-user files) are the Bureau's claims, not adjudicated facts.
- Several quantified accuracy and dispute-volume figures rest on the FTC's 2012 §319 study and the CFPB's 2012 white paper; no official cross-bureau update to the "~8m contacts / 32–38m items" dispute baseline has been published, and the CFPB now reports *complaints* rather than *disputes* — the two must not be conflated.
- Headcount figures blend a company statement (~25,200) with a third-party estimate (Revelio, 25,346) that may use a different consolidation basis.
- Some ROI and performance figures (Forrester TEI; "up to 70%"; "60%") are company or company-commissioned claims and are labelled COMPANY CLAIM.

*Volume III ends here. Volume IV not begun.*


---

# Part IV — Financial Statements, Revenue Architecture, Unit Economics & Capital

### Financial Statements, Revenue Architecture, Unit Economics & Capital

*Basis convention (binding): Experian reports under IFRS in US dollars with a 31 March year-end. "Benchmark" denotes the company's non-GAAP suite (Benchmark EBIT, Benchmark PBT, Benchmark EBITDA, Benchmark EPS). Every figure below is labelled statutory or Benchmark, and every growth rate is labelled organic / constant-currency (CER) / actual-rate. FY26 = year to 31 March 2026; FY25 = year to 31 March 2025; and so on. Evidence tags: CONFIRMED FACT, COMPANY CLAIM, THIRD-PARTY ESTIMATE, ANALYTICAL INFERENCE, HYPOTHESIS, UNKNOWN. Arithmetic is shown for every derived figure so the reader can audit it.*

---

### TL;DR (the core answer)

- **The 28.6% Benchmark EBIT margin is not made by a free input; it is manufactured by three things: oligopolistic pricing power in a three-firm US bureau market, operating leverage over a largely fixed data-and-compliance platform, and net (agent) revenue recognition on the consumer marketplace. FY26 profitability is *mostly* structural but is flattered by a non-durable US mortgage pricing windfall (mortgage revenue +45% on roughly flat volume) and depressed by cloud dual-run costs that roll off from FY27 — the two roughly offsetting.**
- **The Benchmark presentation is broadly fair on volatile financing items but flattering on the amortisation of acquisition intangibles (US$271m in FY26 and rising every year), which — for a company that acquires continuously — is in substance a permanent cost of strategy excluded from the headline number the market prices.** Thirty years of acquisition created clear value in the core (North America, Latin America and UK cash-generating units have never been impaired) but destroyed roughly US$232m of goodwill at the margin in EMEA/Asia Pacific (US$53m impaired in FY21, US$179m in FY23).
- **The single variable that most determines earnings is US Financial Services inquiry pricing, above all mortgage. Growth is capital-light organically but capital-heavy through M&A (US$792m in FY26) and an 8.6%-of-revenue capex load — so the "capital-light information business" label is only half true.** ROCE of 17.2% comfortably exceeds the ~8–9% cost of capital, and leverage of 1.7x net-debt/EBITDA sits below the 2.0–2.5x target range, leaving ample capacity for both buybacks and deals.

---

### Key Findings

1. **Scale and shape (FY26, CONFIRMED):** statutory revenue US$8,445m (+12% actual); ongoing revenue US$8,425m (+13% actual, +11% CER, +8% organic); Benchmark EBIT from ongoing activities US$2,407m at 28.6% margin; statutory operating profit US$2,045m; Benchmark PBT US$2,212m; statutory PBT US$1,951m (+26%); Benchmark EPS 179.8 US cents (+15% actual); statutory basic EPS 164.5 US cents (+29%); Benchmark operating cash flow US$2,221m at 93% conversion; Benchmark free cash flow US$1,583m; ROCE 17.2%; net debt US$5,179m at 1.7x Benchmark EBITDA.

2. **The margin is a mix story, not an input story.** North America (66.3% of revenue) earns 34.2%; EMEA/Asia Pacific earns 6.7%. The dispersion is driven by fixed-cost absorption, not pricing — the same data/platform cost base spread over vastly different revenue.

3. **The FY26 mortgage windfall is a pricing event, not a franchise event, and it is politically exposed.** FICO's foundational tri-merge score price rose from US$1.80 (late 2022) to US$30 (2026) — a 1,567% increase per the Community Home Lenders of America — and total per-loan credit-report cost rose from about US$50 in 2022 to roughly US$540 in 2026. Experian captured bureau/reseller mark-up on top of the US$4.95 FICO royalty pass-through.

4. **Benchmark-to-statutory gap is persistent and partly structural.** The FY26 bridge from Benchmark PBT US$2,212m to statutory PBT US$1,951m is a US$261m deduction, dominated by acquisition-intangible amortisation (US$271m) — an item that has risen every year (US$174m FY22 → US$211m FY25 → US$271m FY26) because the company acquires every year.

5. **The acquisition programme is value-creating in the core and value-destructive at the edge.** Acquired goodwill has been impaired only twice in ~15 years, both in EMEA/Asia Pacific (US$53m FY21, US$179m FY23); the North America, Latin America and UK cash-generating units have never been impaired.

6. **The regulatory paradox is financial, not merely legal.** The dispute machinery the CFPB alleges is inadequate is deliberately run at very low unit cost (as low as US$0.57 per dispute letter across >12 million disputes a year), and that low cost is itself a contributor to the near-30% margin. Mandated remediation is the single most material adverse contingency, more than any fine.

---

### Details

#### IV.1 Multi-Year Financial History

**Statutory revenue (US$m, actual rates) [CONFIRMED — company results; older years via Macrotrends]:** FY19 4,861; FY20 5,179; FY21 5,372; FY22 6,288; FY23 6,619; FY24 7,097; FY25 7,523; FY26 8,445. Compound growth FY19→FY26 ≈ 8.2% p.a. (8,445 / 4,861 = 1.737 over 7 years → 1.737^(1/7) − 1 = 8.2%).

**Statutory profit before tax (US$m) [CONFIRMED]:** FY20 942; FY21 1,077; FY22 1,447; FY23 1,174; FY24 1,551; FY25 1,549; FY26 1,951. The FY23 dip reflects a US$179m EMEA goodwill impairment and adverse financing remeasurements; the FY26 jump reflects revenue growth plus a swing in financing fair-value remeasurements from −US$85m (FY25) to +US$101m (FY26) and lower restructuring.

**Benchmark EBIT margin (ongoing) [CONFIRMED]:** FY22 ≈26.2%; FY24 27.6%; FY25 28.1%; FY26 28.6%. A steady ~50–90bps annual climb, management-attributed to operating leverage, AI productivity and Consumer Services scaling.

**Benchmark EPS (US cents) [CONFIRMED]:** FY22 124.5; FY24 144.2; FY25 156.9; FY26 179.8. **Statutory basic EPS (US cents):** FY22 127.5; FY25 127.6; FY26 164.5.

**Benchmark EBITDA (US$m) [CONFIRMED, company cash-flow summary]:** FY25 2,630; FY26 3,010 (Benchmark EBIT 2,397 + amortisation/depreciation 613).

**ROCE (post-tax, Benchmark) [CONFIRMED]:** FY24 ~17%; FY25 16.6%; FY26 17.2%. **Net debt/Benchmark EBITDA [CONFIRMED]:** 1.7x in FY24, FY25 and FY26.

**Structural vs presentational:** The 2020–2022 US mortgage boom lifted transactional bureau revenue; the 2023–2025 rate-driven bust cut volumes, but from FY24 Experian offset volume weakness with tri-merge price escalation. Two FY26 presentational changes must be separated from economics: (a) certain Latin America and EMEA/AP B2B lines were reclassified as "exited activities" (US$20m revenue in FY26 vs US$48m in FY25, with a US$10m operating loss removed to arrive at ongoing Benchmark EBIT of US$2,407m vs total US$2,397m); and (b) from 1 April 2025 the B2B line was split into Financial Services and Verticals. Neither changes the underlying economics.

#### IV.2 Revenue Taxonomy and Quality

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

#### IV.3 Revenue Recognition and Accounting Judgements

[CONFIRMED, Revenue note]: Per-transaction bureau revenue is recognised at the point of delivery. Hosted software licences are recognised over the service period, creating contract liabilities; on-premise licences are released on delivery completion; support/maintenance is released over the maintenance term. **Consumer Services marketplace and referral revenue is recognised NET** — Experian acts as an agent, recognising only the referral/commission fee, not the gross value of the credit or insurance product placed. This is material: gross presentation would inflate reported revenue and depress the reported margin; net presentation is a structural reason Consumer Services shows a 29.6% Benchmark EBIT margin. The **FICO royalty (US$4.95/score under the mortgage performance model, or US$10 traditional) is a genuine cost of sale / pass-through** [CONFIRMED, FICO]. The accounting judgements that most affect reported results are: (1) the value and economic life of acquisition intangibles (drives the amortisation excluded from Benchmark); (2) the capitalisation and amortisation life of internally generated software (3–10 years, average ~5); and (3) the principal-vs-agent (gross/net) marketplace judgement.

#### IV.4 Pricing Economics and the Mortgage Question

**Mechanism:** a conforming mortgage requires a "tri-merge" — a pull from all three bureaus. Per the Community Home Lenders of America (March 2026 white-paper addendum), *"FICO's foundational price for a tri-merge score escalated from $1.80 in late 2022 to $30 today, marking a 1,567% increase,"* while *"total credit report costs associated with closing a conventional loan have risen from about $50 in 2022 to roughly $540 in 2026"* [CONFIRMED, CHLA via HousingWire / NMP]. FICO's own disclosure: the wholesale royalty is US$4.95/score under the performance model (plus a US$33 per-borrower funded-loan fee) or US$10/score traditional; FICO states that *"any amounts charged beyond … FICO's $4.95 per-score royalty … is collected by the credit bureaus or other parties but not by FICO"* [CONFIRMED]. So the escalation captured by Experian is the **bureau mark-up and reseller bundle**, not the FICO royalty.

**FY26 outcome:** North America mortgage-profile revenue grew ~45% (management indicated "45% to 50%") on roughly flat volumes — a near-pure pricing effect [CONFIRMED]. This sits inside North America Financial Services (FY26 US$2,363m, +14% total).

**Competitive/regulatory threat:** the FHFA authorised VantageScore 4.0 for conforming mortgages on 8 July 2025 [CONFIRMED]. By the Q1 FY27 update, per CFO Lloyd Pitchford, *"eleven out of the 15 largest mortgage lenders are also using VantageScore 4.0, now reaching close to 30% of the U.S. mortgage market"* [COMPANY CLAIM]. Deep Future Analytics, in its study "Economic Benefits of Score Market Competition for Conforming Mortgages" (Feb 25 2026), estimated *"an estimated $648 million in savings in the first full year"* under full adoption and *"up to $2.5 billion in cumulative cost savings over a five-year period,"* with a March 18 2026 update raising the first-year figure to *"more than $930 million"* [THIRD-PARTY ESTIMATE].

**Scenario read [ANALYTICAL INFERENCE]:** (i) *Price normalisation* would reverse much of the FY26 uplift and is the single biggest threat to the FY26 growth optics; (ii) *volume recovery* would partly offset — management guides modestly lower mortgage volumes into FY27; (iii) *VantageScore share gain* is largely neutral-to-modestly-negative for Experian because Experian sells both scores and the underlying data pull persists regardless of which score is calculated — the economics that shift are chiefly FICO's royalty, not Experian's bureau revenue. The durable risk is political: a per-loan cost of ~US$540 on a government-sponsored mortgage market is an obvious target for the FHFA, the MBA and the CHLA.

**Beyond mortgage:** the same pricing muscle appears in analytics/platform renewals (double-digit contract-value uplifts) and Serasa. Pricing power derives from the difficulty of replicating regulated historical datasets, switching costs once embedded in a client's decisioning workflow, and the three-firm structure of the US bureau market.

#### IV.5 The Cost Architecture of a Zero-Input-Cost Business [PRIORITY DEPTH]

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

#### IV.6 Unit Economics Across Incompatible Units

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

#### IV.7 Segment Economics

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

#### IV.8 The Statutory-to-Benchmark Forensic Reconciliation [PRIORITY DEPTH]

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

#### IV.9 Balance Sheet Teardown

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

#### IV.10 Cash Flow and Conversion

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

#### IV.11 Capital Intensity and Return on Capital

ROCE 17.2% = Benchmark EBIT less tax at the Benchmark rate, divided by average capital employed (US$10,720m at year-end; average of ~US$10,226m). Sanity check: Benchmark EBIT US$2,397m × (1 − 25.5%) = US$1,786m; 1,786 / ~10,226 ≈ 17.5% — consistent with the 17.2% reported on the precise averaging basis [ANALYTICAL INFERENCE confirms the disclosed figure].

The goodwill-heavy balance sheet (US$7,261m goodwill, US$3,078m other intangibles) depresses reported ROCE. **Return on tangible capital [ANALYTICAL INFERENCE]:** stripping the US$7,261m of goodwill from the US$10,720m capital employed leaves ~US$3.46bn of tangible/working capital; US$1,786m post-tax Benchmark EBIT on that base implies a return above 50%. This is the mechanical signature of a business whose true "capital" is off-balance-sheet data, and whose on-balance-sheet capital is largely the accounting price paid for acquisitions. **Is growth capital-light? Organically, yes; in aggregate, no** — the 8.6% capex ratio plus ~US$800m/yr of M&A mean incremental growth consumes real capital. The "capital-light" label describes the *organic core*, not the *reported enterprise*.

#### IV.12 Debt, Funding and Liquidity

Net debt US$5,179m at 31 March 2026 (up from US$4,684m), at 1.7x Benchmark EBITDA — **below the stated 2.0–2.5x target range** [CONFIRMED]. Debt is issued principally through **Experian Finance plc** (a US$6bn Euro Medium-Term Note programme, the former GUS financing vehicle) and **Experian Europe DAC**, both guaranteed by Experian plc [CONFIRMED, Moody's]. Credit ratings: **Baa1 (Moody's) / BBB+ (S&P)**, with a stated policy to maintain "a strong investment grade credit rating (BBB+ / Baa1 or above)" [CONFIRMED]. FY26 net interest US$185m at an average rate of ~3.6% (benefiting from a rate-hedging programme); FY27 guided to US$250–260m (reflecting acquisition financing and Own Up/Konfir, both closed 1 April 2026). Undrawn committed facilities US$2.5bn. **The leverage policy does not currently constrain M&A or buybacks** — running below the bottom of its own range, Experian has explicit headroom, which is why it could simultaneously spend US$792m on acquisitions, pay a US$590m dividend and execute US$725m of buybacks in FY26.

#### IV.13 The Litigation and Regulatory Contingency

**CFPB v. Experian Information Solutions, Inc.** (filed 7 January 2025, Central District of California) alleges "sham investigations" of disputes under FCRA. Procedural history [CONFIRMED, CFPB docket/CourtListener]: motion to dismiss granted in part 5 May 2025; amended complaint 6 June 2025; further dismissal 6 August 2025; second amended complaint 22 August 2025; **motion to dismiss denied 22 October 2025**; Experian answered 3 November 2025; the CFPB's motion to strike affirmative defenses was heard 30 January 2026; **jury trial set for 21 September 2026**. Experian calls the suit "completely without merit" and states it does "not expect this to have any material impact on our business" [COMPANY CLAIM].

**Provision status [ANALYTICAL INFERENCE]:** total balance-sheet provisions are only US$18m current + US$7m non-current — consistent with routine matters and indicating **no material provision has been recognised for the CFPB case**, which is standard where an outflow is not assessed as probable and reliably estimable. The full contingent-liabilities note (in AR2026) would carry the qualitative disclosure [not in the preliminary announcement — flagged].

**Historical cost benchmarks [CONFIRMED]:** the 2012/2015 breaches produced a 40-state multistate settlement of **US$13.67m with Experian** (November 2022), alongside a separate **US$2.43m settlement with T-Mobile**; FCRA class actions have settled in the low tens of millions (e.g., Hill-Green "Fraud Shield" ~US$22.45m; a T-Mobile breach class action ~US$22m).

**Outcome model [HYPOTHESIS]:** (i) *Dismissal/settlement with a civil money penalty* — tens of millions, immaterial to a group earning US$2.2bn Benchmark PBT; (ii) *Adverse judgment with a penalty plus redress* — potentially low hundreds of millions, a one-off, still manageable; (iii) **the material scenario — mandated remediation of the dispute system.** Volume III established that the dispute operation is deliberately low-cost (as low as US$0.57 per letter). A court-mandated requirement to conduct substantive, human-reviewed investigations across >12 million disputes a year could raise the run-rate cost by an order of magnitude — the recurring margin risk, not the one-off fine, is the real financial exposure. This is the point where the report's central paradox becomes a P&L line.

#### IV.14 Capital Allocation and Return on a Thirty-Year Acquisition Programme [PRIORITY DEPTH]

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

#### IV.15 One Dollar of Group Revenue (FY26, per US$1 of statutory revenue US$8,445m)

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

#### IV.16 Economic Driver Tree

Bureau revenue = files held × permissible-purpose inquiries per file × price per inquiry. FY26 demonstrated the **price** term dominating (mortgage +45% on flat volume). The full frame:

> (files × inquiries/file × price/inquiry) + platform/software subscription + (members × [subscription conversion × ARPU + referrals × fee]) + vertical revenue (Health, Automotive, Marketing) − labour − technology/cloud − data operations − disputes/compliance − FICO royalty − marketing = Benchmark EBIT − amortisation of acquisition intangibles − exceptionals − interest − tax = statutory profit.

**The five variables explaining most outcomes:** (1) US Financial Services inquiry pricing (above all mortgage); (2) US origination volumes; (3) Consumer marketplace referral volume × fee; (4) labour cost as a % of revenue (the productivity lever); (5) cloud dual-run roll-off. Secondary: Brazilian real translation, acquisition-intangible amortisation, net interest.

#### IV.17 Scenario and Sensitivity Analysis [ANALYTICAL INFERENCE unless stated]

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

#### IV.18 Profitability Decomposition and Normalisation

FY26 Benchmark EBIT US$2,397m decomposes into: (1) **structural earnings power** — the recurring bureau, platform, verticals and Consumer base; (2) **the mortgage pricing windfall** — a boost inside the +45% NA mortgage line, not durable; (3) **cloud dual-run costs still carried** — a self-reversing headwind from FY27; (4) **acquisition contribution** — ~1% of revenue, ~50bps margin-dilutive near-term; (5) **FX** — a 2% Benchmark EPS tailwind in FY26. **Normalised through-cycle Benchmark EBIT margin [HYPOTHESIS]: ~28–29%.** The FY27 guidance (double-digit Benchmark EPS growth, organic revenue 6–8%, ~+50bps margin at CER, capex ~8% trending to 7%, Benchmark tax ~26%) implies management believes the cloud roll-off and AI productivity will more than offset mortgage normalisation — i.e., management itself treats the mortgage windfall as impermanent and is guiding to structural, not windfall, expansion.

---

### Recommendations

**Stage 1 — Underwrite the structural core, discount the windfall (now).** Value Experian on **statutory** and normalised numbers, not on the Benchmark headline: apply at least the US$271m acquisition-intangible amortisation as a real recurring cost, and treat the FY26 mortgage +45% as a one-off pricing event, not a run-rate. Anchor to organic growth of 6–8% and a normalised ~28–29% margin. *Benchmark that would change this view:* if mortgage pricing holds AND VantageScore fails to compress bureau economics through FY27, raise the durable growth assumption.

**Stage 2 — Track five telltales quarterly.** (i) US mortgage-profile revenue growth (watch for the +45% decaying toward volume-led single digits); (ii) VantageScore adoption among top-15 lenders (already ~30% of the market — a share above ~50% would begin to matter); (iii) labour cost as a % of revenue (the 31.8% figure falling further validates the AI thesis; a stall is a margin warning); (iv) the current-receivables trend (the FY26 +37% jump vs +12% revenue is a DSO flag); (v) cloud dual-run roll-off actually landing in the FY27 P&L as guided. *Thresholds:* a labour ratio rising back above ~33%, or receivables growth persistently outpacing revenue by >15pts, would each warrant a quality-of-earnings downgrade.

**Stage 3 — Price the CFPB tail explicitly.** Do not model the CFPB matter as a binary fine. Model the **remediation scenario**: estimate the incremental cost of substantive dispute investigations across >12m disputes/year and haircut the margin accordingly as a low-probability, high-impact recurring cost. *Benchmark:* a summary-judgment or settlement that leaves the low-cost dispute process intact removes most of the downside; any consent order mandating process change is a structural margin event, not a one-off.

**Stage 4 — Judge M&A on the impairment scoreboard, not the pipeline.** Continue to credit core-market bolt-ons (never impaired) but treat further EMEA/AP expansion sceptically given the ~US$232m impairment record there. *Benchmark:* any new goodwill impairment outside EMEA/AP would be a first — and a signal that the acquisition machine is over-reaching into the profitable core.

**Stage 5 — On the buyback, require continued per-share compounding.** The US$1bn programme (to 30 June 2027) creates value only if Benchmark EPS keeps compounding double-digit. *Threshold:* if organic growth slips below ~6% while the mortgage windfall reverses, buying back at a mid-30s multiple becomes value-neutral-to-destructive and cash should tilt back to debt reduction or higher-return M&A.

---

### Caveats

- **The non-GAAP question is unresolved by design.** The market prices Benchmark EPS (179.8c) at a 9.3% premium to statutory (164.5c). This report treats the acquisition-intangible amortisation and recurring acquisition expenses as real economic costs; readers who accept the company's framing will reach a rosier view. The disagreement is analytical, not factual.
- **Pricing opacity forces inference.** Per-inquiry bureau rates and marketplace referral fees are confidential; revenue-per-inquiry and revenue-per-referral are therefore labelled UNKNOWN rather than estimated. Unit economics in IV.6 are derived transparently and flagged as inference.
- **Preliminary-announcement basis.** Figures are from the FY26 results announcement (approved 19 May 2026) and prior-year announcements; the full AR2026 notes (segmental detail, the acquisition-vs-internally-generated split of the US$3,078m intangibles balance, the 31 March 2026 contract-liability/deferred-income balance, and the qualitative contingent-liabilities disclosure) were not all independently accessible and are flagged UNKNOWN where relevant. The FY26 goodwill balance (US$7,261m) and intangibles (US$3,078m) are taken from the published balance sheet; the goodwill *impairment history* (US$53m FY21, US$179m FY23, both EMEA/AP; none in NA/LatAm/UK) is confirmed from the AR2022/FY23/FY24 notes.
- **Forward-looking items are labelled.** FY27 guidance, the cloud dual-run roll-off, the VantageScore savings estimates (Deep Future Analytics US$648m first-year / US$930m updated / US$2.5bn five-year) and all scenario outputs are projections, not realised results, and are tagged COMPANY CLAIM, THIRD-PARTY ESTIMATE, ANALYTICAL INFERENCE or HYPOTHESIS accordingly.
- **Revenue quality is partly a legal question.** Multiple streams depend on legal permissions persisting — FCRA permissible purpose, UK GDPR legitimate interests, LGPD Article 7(X). The medical-debt precedent shows data categories can be removed from the file by legislation or regulation; where that happens, the associated revenue is contingent, not guaranteed.

*Work paused at the completion of Volume IV. Volume V has not been begun.*


---

# Part V — Management, Culture, Competition, Moat, Risk & Strategic Evolution

## VOLUME V — Management, Culture, Competition, Moat, Risk & Strategic Evolution

*Research date: 9 August 2026. Established context from Volumes I–IV is treated as verified. Evidence labels: CONFIRMED FACT / COMPANY CLAIM / THIRD-PARTY ESTIMATE / ANALYTICAL INFERENCE / HYPOTHESIS / UNKNOWN. Basis discipline observed throughout: statutory vs Benchmark, and organic vs constant-currency vs actual-rate, are distinguished; total revenue and ongoing-activities revenue are kept separate. This is the concluding volume and is written to be the least deferential: financial excellence is not assumed to equal strategic invulnerability, and the moat is tested rather than asserted.*

---

### V.1 Institutional Architects and the Two Lineages (replaces Founder Analysis)

Experian has no founder. It is the 1996 fusion of two dissimilar corporate cultures, and almost every strategic characteristic of the modern group can be traced to one lineage or the other.

**The TRW lineage (the American bureau).** [CONFIRMED FACT] The US business began as Credit Data Corporation, founded in Detroit in 1964 by Dr Harry C. Jordan to centralise computerised credit records. TRW Inc. — a Cleveland aerospace, automotive and electronics conglomerate descended from the 1901 Cleveland Cap Screw Company — acquired CDC in 1968, renaming it TRW Information Systems & Services and giving it national scale and engineering capital. By the mid-1980s TRW held files on roughly 90 million individuals and was the dominant US bureau, though it suffered a 1984 password-theft breach and 1991 accuracy lawsuits that settled with commitments to free credit disclosures. In September 1996 TRW spun off Information Systems & Services to a buyout group led by Bain Capital and Thomas H. Lee, who paid roughly US$1.0–1.1bn and christened it "Experian."

**The CCN lineage (the British bureau).** [CONFIRMED FACT] In 1980 Great Universal Stores (GUS) — a British mail-order and retail conglomerate whose brands included Burberry — commercialised its in-house credit-checking operation as CCN in Nottingham, to manage mail-order credit risk. CCN became the UK's largest credit-reference agency and had wanted to buy TRW's information business for years.

**The fusion (November 1996).** [CONFIRMED FACT] Weeks after the Bain/Thomas H. Lee buyout closed, GUS offered to buy the newly-formed Experian; the buyout group flipped it for roughly US$1.7bn, netting about US$500m in weeks (Thomas H. Lee and Bain each roughly tripled US$100m stakes). GUS merged Experian with CCN, adopted the Experian name group-wide in 1997, and ran the company from two headquarters — Nottingham and Orange (later Costa Mesa), California.

**Analytical reading of the two lineages [ANALYTICAL INFERENCE].** The path dependencies are visible today: (i) the *engineering-and-scale orientation* and appetite for regulatory combat descend from TRW's US bureau, which had operated at national scale and litigated accuracy disputes since the 1970s; (ii) the *marketing-data and consumer-segmentation instinct* descends from CCN, which grew out of a retailer's need to profile customers — the very capability the ICO later challenged; (iii) the *serial-acquisition, portfolio-conglomerate habit* is a direct inheritance of GUS, itself a holding company; (iv) the dual-HQ structure (Nottingham + Costa Mesa, later + São Paulo, now legally domiciled in Dublin) is the institutional residue of a merger of equals that never fully picked a home.

**The 2006 demerger.** [CONFIRMED FACT] Experian demerged from GUS and listed on the LSE on 10 October 2006. **John Peace** — who had built CCN inside GUS from 1980 — became Experian's first chairman (later also chairing Standard Chartered and Burberry). **Don Robert** (CEO 2005–2014, then Chairman 2014–2019) drove the international expansion, above all Brazil. **Brian Cassin** joined as CFO in 2012 and became CEO in 2014.

**Beliefs consistently revealed in strategy [ANALYTICAL INFERENCE, HIGH CONFIDENCE].** (1) *Own the bureau, then build on it* — Robert's stated rationale for Serasa in 2007 was "owning market-leading credit bureaux in key markets." (2) *Go direct to the consumer early* — Experian built a direct-to-consumer arm long before most bureaus; it now reports over 215 million free members globally. (3) *Build platforms, not just sell data* — Ascend is deliberately a platform with switching costs, not a data feed. (4) *Tolerate regulatory conflict* — the company litigated both the ICO and the CFPB rather than settling. These four beliefs are the strategic DNA of the group and recur throughout this volume.

---

### V.2 Current Management Team

**CEO — Brian Cassin (CEO since 2014; previously CFO 2012–2014).** [CONFIRMED FACT] A former investment banker (Greenhill), Cassin has now led Experian for roughly twelve years and delivered FY26 as "a record year" — Benchmark EPS +15%, organic revenue +8%, ROCE 17.2%. His long tenure is both an asset (consistency, credibility on the medium-term framework) and a governance watch-item: [ANALYTICAL INFERENCE] succession is not visibly telegraphed, and the CFO is the obvious internal heir.

**CFO — Lloyd Pitchford.** [CONFIRMED FACT] Long-serving, highly regarded by the sell-side, and the public voice on capital discipline, the Benchmark framework, AI-driven productivity ("stable headcount despite 8% organic growth"), and margin progression. The Cassin–Pitchford axis is the real operating core of the company. [ANALYTICAL INFERENCE] The durability of this partnership is a genuine key-person concentration.

**Chair transition — Mike Rogers → Adam Crozier (at the 22 July 2026 AGM).** [CONFIRMED FACT] Rogers retires after nine years on the board (seven as chair). Crozier joined as non-executive director and chair-designate on 12 May 2026 and chairs from the AGM. Crozier is simultaneously chair of **BT Group** (which he is retaining) and of **Kantar** (a marketing-data and analytics business), and previously chaired Whitbread and ASOS and was a NED of Sony. Senior Independent Director **Alison Brittain** led the search; **Caroline Donahue** also steps down at the 2026 AGM.

**Assessment of the Crozier appointment [ANALYTICAL INFERENCE].** The signal is *consumer-and-data-marketing*, not credit. Crozier's career is brand-led consumer businesses (ITV, Royal Mail, Whitbread, ASOS) and, critically, **Kantar** — a data-and-analytics-for-marketing company structurally adjacent to Experian Marketing Solutions and the Experian Graph. This is consistent with a board that increasingly sees Experian as a consumer-data-and-marketing-and-analytics company rather than a wholesale credit utility. The retained BT and Kantar chairmanships raise a legitimate **over-boarding / bandwidth question** for a FTSE-100 chair, which proxy advisers may flag. His media/telecoms background brings little credit-bureau or FCRA-specific regulatory expertise — a gap given the CFPB trial.

**The absence of a dedicated board data-ethics / privacy committee [CONFIRMED FACT; ANALYTICAL INFERENCE].** For a company whose entire revenue base is contingent on data-use permissions (FCRA permissible purpose, UK GDPR legitimate interests, LGPD Art. 7(X)), the absence of a dedicated board-level data-ethics or privacy committee is a deliberate governance choice; data-use risk is handled within existing audit/risk structures. [ANALYTICAL INFERENCE] Given that data permissions are the single largest latent risk to the franchise, this is the most questionable single feature of Experian's governance architecture — defensible only if one believes (as management evidently does, having beaten the ICO decisively) that operational compliance is strong enough not to need board-level ring-fencing.

**Compensation structure [CONFIRMED FACT / ANALYTICAL INFERENCE].** Executive awards run through a Co-Investment Plan and Performance Share Plan; the May 2026 grants to Cassin (reference price 2,646.664p) and Pitchford (2,573.00p) comprise invested shares plus larger conditional matching and performance shares vesting on performance conditions. [ANALYTICAL INFERENCE] Because the headline performance metric emphasises **Benchmark EPS growth**, and Benchmark EPS *excludes* the rising amortisation of acquisition intangibles (US$271m in FY26 and rising every year), the incentive structure rewards acquisitions and buybacks in a way statutory EPS would not. This is analysed in V.5.

---

### V.3 Management System and Governance in Practice

**The matrix.** [ANALYTICAL INFERENCE, from disclosures] Experian runs a regional P&L structure (North America, Latin America, UK&I, EMEA/AP) crossed with global product lines (Financial Services / B2B, Verticals, Consumer Services) and global platforms (Ascend, PowerCurve). Real power sits with **North America** — US$5,587m revenue at 34.2% margin, the dominant profit centre and the home of the FCRA bureau (Experian Information Solutions, Inc., Ohio) — and with the **central CEO/CFO axis** that controls capital allocation.

**How data-use decisions are escalated [PARTIAL UNKNOWN].** The precise internal escalation path for contested data uses is not publicly disclosed [UNKNOWN]. What is observable: the company chose to litigate the ICO matter to the Upper Tribunal and won, implying data-use decisions are made with high legal confidence and central legal control, not devolved to product teams.

**Coordinating the two opposed customer bases.** [ANALYTICAL INFERENCE] The B2B business sells lenders the ability to assess consumers; the Consumer Services business sells consumers tools to improve their standing with lenders, and monetises them via marketplace referrals back to those same lenders. These interests are partly opposed (a consumer disputing a tradeline is a cost to B2B but a service to Consumer). The coordination mechanism is that **both sit on the same underlying data asset** and both ultimately monetise the lender relationship — the consumer app is, in revenue terms, a lead-generation channel for lenders. This is the structural tension Volume II established, managed by keeping the businesses organisationally separate while sharing the data spine.

**Capital-allocation governance.** [CONFIRMED FACT] FY26: US$792m of acquisitions, US$725m of buybacks (plus a new US$1bn buyback announced with FY26 results), a progressive dividend (interim +10%), net debt 1.7x Benchmark EBITDA (below the 2.0–2.5x target). [ANALYTICAL INFERENCE] The below-target leverage plus the fresh US$1bn buyback signals a company generating more cash than it can redeploy into acquisitions at acceptable prices — a "problem" of strength, but also evidence that organic reinvestment opportunities are not large enough to absorb the free cash flow (US$1,583m, 93% cash conversion).

---

### V.4 Culture — Declared versus Revealed

| Declared value | Revealed behaviour | Verdict |
|---|---|---|
| "Financial health" & inclusion (Boost, Go, United for Financial Health) | Genuine free-membership scale (215m+); but the same members are monetised three ways and the marketplace is placement-paid | [ANALYTICAL INFERENCE] Partly real, partly a customer-acquisition narrative |
| Consumer champion | US mortgage revenue +45% on flat volumes — pure pricing; dispute operation run at ~US$0.57/letter | [ANALYTICAL INFERENCE] Consumer orientation is real in product, weaker in pricing and dispute economics |
| Responsible data steward | Beat the ICO decisively; but no board data-ethics committee | [ANALYTICAL INFERENCE] Confident, compliance-led, not precautionary |
| Innovation / engineering | AWS 10-year deal, Ascend, SHAP explainability, AI in model-dev | [CONFIRMED FACT] Genuinely strong engineering orientation |
| Long-termism | 100% renewal of top NA FS accounts, durations +~10% to >4 years | [CONFIRMED FACT] Real client stickiness |

**Risk appetite:** high on regulatory conflict (litigated ICO and CFPB), disciplined on capital. **Regulatory posture:** combative and confident, backed by a genuine win record. **Central contradiction [ANALYTICAL INFERENCE]:** Experian markets itself as a consumer financial-health champion while (a) running the dispute operation — the one process that most directly determines whether a consumer's file is accurate — at deliberately minimal unit cost, and (b) extracting a pricing windfall from mortgage borrowers who cannot shop for a bureau. The CFPB case sits precisely on this fault line. *Employee evidence is not relied upon here [UNKNOWN as to representativeness].*

---

### V.5 Incentive Architecture

- **Benchmark EPS as the lodestar [CONFIRMED FACT + ANALYTICAL INFERENCE].** Benchmark PBT (US$2,212m) excludes amortisation of acquisition intangibles (US$271m FY26, rising: US$174m FY22 → US$211m FY25 → US$271m FY26). Because executive LTIP metrics centre on Benchmark EPS, **acquisitions are "free" in the incentive currency**: the goodwill/intangible amortisation they create never touches the number executives are paid on. This structurally biases the company toward serial acquisition and buyback (which mechanically lifts EPS) over organic quality investment. This is the single most important incentive distortion in the company.
- **The dispute operation [ANALYTICAL INFERENCE, HIGH CONFIDENCE].** Dispute quality generates no revenue; every dollar of cost reduction in the >12m-disputes-a-year machine flows straight to the 28.6% Benchmark EBIT margin. The incentive is therefore to minimise dispute cost, not maximise investigation quality — exactly the behaviour the CFPB alleges. The incentive and the litigation are two views of the same mechanism.
- **Sales incentives where buyer = supplier [ANALYTICAL INFERENCE].** In the bureau, the lender is both the customer and the (free, reciprocity-bound) data furnisher. This dampens price competition on data-in and concentrates monetisation on data-out (scores, attributes, decisioning).
- **Consumer marketplace [CONFIRMED FACT].** Experian is paid on placement/referral. The incentive is to optimise conversion and lender payout, which can diverge from surfacing the objectively best consumer offer.

**What the system rewards:** EPS-accretive M&A, buybacks, margin protection, client retention. **What can be gamed:** Benchmark adjustments; dispute-cost minimisation. **Where incentives conflict with consumers:** dispute quality and marketplace placement.

---

### V.6 Competitive Universe — Per Business Line

#### (a) Consumer credit bureau (US tri-opoly)
[CONFIRMED FACT] Equifax, Experian, TransUnion. Specialty/alternative: Innovis (the "fourth bureau"), LexisNexis Risk Solutions, Clarity Services, FactorTrust (the latter two owned within the big three / TransUnion). **Why the three-firm structure is stable [ANALYTICAL INFERENCE]:** reciprocity (furnishers supply all three or the data is worth less), FCRA compliance scale, matching engines built over decades, and mutual co-ownership of VantageScore. Entry is effectively impossible (see V.10).

#### (b) Credit scores — FICO vs VantageScore
[CONFIRMED FACT] FICO is simultaneously **supplier** (its score rides on the bureaus' tri-merge), **partner** (bureaus distribute it) and **rival** (VantageScore, co-owned equally by the three bureaus, competes with it). FHFA authorised **VantageScore 4.0** for conforming mortgages on 8 July 2025; by the Q1 FY27 update, eleven of the fifteen largest mortgage lenders were using it, reaching close to 30% of the US mortgage market. FICO's Julie May (VP/GM B2B Scores) called the bureau-owned VantageScore "a de facto monopoly … handing complete pricing power to Equifax, Experian, and TransUnion." [CONFIRMED FACT] FICO's mortgage royalty rose from US$1.80 (pre-2022) to US$4.95, and then, per Senator Josh Hawley's 23 March 2026 oversight letter to FICO, "For 2026, FICO doubled its per-score price from $4.95 to $10.00 for the identical product offered the prior year … the potential to raise mortgage credit score costs across the industry by approximately $500 million." FICO also launched a "Mortgage Direct" licence program. TransUnion is countering aggressively: per its 8 January 2026 release (CEO Chris Cartwright), "TransUnion is offering VantageScore 4.0 for $4 per score in 2026, representing a 60% discount compared to a FICO score." **Economics [ANALYTICAL INFERENCE]:** every share point that shifts from FICO to VantageScore moves high-margin royalty economics from FICO to the bureau JV — a direct positive for Experian, and the clearest reason FICO is fighting.

#### (c) Decisioning and analytics
[CONFIRMED FACT/INFERENCE] Experian's Ascend and PowerCurve vs FICO (Software/Platform), SAS, Provenir, Zest AI, Taktile (which counts Serasa as a client), Oscilar, and lender in-house platforms. Basis of competition: breadth of embedded data, explainability (Experian's SHAP-based adverse-action reason codes), speed of deployment, and switching costs once integrated.

#### (d) Fraud and identity
[CONFIRMED FACT/INFERENCE] Experian (CrossCore, Precise ID, NeuroID, ClearSale) vs **LexisNexis Risk**, **Socure**, Alloy, Sift, Persona, Prove, **Entrust/Onfido**, and **Mastercard's Ekata**. Socure is the standout specialist: it "counts 18 of America's 20 largest banks as customers" and "verified 5 billion identity requests in 2025, up 85% year over year" (Forbes), on a US$4.5bn valuation set in a November 2021 Series E led by Accel and T. Rowe Price. This is Experian's most genuinely contested line: fast-moving, venture-funded specialists with strong graphs. Experian competes on the bundle (fraud + credit + identity on one data spine), not on standalone best-of-breed.

#### (e) Marketing data and identity
[CONFIRMED FACT/INFERENCE] Experian Marketing Solutions / Experian Graph / Tapad / Audigent / AtData vs **Acxiom (IPG)**, **Epsilon (Publicis)**, **LiveRamp**, **TransUnion's Neustar**. **Regulatory fragility [CONFIRMED FACT]:** this is the line the ICO attacked; Experian won at both tribunals (Upper Tribunal dismissed the ICO's appeal 23 April 2024; ICO declined further appeal May 2024), and the case is now cited as precedent *supporting* legitimate-interest marketing. So the near-term regulatory cloud has lifted, but the line remains the most exposed to any future statutory tightening.

#### (f) Healthcare revenue cycle
[CONFIRMED FACT/INFERENCE] Experian Health vs **Optum / Change Healthcare** (UnitedHealth), **Waystar**, **R1 RCM**, **Availity**. Experian Health is a strong niche (patient access, claims, identity, Patient Access Curator) but is a challenger to Optum/Change's scale. [UNKNOWN] precise US RCM share figures not sourced here.

#### (g) Automotive
[CONFIRMED FACT] Experian's **AutoCheck** vs **Carfax** (owned by S&P Global via IHS Markit). Carfax is the dominant, consumer-trusted brand (35bn+ records, 151,000+ data sources per its March 2026 statements); AutoCheck (since 1996) is cheaper, preferred for auction/wholesale data, and used by 13,000+ dealers, but is clearly #2 in consumer mindshare. **This is a line Experian does not win.**

#### (h) Consumer-facing apps
[CONFIRMED FACT] Experian's over 215 million free members (85m NA) vs **Credit Karma (Intuit)** — Intuit's 24 February 2020 acquisition was "approximately $7.1 billion in cash and stock"; the Credit Karma segment generated roughly US$2.3bn revenue in Intuit's fiscal 2025 (+32%), and Intuit's own reporting cites "nearly 99.5 million members" (media profiles cite ~130m cumulative); Credit Karma uses Equifax and TransUnion scores. Also **NerdWallet**, **ClearScore** (the firm the CMA blocked Experian from buying in 2019), **Credit Sesame**, and banks/neobanks giving away scores. Credit Karma is the sharpest consumer rival; Experian's differentiator is that it *owns a bureau* and can offer Boost (adding utility/telecom/rent to the file) natively.

#### (i) Brazil
[CONFIRMED FACT] **Serasa** — per Experian's 23 October 2012 press release, "the market leader in Brazil, with approximately 60% market share" — vs **Boa Vista (now Equifax**, acquired 2023 for ~US$596m EV), **Quod** (bank-owned, founded 2016 by the five largest Brazilian banks at 20% each, built explicitly to reduce dependence on Serasa), and **SPC Brasil**. The Quod natural experiment is analysed in V.10.

#### (j) Australia/New Zealand
[CONFIRMED FACT] **illion** (now Experian; A$820m acquisition completed 2024, ACCC unopposed; combined #2+#3 bureau; ~500 employees) vs **Equifax** (the incumbent #1, formerly Veda) and **Centrix** (NZ). illion also brings **BankStatements.com** and an accredited Consumer Data Right open-banking platform.

#### Cross-cutting entrants
[CONFIRMED FACT/INFERENCE] Open-banking / cashflow-data providers — **Plaid**, **Nova Credit**, **Prism Data**, **Ocrolus** — plus large technology/payments platforms (Mastercard via Ekata/open banking; potentially Apple, Amazon, or a bank consortium). These are the disruptive vector analysed in V.9.

---

### V.7 Competitor Teardowns

#### Experian vs Equifax vs TransUnion (most recent full years)

| Metric | **Experian (FY26, to 31 Mar 2026)** | **Equifax (FY2025, to 31 Dec 2025)** | **TransUnion (FY2025, to 31 Dec 2025)** |
|---|---|---|---|
| Total revenue | US$8,445m statutory (ongoing US$8,425m) | US$6,074.5m (+7%) | US$4,576m (+9%) |
| Growth (organic) | +8% organic | +7% (local currency) | ~+8.5% organic cc (~6.5% ex-mortgage) |
| Margin | 28.6% Benchmark EBIT | 31.9% adj. EBITDA; ~18.0% GAAP operating | operating income US$857.8m (~18.7%) |
| Net income | Statutory PBT US$1,951m | US$660.3m (+9%) | US$455m |
| Segments | B2B US$6,168m / Consumer US$2,257m | Workforce Solutions US$2,582.3m / USIS US$2,078.5m / International US$1,413.7m | US Markets ~US$3,568m (~78%) / International ~US$1,008m (~22%) |
| Cloud | 10-yr AWS deal (Jun 2025); migration completing | ~90% in Equifax Cloud (post-2017 rebuild) | Multi-year cloud/tech transformation ongoing |
| Consumer | 215m+ free members | Smaller D2C | Consumer Interactive (volatile; −18% organic in Q3-25 lapping a breach-remediation win) |
| Geography | Genuinely global; Brazil leadership | US-heavy; Brazil via Boa Vista | US-heavy (~78%); India (CIBIL) strength |
| Regulatory record | Beat ICO; CFPB trial 21 Sep 2026 | 2017 breach (147m) — the industry's defining event | Mixed |
| Employees | ~25,200 | ~15,000 | ~13,500 |

**Reading [ANALYTICAL INFERENCE].** Equifax's distinctive asset is **Workforce Solutions** (payroll/income verification — The Work Number), which earns bureau-plus economics (Q4 2025 EWS adjusted-EBITDA margin ~51%) and has no direct Experian equivalent at scale — this is why Equifax's group adjusted-EBITDA margin (31.9%) rivals Experian's despite a smaller top line. Equifax's post-2017 forced cloud rebuild is now a competitive advantage (~90% cloud), and its Boa Vista purchase directly attacks Serasa's home market. TransUnion is the smallest and most US-concentrated, hence the most mortgage- and macro-exposed. **Experian's edge** is the combination of true geographic diversification (Brazil), the largest consumer franchise, and the highest absolute revenue.

#### Experian vs FICO — why FICO earns more on less
[CONFIRMED FACT] FICO FY2025 (to 30 Sep 2025): revenue US$1.991bn (+16%); Scores US$1.169bn (+27%), Software US$0.822bn; full-year non-GAAP operating margin 55%; Scores-segment operating margin ~88%. [ANALYTICAL INFERENCE] FICO out-margins Experian because it owns a **standard, not a database**: the FICO score is a piece of IP embedded in regulation and contracts, sold at near-zero marginal cost, with none of the data-collection, dispute-handling, or matching-infrastructure cost that Experian carries. Experian bears the cost of building and defending the data asset; FICO monetises a thin, protected layer on top of it. The 2022–2026 royalty escalation (US$1.80 → US$4.95 → US$10.00) shows FICO exercising the pricing power of a standard — the same power that motivated the bureaus to build VantageScore to reclaim it.

---

### V.8 Why Experian Wins — and Where It Does Not

**Decomposition of the win mechanism:**
1. **Reciprocity-protected furnisher network [STRUCTURAL, durable].** Lenders furnish data free in exchange for access; a new entrant cannot assemble the same comprehensive file because furnishers have no reason to feed a bureau lenders don't yet use. This is the deepest moat.
2. **Identity graph and matching [STRUCTURAL + MANAGEMENT].** Matching ~1.3bn monthly updates to ~245m credit-active US consumers accurately is a decades-built capability.
3. **Scale in attributes/models [MANAGEMENT CHOICE].** The attribute library and Ascend are cumulative investments.
4. **Ascend platform switching costs [MANAGEMENT CHOICE].** 100% renewal of top NA FS accounts, durations +~10% to >4 years.
5. **Consumer franchise [MANAGEMENT CHOICE].** 215m+ members = a marketing channel that pays for itself.
6. **Brazil diversification [MANAGEMENT CHOICE, executed].** Serasa gives growth and geographic balance no US-only peer has.
7. **Regulatory capability [STRUCTURAL barrier].** FCRA/GDPR/LGPD compliance at scale is itself a barrier; the ICO win demonstrates it.

**Separating advantage types [ANALYTICAL INFERENCE]:**
- *Structural:* reciprocity network, matching, regulatory-compliance scale, tri-opoly structure.
- *Management choice:* Ascend, consumer franchise, Brazil, attribute library.
- *Temporary:* **the FY26 US mortgage pricing windfall (+45% on flat volumes)** — the clearest non-durable item, not to be extrapolated (see V.22).

**Where Experian does not win:** AutoCheck vs Carfax (clear #2); **EMEA/Asia-Pacific** (6.7% margin, the only region ever impaired — US$53m FY21, US$179m FY23); marketing services (structurally the most regulation-exposed line, even after the ICO win).

---

### V.9 Moat Analysis — Tested Against Open Banking

#### Moat scorecard (0–5; "prevents substitution" vs "creates value" separated)

| Moat | Score | Prevents substitution? | Creates genuine value? |
|---|---|---|---|
| Furnisher network + reciprocity | **5** | Yes — the core barrier | Yes — comprehensiveness |
| Identity graph / matching | 4 | Partly | Yes |
| Regulatory / compliance capability | 4 | Yes (barrier to entry) | Indirect |
| Attribute library + models | 3 | Weakly (replicable with data) | Yes |
| Ascend platform / integration switching costs | 3 | Yes once embedded | Yes |
| Consumer franchise | 3 | No (Credit Karma competes) | Yes (channel) |
| Brand / trust | 2 | No | Modest |
| Tri-opoly market structure | 4 | Yes | Neutral/negative for society |

#### The central question: does consumer-permissioned open banking threaten the bureau?

**The case FOR substitution [evidence].** Cashflow/transaction data is demonstrably predictive — FinRegLab found cashflow scores "generally at least as strong as" traditional bureau scores, and that a machine-learning model **combining bureau + cashflow data was the most predictive overall and across all subgroups**. The inclusion prize is large: per FinRegLab, "about one-third of U.S. adults are estimated to have thin or no credit files and another 25 percent to have below 'prime' scores." Plaid, Nova Credit and Prism Data are building the rails; the UK Open Banking regime is live; the US CFPB Section 1033 rule created a legal right to permission data.

**The case AGAINST substitution [evidence].** (1) **Comprehensiveness** — a bureau sees (via reciprocity) essentially all of a consumer's tradelines across all lenders; open banking sees only the accounts a consumer chooses to permission at the institutions they bank with, missing loans held elsewhere. (2) **Consistency/auditability** — lenders need standardised, comparable, regulator-accepted, adverse-action-explainable inputs across millions of applicants; bespoke transaction parsing is harder to standardise and defend. (3) **Permission fatigue** — participation requires an affirmative consumer action every time, whereas the bureau file exists automatically. (4) **The winning model is additive, not substitutive** — FinRegLab's own result is that bureau + cashflow beats either alone.

**Status of CFPB Section 1033 [CONFIRMED FACT — critical update].** The rule is **not in force**. Finalised October 2024 with compliance phasing from April 2026, it was challenged (Bank Policy Institute, Kentucky Bankers Association, Forcht Bank, E.D. Kentucky). The CFPB first sided with plaintiffs to vacate, then on 29 July 2025 pivoted to a stay and "accelerated" reconsideration rulemaking, issuing an ANPR on 22 August 2025. As of mid-2026 the rule is **enjoined and being rewritten** — the court found the CFPB likely exceeded its authority (§1033 authorises data-sharing to consumers and fiduciary representatives, "not to commercial third parties such as fintech companies") and that the no-fee provision lacked statutory support. The appeal to the Sixth Circuit is stayed. State-level action (New York AB 10640 / SB 9483, introduced March 2026) may create a patchwork. **The US legal rail for open-banking disintermediation is therefore delayed and legally contested — a materially more favourable near-term environment for the bureau than a year ago.**

**Is Experian's cashflow investment confident hedging or defensive necessity? [ANALYTICAL INFERENCE].** Both, but weighted toward *confident hedging*. Experian has built cashflow attributes, Boost (consumer-permissioned utility/telecom/rent data added to the file), and acquired illion's **BankStatements** and an accredited CDR open-banking platform in Australia. The tell is *how* Experian uses open banking: to **enrich the file and win thin-file and affordability decisions**, feeding permissioned data back into its own decisioning — i.e., it is absorbing open banking as a complement that deepens the moat, not defending against it as a substitute. If Experian believed open banking were an existential substitute, it would not be routing it through its own bureau-and-decisioning stack.

**Ten-year verdict [ANALYTICAL INFERENCE, MEDIUM-HIGH CONFIDENCE].** Open banking is a **complement and a thin-file niche, not a substitute**, on a ten-year horizon. It will (a) compress the bureau's monopoly on *thin-file* decisions, (b) become a standard *input* that the bureaus themselves resell, and (c) raise the ceiling on decision quality for everyone. It will not dissolve the reciprocity-protected comprehensiveness advantage for mainstream, full-file lending. The risk is real but slow, and Experian is positioned on the right side of it.

---

### V.10 Replication and Substitution Test

**(a) Replication — building a US bureau from zero.** [ANALYTICAL INFERENCE, HIGH CONFIDENCE]
- *Buildable with time/money:* the matching engine, FCRA compliance function, cloud infrastructure, lender integrations.
- *Effectively impossible:* the **furnisher relationships and reciprocity**. A new bureau has no data because furnishers gain nothing by feeding a bureau no lender queries; and lenders won't query a bureau with no data. This chicken-and-egg is the true barrier. Historical depth (decades of repayment history) cannot be bought at any price.
- *Verdict:* a well-funded entrant could replicate the technology in years but not the data network in any timeframe. Entry is not capital-constrained; it is network-constrained.

**(b) Substitution — could lenders assemble equal decision quality otherwise?** Partly, for some segments (open banking + own portfolio data + a consortium), but not the comprehensive cross-lender view. Large lenders' own portfolio data sees only their own customers.

**(c) The Quod natural experiment [CONFIRMED FACT + ANALYTICAL INFERENCE — decisive evidence].** In 2016 the five largest Brazilian banks built **Quod** *specifically* to reduce dependence on Serasa — the closest real-world test of whether even the most powerful, best-informed buyers (who are also the furnishers) can build their own bureau. The result: nearly a decade later, **Serasa remains the market leader (~60% share), and the more consequential competitive event was Equifax buying the #2 (Boa Vista), not Quod displacing Serasa.** [ANALYTICAL INFERENCE] Quod proves the replication barrier empirically: even the furnishers themselves, acting in concert with regulatory blessing and their own data, could not readily dislodge an incumbent bureau. This is the single strongest piece of evidence that the bureau moat is durable.

---

### V.11 Porter's Five Forces (tied to Experian)

- **Rivalry — MODERATE.** Stable three-firm US structure, high fixed costs, differentiated adjacencies (Equifax = Workforce; Experian = consumer + Brazil; TransUnion = insurance/India). Rivalry is real in adjacencies (fraud, consumer apps) but muted in the core bureau.
- **Supplier power — MIXED / HIGH at one node.** Furnishers supply free but hold *latent* power (they could restrict data). **FICO is the supplier with genuine, exercised pricing power** — the US$1.80→US$10.00 royalty escalation. This is the one place Experian is a price-taker.
- **Buyer power — MODERATE.** Large lenders are concentrated and are also the suppliers, giving them leverage — but tri-merge non-substitutability in mortgage neutralises it (they must buy all three). BNPL lenders who largely don't furnish are a latent buyer-power risk.
- **Substitutes — LOW-TO-MODERATE, RISING SLOWLY.** Open banking, cashflow data, in-house models, BNPL non-furnishing. Delayed by the §1033 injunction.
- **New entrants — NEAR-ZERO in the bureau; HIGH in adjacencies.** Reciprocity blocks bureau entry (Quod proves it); analytics, fraud and consumer apps are easily entered (Socure, Credit Karma).

---

### V.12 PESTLE (material factors only)

- **Political:** CFPB's changed posture (the case was filed under Chopra; enforcement priorities shifted under the new administration — [UNKNOWN] whether the CFPB presses the September 2026 trial with full vigour); mortgage-cost political pressure (Senator Hawley's March 2026 oversight letter); FHFA's pro-VantageScore, "junk-fee" stance under Director Pulte.
- **Economic:** US origination volumes and mortgage rates (the swing factor); consumer credit quality; **Brazilian macro** — high interest rates and consumer indebtedness constrained Latin America growth in FY26; BRL FX.
- **Social:** consumer expectation of free scores (Credit Karma effect); privacy attitudes; ~one-third of US adults thin/no-file (the inclusion opportunity and the open-banking wedge).
- **Technological:** AI in underwriting; open banking; agentic commerce ("Experian Agent Trust" / Agent Operating System); cloud (AWS migration completing).
- **Legal:** FCRA (and possible amendment); **§1033 (enjoined, being rewritten)**; state privacy laws; UK GDPR + the **CRGB replacing SCOR**; FCA CP26/7 mandatory-reporting remedies (Feb 2026); Brazilian LGPD Art. 7(X).
- **Environmental:** immaterial to the investment case. [Stated explicitly, as instructed.]

---

### V.13 Strategic Flywheels (genuine)

1. **Data → predictive power → lender demand → furnisher participation → more data.** [CONFIRMED mechanism] Limits: finite credit-active population and inquiry volume; failure condition: mass furnisher withdrawal or data-category removal.
2. **Consumer members → marketplace inventory → referral revenue → consented data → better matching → more members.** [CONFIRMED mechanism, 215m+ members] Limits: placement-conflict and consumer trust; failure condition: a Credit-Karma-style rival out-engaging, or a mis-selling scandal.
3. **Ascend deployments → deeper integration → higher switching costs → renewals → more deployments.** [CONFIRMED, 100% top-account renewal] Limits: a genuinely better platform (FICO Platform, cloud-native rivals).

**Rejected flywheel:** "brand → pricing power." Experian's brand does not command consumer pricing power (consumers expect free); pricing power in mortgage comes from structural non-substitutability, not brand.

---

### V.14 Negative Flywheels

1. **Dispute-quality underinvestment → litigation → regulatory action → remediation cost + reputational damage → margin compression.** This is the CFPB loop, live now.
2. **Aggressive mortgage pricing → political attention → regulatory intervention → structural price caps.** FHFA scrutiny of "junk fees" and Congressional letters are the channel; the +45%-on-flat-volumes windfall is politically conspicuous.
3. **Data-category removal (the medical-debt precedent) → thinner file → weaker predictive power → less lender value.** Each removal is individually small but cumulative and one-directional.
4. **Marketing-services regulatory pressure → constrained identity-graph uses → lower Marketing Solutions growth.** Muted for now by the ICO win, but structurally present.

---

### V.15 Theory of Constraints

**Current binding constraint [ANALYTICAL INFERENCE]:** **regulatory permission to use data, and the dispute-quality ceiling that gates it** — not technology, not capital, not the finite consumer population. If every other part of the company improved 50%, the limiting factor would still be the legal permissions (FCRA permissible purpose, GDPR legitimate interests, LGPD 7(X)) and the reputational/legal ceiling created by dispute quality. The CFPB trial is the acute expression of this constraint.

**Next constraint if that were solved:** the **finite pool of US credit-active consumers and inquiry volume** — the bureau's TAM is ultimately capped by population and origination cycles, which is precisely why growth must come from adjacencies (fraud, health, Ascend, Brazil) and from raising revenue-per-decision (scores, attributes) rather than from more consumers.

---

### V.16 Risk Register (probability × severity × detectability; residual; horizon)

| # | Risk | Prob. | Severity | Detect. | Residual | Horizon |
|---|---|---|---|---|---|---|
| 1 | **Adverse CFPB verdict mandating substantive dispute remediation** | Med | **Very High** | High (dated: 21 Sep 2026) | **High** | **Weeks** |
| 2 | Catastrophic data breach (Equifax model) | Low-Med | Very High | Low | High | Any time |
| 3 | FCRA class-action escalation (e.g., Davis trigger-leads) | Med | Med-High | High | Med | 1–3 yr |
| 4 | Legislative/regulatory data-category removal | Med | Med (cumulative) | High | Med | Ongoing |
| 5 | Mortgage-pricing political intervention / FHFA caps | Med | Med-High | Med | Med-High | 1–2 yr |
| 6 | FICO royalty economics / score-share shifts | Med-High | Low-Med (net positive to Experian) | High | Low | Now |
| 7 | UK reciprocity restructuring via CRGB opening data to entrants | Med | Med | High | Med | 1–3 yr |
| 8 | Open-banking disintermediation (§1033) | Low-Med (delayed) | Med | High | Low-Med | 3–10 yr |
| 9 | Marketing-services regulatory constraint | Low (post-ICO win) | Med | High | Low | Ongoing |
| 10 | Brazilian macro/FX + Equifax/Quod competition | Med | Med | High | Med | Ongoing |
| 11 | Key-person (Cassin/Pitchford) + chair transition | Low-Med | Med | Med | Med | 1–3 yr |
| 12 | EMEA/AP goodwill impairment (history: FY21, FY23) | Med | Low-Med | High | Low-Med | 1–2 yr |
| 13 | Cyber / operational resilience (AWS concentration) | Low-Med | High | Med | Med | Ongoing |

**Foregrounded: Risk 1 is the single most consequential dated event and is modelled explicitly in V.17.**

---

### V.17 Stress Tests — with the 21 September 2026 CFPB trial modelled explicitly

*Baseline: FY26 ongoing revenue US$8,425m; Benchmark EBIT US$2,407m at 28.6%; NA is 66% of group revenue at 34.2% margin; US bureau dispute volume >12m/yr at reported vendor economics as low as ~US$0.57/dispute letter.*

**Procedural status confirmed.** The case was filed 7 January 2025 (Central District of California). The court **denied Experian's motion to dismiss on 22 October 2025** and ordered it to answer; Experian filed its answer on 3 November 2025; discovery is ongoing; **jury trial is set for 21 September 2026**. The CFPB alleges FCRA §1681i (reinvestigation, deletion/reinsertion, written-notice) and §1681e(b) (maximum-possible-accuracy) violations plus CFPA unfair-acts claims, and seeks **civil money penalties, consumer redress, and injunctive relief**. No material provision is recognised (total provisions US$25m). Experian's public position (7 January 2025 statement): "The lawsuit is completely without merit … another example of irresponsible overreach by the CFPB … we will defend it vigorously and are confident we will prevail."

**Scenario (1) — Adverse verdict with an operational remediation mandate [the tail that matters].**
- *One-off:* civil money penalty (into the CFPB's victims relief fund) + consumer redress. [THIRD-PARTY ESTIMATE/UNKNOWN — no figure pleaded]; plausibly tens to low-hundreds of millions, absorbable against US$1.58bn FCF.
- *Recurring — the real exposure [ANALYTICAL INFERENCE]:* an injunction requiring *substantive* investigation of each dispute (reviewing consumer-submitted documents, not merely relaying ACDVs to furnishers) converts a ~US$0.57/letter operation into a labour-intensive one. Illustrative arithmetic: if fully-loaded per-dispute cost rose from ~US$1–2 to US$15–30 across >12m disputes/yr, incremental annual cost is on the order of **US$150m–US$350m+**. Against Benchmark EBIT of US$2,407m that is roughly **~60–145bps of group margin**, concentrated in the high-margin NA bureau where it would bite hardest. It would set a precedent the other two bureaus would have to follow (industry-wide cost reset) and would invite copy-cat FCRA class actions (Risk 3).
- *Effect:* revenue ~unchanged; Benchmark EBIT margin −60 to −145bps recurring; statutory profit hit by one-offs; FCF and buyback capacity reduced; strategic damage via precedent and reputational narrative.

**Scenario (2) — Settlement without operational mandates.** A monetary settlement (penalty + redress) with process tweaks but no wholesale re-engineering: one-off cash cost, minimal recurring margin impact, litigation overhang removed. [ANALYTICAL INFERENCE] This is management's evident preferred/expected outcome and the most probable if the CFPB's post-2025 enforcement appetite has cooled.

**Scenario (3) — Dismissal / defence verdict.** No financial impact; validates the low-cost dispute model; emboldens the industry; the negative flywheel (V.14 #1) is deferred, not removed.

**Scenario (4) — Catastrophic breach.** Equifax's 2017 breach (147m) is the reference. Modelled effect: direct costs + multi-year remediation, regulatory penalties, and — most damaging — erosion of the trust that underpins the consumer franchise and furnisher relationships. Margin and multiple impact would dwarf the CFPB case. Low-probability, very-high-severity, low-detectability.

**Scenario (5) — Mortgage price normalisation + volume weakness.** The FY26 +45%-on-flat-volumes pricing windfall reverses or plateaus while originations stay weak. [ANALYTICAL INFERENCE] This is the most *likely* negative and the market's biggest mis-read of the run rate: it would slow NA growth by several points and remove a chunk of incremental margin. Not existential; simply the end of a one-off.

**Scenario (6) — VantageScore displaces FICO at scale.** [ANALYTICAL INFERENCE] Net **positive** for Experian: royalty economics shift from FICO to the bureau-owned JV. The risk is asymmetric in Experian's favour; the loser is FICO.

**Scenario (7) — US recession cutting originations.** Cyclical revenue hit across credit marketing, originations and scores; partly offset by counter-cyclical collections, fraud and portfolio-management demand. Brazil and adjacencies cushion. Margin resilient given operating leverage works both ways.

**Scenario (8) — §1033 open banking arrives in force.** Given the current injunction/rewrite, this is a 3–10-year scenario. Effect: gradual thin-file margin compression, offset by Experian reselling open-banking-enriched attributes. Net modest.

**Scenario (9) — UK CRGB reform opening reciprocated data to entrants.** The FCA's replacement of SCOR with the CRGB (IWG final recommendations May 2025; FCA CP26/7 mandatory-reporting remedies Feb 2026) could lower entry barriers in the UK (a US$942m, 23.4%-margin region). Effect: UK margin pressure over 1–3 years; immaterial to group.

**Scenario (10) — Brazilian FX + competitive deterioration.** BRL weakness and Equifax/Boa Vista + Quod pressure on Serasa. Effect: Latin America (US$1,297m, 30.8% margin) growth and translated earnings pressure; already partly visible in FY26's constrained LatAm growth.

**Scenario (11) — Large adverse FCRA class action.** Statutory damages (US$100–1,000 per willful violation) across a large class could be material and would compound an adverse CFPB precedent.

---

### V.18 What Could Make Experian Obsolete?

| Disruptor | Removes the customer problem? | Can Experian adopt it? | Do existing assets stay useful? | Strands capital? | Verdict |
|---|---|---|---|---|---|
| Consumer-permissioned data replacing furnished data | No (comprehensiveness gap) | Yes (Boost, illion BankStatements) | Yes | No | **Complement, not killer** |
| AI underwriting on raw transactions | Partly (thin-file) | Yes (feeds its own decisioning) | Yes (standardised attributes still valued) | No | Slow erosion at edges |
| Government/central-bank credit registry | It's the function, done publicly | N/A | Brazil's Cadastro Positivo already coexists with Serasa | Possibly, if mandated | Low probability in US/UK |
| BNPL/embedded lenders not furnishing | Hollows the file over time | Partly (pushing BNPL reporting) | Degrades if furnishing gaps grow | No | Real slow risk |
| Big-tech/payments entrant with permissioned model | Possibly | Compete/partner | Yes | No | Watch Mastercard/Apple |
| Blockchain / self-sovereign identity | Not credibly at scale | Could adopt | Yes | No | Overhyped |

**The instructive precedent:** Brazil's **Cadastro Positivo** (a positive-data registry Serasa participates in) shows that even a government-backed positive-data regime *coexists with and is operated through* the incumbent bureaus rather than replacing them. [ANALYTICAL INFERENCE] Obsolescence would require the simultaneous failure of reciprocity, comprehensiveness and regulatory acceptance — none of which is close.

---

### V.19 Strategic Optionality

| Adjacency | Classification |
|---|---|
| Deepen Experian Health (RCM, patient access) | **Natural adjacency** — same data/identity spine |
| Consumer marketplace → mortgage (via Own Up) & insurance | **Natural adjacency** — monetises existing members |
| Agentic commerce / "Experian Agent Trust" / Agent Operating System | **Plausible adjacency** — leverages identity + trust; unproven economics |
| Identity infrastructure provider (credit as one use case) | **Plausible adjacency** — arguably the strategic direction (see H2) |
| Further APAC consolidation after illion | **Plausible adjacency** — but low-margin region |
| Buy/build open-banking capability at scale | **Plausible adjacency** — already doing it defensively/offensively |
| Small-business credit | **Plausible adjacency** — heritage asset (TRW's business database) |
| Becoming a lender | **Strategic fantasy** — would destroy neutrality, invite conflict, and torch the furnisher relationship |

---

### V.20 What Is Experian Becoming? (ranked hypotheses)

| Hypothesis | Prob. | Key evidence for | Key evidence against |
|---|---|---|---|
| **H1: US bureau + widening ring of adjacencies (current trajectory)** | **45%** | FY26 mix; capital allocation; renewals | Doesn't capture the identity/AI pivot |
| **H2: Identity/fraud/decisioning infrastructure co. where credit is one app** | **25%** | Ascend, CrossCore, NeuroID, ClearSale, Crozier/Kantar signal, Agent OS | Bureau still the profit centre |
| **H3: Consumer fintech/marketplace (215m members as primary asset)** | **10%** | Membership scale, Serasa SuperApp, Own Up | Marketplace is a channel, not the core; Credit Karma competition |
| **H4: Progressively hollowed at edges, regulated wholesale core retained** | **10%** | Data-category removals, BNPL non-furnishing, §1033 | Slow; Experian absorbing open banking |
| **H5: Structurally constrained/restructured by regulation** | **7%** | CFPB trial, FCRA amendment risk, CRGB | Beat ICO; §1033 enjoined; no dividing wall proposed |
| **H6: Acquired/broken up by competition intervention** | **3%** | No controlling shareholder; CMA blocked ClearScore | Too large; no live break-up pressure |

[ANALYTICAL INFERENCE] The most probable *reality* is **H1 evolving into H2** — Experian remains a bureau at its profit core while re-badging itself as a data-technology-and-identity company, a repositioning the Crozier/Kantar appointment and the Agent OS launch both signal.

---

### V.21 Five-Year and Ten-Year Strategic Map

- **Base case:** organic mid-to-high-single-digit growth; margin creep; adjacencies (fraud, health, Ascend, Brazil) offset a normalising mortgage line; CFPB settled monetarily; identity re-positioning advances. Moat intact.
- **Strong execution:** Ascend becomes a genuine platform standard; open banking absorbed as an Experian-resold input; VantageScore share gains lift score economics; margin toward 30%+.
- **Regulatory shock:** adverse CFPB verdict + FCRA amendment + CRGB opening UK data → margin −100 to −200bps, slower growth, strategic identity forced toward "regulated utility."
- **Technology disruption (open banking in force):** thin-file share ceded; bureau becomes one input among several; Experian survives as the aggregator/standardiser.
- **Competitive erosion:** Equifax (Workforce + Boa Vista) and fast fraud/consumer rivals compress adjacency growth; core bureau safe.
- **Operational/reputational failure (breach):** the one scenario that damages the trust-and-furnisher core; multi-year value impairment.

---

### V.22 What the Market May Misunderstand (≥6)

1. **"Experian sells data."** Reality: it sells a *permissioned network position and derived IP* (scores, attributes, decisioning). The raw data is a commodity; the reciprocity-protected network and the models are the asset. *Persists because* "data broker" is the media shorthand. *Implication:* the moat is the network, not the bytes.
2. **"The raw material is free, so the margin is easy."** Reality: margin comes from operating leverage, oligopoly/tri-merge pricing, and net revenue recognition — not from cheap inputs. *Implication:* margin is defensible only while pricing power and operating leverage persist.
3. **"Benchmark EPS is the right earnings number."** Reality: Benchmark excludes a **rising, permanent** acquisition-amortisation cost (US$174m FY22 → US$271m FY26). It flatters a serial acquirer. *Implication:* statutory EPS (164.5c vs Benchmark 179.8c) is the more honest long-run figure; the ~15c gap is structural, not one-off.
4. **"The consumer business is a public good."** Reality: it is a three-way monetisation of one relationship (subscription/premium, marketplace placement, consented data). *Implication:* "free" is a customer-acquisition cost, not philanthropy.
5. **"FY26 growth is the run rate."** Reality: it includes the **non-durable US mortgage pricing windfall (+45% on flat volumes)**. *Implication:* normalise NA growth before extrapolating; the market risks over-paying for a one-off.
6. **"Open banking will kill the bureau."** Reality (tested in V.9): complement and thin-file niche, not substitute, on a 10-year view; §1033 is enjoined and being rewritten. *Implication:* the disruption narrative is over-discounted near-term.
7. **"The CFPB case is just a fine."** Reality: the fine is absorbable; the **recurring cost of a mandated substantive-investigation regime** (potentially US$150m–US$350m+ annually, ~60–145bps of margin, plus industry precedent and class-action follow-on) is the real exposure. *Implication:* the market is watching the wrong number.

---

### V.23 Management and Capital-Allocation Judgement

| Decision | Verdict |
|---|---|
| 1996 TRW acquisition by GUS | **Value-creating** (foundational; combined two #1 bureaus) |
| 2006 demerger & listing | **Value-creating** (unlocked focus and rating) |
| Serasa acquisitions (2007/2012, to 99.6%) | **Value-creating** — Robert's best call; ~60% share of a growth market |
| Attempted ClearScore acquisition / CMA block (2019) | **Strategically sound, correctly blocked** — would have entrenched; not management's failure |
| Direct-to-consumer build-out | **Value-creating** — 215m members, self-funding channel |
| Ascend platform investment | **Value-creating** — switching costs, 100% top-account renewal |
| AWS 10-year migration (2025) | **Strategically necessary** — matches Equifax's cloud lead; too early to judge ROI |
| illion (2024), ClearSale, NeuroID, AtData, KYC360, Own Up | **Too early to judge**, trending positive (illion synergies delivering; EMEA/AP EBIT more than doubled in FY26) |
| Sustained low-cost dispute operation | **Questionable** — the margin source that created the CFPB tail risk |
| Aggressive mortgage pricing | **Questionable** — value-creating short-term, politically/regulatorily dangerous |
| Litigating ICO and CFPB | **Vindicated on ICO; unresolved on CFPB** — the posture is consistent and, on ICO, correct |
| Buyback programme (US$725m FY26 + new US$1bn) | **Value-creating but partly incentive-driven** (Benchmark EPS mechanics) |

---

### V.24 Volume V Reconstruction — Synthesis

The preceding sections supply the required synthesis artefacts: (1) the Lineage and Leadership Map (V.1); (2) Management-System Analysis (V.3); (3) the Declared-vs-Revealed Culture Matrix (V.4); (4) the Incentive Map (V.5); (5) Competitive Maps per business line (V.6); (6) Competitor Comparison Matrices (V.7); (7) the Why-Experian-Wins Decomposition (V.8); (8) the Moat Scorecard with the open-banking stress test (V.9); (9) the Replication and Substitution Matrix including the Quod natural experiment (V.10); (10) Porter's Five Forces (V.11); (11) Material PESTLE Factors (V.12); (12) Positive Flywheels (V.13); (13) Negative Flywheels (V.14); (14) the Current Bottleneck (V.15); (15) the Risk Heatmap (V.16); (16) Stress-Test Results including the September 2026 trial model (V.17); (17) Obsolescence Scenarios (V.18); (18) the Strategic Optionality Matrix (V.19); (19) the What-Experian-Is-Becoming Probability Matrix (V.20); (20) Five-Year and Ten-Year Scenarios (V.21); (21) Market Misconceptions (V.22); and (22) the Management Judgement Assessment (V.23).

**(23) Key unknowns [UNKNOWN, explicitly]:** the CFPB's settlement posture and the new administration's appetite to press the September 2026 trial; the exact penalty/redress sought; internal data-use escalation governance; board deliberations; Experian Health's precise US RCM share; the durability of the mortgage price level.

**(24) Ten most important conclusions:**
1. Experian is two merged lineages (TRW's engineering-scale US bureau; CCN/GUS's marketing-data, acquisitive retailer culture), and both are legible in today's strategy.
2. The reciprocity-protected furnisher network is the real moat; the **Quod natural experiment proves it** — even Brazil's five biggest banks could not dislodge Serasa.
3. The FY26 mortgage windfall (+45% on flat volumes) is **temporary** and the market's biggest run-rate error.
4. Benchmark EPS **structurally flatters** a serial acquirer by excluding rising acquisition amortisation, and executive pay rides on it.
5. The dispute operation's low unit cost is both a margin source and the origin of the CFPB tail risk — the same fact seen two ways.
6. The CFPB trial's real exposure is **recurring remediation cost (~60–145bps of margin), not the fine**.
7. Open banking is a **complement and thin-file niche**, delayed further by the §1033 injunction; Experian is absorbing it, not being disrupted by it.
8. VantageScore's rise is **net positive** for Experian at FICO's expense; FICO is the one supplier with real pricing power over Experian.
9. Governance gap: **no board data-ethics committee** despite data-permission being the binding constraint; the Crozier/Kantar chair appointment signals a consumer-data-and-identity repositioning.
10. Experian is most probably **H1 evolving into H2** — a bureau at its profit core, re-badging as a data-technology-and-identity infrastructure company.

**Concluding answers:**
- **Why does Experian win today, and would it be creatable now?** It wins on a reciprocity-protected data network, matching infrastructure, scale adjacencies and geographic diversification. It **could not be built from scratch today** — the furnisher/reciprocity chicken-and-egg and decades of historical depth are unbuildable at any price (Quod proves it). The technology is replicable; the network is not.
- **Genuinely defensible vs merely structurally protected?** *Genuinely defensible (creates value):* matching, attributes, Ascend, Brazil, compliance capability. *Merely structurally protected (rent, not value):* the tri-opoly and tri-merge non-substitutability in mortgage — protected by structure and regulation, not by superior value, and therefore the part most vulnerable to political/regulatory attack.
- **Hardest/easiest to replicate?** Hardest: the furnisher network and historical depth. Easiest: the technology, the consumer app, the analytics.
- **Current bottleneck?** Regulatory permission to use data + the dispute-quality ceiling that gates it.
- **Single greatest structural risk?** A catastrophic breach (existential to trust); the greatest *near-term dated* risk is the CFPB trial's remediation tail.
- **Most dangerous competitor/force, and horizon?** Near-term (0–2 yr): the CFPB and mortgage-pricing politics. Medium (2–5 yr): Equifax (Workforce + Boa Vista) in adjacencies and Brazil. Long (5–10 yr): open banking / cashflow disintermediation of thin-file lending.
- **Could open banking make the bureau obsolete?** No, not on a ten-year horizon — complement and niche, not substitute.
- **Is the consumer well served?** Partly. Well served in free access, monitoring and inclusion tools; **under-served in dispute quality and mortgage pricing**, which is exactly where the CFPB and political pressure land.
- **The central question — is a credit bureau a permanent utility or a historically contingent arrangement?** [ANALYTICAL INFERENCE, the study's core judgement] **The *function* — shared repayment information — is permanent; any developed credit market must have it in some form.** But Experian's *particular arrangement* — a private, reciprocity-protected, three-firm oligopoly monetising the same consumer relationship three ways and pricing mortgage inputs at will — is historically contingent. Open banking and modern computation are not making the *function* unnecessary; they are making the *private-oligopoly form of it* contestable at the edges and politically harder to defend at the centre. The bureau is not becoming obsolete; the *rents* attached to this specific version of it are slowly being competed and regulated down. Experian's genuine achievement — and its genuine risk — is that it has built the most durable version of a function the economy cannot do without, while extracting from it returns that invite the very regulation that constrains it.

*[End of Volume V. No cross-volume synthesis undertaken, per scope.]*


---

# Part VI — Cross-Volume Synthesis

*This section is new. It exists only in the master edition and draws on all five volumes.*

## VI.1 What Experian actually owns

The single most consequential fact about this enterprise is the one it never states plainly: **it does not own its raw material.**

Lenders, card issuers, telecoms and utilities furnish account and repayment data to Experian at their own cost, receiving no cash. Experian holds that data under statutory permission — the Fair Credit Reporting Act in the United States, legitimate interests under UK GDPR, Article 7(X) "protection of credit" under Brazil's LGPD — and under contractual reciprocity, the rule that a furnisher may only draw out the categories it contributes.

What Experian owns outright is the **aggregation**, the **derived attributes and bureau scores**, the **models**, and the **identity graph** that links records to people.

In one line: **Experian owns the refinery and the refined product, not the crude oil.**

Every other feature of the enterprise follows from this. The margin follows from it, because there is no procurement cost. The moat follows from it, because a competitor cannot buy the crude either. The litigation follows from it, because the accuracy of borrowed data is a legal duty that generates no revenue. And the strategic risk follows from it, because a permission can be withdrawn in a way that ownership cannot.

## VI.2 The single causal model

```
        ~10,000 FURNISHERS contribute data FREE
        (reciprocity: contribute or lose access)
                        ↓
        ~1.3 billion record updates per month
                        ↓
        ┌──── THE MATCHING ENGINE ────────────────────┐
        │  Attach each record to the right person     │
        │  among ~245 million credit-active US        │
        │  consumers. No universal identifier.        │
        │                                             │
        │  Match too loosely → MIXED FILE             │
        │  Match too tightly → FRAGMENTED FILE        │
        │  The threshold is a POLICY CHOICE           │
        └─────────────────────────────────────────────┘
                        ↓
        AGGREGATION + ATTRIBUTES + MODELS + GRAPH
        ← this is what Experian owns
                        ↓
        Sold back to the same furnishers, per pull,
        at prices they cannot escape
        (tri-merge: mortgage requires all three bureaux)
                        ↓
        US$8,445m revenue · 28.6% Benchmark EBIT margin
                        ↓
        ┌──── THE CONSUMER, MONETISED THREE WAYS ─────┐
        │  1. Data sold to lenders (largest)          │
        │  2. Subscription sold to the consumer       │
        │  3. Referral fee for sending the consumer   │
        │     back to a lender (fastest-growing)      │
        └─────────────────────────────────────────────┘
                        ↓
        ┌──── THE PROCESS THAT CHECKS THE DATA ───────┐
        │  >12 million disputes a year                │
        │  Coded into a 3-digit ACDV, routed via      │
        │  e-OSCAR, consumer documents not forwarded  │
        │  Reported vendor economics: ~US$0.57/letter │
        │  GENERATES NO REVENUE                       │
        └─────────────────────────────────────────────┘
                        ↓
        CFPB sues. Motion to dismiss denied.
        JURY TRIAL: 21 SEPTEMBER 2026
```

**The defining property:** the process that determines whether the data is *correct* is the only process in the chain that produces no revenue — and it is therefore the only one run at minimum cost.

## VI.3 What the volumes prove together that none proves alone

**1. The margin and the litigation are the same fact.**

Volume II established the inverted value flow: no procurement cost for the core input. Volume III established that the dispute machinery codes each complaint into a three-digit ACDV, routes it through the industry-shared e-OSCAR system, does not by default forward the consumer's own documents to the furnisher, and runs at reported vendor economics as low as US$0.57 per dispute letter. Volume IV established that this low cost contributes materially to the 28.6% Benchmark EBIT margin. Volume V established that the CFPB's case goes to a jury on 21 September 2026.

Chain them and the conclusion is uncomfortable but unavoidable: **the margin exists partly because the accuracy machinery is cheap, and the regulator is suing over precisely the cost structure that produces the profit.**

This is not a compliance failure bolted onto a good business. It is the business model's central tension, and the reason the financial exposure is the *recurring remediation cost* — plausibly 60 to 145 basis points of group margin — rather than any fine.

**2. The moat is a network, not a technology — and Brazil proved it empirically.**

Volume I established the reciprocity principle. Volume III established that the matching engine, while sophisticated, is replicable in engineering terms — a well-funded entrant could build the technology in a few years. Volume V established the decisive natural experiment: in 2016 **Brazil's five largest banks founded Quod**, a bureau built specifically to reduce their dependence on Serasa. A decade later, Serasa retains roughly 60% share, and the more consequential competitive event was Equifax buying the number two, not Quod displacing the leader.

Together these establish the barrier's true nature. It is not capital and not technology. It is the **chicken-and-egg of furnisher participation**: a new bureau has no data because furnishers gain nothing from feeding a bureau no lender queries, and no lender queries a bureau with no data. Quod is the strongest available evidence that even the furnishers themselves, acting together, with regulatory blessing and their own data, cannot readily break it.

**3. Pricing power is real, politically fragile, and being exercised by the supplier too.**

Volumes II and IV established the mortgage windfall: revenue up 45% on roughly flat volumes, with the total credit-report cost of a conventional loan rising from about US$50 in 2022 to roughly US$540 in 2026. Volume V established that **FICO — Experian's own supplier — doubled its per-score royalty from US$4.95 to US$10.00 for 2026**, drawing a Congressional oversight letter.

Together: every layer of the mortgage credit-data stack is raising price simultaneously, against a borrower who cannot shop for a bureau and a lender who must buy all three. The revenue is real. The durability is not. This is the clearest case in the study of profit that invites the regulation that will constrain it.

**4. The metric that governs executive pay excludes the cost of the strategy that generates it.**

Volume IV established that amortisation of acquisition intangibles has risen every year — US$174m in FY22, US$211m in FY25, US$271m in FY26 — because Experian acquires every year, and that Benchmark measures exclude it. Volume V established that executive long-term incentives centre on Benchmark EPS growth.

Together: **acquisitions are effectively free in the currency in which management is paid.** This is industry-normal — Equifax and TransUnion adjust similarly — but "normal" is not "economically neutral." The 15-cent gap between Benchmark EPS of 179.8 and statutory EPS of 164.5 is the visible price of a growth algorithm whose cost never reaches the headline number.

**5. Open banking is being absorbed rather than resisted, which is the tell.**

Volume II established Experian Boost, which adds consumer-permissioned utility and telecom payments to the file. Volume III established the acquisition of illion's BankStatements and an accredited Australian open-banking platform. Volume V established that the US Section 1033 rule is currently enjoined and being rewritten, and that Experian routes permissioned data through its own bureau and decisioning stack.

Together: Experian is treating the supposed disruptor as an **input**. A company that believed open banking were existential would fight it; this one is buying it and reselling it. The evidence supports treating open banking as a complement and a thin-file niche on a ten-year horizon — not because the threat is imaginary, but because comprehensiveness across all lenders is the property open banking cannot replicate, and that property is what the reciprocity network exists to produce.

## VI.4 The central tension

**Experian's profitability depends on the accuracy of data it does not own, contributed by parties it cannot compel, about people who are not its customers, verified by a process that generates no revenue.**

Every actor in this system behaves rationally. A lender furnishes data because reciprocity makes it cheaper than not furnishing. Experian minimises dispute cost because disputes produce no revenue and the consumer is not the paying customer. A consumer accepts a free membership because it costs nothing visible. A regulator sues because the accumulated consequence is millions of people carrying errors they cannot easily fix.

And the aggregate outcome is a business earning a near-30% margin on an asset whose quality is assured by the cheapest process in the chain.

That is not hypocrisy; it is incentive design. But it is why the September 2026 trial matters more than any single quarter's results.

## VI.5 What would falsify this reading

Specific, checkable markers, so the study can be audited against reality:

| If this happens | The reading weakens because |
|---|---|
| The CFPB case is dismissed or settled with no operational mandate | The dispute cost structure survives, and the margin thesis holds unchanged |
| Mortgage revenue holds its FY26 level for two more years without political intervention | The pricing windfall was more durable than assessed |
| A new bureau achieves meaningful US furnisher participation | The reciprocity barrier is weaker than Quod suggests |
| Experian discloses mixed-file rates or tightens SSN matching to eight-of-nine with a flag | Accuracy is being genuinely invested in, not merely defended |
| Section 1033 is finalised in force and thin-file lending migrates to permissioned data at scale | Open banking is a substitute, not a complement |
| Benchmark and statutory EPS converge as acquisition intangible amortisation plateaus | The acquisition treadmill is slowing and the metric gap closes |
| A goodwill impairment appears outside EMEA/Asia Pacific | The acquisition machine is over-reaching into the profitable core |
| VantageScore passes 50% of conforming mortgage volume | The score layer's economics shift materially, mostly at FICO's expense |

## VI.6 What Experian is becoming

Ranked by probability on the evidence assembled across all five volumes:

| Hypothesis | Probability | Strongest evidence |
|---|---|---|
| US bureau with a widening ring of adjacencies — the current trajectory | ~45% | FY26 revenue mix; capital allocation; 100% top-account renewal |
| Identity, fraud and decisioning infrastructure where credit is one application | ~25% | Ascend, CrossCore, NeuroID, ClearSale; the Crozier and Kantar signal; Agent OS |
| Consumer fintech and marketplace with 215 million members as the primary asset | ~10% | Membership scale; Own Up; Serasa's consumer platform |
| Progressively hollowed at the edges, regulated wholesale core retained | ~10% | Data-category removals; BNPL non-furnishing; Section 1033 |
| Structurally constrained or restructured by regulation | ~7% | The CFPB trial; FCRA amendment risk; the UK CRGB reform |
| Acquired, broken up or reshaped by competition intervention | ~3% | No controlling shareholder; the CMA's ClearScore precedent |

**Synthesis:** the first evolving into the second. Experian remains a bureau at its profit core while re-badging itself as a data-technology and identity company — a repositioning that the chair appointment and the agentic-commerce launch both signal, and that the economics do not yet reflect.

## VI.7 Implications for a fintech builder

*This section applies the study to the reader's own context rather than to Experian. Analytical inference throughout.*

**If you are building a data network, the hard part is the chicken-and-egg, not the technology.** This is the most transferable lesson in the study. Experian's moat is not its matching engine, which is replicable, but the fact that no furnisher will feed a bureau nobody queries and no lender will query a bureau with no data. Quod — five of Brazil's largest banks, with their own data and regulatory support — could not break it in a decade. If your model depends on assembling a contributed-data network, solve the cold-start problem first and treat everything else as secondary.

**Understand what you are actually buying when you buy a credit report.** You are not buying data. You are buying a **permission and an auditable basis for a decision** — a defensible, regulator-acceptable answer to the question "why did you decline this applicant?" That is why bureau pricing survives despite the underlying data being contributed free, and why a cheaper source of raw signal does not straightforwardly substitute.

**The adverse-action requirement shapes what machine learning you can deploy.** Volume III established this precisely: because a declined consumer must be told the principal reasons, models that cannot produce stable, defensible reason codes are effectively unusable in a credit decision. This is why the industry uses monotonic gradient-boosted trees with SHAP-derived reason codes rather than arbitrary deep models, and why generative AI sits in model development, documentation and servicing rather than in the decision itself. If you are building credit models, explainability is a hard constraint before it is a virtue.

**Watch the September 2026 trial, whatever you are building.** If the court mandates substantive dispute investigation, the standard applies to the whole industry — Equifax and TransUnion included — and to any furnisher whose data quality is implicated. The cost of accuracy is about to be repriced, and anyone who reports to or reads from a bureau is affected.

**On monetising a consumer who is also your product.** Experian sells a consumer's data to lenders, sells that consumer protection against the resulting risks, and takes a fee for sending them back to a lender. All three are lawful and all three are disclosed. The lesson is not that this is wrong but that it is **structurally unstable**: it depends on the consumer never fully pricing what is happening. If your model has a similar shape, the regulatory risk arrives not when someone proves harm but when the arrangement becomes legible.

**Finally, on rents versus function.** A credit market needs shared repayment information; that function is permanent. What is contingent is the particular private, three-firm, reciprocity-protected form of it, and the rents attached. Modern computation and consumer-permissioned data are not making the function unnecessary — they are making this version of it contestable at the edges and harder to defend at the centre. That distinction is worth carrying into any market where an incumbent looks unassailable.

## VI.8 Ten cross-volume conclusions

1. Experian owns the aggregation, attributes, models and identity graph — not the raw data, which is contributed free under permission and reciprocity.
2. The 28.6% margin and the CFPB litigation are the same fact viewed from two sides: the accuracy machinery is cheap because it produces no revenue.
3. The moat is the furnisher network's chicken-and-egg, not the technology — and Brazil's Quod proves even the furnishers themselves cannot break it.
4. The FY26 mortgage windfall is a pricing event, not a franchise event, and every layer of the stack is raising price at once.
5. Benchmark EPS excludes a permanent and rising cost of the acquisition strategy that generates it, and executive pay rides on Benchmark EPS.
6. Identity matching is irreducibly error-prone, but the error rate is a tunable policy choice biased toward looser matching by commercial incentive.
7. The consumer is monetised three ways and is unambiguously the product in the largest of them.
8. Open banking is being absorbed as an input rather than resisted as a substitute — a complement and thin-file niche on a ten-year view.
9. The jury trial on 21 September 2026 is the single most consequential dated event, and the recurring remediation cost is the exposure, not the fine.
10. The function a bureau performs is permanent; this particular private, oligopolistic form of it, and its rents, are historically contingent.

---

# Appendix A — Glossary of Regulatory and Technical Terms

*Load-bearing. Read before Part II.*

## US regulatory

| Term | Meaning |
|---|---|
| **FCRA** | Fair Credit Reporting Act, 15 U.S.C. §1681 — the foundational US statute governing consumer reporting |
| **CRA** | Consumer Reporting Agency — the FCRA term for a credit bureau |
| **Permissible purpose** | The statutory basis on which a report may be pulled (credit transaction, account review, employment, insurance, firm offer of credit) |
| **§611 reinvestigation** | The bureau's duty to reinvestigate a disputed item, generally within 30 days |
| **§623 furnisher duties** | The furnisher's duty of accuracy and to investigate disputes routed to it |
| **§605** | Retention limits — most adverse items seven years, Chapter 7 bankruptcy ten years |
| **Adverse action notice** | The notice a declined applicant must receive, stating the principal reasons |
| **CFPB** | Consumer Financial Protection Bureau — the federal supervisor under the larger-participant rule |
| **Larger-participant rule** | The 2012 rule bringing the major bureaux under CFPB supervision |
| **ECOA / Regulation B** | Equal Credit Opportunity Act and its implementing regulation — fair-lending rules |
| **GLBA** | Gramm-Leach-Bliley Act — data safeguarding |
| **CCPA / CPRA** | California's consumer privacy statutes |
| **§1033** | The CFPB's open-banking rule creating a consumer right to permission financial data; currently enjoined and being rewritten |
| **NCAP** | National Consumer Assistance Plan — the 2015 state-AG settlement that removed civil judgments and most tax liens from files |
| **Trigger lead** | A prescreen lead generated when a consumer's credit is pulled for a mortgage |

## UK and EU regulatory

| Term | Meaning |
|---|---|
| **UK GDPR / DPA 2018** | The UK data-protection regime |
| **Legitimate interests** | The Article 6(1)(f) lawful basis on which UK bureau processing rests |
| **ICO** | Information Commissioner's Office — the UK data-protection regulator |
| **CRAIN** | Credit Reference Agency Information Notice — the industry transparency notice |
| **FCA** | Financial Conduct Authority — authorises UK credit reference agencies |
| **CIMS** | Credit Information Market Study — the FCA study concluding December 2023 |
| **SCOR** | Steering Committee on Reciprocity — the industry body governing UK data sharing, judged not fit for purpose by the FCA |
| **CRGB** | Credit Reporting Governance Body — SCOR's broader, more accountable replacement |
| **CAIS** | Credit Account Information Sharing — Experian's UK bureau database |
| **Closed user group** | The reciprocity structure limiting access to what a furnisher contributes |
| **CMA** | Competition and Markets Authority — blocked the ClearScore acquisition in 2019 |

## Brazil

| Term | Meaning |
|---|---|
| **LGPD** | Lei Geral de Proteção de Dados — Brazil's data-protection law |
| **Article 7(X)** | The "protection of credit" lawful basis on which Serasa's processing rests |
| **Cadastro Positivo** | The positive credit registry, made opt-out by LC 166/2019 |
| **GBD** | Gestor de Banco de Dados — an accredited positive-registry database manager |
| **ANPD** | Autoridade Nacional de Proteção de Dados — the Brazilian data-protection authority |
| **Negativado** | A consumer with a registered default; the state Limpa Nome exists to clear |
| **Limpa Nome** | Serasa's creditor-paid debt-renegotiation marketplace |
| **Quod** | The bureau founded in 2016 by Brazil's five largest banks to reduce dependence on Serasa |

## Industry mechanics

| Term | Meaning |
|---|---|
| **Furnisher** | An institution that supplies account and repayment data to a bureau |
| **Reciprocity** | The principle that a furnisher may only draw out the data categories it contributes |
| **Metro 2** | The fixed-format data standard for furnishing, maintained by the CDIA |
| **CDIA** | Consumer Data Industry Association — the US industry body |
| **e-OSCAR** | The dispute-routing system jointly operated by the bureaux |
| **ACDV** | Automated Credit Dispute Verification — the one-page form carrying a dispute to a furnisher |
| **Tri-merge** | The US mortgage convention requiring reports from all three bureaux |
| **Mixed file** | Two consumers' data merged by over-matching — the most damaging bureau error |
| **Fragmented file** | One consumer's history split across files by under-matching |
| **Thin file / credit invisible** | Consumers with insufficient or no bureau history |
| **Prescreen** | A lender campaign selecting consumers meeting pre-set criteria, requiring a firm offer of credit |
| **Attribute** | A derived variable computed from the file and sold to lenders |
| **Tradeline** | An individual account record on a consumer's file |

## Products and platforms

| Term | Meaning |
|---|---|
| **File One** | Experian's core US consumer database |
| **Find Consumer** | Experian's search-and-match engine |
| **Ascend** | Experian's cloud-native analytics and decisioning platform |
| **PowerCurve** | Experian's decisioning software suite |
| **CrossCore / Precise ID** | Fraud orchestration and identity verification |
| **Boost** | The consumer product adding permissioned utility, telecom and rent payments to the file |
| **Experian Go** | The product establishing a file for credit-invisible consumers |
| **AutoCheck** | Experian's vehicle-history product, second to Carfax |
| **VantageScore** | The scoring venture co-owned equally by the three bureaux |
| **FICO** | Fair Isaac's score — distributed by Experian under licence; simultaneously supplier, partner and rival |

## Financial

| Term | Meaning |
|---|---|
| **Benchmark** | Experian's non-GAAP measures — Benchmark EBIT, PBT, EBITDA and EPS |
| **Ongoing activities** | Revenue excluding lines re-presented as exited from FY26 |
| **Organic growth** | Growth excluding acquisitions and currency |
| **Constant currency (CER)** | Growth excluding currency movement |
| **Acquisition intangibles** | Customer-relationship and technology assets created on acquisition, whose amortisation Benchmark excludes |
| **ROCE** | Return on capital employed, post-tax on the Benchmark basis |

---

# Appendix B — Canonical Figures Register

**Where any volume disagrees with this table, this table governs.** Every figure carries its basis. As of 9 August 2026.

## Group financials — FY26 (year to 31 March 2026)

| Figure | Canonical value | Basis |
|---|---|---|
| Statutory revenue | **US$8,445m** (+12% actual) | Statutory |
| Ongoing activities revenue | **US$8,425m** | Benchmark/ongoing |
| Organic revenue growth | **+8%** | Organic |
| Constant-currency growth | +11% | CER |
| Benchmark EBIT (ongoing) | **US$2,407m — 28.6% margin** | Benchmark |
| Benchmark EBIT (total) | US$2,397m | Benchmark |
| Statutory operating profit | US$2,045m | Statutory |
| Benchmark PBT | **US$2,212m** | Benchmark |
| Statutory PBT | **US$1,951m** (+26%) | Statutory |
| Benchmark EPS | **179.8 US cents** (+15% actual) | Benchmark |
| Statutory basic EPS | **164.5 US cents** (+29%) | Statutory |
| Benchmark EBITDA | US$3,010m | Benchmark |
| Benchmark operating cash flow | US$2,221m — 93% conversion | Benchmark |
| Benchmark free cash flow | US$1,583m | Benchmark |
| Benchmark tax rate | 25.5% | Benchmark |
| ROCE (post-tax) | **17.2%** | Benchmark |
| Net debt | US$5,179m — **1.7× Benchmark EBITDA** | — |
| Capital expenditure | 8.6% of revenue | — |
| Dividend | 69.25 US cents (+11%) | — |

## Revenue architecture

| Segment | Revenue | Benchmark EBIT | Margin |
|---|---|---|---|
| **B2B** | **US$6,168m** | US$1,903m | 30.9% |
| — Financial Services | US$4,463m | — | — |
| — Verticals | US$1,705m | — | — |
| **Consumer Services** | **US$2,257m** | US$668m | 29.6% |
| **North America** | **US$5,587m** (66.3%) | US$1,912m | **34.2%** |
| **Latin America** | US$1,297m | US$399m | 30.8% |
| **UK & Ireland** | US$942m | US$220m | 23.4% |
| **EMEA & Asia Pacific** | US$599m | US$40m | **6.7%** |
| Central costs | — | (US$164m) | — |
| **Total ongoing** | **US$8,425m** | **US$2,407m** | **28.6%** |

## Cost architecture (Benchmark, % of revenue)

| Category | Value |
|---|---|
| Labour | **31.8%** (>300bps lower than two years earlier) |
| Data & IT | 19.2% |
| Amortisation & depreciation | 7.3% |
| Marketing & customer acquisition | 7.1% |
| Other operating | 6.3% |
| **Total operating expenses** | **71.7%** |

## Balance sheet and capital

| Figure | Canonical value |
|---|---|
| Goodwill | US$7,261m |
| Other intangibles | US$3,078m |
| Property, plant & equipment | US$337m |
| Provisions (current + non-current) | **US$25m — no material CFPB provision** |
| Amortisation of acquisition intangibles | **US$271m FY26** (US$211m FY25; US$174m FY22) |
| Goodwill impairments, all time | **US$53m FY21 + US$179m FY23, both EMEA/Asia Pacific only** |
| FY26 acquisition spend | US$792m |
| FY26 buybacks | US$725m, plus a new US$1bn programme to 30 June 2027 |
| Credit ratings | Baa1 (Moody's) / BBB+ (S&P) |

## Corporate

| Figure | Canonical value |
|---|---|
| Incorporation | **Jersey** — registered office 22 Grenville Street, St Helier |
| Tax residence | **Ireland** |
| Corporate HQ | **Dublin** — 2 Cumberland Place, Fenian Street |
| Operational hubs | Nottingham, Costa Mesa, São Paulo |
| Listing | LSE (EXPN), FTSE 100; largest holder BlackRock ~5.9%; no controlling shareholder |
| CEO / CFO | Brian Cassin (since 2014) / Lloyd Pitchford |
| Chair | Mike Rogers → **Adam Crozier** from the 22 July 2026 AGM |
| Employees | ~**25,200** across 32–33 countries |
| US bureau entity | **Experian Information Solutions, Inc.** (Ohio) — the principal profit centre |
| UK entity | Experian Limited (company 00653331, FCA-authorised) |
| US consumer entity | ConsumerInfo.com, Inc. dba Experian Consumer Services |
| Finance entity | Experian Finance plc (company 00146575, incorporated 1917 — the former Great Universal Stores / GUS plc shell) |
| Brazil | Serasa S.A., ~99.6% owned |

## Operational scale

| Figure | Canonical value |
|---|---|
| US credit-active consumers | ~**245 million** |
| Monthly record updates (US) | ~**1.3 billion** |
| Furnishers | ~10,000 |
| UK records shared | 350m+ across ~400 institutions |
| Free consumer members | **215m+ globally** (85m North America) |
| Consumer disputes | **>1 million per month, >12 million per year** |
| Reported dispute vendor economics | as low as **US$0.57 per dispute letter** |
| US credit invisible / unscorable | ~28m / ~21m (CFPB 2015 vintage: 26m / 19m) |
| Ascend | 2,300+ client solutions; 37 product capabilities |
| Attributes | 2,100+, rising to ~6,000 with cashflow data |
| Cloud | 10-year AWS agreement announced 19 June 2025 |
| NA top-account renewal | **100%**, durations +~10% to over four years |

## Pricing and the mortgage chain

| Figure | Canonical value |
|---|---|
| FY26 US mortgage revenue growth | **+45% on roughly flat volumes** |
| Total credit-report cost per conventional loan | ~US$50 (2022) → ~**US$540 (2026)** |
| FICO tri-merge base price | US$1.80 (late 2022) → US$30 (2026) |
| FICO wholesale royalty | US$4.95, **doubled to US$10.00 for 2026** |
| VantageScore 4.0 | FHFA-authorised 8 July 2025; 11 of the 15 largest lenders; ~30% of the US mortgage market |
| TransUnion VantageScore 4.0 price | US$4 per score for 2026 |

## Litigation and regulation

| Item | Canonical position |
|---|---|
| **CFPB v. Experian Information Solutions** | Filed 7 January 2025 (C.D. Cal.); motion to dismiss **denied 22 October 2025**; answered 3 November 2025; **JURY TRIAL 21 SEPTEMBER 2026**; no material provision recognised |
| ICO enforcement notice | Issued 27 October 2020 over ~51m adults' marketing data; substantially overturned by the First-tier Tribunal 20 February 2023; ICO appeal dismissed by the Upper Tribunal **23 April 2024**; ICO declined further appeal |
| CMA / ClearScore | Merger abandoned; reference cancelled 27 February 2019 |
| CFPB consent order | March 2017, US$3m civil penalty over score marketing |
| 2015 T-Mobile breach | ~15 million consumers; 40-state settlement November 2022 |
| Equifax breach (context) | 2017, 147 million consumers — the industry's defining event |
| Section 1033 | **Enjoined and being rewritten**; ANPR issued 22 August 2025 |
| FCA CIMS | Final report December 2023; CRGB replacing SCOR; consultation CP26/7 February 2026 |

---

# Appendix C — Reconciliation of Cross-Volume Discrepancies

The volumes were written sequentially against a moving evidence base. Discrepancies fall into two categories that must be kept apart: **basis, date and perimeter differences**, which are legitimate, and **genuine errors or supersessions**, which are not.

## Basis, date and vintage differences — not errors

| # | Item | Appears as | Resolution |
|---|---|---|---|
| 1 | **Group revenue** | US$8,445m versus US$8,425m | **Statutory total versus ongoing activities.** The US$20m difference is the exited Latin America and EMEA/Asia Pacific B2B lines re-presented from FY26. Both correct; state which. |
| 2 | **Benchmark EBIT** | US$2,407m versus US$2,397m | **Ongoing versus total.** The US$10m difference is the operating loss on exited activities. Volume IV uses both correctly in different contexts. |
| 3 | **Group growth rate** | +8% / +11% / +12% / +13% | **Organic / constant-currency / statutory actual / ongoing actual.** All four are correct on their stated basis and must never be used interchangeably. |
| 4 | **EPS** | 179.8 cents versus 164.5 cents | **Benchmark versus statutory basic.** The 15.3-cent gap is the subject of Part IV's reconciliation and is structural, not a one-off. |
| 5 | **Labour cost** | "32%" versus "31.8%" | Rounded versus precise. 31.8% governs. |
| 6 | **Credit invisible / unscorable** | 26m / 19m versus 28m / 21m | **Different vintages.** The 26m/19m figures are the CFPB's foundational 2015 measurement (as of 2010 data); the 28m/21m are the later-vintage figures used in Experian's own materials. Cite the vintage. |
| 7 | **Employee count** | ~25,200 versus 25,346 | Company statement versus a third-party estimate (Revelio, March 2026) on a possibly different consolidation basis. ~25,200 governs. |
| 8 | **Serasa market share** | ~60% | A 2012 Experian statement; no more recent published figure was established. Treat as approximate and dated. |
| 9 | **FICO royalty** | US$4.95 versus US$10.00 | **Sequential, not conflicting.** US$4.95 was the mortgage performance-model royalty; FICO doubled it to US$10.00 for 2026, drawing a Congressional oversight letter. The US$10.00 figure is current. |
| 10 | **Dispute volume** | ">1 million per month" versus ">12 million per year" | The same figure expressed at different cadences, both from the CFPB complaint. |
| 11 | **Credit Karma members** | ~99.5 million versus ~130 million | Intuit's reported figure versus media citations of cumulative sign-ups. The lower figure is the more defensible. |

## Genuine errors, corrections and supersessions

| # | Item | Status |
|---|---|---|
| 12 | **The T-Mobile breach settlement amount** | **UNRESOLVED DISCREPANCY.** Volume I records the Experian share of the November 2022 40-state settlement as **US$12.67m**; Volume IV records it as **US$13.67m**. Both cite the same multistate action, in which the combined Experian-plus-T-Mobile figure exceeded US$15–16m. The two figures are not reconciled here and one is a transcription error. Treat the settlement as **"approximately US$13m"** pending verification against a state attorney-general press release. |
| 13 | **Goodwill impairment arithmetic** | **PARTIALLY UNRESOLVED.** Volume V records two impairments totalling US$232m (US$53m FY21, US$179m FY23), both EMEA/Asia Pacific. Volume III records **accumulated** goodwill impairment of US$246m by 31 March 2023. The US$14m difference implies an earlier or smaller impairment not separately identified. The material conclusion is unaffected: **impairments have occurred only in EMEA/Asia Pacific; North America, Latin America and the UK have never been impaired.** |
| 14 | **Experian plc's domicile** | **CORRECTED.** An early characterisation described Experian as Dublin-headquartered. The verified position is a three-way split: **incorporated in Jersey** (registered office 22 Grenville Street, St Helier), **tax resident in Ireland**, **corporate headquarters in Dublin**, with operational hubs in Nottingham and Costa Mesa. All three descriptions are simultaneously true and are routinely garbled in secondary sources. |
| 15 | **Section 1033 status** | **SUPERSEDED WITHIN THE STUDY.** Earlier volumes treat the CFPB's open-banking rule as a live legal rail. Volume V establishes it is **enjoined and being rewritten** following litigation in the Eastern District of Kentucky, with an ANPR issued 22 August 2025 and the Sixth Circuit appeal stayed. The later position governs and materially weakens the near-term open-banking disruption thesis. |
| 16 | **File architecture attribution** | **LABELLED HYPOTHESIS, not fact.** The CFPB's 2012 white paper describes "at least one NCRA" as using a flat-file architecture. Attributing that specifically to Experian is inference, and Volume III labels it as such. Do not present it as established. |
| 17 | **Per-dispute agent time** | **NOT ESTABLISHED.** The US$0.57-per-dispute-letter figure comes from NCLC research on an unnamed bureau, not from the CFPB complaint, which names no offshore vendor and states no seconds-per-dispute figure. Volume III labels this correctly; secondary retellings often do not. |

## Known unknowns carried forward

- Per-inquiry bureau pricing, enterprise contract terms and marketplace referral economics.
- The Limpa Nome creditor take-rate.
- The paid-conversion rate of the 215 million free members and the subscription-versus-marketplace split within Consumer Services.
- The split of the US$3,078m intangibles balance between acquisition intangibles and internally generated software.
- Experian's internal match thresholds, validation stage counts and mixed-file rates.
- The identity of the group CISO and the scope of security certifications.
- Formal availability SLAs, RTO and RPO targets.
- Experian's dispute-operation offshore vendor and its contract terms.
- The CFPB's settlement posture and the penalty or redress sought.
- Deal values for Own Up, KYC360, AtData, NeuroID and Audigent.

---

# Appendix D — Source Hierarchy & Evidence Conventions

Sources were prioritised as follows, with primary evidence preferred wherever it existed:

1. **Experian plc's Annual Report and results announcements** — the FY26 report and results (year to 31 March 2026), segmental notes, the non-GAAP reconciliation, the cash-flow statement, the goodwill and intangibles notes, and the provisions and contingent-liabilities disclosure.
2. **Regulatory filings and enforcement records** — the **CFPB's complaint of 7 January 2025** and the subsequent docket including the order denying the motion to dismiss; the CFPB's larger-participant rule and supervisory publications; the **ICO's 2020 enforcement notice** and the First-tier and Upper Tribunal judgments; the **FCA's Credit Information Market Study** and CP26/7; the **CMA's ClearScore** decision; **FHFA** materials on VantageScore; and Brazilian material from the Banco Central and ANPD.
3. **Corporate registries** — the Jersey Financial Services Commission, the Irish CRO and UK Companies House.
4. **Litigation records** — FCRA class actions, mixed-file and reinsertion cases, and expert testimony describing matching logic. **For this subject, adversarial filings are the single richest window into internal operations**, since the company publishes very little about its systems.
5. **Industry bodies and standards** — the CDIA on Metro 2 and e-OSCAR, SCOR's Principles of Reciprocity, and the National Consumer Assistance Plan.
6. **Competitor filings** — Equifax and TransUnion 10-Ks and adjusted-measure reconciliations, which disclose segment detail in more granularity than Experian and permit benchmarking; and FICO's filings and public statements on score royalties.
7. **Independent research** — the **FTC's Section 319 FACTA accuracy studies**, the CFPB's credit-invisibles research, FinRegLab on cashflow underwriting and explainability, and **National Consumer Law Center** research on dispute handling and mixed files, used deliberately as a counterweight to company framing.
8. **Vendor case studies and job advertisements**, which for a company this reticent are among the few sources naming concrete systems.
9. Reputable financial and trade journalism: the Financial Times, Reuters, Bloomberg, American Banker, HousingWire and National Mortgage News.

SEO-oriented aggregators were not relied on where primary evidence existed. For strategically significant claims, sources were triangulated.

**Three conventions specific to this study.** First, **allegations are labelled as allegations**: the CFPB's descriptions of Experian's internal dispute and matching processes are pleadings in unresolved litigation, not adjudicated findings, and the study says so at every use. Second, **the prohibition on inventing architecture is absolute**: where Experian has published nothing about an internal mechanism, the study records UNKNOWN rather than describing a plausible-sounding system. Third, **company framing is treated as a claim to be tested**, not a conclusion to be adopted — this applies particularly to the "financial health" narrative around the consumer business and to the Benchmark presentation of earnings.

---

*End of the Experian Enterprise Reverse-Engineering Study.*
