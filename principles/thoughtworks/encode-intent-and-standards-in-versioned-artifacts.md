# Encode intent and standards in versioned artifacts

Verified: 8 verbatim quotes from 20 sources

Dimension: Techniques (techniques)

Evidence: experience

How to measure: Track the share of behaviour changes whose commit also updates the matching spec or rules file, and compare variance in agent output quality and rework across team members before and after standards are encoded.

Put specs, rules files, skills and senior developers' tacit standards into versioned, reviewed artifacts that load into every session and change before the code does. Output quality then stops depending on who prompts, and agent work becomes traceable, though these artifacts guide rather than enforce unless checks are paired with them.

## Quotes

> Every team has senior developers who instinctively know when code is right—they spot architectural drift, security gaps, and convention violations that others miss.
>
> [Patterns for Reducing Friction in AI-Assisted Development](https://martinfowler.com/articles/reduce-friction-ai/)

> When reality diverges, fix the prompt first — then update the code.
>
> [Structured-Prompt-Driven Development (SPDD)](https://martinfowler.com/articles/structured-prompt-driven/)

> The key distinction from a casual prompt is operational discipline: the file is versioned, loaded by default, reviewed, and paired with automated checks.
>
> [The VibeSec Reckoning](https://martinfowler.com/articles/vibesec-reckoning.html)

> Minor changes often caused unexpected failures, putting us in a loop of manual fixes.
>
> [Beyond the hype: A real-world guide to building enterprise-grade AI agents](https://www.thoughtworks.com/insights/articles/a-real-world-guide-to-building-enterprise-grade-ai-agents)

> We also maintained architecture decision records (ADR) that captured every significant structural choice, so the AI followed decisions the team had already made, rather than guessing.
>
> [AI-assisted migration: Critical lessons from the modernization frontlines](https://www.thoughtworks.com/insights/articles/ai-assisted-migration-lessons)

> On some AI-enabled projects, requirements, specifications and architectural decision records are moving closer to the codebase so both people and AI can use them.
>
> [Path to AI-first organization](https://www.thoughtworks.com/insights/articles/path-to-ai-first-organization)

> This involves feeding the agent precise architectural constraints, API specifications and style guides.
>
> [Supervisory engineering: Orchestrating software’s ‘middle loop’](https://www.thoughtworks.com/insights/blog/agile-engineering-practices/supervisory-engineering-orchestrating-software-middle-loop)

> Store all agent definitions, skills, rules and workflows in version control. Submit harness edits through pull requests with peer review.
>
> [Engineering the harness: A practical pattern for reliable coding agents](https://www.thoughtworks.com/insights/blog/architecture/engineering-the-harness-a-practical-pattern-for-reliable-coding-agents)

## Support

Established: 20 independent sources support this principle.

Expert: Thoughtworks

Topics: deterministic-guardrails, techniques

## Related principles

- [Thoughtworks: Enforce agent work with deterministic sensors in the loop](enforce-agent-work-with-deterministic-sensors-in-the-loop.md)
- [Thoughtworks: Humans on the loop: fix the harness, not the artefact](humans-on-the-loop-fix-the-harness-not-the-artefact.md)
- [Thoughtworks: Design and confirm intent in small staged steps](design-and-confirm-intent-in-small-staged-steps.md)
