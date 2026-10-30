# Prescribe test-first process to agents?

Status: leaning. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should a team require agents to follow a test-first workflow, or only verify outcomes?

Why leaning: Böckeler measured no quality gain from prescribing TDD, while Martin's measurement shows the suite's shape changes but not that quality improves.

## Sides
- **Birgitta Böckeler** (measured): Prescribing TDD added cost without measurable quality gains, so enforce must-haves with hooks and invest in automated feedback on results instead.
  - "Once the agent gets all these instructions and guidance, execution still depends on how well the LLM interprets them!" ([source](https://martinfowler.com/articles/exploring-gen-ai/context-engineering-coding-agents.html), [Birgitta Böckeler: Verify outcomes instead of prescribing the agent's process](../principles/bockeler/verify-outcomes-instead-of-prescribing-the-agent-s-process.md))
- **Simon Willison, Kent Beck, Robert C. Martin** (measured): Agents should work red/green test-first in small test-gated steps, and the chosen test discipline measurably changes the suite and the program.
  - "When you implement this use playwright and red/green TDD, plan that too" ([source](https://simonwillison.net/2026/Apr/23/liteparse-for-the-web/), [Simon Willison: Automated tests are mandatory, and agents work test-first](../principles/willison/automated-tests-are-mandatory-and-agents-work-test-first.md))
  - "So I'm gonna keep using tests because it makes sense to me to use tests. And I've had really bad experiences with the genie not using tests. or deleting tests or taking assertions out of tests." ([source](https://newsletter.kentbeck.com/p/genie-session-codex-for-macgpusortedmap?t=841s), [Kent Beck: Rein in the agent with small, test-gated steps](../principles/beck/rein-in-the-agent-with-small-test-gated-steps.md))
  - Also: [Robert C. Martin: Choose the test discipline deliberately](../principles/unclebob/choose-the-test-discipline-deliberately.md)

## Evidence to settle it
Run the same set of representative tasks several times with and without a TDD instruction, comparing mutation score, escaped defects, blind quality ranking and tokens per task.

## Metric
Scoreboard: Mutation score (`mutation-score`). Compare mutation score and tokens per task for TDD-instructed versus outcome-only runs; equal scores at higher cost favour the outcome side.

## Related principles
- [principles/bockeler/verify-outcomes-instead-of-prescribing-the-agent-s-process.md](../principles/bockeler/verify-outcomes-instead-of-prescribing-the-agent-s-process.md) - Birgitta Böckeler: Verify outcomes instead of prescribing the agent's process
- [principles/willison/automated-tests-are-mandatory-and-agents-work-test-first.md](../principles/willison/automated-tests-are-mandatory-and-agents-work-test-first.md) - Simon Willison: Automated tests are mandatory, and agents work test-first
- [principles/beck/rein-in-the-agent-with-small-test-gated-steps.md](../principles/beck/rein-in-the-agent-with-small-test-gated-steps.md) - Kent Beck: Rein in the agent with small, test-gated steps
- [principles/unclebob/choose-the-test-discipline-deliberately.md](../principles/unclebob/choose-the-test-discipline-deliberately.md) - Robert C. Martin: Choose the test discipline deliberately
