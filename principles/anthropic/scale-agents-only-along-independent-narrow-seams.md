# Scale agents only along independent, narrow seams

Verified: 8 verbatim quotes from 6 sources

Dimension: Number of agents (agent-count)

Evidence: measurement

How to measure: Track merge conflicts, rework, tokens per completed task and throughput as the number of parallel agents grows, split by whether sub-tasks were independent.

Parallel agents help only when work splits into independent pieces, such as separate files, benchmarks or services; on coupled work they collide and overwrite each other, and agent teams multiply token spend. Keep each thread narrow and self-contained, verify subagent results before accepting them, keep a small roster of well-scoped specialist agents, and let humans sequence, merge and close threads.

## Quotes

> Split parallel tasks along file boundaries, merge the branches in a sensible order, and expect a session to report problems that another session is already fixing.
>
> [Claude Code in the cloud: a field guide to cloud sessions](https://claude.dev/blog/claude-code-in-the-cloud/)

> On a single laptop, two agents working in one checkout would edit the same files, and would collide on a port unless each picked its own.
>
> [Claude Code in the cloud: a field guide to cloud sessions](https://claude.dev/blog/claude-code-in-the-cloud/)

> Give each service to its own subagent. When a subagent reports back, check its evidence before you accept it.
>
> [Getting the most out of Opus 5.5 in Claude and Claude Code](https://claude.dev/blog/getting-the-most-out-of-opus-5-5/)

> Early testers had Opus 5.5 coordinate parallel subagents on long audits and migrations, with little oversight.
>
> [Getting the most out of Opus 5.5 in Claude and Claude Code](https://claude.dev/blog/getting-the-most-out-of-opus-5-5/)

> That was one thread. During the sprint, we ran more than a hundred and fifty at a time.
>
> [How we made claude.ai 3x faster in two weeks](https://claude.dev/blog/how-we-made-claude-ai-faster/)

> Each teammate is a separate Claude Code instance with its own context window, and it keeps using tokens until it exits.
>
> [What a task costs on Opus 5.5](https://claude.dev/blog/what-a-task-costs-on-opus-5-5/)

> Every agent would hit the same bug, fix that bug, and then overwrite each other's changes. Having 16 agents running didn't help because each was stuck solving the same task.
>
> [Building a C compiler with a team of parallel Claudes](https://www.anthropic.com/engineering/building-c-compiler)

> When a task requires exploring ten or more files, or involves three or more independent pieces of work, that's a strong signal to direct Claude toward subagents.
>
> [How and when to use subagents in Claude Code](https://claude.com/resources/articles/subagents-in-claude-code)

## Support

Established: 6 independent sources support this principle.

Expert: Anthropic engineering

Topics: agent-count, agent-roles, human-roles

## Related principles

- [Anthropic engineering: Independent, human-calibrated agent reviewers](independent-human-calibrated-agent-reviewers.md)
- [Anthropic engineering: Humans own the what, agents own the how](humans-own-the-what-agents-own-the-how.md)
