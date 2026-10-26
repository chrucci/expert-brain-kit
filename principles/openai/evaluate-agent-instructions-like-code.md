# Evaluate agent instructions like code

Verified: 4 verbatim quotes from 2 sources

Dimension: Techniques (techniques)

Evidence: experience

How to measure: For each skill or rule version, track eval scores, regressions caught before release, and false findings on safe and unrelated changes.

Treat skills and review rules as artifacts that need regression tests. Run a small eval of prompts, captured traces and checks, including cases that should trigger, safe counterexamples and unrelated changes. Narrow or remove instructions that produce noise, because noisy guidance quickly erodes the team's trust in the agent.

## Quotes

> Codex could find and cite local guidance that a default review might miss, but broad instructions could easily create noise.
>
> [Custom Code Review rules for Codex | OpenAI Developers](https://developers.openai.com/blog/custom-code-review-rules-for-codex/)

> Try one change that should trigger the rule, one safe counterexample, and one unrelated change. Check that the first produces a useful finding and the others do not create noise, then refine the guidance from what you see.
>
> [Custom Code Review rules for Codex | OpenAI Developers](https://developers.openai.com/blog/custom-code-review-rules-for-codex/)

> Review updates to the rules and narrow or remove guidance that repeatedly produces noise.
>
> [Custom Code Review rules for Codex | OpenAI Developers](https://developers.openai.com/blog/custom-code-review-rules-for-codex/)

> Concretely, an eval is: a prompt → a captured run (trace + artifacts) → a small set of checks → a score you can compare over time.
>
> [Testing Agent Skills Systematically with Evals | OpenAI Developers](https://developers.openai.com/blog/eval-skills/)

## Support

Established: 2 independent sources support this principle.

Expert: OpenAI engineering

Topics: deterministic-guardrails, metrics, techniques

## Related principles

- [OpenAI engineering: Encode reviewers' tribal knowledge as scoped agent review rules](encode-reviewers-tribal-knowledge-as-scoped-agent-review-rules.md)
- [OpenAI engineering: Engineers own the harness and turn each agent failure into a lasting fix](engineers-own-the-harness-and-turn-each-agent-failure-into-a-lasting-fix.md)
