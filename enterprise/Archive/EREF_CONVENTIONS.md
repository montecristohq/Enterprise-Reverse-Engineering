# EREF CONVENTIONS — Enterprise Reverse-Engineering Framework

*Subject-agnostic. Instantiate per study by completing §0, then carry this document verbatim into every volume brief so that continuity does not depend on conversation memory.*

**Distilled from seven completed studies:** Wise plc · Atruvia AG · the DZ BANK Group · Experian plc · Robinhood Markets, Inc. · Klarna · Block, Inc.

---

## How to use this document

EREF disassembles an **enterprise** — its legal form, its customers, its machinery, its economics, its strategy — until the reader could reconstruct why it makes money and whether it will continue to.

TREF, its sibling, disassembles a **technology**. The two share a spine and diverge where the object differs, and the divergence matters: **TREF's best sources are specifications and source code, which cannot easily misrepresent themselves. EREF's sources are filings and disclosures, which a company chooses to publish and frames to its advantage.** Almost every convention below exists to manage that asymmetry.

This document is the constitution. Each volume brief instantiates it. Nothing here is advisory.

---

## §0 — SUBJECT HEADER (complete before Volume I; reproduce at the head of every brief)

```text
Subject:                 [LEGAL NAME AND TICKER]
Sector:                  [BANK / PAYMENTS / DATA / BROKER / PLATFORM / COOPERATIVE / OTHER]
Reporting basis:         [US GAAP / IFRS-IASB / IFRS-EU / LOCAL — AND WHICH ENTITY REPORTS ON IT]
Reporting currency:      [CURRENCY, AND ANY SECOND CURRENCY IN PLAY]
Financial year end:      [DATE]
Filing regime:           [10-K DOMESTIC / 20-F FPI / LOCAL STATUTORY / PRIVATE — DISCLOSURE DEPTH]
Reporting entities:      [LIST ALL THAT PUBLISH SEPARATE FIGURES]
Governing metric:        [SEE CONVENTION 3 — THE "FOLLOW THE X" RULE]
Restatement history:     [ANY SEGMENT OR BASIS CHANGES IN THE PERIOD STUDIED]
Research cut-off:        [DATE]
Study objective:         [NEUTRAL TEARDOWN / PLAYBOOK EXTRACTION — SEE CONVENTION 10]
Volume count:            [FIVE CANONICAL, OR EXPANDED — SEE THE VOLUME TABLE]
```

**Two fields do the most work.** `Reporting entities` — because a group that publishes three sets of figures in two currencies under two frameworks will produce nonsense if they are conflated, and Klarna did exactly that. And `Governing metric`, which is the framework's signature instrument and is explained at Convention 3.

---

## Convention 1 — Evidence classification (MANDATORY, all volumes)

| Label | Meaning |
|---|---|
| **CONFIRMED FACT** | Directly supported by primary evidence — a filing, a regulatory order, a court opinion, a statute, a dated event |
| **COMPANY CLAIM** | Stated by the subject but not independently verified |
| **THIRD-PARTY ESTIMATE** | Externally reported or estimated; not from filings |
| **ANALYTICAL INFERENCE** | Reasoned from multiple known facts, with the reasoning shown |
| **HYPOTHESIS** | Plausible, requiring further evidence |
| **UNKNOWN** | The evidence is insufficient — flagged, never papered over |

**COMPANY CLAIM is the default for every operational, cultural, productivity and strategic assertion the subject makes about itself.** This is the framework's most important single rule, and it is not scepticism for its own sake — it is a response to what seven studies actually found.

An inference is never silently promoted to a fact.

**Where the subject is a theory-and-institutions study rather than a company teardown**, substitute SCHOLARLY CONSENSUS and CONTESTED IN THE LITERATURE for COMPANY CLAIM and THIRD-PARTY ESTIMATE. The ladder must fit the evidence available, and academic disagreement is a different object from corporate assertion.

---

## Convention 2 — Basis discipline

**State the entity, currency and framework on every material figure.** Never mix bases in a single comparison.

Three failure modes, all observed:

**Multiple reporting entities.** One subject published consolidated group figures in one currency under one framework, statutory accounts for its licensed subsidiary in another currency under another, and prudential figures on a third basis entirely — with capital ratios existing *only* on the third. A study that quotes a capital ratio beside a group revenue figure without noting the basis has produced a sentence that cannot be true.

