# Can one person replace a team?

Status: open. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should a leader restructure toward individuals each owning large components with agents, or keep small multi-person teams that share the mental model?

Why open: The one-person claim is an explicit conjecture and the opposing side is experience, with no measured comparison.

## Sides
- **Robert C. Martin**: One human directing agents can do the work of five or six developers, so teams become individuals owning components behind narrow interfaces.
  - "This is my wild conjecture, but it seems to me that a single human can now do the work of a team." ([source](https://www.aviator.co/podcast/uncle-bob-martin-ai-clean-code), [Robert C. Martin: One person can do a team's work behind narrow interfaces](../principles/unclebob/one-person-can-do-a-team-s-work-behind-narrow-interfaces.md))
- **Thoughtworks, Simon Willison, Kent Beck**: Teams shrink but not to one. Several people are needed to share the cognitive load, hold the mental model and build trust through daily collaboration.
  - "If you take such a challenge, you need to shift from a traditional pre-AI era, classic agile product/IT team delivery model, otherwise it’s impossible to keep up and build the full feature set, even when using vibe coding tools like Lovable and coding assistants like Claude Code to expedite the development process." ([source](https://www.thoughtworks.com/insights/articles/making-sense-saaspocalypse), [Thoughtworks: Agents shrink and reshape teams, but not down to one person](../principles/thoughtworks/agents-shrink-and-reshape-teams-but-not-down-to-one-person.md))
  - "I can fire up four agents in parallel and have them work on four different problems. And by like 11 AM, I am wiped out for the day." ([source](https://simonwillison.net/2026/Apr/2/lennys-podcast/), [Simon Willison: Human cognitive capacity limits agents per person and team size](../principles/willison/human-cognitive-capacity-limits-agents-per-person-and-team-size.md))
  - Also: [Kent Beck: Keep humans working with humans](../principles/beck/keep-humans-working-with-humans.md)

## Evidence to settle it
Run comparable components with one owner plus agents against a team of two or three plus agents for six months, tracking functionality delivered, incident response time, defects and what happens when the solo owner is away.

## Metric
Scoreboard: Failed deployment recovery time (`recovery-time`). Compare failed deployment recovery time between solo-owned and team-owned components, alongside throughput, since bus-factor risk shows up first in recovery.

## Related principles
- [principles/unclebob/one-person-can-do-a-team-s-work-behind-narrow-interfaces.md](../principles/unclebob/one-person-can-do-a-team-s-work-behind-narrow-interfaces.md) - Robert C. Martin: One person can do a team's work behind narrow interfaces
- [principles/thoughtworks/agents-shrink-and-reshape-teams-but-not-down-to-one-person.md](../principles/thoughtworks/agents-shrink-and-reshape-teams-but-not-down-to-one-person.md) - Thoughtworks: Agents shrink and reshape teams, but not down to one person
- [principles/willison/human-cognitive-capacity-limits-agents-per-person-and-team-size.md](../principles/willison/human-cognitive-capacity-limits-agents-per-person-and-team-size.md) - Simon Willison: Human cognitive capacity limits agents per person and team size
- [principles/beck/keep-humans-working-with-humans.md](../principles/beck/keep-humans-working-with-humans.md) - Kent Beck: Keep humans working with humans
