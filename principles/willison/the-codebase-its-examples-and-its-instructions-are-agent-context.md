# The codebase, its examples and its instructions are agent context

Verified: 8 verbatim quotes from 12 sources

Dimension: Techniques (techniques)

Evidence: experience

How to measure: Compare convention adherence, first-attempt success and recurrence of known mistakes for agent work in repos with clean patterns, example libraries and updated instructions against repos without them.

Agents copy the patterns they find, so clean code, tests in the house style, consistent conventions, git history and searchable working examples steer their output better than prose instructions do. Pointing agents at reference code works the same way. Teams should also feed lessons from each project back into agent instructions, and with frontier models those instructions can rely on the model's judgement rather than rigid rules.

## Quotes

> If you’ve got a codebase with a bunch of patterns in, they will follow those patterns almost to a tee.
>
> [My fireside chat about agentic engineering at the Pragmatic Summit](https://simonwillison.net/2026/Mar/14/pragmatic-summit/)

> the agent will consult enough of the existing examples to understand patterns, then iterate and test its own output to fill in the gaps.
>
> [Perhaps not Boring Technology after all](https://simonwillison.net/2026/Mar/9/not-so-boring/)

> Coding agents can clone code from GitHub, and the best way to explain a problem is often to have them look at relevant code.
>
> [Adding a new content type to my blog-to-newsletter tool](https://simonwillison.net/guides/agentic-engineering-patterns/adding-a-new-content-type/)

> Telling the agent to look at recent changes causes it to run `git log`, which can instantly load its context with details of what you have been working on recently - both the modified code and the commit messages that describe it.
>
> [Using Git with coding agents - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/using-git-with-coding-agents/)

> One of my favorite prompting patterns is to tell an agent to build something new by combining two or more existing working examples.
>
> [Hoard things you know how to do - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/hoard-things-you-know-how-to-do/)

> LLMs don't learn from their past mistakes, but coding agents can, provided we deliberately update our instructions and tool harnesses to account for what we learn along the way.
>
> [What is agentic engineering? - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/what-is-agentic-engineering/)

> Tests are also a great tool to help get an agent up to speed with an existing codebase.
>
> [First run the tests - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/first-run-the-tests/)

> Agents follow instructions. We can evolve these instructions over time to get better results from future runs, based on what we've learned previously.
>
> [AI should help us produce better code - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/better-code/)

## Support

Established: 12 independent sources support this principle.

Expert: Simon Willison

Topics: techniques

## Related principles

- [Simon Willison: Build tools agents can learn from their own help](build-tools-agents-can-learn-from-their-own-help.md)
- [Simon Willison: Plan in the repo, steer in flight, land small steps](plan-in-the-repo-steer-in-flight-land-small-steps.md)
