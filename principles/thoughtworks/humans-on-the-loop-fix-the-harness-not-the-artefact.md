# Humans on the loop: fix the harness, not the artefact

Verified: 8 verbatim quotes from 13 sources

Dimension: Roles for humans (human-roles)

Evidence: experience

How to measure: Track how often the same class of agent failure recurs after a harness change versus a direct fix to the output, and whether each harness has a named owner who updates it on a set cadence.

Humans should build and improve the harness that produces agent output rather than gatekeeping every line, because line-by-line review makes them the bottleneck. When output goes wrong, the human decides what to codify, preferring to state a missing fact over adding approval gates that people soon approve on autopilot, and someone named owns that steering loop so the harness does not decay.

## Quotes

> The right place for us humans is to build and manage the working loop rather than either leaving the agents to it or micromanaging what they produce. Let’s call this “on the loop.”
>
> [Humans and Agents in Software Engineering Loops](https://martinfowler.com/articles/exploring-gen-ai/humans-and-agents.html)

> The orchestrator can grade its own session and surface clues, as it did here, but it cannot make that judgment call itself. The choice of what to codify, what to leave alone, and what might be an overreaction is still mine.
>
> [The Orchestrator's Tax](https://martinfowler.com/articles/orchestrator-tax.html)

> Systematically harvest learnings from AI interactions to improve the other four patterns. When a prompt works particularly well, capture it.
>
> [Patterns for Reducing Friction in AI-Assisted Development](https://martinfowler.com/articles/reduce-friction-ai/)

> The goal is to reach the full feature set and workflows the business requires, while continuously regenerating application components as business requirements and regulations change, with less human intervention.
>
> [Making sense of the SaaSpocalypse](https://www.thoughtworks.com/insights/articles/making-sense-saaspocalypse)

> Every harness needs an owner. If ownership is unclear, agents will effectively govern themselves.
>
> [The operating system for enterprise AI](https://www.thoughtworks.com/insights/articles/operating-system-enterprise-ai)

> Every interaction with AI can reveal useful information: where prompts work, where context is missing and where controls fail.
>
> [Path to AI-first organization](https://www.thoughtworks.com/insights/articles/path-to-ai-first-organization)

> In more predictable areas, the role of humans is evolving from "human-in-the-loop" to "human-on-the-loop" to meet these new challenges.
>
> [Preparing your team for the agentic software development life cycle](https://www.thoughtworks.com/insights/articles/preparing-your-team-for-agentic-software-development-life-cycle)

> At the retreat we talked about greater focus on the ‘middle loop’ of supervisory work. This is situated somewhere between writing code and release management, with its objectives being agent orchestration and governance.
>
> [Reflections on the future of Software Engineering retreat](https://www.thoughtworks.com/insights/articles/reflections-future-software-engineering-retreat)

## Support

Established: 13 independent sources support this principle.

Expert: Thoughtworks

Topics: human-roles, processes, techniques

## Related principles

- [Thoughtworks: Enforce agent work with deterministic sensors in the loop](enforce-agent-work-with-deterministic-sensors-in-the-loop.md)
- [Thoughtworks: Encode intent and standards in versioned artifacts](encode-intent-and-standards-in-versioned-artifacts.md)
- [Thoughtworks: Verification is the bottleneck; spend human review by risk](verification-is-the-bottleneck-spend-human-review-by-risk.md)
