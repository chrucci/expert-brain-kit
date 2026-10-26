# Pair guides with fast, self-correcting sensors

Verified: 6 verbatim quotes from 2 sources

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: Measure the share of agent defects caught by pre-commit computational checks versus later review, and how often the agent suppresses rules with custom guidance versus default messages.

Agents need guides that steer them before they act and sensors that let them correct themselves afterwards. Run cheap computational checks on every change, early in the path to production, and write lint messages that tell the agent how to fix the problem. Any exceptions the agent makes should stay visible, so reviewers know where to start.

## Quotes

> Separately, you get either an agent that keeps repeating the same mistakes (feedback-only) or an agent that encodes rules but never finds out whether they worked (feed-forward-only).
>
> [Harness engineering for coding agent users](https://martinfowler.com/articles/harness-engineering.html)

> Computational sensors are cheap and fast enough to run on every change, alongside the agent.
>
> [Harness engineering for coding agent users](https://martinfowler.com/articles/harness-engineering.html)

> You want to have checks as far left in the path to production as possible, since the earlier you find issues, the cheaper they are to fix.
>
> [Harness engineering for coding agent users](https://martinfowler.com/articles/harness-engineering.html)

> In the guidance text above, the agent is told to make a judgment call, and allowed to suppress a warning in the code. This keeps the suppressions manageable, visible and reviewable.
>
> [Maintainability sensors for coding agents](https://martinfowler.com/articles/sensors-for-coding-agents.html)

> Looking at the exceptions AI created (suppressed warnings, increased thresholds) was a good point to start my code review.
>
> [Maintainability sensors for coding agents](https://martinfowler.com/articles/sensors-for-coding-agents.html)

> This is an indicator that the custom lint messages can indeed make quite a difference.
>
> [Maintainability sensors for coding agents](https://martinfowler.com/articles/sensors-for-coding-agents.html)

## Support

Established: 2 independent sources support this principle.

Expert: Birgitta Böckeler

Topics: deterministic-guardrails, processes, techniques

## Related principles

- [Birgitta Böckeler: Humans steer by improving the harness](humans-steer-by-improving-the-harness.md)
- [Birgitta Böckeler: Measure the harness and agent setup with data](measure-the-harness-and-agent-setup-with-data.md)
- [Birgitta Böckeler: Agent-written tests are not proof of correctness](agent-written-tests-are-not-proof-of-correctness.md)
