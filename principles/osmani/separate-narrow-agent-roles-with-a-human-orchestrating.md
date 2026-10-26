# Separate, narrow agent roles with a human orchestrating

Verified: 8 verbatim quotes from 12 sources

Dimension: Roles for agents (agent-roles)

Evidence: measurement

How to measure: Compare escaped defects for changes checked by the authoring agent with changes checked by separate verifier agents, and record the overlap of findings across different AI reviewers on the team's own PRs.

The agent that writes a change should never be the one that grades it, because agents rate their own work too kindly. Give review, security and testing to separate single-role agents with least-privilege tools, and run differently built AI reviewers, since they rarely catch the same bugs. The human or a fixed command orchestrates, and agents do not call each other.

## Quotes

> Adversarial fresh-context review of the agent's claims about how the legacy system works catches confident hallucinations before they become commits.
>
> [agent-skills: docs/adoption-guide.md](https://github.com/addyosmani/agent-skills/blob/main/docs/adoption-guide.md)

> it removes the listed tools from the available pool while the skill is active, which is what least-privilege needs for passive stages such as review or audit.
>
> [agent-skills: docs/advanced-per-agent-configuration.md](https://github.com/addyosmani/agent-skills/blob/main/docs/advanced-per-agent-configuration.md)

> The user (or a slash command) is the orchestrator. **Personas do not call other personas.**
>
> [agent-skills: docs/agents.md](https://github.com/addyosmani/agent-skills/blob/main/docs/agents.md)

> The plugin registers reusable subagent definitions from the `agents/` directory:
>
> [agent-skills: docs/antigravity-setup.md](https://github.com/addyosmani/agent-skills/blob/main/docs/antigravity-setup.md)

> The code-reviewer, test-engineer, and security-auditor agents are designed for Copilot's agent model.
>
> [agent-skills: docs/copilot-setup.md](https://github.com/addyosmani/agent-skills/blob/main/docs/copilot-setup.md)

> Personas never invoke other personas; the only endorsed multi-persona pattern is parallel fan-out with a merge step
>
> [agent-skills: docs/developer-onboarding.md](https://github.com/addyosmani/agent-skills/blob/main/docs/developer-onboarding.md)

> Anthropic’s long-running harness work is explicit that separating generation from evaluation into distinct agents outperforms self-evaluation, because agents reliably skew positive when grading their own work.
>
> [Agent Harness Engineering | AddyOsmani.com](https://addyosmani.com/blog/agent-harness-engineering/)

> At this point in the climb, it becomes increasingly important to have independent verification: separate implementers and reviewers, separate test runners and QA, separate security checks, separate process gates for acceptance.
>
> [Agentic Autonomy Levels | AddyOsmani.com](https://addyosmani.com/blog/agentic-autonomy-levels/)

## Support

Established: 12 independent sources support this principle.

Expert: Addy Osmani

Topics: agent-count, agent-roles, tools

## Related principles

- [Addy Osmani: Deterministic checks, not the agent, decide when work is done](deterministic-checks-not-the-agent-decide-when-work-is-done.md)
- [Addy Osmani: Let verification and risk set agent autonomy](let-verification-and-risk-set-agent-autonomy.md)
