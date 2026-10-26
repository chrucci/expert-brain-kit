# The repository is the agent's system of record

Verified: 8 verbatim quotes from 4 sources

Dimension: Techniques (techniques)

Evidence: experience

How to measure: Track how often agent mistakes or review corrections come from context that wasn't in the repository, and check docs for freshness and cross-links in CI.

Team agreements, business rules, conventions and quirks that the code doesn't show belong in versioned, layered instruction files. Use a short root AGENTS.md as a map, with nested overrides close to specialised code. Knowledge kept in chat, documents outside the repo or people's heads doesn't exist for the agent.

## Quotes

> Create persistent defaults in your Codex home directory so every repository inherits your working agreements.
>
> [Custom instructions with AGENTS.md | ChatGPT Learn](https://learn.chatgpt.com/docs/agent-configuration/agents-md)

> Add overrides in nested directories when specific teams need different rules.
>
> [Custom instructions with AGENTS.md | ChatGPT Learn](https://learn.chatgpt.com/docs/agent-configuration/agents-md)

> Codex stops searching once it reaches your current directory, so place overrides as close to specialized work as possible.
>
> [Custom instructions with AGENTS.md | ChatGPT Learn](https://learn.chatgpt.com/docs/agent-configuration/agents-md)

> Before asking Codex to review or repair an artifact, give it a small shared contract. That keeps the loop focused on the issues that matter, instead of asking the model to infer every product and style rule from scratch.
>
> [Build iterative repair loops with Codex](https://developers.openai.com/cookbook/examples/codex/build_iterative_repair_loops_with_codex/)

> From the agent’s point of view, anything it can’t access in-context while running effectively doesn’t exist. Knowledge that lives in Google Docs, chat threads, or people’s heads are not accessible to the system.
>
> [Harness engineering: leveraging Codex in an agent-first world](https://web.archive.org/web/20261006122733id_/https://openai.com/index/harness-engineering/)

> A short `AGENTS.md` (roughly 100 lines) is injected into context and serves primarily as a map, with pointers to deeper sources of truth elsewhere.
>
> [Harness engineering: leveraging Codex in an agent-first world](https://web.archive.org/web/20261006122733id_/https://openai.com/index/harness-engineering/)

> Dedicated linters and CI jobs validate that the knowledge base is up to date, cross-linked, and structured correctly.
>
> [Harness engineering: leveraging Codex in an agent-first world](https://web.archive.org/web/20261006122733id_/https://openai.com/index/harness-engineering/)

> include naming conventions, business logic, known quirks, or
>
> [How OpenAI at p.12](https://cdn.openai.com/pdf/6a2631dc-783e-479b-b1a4-af0cfbd38630/how-openai-uses-codex.pdf#page=12)

## Support

Established: 4 independent sources support this principle.

Expert: OpenAI engineering

Topics: deterministic-guardrails, techniques

## Related principles

- [OpenAI engineering: Engineers own the harness and turn each agent failure into a lasting fix](engineers-own-the-harness-and-turn-each-agent-failure-into-a-lasting-fix.md)
- [OpenAI engineering: Durable plans and run logs make delegated work inspectable](durable-plans-and-run-logs-make-delegated-work-inspectable.md)
