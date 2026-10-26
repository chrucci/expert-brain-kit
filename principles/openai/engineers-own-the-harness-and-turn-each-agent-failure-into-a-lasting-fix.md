# Engineers own the harness and turn each agent failure into a lasting fix

Verified: 8 verbatim quotes from 5 sources

Dimension: Roles for humans (human-roles)

Evidence: experience

How to measure: Track how often an agent failure leads to a change in repository guidance, tooling or tests rather than a retry or manual fix, and how often the same class of failure comes back afterwards.

When agents write the code, engineers mainly design the agent's environment, state intent and build feedback loops. Every repeated agent mistake is a sign that a requirement, tool, guardrail or piece of documentation is missing. Engineers write that missing piece into the repository as docs, lints, tests, environment config or eval cases, so the fix lasts beyond the one change.

## Quotes

> Keep it practical. A short, accurate `AGENTS.md` is more useful than a long file full of vague rules. Start with the basics, then add new rules only after you notice repeated mistakes.
>
> [Best practices | ChatGPT Learn](https://learn.chatgpt.com/guides/best-practices)

> When Codex makes the same mistake twice, ask it for a retrospective and update
> `AGENTS.md`. Guidance stays practical and based on real friction.
>
> [Best practices | ChatGPT Learn](https://learn.chatgpt.com/guides/best-practices)

> For a single skill, a small set of 10–20 prompts is enough to surface regressions and confirm improvements early.
>
> [Testing Agent Skills Systematically with Evals | OpenAI Developers](https://developers.openai.com/blog/eval-skills/)

> **Let real failures drive coverage.** Every manual fix is a signal. Turn it into a test so the skill keeps getting it right.
>
> [Testing Agent Skills Systematically with Evals | OpenAI Developers](https://developers.openai.com/blog/eval-skills/)

> we needed to understand what changes when a software engineering team’s primary job is no longer to write code, but to design environments, specify intent, and build feedback loops that allow Codex agents to do reliable work.
>
> [Harness engineering: leveraging Codex in an agent-first world](https://web.archive.org/web/20261006122733id_/https://openai.com/index/harness-engineering/)

> We prioritize work, translate user feedback into acceptance criteria, and validate outcomes. When the agent struggles, we treat it as a signal: identify what is missing—tools, guardrails, documentation—and feed it back into the repository, always by having Codex itself write the fix.
>
> [Harness engineering: leveraging Codex in an agent-first world](https://web.archive.org/web/20261006122733id_/https://openai.com/index/harness-engineering/)

> Setting a startup script, environment variables, and internet
>
> [How OpenAI at p.11](https://cdn.openai.com/pdf/6a2631dc-783e-479b-b1a4-af0cfbd38630/how-openai-uses-codex.pdf#page=11)

> So the whole meta of the thing is to basically tease out of the heads of all the engineers on my team, what they think good looks like, what they would do by default, or what they would coach a new hire on the team to do to get things to merch.
>
> [Extreme Harness Engineering for Token Billionaires: 1M LOC, 1B toks/day, 0% human code, 0% human review — Ryan Lopopolo, OpenAI Frontier & Symphony](https://latent.space/p/harness-eng)

## Support

Established: 5 independent sources support this principle.

Expert: OpenAI engineering

Topics: deterministic-guardrails, human-roles, techniques

## Related principles

- [OpenAI engineering: The repository is the agent's system of record](the-repository-is-the-agent-s-system-of-record.md)
- [OpenAI engineering: Enforce architecture and taste mechanically and continuously](enforce-architecture-and-taste-mechanically-and-continuously.md)
- [OpenAI engineering: Evaluate agent instructions like code](evaluate-agent-instructions-like-code.md)
