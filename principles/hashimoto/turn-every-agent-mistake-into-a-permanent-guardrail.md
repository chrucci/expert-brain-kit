# Turn every agent mistake into a permanent guardrail

Verified: 6 verbatim quotes from 2 sources

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: Log each agent mistake and the guardrail added for it, then track whether that kind of mistake comes back and whether the touch-up rate on agent output falls.

Whenever an agent gets something wrong, change its environment so the mistake can't happen again. Small fixes go in AGENTS.md. Bigger ones become fast tools or tests the agent can run to find out it is wrong. Over time the harness, rather than human vigilance, keeps agents on track and cuts the touch-ups humans have to make.

## Quotes

> It is the idea that anytime you find an agent makes a mistake, you take the time to engineer a solution such that the agent never makes that mistake again.
>
> [My AI Adoption Journey](https://mitchellh.com/writing/my-ai-adoption-journey)

> The most sure-fire way to achieve this is to give the agent fast, high quality tools to automatically tell it when it is wrong.
>
> [My AI Adoption Journey](https://mitchellh.com/writing/my-ai-adoption-journey)

> Each line in that file is based on a bad agent behavior, and it almost completely resolved them all.
>
> [My AI Adoption Journey](https://mitchellh.com/writing/my-ai-adoption-journey)

> But AI is more goal oriented in terms of I want this feature to work this way that if it doesn't see a spec somewhere or a test somewhere that other things should work in a different way, it'll just break it on its path to its own goal.
>
> [Mitchell Hashimoto’s new way of writing code at 01:36:46](https://newsletter.pragmaticengineer.com/p/mitchell-hashimoto?t=5806s)

> which is that anytime you see AI do a bad thing, try to build tooling that it could have called out to, to have prevented that bad thing or course corrected that bad thing.
>
> [Mitchell Hashimoto’s new way of writing code at 01:37:23](https://newsletter.pragmaticengineer.com/p/mitchell-hashimoto?t=5843s)

> same thing I realized oh if it makes a mistake and I add that just to agents.md it never makes that mistake again
>
> [Mitchell Hashimoto’s new way of writing code at 01:48:13](https://newsletter.pragmaticengineer.com/p/mitchell-hashimoto?t=6493s)

## Support

Established: 2 independent sources support this principle.

Expert: Mitchell Hashimoto

Topics: deterministic-guardrails, techniques

## Related principles

- [Mitchell Hashimoto: Read-only triage agents, with a human choosing what agents implement](read-only-triage-agents-with-a-human-choosing-what-agents-implement.md)
