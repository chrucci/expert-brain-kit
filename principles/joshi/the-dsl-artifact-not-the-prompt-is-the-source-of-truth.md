# The DSL artifact, not the prompt, is the source of truth

Verified: 2 verbatim quotes from 1 source

Dimension: Processes (processes)

Evidence: opinion

How to measure: Measure how often changes to agent-generated artifacts are made by editing the artifact versus regenerating it from a stored prompt, and how long each path takes.

When agents generate code in a dense domain DSL, the generated artifact holds the intent and is what humans maintain. Later changes edit it directly instead of recovering and rerunning prompts, so the DSL and its semantic model are the team's lasting asset.

## Quotes

> If the scenario needs to change next month, there is no need to recover the original prompt and regenerate everything.
>
> [DSLs Enable Reliable Use of LLMs](https://martinfowler.com/articles/llm-and-dsls.html)

> The enduring asset is not the prompt, but the DSL and the semantic model.
>
> [DSLs Enable Reliable Use of LLMs](https://martinfowler.com/articles/llm-and-dsls.html)

## Support

Candidate: one source supports this principle so far.

Expert: Unmesh Joshi

Topics: deterministic-guardrails, processes

## Related principles

- [Unmesh Joshi: Constrained DSLs with validators let agents self-correct](constrained-dsls-with-validators-let-agents-self-correct.md)
