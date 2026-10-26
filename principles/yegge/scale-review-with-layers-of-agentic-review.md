# Scale review with layers of agentic review

Verified: 8 verbatim quotes from 4 sources

Dimension: Processes (processes)

Evidence: experience

How to measure: Compare escaped defects and time-to-merge as agentic review layers are added, and track the share of changes resolved without human touch.

Human approval of every diff can't keep up with agent speed. Treat reliability as a dial set by rounds of review, judges and backstops, never run a single agent on a real process, fan out parallel reviewers with a synthesis step, and automatically triage incoming changes. Fix and merge flawed contributions rather than sending them back. Human review is kept for now but should be planned away.

## Quotes

> You can't work at agentic speeds and block everything with human reviews. Those are incompatible.
>
> [The Shape of Things to Come, Part 1: The Continuous Thunderdome](https://yegge.ai/essays/the-shape-of-things-to-come/)

> Upshot: in the short term, yes, keep reviewing agent code.
>
> [The Shape of Things to Come, Part 1: The Continuous Thunderdome](https://yegge.ai/essays/the-shape-of-things-to-come/)

> Plan now for that day to arrive, and get ready to replace your human code review with many, many rounds of agentic code review.
>
> [The Shape of Things to Come, Part 1: The Continuous Thunderdome](https://yegge.ai/essays/the-shape-of-things-to-come/)

> Convoy formulas create multiple polecats (one per leg) + synthesis step
>
> [gastown: docs/reference.md](https://github.com/gastownhall/gastown/blob/main/docs/reference.md)

> `gt formula run` handles convoy dispatch directly, spawning parallel polecats
>
> [gastown: docs/reference.md](https://github.com/gastownhall/gastown/blob/main/docs/reference.md)

> Anyway, the workflow begins with the sheriff pulling descriptions of all open PRs, and categorizing them into easy-wins, fix-merge, and needs-review.
>
> [Vibe Maintainer](https://steve-yegge.medium.com/vibe-maintainer-a2273a841040?source=rss-c1ec701babb7------2)

> I have at least managed to automate all the easy stuff, which is about half the PRs, sometimes up to two thirds of them.
>
> [Vibe Maintainer](https://steve-yegge.medium.com/vibe-maintainer-a2273a841040?source=rss-c1ec701babb7------2)

> You should almost never deploy a single-agent pack for a real business process.
>
> [Welcome to Gas City](https://steve-yegge.medium.com/welcome-to-gas-city-57f564bb3607?source=rss-c1ec701babb7------2)

## Support

Established: 4 independent sources support this principle.

Expert: Steve Yegge

Topics: agent-count, human-roles, processes

## Related principles

- [Steve Yegge: Agents never land their own work: a gated merge queue decides](agents-never-land-their-own-work-a-gated-merge-queue-decides.md)
- [Steve Yegge: Humans keep judgment, taste and the final say](humans-keep-judgment-taste-and-the-final-say.md)
