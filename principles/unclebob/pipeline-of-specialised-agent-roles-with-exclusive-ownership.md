# Pipeline of specialised agent roles with exclusive ownership

Verified: 4 verbatim quotes from 3 sources

Dimension: Roles for agents (agent-roles)

Evidence: opinion

How to measure: Compare defect escape rate and rework between single-agent runs and role-pipeline runs, and track how many cards pass through every stage.

In his swarm work, Martin splits agent work into a fixed chain of roles (specifier, coder, cleaner, architect, hardener, QA). Each role's prompt says what it may change, what it must verify and where it hands off, and every intermediate role always forwards to the next, so no stage is skipped and each stage is accountable for one concern.

## Quotes

> Role prompts divide ownership inside that law: what a role may change, what it must verify, what it must leave to another role, and where its next handoff goes.
>
> [swarm-forge: README.md](https://github.com/unclebob/swarm-forge/blob/main/README.md)

> `six-pack`: `specifier` -> `coder` -> `cleaner` -> `architect` -> `hardender` -> `QA`; each intermediate role always forwards to the next role in the
>
> [swarm-forge/swarmforge/handoff-protocol.md at main · unclebob/swarm-forge](https://github.com/unclebob/swarm-forge/blob/main/swarmforge/handoff-protocol.md)

> Configuration establishes topology and propagation; the constitution governs the entire project; role prompts assign exclusive artifacts, checks, and handoffs.
>
> [swarm-forge/README.md at six-pack · unclebob/swarm-forge](https://github.com/unclebob/swarm-forge/blob/six-pack/README.md)

> Turns QA procedures into executable UI-level checks, performs independent final verification, and makes only narrow fixes found through QA.
>
> [swarm-forge/README.md at six-pack · unclebob/swarm-forge](https://github.com/unclebob/swarm-forge/blob/six-pack/README.md)

## Support

Established: 3 independent sources support this principle.

Expert: Robert C. Martin

Topics: agent-count, agent-roles, processes

## Related principles

- [Robert C. Martin: Deterministic plumbing owns coordination, agents own adaptation](deterministic-plumbing-owns-coordination-agents-own-adaptation.md)
- [Robert C. Martin: Agents self-audit before every handoff](agents-self-audit-before-every-handoff.md)
- [Robert C. Martin: Drive one capable agent rather than fencing it in](drive-one-capable-agent-rather-than-fencing-it-in.md)
