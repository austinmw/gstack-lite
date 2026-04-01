# /careful

## TL;DR

### Intent

Use this to force a pause before destructive commands or high-blast-radius operations.

### How to use it

Turn it on when you are working in production, touching shared infrastructure, running risky git commands, or doing anything that could be painful to undo.

### What is actually useful here

This is simple, but genuinely practical.

The useful part is just the habit:

- identify destructive actions before running them
- restate the blast radius
- confirm rollback or backup assumptions
- make the user choose intentionally

There is no deeper intelligence here. It is a good safety brake.

## Core Use

Use this for:

- deleting data
- force-pushing or history rewrites
- risky database commands
- production-impacting shell commands

## Minimal Flow

1. Notice that the next action is destructive or hard to reverse.
2. State exactly what could be lost or broken.
3. Confirm whether a rollback exists.
4. Proceed only if the risk is understood.

## Rules

- Do not normalize destructive commands.
- Do not hide the blast radius in vague language.
- Do not skip the pause because the command is familiar.

## In One Sentence

`/careful` is useful because a short forced pause prevents a lot of avoidable damage.
