# PP-SPEC-037: Proof of Efficacy Mapping to A2AS BASIC

| Field | Value |
|---|---|
| Status | DRAFT v0.1 |
| Author | Craig Ellrod, Nebulonium, Inc. (dba HACKERverse®) |
| Date | October 1, 2026 |
| License | CC BY 4.0 |
| Maps to | A2AS BASIC |
| Series | Proof Protocol Framework Mapping Specifications |

---

## 1. Purpose

This specification defines how A2AS BASIC agent-to-agent security, identity, authorization, and interaction claims can be bound to Proof Protocol test cases, evidence, and efficacy results.

The referenced external work remains authoritative for its own terminology, identifiers, requirements, and architecture. This document defines a **Proof Protocol mapping** and does not supersede or modify A2AS BASIC.

## 2. Scope

A2AS BASIC supplies protocol or framework context describing expected behavior between agents and related security boundaries. Proof Protocol supplies an independent evidence model for testing selected claims under defined conditions.

Independent witnessing and evidence-capture implementation are defined elsewhere in the Proof Protocol specification family.

## 3. Core Question

Proof of efficacy asks:

> **Was there a control, and did it work?**

For agent-to-agent interactions, this means distinguishing a claimed identity, policy, permission, or protocol behavior from evidence that it actually constrained or protected the tested interaction.

## 4. Metric Definitions

Against a defined adversarial corpus, each case is recorded as **blocked**, **detected**, **missed**, or **INVALID**.

Relevant measurements include:

- containment rate;
- detection rate;
- miss rate;
- false-positive rate against paired benign interactions;
- robustness against impersonation, replay, confused-deputy behavior, privilege misuse, manipulation, or bypass;
- version-level results; and
- INVALID status when required evidence is incomplete or broken.

Target levels are defined by the engagement and risk context rather than by this mapping.

## 5. Evidence Produced

Mapped tests can produce:

- **Proof records** binding agent identities/context, control, test case, system/version, verdict, timestamp, and evidence references;
- **ProofStamp™** trusted timestamps bound to evidence/verdict objects;
- **ProofBundle™** packages containing proof records, metrics, corpus manifests, and environment/context;
- **ProofRegister™** records for issued proof artifacts; and
- corpus and environment manifests identifying the tested interaction conditions.

## 6. Mapping to A2AS BASIC

| A2AS BASIC context | Proof Protocol treatment | Evidence |
|---|---|---|
| Agent identity claim | Exercise valid and invalid identity conditions and record observed authorization behavior. | Proof record; identity evidence |
| Authentication condition | Test acceptance/rejection under valid, invalid, replayed, or manipulated credentials where applicable. | Execution evidence; verdict |
| Authorization or delegated authority | Attempt actions inside and outside the asserted authority boundary. | Proof records; outcome evidence |
| Agent-to-agent message or request | Bind the interaction to a reproducible test case and observed result. | Corpus manifest; proof record |
| Policy/control assertion | Record the asserted control separately from its observed effect. | Control descriptor; efficacy result |
| Trust relationship | Exercise conditions intended to violate or exploit the assumed trust boundary. | Robustness evidence |
| Protected downstream action | Obtain target/application/tool evidence when necessary to establish whether the action actually occurred. | Outcome evidence |
| Version/protocol context | Bind material implementation and protocol versions to the result. | Environment descriptor |

## 7. Interoperability Rules

1. The A2AS BASIC version or revision and mapped element SHOULD be recorded when available.
2. Upstream identifiers and terminology MUST NOT be silently redefined.
3. Authentication or policy evaluation alone does not establish efficacy when the claim concerns a downstream action or protected target.
4. Where necessary, target, application, tool, SIEM, vendor, or equivalent evidence SHOULD complete the evidence round trip.
5. Missing required evidence MUST yield **INVALID**, not PASS.
6. Material changes to agent identity, policy, model, tool permissions, system version, protocol version, environment, or corpus SHOULD trigger retesting where they can affect the result.

## 8. Framework-Agnostic Architecture

> **Threat frameworks are pluggable inputs to Proof Protocol. Proof Protocol is framework-agnostic.**

External frameworks and protocols can identify **what to test**: threats, vulnerabilities, controls, design assertions, identity claims, permissions, or risk conditions. Proof Protocol independently establishes **whether the control worked and what evidence proves that result**.

No external framework or protocol is required for Proof Protocol to operate. A Proof Protocol implementation MAY use A2AS BASIC, MAESTRO, MITRE ATLAS, OWASP, AIVSS, a proprietary model, another recognized framework, or no external framework at all when the test condition is otherwise sufficiently defined.

Adding, replacing, muting, or removing a framework mapping does not alter the Proof Protocol architecture, evidence model, Proof of Efficacy determination, ProofBundle™, ProofStamp™, ProofRegister™, or independent corroboration requirements.

A mapping therefore establishes **interoperability**, not architectural dependency.

## 9. Relationship to Proof Protocol

This mapping is part of the Proof Protocol specification family maintained by Nebulonium, Inc.

The relationship is intentionally asymmetric:

> **A2AS BASIC supplies agent-to-agent security context. Proof Protocol supplies the evidence model for determining whether a selected control or claim performed as asserted.**

No affiliation, endorsement, certification, or sponsorship by A2AS BASIC's maintainers is implied.

## 10. Source Framework, Attribution, and License

A2AS BASIC is external work. Its names, specifications, implementations, and expressive materials retain their original ownership and licensing.

At the time this mapping was prepared, an open-content license for all referenced A2AS BASIC specification material had not been independently verified. Accordingly, this mapping uses **reference-only treatment**: upstream concepts may be identified for interoperability, but upstream prose, diagrams, tables, or other expressive material should not be copied unless its applicable license permits that use.

This Proof Protocol mapping is independently authored and licensed under **CC BY 4.0**.

## 11. Versioning

This mapping is versioned independently of A2AS BASIC. Material upstream changes SHOULD trigger a mapping review and, where necessary, a new version identifying the upstream revision mapped.

---

*Proof Protocol · proofprotocol.io · CC BY 4.0*
