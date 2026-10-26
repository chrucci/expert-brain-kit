# Keep secrets out of agents' reach and out of their transcripts

Verified: 3 verbatim quotes from 2 sources

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: Count credentials readable inside agent environments, unaudited authenticated requests, and secrets caught by the scanner or leaked in shared transcripts.

Agents should reach authenticated services through a proxy that injects and audits credentials, so they never hold the secrets themselves, and agent transcripts should be scanned deterministically, including encoded forms, before they are shared. This limits damage from prompt injection and from leaked logs.

## Quotes

> I'm often paranoid that one of my API keys or similar secrets might inadvertently be revealed in the detailed log files.
>
> [scan-for-secrets 0.1](https://simonwillison.net/2026/Apr/5/scan-for-secrets-3/)

> It doesn't just scan for the literal secrets - it also scans for common encodings of those secrets e.g. backslash or JSON escaping
>
> [scan-for-secrets 0.1](https://simonwillison.net/2026/Apr/5/scan-for-secrets-3/)

> I really like that credential injection pattern, where Claude Code can access an API via a proxy and that proxy both audits the request and injects the relevant API key—so Claude can access authenticated endpoints without having access to the API credentials itself.
>
> [A Fireside Chat with Cat and Thariq from the Claude Code team](https://simonwillison.net/2026/Jul/21/cat-and-thariq/)

## Support

Established: 2 independent sources support this principle.

Expert: Simon Willison

Topics: deterministic-guardrails, tools
