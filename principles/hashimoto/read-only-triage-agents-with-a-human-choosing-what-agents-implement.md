# Read-only triage agents, with a human choosing what agents implement

Verified: 1 verbatim quote from 1 source

Dimension: Roles for agents (agent-roles)

Evidence: experience

How to measure: Compare the success rate of agent-implemented issues a human picked from triage reports with issues assigned without that filter.

Triage agents review issues and PRs and write reports, but they are not allowed to respond. A human then picks the issues an agent will almost certainly solve well and hands them to a background agent one at a time. Agents do the broad scanning, and humans keep control over what agents implement.

## Quotes

> filter them manually to find the issues that an agent will almost certainly solve well, and then keep them going in the background (one at a time, not in parallel).
>
> [My AI Adoption Journey](https://mitchellh.com/writing/my-ai-adoption-journey)

## Support

Candidate: one source supports this principle so far.

Expert: Mitchell Hashimoto

Topics: agent-roles, human-roles, processes

## Related principles

- [Mitchell Hashimoto: Run one or two agents, not a swarm](run-one-or-two-agents-not-a-swarm.md)
