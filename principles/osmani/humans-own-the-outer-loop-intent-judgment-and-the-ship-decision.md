# Humans own the outer loop: intent, judgment and the ship decision

Verified: 8 verbatim quotes from 20 sources

Dimension: Roles for humans (human-roles)

Evidence: experience

How to measure: Check that every change merged to production has a named human owner and a recorded verdict with evidence, and that each critical subsystem has someone who can explain its recent changes.

Agents run the inner loop of investigating, implementing and testing. Humans own intent, architecture, the quality bar, the decision to ship, block or reject, and accountability for the result, and they put their review where automated checks are weak or the stakes are high. Agents can only guess at intent, so named people must hold the system's mental model and be able to explain and debug what ships.

## Quotes

> If you put a human check into a system that otherwise moves at machine speed, don’t be surprised if that impacts productivity.
>
> [Agentic Code Quality](https://addyosmani.com/blog/agentic-code-quality/)

> A model cannot be paged and cannot be held responsible for what it shipped, so whoever clicks merge owns it.
>
> [Agentic Code Review | AddyOsmani.com](https://addyosmani.com/blog/agentic-code-review/)

> Agentic engineering = AI does the implementation, human owns the architecture, quality, and correctness.
>
> [Agentic Engineering | AddyOsmani.com](https://addyosmani.com/blog/agentic-engineering/)

> You’ll be able to start writing up plans, refining plans, coming up with some definition for what done means, and also planning out for those places where humans are going to stay in the loop to check on correctness, safety, or user impact.
>
> [Agentic Skill Decay](https://addyosmani.com/blog/agentic-skill-decay/)

> Agents excel at anything with a tight evaluation function - where the agent can measure its own work.
>
> [The Code Agent Orchestra - what makes multi-agent coding work | AddyOsmani.com](https://addyosmani.com/blog/code-agent-orchestra/)

> **Use AI as first-pass reviewer, not final arbiter.** Treat AI review output as advisory - a dialog where one AI writes code, another reviews it, and the human orchestrates fixes.
>
> [Code Review in the Age of AI | AddyOsmani.com](https://addyosmani.com/blog/code-review-in-the-age-of-ai/)

> As AI volume goes up, the engineer who truly understands the system becomes more valuable, not less.
>
> [Comprehension Debt - the hidden cost of AI generated code. | AddyOsmani.com](https://addyosmani.com/blog/comprehension-debt/)

> The new loop looks like this: **specify intent -> delegate -> observe -> review diffs -> merge**.
>
> [Is the IDE dead? | AddyOsmani.com](https://addyosmani.com/blog/death-of-the-ide/)

## Support

Established: 20 independent sources support this principle.

Expert: Addy Osmani

Topics: human-roles, processes, skills

## Related principles

- [Addy Osmani: Build and protect engineering judgment on purpose](build-and-protect-engineering-judgment-on-purpose.md)
- [Addy Osmani: Let verification and risk set agent autonomy](let-verification-and-risk-set-agent-autonomy.md)
- [Addy Osmani: Start from a precise, human-approved spec and record intent](start-from-a-precise-human-approved-spec-and-record-intent.md)
