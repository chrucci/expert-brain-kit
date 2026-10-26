# Let the LLM interview the human to build context

Verified: 3 verbatim quotes from 1 source

Dimension: Techniques (techniques)

Evidence: experience

How to measure: For interview-built context and hand-written context, compare the time it takes to prepare and how much rework the downstream agent output needs.

Instead of a human writing long context by hand, have an LLM question the human one question at a time and then write a context report that another session or model uses to do the work. This makes good context cheaper and keeps gathering context separate from doing the work.

## Quotes

> The obvious way to do this is for a human to write this context, but an alternative is to use an LLM to write this context after interviewing a human.
>
> [Interrogatory LLM](https://martinfowler.com/bliki/InterrogatoryLLM.html)

> Once it's done, it can then create the context report for another session (perhaps with another model) to carry out the next step.
>
> [Interrogatory LLM](https://martinfowler.com/bliki/InterrogatoryLLM.html)

> A striking element of his approach is insisting that the LLM
>   ask only one question at a time. (When I tried it, I found it needed to be
>   frequently reminded of this.)
>
> [Interrogatory LLM](https://martinfowler.com/bliki/InterrogatoryLLM.html)

## Support

Candidate: one source supports this principle so far.

Expert: Martin Fowler

Topics: agent-roles, techniques

## Related principles

- [Martin Fowler: Validate specs by having an LLM interview domain experts](validate-specs-by-having-an-llm-interview-domain-experts.md)
- [Martin Fowler: Capture knowledge from non-writers through LLM interviews](capture-knowledge-from-non-writers-through-llm-interviews.md)
