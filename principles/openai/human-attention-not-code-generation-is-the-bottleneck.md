# Human attention, not code generation, is the bottleneck

Verified: 8 verbatim quotes from 4 sources

Dimension: Roles for humans (human-roles)

Evidence: measurement

How to measure: Track weekly PR volume against time-to-first-review and time-to-merge, and synchronous human hours per merged PR.

Agents more than doubled PR volume at OpenAI, and review became the constraint. Synchronous human attention is the scarce resource. Humans should steer at milestones, keep design and architecture decisions, hand side work to background agents to review asynchronously, and review a sample of code to find where the system is struggling instead of micromanaging every line.

## Quotes

> At OpenAI, weekly PR volume has more than doubled since Q4, and we’re seeing similar trends for many of our customers.
>
> [Custom Code Review rules for Codex | OpenAI Developers](https://developers.openai.com/blog/custom-code-review-rules-for-codex/)

> It also means more pull requests waiting for someone who knows what to look for, and code review can quickly become the bottleneck.
>
> [Custom Code Review rules for Codex | OpenAI Developers](https://developers.openai.com/blog/custom-code-review-rules-for-codex/)

> We’re moving beyond single-shot prompts and tight pair-programming loops toward long-running teammates that can take a real slice of work end to end, with you steering at milestones instead of micromanaging every line.
>
> [Run long horizon tasks with Codex | OpenAI Developers](https://developers.openai.com/blog/run-long-horizon-tasks-with-codex/)

> We’re already seeing developers move faster when the agent absorbs routine implementation and verification, freeing humans up for the parts that matter most: design, architecture, product decisions, and the novel problems that don’t have a template.
>
> [Run long horizon tasks with Codex | OpenAI Developers](https://developers.openai.com/blog/run-long-horizon-tasks-with-codex/)

> If I spot a drive‑by fix, I fire a Codex task
>
> [How OpenAI at p.9](https://cdn.openai.com/pdf/6a2631dc-783e-479b-b1a4-af0cfbd38630/how-openai-uses-codex.pdf#page=9)

> Fire off tasks to capture tangential ideas, partial work, or
>
> [How OpenAI at p.11](https://cdn.openai.com/pdf/6a2631dc-783e-479b-b1a4-af0cfbd38630/how-openai-uses-codex.pdf#page=11)

> The only fundamentally scarce thing is the synchronous human attention of my team.
>
> [Extreme Harness Engineering for Token Billionaires: 1M LOC, 1B toks/day, 0% human code, 0% human review — Ryan Lopopolo, OpenAI Frontier & Symphony](https://latent.space/p/harness-eng)

> Like I have some representative sample of the code as it is written, and I have to use that to infer what the teams are struggling with, where they could use help, where they’re already moving quickly and I can pivot my focus elsewhere.
>
> [Extreme Harness Engineering for Token Billionaires: 1M LOC, 1B toks/day, 0% human code, 0% human review — Ryan Lopopolo, OpenAI Frontier & Symphony](https://latent.space/p/harness-eng)

## Support

Established: 4 independent sources support this principle.

Expert: OpenAI engineering

Topics: human-roles, metrics, processes

## Related principles

- [OpenAI engineering: Encode reviewers' tribal knowledge as scoped agent review rules](encode-reviewers-tribal-knowledge-as-scoped-agent-review-rules.md)
- [OpenAI engineering: Plan, size and bound each agent run](plan-size-and-bound-each-agent-run.md)
