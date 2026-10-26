# Preserve the intent and decisions behind agent code

Verified: 7 verbatim quotes from 4 sources

Dimension: Processes (processes)

Evidence: opinion

How to measure: Track the share of agent-authored PRs linked to a prompt, spec or decision log, and compare review and debugging time with and without one.

The prompt and conversation that produced a change often carry more information than the diff, and that intent is lost when only code is committed. Keep prompts, specs and agent decision logs alongside the code so reviewers and maintainers can understand the important choices.

## Quotes

> I find that the prompt and conversation with the agent carries more information than the PR itself, at least for me.
>
> [Building Codex with Tibo Sottiaux at 00:28:36](https://newsletter.pragmaticengineer.com/p/building-codex-with-tibo-sottiaux?t=1716s)

> AI makes it easier than ever to build software, but it also makes it easier than ever to lose understanding of the software that we're building.
>
> [From Chrome DevTools to AI Engineering, with Addy Osmani at 01:30:11](https://newsletter.pragmaticengineer.com/p/from-chrome-devtools-to-ai-engineering?t=5411s)

> So have the agents record decisions, document what it learned and explain unusual choices. It's just no longer feasible to understand how or why every single token was generated, but you want to keep understanding the important decisions that any of your agents make.
>
> [From Chrome DevTools to AI Engineering, with Addy Osmani at 01:30:11](https://newsletter.pragmaticengineer.com/p/from-chrome-devtools-to-ai-engineering?t=5411s)

> I do think we might have to rethink the importance of prompts or at the very least sharing of prompts in software development,
>
> [The creator of Clawd: "I ship code I don't read" at 01:52:18](https://newsletter.pragmaticengineer.com/p/the-creator-of-clawd-i-ship-code?t=6738s)

> But that conversation, your actual intent, it disappears.
>
> [The programming language after Kotlin – with the creator of Kotlin at 01:43:20](https://newsletter.pragmaticengineer.com/p/the-programming-language-after-kotlin?t=6200s)

> You communicate with the machine in human language, but with your teammates in code in machine language.
>
> [The programming language after Kotlin – with the creator of Kotlin at 01:43:20](https://newsletter.pragmaticengineer.com/p/the-programming-language-after-kotlin?t=6200s)

> Whether or not Codespeak becomes the answer, what is sure that we're missing an intent layer
>
> [The programming language after Kotlin – with the creator of Kotlin at 01:43:20](https://newsletter.pragmaticengineer.com/p/the-programming-language-after-kotlin?t=6200s)

## Support

Established: 4 independent sources support this principle.

Expert: Gergely Orosz

Topics: processes, techniques

## Related principles

- [Gergely Orosz: Settle intent and design before agents build](settle-intent-and-design-before-agents-build.md)
