# Can one person replace a team?

Status: open. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should a leader staff components with single agent-directing individuals, or keep stable multi-person teams?

Why open: Martin offers a conjecture and the counterpositions are experience reports, with no measured comparison.

## Sides
- **Robert C. Martin**: One human directing agents can do a five or six person team's work, so organise around individuals owning large components behind narrow interfaces.
  - "This is my wild conjecture, but it seems to me that a single human can now do the work of a team." ([source](https://www.aviator.co/podcast/uncle-bob-martin-ai-clean-code), [Robert C. Martin: One person can do a team's work behind narrow interfaces](../principles/unclebob/one-person-can-do-a-team-s-work-behind-narrow-interfaces.md))
- **Thoughtworks, Simon Willison, Kent Beck, Steve Yegge**: Teams shrink but not to one. A stable group must share the mental model and cognitive load, and people should keep working with people.
  - "If you take such a challenge, you need to shift from a traditional pre-AI era, classic agile product/IT team delivery model, otherwise it’s impossible to keep up and build the full feature set, even when using vibe coding tools like Lovable and coding assistants like Claude Code to expedite the development process." ([source](https://www.thoughtworks.com/insights/articles/making-sense-saaspocalypse), [Thoughtworks: Agents shrink and reshape teams, but not down to one person](../principles/thoughtworks/agents-shrink-and-reshape-teams-but-not-down-to-one-person.md))
  - "I can fire up four agents in parallel and have them work on four different problems. And by like 11 AM, I am wiped out for the day." ([source](https://simonwillison.net/2026/Apr/2/lennys-podcast/), [Simon Willison: Human cognitive capacity limits agents per person and team size](../principles/willison/human-cognitive-capacity-limits-agents-per-person-and-team-size.md))
  - Also: [Kent Beck: Keep humans working with humans](../principles/beck/keep-humans-working-with-humans.md), [Steve Yegge: Small, oversubscribed human teams](../principles/yegge/small-oversubscribed-human-teams.md)

## Evidence to settle it
Run comparable services with a solo owner and with a team of two or three for six months, tracking delivered functionality, incident recovery when the owner is away, and defects.

## Metric
Scoreboard: Failed deployment recovery time (`recovery-time`). Compare failed deployment recovery time, especially when the primary owner is unavailable, for solo-owned versus team-owned services.

## Related principles
- [principles/unclebob/one-person-can-do-a-team-s-work-behind-narrow-interfaces.md](../principles/unclebob/one-person-can-do-a-team-s-work-behind-narrow-interfaces.md) - Robert C. Martin: One person can do a team's work behind narrow interfaces
- [principles/thoughtworks/agents-shrink-and-reshape-teams-but-not-down-to-one-person.md](../principles/thoughtworks/agents-shrink-and-reshape-teams-but-not-down-to-one-person.md) - Thoughtworks: Agents shrink and reshape teams, but not down to one person
- [principles/willison/human-cognitive-capacity-limits-agents-per-person-and-team-size.md](../principles/willison/human-cognitive-capacity-limits-agents-per-person-and-team-size.md) - Simon Willison: Human cognitive capacity limits agents per person and team size
- [principles/beck/keep-humans-working-with-humans.md](../principles/beck/keep-humans-working-with-humans.md) - Kent Beck: Keep humans working with humans
- [principles/yegge/small-oversubscribed-human-teams.md](../principles/yegge/small-oversubscribed-human-teams.md) - Steve Yegge: Small, oversubscribed human teams
