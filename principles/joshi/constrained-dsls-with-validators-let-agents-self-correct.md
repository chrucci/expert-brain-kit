# Constrained DSLs with validators let agents self-correct

Verified: 2 verbatim quotes from 1 source

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: Compare how often agents need human correction and how long reviews take for tasks done through a validated DSL versus the same tasks done in general-purpose code.

Give agents a small domain-specific language backed by a parser, schema or compiler. The agent can then generate, validate and repair its output without a human, and reviewers can read the results as statements of intent. This only pays off while the DSL stays small and someone funds its upkeep.

## Quotes

> The agent can generate a candidate, run it past the validator, and repair it from the error, all without a human in the loop.
>
> [DSLs Enable Reliable Use of LLMs](https://martinfowler.com/articles/llm-and-dsls.html)

> The payoff is therefore concentrated in well-factored, genuinely constrained DSLs backed by a validator.
>
> [DSLs Enable Reliable Use of LLMs](https://martinfowler.com/articles/llm-and-dsls.html)

## Support

Candidate: one source supports this principle so far.

Expert: Unmesh Joshi

Topics: agent-roles, deterministic-guardrails, techniques

## Related principles

- [Unmesh Joshi: The DSL artifact, not the prompt, is the source of truth](the-dsl-artifact-not-the-prompt-is-the-source-of-truth.md)
- [Unmesh Joshi: Humans own abstraction design; the LLM brainstorms, then becomes the interface](humans-own-abstraction-design-the-llm-brainstorms-then-becomes-the-interface.md)
