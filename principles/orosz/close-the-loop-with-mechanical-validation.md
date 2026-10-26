# Close the loop with mechanical validation

Verified: 8 verbatim quotes from 7 sources

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: Measure the share of agent tasks that end with the agent running tests or builds, the share of production errors that trigger agent triage, and the rate of escaped defects as those shares rise.

Code suits agents because it can be compiled, linted, tested and run. Teams should design systems and choose harnesses so agents validate their own work, expand testing as diffs grow, and feed production errors back into the loop. When review volume outgrows humans, they should accept it and invest in validation rather than review theater.

## Quotes

> Tools that help agents get feedback – CLIs like Claude Code, Codex, and similar – have been a big boost.
>
> [Inside a five-year-old startup’s rapid AI makeover](https://newsletter.pragmaticengineer.com/p/ai-first-makeover-craft)

> I really like this point Armin made just a few seconds ago that AI works best when the engineer stays in the loop and the system can actually validate what changed.
>
> [Building Pi, and what makes self-modifying software so fascinating at 00:42:33](https://newsletter.pragmaticengineer.com/p/building-pi-and-what-makes-self-modifying?t=2553s)

> But with software, specifically SaaS and most software that we do, it's not done. When it's finished, we release it to production. And that's where it crashes, the bugs come out.
>
> [From Chrome DevTools to AI Engineering, with Addy Osmani at 01:06:45](https://newsletter.pragmaticengineer.com/p/from-chrome-devtools-to-ai-engineering?t=4005s)

> If in production it's not connected to how it's running and having that feedback, you see what I mean?
>
> [From Chrome DevTools to AI Engineering, with Addy Osmani at 01:07:17](https://newsletter.pragmaticengineer.com/p/from-chrome-devtools-to-ai-engineering?t=4037s)

> It also goes back a little bit to source codes being a liability, right? We're also seeing diffs increase and eventually opportunities for bugs will increase. In fact, probably bugs will increase unless you have more thorough testing.
>
> [Measuring the impact of AI on software engineering – with Laura Tacho at 00:53:04](https://newsletter.pragmaticengineer.com/p/measuring-the-impact-of-ai-on-software?t=3184s)

> As Peter explained, the reason AI is so good at coding, but often mediocre at writing, is because you can validate code.
>
> [The creator of Clawd: "I ship code I don't read" at 01:52:52](https://newsletter.pragmaticengineer.com/p/the-creator-of-clawd-i-ship-code?t=6772s)

> You need to verify it, right? That's what you're saying is verifying might not mean reviewing.
>
> [The programming language after Kotlin – with the creator of Kotlin at 01:31:08](https://newsletter.pragmaticengineer.com/p/the-programming-language-after-kotlin?t=5468s)

> Today at most companies, there is indeed a “theater of code reviews”. The fact is that no engineer can keep up with 5-10 times more code to review, so most don’t thoroughly review the code.
>
> [The state of the tech industry in 2026](https://newsletter.pragmaticengineer.com/p/the-state-of-the-tech-industry-in)

## Support

Established: 7 independent sources support this principle.

Expert: Gergely Orosz

Topics: deterministic-guardrails, processes, tools

## Related principles

- [Gergely Orosz: Keep real human gates on agent changes, strongest on critical services](keep-real-human-gates-on-agent-changes-strongest-on-critical-services.md)
- [Gergely Orosz: Steer agents with classic structure and organisational context](steer-agents-with-classic-structure-and-organisational-context.md)
