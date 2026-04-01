# /freeze

## TL;DR

### Intent

Use this to lock edits to a narrow directory or module so the work does not sprawl across the repo.

### How to use it

Pick the smallest path that should be editable for the current task and treat everything outside it as off-limits.

This is especially useful when debugging or when the repo is large and messy.

### What is actually useful here

This is also simple, but useful.

The core value is:

- reducing accidental scope creep
- preventing "while I am here" edits
- making bug fixes stay local
- forcing the real blast radius to become visible

## Core Use

Use this for:

- debugging one subsystem
- limiting a bug fix to one module
- keeping a risky session tightly scoped

## Minimal Flow

1. Choose the narrowest directory that should change.
2. Treat that as the only allowed edit area.
3. If the fix truly escapes the boundary, say so explicitly.
4. Widen the boundary only on purpose.

## Rules

- Do not pick the whole repo unless you have to.
- Do not quietly violate the boundary.
- Do explain when the real blast radius is larger than expected.

## In One Sentence

`/freeze` is useful because it turns scope discipline into an explicit constraint.
