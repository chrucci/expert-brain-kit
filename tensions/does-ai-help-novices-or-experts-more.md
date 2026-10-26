# Does AI help novices or experts more?

Status: open. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should a team point agents mainly at unfamiliar code and tasks, or at its deepest domain experts working in their own areas?

Why open: Both sides cite measurements, but they measure different things (speed versus verified success), so neither yet decides the staffing question.

## Sides
- **METR** (measured): AI help is worth most on unfamiliar tasks and small greenfield work and least where the developer is already an expert.
  - "developers are slowed down more when they have high prior task exposure and lower external resource needs." ([source](https://arxiv.org/pdf/2507.09089#page=19), [METR: Expect AI to help most where you know least](../principles/metr/expect-ai-to-help-most-where-you-know-least.md))
- **Anthropic engineering, Gergely Orosz, Simon Willison** (measured): Agents amplify existing expertise, so domain and systems experts get the most out of them and should be staffed and hired for.
  - "On the Claude Code engineering team, I’ve indexed heavily on two profiles. One is creative builders with product sense: the dreamers who are deeply curious and passionate about shipping products that solve problems." ([source](https://claude.com/resources/articles/running-an-ai-native-engineering-org), [Anthropic engineering: Staff for domain and product expertise, not throughput](../principles/anthropic/staff-for-domain-and-product-expertise-not-throughput.md))
  - "And I do have this belief that when you're working with AI, like as long as we're learning, I think we're fine. As long as we stop learning and outsource the learning to this thing, trouble will be brewing maybe, you know, months or years down the road." ([source](https://newsletter.pragmaticengineer.com/p/ai-skills-with-matt-pocock?t=2133s), [Gergely Orosz: Hire and grow for judgment, deep expertise and domain knowledge](../principles/orosz/hire-and-grow-for-judgment-deep-expertise-and-domain-knowledge.md))
  - Also: [Simon Willison: Agents amplify experience, and the skill is built by visible practice](../principles/willison/agents-amplify-experience-and-the-skill-is-built-by-visible-practice.md)

## Evidence to settle it
Break down agent-assisted task time and verified success by the engineer's prior exposure to the code, separating speed (METR's measure) from quality of outcome (Anthropic's measure).

## Metric
Verified task success rate and time-to-complete for agent-assisted work, split by the engineer's self-rated familiarity with the code area.

## Related principles
- [principles/metr/expect-ai-to-help-most-where-you-know-least.md](../principles/metr/expect-ai-to-help-most-where-you-know-least.md) - METR: Expect AI to help most where you know least
- [principles/anthropic/staff-for-domain-and-product-expertise-not-throughput.md](../principles/anthropic/staff-for-domain-and-product-expertise-not-throughput.md) - Anthropic engineering: Staff for domain and product expertise, not throughput
- [principles/orosz/hire-and-grow-for-judgment-deep-expertise-and-domain-knowledge.md](../principles/orosz/hire-and-grow-for-judgment-deep-expertise-and-domain-knowledge.md) - Gergely Orosz: Hire and grow for judgment, deep expertise and domain knowledge
- [principles/willison/agents-amplify-experience-and-the-skill-is-built-by-visible-practice.md](../principles/willison/agents-amplify-experience-and-the-skill-is-built-by-visible-practice.md) - Simon Willison: Agents amplify experience, and the skill is built by visible practice
