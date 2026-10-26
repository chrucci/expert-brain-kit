# Grow agent context gradually

Verified: 5 verbatim quotes from 2 sources

Dimension: Techniques (techniques)

Evidence: experience

How to measure: Track context tokens used before the task starts and the size of rules files against how often humans correct the agent, and check that each added rule or extension cuts a recurring correction.

Start rules files and other context small, and add to them only when real use shows a need. Too much up-front context makes agents less effective and costs more, and newer models often no longer need guidance that older ones did.

## Quotes

> My recommendation would be to build context like rules files up gradually, and not pump too much stuff in there right from the start.
>
> [Context Engineering for Coding Agents](https://martinfowler.com/articles/exploring-gen-ai/context-engineering-coding-agents.html)

> There is a tendency to overengineer the context with unnecessary, copied & pasted instructions up front, in my experience it’s best to build this up iteratively
>
> [Context Engineering for Coding Agents](https://martinfowler.com/articles/exploring-gen-ai/context-engineering-coding-agents.html)

> An agent’s effectiveness goes down when it gets too much context, and too much context is a cost factor as well of course.
>
> [Context Engineering for Coding Agents](https://martinfowler.com/articles/exploring-gen-ai/context-engineering-coding-agents.html)

> Our own expanded harness around that also makes a difference, e.g. how many skills or MCP servers are active. A description of each of them will be sent to the model, and again, take up space in the context window.
>
> [Viability of local models for coding](https://martinfowler.com/articles/exploring-gen-ai/local-models-for-coding-factors.html)

> Coding harnesses can vary significantly in how much overhead they inject into the context window (system prompt, number of tools), which becomes more of a problem locally where we're so resource constrained.
>
> [Viability of local models for coding](https://martinfowler.com/articles/exploring-gen-ai/local-models-for-coding-factors.html)

## Support

Established: 2 independent sources support this principle.

Expert: Birgitta Böckeler

Topics: techniques, tools

## Related principles

- [Birgitta Böckeler: Share harness setups among people with similar contexts](share-harness-setups-among-people-with-similar-contexts.md)
- [Birgitta Böckeler: Choose deliberately who triggers context](choose-deliberately-who-triggers-context.md)
