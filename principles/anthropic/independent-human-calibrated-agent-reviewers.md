# Independent, human-calibrated agent reviewers

Verified: 8 verbatim quotes from 6 sources

Dimension: Roles for agents (agent-roles)

Evidence: experience

How to measure: Measure agreement between agent reviewers and human reviewers on the same changes across tuning rounds and in shadow mode, and compare defects reaching human review with and without independent agent reviewers.

Agents overrate their own work, so review should come from separate fresh-context agents, ideally several with narrow focuses and rubrics that encode team taste. Out of the box they are weak judges, so humans calibrate them by reading their traces, approving eval cases and graders, and running new reviewers in shadow mode until they have earned trust.

## Quotes

> When you run `/claude-api build-eval` in Claude Code, Claude interviews you, builds the eval inside your codebase, and pauses for approval at specific points.
>
> [Automating eval design and hillclimbing with Claude](https://claude.dev/blog/automating-eval-design-and-hillclimbing/)

> Claude grades a handful of cases and asks whether you would have scored any of them differently (Figure 4).
>
> [Automating eval design and hillclimbing with Claude](https://claude.dev/blog/automating-eval-design-and-hillclimbing/)

> Claude will employ the guidance shared in this article to design the examples and grader, and ensure you approve the examples and the grader.
>
> [Automating eval design and hillclimbing with Claude](https://claude.dev/blog/automating-eval-design-and-hillclimbing/)

> Rubrics allow Claude to try and verify your taste in a particular field (e.g. what does a good API design look like) by using [dynamic workflows](https://claude.com/blog/a-harness-for-every-task-dynamic-workflows-in-claude-code) and spinning up verifier agents with those rubrics.
>
> [The new rules of context engineering for Claude 5 generation models](https://claude.dev/blog/the-new-rules-of-context-engineering-for-claude-5-generation-models/)

> The longer Claude works unattended, the more an independent check matters before you count the work as done.
>
> [Best practices for Claude Code - Claude Code Docs](https://www.anthropic.com/engineering/claude-code-best-practices)

> Separating the agent doing the work from the agent judging it proves to be a strong lever to address this issue.
>
> [Harness design for long-running application development](https://www.anthropic.com/engineering/harness-design-long-running-apps)

> When a PR is opened at Anthropic, multiple agents automatically review it. Each review agent is designed and scoped to a specific, narrow focus and leverages RAG for additional context and memory surrounding past incidents.
>
> [How Anthropic secures its AI-native software development lifecycle](https://claude.com/resources/articles/how-anthropic-secures-its-ai-native-software-development-lifecycle)

> When an unbiased review of an implementation is the goal, a subagent provides a clean slate because it doesn't inherit the assumptions, context, or blind spots from the primary conversation.
>
> [How and when to use subagents in Claude Code](https://claude.com/resources/articles/subagents-in-claude-code)

## Support

Established: 6 independent sources support this principle.

Expert: Anthropic engineering

Topics: agent-count, agent-roles, human-roles, processes

## Related principles

- [Anthropic engineering: Agents review first, humans approve by risk](agents-review-first-humans-approve-by-risk.md)
- [Anthropic engineering: Done means a check the agent can run](done-means-a-check-the-agent-can-run.md)
