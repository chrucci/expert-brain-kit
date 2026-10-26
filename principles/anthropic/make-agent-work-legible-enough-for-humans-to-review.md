# Make agent work legible enough for humans to review

Verified: 6 verbatim quotes from 1 source

Dimension: Processes (processes)

Evidence: experience

How to measure: Compare how often reviewers open, comment on or reject agent plans and PRs, and how many defects they miss, with and without agent-generated review artifacts.

As agents produce longer plans, specs and diffs, humans stop reading them closely. Have agents present plans, PR explanations and findings as structured, visual artifacts aimed at what the reviewer knows least, and build throwaway editors that feed human choices straight back to the agent, so people stay engaged with the agent's decisions.

## Quotes

> As Claude takes on more, I'd noticed I was reading plans less closely, and I wanted a way to stay engaged with its choices rather than just hand them off.
>
> [Using Claude Code: The unreasonable effectiveness of HTML](https://claude.dev/blog/using-claude-code-the-unreasonable-effectiveness-of-html/)

> I’ve found that I tend to not actually read more than a 100-line Markdown file, and I certainly am not able to get anyone else in my organization to read it.
>
> [Using Claude Code: The unreasonable effectiveness of HTML](https://claude.dev/blog/using-claude-code-the-unreasonable-effectiveness-of-html/)

> The chance of someone actually reading your spec, report, or PR writeup is much higher if it’s in HTML.
>
> [Using Claude Code: The unreasonable effectiveness of HTML](https://claude.dev/blog/using-claude-code-the-unreasonable-effectiveness-of-html/)

> Use HTML to understand code that the agent has written, to review code, or to explain a PR to someone reviewing your code.
>
> [Using Claude Code: The unreasonable effectiveness of HTML](https://claude.dev/blog/using-claude-code-the-unreasonable-effectiveness-of-html/)

> I'll often ask Claude to build me a throwaway editor for the exact thing I'm working on: not a product, or a reusable tool, but a single HTML file, purpose-built for this one piece of data.
>
> [Using Claude Code: The unreasonable effectiveness of HTML](https://claude.dev/blog/using-claude-code-the-unreasonable-effectiveness-of-html/)

> The trick is always to end with an export: a "copy as JSON" or "copy as prompt" button that turns whatever I did in the UI back into something I can paste into Claude Code or commit to a file.
>
> [Using Claude Code: The unreasonable effectiveness of HTML](https://claude.dev/blog/using-claude-code-the-unreasonable-effectiveness-of-html/)

## Support

Candidate: one source supports this principle so far.

Expert: Anthropic engineering

Topics: human-roles, processes, techniques

## Related principles

- [Anthropic engineering: Agents review first, humans approve by risk](agents-review-first-humans-approve-by-risk.md)
- [Anthropic engineering: Agree the plan and testable criteria before agents build](agree-the-plan-and-testable-criteria-before-agents-build.md)
