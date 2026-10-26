# Verification is the bottleneck; spend human review by risk

Verified: 8 verbatim quotes from 16 sources

Dimension: Processes (processes)

Evidence: experience

How to measure: Track how much lead time is spent waiting on human verification or approval, split by risk tier, and how approval time relates to changeset size and escaped defects.

Agents generate change faster than people can verify it, so review capacity, reviewer fatigue and approval latency set the pace of delivery. Tier code and decisions by risk, run mechanical checks first, keep human gates for high-blast-radius choices, and deliberately rehome what code review used to do instead of letting rigor evaporate into rubber-stamping.

## Quotes

> If extraction runs in parallel but SME capacity doesn't, review becomes the pacing function and timelines stretch.
>
> [AI-assisted migration: Critical lessons from the modernization frontlines](https://www.thoughtworks.com/insights/articles/ai-assisted-migration-lessons)

> A key insight, and one I’ve been thinking about for a while, is the possibility of tiering software in terms of importance and criticality. In other words, we may be able to circumvent code reviews where code quality is deemed of less importance, and instead focus our attention on areas where it really matters.
>
> [Reflections on the future of Software Engineering retreat](https://www.thoughtworks.com/insights/articles/reflections-future-software-engineering-retreat)

> In the middle loop, the human engineer evaluates whether the agent actually solved the right problem, ensures the code doesn't introduce architectural drift and orchestrates how multiple agent-created components fit together.
>
> [Supervisory engineering: Orchestrating software’s ‘middle loop’](https://www.thoughtworks.com/insights/blog/agile-engineering-practices/supervisory-engineering-orchestrating-software-middle-loop)

> If engineering can build in hours but decision-making takes months, the approval becomes the new bottleneck.
>
> [AI makes Agile more alive](https://www.thoughtworks.com/insights/blog/agile-engineering-practices/ai-makes-agile-more-alive)

> The practitioners navigating this well aren't trying to preserve code review in its current form. They're decomposing it into these functions and finding new homes for each one.
>
> [Where does the rigor go?](https://www.thoughtworks.com/insights/blog/agile-engineering-practices/where-does-the-rigor-go)

> Agents can produce that change faster than a reviewer can read it. Tests and types can pass while the diff is still too large to judge with care.
>
> [Designing agentic delivery for bounded context and bounded human attention](https://www.thoughtworks.com/insights/blog/architecture/designing-agentic-delivery-for-bounded-context-and-bounded-human-attention)

> human confirmation gates are reserved for irreversible or high-blast-radius choices, such as multi-repository scope changes, schema migrations or public API modifications. Lower-risk decisions proceed with sensible defaults.
>
> [Engineering the harness: A practical pattern for reliable coding agents](https://www.thoughtworks.com/insights/blog/architecture/engineering-the-harness-a-practical-pattern-for-reliable-coding-agents)

> The primary friction point in 2026 isn't producing code, it’s verifying it.
>
> [Is developer experience dead?](https://www.thoughtworks.com/insights/blog/continuous-delivery/is-developer-experience-dead)

## Support

Established: 16 independent sources support this principle.

Expert: Thoughtworks

Topics: deterministic-guardrails, human-roles, processes

## Related principles

- [Thoughtworks: Enforce agent work with deterministic sensors in the loop](enforce-agent-work-with-deterministic-sensors-in-the-loop.md)
- [Thoughtworks: Design and confirm intent in small staged steps](design-and-confirm-intent-in-small-staged-steps.md)
- [Thoughtworks: Humans on the loop: fix the harness, not the artefact](humans-on-the-loop-fix-the-harness-not-the-artefact.md)
