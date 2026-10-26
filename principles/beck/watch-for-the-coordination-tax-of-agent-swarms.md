# Watch for the coordination tax of agent swarms

Verified: 4 verbatim quotes from 2 sources

Dimension: Number of agents (agent-count)

Evidence: experience

How to measure: Compare human monitoring and reconciliation time and merge conflicts per delivered change for one agent versus several in parallel, split by file versus overlapping.

If you end up tracking which agent does what and holding state the system should hold, the tool has handed you a coordination problem instead of solving yours. What you want is an outcome, so treat multi-agent setups as a means, be skeptical of several agents on one codebase, and run agents in parallel only when their work is split into separate files.

## Quotes

> I have never been able to get two agents working on the same code base at the same time without my head exploding. So definitely anti that.
>
> [Genie Lessons: Nobody Wants Agents at 00:25:38](https://newsletter.kentbeck.com/p/genie-lessons-nobody-wants-agents?t=1538s)

> I was managing it. Watching which agent was doing what. Wondering when to interrupt. Holding state in my head that the system should have been holding for me.
>
> [Genie Lessons: Nobody Wants Agents](https://newsletter.kentbeck.com/p/genie-lessons-nobody-wants-agents)

> Multi-agent is a feature. Outcome-orientation is the thing the feature is supposed to deliver. We keep getting those confused.
>
> [Genie Lessons: Nobody Wants Agents](https://newsletter.kentbeck.com/p/genie-lessons-nobody-wants-agents)

> Hey, I got two genies going at the same time. I have the hardest time getting two genies not to be stepping on each other's body parts.
>
> [Genie Sessions: Run, Right, and Fast for the Adaptive Radix Tree at 00:52:11](https://newsletter.kentbeck.com/p/run-right-and-fast-for-the-adaptive?t=3131s)

## Support

Established: 2 independent sources support this principle.

Expert: Kent Beck

Topics: agent-count, human-roles

## Related principles

- [Kent Beck: Keep agent changes to one cohesive file](keep-agent-changes-to-one-cohesive-file.md)
- [Kent Beck: Try many cheap attempts and keep the winners](try-many-cheap-attempts-and-keep-the-winners.md)
