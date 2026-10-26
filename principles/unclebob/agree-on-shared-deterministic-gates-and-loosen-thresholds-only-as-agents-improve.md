# Agree on shared deterministic gates and loosen thresholds only as agents improve

Verified: 8 verbatim quotes from 3 sources

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: For each threshold setting, track escaped defects, how often agents break tests, and how often each gate catches a problem earlier stages missed. Relax a threshold only when these stay flat.

A team should agree up front on non-negotiable deterministic rules for agent work, such as unit and acceptance tests, high coverage, a CRAP ceiling, DRY checks, mutation testing and property tests. These rules go in a shared constitution that local configurations cannot quietly override. Agent output is accepted because it passes these checks, not because another model approves it, and Martin relaxes thresholds (CRAP 4 to 6 to 12) only as models get better.

## Quotes

> If you don't have agents write unit tests, so far as I have seen, they will go off into Wonderland.
>
> [Uncle Bob: Why I Stopped Reading Code and Building Harnesses | Aviator](https://www.aviator.co/podcast/uncle-bob-martin-ai-clean-code)

> I used to keep CRAP down to four. Then I thought that was probably too restrictive and backed it off to six. At this point I think 12 is probably okay.
>
> [Uncle Bob: Why I Stopped Reading Code and Building Harnesses | Aviator](https://www.aviator.co/podcast/uncle-bob-martin-ai-clean-code)

> The first thing any team needs is a set of disciplines: rules they all decide to follow until they have a meeting and decide they've got to break one.
>
> [Uncle Bob: Why I Stopped Reading Code and Building Harnesses | Aviator](https://www.aviator.co/podcast/uncle-bob-martin-ai-clean-code)

> The composer reserves the three shared names above for `main`, so a pack cannot silently replace common law.
>
> [swarm-forge: README.md](https://github.com/unclebob/swarm-forge/blob/main/README.md)

> Language defaults, testability, acceptance-pipeline tooling, verification, and quality-tool guardrails.
>
> [swarm-forge: README.md](https://github.com/unclebob/swarm-forge/blob/main/README.md)

> Requires non-specifier agents to verify unit and acceptance behavior and the final quality roles to run available property tests.
>
> [swarm-forge/README.md at six-pack · unclebob/swarm-forge](https://github.com/unclebob/swarm-forge/blob/six-pack/README.md)

> Owns language and Gherkin mutation hardening, CRAP and DRY gates, and robustness work.
>
> [swarm-forge/README.md at six-pack · unclebob/swarm-forge](https://github.com/unclebob/swarm-forge/blob/six-pack/README.md)

> Performs local behavior-preserving cleanup, coverage, CRAP and DRY analysis, and module-responsibility checks.
>
> [swarm-forge/README.md at six-pack · unclebob/swarm-forge](https://github.com/unclebob/swarm-forge/blob/six-pack/README.md)

## Support

Established: 3 independent sources support this principle.

Expert: Robert C. Martin

Topics: deterministic-guardrails, processes, techniques

## Related principles

- [Robert C. Martin: Quality gates buy test strength, not design](quality-gates-buy-test-strength-not-design.md)
- [Robert C. Martin: Choose the test discipline deliberately](choose-the-test-discipline-deliberately.md)
- [Robert C. Martin: Humans own the behavioural specification](humans-own-the-behavioural-specification.md)
