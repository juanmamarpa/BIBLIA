# Git Publication Protocol

**Version:** 0.1.0-draft

## Authority

The configured remote Git repository is the authoritative persistence and audit layer. If knowledge is not present in the verified remote repository, it is not officially preserved.

## Standard workflow

```text
Development → Canon update → Validation → Commit → Push → Pull request → Verify → Merge
```

## Branches

Knowledge changes SHOULD be created on a dedicated branch. Branch names SHOULD describe the preservation scope, for example:

```text
feature/biblia-v0.1
canon/session-2026-07-18
knowledge/decision-d-014
```

## Commits

Commits MUST be descriptive, reviewable, and limited to coherent changes. A commit message SHOULD state the type and purpose, such as:

```text
docs: define knowledge canon
canon: preserve authentication redesign decisions
fix: repair supersession references
```

## Pull requests

Pull requests SHOULD include:

- preservation scope;
- artifacts created or changed;
- important decisions and supersessions;
- validation performed;
- unresolved risks or gaps;
- recovery impact.

Draft pull requests MAY be used while preservation is incomplete. A PR MUST NOT be represented as ready when validation has failed.

## Verification

After publishing, a conforming implementation MUST verify at least:

- the remote branch exists;
- expected files contain the intended changes;
- commits are present remotely;
- the pull request points to the correct base and head branches;
- no publication error remains unresolved.

## Merge

Merge indicates acceptance into the authoritative Canon. Repository policy determines who may approve and merge.

## Failure and recovery

On conflict, rejected push, missing permission, failed validation, or partial publication, the last verified remote Canon remains authoritative. The failure and recovery steps MUST be reported explicitly.
