# How many agents should one engineer run?

Status: open. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should an engineer run one or two agents at a time, or scale to many parallel agents with coordination machinery?

Why open: Every position comes from personal experience at very different scales, and no controlled comparison exists.

## Sides
- **Mitchell Hashimoto, Kent Beck, Robert C. Martin**: Run one agent, two at most. Extra agents add cleanup and coordination work for the human.
  - "I find having the one agent running is a good balance for me right now" ([source](https://mitchellh.com/writing/my-ai-adoption-journey), [Mitchell Hashimoto: Run one or two agents, not a swarm](../principles/hashimoto/run-one-or-two-agents-not-a-swarm.md))
  - "I have never been able to get two agents working on the same code base at the same time without my head exploding. So definitely anti that." ([source](https://newsletter.kentbeck.com/p/genie-lessons-nobody-wants-agents?t=1538s), [Kent Beck: Watch for the coordination tax of agent swarms](../principles/beck/watch-for-the-coordination-tax-of-agent-swarms.md))
  - Also: [Robert C. Martin: Drive one capable agent rather than fencing it in](../principles/unclebob/drive-one-capable-agent-rather-than-fencing-it-in.md)
- **Steve Yegge, Gergely Orosz, Addy Osmani**: Run many agents in parallel, adding one at a time until throughput stops rising, with deterministic dispatch and owned areas to keep them apart.
  - "A seat has all of those answers already written down, so the same question becomes a lookup instead of a derivation." ([source](https://yegge.ai/essays/seats-and-sunsets/), [Steve Yegge: Cap the number of agents at what humans and the fleet can absorb](../principles/yegge/cap-the-number-of-agents-at-what-humans-and-the-fleet-can-absorb.md))
  - "AI handles much of the implementation, but engineers are setting the direction, and make continuous course corrections." ([source](https://newsletter.pragmaticengineer.com/p/ai-first-makeover-craft), [Gergely Orosz: Engineers own areas, architecture and the release decision](../principles/orosz/engineers-own-areas-architecture-and-the-release-decision.md))
  - Also: [Addy Osmani: Run parallel agents only on independent work, and only as many as you can review](../principles/osmani/run-parallel-agents-only-on-independent-work-and-only-as-many-as-you-can-review.md)
- **Charity Majors**: There is no team-wide answer. Each engineer finds their own count from their own data.
  - "Everyone should put in the time and experimentation to find out where their "sweet spot" is." ([source](https://www.honeycomb.io/blog/ai-norms-values-part-2-ai-honeycomb-engineering), [Charity Majors: Each engineer finds their own agent count from data](../principles/majors/each-engineer-finds-their-own-agent-count-from-data.md))

## Evidence to settle it
Have engineers rotate through two-week periods at one, two, four and eight concurrent agents on comparable backlog work, recording merged changes after full review, human cleanup hours, rework and defects per period.

## Metric
Scoreboard: Rework rate (`rework-rate`). Plot rework rate against concurrent agents per engineer; the count where rework starts to climb while merged output flattens marks the practical limit.

## Related principles
- [principles/hashimoto/run-one-or-two-agents-not-a-swarm.md](../principles/hashimoto/run-one-or-two-agents-not-a-swarm.md) - Mitchell Hashimoto: Run one or two agents, not a swarm
- [principles/beck/watch-for-the-coordination-tax-of-agent-swarms.md](../principles/beck/watch-for-the-coordination-tax-of-agent-swarms.md) - Kent Beck: Watch for the coordination tax of agent swarms
- [principles/unclebob/drive-one-capable-agent-rather-than-fencing-it-in.md](../principles/unclebob/drive-one-capable-agent-rather-than-fencing-it-in.md) - Robert C. Martin: Drive one capable agent rather than fencing it in
- [principles/yegge/cap-the-number-of-agents-at-what-humans-and-the-fleet-can-absorb.md](../principles/yegge/cap-the-number-of-agents-at-what-humans-and-the-fleet-can-absorb.md) - Steve Yegge: Cap the number of agents at what humans and the fleet can absorb
- [principles/orosz/engineers-own-areas-architecture-and-the-release-decision.md](../principles/orosz/engineers-own-areas-architecture-and-the-release-decision.md) - Gergely Orosz: Engineers own areas, architecture and the release decision
- [principles/osmani/run-parallel-agents-only-on-independent-work-and-only-as-many-as-you-can-review.md](../principles/osmani/run-parallel-agents-only-on-independent-work-and-only-as-many-as-you-can-review.md) - Addy Osmani: Run parallel agents only on independent work, and only as many as you can review
- [principles/majors/each-engineer-finds-their-own-agent-count-from-data.md](../principles/majors/each-engineer-finds-their-own-agent-count-from-data.md) - Charity Majors: Each engineer finds their own agent count from data
