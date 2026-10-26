# Write docs or just ask the agent?

Status: open. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should a team write and maintain documents recording intent and decisions, or keep code simple and ask the agent when questions arise?

Why open: Both sides are opinion and experience, and no one has tested whether agents can recover intent from code alone.

## Sides
- **Kent Beck**: Agents weaken the case for docs and ADRs; ask the agent about the source instead of writing documents that go stale.
  - "So I think that the case for documentation actually gets weaker if we have the genie, not stronger." ([source](https://newsletter.kentbeck.com/p/genie-session-codex-for-macgpusortedmap?t=1758s), [Kent Beck: Ask the agent instead of writing docs that go stale](../principles/beck/ask-the-agent-instead-of-writing-docs-that-go-stale.md))
- **Gergely Orosz, OpenAI engineering, Charity Majors**: Intent, decisions and tacit rules are not in the code, so record them in versioned files beside it or they are lost to people and agents.
  - "I find that the prompt and conversation with the agent carries more information than the PR itself, at least for me." ([source](https://newsletter.pragmaticengineer.com/p/building-codex-with-tibo-sottiaux?t=1716s), [Gergely Orosz: Preserve the intent and decisions behind agent code](../principles/orosz/preserve-the-intent-and-decisions-behind-agent-code.md))
  - "Create persistent defaults in your Codex home directory so every repository inherits your working agreements." ([source](https://learn.chatgpt.com/docs/agent-configuration/agents-md), [OpenAI engineering: The repository is the agent's system of record](../principles/openai/the-repository-is-the-agent-s-system-of-record.md))
  - Also: [Charity Majors: Encode the team's knowledge into the system](../principles/majors/encode-the-team-s-knowledge-into-the-system.md)

## Evidence to settle it
Collect real questions engineers ask about a service, answer half by asking an agent of the code alone and half with linked specs and decision logs, and score accuracy and time, especially for why-questions.

## Metric
Share of questions about past design decisions answered correctly by an agent reading only the code versus with stored decision records.

## Related principles
- [principles/beck/ask-the-agent-instead-of-writing-docs-that-go-stale.md](../principles/beck/ask-the-agent-instead-of-writing-docs-that-go-stale.md) - Kent Beck: Ask the agent instead of writing docs that go stale
- [principles/orosz/preserve-the-intent-and-decisions-behind-agent-code.md](../principles/orosz/preserve-the-intent-and-decisions-behind-agent-code.md) - Gergely Orosz: Preserve the intent and decisions behind agent code
- [principles/openai/the-repository-is-the-agent-s-system-of-record.md](../principles/openai/the-repository-is-the-agent-s-system-of-record.md) - OpenAI engineering: The repository is the agent's system of record
- [principles/majors/encode-the-team-s-knowledge-into-the-system.md](../principles/majors/encode-the-team-s-knowledge-into-the-system.md) - Charity Majors: Encode the team's knowledge into the system