**Restatement.** One subject restated its segment reporting twice in three years. A naive multi-year comparison across that boundary is wrong, and wrong in a way that looks consistent. **Log every restatement in §0 and flag it wherever the series crosses it.**

**Non-GAAP measures.** Label them, reconcile them where disclosure permits, and never mix them with statutory figures. Assess each adjustment on its merits — particularly share-based compensation, which is a real economic cost borne by shareholders through dilution. **A measure that adds it back is not a measure of economic performance.** Where a subject promotes a self-selected composite metric, scrutinise it rather than repeating it.

---

## Convention 3 — The governing metric: "Follow the X"

**Every EREF study identifies the one thing which, traced consistently through every volume, explains the enterprise.** This is the framework's signature instrument and the thing that turns five volumes into one argument.

From the completed studies:

| Subject | Governing rule | What it prevented |
|---|---|---|
| Experian | **Follow-the-Data-Right** | Mistaking the consumer for the customer |
| Robinhood | **Follow-the-Order** | Mistaking the user for the payer |
| Klarna | **Follow-the-Credit-Risk** | Mistaking the lender of record |
| Block | **Follow-the-Gross-Profit** | Misstating the business by a factor of three |

The Block case is the clearest demonstration. Bitcoin sold to customers was booked as revenue at the full sale amount at roughly a 3% margin, making it about 42% of reported revenue and a rounding error in gross profit. **Any volume anchored on revenue would have been internally consistent and wrong.** Fourteen independently-executed volumes avoided it because the rule was in every brief.

**Choosing the rule is the most consequential decision in the study, and it is made before Volume I.** The test: *which single quantity, if traced wrongly, would make every subsequent volume wrong in the same direction?* Trace that.

---

## Convention 4 — Follow-the-Legal-Entity

Attribute every activity, licence, obligation and enforcement action to **the specific entity that performs or holds it**. Never attribute subsidiary conduct to a parent without saying so.

**Name the parties that are not in the group.** Sponsoring banks, processors, card networks, partner lenders, outsourced providers. One subject's US lender of record was a bank it did not own; another's merchant relationships ran through processors acting as merchant of record. In both cases the entity that appeared to own the customer did not.

Where a group contains a **licensed entity beside an unlicensed one**, establish the ring-fence explicitly: the capital undertakings, the affiliate-transaction limits, the governance separation, the dividend position. **Map the group by regulatory perimeter, not by ownership tree** — the ownership chart is public and uninformative; the perimeter is what constrains the business.

---

## Convention 5 — The organising question

**Where a service is free to the user, establish who actually pays.** Run this question through the whole study rather than answering it once.

The completed studies produced four structurally different answers, and the differences are the point: the consumer as **raw material** (data furnished about them); the customer's **order** as the product, bought by a wholesale counterparty; the consumer as **bait** with the merchant paying for conversion; and a **free wedge subsidised by a downstream monetisation ladder** on both sides of a group.

Where a subject charges everyone openly, the question still applies in its second form: **which customer subsidises which, and what happens if the subsidy is withdrawn?**

---

## Convention 6 — Every volume owns a question

**Each volume answers a question no other volume can.** State it at the head of the brief. If a section cannot be justified against its volume's owned question, it belongs elsewhere or nowhere.

At five volumes this is hygiene; at fourteen it is the only thing preventing restatement.

**Re-cuts.** Where the evidence warrants a sharpened or contrarian angle, state the re-cut explicitly at the head of the brief with its reasoning. Re-cuts are how a study stops being a template and becomes an argument. Two that produced the programme's best findings: treating **management credibility as an analytical object** rather than a character question, and requiring a moat scorecard to be **honestly asymmetric** rather than uniformly sceptical.

---

## Convention 7 — Management credibility as an analytical object

Where a subject's public claims are found to require correction, **that pattern is itself an analytical finding** and belongs in the study rather than in a footnote.

The method: catalogue the instances; establish what was claimed, what was independently found, and whether the subject later qualified it; then **reach a settled position on which categories of statement are reliable and which are not.**

