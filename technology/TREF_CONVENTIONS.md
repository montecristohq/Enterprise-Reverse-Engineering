# TREF CONVENTIONS — Technology Reverse-Engineering Framework

*Subject-agnostic. Instantiate per study by completing §0, then carry this document verbatim into every volume brief so that continuity does not depend on conversation memory.*

---

## How to use this document

TREF is the technology sibling of the EREF programme. EREF disassembles an **enterprise** — its legal form, its customers, its economics, its strategy. TREF disassembles a **technology** — its domain model, its architecture, its runtime, its guarantees, its failure behaviour.

The two frameworks share a spine (a depth rule, an evidence ladder, a reconstruction stage) and diverge where the object differs. **The most important divergence: EREF's sources are filings and disclosures, which a company chooses to publish. TREF's best sources are specifications, source code, schemas and commit history, which a project cannot easily misrepresent.** Where the source is open, TREF can reach a standard of proof EREF never can. Where it is closed, TREF must say so loudly rather than paper over the gap — see Convention 6.

This document is the constitution. Each volume brief instantiates it. Nothing here is advisory.

---

## §0 — SUBJECT HEADER (complete before Volume I; reproduce at the head of every brief)

```text
Technology:              [NAME]
Technology type:         [DATABASE / LEDGER / PROTOCOL / FRAMEWORK / SERVICE / HARDWARE / OTHER]
Version / release:       [VERSION]
Commit / tag:            [SHA OR TAG, IF SOURCE IS AVAILABLE]
Official documentation:  [URL]
Source repository:       [URL OR NONE]
Deployment model:        [SELF-HOSTED / CLOUD / BOTH / UNKNOWN]
Licence / edition:       [IF RELEVANT]
Research date:           [DATE]
Source openness:         [OPEN SOURCE / SOURCE-AVAILABLE / DOCUMENTED-ONLY / OPAQUE]
Study objective:         [NEUTRAL TEARDOWN / BUILD EXTRACTION — see Convention 9]
Special focus:           [OPTIONAL]
```

**The `Source openness` field governs how much of this framework is usable.** Fill it honestly at the outset. A study of an OPAQUE technology cannot reach CONFIRMED IMPLEMENTATION on anything and should say so in its front matter rather than discovering it at Volume IV.

---

## Convention 1 — Evidence classification (MANDATORY, all volumes)

Deliberately different from EREF's ladder, because a technology's evidence has different provenance.

| Label | Meaning |
|---|---|
| **CONFIRMED IMPLEMENTATION** | Verified in source, schema, or specification. The named file, function, table or clause should be identifiable |
| **DOCUMENTED BEHAVIOR** | Stated in official documentation but not verified in source |
| **MAINTAINER CLAIM** | Asserted by the project, vendor or maintainer — a blog post, a talk, a marketing page. **Not evidence of implementation** |
| **MEASURED RESULT** | A benchmark or measurement, with its methodology and conditions stated. A benchmark without conditions is a MAINTAINER CLAIM |
| **SOURCE-CODE INFERENCE** | Reasoned from reading code, with the reasoning shown |
| **ANALYTICAL INFERENCE** | Reasoned from multiple known facts, with the reasoning shown |
| **HYPOTHESIS** | Plausible, requiring further evidence |
| **UNKNOWN** | The evidence is insufficient — flagged, never papered over |

**Three rules on use.**

An inference is never silently promoted to a confirmation. If a volume says CONFIRMED IMPLEMENTATION, a reader must be able to go and look.

**DOCUMENTED BEHAVIOR and CONFIRMED IMPLEMENTATION diverge more often than anyone expects.** Documentation lags, aspires, and occasionally describes a version that no longer exists. Where a volume finds divergence, that divergence is itself a finding and belongs in the reconstruction.

**MAINTAINER CLAIM is the default for every performance, scale and security assertion** made by the project about itself, until a MEASURED RESULT or CONFIRMED IMPLEMENTATION supersedes it.

---

## Convention 2 — Version discipline

**Pin the version. Never silently mix behaviour across incompatible versions.**

Every material claim carries its version context where behaviour has changed. Where a volume describes something that changed across releases, it states the release boundary and which side it is describing.

