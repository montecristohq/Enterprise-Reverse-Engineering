# EREF CONVENTIONS — Enterprise Reverse-Engineering Framework

*Subject-agnostic. Instantiate per study by completing §0, then carry this document verbatim into every volume brief so that continuity does not depend on conversation memory.*

**Sources:** the EREF specification (Volumes I–VII plus Reconstruction), and the operational discipline distilled from seven completed studies — Wise plc · Atruvia AG · the DZ BANK Group · Experian plc · Robinhood Markets, Inc. · Klarna · Block, Inc.

---

## How to use this document

The **volume prompts** say what to research. **This document says how**, and how the volumes cohere into one study. Both go into every brief; neither substitutes for the other.

EREF disassembles an **enterprise**. TREF, its sibling, disassembles a **technology**. The bridge runs one way and is formal: **a critical system identified in the technology volume is handed to TREF for separate teardown** (Convention 15).

One asymmetry between the frameworks governs almost everything below. **TREF's best sources are specifications and source code, which cannot easily misrepresent themselves. EREF's sources are filings and disclosures, which a company chooses to publish and frames to its advantage.**

This document is the constitution. Nothing here is advisory.

---

## §0 — SUBJECT HEADER (complete before Volume I; reproduce at the head of every brief)

```text
Company:                 [LEGAL NAME AND TICKER]
Industry / industries:   [OR LEAVE FOR THE AGENT TO DETERMINE]
Primary geographies:     [OR LEAVE FOR THE AGENT TO DETERMINE]
Reporting basis:         [US GAAP / IFRS-IASB / IFRS-EU / LOCAL — AND WHICH ENTITY REPORTS ON IT]
Reporting currency:      [CURRENCY, AND ANY SECOND CURRENCY IN PLAY]
Financial year end:      [DATE]
Filing regime:           [10-K DOMESTIC / 20-F FPI / LOCAL STATUTORY / PRIVATE — DISCLOSURE DEPTH]
Reporting entities:      [LIST ALL THAT PUBLISH SEPARATE FIGURES]
Governing metric:        [SEE CONVENTION 3]
Restatement history:     [ANY SEGMENT OR BASIS CHANGES IN THE PERIOD STUDIED]
Research date:           [DATE]
Study objective:         [NEUTRAL TEARDOWN / PLAYBOOK EXTRACTION — SEE CONVENTION 13]
Configuration:           [COMPACT 5 / STANDARD 7 / EXTENDED 8–10 — SEE THE VOLUME ARCHITECTURE]
Special focus:           [OPTIONAL]
```

**Two fields do the most work.** `Reporting entities`, because a group publishing three sets of figures in two currencies under two frameworks produces nonsense if they are conflated — one subject did exactly that. And `Governing metric`, the framework's signature instrument, explained at Convention 3.

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

**Never present inference as fact.** An inference is never silently promoted.

**COMPANY CLAIM is the default for every operational, cultural, productivity and strategic assertion the subject makes about itself.** Not scepticism for its own sake — a response to what seven studies found (Convention 9).

**Where the subject is a theory-and-institutions study** rather than a company teardown, substitute SCHOLARLY CONSENSUS and CONTESTED IN THE LITERATURE for COMPANY CLAIM and THIRD-PARTY ESTIMATE. The ladder must fit the evidence available; academic disagreement is a different object from corporate assertion.

---

## Convention 2 — Basis discipline

**State the entity, currency and framework on every material figure. Never mix bases in a single comparison.**

Three failure modes, all observed:

**Multiple reporting entities.** One subject published consolidated group figures in one currency under one framework, statutory accounts for its licensed subsidiary in another currency under another, and prudential figures on a third basis — with capital ratios existing *only* on the third. A study quoting a capital ratio beside a group revenue figure without noting the basis has written a sentence that cannot be true.

**Restatement.** One subject restated its segment reporting twice in three years. A naive multi-year comparison across that boundary is wrong, and wrong in a way that looks internally consistent. **Log every restatement in §0 and flag it wherever a series crosses it.**

**Non-GAAP measures.** Label them, reconcile them where disclosure permits, never mix them with statutory figures. Assess each adjustment on its merits — particularly share-based compensation, a real economic cost borne by shareholders through dilution. **A measure that adds it back is not a measure of economic performance.** Where a subject promotes a self-selected composite metric, scrutinise it rather than repeat it.

