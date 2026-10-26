# Measure verified outcomes with noise-aware evals

Verified: 8 verbatim quotes from 5 sources

Dimension: Metrics (metrics)

Evidence: measurement

How to measure: Report verified versus perceived success, cost per real task, PR cycle time by stage, and for each merged eval-driven change whether its gain held on held-out data and exceeded the confidence interval.

Count success only when hard signals back it, such as matching commits, passing tests or the real outcome you care about, not throughput, impressions or price per token. Give agents deterministic benchmarks to climb that also ratchet in CI, and discard flaky ones. Gate agent changes on held-out splits and refuse to act on gains within measurement noise.

## Quotes

> This one's interesting to dig into because it might help you identify where your pipeline is struggling to scale. As we’re generating so much more code, sometimes build systems and continuous integration (CI) may struggle to keep up.
>
> [Running an AI-native engineering org](https://claude.com/resources/articles/running-an-ai-native-engineering-org)

> On the third bullet, don't confuse throughput with success. Throughput is one metric, but the real metric is measuring the thing you're trying to solve.
>
> [Running an AI-native engineering org](https://claude.com/resources/articles/running-an-ai-native-engineering-org)

> In particular, it looks for git activity like commits and pull requests matching the work, as well as test suites passing, and explicit affirmation from the user.
>
> [How Claude Code is used in practice](https://www.anthropic.com/research/claude-code-expertise)

> A novice-rated session reaches our strictest measure, *verified success,* 15% of the time and at least partial success 77% of the time.
>
> [How Claude Code is used in practice](https://www.anthropic.com/research/claude-code-expertise)

> At this point, Claude applies a check: if the `train` set improves but the `test` set is flat, Claude suspects overfitting and reverts the patch.
>
> [Automating eval design and hillclimbing with Claude](https://claude.dev/blog/automating-eval-design-and-hillclimbing/)

> These harness additions improve your evaluation score, but don’t translate to improvements in production (Figure 5).
>
> [Automating eval design and hillclimbing with Claude](https://claude.dev/blog/automating-eval-design-and-hillclimbing/)

> Each one had two jobs: first, a metric Claude could move in the lab; second, a guardrail in CI with a number that could only ratchet down.
>
> [How we made claude.ai 3x faster in two weeks](https://claude.dev/blog/how-we-made-claude-ai-faster/)

> Two models with the same cost per token can cost very different amounts on the same task.
>
> [What a task costs on Opus 5.5](https://claude.dev/blog/what-a-task-costs-on-opus-5-5/)

## Support

Established: 5 independent sources support this principle.

Expert: Anthropic engineering

Topics: deterministic-guardrails, metrics

## Related principles

- [Anthropic engineering: Done means a check the agent can run](done-means-a-check-the-agent-can-run.md)
- [Anthropic engineering: Match model and effort to scope, checkability and supervision](match-model-and-effort-to-scope-checkability-and-supervision.md)
