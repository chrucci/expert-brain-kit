# Does line-by-line human review stay?

Status: open. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should a human read every agent-written diff before it merges, or should human review move above the code and be planned away?

Why open: Both sides rest on experience and opinion, and no one has measured escaped defects for the two review modes side by side.

## Sides
- **Gergely Orosz, Simon Willison, Martin Fowler, Andrej Karpathy**: Keep an engaged human reviewer who reads agent code, with extra friction on critical services, because automation bias lets defects through once nobody reads.
  - "The good thing about friction is that it makes humans stop and think." ([source](https://newsletter.pragmaticengineer.com/p/building-pi-and-what-makes-self-modifying), [Gergely Orosz: Keep real human gates on agent changes, strongest on critical services](../principles/orosz/keep-real-human-gates-on-agent-changes-strongest-on-critical-services.md))
  - "The moment you ship your vibe coding code for other people to use, where your bugs might actually harm somebody else, that’s when you need to take a step back." ([source](https://simonwillison.net/2026/Apr/2/lennys-podcast/), [Simon Willison: A human vouches for agent output before others depend on it](../principles/willison/a-human-vouches-for-agent-output-before-others-depend-on-it.md))
  - Also: [Martin Fowler: Humans own and evaluate what agents build](../principles/fowler/humans-own-and-evaluate-what-agents-build.md), [Andrej Karpathy: Stay responsible for agent-written software](../principles/karpathy/stay-responsible-for-agent-written-software.md)
- **Robert C. Martin, Steve Yegge, Charity Majors**: Line-by-line review is slow and low value. Humans sign off on architecture, deployability and the running system, while machines and layered agent reviewers do the checking.
  - "The agents are not responsible for anything. They're entirely irresponsible. Only humans can be responsible, at the moment and probably over the next several years." ([source](https://www.aviator.co/podcast/uncle-bob-martin-ai-clean-code), [Robert C. Martin: Humans are responsible just above the code level](../principles/unclebob/humans-are-responsible-just-above-the-code-level.md))
  - "You can't work at agentic speeds and block everything with human reviews. Those are incompatible." ([source](https://yegge.ai/essays/the-shape-of-things-to-come/), [Steve Yegge: Scale review with layers of agentic review](../principles/yegge/scale-review-with-layers-of-agentic-review.md))
  - Also: [Charity Majors: Humans judge what to build; machines are the quality gate](../principles/majors/humans-judge-what-to-build-machines-are-the-quality-gate.md)

## Evidence to settle it
For one quarter, randomly route low and medium risk agent PRs to either full human line review or architecture and behaviour sign-off plus agentic review, and compare escaped defects, rollbacks and review hours per tier.

## Metric
Scoreboard: Change fail rate (`change-fail-rate`). Compare change fail rate between the two review arms within each risk tier; if the no-line-review arm holds steady while review latency drops, the second side wins for that tier.

## Related principles
- [principles/orosz/keep-real-human-gates-on-agent-changes-strongest-on-critical-services.md](../principles/orosz/keep-real-human-gates-on-agent-changes-strongest-on-critical-services.md) - Gergely Orosz: Keep real human gates on agent changes, strongest on critical services
- [principles/willison/a-human-vouches-for-agent-output-before-others-depend-on-it.md](../principles/willison/a-human-vouches-for-agent-output-before-others-depend-on-it.md) - Simon Willison: A human vouches for agent output before others depend on it
- [principles/fowler/humans-own-and-evaluate-what-agents-build.md](../principles/fowler/humans-own-and-evaluate-what-agents-build.md) - Martin Fowler: Humans own and evaluate what agents build
- [principles/karpathy/stay-responsible-for-agent-written-software.md](../principles/karpathy/stay-responsible-for-agent-written-software.md) - Andrej Karpathy: Stay responsible for agent-written software
- [principles/unclebob/humans-are-responsible-just-above-the-code-level.md](../principles/unclebob/humans-are-responsible-just-above-the-code-level.md) - Robert C. Martin: Humans are responsible just above the code level
- [principles/yegge/scale-review-with-layers-of-agentic-review.md](../principles/yegge/scale-review-with-layers-of-agentic-review.md) - Steve Yegge: Scale review with layers of agentic review
- [principles/majors/humans-judge-what-to-build-machines-are-the-quality-gate.md](../principles/majors/humans-judge-what-to-build-machines-are-the-quality-gate.md) - Charity Majors: Humans judge what to build; machines are the quality gate
