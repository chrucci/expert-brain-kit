# Keep agent changes small so verification stays fast

Verified: 6 verbatim quotes from 1 source

Dimension: Processes (processes)

Evidence: experience

How to measure: Track median human review time and defect escape rate for agent changes bucketed by diff size, and drift for runs with and without a reviewed intermediate artifact.

The AI generates and the human verifies, and the human is the bottleneck, so the goal is to make that loop as fast as possible. Work in small, concrete increments or with auditable intermediate artifacts rather than huge diffs, and use visual review interfaces.

## Quotes

> we we're now kind of like cooperating with AIS and usually they are doing the generation and we as humans are doing the verification. It is in our interest to make this loop go as fast as possible.
>
> [Andrej Karpathy: Software Is Changing (Again) at 00:22:00](https://www.youtube.com/watch?v=LCEmiRjPEtQ&t=1320s)

> I have to make sure that this thing is not introducing bugs. It's just like and that it's doing the correct thing, right?
>
> [Andrej Karpathy: Software Is Changing (Again) at 00:23:07](https://www.youtube.com/watch?v=LCEmiRjPEtQ&t=1387s)

> And in my own work, I'm always scared to get way too big diffs. I always go in small incremental chunks. I want to make sure that everything is good.
>
> [Andrej Karpathy: Software Is Changing (Again) at 00:23:40](https://www.youtube.com/watch?v=LCEmiRjPEtQ&t=1420s)

> I want to spin this loop very very fast and um I sort of work on small chunks of single concrete thing.
>
> [Andrej Karpathy: Software Is Changing (Again) at 00:23:40](https://www.youtube.com/watch?v=LCEmiRjPEtQ&t=1420s)

> And in both cases, we now have this intermediate artifact of a course that is auditable and we can make sure it's good.
>
> [Andrej Karpathy: Software Is Changing (Again) at 00:25:16](https://www.youtube.com/watch?v=LCEmiRjPEtQ&t=1516s)

> the AI is kept on the leash with respect to a certain syllabus, a certain like um progression of projects and so on.
>
> [Andrej Karpathy: Software Is Changing (Again) at 00:25:16](https://www.youtube.com/watch?v=LCEmiRjPEtQ&t=1516s)

## Support

Candidate: one source supports this principle so far.

Expert: Andrej Karpathy

Topics: deterministic-guardrails, human-roles, processes

## Related principles

- [Andrej Karpathy: Write concrete prompts that state the goal](write-concrete-prompts-that-state-the-goal.md)
- [Andrej Karpathy: Turn up autonomy gradually with an autonomy slider](turn-up-autonomy-gradually-with-an-autonomy-slider.md)
