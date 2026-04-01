# /cso

## TL;DR

### Intent

Use this for a focused security review when the codebase, diff, or system surface is important enough that "probably fine" is not good enough.

### How to use it

Bring it a repo, diff, subsystem, or trust boundary and ask for a real security posture review.

Use it on auth flows, payments, file uploads, webhooks, AI features, CI/CD, infra, or anything internet-facing.

### What is actually useful here

This can be useful, but only if it stays focused.

The genuinely useful parts are:

- start with attack surface, secrets, CI/CD, and dependencies before nitpicking code
- map trust boundaries and real exploit paths
- separate verified findings from weak suspicions
- prioritize by severity and exploitability
- include LLM or tool-use security when the product actually has that surface

The rest can easily drift into security theater if it is not scoped tightly.

## Core Use

Use this for:

- "Do a security review."
- "Threat model this system."
- "What are the real exploit paths here?"

This is not a generic lint pass and not a compliance checklist.

## Minimal Flow

1. Understand the stack, trust boundaries, and internet-facing surface.
2. Look for the highest-risk paths first: auth, secrets, CI/CD, webhooks, uploads, dependencies.
3. Trace whether those paths are actually protected.
4. Distinguish confirmed issues from plausible but unverified concerns.
5. Leave a prioritized report with remediation ideas.

## What It Should Push On

- auth and authorization gaps
- leaked or mishandled secrets
- supply-chain and CI/CD risk
- unsafe webhooks and external integrations
- prompt injection, tool abuse, or data exfiltration in AI systems
- infrastructure shortcuts that quietly expose prod

## Rules

- Do not flood the output with low-confidence noise.
- Do not report severity without explaining why.
- Do not turn every app into an enterprise audit.
- Do be explicit about what was verified versus inferred.

## In One Sentence

`/cso` is useful when it behaves like a focused exploit-path audit, not when it turns into a giant checklist.
