# Validate specs by having an LLM interview domain experts

Verified: 3 verbatim quotes from 1 source

Dimension: Processes (processes)

Evidence: opinion

How to measure: For interview-based review and traditional read-through, compare how many spec defects each finds before implementation and how much expert time each takes.

People find reviewing documents hard, so a team can check a specification by having an LLM question a domain expert against it instead of asking for a read-through. This catches spec errors before agents build from the spec, especially when the spec is badly written.

## Quotes

> give it a document, such as a software specification, that captures knowledge about a domain - and then ask the LLM to interview a human expert to determine if the document is accurate.
>
> [Interrogatory LLM](https://martinfowler.com/bliki/InterrogatoryLLM.html)

> People often find reviewing hard, so a conversation with an LLM might be more fruitful, particularly if the document isn't well-written.
>
> [Interrogatory LLM](https://martinfowler.com/bliki/InterrogatoryLLM.html)

> Naturally we can use both of these, using one interrogatory LLM to build a document, then using other interrogatory LLMs to review it with other experts.
>
> [Interrogatory LLM](https://martinfowler.com/bliki/InterrogatoryLLM.html)

## Support

Candidate: one source supports this principle so far.

Expert: Martin Fowler

Topics: deterministic-guardrails, processes, techniques

## Related principles

- [Martin Fowler: Let the LLM interview the human to build context](let-the-llm-interview-the-human-to-build-context.md)
