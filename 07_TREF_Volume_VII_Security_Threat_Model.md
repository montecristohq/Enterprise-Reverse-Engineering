# TREF VOLUME VII — SECURITY & THREAT MODEL
## *Conditional volume*

**Standalone research prompt. Send together with `TREF_CONVENTIONS.md`, which is binding and is not repeated here.**

**Commission this volume when the technology holds money, credentials or personal data, or is internet-facing or multi-tenant.** Where none of those apply — a compression library, a build tool, a local utility — skip it and leave the security material in Volume V, where the core set retains it.

## Subject header
*Reproduce §0 from the instantiated conventions.*

## This volume
**Owned question:** *Which of the system's guarantees can be broken deliberately, and by whom?*
**Execute Volume VII only.** Do not begin the reconstruction.

Volume V established what the technology guarantees under normal operation. **This volume asks the adversarial version of the same question.** The division is deliberate: V asks where the system stops working; VII asks whether someone can make it stop.

## Standing rule — defensive orientation
**Build this volume defensively. Assess the posture; do not produce operational attack material.**

Describe trust boundaries, control placement, classes of weakness and the historical record. **Do not write exploit paths, working proof-of-concept material, or step-by-step procedures for defeating a live control.** Where a class of weakness is material, name the class and the mitigation rather than the method.

The test: **would this section help a defender more than an attacker?** If not, cut it. A reader should finish able to evaluate and improve the security posture — and to build a safer system of their own — not to attack this one.

## Evidence ceiling
*State what the source-openness position permits.*

**And a rule specific to this volume: a security claim by the project about itself is a MAINTAINER CLAIM.** A completed third-party audit with published scope is a MEASURED RESULT. A certification is evidence of process, not of security. Distinguish the three throughout, and never let the presence of a compliance badge stand in for an assessment.

## Carried forward
*Restate Volumes I–VI — the trust assumptions from I.10, the system boundary and rented dependencies from II, the authorisation points from III, the configuration surface from IV.9, and above all **the guarantee ledger from V.1**, which this volume tests adversarially.*

## Re-cut *(optional)*

---

### 1. Assets
**What is worth attacking, and what is it worth?**

Money and value transfer; credentials and secrets; personal and regulated data; the integrity of records; availability itself; compute and bandwidth; reputation and trust; and access to connected systems. For each: where it lives, who legitimately reaches it, and what its loss would mean.

### 2. Actors and capability
Classify by capability rather than intent: unauthenticated external; authenticated user; another tenant; a privileged operator; a compromised dependency; a malicious insider; the infrastructure provider.

**For each, state what they can legitimately reach and what the system assumes they cannot.** The gap between the two is the threat surface.

### 3. Trust boundaries and entry points
Map every boundary at which trust changes — network edge, authentication, tenant, process, privilege, dependency, physical. For each: what crosses it, what validates the crossing, and **what the system does if validation is skipped.**

Cross-reference the system boundary from Volume II. **Where a boundary exists architecturally but no control enforces it, that is a finding.**

### 4. Authentication
Mechanisms, credential lifecycle, storage, rotation, expiry, multi-factor support, session handling, federation. **Establish what happens on credential compromise** — detection, revocation, blast radius.

### 5. Authorisation
Model — role-based, attribute-based, capability-based, access-control lists. **Establish where authorisation is enforced**, using Volume III's four-way classification: structurally, by check, by convention, or not at all.

**Then establish whether any path bypasses it** — internal interfaces, administrative tools, background jobs, replication, direct storage access, debugging endpoints. Authorisation enforced at one layer and absent at another is the most common structural weakness in this class of system.

### 6. Identity between services
Service identity, mutual authentication, credential distribution, trust within a deployment. **Establish whether internal traffic is authenticated or merely assumed** — the flat internal network remains a widespread default.

### 7. Tenant isolation *(where multi-tenant)*
Namespaces, data partitioning, query scoping, resource limits, cross-tenant references. **Establish the mechanism that prevents one tenant reading another** and whether it is enforced at storage, query, or application level.

*Resource-contention isolation — the noisy-neighbour performance question — remains in Volume V. This section is about confidentiality and integrity across the tenant boundary.*

### 8. Data protection
Encryption in transit and at rest; what is encrypted and what is not; key management, rotation and custody; envelope encryption; hardware-backed keys where present.

**Establish who can decrypt** — including the operator, the infrastructure provider and anyone holding a backup.

### 9. Secrets management
Where secrets live, how they reach running processes, rotation, what happens on leak. **Establish whether any secret is defaulted, embedded or documented** — a default credential shipped in a container image is a recurring class of failure.

### 10. Sensitive data in unexpected places
**Logs, error messages, telemetry, crash dumps, backups, caches, temporary files, support bundles and debug endpoints.**

This section catches what the encryption section misses. Data protected at rest and in transit is routinely written in clear to a log that is shipped to a third-party aggregator, and this is one of the most consistently under-examined surfaces in any system.

