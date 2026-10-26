# Validation in production is the new bottleneck

Verified: 8 verbatim quotes from 6 sources

Dimension: Processes (processes)

Evidence: opinion

How to measure: Track time from deploy to confirmed production behaviour for agent-generated changes, and the share of those changes validated against production telemetry before the next change ships.

Agents push the cost of writing code close to zero, so a team's limit becomes how fast it can validate what each change does in production. Pre-production checks quickly stop paying off. Teams should replace merge-and-hope with a build, deploy, observe, learn loop, using flags, progressive rollouts and traces, so that validation keeps up with generation.

## Quotes

> Having nondeterministic code in production is finally forcing us to do the things we should have done all along. Instrumenting with traces. Tests and evals in production.
>
> [AI demands more engineering discipline. Not less](https://charity.wtf/p/ai-demands-more-engineering-discipline)

> The hardest and most interesting problems (I think) are around validation. How do we validate a change rate that is 10x, 100x, 1000x greater than before?
>
> [Your Data Is Made Powerful By Context (so stop destroying it already)](https://charity.wtf/p/your-data-is-made-powerful-by-context)

> agents are going to need production observability with speed, flexibility, TONS of context, and some kind of ontological grounding via semantic conventions.
>
> [Your Data Is Made Powerful By Context (so stop destroying it already)](https://charity.wtf/p/your-data-is-made-powerful-by-context)

> How do you expect your agents to validate each change, if the consequences of each change cannot be found?
>
> [Your Data Is Made Powerful By Context (so stop destroying it already)](https://charity.wtf/p/your-data-is-made-powerful-by-context)

> AI has pushed the cost of generating code down close to zero, which means that the bottleneck has moved from building to learning and validating.
>
> [Happy Birthday to Us: Honeycomb 10 Year Manifesto, Part 1](https://www.honeycomb.io/blog/honeycomb-10-year-manifesto-part-1)

> The bottleneck shifts from, “How fast can I write code?” to, “How fast can I understand what’s happening and make good decisions about it?”
>
> [“You Had One Job”: Why Twenty Years of DevOps Has Failed to Do it](https://www.honeycomb.io/blog/you-had-one-job-why-twenty-years-of-devops-has-failed-to-do-it)

> You have to validate at agentic speed to match the code being generated at agentic speed.
>
> [Production Is Where the Rigor Goes](https://www.honeycomb.io/blog/production-is-where-the-rigor-goes)

> And if you look at like AI has made it more important than ever to have these fast feedback loops, right? It has shortened the definition of what fast is.
>
> [O11ycast | Ep. #88, Metrics Are Good, Actually with Charity Majors | Heavybit](https://www.heavybit.com/library/podcasts/o11ycast/ep-88-metrics-are-good-actually-with-charity-majors)

## Support

Established: 6 independent sources support this principle.

Expert: Charity Majors

Topics: deterministic-guardrails, processes

## Related principles

- [Charity Majors: Agents instrument, roll out and watch changes](agents-instrument-roll-out-and-watch-changes.md)
- [Charity Majors: Keep telemetry wide and high-cardinality](keep-telemetry-wide-and-high-cardinality.md)
- [Charity Majors: AI amplifies discipline, so measure outcomes alongside throughput](ai-amplifies-discipline-so-measure-outcomes-alongside-throughput.md)
