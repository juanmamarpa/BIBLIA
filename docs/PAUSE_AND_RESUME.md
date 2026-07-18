# BIBLIA Pause and Resume Protocol

**Status:** Active  
**Recorded:** 2026-07-18

## Current decision

Development of BIBLIA is intentionally paused so the primary effort can return to the quantitative trading system project.

BIBLIA v0.1 already exists in the `main` branch and provides the initial specification, architecture, Canon model, workflow, Git protocol, glossary, agent contract, schema, template, examples directory, and tools directory.

No further BIBLIA software development should be started until the user explicitly activates the resume keyword.

## Resume keyword

The exact activation phrase is:

> **REANUDAR BIBLIA**

When this phrase is issued, the agent must:

1. Treat the repository `juanmamarpa/BIBLIA` as the authoritative source of truth.
2. Read the current repository state before proposing changes.
3. Confirm that `main` contains BIBLIA v0.1 and inspect any later commits or open pull requests.
4. Resume from the first software milestone: create the Python project and implement the initial CLI command `biblia init`.
5. Use a feature branch, commits, remote verification, Pull Request, review, merge, and branch cleanup.
6. Preserve all durable decisions, risks, unknowns, implementation context, tests, and recovery instructions in GitHub.
7. Never rely on the old conversation as the only source of project knowledge.

## Planned next milestone

### BIBLIA v0.2 — Initial CLI

Target structure:

```text
src/
└── biblia/
    ├── __init__.py
    ├── cli.py
    ├── init.py
    ├── validator.py
    ├── canon.py
    └── workflow.py

tests/
pyproject.toml
```

First functional command:

```bash
biblia init
```

The command must initialize a project with the standard BIBLIA structure and baseline files.

## Priority rule

Until `REANUDAR BIBLIA` is explicitly issued, the primary project is the quantitative trading system. BIBLIA remains preserved, paused, and recoverable.