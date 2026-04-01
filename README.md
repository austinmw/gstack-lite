# gstack-lite

`gstack-lite` is a standalone, markdown-only take on gstack: minimal ceremony, lower cognitive load, and no generated skill layer.

The tradeoff is real. Removing the bootstrap code, shared preambles, browser/runtime hooks, and host-specific automation reduces some of the repeatability, safety checks, and operational consistency of the full version. The upside is that each skill is easier to read, copy, tweak, and use as plain text.

These skills are readable first. They explain what to do in plain English instead of asking the reader to execute setup code before they can understand the skill.

Unlike the main repo, `gstack-lite` skills are not generated. Each lite skill is a single canonical markdown file.

## Curation Principle

`gstack-lite` is curated, not copied verbatim.

The rule is simple: keep only the parts of a skill that add real value beyond a generic prompt like "review this PR" or "help me plan this." Boilerplate, theater, host-specific setup, and low-value ceremony are cut aggressively.

If a skill is mostly workflow glue and not much thinking, it stays small or is omitted.

## Tradeoffs

Current tradeoffs of the lite version:

- It loses a lot of the repeatability that comes from explicit tool orchestration and shared preambles.
- It is weaker at host-aware behavior, automation, and stateful workflows.
- Skills that depended on real browser tooling, generated artifacts, or repo-local helper scripts lose some of their force when reduced to plain markdown.
- Some full gstack skills are mostly workflow glue; in lite they are much smaller or omitted.
- The port is intentionally opinionated and lossy. It preserves what seems genuinely useful, not everything the original system did.
- The lite set is intentionally stronger on thinking frameworks than on automation-heavy skills.
- The lite skills are mostly standalone. They do not automatically invoke one another the way the full system did, so the README has to carry more of the workflow map.
- Some original skills are intentionally not included. `/autoplan` was mostly orchestration, and `/design-html` was too tied to a specific toolchain.

## Structure

- `skills/`: prose-first lite versions of individual skills
- `README.md`: short map of the whole skill set

Each lite skill should start with a short TL;DR that answers two questions:

- what is this skill trying to do?
- how should someone actually use it?

## Strongest Skills

If you only read a few, start with these:

- [`/office-hours`](./skills/office-hours.md): the best early-stage idea sharpening skill
- [`/plan-eng-review`](./skills/plan-eng-review.md): one of the strongest planning skills in the set
- [`/review`](./skills/review.md): the strongest code-review skill in the set
- [`/investigate`](./skills/investigate.md): the strongest debugging skill in the set
- [`/qa`](./skills/qa.md): strong when you have real browser access and want a fix-and-verify loop

These are the skills that most clearly add something beyond a generic prompt.

## One-Line Skill List

- `/office-hours`: sharpen an idea
- `/plan-ceo-review`: challenge product scope
- `/plan-eng-review`: harden the implementation plan
- `/plan-design-review`: catch design gaps early
- `/design-consultation`: define visual direction
- `/design-shotgun`: explore multiple design directions
- `/design-review`: audit and polish UI
- `/review`: serious diff review
- `/investigate`: root-cause debugging
- `/cso`: focused security review
- `/benchmark`: performance regression check
- `/codex`: second opinion
- `/qa`: test, fix, re-verify
- `/qa-only`: report-only QA
- `/browse`: browser testing checklist
- `/connect-chrome`: visible shared browser
- `/setup-browser-cookies`: reuse authenticated browser sessions
- `/ship`: final branch/PR checklist
- `/land-and-deploy`: merge, deploy, verify
- `/canary`: short post-deploy watch
- `/document-release`: sync docs to shipped reality
- `/retro`: lightweight retrospective
- `/setup-deploy`: record deploy config
- `/careful`: pause before destructive actions
- `/freeze`: restrict edit scope
- `/guard`: combine caution and scope restriction
- `/unfreeze`: remove scope restriction
- `/learn`: keep project memory

## Active Lite Skills

### Advisory / Plan

- [`/office-hours`](./skills/office-hours.md): sharpen an idea before coding
- [`/plan-ceo-review`](./skills/plan-ceo-review.md): challenge product framing and scope
- [`/plan-eng-review`](./skills/plan-eng-review.md): harden the implementation plan
- [`/plan-design-review`](./skills/plan-design-review.md): catch design gaps before building

### Design

