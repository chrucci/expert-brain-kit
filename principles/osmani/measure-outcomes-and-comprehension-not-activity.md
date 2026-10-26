# Measure outcomes and comprehension, not activity

Verified: 8 verbatim quotes from 9 sources

Dimension: Metrics (metrics)

Evidence: experience

How to measure: Put outcome, cost and comprehension metrics on the same dashboard as throughput, and check whether they move with agent output volume.

Commits, lines generated, PR counts and even DORA metrics can look healthy while fewer people understand the codebase and agent output is rubber-stamped. Choose metrics before raising autonomy. Track lead time, review minutes, interventions, escaped defects, rollbacks, cost per merged PR and per-stage timing, and pair them with a measure of comprehension and learning.

## Quotes

> Deciding on metric after-the-fact is probably not enough. Metrics can be put in place in advance, in a concise doc.
>
> [Agentic Autonomy Levels | AddyOsmani.com](https://addyosmani.com/blog/agentic-autonomy-levels/)

> If you’re running agents at scale in CI/CD or automated review pipelines, the 15-20% cost overhead from context files compounds across thousands of runs. Calculate it before assuming the tradeoff is worth it.
>
> [Stop Using /init for AGENTS.md | AddyOsmani.com](https://addyosmani.com/blog/agents-md/)

> Lines generated don’t tell you whether the codebase improved. I would track lead time, review minutes, human interventions, escaped defects, rollbacks, oracle mismatches, and suppressions left behind.
>
> [Brownfield Agentic Engineering](https://addyosmani.com/blog/brownfield-agentic-engineering/)

> There’s a seductive quality to watching agents work in parallel. The activity metrics are impressive - commits per hour, parallel task completion, lines of code touched.
>
> [Claude Code Swarms | AddyOsmani.com](https://addyosmani.com/blog/claude-code-agent-teams/)

> None of these distinguish between “I built this and understand it” and “the agent built this and I approved it.”
>
> [Cognitive Surrender | AddyOsmani.com](https://addyosmani.com/blog/cognitive-surrender/)

> The reason comprehension debt is so dangerous is that nothing in your current measurement system captures it.
>
> [Comprehension Debt - the hidden cost of AI generated code. | AddyOsmani.com](https://addyosmani.com/blog/comprehension-debt/)

> Ship and learn are two separate metrics. Your manager and your customers will only ever ask about the first one.
>
> [Don't Outsource the Learning | AddyOsmani.com](https://addyosmani.com/blog/dont-outsource-learning/)

> From a measurement perspective, you might look at metrics like cost per merged PR and code shelf life as comprehension debt metrics.
>
> [Human judgment doesn't leave the software factory. It relocates.](https://addyosmani.com/blog/human-judgment-doesnt-leave-the-software/)

## Support

Established: 9 independent sources support this principle.

Expert: Addy Osmani

Topics: metrics, skills

## Related principles

- [Addy Osmani: Review capacity is the bottleneck, so size work to it](review-capacity-is-the-bottleneck-so-size-work-to-it.md)
- [Addy Osmani: Build and protect engineering judgment on purpose](build-and-protect-engineering-judgment-on-purpose.md)
