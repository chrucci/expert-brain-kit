# Agents never land their own work: a gated merge queue decides

Verified: 8 verbatim quotes from 17 sources

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: Track the share of agent changes that reach main only through the gated queue, main-branch breakages and reverts, rework from failed gates, and reopen rates for merge-validated versus self-closed tasks.

Worker agents run in isolated worktrees, push branches and open PRs, but never merge or push to main themselves. A separate merge role runs the project's deterministic checks (tests, lint, build), batches and bisects, sends failures back, reviews the combined diff of an epic before it lands atomically, and owns branch cleanup. 'Done' counts only once recorded gates pass, and a validated merge counts for more than a self-closed task.

## Quotes

> Do not commit, push, or run Dolt remote sync without explicit user or orchestrator approval.
>
> [beads: docs/getting-started/ide-setup.md](https://github.com/gastownhall/beads/blob/main/docs/getting-started/ide-setup.md)

> Avoid conflicts** - Claim atomically; use merge slots to serialize
>
> [beads: docs/multi-agent/coordination.md](https://github.com/gastownhall/beads/blob/main/docs/multi-agent/coordination.md)

> | Trusted CI, no human review needed | Enable auto-land |
>
> [gastown: docs/concepts/integration-branches.md](https://github.com/gastownhall/gastown/blob/main/docs/concepts/integration-branches.md)

> Work exists in the MQ, not in the polecat
>
> [gastown: docs/concepts/polecat-lifecycle.md](https://github.com/gastownhall/gastown/blob/main/docs/concepts/polecat-lifecycle.md)

> Merge your own PR. A maintainer or the merge queue handles merging.
>
> [gastown: docs/contrib-harnesses/polecat-pr-flow/polecat.md](https://github.com/gastownhall/gastown/blob/main/docs/contrib-harnesses/polecat-pr-flow/polecat.md)

> Sets a rig-level policy that a PR is the review artifact
>
> [gastown: docs/contrib-harnesses/polecat-pr-flow/README.md](https://github.com/gastownhall/gastown/blob/main/docs/contrib-harnesses/polecat-pr-flow/README.md)

> The refinery processes MRs through a batch-then-bisect merge queue (Bors-style). This is a core capability, not a pluggable strategy.
>
> [gastown: docs/design/architecture.md](https://github.com/gastownhall/gastown/blob/main/docs/design/architecture.md)

> There is no review step that examines the combined diff.
>
> [gastown: docs/design/convoy/roadmap.md](https://github.com/gastownhall/gastown/blob/main/docs/design/convoy/roadmap.md)

## Support

Established: 17 independent sources support this principle.

Expert: Steve Yegge

Topics: agent-count, agent-roles, deterministic-guardrails, processes

## Related principles

- [Steve Yegge: Megabatch onto main once commits outrun the build](megabatch-onto-main-once-commits-outrun-the-build.md)
- [Steve Yegge: Enforce critical rules mechanically, and curate the fences](enforce-critical-rules-mechanically-and-curate-the-fences.md)
- [Steve Yegge: Scale review with layers of agentic review](scale-review-with-layers-of-agentic-review.md)
