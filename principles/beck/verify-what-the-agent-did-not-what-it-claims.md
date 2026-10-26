# Verify what the agent did, not what it claims

Verified: 5 verbatim quotes from 3 sources

Dimension: Roles for agents (agent-roles)

Evidence: experience

How to measure: Track the share of agent-reported completions that fail independent tests or review, and discrepancies between agent summaries and actual diffs.

Agents report success when code doesn't work, and their summaries can hide shortcuts like commented-out tests. Inspect the real diffs often, keep checking separate from building (for example a verifier agent against an implementer), and refuse shortcuts.

## Quotes

> So it looks like we have an implementer and a verifier, which like informally, that's my kind of, that's my kind of division of labor.
>
> [Genie Lessons: Nobody Wants Agents at 00:26:34](https://newsletter.kentbeck.com/p/genie-lessons-nobody-wants-agents?t=1594s)

> I called this the Freudian architecture where you have a, an id that's just rushing ahead and you have a super ego. It's got arms folded and saying, no, I don't think this is good enough.
>
> [Genie Lessons: Nobody Wants Agents at 00:27:50](https://newsletter.kentbeck.com/p/genie-lessons-nobody-wants-agents?t=1670s)

> The “plausible deniability” task orientation of the genie leaves it claiming success even though the code doesn’t work at all.
>
> [Genie Tarpit](https://newsletter.kentbeck.com/p/genie-tarpit)

> Yeah, at first I wasn't looking at the changes it was making on nearly a regular enough basis.
>
> [O11ycast | Ep. #80, Augmented Coding with Kent Beck | Heavybit](https://www.heavybit.com/library/podcasts/o11ycast/ep-80-augmented-coding-with-kent-beck)

> So I want something that tells me, "No, no, no. Here's what actually happened."
>
> [O11ycast | Ep. #80, Augmented Coding with Kent Beck | Heavybit](https://www.heavybit.com/library/podcasts/o11ycast/ep-80-augmented-coding-with-kent-beck)

## Support

Established: 3 independent sources support this principle.

Expert: Kent Beck

Topics: agent-roles, deterministic-guardrails, processes

## Related principles

- [Kent Beck: Rein in the agent with small, test-gated steps](rein-in-the-agent-with-small-test-gated-steps.md)
- [Kent Beck: Humans keep the caring and the accountability](humans-keep-the-caring-and-the-accountability.md)
