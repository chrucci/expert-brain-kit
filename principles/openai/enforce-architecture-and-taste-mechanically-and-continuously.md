# Enforce architecture and taste mechanically and continuously

Verified: 6 verbatim quotes from 1 source

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: Track architectural violations caught per merged PR, engineer time spent on manual cleanup, and how long a bad pattern lasts between being introduced and being fixed.

Agents copy whatever patterns the repository already has, so set strict layering and taste invariants early. Enforce them with custom linters whose error messages tell the agent how to fix the problem, and with scheduled background agents that open small cleanup PRs. This replaces manual cleanup of agent output, which doesn't scale.

## Quotes

> This is the kind of architecture you usually postpone until you have hundreds of engineers. With coding agents, it’s an early prerequisite: the constraints are what allows speed without decay or architectural drift.
>
> [Harness engineering: leveraging Codex in an agent-first world](https://web.archive.org/web/20261006122733id_/https://openai.com/index/harness-engineering/)

> Because the lints are custom, we write the error messages to inject remediation instructions into agent context.
>
> [Harness engineering: leveraging Codex in an agent-first world](https://web.archive.org/web/20261006122733id_/https://openai.com/index/harness-engineering/)

> By enforcing invariants, not micromanaging implementations, we let agents ship fast without undermining the foundation.
>
> [Harness engineering: leveraging Codex in an agent-first world](https://web.archive.org/web/20261006122733id_/https://openai.com/index/harness-engineering/)

> Our team used to spend every Friday (20% of the week) cleaning up “AI slop.” Unsurprisingly, that didn’t scale.
>
> [Harness engineering: leveraging Codex in an agent-first world](https://web.archive.org/web/20261006122733id_/https://openai.com/index/harness-engineering/)

> On a regular cadence, we have a set of background Codex tasks that scan for deviations, update quality grades, and open targeted refactoring pull requests. Most of these can be reviewed in under a minute and automerged.
>
> [Harness engineering: leveraging Codex in an agent-first world](https://web.archive.org/web/20261006122733id_/https://openai.com/index/harness-engineering/)

> Human taste is captured once, then enforced continuously on every line of code.
>
> [Harness engineering: leveraging Codex in an agent-first world](https://web.archive.org/web/20261006122733id_/https://openai.com/index/harness-engineering/)

## Support

Candidate: one source supports this principle so far.

Expert: OpenAI engineering

Topics: agent-roles, deterministic-guardrails, processes

## Related principles

- [OpenAI engineering: Engineers own the harness and turn each agent failure into a lasting fix](engineers-own-the-harness-and-turn-each-agent-failure-into-a-lasting-fix.md)
- [OpenAI engineering: A small team with many agents needs large-organisation structure](a-small-team-with-many-agents-needs-large-organisation-structure.md)
