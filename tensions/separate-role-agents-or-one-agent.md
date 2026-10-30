# Separate role agents or one agent?

Status: open. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should a team split agent work into separate specialised roles such as implementer and verifier, or drive a single capable agent?

Why open: Osmani measured that self-grading is too kind and Willison measured subagent cost savings, but neither compares a verifier split with a single strong agent on outcomes.

## Sides
- **Addy Osmani, Steve Yegge, Anthropic engineering, Kent Beck** (measured): The agent that writes a change should never grade it; use separate narrow-role agents for review, testing and merging.
  - "Adversarial fresh-context review of the agent's claims about how the legacy system works catches confident hallucinations before they become commits." ([source](https://github.com/addyosmani/agent-skills/blob/main/docs/adoption-guide.md), [Addy Osmani: Separate, narrow agent roles with a human orchestrating](../principles/osmani/separate-narrow-agent-roles-with-a-human-orchestrating.md))
  - "Polecats manage their own session lifecycle. External manipulation bypasses verification." ([source](https://github.com/gastownhall/gastown/blob/main/docs/concepts/polecat-lifecycle.md), [Steve Yegge: Separate worker, supervisor and merger roles; supervisors are a safety net](../principles/yegge/separate-worker-supervisor-and-merger-roles-supervisors-are-a-safety-net.md))
  - Also: [Anthropic engineering: Independent, human-calibrated agent reviewers](../principles/anthropic/independent-human-calibrated-agent-reviewers.md), [Kent Beck: Verify what the agent did, not what it claims](../principles/beck/verify-what-the-agent-did-not-what-it-claims.md)
- **Robert C. Martin, Simon Willison** (measured): Drive one capable agent like a senior colleague, and use subagents only to protect context and cut cost, not as role swarms.
  - "The real giveaway was that I never used the harness to create the harness. The whole time I was creating it, I was just driving a single agent, and the agent was getting better and better." ([source](https://www.aviator.co/podcast/uncle-bob-martin-ai-clean-code), [Robert C. Martin: Drive one capable agent rather than fencing it in](../principles/unclebob/drive-one-capable-agent-rather-than-fencing-it-in.md))
  - "I really should have [followed my own advice](https://simonwillison.net/2026/Jul/3/judgement/) and leaned more heavily into subagents with cheaper models." ([source](https://simonwillison.net/2026/Jul/5/sqlite-utils-fable/), [Simon Willison: Use subagents to protect context and cut cost, not as role swarms](../principles/willison/use-subagents-to-protect-context-and-cut-cost-not-as-role-swarms.md))

## Evidence to settle it
Run the same tasks with a single agent and with an implementer plus independent verifier agent, comparing escaped defects, tokens per task and human orchestration time.

## Metric
Scoreboard: Rework rate (`rework-rate`). Compare rework rate and token cost per merged change for single-agent versus role-split runs.

## Related principles
- [principles/osmani/separate-narrow-agent-roles-with-a-human-orchestrating.md](../principles/osmani/separate-narrow-agent-roles-with-a-human-orchestrating.md) - Addy Osmani: Separate, narrow agent roles with a human orchestrating
- [principles/yegge/separate-worker-supervisor-and-merger-roles-supervisors-are-a-safety-net.md](../principles/yegge/separate-worker-supervisor-and-merger-roles-supervisors-are-a-safety-net.md) - Steve Yegge: Separate worker, supervisor and merger roles; supervisors are a safety net
- [principles/anthropic/independent-human-calibrated-agent-reviewers.md](../principles/anthropic/independent-human-calibrated-agent-reviewers.md) - Anthropic engineering: Independent, human-calibrated agent reviewers
- [principles/beck/verify-what-the-agent-did-not-what-it-claims.md](../principles/beck/verify-what-the-agent-did-not-what-it-claims.md) - Kent Beck: Verify what the agent did, not what it claims
- [principles/unclebob/drive-one-capable-agent-rather-than-fencing-it-in.md](../principles/unclebob/drive-one-capable-agent-rather-than-fencing-it-in.md) - Robert C. Martin: Drive one capable agent rather than fencing it in
- [principles/willison/use-subagents-to-protect-context-and-cut-cost-not-as-role-swarms.md](../principles/willison/use-subagents-to-protect-context-and-cut-cost-not-as-role-swarms.md) - Simon Willison: Use subagents to protect context and cut cost, not as role swarms
