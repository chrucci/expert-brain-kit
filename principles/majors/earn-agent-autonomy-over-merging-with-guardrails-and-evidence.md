# Earn agent autonomy over merging with guardrails and evidence

Verified: 7 verbatim quotes from 4 sources

Dimension: Roles for agents (agent-roles)

Evidence: opinion

How to measure: Track the percentage of PRs that are AI-reviewed and auto-merged against change failure rate (for example under 3%), SLO attainment and incident load, and how AI review's catch rate compares with human review during side-by-side trials.

Shipping AI code without human review is a direction to work toward, not a switch to flip. Set autonomy per task, build the evals, flags, observability and blast-radius reductions first, run AI review next to human review to compare catch rates, and raise the auto-merge share only while change failure rate and SLOs stay within limits.

## Quotes

> Yes, it may be absolutely unthinkable to start auto-accepting diffs given the current state of your codebase and guardrails.
>
> [AI enthusiasts are in a race against time, AI skeptics are in a race against entropy](https://charity.wtf/p/ai-enthusiasts-are-in-a-race-against)

> Better evals? Better tests? Better feature flags, guardrails, observability? Work on decoupling dependencies and reducing blast radius? Start with something small and out of the critical path?
>
> [AI enthusiasts are in a race against time, AI skeptics are in a race against entropy](https://charity.wtf/p/ai-enthusiasts-are-in-a-race-against)

> Approach this like an engineering problem, not an epistemological debate. What would it take? Start there.
>
> [AI enthusiasts are in a race against time, AI skeptics are in a race against entropy](https://charity.wtf/p/ai-enthusiasts-are-in-a-race-against)

> The question isn't "human or AI." It's "how much autonomy, for which task, right now."
>
> [Happy Birthday to Us: Honeycomb 10 Year Manifesto, Part 1](https://www.honeycomb.io/blog/honeycomb-10-year-manifesto-part-1)

> By the end of the year, our systems are safe enough that at least 25% of all PRs are AI-reviewed and auto-merged (with no human review required) while maintaining a change failure rate under 3%
>
> [AI Norms & Values, Part 2 of 3: AI for Honeycomb Engineering](https://www.honeycomb.io/blog/ai-norms-values-part-2-ai-honeycomb-engineering)

> We maintain our SLOs and don't increase incident response workload outside of sustainable bounds
>
> [AI Norms & Values, Part 2 of 3: AI for Honeycomb Engineering](https://www.honeycomb.io/blog/ai-norms-values-part-2-ai-honeycomb-engineering)

> Or, for example, if you and the AI would both do it in tandem for a few months and you would be like, you would get to, how much are they catching? How much am I catching? Is it about the same? Is it more? Is it less?
>
> [Stop being skeptical about AI for development with Charity Majors at 00:12:19](https://newsletter.pragmaticengineer.com/p/stop-being-skeptical-about-ai-for?t=739s)

## Support

Established: 4 independent sources support this principle.

Expert: Charity Majors

Topics: agent-roles, deterministic-guardrails, metrics

## Related principles

- [Charity Majors: Move trust from authorship to deterministic validation](move-trust-from-authorship-to-deterministic-validation.md)
- [Charity Majors: Owning engineers set the shipping conditions](owning-engineers-set-the-shipping-conditions.md)
