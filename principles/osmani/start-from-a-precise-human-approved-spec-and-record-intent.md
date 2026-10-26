# Start from a precise, human-approved spec and record intent

Verified: 8 verbatim quotes from 13 sources

Dimension: Processes (processes)

Evidence: experience

How to measure: Compare rework and rejection rates for agent tasks that started from an approved spec with acceptance criteria against tasks that started from a loose prompt.

Agent work should go through gated phases: spec, plan, tasks, then implementation. A human approves the spec and plan before any code is written, and the approved files, kept in version control, carry the work between sessions. Spec quality is the biggest lever on output, and ambiguity multiplies across parallel agents, so specs and decision records must capture goals, constraints and the reasons behind them, not just current behaviour.

## Quotes

> To enforce strict skill compliance (e.g. requiring a spec or plan before writing code), copy or link `AGENTS.md` into the root of your workspace.
>
> [agent-skills: docs/antigravity-setup.md](https://github.com/addyosmani/agent-skills/blob/main/docs/antigravity-setup.md)

> Write no product code — show me the plan and wait for my approval.
>
> [agent-skills: docs/copilot-setup.md](https://github.com/addyosmani/agent-skills/blob/main/docs/copilot-setup.md)

> The repo ships 9 slash commands under `.gemini/commands/`: 8 lifecycle commands plus the `/webperf` specialist audit.
>
> [agent-skills: docs/gemini-cli-setup.md](https://github.com/addyosmani/agent-skills/blob/main/docs/gemini-cli-setup.md)

> Keep them in version control during development so the human and the agent have a shared source of truth.
>
> [agent-skills: docs/getting-started.md](https://github.com/addyosmani/agent-skills/blob/main/docs/getting-started.md)

> Never skip required steps such as spec, plan, or test when a skill demands them.
>
> [agent-skills: docs/opencode-setup.md](https://github.com/addyosmani/agent-skills/blob/main/docs/opencode-setup.md)

> Write a PRD covering objectives, commands, structure, code style, testing, and boundaries before any code
>
> [agent-skills: README.md](https://github.com/addyosmani/agent-skills/blob/main/README.md)

> Before prompting anything, you write a design doc or spec  -  sometimes with AI assistance. You break the work into well-defined tasks. You decide on the architecture.
>
> [Agentic Engineering | AddyOsmani.com](https://addyosmani.com/blog/agentic-engineering/)

> “Build me an app” burns tokens while agents flail. “Implement these five clearly-defined API endpoints according to this specification” produces something good.
>
> [Claude Code Swarms | AddyOsmani.com](https://addyosmani.com/blog/claude-code-agent-teams/)

## Support

Established: 13 independent sources support this principle.

Expert: Addy Osmani

Topics: deterministic-guardrails, human-roles, processes, techniques

## Related principles

- [Addy Osmani: Humans own the outer loop: intent, judgment and the ship decision](humans-own-the-outer-loop-intent-judgment-and-the-ship-decision.md)
- [Addy Osmani: Review capacity is the bottleneck, so size work to it](review-capacity-is-the-bottleneck-so-size-work-to-it.md)
