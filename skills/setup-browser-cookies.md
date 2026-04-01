# /setup-browser-cookies

## TL;DR

### Intent

Use this to make authenticated browser testing easier by reusing an existing logged-in session.

### How to use it

Use it before testing logged-in pages, admin flows, or authenticated QA paths that would otherwise require rebuilding login state from scratch.

### What is actually useful here

This is practical but narrow.

The useful part is simple:

- reuse an existing session
- avoid wasting time on repeated login setup
- make authenticated QA possible in a faster, cleaner way

Beyond that, it is just setup.

## Core Use

Use this for:

- "Import my browser session."
- "Test this logged-in flow."
- "Get the test browser authenticated."

## Minimal Flow

1. Confirm whether the testing browser already shares the real browser session.
2. If not, import or copy the needed domains or cookies.
3. Verify that the authenticated session is actually present.
4. Start the real QA flow only after auth works.

## Rules

- Do not assume auth imported correctly without checking.
- Do not treat cookie setup as the test itself.
- Do be careful with what domains or sessions you import.

## In One Sentence

`/setup-browser-cookies` is useful because logged-in QA is much faster when you can reuse a real session.
