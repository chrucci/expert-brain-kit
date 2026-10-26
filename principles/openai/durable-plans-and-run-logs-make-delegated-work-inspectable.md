# Durable plans and run logs make delegated work inspectable

Verified: 8 verbatim quotes from 3 sources

Dimension: Processes (processes)

Evidence: experience

How to measure: Measure how long a human needs to understand the state of a run after being away, and the time and interventions per run of a recurring task before and after earlier run records are available.

For long or recurring agent work, have the agent keep the spec, plan, status, decisions and the results of each pass in shareable files as it works. Humans can then step away and come back to steer, each run feeds context into the next one, and knowledge doesn't stay trapped in one person's chat history.

## Quotes

> That record lets a maintainer understand why the loop continued, why it stopped, and which artifact is ready for review.
>
> [Build iterative repair loops with Codex](https://developers.openai.com/cookbook/examples/codex/build_iterative_repair_loops_with_codex/)

> That is the difference between an impressive-looking edit and a repair workflow a maintainer can trust.
>
> [Build iterative repair loops with Codex](https://developers.openai.com/cookbook/examples/codex/build_iterative_repair_loops_with_codex/)

> A maintainer can start with the pass/fail pattern, open records for anything that still has a delta, and inspect only the repaired artifacts that are ready for review.
>
> [Build iterative repair loops with Codex](https://developers.openai.com/cookbook/examples/codex/build_iterative_repair_loops_with_codex/)

> Before wrapping up, I work with Codex to capture decisions that would otherwise disappear into the conversation: why one option was chosen, which approach is now preferred, and what someone should do differently next time.
>
> [Automating repetitive work at OpenAI with Codex](https://developers.openai.com/blog/automating-repetitive-work-at-openai-with-codex/)

> As the workflow improves, it produces more useful context. That context, in turn, helps Codex handle the next version of the task more effectively.
>
> [Automating repetitive work at OpenAI with Codex](https://developers.openai.com/blog/automating-repetitive-work-at-openai-with-codex/)

> Because the resulting notebook is easy to share, that practical knowledge doesn't have to stay trapped in one person's chat history.
>
> [Automating repetitive work at OpenAI with Codex](https://developers.openai.com/blog/automating-repetitive-work-at-openai-with-codex/)

> The hard part isn't proving that documentation is useful; it's making the documentation cheap enough to create while the work is happening.
>
> [Automating repetitive work at OpenAI with Codex](https://developers.openai.com/blog/automating-repetitive-work-at-openai-with-codex/)

> The most important technique was durable project memory. I wrote the spec, plan, constraints, and status in markdown files that Codex could revisit repeatedly. That prevented drift and kept a stable definition of “done.”
>
> [Run long horizon tasks with Codex | OpenAI Developers](https://developers.openai.com/blog/run-long-horizon-tasks-with-codex/)

## Support

Established: 3 independent sources support this principle.

Expert: OpenAI engineering

Topics: human-roles, processes, techniques

## Related principles

- [OpenAI engineering: The repository is the agent's system of record](the-repository-is-the-agent-s-system-of-record.md)
- [OpenAI engineering: Plan, size and bound each agent run](plan-size-and-bound-each-agent-run.md)
