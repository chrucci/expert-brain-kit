# Megabatch onto main once commits outrun the build

Verified: 3 verbatim quotes from 1 source

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: Compare merge-queue depth, commit-to-landing time and how long main stays red under megabatch landing against batched bisection.

When agents commit faster than the build can verify one green build per commit, even a batch-and-bisect queue grows without limit. Yegge's newer practice is to land large batches onto main together, have a swarm of agents diagnose and fix whatever breaks, and roll forward.

## Quotes

> Once your commit rate outruns your build slots, one commit per green build becomes mathematically impossible.
>
> [The Shape of Things to Come, Part 1: The Continuous Thunderdome](https://yegge.ai/essays/the-shape-of-things-to-come/)

> Agents multiply the commit rate by orders of magnitude, while your build time stays fixed.
>
> [The Shape of Things to Come, Part 1: The Continuous Thunderdome](https://yegge.ai/essays/the-shape-of-things-to-come/)

> I've been doing this every day for roughly a week now, and it is clearly the future.
>
> [The Shape of Things to Come, Part 1: The Continuous Thunderdome](https://yegge.ai/essays/the-shape-of-things-to-come/)

## Support

Candidate: one source supports this principle so far.

Expert: Steve Yegge

Topics: agent-count, deterministic-guardrails, processes

## Related principles

- [Steve Yegge: Agents never land their own work: a gated merge queue decides](agents-never-land-their-own-work-a-gated-merge-queue-decides.md)
