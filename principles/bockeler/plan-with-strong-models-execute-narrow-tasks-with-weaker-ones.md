# Plan with strong models, execute narrow tasks with weaker ones

Verified: 5 verbatim quotes from 2 sources

Dimension: Tools (tools)

Evidence: experience

How to measure: Track success rate and engineer setup time for local-model tasks, grouped by whether the task was pre-planned by a stronger model and scoped to named files, against a frontier-model baseline.

Small or local models are viable only for small, well-defined tasks pointed at specific files, ideally planned first by a stronger model. Tasks that need a lot of code discovery or complex logic break down, so teams should split work by what each model can do.

## Quotes

> I would therefore say that it's still not ready for a simple “plug and play” experience for developers who don't want to spend too much time on it.
>
> [Viability of local models for coding](https://martinfowler.com/articles/exploring-gen-ai/local-models-for-coding-factors.html)

> Depends on the task (more on that in the next memo), but obviously nowhere near the type of capability we can get from the big models. Overall it was very hit and miss.
>
> [Viability of local models for coding](https://martinfowler.com/articles/exploring-gen-ai/local-models-for-coding-factors.html)

> I reach for it when I have small, straightforward tasks, often pre-planned by a bigger model
>
> [Experiences with local models for coding](https://martinfowler.com/articles/exploring-gen-ai/local-models-for-coding-experiences.html)

> Building a game from scratch (planning with Claude Sonnet, then delegating coding execution to the local model) - started well, but fell apart for more complex logic
>
> [Experiences with local models for coding](https://martinfowler.com/articles/exploring-gen-ai/local-models-for-coding-experiences.html)

> The more discovery the agent has to do, the more it requires tool calling, and the more it fills up the context window, and therefore precious RAM.
>
> [Experiences with local models for coding](https://martinfowler.com/articles/exploring-gen-ai/local-models-for-coding-experiences.html)

## Support

Established: 2 independent sources support this principle.

Expert: Birgitta Böckeler

Topics: agent-roles, techniques, tools

## Related principles

- [Birgitta Böckeler: Measure the harness and agent setup with data](measure-the-harness-and-agent-setup-with-data.md)