Where a study spans a version change mid-research — which happens on long runs — the change is logged in the reconciliation register (Convention 11), not absorbed silently.

**This convention exists because the alternative is a study that is internally inconsistent and externally unfalsifiable.** The EREF programme learned this the expensive way: one subject restated its own reporting basis twice in three years, and the resulting study needed a full reconciliation appendix to remain usable.

---

## Convention 3 — Source priority

Prefer, in descending order:

1. Official specification
2. Official documentation
3. **Source code**
4. Architecture and design documents
5. ADRs, RFCs, design proposals
6. **Tests** — often the most honest statement of intended behaviour
7. Schemas and migrations
8. Release notes and changelogs
9. Issue tracker
10. Commit history
11. Official engineering posts
12. Official benchmarks
13. Package and deployment manifests
14. Standards bodies and peer-reviewed papers
15. Reputable independent technical analysis

**Two notes.** *Tests* are ranked deliberately high: a project's test suite states what it believes it guarantees, in executable form, and frequently contradicts its own documentation. *Issue trackers and commit history* are ranked low as primary sources but are the best available evidence for **why** a design is as it is — Convention 5's sixth question.

---

## Convention 4 — The five mandatory traces

Every study performs all five. These are the framework's distinctive instrument and the thing that makes a TREF study falsifiable rather than descriptive.

**Follow the execution.** Input → validation → authentication and authorisation → routing → core logic → reads → invariant checks → mutation → persistence → side effects and events → response. Trace at least one critical path end to end, naming the component at each hop.

**Follow the state.** Distinguish client-visible, in-memory, durable, derived, cached, replicated and external-system state. Establish which is authoritative, and what happens when two disagree.

**Follow the failure.** Crashes, timeouts, retries, duplicate requests, dependency failure, partial success, recovery. **Partial success is the case most studies skip and the case that most often breaks systems in production.**

**Follow the invariant.** Identify what must never be violated, then identify **exactly where it is enforced** — which component, which line, which constraint. An invariant nobody can point to is a HYPOTHESIS, not a guarantee.

**Follow the resources.** CPU, memory, disk, I/O, network, locks, queues, connections, external calls — **and operator effort**, which is a resource and is routinely omitted.

---

## Convention 5 — The six questions and the five lenses

For every material component, ask: **What? How? Who or what controls it? Where? When? Why?**

Then apply five lenses: **Structure · Flow · Control · Resource economics · Failure.**

The sixth question — **Why was it designed this way?** — is the one that separates a reverse-engineering study from a manual. Answer it from ADRs, RFCs, issue threads and commit messages where they exist, and mark it HYPOTHESIS where they do not.

---

## Convention 6 — Never invent implementation

**Where the implementation is not public, do not construct it.**

State what is known, present the plausible alternatives, name which the evidence favours and why, and label the whole as ANALYTICAL INFERENCE or HYPOTHESIS. A study that quietly fills gaps with plausible-sounding architecture is worse than useless, because it is indistinguishable from one that did not.

**UNKNOWN is a valid and frequently correct answer.** A study of an opaque technology that reaches UNKNOWN forty times has done its job. One that reaches it zero times has not.

---

## Convention 7 — Depth follows the subject

Depth follows complexity and importance, never a page count. If concurrency requires eighteen pages, write eighteen. If a subsystem needs two paragraphs, write two.

**Never compress later material because earlier material ran long.** Where output limits intervene, stop at a logical boundary and continue without compressing.

> **Completeness before concision.** There is no reward for brevity and a substantial penalty for superficiality.

---

## Convention 8 — Every volume owns a question

**Each volume answers a question no other volume can.** The question is stated at the head of the brief. If a section cannot be justified against its volume's owned question, it belongs in another volume or nowhere.

At seven volumes this is a discipline; at fourteen it is the difference between depth and restatement. The EREF programme's fourteen-volume run held together only because every brief named its owned question and refused material that belonged elsewhere.

**Where a volume is re-cut** — given a sharpened or contrarian angle because the evidence warrants it — the re-cut is stated explicitly at the head of the brief, with its reasoning. Re-cuts are how a study stops being a template and starts being an argument.

---

## Convention 9 — The build objective (studies with a transplant purpose)

