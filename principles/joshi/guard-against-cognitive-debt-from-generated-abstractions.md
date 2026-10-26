# Guard against cognitive debt from generated abstractions

Verified: 2 verbatim quotes from 1 source

Dimension: Skills (skills)

Evidence: opinion

How to measure: Regularly ask developers to explain the purpose and invariants of recently generated abstractions, and track the share they can explain correctly.

LLMs can add vocabulary and structure to a codebase faster than the team comes to understand it, and the code can still compile and pass tests. Teams need to watch the gap between what the code expresses and what they actually share an understanding of.

## Quotes

> The problem is not that the LLM generated code. The problem is that the code introduced vocabulary faster than the developers built understanding.
>
> [What Is Code?](https://martinfowler.com/articles/what-is-code.html)

> The code may compile. It may even pass basic tests. But if the team does not understand the conceptual model behind those structures, the codebase has gained vocabulary without shared understanding.
>
> [What Is Code?](https://martinfowler.com/articles/what-is-code.html)

## Support

Candidate: one source supports this principle so far.

Expert: Unmesh Joshi

Topics: human-roles, skills

## Related principles

- [Unmesh Joshi: Humans keep writing code to discover design](humans-keep-writing-code-to-discover-design.md)
