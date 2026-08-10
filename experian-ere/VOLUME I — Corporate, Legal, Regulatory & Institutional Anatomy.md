# EXPERIAN plc — Enterprise Reverse-Engineering Framework (EREF), Subject IV
## VOLUME I — Corporate, Legal, Regulatory & Institutional Anatomy
*Prepared as of 9 August 2026. Reporting basis: IFRS, US dollars, 31 March financial year-end. Non-GAAP measures (Benchmark PBT/EBIT/EPS, organic revenue growth) are labelled wherever used and never mixed with statutory figures in the same comparison.*

---

## TL;DR
- Experian plc is a **Jersey-incorporated, Irish-tax-resident, Dublin-headquartered, London-listed** information utility whose single most valuable and most misunderstood asset is not data it owns but the **legally-sanctioned aggregation of data contributed for free by its own customers** under reciprocity rules and statutory permission — a position that would take a new entrant a decade to replicate and, in the UK, is close to legally impossible to build from zero.
- The group is a **listed information utility with no controlling shareholder** (largest holder BlackRock ~5.9%); real control sits with a dispersed institutional register and the executive team, while the single most strategically decisive legal entity is **Experian Information Solutions, Inc.** (an Ohio corporation), the US FCRA bureau that generates the majority of group profit.
- Regulation is simultaneously Experian's **deepest moat and its largest tail risk**: the FCRA/CFPB, UK GDPR/ICO/FCA and Brazilian LGPD/Cadastro Positivo/Banco Central regimes are mutually incompatible, and the live **CFPB "sham investigations" lawsuit (7 January 2025)**, the 2015 breach settlements and the multi-year ICO litigation demonstrate that the enforcement surface is structural rather than incidental.

---

## Key Findings

1. **The three-way corporate split is confirmed by primary sources.** The FY26 results announcement (20 May 2026) states verbatim that Experian plc "is incorporated and registered in Jersey as a public company limited by shares and is resident in Ireland. The Company's registered office is at 22 Grenville Street, St Helier, Jersey, JE4 8PX, Channel Islands." Corporate headquarters are in Dublin (2 Cumberland Place, Fenian Street, D02 HY05); operational hubs are Nottingham (The Sir John Peace Building, NG80 1ZZ), Costa Mesa (California) and São Paulo. **The user's summary was correct** — with one nuance: the *registered office* is in Jersey, while Dublin is the *corporate HQ* and tax residence.

2. **The finance entity is the ghost of GUS.** Experian Finance plc (UK company 00146575, incorporated 17 March 1917) is the same legal person that was "The Great Universal Stores PLC" (1917–2001) and then "GUS plc" (2001–2006) — the retailer parent, repurposed after the 2006 demerger as the group's principal bond-issuing vehicle. This is a striking path-dependency: the retailer did not spin its credit department out into a fresh shell; the credit department kept the retailer's 108-year-old corporate shell as its treasury.

3. **Scale (FY26, year to 31 March 2026, primary source Experian FY26 announcement).** Statutory revenue US$8,445m (up 12%); Benchmark EBIT from ongoing activities US$2,407m at a 28.6% margin (up 50bps at actual rates); Benchmark EPS 179.8 US cents (up 15% at actual rates); statutory profit before tax US$1,951m (up 26% from US$1,549m in FY25); Benchmark tax rate 25.5%; post-tax ROCE 17.2%; net debt/Benchmark EBITDA 1.7x. North America delivered ~two-thirds of group revenue; Consumer Services now serves "over 215 million free members globally."

4. **The data-rights architecture is the institutional heart.** Experian largely does *not* own the raw data. It holds it under statutory permission (FCRA in the US; "protection of credit" under LGPD Article 7(X) and the Cadastro Positivo law in Brazil) and under contractual reciprocity (the SCOR Principles of Reciprocity in the UK). What Experian owns outright is the *aggregation*, the *derived attributes and bureau scores*, the *models* and the *identity-matching graph*.

5. **The enforcement record is extensive and continuing** (see enforcement table in I.6), spanning a 2017 CFPB consent order (US$3m), the 2015 T-Mobile breach settlements (~US$16m across the coalition), the ICO litigation (2020–2024, largely won by Experian), the abandoned ClearScore merger (CMA, 2018–19) and the live CFPB dispute-handling lawsuit (2025).

---

## Details

### I.1 Origin and Corporate History — Chronological Institutional Evolution

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

### I.2 Corporate Group Structure

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

### I.3 Ownership and Share Structure