---

## Convention 3 — The governing metric: "Follow the X"

**Every study identifies the one quantity which, traced consistently through every volume, explains the enterprise.** This is what turns a set of volumes into a single argument.

| Subject | Governing rule | What it prevented |
|---|---|---|
| Experian | **Follow-the-Data-Right** | Mistaking the consumer for the customer |
| Robinhood | **Follow-the-Order** | Mistaking the user for the payer |
| Klarna | **Follow-the-Credit-Risk** | Mistaking the lender of record |
| Block | **Follow-the-Gross-Profit** | Misstating the business by a factor of three |

The Block case is the clearest demonstration. Bitcoin sold to customers was booked as revenue at the full sale amount at roughly a 3% margin — about 42% of reported revenue, a rounding error in gross profit. **Any volume anchored on revenue would have been internally consistent and wrong.** Fourteen independently-executed volumes avoided it because the rule was in every brief.

**Choose the rule before Volume I.** The test: *which single quantity, traced wrongly, would make every subsequent volume wrong in the same direction?* Trace that one everywhere.

---

## Convention 4 — The universal questions and the five lenses

For every material component ask: **What? How? Who? Where? When? Why?**

Then analyse: **Structure · Flow · Control · Economics · Risk.**

**Why is the question that separates a reverse-engineering study from a company profile.** Answer it from filings, transcripts, litigation and contemporaneous reporting where they exist; mark it HYPOTHESIS where they do not.

---

## Convention 5 — The six mandatory traces

Every study performs all six.

**Follow the money.** Whose money it is; which entity controls it; where it resides; when ownership or economic entitlement changes; when revenue is recognised; what costs are deducted; who bears the risk.

**Follow the physical flow.** Materials, inventory, production, warehousing, logistics, delivery, returns and service, where relevant.

**Follow the data.** Generation, storage, processing, access, analytics, governance, privacy and decision use.

**Follow the legal entity.** Which entity owns assets, signs contracts, employs people, holds licences, earns revenue, bears liabilities, owns IP, pays taxes. **Name the parties that are not in the group** — sponsoring banks, processors, networks, partner lenders, outsourced providers. In two studies the entity that appeared to own the customer did not.

**Follow the authority.** Who can make, approve, block, override or terminate important decisions.

**Follow the revenue.** Customer need → commercial event → pricing → gross transaction or billing → direct costs → recognised revenue → contribution → operating expenses → profit → cash.

**Where a group contains a licensed entity beside an unlicensed one**, map the group by **regulatory perimeter, not ownership tree.** The ownership chart is public and uninformative; the perimeter is what constrains the business. Establish the capital undertakings, affiliate-transaction limits, governance separation and dividend position explicitly.

---

## Convention 6 — Industry adaptation, and the anti-speculation rule

**Adapt the framework to the company.** Do not force fintech, software, manufacturing, banking or other sector concepts where they do not apply. A volume with nothing to say about supply chain should say so briefly rather than manufacture content.

**If evidence is unavailable:** state what is known, label the inference, preserve the uncertainty, and identify what evidence would resolve it. **UNKNOWN is a valid and frequently correct answer.** A study that reaches it forty times has done its job; one that reaches it never has not.

---

## Convention 7 — The organising question

**Where a service is free to the user, establish who actually pays.** Run this through the whole study rather than answering it once.

The completed studies produced four structurally different answers: the consumer as **raw material** (data furnished about them); the customer's **order** as the product, bought by a wholesale counterparty; the consumer as **bait**, with the merchant paying for conversion; and a **free wedge subsidised by a downstream monetisation ladder** on both sides of a group.

Where the subject charges everyone openly, the question applies in its second form: **which customer subsidises which, and what happens if the subsidy is withdrawn?**

**In Standard and Extended configurations this question spans Volumes II and III.** Carry it explicitly across the boundary. It is the sharpest instrument the framework has and the one most easily lost to a volume split.

---

## Convention 8 — Every volume owns a question

**Each volume answers a question no other volume can.** State it at the head of the brief. If a section cannot be justified against its volume's owned question, it belongs elsewhere or nowhere.

