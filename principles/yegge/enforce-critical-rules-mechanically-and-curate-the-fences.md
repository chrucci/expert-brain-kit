# Enforce critical rules mechanically, and curate the fences

Verified: 8 verbatim quotes from 7 sources

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: Track re-violations of each rule before and after mechanical enforcement, dangerous actions blocked versus executed, the number of fences over time, and the ratio of factory code to product code.

Prompt instructions are a soft guardrail that agents break under pressure. Rules that keep getting violated should tighten from custom to written law to fail-closed mechanical refusals at boundaries: tool-call gates, git hooks, permission sets for each role and removing tools from coordinators. Fences pile up, though, and so does agent-built factory tooling, so keep the fence set small, require a named human to approve new ones and prune the factory regularly.

## Quotes

> Now rules go through a lifecycle, tightening each time they're re-violated: first custom, then advisories/warnings, then written law in the constitution that all agents must obey, and finally, mechanical enforcement: programs that refuse by policy, or observe and alert loudly.
>
> [Fences, not Sandboxes](https://yegge.ai/essays/fences-not-sandboxes/)

> Every daily incident postmortem led to new rulings and new doctrine.
>
> [Fences, not Sandboxes](https://yegge.ai/essays/fences-not-sandboxes/)

> But I had made it far too easy for any incident to produce a new fence from the postmortem, and it was nobody's job to curate or review the fences.
>
> [Seats and Sunsets](https://yegge.ai/essays/seats-and-sunsets/)

> The refinery formula and role template explicitly forbid landing integration branches via raw git commands. Only `gt mq integration land` is authorized.
>
> [gastown: docs/concepts/integration-branches.md](https://github.com/gastownhall/gastown/blob/main/docs/concepts/integration-branches.md)

> Force PR creation via framework-level validation (agents can still misbehave)
>
> [gastown: docs/contrib-harnesses/polecat-pr-flow/README.md](https://github.com/gastownhall/gastown/blob/main/docs/contrib-harnesses/polecat-pr-flow/README.md)

> The runtime asks GT before executing tools. GT decides.
>
> [gastown: docs/design/factory-worker-api.md](https://github.com/gastownhall/gastown/blob/main/docs/design/factory-worker-api.md)

> Agents can and do violate this under pressure.
>
> [gastown: docs/design/witness-at-team-lead.md](https://github.com/gastownhall/gastown/blob/main/docs/design/witness-at-team-lead.md)

> - **bd init guard** (gastown/crew, beads/crew) - blocks `bd init*` inside `.beads/`
>
> [gastown: docs/HOOKS.md](https://github.com/gastownhall/gastown/blob/main/docs/HOOKS.md)

## Support

Established: 7 independent sources support this principle.

Expert: Steve Yegge

Topics: agent-roles, deterministic-guardrails, human-roles

## Related principles

- [Steve Yegge: Agents never land their own work: a gated merge queue decides](agents-never-land-their-own-work-a-gated-merge-queue-decides.md)
- [Steve Yegge: Version-controlled, layered agent instructions and workflow templates](version-controlled-layered-agent-instructions-and-workflow-templates.md)
