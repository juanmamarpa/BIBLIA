# BIBLIA Architecture

**Version:** 0.1.0-draft

## Objective

This document defines the logical components and data flow of BIBLIA. Implementations MAY combine components, but MUST preserve their responsibilities.

## Components

### Knowledge Collector

Finds candidate durable knowledge in conversations, code, documents, issues, pull requests, tests, and operational events.

### Knowledge Analyzer

Separates facts, decisions, hypotheses, evidence, risks, unknowns, constraints, and transient content.

### Artifact Classifier

Assigns artifact type, identifier, lifecycle state, metadata, tags, and relationships.

### Canonical Router

Selects the authoritative destination and prevents uncontrolled duplication.

### Documentation Engine

Creates or updates complete human-readable and machine-processable Canon content.

### Consistency Validator

Checks metadata, identifiers, links, lifecycle rules, contradictions, supersession chains, and required recovery context.

### Canon Manager

Applies additions and changes while retaining history and maintaining artifact relationships.

### Git Publisher

Creates branches, commits, pushes changes, and opens or updates pull requests.

### Verification Engine

Reads the remote repository after publication and confirms that intended changes exist.

### Recovery Engine

Reconstructs project purpose, architecture, decisions, state, risks, roadmap, and operating instructions from the Canon.

## Canonical flow

```text
Sources
  ↓
Collection
  ↓
Analysis
  ↓
Classification
  ↓
Canonical routing
  ↓
Conflict and gap detection
  ↓
Canon update
  ↓
Validation
  ↓
Git publication
  ↓
Remote verification
  ↓
Recovery-ready Canon
```

## Architectural constraints

BIBLIA MUST NOT depend on a particular model, chat system, IDE, repository provider, or documentation platform.

The repository representation SHOULD remain human-readable. Machine-readable schemas MAY complement but MUST NOT replace recoverable human documentation.

## Failure behavior

Validation or publication failure MUST leave the Canon's last verified state authoritative. Failed or partial preservation MUST be reported and MUST NOT be represented as complete.
