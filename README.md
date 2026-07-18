# BIBLIA

> **Open Knowledge Preservation System**

BIBLIA is an open, vendor-independent specification for preserving, governing, and evolving project knowledge created by humans and AI systems.

BIBLIA is not a chatbot, a prompt, or a documentation generator. It defines how durable knowledge is captured, classified, validated, versioned, related, published, and recovered.

## Mission

A project should never lose its knowledge.

Conversations are temporary. Models, tools, and teams change. The **Knowledge Canon** must remain sufficient to continue the project without relying on lost chats or individual memory.

## Core principles

1. Knowledge is a first-class project asset.
2. The Canon is the authoritative source of truth.
3. Durable knowledge is preserved completely, not merely summarized.
4. Knowledge evolves through explicit, traceable changes.
5. Every important decision has an origin, rationale, and history.
6. AI implementations are replaceable.
7. Git is the persistence and audit layer.
8. If knowledge is not consolidated in the repository, it does not officially exist.

## Initial scope

BIBLIA v0.1 defines:

- the Knowledge Canon;
- knowledge artifact types and lifecycle;
- a preservation workflow;
- agent behavior;
- Git publication rules;
- recovery and integrity requirements.

## Repository structure

```text
.
├── AGENTS.md
├── CHANGELOG.md
├── README.md
├── VERSION.md
├── docs/
├── examples/
├── schemas/
├── templates/
└── tools/
```

## Status

**Version 0.1.0 — Draft**

The project is in its initial specification phase. QRAI is the first intended pilot project.

## Defining test

> If every conversation disappeared and the AI model, tools, and team changed, could the project continue using only the repository?

A conforming BIBLIA implementation aims to make the answer **yes**.
