# /qa-only

## TL;DR

### Intent

Use this to test a product like a real user and report what is broken without making any code changes.

### How to use it

Bring it a running app, staging URL, or local URL when you want a QA report but do not want the agent fixing anything yet.

### What is actually useful here

This is a small but legitimate skill.

The useful part is simply the constraint: do the same kind of user-centered QA pass as `/qa`, but stop at reporting. That is valuable when you want findings without churn in the branch.

## Core Use

Use this for:

- "Test this, but don't change code."
- "Give me a QA report only."
- "Find bugs before I decide what to fix."

## Minimal Flow

1. Decide the testing scope.
2. Test the main user flows.
3. Triage findings by severity.
4. Write clear repro steps and evidence.
5. Stop.

## Rules

- Do not edit code.
- Do not suggest sprawling speculative fixes.
- Do report like a QA lead, not like a casual tester.

## In One Sentence

`/qa-only` is useful because it preserves the disciplined testing part of `/qa` while removing the implementation side entirely.
