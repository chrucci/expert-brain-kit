# Choose deliberately who triggers context

Verified: 2 verbatim quotes from 1 source

Dimension: Roles for agents (agent-roles)

Evidence: opinion

How to measure: For each piece of context the model is left to load, log how often it actually gets loaded on the tasks where it is relevant.

If the model decides what context to load, agents can run unsupervised, but nobody can be sure the context gets loaded. If a human triggers it, the team gains control and loses automation, and hooks fire at fixed points in the run. Pick among these based on how much autonomy the task can safely have.

## Quotes

> Allowing the LLM to decide when to load context is a prerequisite for running agents in an unsupervised way.
>
> [Context Engineering for Coding Agents](https://martinfowler.com/articles/exploring-gen-ai/context-engineering-coding-agents.html)

> A human invocation of context gives us control, but reduces the level of automation overall.
>
> [Context Engineering for Coding Agents](https://martinfowler.com/articles/exploring-gen-ai/context-engineering-coding-agents.html)

## Support

Candidate: one source supports this principle so far.

Expert: Birgitta Böckeler

Topics: agent-roles, techniques

## Related principles

- [Birgitta Böckeler: Verify outcomes instead of prescribing the agent's process](verify-outcomes-instead-of-prescribing-the-agent-s-process.md)
- [Birgitta Böckeler: Grow agent context gradually](grow-agent-context-gradually.md)
