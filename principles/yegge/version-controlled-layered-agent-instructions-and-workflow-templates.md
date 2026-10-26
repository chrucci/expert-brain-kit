# Version-controlled, layered agent instructions and workflow templates

Verified: 8 verbatim quotes from 10 sources

Dimension: Techniques (techniques)

Evidence: experience

How to measure: Track whether all instruction files go through code review, how many overrides are stale after each workflow release, and how often work is misrouted or sessions end without submitting.

Keep agent instructions in the repository where they can be reviewed: one shared cross-tool file, broad role-level directives plus narrow step-level overrides scoped to each project, and reusable workflow templates that end in a mandatory completion step. Define roles with examples, anti-examples and out-of-scope lists, and check overrides deterministically for drift. Operators can then steer agents consistently without forking workflows.

## Quotes

> Commit the instruction files (`AGENTS.md`, `CLAUDE.md`, `GEMINI.md`, as applicable) to git so all team members and AI tools get the same instructions.
>
> [beads: docs/getting-started/ide-setup.md](https://github.com/gastownhall/beads/blob/main/docs/getting-started/ide-setup.md)

> Teams can review the instructions like any other project documentation
>
> [beads: docs/integrations/copilot-cli.md](https://github.com/gastownhall/beads/blob/main/docs/integrations/copilot-cli.md)

> Use `bd remember "insight"` for durable project facts; keep per-operator preferences in your harness's own memory.
>
> [beads: README.md](https://github.com/gastownhall/beads/blob/main/README.md)

> Agents do NOT use `bd mol current` or `bd close <step-id>` for formula workflows.
>
> [gastown: docs/concepts/molecules.md](https://github.com/gastownhall/gastown/blob/main/docs/concepts/molecules.md)

> Both layers are intentional: the directive sets the rig-level expectation
>
> [gastown: docs/contrib-harnesses/polecat-pr-flow/README.md](https://github.com/gastownhall/gastown/blob/main/docs/contrib-harnesses/polecat-pr-flow/README.md)

> Operators can customize agent behavior at the town or rig level without modifying the Go binary or embedded templates.
>
> [gastown: docs/design/architecture.md](https://github.com/gastownhall/gastown/blob/main/docs/design/architecture.md)

> Both are needed: directives for broad guardrails, overlays for surgical fixes.
>
> [gastown: docs/design/directives-and-overlays.md](https://github.com/gastownhall/gastown/blob/main/docs/design/directives-and-overlays.md)

> `example_tasks` and `anti_examples` are more valuable than any taxonomy — they're grounded in the language of problems, not solutions.
>
> [gastown: docs/gas-city/crew-specialization-design.md](https://github.com/gastownhall/gastown/blob/main/docs/gas-city/crew-specialization-design.md)

## Support

Established: 10 independent sources support this principle.

Expert: Steve Yegge

Topics: deterministic-guardrails, processes, techniques

## Related principles

- [Steve Yegge: Keep agent context lean and re-inject it automatically](keep-agent-context-lean-and-re-inject-it-automatically.md)
- [Steve Yegge: Enforce critical rules mechanically, and curate the fences](enforce-critical-rules-mechanically-and-curate-the-fences.md)
