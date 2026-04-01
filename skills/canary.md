# /canary

## TL;DR

### Intent

Use this right after deploy to catch obvious production breakage early.

### How to use it

Bring it a production URL or the set of pages you most care about after a release.

Use it when you want a short post-deploy watch instead of assuming that a green deploy means a healthy app.

### What is actually useful here

The useful part is not the monitoring theater. It is the baseline mindset:

- compare against what the app looked like before
- watch a few high-value pages
- check for new console errors, broken loads, and large regressions
- only escalate if the issue looks persistent rather than transient

That is a decent discipline even in lite form.

## Core Use

Use this for:

- "Watch production after this deploy."
- "Do a canary pass on the main flows."
- "Verify that this release did not obviously break the app."

## Minimal Flow

1. Choose the few pages that matter most.
2. Capture a baseline if you can.
3. Check those pages after deploy.
4. Compare for obvious regressions.
5. Escalate only if the issue persists or is severe.
6. End with a healthy/degraded/broken verdict.

## What It Should Push On

- pages that no longer load
- new console errors
- major performance regressions
- visible breakage on core flows

## Rules

- Do not monitor everything.
- Do not alert on one-off noise if it looks transient.
- Do include evidence for anything you flag.

## In One Sentence

`/canary` is useful because it forces a short, evidence-based post-deploy check instead of blind optimism.