TREF may be run **neutrally** — to understand a technology — or as a **build extraction**, where the reader intends to construct something informed by the subject. Declare which in §0.

Where the objective is build extraction, every volume additionally carries a verdict on each material mechanism:

| Verdict | Meaning |
|---|---|
| **ADOPT** | Works on its own logic; carry it across substantially unchanged |
| **ADAPT** | The design intent transfers but the implementation must change — state precisely what must change, and to what |
| **REJECT** | Depends on scale, infrastructure, licensing or operational capacity the builder does not have — name the dependency that kills it |

Apply the **environment question** before each verdict: *did this work because of the mechanism itself, or because of the environment surrounding it* — the team size, the hardware, the traffic profile, the operational maturity, the surrounding ecosystem? Strip the environment out, then judge.

**A REJECT is as valuable as an ADOPT**, and frequently more so, because it is the finding a builder would otherwise discover by spending a year on it.

Verdicts are stated **in the volume where the mechanism is analysed**. The reconstruction stage consolidates them; it does not generate them.

---

## Convention 10 — Cross-references written forward

Volumes may be researched out of order. **They are always assembled in canonical order I–VII.**

A brief written early must not reference a later volume by number as though it exists. Reference forward **by topic** — "the concurrency model, developed in a later volume" — and verify the reference at assembly.

---

## Convention 11 — Staging, assembly and reconciliation

**File naming.** Stage files are named by **volume number, not writing order**, zero-padded: `stages/v01.md` through `stages/v07.md`. Padding matters the moment a study exceeds nine volumes.

**Gap check.** The assembler verifies every slot is present and aborts if one is missing. A document with a silent hole in it is worse than a build failure.

**The reconciliation register.** Log every conflict as it surfaces, not at the end. Classify each as:

- **Genuine error** — one volume is wrong. Establish which governs, and **correct it at source with a visible inline note**, not only in an appendix. A reader meets the error in the body, so the correction belongs there.
- **Dual-value figure** — both values are defensible (an announced figure against a settled one; a documented default against a deployed configuration). State one canonical value and explain the other.
- **Version or vintage difference** — not a conflict at all. Present as a dated or versioned series so a reader does not mistake movement for disagreement.

**Every study ships a reconciliation appendix** recording all three categories plus the unknowns carried forward. On a long run this appendix is not housekeeping; it is the document's warrant.

---

## Convention 12 — The completion standard

The research is complete only when a sophisticated engineer can explain: why the technology exists; its domain model; its core abstractions and invariants; its architecture; its critical runtime path; how state is represented; how concurrency works; what happens under partial failure; how it scales; its security boundaries; how it is operated; its major design tradeoffs; and how to rebuild a functionally equivalent system.

The final standard:

> **"I can mentally disassemble and reconstruct this technology."**

Where the objective is build extraction (Convention 9), a second standard applies:

> **"I know which parts I would carry across, which I would change, and which I would refuse — and why."**

---

# THE VOLUME ARCHITECTURE

Three configurations. **Standard is the default; Extended is what most subjects worth a teardown will actually run.** Declare the choice in §0.

## Core volumes

| | Volume | The question it owns | Compact | Standard | Extended |
|---|---|---|---|---|---|
| **I** | Purpose, Domain & Conceptual Model | Why does this exist, what problem does it hold, and what does it promise never to violate? | ◐ | ● | ● |
| **II** | Architecture & Component Anatomy | What are the parts, where do the boundaries fall, and what talks to what? | ◐ | ● | ● |
| **III** | Data, State, Control & Execution Flows | What actually happens at runtime, and what happens when it goes wrong? | ◐ | ● | ● |
| **IV** | Implementation & Infrastructure Anatomy | What is it actually made of, and what was bought rather than built? | ◐ | ● | ● |
| **V** | Correctness, Performance, Scale & Reliability | What does it genuinely guarantee, and under what conditions do the guarantees hold? | ◐ | ● | ● |
| **VI** | Operations, Tradeoffs, Ecosystem & Rebuildability | What does it cost to run, what was traded away, and could it be rebuilt? | ◐ | ● | ● |

*● full volume · ◐ merged pair in Compact — I+II, III+IV, V+VI*

