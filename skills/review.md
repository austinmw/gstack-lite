# /review

## TL;DR

### Intent

Use this right before merge to review the actual diff for structural problems that are easy to miss even when the code seems done.

### How to use it

Bring it a feature branch or PR-sized diff when the code is mostly finished.

Use it when you want a serious pass on whether the change is actually safe, complete, and mergeable.

### What is actually useful here

This is another strong skill.

The genuinely useful parts are:

- reviewing the full diff, not just snippets
- checking specific high-risk bug classes
- verifying claims with evidence instead of guessing
- fixing mechanical issues directly when possible
- separating real findings from noisy review chatter

That is substantially better than just saying "review this PR."

## Core Use

Use this for:

- "Review this PR."
- "What is wrong with this diff?"
- "What am I about to miss before merge?"

This is not a plan review and not a style-policing exercise.

## Minimal Flow

1. Confirm there is a real diff to review.
2. Read the full diff.
3. Do a critical pass first.
4. Do a completeness pass second.
5. Fix obvious mechanical problems directly.
6. Summarize remaining risks and judgment calls.

## What It Should Push On

- data and SQL safety
- race conditions and ordering problems
- unsafe trust of external or model output
- incomplete handling of new states, enums, or branches
- tests or docs that no longer match the change

## Rules

- Do not comment before reading the full diff.
- Do not invent uncertainty where evidence is available.
- Do not flood the user with low-value style comments.
- Do be terse, specific, and risk-weighted.

## In One Sentence

`/review` is useful because it teaches the agent what kinds of bugs to hunt for instead of giving generic PR commentary.
