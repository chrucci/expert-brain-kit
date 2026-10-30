# Do experts gain most or least?

Status: open. Verified: every side has a verbatim quote from a verified principle.

**Question:** Does AI help most in work the engineer already knows deeply, or in unfamiliar territory?

Why open: Both sides cite measurement but measure different things, speedup against a no-AI baseline versus agent output per instruction, so neither decides it.

## Sides
- **METR** (measured): AI helps least where the developer is already expert and most on unfamiliar code and small greenfield work, so be sceptical of it in code you know well.
  - "developers are slowed down more when they have high prior task exposure and lower external resource needs." ([source](https://arxiv.org/pdf/2507.09089#page=19), [METR: Expect AI to help most where you know least](../principles/metr/expect-ai-to-help-most-where-you-know-least.md))
- **Anthropic engineering, Gergely Orosz, Simon Willison** (measured): AI amplifies existing expertise, and the operator's domain knowledge multiplies what the agent accomplishes, so lean on experts and hire for depth.
  - "On the Claude Code engineering team, I’ve indexed heavily on two profiles. One is creative builders with product sense: the dreamers who are deeply curious and passionate about shipping products that solve problems." ([source](https://claude.com/resources/articles/running-an-ai-native-engineering-org), [Anthropic engineering: Staff for domain and product expertise, not throughput](../principles/anthropic/staff-for-domain-and-product-expertise-not-throughput.md))
  - "And I do have this belief that when you're working with AI, like as long as we're learning, I think we're fine. As long as we stop learning and outsource the learning to this thing, trouble will be brewing maybe, you know, months or years down the road." ([source](https://newsletter.pragmaticengineer.com/p/ai-skills-with-matt-pocock?t=2133s), [Gergely Orosz: Hire and grow for judgment, deep expertise and domain knowledge](../principles/orosz/hire-and-grow-for-judgment-deep-expertise-and-domain-knowledge.md))
  - Also: [Simon Willison: Agents amplify experience, and the skill is built by visible practice](../principles/willison/agents-amplify-experience-and-the-skill-is-built-by-visible-practice.md)

## Evidence to settle it
Tag each agent task with the engineer's self-rated familiarity and measure time to merge and rework against a no-agent baseline in each familiarity band.

## Metric
Scoreboard: Rework rate (`rework-rate`). Split rework rate and lead time for agent-assisted changes by author familiarity with the area; if high-familiarity changes gain least, the first side holds.

## Related principles
- [principles/metr/expect-ai-to-help-most-where-you-know-least.md](../principles/metr/expect-ai-to-help-most-where-you-know-least.md) - METR: Expect AI to help most where you know least
- [principles/anthropic/staff-for-domain-and-product-expertise-not-throughput.md](../principles/anthropic/staff-for-domain-and-product-expertise-not-throughput.md) - Anthropic engineering: Staff for domain and product expertise, not throughput
- [principles/orosz/hire-and-grow-for-judgment-deep-expertise-and-domain-knowledge.md](../principles/orosz/hire-and-grow-for-judgment-deep-expertise-and-domain-knowledge.md) - Gergely Orosz: Hire and grow for judgment, deep expertise and domain knowledge
- [principles/willison/agents-amplify-experience-and-the-skill-is-built-by-visible-practice.md](../principles/willison/agents-amplify-experience-and-the-skill-is-built-by-visible-practice.md) - Simon Willison: Agents amplify experience, and the skill is built by visible practice
