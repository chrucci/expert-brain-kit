# Settle intent and design before agents build

Verified: 8 verbatim quotes from 3 sources

Dimension: Processes (processes)

Evidence: experience

How to measure: Compare rework, late intent rejections and security findings for agent work that started from an explicit human design or planning step against work handed straight to an agent.

Humans should make the key design decisions, especially sensitive ones like authentication and authorization, before agents write code. Use whiteboard sessions, agent-led interviews kept short enough to stay engaged, and planning scaled to the size of the work. Discussion of intent then moves out of pull-request review and into the step before coding.

## Quotes

> It forced me to make decisions that I know what decision to make when I think about it, but it is my decision.
>
> [AI Skills with Matt Pocock at 00:34:58](https://newsletter.pragmaticengineer.com/p/ai-skills-with-matt-pocock?t=2098s)

> So unlike when I tell the when you do the slash goal command, like build this and it goes off. And it makes all the decisions or most key decisions.
>
> [AI Skills with Matt Pocock at 00:34:58](https://newsletter.pragmaticengineer.com/p/ai-skills-with-matt-pocock?t=2098s)

> Now, in my case, I had a decent idea of what I wanted, but it's generally a terrible idea to let an agent improvise authentication and authorization as they would often do.
>
> [AI Skills with Matt Pocock at 00:36:57](https://newsletter.pragmaticengineer.com/p/ai-skills-with-matt-pocock?t=2217s)

> If it's something trivial, just build it. If it requires the team, like it's a team level scope, I mean, write a PRD, send it out to the team, maybe CC some other teams, but it's not a blocker.
>
> [AI Skills with Matt Pocock at 01:13:44](https://newsletter.pragmaticengineer.com/p/ai-skills-with-matt-pocock?t=4424s)

> If it's like a one-month project, like spend two days, like it's not a bad thing to spend like one or two days planning it
>
> [AI Skills with Matt Pocock at 01:13:44](https://newsletter.pragmaticengineer.com/p/ai-skills-with-matt-pocock?t=4424s)

> With AI code review, conversations about what the system should do still matter, and are probably best had before the code is written.
>
> [Building Codex with Tibo Sottiaux](https://newsletter.pragmaticengineer.com/p/building-codex-with-tibo-sottiaux)

> So maybe this helps crystallize where a discussion needs to happen versus where we did it because maybe we didn't have the type of tooling that we have right now.
>
> [Building Codex with Tibo Sottiaux at 00:49:08](https://newsletter.pragmaticengineer.com/p/building-codex-with-tibo-sottiaux?t=2948s)

> some of the, I guess, most productive sessions I've observed have been in person around the whiteboard where people, again, we're talking about like components, databases, networking connections, retry logics, whatever, you know, like these things you could describe or you could put it on a computer.
>
> [Design Engineering with Maggie Appleton at 00:27:40](https://newsletter.pragmaticengineer.com/p/design-engineering-with-maggie-appleton?t=1660s)

## Support

Established: 3 independent sources support this principle.

Expert: Gergely Orosz

Topics: agent-roles, human-roles, processes, techniques

## Related principles

- [Gergely Orosz: Engineers own areas, architecture and the release decision](engineers-own-areas-architecture-and-the-release-decision.md)
- [Gergely Orosz: Preserve the intent and decisions behind agent code](preserve-the-intent-and-decisions-behind-agent-code.md)
