# Done means a check the agent can run

Verified: 8 verbatim quotes from 8 sources

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: Compare rework after merge, escaped defects and cost per task for agent work with and without an agent-runnable pass/fail check named in the task.

Every agent task needs a deterministic finish line, such as passing tests, a build or a script that calls the endpoint, and an environment where the agent can actually run it before it hands work back. Without one, the human becomes the verification loop. A near-perfect verifier is what lets a team safely give agents long unattended runs, and adding a check is cheaper than raising effort or moving to a bigger model.

## Quotes

> Software is comparatively easy to test and review—you can run code and see if it works—which makes it easier to trust an agent and catch its mistakes.
>
> [Measuring AI agent autonomy in practice](https://www.anthropic.com/research/measuring-agent-autonomy)

> Sonnet 5.5 generally checks its work before reporting a change as done, but at `low` effort it sometimes skips a check that exercises the change.
>
> [Building with Claude Sonnet 5.5](https://claude.dev/blog/building-with-claude-sonnet-5-5/)

> Write each task as a self-contained ticket that states what's wrong, what done looks like, and how to prove it.
>
> [Claude Code in the cloud: a field guide to cloud sessions](https://claude.dev/blog/claude-code-in-the-cloud/)

> Done means: every endpoint uses the new client, the old client is deleted, and the test suite passes.
>
> [Getting the most out of Opus 5.5 in Claude and Claude Code](https://claude.dev/blog/getting-the-most-out-of-opus-5-5/)

> Verification skills have had the most measurable impact on Claude’s output quality internally. It can be worth having an engineer spend a week just making your verification skills excellent.
>
> [Lessons from building Claude Code: How we use skills](https://claude.dev/blog/lessons-from-building-claude-code-how-we-use-skills/)

> One habit that can cut turns is giving the model a way to check its work. For example, a test to run, a build, or a script that calls the endpoint.
>
> [What a task costs on Opus 5.5](https://claude.dev/blog/what-a-task-costs-on-opus-5-5/)

> So it’s important that the task verifier is nearly perfect, otherwise Claude will solve the wrong problem.
>
> [Building a C compiler with a team of parallel Claudes](https://www.anthropic.com/engineering/building-c-compiler)

> Without a check it can run, “looks done” is the only signal available, and you become the verification loop: every mistake waits for you to notice it.
>
> [Best practices for Claude Code - Claude Code Docs](https://www.anthropic.com/engineering/claude-code-best-practices)

## Support

Established: 8 independent sources support this principle.

Expert: Anthropic engineering

Topics: agent-roles, deterministic-guardrails, techniques

## Related principles

- [Anthropic engineering: Move rules out of prompts and into deterministic gates](move-rules-out-of-prompts-and-into-deterministic-gates.md)
- [Anthropic engineering: Agree the plan and testable criteria before agents build](agree-the-plan-and-testable-criteria-before-agents-build.md)
- [Anthropic engineering: Measure verified outcomes with noise-aware evals](measure-verified-outcomes-with-noise-aware-evals.md)
