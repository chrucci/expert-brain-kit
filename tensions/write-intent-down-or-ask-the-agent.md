# Write intent down or ask the agent?

Status: open. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should a team record intent, decisions and tacit knowledge in documents, or keep code simple and ask the agent when questions come up?

Why open: Beck's view is opinion, and the other side's evidence is mostly experience; METR's measurement shows tacit knowledge hurts but not that documents fix it.

## Sides
- **Kent Beck**: Agents weaken the case for docs and ADRs; keep code simple and ask the agent about the source rather than write documents that go stale.
  - "So I think that the case for documentation actually gets weaker if we have the genie, not stronger." ([source](https://newsletter.kentbeck.com/p/genie-session-codex-for-macgpusortedmap?t=1758s), [Kent Beck: Ask the agent instead of writing docs that go stale](../principles/beck/ask-the-agent-instead-of-writing-docs-that-go-stale.md))
- **Gergely Orosz, Charity Majors, OpenAI engineering, METR** (measured): Intent, decisions and tacit rules are invisible to agents unless written into versioned artifacts in the repo, so preserve prompts, specs and decision records.
  - "I find that the prompt and conversation with the agent carries more information than the PR itself, at least for me." ([source](https://newsletter.pragmaticengineer.com/p/building-codex-with-tibo-sottiaux?t=1716s), [Gergely Orosz: Preserve the intent and decisions behind agent code](../principles/orosz/preserve-the-intent-and-decisions-behind-agent-code.md))
  - "Those tests and techniques are not about testing for correctness or what *ought* to be happening, they are about observing and encoding what *is* happening." ([source](https://charity.wtf/p/ai-demands-more-engineering-discipline), [Charity Majors: Encode the team's knowledge into the system](../principles/majors/encode-the-team-s-knowledge-into-the-system.md))
  - Also: [OpenAI engineering: The repository is the agent's system of record](../principles/openai/the-repository-is-the-agent-s-system-of-record.md), [METR: Tacit knowledge and implicit standards limit AI in mature codebases](../principles/metr/tacit-knowledge-and-implicit-standards-limit-ai-in-mature-codebases.md)

## Evidence to settle it
Collect real questions about why the code is the way it is and time how accurately they get answered by asking an agent over code alone versus code plus decision records, and count agent mistakes traced to missing context.

## Metric
Scoreboard: Rework rate (`rework-rate`). Compare rework rate in areas with maintained decision records against areas without, and tag rework caused by context that was not in the repo.

## Related principles
- [principles/beck/ask-the-agent-instead-of-writing-docs-that-go-stale.md](../principles/beck/ask-the-agent-instead-of-writing-docs-that-go-stale.md) - Kent Beck: Ask the agent instead of writing docs that go stale
- [principles/orosz/preserve-the-intent-and-decisions-behind-agent-code.md](../principles/orosz/preserve-the-intent-and-decisions-behind-agent-code.md) - Gergely Orosz: Preserve the intent and decisions behind agent code
- [principles/majors/encode-the-team-s-knowledge-into-the-system.md](../principles/majors/encode-the-team-s-knowledge-into-the-system.md) - Charity Majors: Encode the team's knowledge into the system
- [principles/openai/the-repository-is-the-agent-s-system-of-record.md](../principles/openai/the-repository-is-the-agent-s-system-of-record.md) - OpenAI engineering: The repository is the agent's system of record
- [principles/metr/tacit-knowledge-and-implicit-standards-limit-ai-in-mature-codebases.md](../principles/metr/tacit-knowledge-and-implicit-standards-limit-ai-in-mature-codebases.md) - METR: Tacit knowledge and implicit standards limit AI in mature codebases
