# Agent-written tests are not proof of correctness

Verified: 8 verbatim quotes from 3 sources

Dimension: Deterministic guardrails (deterministic-guardrails)

Evidence: experience

How to measure: Track mutation score and surviving mutants alongside coverage for AI-tested code, and compare functional defect escape rates for changes validated only by agent-written tests against changes checked against human-written specifications.

A green, high-coverage suite that the agent wrote, or a red test that the agent confirmed itself, does not show that the behaviour is right. Humans must own clear specifications and check them, and because nobody will review every AI-written test, mutation testing should show whether those tests actually catch broken code.

## Quotes

> When the agent both writes the test and confirms it failed, a red test tells you the agent ran it and saw failure, not that the failure was for the right reason.
>
> [TDD inside the agent loop - theater or actual value?](https://martinfowler.com/articles/exploring-gen-ai/tdd-in-the-agent-loop.html)

> Without a human checkpoint between the two, is there really any purpose left to writing the test first?
>
> [TDD inside the agent loop - theater or actual value?](https://martinfowler.com/articles/exploring-gen-ai/tdd-in-the-agent-loop.html)

> That is theoretically shifting to when we are writing the specs to give to an agent, but we don't have a TDD-like mechanism there that lets us think the spec through in small steps.
>
> [TDD inside the agent loop - theater or actual value?](https://martinfowler.com/articles/exploring-gen-ai/tdd-in-the-agent-loop.html)

> This approach puts a lot of faith into the AI-generated tests, that's not good enough yet.
>
> [Harness engineering for coding agent users](https://martinfowler.com/articles/harness-engineering.html)

> Correctness is outside any sensor's remit if the human didn't clearly specify what they wanted in the first place.
>
> [Harness engineering for coding agent users](https://martinfowler.com/articles/harness-engineering.html)

> Neither catches reliably some of the higher-impact problems: Misdiagnosis of issues, overengineering and unnecessary features, misunderstood instructions.
>
> [Harness engineering for coding agent users](https://martinfowler.com/articles/harness-engineering.html)

> I acknowledge the reality that it is unrealistic to think that human review of all tests is sustainable, and it's unrealistic to think that people will actually do it.
>
> [Maintainability sensors for coding agents](https://martinfowler.com/articles/sensors-for-coding-agents.html)

> acceptance tests increase coverage, but are often not very assertion-heavy, giving us a false sense of security in test effectiveness — mutation testing helps us monitor that gap.
>
> [Maintainability sensors for coding agents](https://martinfowler.com/articles/sensors-for-coding-agents.html)

## Support

Established: 3 independent sources support this principle.

Expert: Birgitta Böckeler

Topics: deterministic-guardrails, human-roles, metrics

## Related principles

- [Birgitta Böckeler: Verify outcomes instead of prescribing the agent's process](verify-outcomes-instead-of-prescribing-the-agent-s-process.md)
- [Birgitta Böckeler: Pair guides with fast, self-correcting sensors](pair-guides-with-fast-self-correcting-sensors.md)
