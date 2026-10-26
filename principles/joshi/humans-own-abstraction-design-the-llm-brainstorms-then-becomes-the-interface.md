# Humans own abstraction design; the LLM brainstorms, then becomes the interface

Verified: 1 verbatim quote from 1 source

Dimension: Roles for humans (human-roles)

Evidence: experience

How to measure: Track the share of agent-generated changes that pass review unchanged in areas with an established domain vocabulary versus areas without one.

While a domain abstraction or DSL is being designed, use the LLM as a brainstorming partner and leave the design decisions with humans. Once the vocabulary exists, let the LLM act as the natural-language interface that generates code against it. Put human judgement into the first phase and agent throughput into the second.

## Quotes

> They are a great help while we shape the design and its vocabulary, acting as brainstorming partners to help us explore the design space and discover the right abstractions. Once the vocabulary is established, LLMs work as an excellent natural language interface to it.
>
> [DSLs Enable Reliable Use of LLMs](https://martinfowler.com/articles/llm-and-dsls.html)

## Support

Candidate: one source supports this principle so far.

Expert: Unmesh Joshi

Topics: agent-roles, human-roles, techniques

## Related principles

- [Unmesh Joshi: Humans keep writing code to discover design](humans-keep-writing-code-to-discover-design.md)
- [Unmesh Joshi: Constrained DSLs with validators let agents self-correct](constrained-dsls-with-validators-let-agents-self-correct.md)
