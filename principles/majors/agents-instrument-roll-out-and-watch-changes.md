# Agents instrument, roll out and watch changes

Verified: 8 verbatim quotes from 3 sources

Dimension: Roles for agents (agent-roles)

Evidence: opinion

How to measure: Track instrumentation coverage of merged changes, the share of releases going through agent-run staged rollouts, and regressions caught by scheduled agent checks.

Developer cognitive load is scarce, so agents should add instrumentation, check it in dev, dig through traces, run staged rollouts and watch risky changes for months afterwards. They should bring production signals, including which recent diff is a likely cause, to developers in their IDE or Slack.

## Quotes

> Agentic workflows are going to make these automated validation techniques much easier and more widely used; at the exact same time, agents developing to spec are going to require a dramatically higher degree of precision and automated validation in production.
>
> [Your Data Is Made Powerful By Context (so stop destroying it already)](https://charity.wtf/p/your-data-is-made-powerful-by-context)

> wouldn’t it be nice if your agentic task force could check up on any diffs that involve cache key or schema changes, say, once a day for the next 6-12 months?
>
> [Your Data Is Made Powerful By Context (so stop destroying it already)](https://charity.wtf/p/your-data-is-made-powerful-by-context)

> The cost of instrumentation has effectively fallen to zero, and AI models and agents are able to understand important patterns in your code and generalize from the patterns they know how to instrument.
>
> [“You Had One Job”: Why Twenty Years of DevOps Has Failed to Do it](https://www.honeycomb.io/blog/you-had-one-job-why-twenty-years-of-devops-has-failed-to-do-it)

> if your agentic harness can run your code in dev, inspect the output, verify that it’s working as expected, etc., then by the time you’re ready to merge your changes to production, you’ve already validated that the instrumentation can explain itself back to you from production.
>
> [“You Had One Job”: Why Twenty Years of DevOps Has Failed to Do it](https://www.honeycomb.io/blog/you-had-one-job-why-twenty-years-of-devops-has-failed-to-do-it)

> Instead of spending hours poring through traces, looking for outliers and suspicious symptoms… let your little buddy do that.
>
> [“You Had One Job”: Why Twenty Years of DevOps Has Failed to Do it](https://www.honeycomb.io/blog/you-had-one-job-why-twenty-years-of-devops-has-failed-to-do-it)

> Like cognitive load for developers is the scarcest resource in every R&D org.
>
> [O11ycast | Ep. #88, Metrics Are Good, Actually with Charity Majors | Heavybit](https://www.heavybit.com/library/podcasts/o11ycast/ep-88-metrics-are-good-actually-with-charity-majors)

> Just you're writing code and you don't have to do anything special to instrument. It does it for you. And you don't have to go look for the dashboards because the detail you need comes to you in your developer environment, your IDE, in Slack.
>
> [O11ycast | Ep. #88, Metrics Are Good, Actually with Charity Majors | Heavybit](https://www.heavybit.com/library/podcasts/o11ycast/ep-88-metrics-are-good-actually-with-charity-majors)

> It's checking in with you being like, does this look right? Does this look right? It knows the diffs that you've submitted over the past.
>
> [O11ycast | Ep. #88, Metrics Are Good, Actually with Charity Majors | Heavybit](https://www.heavybit.com/library/podcasts/o11ycast/ep-88-metrics-are-good-actually-with-charity-majors)

## Support

Established: 3 independent sources support this principle.

Expert: Charity Majors

Topics: agent-roles, tools

## Related principles

- [Charity Majors: Validation in production is the new bottleneck](validation-in-production-is-the-new-bottleneck.md)
- [Charity Majors: Keep telemetry wide and high-cardinality](keep-telemetry-wide-and-high-cardinality.md)
