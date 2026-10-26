# Humans keep writing code to discover design

Verified: 8 verbatim quotes from 3 sources

Dimension: Roles for humans (human-roles)

Evidence: experience

How to measure: Compare readability and later change lead time for modules where humans refactored or authored the structure against modules merged as generated.

Reviewing generated code checks it against intent but rarely makes people work through design decisions such as where a responsibility belongs. Developers should keep actively writing and reshaping code, especially while the design is still being discovered.

## Quotes

> we cannot simply 'prompt' the LLMs to do the work. We make use of them, certainly, but we must iteratively drive the code to build the stable structure ourselves.
>
> [Conversation: LLMs and the what/how loop](https://martinfowler.com/articles/convo-what-how.html)

> LLMs should be treated as powerful instruments in this phase, but the developer must remain the primary architect of the model.
>
> [Conversation: LLMs and the what/how loop](https://martinfowler.com/articles/convo-what-how.html)

> This is why I prefer to use LLMs as a translation layer inside my what/how loop. I use them to quickly sketch a first version, but I still rely on writing and refactoring to shape the structure—because the code I keep is the code I can explain, test, and change with confidence.
>
> [Conversation: LLMs and the what/how loop](https://martinfowler.com/articles/convo-what-how.html)

> When I asked the LLM to derive the implementation for MinIO, it produced something that was too procedural and harder to understand.
>
> [Conversation: LLMs and the what/how loop](https://martinfowler.com/articles/convo-what-how.html)

> It is important to remember that
> generated code is usually the first version that makes the test pass.
>
> [Conversation: LLMs and the what/how loop](https://martinfowler.com/articles/convo-what-how.html)

> But reviewing rarely forces us to wrestle with the design decisions. Writing code, by contrast, forces us to think through concrete decisions—such as where a responsibility belongs or what boundaries should be exposed so the design can be extended further.
>
> [DSLs Enable Reliable Use of LLMs](https://martinfowler.com/articles/llm-and-dsls.html)

> Building vocabulary through code requires active engagement in writing and reshaping code; not just passive review of generated code .
>
> [What Is Code?](https://martinfowler.com/articles/what-is-code.html)

> We are not meant to be passive reviewers of generated code. The act of writing code is itself part of our thinking.
>
> [What Is Code?](https://martinfowler.com/articles/what-is-code.html)

## Support

Established: 3 independent sources support this principle.

Expert: Unmesh Joshi

Topics: human-roles, skills, techniques

## Related principles

- [Unmesh Joshi: Guard against cognitive debt from generated abstractions](guard-against-cognitive-debt-from-generated-abstractions.md)
- [Unmesh Joshi: Humans own abstraction design; the LLM brainstorms, then becomes the interface](humans-own-abstraction-design-the-llm-brainstorms-then-becomes-the-interface.md)
