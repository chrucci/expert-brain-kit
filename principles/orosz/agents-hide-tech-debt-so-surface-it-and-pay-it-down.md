# Agents hide tech debt, so surface it and pay it down

Verified: 8 verbatim quotes from 3 sources

Dimension: Processes (processes)

Evidence: opinion

How to measure: Track workaround and TODO additions in agent PRs, complexity trends, and the volume and merge rate of agent refactoring PRs over time.

Agents don't feel a codebase's pain and quietly add hacks, so engineers who aren't working in the code stop noticing debt. Keep humans close to the code, and use the low cost of agent refactoring to clean up continuously, for example with nightly single-fix PRs that a human reviews.

## Quotes

> When a codebase gets too complex, the human engineer feels the issues this creates.
>
> [Building Pi, and what makes self-modifying software so fascinating at 01:31:44](https://newsletter.pragmaticengineer.com/p/building-pi-and-what-makes-self-modifying?t=5504s)

> And in a codebase where where devs regularly feel the pain of the code base and do something about it, the quality will probably be also better.
>
> [Building Pi, and what makes self-modifying software so fascinating at 01:32:20](https://newsletter.pragmaticengineer.com/p/building-pi-and-what-makes-self-modifying?t=5540s)

> fixes one issue or one anti-pattern, and opens one small pull request. The team wakes up to a codebase that's a little bit better every morning, and devs still need to review and approve it.
>
> [Context engineering with Dex Horthy at 01:31:34](https://newsletter.pragmaticengineer.com/p/context-engineering-with-dex-horthy?t=5494s)

> This is a practice that, honestly, any engineering team could just adopt today.
>
> [Context engineering with Dex Horthy at 01:31:34](https://newsletter.pragmaticengineer.com/p/context-engineering-with-dex-horthy?t=5494s)

> They don't even tell you I'm doing a hack. They don't even know it's doing a hack.
>
> [Building OpenCode with Dax Raad at 00:50:20](https://newsletter.pragmaticengineer.com/p/opencode?t=3020s)

> Now someone else is dealing with the consequences. The landmines are still there, they just won't blow up on you today, and we don't even pay attention to a lot of these landmines being placed by AI agents.
>
> [Building OpenCode with Dax Raad at 01:19:27](https://newsletter.pragmaticengineer.com/p/opencode?t=4767s)

> Now, the agent hides the hack, which skews devs’ judgment and results in less tech debt being cleaned up.
>
> [Building OpenCode with Dax Raad](https://newsletter.pragmaticengineer.com/p/opencode)

> Agents make refactoring across a codebase cheap: for example, ask an agent to implement a new pattern everywhere across the codebase. It’s very easy and cheap to clear up tech debt, today. So, do more of it!
>
> [Building OpenCode with Dax Raad](https://newsletter.pragmaticengineer.com/p/opencode)

## Support

Established: 3 independent sources support this principle.

Expert: Gergely Orosz

Topics: agent-roles, human-roles, processes

## Related principles

- [Gergely Orosz: Keep real human gates on agent changes, strongest on critical services](keep-real-human-gates-on-agent-changes-strongest-on-critical-services.md)
