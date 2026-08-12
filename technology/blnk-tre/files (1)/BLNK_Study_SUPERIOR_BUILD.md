# BUILD SPECIFICATION — read this before rendering

This document contains a six-volume technical reverse-engineering study of approximately **37,600 words**. What follows is a binding specification for how it must be rendered. It is not editorial guidance. Every clause is a requirement.

Render as a **screen document with a persistent sidebar** — not a paginated print document. Use the **Industry** design system: Barlow Condensed for headings, Barlow for body, `ui-monospace` for numerals, identifiers and code.

**Palette for this subject.** A **cool slate ground with a deep ink and a single amber accent** — the amber of a warning lamp, not gold. The register should be that of an engineering assessment written to be acted on, not a marketing document.

**Six palette prohibitions.** Do not reuse the **steel-blue** of the Wise, Atruvia, DZ BANK and Robinhood studies; the **signal-red** of Experian; the **bone-and-teal** of Klarna; the **warm-grey-and-oxidised-copper** of Block; or the **Broadsheet CMYK** of the Cooperative Encyclopedia. And do not use **Blnk's own brand livery** — this study reaches critical conclusions about its subject and should not wear its colours.

**This document is unusual in one respect and the design must not hide it: it declares its own incompleteness in the front matter.** Volume VII was commissioned and never executed. See §7.

---

## 1. PRESERVATION CONTRACT — non-negotiable

**1.1 Every word is retained.** Approximately **37,613 words**. Do not summarise, condense, abridge, truncate or paraphrase any section.

**1.2 Every table renders as a table.** There are **24 tables containing 243 data rows**. Appendices B and C are the document's lookup instruments; converting them to prose destroys their function. Do not drop columns to make a table fit; see §3.4.

**1.3 Every evidence label is retained in place.** The eight labels appear **158 times**: UNKNOWN (60), DOCUMENTED BEHAVIOR (26), CONFIRMED IMPLEMENTATION (19), MAINTAINER CLAIM (18), SOURCE-CODE INFERENCE (18), ANALYTICAL INFERENCE (9), MEASURED RESULT (5), HYPOTHESIS (3).

**Note the distribution and design for it.** This is a study of an open-source repository that proved substantially unreadable by automated means, and **UNKNOWN outnumbers CONFIRMED IMPLEMENTATION more than three to one.** That asymmetry is the honest summary of what four blocked retrieval attempts cost, and it should be visible at a glance rather than buried in prose. See §4.

**1.4 Every verdict is retained and rendered distinctly.** ADOPT / ADAPT / REJECT appear **81 times** (33 / 28 / 20). See §5.

**1.5 Identifiers, code and figures render intact.** Do not break these across lines: `RecordTransactionWithBalancesAndOutbox`, `idx_transactions_reference_unique`, `redlock.NewMultiLocker`, `precise_amount`, `*big.Int`, `QUEUE_BACKPRESSURE`, `SELECT FOR UPDATE SKIP LOCKED`, `±9.22×10¹⁸`, `v0.15.2`. Set all identifiers in the monospace face.

**1.6 No content in a collapsed, hidden or truncated state.**

**Verification:** the output must contain approximately 37,613 words, 24 tables and 243 data rows.

---

## 2. STRUCTURE CONTRACT

**2.1 Twelve top-level sections**, each rendering as an `h1` with a section-opening treatment:

1. Front matter — title, the interim-build gap declaration, what this document is, conventions, contents
2. Volume I — Purpose, Domain & Conceptual Model
3. Volume II — Architecture & Component Anatomy
4. Volume III — Data, State, Control & Execution Flows
5. Volume IV — Implementation & Infrastructure Anatomy
6. Volume V — Correctness, Performance, Scale & Reliability
7. Volume VI — Operations, Tradeoffs, Ecosystem & Rebuildability
8. Appendix A — Glossary
9. Appendix B — Canonical Facts Register
10. Appendix C — The Invariant Chain
11. Appendix D — Source Register
12. Appendix E — Reconciliation

**Do not collapse these into fewer top-level headings.**

**2.2 The gap declaration opens the document and must not be softened.** The front matter carries a status table in which two rows read **NOT EXECUTED** and **NOT WRITTEN**. Render those two rows in the amber accent. This is the first thing a reader should see.

**2.3 Volume VI receives a distinguished opening.** It carries the study's central judgement and is what the reader acts on.

**2.4 Numerals alternate sides.** Left on odd-numbered volumes and Appendices A, C, E; right on even-numbered volumes and Appendices B, D.

**2.5 Heading hierarchy follows the source.** Numbered sections (I.8, III.3, IV.4, V.1, VI.15) are second level; their subsections third.

**2.6 Table of contents.** Three levels. The source contains **145 linked entries** and all must appear, each linked to a live anchor.

**2.7 Persistent sidebar navigation with a current-section indicator. Build the sidebar from every heading at all three levels — 12 h1, 52 h2 and 112 h3 — not from the top-level sections alone.** This programme has already shipped one document with an 18-entry sidebar where 310 were available, and it made the longest study in the set nearly unnavigable.

**2.8 Anchors on every heading.** Cross-references between volumes are frequent — "Volume IV established…", "see Appendix E note 2" — and should be live links where the target is unambiguous.

---

## 3. TYPOGRAPHY AND TABLES

**3.1 Design system: Industry.** Barlow Condensed headings, Barlow body, monospace for identifiers.

**3.2 Palette:** slate ground, deep ink body, single amber accent. Ensure the accent is legible at 8pt — the evidence labels use it.

**3.3 Tabular numerals are mandatory** in every table and stat component.

**3.4 Wide tables.** Appendix C (the invariant chain, five columns × twelve rows), Appendix B.3 and B.5, Volume V's guarantee ledger, and Volume VI's rebuildability and alternatives matrices are all wide. Handle in this order: full-bleed or landscape on their own page; horizontal scroll within the container; reduced type size. **Never drop columns.**

**3.5 Evidence labels** as small typographic tags. **Give UNKNOWN a distinct and slightly heavier treatment** — it appears 60 times, and the document's honesty rests on a reader being able to see where the evidence ran out.

**3.6 Code and identifiers** in monospace, with a subtle ground tint. Function names, file paths, config keys and PostgreSQL error codes all qualify.

**3.7 Measure** capped at roughly 65–75 characters for body text.

---

## 4. THE EVIDENCE DISTRIBUTION — render it as a finding

**This study's most instructive methodological result is that an Apache-2.0 repository resisted four volumes of automated reading.** The label distribution *is* that result.

Build **Figure 1** (§6) as a front-matter element, and let the UNKNOWN treatment established in §3.5 carry the point through the body. A reader should finish the front matter already knowing that this is a study which says "I could not establish that" sixty times.

---

## 5. THE VERDICT SYSTEM

**5.1 Three visually distinct states**, used consistently wherever ADOPT / ADAPT / REJECT appear as verdicts:
- **ADOPT** — affirmative, amber accent at full strength.
- **ADAPT** — intermediate, distinguishable from both others at a glance.
- **REJECT** — muted or struck; **not alarm-red**, since a REJECT here is a useful finding.

**5.2 The verdicts are distributed across all six volumes**, not collected in one table — this study has no consolidated verdict table because the reconstruction stage was never written. **Note that absence in the front matter's gap treatment rather than manufacturing a table.**

**5.3 The test to design against:** a reader should be able to flick through and locate every REJECT in under a minute.

---

## 6. FIGURE MANIFEST — build all twenty

Twenty figures are specified below **with their data**. Build every one, numbered, captioned, and placed in the section named. Do not substitute, omit or invent alternatives.

**Three figures carry the study and receive full-page treatment: Figure 11 (the atomicity answer), Figure 13 (the guarantee ledger), and Figure 19 (the invariant chain).**

### FRONT MATTER

**Figure 1 — What Could and Could Not Be Established**
*Horizontal bars, the eight evidence labels by frequency.* UNKNOWN **60** · DOCUMENTED BEHAVIOR **26** · CONFIRMED IMPLEMENTATION **19** · MAINTAINER CLAIM **18** · SOURCE-CODE INFERENCE **18** · ANALYTICAL INFERENCE **9** · MEASURED RESULT **5** · HYPOTHESIS **3**. Set UNKNOWN in the amber accent; leave the rest in ink.
**Caption:** "Sixty times this study says the evidence ran out. Nineteen times it says a file and function can be named. That ratio is what four blocked retrieval attempts cost."

### VOLUME I

**Figure 2 — The Domain Model**
*Entity diagram.* Ledger (`ldg_`) contains Balance (`bln_`); Transaction (`txn_`) moves value from a **source** balance to a **destination** balance; Identity (`idt_`) attaches to balances; Transaction links to Transaction via `parent_transaction`. Show the **internal `@` balance** (e.g. `@World`, `@Fees`) sitting in the default General Ledger as the counter-entry, annotated "typically runs negative under overdraft."
**Caption:** "Debit and credit renamed to source and destination. The `@` balance is Blnk's substitute for a chart-of-accounts normality model."

**Figure 3 — Balance: Six Fields, One Version**
*The balance object.* `balance` · `credit_balance` · `debit_balance` · `inflight_balance` · `inflight_credit_balance` · `inflight_debit_balance`, plus `version` for optimistic locking and the separately-exposed `queued_credit_balance` / `queued_debit_balance` estimates. Mark clearly: **mutable cached running total, not a derived quantity.**
**Caption:** "The textbook balance is computed on demand. Blnk's is stored, mutable and versioned — and can drift from its own history."

**Figure 4 — The Removal Record**
*What was built and taken out.* **In-transaction FX** — `rate` added v0.6.2 (May 2024), removed v0.15.0 (June 2026), with `currency_multiplier` and `modification_ref`. Plus: synchronous-by-default bulk and inflight commit (moved to queue-by-default); plaintext API keys (hashed at rest v0.12.0).
**Caption:** "The most informative removal in the record. Blnk chose strict value conservation — destination credit equals source debit — over the convenience of converting inside a transfer."

### VOLUME II

**Figure 5 — One Binary, Three Roles**
*The deployment.* One Go image invoked as **`blnk migrate up`** (one-shot), **`blnk start`** (API server, port 5001), **`blnk workers`** (queue consumer, port 5004). Beneath: **PostgreSQL 16** (source of truth) · **Redis 7.2.4** (queue + locks, via `hibiken/asynq`) · **Typesense 29.0** (optional search) · **Jaeger** (optional tracing).
**Caption:** "A modular monolith. Redis is on the correctness path, not a cache — it holds the locks that serialise every balance mutation."

**Figure 6 — Rented Versus Owned**
*Register with consequence.* **PostgreSQL** — rented; if it goes, total halt; no like-for-like substitute; migration prohibitive. **Redis** — rented; money movement halts; drop-in substitute exists but swapping `asynq` is costly. **asynq** — a dependency on the correctness path; rewrite required to replace. **Typesense** — optional; search degrades to DB-filter fallback. **Blnk Cloud** — optional; Core unaffected.
**Caption:** "Two dependencies define the correctness envelope, and neither can be replaced without rebuilding the ledger around it."

**Figure 7 — Single Points of Failure**
*Blast radius per component.* Postgres unavailable → total halt, not graceful. Redis unavailable → all money movement stops; locks unobtainable. Typesense unavailable → search only, graceful. Worker crash mid-transaction → recoverable via `queue_recovery` and the unique-reference index.
**Caption:** "Only one of these degrades gracefully."

### VOLUME III

**Figure 8 — Where the Money Actually Moves**
*The queued path, with the response point marked.* API process: parse → authenticate → `validateTxn` (reference SELECT) → set status → `HashTxn` → enqueue to Redis. **⟵ THE CALLER'S RESPONSE RETURNS HERE, STATUS `QUEUED`, REFERENCE SUFFIXED `_q`. NO MONEY HAS MOVED.** Worker process: dequeue → `executeWithLock` → validate → apply to balances in memory → **the atomic composite write ⟵ THE REAL COMMIT POINT** → post-commit actions.
**Caption:** "A 201 means accepted, not settled. For a member watching a contribution land, these are entirely different moments."

**Figure 9 — The TOCTOU Window and What Closes It**
*Two concurrent identical requests.* Both call `validateTxn` → both find no existing reference → both proceed. The database resolves it: **unique index `idx_transactions_reference_unique`** → PostgreSQL error **`23505`** → caught by `IsDuplicateReferenceError`. Annotate: the loser receives an error to interpret, not a clean success echo.
**Caption:** "The application check is an optimisation. The index is the guarantee."

**Figure 10 — The Supersession**
*What Volume III found in the 2024 fork, against what Volume IV found at v0.15.2.* Three rows. **Balance and row written separately, balance first** → **one atomic composite write.** **`int64(Amount × Precision)` lossy float multiply** → **`*big.Int` accepted directly.** **Lock on source balance only** → **MultiLocker over both, sorted and deduplicated.**
**Caption:** "Volume III wrote down the condition under which its own conclusions would collapse. Volume IV tested it. They collapsed — and that is the method working."

### VOLUME IV

**Figure 11 — The Atomicity Answer** *(signature figure, full page)*
*The question three volumes deferred, resolved.* Left panel, **the hazard as it was**: `processBalances` persists balances → *crash window* → `finalizeTransaction` inserts the row. Durable one-sided state: balances moved, no APPLIED row, nothing detects it.
Right panel, **v0.15.2**: apply to balances **in memory** → build work including the lineage outbox → **one call, `RecordTransactionWithBalancesAndOutbox(ctx, txn, sourceBalance, destinationBalance, outbox)`** → source comment reads *"Transaction and balances persisted atomically."* Either all three land or none do.
**Caption:** "This single question governs whether the ledger is usable for members' savings without patching it. The answer is yes — and it is the most valuable thing Volume IV established."

**Figure 12 — The MultiLocker**
*The lock, corrected.* `executeWithLock` resolves `@`-indicator balances to IDs **before** locking → `redlock.NewMultiLocker(l.redis, []string{sourceBalanceID, destinationBalanceID}, token)` → **deduplicates when source equals destination** → **sorts keys lexicographically**, giving a global acquisition order that makes deadlock structurally impossible. Annotate the default TTL: **1800 seconds**, flagged as a live risk.
**Caption:** "Deterministic ordering prevents deadlock. A thirty-minute TTL means a stalled worker can hold a balance hostage — and if it expires mid-operation, the serialisation is simply gone."

### VOLUME V

**Figure 13 — The Guarantee Ledger, Ranked** *(signature figure, full page)*
*Nine guarantees, strongest to weakest, each with its enforcement class.*
**1 · Atomicity and conservation** — structural — *strongest*
**2 · Immutability** — DB protection, trigger definition unread
**3 · Idempotency** — structural, unique index
**4 · Precision integrity** — structural in Go, storage range UNKNOWN
**5 · Concurrency safety** — by check; fails if the lock expires
**6 · Sufficient funds** — by check
**7 · Zero and malformed rejected** — by check
**8 · Tamper-evidence** — by convention, **off by default**
**9 · Read-your-writes, and tenancy plus resource isolation** — **not guaranteed / not enforced** — *weakest*
**Caption:** "Technologies are marketed on their strongest guarantee and broken through their weakest. Blnk is sold on immutability and double-entry correctness. It will be broken by a caller who assumes a read reflects a write, or an operator who assumes tenants are isolated."

**Figure 14 — The Hot Balance**
*Behaviour at the contention point.* **10 concurrent writers** into one pooled balance: queue absorbs, brief lock waits, latency rises modestly. **100**: lock queue depth grows; coalescing batches same-pair work; hot-lane routing may activate. **1000**: serial commit rate is the hard ceiling; `QUEUE_BACKPRESSURE` 503 sheds new enqueues; **only balance sharding removes the bottleneck.** Annotate: *adding workers does not help and can worsen contention.*
**Caption:** "A cooperative's pooled contribution account on collection day is a hot balance by construction. This is the reader's most likely incident, and it arrives long before aggregate volume matters."

**Figure 15 — The Correctness-Detection Gap**
*What the observability stack sees, and what it misses.* **Detected:** availability, latency, queue depth, lock contention (`HotpairsContentionTotal`), chain lag (`CountUnchainedTransactions` — *only if the chain is enabled*). **Not detected by default:** a balance that has silently drifted from its transaction history. Show reconstruction recording a `difference` in metadata **with no alert**.
**Caption:** "Strong availability detection, weak correctness detection. A drifted balance can sit unnoticed indefinitely — and this is money held on behalf of members."

### VOLUME VI

**Figure 16 — Total Cost of Ownership**
*Sized for a Nigerian cooperative group, 5,000–50,000 members, monthly contribution cycles.* Compute $40–120 · PostgreSQL $60–250 · Redis $15–60 · Object storage $5–20 · Optional search and observability $0–60 · Bandwidth $5–20 · **Licensing $0**. **Infrastructure subtotal $150–600/month.** Then, at visibly greater weight: **operator labour 0.3–0.5 FTE**, plus a one-time correctness-layer build of 4–8 engineer-weeks. Per-transaction infrastructure ~$0.001–0.003.
**Caption:** "The servers are trivial. The engineer is the cost — and most of that engineer's time goes to the correctness monitoring Blnk deliberately does not provide."

**Figure 17 — The Rebuildability Matrix**
*Twelve capabilities, scored, then sorted into three buckets.* **Must build:** the atomic composite write · the distributed-lock discipline · precision correctness · drift monitoring. **Can assemble:** queue and backpressure · immutability and hash chain · reconciliation · search · observability · backup and point-in-time recovery. **Can buy:** managed Postgres · managed Redis · object storage · managed search — or Blnk Cloud wholesale. Annotate the timeline: **~2–3 months to a minimum-viable correct ledger, ~6–9 months to production-grade**, for a 2–3 engineer team.
**Caption:** "Four things must be built. Everything else is assemblable or buyable — and the distance from viable to production is almost entirely monitoring and drills, not ledger algorithms."

**Figure 18 — Preserve or Redesign**
*For a builder.* **Preserve:** atomic composite write · idempotency index · modular monolith · PostgreSQL. **Preserve with modification:** MultiLocker (keep the sorted-dedup discipline, shorten the TTL) · cached balance (add an always-on drift alarm) · hash chain (make it always-on). **Replace:** caller-supplied per-transaction precision → a canonical per-asset registry. **Needs benchmark:** queue-by-default, against the hot-balance profile.
**Caption:** "Written for someone building, not someone assessing."

### APPENDIX C

**Figure 19 — The Invariant Chain** *(signature figure, full page)*
*Twelve invariants tracked across four volumes.* Columns: number · invariant · where enforced · **the four-way classification** · evidence. Render the classification as four visually distinct states: **structural** (a constraint or type makes violation impossible) · **by check** (code tests it; another path could reach the same state) · **by convention** (nothing tests it) · **not enforced**.
Mark the four genuine guarantees — conservation, idempotency, precision-in-Go, immutability-if-the-trigger-is-real. Mark in the amber accent the two that are **not enforced in any meaningful sense: tamper-evidence, because it ships disabled, and tenancy, because no component owns it.**
**Caption:** "Volume I catalogued these. Volume II located them in components. Volume III verified them at runtime. Volume V specified them as assertable conditions. This is the study's spine, and the two amber rows are what a builder inherits if he adopts without patching."

### APPENDIX E

**Figure 20 — The Reconciliation**
*Three corrections and two version differences.* **Corrected at source:** the lock package (`internal/lock` → `internal/redlock`, four occurrences) · the money column type (NUMERIC inferred → **permanently UNKNOWN**) · Volume III's runtime findings (superseded by Volume IV, banner at the head). **Version differences, not errors:** the release pin (v0.15.0 → **v0.15.2 governs**) · the fork (August 2024 source, two years before the pinned release).
**Caption:** "Corrections belong in the body where a reader meets the error, not in an appendix they may never reach."

---

## 7. THE GAP — render it honestly

**This study is incomplete and says so.** Volume VII — Security & Threat Model — was commissioned in the EXTENDED 7 configuration and never executed; the reconstruction stage was never written.

Four requirements:

- **The status table in the front matter** carries two rows reading **NOT EXECUTED** and **NOT WRITTEN**. Render them in the amber accent, visually heavier than the six complete rows.
- **The paragraph naming what the missing volume would have established** — which guarantees can be broken deliberately, what bypasses authorisation, who can decrypt, the disclosed-vulnerability pattern — is the most important prose in the front matter. Give it weight.
- **Do not manufacture a consolidated verdict table.** The 81 verdicts are distributed across six volumes because the reconstruction that would have collected them was never written. Note the absence; do not paper over it.
- **The filename says INTERIM. Keep that visible in the running header or the title treatment.** A reader who opens this document in six months must not mistake it for the finished study.

---

## 8. ANTI-PATTERNS — build failures to avoid

- **Softening or hiding the gap declaration.** It is the first thing a reader should see.
- **Rendering the Volume III supersession banner as a decorative blockquote.** It is a correction notice and the single most valuable passage in the document — a volume that predicted its own falsification. Render it as an alert, not an aside.
- **Building the sidebar from top-level sections only.** This failure has already occurred once in this programme.
- **Treating UNKNOWN as a soft label.** It appears sixty times and carries the document's honesty.
- **Converting Appendix B or Appendix C to prose.** They are lookup instruments; the tables *are* the content.
- **Rendering ADOPT / ADAPT / REJECT as plain text.**
- **Setting identifiers in the body face.** `RecordTransactionWithBalancesAndOutbox` in Barlow is unreadable and unsearchable.
- **Using Blnk's brand livery or any prior study's palette.**

---

## 9. BUILD CHECKLIST

- [ ] ~37,613 words of body prose present
- [ ] 24 tables, 243 data rows, all rendered as tables
- [ ] Twelve `h1` sections in the correct order
- [ ] **The gap declaration opens the document, with NOT EXECUTED / NOT WRITTEN in the accent**
- [ ] **"INTERIM" visible in the title or running header**
- [ ] Volume VI given a distinguished opening
- [ ] Numerals alternate — odd volumes and A, C, E left; even volumes and B, D right
- [ ] Three-level contents list, 145 entries, zero dead links
- [ ] **Persistent sidebar built from all three heading levels (12 h1, 52 h2, 112 h3)**
- [ ] **ADOPT / ADAPT / REJECT rendered as three distinct states throughout**
- [ ] All twenty figures built, numbered and captioned
- [ ] Figures 11, 13 and 19 given full-page treatment
- [ ] Evidence labels intact; **UNKNOWN given distinct, heavier treatment**
- [ ] All identifiers in monospace; none broken across lines
- [ ] Tabular numerals active in all tables
- [ ] Wide tables full-bleed or scrollable, no columns dropped
- [ ] **The Volume III supersession banner rendered as an alert, not a quotation**
- [ ] Every heading carries a stable anchor; cross-volume references linked
- [ ] Slate and amber; no brand livery, no prior study's palette

---

*The specification ends here. The study follows in full.*

---

# Blnk

**A Technology Reverse-Engineering Study — with a Build-Extraction Objective**

Six of seven volumes · Domain model and invariants · Architecture · Runtime behaviour · Implementation · Guarantees · Operations and rebuildability

Subject: the open-source double-entry financial ledger by Blnk Finance
Repository: `github.com/blnkfinance/blnk` · Apache-2.0
Research cut-off: 11 August 2026
First subject in the TREF programme

---

## ⚠ INTERIM BUILD — the gap check fails on one slot

**This study was commissioned in the EXTENDED 7 configuration. Volume VII — Security & Threat Model — has not been executed, and the reconstruction stage has not been written.**

The TREF reconstruction prompt requires a gap check before synthesis, on the principle that *synthesis across a hole produces a document that looks complete and is not, and the hole will be invisible to every subsequent reader.* This front matter is that declaration.

| | Volume | Status |
|---|---|---|
| **I** | Purpose, Domain & Conceptual Model | ✓ Complete |
| **II** | Architecture & Component Anatomy | ✓ Complete |
| **III** | Data, State, Control & Execution Flows | ✓ Complete — **partially superseded by IV, see the notice at its head** |
| **IV** | Implementation & Infrastructure Anatomy | ✓ Complete |
| **V** | Correctness, Performance, Scale & Reliability | ✓ Complete |
| **VI** | Operations, Tradeoffs, Ecosystem & Rebuildability | ✓ Complete |
| **VII** | **Security & Threat Model** | **✗ NOT EXECUTED** |
| **00** | **Reconstruction** | **✗ NOT WRITTEN** |

**What the missing volume would have established**, and what the reader therefore does not yet know: which of the guarantees ranked in Volume V can be broken *deliberately* rather than merely failing under load; where authorisation is enforced and what bypasses it; who can decrypt the data, including operators and backup holders; where sensitive data ends up that the design did not intend; the pattern formed by Blnk's disclosed vulnerabilities and what it says about the architecture; whether the project has a functioning security-response process; and which controls a new implementation cannot defer.

**For a ledger holding cooperative members' savings, that is not an optional appendix.** Volume VI's central judgement — fork Blnk, take its mechanisms, fix its correctness defaults — should be treated as provisional until Volume VII has tested the adversarial case.

---

## What this document is

A forensic technical reverse-engineering study of **Blnk**, an open-source double-entry financial ledger written in Go, backed by PostgreSQL and Redis, published under Apache-2.0 by Blnk Finance LLC.

**It is a build extraction, not a neutral teardown.** The reader is a founder building a proprietary core-banking platform for cooperative societies in Nigeria, intended to be permanently founder-owned on a vendor model, supporting member savings, contributions, loans and eventually remittance. Blnk was selected because it is the closest existing open-source analogue to the ledger layer of that platform — and because it is Nigerian in origin, which makes its design assumptions unusually relevant.

Every volume therefore carries **ADOPT / ADAPT / REJECT** verdicts, and Volume VI reaches a judgement on whether to adopt, fork, rebuild or look elsewhere.

| | Volume | The question it owns |
|---|---|---|
| **I** | Purpose, Domain & Conceptual Model | Why does this exist, what problem does it hold, and what does it promise never to violate? |
| **II** | Architecture & Component Anatomy | What are the parts, where do the boundaries fall, and what talks to what? |
| **III** | Data, State, Control & Execution Flows | What actually happens at runtime, and what happens when it goes wrong? |
| **IV** | Implementation & Infrastructure Anatomy | What is it actually made of, and what was bought rather than built? |
| **V** | Correctness, Performance, Scale & Reliability | What does it genuinely guarantee, and under what conditions do the guarantees hold? |
| **VI** | Operations, Tradeoffs, Ecosystem & Rebuildability | What does it cost to run, what was traded away, and could it be rebuilt? |
| **A** | Glossary | Ledger, Go, PostgreSQL and Redis vocabulary |
| **B** | Canonical Facts Register | The governing value for every material claim |
| **C** | The Invariant Chain | Twelve invariants tracked across four volumes |
| **D** | Source Register | What the study rests on, and the retrieval problem |
| **E** | Reconciliation | Where the volumes disagreed, and which governs |

**Recommended first pass.** Volume VI, sections 15–17 (rebuildability, preserve-versus-redesign, and the central judgement) → Volume V, section 1 (the guarantee ledger, ranked) → Volume IV, section 4 (the atomicity answer) → Appendix C (the invariant chain). The remaining material is reference-depth.

---

## Conventions governing the whole study

### §0 — Subject header

```text
Technology:              Blnk — open-source double-entry financial ledger
Technology type:         LEDGER
Primary repository:      github.com/blnkfinance/blnk
Client SDK:              github.com/blnkfinance/blnk-go (client interface only)
Version / release:       v0.15.2 (31 July 2026) — the governing pin
                         Volumes I and II were researched against v0.15.0 (22 June 2026)
Source openness:         OPEN SOURCE — Apache-2.0 ("Blnk Core"); open-core, Blnk Cloud commercial
Deployment model:        BOTH — self-hosted or managed Blnk Cloud
Research date:           11 August 2026
Study objective:         BUILD EXTRACTION
Configuration:           EXTENDED 7 — Volume VII commissioned, NOT EXECUTED
```

**On the version pin.** The study opened against v0.15.0 and Volumes IV, V and VI read v0.15.2 directly. **v0.15.2 governs.** Where a finding derives from v0.15.0 or earlier, the volume states the release. Behaviour is not silently mixed across releases.

### Evidence classification

| Label | Meaning |
|---|---|
| **CONFIRMED IMPLEMENTATION** | Verified in source, schema or specification — the file, function or clause is named |
| **DOCUMENTED BEHAVIOR** | Stated in official documentation but not verified in source |
| **MAINTAINER CLAIM** | Asserted by the project — a blog post, README, talk. **Not evidence of implementation** |
| **MEASURED RESULT** | A benchmark with methodology and conditions stated. Without conditions it is a MAINTAINER CLAIM |
| **SOURCE-CODE INFERENCE** | Reasoned from reading code, with the reasoning shown |
| **ANALYTICAL INFERENCE** | Reasoned from multiple known facts, with the reasoning shown |
| **HYPOTHESIS** | Plausible, requiring further evidence |
| **UNKNOWN** | The evidence is insufficient — flagged, never papered over |

**Three rules on use.** An inference is never silently promoted to a confirmation. Where documentation and source diverge, **the divergence is itself a finding** — and this study found several. And **every performance, scale and reliability claim the project makes about itself is a MAINTAINER CLAIM** until a MEASURED RESULT supersedes it; Blnk's "up to about 5×" throughput figure states no hardware, dataset, concurrency level or measured metric, and does not clear that bar.

### The evidence ceiling, and the retrieval problem

**This study's most instructive methodological finding is that an Apache-2.0 repository proved substantially unreadable by automated means for four volumes.**

GitHub's tree, blob and raw endpoints blocked retrieval; jsDelivr and the Go module proxy did not work. Volumes II and III were forced to work from documentation and, in Volume III's case, from a two-year-old public fork. **Volume IV broke it**: `pkg.go.dev` at the current module returns the complete exported API with source paths and line numbers, *and surfaces GitHub blob URLs at a version tag which can then be fetched.*

The consequence is recorded honestly throughout: **the PostgreSQL DDL was never read.** After four attempts across four volumes, Volume V declared the money column type **permanently UNKNOWN** for this study. Appendix E note 2 states the consequence.

### Never invent implementation

Where something could not be established, the study writes UNKNOWN, presents the plausible alternatives and names which the evidence favours. **A volume that quietly fills gaps with plausible-sounding architecture is worse than useless, because it is indistinguishable from one that did not.**

### The build-extraction verdicts

| Verdict | Meaning |
|---|---|
| **ADOPT** | Works on its own logic; carry it across substantially unchanged |
| **ADAPT** | The design intent transfers but the implementation must change — stated precisely |
| **REJECT** | Depends on scale, infrastructure, licensing or operational capacity the builder does not have |

Each carries the **environment question**: *did this work because of the mechanism itself, or because of the environment around it — the team, the scale, the deployment, the ecosystem?* Strip the environment out, then judge. **A REJECT is as valuable as an ADOPT**, and must carry its constructive half.

### Depth follows the subject

Sections are not of equal length. A section ends when its questions are answered.

---

## Contents

