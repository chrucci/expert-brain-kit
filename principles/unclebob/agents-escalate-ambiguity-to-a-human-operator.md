# Agents escalate ambiguity to a human operator

Verified: 1 verbatim quote from 1 source

Dimension: Roles for humans (human-roles)

Evidence: opinion

How to measure: Count clarification requests and human interventions per card, and compare them with defects traced to ambiguities agents resolved on their own.

The human acts as an operator: they start work, inspect agents, handle approval gates, answer clarifications and stop the swarm. When agents hit ambiguity or a conflict between tests and the spec, they send a structured clarification request instead of improvising, so the human stays the authority on unclear requirements.

## Quotes

> Agents exchange committed work through durable handoffs, while the operator uses a local dashboard to start work, inspect agents, handle approval gates, answer clarifications, and stop the swarm.
>
> [swarm-forge: README.md](https://github.com/unclebob/swarm-forge/blob/main/README.md)

## Support

Candidate: one source supports this principle so far.

Expert: Robert C. Martin

Topics: agent-roles, human-roles

## Related principles

- [Robert C. Martin: Humans are responsible just above the code level](humans-are-responsible-just-above-the-code-level.md)
- [Robert C. Martin: Pipeline of specialised agent roles with exclusive ownership](pipeline-of-specialised-agent-roles-with-exclusive-ownership.md)
