# Keep subagent waves small and the orchestrator's context clean

Verified: 8 verbatim quotes from 5 sources

Dimension: Number of agents (agent-count)

Evidence: experience

How to measure: Compare orientation tokens, total session cost and end-to-end cycle time as the number of parallel agents grows, and survey the fatigue of humans running them.

Group work that shares a mental model into one agent, prefer two to four agents per wave, and treat overlapping file ownership as a reason to merge tasks. Subagents earn their place by keeping exploration noise out of the orchestrator's context, not by speed, and more concurrent agents mainly add cognitive load on the humans running them.

## Quotes

> Tasks that need the same mental model should usually stay together.
>
> [The Orchestrator's Tax](https://martinfowler.com/articles/orchestrator-tax.html)

> Prefer two to four agents in one wave. If the orchestrator wants five or more, it should first ask whether tasks sharing files or conventions ought to be merged.
>
> [The Orchestrator's Tax](https://martinfowler.com/articles/orchestrator-tax.html)

> Treat overlapping file ownership as a consolidation signal, not a cue to spawn more agents.
>
> [The Orchestrator's Tax](https://martinfowler.com/articles/orchestrator-tax.html)

> Exploration, repeated file reads, failed approaches, and noisy intermediate reasoning are meant to stay in worker contexts and never make the trip back to the main thread.
>
> [The Orchestrator's Tax](https://martinfowler.com/articles/orchestrator-tax.html)

> Developers using AI tools are finding that while they’re capable of producing a lot more, faster, they’re becoming fatigued and even burned out with these new workflows and modes of interaction.
>
> [Reflections on the future of Software Engineering retreat](https://www.thoughtworks.com/insights/articles/reflections-future-software-engineering-retreat)

> A larger context window still leaves the early instruction buried. Capacity and relevance are different problems.
>
> [Designing agentic delivery for bounded context and bounded human attention](https://www.thoughtworks.com/insights/blog/architecture/designing-agentic-delivery-for-bounded-context-and-bounded-human-attention)

> We also discussed the perils of the cognitive load of managing a swarm of agents, and agreed that what really matters is focusing on effectiveness and optimizing workflow bottlenecks.
>
> [Last week in AI | 16 March](https://www.thoughtworks.com/insights/blog/generative-ai/last-week-ai-16-march)

> Developers practicing advanced agentic engineering reported a paradox of exhaustion and euphoria. Spawning eight or nine sub-agents to execute tasks concurrently changes the role from an individual contributor who writes code to a kind of overseer or structural validator.
>
> [Caught between ephemerality and materiality](https://www.thoughtworks.com/insights/blog/technology-strategy/caught-between-ephemerality-materiality-reflections-fose-europe)

## Support

Established: 5 independent sources support this principle.

Expert: Thoughtworks

Topics: agent-count, human-roles, techniques

## Related principles

- [Thoughtworks: Give parallel agents a deliberate coordination channel](give-parallel-agents-a-deliberate-coordination-channel.md)
- [Thoughtworks: Verification is the bottleneck; spend human review by risk](verification-is-the-bottleneck-spend-human-review-by-risk.md)
