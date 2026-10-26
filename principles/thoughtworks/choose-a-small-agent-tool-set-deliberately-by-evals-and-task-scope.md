# Choose a small agent tool set deliberately, by evals and task scope

Verified: 8 verbatim quotes from 7 sources

Dimension: Tools (tools)

Evidence: experience

How to measure: Run a fixed eval set across candidate agents on a schedule, recording time, cost, error rates and run-to-run variance, and count AI tools in active use per engineer.

Pick coding agents with evals on cost, time, correctness and drift rather than by reputation, match each tool mode to the scope of the task, and keep the stack small so people build mastery instead of switching contexts. Plan for the tools from discovery so estimates and client approvals reflect them.

## Quotes

> Teams should always evaluate these tools using evals; doing so not only helps us measure how good our agents are over time, it also helps us assess which agents perform better for specific use cases.
>
> [Claude Code and COBOL modernization: What’s the reality?](https://www.thoughtworks.com/insights/articles/claude-code-cobol-modernization-reality)

> When you ask the same tool to do the same thing what variance do you see in the results? Is this variance impacting the other dimensions?
>
> [Claude Code and COBOL modernization: What’s the reality?](https://www.thoughtworks.com/insights/articles/claude-code-cobol-modernization-reality)

> Uncertainty won’t resolve before teams need to make decisions; waiting for the ecosystem to settle is itself a choice, and an increasingly expensive one.
>
> [The cognitive demands of AI novelty](https://www.thoughtworks.com/insights/blog/generative-ai/cognitive-demands-ai-novelty)

> Don't tie yourself to an IDE that forces you into their proprietary model. Use tools that allow you to swap your LLM provider with ease.
>
> [The dangers of token usage billing](https://www.thoughtworks.com/insights/blog/generative-ai/dangers-token-usage-billing)

> If you want to work on the repository as a whole, the CLI is fantastic. With a well-made plan (that the agent can also generate) it's able to work autonomously to upgrade configurations, research and modify code, refactor, run various command line tools, process the output and react accordingly.
>
> [GitHub Copilot and me: The evolution of my partnership with a coding assistant](https://www.thoughtworks.com/insights/blog/generative-ai/github-copilot-me-evolution-partnership-coding-assistant)

> technology leaders must conduct a comprehensive cognitive audit to assess which tools provide genuine, distinct value.
>
> [The paradox of acceleration: Overcoming AI-induced decision fatigue and business bottlenecks](https://www.thoughtworks.com/insights/blog/generative-ai/paradox-acceleration-overcoming-ai-decision-fatigue-bottlenecks)

> When designing agentic interfaces, creating an explicit capability API is vastly superior to forcing an agent to navigate legacy endpoints designed for human orchestration.
>
> [The primitive paradox: Reclaiming software discipline in an agentic world](https://www.thoughtworks.com/insights/blog/generative-ai/primitive-paradox-reclaiming-software-discipline-agentic-world)

> Finally, the project showed that AI tools should be factored in from the very beginning. By considering them during the discovery phase, teams can build realistic estimates, secure client approvals early, and avoid last-minute roadblocks
>
> [Unlocking Infrastructure as Code’s potential through AI](https://www.thoughtworks.com/insights/blog/generative-ai/unlocking-infrastructure-as-code-potential-through-ai)

## Support

Established: 7 independent sources support this principle.

Expert: Thoughtworks

Topics: metrics, tools

## Related principles

- [Thoughtworks: Measure internal quality and rework, not generation speed](measure-internal-quality-and-rework-not-generation-speed.md)
