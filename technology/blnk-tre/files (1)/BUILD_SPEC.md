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

