# Code structure is a running cost of agent work

Verified: 8 verbatim quotes from 8 sources

Dimension: Techniques (techniques)

Evidence: measurement

How to measure: Record input tokens, output tokens and wall-clock time for a fixed representative change, run by a fresh sub-agent at each codebase checkpoint.

Well-factored code lets an agent read only the few files a change needs, and refactoring a 17K-line file cut input tokens for the same change by 83%. Teams can benchmark this repeatably by having a fresh agent run a fixed change at each checkpoint.

## Quotes

> The goal of refactoring an agentic code base is to spend tokens now in refactoring to make token consumption for future work lower.
>
> [The Economic Benefit of Refactoring](https://martinfowler.com/articles/exploring-gen-ai/refactoring-economic-benefit.html)

> the same traits making high-quality software understandable to humans also allow AIs to understand it more quickly. Therefore, building high-quality software enables the AI to move faster as well.
>
> [Quality is speed: Where engineering discipline moves in the AI era](https://www.thoughtworks.com/insights/articles/quality-is-speed-AI-era)

> The foundational principles of software engineering remain the same: clean code, testability and decoupled architecture.
>
> [Why AI is raising the stakes of the software engineering craft](https://www.thoughtworks.com/insights/blog/agile-engineering-practices/why-ai-raising-stakes-software-engineering-craft)

> The most valuable AI use case I've found isn't generating new code. It's helping teams understand, modernize and refactor the code they already have.
>
> [Generative ref-AI-ctoring: Solving tech debt in the age of AI](https://www.thoughtworks.com/insights/blog/generative-ai/generative-ai-refactoring)

> If the current codebase is messy or inconsistent, the AI will absorb and amplify that mess.
>
> [In the age of AI coding, code quality still matters](https://www.thoughtworks.com/insights/blog/generative-ai/in-the-age-of-AI-coding-code-quality-still-matters)

> An AI agent trying to implement a feature often lacks the holistic view required to connect the dots between Service A and Service B without hallucinating or breaking contracts.
>
> [The Ferrari in the jungle: AI-driven software development in large enterprises](https://www.thoughtworks.com/insights/blog/generative-ai/The-Ferrari-in-jungle-AI-driven-software-development-in-large-enterprises)

> I’ve seen agents make many more incorrect assumptions and outright mistakes when dealing with less legible codebases, which then requires human intervention.
>
> [Should we still design code for humans?](https://www.thoughtworks.com/insights/blog/programming-languages/should-still-design-code-humans)

> When an engineer works by updating a highly detailed specification and allows an LLM or agent to completely regenerate the application rather than line-patching it, the code behaves less like a permanent monument and more like a compiled binary.
>
> [Caught between ephemerality and materiality](https://www.thoughtworks.com/insights/blog/technology-strategy/caught-between-ephemerality-materiality-reflections-fose-europe)

## Support

Established: 8 independent sources support this principle.

Expert: Thoughtworks

Topics: metrics, processes, techniques

## Related principles

- [Thoughtworks: Experienced humans own design quality, intent and strategy](experienced-humans-own-design-quality-intent-and-strategy.md)
- [Thoughtworks: Measure internal quality and rework, not generation speed](measure-internal-quality-and-rework-not-generation-speed.md)
