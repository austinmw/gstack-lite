# /unfreeze

## TL;DR

### Intent

Use this to remove the edit boundary once the constrained scope is no longer helpful.

### How to use it

Run it when the investigation or change genuinely needs to cross the old boundary, or when the scoped phase is over.

### What is actually useful here

This is pure utility.

It matters only because `/freeze` is useful and boundaries need a clean way to end.

## Core Use

Use this for:

- widening the edit scope after a local fix
- ending a tightly scoped debug session
- avoiding accidental confusion about what is still frozen

## Minimal Flow

1. Confirm the old boundary no longer makes sense.
2. Remove it explicitly.
3. Say that the scope is open again.

## Rules

- Do not silently drift past the boundary.
- Do not leave an old constraint in place after the work moved on.

## In One Sentence

`/unfreeze` is useful because explicit boundaries should also end explicitly.
