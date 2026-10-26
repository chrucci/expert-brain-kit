# A checkable definition of done, proven by fast execution

Verified: 8 verbatim quotes from 5 sources

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: Compare acceptance and post-merge defect rates for agent changes accepted on passing execution checks versus diff inspection, and track p95 inner-loop check time against its budget.

Each agent task, milestone or skill needs success criteria that can be checked, along with the commands to check them. The agent must pass tests, lint, typecheck or build before it moves on, and each failure becomes structured feedback for the next pass. Keep that inner loop fast, about a minute, so validation stays cheap enough to run every time.

## Quotes

> Codex can do this loop for you, but only if it knows what “good” looks like. That guidance can come from either the prompt or `AGENTS.md`.
>
> [Best practices | ChatGPT Learn](https://learn.chatgpt.com/guides/best-practices)

> Not letting the agent see its work by not giving details on how to best run build and test commands
>
> [Best practices | ChatGPT Learn](https://learn.chatgpt.com/guides/best-practices)

> If validation fails, the failure becomes evidence for the next repair pass. This keeps the next repair grounded in observed behavior, not just what looked right in the diff.
>
> [Build iterative repair loops with Codex](https://developers.openai.com/cookbook/examples/codex/build_iterative_repair_loops_with_codex/)

> The important part is that failures become structured feedback instead of a dead end.
>
> [Build iterative repair loops with Codex](https://developers.openai.com/cookbook/examples/codex/build_iterative_repair_loops_with_codex/)

> Iterative repair loops make agentic maintenance easier to review and operate because they separate judgment from proof.
>
> [Build iterative repair loops with Codex](https://developers.openai.com/cookbook/examples/codex/build_iterative_repair_loops_with_codex/)

> Before writing the skill itself, write down what “success” means in terms you can actually measure.
>
> [Testing Agent Skills Systematically with Evals | OpenAI Developers](https://developers.openai.com/blog/eval-skills/)

> Stop-and-fix rule: if validation fails, repair before moving on
>
> [Run long horizon tasks with Codex | OpenAI Developers](https://developers.openai.com/blog/run-long-horizon-tasks-with-codex/)

> want the inner loop to be as fast as possible. Okay. One minute was just a nice round number and we were able to hit it.
>
> [Extreme Harness Engineering for Token Billionaires: 1M LOC, 1B toks/day, 0% human code, 0% human review — Ryan Lopopolo, OpenAI Frontier & Symphony](https://latent.space/p/harness-eng)

## Support

Established: 5 independent sources support this principle.

Expert: OpenAI engineering

Topics: deterministic-guardrails, processes, techniques

## Related principles

- [OpenAI engineering: Deterministic checks in CI, model review only for judgment](deterministic-checks-in-ci-model-review-only-for-judgment.md)
- [OpenAI engineering: Plan, size and bound each agent run](plan-size-and-bound-each-agent-run.md)
