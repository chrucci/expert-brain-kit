# Is token spend a useful team metric?

Status: leaning. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should a leader track and encourage per-engineer token spend during adoption, or ignore activity measures in favour of outcomes?

Why leaning: DORA's measurement found usage frequency less meaningful than downstream impact, which favours outcome measures over spend.

## Sides
- **Steve Yegge** (measured): Token spend shows real practice and is worth pushing up to around 15M tokens a day before switching to waste and outcomes per token.
  - "Token usage per turn (not per content block — avoids double-counting)" ([source](https://github.com/gastownhall/gastown/blob/main/docs/design/factory-worker-api.md), [Steve Yegge: Measure token spend on the way up, then waste and outcomes](../principles/yegge/measure-token-spend-on-the-way-up-then-waste-and-outcomes.md))
- **DORA, Gergely Orosz, Charity Majors** (measured): Usage and token counts reward looking busy and invite gaming; judge AI only by delivery outcomes and never set individual usage targets.
  - "We determined measuring usage frequency is likely not as meaningful as measuring reliance for understanding AI’s centrality to development workflows." ([source](https://services.google.com/fh/files/misc/2024_final_dora_report.pdf#page=30), [DORA: Judge AI by downstream impact, not adoption](../principles/dora/judge-ai-by-downstream-impact-not-adoption.md))
  - "This is an observed thing that when you start to have more output, you increase your deployment frequency. You often, not always, but you often have more regressions." ([source](https://newsletter.pragmaticengineer.com/p/distributed-databases-with-peter?t=4967s), [Gergely Orosz: Measure delivery outcomes, not AI activity](../principles/orosz/measure-delivery-outcomes-not-ai-activity.md))
  - Also: [Charity Majors: No individual AI-usage quotas](../principles/majors/no-individual-ai-usage-quotas.md)

## Evidence to settle it
Over two quarters, correlate each engineer's token spend with their change fail rate, rework and lead time, and check whether teams told to raise spend improve outcomes more than teams given only outcome goals.

## Metric
Scoreboard: AI-assisted change share (`ai-assisted-share`). Read AI-assisted share next to change fail rate and rework rate; if usage climbs without outcome gains, activity metrics are not tracking value.

## Related principles
- [principles/yegge/measure-token-spend-on-the-way-up-then-waste-and-outcomes.md](../principles/yegge/measure-token-spend-on-the-way-up-then-waste-and-outcomes.md) - Steve Yegge: Measure token spend on the way up, then waste and outcomes
- [principles/dora/judge-ai-by-downstream-impact-not-adoption.md](../principles/dora/judge-ai-by-downstream-impact-not-adoption.md) - DORA: Judge AI by downstream impact, not adoption
- [principles/orosz/measure-delivery-outcomes-not-ai-activity.md](../principles/orosz/measure-delivery-outcomes-not-ai-activity.md) - Gergely Orosz: Measure delivery outcomes, not AI activity
- [principles/majors/no-individual-ai-usage-quotas.md](../principles/majors/no-individual-ai-usage-quotas.md) - Charity Majors: No individual AI-usage quotas
