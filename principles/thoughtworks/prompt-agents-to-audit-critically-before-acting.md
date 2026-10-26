# Prompt agents to audit critically before acting

Verified: 8 verbatim quotes from 6 sources

Dimension: Roles for agents (agent-roles)

Evidence: experience

How to measure: Measure the share of defects and wrong claims caught by audit or reviewer agents before human review, and the share of agent-extracted facts that experts must check.

Assistants default to optimism and give confident, wrong answers about unfamiliar systems. Reset the context and give the agent a critical, evidence-citing audit role, make it flag ambiguity rather than resolve it, and use adversarial reviewer agents to challenge generated code before humans see it.

## Quotes

> AI defaults to optimism. When I ask “How do I run this?”, it assumes I can run it. In a restoration mission, optimism is fatal.
>
> [The Archaeologist’s Copilot](https://martinfowler.com/articles/archaeologist-copilot.html)

> I shifted my mental model from “How do I run this?” to “Why did this fail?”. I reset the context with the AI, asking it to be critical rather than helpful.
>
> [The Archaeologist’s Copilot](https://martinfowler.com/articles/archaeologist-copilot.html)

> One was that if the code was ambiguous, the AI had to flag the ambiguity in its output so a human expert could resolve it.
>
> [AI-assisted migration: Critical lessons from the modernization frontlines](https://www.thoughtworks.com/insights/articles/ai-assisted-migration-lessons)

> Source traceability is the real anti-hallucination mechanism. Every extracted fact carries a file:line reference back to the legacy code.
>
> [AI-assisted migration: Critical lessons from the modernization frontlines](https://www.thoughtworks.com/insights/articles/ai-assisted-migration-lessons)

> If humans are writing the code, then AI can be used in even more of an assistant coach’s role. Checking for holes in the defense (security vulnerabilities) or stronger offense (more efficient queries) can be done faster on more lines of code and in a more consistent manner than relying on human reviews alone.
>
> [Modern engineering is a flow game](https://www.thoughtworks.com/insights/blog/agile-engineering-practices/modern-engineering-flow-game)

> If agents are writing the code, humans cannot be the sole verification mechanism.
>
> [Is developer experience dead?](https://www.thoughtworks.com/insights/blog/continuous-delivery/is-developer-experience-dead)

> Instead of designing everything in advance, we could automatically use agents on every codebase change to assess the impact it has on our Domain model, we could evaluate how it changes the user journeys or how it aligns with other domains, identifying early possible misunderstandings.
>
> [Semantic drift and semantic integrity: Stewarding meaning in the age of AI](https://www.thoughtworks.com/insights/blog/data-strategy/semantic-drift-stewarding-meaning-ai)

> An automated code review feature was also introduced, highlighting a growing need for "antagonistic agents" to stress test quality.
>
> [Last week in AI | 16 March](https://www.thoughtworks.com/insights/blog/generative-ai/last-week-ai-16-march)

## Support

Established: 6 independent sources support this principle.

Expert: Thoughtworks

Topics: agent-roles, techniques

## Related principles

- [Thoughtworks: Verification is the bottleneck; spend human review by risk](verification-is-the-bottleneck-spend-human-review-by-risk.md)
- [Thoughtworks: Enforce agent work with deterministic sensors in the loop](enforce-agent-work-with-deterministic-sensors-in-the-loop.md)
