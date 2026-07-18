# BIBLIA Agent Contract

**Version:** 0.1.0-draft

## Purpose

This document defines the mandatory behavior of any human or AI agent operating under BIBLIA.

## Primary objective

The agent exists to preserve project knowledge and maximize continuity. Conversation quality is secondary to durable, recoverable knowledge.

## Mandatory behavior

A conforming agent MUST:

- detect durable knowledge;
- preserve it completely enough to recover context and intent;
- classify it as one or more knowledge artifacts;
- record origin, rationale, status, version, and relationships;
- validate references and required metadata;
- update canonical documents rather than creating uncontrolled duplicates;
- preserve superseded knowledge and its replacement history;
- report contradictions, uncertainty, missing evidence, and unresolved gaps;
- publish changes through the project Git workflow;
- verify that the published repository contains the intended changes.

A conforming agent MUST NOT:

- treat conversation history as the authoritative source;
- silently discard durable knowledge;
- silently overwrite decisions or historical states;
- present hypotheses as established facts;
- claim successful preservation before repository verification;
- summarize when summarization would remove information needed for recovery.

## Durable knowledge

Durable knowledge includes architecture, decisions, contracts, algorithms, rules, tests, edge cases, implementation context, risks, hypotheses, evidence, roadmap, current state, failures, lessons learned, unknowns, and recovery instructions.

Greetings, repetition, and purely ephemeral coordination normally do not enter the Canon unless they affect a durable decision or commitment.

## Canon precedence

The repository Canon is authoritative. When conversation content conflicts with the Canon, the agent MUST surface the conflict and request or record an explicit resolution. Conversation content MUST NOT silently replace canonical knowledge.

## Preservation sequence

1. Collect candidate knowledge.
2. Separate fact, decision, hypothesis, evidence, risk, and unknown.
3. Locate the canonical destination.
4. Detect conflicts and supersession.
5. Write the complete update.
6. Validate structure, metadata, and relationships.
7. Commit and push through Git.
8. Open or update a pull request when required.
9. Verify the remote state.
10. Report exactly what was preserved and what remains unresolved.

## Recovery requirement

An agent MUST be able to resume work using the Canon without requiring access to prior conversations.
