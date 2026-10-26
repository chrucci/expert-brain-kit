# Experienced humans own design quality, intent and strategy

Verified: 8 verbatim quotes from 23 sources

Dimension: Roles for humans (human-roles)

Evidence: experience

How to measure: Count design, semantic and security problems in agent changes that passed automated checks but were caught by experienced human reviewers, and compare rework on workstreams with and without an expert in the target stack.

Left alone, agents produce working code that adds debt, changes semantics and takes the insecure path of least resistance, and they cannot choose the right refactorings. Experienced humans have to set strategy and constraints, judge whether the spec matches business intent, and steer agents toward correct designs, with automated gates as a backstop rather than a replacement.

## Quotes

> I think this is a clear example where an AI agent left to their own would have changed the codebase for the worse, and it took a developer with experience to notice the issue and to direct the agent to the correct implementation.
>
> [Assessing internal quality while coding with an agent](https://martinfowler.com/articles/exploring-gen-ai/ccmenu-quality.html)

> Claude is unable to look at code, look at refactorings in general and work out which are suitable to apply: a human needs to actively guide it.
>
> [The Economic Benefit of Refactoring](https://martinfowler.com/articles/exploring-gen-ai/refactoring-economic-benefit.html)

> The most important lesson from this experiment was fundamentally about human agency.
>
> [The Archaeologist’s Copilot](https://martinfowler.com/articles/archaeologist-copilot.html)

> So the command is there when you want to use it, but it is built to handle the mechanical part of review, not to take it over. For now, humans stay in the loop by design.
>
> [Structured-Prompt-Driven Development (SPDD)](https://martinfowler.com/articles/structured-prompt-driven/)

> In both cases, the AI suggested a path with serious security implications. In both cases, it took a human asking the right question to catch it.
>
> [The VibeSec Reckoning](https://martinfowler.com/articles/vibesec-reckoning.html)

> It’s important to remember, though, that it’s the human engineer who consumes this data — they are key for the next step.
>
> [Claude Code and COBOL modernization: What’s the reality?](https://www.thoughtworks.com/insights/articles/claude-code-cobol-modernization-reality)

> This is where we determine whether the agent produced something that actually meets user intent. It requires judgment. Automation helps, but it doesn’t replace human accountability.
>
> [The operating system for enterprise AI](https://www.thoughtworks.com/insights/articles/operating-system-enterprise-ai)

> Software roles are evolving beyond traditional syntax writing toward judgment, intent, architecture, validation and deciding what feedback matters.
>
> [AI makes Agile more alive](https://www.thoughtworks.com/insights/blog/agile-engineering-practices/ai-makes-agile-more-alive)

## Support

Established: 23 independent sources support this principle.

Expert: Thoughtworks

Topics: human-roles, skills

## Related principles

- [Thoughtworks: Developer value shifts to thinking, and understanding must keep pace](developer-value-shifts-to-thinking-and-understanding-must-keep-pace.md)
- [Thoughtworks: Code structure is a running cost of agent work](code-structure-is-a-running-cost-of-agent-work.md)
- [Thoughtworks: Enforce agent work with deterministic sensors in the loop](enforce-agent-work-with-deterministic-sensors-in-the-loop.md)
