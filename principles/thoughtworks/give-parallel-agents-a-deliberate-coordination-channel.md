# Give parallel agents a deliberate coordination channel

Verified: 7 verbatim quotes from 1 source

Dimension: Number of agents (agent-count)

Evidence: experience

How to measure: Track how often parallel agents duplicate work or block on integration points, and CI queue time as agent push frequency changes, with and without a dedicated coordination channel.

Many agents in one repo can coordinate through shared, spec-linked plans that show work in progress and let one agent integrate another's work when it lands. That coordination should be built on purpose, on a channel separate from source control, because constant commits for coordination overload CI.

## Quotes

> We were directing the agents to plan, to scope work to sections in the spec and to create plans linked to those sections. These plans were stored in the repo. All agents were working off the same spec using the same numbered and identified sections.
>
> [An Accidental Blackboard](https://martinfowler.com/articles/exploring-gen-ai/an-accidental-blackboard.html)

> One agent would mark a line of the plan as in progress, the other agent would see that and not work on that line.
>
> [An Accidental Blackboard](https://martinfowler.com/articles/exploring-gen-ai/an-accidental-blackboard.html)

> we directed the agent working on the verifier to look at plans and source, monitor the repo, and when the work for the cost model lands start to integrate it. And it did.
>
> [An Accidental Blackboard](https://martinfowler.com/articles/exploring-gen-ai/an-accidental-blackboard.html)

> With lot of agents working in one repo, build pipelines suffered. To deal with this we introduced a discipline: our agents were to continually commit and rebase from main.
>
> [An Accidental Blackboard](https://martinfowler.com/articles/exploring-gen-ai/an-accidental-blackboard.html)

> The frequent commits were overloading our CI pipeline. We switched to only push when a more coherent chunk of change was complete.
>
> [An Accidental Blackboard](https://martinfowler.com/articles/exploring-gen-ai/an-accidental-blackboard.html)

> because it was accidental, I’m not convinced I would be able to reliably prompt our agents into doing it again.
>
> [An Accidental Blackboard](https://martinfowler.com/articles/exploring-gen-ai/an-accidental-blackboard.html)

> As well as creating this intentionally, rather than accidentally, I believe you want this communication channel to be sitting independently of source control.
>
> [An Accidental Blackboard](https://martinfowler.com/articles/exploring-gen-ai/an-accidental-blackboard.html)

## Support

Candidate: one source supports this principle so far.

Expert: Thoughtworks

Topics: agent-count, processes, tools

## Related principles

- [Thoughtworks: Keep subagent waves small and the orchestrator's context clean](keep-subagent-waves-small-and-the-orchestrator-s-context-clean.md)
