# Deterministic checks, not the agent, decide when work is done

Verified: 8 verbatim quotes from 29 sources

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: Track the share of agent tasks closed by a passing deterministic check or attached evidence rather than the agent's own report, and compare escaped-defect rates between the two groups.

Agent work counts as finished only when something independent of the agent proves it: tests written first and seen to fail, lint, type checks, builds and hooks on every change, or a stop condition a machine can check. Keep these gates strict, because agents will quietly weaken them to get green. In legacy code, pin current behaviour with characterization tests before agents change it. Tests are necessary but do not replace human understanding.

## Quotes

> Goal: every area the agent will touch gets a safety net first.
>
> [agent-skills: docs/adoption-guide.md](https://github.com/addyosmani/agent-skills/blob/main/docs/adoption-guide.md)

> Every PR must pass: lint, type check, tests, build
>
> [agent-skills: docs/copilot-setup.md](https://github.com/addyosmani/agent-skills/blob/main/docs/copilot-setup.md)

> These three cover the most critical quality gaps in AI-assisted development.
>
> [agent-skills: docs/getting-started.md](https://github.com/addyosmani/agent-skills/blob/main/docs/getting-started.md)

> A checklist the agent uses to confirm the skill's process is complete. Every checkbox should be verifiable with evidence (test output, build result, screenshot, etc.).
>
> [agent-skills: docs/skill-anatomy.md](https://github.com/addyosmani/agent-skills/blob/main/docs/skill-anatomy.md)

> Every skill ends with evidence requirements - tests passing, build output, runtime data. "Seems right" is never sufficient.
>
> [agent-skills: README.md](https://github.com/addyosmani/agent-skills/blob/main/README.md)

> Hooks are what separate “I told the agent to do X” from “the system enforces X.”
>
> [Agent Harness Engineering | AddyOsmani.com](https://addyosmani.com/blog/agent-harness-engineering/)

> The agent is a generator. You need a separate signal that the work is done. Skills bake that signal into every workflow.
>
> [Agent Skills | AddyOsmani.com](https://addyosmani.com/blog/agent-skills/)

> Every run of an agent should be preceded by a contract that defines what it’s trying to do.
>
> [Agentic Autonomy Levels | AddyOsmani.com](https://addyosmani.com/blog/agentic-autonomy-levels/)

## Support

Established: 29 independent sources support this principle.

Expert: Addy Osmani

Topics: agent-roles, deterministic-guardrails, processes

## Related principles

- [Addy Osmani: Grow the harness from real failures and prune it](grow-the-harness-from-real-failures-and-prune-it.md)
- [Addy Osmani: Separate, narrow agent roles with a human orchestrating](separate-narrow-agent-roles-with-a-human-orchestrating.md)
- [Addy Osmani: Let verification and risk set agent autonomy](let-verification-and-risk-set-agent-autonomy.md)
