# Encode team process as shared, tested skill workflows

Verified: 8 verbatim quotes from 11 sources

Dimension: Techniques (techniques)

Evidence: measurement

How to measure: Track how often agents skip mandated steps, how many skill-routing regressions CI catches against those found later, and how far setups drift across engineers and tools.

A team needs one enforceable standard rather than a private workflow per engineer. That means one versioned, portable skill library with a single router, shared across every agent tool and kept separate from each repo's configuration. Write skills as step-by-step workflows or explicit graphs with exit criteria and tables that rebut the excuses agents give for skipping steps, keep them model-neutral, and test their routing deterministically in CI.

## Quotes

> Maintaining per-agent metadata by hand across every skill is repetitive, drifts out of sync, and is easy to get wrong. A better approach is to keep a single source of truth and generate the agent-specific output:
>
> [agent-skills: docs/advanced-per-agent-configuration.md](https://github.com/addyosmani/agent-skills/blob/main/docs/advanced-per-agent-configuration.md)

> The same root-level `skills/` directory used by Claude Code is consumed by Codex, so no files are copied or duplicated.
>
> [agent-skills: docs/codex-setup.md](https://github.com/addyosmani/agent-skills/blob/main/docs/codex-setup.md)

> For a team, the calculus shifts toward shared structure and guardrails you can enforce: named phases, review personas, checklists, and evals that fail CI are what keep five people (and their agents) converging on the same standard rather than five private workflows.
>
> [agent-skills: docs/comparison.md](https://github.com/addyosmani/agent-skills/blob/main/docs/comparison.md)

> Treat `agent-skills/skills/` (or a cloned [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills)) as **upstream** — sync into `.cursor/skills/`, do not edit only upstream and expect Cursor to see it.
>
> [agent-skills: docs/cursor-setup.md](https://github.com/addyosmani/agent-skills/blob/main/docs/cursor-setup.md)

> The repo eats its own cooking: verification is non-negotiable for skills, and it's non-negotiable for contributions to the repo too.
>
> [agent-skills: docs/developer-onboarding.md](https://github.com/addyosmani/agent-skills/blob/main/docs/developer-onboarding.md)

> Map the user's intent to the matching skill automatically:
>
> [agent-skills: docs/opencode-setup.md](https://github.com/addyosmani/agent-skills/blob/main/docs/opencode-setup.md)

> These are excuses agents use to skip important steps, paired with rebuttals. They prevent the agent from rationalizing its way out of following the process.
>
> [agent-skills: docs/skill-anatomy.md](https://github.com/addyosmani/agent-skills/blob/main/docs/skill-anatomy.md)

> AI coding agents default to the shortest path - which often means skipping specs, tests, security reviews, and the practices that make software reliable.
>
> [agent-skills: README.md](https://github.com/addyosmani/agent-skills/blob/main/README.md)

## Support

Established: 11 independent sources support this principle.

Expert: Addy Osmani

Topics: deterministic-guardrails, processes, techniques, tools

## Related principles

- [Addy Osmani: Keep agent context lean, hand-written and earned](keep-agent-context-lean-hand-written-and-earned.md)
- [Addy Osmani: Start from a precise, human-approved spec and record intent](start-from-a-precise-human-approved-spec-and-record-intent.md)
