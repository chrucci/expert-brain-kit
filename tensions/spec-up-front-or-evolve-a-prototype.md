# Spec up front or evolve a prototype?

Status: open. Verified: every side has a verbatim quote from a verified principle.

**Question:** Should agent work start from a human-approved spec and plan, or from a shared prototype evolved in short visible cycles?

Why open: All positions rest on experience or opinion, and none measures the two approaches on similar work.

## Sides
- **Addy Osmani, Thoughtworks, Gergely Orosz**: Agents should build from a precise, approved spec and staged design checkpoints, because ambiguity multiplies across agents.
  - "To enforce strict skill compliance (e.g. requiring a spec or plan before writing code), copy or link `AGENTS.md` into the root of your workspace." ([source](https://github.com/addyosmani/agent-skills/blob/main/docs/antigravity-setup.md), [Addy Osmani: Start from a precise, human-approved spec and record intent](../principles/osmani/start-from-a-precise-human-approved-spec-and-record-intent.md))
  - "The approach remained similar: break down the task into smaller chunks. For each of the chunks I asked Windsurf to come up with a plan first before asking for an implementation." ([source](https://martinfowler.com/articles/exploring-gen-ai/ccmenu-quality.html), [Thoughtworks: Design and confirm intent in small staged steps](../principles/thoughtworks/design-and-confirm-intent-in-small-staged-steps.md))
  - Also: [Gergely Orosz: Settle intent and design before agents build](../principles/orosz/settle-intent-and-design-before-agents-build.md)
- **Steve Yegge**: At agent speed, evolve a living prototype in the open instead of writing a big upfront spec.
  - "They’re also the ones that told me you need full transparency at all times, at their speeds, or nobody will ever see what you are doing and you’ll fall irretrievably behind." ([source](https://steve-yegge.medium.com/the-anthropic-hive-mind-d01f768f3d7b?source=rss-c1ec701babb7------2), [Steve Yegge: Build in the open around a living prototype](../principles/yegge/build-in-the-open-around-a-living-prototype.md))
- **Kent Beck**: Whether spec-first fits depends on whether the software is a one-off or must keep paying for its next step, so decide that first.
  - "Spec-driven or not spec-driven is *not* the question. The first question is, “What game are we playing?”" ([source](https://newsletter.kentbeck.com/p/earn-and-learn), [Kent Beck: Decide which game you are playing before choosing a method](../principles/beck/decide-which-game-you-are-playing-before-choosing-a-method.md))

## Evidence to settle it
Label features as one-off or long-lived, run comparable features spec-first and prototype-first, and compare idea-to-ship time, rework and later rewrite rates.

## Metric
Scoreboard: Rework rate (`rework-rate`). Compare rework rate for spec-first versus prototype-first features, split by one-off versus long-lived work.

## Related principles
- [principles/osmani/start-from-a-precise-human-approved-spec-and-record-intent.md](../principles/osmani/start-from-a-precise-human-approved-spec-and-record-intent.md) - Addy Osmani: Start from a precise, human-approved spec and record intent
- [principles/thoughtworks/design-and-confirm-intent-in-small-staged-steps.md](../principles/thoughtworks/design-and-confirm-intent-in-small-staged-steps.md) - Thoughtworks: Design and confirm intent in small staged steps
- [principles/orosz/settle-intent-and-design-before-agents-build.md](../principles/orosz/settle-intent-and-design-before-agents-build.md) - Gergely Orosz: Settle intent and design before agents build
- [principles/yegge/build-in-the-open-around-a-living-prototype.md](../principles/yegge/build-in-the-open-around-a-living-prototype.md) - Steve Yegge: Build in the open around a living prototype
- [principles/beck/decide-which-game-you-are-playing-before-choosing-a-method.md](../principles/beck/decide-which-game-you-are-playing-before-choosing-a-method.md) - Kent Beck: Decide which game you are playing before choosing a method
