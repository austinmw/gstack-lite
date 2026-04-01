# gstack-lite

`gstack-lite` is a markdown-only, low-ceremony version of gstack.

It keeps the parts of the original skills that are genuinely useful as thinking frameworks and strips out most of the bootstrap code, host-specific automation, and prompt theater.

Each skill is a single canonical markdown file in `skills/`.

## Principles

- Keep only what adds value beyond a generic prompt.
- Prefer readable plain English over setup instructions.
- Preserve strong judgment frameworks; shrink or omit workflow glue.

## Tradeoffs

- Less repeatable than full gstack.
- Weaker automation, browser integration, and host-aware behavior.
- Stronger on thinking than on tool-heavy workflows.
- Some original skills are intentionally omitted.

## Start Here

If you only read a few skills, start with these:

- [`/office-hours`](./skills/office-hours.md)
- [`/plan-eng-review`](./skills/plan-eng-review.md)
- [`/review`](./skills/review.md)
- [`/investigate`](./skills/investigate.md)
- [`/qa`](./skills/qa.md)

## Skill List

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

## How to Use It

Do not try to memorize every skill or run all of them in order.

Use a few entry skills and branch only when the current phase needs it.

### Main Entry Skills

- `/office-hours` when the idea is still fuzzy
- `/investigate` when something is broken and you do not yet know why
- `/review` when code exists and you want to know if it is safe
- `/qa` when the product needs user-centered testing

### Default Backbone

`/office-hours` → `/plan-ceo-review` → `/plan-eng-review` → `/review` → `/qa` → `/ship` → `/document-release` → `/retro`

Use the parts that match the stage you are in. This is a default path, not a ritual.

### Common Branches

- UI-heavy work: `/plan-design-review` → `/design-consultation` → `/design-shotgun` → `/design-review`
- Findings only: `/qa-only`
- Shipped code: `/land-and-deploy`, `/canary`, `/benchmark`
- Security-sensitive work: `/cso`
- Outside voice: `/codex`
- Browser/session setup: `/browse`, `/connect-chrome`, `/setup-browser-cookies`
- Release setup: `/setup-deploy`
- Risky or messy work: `/careful`, `/freeze`, `/guard`, `/unfreeze`
- Old context or recurring lessons: `/learn`

## Not Included

- `/autoplan`: omitted because its value was mostly orchestration.
- `/design-html`: omitted because it depended too heavily on a specific toolchain.
- `/gstack-upgrade`: omitted because lite has no generated/runtime layer to upgrade.
