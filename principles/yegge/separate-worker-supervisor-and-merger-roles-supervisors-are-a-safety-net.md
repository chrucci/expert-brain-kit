# Separate worker, supervisor and merger roles; supervisors are a safety net

Verified: 8 verbatim quotes from 10 sources

Dimension: Roles for agents (agent-roles)

Evidence: experience

How to measure: Track time to detect and recover stalled agents, false kills of healthy sessions, work lost per incident, and completion latency as the number of parallel workers grows.

Give agents distinct jobs. Workers own their task through to completion, monitoring agents detect stalls, restart crashed sessions and recover abandoned work with bounded retries, and a merger integrates. Supervisors use generous thresholds, restart before destroying anything and overlap one another, but stay out of the routine completion path, because a single-threaded gatekeeper turns parallel work back into serial work.

## Quotes

> Polecats manage their own session lifecycle. External manipulation bypasses verification.
>
> [gastown: docs/concepts/polecat-lifecycle.md](https://github.com/gastownhall/gastown/blob/main/docs/concepts/polecat-lifecycle.md)

> Polecats manage their own lifecycle end-to-end. The Witness observes but does NOT gate completion. This prevents the Witness from becoming a bottleneck.
>
> [gastown: docs/design/architecture.md](https://github.com/gastownhall/gastown/blob/main/docs/design/architecture.md)

> Witness detects a zombie polecat with work still hooked/in_progress.
>
> [gastown: docs/design/mail-protocol.md](https://github.com/gastownhall/gastown/blob/main/docs/design/mail-protocol.md)

> Polecat in WORKING state for too long → escalate (don't nuke)
>
> [gastown: docs/design/persistent-polecat-pool.md](https://github.com/gastownhall/gastown/blob/main/docs/design/persistent-polecat-pool.md)

> These thresholds are intentionally generous. The goal is to catch truly stuck
>
> [gastown: docs/design/polecat-lifecycle-patrol.md](https://github.com/gastownhall/gastown/blob/main/docs/design/polecat-lifecycle-patrol.md)

> The witness role **returns to being an observer** — it patrols for anomalies
> and intervenes only when something is wrong:
>
> [gastown: docs/design/polecat-self-managed-completion.md](https://github.com/gastownhall/gastown/blob/main/docs/design/polecat-self-managed-completion.md)

> Persistent Beads and oversight agents (Witness, Deacon) guarantee eventual workflow completion even when individual operations may fail or produce varying results.
>
> [gastown: docs/glossary.md](https://github.com/gastownhall/gastown/blob/main/docs/glossary.md)

> Crew is persistent and human-managed. Polecats are transient and Witness-managed.
>
> [gastown: docs/overview.md](https://github.com/gastownhall/gastown/blob/main/docs/overview.md)

## Support

Established: 10 independent sources support this principle.

Expert: Steve Yegge

Topics: agent-count, agent-roles, processes

## Related principles

- [Steve Yegge: Agents stay in scope and escalate instead of bypassing](agents-stay-in-scope-and-escalate-instead-of-bypassing.md)
- [Steve Yegge: Cap the number of agents at what humans and the fleet can absorb](cap-the-number-of-agents-at-what-humans-and-the-fleet-can-absorb.md)
