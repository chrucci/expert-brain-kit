# Should humans keep writing code?

Status: open. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should engineers keep hand-writing and reshaping code, or move entirely to specifying, judging and validating?

Why open: Anthropic measured that delegated learning hurts comprehension but that asking for explanations preserves it, which does not show whether hand-writing code is needed.

## Sides
- **Unmesh Joshi, Mitchell Hashimoto**: Reviewing generated code rarely forces design thinking, so developers should keep writing some code by hand to discover design and preserve skills.
  - "we cannot simply 'prompt' the LLMs to do the work. We make use of them, certainly, but we must iteratively drive the code to build the stable structure ourselves." ([source](https://martinfowler.com/articles/convo-what-how.html), [Unmesh Joshi: Humans keep writing code to discover design](../principles/joshi/humans-keep-writing-code-to-discover-design.md))
  - "Well, you're trading off: not forming skills for the tasks you're delegating to the agent while continuing to form skills naturally in the tasks you continue to work on manually." ([source](https://mitchellh.com/writing/my-ai-adoption-journey), [Mitchell Hashimoto: Delegate some work and keep doing the rest by hand to protect skills](../principles/hashimoto/delegate-some-work-and-keep-doing-the-rest-by-hand-to-protect-skills.md))
- **Charity Majors, Anthropic engineering** (measured): Engineers' work moves from typing code to writing specs, running experiments, interpreting production and deciding what to build.
  - "There's a fantasy that AI will replace operators. Deploy the system, let it run itself, go home." ([source](https://www.honeycomb.io/blog/honeycomb-10-year-manifesto-part-1), [Charity Majors: Humans decide and make sense, close to production](../principles/majors/humans-decide-and-make-sense-close-to-production.md))
  - "On average, people make about 70% of the planning decisions but only 20% of the execution decisions (Figure 2)." ([source](https://www.anthropic.com/research/claude-code-expertise), [Anthropic engineering: Humans own the what, agents own the how](../principles/anthropic/humans-own-the-what-agents-own-the-how.md))

## Evidence to settle it
Give engineers periodic debugging and design-explanation checks, and compare scores and later change lead time for those who keep hand-authoring part of their work against those who fully delegate.

## Metric
Share of engineers who can correctly explain and safely change recently agent-written core modules without agent help, split by whether they still hand-author code.

## Related principles
- [principles/joshi/humans-keep-writing-code-to-discover-design.md](../principles/joshi/humans-keep-writing-code-to-discover-design.md) - Unmesh Joshi: Humans keep writing code to discover design
- [principles/hashimoto/delegate-some-work-and-keep-doing-the-rest-by-hand-to-protect-skills.md](../principles/hashimoto/delegate-some-work-and-keep-doing-the-rest-by-hand-to-protect-skills.md) - Mitchell Hashimoto: Delegate some work and keep doing the rest by hand to protect skills
- [principles/majors/humans-decide-and-make-sense-close-to-production.md](../principles/majors/humans-decide-and-make-sense-close-to-production.md) - Charity Majors: Humans decide and make sense, close to production
- [principles/anthropic/humans-own-the-what-agents-own-the-how.md](../principles/anthropic/humans-own-the-what-agents-own-the-how.md) - Anthropic engineering: Humans own the what, agents own the how
