# Specialist role pipelines or lean subagents?

Status: open. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should a team split agent work into a fixed pipeline of specialist roles, or keep one main agent and use subagents only to protect context and cut cost?

Why open: Willison's cost data covers subagent savings but not quality against role pipelines, and the pipeline side is opinion and experience.

## Sides
- **Robert C. Martin, Steve Yegge**: Divide work into distinct agent roles (specifier, coder, cleaner, architect, QA, or worker, supervisor, merger) each owning one concern.
  - "Role prompts divide ownership inside that law: what a role may change, what it must verify, what it must leave to another role, and where its next handoff goes." ([source](https://github.com/unclebob/swarm-forge/blob/main/README.md), [Robert C. Martin: Pipeline of specialised agent roles with exclusive ownership](../principles/unclebob/pipeline-of-specialised-agent-roles-with-exclusive-ownership.md))
  - "Polecats manage their own session lifecycle. External manipulation bypasses verification." ([source](https://github.com/gastownhall/gastown/blob/main/docs/concepts/polecat-lifecycle.md), [Steve Yegge: Separate worker, supervisor and merger roles; supervisors are a safety net](../principles/yegge/separate-worker-supervisor-and-merger-roles-supervisors-are-a-safety-net.md))
- **Simon Willison, Kent Beck** (measured): Role swarms add coordination cost without matching benefit; use subagents for context isolation and cheaper models only.
  - "I really should have [followed my own advice](https://simonwillison.net/2026/Jul/3/judgement/) and leaned more heavily into subagents with cheaper models." ([source](https://simonwillison.net/2026/Jul/5/sqlite-utils-fable/), [Simon Willison: Use subagents to protect context and cut cost, not as role swarms](../principles/willison/use-subagents-to-protect-context-and-cut-cost-not-as-role-swarms.md))
  - "I have never been able to get two agents working on the same code base at the same time without my head exploding. So definitely anti that." ([source](https://newsletter.kentbeck.com/p/genie-lessons-nobody-wants-agents?t=1538s), [Kent Beck: Watch for the coordination tax of agent swarms](../principles/beck/watch-for-the-coordination-tax-of-agent-swarms.md))

## Evidence to settle it
Run the same features through a role pipeline and through a single agent with subagents, comparing escaped defects, rework, tokens per task and human coordination time.

## Metric
Escaped defects and tokens per completed feature for role-pipeline runs versus single-agent-with-subagents runs.

## Related principles
- [principles/unclebob/pipeline-of-specialised-agent-roles-with-exclusive-ownership.md](../principles/unclebob/pipeline-of-specialised-agent-roles-with-exclusive-ownership.md) - Robert C. Martin: Pipeline of specialised agent roles with exclusive ownership
- [principles/yegge/separate-worker-supervisor-and-merger-roles-supervisors-are-a-safety-net.md](../principles/yegge/separate-worker-supervisor-and-merger-roles-supervisors-are-a-safety-net.md) - Steve Yegge: Separate worker, supervisor and merger roles; supervisors are a safety net
- [principles/willison/use-subagents-to-protect-context-and-cut-cost-not-as-role-swarms.md](../principles/willison/use-subagents-to-protect-context-and-cut-cost-not-as-role-swarms.md) - Simon Willison: Use subagents to protect context and cut cost, not as role swarms
- [principles/beck/watch-for-the-coordination-tax-of-agent-swarms.md](../principles/beck/watch-for-the-coordination-tax-of-agent-swarms.md) - Kent Beck: Watch for the coordination tax of agent swarms
