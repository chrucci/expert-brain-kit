# Deterministic plumbing owns coordination, agents own adaptation

Verified: 6 verbatim quotes from 3 sources

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: opinion

How to measure: Count malformed, lost or duplicated handoffs and merge conflicts as the number of parallel agents grows, before and after moving coordination into validated scripts.

Each agent runs isolated in its own worktree and session and passes only committed work. Deterministic scripts validate handoff drafts and own transport, queue state and the audit log, and fixed tools own the checking, while agents write only project-specific glue. This keeps parallel agents from corrupting shared state and leaves an audit trail that can be trusted.

## Quotes

> Some pipeline tools are pre-supplied Go commands from this repository. Other
> components are project-dependent and are written by the agents responsible for
> installing and maintaining acceptance testing in the target project.
>
> [Acceptance-Pipeline-Specification: README.md](https://github.com/unclebob/Acceptance-Pipeline-Specification/blob/main/README.md)

> SwarmForge coordinates AI agents in isolated git worktrees and tmux sessions.
>
> [swarm-forge: README.md](https://github.com/unclebob/swarm-forge/blob/main/README.md)

> Agents send committed work with `swarm_handoff.sh`, accept it with `ready_for_next.sh`, and finish the current item with `done_with_current.sh`.
>
> [swarm-forge: README.md](https://github.com/unclebob/swarm-forge/blob/main/README.md)

> Agents should not send tmux commands, manage socket permissions, or maintain a separate logbook.
>
> [swarm-forge/swarmforge/handoff-protocol.md at main · unclebob/swarm-forge](https://github.com/unclebob/swarm-forge/blob/main/swarmforge/handoff-protocol.md)

> Agents should not manually move inbox files. Helper scripts should own queue state transitions.
>
> [swarm-forge/swarmforge/handoff-protocol.md at main · unclebob/swarm-forge](https://github.com/unclebob/swarm-forge/blob/main/swarmforge/handoff-protocol.md)

> Validation errors should be explicit enough for an agent to repair the draft.
>
> [swarm-forge/swarmforge/handoff-protocol.md at main · unclebob/swarm-forge](https://github.com/unclebob/swarm-forge/blob/main/swarmforge/handoff-protocol.md)

## Support

Established: 3 independent sources support this principle.

Expert: Robert C. Martin

Topics: agent-count, agent-roles, deterministic-guardrails

## Related principles

- [Robert C. Martin: Pipeline of specialised agent roles with exclusive ownership](pipeline-of-specialised-agent-roles-with-exclusive-ownership.md)
- [Robert C. Martin: Agents self-audit before every handoff](agents-self-audit-before-every-handoff.md)
