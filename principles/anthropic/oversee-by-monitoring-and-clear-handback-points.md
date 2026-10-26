# Oversee by monitoring and clear handback points

Verified: 8 verbatim quotes from 3 sources

Dimension: Roles for humans (human-roles)

Evidence: measurement

How to measure: Instrument agent sessions and track interventions, agent-initiated stops, unapproved destructive actions and success rate on hard tasks over time.

Effective oversight means being able to see what agents do and intervene in time, not approving every action; agents can usually take more autonomy than teams give them. Write down where the agent must stop (blocked, destructive or outside the repo), treat agent-initiated clarification stops as part of oversight, keep steerable work in the main thread, and instrument real sessions rather than relying on pre-deployment evals.

## Quotes

> Experienced users are more likely to let Claude work autonomously, stepping in when something goes wrong or needs redirection.
>
> [Measuring AI agent autonomy in practice](https://www.anthropic.com/research/measuring-agent-autonomy)

> effective oversight doesn’t require approving every action but being in a position to intervene when it matters.
>
> [Measuring AI agent autonomy in practice](https://www.anthropic.com/research/measuring-agent-autonomy)

> Oversight requirements that prescribe specific interaction patterns, such as requiring humans to approve every action, will create friction without necessarily producing safety benefits.
>
> [Measuring AI agent autonomy in practice](https://www.anthropic.com/research/measuring-agent-autonomy)

> From August to December, Claude Code’s success rate on internal users’ most challenging tasks doubled, at the same time that the average number of human interventions per session decreased from 5.4 to 3.3.
>
> [Measuring AI agent autonomy in practice](https://www.anthropic.com/research/measuring-agent-autonomy)

> together they suggest that the latitude granted to models in practice lags behind what they can handle.
>
> [Measuring AI agent autonomy in practice](https://www.anthropic.com/research/measuring-agent-autonomy)

> On the most complex tasks, Claude Code stops to ask for clarification more than twice as often as humans interrupt it.
>
> [Measuring AI agent autonomy in practice](https://www.anthropic.com/research/measuring-agent-autonomy)

> Stop and ask only when you can't continue without me, or before anything destructive: deleting data, force-pushing, or changing anything outside this repository.
>
> [Getting the most out of Opus 5.5 in Claude and Claude Code](https://claude.dev/blog/getting-the-most-out-of-opus-5-5/)

> Use a subagent when a side task like deep search, a log analysis pass, or a dependency audit would clutter your main conversation with intermediate results you won't reference again.
>
> [Steering Claude Code: when to use CLAUDE.md, skills, hooks, and subagents](https://claude.com/resources/articles/steering-claude-code-skills-hooks-rules-subagents-and-more)

## Support

Established: 3 independent sources support this principle.

Expert: Anthropic engineering

Topics: agent-roles, human-roles, metrics

## Related principles

- [Anthropic engineering: Humans own the what, agents own the how](humans-own-the-what-agents-own-the-how.md)
- [Anthropic engineering: Move rules out of prompts and into deterministic gates](move-rules-out-of-prompts-and-into-deterministic-gates.md)
