# Gate agent rewrites with tests and a trusted reference

Verified: 1 verbatim quote from 1 source

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: Track defect escape rate for agent-written code in unfamiliar languages with and without a reference implementation and test suite.

Keep a simple implementation you fully understand plus a test suite, and require agent-assisted ports or optimized rewrites to match it step for step. Deterministic parity checks make agent help trustworthy even in unfamiliar languages, without relying on review alone.

## Quotes

> But I had a Python implementation that I fully understand, and I’m just making sure I’m making a more efficient version of it, and I have tests so I feel safer doing that stuff.
>
> [Andrej Karpathy — AGI is still a decade away](https://www.dwarkesh.com/p/andrej-karpathy)

## Support

Candidate: one source supports this principle so far.

Expert: Andrej Karpathy

Topics: agent-roles, deterministic-guardrails

## Related principles

- [Andrej Karpathy: Reduce quality to one clear number](reduce-quality-to-one-clear-number.md)
- [Andrej Karpathy: Keep agent changes small so verification stays fast](keep-agent-changes-small-so-verification-stays-fast.md)
