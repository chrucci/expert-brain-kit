# Give agents a drivable interface and feature map of the system

Verified: 2 verbatim quotes from 1 source

Dimension: Techniques (techniques)

Evidence: experience

How to measure: Track the share of agent-authored PRs tested end to end through the agent-drivable CLI before opening, and compare their post-merge defect rate with that of other PRs.

Generate a command-line interface and a feature map so each agent can start its own copy of the application, move through it, inspect state and read back structured JSON. This lets the agent test a change end to end without a human, which makes self-verification practical.

## Quotes

> The verification skill she describes generates a command line interface (CLI) and a feature map for the application.
>
> [One engineer shipped 2,000 PRs a month to production. Verification is the key.](https://thenewstack.io/agentic-verification-distributed-systems/)

> The CLI lets an agent start the app, navigate it, inspect state, and read structured JSON results back. Each agent gets a complete copy of the application and can test a change end to end.
>
> [One engineer shipped 2,000 PRs a month to production. Verification is the key.](https://thenewstack.io/agentic-verification-distributed-systems/)

## Support

Candidate: one source supports this principle so far.

Expert: Lauren Tan

Topics: agent-count, deterministic-guardrails, techniques, tools

## Related principles

- [Lauren Tan: Agents verify their own work so humans stop being the bottleneck](agents-verify-their-own-work-so-humans-stop-being-the-bottleneck.md)
