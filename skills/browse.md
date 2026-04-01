# /browse

## TL;DR

### Intent

Use this when you need to test a real user flow in a browser and gather evidence about what actually happened.

### How to use it

Bring it a URL, page, or flow and use it to verify loading, interactions, network state, console errors, screenshots, and responsive behavior.

This is the browser-shaped QA skill.

### What is actually useful here

This is useful if you truly have browser access.

The genuinely useful parts are:

- verify visible state instead of guessing from code
- compare before and after an action
- check console and network errors alongside the UI
- capture screenshots as evidence
- test flows the way a user experiences them

Without browser tooling, this collapses into a checklist.

## Core Use

Use this for:

- "Open this in a browser."
- "Test this flow."
- "Take screenshots and tell me what broke."

This is not code review. It is runtime verification.

## Minimal Flow

1. Open the page or flow.
2. Confirm the page actually loads and the key UI appears.
3. Trigger the action you care about.
4. Check what changed on screen, in network activity, and in the console.
5. Save evidence if something is wrong.

## What It Should Push On

- pages that "load" but are visibly broken
- silent failed requests
- JavaScript errors hidden behind a working shell
- forms that submit but do not complete the user goal
- responsive layouts that fail on real screen sizes

## Rules

- Do not rely on one screenshot alone.
- Do not ignore console or network evidence.
- Do not say a flow works unless the success state is actually visible.

## In One Sentence

`/browse` is useful because it forces testing against the real runtime state instead of the imagined one.
