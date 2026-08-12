# The Atruvia Enterprise Reverse-Engineering Study

**A forensic institutional teardown of Atruvia AG — the captive IT utility of the German cooperative banking sector**

Research cut-off: 8 August 2026
Prepared by: Damascus Research
Volumes I–V complete · Cross-Volume Synthesis included

---

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