Experian is a FTSE 100 constituent (ticker EXPN) with **ordinary shares on a one-share-one-vote basis, no dual-class or golden shares, and no controlling shareholder.** As most recently disclosed, the largest holders are global asset managers: **BlackRock ~5.9%**, with **The Vanguard Group** and **Massachusetts Financial Services** roughly level at ~5.1% each; Norges Bank Investment Management and Capital Group are also significant. The top ~25 shareholders together hold less than half the register, indicating a long tail of smaller holders. There is an OTC ADR/depositary programme (EXPGY/EXPGF). The group runs continuous buybacks (**US$725m executed in FY26**, plus a new **US$1bn programme announced May 2026 valid to 30 June 2027**) alongside a progressive dividend (FY26 total **69.25 US cents**, +11%).

**Economic and voting ownership do not diverge.** Control is contestable in principle: management can be removed by ordinary shareholder resolution, and there is no defensive bloc or family stake. In practice, control rests with the executive team, legitimised by a dispersed long-only institutional base that has historically backed the "Experian Way" strategy; there has been no public activist campaign. This is a materially different control structure from EREF Subjects II and III (Atruvia and DZ BANK), which are captive/cooperatively-owned — Experian is genuinely widely-held.

### I.4 Governance Architecture

- **Chair:** Mike Rogers (independent NED from 1 July 2017; Chair from 24 July 2019). He has confirmed retirement at the AGM on **22 July 2026** after nine years. **Adam Crozier** was named as incoming Chair (announced April 2026); the succession was led by Senior Independent Director **Alison Brittain**.
- **CEO:** Brian Cassin. **CFO:** Lloyd Pitchford. Both remained in post through 2026.
- **Committees:** Audit; Remuneration (**Kathleen DeRose** appointed chair from the July 2025 AGM); Nomination and Corporate Governance (chaired by the Chair).
- **Analytically significant governance gap:** there is **no dedicated board-level data-ethics/privacy committee.** For an enterprise whose entire franchise is the lawful processing of personal data across incompatible regimes, the absence of a standalone data/privacy board committee — with data-use decisions instead handled through management and the audit/risk apparatus — is a notable structural feature and, in this analyst's assessment, a governance weakness relative to the risk profile.
- The **UK Corporate Governance Code** applies despite Jersey incorporation. Executive pay is performance-linked to Benchmark EPS, organic revenue growth, ROCE and relative TSR.
- **Decision-rights map:** capital allocation and M&A → Board on management recommendation; data-use policy and permissible-use changes → management-led with board/risk oversight (no dedicated committee); new-jurisdiction entry → management/regional presidents with board sign-off on material commitments; pricing → business-line management; regulatory-enforcement response → CEO/CFO/General Counsel plus the relevant regional president and legal entity.

### I.5 Legal Architecture