## Conditional volume

| | Volume | The question it owns | Commission when |
|---|---|---|---|
| **VII** | **Security & Threat Model** | **Which of the system's guarantees can be broken deliberately, and by whom?** | The technology **holds money, credentials or personal data, or is internet-facing or multi-tenant** |

**Why security is separated rather than kept in Volume V.** Correctness, performance, scale and reliability all ask one underlying question — *does it work, and where does it stop working?* Security asks a structurally different one: *can someone make it fail on purpose?* It draws on a different evidence base — advisories, disclosed vulnerabilities, audit scopes, disclosure policy rather than benchmarks and source — and it fails differently when done badly. **A thin performance section is incomplete; a thin security section is misleading.**

Volume V establishes the guarantee ledger. Volume VII tests every entry in it adversarially and classifies each as structurally protected, protected by control, protected by assumption, or unprotected. **That is where the two volumes reconnect, and it is the payoff of the split.**

**The conditional marking is honest, not decorative.** A compression library, a build tool or a local utility should skip Volume VII and let Volume V.15 cover the essentials. Anything holding money or identity should not.

**Reconstruction** is not a volume. It is the synthesis stage, numbered `00`, operating on whatever configuration was run.

## Choosing the configuration

**Compact (3).** A small library, a single-purpose tool, a well-documented protocol. Merge I+II, III+IV, V+VI. Six volumes on a thousand-line library is ceremony.

**Standard (6).** The default. Correct where security is genuinely a secondary concern.

**Extended (7).** Standard plus Volume VII. **For ledgers, payment rails, core banking systems, identity systems, wallets and anything multi-tenant, this is the real default** — the commission test fires on the first page.

## When to depart from all three

**The test for any additional volume: does it own a question no existing volume can answer?** If not, it is a section.

One candidate is worth naming and deliberately not promoting. **The evolution and deprecation record** — reverted architectures, removed features, abandoned proposals, major version breaks, licence changes — currently sits at Volume I.3. For a project with decades of history and a major architectural break it may earn its own volume; for most it will not. The enterprise framework promoted its equivalent only after seven completed studies proved the need. **TREF has run none, and should not front-run that evidence.**

---

## Stage plans

Commission in stages with a decision point at the end of each, so a study can be stopped if the early volumes show the subject does not repay the effort.

**Compact (3):** I+II · III+IV · V+VI + reconstruction.

**Standard (6):** I–II · III–V · VI + reconstruction.

**Extended (7):** I–II · III–V · VI–VII + reconstruction.

**Stage 1 is a genuine decision point.** If the sources will not support Volumes I and II at CONFIRMED IMPLEMENTATION or DOCUMENTED BEHAVIOR, the remaining volumes will not improve, and the honest move is to stop and record why.

**Where the objective is build extraction**, lead with the volumes carrying the transferable mechanisms. For most subjects that means **III and V before IV** — runtime behaviour and the guarantees matter more to a builder than the incumbent's implementation choices, which they will not copy anyway.

---

## Deliverables

A completed TREF study ships:

1. **`TREF_[SUBJECT]_Study_COMPLETE.md`** — the seven volumes plus master layer, assembled in canonical order
2. **A master layer** — front matter, these conventions instantiated, contents, and the appendices: glossary, canonical values register, source register, reconciliation
3. **`BUILD_SPEC.md`** — the rendering specification, prepended to the study for handoff
4. **`assemble.py`** — the assembler, with gap check and anchored contents generation
5. **Where the objective is build extraction** — a consolidated verdict table, and a sequenced build order

---

## A closing note on what this framework is for

EREF asks *how does this company make money, and would that survive being moved?* TREF asks *how does this system actually work, and could I build one?*

The second question is answerable to a much higher standard than the first, because a specification does not have an incentive to flatter itself and source code cannot be spun. **Use that.** Where the subject is open, push every material claim to CONFIRMED IMPLEMENTATION and cite the file. Where it is closed, say UNKNOWN as often as the evidence requires, and let the pattern of unknowns become a finding in its own right.

A study that reaches the completion standard is worth more than the technology it describes, because the technology will change and the reconstruction will still explain why it was ever built that way.
