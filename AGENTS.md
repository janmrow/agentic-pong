# AGENTS.md

## Purpose

This repository is a minimal browser Pong project and an experiment in agentic software engineering.

Prefer the smallest clear solution that satisfies the product specification. Do not add complexity, features, abstractions, dependencies, or process without a concrete need.

## Sources of truth

Read these before changing the project:

1. `docs/spec.md` — product behavior and player experience.
2. `AGENTS.md` — engineering and workflow rules.
3. Code, tests, and repository automation — executable project state.

`README.md` is the public project overview. Keep it concise and consistent with the sources above.

## Technology constraints

Use:

* TypeScript with strict type checking
* vanilla browser APIs
* Canvas 2D
* Vite
* npm
* Biome
* Vitest
* Playwright
* GitHub Actions
* GitHub Pages

Keep runtime dependencies at zero unless an explicit requirement makes one necessary.

Do not replace the stack or introduce frameworks, architectural layers, or additional tooling without a concrete task-level reason.

## Engineering principles

* Keep the implementation small, direct, and readable.
* Prefer plain functions and data over speculative abstractions.
* Keep gameplay logic deterministic where practical.
* Separate product behavior from rendering when that improves testability.
* Avoid duplicate logic, dead code, placeholders, and unnecessary configuration.
* Do not add features outside `docs/spec.md`.
* Make the repository understandable from the files in the repository, not from chat history.

## Verification

The canonical quality command will be:

```bash
npm run verify
```

Once implemented, it must cover the repository's required automated checks, including formatting/linting, type checking, tests, and production build validation.

Before that command exists, use the checks appropriate to the current bootstrap task.

Tests should be few, stable, and behavior-focused. Prefer strong coverage of important invariants over high test counts or coverage targets.

## Playtest gate

Any pull request that changes gameplay, rendering, interaction, or other player-visible runtime behavior requires a successful human playtest of the production build before the pull request is opened.

* Agents must never approve their own playtests.
* Failed playtest observations are feedback for the next iteration, not permanent repository notes.
* Approved production builds will be recorded in `docs/playtests.md` once the playtest tooling is introduced.
* A changed production build invalidates the previous approval.
* Documentation-only, test-only, CI-only, and other non-runtime changes do not require a new playtest unless they alter the production build.

## Git workflow

Create short-lived branches from `main`.

Branch names:

```text
<type>/<short-description>
```

Allowed types:

```text
feat
fix
test
docs
ci
refactor
chore
```

Commit messages and pull request titles use the same simple convention:

```text
<type>: <short imperative summary>
```

Examples:

```text
docs: define project foundation
feat: add deterministic game core
fix: prevent paddle tunneling
```

Keep pull requests small and focused.

Use this pull request structure:

```markdown
## What

- concise summary of the change

## Verification

- checks performed
```

Use squash merge into `main`.

## Definition of done

A change is done when:

* it satisfies the relevant product specification;
* the implementation is no more complex than necessary;
* relevant automated verification passes;
* relevant tests are added or updated;
* independent review findings are resolved;
* a required human playtest has passed;
* the pull request accurately describes the completed change.
