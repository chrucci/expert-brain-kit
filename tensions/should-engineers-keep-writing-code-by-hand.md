# Should engineers keep writing code by hand?

Status: open. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should engineers keep hand-writing and reshaping a meaningful share of code, or move almost entirely to directing, specifying and harness work?

Why open: Anthropic's measurement shows asking-for-explanations preserves skill as well as hand coding does, which leaves open whether hand writing itself is needed.

## Sides
- **Unmesh Joshi, Mitchell Hashimoto**: Humans should keep writing and reshaping code, because design is discovered by writing it and skills only grow in work not delegated.
  - "we cannot simply 'prompt' the LLMs to do the work. We make use of them, certainly, but we must iteratively drive the code to build the stable structure ourselves." ([source](https://martinfowler.com/articles/convo-what-how.html), [Unmesh Joshi: Humans keep writing code to discover design](../principles/joshi/humans-keep-writing-code-to-discover-design.md))
  - "Well, you're trading off: not forming skills for the tasks you're delegating to the agent while continuing to form skills naturally in the tasks you continue to work on manually." ([source](https://mitchellh.com/writing/my-ai-adoption-journey), [Mitchell Hashimoto: Delegate some work and keep doing the rest by hand to protect skills](../principles/hashimoto/delegate-some-work-and-keep-doing-the-rest-by-hand-to-protect-skills.md))
- **Charity Majors, Anthropic engineering, OpenAI engineering** (measured): The human job moves from typing code to deciding what to build, writing specs, interpreting production and improving the harness.
  - "There's a fantasy that AI will replace operators. Deploy the system, let it run itself, go home." ([source](https://www.honeycomb.io/blog/honeycomb-10-year-manifesto-part-1), [Charity Majors: Humans decide and make sense, close to production](../principles/majors/humans-decide-and-make-sense-close-to-production.md))
  - "On average, people make about 70% of the planning decisions but only 20% of the execution decisions (Figure 2)." ([source](https://www.anthropic.com/research/claude-code-expertise), [Anthropic engineering: Humans own the what, agents own the how](../principles/anthropic/humans-own-the-what-agents-own-the-how.md))
  - Also: [OpenAI engineering: Engineers own the harness and turn each agent failure into a lasting fix](../principles/openai/engineers-own-the-harness-and-turn-each-agent-failure-into-a-lasting-fix.md)

## Evidence to settle it
Compare modules where humans authored or refactored the structure with modules merged as generated, on later change lead time and readability, and run periodic debugging checks on engineers by how much they hand-code.

## Metric
Scoreboard: 30-day churn on AI-authored changes (`ai-churn-30d`). Compare 30-day churn on AI-authored changes in human-structured modules versus fully generated ones; higher churn in generated modules supports hand-shaping.

## Related principles
- [principles/joshi/humans-keep-writing-code-to-discover-design.md](../principles/joshi/humans-keep-writing-code-to-discover-design.md) - Unmesh Joshi: Humans keep writing code to discover design
- [principles/hashimoto/delegate-some-work-and-keep-doing-the-rest-by-hand-to-protect-skills.md](../principles/hashimoto/delegate-some-work-and-keep-doing-the-rest-by-hand-to-protect-skills.md) - Mitchell Hashimoto: Delegate some work and keep doing the rest by hand to protect skills
- [principles/majors/humans-decide-and-make-sense-close-to-production.md](../principles/majors/humans-decide-and-make-sense-close-to-production.md) - Charity Majors: Humans decide and make sense, close to production
- [principles/anthropic/humans-own-the-what-agents-own-the-how.md](../principles/anthropic/humans-own-the-what-agents-own-the-how.md) - Anthropic engineering: Humans own the what, agents own the how
- [principles/openai/engineers-own-the-harness-and-turn-each-agent-failure-into-a-lasting-fix.md](../principles/openai/engineers-own-the-harness-and-turn-each-agent-failure-into-a-lasting-fix.md) - OpenAI engineering: Engineers own the harness and turn each agent failure into a lasting fix