- [`/design-consultation`](./skills/design-consultation.md): define a visual direction
- [`/design-shotgun`](./skills/design-shotgun.md): explore real alternatives
- [`/design-review`](./skills/design-review.md): audit and polish the implemented UI

### Engineering Review / Diagnosis

- [`/review`](./skills/review.md): serious pre-merge diff review
- [`/investigate`](./skills/investigate.md): root-cause-first debugging
- [`/cso`](./skills/cso.md): focused security review
- [`/benchmark`](./skills/benchmark.md): performance regression checks
- [`/codex`](./skills/codex.md): independent second opinion

### QA / Browser Validation

- [`/qa`](./skills/qa.md): test, fix, and re-verify
- [`/qa-only`](./skills/qa-only.md): report-only QA
- [`/browse`](./skills/browse.md): runtime browser testing
- [`/connect-chrome`](./skills/connect-chrome.md): visible shared-browser workflow
- [`/setup-browser-cookies`](./skills/setup-browser-cookies.md): authenticated-browser setup

### Ship / Release / Operate

- [`/ship`](./skills/ship.md): final branch and PR checklist
- [`/land-and-deploy`](./skills/land-and-deploy.md): merge, deploy, and verify
- [`/canary`](./skills/canary.md): short post-deploy watch
- [`/document-release`](./skills/document-release.md): sync docs to reality
- [`/retro`](./skills/retro.md): lightweight retrospective
- [`/setup-deploy`](./skills/setup-deploy.md): record deploy configuration

### Safety / Scope

- [`/careful`](./skills/careful.md): pause before destructive actions
- [`/freeze`](./skills/freeze.md): restrict edit scope
- [`/guard`](./skills/guard.md): combine caution and scope restriction
- [`/unfreeze`](./skills/unfreeze.md): remove the scope restriction

### Memory

- [`/learn`](./skills/learn.md): keep lightweight project memory

## Not Included

- `/autoplan`: omitted because its value was mostly orchestration, and the README workflow already captures the useful part.
- `/design-html`: omitted because the original was too tied to a specific design-to-HTML toolchain to preserve honestly as a general markdown skill.
- `/gstack-upgrade`: omitted because there is no generated/runtime stack to upgrade in the same way.

## Intended Workflow

Do not try to memorize every skill and manually call all of them in sequence.

The better mental model is:

- remember a few entry skills
- start with the one that matches the current phase
- branch only when that phase reveals a real need

The lite skills mostly do not route you automatically. Use this README as the map. The individual skill files should stay readable and mostly standalone.

### The main entry skills

- `/office-hours` when the idea is still fuzzy
- `/investigate` when behavior is broken and you do not yet know why
- `/review` when code exists and you want to know if it is actually safe
- `/qa` when the product needs user-centered testing

### The normal backbone

The default path is:

`/office-hours` → `/plan-ceo-review` → `/plan-eng-review` → `/review` → `/qa` → `/ship` → `/document-release` → `/retro`

That is the backbone, not a mandatory ritual. Use the pieces that match the stage you are in.

### The main branches

- If the work is UI-heavy, branch into `/plan-design-review`, `/design-consultation`, `/design-shotgun`, and `/design-review`.
- If you only want findings and not fixes, use `/qa-only` instead of `/qa`.
- If the code is already shipped, move from `/ship` into `/land-and-deploy`, `/canary`, or `/benchmark` as needed.
- If QA needs a real browser or an authenticated session, use `/browse`, `/connect-chrome`, or `/setup-browser-cookies`.
- If release steps are still tribal knowledge, use `/setup-deploy` before relying on deploy workflows.
- If the risk is security, pull in `/cso` as a focused audit rather than treating it as part of every normal workflow.
- If you want an outside voice, use `/codex` as an optional pressure test, not a default ritual.
- If the work gets risky or messy, use `/careful`, `/freeze`, or `/guard`.
- If old context matters, use `/learn` to recover or prune project memory.

### How to think about the rest

- Some skills are real thinking frameworks: `/plan-eng-review`, `/review`, `/office-hours`.
- Some are workflow wrappers: `/ship`, `/land-and-deploy`.
- Some are control or safety tools: `/careful`, `/freeze`, `/guard`, `/unfreeze`.

The lite version should preserve the first category most aggressively, keep the second category small, and cut the third category unless it adds clear value in plain English.
