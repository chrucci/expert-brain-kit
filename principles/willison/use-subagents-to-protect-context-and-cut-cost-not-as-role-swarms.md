# Use subagents to protect context and cut cost, not as role swarms

Verified: 8 verbatim quotes from 3 sources

Dimension: Number of agents (agent-count)

Evidence: measurement

How to measure: Track cost per task by main session, subagent and model, along with root-context compaction and task success, as delegation and subagent count change.

Subagents are worth using to keep token-heavy exploration out of the root agent's context, and to fan out routine coding to cheaper, faster models chosen by the top model, which session cost data shows saves real money. Splitting work across dozens of specialist role agents adds coordination cost without a matching benefit.

## Quotes

> I really should have [followed my own advice](https://simonwillison.net/2026/Jul/3/judgement/) and leaned more heavily into subagents with cheaper models.
>
> [sqlite-utils 4.0rc2, mostly written by Claude Fable (for about $149.25)](https://simonwillison.net/2026/Jul/5/sqlite-utils-fable/)

> Carefully managing the context such that it fits within those limits is critical to getting great results out of a model.
>
> [Subagents - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/subagents/)

> provide a simple but effective way to handle larger tasks without burning through too much of the coding agent’s valuable top-level context.
>
> [Subagents - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/subagents/)

> The principle advantage of this kind of subagent is that it can work with a fresh context in a way that avoids spending tokens from the parent’s available limit.
>
> [Subagents - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/subagents/)

> While it can be tempting to go overboard breaking up tasks across dozens of different specialist subagents, it's important to remember that the main value of subagents is in preserving that valuable root context and managing token-heavy operations.
>
> [Subagents - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/subagents/)

> Your root coding agent is perfectly capable of debugging or reviewing its own output provided it has the tokens to spare.
>
> [Subagents - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/subagents/)

> Subagents can also provide a significant performance boost by having the parent agent run multiple subagents at the same time, potentially also using faster and cheaper models such as Claude Haiku to accelerate those tasks.
>
> [Subagents - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/subagents/)

> Tell Fable to use other models for smaller tasks, applying its own judgement about which model to use.
>
> [Fable's judgement](https://simonwillison.net/2026/Jul/3/judgement/)

## Support

Established: 3 independent sources support this principle.

Expert: Simon Willison

Topics: agent-count, techniques, tools

## Related principles

- [Simon Willison: Human cognitive capacity limits agents per person and team size](human-cognitive-capacity-limits-agents-per-person-and-team-size.md)
