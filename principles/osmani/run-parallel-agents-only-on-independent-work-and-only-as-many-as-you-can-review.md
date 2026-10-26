# Run parallel agents only on independent work, and only as many as you can review

Verified: 8 verbatim quotes from 16 sources

Dimension: Number of agents (agent-count)

Evidence: experience

How to measure: As concurrent agents per engineer rise, track merged-after-full-review output, merge conflicts, review latency and defects in late-session approvals, and find where they start to drop.

Parallel agents pay off only when the work splits into isolated slices, with no shared state, separate files and their own worktrees. Judgement-heavy work should stay serial. Even then, human attention does not parallelize: the useful number is about three to five agents per person, and falling review quality, not any fixed count, is the signal that the limit has been reached. Scale deeper before wider, and make environments reliable before running many agents.

## Quotes

> Pick this only when **independent** investigations can run in parallel and produce reports that a single agent then merges.
>
> [agent-skills: docs/agents.md](https://github.com/addyosmani/agent-skills/blob/main/docs/agents.md)

> The biggest bottleneck at this level is decomposition: defining the right slices to delegate.
>
> [Agentic Autonomy Levels | AddyOsmani.com](https://addyosmani.com/blog/agentic-autonomy-levels/)

> On some days I have five or ten sessions running, and I once caught myself asking the wrong project to add dark mode.
>
> [Agentic Skill Decay](https://addyosmani.com/blog/agentic-skill-decay/)

> Parallelism multiplies the bottleneck you already have. Automated verification can handle five checked changes. One senior reading every line gets a queue, fragmented attention, and eventually ceremonial approval.
>
> [Brownfield Agentic Engineering](https://addyosmani.com/blog/brownfield-agentic-engineering/)

> Agent teams add coordination overhead and use significantly more tokens than a single session. They work best when teammates can operate independently.
>
> [Claude Code Swarms | AddyOsmani.com](https://addyosmani.com/blog/claude-code-agent-teams/)

> Don't run more agents than you can meaningfully review. 3-5 is the sweet spot.
>
> [The Code Agent Orchestra - what makes multi-agent coding work | AddyOsmani.com](https://addyosmani.com/blog/code-agent-orchestra/)

> I’ve accepted that three focused, well-reviewed threads produce more usable output than six threads I’m half-supervising. Throughput looks better with six. Code I’m willing to actually merge without a second pass looks better with three.
>
> [Your parallel Agent limit | AddyOsmani.com](https://addyosmani.com/blog/cognitive-parallel-agents/)

> Parallel agents need to not step on each other. Virtually every serious tool in this space has landed on git worktrees (or similar) as the answer.
>
> [Is the IDE dead? | AddyOsmani.com](https://addyosmani.com/blog/death-of-the-ide/)

## Support

Established: 16 independent sources support this principle.

Expert: Addy Osmani

Topics: agent-count, human-roles, processes

## Related principles

- [Addy Osmani: Review capacity is the bottleneck, so size work to it](review-capacity-is-the-bottleneck-so-size-work-to-it.md)
- [Addy Osmani: Humans own the outer loop: intent, judgment and the ship decision](humans-own-the-outer-loop-intent-judgment-and-the-ship-decision.md)
