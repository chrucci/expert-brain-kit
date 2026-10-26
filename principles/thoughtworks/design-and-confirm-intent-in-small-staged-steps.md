# Design and confirm intent in small staged steps

Verified: 8 verbatim quotes from 15 sources

Dimension: Processes (processes)

Evidence: experience

How to measure: Compare rework, post-merge intent drift and review time for work done design-first in small reviewed increments against work generated and reviewed in one large pass.

For non-trivial work, take the agent through design before code and confirm intent at small checkpoints (story, analysis, spec, code, tests) rather than in one large review that reviewers end up skimming. Break work into chunks and use version control to back out of wrong turns.

## Quotes

> The approach remained similar: break down the task into smaller chunks. For each of the chunks I asked Windsurf to come up with a plan first before asking for an implementation.
>
> [Assessing internal quality while coding with an agent](https://martinfowler.com/articles/exploring-gen-ai/ccmenu-quality.html)

> Rather than asking AI to immediately produce code, walk through progressive levels of design: capabilities, components, interactions, contracts, and only then implementation.
>
> [Patterns for Reducing Friction in AI-Assisted Development](https://martinfowler.com/articles/reduce-friction-ai/)

> Intent confirmation has to be distributed across the workflow, because compressing it into a single review after plan generation puts too much in front of the reviewer at once.
>
> [Structured-Prompt-Driven Development (SPDD)](https://martinfowler.com/articles/structured-prompt-driven/)

> Treating this as if we’re deploying the tool and letting it run with a prompt is a deeply naive view of execution and modernization overall.
>
> [Claude Code and COBOL modernization: What’s the reality?](https://www.thoughtworks.com/insights/articles/claude-code-cobol-modernization-reality)

> We are going to shift where our rigor applies, and a key point is that we want this discipline and control to be closer to reality, much like what XP achieved.
>
> [Quality is speed: Where engineering discipline moves in the AI era](https://www.thoughtworks.com/insights/articles/quality-is-speed-AI-era)

> That makes small-batch discipline more important, not less. Easier generation can tempt teams to produce more change than they can effectively review, understand or validate.
>
> [AI makes Agile more alive](https://www.thoughtworks.com/insights/blog/agile-engineering-practices/ai-makes-agile-more-alive)

> The biggest lesson for me was that speed doesn't come from typing; it comes from understanding.
>
> [Rethinking leadership: How a sabbatical transformed a CIO into a coding intern  [part one]](https://www.thoughtworks.com/insights/blog/careers-at-thoughtworks/Rethinking-leadership-cio-journey-as-a-coding-intern)

> In the SPDD workflow, the developer's value has shifted from writing to reviewing and directing.
>
> [Rethinking leadership: How a sabbatical transformed a CIO into a coding intern  [part two]](https://www.thoughtworks.com/insights/blog/careers-at-thoughtworks/cio-journey-as-a-coding-intern-part-two)

## Support

Established: 15 independent sources support this principle.

Expert: Thoughtworks

Topics: processes, techniques

## Related principles

- [Thoughtworks: Encode intent and standards in versioned artifacts](encode-intent-and-standards-in-versioned-artifacts.md)
- [Thoughtworks: Verification is the bottleneck; spend human review by risk](verification-is-the-bottleneck-spend-human-review-by-risk.md)
