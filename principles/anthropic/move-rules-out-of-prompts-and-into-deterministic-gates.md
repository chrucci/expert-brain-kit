# Move rules out of prompts and into deterministic gates

Verified: 8 verbatim quotes from 5 sources

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: Count violations of critical constraints and repeats of known review comments before and after each rule is moved from instructions into a hook, lint rule, permission or PR gate.

Anything that must always or never happen should be enforced by hooks, permissions, lint rules or access limits, not by instructions the model can fail to follow. Give each agent a single-purpose identity with minimal permissions. Turn corrections you keep making by hand into encoded checks, start them as personal or conversational loops, and promote them to team-wide PR gates once they are stable.

## Quotes

> We have type checkers. We have linters. We run the build. Claude is actually so good at writing lint rules.
>
> [Building Claude Code with Boris Cherny at 00:44:16](https://newsletter.pragmaticengineer.com/p/building-claude-code-with-boris-cherny?t=2656s)

> when a coworker puts up a pull request and I'm like, this is lintable. I'll just be at Claude. Please write a lint rule for this in that PR on their PR.
>
> [Building Claude Code with Boris Cherny at 00:44:16](https://newsletter.pragmaticengineer.com/p/building-claude-code-with-boris-cherny?t=2656s)

> anytime that a particular row had more than three or four instances, I would write a lint row for it. So just automate it with kind of static analysis.
>
> [Building Claude Code with Boris Cherny at 00:40:23](https://newsletter.pragmaticengineer.com/p/building-claude-code-with-boris-cherny?t=2423s)

> Give every agent a single-purpose identity with the minimum permissions for its job.
>
> [How Anthropic secures its AI-native software development lifecycle](https://claude.com/resources/articles/how-anthropic-secures-its-ai-native-software-development-lifecycle)

> this experience taught us to draw the boundary around access and actions, not around a model’s instructions or what we believe a model can do.
>
> [How Anthropic secures its AI-native software development lifecycle](https://claude.com/resources/articles/how-anthropic-secures-its-ai-native-software-development-lifecycle)

> When there's something that absolutely must not happen, an instruction is the wrong tool.
>
> [Steering Claude Code: when to use CLAUDE.md, skills, hooks, and subagents](https://claude.com/resources/articles/steering-claude-code-skills-hooks-rules-subagents-and-more)

> CI-like quality gates belong in the local development process
>
> [How and when to use subagents in Claude Code](https://claude.com/resources/articles/subagents-in-claude-code)

> When you have an existing project and you find yourself making the same small corrections every time Claude implements a new feature for you, it’s time to turn those steps into your own custom verification loop.
>
> [Building verification loops in Claude Code with skills](https://claude.com/resources/articles/building-verification-loops-in-claude-code-with-skills)

## Support

Established: 5 independent sources support this principle.

Expert: Anthropic engineering

Topics: agent-roles, deterministic-guardrails, processes

## Related principles

- [Anthropic engineering: Done means a check the agent can run](done-means-a-check-the-agent-can-run.md)
- [Anthropic engineering: Treat shared agent context as owned, pruned code](treat-shared-agent-context-as-owned-pruned-code.md)
