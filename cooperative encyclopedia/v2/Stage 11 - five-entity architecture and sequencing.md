# PART VI (REVISED) — THE FIVE-ENTITY ARCHITECTURE AND THE DESIGN BRIEF

*Stage 11 · The Cooperative Encyclopedia: Legal Form, Capital, Governance and the Nigerian Path*

*Preserved by reference and not reproduced here: VI.1 (the transplant problem — Guinnane's failed Irish transplant, Colvin and McLaughlin on the Netherlands, and the self-contained / institution-dependent / culture-or-scale-dependent classification); VI.2 (the ten-mechanism transplant audit); VI.3 (what Nigeria has that the comparators lack — the permissive statute, low formation threshold, tax treatment, the diaspora remittance market, and the ajo/esusu/adashe social-collateral tradition); and the fourteen-clause bye-law specification, which remains valid for the cooperative entity. This revision rewrites the design space, the recommendation, the sequencing, the early-warning indicators, the falsification conditions and the propositions — now for a five-entity architecture.*

---

## TL;DR

- **A founder with ~₦50 million cannot start five financial institutions within three years.** The licences alone — credit bureau ₦500m, PSB ₦5bn, and the apex's bank-level capital of ₦5–50bn — exceed his entire capital by one to two orders of magnitude. The "all five within three years" ambition is not fundable and must be replaced by a trigger-gated sequence.
- **Two of the five fail on their own logic under founder ownership.** The **central/apex institution loses its entire rationale** — it mutualises nothing if one man owns it, so it is simply a wholesale bank he happens to own, carrying bank capital and delivering no cooperative benefit — and should be **dropped**. The **credit bureau should not be a separate company at all**, but a furnishing-and-scoring feature of the platform, deferred until six trigger conditions converge.
- **Build in this order, gated on triggers not dates:** (1) the platform on an open-source core (Apache Fineract/Mifos) with the data-rights chain written in at launch; (2) the anchor cooperative society, pre-sold as tenant; (3) remittance as naira-payout sub-agent of a licensed IMTO — never an own IMTO licence; (4) a bureau *feature*, not a fifth company; and treat the apex as abandoned. The single non-negotiable proceed-gate is a **second, independent, paying tenant** — until then the founder has a bespoke build, not a product.

---

## Key Findings

**1. The arithmetic is decisive and adverse.** The five entities as licensed businesses require, at minimum: a credit bureau's ₦500,000,000 refundable capital deposit with the CBN [CF]; a Payment Service Bank's ₦5,000,000,000 [CF]; a national MFB's ₦5,000,000,000 or a state MFB's ₦1,000,000,000 [CF]; and, if the apex were a real wholesale bank, merchant-bank capital of ₦50,000,000,000 [CF]. Against ₦50m of starting capital, the bureau licence alone is ten times the entire war-chest, and the apex a thousand times it. ₦50m starts the platform *or* buys one Super-Agent licence (₦50m), not both.

**2. Founder ownership dissolves the apex's reason to exist.** DZ BANK is the central institution for "the approximately 700 cooperative banks in Germany, which hold a majority stake in DZ BANK" (DZ BANK profile) and is Germany's second-largest bank by assets [CF]; per the Co-operative Bank of Kenya's own account, shares "were ring-fenced under Coop Holdings Co-operative Society Limited which became the strategic investor in the Bank with a 64.56% stake," representing 3,805 cooperative societies and unions and over 15 million members [CF]. In both, the apex mutualises members' solvency *because the network owns it*. A founder-owned apex mutualises nothing and relocates nothing. It retains no cooperative rationale and should be dropped.

**3. The bureau is a feature, not a firm — and the state is already in the niche.** The Credit Reporting Act 2017 makes cooperative societies eligible Credit Information Providers, and the operative lawful basis for the bureau is the cooperative furnishing a *licensed* bureau — a chain that must be written into launch terms because it cannot be retrofitted. Nigeria's three private bureaus (CRC, established 2008; CreditRegistry, corporate roots to 2003; FirstCentral, formerly XDS, final licence 2009) are genuine ~15-year incumbents [CF]. The government's CoopCHECK (powered by CreditRegistry) and CREDICORP's NIN-anchored scoring are moving into exactly the cooperative niche — though, as of 2026, both remain announced intentions rather than operating fact.

**4. The conflict lattice is uncurable by firewalls where conflicts sit at the level of *role*.** One person as vendor-to-cooperatives, owner-of-a-competing-cooperative, operator-of-the-apex-that-clears-their-funds, and owner-of-the-bureau-that-scores-their-members holds conflicts that disclosure and Chinese walls cannot cure. At minimum the founder must not own both a competing anchor cooperative and the bureau that scores rival cooperatives' members.

**5. There is a fundable plan — but it is three entities built in sequence, not five in parallel.** Platform (open-source core) → anchor cooperative → remittance sub-agency → bureau-as-feature, gated on a second independent paying tenant and on the data-rights chain being present at launch.

---

## Details

### VI.4 (revised) — The five entities, each interrogated for its rationale under founder ownership

The original Part VI asked whether a single cooperative fintech could be transplanted into Nigerian soil. The plan has since fractured into five entities, all wholly owned by one founder. The right question is no longer "can it be transplanted?" but a sharper one the founder has not yet been asked of each entity in turn: **does this thing still have a reason to exist once it is founder-owned rather than member-owned?**

Ownership is not a detail of the design; in cooperative institutions it *is* the design. The entire benefit architecture of Parts II and IV — capability relocating to the network, solvency mutualised across primaries, the substitute monitor supplied by collective ownership — is contingent on *who owns the thing*. Change the owner from "the network" to "one man" and, for some entities, the benefit survives untouched; for others, it evaporates entirely while the cost and the licence remain. We take each in turn.

#### Entity 1 — The platform (core banking software for cooperative societies)

**What it is.** A software vendor selling core-banking capability to cooperative societies: ledgers, member records, savings and loan management, reporting, and the integration points to payments and identity rails. Founder-owned permanently, with contractual protections instead of equity — explicitly the Fiserv/Jack Henry vendor model (an arm's-length supplier selling to institutions it does not own) rather than the Atruvia model. The distinction is instructive: Atruvia AG, "one of the largest IT service providers in Germany… serving 91 million bank accounts, 155,000 banking workplaces" on roughly EUR 1.7 billion in revenue (IBM case study), is *owned by* the German cooperative financial group it serves. The founder is choosing, correctly, the opposite structure — because the German model presupposes a pre-existing owned network he does not have.

**What problem it solves.** Nigerian cooperative societies overwhelmingly run on paper, spreadsheets and the cashbook. A shared, standardised platform gives them a general ledger that reconciles, member data that survives a change of secretary, and — critically — the data substrate on which every later entity (remittance, bureau, apex) depends. The platform is the keystone: without it there is no data layer, and without the data layer none of the other four entities has anything to work with.

**Does founder ownership preserve or destroy the rationale?** It preserves it. A vendor is a vendor. Fiserv is not owned by the thousands of US banks and credit unions it serves, and no one thinks its software is worse for it. The permanent-founder-ownership model (Part VII's "Option 4") is the global vendor norm and, given that no cooperative cluster yet exists to *do* the owning, it is the only buildable option. But — and Part VII was emphatic — it is **second-best for the cooperatives**, because the Part IV benefit (capability relocating into the network so that the network eventually controls its own rails) never accrues. The founder remains the permanent chokepoint. In Part III's taxonomy of seven capture types, **the founder is the external-capture vector by construction**: he sits outside the mutual, owns the rail every member rides, and cannot be voted out because members hold no equity in him. This is not a flaw to be fixed; it is a structural feature of the vendor model that must instead be *fenced* by contract.

**What makes it defensible.** Part VII's contractual architecture is precisely the fencing: (a) verified escrow holding a full operational source-code and configuration deposit, released on defined triggers; (b) tenant-vested data with genuine portability, so a cooperative can leave and take its ledger with it; (c) capped exit and price terms, so the chokepoint cannot be monetised abusively; (d) real SLA remedies with teeth, not credits that never pay out; (e) an advisory council (candidly, near-theatre — it signals voice without granting control); and (f) most acute of all, **key-person and business-continuity protection**, because one owner means every tenant's operational continuity depends on one human life. The escrow and continuity provisions are not niceties; they are the difference between a defensible vendor and a single point of catastrophic failure.

**Capital and licence.** The platform itself needs *no CBN licence until it touches money*. It is software. But it becomes **indirectly bound by the CBN's Risk-Based Cybersecurity Framework for Other Financial Institutions** the moment its tenants include microfinance banks, and it must **register with the NDPC as a data controller/processor of major importance** — the threshold being processing the personal data of more than 200 data subjects in six months, which a multi-tenant cooperative platform crosses on essentially day one. Build cost is the real number, addressed in VI.5.

**Verdict: BUILD. Rationale survives intact.** The platform is the keystone and the only entity whose logic is undamaged by founder ownership. Two design rules are non-negotiable and flow from Parts VII and VIII: **multi-tenant at the data layer from day one; operational multi-tenancy on the first external contract**; and the **data-rights chain written into platform and cooperative terms at launch**, because (per VI.6 and Part VIII) you cannot lawfully repurpose data collected under a narrower notice.

#### Entity 2 — The cooperative society (anchor tenant and proving ground)

**What it is.** A registered primary cooperative society under the relevant state Cooperative Societies Law (the Nigerian framework descending from the 1993 statute), which will be the platform's first tenant, its live testing ground and its reference customer.

**What problem it solves.** A platform with zero tenants cannot be debugged, demonstrated or sold. The anchor cooperative gives the founder a controlled environment to harden the software against real member behaviour — real deposits, real loan cycles, real month-end — before exposing it to an independent paying customer. It is also the vehicle through which the *cooperative benefit* is actually delivered to real members: social-collateral lending in the ajo/esusu/adashe tradition, member savings, and eventually access to remittance and thin-file credit scoring.

**Does founder ownership preserve or destroy the rationale?** The rationale as *proving ground* survives cleanly. The rationale as *cooperative* is more delicate, because a cooperative is defined by member control, and a founder who both runs the platform and dominates the anchor society risks a society that is cooperative in name and captured in fact. This is Part III's **internal capture** risk sitting directly next to the **external capture** vector of the platform. The mitigations are the Part VI.6 bye-law specification (the fourteen clauses, preserved by reference — participation quorums, board tenure limits, contestable elections, the insider-lending cap) and a genuine handover of governance to members as the society matures. Under a proper bye-law regime and a real membership, the anchor can be a genuine cooperative. Under founder domination it becomes what Part VIII called the founder's **conflict problem** — because this same society is simultaneously his customer, his lab, and (once the bureau exists) a competitor to every *other* cooperative whose members the bureau will score.

**Capital and licence.** Formation is cheap — the low formation threshold is one of the things Part VI.3 identified as a Nigerian advantage. The society registers with the state Registrar under the Cooperative Societies framework; it needs no CBN licence to take members' savings and lend to members, because **members-only deposit-taking is lawful**. The bright line, from Parts IV–V, is BOFIA §2: soliciting or accepting deposits *from the general public* is a criminal offence under §2(2). The anchor society must stay strictly members-only or it commits a crime.

**Verdict: BUILD — but govern it honestly.** The rationale survives. The danger is not legal but characterological: a captured "cooperative" that exists to validate the founder's software rather than to serve its members. The bye-laws and, later, real member control are what keep it a cooperative rather than a prop.

#### Entity 3 — The remittance capability

**What it is.** A capability to receive diaspora remittances and pay them out to cooperative members in naira. The CBN's Balance of Payments data record personal remittances "rising by 8.9 per cent to $20.93bn" in 2024, with IMTO inflows up 43.5% to $4.73bn — a market of obvious relevance to a membership drawn substantially from working Nigerians with relatives abroad [CF].

**What problem it solves.** Remittance is the single most reliable recurring inflow into the exact households cooperatives serve. Capturing the payout leg — turning the cooperative into the place a member's diaspora money lands — deepens the member relationship, funds the deposit base, and generates fee margin, all without the cooperative taking currency risk.

**Does founder ownership preserve or destroy the rationale?** It preserves it, because remittance payout is a *service*, not a mutual-ownership benefit; whether the founder or the members own the entity that performs it changes nothing about its value to the member. What constrains the design is not ownership but the licence wall.

**Capital and licence — the hard constraint.** The three-regime problem from Parts IV–V governs absolutely. A cooperative society can never itself hold a CBN or IMTO licence; it must own a CAMA company that does. And the IMTO route is closed to this founder on two independent grounds: the **2024 CBN Guidelines set indigenous-IMTO minimum share capital at the naira equivalent of US$1,000,000** [CF] (roughly ₦900m–₦1.6bn depending on the rate), and — decisively — the same guidelines **bar fintechs from obtaining IMTO approval** altogether [CF]. An own IMTO licence is therefore both unaffordable and legally unavailable. The only lawful route is as **naira-payout agent or sub-agent of an already-licensed IMTO** — the cooperative's CAMA company partners with a licensed IMTO and (through an authorised dealer bank) disburses naira to members' accounts. Post-2024, all inbound remittances must be paid to beneficiaries in naira through a bank account or cash [CF], and IMTOs must route disbursements through designated naira settlement accounts at authorised dealer banks — so the founder's entity slots in as the last-mile member-facing agent, not the principal. Eventually, at far greater scale and capital, a Payment Service Bank licence (₦5bn) would allow holding customer funds directly; that is a decade-out proposition, not a year-one one.

**Verdict: BUILD — as sub-agent, never as principal.** Rationale survives; the route is agent/sub-agent of a licensed IMTO. Attempting an own IMTO licence would be both illegal (fintech bar) and unaffordable (US$1m). This is a partnership and integration task, not a licensing task, and it is therefore genuinely achievable on modest capital.

#### Entity 4 — The central / apex institution *(interrogated hardest)*

**What it is, in the cooperative tradition.** An apex or central institution exists to sit *above* a network of primary cooperatives and do for them collectively what none can do alone: pool liquidity, mutualise solvency, clear payments among members, hold the network's reserves and represent it. DZ BANK is the central institution for the approximately 700 cooperative banks that *hold a majority stake in it* [CF]; the Co-operative Bank of Kenya, founded in 1965, is today **64.56% owned by Co-op Holdings Co-operative Society Limited**, the vehicle that ring-fenced the shares of 3,805 cooperative societies and unions [CF]. The defining feature in every genuine case is the same: **the primaries own the apex.**

**Why Part II said the apex matters.** Part II established that the institutional protection scheme — the mutual guarantee that makes a cooperative network resilient — *relocates capital to the network because the network owns it*. When a primary society is in trouble, the apex can support it because the apex's capital is, in substance, the primaries' own pooled capital, contributed and controlled by them. The solvency of each is mutualised into the solvency of all. That is the entire point.

**Now apply founder ownership — and watch the rationale vanish.** If the founder owns the apex, then when a member cooperative is in trouble and the apex supports it, whose capital is being deployed? The founder's. Not the network's. Nothing is mutualised, because the primaries contributed nothing and own nothing. Nothing is relocated *to the network*, because the capital never belonged to the network. What is left when you strip out mutualisation and relocation? A **wholesale bank that one man happens to own**, lending to and clearing for cooperatives that are his customers. It carries full bank capital requirements — merchant-banking capital under the 2024 recapitalisation is **₦50,000,000,000** [CF], and even a national MFB acting as a quasi-wholesale lender is ₦5bn — and it delivers, in exchange, *none* of the cooperative benefit that was the only reason to prefer an apex to an ordinary bank in the first place. It is all of the cost and none of the point.

This is the cleanest example in the entire study of a feature whose value is *institution-dependent* in the VI.1 sense: it works only inside the ownership structure that generates it. Transplant the box (a central institution) without the soil (collective ownership by the primaries) and you have transplanted a dead thing.

**Verdict: DROP under founder ownership. It has no rationale.** Say it plainly to the founder: a founder-owned apex is not a cooperative apex; it is a wholesale bank with a cooperative logo, and it requires ₦5–50bn to deliver a benefit it structurally cannot deliver.

**What should replace it.** Three things, in ascending order of scale:
1. **Correspondent and agency relationships** with existing licensed banks for clearing and settlement — buy the plumbing, don't build the bank. This is what the remittance sub-agency already implies.
2. **The NPF precedent, deferred.** Part V's governing precedent is that **a cooperative can lawfully control a CBN-licensed MFB — the Nigeria Police Co-operative Society Limited holds about 62.6% of NPF Microfinance Bank Plc** (NGX: NPFMCRFBK) [CF], which its MD describes as having "grew[n] from a capital base of ₦500,000 in 1993 to shareholders' funds of about ₦13 billion today," serving 1.5 million customers (Vanguard, Jan 2026) [CF]. If, years out, the cooperative network genuinely accumulates the capital and the members, the *network* (not the founder) can control an MFB — and *that* MFB, owned by the cooperatives, would be a genuine apex-like institution because it satisfies the ownership condition the founder-owned apex fails. The route to a real apex runs through member ownership, and the founder cannot short-circuit it by owning it himself.
3. **CREDICORP and the RH-CRRP's proposed Cooperative Bank of Nigeria** may occupy this apex space at the national level before any single founder could; the founder should plan to *connect to* a national apex, not to *be* one.

#### Entity 5 — The credit bureau

Part VIII's analysis is preserved by reference; the verdict is restated and integrated here because it drives the whole recommendation.

**What it is and what it solves.** A credit bureau collects borrower repayment data, builds it into scores, and sells the scores to lenders. The value proposition for cooperatives is thin-file scoring: bringing members with no formal credit history into the credit system on the strength of their cooperative repayment behaviour.

**Does founder ownership preserve or destroy the rationale?** Founder ownership is not even the binding problem here — four other problems bind first, and Part VIII worked through each:

- **Holding the data is not permission to use it.** The platform is a data *processor*; the bureau would be a separate data *controller* for a new purpose. Under the Nigeria Data Protection Act 2023, that repurposing is lawful only if members were noticed at collection. The operative lawful basis is the cooperative acting as a **Credit Information Provider under the Credit Reporting Act 2017**, furnishing a *licensed* bureau — not consent, not bare legitimate interest. **This chain must be written into the platform and cooperative terms at launch; it cannot be retrofitted**, because you cannot lawfully repurpose data collected under a narrower notice.
- **The platform does not solve the reciprocity cold-start.** A viable bureau needs four things: data supply, the legal right to use it, standalone predictive value, and paying lender demand. The platform supplies at most one and a half of the four (some data, and part of the legal right if the chain is written in). It supplies neither predictive value at launch nor paying demand.
- **The Quod verdict governs.** When Brazil's five largest banks built their own bureau (Quod, formed 2016, each of the five holding 20%) with their own data and regulatory blessing, they could not dislodge Serasa — which Experian described as "the market leader in Brazil, with approximately 60% market share" [CF]. If five giant banks could not dislodge an incumbent with every advantage, one founder cannot dislodge three fifteen-year Nigerian incumbents. The bureau survives, at most, as a **complement** serving thin-file cooperative members — not as a challenger.
- **The capital wall is absolute.** A Nigerian credit bureau requires a **₦500,000,000 refundable minimum capital deposit with the CBN** [CF] — ten times the founder's entire starting capital.

**And the state is already in the niche.** The RH-CRRP's proposed **CoopCHECK Credit Bureau, powered by CreditRegistry**, and **CREDICORP's** NIN-anchored national scoring both aim at exactly the cooperative/thin-file segment, with more capital and — via the NIN — a better identity rail than any founder can assemble. (Their 2026 status is treated in VI.10; both are, as of now, announced rather than operational.)

**The conflict is uncurable by firewalls** because it is a conflict of *role*, not of data: the founder as owner of a competing anchor cooperative cannot credibly own the bureau that scores rival cooperatives' members. At minimum, the founder **should not own both the competing anchor cooperative and the bureau**.

**Verdict: NOT a fifth company.** The bureau should be **a product of the platform — a furnishing-and-scoring feature plus a partnership margin** (the platform furnishes members' repayment data, under the CRA-2017 chain, to a licensed incumbent bureau or to CoopCHECK, and resells scores back to cooperatives) — **deferred or abandoned as a standalone entity until six trigger conditions converge** (VI.8).

### VI.5 (revised) — The capital reconciliation: the arithmetic, stated plainly

Set the requirements beside the ₦50m and the picture is not ambiguous.

| Entity / licence | Minimum capital | Tag |
|---|---|---|
| Cooperative society (formation) | Nominal (low threshold) | [CF] |
| Platform build (from scratch, ground-up) | ₦150m–₦400m+ over 2–3 yrs (est.) | [AI] |
| Platform build (open-source-core assembly) | ₦30m–₦80m (est.) | [AI] |
| Super-Agent licence (agency banking) | ₦50,000,000 | [CF] |
| PSSP (payment solution service provider) | ₦100,000,000 | [CF] |
| PSS (payment solution services, full) | ₦250,000,000 | [CF] |
| Unit MFB Tier 2 / Tier 1 | ₦50m / ₦200m | [CF] |
| State MFB | ₦1,000,000,000 | [CF] |
| National MFB | ₦5,000,000,000 | [CF] |
| MMO (may hold customer funds) | ₦2,000,000,000 | [CF] |
| Switching & processing | ₦2,000,000,000 | [CF] |
| Payment Service Bank | ₦5,000,000,000 | [CF] |
| IMTO (indigenous) | US$1,000,000 (~₦900m–₦1.6bn) + fintechs barred | [CF] |
| **Credit bureau** | **₦500,000,000 (refundable, at CBN)** | **[CF]** |
| Apex as merchant bank (if it survived) | ₦50,000,000,000 | [CF] |

**The total.** Even the *minimum* licensed version of the five-entity plan — platform + Super-Agent + a state MFB + remittance-via-PSB + bureau, and *excluding* the apex entirely — sums to roughly **₦500m (bureau) + ₦5bn (PSB) + ₦1bn (state MFB) + ₦50m (Super-Agent) + ₦150m+ (platform) ≈ ₦6.7 billion**, before working capital, professional fees, or the separate refundable escrows the CBN demands on top of paid-up capital (a PSS applicant, for instance, escrows a further ₦250m). Add the apex as a genuine wholesale bank and the number runs to **₦11.7bn–₦56.7bn**. Against this, ₦50 million is **0.75% of the no-apex minimum and under 0.1% of the with-apex figure.**

**How far ₦50m goes, stated plainly.** ₦50 million is enough to: register the cooperative society; assemble a platform on an open-source core with a small team; register with the NDPC and stand up cybersecurity controls; and *either* hold a single Super-Agent licence *or* fund the platform build — **not both**. It is not remotely enough for the bureau, the PSB, an MFB above Tier 2, an IMTO, or the apex. Part VII's conclusion stands without qualification: **"all five started within three years" is not achievable on ₦50m as a from-scratch build.**

**The four levers, worked through.** Part VII identified four things that could change the arithmetic. Here is what each actually buys:

1. **Open-source-core assembly instead of ground-up build.** Apache Fineract (the Apache Software Foundation's core-banking engine) and its Mifos distribution are genuinely production-grade: the Mifos Initiative reports that "more than 20 million clients supported by 400+ fintechs and financial institutions use our open APIs… across 41+ countries," and one African lender, Advancly, reported saving a year of build time by starting on Mifos rather than from scratch. This is the single highest-leverage decision available: it can cut the platform build from a multi-hundred-million-naira, multi-year effort to something a ₦50m budget can begin. **Caveat (vendor material used with caution):** Fineract/Mifos and their implementation partners promote their own product; "16 weeks to go live" is a vendor claim, not an independent benchmark, and Nigerian cooperative-specific configuration, data migration, security hardening and regulatory integration will extend it materially. Treat open-source-core as *decisive for feasibility* but not as *free*.

2. **Pre-selling the anchor tenant.** If the anchor cooperative (and, better, a second independent cooperative) commits to pay before the build completes, the platform is funded partly by revenue rather than entirely by capital, and — more importantly — it converts the project from a speculative product into a contracted one. This directly attacks Part VII's "one captive customer validates nothing" problem.

3. **Sequencing rather than parallelising.** Building the entities one at a time, each funding the next, is the only way ₦50m can touch a multi-billion-naira licence ladder at all: the platform's revenue and the anchor's deposit growth become the capital base for the next step. Parallelising guarantees that ₦50m is spread so thin it completes nothing.

4. **Raising external capital.** This is the lever that works arithmetically and *fails strategically*: external equity is exactly the outside ownership the founder built the whole permanent-founder-ownership model to avoid. It reintroduces the external-capture vector at the *ownership* level rather than the vendor level. External *debt* (development-finance lines, CREDICORP wholesale funding, grant capital) is less corrosive to control and should be preferred where available; external *equity* should be a last resort and, if taken, should be taken into the licensed operating subsidiaries (the MFB, the PSB) rather than into the platform holding company, so that the founder keeps the rail even if he shares the bank.

**What combination makes the plan fundable?** Only this: **open-source core (lever 1) + pre-sold anchor and second tenant (lever 2) + strict sequencing (lever 3)**, with external *debt* (not equity) considered only at the MFB/PSB step years later. That combination funds a *three-entity* plan (platform, cooperative, remittance-sub-agency) plus a bureau *feature*. It does not fund five licensed institutions, and no honest sequence pretends otherwise. **Do not produce a sequence the capital cannot fund** — so the recommended sequence (VI.7–VI.8) is explicitly a three-entity sequence with two entities dropped or demoted.

### VI.6 (revised) — The conflict lattice across five entities

Part VIII mapped the conflicts around the bureau. Extended across all five roles the founder proposes to hold simultaneously, the lattice looks like this. Read each cell as "Founder as ROW is conflicted with Founder as COLUMN over WHAT."

| Founder as ↓ / vs → | Platform vendor | Anchor cooperative | Remittance sub-agent | Apex/wholesale | Bureau |
|---|---|---|---|---|---|
| **Platform vendor** | — | Pricing & data terms to a tenant he controls | Data flows & fees | Clearing data access | Data repurposing rights |
| **Anchor cooperative** | Gets favoured terms vs other tenants | — | Preferential payout | Preferential liquidity | **Its members scored by an owner who runs a rival** |
| **Remittance sub-agent** | — | Steers flow to own society | — | Self-clearing | Transaction data into scores |
| **Apex/wholesale** | Prefers own platform | Rescues own society first | — | — | Lending decisions using own bureau |
| **Bureau** | Buys data cheap from own platform | **Scores competitors of own cooperative** | Ingests own remittance data | Feeds own lending | — |

**Classify each conflict by its only available cure:**

- **Curable by firewall / technical control (data-layer separation, access logging, purpose limitation):** the platform-vendor-vs-bureau *data* conflicts. Multi-tenant data isolation, the CRA-2017 furnishing chain and NDPC purpose-limitation controls genuinely address these — because the conflict is about *data handling*, and data handling can be walled.

- **Curable by disclosure (transparent, published terms):** the platform-vendor-vs-tenant *pricing* conflict. Capped, published, uniform price and exit terms (Part VII) mean every tenant sees the same schedule, so the founder cannot secretly favour his own society on price. Disclosure works here because the harm is *hidden preference*, and publication removes the hiding.

- **Curable by governance (independent boards, member control, related-party rules):** the anchor-cooperative-vs-network conflicts around liquidity and rescue preference. Genuine member control of the anchor (the bye-laws), independent directors on any licensed subsidiary, and hard related-party-transaction limits (mirroring the SASRA insider-lending discipline in VI.9) can contain these — *if* the governance is real rather than theatre.

- **Uncurable — require an entity to be given up:** the **role-level** conflicts, chiefly **anchor-cooperative-vs-bureau**. No firewall cures the fact that the man who owns a competing cooperative also owns the machine that scores every rival cooperative's members and decides who is creditworthy. This is not a data problem (walls won't fix it), not a pricing problem (disclosure won't fix it), and not a board problem (governance inside one entity can't fix a conflict *between* two entities one person owns). It is a conflict of *interest at the level of role*, and the only cure is to not hold both roles. Part VIII's minimum condition is the operative rule: **the founder must not own both the competing anchor cooperative and the bureau.** The apex-vs-everything conflicts are in the same uncurable class, which is a second, independent reason (beyond VI.4's rationale failure and VI.5's capital wall) to drop the apex.

**Specific recommendation on defensible ownership.** One person can defensibly own, simultaneously: **(1) the platform, (2) the anchor cooperative, and (3) the remittance sub-agency** — because the conflicts among these three are all firewall-, disclosure- or governance-curable, provided the controls are actually built. One person **cannot** defensibly own the bureau *as well as* the competing anchor cooperative (role conflict, uncurable), and **should not** own the apex at all (no rationale, unaffordable, role-conflicted). Therefore the defensible maximal set is **{platform, anchor cooperative, remittance sub-agency}**, with the bureau demoted to a platform *feature* that furnishes an *independent* licensed bureau (so the scoring is not done by the founder), and the apex abandoned.

### VI.7 (revised) — The recommended architecture: commit and defend

Having interrogated all five, the study commits to the following. This is a decision, not a menu.

**BUILD (three entities + one feature):**
1. **The platform** — founder-owned permanently, assembled on an **open-source core (Apache Fineract / Mifos)**, multi-tenant at the data layer from day one, with the full Part VII contractual-protection architecture (escrow, tenant-vested portable data, capped price/exit, SLA remedies, key-person/continuity cover) and the **CRA-2017 data-rights furnishing chain written into terms at launch**. NDPC registration as controller/processor of major importance from the outset.
2. **The anchor cooperative society** — members-only (BOFIA §2 line respected absolutely), governed under the VI.6 fourteen-clause bye-laws, pre-committed as the platform's first paying tenant.
3. **The remittance sub-agency** — a CAMA company owned by the cooperative (or by the founder alongside it), operating as **naira-payout agent/sub-agent of a licensed IMTO** through an authorised dealer bank. Never an own IMTO licence (fintech bar + US$1m).
4. **The bureau — as a platform feature, not a company** — furnishing members' repayment data, under the CRA-2017 chain, to an *independent* licensed bureau (CRC / CreditRegistry / FirstCentral) or to CoopCHECK if and when it becomes operational, and reselling scores back to cooperatives for a partnership margin.

**DEFER (revisit only on trigger):** a standalone licensed credit bureau (₦500m; six triggers in VI.8); any MFB above Tier 2; a PSB.

**DROP / RESTRUCTURE:** the **central/apex institution** — dropped as a founder-owned entity (no rationale, ₦5–50bn, uncurable role conflicts). Its functions are met by correspondent/agency relationships now, and — years out and only under *member* ownership — potentially by the NPF-style route of the cooperative network controlling an MFB.

**Ownership and capital at each step.** Platform: founder-owned holding company, funded from the ₦50m + anchor revenue, open-source-core keeping the build inside budget. Cooperative: member-owned in form, pre-sold as tenant. Remittance: CAMA subsidiary, capitalised only to the modest level an IMTO sub-agency requires (partnership, not licence). Bureau feature: near-zero incremental capital — it is code plus a data-exchange agreement. External *debt* (DFI lines, CREDICORP wholesale funding) considered only at a future licensed-banking step; external *equity* avoided, and if ever taken, ring-fenced into the licensed subsidiary rather than the platform. Note CAMA 2020 makes this structuring easy: it permits single-shareholder, single-director companies and a holding-company/subsidiary group, so the founder can lawfully own a platform holdco with the licensed operating companies beneath it.

**What the founder gives up by following this.** He gives up the apex (and with it the fantasy of owning the whole vertical stack), the standalone bureau (and its licence-fee revenue and data ownership), and the three-year "all five" timeline. He accepts that the platform's Part IV benefit — capability relocating to a network that owns its own rails — will not accrue while he owns the platform permanently; he remains the external-capture vector, fenced by contract rather than dissolved by ownership.

**What he risks by not following it.** If he insists on five-in-three-years on ₦50m, the deterministic outcome is capital spread so thin that *nothing* reaches a licence threshold: an unfinished platform, an undercapitalised society, a bureau that never clears ₦500m, and an apex that is a PowerPoint slide. He risks NDPA liability (unlawful data repurposing if the chain is retrofitted rather than built in), BOFIA §2(2) criminal exposure (if the society drifts into public deposits to fund the shortfall), and a conflict lattice so visibly self-dealing that no *independent* cooperative ever becomes the second paying tenant — which, per the next section, is the one thing that proves the whole enterprise is a business at all.

### VI.8 (revised) — The sequencing plan: trigger conditions, not dates

Because the three-year ambition is not fundable, the plan advances on **triggers, not calendar dates**. Each phase names what is built, its cost, its licences, its governance, its leading risks, and — decisively — **what must be true to proceed.**

**Phase 0 — Foundation (fundable now on ₦50m).**
*Build:* register the anchor cooperative; stand up the platform on Fineract/Mifos, multi-tenant at the data layer; write the CRA-2017 furnishing chain and NDPA notices into platform and cooperative terms; register with the NDPC as controller/processor of major importance; implement the CBN OFI cybersecurity controls in anticipation of MFB tenants.
*Cost:* within ₦50m (open-source core is what makes this true).
*Licences:* none yet (software touching no money); NDPC registration.
*Governance:* founder-owned platform; anchor cooperative under the fourteen-clause bye-laws.
*Leading risks:* build overrun; the data-rights chain being treated as a "later" item (fatal — it cannot be retrofitted); scope creep toward a licence before revenue exists.
*Proceed when:* the platform runs the anchor cooperative's full monthly cycle cleanly, **and the data-rights chain is demonstrably present at launch** (not planned, present).

**Phase 1 — Proof of product (the make-or-break gate).**
*Build:* operational multi-tenancy; onboard the **second, independent, paying tenant.**
*Cost:* funded by anchor + second-tenant revenue.
*Licences:* still none required.
*Governance:* published, capped, uniform pricing (the disclosure cure from VI.6); advisory council stood up (acknowledged as near-theatre).
*Leading risks:* the second tenant never signs — meaning the founder has a bespoke build, not a product; conflict-lattice visibility deterring independents.
*Proceed when:* **a second independent paying tenant has signed and is live.** This is the single non-negotiable trigger in the entire plan. Until it fires, *nothing downstream is attempted*, because Part VII is right that **one captive customer validates nothing.**

**Phase 2 — Remittance sub-agency.**
*Build:* CAMA company; partnership with a licensed IMTO; authorised-dealer-bank disbursement integration; naira-payout to members.
*Cost:* modest (partnership + integration, not licence capital).
*Licences:* none of its own; rides the IMTO's licence as sub-agent.
*Governance:* related-party rules so remittance flow is not covertly steered to the anchor over other tenants (governance cure).
*Leading risks:* IMTO partner concentration; CBN settlement-rule changes (the space is actively re-regulated — e.g., the 2024 naira-payout mandate and subsequent settlement-account circulars).
*Proceed when:* remittance runs reliably for members across *more than one* tenant cooperative, proving it is a network service, not an anchor perk.

**Phase 3 — Bureau as feature.**
*Build:* furnishing pipeline to an independent licensed bureau (or CoopCHECK if live) under the CRA-2017 chain; score resale to cooperatives.
*Cost:* near-zero incremental.
*Licences:* none — furnishing/reselling, not operating a bureau.
*Governance:* the founder does **not** operate scoring (avoids the uncurable role conflict); bureau feature serves all tenants uniformly.
*Proceed when:* enough tenants furnish enough data that thin-file members gain measurable scoring benefit.

**Phase 4 (DEFERRED, revisit only on triggers) — a standalone licensed bureau.**
Attempt a ₦500m licensed bureau **only if all six converge:** (1) the platform has many independent paying tenants furnishing rich, standardised data; (2) the CRA-2017/NDPA data-rights chain is unbroken and audited; (3) demonstrated, *paying* lender demand for cooperative-member scores; (4) ₦500m raised **without** ceding platform equity; (5) the anchor-cooperative-vs-bureau role conflict resolved (e.g., the anchor spun out of founder control, or the bureau owned by the network); (6) neither CoopCHECK nor CREDICORP has already commoditised cooperative scoring (VI.10). If any one fails, the bureau stays a feature.

**Phase 5 (DEFERRED / conditional) — member-owned banking.**
Only if the *network* (not the founder) accumulates capital and members: the NPF route — the cooperative network controlling a CBN-licensed MFB (₦200m Tier-1 unit → ₦1bn state → ₦5bn national as scale dictates), owned by the cooperatives, which is the *only* legitimate form of the "apex" idea. The founder does not own this; the network does. If it never triggers, the architecture is complete and coherent without it.

### VI.9 (revised) — Early-warning indicators across five entities

The original degeneration dashboard (Parts III–V) is extended to the multi-entity architecture. Thresholds are stated where the literature or regulation supplies one; where it does not, the metric is flagged as a monitored trend.

**Cooperative member-control metrics (the degeneration front):**
- **Participation:** AGM attendance / voting turnout. Red flag: sustained decline, or turnout so low that quorum is manufactured. (The substitute monitor is the best single predictor of degeneration, and Nigeria has effectively none — so *internal* participation is doing double duty as the monitor.)
- **Contestation:** proportion of board seats actually contested at election. Red flag: uncontested elections two cycles running (capture signature).
- **Board tenure:** years in seat; violation of the bye-law tenure cap. Red flag: any director exceeding the cap, or a chair entrenched beyond it.
- **Insider lending:** insider loans as a share of core capital. **Hard red line drawn from the SASRA discipline: insider lending exceeding 20% of core capital** — the very breach for which SASRA's 2024 supervision report flagged 22 Kenyan SACCOs [CF]. Nigeria lacks an equivalent prudential regulator for cooperatives, so this threshold must be self-imposed in the bye-laws and monitored monthly.

**Platform tenant-concentration and churn metrics:**
- **Tenant concentration:** revenue share from the single largest tenant. Red flag: the anchor (a founder-controlled entity) exceeding ~50% of platform revenue — it means the platform is still, in substance, a captive build. The Phase-1 trigger exists precisely to break this.
- **Independent-tenant count:** number of *independent* paying tenants. Red flag: stuck at one for more than a defined window (VI.10).
- **Churn:** tenants leaving. Because data is tenant-vested and portable, churn is honest signal, not lock-in noise — a rising churn rate is an early warning the product is failing, not that exit is hard.

**Related-party pricing between founder-owned entities:**
- Price paid by the anchor cooperative for platform services vs the published schedule. Red flag: **any** deviation below the uniform published price — the disclosure cure only works if it is enforced. Same test for remittance fees and any data purchased by the bureau feature from the platform.

**Data-rights-chain integrity:**
- Proportion of member records collected under a notice that supports CRA-2017 furnishing. **Threshold: 100%.** Any record furnished to a bureau without a supporting notice is an NDPA breach exposing the founder to fines of up to the greater of 2% of annual gross revenue or ₦10 million for serious contraventions [CF]. This is monitored as a compliance gate, not a trend.

**Conflict-lattice visibility to tenants:**
- Whether independent tenants can *see* the founder's other roles (anchor owner, remittance operator, bureau furnisher) in a published conflicts register. Red flag: independent tenants discovering an undisclosed founder interest — the fastest way to lose the second paying tenant and, with it, the whole proof-of-product.

### VI.10 (revised) — What would falsify this design

A synthesis earns its keep by naming, in advance, the specific checkable developments that would prove it wrong — and what to do in each case.

**1. CoopCHECK launches successfully and onboards cooperatives at scale.** As of 2026, CoopCHECK (powered by CreditRegistry) is an *announced component* of the Ministry's National Cooperative Digital Architecture Platform — announced by the Minister of State for Agriculture on 18 June 2026 in Kaduna in prospective terms ("the Ministry is rolling out…"), with no CBN credit-bureau licence, launch date, pilot or cooperative onboarding reported, and no dedicated capital figure (the widely-cited ₦200bn belongs to the *separate* proposed Cooperative Bank of Nigeria — itself structured 65% cooperative-owned via CoopTrust, 30% institutional, 5% employee — not to CoopCHECK). *Falsification:* if CoopCHECK becomes a licensed, operating bureau onboarding cooperatives nationally. *Response:* this *strengthens*, not weakens, the recommendation to keep the bureau a feature — the founder furnishes CoopCHECK rather than competing with a state-backed, CreditRegistry-powered incumbent. Abandon Phase 4 entirely and integrate.

**2. CREDICORP's national scoring becomes operating fact with mandatory furnishing.** As of 2026, CREDICORP's NIN-anchored universal scoring with compulsory lender reporting traces to a single State House "Meet the Press" briefing (MD Uzoma Nwagba, June 2025), framed around *draft rules* — no enacted regulation, directive or CBN/CREDICORP instrument legally compelling furnishing has been found. The binding baseline remains the pre-existing Credit Reporting Act 2017 plus CBN's bureau guidelines. CREDICORP itself is a real, functioning development-finance institution (established April 2024) running live wholesale-lending programmes — but that is separate from mandatory central-bureau furnishing, which remains announced intention. *Falsification:* if a binding rule actually compels all lenders (including MFBs, fintechs, cooperatives) to furnish a central NIN-anchored bureau. *Response:* the bureau-as-feature becomes near-mandatory plumbing; the founder builds the furnishing pipeline to CREDICORP's rail and drops any standalone-bureau ambition permanently. Either way, the standalone bureau stays dropped.

**3. No independent tenant pays within a defined window.** *Falsification of the core premise that this is a product:* if, within (say) 18–24 months of the platform running the anchor cleanly, **no second independent paying tenant has signed.** *Response:* stop treating it as a product company. Either the platform is a bespoke internal tool for the founder's own cooperative (a legitimate but far smaller business), or the design is wrong and must be re-scoped. Do not proceed to remittance, bureau, or any licence. This is the hardest-edged falsifier in the study and the reason it is the Phase-1 gate.

**4. External capital proves unavailable on non-dilutive terms.** *Falsification of the funding path:* if neither DFI debt, CREDICORP wholesale lines, nor grant capital can be raised, and the only money available is external *equity*. *Response:* do **not** take platform equity (it destroys the permanent-founder-ownership rationale and reintroduces external capture at the ownership level). Instead, stay at the three-entity, feature-not-firm scale indefinitely — a smaller but coherent business — rather than fund a bigger one by surrendering the rail. If equity must be taken, ring-fence it inside a licensed operating subsidiary, never the platform holding company.

**5. The asset-lock / degeneration failsafe fires.** Recall from Parts I–V that Nigeria has *no statutory asset lock*, and a bye-law lock is weaker than a statutory one because members can amend bye-laws. *Falsification:* if the anchor cooperative amends away its bye-law lock or its insider-lending cap. *Response:* treat as a live degeneration event (VI.9), because g\* = b × ROE already caps organic growth (₦200m at 20% ROE takes ~18 years to reach ₦5bn), so a cooperative that also strips its own governance protections is degenerating faster than it can grow — intervene or exit.

### VI.11 — Ten propositions on building an institutional architecture single-handed

1. **Ownership is the design, not a detail of it.** For an entity whose value comes from mutualisation, changing the owner from "the network" to "one person" can delete the entity's entire reason to exist while leaving its cost and its licence fully intact. The apex is the proof.

2. **A feature is cheaper than a firm and often does the same job.** The credit bureau delivers most of its cooperative benefit as a furnishing-and-scoring feature of the platform at near-zero incremental capital; as a standalone company it costs ₦500m and inherits an unwinnable fight with fifteen-year incumbents. Ask of every proposed entity: could this be a feature of one you are already building?

3. **The second independent paying customer is the birth certificate of a product.** One captive customer validates nothing; it proves only that you can build for yourself. Until an unrelated party pays, you have a project, not a business — so make that signature the gate everything else waits behind.

4. **You cannot retrofit a lawful basis.** Data collected under a narrow notice cannot later be repurposed for a new controller and a new purpose. The right to use data downstream must be written into the terms upstream, at launch, or it is lost — and no amount of later consent-chasing recovers it cleanly.

5. **Some conflicts are cured by walls, some by disclosure, some by governance — and some only by giving up an entity.** The test is the *level* of the conflict: data-handling conflicts wall off, hidden-preference conflicts disclose away, single-entity conflicts govern away, but a conflict of *role* between two entities one person owns has no cure except not owning both.

6. **Capital is a wall, not a slope.** Licence thresholds are discontinuous: ₦50m does not get you 1% of the way to a ₦5bn PSB; it gets you nothing at that gate. Sequencing lets revenue climb the wall one course at a time; parallelising spreads the mortar so thin that no course sets.

7. **Buy the plumbing you cannot afford to build.** Correspondent banking instead of an apex; IMTO sub-agency instead of an IMTO licence; open-source core instead of a ground-up build; an incumbent bureau instead of your own. The founder's scarce capital should buy the things only he can build — the member relationship and the cooperative-specific configuration — and rent everything else.

8. **External equity is the lever that solves the arithmetic and breaks the strategy.** If the entire point of permanent founder ownership is to avoid outside control, then funding the plan by selling ownership defeats the plan. Prefer debt; if equity is unavoidable, quarantine it in the licensed subsidiary and never let it touch the rail.

9. **Being the indispensable supplier is a form of capture even when it is the only buildable model.** The vendor model is legitimate and global, but it makes the founder the permanent external-capture vector by construction. Legitimacy comes not from pretending the chokepoint away but from fencing it — escrow, portable data, capped terms, continuity cover — so tenants can always leave.

10. **A plan you can execute beats a plan you can admire.** Five institutions in three years on ₦50m is admirable and impossible; three entities and a feature, gated on real triggers, is modest and buildable. The honest synthesis is not the one that flatters the ambition or the one that only attacks it — it is the one that tells the founder exactly which two of his five ideas to drop, and then hands him a sequence that actually funds the other three.

---

## Recommendations

**Immediately (Phase 0, within current ₦50m):**
1. Register the anchor cooperative under state Cooperative Law; keep it strictly members-only (BOFIA §2(2) is criminal).
2. Assemble the platform on **Apache Fineract / Mifos**, multi-tenant at the data layer from day one; do not build ground-up.
3. **Write the CRA-2017 furnishing chain and NDPA collection notices into platform and cooperative terms now** — this is the one thing that cannot be retrofitted.
4. Register with the NDPC as a controller/processor of major importance; implement CBN OFI cybersecurity controls ahead of MFB tenants.

**Next (Phase 1 — the gate):** Sign a **second, independent, paying tenant** before attempting anything downstream. Publish capped, uniform pricing and a conflicts register. *Benchmark that changes everything:* if no independent tenant pays within 18–24 months of a clean anchor deployment, stop and re-scope — you have a bespoke tool, not a product.

**Then (Phases 2–3):** Stand up remittance as **naira-payout sub-agent of a licensed IMTO** (never an own licence). Add the **bureau as a feature** furnishing an *independent* licensed bureau — do not operate scoring yourself.

**Drop now:** the **founder-owned apex** (no rationale, ₦5–50bn, uncurable conflicts). Meet its functions with correspondent/agency relationships.

**Defer behind hard triggers:** the standalone ₦500m bureau (six triggers) and any MFB above Tier-2 or PSB. Revisit member-owned banking (the NPF route) only if the *network* accumulates the capital and members.

**Funding rule:** prefer external *debt* (DFI, CREDICORP wholesale lines); avoid external *equity*; if equity is unavoidable, ring-fence it in a licensed subsidiary, never the platform holding company.

**Thresholds that would change the plan:** CoopCHECK going live → integrate, do not compete. CREDICORP mandatory furnishing becoming binding law → build the pipeline to it, drop the standalone bureau forever. Insider lending in the anchor breaching 20% of core capital, or its bye-law asset lock being amended away → treat as an active degeneration event and intervene or exit.

---

## Caveats

- **Capital figures are current statutory/regulatory minimums**, not the working capital a real institution needs; the true funding requirement at every licensed step is materially higher once escrows (which the CBN demands *on top of* paid-up capital), professional fees and operating runway are added. Where I have estimated (platform build costs), I have tagged the figure [AI] and shown the reasoning; Nigerian software-cost benchmarks vary widely with team seniority and currency exposure.
- **CoopCHECK and CREDICORP mandatory-furnishing status is announced-intention, not operating fact, as of 2026.** This is well-sourced but the coverage is heavily press-release-driven and repeats official quotes across outlets; no primary regulatory or gazette instrument confirming operational/binding status was located. If either becomes operational fact, the falsification responses in VI.10 apply.
- **The NPF ownership figure** is reported at ~62.6% for the Nigeria Police Co-operative Society alone in NGX filings, with the Welfare Insurance Scheme holding a further ~15.6% (jointly ~76–78%); sources vary on whether "~62.6%" or "~75–76%" is quoted depending on whether the Welfare Scheme is included. The precedent — that a cooperative can lawfully control a CBN-licensed bank — holds on either figure.
- **This Part is synthesis.** The evidential bases for the transplant methodology (VI.1), the ten-mechanism transplant audit (VI.2), Nigeria's comparative advantages (VI.3) and the fourteen-clause bye-law specification (VI.6, preserved) live in the earlier Parts and are relied on here by reference, not re-proven.
- **Vendor, federation and government-programme material** (Fineract/Mifos performance claims, Atruvia scale figures, RH-CRRP announcements) is treated as promotional and flagged as such; the "16-week go-live" and similar figures are vendor claims, not independent benchmarks.
- **Evidence tags used:** [CF] confirmed fact (statute, regulation, regulator data, audited/filed accounts); [SC] scholarly consensus; [CL] contested in the literature; [AI] analytical inference with reasoning shown; [H] hypothesis; [U] unknown. Terminology follows the study's fixed conventions, including the distinction between **demutualisation** (event) and **degeneration** (process), Cook's five property-rights problems, the four failure modes and Part III's seven capture types (external and political included).