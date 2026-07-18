# Knowledge Canon

**Version:** 0.1.0-draft

## Definition

The Knowledge Canon is the authoritative, version-controlled collection of durable knowledge required to understand, operate, verify, evolve, and recover a project.

## Knowledge artifacts

A knowledge artifact is a durable unit of project knowledge. The initial types are:

- specification;
- architecture;
- decision;
- rule;
- contract;
- algorithm;
- test;
- edge case;
- risk;
- hypothesis;
- evidence;
- unknown;
- project state;
- roadmap item;
- experiment;
- lesson learned;
- recovery instruction.

## Required metadata

Every independently managed artifact MUST include or inherit:

- unique identifier;
- type;
- title;
- lifecycle status;
- version or revision reference;
- creation and update dates;
- author or responsible agent when known;
- source or origin;
- rationale where applicable;
- relationships;
- content.

## Lifecycle

The standard lifecycle is:

```text
candidate → draft → review → approved → active → superseded → archived
```

An implementation MAY add states, but MUST retain explicit transitions and historical traceability.

## Relationships

Supported initial relationship semantics include:

- `depends_on`;
- `implements`;
- `modifies`;
- `supersedes`;
- `validated_by`;
- `contradicts`;
- `references`;
- `affects`;
- `derived_from`;
- `evidenced_by`;
- `blocked_by`.

Relationships MUST use stable identifiers or explicit external references.

## Preservation rules

- Durable knowledge MUST have a canonical destination.
- Duplicate narratives SHOULD be consolidated through references.
- Historical content MUST remain recoverable through Git and explicit supersession.
- Hypotheses MUST NOT be presented as facts.
- Unknowns and missing evidence MUST remain visible.
- Current-state documents MUST identify their update time and scope.

## Integrity

The Canon MUST have no duplicate identifiers, unresolved internal links, circular supersession chains, invisible contradictions, or claims of verification without evidence.

## Recovery completeness

The Canon is complete only when it contains enough context to continue the project without conversation history, including purpose, constraints, architecture, decisions, interfaces, algorithms, tests, risks, current state, roadmap, and operating instructions relevant to continuation.
