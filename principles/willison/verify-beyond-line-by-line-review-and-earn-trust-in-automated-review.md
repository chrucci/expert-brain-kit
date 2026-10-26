# Verify beyond line-by-line review, and earn trust in automated review

Verified: 8 verbatim quotes from 7 sources

Dimension: Processes (processes)

Evidence: experience

How to measure: Count confirmed defects found by cross-model and doc-first review that other review missed, and per code area compare escaped defects for code merged without line-by-line review against fully reviewed code.

Reading every line has never been the best way to validate a change. Willison has teams combine other checks: a model from another vendor reviewing the work, multi-model security audits, separate humans writing the test and the fix, and reading the agent's documentation diff first. Teams can relax human review only where the blast radius is small or the automated review has earned trust, and should watch for normalised deviance as unreviewed successes pile up.

## Quotes

> With this kind of project there’s always a major risk that the model might “cheat”—mark key features as “TODO” and fake them, or take shortcuts that ignore the initial requirements.
>
> [Extract PDF text in your browser with LiteParse for the web](https://simonwillison.net/2026/Apr/23/liteparse-for-the-web/)

> The responsible way to prevent this is to review all of the code... but this wasn’t intended as that kind of project, so instead I fired up OpenAI Codex with GPT-5.5 (I had preview access) and told it:
>
> [Extract PDF text in your browser with LiteParse for the web](https://simonwillison.net/2026/Apr/23/liteparse-for-the-web/)

> Sometimes this involves reviewing every line of code they have written, but there are other ways to achieve that goal.
>
> [More than just code review](https://simonwillison.net/2026/Aug/22/more-than-just-code-review/)

> I used to think that the idea of having one model review the work of another was somewhat absurd—it felt weirdly superstitious. The problem is *it really does work*
>
> [sqlite-utils 4.0rc2, mostly written by Claude Fable (for about $149.25)](https://simonwillison.net/2026/Jul/5/sqlite-utils-fable/)

> I had it write the documentation as well which gave me a very useful frame for reviewing the design—much of the iteration on the feature came from reviewing that documentation, spotting things that were redundant, inconsistent or confusing, and requesting (or dictating) a better design.
>
> [Have your agent record video demos of its work with shot-scraper video](https://simonwillison.net/2026/Jun/30/shot-scraper-video/)

> The problem is that as the coding agents get more reliable, I’m not reviewing every line of code that they write anymore, even for my production level stuff.
>
> [Vibe coding and agentic engineering are getting closer than I'd like](https://simonwillison.net/2026/May/6/vibe-coding-and-agentic-engineering/)

> and I ran an extensive audit of Datasette using Claude Fable 5.1, GPT-5.6, and GPT-6 Astra.
>
> [Datasette 1.0a39 and 0.65.4 security releases](https://simonwillison.net/2026/Sep/11/datasette-security/)

> So the key seems to be constantly iterating on the automated review systems themselves, in order to build trust in them over time.
>
> [A Fireside Chat with Cat and Thariq from the Claude Code team](https://simonwillison.net/2026/Jul/21/cat-and-thariq/)

## Support

Established: 7 independent sources support this principle.

Expert: Simon Willison

Topics: agent-roles, human-roles, processes

## Related principles

- [Simon Willison: A human vouches for agent output before others depend on it](a-human-vouches-for-agent-output-before-others-depend-on-it.md)
- [Simon Willison: Pay down cognitive debt on agent-written code](pay-down-cognitive-debt-on-agent-written-code.md)