### 11. Input handling
Where untrusted input enters, what validates it, and what the validation assumes. **Establish the classes of weakness the architecture is structurally exposed to** — injection into a query or command layer, deserialisation of untrusted data, path traversal, server-side request forgery, template evaluation — and **the structural mitigation for each**, such as parameterisation, allow-listing, sandboxing or type safety.

Name classes and mitigations. Do not produce payloads.

### 12. Abuse and resource exhaustion
Duplicates, replay, malformed input, unbounded queries, expensive operations, privilege misuse. **Establish which operations are unbounded in cost and whether anything limits them** — rate limits, quotas, query complexity limits, timeouts, pagination.

An unbounded operation reachable without authentication is an availability weakness regardless of intent.

### 13. Supply chain
Dependency provenance, lock files, transitive depth, build reproducibility, artefact signing, release integrity, plugin and extension trust.

**Establish what executes that the project did not write**, and what would happen if an upstream package or a build system were compromised. Cross-reference the rented-versus-owned register from Volume II.

### 14. Cryptographic choices
Algorithms, modes, key sizes, random-number sources, protocol versions, certificate handling. **Establish whether anything deprecated remains supported for compatibility**, and whether the project implemented cryptography itself rather than using a vetted library.

### 15. THE DISCLOSED-VULNERABILITY RECORD
**The single most informative section in this volume**, and the equivalent of an enforcement post-mortem in the enterprise framework.

Catalogue publicly disclosed vulnerabilities: what class, which component, what severity, what caused it, and how long it existed before discovery.

**Then look for the pattern.** Do the findings cluster in one component, one class, one abstraction? Recurrence of a class is a statement about the architecture, not about the individual defects — and it is the best available evidence of where this design is structurally hard to get right.

**A project with no disclosed vulnerabilities is not necessarily secure.** Establish whether that reflects a hardened design, a small attack surface, an absence of scrutiny, or an absence of a disclosure process. The last two are findings.

### 16. The security response process
Reporting channel, disclosure policy, response times, patch cadence, advisory quality, backporting to supported versions, and whether users are notified.

**This is frequently more informative than the vulnerability list.** A project that publishes clear advisories, credits reporters and backports fixes has a functioning security culture; one that fixes silently does not, whatever its defect count.

### 17. Compliance and certification *(where relevant)*
Certifications held, audits completed, standards claimed, scope and date of each. **Establish what the scope actually covered** — certification scopes are narrower than they appear, and a badge is evidence of process rather than of security.

### 18. THE ADVERSARIAL GUARANTEE LEDGER
**Take Volume V's guarantee ledger and test each entry adversarially.**

For each guarantee: can it be broken deliberately, by which class of actor, under what conditions, and what control prevents it? Classify each as **structurally protected · protected by control · protected by assumption · unprotected.**

A guarantee that holds against accident but not against intent is not a security property, and the system's marketing frequently does not distinguish the two. **This section is where the two volumes reconnect and is the payoff of the split.**

### 19. Defensive posture assessment
Reach a verdict. What is genuinely well protected; what is protected by assumption; what is exposed; and what the project appears not to have considered.

**Where a control is absent, establish whether that is an accepted risk documented as a non-goal — see Volume I.11 — or an oversight.** The difference matters, and the answer is usually in the documentation or the issue tracker.

### 20. Transplant verdicts *(where the objective is build extraction)*
Adjudicate each security mechanism **ADOPT · ADAPT · REJECT**, applying the environment question: *did this control work because of the mechanism, or because of the surrounding environment — a private network, a small trusted user base, an operator team, a compliance regime?*

**State plainly which controls a new implementation must have from day one and which can follow**, because security retrofitted after scale is the most expensive rebuild there is.

## Required deliverables
1. Asset register · 2. Actor and capability model · 3. Trust-boundary map with unenforced boundaries flagged · 4. Authentication model with compromise blast radius · 5. **Authorisation map with bypass-path analysis** · 6. Service-identity model · 7. Tenant-isolation model · 8. Data-protection model with decryption-capability list · 9. Secrets model · 10. **Sensitive-data-exposure map** · 11. Input-handling and structural-mitigation map · 12. Abuse and unbounded-operation register · 13. Supply-chain map · 14. Cryptographic inventory · 15. **Disclosed-vulnerability record with pattern analysis** · 16. Security-response assessment · 17. Compliance scope map · 18. **Adversarial guarantee ledger** · 19. Defensive-posture verdict · 20. Transplant verdicts where applicable · 21. Key unknowns · 22. Ten most important findings

## Final questions
- Which guarantee can be broken deliberately, and by whom?
- Where is authorisation enforced, and what bypasses it?
- Who can decrypt the data — including operators, providers and backup holders?
- Where does sensitive data end up that the design did not intend?
- What pattern do the disclosed vulnerabilities form, and what does it say about the architecture?
- Does the project have a functioning security response process?
- What must a new implementation have on day one?

**Completion test:** a reader should be able to state what the technology protects, against whom, by what mechanism, and where the protection rests on assumption rather than control — and a builder should know which controls cannot be deferred.
