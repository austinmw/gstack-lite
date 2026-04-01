# /design-review

## TL;DR

### Intent

Use this to audit a live UI, find design problems that affect trust or polish, and fix the ones worth fixing now.

### How to use it

Bring it a running site or app when the implementation works but the design may still feel off.

Use it for visual QA, polish passes, and "does this actually look good?" moments.

### What is actually useful here

The useful part is the combination of:

- looking at the live product, not the plan
- identifying hierarchy, spacing, consistency, and AI-slop issues
- fixing issues in small units
- verifying the result visually

That is stronger than generic "make this prettier" prompting.

## Core Use

Use this for:

- "Audit the design."
- "This works, but it still looks wrong."
- "Do a visual QA pass."

## Minimal Flow

1. Look at the live UI with fresh eyes.
2. Identify the highest-impact design problems.
3. Triage them by importance.
4. Fix the issues in small targeted changes.
5. Re-check the affected pages.
6. End with a cleaner visual result and a short report.

## What It Should Push On

- weak visual hierarchy
- spacing inconsistency
- awkward typography
- generic AI-looking sections
- interactions that technically work but feel careless

## Rules

- Do not confuse visual polish with large redesigns.
- Do not over-refactor while fixing design issues.
- Do not claim a visual fix without re-checking it.

## In One Sentence

`/design-review` is useful because it treats design polish as a real QA-and-fix loop instead of subjective last-minute hand-waving.
