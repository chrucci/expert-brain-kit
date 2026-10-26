# Deterministic checks in CI, model review only for judgment

Verified: 8 verbatim quotes from 3 sources

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: opinion

How to measure: Track the share of agent review comments that duplicate CI checks compared with comments on domain-rule violations, and which failures deterministic checks catch compared with rubric checks.

Formatting, linting, tests, branch protections and required approvals stay as the hard, deterministic gates. Model-based review and model-graded rubrics are added only for judgment calls that rules can't express. Each kind of check then runs where it is most reliable and easiest to debug.

## Quotes

> Keep rules concise, explain the behavior to flag and any safe path or
> exception, and reserve formatting and lint checks for CI.
>
> [Custom instructions with AGENTS.md | ChatGPT Learn](https://learn.chatgpt.com/docs/agent-configuration/agents-md)

> Put repository-wide checks at the root and service-specific
> checks in a nested file.
>
> [Custom instructions with AGENTS.md | ChatGPT Learn](https://learn.chatgpt.com/docs/agent-configuration/agents-md)

> Tests and linters work well for checks you can express deterministically; repository rules help capture the judgment that is harder to encode.
>
> [Custom Code Review rules for Codex | OpenAI Developers](https://developers.openai.com/blog/custom-code-review-rules-for-codex/)

> Keep formatting and other mechanical checks in CI. Save repository rules for the questions a reviewer would otherwise have to ask again.
>
> [Custom Code Review rules for Codex | OpenAI Developers](https://developers.openai.com/blog/custom-code-review-rules-for-codex/)

> Codex Code Review is still an additional reviewer; tests, branch protections, and required approvals continue to provide hard enforcement.
>
> [Custom Code Review rules for Codex | OpenAI Developers](https://developers.openai.com/blog/custom-code-review-rules-for-codex/)

> The value here is that everything is **deterministic and debuggable**.
>
> [Testing Agent Skills Systematically with Evals | OpenAI Developers](https://developers.openai.com/blog/eval-skills/)

> Deterministic checks answer *“did it do the basics?”* but they don’t answer *“did it do it the way you wanted?”*
>
> [Testing Agent Skills Systematically with Evals | OpenAI Developers](https://developers.openai.com/blog/eval-skills/)

> The pattern is consistent: begin with fast checks that explain behavior, then add slower, heavier checks only when they reduce risk.
>
> [Testing Agent Skills Systematically with Evals | OpenAI Developers](https://developers.openai.com/blog/eval-skills/)

## Support

Established: 3 independent sources support this principle.

Expert: OpenAI engineering

Topics: deterministic-guardrails, processes

## Related principles

- [OpenAI engineering: A checkable definition of done, proven by fast execution](a-checkable-definition-of-done-proven-by-fast-execution.md)
- [OpenAI engineering: Encode reviewers' tribal knowledge as scoped agent review rules](encode-reviewers-tribal-knowledge-as-scoped-agent-review-rules.md)
