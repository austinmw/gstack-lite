# /guard

## TL;DR

### Intent

Use this when you want both kinds of safety at once: a pause before destructive actions and a hard boundary around where edits are allowed.

### How to use it

Use it for high-risk sessions: production work, live debugging, or messy repos where both command risk and scope creep matter.

### What is actually useful here

This is mostly convenience.

There is no new thinking beyond combining `/careful` and `/freeze`, but that combination is practical enough to keep.

## Core Use

Use this for:

- risky production work
- debugging in a shared or fragile repo
- sessions where you want maximum caution without juggling two separate habits

## Minimal Flow

1. Turn on destructive-action awareness.
2. Set a tight edit boundary.
3. Keep both protections active until the risky phase is over.

## Rules

- Do not use this as a substitute for understanding the system.
- Do not keep the boundary vague.
- Do not assume caution means paralysis.

## In One Sentence

`/guard` is useful because it combines two small but practical safety controls into one mode.
