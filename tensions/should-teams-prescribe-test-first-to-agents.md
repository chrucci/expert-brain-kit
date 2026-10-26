# Should teams prescribe test-first to agents?

Status: leaning. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should the team instruct agents to follow a test-first process such as TDD, or only verify outcomes and leave the process to the agent?

Why leaning: The only quality measurement (Böckeler's) found no gain from prescribed TDD, while the test-first side rests on experience; Martin's measurement shows the discipline changes code shape but not that it improves quality.

## Sides
- **Birgitta Böckeler** (measured): Prescribing TDD added cost with no measured quality gain; enforce what must happen with hooks and invest in feedback on results.
  - "Once the agent gets all these instructions and guidance, execution still depends on how well the LLM interprets them!" ([source](https://martinfowler.com/articles/exploring-gen-ai/context-engineering-coding-agents.html), [Birgitta Böckeler: Verify outcomes instead of prescribing the agent's process](../principles/bockeler/verify-outcomes-instead-of-prescribing-the-agent-s-process.md))
- **Simon Willison, Kent Beck, Robert C. Martin**: Agents should work test-first in small test-gated steps, because without it they drift, skip tests or delete assertions.
  - "When you implement this use playwright and red/green TDD, plan that too" ([source](https://simonwillison.net/2026/Apr/23/liteparse-for-the-web/), [Simon Willison: Automated tests are mandatory, and agents work test-first](../principles/willison/automated-tests-are-mandatory-and-agents-work-test-first.md))
  - "So I'm gonna keep using tests because it makes sense to me to use tests. And I've had really bad experiences with the genie not using tests. or deleting tests or taking assertions out of tests." ([source](https://newsletter.kentbeck.com/p/genie-session-codex-for-macgpusortedmap?t=841s), [Kent Beck: Rein in the agent with small, test-gated steps](../principles/beck/rein-in-the-agent-with-small-test-gated-steps.md))
  - Also: [Robert C. Martin: Agree on shared deterministic gates and loosen thresholds only as agents improve](../principles/unclebob/agree-on-shared-deterministic-gates-and-loosen-thresholds-only-as-agents-improve.md)

## Evidence to settle it
Run the same set of tasks with and without TDD instructions, several runs each, and compare blind quality rankings, mutation scores, defects and tokens per task.

## Metric
Scoreboard: Mutation score (`mutation-score`). Compare mutation score and tokens per task between TDD-prompted and outcome-only runs; equal scores at lower cost favour the outcome side.

## Related principles
- [principles/bockeler/verify-outcomes-instead-of-prescribing-the-agent-s-process.md](../principles/bockeler/verify-outcomes-instead-of-prescribing-the-agent-s-process.md) - Birgitta Böckeler: Verify outcomes instead of prescribing the agent's process
- [principles/willison/automated-tests-are-mandatory-and-agents-work-test-first.md](../principles/willison/automated-tests-are-mandatory-and-agents-work-test-first.md) - Simon Willison: Automated tests are mandatory, and agents work test-first
- [principles/beck/rein-in-the-agent-with-small-test-gated-steps.md](../principles/beck/rein-in-the-agent-with-small-test-gated-steps.md) - Kent Beck: Rein in the agent with small, test-gated steps
- [principles/unclebob/agree-on-shared-deterministic-gates-and-loosen-thresholds-only-as-agents-improve.md](../principles/unclebob/agree-on-shared-deterministic-gates-and-loosen-thresholds-only-as-agents-improve.md) - Robert C. Martin: Agree on shared deterministic gates and loosen thresholds only as agents improve