- [VOLUME I — Purpose, Domain & Conceptual Model](#volume-i-purpose-domain-conceptual-model)
  - [§0 — Subject Header](#0-subject-header)
  - [TL;DR](#tldr)
  - [Key Findings (ten most important)](#key-findings-ten-most-important)
  - [Details](#details)
    - [I.1 Problem origin](#i1-problem-origin)
    - [I.2 Historical evolution (with causes)](#i2-historical-evolution-with-causes)
    - [I.3 The removal record](#i3-the-removal-record)
    - [I.4 Actors and users](#i4-actors-and-users)
    - [I.5 Jobs to be done](#i5-jobs-to-be-done)
    - [I.6 Domain glossary (industry-standard vs Blnk-specific; redefinitions flagged)](#i6-domain-glossary-industry-standard-vs-blnk-specific-redefinitions-flagged)
    - [I.7 Core abstractions (domain model)](#i7-core-abstractions-domain-model)
    - [I.8 THE INVARIANT CATALOGUE](#i8-the-invariant-catalogue)
    - [I.9 Semantics (Blnk meaning vs ordinary meaning)](#i9-semantics-blnk-meaning-vs-ordinary-meaning)
    - [I.10 Assumptions (what Blnk assumes the surrounding system provides)](#i10-assumptions-what-blnk-assumes-the-surrounding-system-provides)
    - [I.11 Explicit non-goals](#i11-explicit-non-goals)
    - [I.12 Standards and theory](#i12-standards-and-theory)
    - [I.13 Competing conceptual models](#i13-competing-conceptual-models)
    - [I.14 Falsification test](#i14-falsification-test)
    - [I.15 Preliminary build-extraction verdicts (ADOPT / ADAPT / REJECT)](#i15-preliminary-build-extraction-verdicts-adopt-adapt-reject)
    - [I.16 Volume I reconstruction (synthesis)](#i16-volume-i-reconstruction-synthesis)
  - [Recommendations](#recommendations)
  - [Caveats](#caveats)
- [VOLUME II — Architecture & Component Anatomy](#volume-ii-architecture-component-anatomy)
  - [TL;DR](#tldr-1)
  - [Key Findings](#key-findings)
  - [Details](#details-1)
    - [II.1 System boundary; what Blnk Cloud is](#ii1-system-boundary-what-blnk-cloud-is)
    - [II.2 Component inventory (selected; state ownership in bold)](#ii2-component-inventory-selected-state-ownership-in-bold)
    - [II.3 Architectural style — PROVEN](#ii3-architectural-style-proven)
    - [II.4 Interfaces](#ii4-interfaces)
    - [II.5 Dependency graph (from imports; `go.mod` not opened directly)](#ii5-dependency-graph-from-imports-gomod-not-opened-directly)
    - [II.6 Rented vs owned](#ii6-rented-vs-owned)
    - [II.7 Single points of failure](#ii7-single-points-of-failure)
    - [II.8 State ownership](#ii8-state-ownership)
    - [II.9 Storage architecture — the money-type question, answered honestly](#ii9-storage-architecture-the-money-type-question-answered-honestly)
    - [II.10 Control plane vs data plane](#ii10-control-plane-vs-data-plane)
    - [II.11 Integration architecture](#ii11-integration-architecture)
    - [II.12 Deployment topologies](#ii12-deployment-topologies)
    - [II.13 Multi-tenancy and isolation — critical for the reader](#ii13-multi-tenancy-and-isolation-critical-for-the-reader)
    - [II.14 Architecture evolution](#ii14-architecture-evolution)
    - [II.15 INVARIANT LOCATION TABLE — the spine](#ii15-invariant-location-table-the-spine)
    - [II.16 Falsification watch](#ii16-falsification-watch)
    - [II.17 Build-extraction verdicts](#ii17-build-extraction-verdicts)
    - [II.18 Reconstruction summary](#ii18-reconstruction-summary)
  - [Recommendations](#recommendations-1)
  - [Caveats](#caveats-1)
- [VOLUME III — Data, State, Control & Execution Flows](#volume-iii-data-state-control-execution-flows)
  - [TL;DR](#tldr-2)
  - [Key Findings](#key-findings-1)
  - [Details](#details-2)
    - [III.1 Representative operations (boundary-crossing set)](#iii1-representative-operations-boundary-crossing-set)
    - [III.2 Happy-path execution — queued vs direct](#iii2-happy-path-execution-queued-vs-direct)
    - [III.3 INVARIANT ENFORCEMENT VERIFICATION TABLE](#iii3-invariant-enforcement-verification-table)
    - [III.4 State machines](#iii4-state-machines)
    - [III.5 Data flow & lossy transformations](#iii5-data-flow-lossy-transformations)
    - [III.6 Transaction boundaries & the real commit point](#iii6-transaction-boundaries-the-real-commit-point)
    - [III.7 Ordering & time](#iii7-ordering-time)
    - [III.8 Concurrency at the contention point](#iii8-concurrency-at-the-contention-point)
    - [III.9 Idempotency model](#iii9-idempotency-model)
    - [III.10 Events & asynchrony](#iii10-events-asynchrony)
    - [III.11 PARTIAL-SUCCESS MATRIX](#iii11-partial-success-matrix)
    - [III.12 Failure matrix — durable end-state](#iii12-failure-matrix-durable-end-state)
    - [III.13 Recovery & reconciliation](#iii13-recovery-reconciliation)
    - [III.14 Read paths & staleness](#iii14-read-paths-staleness)
    - [III.15 Mutation, deletion, immutability](#iii15-mutation-deletion-immutability)
    - [III.16 Falsification watch](#iii16-falsification-watch)
    - [III.17 Build-extraction verdicts](#iii17-build-extraction-verdicts)
    - [III.18 Reconstruction — answers to the volume's closing questions](#iii18-reconstruction-answers-to-the-volumes-closing-questions)
    - [Ten most important findings (ranked)](#ten-most-important-findings-ranked)
  - [Recommendations](#recommendations-2)
  - [Caveats](#caveats-2)
- [VOLUME IV — Implementation & Infrastructure Anatomy](#volume-iv-implementation-infrastructure-anatomy)
  - [What Blnk is made of, and what was bought rather than built](#what-blnk-is-made-of-and-what-was-bought-rather-than-built)
  - [EVIDENCE CEILING (read first)](#evidence-ceiling-read-first)
  - [TL;DR](#tldr-3)
  - [Key Findings](#key-findings-2)
  - [Details](#details-3)
    - [IV.1 Repository & artefact map](#iv1-repository-artefact-map)
    - [IV.2 Languages, runtimes, concurrency & memory model](#iv2-languages-runtimes-concurrency-memory-model)
    - [IV.3 Critical source paths — named (literal trace)](#iv3-critical-source-paths-named-literal-trace)
    - [IV.4 THE TRANSACTION-BOUNDARY QUESTION (Debt 1) — ANSWERED](#iv4-the-transaction-boundary-question-debt-1-answered)
    - [IV.5 Algorithms & data structures](#iv5-algorithms-data-structures)
    - [IV.6 SCHEMA RECONSTRUCTION (Debt 2) — PARTIAL; DDL STILL UNREAD (third time)](#iv6-schema-reconstruction-debt-2-partial-ddl-still-unread-third-time)
    - [IV.7 Persistence layer](#iv7-persistence-layer)
    - [IV.8 Networking & protocols](#iv8-networking-protocols)
    - [IV.9 Background work & failure consequences](#iv9-background-work-failure-consequences)
    - [IV.10 Configuration surface & dangerous combinations](#iv10-configuration-surface-dangerous-combinations)
    - [IV.11 Build, test & release](#iv11-build-test-release)
    - [IV.12 TESTS AS EXECUTABLE SPECIFICATION](#iv12-tests-as-executable-specification)
    - [IV.13 Deployment reconstruction](#iv13-deployment-reconstruction)
    - [IV.14 Infrastructure dependencies & minimum viable deployment](#iv14-infrastructure-dependencies-minimum-viable-deployment)
    - [IV.15 Build, buy or open source](#iv15-build-buy-or-open-source)
    - [IV.16 Build-extraction verdicts](#iv16-build-extraction-verdicts)
    - [IV.17 Volume IV reconstruction — synthesis answers](#iv17-volume-iv-reconstruction-synthesis-answers)
  - [Recommendations (staged, with thresholds)](#recommendations-staged-with-thresholds)
  - [Caveats](#caveats-3)
- [VOLUME V — Correctness, Performance, Scale & Reliability](#volume-v-correctness-performance-scale-reliability)
  - [TL;DR](#tldr-4)
  - [Key Findings](#key-findings-3)
  - [Details](#details-4)
    - [V.1 — The Guarantee Ledger (ranked)](#v1-the-guarantee-ledger-ranked)
    - [V.2 — Correctness specification (invariants as assertable conditions)](#v2-correctness-specification-invariants-as-assertable-conditions)
    - [V.3 — Numerical and precision semantics](#v3-numerical-and-precision-semantics)
    - [V.4 — Consistency guarantees (in caller terms)](#v4-consistency-guarantees-in-caller-terms)
    - [V.5 — Atomicity and isolation](#v5-atomicity-and-isolation)
    - [V.6 — Concurrency under stress (at the contention point, not the average)](#v6-concurrency-under-stress-at-the-contention-point-not-the-average)
    - [V.7 — Latency decomposition (QUEUED vs APPLIED are different numbers)](#v7-latency-decomposition-queued-vs-applied-are-different-numbers)
    - [V.8 — Throughput model](#v8-throughput-model)
    - [V.9 — Scalability](#v9-scalability)
    - [V.10 — Capacity model (sized for a real cooperative)](#v10-capacity-model-sized-for-a-real-cooperative)
    - [V.11 — Reliability mechanisms and retry-amplification assessment](#v11-reliability-mechanisms-and-retry-amplification-assessment)
    - [V.12 — Durability and recovery](#v12-durability-and-recovery)
    - [V.13 — Observability and the correctness-detection verdict](#v13-observability-and-the-correctness-detection-verdict)
    - [V.14 — Resource isolation and noisy neighbours (performance dimension only)](#v14-resource-isolation-and-noisy-neighbours-performance-dimension-only)
    - [V.15 — Security (deferred)](#v15-security-deferred)
    - [V.16 — Failure-scenario matrix](#v16-failure-scenario-matrix)
    - [V.17 — Build-extraction verdicts](#v17-build-extraction-verdicts)
    - [V.18 — Volume V reconstruction](#v18-volume-v-reconstruction)
  - [Recommendations](#recommendations-3)
  - [Caveats](#caveats-4)
- [VOLUME VI — Operations, Tradeoffs, Ecosystem & Rebuildability](#volume-vi-operations-tradeoffs-ecosystem-rebuildability)
  - [TL;DR](#tldr-5)
  - [Key Findings](#key-findings-4)
  - [Details](#details-5)
    - [VI.1 Installation and bootstrap](#vi1-installation-and-bootstrap)
    - [VI.2 Day-two operations](#vi2-day-two-operations)
    - [VI.3 Upgrade and migration](#vi3-upgrade-and-migration)
    - [VI.4 Troubleshooting](#vi4-troubleshooting)
    - [VI.5 Incident response (cross-referenced to Volume V's failure matrix)](#vi5-incident-response-cross-referenced-to-volume-vs-failure-matrix)
    - [VI.6 Developer experience](#vi6-developer-experience)
    - [VI.7 Operator experience — effort in people](#vi7-operator-experience-effort-in-people)
    - [VI.8 Total cost of ownership — model sized for the reader](#vi8-total-cost-of-ownership-model-sized-for-the-reader)
    - [VI.9 Governance and maintainership — first-order risk](#vi9-governance-and-maintainership-first-order-risk)
    - [VI.10 Licensing and commercial boundaries — and the fork question](#vi10-licensing-and-commercial-boundaries-and-the-fork-question)
    - [VI.11 Ecosystem](#vi11-ecosystem)
    - [VI.12 Alternatives](#vi12-alternatives)
    - [VI.13 The design-tradeoff ledger (with losing cases named)](#vi13-the-design-tradeoff-ledger-with-losing-cases-named)
    - [VI.14 Technical debt and constraints (what the maintainers themselves surface)](#vi14-technical-debt-and-constraints-what-the-maintainers-themselves-surface)
    - [VI.15 The rebuildability test](#vi15-the-rebuildability-test)
    - [VI.16 Preserve or redesign (for a builder)](#vi16-preserve-or-redesign-for-a-builder)
    - [VI.17 Transplant verdicts (ADOPT / ADAPT / REJECT)](#vi17-transplant-verdicts-adopt-adapt-reject)
    - [VI.18 Volume VI reconstruction (summary)](#vi18-volume-vi-reconstruction-summary)
  - [Recommendations](#recommendations-4)
  - [Caveats](#caveats-5)

---

# VOLUME I — Purpose, Domain & Conceptual Model

## §0 — Subject Header

```
Technology:              Blnk — open-source double-entry financial ledger
Technology type:         LEDGER
Primary repository:      https://github.com/blnkfinance/blnk  (ledger core — the subject)
Client SDK:              https://github.com/blnkfinance/blnk-go (Go client; client interface only)
Version / release:       v0.15.0 (Jun 22, 2026) — latest MAJOR release analysed; patch line runs to v0.15.2 (Jul 31, 2026)
Commit / tag:            tag v0.15.0; repository at 604 commits / 54 releases as observed 11 Aug 2026
Official documentation:  docs.blnkfinance.com (Mintlify); README in repo; changelog at /changelog/blnk-core
Source openness:         OPEN SOURCE — Apache License 2.0 (LICENSE.md), "Blnk Core" edition
Deployment model:        BOTH — self-hosted (bring-your-own PostgreSQL) or managed "Blnk Cloud"
Licence / edition:       Apache-2.0 for Core; open-core split — Cloud dashboard/back-office/monitoring is commercial
Research date:           11 August 2026
Study objective:         BUILD EXTRACTION
Configuration:           EXTENDED 7 (Volume VII Security & Threat Model commissioned — ledger holds balances)
```

**Evidence ceiling statement.** Blnk is open source (Apache-2.0), so this study reaches CONFIRMED IMPLEMENTATION on several material claims by naming files, structs and schema behaviour. Where I relied on official documentation without opening the exact source line, I mark DOCUMENTED BEHAVIOR; where the project asserts something in a blog or README, MAINTAINER CLAIM. The single most important source-level fact — that money is carried as Go `*big.Int` — is CONFIRMED at `transaction.go` (root), which imports `math/big` and declares `transactionWorker` with an `amount *big.Int` parameter; the field-level declarations live in `model/transaction.go` and `model/balance.go`, which I could not open directly and therefore mark SOURCE-CODE INFERENCE where cited. **Version is pinned at v0.15.0 and behaviour is not mixed silently across releases.**

---

## TL;DR
- **Blnk exists to give fintech developers a correctness-first, double-entry ledger as a drop-in service** — the "boring but unforgiving" layer (balances, immutable transactions, reconciliation, identity) that every fintech otherwise hand-rolls in an application database and gets wrong. It is Nigerian in origin (founder Jerry Enebeli, ex-Flutterwave/Eyowo/Bloc), which shows in its assumptions: money movement modelled as source→destination flows, multi-currency and crypto precision as first-class, and PostgreSQL-only so an operator can bring their own database.
- **The problem it holds is: never lose or invent money, and always be able to prove how a balance was reached.** Its defining invariants are conservation (every transaction has a source and a destination that move the same precise integer amount), immutability of posted transactions (no updates/deletes; corrections are new transactions), and idempotency (a unique `reference` per transaction, enforced by a DB unique index since v0.13.2).
- **What it promises never to violate:** posted transactions are never mutated or deleted; balances change only through transactions; amounts are stored as arbitrary-precision integers in minor units (never floats); and a duplicate `reference` never produces a second money movement. For the cooperative-society builder, the money representation and the immutability/idempotency model are strong ADOPT candidates; the "balance is a cached running total updated in place" design and the single-Postgres deployment are ADAPT/REJECT candidates examined below.

---

## Key Findings (ten most important)

1. **Money is an arbitrary-precision integer in minor units, never a float.** `precise_amount` is carried as Go `*big.Int` (CONFIRMED: `transaction.go` imports `math/big`; DOCUMENTED, from Blnk's split-payments blog: "Blnk uses integer amounts with a precision field to avoid floating-point [errors]… precision: 100 means you divide by 100 to get the display amount. 10000 / 100 = $100.00"). A convenience `amount` (float64) is multiplied by a per-transaction `precision` multiplier to derive `precise_amount`. This is the single most consequential and most transferable decision in the system.
2. **`precision` is caller-supplied per transaction, not a property of the currency.** Blnk does not hold a canonical precision per asset; it trusts the caller to pass a consistent `precision` (e.g. 100 for USD, 10^18 for ETH). Balance responses do not even return precision. This is a redefinition trap — an inconsistent precision silently corrupts a balance.
3. **"Balance" in Blnk is a mutable, cached running total, not a derived quantity.** Balances are updated in place through transactions and carry a `version` for optimistic locking. This diverges from the textbook/TigerBeetle model where balance = f(cumulative debits, credits). Blnk keeps `credit_balance` and `debit_balance` alongside a net `balance`, and can *reconstruct* balances from transactions on demand — but the day-to-day balance is a stored mutable field.
4. **Immutability is by convention + DB protections, not a pure append-only log.** Posted transactions "cannot be modified or deleted" (DOCUMENTED), each state transition is a *new* row linked by `parent_transaction`, and v0.10.1 added "database protections to prevent unauthorized changes to transactions and balance snapshots." But the balance row itself is mutated. Immutability therefore applies to the transaction journal, not to balances.
5. **Idempotency hinges entirely on a unique `reference`.** Since v0.13.2 a unique index `idx_transactions_reference_unique` enforces this at the storage layer (DOCUMENTED, breaking change). Before that it was an application-layer check. A duplicate reference is *discarded*, not errored into a second movement.
6. **The inflight (two-phase) transaction is a native primitive.** A transaction with `inflight: true` holds funds (`inflight_debit_balance`) and settles to APPLIED (commit) or VOID. This is Blnk's built-in authorise/settle and escrow mechanism — directly relevant to loans and remittance holds.
7. **The `@`-prefixed internal balance (e.g. `@World`, `@Fees`) is how Blnk represents the outside world and equity/revenue accounts.** These auto-create in the default General Ledger and typically run negative (they are the counter-entry that keeps double-entry balanced). This is Blnk's substitute for a formal chart-of-accounts normality model.
8. **A significant capability was removed in v0.15.0: built-in FX.** The `rate`, `currency_multiplier` and `modification_ref` fields were deleted; "destination credit equals source debit." Blnk retreated from doing currency conversion inside a transaction — a revealing narrowing of scope toward pure value-conservation.
9. **Concurrency correctness rests on Redis distributed locks plus Postgres optimistic locking (`version`).** Under the default queue, transactions serialise per balance; with `skip_queue: true` they take a Redis lock and a versioned DB write. Hot-balance contention is an explicitly acknowledged failure mode.
10. **Blnk is open-core.** Core (ledger, reconciliation, identity, inflight, lineage, hashing) is Apache-2.0 and fully self-hostable on your own Postgres; the commercial line is Blnk Cloud (managed hosting, dashboard, anomaly detection, back-office approvals/monitoring). No ledger correctness feature is paywalled as of v0.15.0.

---

## Details

### I.1 Problem origin

**The problem.** Every fintech product — wallet, neobank, lender, remittance app, savings/contribution scheme — needs an internal source of truth for "who has how much, and how did they get it." Teams routinely build this as a `balances` table in their application database, incrementing and decrementing a number. That approach fails predictably: it loses money to floating-point rounding; double-counts on retries; cannot answer "what was this balance on 3 March"; has no audit trail; and corrupts under concurrency. Blnk's own framing (MAINTAINER CLAIM, Enebeli, "Reimagining Fintech Infrastructure", Mar 5 2025): payments APIs got easy, but ledgers, reconciliation, identity management and compliance "often exist in rigid, legacy systems that are difficult to access, customize, or scale. Developers are forced to either reinvent the wheel or piece together unreliable solutions, slowing down innovation and increasing operational risk." The stated goal is to make a ledger "as simple as signing up for a Stripe API."

**Who experienced it.** Founder Jerry Enebeli spent a decade in African fintech engineering — Backend Engineer at Eyowo (a Nigerian neobank, maintaining banking infrastructure), integration work at Flutterwave (whose own scale, per Y Combinator's company profile, is "close to $20 billion in payments and 100 million transactions across over 33 African countries"), Chief/Head of Product at Bloc (business banking/BaaS), and founder/CEO of Orchestrate (payments orchestration, acquired 2021). Blnk is the generalisation of a ledger he had repeatedly built by hand. (DOCUMENTED, blnkfinance.com/about; LinkedIn.)

**Prior approaches and their inadequacy:**
- *Hand-rolled application-DB ledgers* — fast to start, but no immutability, weak idempotency, float errors, no reconciliation, no history. This is precisely the pain Blnk targets.
- *General-purpose accounting packages (QuickBooks, LedgerSMB, Beancount)* — built for books and reporting at human scale, not high-throughput programmatic money movement via API; no concept of inflight holds, no per-transaction API idempotency.
- *Core-banking systems (Temenos, Finacle, Mambu)* — heavyweight, licensed, closed, hard to customise or self-host; the opposite of "deploy a sandbox in 5 minutes."
- *Other open-source/purpose-built ledgers (TigerBeetle, Formance, Midaz)* — credible, but each makes different tradeoffs (§I.13). At the time Blnk emerged (first release Mar 2024) none combined "single-binary-ish, Postgres-backed, REST-first, batteries-included (reconciliation + identity)" for the developer-first African fintech audience.

**The African/Nigerian context (why a Lagos ledger differs from a Valley one):**
- **Multi-currency and crypto are not edge cases.** Nigerian fintech routinely spans NGN, USD and stablecoins; Blnk treats per-asset precision (including 10^18 for ETH) as first-class rather than assuming two decimal places.
- **High inflation and large nominal values** make >15-digit amounts real, motivating the arbitrary-precision `precise_amount` (added v0.10.1) — a Valley ledger assuming int64 cents would overflow.
- **Bring-your-own-infrastructure and cost sensitivity.** Postgres + Redis + Docker Compose on modest hardware, self-hosted, "100% control on your data" — important where managed-cloud spend and data-residency/regulatory control matter.
- **Reconciliation against many external providers** (agency banking, multiple PSPs across countries) is a headline module, not an afterthought — reflecting the fragmented rails Enebeli integrated across his career at Flutterwave/Orchestrate.

### I.2 Historical evolution (with causes)

Release history is CONFIRMED from the official changelog (`/changelog/blnk-core`) and GitHub releases. Cause attributions are the technical pressure evidenced by the changelog text; where inferred they are marked HYPOTHESIS.

- **v0.5.0 — First release (Mar 25, 2024).** Ledgers, ledger balances, transactions, identities, balance monitoring, General Ledger (chart of accounts), refunds, scheduling. Establishes the core object model.
- **v0.6.0 (Apr 8, 2024).** *Inflight transactions*, *multiple sources/destinations*, *overdrafts*, enhanced concurrency control. Cause: real money flows are two-phase (authorise/settle) and split (fees); wallets need holds — the application-DB model could not.
- **v0.6.1 (Apr 12, 2024).** `precision` becomes a **transaction parameter**; search added; partial inflight commits. Cause: correct per-asset decimal handling; "convert naira to kobo."
- **v0.6.2 (May 3, 2024).** *Rates* (FX between currencies); `inflight_expiry_date`. (Later reversed — see §I.3.)
- **v0.7.0 (Sep 9, 2024).** *Reconciliation* module; `parent_transaction` introduced to link derived transaction states. Cause: audit/traceability and matching external records; the immutable model needs a lineage pointer instead of updates.
- **v0.8.x (Jan–Feb 2025).** `skip_queue` direct processing (0.8.2); configurable insufficient-funds retries and **queued balances** (0.8.3); **balance snapshots & historical balances** (0.8.4); **PII tokenization** (0.8.8). Cause: latency control, point-in-time reporting, and compliance (PII scope reduction).
- **v0.9.0 (Mar 3, 2025).** *Bulk transactions* (atomic or independent) and *backdated transactions* (`effective_date`). Cause: migrations from legacy systems and batch payouts (payroll) need backdating and all-or-nothing batches.
- **v0.10.1 (Mar 22, 2025).** **`precise_amount`** (amounts >15 digits); *granular API keys* (scopes); *overdraft limits*; balance reconstruction; instant reconciliation; DB protections against unauthorized transaction/snapshot changes. Cause: float/precision ceiling and multi-tenant authorisation.
- **v0.11.0 (Aug 27, 2025).** Metadata search; insufficient-balance checks now include inflight. Breaking (Typesense).
- **v0.12.0 (Dec 8, 2025).** **API keys hashed with SHA-256** at rest (breaking). Cause: security hardening.
- **v0.13.0 (Jan 29, 2026).** **Lineage** — fund-source tracking with FIFO/LIFO/proportional debit allocation; webhook HMAC signing. Cause: traceability of *which* funds left a balance.
- **v0.13.2 (Feb 12, 2026).** **Unique DB index on `transactions.reference`** (breaking; upgrade fails on duplicates); DB-level filter search. Cause: harden idempotency at storage, not just application.
- **v0.14.0 (Apr 9, 2026).** Performance release — internal benchmark throughput improved "up to about 5×" under heavy contention (MAINTAINER CLAIM with stated conditions; not independently MEASURED).
- **v0.15.0 (Jun 22–23, 2026).** **Structured API errors (`error_detail.code`)**; **removal of `rate`/`currency_multiplier`/`modification_ref`**; queued inflight commit/void by default; **optional global hash chain** with `blnk verify-chain`. Current major release under study.
- **v0.15.1/0.15.2 (Jul 2026).** Fixes; queue/Typesense memory backpressure (503 `QUEUE_BACKPRESSURE`).

Architectural turning points: (a) shift from application-checked to DB-enforced idempotency (0.13.2); (b) `parent_transaction` lineage (0.7.0) as the backbone of an immutable multi-state model; (c) narrowing away from in-ledger FX (0.15.0).

### I.3 The removal record

- **Built-in FX / `rate` (added v0.6.2 → removed v0.15.0).** For roughly two years a transaction could carry a `rate` to convert between currencies of different balances, plus `currency_multiplier`. In v0.15.0 these were removed: "Request `rate` no longer applies an exchange rate; destination credit equals source debit." **What it reveals:** Blnk chose to make *strict value conservation* (debit amount == credit amount) an inviolable core invariant, and pushed FX out to the caller. A ledger that silently changes the amount between source and destination cannot guarantee conservation; removing FX is the project settling firmly on the conservation invariant as identity. The most informative removal in the record.
- **`modification_ref` (removed v0.15.0).** A field associated with balance/transaction modification bookkeeping. Its removal reinforces the "transactions are not modified" stance — the concept of a modification reference is inconsistent with pure immutability.
- **Synchronous-by-default bulk and inflight commit/void (changed 0.10.5, 0.15.0).** Bulk (0.10.5) and inflight commit/void (0.15.0) moved to queue-by-default; the previous synchronous behaviour is now opt-in via `skip_queue`. **Reveals:** the project settled on asynchronous, queue-serialised processing as the correctness-preserving default under concurrency, treating synchronous processing as the exceptional (low-contention) case.
- **Plaintext/return-on-list API keys (changed 0.12.0).** Keys are no longer retrievable after creation; only a SHA-256 hash is stored. A deliberate withdrawal of convenience for a security guarantee.

### I.4 Actors and users

| Actor | Goal | Trust level | Inputs | Outputs | Failure impact |
|---|---|---|---|---|---|
| **Calling application/service** (fintech backend) | Record money movement, read balances | High — holds API key | REST/SDK calls | Ledger state, webhooks | Incorrect calls → wrong balances; must supply correct `precision`/`reference` |
| **End user (customer)** | Indirect — their wallet is a balance | None (never talks to Blnk directly) | — | — | Sees wrong balance if caller errs |
| **Operator/administrator** | Deploy, configure, back up, scale | Highest — controls Postgres/Redis/config | `blnk.json`, env, `verify-chain` | Running service | DB access = full mutation power (Vol VII) |
| **API key holder (scoped)** | Least-privilege access (e.g. `transactions:write`) | Medium; scopes since v0.10.1; owner-scoped since v0.14.3 | Scoped API calls | — | Over-broad scope = authz breach |
| **External systems (PSPs, banks)** | Provide statements for reconciliation | None | CSV/records uploaded by operator | Match results | Bad data → false mismatches |
| **Maintainers (Blnk Finance LLC)** | Evolve Core; run Cloud | — | Commits, releases | Releases, docs | Breaking changes (several — §I.2) |
| **Blnk Cloud (managed)** | Dashboard, monitoring, back-office | Connects via read "Query Agent" to your Core | Queries | Insights, approvals | Commercial dependency if adopted |

No plugin architecture in Core; extension is by wrapping the REST API in your own services (Watch, a separate DSL repo, handles monitoring rules).

### I.5 Jobs to be done

- **Core jobs (ledger correctness):** create ledgers; create balances; record double-entry transactions (source→destination); maintain running balances (net, credit, debit, inflight, queued); enforce idempotency; immutable transaction journal with lineage.
- **Transaction workflows:** inflight (two-phase) holds with commit/void/partial-commit/expiry; multiple sources/destinations (splits); bulk (atomic or independent); scheduled; backdated (`effective_date`); refunds (idempotent since 0.10.3); overdrafts with `overdraft_limit`.
- **Convenience/reporting:** balance monitors/alerts; balance snapshots & historical balances (point-in-time); queued balances; search (Typesense or direct-DB filter); metadata on any object.
- **Integrations:** reconciliation (batch + instant; matching rules; 1:1/1:many/many:1 strategies); identity management + PII tokenization; webhooks (HMAC-signed since 0.13.0); lineage/fund-source tracking.
- **Administration/ops:** API keys with scopes; health checks; queue monitoring port; Kubernetes manifests; telemetry; optional hash chain + `verify-chain`.
- **Commercial (open-core boundary):** Blnk Cloud — managed hosting, back-office dashboard (create/edit/approve/void from UI), anomaly detection, analytics, team collaboration. **Everything ledger-correctness-related sits on the open (Apache-2.0) side; the paid side is operational convenience and monitoring, not ledger semantics.**

### I.6 Domain glossary (industry-standard vs Blnk-specific; redefinitions flagged)

- **Ledger** — a grouping/namespace for balances (like a "book"). *Blnk-specific usage:* an organisational container, not the classical "book of final entry." A default **General Ledger** is created at install for internal `@` balances. ⚠️ Redefinition-lite: closer to "a partition/tenant."
- **Balance** — a store of value (wallet/account). ⚠️ **Major redefinition:** in Blnk a "balance" is a *stored, mutable, versioned object* with six sub-fields (`balance`, `credit_balance`, `debit_balance`, `inflight_balance`, `inflight_credit_balance`, `inflight_debit_balance`), not a value *derived* from entries. Textbook "balance" = credits − debits computed on demand; Blnk's `balance` is a cached running total (though it can be reconstructed).
- **Account** — Blnk uses **balance** as the primary noun; "account" appears in an SDK helper (`account.go`) and colloquially. Not the primary abstraction.
- **Transaction** — a single money movement from a `source` to a `destination`. ⚠️ Redefinition: classical double-entry treats a "transaction" as a set of balanced journal lines (n debits, n credits); in Blnk it is fundamentally a *one-source-one-destination transfer* (splits fan out into child transactions linked by `parent_transaction`).
- **Entry** — Blnk exposes no separate "journal entry / posting line" object; the debit and credit are implicit in `source`/`destination` and recorded as increments to `credit_balance`/`debit_balance`.
- **Source / Destination** — the balance money leaves / the balance money enters. Both mandatory; a transaction missing either is rejected. *Blnk's engineer-friendly renaming of debit/credit* (compare Formance, which explicitly frames sources/destinations as the engineer's analog of credit/debit).
- **Reference** — a caller-supplied unique string; the idempotency key.
- **Precision** — an integer multiplier (e.g. 100) applied to `amount` to produce integer `precise_amount`. ⚠️ Redefinition: not "number of decimal places" but "the factor mapping display units to minor units"; per-transaction and caller-owned. Blnk docs: "Use the same precision you pass on transactions for each currency (for example, 100 for USD) to convert integers to display amounts: display_amount = balance / precision."
- **Precise amount (`precise_amount`)** — the amount in smallest indivisible units, stored as an arbitrary-precision integer.
- **Inflight** — a held/pending transaction (two-phase). Blnk-specific term for authorise-then-settle.
- **Indicator** — a human-readable alias for an internal balance (e.g. `@World`), auto-registered in the General Ledger when prefixed with `@`.
- **Identity** — a customer/organisation record (with optional PII tokenization) linkable to balances/transactions.
- **Reconciliation** — matching external records to internal transactions via rules/strategies. First-class module.
- **Lineage** — fund-source tracking; which credits funded a later debit, with FIFO/LIFO/proportional allocation (v0.13.0).
- **Version** — a per-balance integer for optimistic concurrency control.
- **Hash** — SHA-256 digest of a transaction's fields; optional global **hash chain** links transactions to detect tampering.
- **Queued balance** — estimated cumulative effect of not-yet-processed queued transactions (`queued_credit_balance`/`queued_debit_balance`); explicitly labelled an estimate.

### I.7 Core abstractions (domain model)

**Ledger** — identity `ldg_<uuid>`; attributes: name, metadata, created_at. Lifecycle: created (default General Ledger auto-created); renamable (0.11.1) without affecting balances; no delete of core ledger. Owns balances. Persistent.

**Balance** — identity `bln_<uuid>`; attributes: the six balance fields (all integers in minor units), `currency`, `ledger_id`, optional `identity_id`, optional `indicator` (for `@` internal balances), `version`, metadata, created_at. ⚠️ Mutability: **mutable in place** (only via transactions; never set directly); starts at 0; cannot be created with a preset amount. Optimistically locked via `version`. Multi-currency: one balance = one currency; multi-currency is multiple balances. Constraint (0.10.5): no duplicate balance with the same indicator+currency.

**Transaction** — identity `txn_<uuid>`; attributes: `amount` (float64, convenience), `precise_amount` (`*big.Int`), `precision` (int64), `currency`, `source`, `destination`, `reference` (unique), `description`, `status`, `hash`, `allow_overdraft`, `overdraft_limit`, `inflight`, `inflight_expiry_date`, `inflight_commit_date`, `scheduled_for`, `effective_date`, `parent_transaction`, metadata, created_at. Lifecycle: QUEUED → {INFLIGHT → {APPLIED|VOID}} | APPLIED | REJECTED. ⚠️ **Immutable once posted**; each state change is a *new* row linked by `parent_transaction`. Money type CONFIRMED as `*big.Int` at `transaction.go`.

**Identity** — `idt_<uuid>`; person/organisation, optional PII tokenization; links to balances/transactions. Deterministic creation supported (0.14.2). Deletable (0.15.0).

**Internal balance** (`@Name`) — a balance owned by the operator's organisation representing the outside world / equity / revenue / fees; auto-created in General Ledger on first `@`-reference. Typically runs negative under overdraft. The counter-entry mechanism.

**Reconciliation, Lineage allocation, Balance snapshot, Balance monitor, API key, Webhook** — supporting abstractions (files `reconciliation.go`, `lineage*.go`, `apikey.go`, `webhooks.go`, `balance_test.go` etc.).

**Money representation (the decision everything rests on).** Numeric model: integer minor units. Wire/compute type: Go `*big.Int` for `precise_amount` and for balance fields (SOURCE-CODE INFERENCE for the balance struct; CONFIRMED that `transaction.go` uses `math/big` and passes `amount *big.Int`). Convenience `amount` is float64 and is *derived*, not authoritative. Precision: caller-supplied per transaction; **balances do not return precision** (docs: "Balance fields are integers in minor units… Blnk Core does not return precision on balance responses… `display_amount = balance / precision`"). Multi-currency: independent per-balance; **no automatic FX** since v0.15.0 (destination credit == source debit). Postgres storage type not opened directly; the >15-digit requirement and `*big.Int` usage make `NUMERIC` the strongly-favoured inference *(superseded on assembly: after four attempts across four volumes, Volume V declared the money column type **permanently UNKNOWN** for this study. The NUMERIC lean remains the best inference but must not be treated as established. See Appendix E note 2)* (ANALYTICAL INFERENCE; not confirmed from DDL).

### I.8 THE INVARIANT CATALOGUE

Numbered; each with claimed enforcement point and evidence class. Volumes II–III will locate and verify each.

- **INV-1 — Conservation (source and destination move the same precise amount).** Every transaction has a `source` and a `destination`; the amount debited equals the amount credited. Claimed enforcement: transaction validation (a transaction missing source or destination is *rejected*); reinforced by v0.15.0 removal of `rate` so "destination credit equals source debit." Class: DOCUMENTED BEHAVIOR + FX removal CONFIRMED via changelog. (This is per-transfer equality; NOT a periodic trial-balance across all accounts — see falsification test.)
- **INV-2 — Balances change only through transactions.** "Balance amounts are immutable and can only be updated through transactions. You cannot manually set or alter a balance amount directly." Enforcement: API surface + DB protections (0.10.1). Class: DOCUMENTED BEHAVIOR.
- **INV-3 — Balance derivability / reconstructability.** A balance can be recomputed from its transaction history (`from_source=true`; `BLNK_RUN_RECONCILIATION`). Enforcement: balance reconstruction feature (0.10.1). Class: DOCUMENTED BEHAVIOR. ⚠️ The day-to-day balance is a cached total; derivability is a recovery path, not the primary read.
- **INV-4 — Idempotency / reference uniqueness.** A given `reference` yields exactly one money movement; duplicates are discarded. Enforcement: **unique DB index `idx_transactions_reference_unique`** (v0.13.2) — storage-level; previously application-level. Class: DOCUMENTED BEHAVIOR (index named in changelog → strong CONFIRMED-adjacent).
- **INV-5 — Immutability of posted transactions.** Once QUEUED/APPLIED/committed/voided, a transaction row is not modified or deleted; new states are new rows via `parent_transaction`; status cannot roll back. Enforcement: application + DB protections; lineage pointer. Class: DOCUMENTED BEHAVIOR.
- **INV-6 — Valid state transitions.** Allowed: QUEUED→{INFLIGHT,APPLIED,REJECTED}; INFLIGHT→{APPLIED,VOID}; no reverse transitions. Enforcement: transaction lifecycle engine (`transaction_inflight.go`, `transaction_execution.go`). Class: DOCUMENTED BEHAVIOR.
- **INV-7 — Precision integrity (amounts are integers in minor units).** No float storage; `precise_amount` integer; non-integer precision rejected (0.11.3: "rejects transactions with non-integer precision values"). Enforcement: validation + `*big.Int` type. Class: CONFIRMED (type) + DOCUMENTED (rejection).
- **INV-8 — Sufficient funds unless overdraft permitted.** `available = balance − inflight_debit_balance (− queued_debit)`; if amount exceeds available and `allow_overdraft` is false → REJECTED; with overdraft, cannot exceed `overdraft_limit`. Enforcement: pre-processing balance check (v0.11.0 includes inflight). Class: DOCUMENTED BEHAVIOR.
- **INV-9 — Concurrency safety (no lost updates on a balance).** Per-balance serialisation via Redis distributed lock (skip_queue) and Postgres optimistic locking on `version`; queue path serialises. Enforcement: `queue.go`, Redis lock, versioned write. Class: DOCUMENTED BEHAVIOR + MAINTAINER CLAIM (hot-balances blog).
- **INV-10 — Zero-amount and malformed transactions are not recorded.** Zero-amount transactions are discarded; malformed requests rejected. Enforcement: validation. Class: DOCUMENTED BEHAVIOR.
- **INV-11 — Tamper-evidence (optional).** SHA-256 per-transaction hash; optional global hash chain verified by `blnk verify-chain`. Enforcement: hashing subsystem (opt-in, off by default). Class: DOCUMENTED BEHAVIOR. ⚠️ Off by default → not an active guarantee unless enabled.
- **INV-12 — Authorisation/tenancy (scoped keys).** API keys carry scopes (0.10.1), are owner-bound (0.14.3), and hashed at rest (0.12.0). Enforcement: API key middleware. Class: DOCUMENTED BEHAVIOR. ⚠️ No built-in multi-tenant isolation *between ledgers* beyond key scoping — an operator concern for Vol VII.

An invariant nobody can point to is a HYPOTHESIS: **a global "sum of all balances == 0" trial-balance invariant is NOT enforced by Blnk** — conservation is guaranteed per-transfer (INV-1), and because internal `@World`-type balances absorb the counter-entry, the *system* can be made to sum to zero by convention, but Blnk does not enforce a global zero-sum. Flagged as the primary falsification target (§I.14).

### I.9 Semantics (Blnk meaning vs ordinary meaning)

- **Creation** — POST creates ledger/balance/identity/transaction. A balance is always created at 0 (cannot preset). ⚠️ differs from DB "insert with values."
- **Update** — ledgers can be renamed; metadata can be added to any object; **balances and transactions' financial fields cannot be updated**. "Update" in Blnk means metadata/label, never money.
- **Deletion** — identities and balance monitors can be deleted; **transactions cannot be deleted**; balances are not deletable. ⚠️ Accounting-correct: you never delete a posting.
- **Commit** — settle an INFLIGHT transaction to APPLIED (full or partial); idempotent by transaction_id. Queued by default since 0.15.0.
- **Rollback** — ⚠️ **not a ledger operation.** Statuses cannot roll back. "Rollback" exists only at the internal DB-transaction level. A user-level reversal is a *new* transaction.
- **Void** — cancel an INFLIGHT transaction, releasing held funds (INFLIGHT→VOID). Only inflight can be voided; an APPLIED transaction cannot be voided — you refund/reverse instead.
- **Application (APPLIED)** — funds actually moved and balances updated.
- **Reversal / correction** — ⚠️ **a new transaction**, not an edit. A refund is "a new transaction… needs its own reference" (idempotent since 0.10.3; cannot refund twice). Corrections/backdating use `effective_date`. This is the sharpest accounting-vs-database divergence and the key one for the builder: **you never mutate history; you post a compensating entry.**
- **Version** — optimistic-lock counter on a balance, incremented on each applied change; not a semantic "document version."
- **Timestamp** — `created_at` (system time) vs `effective_date` (financial date, may be backdated; defaults to created_at). ⚠️ Two distinct time axes — a real redefinition trap.
- **Equality / identity** — objects identified by prefixed UUIDs (`txn_`, `bln_`, `ldg_`, `idt_`); a transaction's *idempotent identity* is the `reference`.
- **Ordering** — the `parent_transaction` chain defines lineage order; the queue defines processing order; `effective_date` defines financial order (which can differ from insertion order).
- **Finality** — APPLIED and VOID are terminal; no un-apply. Finality is by forward-only compensating entries.
- **Error** — since v0.15.0 structured `error_detail.code` (e.g. `TXN_NOT_FOUND`, `QUEUE_BACKPRESSURE`); duplicate reference / zero amount → *discarded* (not necessarily an error to the caller); insufficient funds → REJECTED status + webhook.

### I.10 Assumptions (what Blnk assumes the surrounding system provides)

- **Callers supply a correct, consistent `precision` per currency.** Blnk holds no canonical asset precision; an inconsistent precision corrupts balances silently. (Docs warn to "use the highest precision value for all transactions.")
- **Callers supply a unique `reference` per intended movement** and reuse it on retries — the entire idempotency guarantee is delegated to caller discipline (backed by the DB unique index).
- **Callers implement FX themselves** (post-v0.15.0) and record conversions as separate movements/legs.
- **PostgreSQL is available, durable and the source of truth**; the operator brings and secures it. Redis is available for queue + distributed locks.
- **Typesense is available if Typesense search is used** (else direct-DB filter).
- **Clocks are reasonable**; `effective_date` correctness is the caller's responsibility; system uses server time for `created_at`.
- **Concurrency is bounded per balance**; hot balances are the caller's design problem (queue vs skip_queue, coalescing).
- **The caller owns authorisation of *end users*** — Blnk authenticates the *service* (API keys), not customers.
- **Workload is transaction-heavy but each transaction is small**; large fan-outs use bulk/multiple-destinations with caps (10,000 items per bulk request in 0.15.0).

### I.11 Explicit non-goals

- **Not a currency-conversion engine** (explicitly removed FX in v0.15.0). Documented by removal.
- **Not a payments processor / bank connector.** Per the Oncely product listing: "While it doesn't include pre-built payment or bank integrations, its flexible infrastructure enables custom integrations for diverse services, from payment processors to banking systems." You bring the rails.
- **Not a customer-facing auth/identity provider** — identities are records, not a login system.
- **Not a general accounting/reporting suite** (no P&L, tax, GAAP statements out of the box; the General Ledger is a chart-of-accounts container, not a reporting engine).
- **Not a multi-tenant SaaS boundary by itself** — isolation between customers is achieved by ledger partitioning + your own key management (compare TigerBeetle's "ledger per customer" pattern; Blnk expects the same discipline).
- **Not a distributed/HA database** — correctness rests on a single Postgres as source of truth; HA is an operator concern.

Mostly these are *inferred from removals and third-party statements*; Blnk documents them implicitly rather than as a formal "non-goals" list. That itself is a finding: the non-goals must be inferred, so a builder can be misled into expecting FX or bank integrations.

### I.12 Standards and theory

- **Double-entry bookkeeping** — the foundational model. Blnk implements the *reciprocal value movement* core (every transaction = value out of source + value into destination) but **renames debit/credit to source/destination** and does not expose the classical five-account-type/normality model (assets/liabilities/equity/income/expense with debit- or credit-normal behaviour). Compare Formance's explicit formal model (position in chart of accounts + normality + list of debits/credits). Blnk's simplification: normality is emulated by convention using internal `@` balances and overdraft, not by a typed account model.
- **Minor-units integer money (ISO 4217 spirit; crypto satoshi/wei model)** — Blnk follows the industry best practice of integer smallest-units, extended to arbitrary precision via `*big.Int` for crypto-scale magnitudes. Standard, correctly applied.
- **Idempotency keys (Stripe-style)** — the `reference` is a classic idempotency key, now DB-enforced.
- **Two-phase authorise/settle** — inflight mirrors card auth→settlement and escrow; conceptually a hold, not distributed 2PC.
- **Cryptographic hash chaining (SHA-256)** — optional tamper-evidence, borrowing the blockchain "each record commits to prior state" idea, but centralised and opt-in — not a consensus ledger.
- **Deviation to note:** Blnk claims "double-entry" but a builder assuming a *balanced multi-line journal with enforced global trial balance* will be surprised: Blnk enforces per-transfer conservation, not a global debits==credits trial balance across a chart of accounts. This is the deviation most likely to mislead.

### I.13 Competing conceptual models

- **TigerBeetle.** Purpose-built financial DB; accounts + transfers are built-in primitives; amounts are unsigned **128-bit integers** (per its docs: "To maximize precision and efficiency, Account debits/credits and Transfer amounts are unsigned 128-bit integers… map the smallest useful unit of the fractional currency to 1"; its 2023 engineering blog notes they "decided to use 128-bit integers to store all financial amounts and balances, retiring our previous use of 64-bit integers"); accounting rules enforced *in the database* via flags (`debits_must_not_exceed_credits`, `credits_must_not_exceed_debits`, balancing transfers); tracks cumulative posted debits/credits and leaves net balance to the app; ledger-per-asset, transfers only within a ledger. *Buys:* extreme throughput, correctness enforced at the DB, no float. *Costs:* opinionated, no metadata/reconciliation/identity, you build the surrounding service; not REST; harder to query. Blnk trades TigerBeetle's raw speed and in-DB enforcement for developer ergonomics, Postgres familiarity, and batteries-included modules.
- **Formance Ledger.** Programmable, source-available; a DSL (Numscript) to express multi-posting flows; explicit formal double-entry model (normality, chart position). *Buys:* expressive, auditable flows; rigorous model. *Costs:* steeper concept load; DSL to learn. Blnk is more CRUD/REST-simple; Formance is more formally accounting-correct.
- **Midaz (Lerian).** Source-available, cloud-native **microservices** (Onboarding + Transaction services), multi-asset/multi-currency, **n:n transactions**, organisations→ledgers→portfolios→segments→accounts hierarchy, accounting/operation "routes." *Buys:* enterprise hierarchy, n:n richness, plugin ecosystem. *Costs:* heavier to run (microservices) than Blnk's Postgres+Redis. Blnk is simpler/flatter; Midaz is more enterprise-core-banking-shaped — notably *closer* to the cooperative-society platform's eventual shape, and worth the builder's attention as an alternative.
- **Hand-rolled application-DB ledger.** *Buys:* zero new infra, full control. *Costs:* re-implements every invariant badly; this is exactly what Blnk replaces. REJECT for anything holding real member savings.
- **Traditional core-banking ledger (Mambu/Temenos/Finacle).** *Buys:* regulatory features, product engines (loans/deposits) out of the box. *Costs:* cost, closed, slow to change, not founder-ownable. The builder's *destination* is core-banking-shaped, but adopting a closed core violates the "permanently founder-owned" constraint.
- **Event-sourced ledger.** Money as an append-only event log; balances are pure projections. *Buys:* perfect auditability, replay, temporal queries by construction. *Costs:* projection complexity, eventual-consistency reasoning. **Blnk is a hybrid:** immutable transaction journal (event-log-like) + a mutable cached balance projection with optimistic locking — pragmatic, not purely event-sourced.

### I.14 Falsification test

The domain model asserted here — *money as arbitrary-precision integer minor-units; balance as a mutable cached projection reconstructable from an immutable, reference-idempotent, source→destination transaction journal; conservation enforced per-transfer* — would be **proven wrong** if Volumes II–IV find any of:

1. **A code path that stores or arithmetic-processes authoritative money as float64** (not merely the convenience `amount`), i.e. balances or `precise_amount` computed in floating point. Falsifies INV-7 and the money model.
2. **A mutation of a posted transaction row's financial fields** (an UPDATE on amount/source/destination/status that overwrites rather than inserting a new `parent_transaction`-linked row). Falsifies INV-5.
3. **A second money movement produced from a duplicate `reference`** under concurrency (idempotency bypass). Falsifies INV-4.
4. **A transaction whose destination credit differs from its source debit** in v0.15.0+ (surviving FX or asymmetric posting). Falsifies INV-1 (conservation).
5. **A balance write that loses an update under concurrency** despite `version`/lock (a real lost-update on a hot balance). Falsifies INV-9.
6. **Evidence that Blnk enforces a global trial-balance (sum of all balances == 0)** — if found, my claim that conservation is *only* per-transfer is wrong (the more interesting and likely-correct finding is that it does NOT).

Volumes II onward are directed to look specifically for (1), (2) and (4) in `transaction_execution.go`, `transaction_inflight.go`, `balance.go`, and the SQL migrations.

### I.15 Preliminary build-extraction verdicts (ADOPT / ADAPT / REJECT)

Applying the environment question (did it work because of the mechanism, or the environment around it?):

- **Money as `*big.Int` minor-units + integer storage — ADOPT (unconditionally).** Mechanism-intrinsic; independent of Blnk's team/scale. For a Nigerian cooperative platform spanning NGN and possibly USD/stablecoins, arbitrary-precision integers are exactly right. Transferable verbatim.
- **Immutable transaction journal + compensating-entry corrections (no edits/deletes) — ADOPT.** Mechanism-intrinsic and audit-mandatory for member savings/loans. Adopt the "never mutate history; post a reversal" discipline regardless of ledger chosen.
- **Idempotency via unique `reference`, DB-enforced — ADOPT.** Cheap, mechanism-intrinsic, prevents the classic double-credit bug on retries — critical for mobile-money-style unreliable networks in the target market.
- **Inflight two-phase transactions — ADOPT (adapt naming).** Directly models loan disbursement holds, contribution collections pending clearance, and remittance holds. Mechanism-intrinsic.
- **`precision` as a per-transaction, caller-supplied value — ADAPT (change to per-asset canonical precision).** This worked for Blnk because its callers are disciplined developer teams (the *environment*). For a founder-owned core-banking platform with many internal services and cooperative admins, per-transaction precision is a footgun. **Change to:** a currency/asset registry that fixes precision per asset and rejects mismatches — do not inherit the "trust the caller each time" model.
- **Balance as a mutable cached running total — ADAPT.** It works at Blnk's scale with Redis+optimistic locking, but that is partly an *environmental* crutch (their queue/lock infra). For a founder-owned system, keep the cached balance for reads but treat the immutable journal as the sole source of truth and reconcile/reconstruct on a schedule; consider event-sourced projection if audit rigor dominates.
- **Single-PostgreSQL-as-source-of-truth deployment — ADAPT.** Fine to start; but member-savings durability/HA obligations mean you must add replication/backup/DR that Blnk leaves to the operator. Don't inherit the assumption uncritically.
- **In-ledger FX — REJECT (follow Blnk's own removal).** Do not put currency conversion inside a transfer; record conversions as explicit paired movements. Blnk's removal is a lesson learned; adopt the lesson, not the removed feature. A REJECT here is as valuable as an ADOPT.
- **Optional/off-by-default hash chain — ADAPT (turn it on, or design equivalent).** For a system holding member balances, tamper-evidence should be on and monitored, not opt-in.
- **Blnk Cloud (commercial) — REJECT for the core dependency.** The "permanently founder-owned, vendor model" constraint forbids a hard dependency on a third-party managed plane; build your own back-office. Core (Apache-2.0) is compatible with founder ownership; Cloud is not.

### I.16 Volume I reconstruction (synthesis)

**Core abstraction diagram (textual):** Ledger 1—* Balance *—* Transaction (source, destination); Identity *—* Balance; Internal `@`-balance ⊂ Balance in General Ledger; Transaction —parent_transaction→ Transaction (lineage tree). The numbered invariant catalogue (INV-1…INV-12, §I.8) is the spine Volumes II–III will locate and verify.

**Key unknowns:** exact Postgres column types for money (NUMERIC inferred, not confirmed from DDL); exact `model/transaction.go`/`model/balance.go` field declarations; whether any internal path uses float arithmetic on authoritative money; precise semantics of lineage allocation under partial commits; behaviour of the hash chain across backdated inserts; whether a global trial-balance is enforced anywhere (believed not).

**What is Blnk fundamentally?** A correctness-first, Postgres-backed, REST-first double-entry *transfer ledger* — an immutable journal of source→destination money movements with cached, reconstructable balances — packaged so a developer can adopt it without hand-rolling money infrastructure.

**Single most important abstraction:** the **Transaction as an immutable source→destination transfer** (with the `@`-internal-balance as its indispensable counter-entry).

**Invariant that most defines correctness:** **INV-1 conservation** (destination credit == source debit), hardened by the v0.15.0 FX removal — closely coupled with INV-4 idempotency and INV-5 immutability.

**Assumption whose removal would most change the design:** that **the caller supplies correct, consistent per-transaction `precision`** — if Blnk instead owned canonical per-asset precision, the money model and much validation would change shape (and be safer).

**What the project tried and removed, and what it reveals:** it built in-transaction **FX (`rate`)** and then removed it (v0.15.0), revealing that the project ultimately privileged *strict value conservation* over convenience — the clearest signal of what Blnk refuses to violate.

**Deepest conceptual tradeoff:** **cached mutable balance vs pure derived balance.** Blnk keeps a mutable, versioned running balance (fast reads, needs locks/queue for correctness) *and* an immutable journal it can replay — a pragmatic hybrid that buys performance and simplicity at the cost of a second source of truth that must be kept reconciled. For a builder holding members' savings, deciding where to sit on this axis is the central design choice this volume surfaces.

---

## Recommendations

1. **Adopt now, verbatim:** the integer/`*big.Int` minor-units money model; the immutable-journal + compensating-entry correction discipline; DB-enforced idempotency via a unique reference; and inflight two-phase transactions. These are mechanism-intrinsic and directly fit cooperative savings/contributions/loans.
2. **Adapt before adopting:** replace per-transaction caller-supplied `precision` with a **canonical per-asset precision registry** that rejects mismatches; treat the immutable journal (not the cached balance) as the sole source of truth and run scheduled reconstruction/reconciliation; and add replication/backup/DR around Postgres (Blnk assumes you will).
3. **Reject:** in-transaction FX (record conversions as explicit paired movements — follow Blnk's own removal); and any hard dependency on Blnk Cloud (incompatible with permanent founder ownership — build your own back-office on Core, Apache-2.0).
4. **Turn on tamper-evidence** (hash chain) from day one rather than leaving it opt-in.
5. **Benchmarks/thresholds that would change these recommendations:** if Volume III finds a lost-update on hot balances despite `version`/locks (INV-9 fails) → do not inherit the cached-balance design; move to event-sourced projections. If Volume II finds authoritative money handled as float (INV-7 fails) → do not reuse Blnk's arithmetic paths. If member-count/throughput projections exceed what a single Postgres can serve with headroom (sustained hot-balance contention on pooled contribution accounts) → evaluate TigerBeetle for the hot core with Blnk/your-own for metadata. If regulatory audit demands an enforced global trial balance, add that invariant explicitly — Blnk will not give it to you.

## Caveats

- Several claims here are **DOCUMENTED BEHAVIOR** from official docs/changelog, not opened line-by-line in source; the money type is CONFIRMED via `transaction.go`'s `math/big`/`*big.Int` usage, but the exact `model/*.go` field declarations and the Postgres DDL column types were **not** directly read and are marked SOURCE-CODE/ANALYTICAL INFERENCE (NUMERIC for money columns is inferred, not confirmed).
- The "up to about 5×" throughput improvement (v0.14.0) is a **MAINTAINER CLAIM with stated conditions**, not an independently reproduced MEASURED RESULT; the reconciliation "over 95% accuracy" figure is third-party marketing (Oncely product listing: "significantly reducing manual work and achieving over 95% accuracy") and should not be treated as a benchmark.
- Behaviour is pinned to **v0.15.0**; earlier releases differ materially (FX existed pre-0.15.0; idempotency was application-level pre-0.13.2; precise_amount arrived at 0.10.1). Do not mix.
- Testimonial and website copy (blnkfinance.com) are promotional; treated as MAINTAINER CLAIM throughout.
- This is Volume I (domain model only). Component location (Vol II), runtime invariant verification (Vol III), and the security/threat model (Vol VII) are out of scope here and are where several of the above INFERENCE-class claims will be confirmed or falsified.

---

*End of TREF Volume I — Blnk. Volume II (component location) is NOT begun, per scope.*

---

# VOLUME II — Architecture & Component Anatomy

## TL;DR

- **Blnk is a modular monolith compiled to a single Go binary that runs as two-to-three process roles (API server, worker, one-shot migration) over one shared PostgreSQL source of truth, with Redis (via the `hibiken/asynq` library) owning both the transaction queue and the distributed locks, and Typesense as an optional search projection.** PostgreSQL is the architectural centre of gravity and the single component that is genuinely hard to replace; Redis is on the correctness path (not a cache) because it holds the locks that serialise balance mutation.
- **The confirmed structural facts close most of Volume I's gaps: money moves through `model.Transaction` (fields `PreciseAmount`, `Amount float64`, `Precision float64`) and balances are cached running totals in `model.Balance` with an optimistic-lock `Version` field. But the single most important schema fact — the PostgreSQL column type for `precise_amount` and the balance fields — could NOT be confirmed even with a targeted attempt**, because the repository's `sql/` directory (embedded via `embed.FS` as `SQLFiles` in `blnk.go`) is served only through GitHub tree/raw endpoints that block automated access. Best inference remains NUMERIC (arbitrary precision), strongly supported by the v0.15.0 move to `*big.Int` and the maintainer's own rationale that `precise_amount` was added to "seamlessly manage amounts larger than 15 digits" (Blnk Core v0.10.1 blog) — but it is INFERENCE, not CONFIRMED.
- **For a cooperative-society savings platform: Blnk gives you double-entry integrity, immutability, idempotency and per-transaction hashing, but it provides essentially NO tenant isolation beyond ledger partitioning and API-key scoping** — one PostgreSQL, one Redis, one namespace shared by all societies. Noisy-neighbour and blast-radius risk is real and must be handled by you at the deployment layer, not by Blnk.

## Key Findings

1. **Architectural style is a modular monolith, proven from the layout and the process model, not the README.** The repository is a flat Go package (`package blnk`) at the root with ~40 sibling `.go` files (`transaction.go`, `balance.go`, `queue.go`, `reconciliation.go`, `apikey.go`, `webhooks.go`, `search.go`, `chain_worker.go`, `lineage_*.go`), plus subpackages `api/`, `model/`, `config/`, `database/`, `cmd/`, and `internal/` (with `lock`, `notification`, `pg-backups`, `pg-listener`, `redis-db`, `request`, `apierror`, `cache`). The `docker-compose.yaml` runs the **same image** as both `server` (`blnk migrate up && blnk start`) and `worker` (`blnk workers`) — CONFIRMED single binary, multiple process roles.

2. **PostgreSQL is the source of truth and the hardest-to-replace component.** All authoritative state (ledgers, balances, transactions, identities, API keys, reconciliation) lives in Postgres, accessed through a `database.IDataSource` interface. The schema is embedded in the binary (`var SQLFiles embed.FS` in `blnk.go`) and applied by `blnk migrate up`.

3. **Redis is on the correctness path, not a cache.** The `Queue` type wraps `*asynq.Client` and `*asynq.Inspector` (`github.com/hibiken/asynq`), so Redis is the transaction queue; `internal/redlock` provides the distributed lock *(corrected on assembly from `internal/redlock`; Volume IV read the current source and established the package is `redlock`. See Appendix E note 1)* that serialises balance updates. If Redis is down, queued processing and lock acquisition stop — this is a correctness-and-liveness dependency, not a performance nicety.

4. **The money model is confirmed at the Go struct level.** `model.Transaction` carries `PreciseAmount` (integer minor units — `int64` in the 2024 source, migrated to `*big.Int` by v0.15.0), a convenience `Amount float64`, and `Precision float64`. `model.Balance` carries `Balance`, `CreditBalance`, `DebitBalance`, `InflightBalance`, `InflightCreditBalance`, `InflightDebitBalance` (all integer minor units) plus `Version int64` for optimistic locking and a `CurrencyMultiplier float64` serialised as `precision`. Balance responses do not return precision — CONFIRMED in docs ("Blnk Core does not return precision on balance responses").

5. **The v0.15.0 conservation hardening is visible as a struct-level deletion.** The 2024 source carried a `Rate float64` field and an `ApplyRate()` function on transactions; the carried-forward v0.15.0 note records the removal of `rate`, `currency_multiplier` and `modification_ref` from the transaction path. This is the mechanism by which INV-1 (conservation) was hardened: asymmetric posting was removed, not merely discouraged.

6. **Transaction lifecycle and immutability are structural.** Status constants are `QUEUED`, `SCHEDULED`, `INFLIGHT`, `APPLIED`, `VOID`, `REJECTED` (`transaction.go`). New states are written as new rows linked by `parent_transaction`; the public API exposes `UpdateTransactionStatus` and `VoidInflightTransaction`/`CommitInflightTransaction` but no method that overwrites a posted transaction's amount, source or destination. Docs confirm: "Once recorded, transactions in Blnk cannot be modified or deleted."

7. **Per-transaction hashing is a method on the model; the chain is a separate worker.** `model.Transaction.HashTxn()` computes the SHA-256 hash; `chain_worker.go` (with `chain_worker_test.go`) is the global hash-chain subsystem, and `blnk verify-chain` is the CLI verifier. Tamper-evidence (INV-11) is therefore owned by two components: the model (per-row hash) and the chain worker (linkage).

8. **Idempotency is enforced at two layers.** The application requires a unique `reference` — docs state verbatim: "Blnk implements idempotency by requiring a unique `reference` for every transaction. This reference serves as a transaction identifier, preventing duplicate processing and ensuring consistent outcomes." Since v0.13.2 a database unique index `idx_transactions_reference_unique` backstops it at the storage layer — so a duplicate reference is rejected even under a race that slips past the application check.

9. **Search is optional and is a projection, not a source of truth.** `internal/pg-listener` listens to Postgres change notifications and `TypesenseClient.HandleNotification` pushes them into Typesense collections built by `EnsureCollectionsExist`. Since v0.13.2 a direct-DB filter search path exists, so Typesense can be removed entirely without affecting money movement.

10. **The `blnk-go` client contract encodes the money model correctly but leans on caller discipline.** It exposes `PreciseAmount: big.NewInt(...)` and a separate `Amount`/`Precision`, mirroring the REST surface; the danger it does not remove is that a caller can still send the float `Amount` with a wrong `Precision` and get a silently wrong `precise_amount`.

## Details

### II.1 System boundary; what Blnk Cloud is

**Inside Blnk Core (trusted, in-process):** the HTTP API layer (`api/`, `api/middleware/`, `api/model/`), the transaction engine (`transaction*.go`), the balance engine (`balance.go`, `model/balance.go`), the queue/worker layer (`queue.go`, `transaction_queue.go`, `queue_recovery.go`), the database access layer (`database/`), reconciliation (`reconciliation*.go`), lineage/shadow-ledger (`lineage_*.go`), identity/tokenization (`identity.go`), hashing/chain (`model.HashTxn`, `chain_worker.go`), API-key management (`apikey.go`), webhooks (`webhooks.go`), search (`search.go`), config (`config/`), CLI (`cmd/`), and migrations (`sql/` embedded).

**Outside Blnk Core (trusted infrastructure, separate processes):** PostgreSQL (required), Redis (required), Typesense (optional), Jaeger/OpenTelemetry collector (optional observability). **Untrusted:** all API callers and webhook receivers.

**Control plane vs data plane:** weakly distinguished. Configuration/orchestration (`blnk.json`, `blnk migrate up`) is separable from runtime processing, but there is no separate policy/management service in Core — the API binary is both.

**Blnk Cloud** is the commercial managed plane. Architecturally it is a hosted dashboard/control surface over Core data. The reader-flagged "Query Agent" that connects a managed plane to a self-hosted Core is a read-oriented connector: the docs say "Connect to Blnk Cloud to see your Core data. You can view your transactions, manage identities, create custom reports, invite other team members to collaborate, and perform operations on your Core." Core does not depend on Blnk Cloud in any way — self-hosted Core runs fully standalone. Exactly what the agent can write is not fully documented; treat write scope as UNKNOWN and assume it should be given a scoped, least-privilege API key.

### II.2 Component inventory (selected; state ownership in bold)

- **HTTP API layer** — `api/`, built on Gin (SOURCE-CODE INFERENCE from Gin routing idioms and the `blnk-go` REST surface). Inputs: REST calls with `X-blnk-key`. Outputs: JSON. **State: none (stateless).** Fails → no ingress; workers keep draining the queue.
- **Transaction engine** — `transaction.go` and siblings (`_execution`, `_inflight`, `_queue`, `_batch_processing`, `_bulk`, `_refunds`, `_rejection`, `_coalescing`, `_queries`). **State: owns transaction rows (write-once).** Core of INV-1/5/6/7/10.
- **Balance engine** — `balance.go`, `model/balance.go`. Methods `CommitInflightCredit/Debit`, `RollbackInflightCredit/Debit`, `UpdateBalances`. **State: owns the cached running-total balance rows + `Version`.** Core of INV-2/3/8/9.
- **Queue/worker** — `queue.go` (`Queue{Client *asynq.Client; Inspector *asynq.Inspector}`), `NumberOfQueues = 20`, queues `new:transaction`, `new:webhoook`, `new:inflight-expiry`. **State: Redis-resident job state + queued balance estimates.** `queue_recovery.go` recovers stuck-QUEUED transactions.
- **Database layer** — `database/`, `database.IDataSource`. **State: gateway to the authoritative store.**
- **Reconciliation** — `reconciliation.go` (+ engine/matching/rules tests). Ingests external files, matches to ledger. **State: reconciliation results in transaction `meta_data`** (e.g. `BLNK_RECONCILIATION_RESULT` with `recalculated_balance`).
- **Lineage / shadow ledger** — `lineage_*.go` (`_allocation`, `_credit`, `_debit`, `_outbox`, `_processing`, `_queries`, `_shadow`, `_worker`). Fund-provenance tracking; `LedgerBalance.GetLineage` surfaces received/spent/available. **State: allocation/lineage rows; uses an outbox pattern.**
- **Identity & tokenization** — `identity.go`, `model/identity.go` (PII fields). **State: identity rows + tokenized PII.**
- **Hashing / chain** — `model.HashTxn()` + `chain_worker.go`. **State: per-row hash + chain linkage.**
- **API-key management** — `apikey.go`. **State: hashed keys + scopes + owner binding.**
- **Webhooks** — `webhooks.go` (`SendWebhook`, `ProcessWebhook` via asynq). **State: none authoritative; delivery via queue.**
- **Search** — `search.go`, `TypesenseClient`; fed by `internal/pg-listener`. **State: Typesense projection (disposable).**
- **Config/CLI/migrations** — `config/`, `cmd/`, `sql/` (embedded `SQLFiles`).
- **Internal shared** — `internal/redlock` (distributed lock), `internal/redis-db`, `internal/pg-listener`, `internal/pg-backups`, `internal/notification`, `internal/request`, `internal/apierror`, `internal/cache`.

### II.3 Architectural style — PROVEN

Modular monolith. Evidence: (1) one root Go package with many sibling files sharing internal state through the `Blnk` struct (`NewBlnk(db database.IDataSource)`); (2) one Docker image invoked with different entrypoints (`blnk start` vs `blnk workers` vs `blnk migrate up`); (3) the worker system is in-process asynq consuming from Redis, not a separate service with its own API. A running Blnk is therefore **1 binary in 2 long-lived process roles** (API + worker) plus a **one-shot migration job**. It is event-driven/worker-queue *internally* (asynq over Redis) but monolithic in packaging.

### II.4 Interfaces

- **REST API** — resources: `/ledgers`, `/balances`, `/balance-monitors`, `/transactions` (+ `/transactions/bulk`, `/transactions/inflight`, `/transactions/refund`, `/transactions/reference/{ref}`, `/transactions/recover?threshold=`), `/identities`, `/reconciliation`, `/search`, `/health`. Auth via `X-blnk-key`. QUEUED transactions get a `_q` reference suffix — docs verbatim: "Blnk appends a `_q` suffix to your original reference after processing a `QUEUED` transaction." No explicit URL version prefix (unversioned; compatibility managed by release).
- **Queue message contract** — `TransactionTypePayload{Data model.Transaction}` enqueued to `new:transaction`; webhook payloads to `new:webhoook`; inflight-expiry to `new:inflight-expiry`.
- **Webhook contract** — `NewWebhook{Event string; Payload interface{}}`; HMAC signing since v0.13.0 (SHA-256 signature in header — DOCUMENTED BEHAVIOR).
- **CLI** — `blnk migrate up`, `blnk start`, `blnk workers`, `blnk verify-chain`, plus collection listing.
- **Config schema** — `blnk.json`: `data_source.dns`, `redis.dns`, `typesense.dns`, `server{port,ssl,domain,ssl_email}`, `notification.slack.webhook_url`, `queue.monitoring_port` (default 5004).
- **`blnk-go` client contract** — `NewClient(baseURL, apiKey, WithTimeout, WithRetry)`; services `Ledger`, `LedgerBalance` (incl. `GetLineage`), `Transaction` (incl. `BulkCommitInflight`, `BulkVoidInflight`), `Identity`, `Reconciliation`, `BalanceMonitor`, `System.health`. Money passed as `PreciseAmount big.NewInt(...)` alongside `Amount`/`Precision`. It mirrors the REST surface faithfully and hides HTTP retry/timeout; the risk it leaves open is the `Amount × Precision` → `precise_amount` conversion, which a caller can still get wrong.

### II.5 Dependency graph (from imports; `go.mod` not opened directly)

- **Runtime/protocol (critical):** `github.com/hibiken/asynq` (Redis queue + locks foundation), `github.com/typesense/typesense-go` (optional search), a PostgreSQL driver (pgx/lib-pq — SOURCE-CODE INFERENCE), Gin (HTTP — INFERENCE), `go.opentelemetry.io/otel` + Jaeger exporter (observability).
- **Compile-time:** Go stdlib `math/big` (money), `crypto/sha256` (hashing), `embed` (schema embedding).
- **Criticality ranking:** PostgreSQL driver > asynq/Redis > Gin > OTel > typesense-go. Replaceability: OTel and Typesense easy; Gin moderate; asynq hard (queue + lock semantics); Postgres driver hard (SQL coupling).

### II.6 Rented vs owned

| Dependency | Owned/Rented | If it disappears | Substitute | Migration cost |
|---|---|---|---|---|
| PostgreSQL | Rented (self-run or managed) | Ledger stops; source of truth gone | None like-for-like | Prohibitive — schema + SQL coupling |
| Redis | Rented | Queue + locks stop; balance mutation halts | Any asynq-compatible Redis | Low if drop-in Redis; high to swap the lib |
| Typesense | Rented (optional) | Search degrades; DB-filter fallback | Direct-DB search (v0.13.2+) | Low |
| asynq (lib) | Owned dep on correctness path | Rewrite queue/lock | River, Machinery, custom | High |
| Blnk Cloud | Rented (optional) | Dashboard only; Core unaffected | Self-host UI | None for Core |

A dependency that cannot be replaced is an architectural feature: **Postgres and the asynq/Redis pairing define Blnk's correctness envelope.**

### II.7 Single points of failure

- **Postgres unavailable:** total halt — no reads, no writes, no balance updates. Not graceful. Recovery: restore/failover Postgres; migrations idempotent.
- **Redis unavailable:** queued-by-default processing stops and locks cannot be acquired, so balance-mutating transactions stall. API may still accept and enqueue-attempt but cannot complete. Blast radius: all money movement. v0.15.2 added a `QUEUE_BACKPRESSURE` 503 so the API sheds load rather than silently backing up.
- **Typesense unavailable:** search only; money movement unaffected (graceful). DB-filter fallback exists.
- **Worker crash mid-transaction:** queue redelivery (asynq) + `queue_recovery.go` recover stuck-QUEUED work — docs: "Blnk now automatically checks for and recovers any transactions stuck in queue... You can also trigger recovery manually with the Queue Recovery endpoint" (`POST /transactions/recover?threshold=5m`, minimum 2 minutes). Per-transaction hash + immutability prevent partial-state corruption because state changes are new rows.

### II.8 State ownership

Authoritative balance lives in **one place: the PostgreSQL `balances` row**, protected by optimistic locking on `Version`. Redis holds *queued balance estimates* (`queued_credit_balance`/`queued_debit_balance`, since v0.8.3) and the *lock* — it is a coordination and estimation store, not an authoritative balance store. This is the one place two components *could appear* to own balance: Redis's queued estimates vs Postgres's committed balance. The design keeps them distinct (estimates are explicitly labelled "queued" and are not the balance), so there is no true dual-ownership — but an operator who reads queued estimates as authoritative would create a correctness illusion. Typesense and the OTel pipeline are pure projections.

### II.9 Storage architecture — the money-type question, answered honestly

Tables (reconstructed from models and ID prefixes): `ledgers` (`ldg_`), `balances` (`bln_`), `transactions` (`txn_`), `identities` (`idt_`), `balance_monitors`, plus reconciliation, lineage/allocation, and API-key tables. Confirmed columns on `transactions` (from a repo test's `SELECT`): `transaction_id, parent_transaction, source, reference, amount, precise_amount, precision, rate, currency, destination, description, status, created_at, meta_data, scheduled_for, hash`.

**The Postgres column type for money remains SOURCE-CODE INFERENCE, not CONFIRMED — this is itself a Volume II finding.** A targeted attempt to open the `sql/` directory (embedded as `SQLFiles embed.FS`) failed: GitHub's tree/blob/raw endpoints block automated retrieval, and no search index surfaced the verbatim `CREATE TABLE`. The strongest inference:

- `precise_amount`: **NUMERIC (arbitrary precision)** *(superseded on assembly: after four attempts across four volumes, Volume V declared the money column type **permanently UNKNOWN** for this study. The NUMERIC lean remains the best inference but must not be treated as established. See Appendix E note 2)* — supported by the v0.15.0 migration to `*big.Int` (which exceeds BIGINT's 19-digit range) and the maintainer's stated goal, verbatim from the Blnk Core v0.10.1 blog: "We initially introduced precision for developers to handle decimal amounts, but this was capped at a maximum of 15 digits. With this update, we've added a new transaction parameter, precise_amount, enabling developers to seamlessly manage amounts larger than 15 digits in their financial applications." A repo DB test passes `precise_amount` as a string ("100000") and `amount` as a float (1000.0), consistent with NUMERIC and DOUBLE PRECISION respectively.
- Balance money fields (`balance`, `credit_balance`, `debit_balance`, `inflight_*`): integer minor units in Go (`int64`, migrating to big.Int); Postgres type most likely **NUMERIC** to match precise_amount and hold >19-digit values; **BIGINT** cannot be excluded for older columns.
- `version`: integer optimistic-lock counter (BIGINT/INTEGER).
- Whether the DB itself constrains precision, sign or magnitude (CHECK constraints): **UNKNOWN / none found.** Negative balances are explicitly allowed (overdrafts), so a non-negativity CHECK on `balance` is unlikely.

`idx_transactions_reference_unique` (v0.13.2) enforces idempotency at the storage layer; its exact predicate (partial? `CONCURRENTLY`?) is **UNKNOWN**.

### II.10 Control plane vs data plane

Weakly separated. If the management/config surface is unavailable, in-flight money movement continues (workers drain Redis, Postgres commits) because configuration is read at process start from `blnk.json`. There is no runtime policy service whose outage would stop postings. Blnk Cloud's outage has zero effect on Core.

### II.11 Integration architecture

- **Synchronous push:** REST (`X-blnk-key`).
- **Asynchronous:** internal asynq queue; outbound webhooks (HMAC-signed since v0.13.0); balance monitors with callback URLs.
- **Pull:** REST GETs; Search API; historical balance API (`/balances/{id}/at?timestamp=`).
- **File ingestion:** reconciliation upload → matching rules → strategies (one-to-one, one-to-many, many-to-one).
- **Import/export:** bulk transactions with `effective_date` backdating (v0.9.0+), `atomic` and `run_async` flags. Blnk's docs describe the Bulk Transaction API as "process multiple transactions within a single request"; the "1,000–5,000 per batch" figure is a *recommendation* in Blnk's Data Migration guide, not an enforced cap, and no fixed limit is documented.
- **SDKs:** Go (`blnk-go`), TypeScript (`blnk-ts`), Java (`blnk-java`).
- **Compatibility boundary:** unversioned REST; behaviour changes are release-gated (e.g. exchange-rate removal at v0.15.0). This is a real risk — pin the server version.

### II.12 Deployment topologies

- **Local / single-node:** `docker compose up` — services `server`, `worker`, `redis`, `postgres:16`, `typesense:29.0`, `jaeger`.
- **Docker Compose (documented):** server runs `blnk migrate up && blnk start`; worker runs `blnk workers`; shared `blnk.json`. Docs describe Blnk as "a distributed system with three core components: API Server... Worker... Migration Service" plus supporting infra (PostgreSQL, Redis, Typesense, optional Jaeger).
- **Kubernetes:** `infrastructure/k8s-manifests/` in-repo; separate `blnk-infrastructure` repo provides Terraform (AWS/Azure/GCP) + k8s/Helm (community-maintained by contributor iamtito).
- **Managed:** Blnk Cloud.
- **What changes by topology:** Typesense and Jaeger appear/disappear as optional; the migration step is a one-shot job; API and worker scale independently (both stateless w.r.t. authoritative state — state is in Postgres/Redis), so **horizontal scaling of API and workers is supported**, bounded by Postgres write throughput and the Redis lock. Scaling requires a shared Redis and Postgres (no in-memory affinity).

### II.13 Multi-tenancy and isolation — critical for the reader

**Blnk provides NO tenant isolation beyond ledger partitioning and API-key scoping.** There are no per-tenant namespaces, no per-tenant databases, no resource quotas, no noisy-neighbour controls in Core. All cooperative societies would share one Postgres, one Redis queue (20 logical asynq queues, but shared infrastructure), one Typesense index. API keys are SHA-256-hashed at rest (v0.12.0), scoped (e.g. `transactions:write`), and owner-bound (v0.14.3) — that governs *authorisation*, not *isolation*. A heavy batch from one society competes for the same Redis queue and Postgres locks as every other. For members' savings, this means: **Blnk will enforce double-entry, immutability, idempotency and overdraft rules per balance, but it will NOT enforce fairness, blast-radius containment, or data-plane isolation between societies — you must provide that (separate deployments per society or per tier, or strict quotas at your gateway).**

### II.14 Architecture evolution

- **Queue-by-default processing:** transactions are enqueued (`QUEUED` → `_q` suffix) and applied by workers. This decoupled ingestion from accounting, enabling burst absorption — at the cost of eventual-consistency semantics (a caller must poll or await webhook for `APPLIED`). v0.15.2's `QUEUE_BACKPRESSURE` 503 and the queue-recovery endpoint are the maturation of this choice.
- **DB-level unique index (v0.13.2):** moved idempotency from application-only to storage-enforced — closing the race window. This made idempotency robust under concurrency but requires the reference column to be genuinely unique (a constraint on import/replay design).
- **Exchange-rate removal (v0.15.0):** deleted `rate`/`currency_multiplier`/`modification_ref` from the transaction path (the 2024 source's `Rate float64` + `ApplyRate()` are gone). This hardened conservation (INV-1) by making asymmetric posting structurally impossible; the cost is that multi-currency conversion must now be modelled as explicit two-leg transactions.
- **`precise_amount` + `*big.Int` migration:** from `int64` (2024) to arbitrary precision, enabling amounts larger than 15 digits.
- **Direct-DB filter search (v0.13.2):** reduced hard dependence on Typesense.
- **API-key hardening:** hashed at rest (v0.12.0), owner-bound (v0.14.3).

### II.15 INVARIANT LOCATION TABLE — the spine

| # | Invariant | Volume I claimed point | Actual component / file / function | Evidence |
|---|---|---|---|---|
| INV-1 | Conservation (dest credit = src debit) | Transaction engine | `transaction.go` posting + `model.UpdateBalances`; hardened by removal of `Rate`/`ApplyRate` at v0.15.0 | SOURCE-CODE INFERENCE (struct deletion CONFIRMED) |
| INV-2 | Balances change only via transactions | Balance engine | `balance.go` / `model/balance.go`; no public balance-mutation API except via transactions | CONFIRMED (API surface) |
| INV-3 | Balance derivability from history | Transaction history + reconciliation | `transaction_queries.go`, historical balance API, `reconciliation.go` recalculated_balance | DOCUMENTED BEHAVIOR |
| INV-4 | Idempotency (unique reference) | App-level reference | App check ("requiring a unique reference for every transaction") + DB unique index `idx_transactions_reference_unique` (v0.13.2) | CONFIRMED (docs) + INFERENCE (index DDL UNKNOWN) |
| INV-5 | Immutability of posted transactions | Transaction engine | New `parent_transaction`-linked rows; no field-overwrite API; docs "cannot be modified or deleted" | CONFIRMED (API surface + docs) |
| INV-6 | Valid state transitions only | Transaction engine | Status constants + `_inflight`/`_rejection`/`_refunds` handlers | CONFIRMED (constants) |
| INV-7 | Precision integrity (integer minor units) | Money model | `model.Transaction.PreciseAmount` (`big.Int`), `ApplyPrecision` → int64; `math/big` | CONFIRMED (Vol I) + SOURCE-CODE INFERENCE |
| INV-8 | Sufficient funds unless overdraft | Balance engine | `balance.go`: available = `balance − inflight_debit_balance` on source; else `REJECTED` (v0.11.0+); inflight included | DOCUMENTED BEHAVIOR |
| INV-9 | Concurrency safety | Redis lock + PG optimistic lock | `internal/redlock` (Redis) + `model.Balance.Version` | CONFIRMED (struct + package) |
| INV-10 | Zero/malformed rejected | Transaction engine | `transaction_rejection.go`; docs: "Zero amounts are not recorded in the Blnk ledger" | DOCUMENTED BEHAVIOR |
| INV-11 | Tamper-evidence | Hash + chain | `model.Transaction.HashTxn()` (SHA-256) + `chain_worker.go` + `blnk verify-chain` | CONFIRMED (method + file) |
| INV-12 | Authorisation & tenancy | API keys | `apikey.go` — hashed (v0.12.0), scoped, owner-bound (v0.14.3); **no tenancy isolation component exists** | CONFIRMED (file) / tenancy UNOWNED |

**No component owns tenant isolation.** INV-12's "tenancy" half is enforced only by convention (ledger partitioning + key scoping), not by an isolation subsystem.

### II.16 Falsification watch

- **Target 1 — authoritative money as float64:** NOT FOUND. Authoritative money is `precise_amount` (`big.Int`/integer minor units); `Amount float64` is a convenience input only, and `ApplyPrecision` returns `int64`. **Volume I money model survives.** (Caveat: not falsified, but not fully closed either — the DB column type is unconfirmed, so a float storage column cannot be 100% ruled out from DDL. Inference strongly against it.)
- **Target 2 — mutation of a posted transaction's financial fields:** NOT FOUND. No API or code path overwrites amount/source/destination/status in place; state changes create new `parent_transaction`-linked rows. **INV-5 survives.**
- **Target 4 — dest credit ≠ src debit in v0.15.0+:** NOT FOUND. The exchange-rate/asymmetric path (`Rate`, `ApplyRate`) was removed at v0.15.0. **INV-1 survives and was structurally hardened.**

No Volume I claim was falsified. The method's honest result is a partial gap, not a contradiction: the schema money type is still inference.

### II.17 Build-extraction verdicts

- **Single-Postgres source of truth — ADOPT.** Works because of the mechanism (one ACID store = one truth), not the environment. Directly transferable to a cooperative-society ledger. Benchmark to change: if write throughput exceeds one Postgres primary's capacity, shard by society/deployment rather than adding balance stores.
- **Redis lock-and-queue (asynq) — ADAPT.** The queue-by-default design is sound, but it makes Redis a correctness dependency. For members' savings, **ADAPT**: run Redis in HA (Sentinel/managed), monitor `QUEUE_BACKPRESSURE`, and decide explicitly whether you want synchronous (inline) posting for small societies to avoid eventual-consistency surprises. What must change: Redis from single-node to HA; add alerting on queue depth and lock wait.
- **Modular-monolith packaging — ADOPT.** The single-binary/multi-role model is simple to operate and scales horizontally on stateless roles. Transferable regardless of team size.
- **Optional-Typesense pattern — ADOPT.** Clean projection with a DB fallback; keep it optional and off unless you need free-text search.
- **API-key scoping model — ADAPT.** Hashed + scoped + owner-bound is good, but it is authorisation, not isolation. **ADAPT for multi-society:** you must add tenant separation above Blnk (deployment-per-society or per-tier, plus gateway quotas). A REJECT of "one shared instance for all societies without quotas" is warranted for real member savings.

### II.18 Reconstruction summary

1. **System context:** Callers → API (X-blnk-key) → Core binary → Postgres (truth) + Redis (queue/lock) + Typesense (optional) + OTel (optional); Blnk Cloud reads Core.
2. **Component diagram:** root `package blnk` + `api/model/config/database/cmd/internal` subpackages; asynq worker in-process.
3. **Critical path:** POST /transactions → enqueue (Redis) → worker acquires lock (internal/redlock) → validate → write txn row + update balance (version-checked) → hash → webhook.
4. **Dependency graph:** Postgres driver > asynq/Redis > Gin > OTel > Typesense.
5. **Rented vs owned:** Postgres + asynq/Redis irreplaceable; Typesense/Cloud/OTel disposable.
6. **SPOF map:** Postgres (total), Redis (money-movement), Typesense (search only).
7. **Interface map:** REST (unversioned) + asynq queue + webhooks (HMAC) + CLI + `blnk.json`; `blnk-go` mirrors REST.
8. **State-ownership matrix:** Postgres = authoritative; Redis = locks + queued estimates; Typesense/OTel = projections.
9. **Storage architecture:** tables named; money column type = NUMERIC (INFERENCE, not confirmed — GitHub blocked DDL retrieval).
10. **Control/data plane:** weakly separated; config outage does not stop postings.
11. **Integration map:** sync REST + async queue/webhooks + file reconciliation + bulk import.
12. **Deployment topology:** compose (server/worker/redis/postgres/typesense/jaeger); k8s manifests; Blnk Cloud.
13. **Isolation model:** ledger partitioning + API-key scoping ONLY; no data-plane isolation.
14. **Architecture evolution:** queue-by-default, DB unique index (v0.13.2), rate removal (v0.15.0), big.Int migration, key hardening.
15. **Invariant→component map:** see II.15; tenancy unowned.
16. **Falsification watch:** none falsified; schema money type still inference.
17. **Build-extraction verdicts:** see II.17.
18. **Key unknowns:** exact money column DDL; `idx_transactions_reference_unique` predicate; Blnk Cloud Query Agent write scope; whether any CHECK constraints exist.

**Which components are indispensable and which are commodity?** Indispensable: PostgreSQL and the asynq/Redis queue-and-lock pair. Commodity: Typesense, Jaeger/OTel, Blnk Cloud, the SDKs. **Centre of gravity:** the PostgreSQL source of truth, guarded by optimistic locking on `Version`. **What owns the source of truth:** the `database` layer over one Postgres. **Rented and breaks if gone:** Postgres (total halt) and Redis (money movement halts). **Boundary that matters most for correctness:** the transaction/balance write path where the Redis lock + Postgres `Version` together serialise mutation. **Hardest to replace:** PostgreSQL (schema + SQL coupling), then the asynq/Redis lock-queue semantics.

## Recommendations

1. **Before production for members' savings, confirm the money column DDL yourself.** Clone the repo and open `sql/` (the embedded `SQLFiles`) directly — verify `precise_amount` and every balance field is NUMERIC (or BIGINT) and never `double precision`/`float`. This is the single most important schema fact and Volume II could only infer it. Threshold to proceed: DDL shows an exact-decimal type for all authoritative money columns.
2. **Isolate tenants at the deployment layer.** Because Blnk enforces no data-plane isolation, run **one Blnk deployment (and Postgres/Redis) per society, or per risk tier**, rather than one shared instance. Change this only if you add hard per-tenant quotas at your gateway and accept shared blast radius. Benchmark: if a single society can saturate the Redis queue or Postgres write lock, isolation is mandatory.
3. **Run Redis and Postgres in HA and treat both as correctness infrastructure.** Redis Sentinel/managed + Postgres primary/replica with tested failover. Alert on `QUEUE_BACKPRESSURE` 503s and on queue depth; wire the queue-recovery endpoint (`/transactions/recover`, threshold ≥ 2m) into ops.
4. **Pin the server version and gate upgrades.** The REST surface is unversioned and behaviour changed materially at v0.15.0 (rate removal). Pin to a tested tag; test bulk-import/replay against the DB unique index before upgrading.
5. **Decide sync vs async posting explicitly.** Queue-by-default means `APPLIED` is eventual; for savings, either await the webhook/poll the `_q` reference before confirming to a member, or evaluate inline posting for low-volume societies.
6. **Give Blnk Cloud (if used) a least-privilege, scoped key** and treat the Query Agent's write scope as unknown until verified.

## Caveats

- **The Postgres money column type is INFERENCE, not CONFIRMED.** GitHub tree/blob/raw endpoints blocked automated retrieval of `sql/`, and no index surfaced the verbatim `CREATE TABLE`. NUMERIC is the strongly-supported best inference (big.Int migration + the maintainer's ">15 digit" rationale), but Volume I's gap is only *narrowed*, not fully closed.
- **Several struct-level facts come from the `northstar-pay/nucleus` fork at commit 1cb559337258 (Aug 2024)**, a faithful Blnk mirror that pkg.go.dev had indexed. Where v0.15.0 differs (notably `PreciseAmount int64` → `*big.Int` and the removal of `Rate`), I have stated the release explicitly. Do not read the 2024 struct as the v0.15.0 struct.
- **Gin as the HTTP framework and the exact Postgres driver are SOURCE-CODE INFERENCE**, not opened in `go.mod`.
- **`idx_transactions_reference_unique` predicate, any CHECK constraints, and the Blnk Cloud Query Agent's write scope are UNKNOWN.**
- **HMAC webhook signing (v0.13.0) is DOCUMENTED BEHAVIOR**, not verified in `webhooks.go` source line-by-line.
- Volume III should verify at runtime what this volume located structurally — especially conservation under concurrency, the unique-index race behaviour, and whether queued balance estimates ever diverge from committed balances.

---

# VOLUME III — Data, State, Control & Execution Flows

> ### ⚠ SUPERSESSION NOTICE — read before this volume
>
> **Volume III was researched against a 2024 fork (`northstar-pay/nucleus` @ `1cb559337258`) because the current source could not be retrieved at the time. Volume IV subsequently read the v0.15.2 source directly and superseded three of this volume's findings. Where they conflict, Volume IV governs.**
>
> **1. The two-write partial-success hazard no longer exists.** This volume reports that `processBalances` persists balances *before* `finalizeTransaction` inserts the row, as two separate datasource calls — and builds its partial-success matrix on that. **Volume IV established that v0.15.2 persists balances, the transaction row and the lineage outbox through a single composite call, `RecordTransactionWithBalancesAndOutbox`, which the source comments describe as "persisted atomically."** The worst rows of §III.11's matrix — durable one-sided state after a crash mid-write — are therefore historical, not current. This volume anticipated exactly this: *"If v0.15.x already wraps the two writes atomically, Findings 2–3 and the worst partial-success rows soften."* They do.
>
> **2. The float ingress is gone.** This volume reports `PreciseAmount = int64(Amount × Precision)` — a lossy float multiply. That is fork behaviour; **v0.15.2 accepts `precise_amount` as `*big.Int` directly.** The caller-discipline warning still stands where the convenience `amount` field is used.
>
> **3. The lock covers both balances, not just the source.** This volume reports a lock keyed on `transaction.Source` alone, leaving the destination protected only by optimistic `version`. **Volume IV found `redlock.NewMultiLocker` over both balance IDs, deduplicated and lexicographically sorted.**
>
> **What survives unchanged:** the queue-by-default finding and the real commit point; the `validateTxn` TOCTOU window backstopped by the unique index; the webhook-without-outbox gap; and the four-way invariant classification, which Volumes IV and V build on directly.


## TL;DR
- **The caller's HTTP response almost never means the money moved.** By default every write returns `QUEUED` with a `_q`-suffixed reference; the real commit point is later, inside an asynq worker that acquires a Redis lock, mutates cached balances, and inserts the row — and even inflight commit/void are queued-by-default since v0.15.0. A cooperative-savings reader must treat 201/200 as "accepted", not "settled".
- **Conservation and precision are strong; concurrency-safety, tenancy and event-durability are weak.** Double-entry conservation (INV-1) and integer-minor-unit precision (INV-7) are enforced structurally/by construction; idempotency (INV-4) and immutability (INV-5/INV-11) are backed by a unique index and a DB immutability trigger. But the single-key Redis lock, webhook-without-outbox, and absent tenancy owner mean INV-9, INV-10 and INV-12 are enforced only by check or by convention — defects a hot cooperative balance will find.
- **The `precise_amount`/balance PostgreSQL column type remains UNKNOWN.** The DDL in the embedded `sql/` dir could not be retrieved by any automated route. Go `*big.Int` plus string-JSON serialization plus the ">15 digit" changelog claim strongly imply unbounded `NUMERIC`, but this is SOURCE-CODE INFERENCE, not confirmed. We keep it UNKNOWN, correcting no earlier volume.

---

## Key Findings

1. **Queue-by-default is the defining mechanism.** `QueueTransaction` (transaction.go) sets `SkipBalanceUpdate=true`, computes `PreciseAmount`, hashes, splits, and enqueues to asynq. The API returns `QUEUED` before any balance moves. A separate worker process later runs `RecordTransaction`, which is where money actually moves. The asynq defaults are named in Blnk's configuration docs: transaction queue `new:transaction`, webhook queue `new:webhook`, index queue `new:index`, inflight-expiry queue `new:inflight-expiry`; number of queues 20, max workers 10, max retries 3, retry delay 5 seconds. [CONFIRMED IMPLEMENTATION — transaction.go `QueueTransaction`, `setTransactionMetadata`, `enqueueTransactions`; DOCUMENTED BEHAVIOR — docs.blnkfinance.com/advanced/configuration]

2. **The real commit point is the worker's `finalizeTransaction` → `persistTransaction`, not the API response.** In the synchronous (`skip_queue`/worker) path, `RecordTransaction` runs under `executeWithLock`: validate → get balances → apply-to-balances in memory → `updateBalances` (persist balances) → `persistTransaction` (insert txn row) → post-actions. Balance write and transaction-row write are **two separate datasource calls**, not one DB transaction, in the code observed. [CONFIRMED IMPLEMENTATION (Aug-2024 fork transaction.go); SOURCE-CODE INFERENCE that v0.15.x preserves the two-call ordering]

3. **Balances are persisted BEFORE the transaction row.** `processBalances` (which calls `updateBalances`) runs before `finalizeTransaction` (which calls `persistTransaction`). A crash between them leaves balances mutated with **no APPLIED transaction row** — a durable, silent partial state. [SOURCE-CODE INFERENCE — transaction.go ordering]

4. **Webhooks fire from a detached goroutine with no outbox on the main path.** `postTransactionActions` launches `go func(){ SendWebhook(...) }()`. There is no transactional coupling: a webhook can be emitted for a state the DB later fails to persist, or lost entirely if the process dies. Volume II found the *lineage* subsystem uses `lineage_outbox.go`; the **main transaction/webhook path does not**. [CONFIRMED IMPLEMENTATION — transaction.go `postTransactionActions`, webhooks.go `SendWebhook`]

5. **Idempotency is a SELECT-then-check race backstopped by a unique index.** `validateTxn` calls `TransactionExistsByRef` and rejects if found — a TOCTOU window. Two identical references racing through the API both pass the check; the DB index `idx_transactions_reference_unique` (v0.13.2) is the real guarantee, converting the loser into an insert error the caller must interpret. [CONFIRMED IMPLEMENTATION — transaction.go `validateTxn`; DOCUMENTED BEHAVIOR — unique index]

6. **The `_q` suffix does NOT weaken caller idempotency.** `validateTxn` checks the caller's original reference before enqueue; the `_q` suffix is applied to the stored/queued record. A caller retrying with the original reference collides correctly at validation and/or at the unique index. [SOURCE-CODE INFERENCE — validateTxn runs on original reference in QueueTransaction]

7. **The distributed lock is keyed on the SOURCE balance only (historically), creating asymmetric protection.** In the Aug-2024 fork, `acquireLock` locked `transaction.Source` with a lock duration that Blnk's configuration docs give as a default of 1800 seconds (30 minutes). v0.15.x changed the inflight-commit lock key to `inflight-commit:%s` (per-transaction). Where the lock is per-source-balance, two transactions crediting the same destination from different sources are **not mutually excluded on the destination** — optimistic `version` is the only backstop there. [CONFIRMED IMPLEMENTATION (fork) `acquireLock`; DOCUMENTED BEHAVIOR (lock duration 1800s); SOURCE-CODE INFERENCE for v0.15.x generalization]

8. **Optimistic `version` is the last line of defence, and its retry behaviour is thin.** Blnk's blog "How Blnk Handles High-Traffic Hot Balances" (17 July 2026) states verbatim: *"Each balance has a version number. A payment remembers the version it read, and its write only succeeds if that version has not changed. If another payment has already updated the balance, the stale write is rejected and must be retried using the new value."* Under a hot cooperative balance the queue serialises work per hot pair (coalescing + hot-lane routing), but a version conflict surfaces as a failed/retried unit, not a silent merge. The same blog specifies the lock-wait behaviour: *"This configuration allows Blnk to wait for up to three seconds when acquiring the required balance locks. It does not delay every transaction by three seconds. A transaction continues as soon as the lock becomes available."* [MAINTAINER CLAIM — hot-balances blog; DOCUMENTED BEHAVIOR]

9. **Backdated transactions do NOT rewrite history or recompute prior balances at runtime.** `effective_date` is stored and used by *historical* balance queries and reconstruction, but a live backdated insert applies to the current cached running balance like any other transaction (it moves `balance` now). Blnk's own migration guidance — set the initial adjustment's `effective_date` before all others — is a workaround precisely because later-applied backdated rows affect the running balance in application order, not effective-date order. [DOCUMENTED BEHAVIOR — migration guide; ANALYTICAL INFERENCE]

10. **Balance reconstruction can silently diverge from the stored balance.** The v0.10.1 "Balance Reconstruction" recomputes balances from transactions and writes a `BLNK_RECONCILIATION_RESULT` into metadata containing `previous_balance`, `recalculated_balance`, and `difference` (the v0.10.1 blog shows a live `"difference":"103842"` recorded in `meta_data`). The difference is recorded in metadata; there is no evidence of an automatic alert/halt when it is non-zero — an operator must inspect it. [DOCUMENTED BEHAVIOR — v0.10.1 blog]

---

## Details

### III.1 Representative operations (boundary-crossing set)
Selected to cross the most boundaries (API ↔ Redis queue ↔ worker ↔ Postgres ↔ webhook/Typesense):
1. Simple queued transaction (`POST /transactions`, default).
2. `skip_queue:true` direct transaction (synchronous, bypasses asynq).
3. Inflight create → commit (two-phase).
4. Inflight create → void.
5. Partial inflight commit (`amount` < original).
6. Multi-destination split (`SplitTransaction`).
7. Bulk transaction `atomic:true`.
8. Refund (`RefundTransaction` → new reversed queued txn).
9. Backdated transaction (`effective_date`).
10. Reconciliation / balance reconstruction run.

### III.2 Happy-path execution — queued vs direct

**Queued (default).** API process: parse → auth (scoped `X-blnk-key`) → `QueueTransaction`: `validateTxn` (reference SELECT) → `setTransactionStatus` (QUEUED/SCHEDULED/INFLIGHT) → `setTransactionMetadata` (`SkipBalanceUpdate=true`, `TransactionID`, `HashTxn`, `PreciseAmount=int64(Amount*Precision)` historically / `*big.Int` in v0.15.x) → `SplitTransaction` → `enqueueTransactions` (asynq `new:transaction`, 20 queues, max 10 workers). **Response returns here: status QUEUED, no money moved.** Worker process later: dequeues → `RecordTransaction` under `executeWithLock` → `validateAndPrepareTransaction` → `processBalances` (`applyTransactionToBalances` in memory → `updateBalances` persists source+destination) → `finalizeTransaction` (`persistTransaction` inserts row, status APPLIED) → `postTransactionActions` (async webhook). **Money moves inside the worker, at `updateBalances`.**

**Direct (`skip_queue:true`).** Same `RecordTransaction` path but executed synchronously in the API request; response returns after `persistTransaction`. This is the only mode where "response received" ≈ "money moved" — and the one that throws `Failed to acquire lock` under contention (after the configured 3-second lock wait elapses).

### III.3 INVARIANT ENFORCEMENT VERIFICATION TABLE

| Inv | Runtime enforcement point (file, function, constraint) | Classification | Evidence | Bypass path |
|---|---|---|---|---|
| INV-1 Conservation | `model.UpdateBalances` applies equal debit to source / credit to destination from one `precise_amount`; double-entry requires both source+destination | **Structural (by construction)** | CONFIRMED IMPL (`applyTransactionToBalances`→`model.UpdateBalances`) | None on write path; a single amount drives both legs |
| INV-2 Balances change only via transactions | All mutation flows through `updateBalances`/`UpdateBalances`; `CreateBalance` starts at 0 | **By check / convention** | CONFIRMED IMPL | Direct DB write; reconstruction overwrites balance |
| INV-3 Derivability from history | Balance Reconstruction recomputes from transactions | **By check** | DOCUMENTED | Cached balance is authoritative day-to-day; drift possible until reconstruction |
| INV-4 Idempotency (unique reference) | `validateTxn` SELECT + DB index `idx_transactions_reference_unique` | **Structural (index) + by check (pre-check)** | CONFIRMED IMPL + DOCUMENTED | Concurrent duplicates pass `validateTxn`; index rejects loser as error |
| INV-5 Immutability of posted txns | New `parent_transaction`-linked rows for every state change; DB immutability trigger on protected fields | **Structural (trigger) + convention (append-only design)** | CONFIRMED IMPL (finalizeCommitment/finalizeVoid create new rows); DOCUMENTED (hash doc "immutability trigger") | Non-protected fields (`description`,`meta_data`) mutable |
| INV-6 Valid state transitions | `fetchAndValidateTransaction` / `fetchAndValidateInflightTransaction` guard status == INFLIGHT; `IsParentTransactionVoid` | **By check** | CONFIRMED IMPL | No DB CHECK on status; guards live only in the two inflight functions |
| INV-7 Precision integrity (integer minor units) | `PreciseAmount` integer; `model.ApplyPrecision`; per-row hash uses float `amount` | **Structural (integer storage) with a lossy ingress** | CONFIRMED IMPL | `int64(Amount*Precision)` truncates float at ingress (see III.5) |
| INV-8 Sufficient funds unless overdraft | Balance check `balance - inflight_debit_balance` since v0.11.0; `allow_overdraft` + overdraft limit | **By check** | DOCUMENTED | Queued estimate vs committed balance gap; overdraft bypasses; check is code not constraint |
| INV-9 Concurrency safety (lock + version) | Redis `redlock` on source balance / per-txn inflight key; optimistic `version` on balance write | **By check** | CONFIRMED IMPL + MAINTAINER CLAIM | Lock keyed on source only → destination collisions rely on version alone; lock is advisory |
| INV-10 Zero/malformed not recorded | Validation rejects zero amount / bad body; discarded (not stored) | **By check** | DOCUMENTED | Convention-level; no DB CHECK(amount>0) confirmed |
| INV-11 Tamper-evidence (`HashTxn` + chain) | `HashTxn` SHA-256 per row (always); optional global hash chain (v0.15.0, off by default); `blnk verify-chain` | **By check (per-row) / structural-if-enabled (chain)** | CONFIRMED IMPL + DOCUMENTED | Per-row hash covers only amount/reference/currency/source/destination; chain disabled by default |
| INV-12 Authorisation & tenancy | Scoped API keys (`transactions:write` etc.) at API middleware | **Auth: by check. Tenancy: NOT ENFORCED (no owner component)** | DOCUMENTED (scopes); Vol II finding | No tenant isolation in data model; keys gate verbs not tenants |

**The decisive distinctions for a savings cooperative:** INV-1 and INV-7-storage are guarantees; INV-8, INV-9, INV-10, INV-12-tenancy are *hopes* enforced by code paths or absent entirely. A concurrent caller on a hot pooled balance is exactly the actor that reaches balance state without the protection being sufficient.

### III.4 State machines

**Transaction:** `QUEUED`/`SCHEDULED` → (`APPLIED` | `INFLIGHT` | `REJECTED`); `INFLIGHT` → (`APPLIED` via commit | `VOID` via void); `APPLIED`/`VOID`/`REJECTED` terminal. Every transition is a **new row** linked by `parent_transaction` (never an in-place update). Guards: `setTransactionStatus` chooses initial state; `fetchAndValidate*` enforce INFLIGHT precondition. Invalid transitions (e.g., commit of an APPLIED txn) are **prevented by check** ("transaction is not in inflight status"), not by a DB constraint — so an untested code path could reach the same state.

**Balance:** mutable running total; fields move between `balance`, `inflight_balance`, `credit/debit`, `inflight_credit/debit`. Inflight create: `balance`↓, `inflight_balance`↑. Commit: `inflight`→`debit/credit` (`CommitInflightDebit/Credit`). Void: `RollbackInflightDebit/Credit` restores `balance`. `version` increments each write.

### III.5 Data flow & lossy transformations
Ingress float `amount` × caller `precision` → `PreciseAmount`. In the fork this is `int64(transaction.Amount * transaction.Precision)` — a **float64 multiply then integer truncation** (lossy, truncates toward zero; the classic 0.1+0.2 float error can shave a minor unit). v0.15.x accepts `precise_amount` directly as `*big.Int`, letting disciplined callers bypass the float entirely — the recommended path for a savings ledger. The original float `amount` **is preserved** on the row and is what the per-row hash fingerprints. Lossy points: (1) float→int at ingress if `amount` is used; (2) partial-commit remainder `float64(amountLeft)/precision` recomputes a display float; (3) Typesense projection is a lossy read model (see III.14).

### III.6 Transaction boundaries & the real commit point
- **Atomic unit:** the balance write (`UpdateBalances`) and the transaction-row insert (`RecordTransaction`) are issued as **separate datasource calls** in the observed code — not a single DB transaction. Balances are written first.
- **Real commit point:** the moment `updateBalances` durably persists the new balances in the worker. After that the money has moved even if the row insert or webhook later fails.
- **Webhook before durability:** yes — `postTransactionActions` fires asynchronously and is not ordered after a single enclosing commit, so a webhook can precede/contradict durable state.

### III.7 Ordering & time
Ordering is per-application-processing-order, serialised per balance by the lock, not by `effective_date`. `created_at` is wall-clock at enqueue (`time.Now()` in `setTransactionMetadata`). Backdated inserts apply to the *current* running balance; historical/`/at?timestamp=` queries and reconstruction use `effective_date`. **A backdated transaction inserted after later ones does not rewrite history or recompute intervening balances at runtime** — the running balance simply moves now, and the hash chain (if enabled) seals rows in chain sequence, so reordering by effective date is not reflected in the chain. This is the ledger-correctness hazard Volume I flagged: for interest/statement purposes the reader must reconstruct, not trust the live running total.

### III.8 Concurrency at the contention point
Lock scope: per **source balance** (historic) / per-inflight-transaction key (v0.15.x commit), with a default lock duration of 1800 seconds. Deadlock across two balances: the single-key-on-source design means a transaction acquires **one** lock, so classic two-lock deadlock is largely avoided — at the cost of not locking the destination. Hot pooled contribution account (the reader's case): with `skip_queue` it throws `Failed to acquire lock` after the 3-second lock wait; the intended path is the queue, where **coalescing** groups same source+destination+currency work and **hot-lane routing** isolates the hot pair, then optimistic `version` rejects stale writes for retry. Starvation/fairness: asynq gives 20 weighted queues with up to 10 workers; a persistently hot balance can still back up (hence the v0.15.2 `503 QUEUE_BACKPRESSURE`).

### III.9 Idempotency model
Key = caller `reference`, scope = whole ledger, persisted as a unique index, retained for life of the row. Payload-mismatch on a reused reference is **not** reconciled — first write wins, duplicate discarded. Blnk's idempotency blog states verbatim: *"If your app retries with the same reference, Blnk discards the duplicate silently. Alex's balance only moves once, and your ledger stays correct."* Concurrent identical requests: both may pass `validateTxn`; the unique index turns the loser into an **error the caller must interpret**, not a clean success echo. **Exactly-once effect** (balance moves once) is delivered by the index; **exactly-once delivery** (of the API/webhook acknowledgement) is NOT — retries and duplicate webhooks are the caller's responsibility. Rejected vs discarded: REJECTED is stored (insufficient funds etc.); discarded (duplicate/zero) is not. Blnk's guidance for correct retries is explicit: *"Create the reference before any retry logic runs. Build it before you enter the retry loop. If you create it inside the loop, every attempt gets a fresh reference, and Blnk has no way to know they're the same operation."*

### III.10 Events & asynchrony
Main path: `SendWebhook` from a goroutine, no outbox, no transactional coupling, at-most-once-ish with best-effort `NotifyError`. Lineage path: `lineage_outbox.go` (durable outbox) — so the project *knows* the pattern but has not applied it to core webhooks. Ordering across webhooks is not guaranteed; dead-letter/replay for core webhooks is absent on the observed path (asynq's own max-retries 3 / retry-delay 5s governs redelivery of the webhook *task*, not durability against a lost emit).

### III.11 PARTIAL-SUCCESS MATRIX

| Scenario | Effects that persist | System knows? | Auto-heal? | Time-to-notice |
|---|---|---|---|---|
| Multi-dest split, one leg fails | Successful legs persist unless `atomic:true`; with `atomic:true` Blnk "rolls back the entire split" | Only via atomic flag | No (non-atomic) | Until reconciliation |
| Bulk `atomic:false`, some fail | Succeeded entries committed, failed skipped | Partially (per-entry result) | No | Immediate per-entry, but no global rollback |
| Committed to PG, webhook never delivers | Balance moved, row APPLIED, downstream never told | No | No | Until external reconciliation |
| PG write ok, Typesense projection fails | Ledger correct, search stale/missing | pg-listener may log | Eventually (re-index) | Search-only impact |
| Inflight commit updates one balance, fails on other | Possible one-sided balance move (two separate writes) | No | No | Until reconstruction |
| Worker crash after balance update, before APPLIED insert | **Balances moved, no APPLIED row** | No | Queue recovery re-drives the QUEUED parent → risk of double-apply if original balance write already landed | Until reconstruction/audit |

The worker-crash-mid-operation row is the most dangerous: it is a durable, silent, one-sided state, and queue recovery keys off the still-`QUEUED` parent. On the atomic-split guarantee, Blnk's own blog is explicit: *"`atomic: true` means the split succeeds completely or fails completely. If one destination fails, Blnk rolls back the entire split."*

### III.12 Failure matrix — durable end-state

| Failure | Durable DB end-state |
|---|---|
| Validation error | Nothing written (discarded) or REJECTED row |
| Redis unavailable at enqueue | Enqueue fails, `NotifyError`, no txn recorded; caller gets error |
| Redis unavailable mid-op (lock) | `Failed to acquire lock`; balances untouched |
| Postgres unavailable at `updateBalances` | Balances not moved; txn stays QUEUED for recovery |
| Postgres unavailable at `persistTransaction` (after balance write) | **Balances moved, no APPLIED row** |
| API process crash pre-enqueue | Nothing persisted; caller must retry (same reference safe) |
| Worker crash mid-op | See III.11 |
| Response loss (ambiguous timeout) | Effect may or may not have happened; safe retry only via same reference (idempotency) |
| Concurrent version conflict | Stale write rejected; retry |
| Queue backpressure (v0.15.2) | `503 QUEUE_BACKPRESSURE`, nothing enqueued |

### III.13 Recovery & reconciliation
`queue_recovery.go` / `POST /transactions/recover?threshold=` (min 2m, default auto since v0.13.2) scans for transactions stuck in `QUEUED` past the threshold and **re-enqueues** them. Re-driving a transaction whose balance write already succeeded but whose row insert failed **can double-apply** if the worker cannot detect the prior balance mutation — the reference index protects against a duplicate *row*, but a re-driven QUEUED parent generates its own APPLIED child. Self-healing: stuck-queue re-drive, inflight-expiry auto-void. Operator-required: balance reconstruction (`from_source=true` / `BLNK_RUN_RECONCILIATION`), which recomputes from transactions and records `difference` in metadata **without a confirmed automatic alert** — a reconstructed balance can silently differ from the stored balance and only a human reading the metadata would know.

### III.14 Read paths & staleness
Primary reads hit Postgres cached balances (authoritative). Between enqueue and apply, the balance does **not** reflect the pending transaction in `balance`; instead `queued_credit_balance`/`queued_debit_balance` (v0.8.3) expose the pending estimate separately, and available balance = `balance - inflight_debit_balance`. **A caller could act on a queued estimate as though committed** — the estimate is explicitly labelled but nothing prevents misuse, and the gap persists for the full queue latency (unbounded under backpressure). Typesense is an eventually-consistent projection via `pg-listener`; its staleness bound is incidental, not guaranteed. Historical balances via `/balances/{id}/at?timestamp=`.

### III.15 Mutation, deletion, immutability
Transactions: append-only; protected fields guarded by DB immutability trigger + hash; `description`/`meta_data` mutable. Balances: mutable running totals (by design). Identities: became **deletable** in v0.15.0 (`DeleteIdentity`). Deleting an identity attached to a balance: the balance and its transaction history persist (identity link is a reference); the hash chain — which does not fingerprint identity — is unaffected. "Deletion" for transactions is effectively not offered; for identities it is real deletion of the identity record.

### III.16 Falsification watch
- **Target 1 (authoritative money as float64 on the write path):** **PARTIALLY CONFIRMED as a latent hazard.** `setTransactionMetadata` computes `PreciseAmount = int64(Amount * Precision)` — a float64 multiply on the write path when the caller supplies `amount`. `CommitInflightTransaction` took `amount float64` in the fork (now `*big.Int` in v0.15.x). Authoritative storage is integer, but the *conversion* touches float. **This does not falsify Volume I's integer-storage claim, but it qualifies it: the ingress is float-lossy unless the caller sends `precise_amount`.** Volume I's precision claim should be annotated accordingly.
- **Target 2 (mutation of a posted txn's financial fields vs new parent-linked row):** **NOT FOUND / model survives.** `finalizeCommitment` and `finalizeVoidTransaction` always mint a new `TransactionID`/`Reference` and set `ParentTransaction`; the immutability trigger guards protected fields. Immutability holds.
- **Target 4 (destination credit ≠ source debit in v0.15.0+):** **NOT FOUND / model survives.** A single `precise_amount` drives both legs via `model.UpdateBalances`; there is no code path that credits a different amount than it debits. Conservation holds at runtime.

### III.17 Build-extraction verdicts
- **Queue-by-default + eventual-consistency contract — ADOPT (with caller discipline).** Works because of the queue *and* the caller treating QUEUED as non-final. For a savings cooperative, ADOPT but expose settlement status to members only on APPLIED webhooks/polls, never on 201.
- **Redis distributed lock as serialiser — ADAPT.** It works largely because of the deployment (single logical Redis, hot pairs isolated by routing) rather than the mechanism's completeness. **Change:** lock on an ordered pair {source,destination} (or both balances) to close the destination-collision gap, or rely on `version` + retry as the primary guarantee and treat the lock as optimisation.
- **Optimistic `version` — ADOPT.** Correct and environment-independent; make retry counts/limits explicit and surface conflicts to callers.
- **Inflight two-phase model — ADOPT.** Clean commit/void with parent linkage; partial commit supported.
- **`_q` suffix convention — ADOPT.** Does not harm idempotency; keep the caller-reference check ahead of enqueue.
- **Queued-balance-estimate exposure — ADAPT.** Rename/relabel and gate in the API so a queued estimate can never be mistaken for available funds; for members' savings this must be UI-enforced.
- **Webhook without outbox — REJECT (for a money system).** **Change:** add a transactional outbox to the core transaction path (the project already has `lineage_outbox.go` to copy).
- **Two-write (balance then row) non-atomic commit — ADAPT/REJECT.** **Change:** wrap balance update and transaction insert in one DB transaction, or make the worker idempotent against its own partial completion before enabling queue recovery in production.

### III.18 Reconstruction — answers to the volume's closing questions
- **Real commit point:** the worker's durable `updateBalances`, not the API response.
- **Authoritative state:** the Postgres cached balance row (with `version`); Redis is on the correctness path but is queue+lock, not the record; Typesense is a projection.
- **Structural vs convention:** structural = conservation (INV-1), integer storage (INV-7), unique-reference index (INV-4), immutability trigger (INV-5/11 protected fields). Convention/check-only = sufficient funds (INV-8), concurrency (INV-9), zero/malformed (INV-10), tenancy (INV-12).
- **Ambiguous timeout + retry:** safe *only* if the caller reuses the same reference; the index/validate then makes the retry a no-op or a clean error. Any new reference double-applies.
- **Half-success:** the balance-then-row ordering and outbox-less webhook mean half-success leaves durable, silent, one-sided state; reconciliation/reconstruction is the only cure and it does not alert.
- **Where races occur:** `validateTxn` TOCTOU; destination balance under source-only lock; queued-estimate reads; queue-recovery re-drive vs partial completion.
- **Hardest operation to make correct:** the inflight partial commit under concurrency touching two balances via two separate writes — most legs, most state, least atomicity.
- **Runtime mechanism that most defines Blnk:** queue-by-default asynchronous processing with a Redis-lock-serialised, optimistically-versioned balance mutation.

### Ten most important findings (ranked)
1. The real commit point is the worker's durable balance write, not the API response — QUEUED ≠ settled.
2. Balance write and transaction-row insert are two separate writes, balance first — a crash between them leaves durable one-sided state.
3. Core webhooks have no outbox; they can fire before durability or be lost.
4. Idempotency is a TOCTOU pre-check saved only by the unique index; the caller gets an error, not a clean echo, on a concurrent duplicate.
5. The Redis lock is keyed on source only; destination collisions rely on optimistic `version` alone.
6. Float ingress (`int64(amount*precision)`) is lossy; send `precise_amount` as an integer/`*big.Int`.
7. Backdated transactions move the running balance now and do not recompute history; correctness needs reconstruction.
8. Balance reconstruction records a `difference` but does not alert — silent drift is possible.
9. Queue recovery re-drives QUEUED parents and can double-apply after a partial completion.
10. Tenancy (INV-12) is owned by no component; scoped keys gate verbs, not tenants.

## Recommendations
1. **Treat 201/QUEUED as "accepted", settle on APPLIED.** Build member-facing balances off APPLIED webhooks or polled status, never the create response. Benchmark to change: if you enable `skip_queue` for a low-traffic reserve balance, you may treat its synchronous 200 as settled.
2. **Do not expose queued/estimated balances as spendable.** Gate `queued_*` fields server-side. Threshold: only relax if you add hard available-funds checks at spend time.
3. **Send `precise_amount` as an integer/`*big.Int`, never `amount` float.** Eliminates the float-truncation ingress. This is mandatory for members' savings. Also generate each transaction `reference` before the retry loop, not inside it.
4. **Before production: wrap balance-write + row-insert in one DB transaction, and add a core webhook outbox.** Until then, run scheduled balance reconstruction and alert on any non-zero `difference` yourself — Blnk will not.
5. **Close the lock gap on hot pooled accounts.** Either always queue (never `skip_queue`) for contribution accounts, or patch the lock to cover both balances. Benchmark: if `blnk_chain_lag`/queue backlog or `503 QUEUE_BACKPRESSURE` appears, you are at the contention limit.
6. **Enable the global hash chain (`BLNK_TRANSACTION_HASHCHAIN_ENABLED=true`) and schedule `blnk verify-chain`.** It is off by default; for members' money, tamper-evidence should be on.
7. **Build tenancy yourself.** Scoped keys gate verbs, not tenants; enforce per-cooperative isolation in your application layer.

## Caveats
- **`precise_amount` / balance PostgreSQL column type: UNKNOWN.** The embedded `sql/` DDL could not be retrieved by any automated route (GitHub blob/raw blocked by robots; not indexed by search; CDN/sourcegraph not reachable by the tools available). `*big.Int` + string-JSON serialization of balance fields (e.g. `"balance":"40000"`) + the v0.10.1 changelog claim of support for amounts "larger than 15 digits" strongly imply an unbounded `NUMERIC` column in current Blnk; the Aug-2024 `northstar-pay/nucleus` fork used Go `int64` for these fields (implying `BIGINT` at that time). We report NUMERIC as SOURCE-CODE INFERENCE only and correct no earlier volume. To confirm, clone the repo and read `sql/*.sql` plus the `UpdateBalances` SQL directly, or use an authenticated GitHub API call / jsDelivr CDN mirror.
- **Version drift in code reads.** The fully-readable source is the Aug-2024 `northstar-pay/nucleus` fork (a public Apache-2.0 fork of `blnkfinance/blnk`); v0.15.x specifics (big.Int, per-txn inflight lock, coalescing, hot-lane, backpressure, hash chain, immutability trigger, queued inflight commit/void) are corroborated from v0.15.x docs and SDK notes, but individual v0.15.x function bodies (e.g., whether balance+row are now wrapped in one DB transaction) are SOURCE-CODE INFERENCE where marked. If v0.15.x already wraps the two writes atomically, Findings 2–3 and the worst partial-success rows soften — verify against the current `transaction.go` before building.
- **Issue-tracker evidence is thin.** The GitHub issue listing was reachable but individual runtime bug reports (duplicate/stuck/drift) were not retrievable in detail; the partial-success and double-apply hazards are derived from code structure and documented recovery behaviour, not from a confirmed production incident report.
- Blog/README claims are treated as MAINTAINER CLAIM throughout; documentation-vs-source divergences (float ingress vs "integer minor units" marketing; webhook "immutability/idempotency" advice that pushes responsibility to the caller) are reported as findings, not smoothed over.

---

# VOLUME IV — Implementation & Infrastructure Anatomy

```
Technology:              Blnk — open-source double-entry financial ledger
Technology type:         LEDGER
Primary repository:      https://github.com/blnkfinance/blnk
Version / release:       v0.15.0 (22 June 2026) pinned; patch line to v0.15.2 (31 July 2026)
Source openness:         OPEN SOURCE — Apache-2.0 ("Blnk Core")
Research date:           11 August 2026
Study objective:         BUILD EXTRACTION
Configuration:           EXTENDED 7
```

## What Blnk is made of, and what was bought rather than built

## EVIDENCE CEILING (read first)

This volume **broke the retrieval curse that crippled Volumes II and III.** The following routes worked and were used:

- **pkg.go.dev at the current module (Route 3) — WORKED, decisively.** `pkg.go.dev/github.com/blnkfinance/blnk@v0.15.2` and `.../database` returned the **complete current exported API surface with source-file paths and line numbers**, including the `Blnk`, `Queue`, `ChainProcessor`, `LineageOutboxProcessor`, `QueuedTransactionRecoveryProcessor` types, all `*big.Int` signatures, and the entire `database.Datasource` method set with the file each lives in.
- **GitHub `blob/v0.15.2/...` HTML pages via web_fetch — WORKED** once the URL was surfaced (pkg.go.dev embeds them). I read the **full verbatim source of `transaction_execution.go` (800 lines) and `transaction.go`** at tag v0.15.2, plus `metadata_test.go` and `docker-compose.yaml`.
- **Official docs and the config reference — WORKED** (docs.blnkfinance.com, blog).
- **jsDelivr (Route 1), the Go module proxy (Route 2), and raw.githubusercontent.com (Route 5) — did NOT work** in this environment (jsDelivr API URLs were not pre-surfaced; proxy.golang.org and raw host are robots-blocked).

**Therefore the evidence ceiling for Volume IV is: current v0.15.2 source, read directly, for the transaction-execution path, the exported API of every package, the datasource method catalogue (names, signatures, file+line, and pkg.go.dev doc comments), the deployment compose file, and the configuration reference.** This is a genuine v0.15.x reading, not the 2024 fork. Volume III's fork-based inferences are now superseded wherever they conflict.

**What remains UNCONFIRMED at the source level:** the raw DDL in `sql/`/`migrations/` (Debt 2) and the verbatim body of the lock package (Debt 3). My targeted subagent could not surface those specific blob URLs through the search→fetch gate. Crucially, however, **both debts are answerable from other current-source evidence** — the datasource method comments on pkg.go.dev, the execution-path source, and docs — so I resolve them below with the correct evidence label and flag exactly which sub-facts stay UNKNOWN. **The schema DDL is now unconfirmed for a third time; per the framing note I say so unambiguously and stop inferring column types I cannot see.**

---

## TL;DR

- **Debt 1 is resolved in the reader's favour.** In v0.15.2 the balance write and the transaction-row insert are **wrapped in a single database transaction.** `recordTransactionSingle` calls one datasource method — `RecordTransactionWithBalancesAndOutbox(ctx, txn, sourceBalance, destinationBalance, outbox)` — and the source comment states the transaction and balances are *"persisted atomically."* The two-call `updateBalances`-then-`persistTransaction` ordering that produced Volume III's worst partial-success rows **no longer exists on the main path.** A cooperative-society ledger can use this without the atomicity patch Volume III demanded — but must still turn on the hash chain and confirm the schema (below).
- **The most fundamental implementation choice is the `database.IDataSource` interface with a small set of composite atomic-write methods** (`RecordTransactionWithBalancesAndOutbox`, `...WithBalanceSetAndOutboxes`) layered over the Go stdlib `database/sql` + `lib/pq`, with **no ORM.** Correctness lives in those composite methods and in the schema; performance lives in the coalescing/hot-lane batch path (`TryRecordQueuedTransactionBatch*`). The most operationally important dependency is **PostgreSQL** (source of truth); the most operationally *dangerous-if-stopped* dependency is the **Redis/asynq worker fleet plus the background chain/outbox/recovery processors.**
- **Debt 2 (schema) and Debt 3 (lock) are answered at the behavioural/interface level but the raw DDL and lock body remain unread.** The lock is a Redis **`redlock`** package (not `internal/lock` as prior volumes assumed) using a `MultiLocker` that **locks BOTH source and destination balance IDs, sorted lexicographically and de-duplicated**, before any balance mutation — a real improvement over the fork's source-only lock. The money column type (NUMERIC vs BIGINT) and the immutability trigger's exact DDL are **still UNKNOWN** and must be read from `sql/` before trusting the ledger with members' savings.

---

## Key Findings

1. **Single atomic write on the main path (CONFIRMED IMPLEMENTATION).** `recordTransactionSingle` (in `transaction_execution.go`) applies the transaction to balances *in memory* (`processBalances` → `applyTransactionToBalances` → `model.UpdateBalances`), then persists everything through **one** datasource call, `RecordTransactionWithBalancesAndOutbox`. The comment on `processBalances` says explicitly: *"The actual database update of balances is done atomically with the transaction persistence step to ensure consistency."* The persist helper logs *"Transaction and balances persisted atomically."*

2. **The lock now covers both balances (CONFIRMED IMPLEMENTATION, execution source).** `executeWithLock` resolves `@`-indicator balances to IDs *before* locking, then `acquireLock` builds a `redlock.NewMultiLocker(l.redis, []string{sourceBalanceID, destinationBalanceID}, model.GenerateUUIDWithSuffix("loc"))`. The comment: *"MultiLocker handles deduplication (if source == destination) and sorts keys lexicographically"* — deterministic ordering to prevent deadlock. This **closes the fork gap** where only `transaction.Source` was locked and the destination relied on optimistic `version` alone.

3. **The lineage outbox is now on the atomic write path (CONFIRMED IMPLEMENTATION).** Volume III found webhooks fire from a detached goroutine with *no outbox on the main path*. That is now only half true: the **lineage** outbox IS written transactionally — `buildTransactionExecutionWork` calls `prepareTransactionOutbox`, and the outbox row is inserted inside `RecordTransactionWithBalancesAndOutbox`. A `LineageOutboxProcessor` background worker (`ClaimPendingOutboxEntries` using `SELECT FOR UPDATE SKIP LOCKED`) drains it. **Webhooks, however, still fire from a detached goroutine in `postTransactionActions` with no outbox** — so webhook delivery is still best-effort.

4. **`RecordTransaction` (the public method) bypasses the coalescing planner; the worker path uses it.** `RecordTransaction` calls `executeTransactionPlan(planTransactionExecution(txn, false, false))` → single mode. Queued/worker processing calls `ProcessQueuedTransaction(ctx, txn, hotLane)` → `planTransactionExecution(txn, true, hotLane)`, which tries `TryRecordQueuedTransactionBatch` (coalescing) or `TryRecordQueuedTransactionBatchForHotLane`, and **fails open to the single path** if batching does not handle the item (SOURCE-CODE INFERENCE from the `executeTransactionPlan` fallback recursion).

5. **Idempotency is defence-in-depth (CONFIRMED IMPLEMENTATION).** `validateTxn` does a SELECT-then-check via `TransactionExistsByRef` (the TOCTOU window Volume III named), but it is now backstopped by `IsDuplicateReferenceError`, which matches PostgreSQL error `23505` on a constraint whose name contains `reference`. So a **unique index on `reference` is the real guarantee**; the SELECT is an optimization. v0.15.0 added `CommitInflightTransactionWithRef` specifically so *"a retry that re-commits the same amount collides on the unique reference index"* — the maintainers explicitly rely on the DB constraint for idempotency.

6. **Money is `*big.Int` end-to-end in Go (CONFIRMED IMPLEMENTATION).** Every amount signature on `Blnk` and `Datasource` (e.g. `CommitInflightTransaction(..., amount *big.Int)`, `GetQueuedAmounts(...) (debit, credit *big.Int, ...)`, `GetTotalCommittedTransactions(...) (*big.Int, ...)`, `Allocation.Amount *big.Int`) uses `math/big.Int`. The lossy `int64(Amount * Precision)` float multiply from the 2024 fork is gone; `precise_amount` is accepted directly as `*big.Int`. Zero-amount transactions are discarded and not persisted (`buildTransactionExecutionWork` returns `skipPersist` when `PreciseAmount.Cmp(big.NewInt(0)) == 0`).

7. **The hash chain is a real, separate, serialized background mechanism (CONFIRMED IMPLEMENTATION).** `ChainProcessor.Start/Stop/IsRunning` plus `Datasource.ChainPendingTransactions` — the doc comment: *"seals the next batch of unchained transactions into the global hash chain in a single DB transaction. It locks the one `chain_state` row FOR UPDATE (serializing every chainer instance)… links each onto the head via `model.ComputeChainHash`… advances `chain_state` — all atomically, so a crash mid-batch loses nothing."* There is a `VerifyChain` method and a `CountUnchainedTransactions` lag metric. This is a per-batch Merkle-style chain sealed asynchronously, **distinct from the per-transaction SHA-256 `hash` field** the docs describe.

8. **The datasource is hand-written SQL over `database/sql` + `lib/pq`, no ORM (CONFIRMED IMPLEMENTATION).** `Datasource{ Conn *sql.DB; Cache cache.Cache }`; `ConnectDB` *"establishes a database connection with pooling."* The presence of `InsertLineageOutboxInTx(ctx, tx *sql.Tx, ...)` proves explicit `*sql.Tx` transaction handles are threaded through composite writes. `pq.Error` code inspection confirms the raw driver.

9. **Queue backpressure and inflight-action idempotency are first-class (CONFIRMED IMPLEMENTATION).** `ErrQueueBackpressure` (*"queue backpressure: redis memory or pending task limit reached"*) rejects enqueues to keep Redis below OOM; `ErrInflightActionQueued` maps an asynq TaskID collision to HTTP 409 so a commit/void cannot be double-queued. `RecoverQueuedTransactions(ctx, threshold)` + `GetStuckQueuedTransactions` re-drive stuck QUEUED parents.

10. **Deployment is one image in three roles (CONFIRMED IMPLEMENTATION).** `docker-compose.yaml`: `server` runs `blnk migrate up && blnk start`; `worker` runs `blnk workers`; dependencies are `redis:7.2.4`, `postgres:16`, `typesense:29.0` (optional search), `jaeger` (OTLP tracing), optional `prometheus`. Migrations are applied at server boot by `blnk migrate up`.

---

## Details

### IV.1 Repository & artefact map
Single Go module `github.com/blnkfinance/blnk`, Apache-2.0, one binary in three roles. Root package `blnk` holds the domain logic as many topical files: `transaction.go` (types/constants only, 118 lines), `transaction_execution.go` (the record/lock/persist path, 800 lines), `transaction_inflight.go`, `transaction_bulk.go`, `balance.go`, `lineage.go`, `queue.go`, `queue_backpressure.go`, `reconciliation.go`, `identity.go`, `apikey.go`, `metadata.go`, `blnk.go` (the `Blnk` struct, `SQLFiles embed.FS`). Subpackages: `database/` (the `Datasource`/`IDataSource` layer, split across `db.go`, `transaction.go`, `transaction_queries.go`, `transaction_coalescing.go`, `transaction_filters.go`, `balance.go`, `chain.go`, `lineage.go`, `reconciliation.go`, `api_key.go`, `identity.go`, `ledger.go`, `account.go`, plus `database/mocks`), `model/`, `config/`, `api/`, `cmd/`, and `internal/` with `redlock` (the lock — **corrected package name**), `hooks`, `hotpairs`, `metrics`, `notification`, `search`, `cache`, `filter`, `apierror`, `request`, `pg-listener`, `pg-backups`, `redis-db`. The weight sits in `transaction*.go` (root) and `database/transaction*.go` + `database/balance.go` (which is >1700 lines).

### IV.2 Languages, runtimes, concurrency & memory model
Go (module path `github.com/blnkfinance/blnk`; **exact `go` directive UNKNOWN — go.mod not read**, but `math/big`, generics-free code, `golang.org/x/sync/semaphore`, and OTEL usage are consistent with a modern Go 1.2x). 49 direct imports at module root. Concurrency model: goroutine-per-async-task bounded by **`semaphore.NewWeighted`** — `asyncBulkSemaphore` = 100, `asyncTxnSemaphore` = 20 — and a `balanceMonitorSem` channel of capacity 32 that bounds concurrent monitor checks. **What this makes easy:** cheap fan-out for bulk and monitor work. **What it makes dangerous:** Go's shared-memory model means the *cached running-total balance* is only safe because the Redis `MultiLocker` serializes writers on both balance IDs; any code path that mutates a balance without going through `executeWithLock` reintroduces a lost-update race. The in-memory `model.UpdateBalances` mutation is fine only because it happens under the lock and is persisted atomically.

### IV.3 Critical source paths — named (literal trace)
- **Queued path:** API handler → `Blnk.QueueTransaction` → `Queue.Enqueue` (asynq, Redis) → returns `QUEUED` + `_q` reference → worker → `Blnk.ProcessQueuedTransaction(ctx, txn, hotLane)` → `processQueuedTransaction` → `executeTransactionPlan(planTransactionExecution(txn, true, hotLane))` → `TryRecordQueuedTransactionBatch[ForHotLane]` (coalescing) **or** fail-open to `recordTransactionSingle`.
- **Single/commit point:** `recordTransactionSingle` → `executeWithLock` (resolve IDs → `acquireLock` MultiLocker on [source,dest]) → `ExecutePreHooks` → `validateAndPrepareTransaction` (`validateTxn` = `TransactionExistsByRef`) → `processBalances` (in-memory `model.UpdateBalances`) → `buildTransactionExecutionWork` (+ `prepareTransactionOutbox`) → **`persistSingleTransactionExecutionWork` → `datasource.RecordTransactionWithBalancesAndOutbox` (ATOMIC)** → `runTransactionPostCommitWork` (monitors, post-hooks, `postTransactionActions` → indexing + webhook in detached goroutine).
- **Inflight commit path:** `CommitInflightTransaction[WithRef|WithQueue]` → `redlock.NewLocker(l.redis, "inflight-commit:<txnID>", token)` → `Lock(ctx, Config().Transaction.LockDuration)` → apply commit/void (`CommitInflightDebit/Credit` or `RollbackInflight*`) → atomic persist → `releaseSingleLock`.
- **Divergence from Volume III's logical trace:** Volume III described `processBalances` (updateBalances) running *before and separately from* `finalizeTransaction` (persistTransaction). **In v0.15.2 this is false:** `processBalances` is in-memory only, and there is a single atomic persist. This is the volume's central finding.

### IV.4 THE TRANSACTION-BOUNDARY QUESTION (Debt 1) — ANSWERED
**Yes, v0.15.x wraps the balance write and the transaction-row insert (and the lineage outbox) in a single database transaction (CONFIRMED IMPLEMENTATION at the call-site and interface level; the `BeginTx/Commit/Rollback` body inside `database/transaction.go` is INFERRED from `InsertLineageOutboxInTx(tx *sql.Tx)` and the "persisted atomically" doc comments, since that file's body was not read).** The exact sequence in `recordTransactionSingle`: lock → validate → in-memory balance apply → build work (incl. outbox) → **one** call `RecordTransactionWithBalancesAndOutbox` → post-commit side effects. On partial failure the single DB transaction rolls back, so there is **no durable one-sided state** of the kind Volume III's partial-success matrix feared. Worker idempotency against its own partial completion is provided by (a) the atomic write and (b) the unique `reference` index catching a re-driven QUEUED parent (`IsDuplicateReferenceError`). **Verdict for the reader: the atomicity patch Volume III mandated is no longer required on the main path.** Residual risk: the *webhook* is still fired post-commit from a detached goroutine (at-most-once), and the bulk atomic path (`CreateBulkTransactions` with `atomic:true`) relies on `RecordTransactionsWithBalanceSetAndOutboxes` — confirm that composite method's rollback semantics before relying on all-or-nothing bulk.

### IV.5 Algorithms & data structures
- **`*big.Int` arithmetic** for all money; precision applied as an integer multiplier (`precise_amount = amount × precision`), no float on the current ingress path. O(digits) big-int ops; edge case = zero amount is dropped.
- **Coalescing (v0.14.0 perf release):** `GetQueuedTransactionsForCoalescing` / `...ForSourceCoalescing` / `...ForDestinationCoalescing` with `maxQueuedCoalescingBatchSize = 10000` and scopes `pair`/`source`/`destination`; merges same-pair queued transactions into one batched persist to reduce lock churn on hot balances.
- **Hot-lane routing:** `TryRecordQueuedTransactionBatchForHotLane` + `CountQueuedTransactionsForPairLane` + `internal/hotpairs.RecordContention` — contended pairs are detected (a `HotpairsContentionTotal` metric) and routed to a batched lane.
- **Hash chain:** `model.ComputeChainHash` links each row onto a single global head; `chain_state` row locked `FOR UPDATE`; verified by `VerifyChain`; lag by `CountUnchainedTransactions`.
- **Lineage allocation:** constants `AllocationFIFO`, `AllocationLIFO`, `AllocationProp` (PROPORTIONAL); `Allocation{BalanceID, Amount *big.Int}`, `BalanceLineage`, shadow/aggregate balances via `LineageProviderKey`/`LineageFundAllocation` metadata keys.
- **Reconciliation matching:** `StartReconciliation`/`StartInstantReconciliation` with strategies + `MatchingRule`s; `FetchAndGroupExternalTransactions`, `GroupTransactions`.

### IV.6 SCHEMA RECONSTRUCTION (Debt 2) — PARTIAL; DDL STILL UNREAD (third time)
**Confirmed column names** (from the transactions SELECT list in a v0.15 datasource test): `transaction_id, parent_transaction, source, reference, amount, precise_amount, precision, rate, currency, destination, description, status, created_at, meta_data, scheduled_for, hash`. **Confirmed tables/relations** (from datasource methods): `blnk.balances`, `blnk.balance_monitors`, transactions, ledgers, identities, accounts, `chain_state`, a lineage **outbox** table, lineage mappings, reconciliations/matches/external transactions, api_keys, balance snapshots.
- **`precise_amount` / balance money column type: UNKNOWN.** Two prior volumes inferred NUMERIC; a third reading still could not open the DDL. The evidence is genuinely conflicting: a tutorial says amounts are stored "as integers," but the maintainers' own v0.10.1 note says `precise_amount` exists to hold values *"larger than 15 digits,"* which a 64-bit BIGINT cannot. **The evidence favours NUMERIC (or a big-integer-as-NUMERIC/TEXT), because the Go type is `*big.Int` and the stated goal exceeds int64 range — but this is ANALYTICAL INFERENCE, not confirmed, and must not be trusted for members' savings until the DDL is read.**
- **CHECK constraints on sign/magnitude/precision: UNKNOWN.**
- **Unique index on reference:** existence is **CONFIRMED behaviourally** (error 23505 on a `reference` constraint is the idempotency backstop), but whether it is **partial** or created **CONCURRENTLY** is **UNKNOWN** (DDL unread).
- **Immutability trigger (Volume III's lead):** the docs assert transactions "cannot be modified or deleted," and a DB-level trigger is the plausible mechanism, but **its name, protected columns, and on-violation behaviour (RAISE EXCEPTION) remain UNKNOWN** — the trigger SQL was not retrievable. Do not present the trigger as confirmed.
- **Schema-enforced invariants that ARE established:** the unique `reference` constraint (idempotency), the `UNIQUE` constraint on `identity_id` (the docs describe relying on it for safe concurrent identity creation → 409). Conservation and sign/overdraft rules appear enforced in **code** (`model.UpdateBalances`, `allow_overdraft`), not confirmably in the schema.

### IV.7 Persistence layer
Raw SQL, `database/sql` + `lib/pq`, connection pooling in `ConnectDB`, a `cache.Cache` on the `Datasource`. Composite atomic writers thread `*sql.Tx`. **Isolation level actually used: UNKNOWN for the transaction/balance write** (the `RecordTransactionWithBalancesAndOutbox` body was not read); the **chain sealer explicitly uses `SELECT … FOR UPDATE`** on `chain_state`, and the outbox drainer uses **`FOR UPDATE SKIP LOCKED`** — both CONFIRMED via doc comments. The optimistic `version` check on balances: whether it is a strict `WHERE version = ?` predicate is **UNKNOWN** (not visible in the execution file), but its role is now secondary because the `MultiLocker` serializes writers on both balances.

### IV.8 Networking & protocols
REST/JSON over HTTP (default port 5001; 80/443 exposed). Header auth `X-blnk-key`; scoped API keys (bcrypt-hashed, prefix lookup, 5-min cache). OTEL tracing to Jaeger (OTLP). **Default timeout/retry:** the SDKs default to a client timeout (e.g. `WithTimeout(5*time.Second)`, `WithRetry(2)`); server-side reconciliation config carries `max_retries: 3, retry_delay: 5`. **Amplification risk:** SDK retries combined with the QUEUED-by-default model and asynq's own `max_retries: 3` mean a slow downstream (webhook target, Typesense) can be retried at multiple layers — but the unique-reference index prevents duplicate money movement, so amplification degrades to wasted work, not double-spend.

### IV.9 Background work & failure consequences
- **Worker fleet (`blnk workers`, asynq):** the actual commit point for queued transactions. **If stopped: money never moves** — everything stays QUEUED; balances do not change (safe but frozen).
- **`ChainProcessor`:** seals the hash chain. **If stopped: chain lag grows** (`CountUnchainedTransactions` climbs); transactions still record, but tamper-evidence falls behind. Silent unless the lag metric is watched.
- **`LineageOutboxProcessor`:** drains lineage outbox (`FOR UPDATE SKIP LOCKED`). **If stopped: fund-lineage/shadow-balance views drift**; core balances stay correct.
- **`QueuedTransactionRecoveryProcessor` / `RecoverQueuedTransactions`:** re-drives stuck QUEUED parents past a threshold. **If stopped: transient worker crashes leave transactions stuck QUEUED indefinitely.**
- **Inflight-expiry job (`QueueInflightExpiry`):** auto-voids expired holds. **If stopped: authorization holds never expire**, tying up funds.
- **Balance snapshots (`TakeBalanceSnapshots`):** historical-balance/point-in-time queries degrade to full replay (`GetBalanceAtTime(..., fromSource=true)`).

### IV.10 Configuration surface & dangerous combinations
From `blnk.json` / `BLNK_` env vars. Confirmed transaction block: `batch_size: 100000, max_queue_size: 1000, max_workers: 10, lock_duration: 1800 (s), index_queue_prefix: "transactions"`; reconciliation `max_retries: 3, retry_delay: 5`; a `Transaction.EnableQueuedChecks` flag (controls whether balance reads include queued amounts and use `GetBalanceByID` vs the faster `GetBalanceByIDLite`); `skip_queue: true` forces synchronous APPLIED/VOID. Carried-forward defaults (Vol III): 20 queues, 3 max retries, 5 s retry delay, 1800 s lock, 3 s lock wait.
**Dangerous combinations:**
- **Hash chain off by default + high throughput** → long tamper-evidence gap that is invisible until an audit. For members' savings, **turn the chain on and monitor `CountUnchainedTransactions`.**
- **`lock_duration: 1800s` + a crashed worker holding a balance lock** → that balance is frozen for up to 30 minutes. The 1800 s TTL is a safety net, not a target; too long jams hot balances, too short risks a slow legitimate txn losing its lock mid-flight.
- **`skip_queue: true` under concurrency** → the docs explicitly warn of lock errors; callers must handle "failed to acquire lock."
- **`EnableQueuedChecks` off** → sufficient-funds checks may not account for in-flight queued debits, permitting transient over-commit on a hot source balance. For savings, **keep queued checks on.**
- Nothing in the observed code *prevents* these jointly; they are operator responsibilities.

### IV.11 Build, test & release
GitHub Actions (`go.yml` build/test, `docker-publish.yml`, `lint.yml`). Semantic-ish versioning (still 0.x, "not stable" per pkg.go.dev). Cadence: v0.15.0 (22 Jun 2026) → v0.15.2 (28–31 Jul 2026) — patch releases weeks apart; feature adds tagged per method ("added in v0.13.0/v0.14.0/v0.15.0"). Migrations applied via `blnk migrate up` at boot from the embedded `SQLFiles embed.FS`. **Reversibility of migrations: UNKNOWN** (migration files unread). Compatibility promise: none formal below v1.

### IV.12 TESTS AS EXECUTABLE SPECIFICATION
Read: `metadata_test.go` (uses `database/mocks.MockDataSource`, `stretchr/testify`) — asserts ID-prefix → entity routing (`txn_`/`bulk_`→transactions, `bln_`→balances, `ldg_`, `idt_`), metadata merge/override semantics, and that transaction metadata update goes through `TransactionExistsByIDOrParentID`. `database/transactions_test.go` exists (uses `DATA-DOG/go-sqlmock`) and pins the exact transactions column list — a de-facto schema spec. **Documentation-vs-test contract:** the docs call transactions "immutable," yet `UpdateTransactionMetadata`/`UpdateMetadata` explicitly mutate `meta_data` — so **immutability applies to the accounting columns, not to metadata**; the tests reveal metadata is deliberately mutable. **Untested/thin (reader's exposure):** I found no evidence in the read tests of coverage for concurrent duplicate-reference races end-to-end, for `MultiLocker` deadlock ordering, for partial-failure rollback of `RecordTransactionWithBalancesAndOutbox`, or for the immutability trigger — these are exactly the correctness-critical paths and their test status is **UNKNOWN**; treat them as unproven until you read `transaction_execution_test.go`/`database/transaction*_test.go`.

### IV.13 Deployment reconstruction
`docker-compose.yaml`: `server` (`blnk migrate up && blnk start`, ports 5001/80/443), `worker` (`blnk workers`, port 5004), `redis:7.2.4`, `postgres:16` (with `pg_isready` healthcheck, `pg_data` volume), `typesense:29.0` (optional, healthchecked), `jaeger` (OTLP 4317/4318, UI 16686), optional `prometheus` (profile `monitoring`). Both app roles mount the same `blnk.json`. A separate `blnk-infrastructure` repo provides Terraform (AWS RDS/ElastiCache/ALB, Azure, GCP) and Kubernetes manifests.

### IV.14 Infrastructure dependencies & minimum viable deployment
**Required to run at all:** the `blnk` binary + **PostgreSQL** + **Redis**. **Smallest configuration that merely starts:** `blnk start` with Postgres + Redis and a minimal `blnk.json` (`data_source.dns`, `redis.dns`, `server.port`). **Smallest genuinely functional configuration:** that **plus a running `blnk workers` process** — because transactions are QUEUED by default and the worker is the real commit point, an instance with no worker *accepts* transactions but never applies them. So MVP = 1 server + 1 worker + Postgres + Redis. Typesense and Jaeger are optional. For members' savings, add: hash chain enabled, the recovery + inflight-expiry + chain + outbox processors confirmed running, and Postgres backups.

### IV.15 Build, buy or open source
- **Money math:** BUILT on Go stdlib `math/big` (adopted the primitive, built the domain logic).
- **Locking:** REIMPLEMENTED — a bespoke `internal/redlock` `MultiLocker` on Redis rather than adopting an off-the-shelf redsync/redislock. **Why:** they needed *multi-key, deterministically-ordered, deduplicated* balance locking with a config-driven TTL and a wait timeout tuned for hot balances — semantics generic libraries don't package. This is a load-bearing reimplementation.
- **Queue:** ADOPTED `hibiken/asynq` (Redis-backed).
- **Persistence:** BUILT hand-written SQL over `database/sql`+`lib/pq`; **rejected an ORM** — because the correctness-critical composite writes (`RecordTransactionWithBalancesAndOutbox`) need exact control of the transaction boundary an ORM would obscure.
- **Migrations:** BUILT — embedded `embed.FS` + `blnk migrate up`, rather than adopting golang-migrate visibly.
- **Search:** ADOPTED Typesense (optional). **Tracing/metrics:** ADOPTED OpenTelemetry/Jaeger/Prometheus. **Hash chain, coalescing, hot-lane, outbox, backpressure:** all BUILT — they encode the "hot balance" constraint the project could not satisfy with a stock ledger.

### IV.16 Build-extraction verdicts
- **Go + `*big.Int` money:** **ADOPT.** Correct because of the mechanism itself (exact integer arithmetic); portable to any reimplementation.
- **Single atomic composite write (`RecordTransactionWithBalancesAndOutbox`):** **ADOPT — this is the load-bearing pattern.** Works because of the mechanism (one DB transaction), not the environment. Any ledger for savings **must** reproduce it.
- **`internal/redlock` MultiLocker (both balances, sorted, dedup):** **ADAPT.** The multi-key ordering is essential and reproducible; the specific TTL/wait values (1800 s / 3 s) are environment-tuned for high-throughput hot balances and should be re-tuned for a cooperative-society workload.
- **Embedded-schema `migrate up`:** **ADAPT** — convenient, but confirm reversibility and run migrations as a deliberate step, not silently at every server boot, in production.
- **`database.IDataSource` abstraction:** **ADOPT** — the interface is what makes the atomic composite methods and mock-based tests possible.
- **asynq dependency + QUEUED-by-default:** **ADAPT.** Works because of the surrounding worker/recovery ecosystem; a reimplementation that adopts asynq must also reproduce the recovery + backpressure + inflight-expiry jobs, or it inherits "stuck QUEUED" and Redis-OOM failure modes.
- **Test coverage as reimplementation spec:** **ADAPT** — mirror the ID-routing/metadata tests, but you must **add** the concurrency/partial-failure/trigger tests the current suite appears to lack.

### IV.17 Volume IV reconstruction — synthesis answers
- **Most fundamental implementation choice:** the atomic composite datasource write (`RecordTransactionWithBalancesAndOutbox`) behind `IDataSource` — it converts the fork's two-write hazard into a single transactional boundary and is the reason the ledger is safe to use for savings.
- **Most operationally important dependency:** **PostgreSQL** (source of truth and the transactional boundary itself). Redis/asynq is a close second and is the most dangerous-if-stopped.
- **Where domain correctness is actually enforced:** **split.** Conservation, sign/overdraft, and precision are enforced in **code** (`model.UpdateBalances`, `applyTransactionToBalances`, `allow_overdraft`). Idempotency/uniqueness and identity uniqueness are enforced in the **schema** (unique indexes). Full immutability *should* be enforced by a DB trigger but that is **UNKNOWN/unconfirmed**. Isolation-level enforcement of concurrent conservation is **UNKNOWN** and currently substituted by the Redis lock — i.e. partly "nowhere in the DB, everywhere in Redis," which is a real caveat.
- **Performance-critical path:** the coalescing/hot-lane batch path (`ProcessQueuedTransaction` → `TryRecordQueuedTransactionBatch[ForHotLane]`, `maxQueuedCoalescingBatchSize = 10000`, `hotpairs` contention routing).
- **What tests guarantee that docs don't mention:** metadata is mutable (contradicting the blanket "immutable" claim) and metadata updates are gated on existence checks; ID-prefix routing is a hard contract.
- **Incidental vs fundamental:** *Incidental* — Typesense/Jaeger/Prometheus choices, the exact 20-queue/10-worker numbers, the `_q` reference suffix cosmetics. *Fundamental* — the atomic composite write, the dual-balance MultiLocker with deterministic ordering, `*big.Int` money, the unique-reference idempotency backstop, and the QUEUED-by-default worker-is-commit-point model.

---

## Recommendations (staged, with thresholds)

1. **Before writing a line of integration code, read three files and close the two open debts.** Fetch `sql/`/`migrations/*.sql`, `internal/redlock/*.go`, and `database/transaction.go`. Confirm: (a) `precise_amount`/balance columns are **NUMERIC** (not BIGINT); (b) the immutability trigger exists, its protected columns, and that it `RAISE`s on UPDATE/DELETE; (c) the isolation level inside `RecordTransactionWithBalancesAndOutbox`. **Threshold to proceed to production for members' savings: all three confirmed.** If the money column turns out to be BIGINT, cap amounts or patch to NUMERIC before go-live.
2. **Deploy the minimum *functional* topology, not the minimum *starting* one:** ≥1 `server` + ≥1 `worker` + Postgres + Redis, and verify via `IsRunning()` that `ChainProcessor`, `LineageOutboxProcessor`, `QueuedTransactionRecoveryProcessor`, and the inflight-expiry job are all live. **Alert if any reports not-running for >1 minute.**
3. **Turn the hash chain ON and alert on `CountUnchainedTransactions` lag** (threshold: sustained backlog growth over, say, 10 minutes means the chainer is falling behind).
4. **Tune the lock:** re-evaluate `lock_duration` (1800 s is for hot marketplaces; a cooperative's contention is lower — a shorter TTL reduces freeze-on-crash blast radius) and keep the 3 s lock-wait. Keep `EnableQueuedChecks` ON so sufficient-funds accounts for queued debits.
5. **Do not rely on webhooks for financial state** — they fire from a detached goroutine, at-most-once. Reconcile from the ledger (or add an outbox on the webhook path) for anything money-critical.
6. **Add the missing tests before trusting the code:** concurrent duplicate-reference, MultiLocker deadlock ordering, partial-failure rollback of the composite write, and the immutability trigger. **Threshold: these must pass in your fork before onboarding real members' funds.**

## Caveats
- **The raw DDL was not read for the third consecutive volume.** Money column type, CHECK constraints, the reference index's partial/CONCURRENTLY status, and the immutability trigger's exact definition are **UNKNOWN**; my NUMERIC lean is ANALYTICAL INFERENCE. Stop treating NUMERIC as fact until `sql/` is opened.
- **The lock package body (`internal/redlock`) was not read.** The MultiLocker's dual-balance/sorted/dedup behaviour and the config-driven TTL are CONFIRMED from the execution source and doc comments, but the exact Redis command (`SET NX PX`), retry interval, and failure sentinel are inferred from the pattern, not quoted. Note the corrected package name: it is **`redlock`**, not `internal/lock`.
- **The interior of `RecordTransactionWithBalancesAndOutbox` (the `BeginTx/Commit/Rollback` envelope and isolation level) is inferred**, not read — but the atomicity conclusion is well-supported by the single call site, the "persisted atomically" comments, and the `InsertLineageOutboxInTx(tx *sql.Tx)` signature.
- Test-coverage gaps (concurrency, partial failure, trigger) are **UNKNOWN**, not confirmed-absent; I read only a subset of `_test.go` files.
- README/blog/docs statements (immutability, "incredibly fast," precision claims) are treated as MAINTAINER CLAIM. The one blog "stores amounts as integers" line conflicts with the "larger than 15 digits" maintainer note and is explicitly left unresolved above.

---

# VOLUME V — Correctness, Performance, Scale & Reliability

---

## TL;DR

- **Strongest guarantee: per-transaction atomicity and value conservation on the main (queued) write path.** Since Volume IV confirmed the single composite datasource write `RecordTransactionWithBalancesAndOutbox(...)` ("persisted atomically"), a posted transaction either moves both balances and records the row, or neither. This is *structural* and CONFIRMED IMPLEMENTATION. **Weakest guarantee: read-your-writes / freshness on the default path (not guaranteed) and tenancy + resource isolation (not enforced at all).** Because the API returns `QUEUED` before money moves, a caller has no guarantee that a subsequent read reflects the transaction until a worker commits — and one noisy cooperative can starve another because there is no per-tenant QoS.
- **Primary scaling bottleneck: the single hot destination balance.** A pooled cooperative contribution account (many members → one account) is a hot balance *by construction*. Every writer to it must acquire the same Redis lock (`internal/redlock` MultiLocker) and pass an optimistic version check; they serialise. **Adding workers does not speed up a contended balance and can worsen contention/retries.** The documented remedies — queueing, coalescing, hot-lane routing, and above all *balance sharding* — manage the symptom; only sharding removes the bottleneck.
- **After saturation Blnk sheds load rather than collapsing.** Since v0.15.2, when Redis memory or pending-task count exceeds limits, new enqueues are rejected with **HTTP 503 / `error_detail.code = QUEUE_BACKPRESSURE`** (backpressure enabled by default). Work already accepted into Redis is retained and drained; nothing already committed is lost. The exposure is that the queue and locks live in Redis, so a Redis loss without persistence loses queued-but-undrained work. **The single most important finding for a savings ledger: a silent balance drift would NOT automatically raise an alarm** — correctness detection (balance reconstruction, hash-chain verification) is entirely opt-in and off by default.

---

## Key Findings

1. **Atomicity is the load-bearing guarantee and it now holds structurally.** Volume III's two-write partial-success hazard is gone: balances are mutated in memory then persisted through one datasource call the source comments describe as *"persisted atomically."* This is the reader's single best reason to trust Blnk with money.

2. **The "up to about 5×" performance claim is a MAINTAINER CLAIM, not a measurement.** The v0.14.0 changelog (Apr 9 2026) states verbatim: *"In internal benchmarks under heavy contention and burst load, processing throughput improved by up to about 5×; your results depend on workload shape, how much traffic overlaps on the same balances, and how you configure the server."* No hardware, dataset size, concurrency level, or measured metric (TPS? p99?) is stated. It fails the volume's stated-conditions test and must be treated as marketing, not evidence.

3. **The money column type remains PERMANENTLY UNKNOWN.** After four volumes and a dedicated extraction subagent, the PostgreSQL DDL in `database/balance.go`, `database/transaction.go`, and `sql/` could not be read (GitHub blob/raw fetches blocked by robots; code-search hits never surfaced). This is now declared permanently unknown for the study. **Consequence for the reader: the representable range of a balance cannot be confirmed.** If the column is `BIGINT`, there is a silent truncation boundary at ±(2⁶³−1) ≈ ±9.22×10¹⁸ minor units that `*big.Int` in Go cannot rescue at the storage layer; if `NUMERIC`, the range is effectively unbounded for financial use. Documentary evidence (docs: *"Balance fields are integers in minor units"*; the `precise_amount` field exists specifically to *"record amounts exceeding 15 digits"* — example `precise_amount: 189207535698279000, precision: 1000000000000000000` for ETH; `precise_amount` handled as a *string* in test mocks) leans toward `NUMERIC`, but this is ANALYTICAL INFERENCE, not confirmed.

4. **Idempotency is defence-in-depth and its storage-layer anchor is named.** The v0.13.2 changelog confirms a unique database index `idx_transactions_reference_unique` on `transactions.reference`. The application `validateTxn` SELECT-then-check is an optimisation over a TOCTOU window; the *real* guarantee is the PostgreSQL `23505` unique-violation caught by `IsDuplicateReferenceError`. Duplicate references are rejected structurally.

5. **Concurrency safety on a single balance is enforced by check, in three layers, none of which is the database transaction isolation level.** Redis distributed lock (serialise) → lock-wait-timeout (absorb brief contention) → optimistic version check on the balance (reject stale writes at write time). The blog states verbatim: *"Blnk still performs an optimistic version check when writing the balance… The version check provides the final database-level protection by rejecting a write if the balance changed after it was read."*

6. **The lock TTL is long enough to be a real correctness risk.** Default `lock_duration` is **1800 seconds**. If a lock expires mid-operation (worker stall, GC pause, slow DB), the *only* serialisation is gone and two writers can proceed concurrently; the optimistic version check is then the last defence against a lost update. v0.15.1 explicitly fixed *"an overflow bug when applying `BLNK_TRANSACTION_LOCK_DURATION`"* — evidence this parameter has been fragile.

7. **Load-shedding is graceful and default-on.** `QUEUE_BACKPRESSURE` (HTTP 503) is the deliberate mechanism, confirmed in the v0.15.2 changelog. Bounded concurrency (`asyncBulkSemaphore=100`, `asyncTxnSemaphore=20`, `balanceMonitorSem=32`) prevents unbounded fan-out inside a node.

8. **Correctness observability is opt-in and would miss a silent drift.** OpenTelemetry/Jaeger/Prometheus cover *availability* and latency; `CountUnchainedTransactions` and `HotpairsContentionTotal` are emitted. But the two instruments that detect a *correctness* failure — balance reconstruction (`BLNK_RUN_RECONCILIATION`) and the hash chain (`verify-chain`) — are manual and off by default. Nothing in the default deployment continuously compares a stored balance against the sum of its transaction history.

9. **Retry amplification is a live risk.** Retries exist at the SDK layer (`WithRetry`), the asynq queue layer, and the application layer simultaneously. Stacked, they can multiply load against an already-contended balance rather than absorbing a transient fault. The documented reconciliation defaults (`max_retries: 3`, `retry_delay: 5`) illustrate the pattern; transaction-queue retry defaults were not independently verifiable.

10. **Durability in the OSS build rests on assumptions Blnk does not itself verify.** Backup is a `pg_dump`→S3 cron calling the `/backup-s3` endpoint, restored with `pg_restore`. There is no built-in WAL archiving / point-in-time recovery in Core; that is a PostgreSQL responsibility the operator must configure. Worst permitted loss is bounded by backup cadence (a daily cron ⇒ up to ~24h RPO) plus any queued-but-undrained Redis work lost on a Redis failure.

---

## Details

### V.1 — The Guarantee Ledger (ranked)

For each guarantee: statement · holds when · fails when · enforcement (structurally / by check / by convention / not enforced, per Volume III, updated for Volume IV) · evidence class.

| Rank | Guarantee | Holds when | Fails / does not hold when | Enforcement | Evidence |
|---|---|---|---|---|---|
| **1 (strongest)** | **Atomicity + conservation** — a posted transaction moves both balances and records the row, or neither; debits equal credits | Main path, single composite write `RecordTransactionWithBalancesAndOutbox` | Multi-leg/bulk flows split across commits; crash *before* the composite write leaves the txn `QUEUED` (see V.16) | **Structurally** (single datasource call, "persisted atomically") | CONFIRMED IMPLEMENTATION (Vol IV) |
| 2 | **Immutability** of posted transactions | Whatever DB protection exists is active | If enforced only in app code and DB is written directly | **By DB protection** (v0.10.1 added "database protections to prevent unauthorized changes to transactions"); trigger definition **UNKNOWN** | DOCUMENTED BEHAVIOR; trigger UNKNOWN |
| 3 | **Idempotency** — a unique `reference` applies once | `reference` supplied and unique | Caller reuses `_q`-suffixed refs carelessly; pre-v0.13.2 deployments | **Structurally** — unique index `idx_transactions_reference_unique` + PG `23505` | CONFIRMED / DOCUMENTED |
| 4 | **Precision integrity** — no float loss in Go | All arithmetic in `*big.Int` | *Storage* range unknown (see V.3); inconsistent per-currency `precision` supplied by caller | **Structurally in Go**; storage **UNKNOWN** | CONFIRMED (Go) / UNKNOWN (DDL) |
| 5 | **Concurrency safety** on one balance | Queue used; lock acquired; version unchanged | Lock lost/expired mid-op (1800s TTL); `skip_queue:true` under contention → "Failed to acquire lock" | **By check** — Redis lock + optimistic version | DOCUMENTED / SOURCE-CODE INFERENCE |
| 6 | **Sufficient funds** unless overdraft | Overdraft not enabled; inflight included (v0.11.0) | `allow_overdraft:true`; TOCTOU if lock lost | **By check** | DOCUMENTED |
| 7 | **Zero / malformed rejected** | Standard path | — (zero-amount dropped before persistence; non-integer precision rejected v0.11.3) | **By check** | CONFIRMED (Vol IV) |
| 8 | **Tamper-evidence** (hash chain) | Chain *enabled* and verified | **Off by default**; lag if `ChainProcessor` stalls | **By convention** (opt-in) | CONFIRMED (Vol IV) |
| **9 (weakest)** | **Consistency / read-your-writes** and **tenancy + resource isolation** | Read-your-writes only with `skip_queue:true`; tenancy only via ledger partition + API-key scope | Default queued path: read after `QUEUED` may not reflect the write; **no per-tenant QoS at all** | **Not guaranteed / not enforced** | DOCUMENTED / ANALYTICAL |

**Ranking rationale.** Blnk is marketed on its strongest properties — "immutable, correct, double-entry" — and those largely hold. It is most likely to be *broken through* its weakest: a caller who assumes read-your-writes on the default queued path, or an operator who assumes tenant isolation that does not exist. For a cooperative ledger, the practical danger is not that a transaction is lost, but that a balance read looks wrong for a window, or that one society's bulk import degrades another's live contributions.

### V.2 — Correctness specification (invariants as assertable conditions)

- **INV-1 Conservation:** for every applied txn, `Δsource + Δdestination = 0` in minor units. *Structural.*
- **INV-2 Balances change only via transactions:** no API mutates a balance amount directly; `CreateBalance` starts at 0. *Structural / by check.*
- **INV-3 Derivability:** `balance = Σ(credits) − Σ(debits)` reconstructable from history (`from_source=true`, `BLNK_RUN_RECONCILIATION`). *Structural but only checked on demand.*
- **INV-4 Idempotency:** `COUNT(*) WHERE reference = X ≤ 1`. *Structural (unique index + 23505).*
- **INV-5 Immutability:** an UPDATE/DELETE on an applied txn is rejected. *By DB protection; exact trigger UNKNOWN.*
- **INV-6 Valid transitions:** `QUEUED→APPLIED|REJECTED`, `INFLIGHT→APPLIED|VOID`; no back-transition. *By check.*
- **INV-7 Precision integrity:** amounts stored as integers in minor units; Go arithmetic in `*big.Int`. *Structural in Go; storage range UNKNOWN.*
- **INV-8 Sufficient funds:** `source.balance − amount ≥ −overdraft_limit` unless `allow_overdraft`. Inflight included since v0.11.0. *By check.*
- **INV-9 Concurrency safety:** concurrent writers to one balance serialise; `version` monotonic. *By check.*
- **INV-10 Zero/malformed rejected:** zero-amount dropped; non-integer precision rejected. *By check.*
- **INV-11 Tamper-evidence:** `ComputeChainHash(prev, txn) = stored hash`. *By convention (opt-in).*
- **INV-12 Authorisation/tenancy:** API-key scopes + ledger partitioning only. *By check for authz; tenancy not enforced.*

### V.3 — Numerical and precision semantics

Money is `*big.Int` end-to-end in Go (the lossy `int64(Amount × Precision)` float multiply from the 2024 fork is gone). `precision` converts display units to minor units (e.g. 100 for USD → cents); `precise_amount` exists to carry values *"exceeding 15 digits"* (docs; e.g. `precise_amount: 189207535698279000, precision: 1000000000000000000` for ETH). Balance responses return integers in minor units — docs state verbatim *"Balance fields are integers in minor units"* with `display_amount = balance / precision`.

**Rounding:** distribution across multiple sources/destinations uses rounding support (v0.8.1); `precise_distribution` (v0.12.2) allows exact splits, indicating the default path can round split remainders. Direction of rounding is not documented precisely — treat as UNKNOWN and use `precise_distribution` where exactness matters.

**Inconsistent precision for the same currency:** `precision` is a *per-transaction* parameter applied to the balance. If a caller supplies different `precision` values for the same currency across transactions, the minor-unit interpretation of that balance becomes ambiguous — Blnk does not enforce a single canonical precision per currency. *Caller discipline required.* This is a real hazard for a cooperative mixing, say, `100` and `1000` for the same currency.

**Representable range — the practical consequence of the unresolved DDL:**
- If the balance columns are **NUMERIC**: range is effectively unbounded; `*big.Int` and storage agree. (Documentary evidence leans this way.)
- If they are **BIGINT**: a silent truncation/overflow boundary exists at **±(2⁶³−1) ≈ ±9,223,372,036,854,775,807 minor units** (~±9.22×10¹⁸). At `precision = 10¹⁸` (ETH-style), that is only ~9.2 whole units — a real risk for high-precision assets. Go's `*big.Int` would compute correctly but the write could overflow/truncate at the column.

**Verdict (stated as a range with caveat, as required):** the representable balance range is **either effectively unbounded (NUMERIC) or ±~9.22×10¹⁸ minor units (BIGINT)** and *cannot be resolved from available sources*. A reader building a cooperative ledger in a low-precision fiat currency (USD `precision=100`) is safe under either type up to ~$9.2×10¹⁶ — far beyond any cooperative. A reader handling crypto or very high `precision` **must confirm the column type in their own deployment before trusting large balances.**

### V.4 — Consistency guarantees (in caller terms)

- **Default (queued) path:** the API returns `QUEUED` with a `_q`-suffixed reference *before money moves*. **There is no read-your-writes guarantee.** A read immediately after `QUEUED` may show the pre-transaction balance (queued balances are surfaced separately via `queued_credit_balance` / `queued_debit_balance` and `?with_queued=true`, precisely because the applied balance is not yet updated). The real commit is inside the worker.
- **How long until visible:** bounded by queue drain time, which under contention is bounded by lock-wait + processing per predecessor — i.e. *not a fixed SLA*; it is workload-dependent. A caller must poll `GET /transactions/reference/{ref}_q` or the transaction ID until `status = APPLIED`, or subscribe to the state-change webhook.
- **`skip_queue:true`:** synchronous apply ⇒ read-after-write within the same request path, at the cost of exposing lock-contention failures directly to the caller.
- **Stale reads / replication:** Blnk is single-source-of-truth PostgreSQL; if the operator runs read replicas, replica lag introduces additional staleness Blnk does not manage. Session consistency is not offered.

**Caller rule:** *treat `QUEUED` as "accepted, not yet true." Never render a balance to a member from a read taken immediately after posting; poll for `APPLIED` or use the webhook.*

### V.5 — Atomicity and isolation

- **Scope:** one composite datasource write per transaction ("persisted atomically"); the `BeginTx/Commit/Rollback` envelope was inferred, not read (Vol IV).
- **Serialisation point:** the Redis `MultiLocker` over `[sourceBalanceID, destinationBalanceID]`, deduped when source==destination and **lexicographically sorted** to prevent deadlock. Inflight commits use `inflight-commit:<txnID>`.
- **Isolation level inside the composite write: UNKNOWN.** This matters: if Blnk uses PostgreSQL's default **READ COMMITTED** (likely, since it relies on the Redis lock + optimistic `version` for correctness rather than DB isolation), then the DB alone permits lost updates and read/write skew — the Redis lock is doing the serialisation work. That is safe *while the lock holds*.
- **What the lock actually guarantees:** mutual exclusion over the *pair* of balances, in a global lexicographic order, so no path that uses `MultiLocker` can deadlock with another. The residual risk is any code path that acquires balance locks *outside* the MultiLocker ordering — not observed in extracted source, but not exhaustively proven (test coverage of MultiLocker ordering is UNKNOWN, per Vol IV).
- **Anomalies prevented (lock held):** lost update, write skew, double-spend on a single balance.
- **Anomalies that remain possible:** (a) **lost update if the lock expires mid-operation** (1800s TTL) — then only the optimistic `version` check protects; if the stale writer's version check also races, a lost update is theoretically possible; (b) **read skew / phantoms across multiple balances** read outside a single locked scope (e.g. reporting queries); (c) staleness on the queued path (V.4).

### V.6 — Concurrency under stress (at the contention point, not the average)

The reader's pooled contribution account is an **N→A hot destination** by construction. Behaviour by writer count against one destination:

- **~10 concurrent writers:** queue absorbs them; workers serialise on the destination lock; each waits briefly (lock-wait-timeout, default 3s). Latency to `APPLIED` rises modestly; failures rare. Caller sees `QUEUED` immediately, `APPLIED` shortly after.
- **~100 concurrent writers:** lock queue depth grows; without coalescing, 100 sequential read-lock-write cycles on one balance. **Coalescing** (v0.14+, `BLNK_TRANSACTION_ENABLE_COALESCING`) batches transactions sharing source+destination+currency into one commit, collapsing repeated lookups/commits — highly effective for N→A into one account. **Hot-lane routing** (v0.14+) may activate if this pair shows repeated contention, isolating it from the rest of the queue (`HotpairsContentionTotal` metric increments). Some `skip_queue:true` callers would see "Failed to acquire lock."
- **~1000 concurrent writers:** the single balance is the hard ceiling. Coalescing + hot lane keep it *correct and moving* but throughput on that one balance is bounded by serial commit rate. If Redis memory/pending-task limits are hit, `QUEUE_BACKPRESSURE` (503) sheds new enqueues. The documented, and only real, fix is **balance sharding** (`@Treasury-0..19`), turning one bottleneck into N parallel lanes; the cooperative must then aggregate shards for reporting.

**Fairness/starvation:** the lock is not a fair queue; under sustained contention, no ordering guarantee among waiters. Coalescing changes *which* transactions batch together, not fairness. A relentless hot pair can starve if not hot-lane-isolated.

### V.7 — Latency decomposition (QUEUED vs APPLIED are different numbers)

**API-visible latency (to `QUEUED`)** — the fast path:
parse → authenticate (API-key hash lookup) → validate (incl. `validateTxn` SELECT on reference) → enqueue to Redis. Dominated by the reference-existence SELECT and the Redis enqueue; typically low and roughly flat with load until backpressure.

**End-to-end latency (to `APPLIED`)** — the meaningful number for a member seeing their contribution land:
queue wait (dominant under contention) → lock acquisition (up to lock-wait-timeout) → balance read (`GetBalanceByID` or faster `GetBalanceByIDLite` when `EnableQueuedChecks` off) → in-memory computation (negligible, `big.Int`) → the atomic composite write (DB round-trip, the dominant *fixed* cost) → post-commit side effects (lineage outbox on the write path; **webhooks fire from a detached goroutine, off the critical path and without an outbox**).

- **Low load:** end-to-end ≈ enqueue + one worker pickup + one DB write. The atomic write dominates.
- **p99 under contention on a hot balance:** **queue wait dominates** — it scales with the number of predecessors holding/awaiting the same lock. This is where coalescing pays off (amortises the DB write across a batch).

### V.8 — Throughput model

- **Unit:** applied transactions/second. Coalescing means *ledger rows* and *commits* decouple (many rows, one commit).
- **Single-node capacity:** bounded by (a) worker concurrency (`max_workers` default 10) × per-txn DB write time for *distinct* balances, and (b) serial commit rate for any *single* hot balance.
- **Scale-out:** more workers/nodes help *only for uncontended, distinct balances*. On one hot balance, more workers do **not** help and increase lock churn/retries.
- **Saturation point:** reached first at a single hot balance, or when Redis memory/pending-task limits trip.
- **Post-saturation behaviour: graceful degradation, not collapse.** `QUEUE_BACKPRESSURE` (HTTP 503, default-on since v0.15.2) sheds *new* enqueues when *"Redis memory usage or pending task count exceeds configured limits."* Already-enqueued work is retained and drained. Callers see 503 and must retry with backoff. Nothing accepted is lost — *unless Redis itself is lost* (V.16).
- **The 5× claim, tested:** MAINTAINER CLAIM. Verbatim: throughput *"improved by up to about 5×"* in *"internal benchmarks under heavy contention and burst load"* with results *"depend[ing] on workload shape…"* No hardware, dataset, concurrency, or metric. Do not size a deployment from it.

### V.9 — Scalability

- **Vertical:** helps DB write throughput and Redis memory headroom.
- **Horizontal:** stateless workers scale for distinct-balance workloads; PostgreSQL is the shared source of truth and the eventual write bottleneck; Redis is the shared queue+lock and the eventual coordination bottleneck.
- **Partitioning/sharding:** *ledger partitioning* is the tenancy model; *balance sharding* is the application-level scaling lever for hot balances (Blnk provides the pattern, not automation).
- **Replication / multi-region:** not provided by Core; operator-supplied PostgreSQL/Redis concern.
- **Primary bottleneck:** the single hot balance's serial commit rate; secondarily Redis memory. **Adding workers hurts on a contended balance.**

### V.10 — Capacity model (sized for a real cooperative)

**Scenario:** 5,000 members, monthly contributions into one pooled account (N→A), plus occasional loans/withdrawals.

- **Load shape:** ~5,000 txns/month is trivial in aggregate (~2 txns/min average). The risk is *not* volume — it is the **temporal spike** if contributions are collected on the same day (e.g. payday), producing hundreds of near-simultaneous writes to one pooled balance.
- **Sizing:** a single modest node (a few vCPU, a few GB RAM), one small PostgreSQL instance, and a small Redis suffice for steady state. Connection pool: default worker/DB pool limits (raised in v0.15.0) are ample.
- **Storage growth:** roughly one transaction row + hash + metadata per contribution; ~60k rows/year — negligible. Balance snapshots (`TakeBalanceSnapshots`) add periodic rows for historical queries.
- **Where the first limit appears:** the *contribution-day spike on the single pooled account*. Mitigations, in order: enable the queue (default), enable coalescing (same source→pooled account batches beautifully), enable hot-lane routing, and if spikes still saturate, **shard the pooled account** and aggregate for reporting.
- **Redis memory:** must hold the queue depth of the largest spike; size it for peak pending tasks or `QUEUE_BACKPRESSURE` will 503 legitimate contributions during collection day.

### V.11 — Reliability mechanisms and retry-amplification assessment

- **Timeouts:** lock-wait-timeout (default 3s); SDK client timeout (e.g. `WithTimeout`).
- **Retries at three layers:** SDK (`WithRetry`), asynq queue (documented reconciliation defaults `max_retries:3, retry_delay:5`; transaction-queue defaults not independently verified), and application (`insufficient_fund_retries`/`max_retry_attempts`).
- **Health checks:** `/health` endpoint (auth-bypassed since v0.10.4); queue monitoring port (v0.10.3).
- **Graceful shutdown:** v0.13.0 ensures pending transactions finish before stop.
- **Retry-amplification verdict: YES, it can amplify.** Three independent retry layers stacked over a *contended hot balance* can multiply attempts against the exact resource that is already the bottleneck, converting a transient stall into a sustained retry storm. Idempotency (unique reference) prevents *double application*, so retries are *safe for correctness* — but not *safe for load*. **Recommendation:** disable SDK-level retries for write paths that also retry at the queue layer, and rely on exponential backoff + `QUEUE_BACKPRESSURE` for shedding.

### V.12 — Durability and recovery

- **`internal/pg-backups` / `/backup-s3`:** triggers a `pg_dump`-style backup to S3 (configured via `blnk.json` AWS keys), scheduled by the operator via cron; restore is manual `pg_restore`. This is *logical backup*, not continuous archiving.
- **WAL / PITR:** **not built into Core.** Point-in-time recovery is a PostgreSQL responsibility the operator must configure separately (e.g. pgBackRest + WAL archiving). Blnk Cloud advertises automatic backups and a rollback window (Cloud figures could not be verified against a Blnk-owned source and are excluded).
- **Durability assumption Blnk relies on but does not verify:** that the underlying PostgreSQL is configured with adequate `fsync`/`synchronous_commit` and durable storage, and that Redis persistence (AOF/RDB) is configured if queue loss is unacceptable. Blnk *assumes* these; it does not check them.
- **Worst permitted loss:** bounded by backup cadence for committed data (daily cron ⇒ up to ~24h RPO) **plus** any queued-but-undrained transactions in Redis if Redis is lost without persistence. Because idempotency is by reference, a client that safely retries un-acknowledged posts can recover queue loss without double-applying.
- **RPO/RTO:** not specified by Core; operator-defined. Set them explicitly.

### V.13 — Observability and the correctness-detection verdict

- **Available:** OpenTelemetry, Jaeger tracing, Prometheus metrics; remote export via `BLNK_CLOUD_DSN` (v0.14.4, redacted); queue monitoring port; `/health`; structured logs (workflow messages moved to `info` in v0.14.5); `system.error` webhooks (incl. duplicate reference); `HotpairsContentionTotal`; `CountUnchainedTransactions` (chain lag).
- **Detects readily:** availability failures, latency, queue depth, lock contention (via hot-pairs metric), chain lag (*if chain enabled*).
- **The operative test — could an operator detect a CORRECTNESS failure (not availability) from what the system emits?** **Largely NO, by default.**
  - **Silent balance drift** (stored balance ≠ Σ history): would *not* raise an alarm unless the operator runs **balance reconstruction** (`BLNK_RUN_RECONCILIATION=SOURCE` / `from_source=true`) and compares — a manual, on-demand action. No continuous reconstruction-diff alarm exists.
  - **Growing chain lag:** *detectable* via `CountUnchainedTransactions` — but only if the hash chain is enabled (off by default) and the metric is alerted on.
  - **Stuck queue:** detectable via queue depth + `RecoverQueuedTransactions`/`GetStuckQueuedTransactions`, but requires the operator to alert on it.
  - **Reconstruction difference:** surfaced only when explicitly requested.
- **Verdict:** the observability stack is a strong *availability*-detection system and a weak *correctness*-detection system out of the box. **For a ledger holding members' savings this is the most important gap after the guarantee ledger.** A drifted balance can sit unnoticed indefinitely.

### V.14 — Resource isolation and noisy neighbours (performance dimension only)

Volume II established there is **no tenant isolation** beyond ledger partitioning and API-key scoping. Performance consequence: workers, the Redis queue, and the PostgreSQL connection pool are **shared**. If cooperative society A runs a bulk import (up to 10,000 items/request per v0.15.0) while society B is taking live member contributions, A's work competes for the same workers, queue capacity, and DB connections. B's contribution latency rises and, if A's burst pushes Redis to its limits, B's enqueues can be rejected with `QUEUE_BACKPRESSURE` (503) — B is penalised for A's behaviour. There is **no per-tenant rate limit or QoS lane** (global rate-limiting exists since v0.7.0, but it is not tenant-aware). Bulk work should be scheduled off-peak and, ideally, run against a separate Blnk deployment per high-volume tenant. *(Confidentiality/integrity of the shared-tenancy model is deferred to Volume VII.)*

### V.15 — Security (deferred)

This volume's analysis depends on two security-adjacent facts, both deferred to Volume VII for adversarial treatment: (1) idempotency and immutability rest on DB constraints/protections whose *bypassability* is a Volume VII question; (2) the Redis lock is the serialisation primitive, and whether it can be *deliberately* subverted (lock theft, TTL manipulation) is a Volume VII question. Here we only note that correctness under *non-adversarial* conditions depends on them holding.

### V.16 — Failure-scenario matrix

| Scenario | What the system does | State left in | Self-heals? | How operator knows |
|---|---|---|---|---|
| **Crash during composite write** | Single atomic write ⇒ commits or rolls back | Txn stays `QUEUED`; no partial balance | Yes — `RecoverQueuedTransactions` re-drives; idempotency prevents double-apply | Stuck-queued metric; `GetStuckQueuedTransactions` |
| **PostgreSQL failover** | Writes fail until new primary; workers error/retry | Consistent (single source of truth) | Yes, once primary returns; queued work drains | Health check, DB errors, queue backlog |
| **Redis failure + restart with queue loss** | Enqueue fails; in-flight locks lost | **Undrained queued txns lost** if no Redis persistence; committed data intact | Partially — clients must re-post (safe via unique reference) | Queue empty/errors; missing `APPLIED` for posted refs |
| **Redis memory exhaustion** | `QUEUE_BACKPRESSURE` 503 on new enqueues | Existing queue drains; new work shed | Yes, as memory frees | 503/`QUEUE_BACKPRESSURE`; Redis mem metric |
| **Network partition worker↔DB** | Worker cannot commit; retries | Txn `QUEUED`; lock may expire | Yes on reconnect | Worker errors; backlog |
| **Disk exhaustion (DB)** | Commits fail | `QUEUED`; no partial | On disk freed | DB errors; health |
| **Clock skew (effective_date, lock TTL)** | `effective_date` may misorder history; **lock TTL may expire early/late** | Possible mis-ordered reporting; **serialisation window lost if TTL early** | No auto-heal for skew | Hard to detect — no clock-skew alarm |
| **Duplicate task delivery (asynq)** | Second delivery hits unique reference ⇒ `23505` | Single application | Yes — idempotent | `system.error` webhook (duplicate reference) |
| **Partial deployment / mixed versions** | Behaviour differences (e.g. pre/post v0.13.2 unique index; v0.15.0 error schema) | Risk of inconsistent enforcement | No | Migration/version checks |
| **Corrupt data** | Detected only if chain enabled or reconstruction run | May persist silently | No | **Only via opt-in reconstruction/verify-chain** |
| **Hot partition (single balance)** | Serialises; coalescing/hot-lane manage; sharding needed | Correct but slow | Partially | `HotpairsContentionTotal`; latency p99 |
| **Lock TTL expires mid-operation** | Serialisation removed; optimistic `version` becomes sole defence | Correct *iff* version check catches the stale writer; else risk of lost update | Version check usually saves it | Not directly alarmed — inferable from drift if reconstruction run |

### V.17 — Build-extraction verdicts

| Mechanism | Verdict | Environment vs mechanism |
|---|---|---|
| **Atomic composite write** | **ADOPT** | Works because of the *mechanism* (single datasource call). Portable. The single most valuable thing to copy. |
| **`redlock` MultiLocker (sorted, deduped)** | **ADOPT** | Mechanism-driven deadlock-freedom via lexicographic ordering. But it depends on Redis availability and TTL discipline — adopt *with* a short, monitored TTL, not 1800s. |
| **Optimistic version check** | **ADOPT** | Correct last-line defence; cheap. Essential precisely because the DB isolation level is not doing the work. |
| **Coalescing / hot-lane routing** | **ADAPT** | Works because of *workload shape* (repeated same-pair traffic). Great for N→A contributions; useless for dispersed traffic. Adopt only if your workload has hot pairs. |
| **Queue backpressure (503)** | **ADAPT** | Mechanism is sound; thresholds are environment-specific. Adopt with Redis sized for peak. |
| **Hash chain as correctness instrument** | **ADOPT-BUT-ENABLE** | Off by default = not a guarantee. For savings, enable it and alert on `CountUnchainedTransactions`. |
| **Balance snapshots** | **ADOPT** | Enables historical queries and faster reconstruction; storage cost modest. |
| **Observability stack as correctness detector** | **REJECT AS-IS** | Detects availability, not silent drift. Must be *supplemented* with a scheduled reconstruction-diff job that alarms on any `stored ≠ reconstructed`. Without that, the environment (a vigilant operator) is doing the work, not the mechanism. |
| **Long lock TTL (1800s default)** | **REJECT (retune)** | A 1800s TTL turns a stalled worker into a serialisation gap. Set it just above worst-case commit time and monitor. |
| **Stacked SDK+queue+app retries** | **REJECT AS-IS** | Amplifies load on the exact bottleneck. Consolidate to one retry layer with backoff. |

### V.18 — Volume V reconstruction

1. **Guarantee ledger, ranked:** atomicity+conservation (strongest, structural) → immutability → idempotency → precision (Go) → concurrency safety → sufficient funds → zero/malformed → tamper-evidence (opt-in) → consistency/read-your-writes & tenancy/resource isolation (weakest).
2. **Invariant spec:** INV-1..12 restated as assertable conditions (V.2); INV-5/7-storage/isolation-level remain UNKNOWN.
3. **Precision model:** `*big.Int` in Go, integer minor units in storage; representable range = *unbounded (NUMERIC) or ±~9.22×10¹⁸ minor units (BIGINT)* — unresolved; safe for fiat cooperatives, risky for high-precision assets.
4. **Consistency model:** no read-your-writes on the queued default; `skip_queue:true` for synchronous read-after-write; poll for `APPLIED`.
5. **Atomicity/isolation model:** one atomic composite write; Redis MultiLock serialises; DB isolation level UNKNOWN (likely READ COMMITTED, compensated by lock+version); remaining anomalies = lost update if lock expires, cross-balance read skew, queued staleness.
6. **Concurrency at the contention point:** single balance serialises; coalescing/hot-lane help at 100s; sharding required at 1000s; adding workers does not help a hot balance.
7. **Latency model:** QUEUED (fast, ~flat) ≠ APPLIED (queue wait dominates under contention; atomic write dominates at low load).
8. **Throughput model:** unit = applied txns/s; ceiling = single hot balance serial commit rate; post-saturation = graceful shedding via `QUEUE_BACKPRESSURE` 503, no loss unless Redis lost.
9. **Scalability model:** stateless workers scale for distinct balances; primary bottleneck = single hot balance, then Redis memory.
10. **Capacity model:** a 5,000-member cooperative is trivial in aggregate; the first limit is the contribution-day spike on one pooled account; fix with coalescing then sharding; size Redis for peak.
11. **Reliability map:** three retry layers → amplification risk; idempotency keeps retries correctness-safe but not load-safe; consolidate retries.
12. **Durability/recovery:** logical backup to S3 + manual restore; no built-in PITR; worst loss ≈ backup cadence (~24h daily) + Redis queue loss; depends on unverified PG/Redis durability config.
13. **Observability map + correctness verdict:** strong availability detection; **weak correctness detection — silent balance drift would not raise an alarm by default.**
14. **Resource-isolation model:** no per-tenant QoS; a bulk import degrades a neighbour's live contributions and can trigger their 503s.
15. **Failure-scenario matrix:** see V.16 — most scenarios self-heal via idempotent recovery; the un-self-healing ones are corrupt/silent-drift data and clock skew.
16. **Build-extraction verdicts:** ADOPT the atomic write, MultiLock, version check, snapshots; ADAPT coalescing/hot-lane/backpressure; ADOPT-BUT-ENABLE the hash chain; REJECT-as-is the default observability-as-correctness-detector, the 1800s lock TTL, and stacked retries.
17. **Key unknowns:** money column type (NUMERIC vs BIGINT) — **permanently UNKNOWN**; CHECK constraints; immutability trigger definition & violation behaviour; DB isolation level inside the composite write; test coverage of concurrent duplicate references, MultiLock ordering, partial-failure rollback, and the trigger; transaction-queue retry defaults; rounding direction.
18. **Ten most important findings:** see Key Findings above.

**Direct answers to the volume's closing questions:**
- **Strongest guarantee?** Per-transaction atomicity + conservation on the main write path (structural, CONFIRMED).
- **Weakest guarantee?** Read-your-writes on the default queued path (not guaranteed) and tenancy/resource isolation (not enforced).
- **Primary scaling bottleneck?** The single hot destination balance's serial commit rate (then Redis memory).
- **What happens after saturation?** Graceful load-shedding via `QUEUE_BACKPRESSURE` (HTTP 503, default-on); accepted work is retained and drained; nothing committed is lost unless Redis itself is lost.
- **Could an operator detect a correctness failure from what the system emits?** Not by default — silent balance drift would go unnoticed unless balance reconstruction and/or the hash chain are explicitly enabled and alerted on.
- **Under what workload does the architecture degrade first?** A spike of concurrent writes to a single hot balance (the pooled cooperative contribution account on collection day) — long before raw aggregate volume matters.

---

## Recommendations

**Stage 0 — Before trusting Blnk with savings (do now):**
1. **Confirm the money column type in your own deployment.** Run `\d balances` / `\d transactions` (or inspect the migration SQL you deploy) and record whether balance/`precise_amount` columns are `NUMERIC` or `BIGINT`. *Threshold to change plan:* if `BIGINT` and you use `precision ≥ 10⁶`, cap or reject balances approaching ±9×10¹⁸ minor units, or migrate the column to `NUMERIC`.
2. **Stand up a scheduled correctness alarm.** Nightly, reconstruct every balance from history (`from_source=true`) and alert on any `stored ≠ reconstructed`. This is the single most important operational control and Blnk does not provide it by default.
3. **Enable the hash chain** and alert when `CountUnchainedTransactions` exceeds a small threshold.

**Stage 1 — Configuration hardening:**
4. **Retune `lock_duration`** from 1800s to just above your worst-case commit latency (seconds, not minutes); monitor for lock-expiry-driven retries.
5. **Consolidate retries** to one layer (prefer queue-layer with exponential backoff); disable SDK write-path retries to avoid amplification.
6. **Size Redis for peak queue depth** and enable Redis persistence (AOF) if losing queued-but-undrained contributions is unacceptable. *Threshold:* if `QUEUE_BACKPRESSURE` 503s appear during normal collection days, add Redis memory or shard load.
7. **Configure PostgreSQL PITR** (WAL archiving, e.g. pgBackRest) — do not rely on the daily `pg_dump`→S3 alone. Set an explicit RPO/RTO.

**Stage 2 — Workload shaping for the cooperative pattern:**
8. **Keep `skip_queue:false`** (default) for member contributions; enable **coalescing** (`BLNK_TRANSACTION_ENABLE_COALESCING=true`) — it is ideal for N→A into one pooled account.
9. **Enable hot-lane routing** (`BLNK_QUEUE_ENABLE_HOT_LANE=true`).
10. If contribution-day spikes still saturate one account, **shard the pooled balance** (`@Pool-0..N`) and aggregate for reporting. *Threshold:* shard when p99 time-to-`APPLIED` on collection day exceeds your member-experience budget or lock-contention metrics climb.
11. **Isolate high-volume tenants:** schedule bulk imports off-peak, and run a separate Blnk deployment per society that regularly does bulk work — there is no per-tenant QoS.

**Stage 3 — Caller discipline (bake into your app):**
12. **Never render a balance from a read taken immediately after `QUEUED`.** Poll `reference+_q`/txn ID for `APPLIED` or use the state-change webhook.
13. **Fix a single canonical `precision` per currency** in your application and never vary it.
14. **Use `precise_amount` / `precise_distribution`** for any high-precision or split amounts to avoid rounding ambiguity.

---

## Caveats

- **Money column type, CHECK constraints, the `reference` unique-index DDL, and the immutability trigger are PERMANENTLY UNKNOWN for this study.** The `sql/` DDL defeated four volumes; GitHub blob/raw access was robots-blocked and code-search hits never surfaced. The **named** index `idx_transactions_reference_unique` and the *existence* of immutability protections and an optimistic `version` are confirmed from the changelog and blog, but their exact SQL text and violation behaviour are not. The representable-range conclusion is therefore stated as a range with a caveat, not a fact.
- **The PostgreSQL isolation level inside the composite write is inferred (likely READ COMMITTED), not read.** If it is stronger, some anomalies noted as "possible" would be additionally guarded at the DB layer.
- **The "up to ~5×" throughput figure is a MAINTAINER CLAIM** with no stated conditions; treat it as marketing. No independent MEASURED RESULT (hardware, dataset, concurrency, metric) was found.
- **No independent benchmark of Blnk under contention was located.** All performance behaviour described is derived from source-code mechanisms, the changelog, and the official hot-balances documentation/blog — not from a controlled measurement.
- **Blnk Cloud figures** (99.9% SLA, 7-day rollback, 7-day backup) appear on marketing pages but could not be verified against a durable, Blnk-owned technical source and are excluded from the reliability conclusions for Core.
- **Transaction-queue retry defaults** (as distinct from the reconciliation `max_retries:3, retry_delay:5`) were not independently verifiable; the retry-amplification assessment stands on the *existence* of three retry layers, which is confirmed.
- **Security/adversarial dimensions are deliberately excluded** and deferred to Volume VII; where correctness depends on a mechanism holding (idempotency constraint, Redis lock), only the non-adversarial case is treated here.

---

# VOLUME VI — Operations, Tradeoffs, Ecosystem & Rebuildability

## TL;DR
- **Blnk is cheap to run but expensive to run *correctly*.** A cooperative of 5,000–50,000 members with monthly contribution cycles can host Blnk for roughly $150–$600/month in infrastructure, but the true cost is operator labour — realistically 0.3–0.5 of a competent backend engineer's time indefinitely, plus a one-time build of the correctness-monitoring layer (reconciliation checks, hash-chain verification, drift alarms) that Blnk deliberately leaves to the operator. That labour line, not the servers, dominates total cost of ownership.
- **Do not adopt Blnk unchanged, and do not rebuild from scratch. Fork it and take its mechanisms.** The codebase is small (~604 commits, Go-dominant, one binary) and Apache-2.0, so a permanent fork is genuinely feasible; but the project is effectively a single-maintainer, pre-seed effort (bus factor ~1), which makes long-term upstream dependence a first-order strategic risk for a founder-owned core-banking platform. The genuinely hard parts to rebuild are few (the atomic composite write, the distributed-lock discipline, precision handling); everything else is assemblable or buyable.
- **The deepest tradeoff — queue-by-default over synchronous — is wrong precisely for the reader's workload.** Monthly contribution cycles funnel thousands of credits into one pooled society account (a "hot balance"); Blnk's queue serialises these onto a single hot destination and no number of workers helps. For a core-banking destination shaped like the reader's, **Midaz is the closer structural analogue** and deserves serious evaluation, but it is source-available (Elastic License 2.0), not Apache-2.0 — a licensing downgrade that matters for a permanently founder-owned platform.

## Key Findings

1. **Time-to-working is minutes; time-to-production is weeks.** `docker compose up` yields a running ledger in under 10 minutes. A production-grade first install — managed Postgres with the *direct* (non-pooled) connection string, managed Redis, TLS, secret_key, observability wired to Prometheus/Jaeger or Blnk Cloud, backups, and a tested restore — is a multi-day-to-multi-week exercise that the quickstart does not describe.

2. **Upgrades and schema migrations are the same event and rollback is generally not possible.** The canonical start command is `blnk migrate up && blnk start`; migrations run automatically at boot. Blnk ships no `migrate down`. Once a forward migration alters the schema, the only rollback is restore-from-backup, and the backup path is logical `pg_dump`/`pg_restore` with no built-in point-in-time recovery. This asymmetry governs all upgrade risk.

3. **Named breaking releases each imposed operator work.** v0.13.2 (12 Feb 2026) added the unique database index `idx_transactions_reference_unique` and the **upgrade fails outright if duplicate `reference` values already exist** — the operator must de-duplicate first. v0.12.0 (8 Dec 2025) hashed API keys with SHA-256 at rest, and **all existing plaintext keys stop working after upgrade** — every integration must be re-keyed. v0.11.0 (27 Aug 2025) changed Typesense/search behaviour and required a reindex. v0.15.0 (23 Jun 2026) introduced structured `error_detail.code` values and **removed `rate`, `currency_multiplier`, and `modification_ref`** — in-transaction FX was removed, so destination credit now equals source debit and any app relying on request `rate` for conversion breaks.

4. **The operational surface is well-documented for install and thin for day-two.** The deployment doc covers single-server, PaaS (Railway/Render/Fly.io), and Kubernetes, and even has a troubleshooting accordion (Postgres connectivity, migration failure, stuck queue, restart loops). But capacity planning, credential/certificate rotation, storage-growth management, and correctness monitoring are effectively undocumented — the operator must design these.

5. **Correctness observability is opt-in and off by default.** The hash chain is disabled by default and verified only on demand via `blnk verify-chain`; reconstruction is opt-in. A silently drifted balance raises no alarm. For money held on behalf of cooperative members, this is the single most important gap the operator must close, and Blnk does not close it for you.

6. **Governance is the biggest strategic risk.** Blnk Finance LLC is a pre-seed company (Wilmington, Delaware; Crunchbase headcount band 1–10, PitchBook indicates ~2 employees, Microtraction an investor) with founder Jerry Enebeli authoring the large majority of core PRs and personally cutting every release. Bus factor is ~1. Release cadence is healthy (~54 total releases; ~11 in H1 2026), but the project's survival is tied to one very small company's runway.

7. **The licence is Apache-2.0 and forkable, but the open-core boundary is real and moving.** Correctness-critical capability remains in Core (atomicity, hash chain, idempotency index). Operational and back-office capability — dashboards, anomaly detection, managed backups with 7-day point-in-time restore, instance branching — lives in the commercial Cloud. There is no evidence Blnk has relicensed away from Apache-2.0, but the sector precedent (HashiCorp→BSL, Redis→dual source-available, Elastic→SSPL/ELv2, and Midaz's own Elastic License 2.0) makes this a live risk to price in.

8. **Blnk Cloud is a self-hosted-data model, not a full SaaS.** Cloud connects to *your* Core instance via database and server URLs; disconnecting stops Cloud but your data stays yours. Pricing is per-deployment/subscription with seat and usage limits (Lite/paid tiers; annual billing saves 10%); the free Lite tier is capped at up to 5,000 transactions-per-minute and 5 GB storage. No free trial of paid plans.

9. **Alternatives are genuinely differentiated.** TigerBeetle is a purpose-built single-threaded, VSR-replicated OLTP database whose interface always deals in batches of up to 8,190 transfers per query; an independent benchmark (backend.how, "1B Payments/Day") measured ~46,600 transfers/second on a single core under an 80/20 hot-account skew over 10M transfers (~63K RPS on a fresh DB) — but you build all surrounding infrastructure (identities, reconciliation, metadata) yourself. Formance is a Go+Postgres programmable ledger with a DSL (Numscript) and an always-on hash chain. Midaz is the closest to a core-banking hierarchy but is source-available under Elastic License 2.0.

10. **Rebuild is smaller than it looks.** A competent 2–3 engineer team can reach a *minimum-viable* correct ledger in ~2–3 months and a *production-grade* one safe enough to hold members' savings in ~6–9 months. The distance between the two is almost entirely correctness monitoring, operational tooling (backup/restore drills, migration safety, reconciliation), and hardening — not core ledger logic.

## Details

### VI.1 Installation and bootstrap
Prerequisites for a real install: a managed PostgreSQL instance, a managed Redis instance, Docker + Docker Compose, and a Linux VM (Ubuntu 20.04+). The documented quickstart is `git clone … && docker compose up` with a minimal `blnk.json` (project name, Postgres DNS, Redis DNS, server port). This produces a working ledger with a default General Ledger created on first run, reachable on port 5001, in under ten minutes — genuinely fast, and multiple testimonials corroborate an easy first setup.

The production-grade first install is a different exercise. The deployment doc's own single-server tab lists managed Postgres and Redis as *required*, sets `"secure": true`, requires a `secret_key`, and exposes ports 5001 (API), 5004 (queue monitoring), and 80/443. Critically, it warns to use the **direct** Postgres connection string, not a pooled one, or Blnk "keeps timing out or disconnecting under load." The server and worker are separate processes/containers with identical configuration; mismatched config between them "causes subtle queue issues." Observability is off unless `BLNK_ENABLE_OBSERVABILITY=true` and a Prometheus/Jaeger stack (or Blnk Cloud DSN) is wired in. Realistic time from nothing to a *production-ready* instance with backups, TLS, monitoring, and a tested restore: several days for an experienced operator, one-to-two weeks if learning the system. Automatable: infrastructure provisioning, compose/k8s manifests, migration-on-boot. Not automatable without bespoke work: correctness monitoring, restore drills, capacity sizing.

### VI.2 Day-two operations
**Every week:** watch queue depth and backpressure via the monitoring port (5004) or Cloud dashboard; confirm workers are consuming (transactions moving out of `QUEUED`); check that backups actually ran and are restorable (a dump that "ran green" against a renamed DB is not a backup); watch Redis memory (backpressure triggers on Redis memory or pending-task count); scan logs — note that as of v0.14.5 normal workflow progress is logged at info, not error, so error-level logs are now meaningful alerting signals.

**Every month:** run a restore drill; reconcile ledger balances against external records (bank statements, mobile-money/agent settlement) using the Reconciliation module; if the hash chain is enabled, run `blnk verify-chain`; review storage growth (transactions are immutable and append-only, so storage grows monotonically and must be capacity-planned); rotate credentials and TLS certs (undocumented — the operator must build this, fetching secrets to the VM/secret manager and restarting). Scaling: adding API servers and workers helps for independent balances but **cannot** help a single hot destination balance; the documented remedies are queueing (default), transaction coalescing, hot-lane routing, intermediary/buffer balances, and ultimately balance sharding.

### VI.3 Upgrade and migration
Because `blnk migrate up && blnk start` is the entrypoint, upgrading the image *is* migrating the schema unless the operator deliberately separates them (run `docker compose run --rm server blnk migrate up` manually first, on a maintenance window, after backup). There is no `migrate down` and no built-in PITR; **rollback after a schema migration means restore-from-`pg_dump`**, losing any writes since the dump. Practically, safe upgrade procedure is: back up → verify backup restores → run migration manually in the foreground to capture errors → start new version → smoke test → keep the old image tagged for image-level (not schema-level) rollback. Rolling upgrades are possible for stateless API/worker pods on Kubernetes, but the migration step is a discrete, non-rolling event. Compatibility breaks at the named releases (Key Finding 3) require pre-migration data work (v0.13.2 dedupe), re-keying (v0.12.0), reindexing (v0.11.0), and client-code changes (v0.15.0 FX removal and structured errors).

### VI.4 Troubleshooting
Documented runbooks exist for: server-can't-reach-Postgres (check DNS/sslmode/direct-connection/network), migrations-fail-on-boot (check CREATE/ALTER grants, read first error, run manually), transactions-stuck-queued/idle-workers (check Redis connectivity, confirm worker running, probe monitoring port), and API-unreachable/restart-loops (check container status, port exposure, config mounted on both services). A stuck queue has a first-class remedy: v0.13.2+ auto-recovers transactions stuck in `QUEUED` and exposes `POST /transactions/recover?threshold=5m` for manual re-enqueue. Undocumented, must-improvise territory: a **drifted balance** (no built-in detector — build reconciliation + snapshot comparison), a **lock that will not release** (the 1800s default lock TTL means a hung operation can hold a lock for 30 minutes; there is no documented "force-release" tool — the operator inspects Redis keys directly; note v0.15.1 fixed an overflow bug in applying `BLNK_TRANSACTION_LOCK_DURATION`), and a **chain that will not verify** (`blnk verify-chain` reports failure but there is no documented repair — the response is forensic: restore, identify the divergent transaction, escalate).

### VI.5 Incident response (cross-referenced to Volume V's failure matrix)
- *Single hot destination balance saturates* → detection: HTTP 503 `QUEUE_BACKPRESSURE` and rising queue depth. Runbook: documented (hot-balances guide) — queue, coalesce, hot-lane, intermediary balances, shard. This is the reader's most likely incident.
- *Lock expires mid-operation (1800s TTL)* → **no runbook.** Containment is manual; this is a correctness risk (loss of serialisation), not just availability.
- *Silent balance drift* → **no runbook and no detector by default.** Must be built.
- *Stuck queue after worker/Redis crash* → runbook exists (auto-recovery + `/transactions/recover`).
- *Retry amplification (SDK + queue + application retries)* → **no runbook**; mitigation is design-time (idempotency via unique `reference`, which v0.13.2 enforces at the storage layer).
- *Postgres/Redis durability loss* → depends on operator's DB config; no built-in PITR; recovery is restore-from-dump with data-loss window. Post-mortem discipline (blameless, timeline, action items) is entirely the operator's to establish; Blnk provides `system.error` webhooks (v0.15.0) and Slack/webhook error push as raw signal.

### VI.6 Developer experience
Documentation is genuinely good for the *intended* path: quickstart, guides (wallets, escrow, payroll, hot balances), API reference, SDKs in Go, TypeScript, and Java, a CLI, and an `llms.txt` index for machine consumption. Local dev is Docker-first and quick. SDKs are official and idiomatic (the Go SDK mirrors the REST surface; TS SDK has typed bulk operations). Learning curve is moderate: the double-entry model, precision handling, inflight/two-phase transactions, and the queue-vs-`skip_queue` distinction all require reading. **Error messages:** v0.15.0 introduced a structured `error_detail` object with a stable `code`, a `message`, and a `details` map (e.g., `TXN_NOT_FOUND`, `QUEUE_BACKPRESSURE`), documented in an API error-codes page. This is a real improvement and the codes are actionable for programmatic handling — but they arrived only in mid-2026, so older integrations and much community content still parse message text, and the migration guide explicitly warns apps that check status codes or message strings to review before upgrading.

### VI.7 Operator experience — effort in people
To keep it *running*: one part-time engineer (≈0.2–0.3 FTE) suffices for a cooperative-scale deployment, given managed Postgres/Redis that absorb most database toil. To keep it *correct*: add a one-time build of the correctness layer (reconciliation automation, drift alarms, hash-chain verification, restore drills) — realistically 4–8 engineer-weeks up front — then ≈0.1–0.2 FTE ongoing to run and heed it. Net: **one competent backend engineer at roughly 0.3–0.5 FTE can run this for a cooperative group**, provided the correctness layer is built first and the deployment stays below the hot-balance ceiling. It does *not* need a dedicated team at 5k–50k members. It *would* need more as transaction concurrency on shared society accounts grows, because that is where the architecture fights back.

### VI.8 Total cost of ownership — model sized for the reader
**Assumptions:** a Nigerian cooperative financial-services group running several societies, 5,000–50,000 members, monthly contribution cycles. Assume 50,000 members each contributing once per cycle plus withdrawals, loans, and internal transfers ≈ 150,000–300,000 transactions/month at the high end, heavily bursty around contribution dates, and heavily concentrated on a handful of pooled society balances. Peak concurrency, not average throughput, is the binding constraint.

**Self-hosted (monthly), order-of-magnitude:**
- Compute (API + worker containers): 2–4 vCPU / 4–8 GB VMs → ~$40–$120.
- Managed PostgreSQL (source of truth; needs headroom for immutable growth + direct connections): ~$60–$250 depending on size/HA.
- Managed Redis (queue + locks; memory-bound, drives backpressure): ~$15–$60.
- Object storage for `pg_dump` backups: ~$5–$20.
- Typesense (optional search), Jaeger/Prometheus (optional observability): ~$0–$60 if self-run on the same VMs.
- Bandwidth: negligible at this scale, ~$5–$20.
- **Infrastructure subtotal: ≈$150–$600/month.** Licensing: $0 (Apache-2.0 Core).
- **Operator labour: the dominant line.** At 0.3–0.5 FTE of a senior backend engineer, this is by far the largest recurring cost and swamps infrastructure. Plus the one-time correctness-layer build (4–8 engineer-weeks) and initial production hardening (1–2 weeks).

**Per-unit:** at ~200,000 tx/month, infrastructure is on the order of **$0.001–$0.003 per transaction**, trivially cheap; the meaningful denominator is engineer-hours per month, not dollars per transaction.

**Blnk Cloud alternative:** subscription + per-deployment pricing with a free Lite tier (≤5,000 TPM, 5 GB) and paid tiers sized Light/Steady/Heavy; annual billing saves 10%; overages (seats, storage, instances, anomaly detection) billed monthly; managed backups retain 7 days with point-in-time restore and one-click instance branching. Cloud buys back the observability and back-office build and the managed backup/PITR that self-hosting lacks — i.e., it converts capex engineer-weeks into opex. For a small cooperative without a spare engineer, Cloud's managed monitoring may be cheaper in true (labour-inclusive) TCO than self-hosting; for a founder who wants permanent data ownership, note Cloud still runs against your self-hosted data.

### VI.9 Governance and maintainership — first-order risk
Owner: Blnk Finance LLC (Wilmington, Delaware; also "Blnk Ledger"). Founder/CEO Jerry Enebeli (Lagos-based, ex-Bloc/Orchestrate); co-founder "Praise" leads design/marketing. Funding stage: pre-seed (Crunchbase); PitchBook lists ~2 employees and Microtraction as an investor; Crunchbase headcount band 1–10. **Critical disambiguation: this is NOT the Egyptian BNPL lender "Blnk" (Amr Sultan / Tarek Elsheikh, $37M debt+equity round led by Algebra Ventures, June 2026) — a wholly unrelated company that shares the name.** Commit history is concentrated: ~604 commits on main, ~54 releases, ~11 in H1 2026; the founder authors the large majority of core PRs and cuts every release. Contributor base beyond the core is ~15 mostly one-off community contributors (plus dependabot). Repo traction as of August 2026: 461 stars, 124 forks, 8 open issues, 1 open PR. **Bus factor ≈ 1.** Release cadence trend: steady-to-accelerating, no slowdown. **Sponsor-withdrawal scenario:** if the pre-seed company fails to raise or is acquired, the most likely outcomes are (a) the repo goes quiet but remains Apache-2.0 and forkable, or (b) an acquirer relicenses future versions source-available (sector precedent is strong). Either way, the Apache-2.0 snapshot as of v0.15.2 is permanently usable — which is exactly why the fork option matters for this reader.

### VI.10 Licensing and commercial boundaries — and the fork question
Core is Apache-2.0 ("download, use, inspect, and extend without license fees or hidden commitments"). Cloud is commercial. The open-core boundary today: correctness-critical capability (atomic composite write, idempotency index, optional hash chain, precision, reconciliation module, identity/PII tokenization) is in Core; operational/back-office capability (dashboards, anomaly detection, RBAC/collaboration, managed backups with 7-day PITR, instance branching, remote monitoring convenience) is in Cloud. **Direction of travel:** no evidence Blnk has relicensed; but the FX-removal in v0.15.0 shows the maintainer will remove features from Core, and the broad industry trend (Terraform→BSL, Redis→dual source-available, Elastic→SSPL/ELv2, and notably Midaz shipping under Elastic License 2.0) means relicensing is a realistic future risk to price in, not dismiss.

**Can the reader fork and own the fork permanently? Yes — legally and practically.** Apache-2.0 grants an irrevocable licence to the v0.15.2 snapshot; no future upstream decision can revoke it. Fork cost: (a) *maintenance burden* — you inherit ~604 commits of Go, one binary, no ORM (hand-written SQL over `database/sql`+`lib/pq`), which one competent team can carry; (b) *divergence risk* — the further you customise, the harder it is to cherry-pick upstream fixes; (c) *loss of upstream security fixes* — you must monitor upstream and backport, or the community around your fork must. The codebase is small enough (Go-dominant, single binary, embedded migrations) that a 2–3 person team can own a fork indefinitely. This is the crux of the central judgement below.

### VI.11 Ecosystem
Integrations/SDKs: official Go, TypeScript, and Java SDKs, a CLI, webhooks, Typesense search, OpenTelemetry, and a "Watch" DSL for real-time monitoring rules. Community: a Discord, ~15 lifetime contributors, growing GitHub stars, active DEV.to tutorials (wallets, payroll, escrow, AI billing). Consultants/third-party production users at scale: **largely UNKNOWN and unverifiable** — testimonials on the vendor site (CTOs at "Seven," "BR Tokens," "Bitnomi," "Digitvant") assert production use but are MAINTAINER-curated and unquantified; no independent large-scale production case study with numbers was found. **Verdict on the ecosystem: it is neither a moat nor a heavy liability — it is thin.** A thin ecosystem means low change-constraint (Blnk can evolve fast, which it does) but also means the reader is substantially on his own for production patterns, and there is no large integration surface to lean on.

### VI.12 Alternatives

| Dimension | Blnk | TigerBeetle | Formance Ledger | Midaz | Hand-rolled in app DB | Traditional core-banking |
|---|---|---|---|---|---|---|
| Conceptual model | Double-entry, ledgers/balances/identities | Accounts + transfers, debit/credit at DB level | Double-entry, Numscript DSL, postings | Org→ledger→asset→portfolio→segment→account, n:n | Whatever you build | Vendor-defined GL + subledgers |
| Architecture | Modular monolith (Go), Postgres+Redis+asynq | Purpose-built DB, single-thread, VSR consensus, LSM | Go + Postgres microservice, log-replicated | Go monorepo (ledger core + Tracer), Postgres 17 primary/replica + Mongo, RabbitMQ events | Your app + your RDBMS | Monolithic/vendor stack |
| Correctness | Per-tx atomicity; hash chain opt-in | Strict serializability, DB-level double-entry invariants | Immutable hash-chained log (always on) | Double-entry + optimistic concurrency, CEL rule engine, hash-chained audit | DIY (highest risk) | Mature, regulated |
| Performance ceiling | Hot-balance-bound; ~5× claim (unconditioned) | ~46,600 transfers/s single core (measured, hot-skew); 8,190/batch | High, Postgres-bound | Postgres-bound, replica reads | RDBMS-bound | Batch-oriented, often slow |
| Operability | Docker/k8s, thin day-two, no PITR | Simple to run, alien ops model, you build the rest | k8s-operator (prod), heavier | Multi-service, heaviest to run | Simplest infra, hardest correctness | Vendor-operated |
| Ecosystem | Thin, growing | Growing, low-level | Moderate, funded | Small, newer (Lerian founded 2024) | None | Large, closed |
| Licence | Apache-2.0 (open) | Apache-2.0 (open) | Open source (MIT-family) | **Elastic License 2.0 (source-available)** | N/A | Proprietary |
| Complexity to adopt | Low–moderate | Moderate (you build surroundings) | Moderate | Moderate–high | Low to start, high to get right | High procurement |

**Deepest treatment — Midaz, the closest structural analogue.** Volume I's flag is correct: Midaz's hierarchy — verbatim from its README, "double-entry accounting over the full financial hierarchy — onboarding (organizations, ledgers, assets, portfolios, segments, accounts), n:n transactions, CRM (holders and instruments) … and in-process fee calculation on the transaction path," plus a "Tracer: real-time transaction validation … a CEL rule engine … and a hash-chained immutable audit trail" — maps almost exactly onto a multi-society cooperative growing toward core-banking. It is the best *conceptual* fit for the reader's eventual destination. **But** it is source-available under Elastic License 2.0 — per the README, ELv2 "allows you to use, copy, modify, and redistribute Midaz, with three primary limitations: you may not provide it to others as a managed/hosted service, circumvent its license key functionality, or remove/obscure license notices" — and it is younger (Lerian, the vendor, was "founded in 2024") and heavier operationally (Go monorepo shipping ledger core plus the Tracer fraud engine, on PostgreSQL 17 primary/replica with MongoDB and RabbitMQ). For a permanently founder-owned platform, ELv2 is a meaningful downgrade from Apache-2.0: fine for internal use, restrictive if the reader ever wants to offer societies a hosted product. **Conclusion: Midaz is the better data model; Blnk is the better licence and the simpler operation.** That tension is central to the verdict.

### VI.13 The design-tradeoff ledger (with losing cases named)
- **Queue-by-default over synchronous.** Benefit: absorbs bursts, sheds load gracefully (503 backpressure), decouples ingestion from balance updates. Cost: no read-your-writes on the default path; retry amplification; latency. Rejected: synchronous writes. **Wrong for:** workloads that need immediate confirmed balances on a hot shared account — *exactly the reader's monthly contribution funnel into one society balance.*
- **Cached mutable balance over purely derived.** Benefit: O(1) balance reads. Cost: the balance can drift from the sum of entries and nothing detects it by default. Rejected: always-derive-from-entries. **Wrong for:** any deployment without an external reconciliation/drift detector — i.e., correctness-critical money at rest with no monitoring budget.
- **Redis locks over database-level serialisation.** Benefit: cross-process locking without DB contention. Cost: 1800s default TTL can expire mid-operation and silently drop serialisation; another moving part (Redis) to run and secure. Rejected: Postgres advisory locks / SERIALIZABLE. **Wrong for:** long-running composite operations, or teams that can't operate Redis to durable standards.
- **PostgreSQL over a purpose-built storage engine.** Benefit: ubiquitous, well-understood, cheap ops, portable backups. Cost: hot-balance write contention, storage amplification vs. a specialised engine. Rejected: LSM/VSR engine (TigerBeetle's path). **Wrong for:** extreme-throughput single-account contention where TigerBeetle's batching wins by orders of magnitude.
- **Hand-written SQL over an ORM.** Benefit: exact control of transaction boundaries for the composite write. Cost: more code, more foot-guns, slower feature velocity. Rejected: ORM. **Wrong for:** teams optimising for CRUD breadth over transactional precision.
- **Modular monolith over services.** Benefit: one binary, simple deploy, easy local dev. Cost: no independent scaling of subsystems; no tenant isolation beyond ledger partitioning + API-key scoping. Rejected: microservices (Midaz's path). **Wrong for:** hard multi-tenant isolation requirements — e.g., legally separate societies needing blast-radius isolation.
- **Removal of in-transaction FX (v0.15.0).** Benefit: simpler, safer core; destination credit == source debit. Cost: multi-currency conversion now the caller's job. Rejected: built-in `rate`. **Wrong for:** genuinely multi-currency products expecting the ledger to convert — and a breaking change for anyone who relied on it.
- **Optional hash chain over always-on.** Benefit: no overhead when disabled. Cost: tamper-evidence is off unless you turn it on and verify it. Rejected: Formance-style always-on chaining. **Wrong for:** audit-critical deployments run by operators who won't remember to enable and check it — the default is unsafe for the reader's use case.
- **Caller-supplied per-transaction precision over a canonical per-asset registry.** Benefit: flexibility. Cost: inconsistent precision across callers can corrupt balances; v0.11.3 had to add rejection of non-integer precision to prevent DB failures. Rejected: per-asset precision registry (there is a separate asset-classes JSON repo, but it's not enforced in-engine). **Wrong for:** multi-team environments where callers disagree on precision — a real risk across several societies with different back-office habits.

### VI.14 Technical debt and constraints (what the maintainers themselves surface)
The changelog is an honest debt register. Recurring themes the maintainers keep fixing: Typesense indexing reliability (v0.12.1, v0.14.4, v0.15.2) and memory backpressure; queue edge-cases (stuck-queued recovery, queued inflight commits against multi-leg parents in v0.15.1); a lock-duration overflow bug (v0.15.1); precision validation gaps (v0.11.3 rejecting non-integer precision "to prevent database failures and balance inconsistencies"); graceful-shutdown of in-flight transactions (v0.13.0). Known structural constraints: single hot balance is the scaling ceiling; no built-in PITR; no tenant/resource isolation; correctness monitoring not provided; the money-column Postgres type is **UNKNOWN** for this study (Volume V, permanently unresolved) and is a real open risk to price into any rebuild. In-flight direction: Cloud-oriented indexes (v0.12.2) and remote monitoring exporters (v0.14.4) suggest ongoing Core→Cloud coupling.

### VI.15 The rebuildability test

| Capability | Conceptual | Implementation | Correctness | Operational | Time | Expertise | Commodity substitute? |
|---|---|---|---|---|---|---|---|
| Double-entry data model | Low | Low | Med | Low | days | Mid | No (but trivial) |
| Atomic composite write (balances+tx+outbox) | Med | High | **Very High** | Med | weeks | Senior | No — must build |
| Distributed lock discipline (multi-key, sorted, dedup, TTL) | Med | High | **Very High** | High | weeks | Senior | Partial (redlock libs) |
| Idempotency (unique reference index) | Low | Low | High | Low | days | Mid | Yes (DB unique index) |
| Precision / money math | Med | Med | **High** | Low | weeks | Senior | Partial (decimal libs) |
| Queue + backpressure + retry | Med | Med | Med | Med | weeks | Mid | Yes (asynq/Sidekiq-class) |
| Immutability + hash chain | Med | Med | Med | Low | weeks | Mid | Partial |
| Reconciliation | Med | Med | Med | Med | weeks | Mid | Partial |
| Search | Low | Low | Low | Med | days | Mid | Yes (Typesense/ES) |
| Observability | Low | Low | Low | Med | days | Mid | Yes (OTel/Prometheus) |
| Backup/restore + PITR | Low | Med | High | High | weeks | Mid | Yes (pgBackRest/WAL) |
| Correctness monitoring (drift alarms) | Med | Med | **High** | High | weeks | Senior | No — must build |

**Must build:** the atomic composite write, the lock discipline, precision correctness, and drift monitoring. **Can assemble:** queue, search, observability, immutability/chain, reconciliation, backup/PITR (commodity components exist for all). **Can buy:** managed Postgres, managed Redis, object storage, managed search, managed monitoring — or Blnk Cloud wholesale. **Price:** a competent 2–3 engineer team reaches a *minimum-viable* correct ledger in ~2–3 months and a *production-grade* one (safe for members' savings) in ~6–9 months. The remaining distance from MVP to production is almost entirely correctness monitoring, backup/restore drills, migration safety, reconciliation, and hardening — not ledger algorithms.

### VI.16 Preserve or redesign (for a builder)
- **Atomic composite write** — **Preserve.** This is the load-bearing correctness mechanism; copy the pattern (one DB transaction: balances + transaction row + outbox), exact boundary control, no ORM.
- **Idempotency via unique `reference` index** — **Preserve.** Cheap, correct, enforced at storage.
- **Redis multi-lock (sorted, dedup)** — **Preserve with modification.** Keep the sorted-dedup discipline; **redesign the TTL** — 1800s is dangerous; make it short with heartbeat/renewal or fall back to Postgres advisory locks for long operations.
- **Cached mutable balance** — **Preserve with modification.** Keep the cache for read speed but **add an always-on derived-balance reconciliation/drift alarm** — do not ship it optional.
- **Hash chain** — **Preserve with modification: make it always-on**, Formance-style, for money held on behalf of members.
- **Caller-supplied precision** — **Replace** with a canonical per-asset precision registry enforced in-engine.
- **Queue-by-default** — **Needs benchmark** for the reader's hot-balance profile; consider a synchronous fast-path for low-contention accounts plus coalescing for the pooled society balances.
- **Modular monolith** — **Preserve.** For a founder-owned platform at cooperative scale, one binary is the right operational choice.
- **PostgreSQL** — **Preserve** (resolve the money-column-type UNKNOWN first). **Needs benchmark** only if single-account concurrency ever approaches TigerBeetle territory.
- **In-transaction FX** — **Replace** by keeping FX out of the ledger (as v0.15.0 did) and handling conversion as explicit two-leg transactions.

### VI.17 Transplant verdicts (ADOPT / ADAPT / REJECT)
- **Operational model as a whole** — **ADAPT.** Works because the system is small and Go-simple, not because of a large team; the reader can run it, but must add the correctness layer the model omits.
- **Backup/recovery (pg_dump→S3 + manual pg_restore)** — **ADAPT.** Adequate but not sufficient; the mechanism works independent of Blnk, but **add WAL archiving/PITR (pgBackRest)** — the absence of PITR is the real gap.
- **Upgrade/migration (migrate-on-boot, no down-migration)** — **ADAPT with discipline: separate migrate from start, always back up first, keep the old image tagged.** The mechanism is fine; the no-rollback asymmetry is the risk to manage.
- **Observability stack (OTel/Jaeger/Prometheus, opt-in)** — **ADOPT**, but **turn it on by default** and add correctness metrics, which the stack does not include.
- **Open-core dependency (Cloud)** — **REJECT as a dependency for a founder-owned platform.** Use Cloud tactically for early monitoring if labour is scarce, but do not let correctness-critical operations depend on a commercial layer you don't control.
- **Fork option** — **ADOPT.** This is the strategic recommendation.

**Central judgement.** *Fork Blnk and take its mechanisms; do not adopt it as an upstream-dependent black box, and do not rebuild from scratch.* Reasoning: (1) the reader needs permanent founder ownership, and Apache-2.0 + a small Go codebase makes a permanent fork genuinely carryable by a 2–3 person team; (2) upstream is a pre-seed, bus-factor-~1 project, so *depending* on it is a strategic risk, while *forking* it converts that risk into a one-time absorption; (3) the genuinely hard parts (atomic write, locks, precision) are already solved well in Blnk and are the last things you'd want to re-derive under time pressure; (4) the parts Blnk gets wrong for the reader (optional correctness monitoring, dangerous lock TTL, optional hash chain, hot-balance handling) are known and fixable in a fork. **What would change this verdict:** if Blnk raised a substantial round and demonstrated a bus factor > 2 with a real maintainer team, straight adoption-with-support becomes defensible; if the reader's roadmap hardens quickly toward a full core-banking hierarchy with multi-society isolation, **Midaz's data model becomes compelling enough to accept its Elastic-License-2.0 constraints** — evaluate Midaz head-to-head before committing the fork.

### VI.18 Volume VI reconstruction (summary)
1. **Install map:** quickstart <10 min; production-grade several days to two weeks (managed DB direct connection, TLS, secrets, observability, backups, tested restore).
2. **Day-two model:** weekly queue/Redis/backup/log checks; monthly restore drill, reconciliation, chain verify, storage/credential review; scaling helps except on hot balances.
3. **Upgrade/migration model:** upgrade == migration; **no down-migration; rollback = restore-from-dump, no PITR**; separate migrate from start and back up first.
4. **Troubleshooting map:** runbooks for Postgres/migration/queue/restart; improvise for drift, stuck locks, chain-verify failure.
5. **Incident response:** hot-balance and stuck-queue have runbooks; lock-TTL, drift, and retry-amplification do not.
6. **Developer experience:** good docs and three SDKs; structured error codes since v0.15.0 are actionable but recent.
7. **Operator experience:** ~0.3–0.5 FTE for one engineer at cooperative scale, after a 4–8-week correctness-layer build; no dedicated team needed at 5k–50k members.
8. **TCO:** ~$150–$600/month infrastructure; operator labour is the dominant line; ~$0.001–$0.003/transaction infra; Cloud converts capex to opex.
9. **Governance:** pre-seed, ~1–10 (≈2) employees, founder-authored, bus factor ~1, healthy cadence, sponsor risk is first-order.
10. **Licensing:** Apache-2.0 Core, commercial Cloud; no relicense yet but sector risk is real; **fork is legal and practical.**
11. **Ecosystem:** thin but growing; three SDKs, Discord, tutorials; no verified large-scale independent production case study.
12. **Alternatives:** TigerBeetle (throughput, low-level), Formance (DSL, always-on chain), **Midaz (closest core-banking model, ELv2)**, hand-rolled (highest correctness risk), traditional core-banking (proprietary, heavy).
13. **Tradeoff ledger:** queue-by-default is the deepest tradeoff and is wrong for the reader's hot-balance contribution funnel.
14. **Technical debt:** Typesense reliability, queue edge-cases, lock-duration bug, precision validation, no PITR, no tenant isolation, money-column type UNKNOWN.
15. **Rebuildability:** MVP ~2–3 months, production-grade ~6–9 months for a 2–3 engineer team; hard parts are few.
16. **Preserve vs redesign:** preserve the atomic write, idempotency, monolith, Postgres; redesign lock TTL, make drift-monitoring and hash chain always-on, replace caller-supplied precision.
17. **Transplant verdicts / central judgement:** **fork Blnk, take its mechanisms, fix its correctness defaults, keep permanent ownership; evaluate Midaz before final commit.**
18. **Key unknowns:** money-column Postgres type; exact top-contributor commit %; verified third-party production scale; Blnk's runway/next raise; whether/when a relicense happens.
19. **Ten most important findings:** see Key Findings above.

**Direct answers.** *Hardest to operate:* the correctness layer Blnk does not provide — detecting silent balance drift on money held for members. *Most expensive to scale:* not machines but people — and specifically the engineering to route around a single hot society balance, since adding workers cannot. *Deepest tradeoff and its wrong workload:* queue-by-default, wrong for immediate-confirmation writes onto one hot pooled account — the reader's monthly contribution cycle. *Hardest to rebuild correctly:* the atomic composite write plus the distributed-lock discipline (and getting precision exactly right). *Replaceable with commodity infrastructure:* queue, search, observability, backup/PITR, and the databases themselves — all buyable or assemblable. *Preserve:* the atomic write, idempotency index, monolith, Postgres. *Redesign:* the 1800s lock TTL, optional-off correctness monitoring, optional-off hash chain, and caller-supplied precision.

## Recommendations
1. **Now (evaluation, ~2–4 weeks):** Stand up Blnk v0.15.2 self-hosted with managed Postgres (direct connection) and Redis; run a realistic load test that funnels a month's contributions into one society balance to observe backpressure and lock behaviour firsthand. In parallel, stand up Midaz and model the same societies in its org→ledger→segment→account hierarchy. **Decision benchmark:** if Blnk's hot-balance handling (coalescing + intermediary balances) holds your peak contribution burst within acceptable latency, and you value Apache-2.0 over Midaz's richer model, proceed with Blnk; if your roadmap needs multi-society isolation and the core-banking hierarchy soon, and you can accept ELv2, prefer Midaz.
2. **If Blnk (staged fork):** Fork at v0.15.2. First changes: (a) shorten the lock TTL and add renewal/heartbeat; (b) build always-on balance-drift reconciliation with alarms; (c) enable and schedule `blnk verify-chain`; (d) add pgBackRest WAL archiving for PITR; (e) turn observability on by default. Keep a script that tracks upstream commits so you can backport security fixes. **Threshold to revisit:** if upstream raises a real round and grows a maintainer team (bus factor > 2), reconsider tracking upstream more closely instead of hard-forking.
3. **Correctness before scale:** Do not onboard real member money until the drift-detection and restore-drill loop is running and has caught a seeded test discrepancy. **Benchmark:** a monthly restore drill that completes within your RTO and a reconciliation job that reconciles to zero.
4. **Staffing:** Budget one backend engineer at ~0.3–0.5 FTE ongoing plus a 4–8-week upfront correctness-layer build. Revisit toward a second engineer only if concurrent writes on shared society balances start hitting backpressure regularly.
5. **Governance hygiene:** Treat the pre-seed sponsor as a risk to monitor — subscribe to releases, mirror the repo, and keep your fork build reproducible so a sudden upstream disappearance or relicense is a non-event.

## Caveats
- The **money-column PostgreSQL type remains UNKNOWN** (Volume V, unresolved after four attempts) and must be resolved before any rebuild — it materially affects precision correctness.
- Third-party **production-at-scale evidence is UNKNOWN**: vendor testimonials assert it but no independent, quantified large-scale case study was found; weight accordingly.
- Infrastructure and labour cost figures are **analytical estimates** sized to stated assumptions (up to ~200k tx/month, bursty, hot-balance-concentrated), not measured bills; actual costs vary with provider, region, HA, and burst shape.
- The **v0.14.0 "up to about 5×" throughput figure is a MAINTAINER CLAIM with no stated conditions.** The TigerBeetle ~46,600 transfers/s figure is a MEASURED RESULT from an independent single-machine benchmark, not vendor-published, and will vary with hardware and workload.
- The **exact top-contributor commit percentage is UNKNOWN** (GitHub contributors graph, DeepWiki, and OSSInsight were unreachable); the bus-factor-~1 conclusion rests on release-authorship and PR-authorship evidence, which is strong but not a precise percentage.
- Blnk Cloud pricing tiers are described qualitatively (Lite free ≤5,000 TPM/5 GB; paid Light/Steady/Heavy; 10% annual discount; 7-day managed backup/PITR) but **exact per-tier dollar figures were not confirmed** in the sources gathered.
- There are at least three unrelated entities named "Blnk"/"Blink" (the ledger; the Egyptian BNPL lender; Blink Charging, Nasdaq: BLNK; Blink home cameras) — all findings here pertain solely to the open-source ledger by Blnk Finance LLC / Jerry Enebeli.

---

# APPENDIX A — GLOSSARY

## A.1 Ledger and accounting

| Term | Meaning |
|---|---|
| **Double-entry** | Every movement of value debits one account and credits another by the same amount. Blnk implements the *reciprocal transfer* core but renames debit and credit to **source** and **destination**, and does not expose the classical five-account-type normality model |
| **Ledger** (`ldg_`) | In Blnk, a grouping or namespace for balances — closer to a partition than the classical "book of final entry." A default **General Ledger** holds internal `@` balances |
| **Balance** (`bln_`) | ⚠ **Major redefinition.** A *stored, mutable, versioned* object with six money fields, not a value derived on demand. Textbook balance = credits − debits computed when asked; Blnk's is a cached running total that *can* be reconstructed |
| **Transaction** (`txn_`) | ⚠ **Redefinition.** A single source→destination transfer, not a balanced set of journal lines. Splits fan out into child transactions linked by `parent_transaction` |
| **Internal balance** (`@Name`) | An operator-owned balance representing the outside world, equity, revenue or fees. Auto-created in the General Ledger; typically runs negative under overdraft. **Blnk's substitute for a chart-of-accounts normality model** |
| **Reference** | A caller-supplied unique string; the idempotency key. Queued transactions receive a **`_q` suffix** on the stored record |
| **Precision** | ⚠ **Redefinition.** Not "number of decimal places" but the integer multiplier mapping display units to minor units. **Caller-supplied per transaction, not canonical per asset** |
| **`precise_amount`** | The authoritative amount, in smallest indivisible units, as Go `*big.Int` |
| **Inflight** | A held or pending transaction — Blnk's two-phase authorise-then-settle primitive. Commits, voids, expires, or partially commits |
| **Lineage** | Fund-source tracking: which credits funded a later debit, allocated FIFO, LIFO or proportionally |
| **Reconciliation** | Matching external records to internal transactions via rules and strategies |

## A.2 Runtime and infrastructure

| Term | Meaning |
|---|---|
| **`asynq`** | `github.com/hibiken/asynq` — the Redis-backed task queue. **Redis is therefore on the correctness path, not a cache** |
| **`redlock` MultiLocker** | Blnk's bespoke distributed lock over **both** balance IDs, deduplicated when source equals destination and **lexicographically sorted** to prevent deadlock |
| **Optimistic locking** | The `version` field on a balance; a write succeeds only if the version is unchanged since read |
| **`RecordTransactionWithBalancesAndOutbox`** | **The load-bearing correctness mechanism.** One composite datasource call persisting balances, the transaction row and the lineage outbox atomically |
| **Outbox** | A durable row written inside the same database transaction as the effect it describes, drained later by a worker. Blnk uses one for **lineage** but **not for webhooks** |
| **Coalescing** | Merging queued transactions sharing source, destination and currency into one batched commit — the hot-balance remedy |
| **Hot lane** | A routing mechanism isolating contended balance pairs from the general queue |
| **`QUEUE_BACKPRESSURE`** | HTTP 503 returned when Redis memory or pending-task count exceeds limits. Default-on since v0.15.2 |
| **Hash chain** | An optional global chain linking transactions via `ComputeChainHash`, sealed in batches by `ChainProcessor` and verified by `blnk verify-chain`. **Off by default** |
| **Balance reconstruction** | Recomputing a balance from its transaction history. Records a `difference` in metadata. **Does not alert** |

---

# APPENDIX B — CANONICAL FACTS REGISTER

**Where any volume disagrees with this table, this table governs.** Compiled 11 August 2026.

## B.1 The subject

| Item | Value | Evidence |
|---|---|---|
| Licence | **Apache-2.0** (Blnk Core) | CONFIRMED |
| Governing version | **v0.15.2** (31 July 2026) | CONFIRMED |
| Repository scale | ~604 commits · ~54 releases · 461 stars · 124 forks | CONFIRMED |
| Language | Go; one binary, three roles (`start`, `workers`, `migrate up`) | CONFIRMED |
| Required infrastructure | PostgreSQL (source of truth) + Redis (queue and locks) | CONFIRMED |
| Optional infrastructure | Typesense (search) · Jaeger/Prometheus (observability) | CONFIRMED |
| Vendor | Blnk Finance LLC, Delaware; founder Jerry Enebeli (Lagos) | CONFIRMED |
| Funding stage | Pre-seed; headcount band 1–10 (~2 per PitchBook); Microtraction investor | THIRD-PARTY |
| **Bus factor** | **≈ 1** — founder authors the majority of core PRs and cuts every release | ANALYTICAL INFERENCE |

**Disambiguation.** This is *not* the Egyptian BNPL lender "Blnk," nor Blink Charging (Nasdaq: BLNK), nor Blink home cameras. Three unrelated entities share the name.

## B.2 The money model

| Item | Value | Evidence |
|---|---|---|
| Go type for amounts | **`*big.Int`** end-to-end | CONFIRMED |
| Storage form | Integer minor units | DOCUMENTED |
| **PostgreSQL column type** | **PERMANENTLY UNKNOWN** — NUMERIC favoured, never confirmed | **UNKNOWN** |
| Consequence if NUMERIC | Effectively unbounded range | — |
| Consequence if BIGINT | Silent boundary at **±(2⁶³−1) ≈ ±9.22×10¹⁸ minor units** | ANALYTICAL INFERENCE |
| Float exposure | Gone from v0.15.x ingress when `precise_amount` is supplied; the convenience `amount` × `precision` path remains lossy | CONFIRMED |
| Precision model | **Caller-supplied per transaction**, not canonical per asset | DOCUMENTED |

## B.3 The correctness mechanisms

| Mechanism | Status | Evidence |
|---|---|---|
| Atomic composite write | `RecordTransactionWithBalancesAndOutbox` — "persisted atomically" | CONFIRMED (envelope inferred) |
| Idempotency | Unique index `idx_transactions_reference_unique` (v0.13.2); PG error `23505` via `IsDuplicateReferenceError` | CONFIRMED |
| Lock | `redlock.NewMultiLocker` over both balance IDs, sorted and deduplicated | CONFIRMED |
| Lock TTL default | **1800 seconds** — a live risk; expiry mid-operation removes serialisation | DOCUMENTED |
| Lock wait default | 3 seconds | DOCUMENTED |
| Optimistic locking | `version` field on balance | CONFIRMED |
| Hash chain | Present, batched, `chain_state` locked `FOR UPDATE`. **Off by default** | CONFIRMED |
| Lineage outbox | On the atomic write path; drained `FOR UPDATE SKIP LOCKED` | CONFIRMED |
| **Webhook outbox** | **None** — detached goroutine, at-most-once | CONFIRMED |
| Isolation level | **UNKNOWN** — likely READ COMMITTED, compensated by the Redis lock | UNKNOWN |
| Immutability trigger | Asserted by docs; **definition never read** | UNKNOWN |

## B.4 Configuration defaults

| Setting | Default |
|---|---|
| Queues | 20 |
| Max workers | 10 |
| Max retries | 3 |
| Retry delay | 5 seconds |
| **Lock duration** | **1800 seconds** |
| Lock wait | 3 seconds |
| Batch size | 100,000 |
| Max queue size | 1,000 |
| Coalescing batch max | 10,000 |
| Hash chain | **Disabled** |
| Backpressure | Enabled (v0.15.2+) |

## B.5 Breaking releases

| Release | Date | Break | Operator action |
|---|---|---|---|
| v0.11.0 | 27 Aug 2025 | Typesense/search behaviour | Reindex |
| v0.12.0 | 8 Dec 2025 | API keys hashed at rest | **Re-key every integration** |
| v0.13.2 | 12 Feb 2026 | Unique reference index | **De-duplicate first or the upgrade fails** |
| v0.15.0 | 23 Jun 2026 | Structured errors; **`rate`, `currency_multiplier`, `modification_ref` removed** | Rewrite any FX-dependent client code |

## B.6 Cost, sized for the reader

*A Nigerian cooperative group, 5,000–50,000 members, monthly contribution cycles, ~150k–300k transactions per month at the high end.*

| Line | Monthly |
|---|---|
| Compute (API + worker) | $40–$120 |
| Managed PostgreSQL | $60–$250 |
| Managed Redis | $15–$60 |
| Object storage (backups) | $5–$20 |
| Optional search and observability | $0–$60 |
| Bandwidth | $5–$20 |
| Licensing | **$0** |
| **Infrastructure subtotal** | **$150–$600** |
| **Operator labour** | **0.3–0.5 FTE — the dominant line** |
| One-time correctness-layer build | 4–8 engineer-weeks |
| Per-transaction infrastructure | ~$0.001–$0.003 |

---

# APPENDIX C — THE INVARIANT CHAIN

**The study's spine.** Volume I catalogued twelve invariants and their *claimed* enforcement points; Volume II located each in a component; Volume III verified each at runtime and classified it four ways; Volume V specified each as an assertable condition and ranked the resulting guarantees.

| # | Invariant | Where enforced | Classification | Governing evidence |
|---|---|---|---|---|
| **1** | **Conservation** — destination credit equals source debit | One `precise_amount` drives both legs via `model.UpdateBalances`; hardened by the v0.15.0 removal of `rate` | **Structural** | CONFIRMED |
| **2** | Balances change only through transactions | No public API mutates a balance directly; `CreateBalance` starts at zero | By check | CONFIRMED |
| **3** | Balance derivability | Reconstruction from history, on demand only | By check | DOCUMENTED |
| **4** | **Idempotency** | Unique index `idx_transactions_reference_unique` + PG `23505` | **Structural** (pre-check is optimisation) | CONFIRMED |
| **5** | Immutability of posted transactions | New `parent_transaction`-linked rows; DB protections asserted | Structural *if the trigger exists* — **definition unread** | DOCUMENTED |
| **6** | Valid state transitions | Guards in the inflight fetch-and-validate functions | By check | CONFIRMED |
| **7** | **Precision integrity** | `*big.Int` in Go; integer minor units in storage | **Structural in Go**; storage range **UNKNOWN** | CONFIRMED / UNKNOWN |
| **8** | Sufficient funds unless overdraft | Balance check including inflight since v0.11.0 | By check | DOCUMENTED |
| **9** | Concurrency safety | `redlock` MultiLocker + optimistic `version` | By check — **and the lock TTL can expire** | CONFIRMED |
| **10** | Zero and malformed rejected | Dropped before persistence | By check | CONFIRMED |
| **11** | Tamper-evidence | `HashTxn` per row; global chain via `ChainProcessor` | **By convention — off by default** | CONFIRMED |
| **12** | Authorisation and tenancy | Scoped, hashed, owner-bound API keys | Authz by check; **tenancy NOT ENFORCED — no component owns it** | CONFIRMED |

**The chain's verdict.** Four invariants are genuine guarantees — conservation, idempotency, precision-in-Go, and immutability if the trigger is real. The rest are code paths that hold while nothing unusual happens. **Two are not enforced at all in any meaningful sense: tamper-evidence, because it ships disabled, and tenancy, because nothing owns it.**

---

# APPENDIX D — SOURCE REGISTER

## D.1 What the study rests on

**Primary source.** The `blnkfinance/blnk` repository at tag v0.15.2 — `transaction_execution.go` and `transaction.go` read in full; the exported API of every package via `pkg.go.dev`, with file paths and line numbers; `docker-compose.yaml`; `metadata_test.go`. Volume III additionally read `transaction.go` from the public Apache-2.0 fork `northstar-pay/nucleus` at commit `1cb559337258` (August 2024) — **clearly labelled throughout, and superseded by Volume IV wherever it conflicts.**

**Official documentation.** `docs.blnkfinance.com` — the changelog (the single most useful document in the corpus, and an honest technical-debt register), the configuration reference, the transaction and balance guides, the hot-balances guide, the deployment and backup pages, and the API error-code reference.

**Maintainer writing, treated as MAINTAINER CLAIM.** The Blnk Finance blog, particularly the hot-balances, idempotency and v0.10.1 posts; the README; conference and community material.

**Company and governance evidence.** Crunchbase and PitchBook for funding stage and headcount; GitHub for commit concentration, release cadence, contributor count and repository traction.

**Comparative material.** TigerBeetle documentation and an independent third-party benchmark; Formance Ledger documentation; the Midaz repository and README, including its Elastic License 2.0 terms.

## D.2 The retrieval problem — a methodological finding

**An Apache-2.0 repository proved substantially unreadable by automated means for four consecutive volumes**, and the study records this as a finding rather than an excuse.

What failed: GitHub tree, blob and raw endpoints (robots-blocked); `jsDelivr`; the Go module proxy; bare `raw.githubusercontent.com`; code-search indexes.

What worked, from Volume IV onward: **`pkg.go.dev` at the current module**, which returns the complete exported API with source paths and line numbers **and surfaces GitHub blob URLs at a version tag that can then be fetched directly.**

**The cost of the delay.** Volume II could not confirm the schema; Volume III was forced onto a two-year-old fork and produced three findings that Volume IV had to supersede; and the DDL was never read at all. **Any future TREF study should attempt the `pkg.go.dev` route first.**

## D.3 What was never read

The `sql/` directory, embedded in the binary as `SQLFiles embed.FS`, containing the schema DDL. Also unread: the body of `database/transaction.go` (so the `BeginTx` envelope inside the composite write is inferred, not confirmed); the body of `internal/redlock` (so the lock's Redis commands and retry interval are inferred from the pattern); and the test files covering concurrency, partial failure and the immutability trigger — **so the test status of the correctness-critical paths is UNKNOWN rather than confirmed-absent.**

---

# APPENDIX E — RECONCILIATION

Six volumes researched independently against a repository that was intermittently unreadable, spanning two release pins and, in one case, a two-year-old fork. **Three genuine corrections were applied at source; two version differences are recorded as such; and one question is declared permanently unresolved.**

## E.1 Corrections applied at source

**Note 1 — the lock package name. CORRECTED in Volume II.** Volumes II and III identified the distributed lock as `internal/lock`. **Volume IV read the current source and established the package is `internal/redlock`**, providing a `MultiLocker`. Volume IV governs; Volume II is corrected in place at four occurrences, with a visible inline note at the first.

**Note 2 — the money column type. SUPERSEDED in Volumes I and II.** Both volumes inferred **NUMERIC** and labelled it inference. Volume V, after a fourth failed retrieval attempt, **declared the type permanently UNKNOWN for this study.** Volume V governs; both earlier volumes now carry an inline note at the point of inference.

*The consequence, stated plainly:* the representable balance range cannot be confirmed. If NUMERIC, it is effectively unbounded. If BIGINT, there is a silent boundary at **±(2⁶³−1) ≈ ±9.22×10¹⁸ minor units** — comfortable for a naira or dollar cooperative at `precision = 100`, and dangerous at `precision = 10¹⁸`. **The reader must read the DDL in his own deployment before trusting large balances.** This is the first item in Volume VI's recommendations for that reason.

**Note 3 — Volume III's runtime findings. SUPERSEDED by Volume IV, with a banner at the head of Volume III.** Volume III was researched against the 2024 fork and reported: balances persisted *before* the transaction row as two separate calls; a lossy `int64(Amount × Precision)` float multiply at ingress; and a lock keyed on the source balance alone.

**Volume IV read v0.15.2 directly and found all three superseded** — a single atomic composite write, `*big.Int` accepted directly, and a MultiLocker over both balances. Volume IV governs.

**This is the method working, not failing.** Volume III explicitly anticipated it: *"If v0.15.x already wraps the two writes atomically, Findings 2–3 and the worst partial-success rows soften — verify against the current `transaction.go` before building."* Volume IV verified, and they did.

## E.2 Version differences — not conflicts

**Note 4 — the release pin.** Volumes I and II were researched against **v0.15.0** (22 June 2026); Volumes IV, V and VI read **v0.15.2** (31 July 2026). **v0.15.2 governs the assembled study.** The difference is material in three places: the queued inflight commit/void default, the lock-duration overflow fix, and queue and Typesense memory backpressure. Where a volume describes v0.15.0 behaviour it says so.

**Note 5 — the fork.** Volume III's source reading comes from `northstar-pay/nucleus` at August 2024, roughly two years before the pinned release. **This is a vintage difference, not an error**, and the banner at the head of Volume III states which findings survive and which do not.

## E.3 Unknowns carried forward

The study could not resolve, and does not pretend to have resolved:

- **The PostgreSQL column type for money**, and any CHECK constraints on sign, magnitude or precision. Permanently UNKNOWN after four attempts.
- **The exact definition of the unique reference index** — whether partial, whether created CONCURRENTLY.
- **The immutability trigger** — its name, its protected columns, and its behaviour on violation. Asserted by documentation, never read.
- **The transaction isolation level** used inside the composite write. Likely READ COMMITTED; the Redis lock is doing the serialisation work either way.
- **The `BeginTx` envelope** inside `RecordTransactionWithBalancesAndOutbox` — inferred from the single call site, the "persisted atomically" comments and the `InsertLineageOutboxInTx(tx *sql.Tx)` signature, but not read.
- **The `internal/redlock` implementation body** — the Redis commands, retry interval and failure sentinel.
- **Test coverage of the correctness-critical paths** — concurrent duplicate references, MultiLocker ordering, partial-failure rollback, and the trigger. UNKNOWN, not confirmed-absent.
- **Third-party production evidence at scale.** Vendor testimonials assert it; no independent quantified case study was found.
- **Blnk Finance's runway, next raise, and the exact top-contributor commit share.**
- **Everything Volume VII would have established.** See the gap declaration at the head of this document.

## E.4 A note on what the reconciliation demonstrates

**The most valuable thing this study produced is not a finding about Blnk but a demonstration that the method catches its own errors.** Volume III wrote down the condition under which its own conclusions would collapse; Volume IV tested it; the conclusions collapsed; and the record now says so in the body of Volume III where a reader meets it, rather than in a footnote.

A study that had smoothed that over would have told the reader that Blnk carries a durable partial-write hazard. **It does not, and the difference between those two answers is the difference between forking this ledger and abandoning it.**
