# Agents verify their own work so humans stop being the bottleneck

Verified: 3 verbatim quotes from 1 source

Dimension: Roles for agents (agent-roles)

Evidence: experience

How to measure: Compare PRs merged to production per engineer, and how long agents sit idle waiting for human review, before and after agents get a self-verification capability.

An agent that can check its own output keeps iterating until the task is done. One that can't hands a diff to a human and waits. Tan treats self-verification as critical infrastructure because it takes the human out of the slowest part of the loop, and she credits it with letting her ship about 2,000 PRs a month with high confidence.

## Quotes

> A verification skill lets an agent check its own work and keep going until the task is done, and she treats it as “critical infrastructure” rather than one skill among many.
>
> [One engineer shipped 2,000 PRs a month to production. Verification is the key.](https://thenewstack.io/agentic-verification-distributed-systems/)

> Her argument for agentic verification is a throughput argument. An agent that can check its own output keeps working until the task is done.
>
> [One engineer shipped 2,000 PRs a month to production. Verification is the key.](https://thenewstack.io/agentic-verification-distributed-systems/)

> That is why she claims strong verification skills can multiply a team’s output by 100 to 1,000 times.
>
> [One engineer shipped 2,000 PRs a month to production. Verification is the key.](https://thenewstack.io/agentic-verification-distributed-systems/)

## Support

Candidate: one source supports this principle so far.

Expert: Lauren Tan

Topics: agent-roles, deterministic-guardrails, human-roles, processes

## Related principles

- [Lauren Tan: Give agents a drivable interface and feature map of the system](give-agents-a-drivable-interface-and-feature-map-of-the-system.md)
- [Lauren Tan: Pick tools and stack for how well agents can verify with them](pick-tools-and-stack-for-how-well-agents-can-verify-with-them.md)
