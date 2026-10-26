# Agents review first, humans approve by risk

Verified: 8 verbatim quotes from 6 sources

Dimension: Processes (processes)

Evidence: experience

How to measure: For each risk tier, track review wait time, the share of defects caught by agent versus human review, and incidents or rollbacks traced to merged agent changes.

Once agents write most of the code, review becomes the bottleneck. Let agents do the first pass on every change (style, bugs, tests) and build a layered safety net of tests, feature flags and staged rollouts, but keep a human accountable for approval. Concentrate human attention on risky, regulated or domain-sensitive code, and remember that green tests are not proof the work is done.

## Quotes

> On the Claude Code team, writing code, writing tests, and refactoring rarely slows us down anymore. But the bottlenecks didn’t go away when agentic coding took away the actual need to type code. Verification, code review, and security took their place.
>
> [Running an AI-native engineering org](https://claude.com/resources/articles/running-an-ai-native-engineering-org)

> Claude handles all the style and linting, PR feedback requests, catching bugs and fixing them before a full commit, and adding tests. Where we still definitely want a human is expertise.
>
> [Running an AI-native engineering org](https://claude.com/resources/articles/running-an-ai-native-engineering-org)

> It’s important to continually evaluate, though, because the right balance of trust vs. verify will keep changing as the models improve.
>
> [Running an AI-native engineering org](https://claude.com/resources/articles/running-an-ai-native-engineering-org)

> Ask Opus 5.5 to review a diff or a pull request before a person does.
>
> [Getting the most out of Opus 5.5 in Claude and Claude Code](https://claude.dev/blog/getting-the-most-out-of-opus-5-5/)

> unit tests always came before optimizations, and anything that could cause a user-visible problem shipped behind a short-lived feature flag.
>
> [How we made claude.ai 3x faster in two weeks](https://claude.dev/blog/how-we-made-claude-ai-faster/)

> When a human sits with Claude during development, they can ensure consistent quality and catch errors in real time.
>
> [Building a C compiler with a team of parallel Claudes](https://www.anthropic.com/engineering/building-c-compiler)

> So every pull request at Anthropic is code reviewed by clod code. And that actually catches maybe like 80% of bugs, something like this.
>
> [Building Claude Code with Boris Cherny at 00:41:36](https://newsletter.pragmaticengineer.com/p/building-claude-code-with-boris-cherny?t=2496s)

> What we did was accelerate the review process by combining automated agentic and deterministic reviews, while reserving human review for regulated or truly critical code.
>
> [How Anthropic secures its AI-native software development lifecycle](https://claude.com/resources/articles/how-anthropic-secures-its-ai-native-software-development-lifecycle)

## Support

Established: 6 independent sources support this principle.

Expert: Anthropic engineering

Topics: deterministic-guardrails, human-roles, processes

## Related principles

- [Anthropic engineering: Independent, human-calibrated agent reviewers](independent-human-calibrated-agent-reviewers.md)
- [Anthropic engineering: Make agent work legible enough for humans to review](make-agent-work-legible-enough-for-humans-to-review.md)
- [Anthropic engineering: Humans own the what, agents own the how](humans-own-the-what-agents-own-the-how.md)
