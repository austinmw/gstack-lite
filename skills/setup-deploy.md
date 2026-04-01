# /setup-deploy

## TL;DR

### Intent

Use this once to record how deployment works so later release steps know where production is and how to verify it.

### How to use it

Bring it the deploy platform, production URL, health check, and any status or trigger commands.

Use it before relying on `/land-and-deploy` or post-deploy verification.

### What is actually useful here

This is moderately useful.

The genuinely useful parts are:

- capture deployment knowledge in one place
- stop relying on tribal memory for production URLs and health checks
- make later merge and deploy steps less ad hoc
- force the team to answer how success is actually verified

The automatic platform detection in the full version is nice, but it is not the real value.

## Core Use

Use this for:

- "How do we deploy this project?"
- "Set up release verification."
- "Record the prod URL and health check."

This is deployment configuration, not deployment itself.

## Minimal Flow

1. Identify the platform or deployment path.
2. Record the production URL.
3. Record how to tell whether a deploy succeeded.
4. Record any pre-merge, deploy, or post-deploy hooks that matter.
5. Save it somewhere durable so release steps can reuse it.

## What It Should Push On

- missing or ambiguous production URLs
- deploys that cannot be verified
- health checks nobody actually knows
- manual tribal knowledge that only one person remembers

## Rules

- Do not store secrets in the config.
- Do not claim deploy automation exists if it does not.
- Do confirm the recorded verification path is real.

## In One Sentence

`/setup-deploy` is useful because release workflows get much safer once deploy verification is written down instead of assumed.
