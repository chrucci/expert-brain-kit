# Must humans read every agent diff?

Status: open. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should a human read and approve agent code line by line, or move human attention to intent and design while automated and agentic checks validate the code?

Why open: Both sides rest on experience and opinion, and no one has compared the two review regimes on the same work.

## Sides
- **Gergely Orosz, Martin Fowler, Simon Willison**: Keep an engaged human reviewer on agent changes, with extra friction on critical services, because people stop reading once output looks fine a few times.
  - "The good thing about friction is that it makes humans stop and think." ([source](https://newsletter.pragmaticengineer.com/p/building-pi-and-what-makes-self-modifying), [Gergely Orosz: Keep real human gates on agent changes, strongest on critical services](../principles/orosz/keep-real-human-gates-on-agent-changes-strongest-on-critical-services.md))
  - "This is a profound change to the nature of programming, where humans oversee LLM agents who generate the code. Humans are still responsible for what the software does and how it works, but use different skills to create their products." ([source](https://martinfowler.com/bliki/AgenticProgramming.html), [Martin Fowler: Humans own and evaluate what agents build](../principles/fowler/humans-own-and-evaluate-what-agents-build.md))
  - Also: [Simon Willison: A human vouches for agent output before others depend on it](../principles/willison/a-human-vouches-for-agent-output-before-others-depend-on-it.md)
- **Robert C. Martin, Charity Majors, Steve Yegge, Thoughtworks**: Line-by-line review is slow and humans are poor validators. Check architecture, deployability and running behaviour, and let machines and layered agent review catch bugs.
  - "The agents are not responsible for anything. They're entirely irresponsible. Only humans can be responsible, at the moment and probably over the next several years." ([source](https://www.aviator.co/podcast/uncle-bob-martin-ai-clean-code), [Robert C. Martin: Humans are responsible just above the code level](../principles/unclebob/humans-are-responsible-just-above-the-code-level.md))
  - "Human brains are *not good* at validation. The nitpickiness, the repetition. This is the worst thing to be clinging to, y’all." ([source](https://charity.wtf/p/ai-demands-more-engineering-discipline), [Charity Majors: Humans judge what to build; machines are the quality gate](../principles/majors/humans-judge-what-to-build-machines-are-the-quality-gate.md))
  - Also: [Steve Yegge: Scale review with layers of agentic review](../principles/yegge/scale-review-with-layers-of-agentic-review.md), [Thoughtworks: Humans on the loop: fix the harness, not the artefact](../principles/thoughtworks/humans-on-the-loop-fix-the-harness-not-the-artefact.md)

## Evidence to settle it
Within one service tier, randomly route agent PRs either to full line-by-line human review or to deterministic gates plus agent review plus a human design check, and compare escaped defects, incidents and review hours over a quarter.

## Metric
Scoreboard: Change fail rate (`change-fail-rate`). Compare change fail rate for the two review arms per service tier; if the lighter arm holds the same fail rate while review latency falls, the second side gains ground.

## Related principles
- [principles/orosz/keep-real-human-gates-on-agent-changes-strongest-on-critical-services.md](../principles/orosz/keep-real-human-gates-on-agent-changes-strongest-on-critical-services.md) - Gergely Orosz: Keep real human gates on agent changes, strongest on critical services
- [principles/fowler/humans-own-and-evaluate-what-agents-build.md](../principles/fowler/humans-own-and-evaluate-what-agents-build.md) - Martin Fowler: Humans own and evaluate what agents build
- [principles/willison/a-human-vouches-for-agent-output-before-others-depend-on-it.md](../principles/willison/a-human-vouches-for-agent-output-before-others-depend-on-it.md) - Simon Willison: A human vouches for agent output before others depend on it
- [principles/unclebob/humans-are-responsible-just-above-the-code-level.md](../principles/unclebob/humans-are-responsible-just-above-the-code-level.md) - Robert C. Martin: Humans are responsible just above the code level
- [principles/majors/humans-judge-what-to-build-machines-are-the-quality-gate.md](../principles/majors/humans-judge-what-to-build-machines-are-the-quality-gate.md) - Charity Majors: Humans judge what to build; machines are the quality gate
- [principles/yegge/scale-review-with-layers-of-agentic-review.md](../principles/yegge/scale-review-with-layers-of-agentic-review.md) - Steve Yegge: Scale review with layers of agentic review
- [principles/thoughtworks/humans-on-the-loop-fix-the-harness-not-the-artefact.md](../principles/thoughtworks/humans-on-the-loop-fix-the-harness-not-the-artefact.md) - Thoughtworks: Humans on the loop: fix the harness, not the artefact
