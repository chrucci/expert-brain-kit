# Make expectations explicit and let the agent observe real behaviour

Verified: 6 verbatim quotes from 3 sources

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: Track the share of contract clauses and performance or error-rate expectations covered by machine-checkable tests or thresholds, and regressions caught before release.

Agents do what you say, not what you mean, and pass/fail tests miss system qualities like performance and error rates. Spell out contracts, hard constraints and quality expectations in checkable form, with tests for every contract clause and telemetry for runtime behaviour, so the agent can use them as a feedback loop.

## Quotes

> Exactly what she told it. Not at all what she wanted. Anyone working with agents today knows the feeling.
>
> [How Do You Know That?](https://newsletter.kentbeck.com/p/how-do-you-know-that)

> I have a fuzz tester. I have run mutation testing on this. I'm pretty confident and I just I haven't seen a test breakage in quite a while.
>
> [Genie Sessions: Run, Right, and Fast for the Adaptive Radix Tree at 00:07:21](https://newsletter.kentbeck.com/p/run-right-and-fast-for-the-adaptive?t=441s)

> Oh, that's interesting that I was my, my total and absolute confidence was misplaced.
>
> [Genie Sessions: Run, Right, and Fast for the Adaptive Radix Tree at 00:23:40](https://newsletter.kentbeck.com/p/run-right-and-fast-for-the-adaptive?t=1420s)

> Specify the contracts. Single sources of truth for every public methods. Pre, post, misuse, edge cases, backfill tests until every contract clause is covered.
>
> [Genie Sessions: Run, Right, and Fast for the Adaptive Radix Tree at 00:31:22](https://newsletter.kentbeck.com/p/run-right-and-fast-for-the-adaptive?t=1882s)

> We need to learn how to be explicit about those expectations in a way that models can then check and use those as a feedback loop.
>
> [O11ycast | Ep. #80, Augmented Coding with Kent Beck | Heavybit](https://www.heavybit.com/library/podcasts/o11ycast/ep-80-augmented-coding-with-kent-beck)

> putting it under simulated load, letting the agent observe its actual behavior, and then tune the parameters from there is way better than me trying to memorize
>
> [O11ycast | Ep. #80, Augmented Coding with Kent Beck | Heavybit](https://www.heavybit.com/library/podcasts/o11ycast/ep-80-augmented-coding-with-kent-beck)

## Support

Established: 3 independent sources support this principle.

Expert: Kent Beck

Topics: deterministic-guardrails, techniques

## Related principles

- [Kent Beck: Rein in the agent with small, test-gated steps](rein-in-the-agent-with-small-test-gated-steps.md)
- [Kent Beck: Personas shape style; explicit constraints shape architecture](personas-shape-style-explicit-constraints-shape-architecture.md)
