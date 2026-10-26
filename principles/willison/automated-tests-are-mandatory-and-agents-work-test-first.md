# Automated tests are mandatory, and agents work test-first

Verified: 8 verbatim quotes from 14 sources

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: Compare defect, revert and rework rates, and prompts per accepted change, for agent tasks run test-first against tasks run without tests written first.

Agents make tests nearly free to write, so every agent session should start by running the suite and then build with red/green TDD, confirming that new tests fail before writing the code that makes them pass. The tests are the deterministic check that agent code works and that agents don't add code nobody needs, and every fix becomes a permanent regression check.

## Quotes

> When you implement this use playwright and red/green TDD, plan that too
>
> [Extract PDF text in your browser with LiteParse for the web](https://simonwillison.net/2026/Apr/23/liteparse-for-the-web/)

> and told it to build the actual tool (using [red/green TDD](https://simonwillison.net/guides/agentic-engineering-patterns/red-green-tdd/), naturally.)
>
> [scan-for-secrets 0.1](https://simonwillison.net/2026/Apr/5/scan-for-secrets-3/)

> describes how test-first development helps agents write more succinct and reliable code with minimal extra prompting.
>
> [Writing about Agentic Engineering Patterns](https://simonwillison.net/2026/Feb/23/agentic-engineering-patterns/)

> The YAML format itself was mostly defined by the coding agent. I had it [use Pydantic](https://github.com/simonw/shot-scraper/blob/1.10/shot_scraper/video.py#L24) to both define and validate the format, partly to make the design easier to review.
>
> [Have your agent record video demos of its work with shot-scraper video](https://simonwillison.net/2026/Jun/30/shot-scraper-video/)

> Having a robust test suite - in this case 974 unit tests - is a *massive unlock* for working with coding agents.
>
> [Shopify/liquid: Performance: 53% faster parse+render, 61% fewer allocations](https://simonwillison.net/2026/Mar/13/liquid/)

> So I say run the test and then I say use red-green TDD and give it its instruction.
>
> [My fireside chat about agentic engineering at the Pragmatic Summit](https://simonwillison.net/2026/Mar/14/pragmatic-summit/)

> A significant risk with coding agents is that they might write code that doesn't work, or build code that is unnecessary and never gets used, or both.
>
> [Red/green TDD - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/red-green-tdd/)

> Automated tests are no longer optional when working with coding agents.
>
> [First run the tests - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/first-run-the-tests/)

## Support

Established: 14 independent sources support this principle.

Expert: Simon Willison

Topics: deterministic-guardrails, techniques

## Related principles

- [Simon Willison: Agents must run their work and show evidence it works](agents-must-run-their-work-and-show-evidence-it-works.md)
- [Simon Willison: Conformance suites make agent-driven ports and rewrites viable](conformance-suites-make-agent-driven-ports-and-rewrites-viable.md)
