# Humans own and evaluate what agents build

Verified: 4 verbatim quotes from 1 source

Dimension: Roles for humans (human-roles)

Evidence: opinion

How to measure: Track the share of agent-generated changes that get a human review before merge, and compare defect and rework rates for reviewed and unreviewed changes.

Agents can edit the source tree, run tests and work for long stretches on their own, but humans stay responsible for what the software does and how it works. The team has to plan for humans to judge the finished work through code review, test results and other sensors, not hand that ownership to the agent.

## Quotes

> This is a profound change to the nature of programming, where humans oversee LLM agents who generate the code. Humans are still responsible for what the software does and how it works, but use different skills to create their products.
>
> [Agentic Programming](https://martinfowler.com/bliki/AgenticProgramming.html)

> With vibe coding humans don't look at the code,
>   indeed they forget that it even exists, while with agentic programming they are
>   concerned with the code, often giving it detailed review.
>
> [Agentic Programming](https://martinfowler.com/bliki/AgenticProgramming.html)

> The LLM then manipulates the source tree directly, creating and modifying files, running the code, evaluating the results of tests, and continuing development work, often for extended periods.
>
> [Agentic Programming](https://martinfowler.com/bliki/AgenticProgramming.html)

> Once done humans evaluate the agents work, doing code review, examining test results, and reviewing outputs from other sensors.
>
> [Agentic Programming](https://martinfowler.com/bliki/AgenticProgramming.html)

## Support

Candidate: one source supports this principle so far.

Expert: Martin Fowler

Topics: agent-roles, deterministic-guardrails, human-roles, processes

## Related principles

- [Martin Fowler: Harness engineering is a core programmer skill](harness-engineering-is-a-core-programmer-skill.md)
- [Martin Fowler: Domain knowledge and customer collaboration matter more](domain-knowledge-and-customer-collaboration-matter-more.md)
