# Let verification and risk set agent autonomy

Verified: 8 verbatim quotes from 13 sources

Dimension: Roles for agents (agent-roles)

Evidence: experience

How to measure: Classify agent tasks by risk tier and autonomy level, and compare escaped-defect, rollback and rework rates across tiers.

How much freedom an agent gets, and how closely humans review its work, should follow blast radius, reversibility and how strong the automated verification is, not the task name or the model's confidence. Use explicit tiers (always, ask first, never; green, yellow and red zones), keep permissions tight outside trusted environments, and raise autonomy only as evidence builds up. Tighten it again when trust is lost.

## Quotes

> You can use the `--dangerously-skip-permissions` flag only in trusted local projects where you want to bypass manual tool approval prompts.
>
> [agent-skills: docs/antigravity-setup.md](https://github.com/addyosmani/agent-skills/blob/main/docs/antigravity-setup.md)

> A human gate at each step vs. a hands-off run**: agent-skills checkpoints by default; Superpowers minimizes mid-run check-ins on purpose.
>
> [agent-skills: docs/comparison.md](https://github.com/addyosmani/agent-skills/blob/main/docs/comparison.md)

> you approve the plan once, then it runs autonomously.
>
> [agent-skills: README.md](https://github.com/addyosmani/agent-skills/blob/main/README.md)

> The autonomy level should follow the verification process, not the task name.
>
> [Agentic Autonomy Levels | AddyOsmani.com](https://addyosmani.com/blog/agentic-autonomy-levels/)

> A config change earns a linter and a glance. A payments path earns the full stack: types, tests, two different AI reviewers, a human who owns that system, and a security pass.
>
> [Agentic Code Review | AddyOsmani.com](https://addyosmani.com/blog/agentic-code-review/)

> A person draws the map, not the agent; left to choose, the agent starts in the scariest file, because the scariest file has the most interesting names.
>
> [Brownfield Agentic Engineering](https://addyosmani.com/blog/brownfield-agentic-engineering/)

> As agents can browse the web, query databases, write to filesystems, and trigger deploys, what they’re *allowed* to do becomes as important as what they’re *capable* of doing.
>
> [Is the IDE dead? | AddyOsmani.com](https://addyosmani.com/blog/death-of-the-ide/)

> If it’s boilerplate, glue code, or a throwaway CI script you’ll never look at again, delegate it.
>
> [Don't Outsource the Learning | AddyOsmani.com](https://addyosmani.com/blog/dont-outsource-learning/)

## Support

Established: 13 independent sources support this principle.

Expert: Addy Osmani

Topics: agent-roles, deterministic-guardrails, human-roles, processes

## Related principles

- [Addy Osmani: Separate, narrow agent roles with a human orchestrating](separate-narrow-agent-roles-with-a-human-orchestrating.md)
- [Addy Osmani: Humans own the outer loop: intent, judgment and the ship decision](humans-own-the-outer-loop-intent-judgment-and-the-ship-decision.md)
