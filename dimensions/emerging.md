# Emerging ideas

Ideas about building human-agent engineering teams that fit none of the other dimensions.

## Where the experts agree
- Adopting agents is an organizational design problem as well as a tooling one. Leaders need to deliberately shape how people learn, share evidence and work alongside agents rather than leaving it to individual habits. ([Charity Majors: Pair individual experimentation with a central AI platform team](../principles/majors/pair-individual-experimentation-with-a-central-ai-platform-team.md), [Simon Willison: Connect AI enthusiasts and skeptics with shared feedback loops](../principles/willison/connect-ai-enthusiasts-and-skeptics-with-shared-feedback-loops.md), [Kent Beck: Protect rest when directing agents](../principles/beck/protect-rest-when-directing-agents.md))

## Open hypotheses
- When agents speed up delivery, longer human hours spent directing them lead to worse decisions, not more output. ([Kent Beck: Protect rest when directing agents](../principles/beck/protect-rest-when-directing-agents.md))
  - How to test it: Track weekly hours for the people directing agents alongside defect rates, rollbacks and reversed design decisions. Check whether the high-hour weeks show more of them.
- Shared feedback loops narrow the gap between AI enthusiasts and skeptics on the same team, so both groups end up with the same view of speed gains and of losses in reliability and system knowledge. ([Simon Willison: Connect AI enthusiasts and skeptics with shared feedback loops](../principles/willison/connect-ai-enthusiasts-and-skeptics-with-shared-feedback-loops.md))
  - How to test it: Survey both groups on speed, incidents and how well they understand the system. Compare the answers with delivery and reliability data, then repeat after a shared review of that data is in place to see whether the gap shrinks.
- Adoption goes better when engineers are expected to keep experimenting and a central enablement team owns the AI platform, tooling and shared practices, than when either side works alone. ([Charity Majors: Pair individual experimentation with a central AI platform team](../principles/majors/pair-individual-experimentation-with-a-central-ai-platform-team.md))
  - How to test it: Compare teams with and without a central platform owner on how quickly useful agent patterns spread between teams and how much duplicated tooling appears.

## Ideas worth a look
- The next bottleneck is probably not code. It is the console and click-through work around it, such as keys, DNS, OAuth setup and cloud settings, which agents cannot see or change. For a team building services and data pipelines, that means moving config, credentials provisioning and runbooks into text and commands an agent can read and run. Measure the share of delivery time spent on manual console steps, and agent task completion before and after the conversion. ([Andrej Karpathy: Make software and infrastructure legible to agents](../principles/karpathy/make-software-and-infrastructure-legible-to-agents.md))
- Treat rest for the people directing agents as a design constraint. Directing agents takes intense focus, and agent speed can quietly push people into longer days that hurt the insight good decisions depend on. ([Kent Beck: Protect rest when directing agents](../principles/beck/protect-rest-when-directing-agents.md))
