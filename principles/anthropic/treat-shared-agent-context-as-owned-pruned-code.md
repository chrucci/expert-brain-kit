# Treat shared agent context as owned, pruned code

Verified: 8 verbatim quotes from 7 sources

Dimension: Techniques (techniques)

Evidence: measurement

How to measure: Track instruction-file size, repeat rates of known failure classes and eval scores before and after pruning or upgrading models.

CLAUDE.md files and skills are team artifacts: check them in, give them an owner, review changes like code, and keep them lean with specialised procedures loaded only when needed. Grow them from observed agent failures and discovered bug classes, measure which skills actually trigger, and after each model upgrade strip workarounds and harness components that no longer earn their place, confirming with evals that nothing got worse.

## Quotes

> If your prompts carry workarounds such as refusal steering, tool-call retry shims, or "do not be lazy," remove them and re-run your evals before tuning anything else.
>
> [Building with Claude Sonnet 5.5](https://claude.dev/blog/building-with-claude-sonnet-5-5/)

> The highest-signal content in any skill is the Gotchas section. These sections should be built up from common failure points that Claude runs into when using your skill.
>
> [Lessons from building Claude Code: How we use skills](https://claude.dev/blog/lessons-from-building-claude-code-how-we-use-skills/)

> Most of our best skills began as a few lines and a single gotcha, then got better because people kept adding to them as Claude hit new edge cases.
>
> [Lessons from building Claude Code: How we use skills](https://claude.dev/blog/lessons-from-building-claude-code-how-we-use-skills/)

> We removed over 80% of Claude Code’s system prompt for models like Claude Opus 5 and Claude Fable 5 with no measurable loss on our coding evaluations.
>
> [The new rules of context engineering for Claude 5 generation models](https://claude.dev/blog/the-new-rules-of-context-engineering-for-claude-5-generation-models/)

> Treat CLAUDE.md like code: review it when things go wrong, prune it regularly, and test changes by observing whether Claude’s behavior actually shifts.
>
> [Best practices for Claude Code - Claude Code Docs](https://www.anthropic.com/engineering/claude-code-best-practices)

> every component in a harness encodes an assumption about what the model can't do on its own, and those assumptions are worth stress testing, both because they may be incorrect, and because they can quickly go stale as models improve.
>
> [Harness design for long-running application development](https://www.anthropic.com/engineering/harness-design-long-running-apps)

> This is done as part of a closed loop. Once an agent discovers a bug class, the relevant file is updated to prevent it recurring in future code.
>
> [How Anthropic secures its AI-native software development lifecycle](https://claude.com/resources/articles/how-anthropic-secures-its-ai-native-software-development-lifecycle)

> In a shared repository, CLAUDE.md grows the way any unowned config file does: every team appends its own instructions and nothing gets deleted.
>
> [Steering Claude Code: when to use CLAUDE.md, skills, hooks, and subagents](https://claude.com/resources/articles/steering-claude-code-skills-hooks-rules-subagents-and-more)

## Support

Established: 7 independent sources support this principle.

Expert: Anthropic engineering

Topics: processes, techniques, tools

## Related principles

- [Anthropic engineering: Move rules out of prompts and into deterministic gates](move-rules-out-of-prompts-and-into-deterministic-gates.md)
