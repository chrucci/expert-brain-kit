# Keep telemetry wide and high-cardinality

Verified: 3 verbatim quotes from 2 sources

Dimension: Tools (tools)

Evidence: opinion

How to measure: Measure how often engineers' or agents' production questions can be answered from existing event data without new instrumentation, and how long it takes to isolate an anomaly to a specific cause.

Splitting telemetry into separate metrics, logs and traces loses the relationships between attributes, and joining them back together (even with AI) becomes a bottleneck at agentic speed. Teams should store rich, wide, structured events that people and agents can query precisely.

## Quotes

> Joins across data siloes can be better than nothing, yes. But they don’t restore the relational seams.
>
> [Your Data Is Made Powerful By Context (so stop destroying it already)](https://charity.wtf/p/your-data-is-made-powerful-by-context)

> At agentic speed, that reconstruction becomes a bottleneck and a failure surface.
>
> [Your Data Is Made Powerful By Context (so stop destroying it already)](https://charity.wtf/p/your-data-is-made-powerful-by-context)

> Dashboards are not rigor. Metrics and logs are not rigor. Rigor requires precision: a function of how rich your data is in context and cardinality, and your ability to pick out meaningful events with a scalpel.
>
> [Production Is Where the Rigor Goes](https://www.honeycomb.io/blog/production-is-where-the-rigor-goes)

## Support

Established: 2 independent sources support this principle.

Expert: Charity Majors

Topics: tools

## Related principles

- [Charity Majors: Validation in production is the new bottleneck](validation-in-production-is-the-new-bottleneck.md)
- [Charity Majors: Agents instrument, roll out and watch changes](agents-instrument-roll-out-and-watch-changes.md)
