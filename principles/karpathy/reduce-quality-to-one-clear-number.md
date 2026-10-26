# Reduce quality to one clear number

Verified: 3 verbatim quotes from 1 source

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: Check that every accepted improvement, human or agent, is backed by a reproducible reference-script run that moves the leaderboard metric.

Judge every change, whether from a human or an agent-driven research loop, against a single objective metric such as time to GPT-2 on a public leaderboard, and require it to hold across the whole range of model sizes. Changes are then accepted on measured results rather than opinion.

## Quotes

> The primary metric we care about is "time to GPT-2" - the wall clock time needed to outperform the GPT-2 (1.6B) CORE metric on an 8XH100 GPU node.
>
> [nanochat: README.md](https://github.com/karpathy/nanochat/blob/master/README.md)

> Inspired by the modded-nanogpt repo and to incentivise progress and community collaboration, nanochat maintains a leaderboard for a "GPT-2 speedrun"
>
> [nanochat: README.md](https://github.com/karpathy/nanochat/blob/master/README.md)

> nanochat is also inspired by [modded-nanoGPT](https://github.com/KellerJordan/modded-nanogpt), which gamified the nanoGPT repo with clear metrics and a leaderboard
>
> [nanochat: README.md](https://github.com/karpathy/nanochat/blob/master/README.md)

## Support

Candidate: one source supports this principle so far.

Expert: Andrej Karpathy

Topics: deterministic-guardrails, metrics

## Related principles

- [Andrej Karpathy: Gate agent rewrites with tests and a trusted reference](gate-agent-rewrites-with-tests-and-a-trusted-reference.md)
