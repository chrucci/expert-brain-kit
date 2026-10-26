# Deterministic machinery dispatches work; models act on judgment

Verified: 8 verbatim quotes from 12 sources

Dimension: Number of agents (agent-count)

Evidence: experience

How to measure: Track how long ready work sits idle, how often agents pick blocked work or collide on the same task, and the share of agent wake-ups that lead to a useful action.

The work itself should decide what runs next. Explicit dependencies (ideally taken from the spec) are validated before a swarm starts, and agents atomically claim only unblocked work, then run it at once without waiting for confirmation. Crons, queues and the graph handle the routine path, and an agent is woken only when something needs judgment. Parallel agents then need no human dispatcher and don't collide.

## Quotes

> wake an agent when something needs judgment. The rule is: crons watch, models act.
>
> [The Shape of Things to Come, Part 1: The Continuous Thunderdome](https://yegge.ai/essays/the-shape-of-things-to-come/)

> Validate an epic's structure to ensure it's ready for swarm execution.
>
> [beads: docs/cli-reference/swarm.md](https://github.com/gastownhall/beads/blob/main/docs/cli-reference/swarm.md)

> the graph — not a human dispatcher — decides what is
> workable next.
>
> [beads: docs/core-concepts/index.md](https://github.com/gastownhall/beads/blob/main/docs/core-concepts/index.md)

> But if that item depends on something else that isn't done yet, you've wasted time. Multiply this across a team of AI agents and humans, and you get thrashing.
>
> [beads: docs/getting-started/quickstart.md](https://github.com/gastownhall/beads/blob/main/docs/getting-started/quickstart.md)

> Assign or claim work so every issue has one owner
>
> [beads: docs/multi-agent/coordination.md](https://github.com/gastownhall/beads/blob/main/docs/multi-agent/coordination.md)

> In orchestrated workflows an orchestrator usually assigns work (`bd assign`); agents picking work directly should use the atomic `--claim`.
>
> [beads: docs/reference/faq.md](https://github.com/gastownhall/beads/blob/main/docs/reference/faq.md)

> Hash-based IDs (`bd-a1b2`) prevent merge collisions in multi-agent/multi-branch workflows.
>
> [beads: README.md](https://github.com/gastownhall/beads/blob/main/README.md)

> There is no supervisor polling asking "did you start yet?"
>
> [gastown: docs/concepts/propulsion-principle.md](https://github.com/gastownhall/gastown/blob/main/docs/concepts/propulsion-principle.md)

## Support

Established: 12 independent sources support this principle.

Expert: Steve Yegge

Topics: agent-count, deterministic-guardrails, processes, techniques

## Related principles

- [Steve Yegge: Keep agent work state in a durable work graph, not the session](keep-agent-work-state-in-a-durable-work-graph-not-the-session.md)
- [Steve Yegge: Cap the number of agents at what humans and the fleet can absorb](cap-the-number-of-agents-at-what-humans-and-the-fleet-can-absorb.md)
