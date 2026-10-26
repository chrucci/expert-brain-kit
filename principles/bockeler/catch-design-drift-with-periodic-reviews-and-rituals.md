# Catch design drift with periodic reviews and rituals

Verified: 5 verbatim quotes from 2 sources

Dimension: Processes (processes)

Evidence: experience

How to measure: Count valid high-severity findings per periodic modularity review and track the trend in files touched and tokens spent per change.

Deterministic tools cannot judge modularity and coupling, and the small refactoring steps of TDD do not work well in the agent loop. Schedule regular AI modularity reviews with strong prompts, run several times when the result matters, plus team rituals that catch drift. Watch the trend in files touched and tokens spent per change.

## Quotes

> Refactoring remains crucial, but the small steps of traditional TDD don't seem to be an efficient or effective way to do it in the agent loop.
>
> [TDD inside the agent loop - theater or actual value?](https://martinfowler.com/articles/exploring-gen-ai/tdd-in-the-agent-loop.html)

> develop team rituals to maintain a good understanding of the codebase and catch drift early; keep an eye on the trend of number of files touched per change, and number of
>
> [TDD inside the agent loop - theater or actual value?](https://martinfowler.com/articles/exploring-gen-ai/tdd-in-the-agent-loop.html)

> Overall, codebase design and modularity seems like a concern where computational sensors alone cannot help us much, AI is needed to add semantic interpretation, and consider trade-offs.
>
> [Maintainability sensors for coding agents](https://martinfowler.com/articles/sensors-for-coding-agents.html)

> The AI modularity review is a great example of “garbage collection”, and worked quite well when given powerful prompts.
>
> [Maintainability sensors for coding agents](https://martinfowler.com/articles/sensors-for-coding-agents.html)

> A useful reminder that when it matters, it's often worth running an LLM-based analysis multiple times, to get a fuller picture.
>
> [Maintainability sensors for coding agents](https://martinfowler.com/articles/sensors-for-coding-agents.html)

## Support

Established: 2 independent sources support this principle.

Expert: Birgitta Böckeler

Topics: metrics, processes, techniques

## Related principles

- [Birgitta Böckeler: Pair guides with fast, self-correcting sensors](pair-guides-with-fast-self-correcting-sensors.md)
- [Birgitta Böckeler: Choose stacks and architecture for harnessability](choose-stacks-and-architecture-for-harnessability.md)
