# Use deterministic gates to finish agent work

Verified: 1 verbatim quote from 1 source

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: measurement

How to measure: For agent-authored PRs, track the share that pass linting and include the required tests and docs on first submission, compared with human PRs.

Autonomous agents often get core functionality right but leave out documentation, tests and lint or style compliance. Automated lint, test and documentation checks are what decide whether agent work is actually complete.

## Quotes

> fully autonomous AI agents using Claude 3.7 Sonnet can often correctly implement the core functionality of issues on several repositories that are included in our study, although they fail to fully satisfy all requirements (typically leaving out important documentation, failing linting/styling rules, and leaving out key unit or integration tests).
>
> [Measuring the Impact of Early-2025 AI on Experienced Open-Source Developer Productivity at p.12](https://arxiv.org/pdf/2507.09089#page=12)

## Support

Candidate: one source supports this principle so far.

Expert: METR

Topics: agent-roles, deterministic-guardrails

## Related principles

- [METR: Tacit knowledge and implicit standards limit AI in mature codebases](tacit-knowledge-and-implicit-standards-limit-ai-in-mature-codebases.md)
