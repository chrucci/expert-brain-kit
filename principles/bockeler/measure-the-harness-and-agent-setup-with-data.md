# Measure the harness and agent setup with data

Verified: 7 verbatim quotes from 3 sources

Dimension: Metrics (metrics)

Evidence: experience

How to measure: Run each candidate model, setting and harness several times on representative tasks recording pass rate, time and review effort, and track each sensor's failure rate over time from logged history.

Impressions from trying a setup by hand can contradict automated evals, so judge agent setups with repeated runs on the team's own tasks, weighing coding speed against review effort. Log every sensor check, so the history shows which sensors never fire, which fail often, and whether guides and models are improving.

## Quotes

> So I also did a few runs of my automated setup with reasoning off - and lo and behold, it's not only faster (which was to be expected), but also performed the same to slightly better!
>
> [Viability of local models for coding](https://martinfowler.com/articles/exploring-gen-ai/local-models-for-coding-factors.html)

> A good reminder that reasoning is not always necessary, and can sometimes even be counterproductive.
>
> [Viability of local models for coding](https://martinfowler.com/articles/exploring-gen-ai/local-models-for-coding-factors.html)

> Frustratingly, the automated setup did not confirm the manual experience.
>
> [Experiences with local models for coding](https://martinfowler.com/articles/exploring-gen-ai/local-models-for-coding-experiences.html)

> What is the balance like between speed of coding and review effort?
>
> [Experiences with local models for coding](https://martinfowler.com/articles/exploring-gen-ai/local-models-for-coding-experiences.html)

> So I started logging a history of sensor states every time they were checked, to get some data.
>
> [Maintainability sensors for coding agents](https://martinfowler.com/articles/sensors-for-coding-agents.html)

> If they're always green, that's suspicious, because they never catch anything.
>
> [Maintainability sensors for coding agents](https://martinfowler.com/articles/sensors-for-coding-agents.html)

> Which sensors are never failing? --> a signal that they are not necessary
>
> [Maintainability sensors for coding agents](https://martinfowler.com/articles/sensors-for-coding-agents.html)

## Support

Established: 3 independent sources support this principle.

Expert: Birgitta Böckeler

Topics: metrics, tools

## Related principles

- [Birgitta Böckeler: Pair guides with fast, self-correcting sensors](pair-guides-with-fast-self-correcting-sensors.md)
- [Birgitta Böckeler: Plan with strong models, execute narrow tasks with weaker ones](plan-with-strong-models-execute-narrow-tasks-with-weaker-ones.md)
