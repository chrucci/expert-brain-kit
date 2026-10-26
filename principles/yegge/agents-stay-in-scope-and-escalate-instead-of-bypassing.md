# Agents stay in scope and escalate instead of bypassing

Verified: 8 verbatim quotes from 8 sources

Dimension: Roles for agents (agent-roles)

Evidence: experience

How to measure: Track out-of-scope changes found in review, discovered issues filed per task, failed steps that were escalated versus silently skipped, and unintended external actions by agents.

An agent should file bugs and TODOs it discovers as linked issues instead of fixing them in place. When it is blocked or tooling fails, it should raise a tracked, severity-rated escalation through supervisors rather than skip a gate. Workflows should include explicit gates for human sign-off, and outward-facing actions should be switchable to report-back mode. This marks clearly where agent autonomy ends.

## Quotes

> A **gate** parks a step until something external happens: a human sign-off,
>   a timer, or a GitHub run or PR
>
> [beads: docs/core-concepts/index.md](https://github.com/gastownhall/beads/blob/main/docs/core-concepts/index.md)

> - **`@task-agent`** - Autonomous agent that finds and completes ready tasks
>
> [beads: docs/integrations/claude-code-plugin.md](https://github.com/gastownhall/beads/blob/main/docs/integrations/claude-code-plugin.md)

> so work discovered while executing a task stays attributed to the same repository as that task — regardless of your role
>
> [beads: docs/multi-agent/routing.md](https://github.com/gastownhall/beads/blob/main/docs/multi-agent/routing.md)

> 4. **File discovered work** — `bd create` for bugs found, don't fix them yourself
>
> [gastown: docs/concepts/molecules.md](https://github.com/gastownhall/gastown/blob/main/docs/concepts/molecules.md)

> PR creation to unblock yourself. Escalate to your Witness:
>
> [gastown: docs/contrib-harnesses/polecat-pr-flow/polecat.md](https://github.com/gastownhall/gastown/blob/main/docs/contrib-harnesses/polecat-pr-flow/polecat.md)

> Surfaces `gh pr create` failure as an escalation to Witness, not a silent skip
>
> [gastown: docs/contrib-harnesses/polecat-pr-flow/README.md](https://github.com/gastownhall/gastown/blob/main/docs/contrib-harnesses/polecat-pr-flow/README.md)

> **Concrete failure:** Multiple crew members autonomously posted `gh pr review`
> comments on GitHub during PR review tasks.
>
> [gastown: docs/design/directives-and-overlays.md](https://github.com/gastownhall/gastown/blob/main/docs/design/directives-and-overlays.md)

> When agents hit blockers, they escalate rather than waiting:
>
> [gastown: README.md](https://github.com/gastownhall/gastown/blob/main/README.md)

## Support

Established: 8 independent sources support this principle.

Expert: Steve Yegge

Topics: agent-roles, human-roles, processes

## Related principles

- [Steve Yegge: Humans keep judgment, taste and the final say](humans-keep-judgment-taste-and-the-final-say.md)
- [Steve Yegge: Separate worker, supervisor and merger roles; supervisors are a safety net](separate-worker-supervisor-and-merger-roles-supervisors-are-a-safety-net.md)
