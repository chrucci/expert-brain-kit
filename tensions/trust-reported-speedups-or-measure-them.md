# Trust reported speedups or measure them?

Status: leaning. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should a leader resize and restructure teams on practitioner reports of large agent speedups, or only on controlled measurement of real work?

Why leaning: METR's randomized measurement shows perception overstates speedup, while the large-gain claims are estimates against pre-agent plans rather than controlled comparisons.

## Sides
- **METR, Gergely Orosz** (measured): Self-reports and forecasts are unreliable, even about direction; experienced developers on mature repos were measured 19% slower while believing they were faster.
  - "This gap between perception and reality is striking: developers expected AI to speed them up by 24%, and even after experiencing the slowdown, they still believed AI had sped them up by 20%." ([source](https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/), [METR: Measure AI speedup instead of trusting perception](../principles/metr/measure-ai-speedup-instead-of-trusting-perception.md))
  - "When developers are allowed to use AI tools, they take 19% longer to complete issues—a significant slowdown that goes against developer beliefs and expert forecasts." ([source](https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/), [METR: Tacit knowledge and implicit standards limit AI in mature codebases](../principles/metr/tacit-knowledge-and-implicit-standards-limit-ai-in-mature-codebases.md))
  - Also: [Gergely Orosz: Remove developer friction rather than optimising AI use](../principles/orosz/remove-developer-friction-rather-than-optimising-ai-use.md)
- **Thoughtworks, Steve Yegge**: Small agent-assisted teams have delivered work estimated for far larger teams, so projects can be staffed with fewer people now.
  - "If you take such a challenge, you need to shift from a traditional pre-AI era, classic agile product/IT team delivery model, otherwise it’s impossible to keep up and build the full feature set, even when using vibe coding tools like Lovable and coding assistants like Claude Code to expedite the development process." ([source](https://www.thoughtworks.com/insights/articles/making-sense-saaspocalypse), [Thoughtworks: Agents shrink and reshape teams, but not down to one person](../principles/thoughtworks/agents-shrink-and-reshape-teams-but-not-down-to-one-person.md))
  - "So now you see how the magic starts and ends. During Golden Ages, there is more work than people. And when they crash, it is because there are more people than work." ([source](https://steve-yegge.medium.com/the-anthropic-hive-mind-d01f768f3d7b?source=rss-c1ec701babb7------2), [Steve Yegge: Small, oversubscribed human teams](../principles/yegge/small-oversubscribed-human-teams.md))

## Evidence to settle it
Randomly assign scoped backlog tasks to AI-allowed and AI-disallowed conditions on the team's own codebase, record completion time, and compare with the developers' forecasts and estimates.

## Metric
Scoreboard: Change lead time (`lead-time`). Compare change lead time on randomized AI-allowed versus AI-disallowed tasks against the speedup engineers report on the trust survey; a gap means perception is driving decisions.

## Related principles
- [principles/metr/measure-ai-speedup-instead-of-trusting-perception.md](../principles/metr/measure-ai-speedup-instead-of-trusting-perception.md) - METR: Measure AI speedup instead of trusting perception
- [principles/metr/tacit-knowledge-and-implicit-standards-limit-ai-in-mature-codebases.md](../principles/metr/tacit-knowledge-and-implicit-standards-limit-ai-in-mature-codebases.md) - METR: Tacit knowledge and implicit standards limit AI in mature codebases
- [principles/orosz/remove-developer-friction-rather-than-optimising-ai-use.md](../principles/orosz/remove-developer-friction-rather-than-optimising-ai-use.md) - Gergely Orosz: Remove developer friction rather than optimising AI use
- [principles/thoughtworks/agents-shrink-and-reshape-teams-but-not-down-to-one-person.md](../principles/thoughtworks/agents-shrink-and-reshape-teams-but-not-down-to-one-person.md) - Thoughtworks: Agents shrink and reshape teams, but not down to one person
- [principles/yegge/small-oversubscribed-human-teams.md](../principles/yegge/small-oversubscribed-human-teams.md) - Steve Yegge: Small, oversubscribed human teams
