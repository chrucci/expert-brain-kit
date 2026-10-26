# Review capacity is the bottleneck, so size work to it

Verified: 8 verbatim quotes from 13 sources

Dimension: Processes (processes)

Evidence: measurement

How to measure: Track PR size, review queue time, review minutes per PR and change failure rate as agent output grows.

Agents generate code faster than humans can verify it, so review becomes the rate limiter: output goes up and review time rises sharply. Teams should treat review capacity as a measured resource. That means handing agents one small, scoped task at a time, keeping PRs to roughly 100 lines a human can actually follow, batching reviews, and slowing generation rather than letting approval become a rubber stamp. Do not cut headcount until the review gap is closed.

## Quotes

> Read `tasks/plan.md` and `tasks/todo.md`, then take the next unchecked task and only that one.
>
> [agent-skills: docs/copilot-setup.md](https://github.com/addyosmani/agent-skills/blob/main/docs/copilot-setup.md)

> Scope discipline is the single biggest determinant of whether an agent’s PR is mergeable or has to be unwound.
>
> [Agent Skills | AddyOsmani.com](https://addyosmani.com/blog/agent-skills/)

> What happens if we can’t apply the constraint because the volume of changes is higher than our tools can consume? We end up building a queue and relying on a verification system that moves at human speed.
>
> [Agentic Code Quality](https://addyosmani.com/blog/agentic-code-quality/)

> The ones handling it well treat review capacity as a real resource to be measured, protected and spent deliberately, not as slack that AI has freed up.
>
> [Agentic Code Review | AddyOsmani.com](https://addyosmani.com/blog/agentic-code-review/)

> When output increases faster than verification capacity, review becomes the rate limiter.
>
> [Code Review in the Age of AI | AddyOsmani.com](https://addyosmani.com/blog/code-review-in-the-age-of-ai/)

> I now define a session duration before I spawn anything, and I size the task scope to fit.
>
> [Your parallel Agent limit | AddyOsmani.com](https://addyosmani.com/blog/cognitive-parallel-agents/)

> Surrender scales with size. A 50-line change you can actually read; a 600-line change you cannot.
>
> [Cognitive Surrender | AddyOsmani.com](https://addyosmani.com/blog/cognitive-surrender/)

> AI flips this: a junior engineer can now generate code faster than a senior engineer can critically audit it.
>
> [Comprehension Debt - the hidden cost of AI generated code. | AddyOsmani.com](https://addyosmani.com/blog/comprehension-debt/)

## Support

Established: 13 independent sources support this principle.

Expert: Addy Osmani

Topics: human-roles, metrics, processes, team-size

## Related principles

- [Addy Osmani: Run parallel agents only on independent work, and only as many as you can review](run-parallel-agents-only-on-independent-work-and-only-as-many-as-you-can-review.md)
- [Addy Osmani: Measure outcomes and comprehension, not activity](measure-outcomes-and-comprehension-not-activity.md)
