# Quality gates buy test strength, not design

Verified: 7 verbatim quotes from 1 source

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: Regenerate the same feature several times under the gates and compare coverage, function count, reviewer-rated readability and structural differences the suite does not detect.

In Martin's repeated builds, a CRAP gate raised coverage but broke code into many tiny, less readable functions. Mutation passes after the fact added operator-level tests without changing the code, and every build passed the same acceptance suite despite very different internal structures. Teams should not read green gates on agent output as evidence of good design.

## Quotes

> CRAP buys coverage and spends cleanliness. It does not improve design.
>
> [negative-test-experiment/experiment-summary.md at main · unclebob/negative-test-experiment](https://github.com/unclebob/negative-test-experiment/blob/main/experiment-summary.md)

> Every CRAP-on row is a 1 or 2 for cleanliness.
>
> [negative-test-experiment/experiment-summary.md at main · unclebob/negative-test-experiment](https://github.com/unclebob/negative-test-experiment/blob/main/experiment-summary.md)

> CRAP raises coverage and wrecks cleanliness; it does not improve design.
>
> [negative-test-experiment/experiment-summary.md at main · unclebob/negative-test-experiment](https://github.com/unclebob/negative-test-experiment/blob/main/experiment-summary.md)

> Hazard check order, `--seed` implementation (`Random` vs two LCGs), and whether IO is injected all vary. Acceptance does not see any of that.
>
> [negative-test-experiment/experiment-summary.md at main · unclebob/negative-test-experiment](https://github.com/unclebob/negative-test-experiment/blob/main/experiment-summary.md)

> Same game, same acceptance script. Every run passed 25/25.
>
> [negative-test-experiment/experiment-summary.md at main · unclebob/negative-test-experiment](https://github.com/unclebob/negative-test-experiment/blob/main/experiment-summary.md)

> Mutation, given that program, writes **operator tests** — never a different Wumpus.
>
> [negative-test-experiment/experiment-summary.md at main · unclebob/negative-test-experiment](https://github.com/unclebob/negative-test-experiment/blob/main/experiment-summary.md)

> Leftovers were the mutator’s parent-line `1→0` no-op. The game did not change.
>
> [negative-test-experiment/experiment-summary.md at main · unclebob/negative-test-experiment](https://github.com/unclebob/negative-test-experiment/blob/main/experiment-summary.md)

## Support

Candidate: one source supports this principle so far.

Expert: Robert C. Martin

Topics: deterministic-guardrails, metrics

## Related principles

- [Robert C. Martin: Agree on shared deterministic gates and loosen thresholds only as agents improve](agree-on-shared-deterministic-gates-and-loosen-thresholds-only-as-agents-improve.md)
- [Robert C. Martin: Choose the test discipline deliberately](choose-the-test-discipline-deliberately.md)
- [Robert C. Martin: Prove acceptance tests are wired to the application](prove-acceptance-tests-are-wired-to-the-application.md)
