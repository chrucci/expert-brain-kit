# Upfront spec or living prototype?

Status: open. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should agent work start from a human-approved spec, or from a shared prototype evolved in short cycles?

Why open: All three positions rest on experience or opinion, and none has compared the approaches on the same kind of work.

## Sides
- **Addy Osmani, Thoughtworks**: Run agent work through gated phases of spec, plan and tasks with human approval before code, because spec quality is the biggest lever.
  - "To enforce strict skill compliance (e.g. requiring a spec or plan before writing code), copy or link `AGENTS.md` into the root of your workspace." ([source](https://github.com/addyosmani/agent-skills/blob/main/docs/antigravity-setup.md), [Addy Osmani: Start from a precise, human-approved spec and record intent](../principles/osmani/start-from-a-precise-human-approved-spec-and-record-intent.md))
  - "The approach remained similar: break down the task into smaller chunks. For each of the chunks I asked Windsurf to come up with a plan first before asking for an implementation." ([source](https://martinfowler.com/articles/exploring-gen-ai/ccmenu-quality.html), [Thoughtworks: Design and confirm intent in small staged steps](../principles/thoughtworks/design-and-confirm-intent-in-small-staged-steps.md))
- **Steve Yegge**: Evolve a shared, visible prototype in short cycles instead of a big upfront spec.
  - "They’re also the ones that told me you need full transparency at all times, at their speeds, or nobody will ever see what you are doing and you’ll fall irretrievably behind." ([source](https://steve-yegge.medium.com/the-anthropic-hive-mind-d01f768f3d7b?source=rss-c1ec701babb7------2), [Steve Yegge: Build in the open around a living prototype](../principles/yegge/build-in-the-open-around-a-living-prototype.md))
- **Kent Beck**: Spec-driven work suits one-off finish-line projects; long-lived systems need practices that keep paying for the next step, so decide which game first.
  - "Spec-driven or not spec-driven is *not* the question. The first question is, “What game are we playing?”" ([source](https://newsletter.kentbeck.com/p/earn-and-learn), [Kent Beck: Decide which game you are playing before choosing a method](../principles/beck/decide-which-game-you-are-playing-before-choosing-a-method.md))

## Evidence to settle it
Label projects as one-off or long-lived, assign spec-first or prototype-first, and compare idea-to-ship time, late intent rejections and rework over six months.

## Metric
Scoreboard: 30-day churn on AI-authored changes (`ai-churn-30d`). Compare 30-day churn on AI-authored lines for spec-first versus prototype-first work, split by one-off versus long-lived projects.

## Related principles
- [principles/osmani/start-from-a-precise-human-approved-spec-and-record-intent.md](../principles/osmani/start-from-a-precise-human-approved-spec-and-record-intent.md) - Addy Osmani: Start from a precise, human-approved spec and record intent
- [principles/thoughtworks/design-and-confirm-intent-in-small-staged-steps.md](../principles/thoughtworks/design-and-confirm-intent-in-small-staged-steps.md) - Thoughtworks: Design and confirm intent in small staged steps
- [principles/yegge/build-in-the-open-around-a-living-prototype.md](../principles/yegge/build-in-the-open-around-a-living-prototype.md) - Steve Yegge: Build in the open around a living prototype
- [principles/beck/decide-which-game-you-are-playing-before-choosing-a-method.md](../principles/beck/decide-which-game-you-are-playing-before-choosing-a-method.md) - Kent Beck: Decide which game you are playing before choosing a method
