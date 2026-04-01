# /plan-design-review

## TL;DR

### Intent

Use this when a plan has UI or UX scope and you want to catch missing design decisions before implementation starts.

### How to use it

Bring it a plan or design doc that describes screens, flows, or user-facing states.

Use it after the product and engineering shape are mostly clear, but before the UI gets built.

### What is actually useful here

The useful part is simple:

- rate the design completeness of the plan
- identify what is missing
- make the plan specify actual user experience decisions
- push on states, hierarchy, responsiveness, and clarity

That is worth keeping. Most of the original mockup automation and long rating ritual is not.

## Core Use

Use this for:

- "Review the design plan."
- "What design decisions are missing here?"
- "Does this plan actually specify the UI well enough?"

## Minimal Flow

1. Confirm the plan actually has UI scope.
2. Rate how complete the design thinking is.
3. Identify the biggest gaps.
4. Improve the plan by adding the missing decisions.
5. Escalate the real design choices that need human judgment.

## What It Should Push On

- unclear information hierarchy
- missing empty, error, and loading states
- vague interaction descriptions
- responsive behavior that was never specified
- generic or AI-slop UI patterns

## Rules

- Do not review backend-only plans as if they were design work.
- Do not settle for "clean modern UI" as a design decision.
- Do not leave obvious design gaps in the plan.

## In One Sentence

`/plan-design-review` is useful because it forces the plan to describe the user experience clearly enough to actually build it.
