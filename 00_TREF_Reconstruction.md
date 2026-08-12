# TREF — RECONSTRUCTION STAGE

**This is a synthesis prompt, not a research prompt.**

Every other TREF prompt commissions research. This one does not. It operates on volumes that already exist, and is given to the synthesiser with those volumes in hand — not to a research agent.

That is why this file carries `00` rather than a volume number, and why its opening apparatus differs from every other prompt in the framework. **Do not perform new research.** If a material gap appears, record it as a known unknown; a finding sourced here has not passed through the evidence discipline the volumes applied.

---

## §A — INPUT MANIFEST (complete and verify before beginning)

```text
Technology:              [NAME]
Type:                    [DATABASE / LEDGER / PROTOCOL / FRAMEWORK / SERVICE / HARDWARE / OTHER]
Version / commit:        [PINNED — SEE §B]
Source openness:         [OPEN SOURCE / SOURCE-AVAILABLE / DOCUMENTED-ONLY / OPAQUE]
Study objective:         [NEUTRAL TEARDOWN / BUILD EXTRACTION]
Research date:           [DATE]

Volumes supplied:
  [ ] I    Purpose, Domain & Conceptual Model
  [ ] II   Architecture & Component Anatomy
  [ ] III  Data, State, Control & Execution Flows
  [ ] IV   Implementation & Infrastructure Anatomy
  [ ] V    Correctness, Performance, Scale, Reliability & Security
  [ ] VI   Operations, Tradeoffs, Ecosystem & Rebuildability
  [ ] VII  Security & Threat Model                        (if commissioned)
```

**Gap check.** If a volume is missing, **stop and say so.** Synthesis across a hole produces a document that looks complete and is not, and the hole will be invisible to every subsequent reader.

---

## §B — INHERITED CONSTRAINTS (binding)

**Evidence labels carry through unchanged.** This stage does not re-grade. It does not promote a HYPOTHESIS to a CONFIRMED IMPLEMENTATION because the assembled picture now looks coherent — **coherence is not evidence**, and a reconstruction is exactly where that temptation is strongest. Where the volumes said UNKNOWN, it remains UNKNOWN and appears in the register.

**The version is pinned and inherited.** Do not blend behaviour across releases. Where the volumes described different versions, say so rather than reconciling silently.

**The evidence ceiling is inherited.** A study of an OPAQUE technology cannot produce a reconstruction at CONFIRMED IMPLEMENTATION, and the reconstruction must carry that limitation in its opening rather than its appendix.

**Where the objective is build extraction,** ADOPT / ADAPT / REJECT verdicts are **consolidated, not generated.** A verdict appearing for the first time here was reasoned from summary rather than evidence. If a mechanism was not adjudicated in its volume, record it as unadjudicated.

---

## §C — RECONCILIATION (perform before writing)

The volumes were researched independently and will disagree. Classify every conflict:

**Genuine error** — one volume is wrong. Establish which governs and why. **Correct it at source with a visible inline note**, then record it here.

**Version difference** — the volumes described different releases. Not an error. State both, pinned.

**Documentation-versus-implementation divergence** — Volume IV or the tests contradicted the documentation. **This is not a conflict to resolve but a finding to elevate.** The divergence itself belongs in §D.18.

**Known unknowns** — carry every UNKNOWN forward into one register.

---

## §D — THE RECONSTRUCTION

**Use the completed volumes. Do not merely summarise them. Reconstruct the technology as one coherent machine.**

The test for every section: *does this say something no single volume could say?* If it restates a volume, cut it.

1. **The technology in one sentence.**
2. **In one paragraph.**
3. **In one page.**
4. **Complete system map** — problem → domain model → abstractions → invariants → architecture → components → interfaces → execution → state → persistence → events → infrastructure → reliability and security → operations.
5. **The critical execution path**, end to end, naming the component at each hop.
6. **The source-of-truth model** — what is authoritative, what is derived, and how divergence is detected.
7. **The correctness kernel** — the minimum set of mechanisms that make the system correct. Carry the four-way enforcement classification from Volume III: what is enforced structurally, by check, by convention, or not at all.
8. **The scaling kernel** — what governs how far it goes, and what breaks first.
9. **The failure kernel** — the small number of failure modes that matter, including partial success.
10. **The security kernel** — the boundaries that must hold. *Where Volume VII was commissioned, carry its adversarial guarantee ledger: which guarantees are structurally protected, which rest on a control, which rest on an assumption, and which are unprotected. Where it was not, state that the study judged the technology outside the commission test, and why.*
11. **The resource model** — what it consumes, per unit of work.
12. **The dependency model** — what is owned, what is rented, what cannot be replaced.
13. **The top ten design tradeoffs**, each with the workload it is wrong for.
14. **Reconstruction plan from zero** — what would have to be built, in what order.
15. **Minimum viable reconstruction** — the smallest system delivering the core guarantee.
16. **Production-grade reconstruction** — what the remaining distance actually consists of.
17. **Essential against incidental** — which design choices are forced by the problem and which are historical accident.
18. **What documentation alone would have missed.** The findings that required source, tests, issues or measurement — and specifically **where the documentation and the implementation disagreed.** This section is the strongest evidence that the study was done properly.
19. **At least five common misconceptions**, with the conventional view, the reality, the evidence, and why the misconception persists.
20. **Final scorecard**, 1–10 with every score explained: conceptual clarity · abstractions · architecture · implementation · correctness · concurrency · performance · scalability · reliability · security · observability · operability · developer experience · ecosystem · maintainability · rebuildability · overall technical quality.

    **Apply discriminating scepticism.** Where the evidence supports genuine quality, score it high; where it does not, score it low and say why. A scorecard on which everything scores alike has said nothing.

21. **Final verdict** — what was built; the most elegant part; the most complex part; the weakest part; what is hardest to reproduce; what is commodity; the key invariant; the principal bottleneck; the principal failure risk; and the preserve-or-redesign recommendation.

---

## §E — WHERE THE OBJECTIVE IS BUILD EXTRACTION

Add, after §D:

**22. The consolidated verdict table.** Every ADOPT / ADAPT / REJECT from every volume, with the volume of origin. Grouped by verdict; indexed by mechanism.

**23. What transfers and what does not.** The mechanisms worth the whole study, and the environmental dependencies that kill the rest. For each REJECT, its constructive half: what should be done instead.

**24. The build order.** Stages with **tests, not instructions** — what would tell the builder to proceed, and what would tell them to stop.

**25. What this study cannot tell you.** The open questions, and which are answerable only by running the thing.

---

## §F — DELIVERABLES

1. The reconstruction document
2. The reconciliation register (§C)
3. The known-unknowns register
4. Where the objective is extraction: the consolidated verdict table and the build order

---

## Final standard

> **A sophisticated engineer can mentally disassemble and reconstruct the technology.**

And, where the objective is extraction:

> **The builder knows which mechanisms to carry across, which to change, which to refuse — and what the remaining distance to production actually consists of.**