**Data furnisher agreements.** In the **UK**, lenders furnish account and performance data into closed user groups (Experian's **CAIS** database) under the **Principles of Reciprocity** administered by SCOR; access is conditioned on contribution — "you only get out what you put in." Over 350 million records relating to ~400 institutions are shared industry-wide. In the **US**, furnishing is voluntary but governed by FCRA §623 furnisher-accuracy duties and the CDIA **Metro 2** reporting format; network effects produce near-universal participation. In **Brazil**, furnishing of *negative* data is governed by the Consumer Defence Code, and of *positive* data by the Cadastro Positivo law (LC 166/2019), under which furnishers have a **statutory duty** to transmit data to accredited GBDs. The precise commercial terms of individual furnisher contracts are private and **UNKNOWN**.

**Scoring IP — FICO and VantageScore.** Experian distributes **FICO** scores licensed from Fair Isaac *and* co-owns **VantageScore Solutions, LLC** (formed 2006) equally with Equifax and TransUnion — a cooperative venture between three direct competitors to challenge FICO's incumbency. After the **FHFA authorised VantageScore 4.0 for Fannie Mae/Freddie Mac conforming mortgages on 8 July 2025** (FHFA projected "Up to Five Million Prospective New Buyers to Qualify"), FICO's VP/GM of B2B scores Julie May attacked the arrangement, stating "there can be zero meaningful competition in the conforming mortgage market until the credit bureaus divest their ownership in VantageScore," and FICO characterised the bureau-owned venture as "a de facto monopoly." This is a live competition-law flashpoint embedded in Experian's own IP portfolio.

**Litigation is structural, not incidental.** As a CRA, Experian Information Solutions, Inc. is a routine FCRA defendant in individual and class actions over accuracy, tradeline reinsertion, mixed files and dispute handling. The headline current matter is the **CFPB "sham investigations" suit** (see I.6).

**Legal-responsibility mapping (Follow-the-Legal-Entity):** FCRA bureau liability → Experian Information Solutions, Inc. (Ohio); UK data-protection and FCA liability → Experian Limited (Nottingham); Brazilian LGPD/Cadastro Positivo liability → Serasa S.A.; D2C consumer liability → ConsumerInfo.com, Inc.; group debt liability → issued by Experian Finance plc and guaranteed by Experian plc.

### I.6 Regulatory and Data-Protection Architecture — PRIORITY DEPTH

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

### I.7 The Data-Rights Architecture — PRIORITY DEPTH (the institutional heart)

**Who contributes.** Banks, card issuers, telecoms, utilities, retailers, and public-record sources (electoral roll, county-court judgments, insolvency registers). Experian Information Solutions describes its US database as representing ~245 million credit-active consumers with ~1.3 billion updates flowing monthly.

**Why they contribute for free, and what they get.** In the **UK**, contribution is the *price of access*: SCOR's Principles of Reciprocity bind furnishers into closed user groups, and a lender that ceases contributing loses access to the equivalent shared data. Reciprocity is enforced contractually and by industry compliance exercises (SCOR-mandated questionnaires). In **Brazil**, positive-data furnishing is a *legal duty* under LC 166/2019 for accredited GBDs. In the **US**, furnishing is nominally voluntary but Metro 2 conventions and competitive parity produce near-universal participation. The consideration is symmetrical information: each furnisher gets a market-wide view of borrower behaviour it could never assemble alone.

**Legal basis to hold data, by jurisdiction.** US = FCRA statutory permissible-purpose regime; UK = UK GDPR **legitimate interests (Art. 6(1)(f))** for the bureau, with the **CRAIN** (Credit Reference Agency Information Notice) as the transparency mechanism — a basis the Tribunal litigation substantially validated for bureau (and less-intrusive marketing) processing; Brazil = LGPD Art. 7(X) plus the credit-specific statutes.

**Controller vs processor.** For the bureau databases Experian is a **data controller** (confirmed in the ICO Tribunal proceedings — the Tribunal agreed Experian was a controller regardless of whether it was labelled a "data broker"). For certain client-hosted decisioning/processing it acts as a processor; the marketing business is controller for its own compiled data.

**Consumer rights and the operating obligations they create.** Access; dispute/correction (FCRA §611 reinvestigation; UK GDPR Art. 16; Cadastro Positivo correction within 10 days); freeze/opt-out; and deletion where permitted. These rights generate enormous operating load — the entire CFPB 2025 suit is about the *dispute/reinvestigation* obligation, which is the single most operationally demanding consumer right for a bureau.

**What happens if a furnisher leaves.** Forward data flow stops; historical contributed data may generally be retained subject to statutory retention limits (e.g., ~6 years for UK defaults; FCRA §605 time-limits in the US). Precise contractual reversion/deletion terms are **UNKNOWN** (private contracts).

**Public-record vs furnished data.** Yes — these sit on a *different* legal footing. Public-record and electoral-roll data are collected under separate statutory/public-interest bases (the ICO case turned partly on the ~5.3m individuals whose *public-source* data Experian had not adequately notified), distinct from the reciprocity-governed furnished data.

**The central institutional question — what does Experian actually own?** Not the raw furnished data (held under permission). It owns: (a) the **aggregated database as a compiled work**; (b) the **derived attributes and bureau scores** it computes; (c) the **models** (and its one-third of VantageScore Solutions); and (d) the **identity-matching / linkage graph**. In one line: **Experian owns the refinery and the refined product, not the crude oil.** This is the deepest structural truth of the enterprise and is nowhere stated so plainly in its own disclosure.

### I.8 Regulation as Barrier, Cost and Moat

Regulation functions as a genuine moat through three distinct mechanisms:

1. **FCRA/permissible-purpose compliance capability is genuinely hard to replicate.** The accuracy, reinvestigation, adverse-action and freeze machinery is expensive, litigation-tested and slow to build; it is a de facto licence to operate that a new entrant cannot shortcut. (The very existence of the CFPB dispute-handling suit shows how demanding — and how central — this capability is.)

2. **The reciprocity principle operates as a legally-sanctioned exclusion mechanism.** A new bureau cannot obtain contributed data without already having contributors — a chicken-and-egg barrier. The FCA examined this directly in CIMS and concluded SCOR was not fit for purpose *precisely because* it could entrench incumbents; the proposed CRGB and common data format are explicitly designed to lower this barrier. This is the clearest case in the study of a moat that is simultaneously a regulatory target.

3. **The CMA's readiness to block Experian/ClearScore reveals the enforcement geometry.** Competition authorities police the *consumer-facing* layer (free credit-checking, comparison platforms) aggressively while leaving the *underlying bureau oligopoly* largely intact — because the bureau layer's barriers are seen as structural/data-driven rather than merger-driven. The lesson: Experian will be blocked from consolidating the consumer layer, but its core bureau position is not currently contestable by a challenger.

**Assessment:** the regulatory moat is real and durable, but it is a **double-edged asset** — the same regulatory density that excludes entrants is the largest source of enforcement, litigation and legislative tail risk. It is best characterised not as pure incumbency advantage but as a *legally-constructed network barrier* that regulators can, and in the UK are actively trying to, dismantle at the margin.

### I.9 Institutional Dependency Map

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

### I.10 Tax and Intercompany Architecture

**Jersey incorporation** (no corporate income tax; company-law flexibility) combined with **Irish tax residence** (management and control exercised from Dublin) produces a group tax charge that the company states is "influenced by the nature of its income and expenditure and prevailing Irish and Jersey tax laws." The **Benchmark tax rate was 25.5% in FY26** (FY25: 25.3%), with FY27 guided to ~26% — i.e., a *rising*, mid-20s effective rate, which argues *against* reading the Jersey/Ireland structure as aggressive tax minimisation. Group debt is issued through Experian Finance plc (the old GUS shell), Experian Europe DAC and Experian Finance US, Inc., all **guaranteed by Experian plc**; brand, models and data are licensed intra-group with attendant transfer pricing. The most defensible interpretation is that the Jersey/Ireland/UK/US split is an **artefact of the 2006 demerger and the group's international footprint** — a legacy of listing a Jersey-incorporated vehicle while running the business from Dublin, Nottingham and Costa Mesa — rather than a tax-optimisation construct. No material disclosed tax dispute was identified in this review (UNKNOWN if any minor uncertain positions exist).

### I.11 Corporate, Regulatory and Legal Risk Register

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

### I.12 Volume I Reconstruction

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

## Recommendations
1. **Track the CFPB *Experian* litigation (C.D. Cal., filed 7 Jan 2025) as the near-term binary.** An adverse judgment or settlement would set FCRA dispute-handling precedent for the whole industry and invite copy-cat class actions; a dismissal (plausible given the CFPB's 2025 posture reversal) would materially de-risk the sector. *Threshold that changes the view:* any dispositive ruling or a settlement figure disclosed as material.
2. **Watch the SCOR→CRGB transition and FCA CP26/7 (2026).** Mandatory reporting and a common data format could erode the reciprocity moat. *Benchmark to monitor:* whether the CRGB opens data access to thin-contribution new entrants — the single most important indicator of moat durability in the UK.
3. **Monitor VantageScore 4.0 conforming-mortgage adoption post-FHFA (8 Jul 2025).** A genuine shift in scoring economics and a competition-law flashpoint (FICO's "de facto monopoly" charge). *Threshold:* any DOJ/FTC or private antitrust action targeting bureau ownership of VantageScore.
4. **For counterparty due diligence, always contract with the correct legal entity:** FCRA obligations attach to Experian Information Solutions, Inc. (Ohio); UK data/FCA obligations to Experian Limited; Brazilian obligations to Serasa S.A.; debt exposure to Experian Finance plc under the Experian plc guarantee. Do not treat "Experian" as a single contracting counterparty.
5. **For Volume II (do not begin here):** carry forward the unresolved entity-registration items and the furnisher-contract terms as the priority primary-source targets (Irish CRO, Ohio SoS, California SoS, Serasa CNPJ via Receita Federal).

## Caveats
- Individual **furnisher contract terms**, **Serasa's exact current ownership percentage and CNPJ**, and the **states of incorporation of Experian Holdings Inc., ConsumerInfo.com and Experian Health** are **UNKNOWN/UNVERIFIED** from public sources and are labelled as such above; the 99.6% Serasa figure is the last publicly verified level (2012) and may since be higher.
- Financial figures are FY26 (year to 31 March 2026) on the bases labelled; **statutory and Benchmark measures are not mixed** in any single comparison.
- The **US CFPB enforcement posture is in flux** as of mid-2026; statements about 2025 dismissals and the medical-debt-rule vacatur reflect actions taken in 2025 and remain subject to appeal and legislative change.
- Some corporate-history dating (e.g., the exact 1996 sequencing of the TRW spin-out and GUS purchase, and pre-1980 pre-history) relies on secondary business-history sources and is corroborated where possible against Experian's own "Our history" disclosure; the PE-backer detail (Bain Capital, Thomas H. Lee) is from a reputable company-history source rather than a primary filing.
- This is a standalone Volume I on Experian; structural contrasts with EREF Subjects I–III (Wise, Atruvia, DZ BANK) are noted only where analytically useful. **Volume II has not been started.**