# Validate before merge or in production?

Status: open. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should a team invest its validation effort in pre-merge gates or in observing changes in production?

Why open: Majors argues from opinion and the gate side from experience, and no one has measured where defects are cheapest to catch for agent changes.

## Sides
- **Charity Majors**: Pre-production checks quickly stop paying off at agent speed; replace merge-and-hope with flags, progressive rollout and telemetry-based validation in production.
  - "Having nondeterministic code in production is finally forcing us to do the things we should have done all along. Instrumenting with traces. Tests and evals in production." ([source](https://charity.wtf/p/ai-demands-more-engineering-discipline), [Charity Majors: Validation in production is the new bottleneck](../principles/majors/validation-in-production-is-the-new-bottleneck.md))
- **Addy Osmani, Thoughtworks, OpenAI engineering**: Deterministic checks in the agent loop and before merge decide when work is done, catching defects before humans or production see them.
  - "Goal: every area the agent will touch gets a safety net first." ([source](https://github.com/addyosmani/agent-skills/blob/main/docs/adoption-guide.md), [Addy Osmani: Deterministic checks, not the agent, decide when work is done](../principles/osmani/deterministic-checks-not-the-agent-decide-when-work-is-done.md))
  - "Agents produce better code when they can gauge the quality of the code they produce themselves rather than relying on us to check it for them." ([source](https://martinfowler.com/articles/exploring-gen-ai/humans-and-agents.html), [Thoughtworks: Enforce agent work with deterministic sensors in the loop](../principles/thoughtworks/enforce-agent-work-with-deterministic-sensors-in-the-loop.md))
  - Also: [OpenAI engineering: A checkable definition of done, proven by fast execution](../principles/openai/a-checkable-definition-of-done-proven-by-fast-execution.md)

## Evidence to settle it
For a service, track where each agent defect was first caught (in-loop check, review, staged rollout, production) and the cost to fix at each stage, before and after adding progressive rollout.

## Metric
Scoreboard: Change fail rate (`change-fail-rate`). Read change fail rate together with recovery time; if staged rollout keeps both low while pre-merge gates add little, the production side gains.

## Related principles
- [principles/majors/validation-in-production-is-the-new-bottleneck.md](../principles/majors/validation-in-production-is-the-new-bottleneck.md) - Charity Majors: Validation in production is the new bottleneck
- [principles/osmani/deterministic-checks-not-the-agent-decide-when-work-is-done.md](../principles/osmani/deterministic-checks-not-the-agent-decide-when-work-is-done.md) - Addy Osmani: Deterministic checks, not the agent, decide when work is done
- [principles/thoughtworks/enforce-agent-work-with-deterministic-sensors-in-the-loop.md](../principles/thoughtworks/enforce-agent-work-with-deterministic-sensors-in-the-loop.md) - Thoughtworks: Enforce agent work with deterministic sensors in the loop
- [principles/openai/a-checkable-definition-of-done-proven-by-fast-execution.md](../principles/openai/a-checkable-definition-of-done-proven-by-fast-execution.md) - OpenAI engineering: A checkable definition of done, proven by fast execution
