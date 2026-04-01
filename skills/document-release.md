# /document-release

## TL;DR

### Intent

Use this after the code is effectively done to make the documentation match reality again.

### How to use it

Bring it a branch that has already been reviewed and is near merge or just shipped.

Use it when README, architecture notes, contributor docs, instructions, changelog wording, or TODOs may now be stale.

### What is actually useful here

The useful parts are:

- audit docs from the diff, not from memory
- make obvious factual updates directly
- separate factual edits from narrative or philosophical rewrites
- preserve changelog history instead of regenerating it
- check consistency across docs, not just within one file

That is better than a generic "update the docs" prompt, though the gap is smaller than it is for `/review` or `/plan-eng-review`.

## Core Use

Use this for:

- "Update the docs."
- "Sync the README with what shipped."
- "Clean up documentation drift."

## Minimal Flow

1. Start from the diff and commit history.
2. Audit the main docs one by one.
3. Apply clear factual updates directly.
4. Surface risky or narrative doc changes explicitly.
5. Polish changelog wording without rewriting history.
6. Check cross-doc consistency and TODO cleanup.

## What It Should Push On

- stale feature descriptions
- setup or contributor instructions that no longer work
- architecture docs that contradict the code
- hidden docs that are no longer discoverable
- TODOs that are completed but still open

## Rules

- Do not rewrite docs from scratch without a strong reason.
- Do not casually change architecture philosophy or security language.
- Do not overwrite changelog history.
- Do update obvious factual mismatches.

## In One Sentence

`/document-release` is useful because it makes documentation updates diff-grounded and disciplined instead of ad hoc.
