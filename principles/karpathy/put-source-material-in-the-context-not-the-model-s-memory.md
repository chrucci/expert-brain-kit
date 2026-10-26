# Put source material in the context, not the model's memory

Verified: 2 verbatim quotes from 1 source

Dimension: Techniques (techniques)

Evidence: experience

How to measure: Track how often agent-generated integration code uses deprecated APIs with and without current docs supplied in context.

A model's weights hold only a hazy, often outdated memory, and an agent doesn't learn the organisation on the job, while the context window is working memory it can use directly. Paste in current docs, organisational context and real source material instead of trusting recall, especially for fast-moving APIs.

## Quotes

> Claude kept hallucinating deprecated APIs, model names, and input/output conventions that have all changed recently, which was confusing, but it resolved them after I copy pasted the docs back and forth for a while.
>
> [Vibe coding MenuGen](https://karpathy.bearblog.dev/vibe-coding-menugen/)

> At this point Claude hallucinated about 1000 lines of code that appeared to be deprecated Clerk APIs. I had to copy paste a lot of the docs back and forth to get things gradually unstuck.
>
> [Vibe coding MenuGen](https://karpathy.bearblog.dev/vibe-coding-menugen/)

## Support

Candidate: one source supports this principle so far.

Expert: Andrej Karpathy

Topics: techniques

## Related principles

- [Andrej Karpathy: Write concrete prompts that state the goal](write-concrete-prompts-that-state-the-goal.md)
- [Andrej Karpathy: Make software and infrastructure legible to agents](make-software-and-infrastructure-legible-to-agents.md)
