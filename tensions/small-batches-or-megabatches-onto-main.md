# Small batches or megabatches onto main?

Status: leaning. Verified: every side has a verbatim quote from a verified principle.

**Question:** When agents commit faster than the build can verify, should a team hold to small verified changes or land large batches and roll forward?

Why leaning: DORA's measurements tie larger changes to instability, while megabatching is a single practitioner's recent experience.

## Sides
- **Steve Yegge**: Land large batches onto main together and have agents diagnose and fix breakage, since one green build per commit becomes impossible.
  - "Once your commit rate outruns your build slots, one commit per green build becomes mathematically impossible." ([source](https://yegge.ai/essays/the-shape-of-things-to-come/), [Steve Yegge: Megabatch onto main once commits outrun the build](../principles/yegge/megabatch-onto-main-once-commits-outrun-the-build.md))
- **DORA, Addy Osmani** (measured): Keep each change small and rollback cheap; larger changes are slower and less stable, and AI makes holding this discipline more important.
  - "The negative impact on delivery stability is larger (an estimated 7.2% reduction for every 25% increase in AI adoption)." ([source](https://services.google.com/fh/files/misc/2024_final_dora_report.pdf#page=40), [DORA: Work in small batches, especially as AI speeds up change](../principles/dora/work-in-small-batches-especially-as-ai-speeds-up-change.md))
  - "Read `tasks/plan.md` and `tasks/todo.md`, then take the next unchecked task and only that one." ([source](https://github.com/addyosmani/agent-skills/blob/main/docs/copilot-setup.md), [Addy Osmani: Review capacity is the bottleneck, so size work to it](../principles/osmani/review-capacity-is-the-bottleneck-so-size-work-to-it.md))

## Evidence to settle it
On a high-commit-rate repo, alternate periods of batched bisection with small changes and megabatch landing, comparing time main stays red, commit-to-landing time and production failures.

## Metric
Scoreboard: Change fail rate (`change-fail-rate`). Read change fail rate next to lead time for each landing mode; megabatching wins only if lead time drops without fail rate rising.

## Related principles
- [principles/yegge/megabatch-onto-main-once-commits-outrun-the-build.md](../principles/yegge/megabatch-onto-main-once-commits-outrun-the-build.md) - Steve Yegge: Megabatch onto main once commits outrun the build
- [principles/dora/work-in-small-batches-especially-as-ai-speeds-up-change.md](../principles/dora/work-in-small-batches-especially-as-ai-speeds-up-change.md) - DORA: Work in small batches, especially as AI speeds up change
- [principles/osmani/review-capacity-is-the-bottleneck-so-size-work-to-it.md](../principles/osmani/review-capacity-is-the-bottleneck-so-size-work-to-it.md) - Addy Osmani: Review capacity is the bottleneck, so size work to it
