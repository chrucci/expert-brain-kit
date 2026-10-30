# Count tokens or only outcomes?

Status: open. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should leaders track token spend per engineer as a sign of healthy agent adoption?

Why open: Yegge's measurement concerns cost telemetry and DORA's concerns reliance versus usage, so neither tests whether spend predicts outcomes.

## Sides
- **Steve Yegge** (measured): Token spend shows real practice up to about 15M tokens a day, so track it on the way up, then switch to waste and outcomes per token.
  - "Token usage per turn (not per content block — avoids double-counting)" ([source](https://github.com/gastownhall/gastown/blob/main/docs/design/factory-worker-api.md), [Steve Yegge: Measure token spend on the way up, then waste and outcomes](../principles/yegge/measure-token-spend-on-the-way-up-then-waste-and-outcomes.md))
- **Gergely Orosz, Charity Majors, DORA** (measured): Activity metrics like tokens and AI lines reward looking busy and invite gaming, so judge AI only by delivery outcomes and set no individual usage targets.
  - "This is an observed thing that when you start to have more output, you increase your deployment frequency. You often, not always, but you often have more regressions." ([source](https://newsletter.pragmaticengineer.com/p/distributed-databases-with-peter?t=4967s), [Gergely Orosz: Measure delivery outcomes, not AI activity](../principles/orosz/measure-delivery-outcomes-not-ai-activity.md))
  - "While we may look at some metrics to understand adoption and usage, there's no specific set of quantitative metrics we expect each person to hit." ([source](https://www.honeycomb.io/blog/ai-norms-values-part-2-ai-honeycomb-engineering), [Charity Majors: No individual AI-usage quotas](../principles/majors/no-individual-ai-usage-quotas.md))
  - Also: [DORA: Judge AI by downstream impact, not adoption](../principles/dora/judge-ai-by-downstream-impact-not-adoption.md)

## Evidence to settle it
Correlate per-engineer token spend over a quarter with their change fail rate, rework and lead time, and see whether spend predicts outcomes below and above the threshold.

## Metric
Correlation between daily token spend per engineer and outcome metrics such as lead time and change fail rate, computed separately below and above 15M tokens a day.

## Related principles
- [principles/yegge/measure-token-spend-on-the-way-up-then-waste-and-outcomes.md](../principles/yegge/measure-token-spend-on-the-way-up-then-waste-and-outcomes.md) - Steve Yegge: Measure token spend on the way up, then waste and outcomes
- [principles/orosz/measure-delivery-outcomes-not-ai-activity.md](../principles/orosz/measure-delivery-outcomes-not-ai-activity.md) - Gergely Orosz: Measure delivery outcomes, not AI activity
- [principles/majors/no-individual-ai-usage-quotas.md](../principles/majors/no-individual-ai-usage-quotas.md) - Charity Majors: No individual AI-usage quotas
- [principles/dora/judge-ai-by-downstream-impact-not-adoption.md](../principles/dora/judge-ai-by-downstream-impact-not-adoption.md) - DORA: Judge AI by downstream impact, not adoption
