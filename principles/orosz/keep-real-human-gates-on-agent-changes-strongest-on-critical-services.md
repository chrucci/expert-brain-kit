# Keep real human gates on agent changes, strongest on critical services

Verified: 8 verbatim quotes from 4 sources

Dimension: Processes (processes)

Evidence: experience

How to measure: Track the share of merged changes with no human reviewer and the review depth on agent PRs over time, against change-failure, incident and security-defect rates for each service tier.

Automation bias leads teams to stop reading agent code once it has looked fine a few times. AI-only review then lets defects and security incidents through, and a codebase nobody reads becomes easier to rewrite than to fix within months. Keep an engaged human reviewer, and on high-tier services keep deliberate friction such as extra reviewers and sign-offs.

## Quotes

> The good thing about friction is that it makes humans stop and think.
>
> [Building Pi, and what makes self-modifying software so fascinating](https://newsletter.pragmaticengineer.com/p/building-pi-and-what-makes-self-modifying)

> you have services based on tier based on criticality, the highest tier software. now needs to have let's say two or three code reviews or an approval from a director to do a configuration change which again all slows down but it's kind of like we know that this is on purpose
>
> [Building Pi, and what makes self-modifying software so fascinating at 01:07:15](https://newsletter.pragmaticengineer.com/p/building-pi-and-what-makes-self-modifying?t=4035s)

> Automation bias is one of the biggest risks of working with AI agents.
>
> [Building Pi, and what makes self-modifying software so fascinating](https://newsletter.pragmaticengineer.com/p/building-pi-and-what-makes-self-modifying)

> Once devs confirm that an AI agent can produce acceptable code, they start to review its output less often, even though agents can – and do! – produce slop.
>
> [Building Pi, and what makes self-modifying software so fascinating](https://newsletter.pragmaticengineer.com/p/building-pi-and-what-makes-self-modifying)

> Dex is such a big believer in gender coding, yet he's the one warning us that if you stop reading the code, you have about 3 -6 months before your codebase becomes easier to rewrite than to fix.
>
> [Context engineering with Dex Horthy at 01:31:02](https://newsletter.pragmaticengineer.com/p/context-engineering-with-dex-horthy?t=5462s)

> except review and validation will become a much more important step in those projects.
>
> [The creator of Clawd: "I ship code I don't read" at 01:53:50](https://newsletter.pragmaticengineer.com/p/the-creator-of-clawd-i-ship-code?t=6830s)

> This is a pretty funny and innocent story, but I personally don't trust code that AI generates without verifying it.
>
> [The creator of Clawd: "I ship code I don't read" at 00:36:49](https://newsletter.pragmaticengineer.com/p/the-creator-of-clawd-i-ship-code?t=2209s)

> AI-generated changes that saw no human input, just another AI code review, were very common during the last two months, across the codebase.
>
> [Why is Meta destroying its engineering organization?](https://newsletter.pragmaticengineer.com/p/why-is-meta-destroying-its-engineering)

## Support

Established: 4 independent sources support this principle.

Expert: Gergely Orosz

Topics: deterministic-guardrails, human-roles, processes

## Related principles

- [Gergely Orosz: Close the loop with mechanical validation](close-the-loop-with-mechanical-validation.md)
- [Gergely Orosz: Agents hide tech debt, so surface it and pay it down](agents-hide-tech-debt-so-surface-it-and-pay-it-down.md)
