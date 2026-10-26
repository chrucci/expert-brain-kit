# Encode reviewers' tribal knowledge as scoped agent review rules

Verified: 6 verbatim quotes from 3 sources

Dimension: Techniques (techniques)

Evidence: measurement

How to measure: On an eval with known violations and safe counterexamples, compare the share of required findings recovered with and without the rules, and track how many review rounds agent PRs take.

Have an agent review every PR using short review rules, each scoped to the code it governs and each naming a safe path. The rules capture the invariants that human reviewers keep explaining. To keep the review loop converging, tell the reviewer agent to raise only high-priority issues and let author agents defer or push back. On OpenAI's eval suite, rules like these raised recovery of required findings from 58% to 98%.

## Quotes

> If you and your team have a `code_review.md` file and reference it from `AGENTS.md`, Codex can follow that guidance during review as well. This is a strong pattern for teams that want review behavior to stay consistent across repositories and contributors.
>
> [Best practices | ChatGPT Learn](https://learn.chatgpt.com/guides/best-practices)

> In the primary suite, rule-guided variants recovered 98% of the required custom findings, compared with 58.3% in the baseline control.
>
> [Custom Code Review rules for Codex | OpenAI Developers](https://developers.openai.com/blog/custom-code-review-rules-for-codex/)

> Small, scoped sets with an explicit safe path helped Codex focus on what was most useful without applying a rule to every nearby change.
>
> [Custom Code Review rules for Codex | OpenAI Developers](https://developers.openai.com/blog/custom-code-review-rules-for-codex/)

> And initially the Codex driving the code author was willing to be bullied by the PR reviewer, which meant you could end up in a situation where things were not converging.
>
> [Extreme Harness Engineering for Token Billionaires: 1M LOC, 1B toks/day, 0% human code, 0% human review — Ryan Lopopolo, OpenAI Frontier & Symphony](https://latent.space/p/harness-eng)

> The reviewer agents were instructed to bias toward merging the thing to not surface anything greater than a P two in priority.
>
> [Extreme Harness Engineering for Token Billionaires: 1M LOC, 1B toks/day, 0% human code, 0% human review — Ryan Lopopolo, OpenAI Frontier & Symphony](https://latent.space/p/harness-eng)

> But also on the code authoring agent side, we also gave it the flexibility to either defer or push back against review feedback, right?
>
> [Extreme Harness Engineering for Token Billionaires: 1M LOC, 1B toks/day, 0% human code, 0% human review — Ryan Lopopolo, OpenAI Frontier & Symphony](https://latent.space/p/harness-eng)

## Support

Established: 3 independent sources support this principle.

Expert: OpenAI engineering

Topics: agent-roles, processes, techniques

## Related principles

- [OpenAI engineering: Evaluate agent instructions like code](evaluate-agent-instructions-like-code.md)
- [OpenAI engineering: Deterministic checks in CI, model review only for judgment](deterministic-checks-in-ci-model-review-only-for-judgment.md)
- [OpenAI engineering: Human attention, not code generation, is the bottleneck](human-attention-not-code-generation-is-the-bottleneck.md)
