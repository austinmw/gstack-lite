# /land-and-deploy

## TL;DR

### Intent

Use this after a PR is ready to actually merge it, wait for deploy, and verify production health.

### How to use it

Bring it an open PR or a feature branch that already has a PR and is ready to land.

Use it when you want merge, deploy, and post-deploy verification treated as one release action.

### What is actually useful here

This is mostly workflow glue, not deep reasoning.

The genuinely useful part is the sequencing:

- verify readiness before merge
- merge in the right way
- wait for deployment instead of assuming
- verify production after deploy
- have a clear response if prod looks unhealthy

If you already have strong release automation and habits, this adds less.

## Core Use

Use this for:

- "Land this PR."
- "Merge and verify production."
- "Deploy it and make sure it is healthy."

## Minimal Flow

1. Find the correct PR.
2. Confirm it is actually ready to merge.
3. Merge it.
4. Wait for deploy or CI/CD completion.
5. Verify production health.
6. Escalate quickly if the deploy looks bad.

## Rules

- Do not merge blindly.
- Do not treat "merged" as the same as "successfully deployed."
- Do not skip the production verification step.

## In One Sentence

`/land-and-deploy` is useful mostly because it treats merge, deploy, and production verification as one operation instead of three disconnected steps.
