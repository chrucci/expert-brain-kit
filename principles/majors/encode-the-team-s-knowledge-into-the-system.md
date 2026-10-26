# Encode the team's knowledge into the system

Verified: 7 verbatim quotes from 4 sources

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: opinion

How to measure: Count incidents or agent failures whose fix needed knowledge held only by specific people, and the share of services that can be regenerated and accepted by existing behavioural suites and replayed traffic.

Agents cannot use intuition, tribal knowledge or context that lives in long-tenured engineers' heads. Teams should write down intent and actual behaviour in machine-readable form, such as characterization tests, capture/replay and semantic conventions, so that code can be safely regenerated and validation does not depend on a few people.

## Quotes

> Those tests and techniques are not about testing for correctness or what *ought* to be happening, they are about observing and encoding what *is* happening.
>
> [AI demands more engineering discipline. Not less](https://charity.wtf/p/ai-demands-more-engineering-discipline)

> The knowledge in our heads is unavailable to AI until we encode it into the system, after all.
>
> [AI demands more engineering discipline. Not less](https://charity.wtf/p/ai-demands-more-engineering-discipline)

> The fact that we cannot regenerate our code in the same way is a sign that we do not understand it.
>
> [AI demands more engineering discipline. Not less](https://charity.wtf/p/ai-demands-more-engineering-discipline)

> The answer is: by using human intuition to bridge the gaps. This will not work for agents. Our wisdom must be encoded into the system, or it does not exist.
>
> [Your Data Is Made Powerful By Context (so stop destroying it already)](https://charity.wtf/p/your-data-is-made-powerful-by-context)

> a few people who have been there for 10+ years and hold the missing context in their heads. As the rate of change is ramping up, all this duct tape is flying off the bus.
>
> [Happy Birthday to Us: Honeycomb 10 Year Manifesto, Part 1](https://www.honeycomb.io/blog/honeycomb-10-year-manifesto-part-1)

> If the knowledge is not encoded into the system, it does not scale.
>
> [Happy Birthday to Us: Honeycomb 10 Year Manifesto, Part 1](https://www.honeycomb.io/blog/honeycomb-10-year-manifesto-part-1)

> As the rate of change ticks up to 10x, 100x or more, all the duct tape comes flying off the bus. You have to encode the context into your system instead of relying on human intuition to bridge the gaps.
>
> [Production Is Where the Rigor Goes](https://www.honeycomb.io/blog/production-is-where-the-rigor-goes)

## Support

Established: 4 independent sources support this principle.

Expert: Charity Majors

Topics: deterministic-guardrails, emerging

## Related principles

- [Charity Majors: Move trust from authorship to deterministic validation](move-trust-from-authorship-to-deterministic-validation.md)
- [Charity Majors: Validation in production is the new bottleneck](validation-in-production-is-the-new-bottleneck.md)
