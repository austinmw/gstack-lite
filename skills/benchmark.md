# /benchmark

## TL;DR

### Intent

Use this to measure performance in a way that can actually detect regressions over time.

### How to use it

Bring it a running app or a few pages you care about when performance is part of the release conversation.

Use it when you want before/after comparison, not just a one-time speed impression.

### What is actually useful here

This skill is useful if it stays focused on the right things:

- gather real measurements
- capture a baseline
- compare against that baseline
- watch bundle size and request count, not just page load vibes

That is more useful than a generic "check performance" prompt.

## Core Use

Use this for:

- "Benchmark this page."
- "Check for performance regressions."
- "See whether this branch made the app slower."

## Minimal Flow

1. Pick the relevant pages.
2. Measure real performance data.
3. Save or compare against a baseline.
4. Highlight regressions with thresholds that matter.
5. Point to the largest likely contributors.

## What It Should Push On

- large timing regressions
- bundle growth
- request count creep
- slowest first-party resources

## Rules

- Do not guess. Measure.
- Do not rely only on absolute numbers if you have a baseline.
- Do not over-focus on third-party noise if the user cannot change it.

## In One Sentence

`/benchmark` is useful because it turns performance into a regression-tracking discipline instead of a subjective impression.
