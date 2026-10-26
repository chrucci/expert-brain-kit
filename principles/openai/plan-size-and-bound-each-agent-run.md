# Plan, size and bound each agent run

Verified: 8 verbatim quotes from 3 sources

Dimension: Roles for agents (agent-roles)

Evidence: experience

How to measure: Track merge and rework rates by task size and by whether a plan came first, and record how loops end and whether the remaining findings fall to zero or stall.

Scope agent tasks to roughly an hour of human work. For larger work, have the agent write a plan that a human approves before execution, so humans make the consequential choices. Give autonomous loops explicit stop conditions (validation passes, an attempt cap, the remaining findings stop shrinking, a human decision is needed), and judge progress by those shrinking findings rather than by the number of edits.

## Quotes

> A good loop usually stops for one of four reasons: validation passes, the loop reaches a maximum number of attempts, the remaining delta stops changing, or the next decision needs human review. Those stop conditions are just as important as the repair prompt.
>
> [Build iterative repair loops with Codex](https://developers.openai.com/cookbook/examples/codex/build_iterative_repair_loops_with_codex/)

> The important signal is not that Codex made edits. The important signal is that the remaining validation delta gets smaller as the loop runs.
>
> [Build iterative repair loops with Codex](https://developers.openai.com/cookbook/examples/codex/build_iterative_repair_loops_with_codex/)

> In a real maintenance workflow, this table tells you whether the loop is converging or needs a clearer constraint or human review.
>
> [Build iterative repair loops with Codex](https://developers.openai.com/cookbook/examples/codex/build_iterative_repair_loops_with_codex/)

> - Wait for me to review and approve the plan before beginning.
>
> [Automating repetitive work at OpenAI with Codex](https://developers.openai.com/blog/automating-repetitive-work-at-openai-with-codex/)

> Often, the useful part of my involvement is helping Codex decide between alternatives: which evaluation system to use, whether to provision new infrastructure, or whether existing resources will do the job.
>
> [Automating repetitive work at OpenAI with Codex](https://developers.openai.com/blog/automating-repetitive-work-at-openai-with-codex/)

> I still decide when a plan is ready and when a consequential choice needs human judgment. Codex does the repetitive execution and records what happened in more detail than I would have written myself.
>
> [Automating repetitive work at OpenAI with Codex](https://developers.openai.com/blog/automating-repetitive-work-at-openai-with-codex/)

> that would take you or a teammate about an hour to complete
>
> [How OpenAI at p.11](https://cdn.openai.com/pdf/6a2631dc-783e-479b-b1a4-af0cfbd38630/how-openai-uses-codex.pdf#page=11)

> input for follow-up prompts when you switch to Code Mode.
>
> [How OpenAI at p.11](https://cdn.openai.com/pdf/6a2631dc-783e-479b-b1a4-af0cfbd38630/how-openai-uses-codex.pdf#page=11)

## Support

Established: 3 independent sources support this principle.

Expert: OpenAI engineering

Topics: agent-roles, human-roles, metrics, techniques

## Related principles

- [OpenAI engineering: Earn agent autonomy gradually within fixed boundaries](earn-agent-autonomy-gradually-within-fixed-boundaries.md)
- [OpenAI engineering: A checkable definition of done, proven by fast execution](a-checkable-definition-of-done-proven-by-fast-execution.md)
- [OpenAI engineering: Human attention, not code generation, is the bottleneck](human-attention-not-code-generation-is-the-bottleneck.md)
