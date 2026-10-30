# Can agents verify their own work?

Status: open. Verified: every side has a verbatim quote from a verified principle.

**Question:** Is agent self-verification enough to call work done, or must humans own the specification it is checked against?

Why open: Both sides rest on experience, and no study compares escaped defects under the two ownership models.

## Sides
- **Lauren Tan, Anthropic engineering**: Agents that run and check their own work let humans step out of the slowest part of the loop, and that capability is critical infrastructure.
  - "A verification skill lets an agent check its own work and keep going until the task is done, and she treats it as “critical infrastructure” rather than one skill among many." ([source](https://thenewstack.io/agentic-verification-distributed-systems/), [Lauren Tan: Agents verify their own work so humans stop being the bottleneck](../principles/tan/agents-verify-their-own-work-so-humans-stop-being-the-bottleneck.md))
  - "Software is comparatively easy to test and review—you can run code and see if it works—which makes it easier to trust an agent and catch its mistakes." ([source](https://www.anthropic.com/research/measuring-agent-autonomy), [Anthropic engineering: Done means a check the agent can run](../principles/anthropic/done-means-a-check-the-agent-can-run.md))
- **Birgitta Böckeler, Robert C. Martin, Unmesh Joshi**: Agent-written tests and agent-confirmed failures prove little, so humans must write or approve the behavioural spec and mutation testing must show the tests bite.
  - "When the agent both writes the test and confirms it failed, a red test tells you the agent ran it and saw failure, not that the failure was for the right reason." ([source](https://martinfowler.com/articles/exploring-gen-ai/tdd-in-the-agent-loop.html), [Birgitta Böckeler: Agent-written tests are not proof of correctness](../principles/bockeler/agent-written-tests-are-not-proof-of-correctness.md))
  - "If you've got a fairly elaborate system that requires a lot of behavioral specification, it is wise to have humans produce that, and I like Gherkin, the old behavior-driven development language, for it." ([source](https://www.aviator.co/podcast/uncle-bob-martin-ai-clean-code), [Robert C. Martin: Humans own the behavioural specification](../principles/unclebob/humans-own-the-behavioural-specification.md))
  - Also: [Unmesh Joshi: Coverage-driven generated tests are not a guardrail](../principles/joshi/coverage-driven-generated-tests-are-not-a-guardrail.md)

## Evidence to settle it
For a set of features, compare defects escaping a fully agent-written and agent-run test suite against defects escaping a human-approved acceptance suite on the same code, and run mutation testing on both.

## Metric
Scoreboard: Mutation score (`mutation-score`). Compare mutation score of agent-authored suites with human-approved suites on the same modules, alongside escaped defects for each.

## Related principles
- [principles/tan/agents-verify-their-own-work-so-humans-stop-being-the-bottleneck.md](../principles/tan/agents-verify-their-own-work-so-humans-stop-being-the-bottleneck.md) - Lauren Tan: Agents verify their own work so humans stop being the bottleneck
- [principles/anthropic/done-means-a-check-the-agent-can-run.md](../principles/anthropic/done-means-a-check-the-agent-can-run.md) - Anthropic engineering: Done means a check the agent can run
- [principles/bockeler/agent-written-tests-are-not-proof-of-correctness.md](../principles/bockeler/agent-written-tests-are-not-proof-of-correctness.md) - Birgitta Böckeler: Agent-written tests are not proof of correctness
- [principles/unclebob/humans-own-the-behavioural-specification.md](../principles/unclebob/humans-own-the-behavioural-specification.md) - Robert C. Martin: Humans own the behavioural specification
- [principles/joshi/coverage-driven-generated-tests-are-not-a-guardrail.md](../principles/joshi/coverage-driven-generated-tests-are-not-a-guardrail.md) - Unmesh Joshi: Coverage-driven generated tests are not a guardrail
