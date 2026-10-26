# Well-designed code is the primary harness

Verified: 4 verbatim quotes from 2 sources

Dimension: Techniques (techniques)

Evidence: experience

How to measure: Compare how often agent changes are accepted and how much rework they need in modules with clean, consistent abstractions (and prompts phrased in them) versus poorly structured modules, across more than one model.

A codebase with stable abstractions, clear semantics and a consistent domain vocabulary, together with its tests, is the most important context an agent gets. Investing in the code itself makes agent output reliable whichever model or prompt is used.

## Quotes

> Because abstractions form the essential
> vocabulary for the prompts, the generated program is more predictable and easier to review.
>
> [Conversation: LLMs and the what/how loop](https://martinfowler.com/articles/convo-what-how.html)

> Without a stable vocabulary of abstractions,
> LLM-generated code tends to be procedural.
>
> [Conversation: LLMs and the what/how loop](https://martinfowler.com/articles/convo-what-how.html)

> A well structured code with abstractions forming a well defined vocabulary itself acts as the most important part of the harness and context. I have repeatedly seen good success with well designed code working very well with the LLMs.
>
> [What Is Code?](https://martinfowler.com/articles/what-is-code.html)

> More importantly, when the code is built with stable abstractions with clear semantics, you get some freedom to choose whatever LLM model you use and do not need to worry much about how accurate your prompts are.
>
> [What Is Code?](https://martinfowler.com/articles/what-is-code.html)

## Support

Established: 2 independent sources support this principle.

Expert: Unmesh Joshi

Topics: deterministic-guardrails, techniques, tools

## Related principles

- [Unmesh Joshi: Discover domain vocabulary through TDD and expert collaboration](discover-domain-vocabulary-through-tdd-and-expert-collaboration.md)
- [Unmesh Joshi: Constrained DSLs with validators let agents self-correct](constrained-dsls-with-validators-let-agents-self-correct.md)
