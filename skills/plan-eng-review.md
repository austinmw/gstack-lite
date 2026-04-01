# /plan-eng-review

## TL;DR

### Intent

Use this when the plan is mostly chosen and you want to make it engineering-grade before anyone starts implementing.

### How to use it

Bring it a design doc or implementation plan after the product direction is mostly settled.

Use it right before coding starts, or whenever the plan feels plausible but not yet trustworthy.

### What is actually useful here

This is one of the stronger skills.

The genuinely useful parts are:

- challenge scope before architecture
- reuse existing code before adding new systems
- enumerate failure modes explicitly
- require a real test and observability story
- prefer boring, reversible, minimum-change designs

That goes meaningfully beyond a generic "review this plan."

## Core Use

Use this for:

- "Review the architecture."
- "Lock the implementation plan."
- "What technical risks are we missing?"

This is not product strategy and not code review. It is plan hardening.

## Minimal Flow

1. Understand the plan and what success means.
2. Ask what existing code or flows already solve parts of it.
3. Cut unnecessary scope and abstraction first.
4. Review architecture, state, data flow, and dependencies.
5. Spell out failure modes and edge cases.
6. Define the test and observability expectations.
7. Leave behind a simpler, clearer plan.

## What It Should Push On

- parallel systems that duplicate existing behavior
- too many new classes, services, or layers
- vague error handling
- missing test coverage
- plans that only work on the happy path
- complexity that could have been avoided

## Rules

- Do not start implementing.
- Do not accept hand-wavy architecture language.
- Do not recommend novelty without a strong reason.
- Do make an opinionated recommendation.

## In One Sentence

`/plan-eng-review` is useful because it turns a plausible plan into one that is much less likely to fall apart during implementation.
