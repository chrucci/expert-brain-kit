# Review in the moment or monitor?

Status: open. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should humans review agent output as it arrives, or let agents run autonomously and step in only when needed?

Why open: Anthropic measured how experienced users behave, not whether autonomous runs produce less rework, and Böckeler's counterclaim is a single experience report.

## Sides
- **Birgitta Böckeler**: Deferring review on high-autonomy runs led to constant rework and late surprises, so understand output as it arrives.
  - "My experience with giving strong models lots of autonomy, and surrendering to them in a way, has often led to constant rework and surprises at later stages." ([source](https://martinfowler.com/articles/exploring-gen-ai/local-models-for-coding-experiences.html), [Birgitta Böckeler: Keep comprehension in the moment](../principles/bockeler/keep-comprehension-in-the-moment.md))
- **Anthropic engineering, Mitchell Hashimoto** (measured): Oversight means being able to see and intervene, not approving each step; agents can take more autonomy, and humans should check in on their own schedule.
  - "Experienced users are more likely to let Claude work autonomously, stepping in when something goes wrong or needs redirection." ([source](https://www.anthropic.com/research/measuring-agent-autonomy), [Anthropic engineering: Oversee by monitoring and clear handback points](../principles/anthropic/oversee-by-monitoring-and-clear-handback-points.md))
  - "Context switching is very expensive. In order to remain efficient, I found that it was my job as a human to be in control of when I interrupt the agent, not the other way around." ([source](https://mitchellh.com/writing/my-ai-adoption-journey), [Mitchell Hashimoto: An agent always runs in the background, on the human's schedule](../principles/hashimoto/an-agent-always-runs-in-the-background-on-the-human-s-schedule.md))

## Evidence to settle it
Assign comparable tasks to in-the-moment review and to autonomous runs with monitoring and handback points, then compare rework, late defects and human hours per task.

## Metric
Scoreboard: 30-day churn on AI-authored changes (`ai-churn-30d`). Compare 30-day churn on AI-authored lines from closely reviewed sessions against autonomous monitored sessions.

## Related principles
- [principles/bockeler/keep-comprehension-in-the-moment.md](../principles/bockeler/keep-comprehension-in-the-moment.md) - Birgitta Böckeler: Keep comprehension in the moment
- [principles/anthropic/oversee-by-monitoring-and-clear-handback-points.md](../principles/anthropic/oversee-by-monitoring-and-clear-handback-points.md) - Anthropic engineering: Oversee by monitoring and clear handback points
- [principles/hashimoto/an-agent-always-runs-in-the-background-on-the-human-s-schedule.md](../principles/hashimoto/an-agent-always-runs-in-the-background-on-the-human-s-schedule.md) - Mitchell Hashimoto: An agent always runs in the background, on the human's schedule
