# Grow the harness from real failures and prune it

Verified: 8 verbatim quotes from 8 sources

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: Track how often each logged class of agent mistake recurs after a check or rule has been added for it, and how many harness pieces are removed at each periodic audit.

When an agent makes a mistake, or a review comment comes up again, fix it for good with a lint rule, test, type, hook or rule line instead of fixing the diff by hand, and never take a gate off once it is added. The harness around the model matters more than which model is picked, so debug it first, and audit it every few weeks to remove pieces that better models have made redundant.

## Quotes

> Adoption should make quality monotonically better: each phase adds a gate that doesn't come back off. If a month in you can't name what's now enforced that wasn't before, the rollout has stalled.
>
> [agent-skills: docs/adoption-guide.md](https://github.com/addyosmani/agent-skills/blob/main/docs/adoption-guide.md)

> The most important habit in harness engineering is treating agent mistakes as permanent signals.
>
> [Agent Harness Engineering | AddyOsmani.com](https://addyosmani.com/blog/agent-harness-engineering/)

> While if you instead try to codify things like specific lessons, tests, lint rules, anything, especially that is small enough that it can be codified in your repo, it can teach future agents.
>
> [Agentic Skill Decay](https://addyosmani.com/blog/agentic-skill-decay/)

> When an agent struggles with something repeatedly, treat it as a codebase problem before treating it as a context problem. Restructure the code. Add a linter rule. Improve the test coverage.
>
> [Stop Using /init for AGENTS.md | AddyOsmani.com](https://addyosmani.com/blog/agents-md/)

> And so I think there’s high value personally in, like maybe every couple of weeks, maybe at once a month even, just running doctor on your skills, on your setup, and auditing what you’re doing and seeing, okay, well, what still holds true?
>
> [Audit your Agent files](https://addyosmani.com/blog/audit-your-agent-files/)

> When the same review comment appears again, move it into a lint rule, hook, type, test, or skill. Keep prose for constraints that cannot be enforced mechanically.
>
> [Brownfield Agentic Engineering](https://addyosmani.com/blog/brownfield-agentic-engineering/)

> So when an agent does something dumb, I’ve learned to debug the harness first. Usually it’s a missing tool, a rule I wrote too loosely, a guardrail I forgot, or a context window full of junk.
>
> [The New Software Lifecycle | AddyOsmani.com](https://addyosmani.com/blog/new-sdlc-vibe-coding/)

> Automated verification at every step (CI/CD, linters, type checkers, tests as guardrails)
>
> [The 80% Problem in Agentic Coding | AddyOsmani.com](https://addyosmani.com/blog/the-80-problem-in-agentic-coding/)

## Support

Established: 8 independent sources support this principle.

Expert: Addy Osmani

Topics: deterministic-guardrails, processes, techniques, tools

## Related principles

- [Addy Osmani: Deterministic checks, not the agent, decide when work is done](deterministic-checks-not-the-agent-decide-when-work-is-done.md)
- [Addy Osmani: Keep agent context lean, hand-written and earned](keep-agent-context-lean-hand-written-and-earned.md)
