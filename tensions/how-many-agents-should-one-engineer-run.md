# How many agents should one engineer run?

Status: open. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should an engineer run one or two agents at a time, a handful in parallel, or a large crew?

Why open: Anthropic's measurement shows parallelism only helps on independent seams but does not fix a number, and the count claims are all individual experience.

## Sides
- **Mitchell Hashimoto, Kent Beck, Robert C. Martin**: Run one agent, two at most, because each extra agent adds cleanup and coordination that lands on the human.
  - "I find having the one agent running is a good balance for me right now" ([source](https://mitchellh.com/writing/my-ai-adoption-journey), [Mitchell Hashimoto: Run one or two agents, not a swarm](../principles/hashimoto/run-one-or-two-agents-not-a-swarm.md))
  - "I have never been able to get two agents working on the same code base at the same time without my head exploding. So definitely anti that." ([source](https://newsletter.kentbeck.com/p/genie-lessons-nobody-wants-agents?t=1538s), [Kent Beck: Watch for the coordination tax of agent swarms](../principles/beck/watch-for-the-coordination-tax-of-agent-swarms.md))
  - Also: [Robert C. Martin: Drive one capable agent rather than fencing it in](../principles/unclebob/drive-one-capable-agent-rather-than-fencing-it-in.md)
- **Addy Osmani, Simon Willison**: About three to five parallel agents per person is workable when the work splits into independent slices, and falling review quality marks the limit.
  - "Pick this only when **independent** investigations can run in parallel and produce reports that a single agent then merges." ([source](https://github.com/addyosmani/agent-skills/blob/main/docs/agents.md), [Addy Osmani: Run parallel agents only on independent work, and only as many as you can review](../principles/osmani/run-parallel-agents-only-on-independent-work-and-only-as-many-as-you-can-review.md))
  - "I can fire up four agents in parallel and have them work on four different problems. And by like 11 AM, I am wiped out for the day." ([source](https://simonwillison.net/2026/Apr/2/lennys-podcast/), [Simon Willison: Human cognitive capacity limits agents per person and team size](../principles/willison/human-cognitive-capacity-limits-agents-per-person-and-team-size.md))
- **Gergely Orosz, Steve Yegge**: Engineers should manage crews of five or more agents and grow the fleet until throughput stops rising.
  - "AI handles much of the implementation, but engineers are setting the direction, and make continuous course corrections." ([source](https://newsletter.pragmaticengineer.com/p/ai-first-makeover-craft), [Gergely Orosz: Engineers own areas, architecture and the release decision](../principles/orosz/engineers-own-areas-architecture-and-the-release-decision.md))
  - "A seat has all of those answers already written down, so the same question becomes a lookup instead of a derivation." ([source](https://yegge.ai/essays/seats-and-sunsets/), [Steve Yegge: Cap the number of agents at what humans and the fleet can absorb](../principles/yegge/cap-the-number-of-agents-at-what-humans-and-the-fleet-can-absorb.md))

## Evidence to settle it
Have each engineer spend two-week periods at one, three and six concurrent agents on comparable work, recording merged-after-full-review output, rework, merge conflicts and self-reported fatigue.

## Metric
Scoreboard: Rework rate (`rework-rate`). Plot rework rate against concurrent agents per engineer; the count where rework rises faster than merged output is that engineer's ceiling.

## Related principles
- [principles/hashimoto/run-one-or-two-agents-not-a-swarm.md](../principles/hashimoto/run-one-or-two-agents-not-a-swarm.md) - Mitchell Hashimoto: Run one or two agents, not a swarm
- [principles/beck/watch-for-the-coordination-tax-of-agent-swarms.md](../principles/beck/watch-for-the-coordination-tax-of-agent-swarms.md) - Kent Beck: Watch for the coordination tax of agent swarms
- [principles/unclebob/drive-one-capable-agent-rather-than-fencing-it-in.md](../principles/unclebob/drive-one-capable-agent-rather-than-fencing-it-in.md) - Robert C. Martin: Drive one capable agent rather than fencing it in
- [principles/osmani/run-parallel-agents-only-on-independent-work-and-only-as-many-as-you-can-review.md](../principles/osmani/run-parallel-agents-only-on-independent-work-and-only-as-many-as-you-can-review.md) - Addy Osmani: Run parallel agents only on independent work, and only as many as you can review
- [principles/willison/human-cognitive-capacity-limits-agents-per-person-and-team-size.md](../principles/willison/human-cognitive-capacity-limits-agents-per-person-and-team-size.md) - Simon Willison: Human cognitive capacity limits agents per person and team size
- [principles/orosz/engineers-own-areas-architecture-and-the-release-decision.md](../principles/orosz/engineers-own-areas-architecture-and-the-release-decision.md) - Gergely Orosz: Engineers own areas, architecture and the release decision
- [principles/yegge/cap-the-number-of-agents-at-what-humans-and-the-fleet-can-absorb.md](../principles/yegge/cap-the-number-of-agents-at-what-humans-and-the-fleet-can-absorb.md) - Steve Yegge: Cap the number of agents at what humans and the fleet can absorb
