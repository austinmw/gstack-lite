# /connect-chrome

## TL;DR

### Intent

Use this when headless or abstract browser testing is not enough and you want a visible browser session that both the user and the agent can reason about.

### How to use it

Use it when you need to watch actions live, handle CAPTCHA or MFA handoffs, or collaborate in a real browser window instead of a hidden one.

### What is actually useful here

This is mostly operational.

The useful part is:

- a visible shared browser state
- easier handoff when human interaction is required
- better trust when the user wants to watch what is happening

The specific side-panel and extension mechanics are not the important part in lite form.

## Core Use

Use this for:

- auth flows that need human help
- debugging UI issues where seeing the browser matters
- collaborative browser sessions

## Minimal Flow

1. Launch a visible browser session.
2. Confirm both sides are looking at the same page state.
3. Let the human handle blockers like login, MFA, or CAPTCHA.
4. Resume testing or browsing from that shared state.

## Rules

- Do not overcomplicate this with tooling details unless they matter.
- Do not use it when a normal browser test is enough.
- Do use it when visibility or human handoff is the main constraint.

## In One Sentence

`/connect-chrome` is useful because some browser tasks go much faster once the session is visible and shared.
