# /ship

## TL;DR

### Intent

Use this when the branch is supposed to be ready and you want the final release path handled in one workflow.

### How to use it

Bring it a feature branch that should be close to landing.

Use it when you want merge-base, tests, review, release hygiene, push, and PR creation treated as one final sequence.

### What is actually useful here

This one is less intellectually special than the review skills.

The useful part is mostly workflow glue:

- merge latest base before testing
- treat tests, review, versioning, changelog, and PR creation as one release path
- stop only for real blockers

If you already have strong release automation and habits, this skill adds less. In lite form it should stay small.

## Core Use

Use this for:

- "Ship this."
- "Push this branch and open the PR."
- "Run the final release checklist."

## Minimal Flow

1. Confirm the branch is actually a feature branch.
2. Merge the latest base branch first.
3. Run tests on the merged state.
4. Run the pre-landing review.
5. Handle release hygiene like versioning, changelog, and docs.
6. Push and open the PR.

## What It Should Push On

- stale branches
- unresolved test failures
- unresolved critical review findings
- missing release or distribution steps
- version or changelog drift

## Rules

- Do not push from the base branch.
- Do not ignore unresolved critical issues.
- Do not add ceremony where a checklist is enough.

## In One Sentence

`/ship` is useful mostly as an integrated release checklist, not as a deep reasoning skill.
