# Earn agent autonomy gradually within fixed boundaries

Verified: 5 verbatim quotes from 2 sources

Dimension: Roles for agents (agent-roles)

Evidence: experience

How to measure: Count permission escalations and the incidents that follow them, actions outside approved boundaries (target zero), and how often humans have to step into scheduled tasks.

Start agents with tight approval and sandbox settings, and widen them only for trusted repositories or proven workflows. Automated approval should work inside the existing permission boundaries, not widen them. A workflow should become a reliable, shared skill before it is scheduled to run unattended.

## Quotes

> Keep approval and sandboxing tight by default, then loosen permissions only for trusted repos or specific workflows once the need is clear.
>
> [Best practices | ChatGPT Learn](https://learn.chatgpt.com/guides/best-practices)

> A useful rule is that skills define the method and scheduled tasks define the schedule. If a workflow still needs a lot of steering, turn it into a skill first. Once it’s predictable, scheduling it can save time.
>
> [Best practices | ChatGPT Learn](https://learn.chatgpt.com/guides/best-practices)

> Scheduling a recurring task before it’s reliable manually
>
> [Best practices | ChatGPT Learn](https://learn.chatgpt.com/guides/best-practices)

> A [persistent goal](https://developers.openai.com/codex/long-running-work) keeps Codex focused on the task, while [automatic approval review](https://developers.openai.com/codex/sandboxing/auto-review) can review eligible actions without changing the existing permission boundaries.
>
> [Automating repetitive work at OpenAI with Codex](https://developers.openai.com/blog/automating-repetitive-work-at-openai-with-codex/)

> If a development environment can't be provisioned because a quota is exhausted, for example, I might suggest reusing an existing environment or looking for another approved option.
>
> [Automating repetitive work at OpenAI with Codex](https://developers.openai.com/blog/automating-repetitive-work-at-openai-with-codex/)

## Support

Established: 2 independent sources support this principle.

Expert: OpenAI engineering

Topics: agent-roles, deterministic-guardrails, processes

## Related principles

- [OpenAI engineering: Plan, size and bound each agent run](plan-size-and-bound-each-agent-run.md)
