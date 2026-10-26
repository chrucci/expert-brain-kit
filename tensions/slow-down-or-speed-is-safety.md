# Slow down, or speed is safety?

Status: open. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should a team deliberately slow agent-driven delivery until trust catches up, or push throughput on the basis that speed and stability rise together?

Why open: DORA's measurements show speed and stability correlate, but the same data links AI adoption to rising instability, which supports Beck's warning, so the evidence cuts both ways.

## Sides
- **Kent Beck, Birgitta Böckeler**: Agents produce code faster than trust; slow down so it really works and lean on trust-building practices.
  - "Slow development to ensure that the damn stuff actually works." ([source](https://newsletter.kentbeck.com/p/trust-factory), [Kent Beck: Slow down until trust catches up with code](../principles/beck/slow-down-until-trust-catches-up-with-code.md))
  - "My experience with giving strong models lots of autonomy, and surrendering to them in a way, has often led to constant rework and surprises at later stages." ([source](https://martinfowler.com/articles/exploring-gen-ai/local-models-for-coding-experiences.html), [Birgitta Böckeler: Keep comprehension in the moment](../principles/bockeler/keep-comprehension-in-the-moment.md))
- **DORA** (measured): Throughput and stability improve together and going slower does not make delivery safer; measure both and fix instability directly.
  - "Yet our data shows AI adoption not only fails to fix instability, it is currently associated with increasing instability." ([source](https://services.google.com/fh/files/misc/2025_state_of_ai_assisted_software_development.pdf#page=41), [DORA: Speed and stability are not a tradeoff](../principles/dora/speed-and-stability-are-not-a-tradeoff.md))
  - "DORA’s research has repeatedly demonstrated that speed and stability are not tradeoffs. In fact, we see that the metrics are correlated for most teams." ([source](https://dora.dev/guides/dora-metrics/), [DORA: Measure delivery by both throughput and instability](../principles/dora/measure-delivery-by-both-throughput-and-instability.md))

## Evidence to settle it
Track deployment frequency, lead time, change fail rate and rework per service as AI adoption grows, and test whether services that throttled agent output saw lower instability than those that did not.

## Metric
Scoreboard: Change fail rate (`change-fail-rate`). Plot change fail rate against deployment frequency per service over time; if fail rate rises with AI-driven throughput, Beck's call to slow down is supported.

## Related principles
- [principles/beck/slow-down-until-trust-catches-up-with-code.md](../principles/beck/slow-down-until-trust-catches-up-with-code.md) - Kent Beck: Slow down until trust catches up with code
- [principles/bockeler/keep-comprehension-in-the-moment.md](../principles/bockeler/keep-comprehension-in-the-moment.md) - Birgitta Böckeler: Keep comprehension in the moment
- [principles/dora/speed-and-stability-are-not-a-tradeoff.md](../principles/dora/speed-and-stability-are-not-a-tradeoff.md) - DORA: Speed and stability are not a tradeoff
- [principles/dora/measure-delivery-by-both-throughput-and-instability.md](../principles/dora/measure-delivery-by-both-throughput-and-instability.md) - DORA: Measure delivery by both throughput and instability
