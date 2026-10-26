# Choose stacks and architecture for harnessability

Verified: 8 verbatim quotes from 2 sources

Dimension: Tools (tools)

Evidence: opinion

How to measure: Compare agent task success, rework and architectural-rule violations across codebases with and without strong typing, enforced module boundaries and structural tests.

AI-generated code that a team can trust at scale needs a constrained solution space: enforced architectural patterns, module boundaries, strong typing and structural tests. Greenfield teams should pick stacks and structures that are easy to harness, while legacy teams must weigh the cost of retrofitting a harness where it is hardest to build.

## Quotes

> But for maintainable, AI-generated code at scale that we can trust, something has to give.
>
> [Harness Engineering - first thoughts](https://martinfowler.com/articles/exploring-gen-ai/harness-engineering-memo.html)

> The harness described suggests that increasing trust and reliability required constraining the solution space: specific architectural patterns, enforced boundaries, standardized structures.
>
> [Harness Engineering - first thoughts](https://martinfowler.com/articles/exploring-gen-ai/harness-engineering-memo.html)

> Do you have ideas for custom linters? What architectural constraints would you like to impose on your codebase? Have you experimented with structural testing frameworks like ArchUnit?
>
> [Harness Engineering - first thoughts](https://martinfowler.com/articles/exploring-gen-ai/harness-engineering-memo.html)

> We might choose stacks with good harnesses available and prioritize “AI-friendliness”.
>
> [Harness Engineering - first thoughts](https://martinfowler.com/articles/exploring-gen-ai/harness-engineering-memo.html)

> We might default to structures that are easier to maintain with AI because they’re easier to harness.
>
> [Harness Engineering - first thoughts](https://martinfowler.com/articles/exploring-gen-ai/harness-engineering-memo.html)

> For older codebases, we’d need to consider whether retrofitting a harness is worth the effort.
>
> [Harness Engineering - first thoughts](https://martinfowler.com/articles/exploring-gen-ai/harness-engineering-memo.html)

> Greenfield teams can bake harnessability in from day one - technology decisions and architecture choices determine how governable the codebase will be.
>
> [Harness engineering for coding agent users](https://martinfowler.com/articles/harness-engineering.html)

> Legacy teams, especially with applications that have accrued a lot of technical debt, face the harder problem: the harness is most needed where it is hardest to build.
>
> [Harness engineering for coding agent users](https://martinfowler.com/articles/harness-engineering.html)

## Support

Established: 2 independent sources support this principle.

Expert: Birgitta Böckeler

Topics: deterministic-guardrails, tools

## Related principles

- [Birgitta Böckeler: Pair guides with fast, self-correcting sensors](pair-guides-with-fast-self-correcting-sensors.md)
- [Birgitta Böckeler: Share harness setups among people with similar contexts](share-harness-setups-among-people-with-similar-contexts.md)
