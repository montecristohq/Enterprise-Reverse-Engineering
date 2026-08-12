# Technology Reverse Engineering Framework (TREF)

**TREF** is a structured methodology for disassembling a technology, tracing how it actually works, proving its important guarantees, and reconstructing it as one coherent technical system.

> **Decompose. Trace. Prove. Reconstruct.**

## Architecture

1. **Volume I — Purpose, Domain & Conceptual Model**  
   Why it exists; users; problem; abstractions; semantics; invariants; assumptions; non-goals.

2. **Volume II — Architecture & Component Anatomy**  
   System boundaries; modules; services; APIs; databases; queues; dependencies; control/data plane; deployment topology.

3. **Volume III — Data, State, Control & Execution Flows**  
   Runtime paths; state transitions; transactions; ordering; concurrency; idempotency; events; failures; recovery.

4. **Volume IV — Implementation & Infrastructure Anatomy**  
   Source code; languages; algorithms; schemas; indexes; runtime; networking; deployment; CI/CD; build-vs-buy.

5. **Volume V — Correctness, Performance, Scale, Reliability & Security**  
   Invariants; precision; consistency; isolation; throughput; latency; scaling; durability; observability; threat model.

6. **Volume VI — Operations, Tradeoffs, Ecosystem & Rebuildability**  
   Installation; day-2 operations; upgrades; debugging; operating cost; licensing; ecosystem; alternatives; rebuild test.

7. **Final Stage — Technology Reconstruction**  
   Recombine Volumes I–VI into one complete technical model.

## Core Questions

For every material component ask:

- **What?** What exists?
- **How?** How does it work?
- **Who/what controls it?** What component owns, invokes, or maintains it?
- **Where?** Where does it execute, persist, or communicate?
- **When?** When does it run, commit, retry, reconcile, expire, or fail?
- **Why?** Why was it designed this way?

Then apply five lenses:

- **Structure**
- **Flow**
- **Control**
- **Resource economics**
- **Failure**

## Non-Negotiable Depth Rule

Depth follows the subject, not page count.

If concurrency requires 18 pages, write 18 pages. If a minor subsystem needs two paragraphs, write two paragraphs. Never shorten important material because earlier sections became long.

> **Completeness before concision.**

## Evidence Hierarchy

Prefer, in order:

1. official specification,
2. official documentation,
3. source code,
4. architecture/design documents,
5. ADRs/RFCs/proposals,
6. tests,
7. schemas/migrations,
8. release notes/changelogs,
9. issue tracker,
10. commit history,
11. official engineering posts,
12. official benchmarks,
13. package/deployment manifests,
14. standards bodies and peer-reviewed papers,
15. reputable independent technical analysis.

Classify claims as:

- **CONFIRMED IMPLEMENTATION**
- **DOCUMENTED BEHAVIOR**
- **MAINTAINER CLAIM**
- **MEASURED RESULT**
- **SOURCE-CODE INFERENCE**
- **ANALYTICAL INFERENCE**
- **HYPOTHESIS**
- **UNKNOWN**

## Version Discipline

Always pin or identify:

```text
Technology: [NAME]
Version / release / commit: [VERSION]
Official docs: [URL]
Source repository: [URL OR NONE]
Deployment model: [SELF-HOSTED / CLOUD / BOTH / UNKNOWN]
License / edition: [IF RELEVANT]
Research date: [DATE]
```

Do not silently mix behavior from incompatible versions.

## Mandatory Trace Rules

### Follow the execution
Input → validation → auth → routing → core logic → reads → invariant checks → mutation → persistence → side effects/events → response.

### Follow the state
Distinguish client-visible, in-memory, durable, derived, cached, replicated, and external-system state.

### Follow the failure
Trace crashes, timeouts, retries, duplicate requests, dependency failure, partial success, and recovery.

### Follow the invariant
Identify what must never be violated and exactly where it is enforced.

### Follow the resources
Trace CPU, memory, disk, I/O, network, locks, queues, connections, external calls, and operator effort.

## Completion Standard

The research is complete only when a sophisticated engineer can explain:

- why the technology exists,
- its domain model,
- its core abstractions and invariants,
- its architecture,
- its critical runtime path,
- how state is represented,
- how concurrency works,
- what happens under partial failure,
- how it scales,
- its security boundaries,
- how it is operated,
- its major design tradeoffs,
- and how to rebuild a functionally equivalent system.

The final standard is:

> **“I can mentally disassemble and reconstruct the technology.”**
