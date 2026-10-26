# Widen agent autonomy narrowly and with evidence

Verified: 8 verbatim quotes from 16 sources

Dimension: Roles for agents (agent-roles)

Evidence: experience

How to measure: For each delegation tier, track the rate of agent actions needing human correction or acting outside scope, and use it to move task types between tiers.

Broadly permissioned agents cannot yet be made safe, so build pipelines of narrowly scoped, least-privilege agents with strong monitoring and hard stops where they hand back to a human. Decide autonomy per task type and domain risk, and widen it step by step as evaluation evidence and confidence grow.

## Quotes

> We can also have the agents add their recommendations to the product backlog, so we can prioritize and schedule them for the agents to pick up, apply, and test as part of the automated flow.
>
> [Humans and Agents in Software Engineering Loops](https://martinfowler.com/articles/exploring-gen-ai/humans-and-agents.html)

> The final step is to package the code, test results, and my reasoning log, then notify the compliance manager for final approval.
>
> [Beyond the hype: A real-world guide to building enterprise-grade AI agents](https://www.thoughtworks.com/insights/articles/a-real-world-guide-to-building-enterprise-grade-ai-agents)

> The organization stopped asking 'do we trust the agent?' and started asking 'what delegation tier does this remediation require?' Every outcome fed back into the strategy registry.
>
> [The operating system for enterprise AI](https://www.thoughtworks.com/insights/articles/operating-system-enterprise-ai)

> there's no proven safe way to run a high-permission agent like that today. These agents are useful largely because they have broad access to systems and information, and that's exactly what makes them risky.
>
> [Quality is speed: Where engineering discipline moves in the AI era](https://www.thoughtworks.com/insights/articles/quality-is-speed-AI-era)

> Treat the agent as a junior developer instead: give it a narrow, documented job inside an executable state machine, validate its output against a schema, advance the gate, repeat.
>
> [Enabling evolutionary database development: Part 3](https://www.thoughtworks.com/insights/blog/agile-engineering-practices/enabling-evolutionary-database-branching-lakebase-part-3)

> This is human-in-the-loop (HITL). Discovery deals with ambiguity, psychology and nuance. AI synthesizes feedback and generates prototypes, but the human Product Owner makes the final empathic and strategic leap.
>
> [Tackling the AI value delivery paradox](https://www.thoughtworks.com/insights/blog/agile-project-management/tackling-ai-value-delivery-paradox)

> Relying on prompt text to ask an agent not to perform unauthorized actions (such as pushing code or editing configs) is inherently fragile. Least-privilege tools convert behavioral guidance into structural enforcement.
>
> [Engineering the harness: A practical pattern for reliable coding agents](https://www.thoughtworks.com/insights/blog/architecture/engineering-the-harness-a-practical-pattern-for-reliable-coding-agents)

> the agent works autonomously (on things such as bug resolution or implementing minor features), but its actions are submitted to the developer for formal review and final authorization (e.g., via a pull request).
>
> [Beyond vibe coding: The five building blocks of AI-native engineering](https://www.thoughtworks.com/insights/blog/generative-ai/beyond-vibe-coding-the-five-building-blocks-of-aI-native-engineering)

## Support

Established: 16 independent sources support this principle.

Expert: Thoughtworks

Topics: agent-roles, deterministic-guardrails

## Related principles

- [Thoughtworks: Enforce agent work with deterministic sensors in the loop](enforce-agent-work-with-deterministic-sensors-in-the-loop.md)
- [Thoughtworks: Verification is the bottleneck; spend human review by risk](verification-is-the-bottleneck-spend-human-review-by-risk.md)
