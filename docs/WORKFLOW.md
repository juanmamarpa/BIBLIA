# BIBLIA Preservation Workflow

**Version:** 0.1.0-draft

## Trigger

The command `BIBLIA` means: consolidate all durable knowledge from the active work into the authoritative repository completely, validate it, publish it, and verify the remote result.

## Workflow

### 1. Establish scope

Identify the session, feature, incident, experiment, or body of work being preserved and the repository and branch that own the Canon.

### 2. Collect

Review all relevant sources, including conversation, code changes, documents, tests, issues, pull requests, decisions, failures, and unresolved questions.

### 3. Classify

Separate:

- established facts;
- explicit decisions;
- hypotheses;
- evidence;
- risks;
- unknowns;
- rejected options;
- current state;
- future work.

### 4. Route

Locate the existing canonical artifact for each item. Create a new artifact only when no suitable canonical destination exists.

### 5. Reconcile

Detect duplication, conflict, stale state, changed decisions, and superseded content. Preserve both the previous state and the explicit transition.

### 6. Write completely

Record all material architecture, rationale, contracts, algorithms, tests, edge cases, operational context, risks, roadmap, and uncertainty needed for future continuation.

### 7. Validate

Check required metadata, identifiers, relationships, source traceability, lifecycle transitions, contradictions, and recovery completeness.

### 8. Publish

Use a branch and descriptive commits. Push the changes and create or update a pull request unless the project's policy explicitly permits direct updates.

### 9. Verify

Read the remote files, commit, and pull request state. Confirm that the intended content exists remotely and that no required update was omitted.

### 10. Report

Report:

- files created or changed;
- decisions and knowledge preserved;
- validation outcome;
- branch, commits, and pull request;
- unresolved conflicts, risks, evidence gaps, or failed operations.

## Completion rule

BIBLIA is complete only after successful remote verification. Local changes, generated text, or an unpushed commit do not count as preservation.

## Failure rule

When any step fails, the agent MUST identify the failed step and remaining work. It MUST NOT claim that consolidation succeeded.
