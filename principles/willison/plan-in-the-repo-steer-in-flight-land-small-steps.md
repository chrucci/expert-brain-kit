# Plan in the repo, steer in flight, land small steps

Verified: 8 verbatim quotes from 5 sources

Dimension: Techniques (techniques)

Evidence: experience

How to measure: Compare rework, silently dropped requirements and review time for agent tasks started from a reviewed committed plan and delivered in small PRs against ad-hoc, large-PR tasks.

Have the agent write its plan or spec as a committed file and correct it before building, which catches scope it quietly cut. Then keep watching and redirecting the agent while it runs, and have it work in small commits and small PRs, so humans can follow and review the work.

## Quotes

> I always like to start with a plan for this kind of project.
>
> [Extract PDF text in your browser with LiteParse for the web](https://simonwillison.net/2026/Apr/23/liteparse-for-the-web/)

> in this case I knew I’d want the plan as an artifact in the repository so I told it to write `plan.md` directly.
>
> [Extract PDF text in your browser with LiteParse for the web](https://simonwillison.net/2026/Apr/23/liteparse-for-the-web/)

> I noticed that Claude had decided to punt on generating screenshots of images in the PDF, and suggested we defer a “canvas-encode swap” to v2.
>
> [Extract PDF text in your browser with LiteParse for the web](https://simonwillison.net/2026/Apr/23/liteparse-for-the-web/)

> I’ve started habitually asking for “small commits along the way” because it makes for code that’s easier to understand or review later on, and I have an unproven hunch that it helps the agent work more effectively too—it’s yet another encouragement towards planning and taking on one problem at a time.
>
> [Extract PDF text in your browser with LiteParse for the web](https://simonwillison.net/2026/Apr/23/liteparse-for-the-web/)

> I built this tool using README-driven-development: I carefully constructed the README describing exactly how the tool should work, then
>
> [scan-for-secrets 0.1](https://simonwillison.net/2026/Apr/5/scan-for-secrets-3/)

> The change is small enough to be reviewed efficiently without inflicting too much additional cognitive load on the reviewer.
>
> [Anti-patterns: things to avoid - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/anti-patterns/)

> When I'm working with Claude Code I usually keep an eye on what it's doing so I can redirect it while it's still in flight. I also often come up with new ideas while it's working which I then inject into the queue.
>
> [GIF optimization tool using WebAssembly and Gifsicle - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/gif-optimization/)

> I still switch back to typing once I get down to the details of things though.
>
> [A new feature for my blog, built using my voice](https://simonwillison.net/2026/Oct/9/built-using-my-voice/)

## Support

Established: 5 independent sources support this principle.

Expert: Simon Willison

Topics: human-roles, processes, techniques

## Related principles

- [Simon Willison: The codebase, its examples and its instructions are agent context](the-codebase-its-examples-and-its-instructions-are-agent-context.md)
- [Simon Willison: Automated tests are mandatory, and agents work test-first](automated-tests-are-mandatory-and-agents-work-test-first.md)