Two studies reached the same structural verdict from different evidence: **the audited financial disclosure is reliable; the operational and strategic narrative is not.** That is a priceable, useful conclusion — and it is different in kind from misrepresentation of audited figures, which is a far graver finding. **Distinguish promotional exuberance, which is common and can be priced, from anything worse.** Do not conflate them, in either direction.

---

## Convention 8 — Discriminating scepticism

**Do not apply uniform scepticism where the evidence is not uniform.**

A moat scorecard, a competitive assessment or a management appraisal that scores everything low is as uninformative as one that scores everything high. Where the evidence supports a genuine advantage, score it accordingly; where a claimed advantage does not survive testing, say so plainly. The Block study scored two moats at five out of five and the company's own central strategic claim at one — and the asymmetry is what made the scorecard worth reading.

The corollary: **an absence of disclosure is evidence.** A company that has asserted something for years and has never published the one metric that would demonstrate it is telling the analyst something. Record the absence as a finding rather than noting that data were unavailable.

---

## Convention 9 — Natural experiments and the abandonment record

**Look for where the subject ran the experiment itself.** A company that operated two comparable businesses and saw only one succeed, or entered eight markets and withdrew from three, has generated better evidence than any external comparison. These cases are the most valuable material in a study and are rarely presented as such by the company.

**Study the failures.** What an enterprise tried and stopped teaches what the success record cannot, because companies volunteer their successes and bury their retreats. Catalogue abandonments **by cause** — bought and sold well, bought and written off, built and failed, conviction bets not returned, and **strategic retreats nobody announced** — rather than chronologically. The last category is the hardest to find and the most revealing.

---

## Convention 10 — The playbook objective (studies with an extraction purpose)

EREF may be run **neutrally** — to understand an enterprise — or as a **playbook extraction**, where the reader intends to build something informed by the subject. Declare which in §0.

Where the objective is extraction, every volume additionally carries a verdict on each material mechanism:

| Verdict | Meaning |
|---|---|
| **ADOPT** | Works on its own logic; survives the move |
| **ADAPT** | The logic transfers but the implementation must change — state precisely what must change, and to what |
| **REJECT** | Depends on institutions, infrastructure, regulation or scale the target lacks — name the dependency that kills it |

Apply the **environment question** before each verdict: *did this work because of the mechanism itself, or because of the institutional environment surrounding it?* Strip the environment out — the payment rails, the credit infrastructure, the deposit insurance, the capital markets, the regulatory perimeter — then judge.

**Two rules that make the difference between a useful verdict and a useless one.**

Do not let verdicts collapse into "that market is different." That is true and worthless. **Name the specific institutional feature doing the silent work**, so the reader can ask what plays that role in their own market.

**A REJECT is as valuable as an ADOPT**, and frequently more so. And a REJECT should carry its constructive half: having established what the reader cannot do, establish what they should do instead.

Verdicts are stated **in the volume where the mechanism is analysed.** The synthesis volume consolidates them; it does not generate them.

---

## Convention 11 — Depth follows the subject

Depth follows importance, never a page count. **No hidden compression:** if there are eleven material competitors, analyse the eleven; if the enforcement record has six entries, list the six; if the risk register has eighteen items, populate the eighteen.

Never compress later material because earlier material ran long.

> **Completeness before concision.** There is no reward for brevity and a substantial penalty for superficiality.

---

## Convention 12 — Cross-references written forward

Volumes may be researched out of order. **They are always assembled in canonical order.**

A brief written early must not reference a later volume by number as though it exists. Reference forward **by topic** — "the credit mechanism, developed in a later volume" — and verify at assembly.

**Carry findings forward explicitly.** Every brief after the first restates the material findings of its predecessors, because the executing agent has not seen them. This is the single practical measure that made a fourteen-volume run cohere.

---

## Convention 13 — Staging, assembly and reconciliation

**File naming.** Stage files are named by **volume number, not writing order**, zero-padded: `stages/v01.md` onward. Padding matters the moment a study exceeds nine volumes.

**Gap check.** The assembler verifies every slot is present and aborts if one is missing.

**The reconciliation register.** Log conflicts as they surface, not at the end. Classify each as:

