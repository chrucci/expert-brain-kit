# Pay down cognitive debt on agent-written code

Verified: 8 verbatim quotes from 4 sources

Dimension: Roles for humans (human-roles)

Evidence: experience

How to measure: Periodically ask engineers to explain or extend recently agent-changed core modules without the agent, and track how often they can't, against the volume of agent changes merged.

Agent speed lets a codebase outgrow the team's understanding, and a core that has become a black box slows planning the way technical debt does. Humans must keep understanding the critical parts deeply enough to keep steering them, using agent-written walkthroughs and interactive explanations, and must deliberately balance speed against thoroughness.

## Quotes

> but this speed also means that changes which we would normally have considered over the course of weeks are landing in a matter of hours.
>
> [Thoughts on slowing the fuck down](https://simonwillison.net/2026/Mar/25/thoughts-on-slowing-the-fuck-down/)

> It's so easy to let the codebase evolve outside of our abilities to reason clearly about it.
>
> [Thoughts on slowing the fuck down](https://simonwillison.net/2026/Mar/25/thoughts-on-slowing-the-fuck-down/)

> I'm not convinced writing by hand is the best way to address this, but it's absolutely the case that we need the discipline to find a new balance of speed v.s. mental thoroughness now that typing out the code is no longer anywhere close to being the bottleneck on writing software.
>
> [Thoughts on slowing the fuck down](https://simonwillison.net/2026/Mar/25/thoughts-on-slowing-the-fuck-down/)

> If you are concerned that LLMs might reduce the speed at which you learn new skills I strongly recommend adopting patterns like this one.
>
> [Linear walkthroughs - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/linear-walkthroughs/)

> I learned a great deal about how SwiftUI apps are structured and absorbed some solid details about the Swift language itself just from reading this document.
>
> [Linear walkthroughs - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/linear-walkthroughs/)

> I released the code [to GitHub](https://github.com/simonw/present) and then realized I didn't know anything about how it actually worked - I had prompted the whole thing into existence
>
> [Linear walkthroughs - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/linear-walkthroughs/)

> If the core of our application becomes a black box that we don't fully understand we can no longer confidently reason about it, which makes planning new features harder and eventually slows our progress in the same way that accumulated technical debt does.
>
> [Interactive explanations - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/interactive-explanations/)

> His argument is that you need to understand the code to a depth that enables you to participate further with the model
>
> [Understand to participate](https://simonwillison.net/2026/Jul/2/understand-to-participate/)

## Support

Established: 4 independent sources support this principle.

Expert: Simon Willison

Topics: human-roles, skills, techniques

## Related principles

- [Simon Willison: Human cognitive capacity limits agents per person and team size](human-cognitive-capacity-limits-agents-per-person-and-team-size.md)
- [Simon Willison: Verify beyond line-by-line review, and earn trust in automated review](verify-beyond-line-by-line-review-and-earn-trust-in-automated-review.md)
