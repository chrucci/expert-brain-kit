# Enforce agent work with deterministic sensors in the loop

Verified: 8 verbatim quotes from 38 sources

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: Track the share of agent defects caught by in-loop deterministic checks versus at human review or in production, and the share of must-hold rules enforced by an automated gate rather than prompt text.

Rules that must hold need deterministic checks, not prompts. Wire compilers, linters, tests, scanners and acceptance tests into the agent loop so failures force the agent to self-correct before a human reviews, and start from an honest test baseline that fails when it should. Humans can then step back from line-by-line checking without losing quality control.

## Quotes

> Agents produce better code when they can gauge the quality of the code they produce themselves rather than relying on us to check it for them.
>
> [Humans and Agents in Software Engineering Loops](https://martinfowler.com/articles/exploring-gen-ai/humans-and-agents.html)

> I now had concrete proof that the code was fully functional in its native environment, meaning any failures from this point forward would be the direct result of our active modernization efforts, not pre-existing rot.
>
> [The Archaeologist’s Copilot](https://martinfowler.com/articles/archaeologist-copilot.html)

> Functional testing alone is insufficient for robust validation; it acts primarily as an auxiliary check and is not factored into code coverage metrics. The final sign-off on core logic requires comprehensive unit tests.
>
> [Structured-Prompt-Driven Development (SPDD)](https://martinfowler.com/articles/structured-prompt-driven/)

> telling an AI agent to be safe is not the same as enforcing that it is safe. Prompts can be overridden, misunderstood, or ignored.
>
> [The VibeSec Reckoning](https://martinfowler.com/articles/vibesec-reckoning.html)

> Our quality assurance had to evolve to design tests that challenge the agent’s reasoning with ambiguous requests and unexpected tool errors, ensuring it can handle real-world uncertainty, not just ideal scenarios.
>
> [Beyond the hype: A real-world guide to building enterprise-grade AI agents](https://www.thoughtworks.com/insights/articles/a-real-world-guide-to-building-enterprise-grade-ai-agents)

> At present, even with large context sizes, models and agents alone cannot ingest tens of millions of lines of code simultaneously and reliably enough to draw a modernization roadmap.
>
> [Claude Code and COBOL modernization: What’s the reality?](https://www.thoughtworks.com/insights/articles/claude-code-cobol-modernization-reality)

> The important point here is that guides and sensors must be designed together. A guide that tells an agent to follow a rule, paired with a sensor that never checks the rule, isn’t a control system — it’s theater.
>
> [The operating system for enterprise AI](https://www.thoughtworks.com/insights/articles/operating-system-enterprise-ai)

> As AI generates more change than people can realistically review manually, traditional code review alone cannot provide the necessary control.
>
> [Path to AI-first organization](https://www.thoughtworks.com/insights/articles/path-to-ai-first-organization)

## Support

Established: 38 independent sources support this principle.

Expert: Thoughtworks

Topics: deterministic-guardrails, processes, techniques

## Related principles

- [Thoughtworks: Encode intent and standards in versioned artifacts](encode-intent-and-standards-in-versioned-artifacts.md)
- [Thoughtworks: Verification is the bottleneck; spend human review by risk](verification-is-the-bottleneck-spend-human-review-by-risk.md)
- [Thoughtworks: Humans on the loop: fix the harness, not the artefact](humans-on-the-loop-fix-the-harness-not-the-artefact.md)