- **Genuine error** — one volume is wrong. Establish which governs and **correct it at source with a visible inline note**, not only in an appendix. A reader meets the error in the body; the correction belongs there.
- **Dual-value figure** — both values are defensible (an announced price against a settled one; a headline figure against a filing figure). State one canonical value and explain the other.
- **Vintage difference** — not a conflict. Present as a dated series so a reader does not mistake movement for disagreement.

**Every study ships a reconciliation appendix** recording all three categories plus the unknowns carried forward. On a long run this is not housekeeping; it is the document's warrant.

---

## Convention 14 — The completion standard

The research is complete only when a sophisticated reader can explain: what the enterprise is legally; who its customer actually is and who pays; how its machinery works; what it earns per unit and why; what funds it; who decides; what its advantages genuinely are; what would break it; and what it would take to build one.

> **"I can explain why this business makes money, and say what would have to change for it to stop."**

Where the objective is playbook extraction, a second standard applies:

> **"I know which mechanisms I would carry across, which I would change, and which I would refuse — and which institution in my own market has to play the role that one plays in theirs."**

---

## The canonical five volumes

| | Volume | The question it owns |
|---|---|---|
| **I** | Corporate, Legal, Regulatory & Institutional Anatomy | What is this entity legally, and what permissions does it hold? |
| **II** | Product, Customer Structure & Value-Flow Architecture | Who is the customer, and who actually pays? |
| **III** | Operations, Technology, Data & Organisational Design | What machinery makes it work? |
| **IV** | Financial Statements, Revenue Architecture, Unit Economics & Capital | What does it earn per unit, and what funds it? |
| **V** | Management, Culture, Incentives, Competition, Moat, Risk & Strategy | Why does it win, and is that durable? |
| **VI** | Cross-Volume Synthesis | The enterprise as one system |

**Six of the seven completed studies used exactly this structure.** It is the default and should be departed from only for cause.

### When to expand beyond five

Expand where the subject contains **genuinely separate businesses that the canonical structure would flatten.** One subject ran two ecosystems with different customers, different economics and, for most of its history, different leadership; compressing them into a single product volume would have destroyed the comparison the study existed to make. That study ran to fourteen volumes, with the two ecosystems separated, the regulatory estate and the money-movement layer given their own volumes, and two volumes devoted to natural experiments — international expansion and the abandonment record.

**The test for an additional volume: does it own a question no canonical volume can answer?** If not, it is a section. Beyond roughly fourteen the risk shifts from omission to repetition, and Convention 6 becomes the binding constraint.

---

## Stage plan (adapt per subject; state in the front matter)

Commission in stages with a decision point at the end of each, so a study can be stopped if the early volumes show the subject does not repay the effort.

For a **canonical five-volume run**: I–II, then III–IV, then V–VI with assembly.

For an **expanded run with an extraction objective**, lead with the volumes carrying the transferable mechanisms rather than the corporate history. The Block study ran the regulatory ladder, the credit mechanism and the payment rails as Stage 1 precisely so that a negative finding would arrive in a week rather than a month. **Stage 1 is a genuine decision point, and saying so before it starts is what makes it one.**

---

## Deliverables

A completed EREF study ships:

1. **`[SUBJECT]_Enterprise_Study_COMPLETE.md`** — all volumes plus master layer, assembled in canonical order
2. **A master layer** — front matter, these conventions instantiated, contents, and the appendices: glossary, canonical figures register, source register, reconciliation. Where the subject has multiple reporting entities, a **basis-discipline appendix** explaining how to read its numbers
3. **`BUILD_SPEC.md`** — the rendering specification, prepended for handoff
4. **`assemble.py`** — the assembler, with gap check and anchored contents generation
5. **Where the objective is extraction** — a consolidated verdict table and a sequenced build order

---

## A closing note on what this framework is for

EREF asks a question companies do not answer about themselves: **not what they do, but why the money arrives, and what would have to be true for it to stop.**

Almost every convention here exists because the subject controls the disclosure. The evidence ladder exists because companies assert things about themselves. The basis discipline exists because they change how they report. The governing metric exists because they choose which number to lead with. The credibility convention exists because seven studies found that operational narrative and audited figures have different reliability. And the discriminating-scepticism rule exists because the opposite failure — treating everything a company says as false — produces a study just as useless as credulity.

A study that reaches the completion standard is worth more than any forecast of the subject, because the forecast will be wrong and the explanation will still hold.
