# Agents self-audit before every handoff

Verified: 2 verbatim quotes from 1 source

Dimension: Processes (processes)

Evidence: opinion

How to measure: Track the audit count and findings per card, and compare downstream rework with and without the audit gate.

An agent's first handoff attempt is held back, and the agent must trace every requirement to its work and verification evidence before resubmitting. Passing checks alone do not prove completeness, and counting audits per card shows how much rework agents needed.

## Quotes

> - Direct the sender to re-read the complete inbound payload and referenced sources, trace every requirement and constraint to role-appropriate work and verification evidence, examine boundaries and failure cases, and fix and re-audit every finding. Passing checks alone do not establish completeness.
>
> [swarm-forge/swarmforge/handoff-protocol.md at main · unclebob/swarm-forge](https://github.com/unclebob/swarm-forge/blob/main/swarmforge/handoff-protocol.md)

> Complete the sender's current inbox item only after the audited handoff has been queued. Approval, when required, occurs after this audit gate.
>
> [swarm-forge/swarmforge/handoff-protocol.md at main · unclebob/swarm-forge](https://github.com/unclebob/swarm-forge/blob/main/swarmforge/handoff-protocol.md)

## Support

Candidate: one source supports this principle so far.

Expert: Robert C. Martin

Topics: agent-roles, processes

## Related principles

- [Robert C. Martin: Pipeline of specialised agent roles with exclusive ownership](pipeline-of-specialised-agent-roles-with-exclusive-ownership.md)
- [Robert C. Martin: Deterministic plumbing owns coordination, agents own adaptation](deterministic-plumbing-owns-coordination-agents-own-adaptation.md)
