# Perceived agent speedup versus measured slowdown

Status: leaning. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should a team reorganise around the large speedups practitioners report, or treat them as unproven until measured on its own work?

Why leaning: METR's randomized measurement shows perception is unreliable, while the throughput claims are uncontrolled experience reports, though the METR study used older tools.

## Sides
- **METR** (measured): Self-reports and forecasts of AI speedup are unreliable and experienced developers on mature repos measured 19 percent slower, so measure with controlled trials before acting.
  - "This gap between perception and reality is striking: developers expected AI to speed them up by 24%, and even after experiencing the slowdown, they still believed AI had sped them up by 20%." ([source](https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/), [METR: Measure AI speedup instead of trusting perception](../principles/metr/measure-ai-speedup-instead-of-trusting-perception.md))
  - "When developers are allowed to use AI tools, they take 19% longer to complete issues—a significant slowdown that goes against developer beliefs and expert forecasts." ([source](https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/), [METR: Tacit knowledge and implicit standards limit AI in mature codebases](../principles/metr/tacit-knowledge-and-implicit-standards-limit-ai-in-mature-codebases.md))
- **Lauren Tan, Steve Yegge, Thoughtworks**: Agent-driven teams already deliver work estimated for far larger teams and hundreds of PRs or features per engineer, so the gain is real and teams should restructure for it now.
  - "A verification skill lets an agent check its own work and keep going until the task is done, and she treats it as “critical infrastructure” rather than one skill among many." ([source](https://thenewstack.io/agentic-verification-distributed-systems/), [Lauren Tan: Agents verify their own work so humans stop being the bottleneck](../principles/tan/agents-verify-their-own-work-so-humans-stop-being-the-bottleneck.md))
  - "300 real features a day on a code base is already well beyond what any humans can vet, so I've had to pace it deliberately." ([source](https://yegge.ai/essays/seats-and-sunsets/), [Steve Yegge: Humans lead and govern agent crews](../principles/yegge/humans-lead-and-govern-agent-crews.md))
  - Also: [Thoughtworks: Agents shrink and reshape teams, but not down to one person](../principles/thoughtworks/agents-shrink-and-reshape-teams-but-not-down-to-one-person.md)

## Evidence to settle it
Randomly assign pre-scoped backlog tasks to agent-allowed and agent-disallowed conditions for a month, collecting developer forecasts beforehand, and compare measured completion time with the forecasts.

## Metric
Scoreboard: Change lead time (`lead-time`). Compare change lead time for randomized agent-allowed and agent-disallowed tasks scoped before assignment, next to the team's own estimate of speedup.

## Related principles
- [principles/metr/measure-ai-speedup-instead-of-trusting-perception.md](../principles/metr/measure-ai-speedup-instead-of-trusting-perception.md) - METR: Measure AI speedup instead of trusting perception
- [principles/metr/tacit-knowledge-and-implicit-standards-limit-ai-in-mature-codebases.md](../principles/metr/tacit-knowledge-and-implicit-standards-limit-ai-in-mature-codebases.md) - METR: Tacit knowledge and implicit standards limit AI in mature codebases
- [principles/tan/agents-verify-their-own-work-so-humans-stop-being-the-bottleneck.md](../principles/tan/agents-verify-their-own-work-so-humans-stop-being-the-bottleneck.md) - Lauren Tan: Agents verify their own work so humans stop being the bottleneck
- [principles/yegge/humans-lead-and-govern-agent-crews.md](../principles/yegge/humans-lead-and-govern-agent-crews.md) - Steve Yegge: Humans lead and govern agent crews
- [principles/thoughtworks/agents-shrink-and-reshape-teams-but-not-down-to-one-person.md](../principles/thoughtworks/agents-shrink-and-reshape-teams-but-not-down-to-one-person.md) - Thoughtworks: Agents shrink and reshape teams, but not down to one person