At five volumes this is hygiene; at fourteen it is the only thing preventing restatement.

**Re-cuts.** Where the evidence warrants a sharpened or contrarian angle, state the re-cut explicitly at the head of the brief with its reasoning. Re-cuts are how a study stops being a template and becomes an argument. Two that produced the programme's best findings: treating **management credibility as an analytical object** rather than a character question, and requiring a **moat scorecard to be honestly asymmetric** rather than uniformly sceptical.

---

## Convention 9 — Management credibility as an analytical object

Where a subject's public claims are found to require correction, **that pattern is itself an analytical finding** and belongs in the study.

The method: catalogue the instances; establish what was claimed, what was independently found, and whether the subject later qualified it; then **reach a settled position on which categories of statement are reliable and which are not.**

Two studies reached the same structural verdict from different evidence: **the audited financial disclosure is reliable; the operational and strategic narrative is not.** That is priceable and useful — and different in kind from misrepresentation of audited figures, which is far graver. **Distinguish promotional exuberance, which is common and can be priced, from anything worse — in both directions.**

---

## Convention 10 — Discriminating scepticism

**Do not apply uniform scepticism where the evidence is not uniform.**

A moat scorecard that scores everything low is as uninformative as one that scores everything high. Where the evidence supports a genuine advantage, score it accordingly; where a claimed advantage does not survive testing, say so plainly. One study scored two moats at five out of five and the company's own central strategic claim at one — and the asymmetry is what made the scorecard worth reading.

**The corollary: an absence of disclosure is evidence.** A company that has asserted something for years and never published the one metric that would demonstrate it is telling the analyst something. **Record the absence as a finding**, not as a data limitation.

---

## Convention 11 — Natural experiments and the abandonment record

**Look for where the subject ran the experiment itself.** A company that operated two comparable businesses and saw only one succeed, or entered eight markets and withdrew from three, has generated better evidence than any external comparison. These cases are the most valuable material in a study and are never presented as such by the company.

**Study the failures.** What an enterprise tried and stopped teaches what the success record cannot, because companies volunteer successes and bury retreats. Catalogue abandonments **by cause** — bought and sold well, bought and written off, built and failed, conviction bets not returned, and **strategic retreats nobody announced** — rather than chronologically. The last category is hardest to find and most revealing.

---

## Convention 12 — Depth follows the subject

Depth follows complexity and importance, never a page or token budget. If a subject requires three pages, write three; if fifty, write fifty.

**No hidden compression.** If there are eleven material competitors, analyse the eleven; if the enforcement record has six entries, list the six; if the risk register has eighteen items, populate the eighteen. Never compress later sections because earlier sections ran long.

Where output limits intervene, stop at a logical boundary and continue without compressing.

> **Completeness before concision.** No reward for brevity; a substantial penalty for superficiality.

---

## Convention 13 — The extraction objective (studies with a build purpose)

EREF may be run **neutrally**, or as a **playbook extraction** where the reader intends to build something informed by the subject. Declare which in §0.

Where the objective is extraction, every volume additionally carries a verdict on each material mechanism:

| Verdict | Meaning |
|---|---|
| **ADOPT** | Works on its own logic; survives the move |
| **ADAPT** | The logic transfers but the implementation must change — state precisely what must change, and to what |
| **REJECT** | Depends on institutions, infrastructure, regulation or scale the target lacks — name the dependency that kills it |

Apply the **environment question** before each verdict: *did this work because of the mechanism itself, or because of the institutional environment surrounding it?* Strip out the payment rails, credit infrastructure, deposit insurance, capital markets and regulatory perimeter — then judge.

**Two rules separate a useful verdict from a useless one.** Do not let verdicts collapse into "that market is different" — true and worthless. **Name the specific institutional feature doing the silent work**, so the reader can ask what plays that role in their own market. And **a REJECT is as valuable as an ADOPT** — frequently more so — but must carry its constructive half: having established what cannot be done, establish what should be done instead.

Verdicts are stated **in the volume where the mechanism is analysed.** Reconstruction consolidates them; it does not generate them.

---

## Convention 14 — Cross-references written forward; findings carried back

Volumes may be researched out of order. **They are always assembled in canonical order.**

