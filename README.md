# EREF & TREF — Reverse-Engineering Frameworks

Two sibling frameworks for taking things apart until their machinery is understood.

**EREF** disassembles an **enterprise** — its legal form, its customers, its economics, its strategy.
**TREF** disassembles a **technology** — its domain model, its architecture, its runtime, its guarantees.

They share a spine and diverge where the object differs. One asymmetry governs almost everything: **TREF's best sources are specifications and source code, which cannot easily misrepresent themselves. EREF's sources are filings and disclosures, which a company chooses to publish and frames to its advantage.**

---

## What is in this bundle

**18 files.** Two constitutions, sixteen prompts.

```
EREF_CONVENTIONS.md            the enterprise constitution — 17 conventions
TREF_CONVENTIONS.md            the technology constitution — 12 conventions

eref/
  00_EREF_Reconstruction.md    synthesis stage (NOT a research prompt)
  01–07_EREF_Volume_*.md       seven volume research prompts

tref/
  00_TREF_Reconstruction.md    synthesis stage (NOT a research prompt)
  01–07_TREF_Volume_*.md       seven volume research prompts
```

---

## How the pieces fit

**The volume prompts say WHAT to research. The conventions say HOW, and how the volumes cohere into one study. Both go into every brief; neither substitutes for the other.**

The reason is mechanical. Each volume is commissioned cold — the agent executing Volume VI has never seen Volumes I through V. Continuity therefore cannot depend on conversation memory; it depends on the conventions document being carried verbatim into every brief, and on each brief restating its predecessors' material findings.

**A complete brief is three things:**

1. The **conventions document**, verbatim.
2. The **volume prompt**, with §0 instantiated.
3. **Subject-specific material** the templates cannot supply — the volume's owned question, any re-cut, the findings carried forward from prior volumes, source direction, and a framing note naming the analytical traps.

The third part is roughly sixty per cent of a real brief. Template plus conventions gets you the other forty.

---

## The `00` convention

**Both reconstruction files carry `00`, not `07`, and this is deliberate.**

Every other prompt commissions research. The reconstruction does not — it operates on volumes that already exist and is given to the synthesiser with those volumes in hand. It has an input manifest and a gap check instead of a source priority; it inherits evidence labels rather than generating them; and it consolidates verdicts rather than reaching them.

`00` sorts it above the volumes it consumes, which is structurally honest: it is the first file you read when deciding to run a study, and the last thing you execute.

---

## Configurations

Neither framework has a fixed volume count. Declare the choice in §0.

**EREF — Compact 5 · Standard 7 · Extended 8–10**

Standard is the default. Compact merges demand into product (II+III) and operations into technology (IV+V). Extended adds conditional volumes against stated tests: **VIII** the Regulatory & Licensing Estate (when permissions determine what the business can be), **IX** International Expansion (three or more markets, or any entry-and-exit), **X** the Abandonment Record (ten or more years of history).

*The IV/V split is the stronger of the two; the II/III split is weaker because it puts a seam through the who-pays question. Mitigate with Convention 7.*

**TREF — Compact 3 · Standard 6 · Extended 7**

Standard is the default. Compact merges I+II, III+IV, V+VI. Extended adds **VII — Security & Threat Model**, commissioned when the technology holds money, credentials or personal data, or is internet-facing or multi-tenant. The conditional marking is honest: a compression library should skip it; a ledger should not.

**The test for any additional volume: does it own a question no existing volume can answer?** If not, it is a section.

---

## The two objectives

Both frameworks run **neutrally** — to understand the subject — or as an **extraction**, where the reader intends to build something informed by it. Declare which in §0.

Under an extraction objective every volume carries **ADOPT / ADAPT / REJECT** verdicts on each material mechanism, each preceded by the **environment question**: *did this work because of the mechanism itself, or because of the environment surrounding it?* Strip the environment out, then judge.

**A REJECT is as valuable as an ADOPT**, and must carry its constructive half: having established what cannot be done, establish what should be done instead.

Verdicts are stated in the volume where the mechanism is analysed. The reconstruction consolidates them; it does not generate them.

---

## The bridge between the frameworks

**It runs one way and is formal.** EREF's technology volume closes with a ranked **TREF candidate list** — scored on business criticality, uniqueness, technical complexity, moat relevance and replacement difficulty. That list is a deliverable, not a gesture: it is where an enterprise study hands a system to a technology study.

In Compact configuration, back-port that section so the handoff survives a short run.

---

## What each framework's evidence ladder looks like

They are deliberately different, because the evidence has different provenance.

**EREF:** CONFIRMED FACT · COMPANY CLAIM · THIRD-PARTY ESTIMATE · ANALYTICAL INFERENCE · HYPOTHESIS · UNKNOWN.
*COMPANY CLAIM is the default for every operational, cultural and strategic assertion a subject makes about itself.*

**TREF:** CONFIRMED IMPLEMENTATION · DOCUMENTED BEHAVIOR · MAINTAINER CLAIM · MEASURED RESULT · SOURCE-CODE INFERENCE · ANALYTICAL INFERENCE · HYPOTHESIS · UNKNOWN.
*MAINTAINER CLAIM is the default for every performance, scale and security assertion. A benchmark without stated conditions is a MAINTAINER CLAIM, not a measurement.*

In both: **UNKNOWN is a valid and frequently correct answer.** A study that reaches it forty times has done its job; one that reaches it never has not.

---

## Provenance

**EREF's conventions are distilled from seven completed enterprise studies** — Wise plc, Atruvia AG, the DZ BANK Group, Experian plc, Robinhood Markets, Klarna, and a fourteen-volume Block, Inc. run. Several conventions exist because a specific study needed them: the governing-metric rule because one subject's revenue was meaningless by a factor of three; basis discipline because another published three sets of figures in two currencies; the credibility convention because two subjects' operational narratives proved unreliable while their audited figures did not.

**TREF's conventions are adapted from EREF plus its own first run** — an Extended-7 study of the Blnk ledger, which produced one methodological finding worth carrying forward: **an Apache-2.0 repository proved substantially unreadable by automated means for four consecutive volumes.** GitHub tree, blob and raw endpoints were blocked; the route that eventually worked was `pkg.go.dev` at the module version, which returns the exported API with source paths *and surfaces fetchable blob URLs at a version tag*. Any future TREF study should try that first.

---

## Deliverables of a completed study

1. `[SUBJECT]_Study_COMPLETE.md` — all volumes plus master layer, assembled in canonical order
2. **A master layer** — front matter, conventions instantiated, contents, and appendices: glossary, canonical figures or facts register, source register, reconciliation
3. `BUILD_SPEC.md` — the rendering specification, prepended for handoff
4. `assemble.py` — assembler with gap check and anchored contents generation
5. The ranked TREF candidate list, where EREF
6. Where the objective is extraction — a consolidated verdict table and a sequenced build order

---

## Two rules worth knowing before you start

**Every volume owns a question.** State it at the head of the brief. If a section cannot be justified against it, the section belongs elsewhere or nowhere. At five volumes this is hygiene; at fourteen it is the only thing preventing restatement.

**Correct errors at source, not only in an appendix.** When volumes disagree — and independently-executed volumes will — classify each conflict as a genuine error, a dual-value figure, or a vintage difference. Where one volume is wrong, fix it in the body with a visible inline note. A reader meets the error there; the correction belongs there.

---

> **EREF:** *"I can explain why this business makes money, and say what would have to change for it to stop."*
>
> **TREF:** *"I can mentally disassemble and reconstruct this technology."*
>
> And where the objective is extraction, in both: *"I know which mechanisms I would carry across, which I would change, and which I would refuse — and why."*
