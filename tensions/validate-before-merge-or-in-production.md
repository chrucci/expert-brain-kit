# Validate before merge or in production?

Status: open. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should a team put its validation effort into pre-merge deterministic gates or into fast production observation with flags and progressive rollout?

Why open: Both sides rely on opinion and experience, and no study compares where validation investment pays off for agent changes.

## Sides
- **Charity Majors**: Pre-production checks quickly stop paying off; replace merge-and-hope with deploy, observe and learn using flags, rollouts and traces.
  - "Having nondeterministic code in production is finally forcing us to do the things we should have done all along. Instrumenting with traces. Tests and evals in production." ([source](https://charity.wtf/p/ai-demands-more-engineering-discipline), [Charity Majors: Validation in production is the new bottleneck](../principles/majors/validation-in-production-is-the-new-bottleneck.md))
- **Addy Osmani, Thoughtworks, Anthropic engineering**: Work is done only when deterministic checks in the loop prove it before merge, so failures are caught before a human or user sees them.
  - "Goal: every area the agent will touch gets a safety net first." ([source](https://github.com/addyosmani/agent-skills/blob/main/docs/adoption-guide.md), [Addy Osmani: Deterministic checks, not the agent, decide when work is done](../principles/osmani/deterministic-checks-not-the-agent-decide-when-work-is-done.md))
  - "Agents produce better code when they can gauge the quality of the code they produce themselves rather than relying on us to check it for them." ([source](https://martinfowler.com/articles/exploring-gen-ai/humans-and-agents.html), [Thoughtworks: Enforce agent work with deterministic sensors in the loop](../principles/thoughtworks/enforce-agent-work-with-deterministic-sensors-in-the-loop.md))
  - Also: [Anthropic engineering: Done means a check the agent can run](../principles/anthropic/done-means-a-check-the-agent-can-run.md)

## Evidence to settle it
For a set of services, shift spend toward either stronger pre-merge gates or production telemetry and progressive rollout, and track where defects are caught and how fast failures are found and fixed.

## Metric
Scoreboard: Failed deployment recovery time (`recovery-time`). Read failed deployment recovery time next to change fail rate; the production side should cut recovery time sharply even if fail rate rises slightly, the pre-merge side should cut fail rate.

## Related principles
- [principles/majors/validation-in-production-is-the-new-bottleneck.md](../principles/majors/validation-in-production-is-the-new-bottleneck.md) - Charity Majors: Validation in production is the new bottleneck
- [principles/osmani/deterministic-checks-not-the-agent-decide-when-work-is-done.md](../principles/osmani/deterministic-checks-not-the-agent-decide-when-work-is-done.md) - Addy Osmani: Deterministic checks, not the agent, decide when work is done
- [principles/thoughtworks/enforce-agent-work-with-deterministic-sensors-in-the-loop.md](../principles/thoughtworks/enforce-agent-work-with-deterministic-sensors-in-the-loop.md) - Thoughtworks: Enforce agent work with deterministic sensors in the loop
- [principles/anthropic/done-means-a-check-the-agent-can-run.md](../principles/anthropic/done-means-a-check-the-agent-can-run.md) - Anthropic engineering: Done means a check the agent can run