A brief written early must not reference a later volume by number as though it exists. Reference forward **by topic** — "the credit mechanism, developed in a later volume" — and verify at assembly.

**Every brief after the first restates the material findings of its predecessors**, because the executing agent has not seen them. This is the single practical measure that made a fourteen-volume run cohere.

---

## Convention 15 — The TREF handoff

**EREF terminates at the point where it has identified which system deserves a technology teardown.**

The technology volume closes with a ranked **TREF candidate list**, scored on business criticality, uniqueness, technical complexity, moat relevance and replacement difficulty. That list is a deliverable, not a gesture: it is the formal bridge between the two frameworks.

**In Compact configuration, back-port this section** into the merged operations-and-technology volume so the handoff survives a short run.

---

## Convention 16 — Staging, assembly and reconciliation

**File naming.** Stage files are named by **volume number, not writing order**, zero-padded: `stages/v01.md` onward. Padding matters the moment a study exceeds nine volumes. **The reconstruction stage takes `00`** — it operates on the volumes rather than being one of them.

**Gap check.** The assembler verifies every slot is present and aborts if one is missing. A document with a silent hole is worse than a build failure.

**The reconciliation register.** Log conflicts as they surface, not at the end. Classify each as:

- **Genuine error** — one volume is wrong. Establish which governs and **correct it at source with a visible inline note**, not only in an appendix. A reader meets the error in the body; the correction belongs there.
- **Dual-value figure** — both defensible (an announced price against a settled one; a headline figure against a filing figure). State one canonical value and explain the other.
- **Vintage difference** — not a conflict. Present as a dated series so movement is not mistaken for disagreement.

**Every study ships a reconciliation appendix** covering all three categories plus unknowns carried forward. On a long run this is not housekeeping; it is the document's warrant.

---

## Convention 17 — The completion standard

Complete only when a sophisticated reader can mentally disassemble and reconstruct: ownership and control; legal structure; market; customers; products; value flows; operations; technology; economics; management; culture; competition; moat; risk; and future evolution.

> **"I can explain why this business makes money, and say what would have to change for it to stop."**

Where the objective is playbook extraction, a second standard applies:

> **"I know which mechanisms I would carry across, which I would change, and which I would refuse — and which institution in my own market has to play the role that one plays in theirs."**

---

# THE VOLUME ARCHITECTURE

Three configurations. **Standard is the default.** Declare the choice in §0.

## Core volumes

| | Volume | The question it owns | Compact | Standard | Extended |
|---|---|---|---|---|---|
| **I** | Institutional Anatomy | What is the legal skeleton, and who ultimately controls it? | ● | ● | ● |
| **II** | Market, Customer & Commercial Anatomy | Who pays, why, and how is demand acquired and held? | ◐ | ● | ● |
| **III** | Product, Service & Value-Flow Anatomy | What is produced, and how does value move from input to outcome? | ◐ | ● | ● |
| **IV** | Operating-System Anatomy | How are resources converted into delivered outcomes at scale? | ◐ | ● | ● |
| **V** | Technology, Data & Infrastructure Anatomy | What technical machinery makes it possible, and what is strategic? | ◐ | ● | ● |
| **VI** | Economic & Capital Anatomy | How does activity become revenue, profit, cash and return on capital? | ● | ● | ● |
| **VII** | Strategic Anatomy | Why does it win, what could destroy it, what is it becoming? | ● | ● | ● |

*● full volume · ◐ merged pair in Compact — II+III and IV+V*

## Conditional volumes — commission only against the stated test

| | Volume | The question it owns | Commission when |
|---|---|---|---|
| **VIII** | The Regulatory & Licensing Estate | How did the enterprise acquire the right to do what it does, and what does each permission cost, permit and **foreclose**? | Permissions **determine what the business can be** — banks, brokers, insurers, payments, healthcare, utilities, telecoms, defence, gambling |
| **IX** | International Expansion & Market Entry | What happened when the enterprise moved **its own mechanisms** into other markets? | The subject operates in **three or more markets**, or has entered and exited any |
| **X** | The Abandonment Record | What did the enterprise try and stop, and why? | The subject has **ten or more years of history**, or a material acquisition and disposal record |

