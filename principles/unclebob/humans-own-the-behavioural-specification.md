# Humans own the behavioural specification

Verified: 4 verbatim quotes from 2 sources

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: Count defects caught by the human-approved Gherkin suite that agent-written unit tests missed, and how many specs are revised at the approval gate.

Agents can write tests that pass while misunderstanding the task. So humans write, or at least review and approve, behavioural specs in Gherkin before any implementation starts, and agents build the tooling that runs those specs as a second test suite tied to human intent. Human approval is concentrated on what gets built, not on how.

## Quotes

> If you've got a fairly elaborate system that requires a lot of behavioral specification, it is wise to have humans produce that, and I like Gherkin, the old behavior-driven development language, for it.
>
> [Uncle Bob: Why I Stopped Reading Code and Building Harnesses | Aviator](https://www.aviator.co/podcast/uncle-bob-martin-ai-clean-code)

> I've had my agents build Gherkin interpretation tools that parse and execute the Gherkin, so you have a second set of tests that are authored, or at least reviewed, by humans.
>
> [Uncle Bob: Why I Stopped Reading Code and Building Harnesses | Aviator](https://www.aviator.co/podcast/uncle-bob-martin-ai-clean-code)

> New Task → specifier → approval → coder → cleaner → architect → hardender → QA → Done
>
> [swarm-forge/README.md at six-pack · unclebob/swarm-forge](https://github.com/unclebob/swarm-forge/blob/six-pack/README.md)

> Writes deterministic Gherkin plus headed end-to-end QA procedures and submits them for dashboard approval.
>
> [swarm-forge/README.md at six-pack · unclebob/swarm-forge](https://github.com/unclebob/swarm-forge/blob/six-pack/README.md)

## Support

Established: 2 independent sources support this principle.

Expert: Robert C. Martin

Topics: deterministic-guardrails, human-roles, processes

## Related principles

- [Robert C. Martin: Prove acceptance tests are wired to the application](prove-acceptance-tests-are-wired-to-the-application.md)
- [Robert C. Martin: Humans are responsible just above the code level](humans-are-responsible-just-above-the-code-level.md)
- [Robert C. Martin: Agents escalate ambiguity to a human operator](agents-escalate-ambiguity-to-a-human-operator.md)
