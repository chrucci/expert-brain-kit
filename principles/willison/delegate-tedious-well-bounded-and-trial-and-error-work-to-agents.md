# Delegate tedious, well-bounded and trial-and-error work to agents

Verified: 8 verbatim quotes from 7 sources

Dimension: Roles for agents (agent-roles)

Evidence: measurement

How to measure: Track completion rate, elapsed time and landing rate for such tasks given to agents, along with benchmark gains per autoresearch run and the trend in known code smells.

Agents excel at work humans put off: long refactors, toolchain trial and error, merge conflicts, commit messages and release notes, research spikes that return code and a report, and autoresearch loops that test candidate improvements one at a time. Each result is gated by tests and human review, and because this work is now cheap, teams can stop tolerating small code smells.

## Quotes

> That's exactly the kind of tedious work that coding agents excel at!
>
> [Eight years of wanting, three months of building with AI](https://simonwillison.net/2026/Apr/5/building-with-ai/)

> Release notes are a great example of writing that I’m OK to outsource to agents because they need to be boring, predictable and accurate.
>
> [sqlite-utils 4.0rc2, mostly written by Claude Fable (for about $149.25)](https://simonwillison.net/2026/Jul/5/sqlite-utils-fable/)

> I had Fable add these to an “Unreleased” section of the changelog as each change landed, reviewing them as it went.
>
> [sqlite-utils 4.0rc2, mostly written by Claude Fable (for about $149.25)](https://simonwillison.net/2026/Jul/5/sqlite-utils-fable/)

> The autoresearch pattern - where an agent brainstorms a multitude of potential improvements and then experiments with them one at a time - is really effective.
>
> [Shopify/liquid: Performance: 53% faster parse+render, 61% fewer allocations](https://simonwillison.net/2026/Mar/13/liquid/)

> Coding agents can navigate the most Byzantine of merge conflicts, reasoning through the intent of the new code and figuring out what to keep and how to combine conflicting changes.
>
> [Using Git with coding agents - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/using-git-with-coding-agents/)

> larger, more complex examples where I’ve challenged a coding agent to research a problem and come back with working code and a written report detailing what it found out.
>
> [Hoard things you know how to do - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/hoard-things-you-know-how-to-do/)

> Refactoring tasks like this are an *ideal* application of coding agents.
>
> [AI should help us produce better code - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/better-code/)

> Coding agents are fantastic at trial and error! They can often brute force their way to a solution where I would have given up after the fifth inscrutable compiler error.
>
> [GIF optimization tool using WebAssembly and Gifsicle - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/gif-optimization/)

## Support

Established: 7 independent sources support this principle.

Expert: Simon Willison

Topics: agent-roles

## Related principles

- [Simon Willison: Cheap code moves the bottleneck to validation](cheap-code-moves-the-bottleneck-to-validation.md)