**Why these three and not others.** Each owns a question the core seven cannot answer, and each proved its worth in practice.

*VIII* is buried in the institutional volume as three subsections (regulators, own-versus-partner capability, regulation as cost or moat). For a regulated subject that is not enough: the permission structure is a **sequence** with capital, time and foreclosure costs at each rung, and it determines the shape of everything downstream. In one study it was the most consequential volume in the set.

*IX* is where a company **ran the experiment itself** (Convention 11). One subject exported one half of its business to eight countries and withdrew the other half from every market it tried — a controlled comparison no external analysis could construct.

*X* has no home at all in the core seven. The strategic volume evaluates major decisions; it does not catalogue retreats, and it has no category for the abandonments nobody announced. In one study this volume produced the sharpest natural experiment in the company's history.

**Reconstruction** is not a volume. It is the synthesis stage, numbered `00`, operating on whatever configuration was run.

## Choosing the configuration

**Compact (5).** Fast or smaller subjects. Merges demand into product (II+III) and operations into technology (IV+V). **Back-port the TREF candidate list** per Convention 15. Note the cost: the merged II+III splits nothing, but it also means the who-pays inversion and the value-flow tracing sit in one volume — which is an advantage, not a loss.

**Standard (7).** The default. Correct for most subjects worth this effort. **The IV/V split is the stronger of the two** — it matters wherever physical operations are genuinely distinct from the technology estate, and matters little where operations *are* technology, as in software and most financial services. **The II/III split is the weaker**, because it puts a seam through the who-pays question; mitigate with Convention 7.

**Extended (8–10).** Add conditional volumes against their tests. Beyond ten, the risk shifts from omission to repetition, and Convention 8 becomes the binding constraint.

## When to depart from all three

**Expand where the subject contains genuinely separate businesses the structure would flatten.** One subject ran two ecosystems with different customers, different economics and, for most of its history, different leadership; compressing them into one product volume would have destroyed the comparison the study existed to make. That study ran to fourteen volumes — the two ecosystems separated, the regulatory estate and the money-movement layer given their own volumes, and two devoted to natural experiments.

**The test for any additional volume: does it own a question no existing volume can answer?** If not, it is a section.

---

## Stage plans

Commission in stages with a decision point at the end of each, so a study can be stopped if the early volumes show the subject does not repay the effort.

**Compact (5):** I–II · III–IV · V + reconstruction.

**Standard (7):** I–II · III–IV · V–VI · VII + reconstruction.

**Extended, licensed subject:** **VIII first**, then I–II, then the remainder. The permission structure determines what the business can be, so establishing it early re-frames every subsequent volume.

**Extraction objective:** lead with the volumes carrying the transferable mechanisms rather than the corporate history. One study ran the regulatory ladder, the credit mechanism and the payment rails as Stage 1, precisely so a negative finding would arrive in a week rather than a month. **Stage 1 is a genuine decision point, and saying so before it starts is what makes it one.**

---

## Deliverables

1. **`[SUBJECT]_Enterprise_Study_COMPLETE.md`** — all volumes plus master layer, assembled in canonical order
2. **A master layer** — front matter, these conventions instantiated, contents, and appendices: glossary, canonical figures register, source register, reconciliation. Where the subject has multiple reporting entities, a **basis-discipline appendix** explaining how to read its numbers
3. **`BUILD_SPEC.md`** — the rendering specification, prepended for handoff
4. **`assemble.py`** — assembler with gap check and anchored contents generation
5. **The ranked TREF candidate list** (Convention 15)
6. **Where the objective is extraction** — a consolidated verdict table and a sequenced build order

---

## A closing note

EREF asks a question companies do not answer about themselves: **not what they do, but why the money arrives, and what would have to be true for it to stop.**

Almost every convention here exists because the subject controls the disclosure. The evidence ladder exists because companies assert things about themselves. The basis discipline exists because they change how they report. The governing metric exists because they choose which number to lead with. The credibility convention exists because seven studies found operational narrative and audited figures have different reliability. And the discriminating-scepticism rule exists because the opposite failure — treating everything a company says as false — produces a study just as useless as credulity.

A study that reaches the completion standard is worth more than any forecast of the subject, because the forecast will be wrong and the explanation will still hold.
