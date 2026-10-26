# Rein in the agent with small, test-gated steps

Verified: 8 verbatim quotes from 4 sources

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: Track the share of agent commits made on a fully green suite, how often agent changes remove or weaken tests, and step size against revert rate.

An agent is fast, non-deterministic and sensitive to initial conditions, so control comes from inhibiting feedback loops: tests written before implementation, one at a time, and disciplines like test && commit || revert that keep only green changes, with a coverage floor to catch skipped tests. Every step must stay safe, though agents may safely take larger steps than a human would.

## Quotes

> So I'm gonna keep using tests because it makes sense to me to use tests. And I've had really bad experiences with the genie not using tests. or deleting tests or taking assertions out of tests.
>
> [Genie Session: Codex for Mac/GPUSortedMap at 00:14:01](https://newsletter.kentbeck.com/p/genie-session-codex-for-macgpusortedmap?t=841s)

> Okay, so before implementation, are there new tests to write that will catch likely errors question mark this is where this is me jostling a little bit the genie
>
> [Genie Session: Codex for Mac/GPUSortedMap at 00:12:46](https://newsletter.kentbeck.com/p/genie-session-codex-for-macgpusortedmap?t=766s)

> and the beauty of TCR is it creates incentives to make for two things, uh, make changes in small steps and everything always has to work.
>
> [Genie Sessions: TCR Skill at 00:05:05](https://newsletter.kentbeck.com/p/genie-sessions-tcr-skill?t=305s)

> We can get the genie to follow a TCR style. It does real TCR in the sense of having a big goal and then working on little pieces that are, as I said, monotonically increasing towards that eventual goal.
>
> [Genie Sessions: TCR Skill at 00:44:55](https://newsletter.kentbeck.com/p/genie-sessions-tcr-skill?t=2695s)

> if we get into a difficult situation are we going to find it uh just not writing tests it's just gonna plow ahead with an implementation that may or may not be correct and not have tests
>
> [Genie Sessions: TCR Skill at 00:47:10](https://newsletter.kentbeck.com/p/genie-sessions-tcr-skill?t=2830s)

> I think it's a terrible way to think about managing software development quality. But in this case, I just want to make sure that the genie hasn't cheated.
>
> [Genie Sessions: TCR Skill at 00:47:10](https://newsletter.kentbeck.com/p/genie-sessions-tcr-skill?t=2830s)

> So for example, a mystery to me is not passing 100% of the tests. I find that so valuable to just know, to have absolute certainty, to have total confidence.
>
> [Nobody Knows at 00:29:55](https://newsletter.kentbeck.com/p/nobody-knows?t=1795s)

> the only way you can get any control over it at all is by pulling in on the reins, slowing it down, creating some kind of inhibiting feedback loop that keeps it from just going, doing whatever it wants to do.
>
> [O11ycast | Ep. #80, Augmented Coding with Kent Beck | Heavybit](https://www.heavybit.com/library/podcasts/o11ycast/ep-80-augmented-coding-with-kent-beck)

## Support

Established: 4 independent sources support this principle.

Expert: Kent Beck

Topics: deterministic-guardrails, processes, techniques

## Related principles

- [Kent Beck: Verify what the agent did, not what it claims](verify-what-the-agent-did-not-what-it-claims.md)
- [Kent Beck: Make expectations explicit and let the agent observe real behaviour](make-expectations-explicit-and-let-the-agent-observe-real-behaviour.md)
- [Kent Beck: Slow down until trust catches up with code](slow-down-until-trust-catches-up-with-code.md)
