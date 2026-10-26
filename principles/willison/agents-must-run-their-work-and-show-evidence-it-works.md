# Agents must run their work and show evidence it works

Verified: 8 verbatim quotes from 13 sources

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: Count defects found by agent manual exercise after tests pass, and compare post-merge defects and review time for changes with and without execution-backed demo evidence.

Agents should be able to execute code and check their own changes, with a server, curl, a browser driver, a benchmark or a source of truth, because passing tests alone don't prove the software works. They should also hand reviewers artifacts made from real execution, such as demo documents, recordings, live previews and PR testing notes, so humans see what the change does without having to trust the agent's claims.

## Quotes

> allowing them to test that code and iterate on it independently of turn-by-turn guidance from their human supervisor.
>
> [Writing about Agentic Engineering Patterns](https://simonwillison.net/2026/Feb/23/agentic-engineering-patterns/)

> I’ve written before about the importance of [having coding agents produce demos](https://simonwillison.net/2026/Feb/10/showboat-and-rodney/#proving-code-actually-works) of their work; this is my latest attempt at enabling them to do that.
>
> [Have your agent record video demos of its work with shot-scraper video](https://simonwillison.net/2026/Jun/30/shot-scraper-video/)

> If you provide an agent with a benchmarking script "make it faster" becomes an actionable goal.
>
> [Shopify/liquid: Performance: 53% faster parse+render, 61% fewer allocations](https://simonwillison.net/2026/Mar/13/liquid/)

> So I will tell my agents, start the server running in the background and then use curl to exercise the API that you just created. And that works, and often that will find new bugs that the test didn’t cover.
>
> [My fireside chat about agentic engineering at the Pragmatic Summit](https://simonwillison.net/2026/Mar/14/pragmatic-summit/)

> Coding agents always work best if they have some kind of validation mechanism they can use to test their own work.
>
> [Adding a new content type to my blog-to-newsletter tool](https://simonwillison.net/guides/agentic-engineering-patterns/adding-a-new-content-type/)

> Code execution is the defining capability that makes agentic engineering possible. Without the ability to directly run the code, anything output by an LLM is of limited value.
>
> [What is agentic engineering? - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/what-is-agentic-engineering/)

> By telling it to use "sed or grep or cat or whatever you need to include snippets of code you are talking about" I ensured that Claude Code would not manually copy snippets of code into the document, since that could introduce a risk of hallucinations or mistakes.
>
> [Linear walkthroughs - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/linear-walkthroughs/)

> I recommend including some form of evidence that you've put that extra work in yourself.
>
> [Anti-patterns: things to avoid - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/anti-patterns/)

## Support

Established: 13 independent sources support this principle.

Expert: Simon Willison

Topics: agent-roles, deterministic-guardrails, processes

## Related principles

- [Simon Willison: Automated tests are mandatory, and agents work test-first](automated-tests-are-mandatory-and-agents-work-test-first.md)
- [Simon Willison: A human vouches for agent output before others depend on it](a-human-vouches-for-agent-output-before-others-depend-on-it.md)
