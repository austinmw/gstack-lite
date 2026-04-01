# /qa

## TL;DR

### Intent

Use this to test like a real user, fix the bugs that matter, and verify that the fixes actually worked.

### How to use it

Bring it a running app, staging URL, local URL, or branch that is supposed to be ready for user testing.

Use it when you want a test-fix-retest loop, not just a passive bug report.

### What is actually useful here

The useful part is the loop:

- test real flows
- triage by severity
- make minimal fixes
- re-test each fix
- add regression coverage when it is worth it

That is better than a generic "test this site" prompt. The catch is that this skill is much more valuable with real browser and edit access than as pure text.

## Core Use

Use this for:

- "Test this app."
- "Find what is broken."
- "Fix what a user would hit."

If you want report-only behavior, use `/qa-only` instead.

## Minimal Flow

1. Decide the testing scope and environment.
2. Establish a baseline by testing the main flows.
3. Triage findings by severity.
4. Fix only the issues worth fixing in this pass.
5. Re-test each fix.
6. Summarize what was fixed, deferred, and how confident we are now.

## What It Should Push On

- broken primary flows
- auth or session failures
- form and state issues
- empty and error states
- console/runtime errors that signal deeper problems
- regressions introduced while fixing something else

## Rules

- Do not only test the happy path.
- Do not treat every cosmetic issue like a release blocker.
- Do not claim a fix without re-verifying it.
- Do not refactor broadly while fixing bugs found in QA.

## In One Sentence

`/qa` is useful because it turns testing into a disciplined fix-and-verify workflow instead of a vague exploratory pass.
