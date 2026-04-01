# /investigate

## TL;DR

### Intent

Use this when something is broken and the first job is to find the real root cause before anyone starts patching symptoms.

### How to use it

Bring it a bug, error, regression, or weird behavior and make it trace the problem before changing code.

Use it early, especially when people are already guessing.

### What is actually useful here

This is one of the stronger skills.

The genuinely useful parts are:

- no fixes before a root-cause hypothesis
- reproduce the bug before arguing about the fix
- trace the code path and recent changes
- test the hypothesis instead of guessing
- stop and reassess when repeated hypotheses fail

That is much better than a generic "debug this."

## Core Use

Use this for:

- "Why is this broken?"
- "Debug this regression."
- "Find the root cause of this error."

This is not a refactor prompt. It is a debugging discipline.

## Minimal Flow

1. Collect the exact symptoms and reproduction steps.
2. Trace the code path and recent changes.
3. Form a specific root-cause hypothesis.
4. Test the hypothesis with evidence.
5. Make the smallest fix that addresses the actual cause.
6. Reproduce again and add a regression test.

## What It Should Push On

- regressions introduced by recent diffs
- config drift between environments
- race conditions and ordering problems
- bad assumptions about null, state, or caching
- fixes that are really guesses

## Rules

- Do not start by editing code.
- Do not pile on speculative fixes.
- Do not say "should fix it" without verification.
- Do stop and rethink the model if several hypotheses fail.

## In One Sentence

`/investigate` is useful because it turns debugging into a root-cause process instead of guess-and-patch thrashing.
