# Match model and effort to scope, checkability and supervision

Verified: 8 verbatim quotes from 3 sources

Dimension: Tools (tools)

Evidence: measurement

How to measure: For each task class, compare cost, cycle time, rework and failure type across model tiers and effort levels.

Send well-specified, checkable or closely supervised work to cheaper models and lower effort, and reserve the biggest models and highest effort for long unsupervised runs and edge-case-heavy domains like security and review. Higher effort also means the agent makes more assumptions on the human's behalf, and it fixes missed edge cases but not a wrong approach, so let evals decide.

## Quotes

> Sonnet 5.5 fits best when the task has a clear spec and a way to check the result.
>
> [Building with Claude Sonnet 5.5](https://claude.dev/blog/building-with-claude-sonnet-5-5/)

> Use Sonnet 5.5 for well-scoped everyday tasks like fixing bugs and quickly iterating on features.
>
> [Building with Claude Sonnet 5.5](https://claude.dev/blog/building-with-claude-sonnet-5-5/)

> The `default` model stays Opus 5.5, so switch with `/model sonnet` for well-scoped tasks.
>
> [Building with Claude Sonnet 5.5](https://claude.dev/blog/building-with-claude-sonnet-5-5/)

> For agentic coding and multistep tool use, start with `medium` for well-specified tasks and move to `high` for harder or longer ones.
>
> [Building with Claude Sonnet 5.5](https://claude.dev/blog/building-with-claude-sonnet-5-5/)

> Use `xhigh` or `max` only where your evals show a quality gain.
>
> [Building with Claude Sonnet 5.5](https://claude.dev/blog/building-with-claude-sonnet-5-5/)

> Start there, evaluate, and then pick the effort level your workload needs.
>
> [Building with Claude Sonnet 5.5](https://claude.dev/blog/building-with-claude-sonnet-5-5/)

> Extra effort gave better results in domains where verification and edgecase testing was more useful like hardware, code review, and security.
>
> [Using Claude Code: Spending your effort](https://claude.dev/blog/spending-your-effort/)

> Most days need three models: a small one for lookups, Opus 5.5 for work you supervise closely, and a bigger one for the hardest tasks.
>
> [What a task costs on Opus 5.5](https://claude.dev/blog/what-a-task-costs-on-opus-5-5/)

## Support

Established: 3 independent sources support this principle.

Expert: Anthropic engineering

Topics: agent-roles, techniques, tools

## Related principles

- [Anthropic engineering: Measure verified outcomes with noise-aware evals](measure-verified-outcomes-with-noise-aware-evals.md)
- [Anthropic engineering: Done means a check the agent can run](done-means-a-check-the-agent-can-run.md)
