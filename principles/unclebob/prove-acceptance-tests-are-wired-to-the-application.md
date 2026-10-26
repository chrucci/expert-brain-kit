# Prove acceptance tests are wired to the application

Verified: 5 verbatim quotes from 1 source

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: opinion

How to measure: Track the acceptance-mutation kill rate per feature and how often mutation runs actually happen per feature change.

A passing acceptance suite is not enough, because agent-written step handlers can pass without really exercising the app. Mutate the specification's example values and confirm the tests fail. Run this as a separate, deliberate step alongside the fast routine acceptance run, and use an advisory duplicate checker to normalize drifting Gherkin wording without merging steps blindly.

## Quotes

> The normal run proves that the project satisfies the feature. The mutation run
> checks whether the acceptance tests fail when important example values change.
>
> [Acceptance-Pipeline-Specification: README.md](https://github.com/unclebob/Acceptance-Pipeline-Specification/blob/main/README.md)

> Runs `bb gherkin-mutator` and improves scenarios or handlers until
>    important mutations are killed.
>
> [Acceptance-Pipeline-Specification: README.md](https://github.com/unclebob/Acceptance-Pipeline-Specification/blob/main/README.md)

> Normal acceptance should be part of regular verification. Acceptance mutation is
> usually a deliberate quality workflow because it may be slower than normal test
> runs.
>
> [Acceptance-Pipeline-Specification: README.md](https://github.com/unclebob/Acceptance-Pipeline-Specification/blob/main/README.md)

> Its purpose is to
> help agents normalize and prune the Gherkin in feature files before generated
> tests are created.
>
> [Acceptance-Pipeline-Specification: README.md](https://github.com/unclebob/Acceptance-Pipeline-Specification/blob/main/README.md)

> Do not blindly merge steps only because they look similar. Some step texts have
> the same shape but different setup or assertion semantics.
>
> [Acceptance-Pipeline-Specification: README.md](https://github.com/unclebob/Acceptance-Pipeline-Specification/blob/main/README.md)

## Support

Candidate: one source supports this principle so far.

Expert: Robert C. Martin

Topics: deterministic-guardrails, processes, techniques

## Related principles

- [Robert C. Martin: Humans own the behavioural specification](humans-own-the-behavioural-specification.md)
- [Robert C. Martin: Quality gates buy test strength, not design](quality-gates-buy-test-strength-not-design.md)
