# A human vouches for agent output before others depend on it

Verified: 8 verbatim quotes from 8 sources

Dimension: Roles for humans (human-roles)

Evidence: experience

How to measure: Track the share of agent-assisted PRs sent back for basic defects the author should have caught, and defects found by humans after the agent's own review.

Unreviewed vibe code is fine for prototypes and personal tools. Once other people depend on it, the engineer who directed the agent owns its quality and must review the code, the PR description and the result before asking reviewers or users to rely on it. Agent self-review doesn't count as acceptance, and shipping worse code with agents is a choice the team should fix.

## Quotes

> The moment you ship your vibe coding code for other people to use, where your bugs might actually harm somebody else, that’s when you need to take a step back.
>
> [Highlights from my conversation about agentic engineering on Lenny's Podcast](https://simonwillison.net/2026/Apr/2/lennys-podcast/)

> That first vibe-coded prototype worked great as a proof of concept, but they eventually made the decision to throw it away and start again from scratch.
>
> [Eight years of wanting, three months of building with AI](https://simonwillison.net/2026/Apr/5/building-with-ai/)

> Vibe coding is more useful in its original definition - we need a term to describe unreviewed, prototype-quality LLM-generated code that distinguishes it from code that the author has brought up to a production ready standard.
>
> [What is agentic engineering? - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/what-is-agentic-engineering/)

> **Don't file pull requests with code you haven't reviewed yourself**.
>
> [Anti-patterns: things to avoid - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/anti-patterns/)

> If adopting coding agents demonstrably reduces the quality of the code and features you are producing, you should address that problem directly: figure out which aspects of your process are hurting the quality of your output and fix them.
>
> [AI should help us produce better code - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/better-code/)

> Delivering new code has dropped in price to almost free... but delivering *good* code remains significantly more expensive than that.
>
> [Writing code is cheap now - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/code-is-cheap/)

> Despite reviewing screenshots during development Codex failed to spot and correct this bug.
>
> [Moonlight & Mayhem (Raccoon Heist by Codex + GPT-5.6 Sol Ultra)](https://simonwillison.net/2026/Aug/7/moonlight-mayhem/)

> Once I had finished cooking and judged it mostly feature-complete, I had Codex create a branch and open a pull request.
>
> [A new feature for my blog, built using my voice](https://simonwillison.net/2026/Oct/9/built-using-my-voice/)

## Support

Established: 8 independent sources support this principle.

Expert: Simon Willison

Topics: human-roles, processes

## Related principles

- [Simon Willison: Verify beyond line-by-line review, and earn trust in automated review](verify-beyond-line-by-line-review-and-earn-trust-in-automated-review.md)
- [Simon Willison: Agents must run their work and show evidence it works](agents-must-run-their-work-and-show-evidence-it-works.md)
