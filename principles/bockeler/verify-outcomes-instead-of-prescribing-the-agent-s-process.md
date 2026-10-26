# Verify outcomes instead of prescribing the agent's process

Verified: 8 verbatim quotes from 2 sources

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: measurement

How to measure: Run the same tasks with and without process instructions such as TDD, comparing blind quality rankings, mutation scores and tokens per task, and compare rule compliance for prompt-only rules versus hook-enforced ones.

Instructions only make good behaviour more likely, and prescribing a detailed workflow such as TDD added cost without measurable quality gains. Put anything that must always happen into deterministic hooks, and invest in automated feedback on results rather than in telling the agent how to work.

## Quotes

> Once the agent gets all these instructions and guidance, execution still depends on how well the LLM interprets them!
>
> [Context Engineering for Coding Agents](https://martinfowler.com/articles/exploring-gen-ai/context-engineering-coding-agents.html)

> However, sometimes people talk about these features with phrases like “ensure it does X”, or “prevent hallucinations”.
>
> [Context Engineering for Coding Agents](https://martinfowler.com/articles/exploring-gen-ai/context-engineering-coding-agents.html)

> When you want something to happen deterministically every single time you edit a file, execute a command, call an MCP server, etc.
>
> [Context Engineering for Coding Agents](https://martinfowler.com/articles/exploring-gen-ai/context-engineering-coding-agents.html)

> Based on Opus's judgment of the quality of the outcomes, there was no clearly discernable difference based on TDD workflow versus no TDD workflow.
>
> [TDD inside the agent loop - theater or actual value?](https://martinfowler.com/articles/exploring-gen-ai/tdd-in-the-agent-loop.html)

> TDD reliably cost several times more, how many times exactly is variable.
>
> [TDD inside the agent loop - theater or actual value?](https://martinfowler.com/articles/exploring-gen-ai/tdd-in-the-agent-loop.html)

> I personally have stopped telling my coding agents to write tests first, let alone do TDD (which I never did, to be honest), until I see evals or other strong arguments that convince me otherwise.
>
> [TDD inside the agent loop - theater or actual value?](https://martinfowler.com/articles/exploring-gen-ai/tdd-in-the-agent-loop.html)

> Instead, we should find as many ways as we can to monitor the outcomes and give feedback. That feedback should be automated wherever possible, and we need to carefully think about where we insert ourselves as arbiters of what is good and correct.
>
> [TDD inside the agent loop - theater or actual value?](https://martinfowler.com/articles/exploring-gen-ai/tdd-in-the-agent-loop.html)

> Regression effectiveness can be monitored and improved with mutation testing
>
> [TDD inside the agent loop - theater or actual value?](https://martinfowler.com/articles/exploring-gen-ai/tdd-in-the-agent-loop.html)

## Support

Established: 2 independent sources support this principle.

Expert: Birgitta Böckeler

Topics: deterministic-guardrails, metrics, techniques

## Related principles

- [Birgitta Böckeler: Agent-written tests are not proof of correctness](agent-written-tests-are-not-proof-of-correctness.md)
- [Birgitta Böckeler: Choose deliberately who triggers context](choose-deliberately-who-triggers-context.md)
