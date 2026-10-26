# Work in small batches, especially as AI speeds up change

Verified: 7 verbatim quotes from 3 sources

Dimension: Processes (processes)

Evidence: measurement

How to measure: Track lines changed per commit and changes per release against change lead time, change fail rate and rework rate as AI adoption rises.

Keep each change as small as possible and keep rollback cheap. Small changes are easier to review, ship and recover from. AI makes large changelists easy to produce, so teams have to hold this discipline deliberately or faster coding won't turn into better delivery.

## Quotes

> The negative impact on delivery stability is larger (an estimated 7.2% reduction for every 25% increase in AI adoption).
>
> [Accelerate at p.40](https://services.google.com/fh/files/misc/2024_final_dora_report.pdf#page=40)

> DORA has consistently shown that larger changes are slower and more prone to creating instability.
>
> [Accelerate at p.40](https://services.google.com/fh/files/misc/2024_final_dora_report.pdf#page=40)

> Considered together, our data suggest that improving the development process does not automatically improve software delivery—at least not without proper adherence to the basics of successful software delivery, like small batch sizes and robust testing mechanisms.
>
> [Accelerate at p.40](https://services.google.com/fh/files/misc/2024_final_dora_report.pdf#page=40)

> Enforce the discipline of working in small batches,
> which improves product performance and reduces
> friction for AI-assisted teams.
>
> [State of AI-assisted at p.64](https://services.google.com/fh/files/misc/2025_state_of_ai_assisted_software_development.pdf#page=64)

> individual effectiveness should not
> necessarily be pursued as a goal
> in and of itself.
>
> [State of AI-assisted at p.58](https://services.google.com/fh/files/misc/2025_state_of_ai_assisted_software_development.pdf#page=58)

> Smaller changes are easier to rationalize and to move through the delivery process. Smaller changes are also easier to recover from if there’s a failure.
>
> [DORA | DORA’s software delivery performance metrics](https://dora.dev/guides/dora-metrics/)

> Teams should make each change as small as possible to make the delivery process fast and stable.
>
> [DORA | DORA’s software delivery performance metrics](https://dora.dev/guides/dora-metrics/)

## Support

Established: 3 independent sources support this principle.

Expert: DORA

Topics: deterministic-guardrails, metrics, processes

## Related principles

- [DORA: Speed and stability are not a tradeoff](speed-and-stability-are-not-a-tradeoff.md)
- [DORA: Point AI at the delivery bottleneck, not at more code](point-ai-at-the-delivery-bottleneck-not-at-more-code.md)
