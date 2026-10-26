# Coverage-driven generated tests are not a guardrail

Verified: 2 verbatim quotes from 1 source

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: opinion

How to measure: Compare mutation scores and escaped-defect rates of LLM-generated coverage tests against test-first tests written to define behaviour.

Tests that LLMs generate just to raise coverage add little value. Tests should define the intended behaviour and push the design toward structure that can handle future scenarios, so a passing test is the minimum bar, not proof that agent work is good.

## Quotes

> This is also why generating test cases with LLMs to improve “test coverage” is not something
> I find very useful.
>
> [Conversation: LLMs and the what/how loop](https://martinfowler.com/articles/convo-what-how.html)

> Passing the test, or making the code work for a scenario, is merely the baseline.
>
> [Conversation: LLMs and the what/how loop](https://martinfowler.com/articles/convo-what-how.html)

## Support

Candidate: one source supports this principle so far.

Expert: Unmesh Joshi

Topics: deterministic-guardrails, metrics

## Related principles

- [Unmesh Joshi: Discover domain vocabulary through TDD and expert collaboration](discover-domain-vocabulary-through-tdd-and-expert-collaboration.md)
