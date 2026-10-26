# Cap the number of agents at what humans and the fleet can absorb

Verified: 8 verbatim quotes from 8 sources

Dimension: Number of agents (agent-count)

Evidence: experience

How to measure: As agents are added, track throughput, queue depth, fleet idle time, coordination failures, per-seat fixed cost and in-flight items the human can actually follow; stop when throughput stops rising.

Grow gradually from one orchestrator to more agents, adding one at a time and stopping when producers swamp consumers or the human can no longer track progress. Prefer a holistic coordinator with few workers, and long-lived seats with written scope that are merged when budgets tighten. Consolidate overlapping specialists and give each role a messaging budget, because extra agents are nearly free to create but costly to coordinate.

## Quotes

> A seat has all of those answers already written down, so the same question becomes a lookup instead of a derivation.
>
> [Seats and Sunsets](https://yegge.ai/essays/seats-and-sunsets/)

> I arrived at 18 by slowly adding them, as needed, until I found equilibrium: I don't really need any more than this, or it overwhelms the fleet.
>
> [The Shape of Things to Come, Part 1: The Continuous Thunderdome](https://yegge.ai/essays/the-shape-of-things-to-come/)

> Agents overuse mail for routine communication, generating permanent beads and
>
> [gastown: docs/design/mail-protocol.md](https://github.com/gastownhall/gastown/blob/main/docs/design/mail-protocol.md)

> For large convoys (20+ issues), the Witness doesn't spawn 20 teammates at once.
>
> [gastown: docs/design/witness-at-team-lead.md](https://github.com/gastownhall/gastown/blob/main/docs/design/witness-at-team-lead.md)

> In agent-land, spinning up a new department is nearly free — unlike human orgs where headcount and budget provide natural friction against duplication.
>
> [gastown: docs/gas-city/crew-specialization-design.md](https://github.com/gastownhall/gastown/blob/main/docs/gas-city/crew-specialization-design.md)

> Run individual runtime instances manually. Gas Town only tracks state.
>
> [gastown: docs/INSTALLING.md](https://github.com/gastownhall/gastown/blob/main/docs/INSTALLING.md)

> The Mayor, acting as PR Sheriff, takes a more holistic view, makes better decisions, and makes better use of Gas Town resources to get the PRs reviewed, fix-merged, and escalated in parallel.
>
> [Vibe Maintainer](https://steve-yegge.medium.com/vibe-maintainer-a2273a841040?source=rss-c1ec701babb7------2)

> At first, it’s just you and the Mayor. Best buds. Later, you’ll be juggling conversations with 20-odd crew members while your Mayor is out slinging polecats at half a dozen epics at once.
>
> [Welcome to the Wasteland: A Thousand Gas Towns](https://steve-yegge.medium.com/welcome-to-the-wasteland-a-thousand-gas-towns-a5eb9bc8dc1f?source=rss-c1ec701babb7------2)

## Support

Established: 8 independent sources support this principle.

Expert: Steve Yegge

Topics: agent-count, agent-roles, human-roles

## Related principles

- [Steve Yegge: Humans lead and govern agent crews](humans-lead-and-govern-agent-crews.md)
- [Steve Yegge: Deterministic machinery dispatches work; models act on judgment](deterministic-machinery-dispatches-work-models-act-on-judgment.md)
