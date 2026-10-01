# PP-SPEC-037: Proof of Efficacy Mapping to A2AS BASIC

**Status:** DRAFT v0.1  
**Author:** Craig Ellrod / Nebulonium, Inc. / HACKERverse®  
**License:** CC BY 4.0

**Normative specification:** [`PP-SPEC-037-A2AS-BASIC-Mapping.md`](./PP-SPEC-037-A2AS-BASIC-Mapping.md)

## Purpose

This repository defines a Proof Protocol mapping between A2AS BASIC and Proof Protocol evidence, efficacy, and proof semantics.

A2AS BASIC is treated as a pluggable source of agent-to-agent security, identity, authorization, and interaction context. Proof Protocol remains framework-agnostic and independently establishes whether a selected control performed as claimed.

## Repository contents

- `PP-SPEC-037-A2AS-BASIC-Mapping.md` — normative mapping specification
- `README.md` — repository overview
- `LICENSE` — license for original Proof Protocol material
- `CONTRIBUTING.md` — contribution guidance
- `CITATION.cff` — citation metadata

## Architectural principle

> **Threat frameworks are pluggable inputs to Proof Protocol. Proof Protocol is framework-agnostic.**

External frameworks and protocols can identify what should be tested. Proof Protocol independently establishes whether the control worked and what evidence proves the result.

## Ownership and external-framework notice

The Proof Protocol mapping is independently authored. A2AS BASIC names, identifiers, specifications, implementations, and other upstream intellectual property remain with their respective owners. Mapping establishes interoperability, not dependency, endorsement, or transfer of ownership.
