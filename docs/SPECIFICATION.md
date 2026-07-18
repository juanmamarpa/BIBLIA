# BIBLIA Core Specification

**Version:** 0.1.0-draft

## 1. Purpose

BIBLIA defines a vendor-independent system for preserving, governing, evolving, and recovering durable project knowledge.

## 2. Scope

BIBLIA specifies how knowledge is collected, classified, validated, related, versioned, consolidated, published, queried, superseded, and recovered.

It does not prescribe a programming language, AI provider, IDE, project-management method, or repository host.

## 3. Normative language

The terms MUST, MUST NOT, SHOULD, SHOULD NOT, and MAY are normative.

## 4. Fundamental requirements

A conforming implementation MUST:

- maintain an authoritative Knowledge Canon;
- preserve durable knowledge with sufficient completeness for recovery;
- distinguish facts, decisions, hypotheses, evidence, risks, and unknowns;
- maintain traceability from knowledge to its source and evolution;
- retain superseded knowledge and explicit replacement links;
- use version control as the persistence and audit mechanism;
- validate Canon integrity before publication;
- verify remote persistence after publication;
- remain independent of any specific AI model.

## 5. Completeness principle

BIBLIA preservation is not ordinary summarization. An implementation MUST retain all material information needed to understand, verify, reproduce, challenge, continue, or recover the project.

Compression MAY be used only when it does not remove material context, constraints, rationale, edge cases, uncertainty, or recovery information.

## 6. Authority

The Canon stored in the configured repository is the official source of truth. Unpublished conversations, local notes, and model memory are non-authoritative.

## 7. Knowledge evolution

Knowledge MUST NOT be silently deleted or overwritten. Changes MUST produce traceable history. Superseded artifacts MUST identify their successors, and successor artifacts SHOULD identify what they replace.

## 8. Integrity invariants

- Artifact identifiers are unique.
- Required metadata is present.
- Relationships resolve to existing or explicitly external targets.
- Supersession chains are non-circular.
- Facts are distinguishable from hypotheses.
- Contradictions are visible until explicitly resolved.
- Published state is verifiable in the remote repository.

## 9. Conformance

An implementation conforms to BIBLIA v0.1 when it satisfies every MUST and MUST NOT requirement in the v0.1 Canon.

## 10. Success criterion

A project is recoverable when an authorized person or agent can continue meaningful work from the repository alone, without access to historical conversations.
