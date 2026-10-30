# Megabatch onto main or small batches?

Status: leaning. Verified: every side has a verbatim quote from a verified principle.

**Question:** When agents commit faster than the build can verify, should a team land large batches and roll forward, or hold to small changes?

Why leaning: DORA has measured that larger changes reduce stability, while megabatching rests on one practitioner's experience.

## Sides
- **Steve Yegge**: Once commits outrun build slots, land large batches onto main together and have agents diagnose and fix whatever breaks.
  - "Once your commit rate outruns your build slots, one commit per green build becomes mathematically impossible." ([source](https://yegge.ai/essays/the-shape-of-things-to-come/), [Steve Yegge: Megabatch onto main once commits outrun the build](../principles/yegge/megabatch-onto-main-once-commits-outrun-the-build.md))
- **DORA, Addy Osmani, Andrej Karpathy** (measured): Keep every change small and cheap to roll back, because larger changes are slower and less stable, and slow generation rather than outgrow review.
  - "The negative impact on delivery stability is larger (an estimated 7.2% reduction for every 25% increase in AI adoption)." ([source](https://services.google.com/fh/files/misc/2024_final_dora_report.pdf#page=40), [DORA: Work in small batches, especially as AI speeds up change](../principles/dora/work-in-small-batches-especially-as-ai-speeds-up-change.md))
  - "Read `tasks/plan.md` and `tasks/todo.md`, then take the next unchecked task and only that one." ([source](https://github.com/addyosmani/agent-skills/blob/main/docs/copilot-setup.md), [Addy Osmani: Review capacity is the bottleneck, so size work to it](../principles/osmani/review-capacity-is-the-bottleneck-so-size-work-to-it.md))
  - Also: [Andrej Karpathy: Keep agent changes small so verification stays fast](../principles/karpathy/keep-agent-changes-small-so-verification-stays-fast.md)

## Evidence to settle it
On a high-commit-rate repo, alternate weeks of megabatch landing and small-batch queueing, recording main-red time, commit-to-landing time and production failures.

## Metric
Scoreboard: Change fail rate (`change-fail-rate`). Compare change fail rate and recovery time under megabatch versus small-batch weeks.

## Related principles
- [principles/yegge/megabatch-onto-main-once-commits-outrun-the-build.md](../principles/yegge/megabatch-onto-main-once-commits-outrun-the-build.md) - Steve Yegge: Megabatch onto main once commits outrun the build
- [principles/dora/work-in-small-batches-especially-as-ai-speeds-up-change.md](../principles/dora/work-in-small-batches-especially-as-ai-speeds-up-change.md) - DORA: Work in small batches, especially as AI speeds up change
- [principles/osmani/review-capacity-is-the-bottleneck-so-size-work-to-it.md](../principles/osmani/review-capacity-is-the-bottleneck-so-size-work-to-it.md) - Addy Osmani: Review capacity is the bottleneck, so size work to it
- [principles/karpathy/keep-agent-changes-small-so-verification-stays-fast.md](../principles/karpathy/keep-agent-changes-small-so-verification-stays-fast.md) - Andrej Karpathy: Keep agent changes small so verification stays fast
