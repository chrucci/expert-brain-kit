# Conformance suites make agent-driven ports and rewrites viable

Verified: 7 verbatim quotes from 3 sources

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: For agent-driven ports, track conformance-suite pass rate, time, token cost, output differences found in a shadow run and incidents after cutover, comparing projects with and without strong suites.

An implementation-independent test suite, together with a trusted reference implementation and a shadow run on real traffic, lets agents port or rewrite large systems in hours. That makes full rewrites, which teams used to rule out, a real option that is worth weighing.

## Quotes

> Having an existing conformance testing suite of the quality of `test262` is a huge unlock for projects of this magnitude, and the ability to compare output with an existing trusted implementation makes agentic engineering much more of a safe bet.
>
> [Ladybird adopts Rust, with help from AI](https://simonwillison.net/2026/Feb/23/ladybird-adopts-rust/)

> A crucial enabling factor for the rewrite was that the Bun test suite was written in TypeScript, which meant it could act as [a conformance suite](https://simonwillison.net/tags/conformance-suites/).
>
> [Rewriting Bun in Rust](https://simonwillison.net/2026/Jul/8/rewriting-bun-in-rust/)

> This allowed an agent harness to automate much of the initial port from Bun to Rust
>
> [Rewriting Bun in Rust](https://simonwillison.net/2026/Jul/8/rewriting-bun-in-rust/)

> Everyone knows you should never stop the world and rewrite a large piece of software from the ground up.
>
> [Rewriting Bun in Rust](https://simonwillison.net/2026/Jul/8/rewriting-bun-in-rust/)

> Coding agents powered by today's frontier models change that equation.
>
> [Rewriting Bun in Rust](https://simonwillison.net/2026/Jul/8/rewriting-bun-in-rust/)

> As with other vibe-porting projects the key enabling factor was JSONata's existing test suite, which helped build the first working Go version in 7 hours and $400 of token spend.
>
> [We Rewrote JSONata with AI in a Day, Saved $500K/Year](https://simonwillison.net/2026/Mar/27/vine-porting-jsonata/)

> The Reco team then used a shadow deployment for a week to run the new and old versions in parallel to confirm the new implementation exactly matched the behavior of the old one.
>
> [We Rewrote JSONata with AI in a Day, Saved $500K/Year](https://simonwillison.net/2026/Mar/27/vine-porting-jsonata/)

## Support

Established: 3 independent sources support this principle.

Expert: Simon Willison

Topics: deterministic-guardrails, emerging, processes

## Related principles

- [Simon Willison: Automated tests are mandatory, and agents work test-first](automated-tests-are-mandatory-and-agents-work-test-first.md)
