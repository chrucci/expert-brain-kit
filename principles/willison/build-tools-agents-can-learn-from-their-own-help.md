# Build tools agents can learn from their own help

Verified: 8 verbatim quotes from 7 sources

Dimension: Tools (tools)

Evidence: experience

How to measure: Measure how often agents use a tool or new library correctly on the first attempt when told only to read its --help, docs or skill.

Team tooling should be agent-first CLIs whose --help output teaches an agent everything it needs, much like a bundled skill. Combined with docs, official vendor skills and access to other vendors' APIs, this lets agents work with new or private technology, so the team can choose its stack on merit rather than by what the model was trained on.

## Quotes

> I really like this pattern where the `--help` output for a command provides enough detail that a coding agent can use it—it works kind of like bundling a `SKILL.md` file directly inside the tool.
>
> [Have your agent record video demos of its work with shot-scraper video](https://simonwillison.net/2026/Jun/30/shot-scraper-video/)

> but in practice they don’t seem to be affecting my technology choices in that way at all.
>
> [Perhaps not Boring Technology after all](https://simonwillison.net/2026/Mar/9/not-so-boring/)

> With the latest models running in good coding agent harnesses I’m not sure this continues to hold up.
>
> [Perhaps not Boring Technology after all](https://simonwillison.net/2026/Mar/9/not-so-boring/)

> Rodney is browser automation software that can be installed using `uvx`, and that has `--help` output designed to teach an agent everything it needs to know in order to use the tool.
>
> [Adding a new content type to my blog-to-newsletter tool](https://simonwillison.net/guides/agentic-engineering-patterns/adding-a-new-content-type/)

> which is designed to give the model everything it needs to know in order to use the tool.
>
> [Linear walkthroughs - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/linear-walkthroughs/)

> Coding agents work really well with dedicated CLIs.
>
> [Agentic manual testing - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/agentic-manual-testing/)

> Giving Claude access to an OpenAI key turns out to work really well for filling in gaps in its capabilities—in this case we needed some way to generate images to use as textures.
>
> [One-shotting a Raccoon Heist game using Claude Fable 5](https://simonwillison.net/2026/Aug/5/raccoon-heist/)

> As with Showboat, this tool is not designed to be used by humans! The goal is for coding agents to be able to run `rodney --help` and see everything they need to know to start using the tool.
>
> [Introducing Showboat and Rodney, so agents can demo what they’ve built](https://simonwillison.net/2026/Feb/10/showboat-and-rodney/)

## Support

Established: 7 independent sources support this principle.

Expert: Simon Willison

Topics: techniques, tools

## Related principles

- [Simon Willison: The codebase, its examples and its instructions are agent context](the-codebase-its-examples-and-its-instructions-are-agent-context.md)
