# Principles v0: building trust as fast as code

## Purpose and how to read it

This is version 0 of a set of principles for building efficient teams of humans and AI agents. It is meant to be tested, not obeyed: each principle is a hypothesis drawn from what leading practitioners and researchers have published, and the scoreboard says what a pilot team would measure to find out whether it holds. Each principle names the experts behind it with one short verified quote each. Its status is established when two or more experts back it with a verified quote, candidate when one does and inferred when none does; empirical support says whether any of the evidence is a measurement rather than opinion or experience. Where the experts disagree, the question is listed under Tensions with the experiment that would settle it.

## The thesis

Agents let teams produce code faster than they produce trust, so a team must build a system of trust that keeps up with the rate at which it builds code. Every principle below is read through that question: does it let trust keep pace with code? Repeatable, deterministic checks are one mechanism, because evidence is what trust is built on. The scoreboard sets the rate at which a team builds trust next to the rate at which it builds code.

> "We're accumulating code faster than we are accumulating trust."
> - quoted by Kent Beck in ["Trust Factory"](https://newsletter.kentbeck.com/p/trust-factory)

## Principles

### 1. Enforce must-hold rules with deterministic gates

Anything that must always or never happen is enforced by compilers, linters, tests, hooks, permissions or CI gates, not by prompt text the model may ignore. When an agent repeats a mistake, the team turns the fix into a new gate, test or rule instead of patching the output by hand, and it does not remove gates once they are added.

Trust: Trust stops depending on how carefully someone reads each change because the system enforces the rules the same way on every change, and each failure leaves the gate set stronger for the next one.

Status: established. Empirical support: measured. Experts: Thoughtworks, Anthropic engineering, Steve Yegge, Birgitta Böckeler, OpenAI engineering, Charity Majors, Mitchell Hashimoto, Addy Osmani.

- Thoughtworks: "Agents produce better code when they can gauge the quality of the code they produce themselves rather than relying on us to check it for them." ([source](https://martinfowler.com/articles/exploring-gen-ai/humans-and-agents.html))
- Anthropic engineering: "We have type checkers. We have linters. We run the build. Claude is actually so good at writing lint rules." ([source](https://newsletter.pragmaticengineer.com/p/building-claude-code-with-boris-cherny?t=2656s))
- Steve Yegge: "Now rules go through a lifecycle, tightening each time they're re-violated: first custom, then advisories/warnings, then written law in the constitution that all agents must obey, and finally, mechanical enforcement: programs that refuse by policy, or observe and alert loudly." ([source](https://yegge.ai/essays/fences-not-sandboxes/))
- Birgitta Böckeler: "Once the agent gets all these instructions and guidance, execution still depends on how well the LLM interprets them!" ([source](https://martinfowler.com/articles/exploring-gen-ai/context-engineering-coding-agents.html))
- OpenAI engineering: "Keep rules concise, explain the behavior to flag and any safe path or exception, and reserve formatting and lint checks for CI." ([source](https://learn.chatgpt.com/docs/agent-configuration/agents-md))
- Charity Majors: "If you're debiting from this trust account and the creation of the code, it has to get built up somewhere else." ([source](https://newsletter.pragmaticengineer.com/p/stop-being-skeptical-about-ai-for?t=1633s))
- Mitchell Hashimoto: "It is the idea that anytime you find an agent makes a mistake, you take the time to engineer a solution such that the agent never makes that mistake again." ([source](https://mitchellh.com/writing/my-ai-adoption-journey))
- Addy Osmani: "The most important habit in harness engineering is treating agent mistakes as permanent signals." ([source](https://addyosmani.com/blog/agent-harness-engineering/))

### 2. Define done as a check that actually runs

Every agent task names a deterministic finish line the agent must run before handing work back, such as the test suite, the build, a script that calls the service endpoint, or a parity run of a pipeline against a trusted reference on real or replayed data. The agent's report of success counts for nothing without the execution evidence attached.

Trust: Reviewers start from proof that the change ran and behaved correctly, not from the agent's word, so confidence in each change is earned before anyone depends on it.

Status: established. Empirical support: measured. Experts: Anthropic engineering, OpenAI engineering, Simon Willison, Gergely Orosz, METR, Addy Osmani, Andrej Karpathy.

- Anthropic engineering: "Software is comparatively easy to test and review—you can run code and see if it works—which makes it easier to trust an agent and catch its mistakes." ([source](https://www.anthropic.com/research/measuring-agent-autonomy))
- OpenAI engineering: "Not letting the agent see its work by not giving details on how to best run build and test commands" ([source](https://learn.chatgpt.com/guides/best-practices))
- Simon Willison: "allowing them to test that code and iterate on it independently of turn-by-turn guidance from their human supervisor." ([source](https://simonwillison.net/2026/Feb/23/agentic-engineering-patterns/))
- Gergely Orosz: "Tools that help agents get feedback – CLIs like Claude Code, Codex, and similar – have been a big boost." ([source](https://newsletter.pragmaticengineer.com/p/ai-first-makeover-craft))
- METR: "fully autonomous AI agents using Claude 3.7 Sonnet can often correctly implement the core functionality of issues on several repositories that are included in our study, although they fail to fully satisfy all requirements (typically leaving out important documentation, failing linting/styling rules, and leaving out key unit or integration tests)." ([source](https://arxiv.org/pdf/2507.09089#page=12))
- Addy Osmani: "Every PR must pass: lint, type check, tests, build" ([source](https://github.com/addyosmani/agent-skills/blob/main/docs/copilot-setup.md))
- Andrej Karpathy: "But I had a Python implementation that I fully understand, and I’m just making sure I’m making a more efficient version of it, and I have tests so I feel safer doing that stuff." ([source](https://www.dwarkesh.com/p/andrej-karpathy))

### 3. Prove your tests catch broken code

The team does not read a green, high-coverage suite as proof, especially when the agent wrote it. It uses mutation testing, deliberately broken inputs and contract tests for every API or schema clause to show the tests fail when they should, and it watches for agents deleting or weakening tests and assertions.

Trust: Gates that have been shown to fail on bad code are gates the team can lean on, so automated checks earn trust rather than borrowing it.

Status: established. Empirical support: unmeasured. Experts: Birgitta Böckeler, Unmesh Joshi, Robert C. Martin, Kent Beck.

- Birgitta Böckeler: "When the agent both writes the test and confirms it failed, a red test tells you the agent ran it and saw failure, not that the failure was for the right reason." ([source](https://martinfowler.com/articles/exploring-gen-ai/tdd-in-the-agent-loop.html))
- Unmesh Joshi: "This is also why generating test cases with LLMs to improve “test coverage” is not something I find very useful." ([source](https://martinfowler.com/articles/convo-what-how.html))
- Robert C. Martin: "The normal run proves that the project satisfies the feature. The mutation run checks whether the acceptance tests fail when important example values change." ([source](https://github.com/unclebob/Acceptance-Pipeline-Specification/blob/main/README.md))
- Kent Beck: "So I'm gonna keep using tests because it makes sense to me to use tests. And I've had really bad experiences with the genie not using tests. or deleting tests or taking assertions out of tests." ([source](https://newsletter.kentbeck.com/p/genie-session-codex-for-macgpusortedmap?t=841s))

### 4. Name an accountable human for every agent change

Every agent-produced change, service and pipeline has a named engineer who owns its quality, decides whether it ships and answers for it in production. Agent work is attributed to the agent and the owner, and the engineers who support a system help set the conditions under which agent code ships into it.

Trust: Trust needs someone who can be held to it, and a named owner keeps the quality bar from quietly dropping as the share of agent-written code grows.

Status: established. Empirical support: measured. Experts: Andrej Karpathy, Kent Beck, Martin Fowler, Addy Osmani, Simon Willison, Gergely Orosz, Anthropic engineering, Charity Majors, Robert C. Martin, Steve Yegge.

- Andrej Karpathy: "Agentic engineering is about preserving the quality bar of professional software. You are not allowed to introduce vulnerabilities because of vibe coding. You are still responsible for your software, just as before." ([source](https://karpathy.bearblog.dev/sequoia-ascent-2026/))
- Kent Beck: "This one is about what stays with us. Who cares whether the work is good? Who is accountable when it goes wrong?" ([source](https://newsletter.kentbeck.com/p/how-do-you-know-that))
- Martin Fowler: "This is a profound change to the nature of programming, where humans oversee LLM agents who generate the code. Humans are still responsible for what the software does and how it works, but use different skills to create their products." ([source](https://martinfowler.com/bliki/AgenticProgramming.html))
- Addy Osmani: "A model cannot be paged and cannot be held responsible for what it shipped, so whoever clicks merge owns it." ([source](https://addyosmani.com/blog/agentic-code-review/))
- Simon Willison: "The moment you ship your vibe coding code for other people to use, where your bugs might actually harm somebody else, that’s when you need to take a step back." ([source](https://simonwillison.net/2026/Apr/2/lennys-podcast/))
- Gergely Orosz: "AI handles much of the implementation, but engineers are setting the direction, and make continuous course corrections." ([source](https://newsletter.pragmaticengineer.com/p/ai-first-makeover-craft))
- Anthropic engineering: "In practice, there is a clear division of labor in agentic coding––people decide what to build, and the agent decides how to build it." ([source](https://www.anthropic.com/research/claude-code-expertise))
- Charity Majors: "Which means software engineers who own the code should be, at minimum, *extremely involved* in defining the conditions for the code they agree to support." ([source](https://charity.wtf/p/ai-enthusiasts-are-in-a-race-against))
- Robert C. Martin: "The agents are not responsible for anything. They're entirely irresponsible. Only humans can be responsible, at the moment and probably over the next several years." ([source](https://www.aviator.co/podcast/uncle-bob-martin-ai-clean-code))
- Steve Yegge: "When you deploy AI agents at scale, anonymous work creates real problems:" ([source](https://github.com/gastownhall/gastown/blob/main/docs/concepts/identity.md))

### 5. Pace generation to verification capacity, spent by risk

The team treats human verification as its scarce, measured resource. It sizes agent work so a reviewer can actually follow it and slows generation rather than letting approval become a rubber stamp. It sets review depth by risk, with the most attention on auth, payments, data integrity, schema changes and high-tier services, and it reads faster approvals as a possible sign of over-trust.

Trust: Code arrives no faster than people can genuinely vouch for it, and human attention goes where a lapse in trust would cost the most.

Status: established. Empirical support: measured. Experts: Thoughtworks, Addy Osmani, OpenAI engineering, DORA, Andrej Karpathy, Mitchell Hashimoto, Anthropic engineering, Gergely Orosz, Kent Beck.

- Thoughtworks: "A key insight, and one I’ve been thinking about for a while, is the possibility of tiering software in terms of importance and criticality. In other words, we may be able to circumvent code reviews where code quality is deemed of less importance, and instead focus our attention on areas where it really matters." ([source](https://www.thoughtworks.com/insights/articles/reflections-future-software-engineering-retreat))
- Addy Osmani: "Scope discipline is the single biggest determinant of whether an agent’s PR is mergeable or has to be unwound." ([source](https://addyosmani.com/blog/agent-skills/))
- OpenAI engineering: "It also means more pull requests waiting for someone who knows what to look for, and code review can quickly become the bottleneck." ([source](https://developers.openai.com/blog/custom-code-review-rules-for-codex/))
- DORA: "With this insight, they can decide to apply AI to improve the code review process, rather than using AI to simply generate more code that will only exacerbate the bottleneck." ([source](https://services.google.com/fh/files/misc/2025_state_of_ai_assisted_software_development.pdf#page=76))
- Andrej Karpathy: "we we're now kind of like cooperating with AIS and usually they are doing the generation and we as humans are doing the verification. It is in our interest to make this loop go as fast as possible." ([source](https://www.youtube.com/watch?v=LCEmiRjPEtQ&t=1320s))
- Mitchell Hashimoto: "If it's ghosty, I'm reviewing everything that's going into it." ([source](https://newsletter.pragmaticengineer.com/p/mitchell-hashimoto?t=4848s))
- Anthropic engineering: "On the Claude Code team, writing code, writing tests, and refactoring rarely slows us down anymore. But the bottlenecks didn’t go away when agentic coding took away the actual need to type code. Verification, code review, and security took their place." ([source](https://claude.com/resources/articles/running-an-ai-native-engineering-org))
- Gergely Orosz: "you have services based on tier based on criticality, the highest tier software. now needs to have let's say two or three code reviews or an approval from a director to do a configuration change which again all slows down but it's kind of like we know that this is on purpose" ([source](https://newsletter.pragmaticengineer.com/p/building-pi-and-what-makes-self-modifying?t=4035s))
- Kent Beck: "Slow development to ensure that the damn stuff actually works." ([source](https://newsletter.kentbeck.com/p/trust-factory))

### 6. Widen agent autonomy per task type, on evidence

Agents start with tight permissions, no direct access to secrets and written handback points where they must stop and escalate, such as ambiguity, destructive actions or anything outside their scope. The team grants more autonomy one task type at a time, only after the record shows low correction rates, and tightens it again when trust is lost.

Trust: Autonomy grows only as fast as evidence that it is safe, so the team never trusts agents with more than they have shown they can handle.

Status: established. Empirical support: unmeasured. Experts: Andrej Karpathy, Thoughtworks, Charity Majors, OpenAI engineering, Steve Yegge, Robert C. Martin, Simon Willison.

- Andrej Karpathy: "you are in charge of the autonomy slider and depending on the complexity of the task at hand you can uh tune the amount of autonomy that you're willing to give up uh for that task" ([source](https://www.youtube.com/watch?v=LCEmiRjPEtQ&t=1229s))
- Thoughtworks: "The final step is to package the code, test results, and my reasoning log, then notify the compliance manager for final approval." ([source](https://www.thoughtworks.com/insights/articles/a-real-world-guide-to-building-enterprise-grade-ai-agents))
- Charity Majors: "Better evals? Better tests? Better feature flags, guardrails, observability? Work on decoupling dependencies and reducing blast radius? Start with something small and out of the critical path?" ([source](https://charity.wtf/p/ai-enthusiasts-are-in-a-race-against))
- OpenAI engineering: "Keep approval and sandboxing tight by default, then loosen permissions only for trusted repos or specific workflows once the need is clear." ([source](https://learn.chatgpt.com/guides/best-practices))
- Steve Yegge: "A **gate** parks a step until something external happens: a human sign-off, a timer, or a GitHub run or PR" ([source](https://github.com/gastownhall/beads/blob/main/docs/core-concepts/index.md))
- Robert C. Martin: "Agents exchange committed work through durable handoffs, while the operator uses a local dashboard to start work, inspect agents, handle approval gates, answer clarifications, and stop the swarm." ([source](https://github.com/unclebob/swarm-forge/blob/main/README.md))
- Simon Willison: "I'm often paranoid that one of my API keys or similar secrets might inadvertently be revealed in the detailed log files." ([source](https://simonwillison.net/2026/Apr/5/scan-for-secrets-3/))

### 7. Measure stability and rework alongside throughput, per service

The team judges agent work by delivery outcomes against a pre-agent baseline for each service or pipeline: change failure rate, rework, escaped defects, lead time and real use. It does not judge by lines, commits or PR counts. Metrics are paired so they pull against each other, used for the team's own improvement rather than as individual targets, and AI wins are reported in the same forum as their downstream cleanup costs.

Trust: Paired outcome metrics show whether trust is actually keeping pace with output, instead of letting rising throughput hide falling stability.

Status: established. Empirical support: measured. Experts: Thoughtworks, DORA, Gergely Orosz, Addy Osmani, METR, Charity Majors, Anthropic engineering, Simon Willison.

- Thoughtworks: "If an AI generates 200 lines of code in seconds, but a developer spends 30 minutes reviewing, debugging, and refactoring to fit team patterns, the net productivity gain is questionable." ([source](https://martinfowler.com/articles/reduce-friction-ai/))
- DORA: "DORA’s research has repeatedly demonstrated that speed and stability are not tradeoffs. In fact, we see that the metrics are correlated for most teams." ([source](https://dora.dev/guides/dora-metrics/))
- Gergely Orosz: "This is an observed thing that when you start to have more output, you increase your deployment frequency. You often, not always, but you often have more regressions." ([source](https://newsletter.pragmaticengineer.com/p/distributed-databases-with-peter?t=4967s))
- Addy Osmani: "Deciding on metric after-the-fact is probably not enough. Metrics can be put in place in advance, in a concise doc." ([source](https://addyosmani.com/blog/agentic-autonomy-levels/))
- METR: "It’s possible for AI assistance to affect the outcomes without actually increasing productivity, e.g. by causing developers to write more verbose but functionally equivalent code, or causing them to break up pull requests into smaller chunks of work." ([source](https://arxiv.org/pdf/2507.09089#page=3))
- Charity Majors: "The problem is, the wins and costs are happening to two different groups of people. There is no natural feedback loop." ([source](https://charity.wtf/p/ai-enthusiasts-are-in-a-race-against))
- Anthropic engineering: "On the third bullet, don't confuse throughput with success. Throughput is one metric, but the real metric is measuring the thing you're trying to solve." ([source](https://claude.com/resources/articles/running-an-ai-native-engineering-org))
- Simon Willison: "So I realized what I value more than the quality of the tests and documentation is that I want somebody to have *used* the thing." ([source](https://simonwillison.net/2026/May/6/vibe-coding-and-agentic-engineering/))

### 8. Keep a human steward of system structure

An experienced engineer owns each system's architecture, module boundaries and long-term health. They enforce layering with custom linters, run regular design-drift reviews, and use cheap agent refactoring to pay debt down continuously, because clean structure is what keeps future agent work accurate and cheap.

Trust: A well-structured codebase keeps agent output predictable and reviewable as the system grows, so trust does not erode as complexity piles up.

Status: established. Empirical support: measured. Experts: Kent Beck, Thoughtworks, Unmesh Joshi, Gergely Orosz, Birgitta Böckeler, OpenAI engineering, Simon Willison.

- Kent Beck: "At some point the complexity will exceed the genie’s capacity & it’s game over with lots of dollar signs left to play for." ([source](https://newsletter.kentbeck.com/p/earn-and-learn))
- Thoughtworks: "the same traits making high-quality software understandable to humans also allow AIs to understand it more quickly. Therefore, building high-quality software enables the AI to move faster as well." ([source](https://www.thoughtworks.com/insights/articles/quality-is-speed-AI-era))
- Unmesh Joshi: "Without a stable vocabulary of abstractions, LLM-generated code tends to be procedural." ([source](https://martinfowler.com/articles/convo-what-how.html))
- Gergely Orosz: "When a codebase gets too complex, the human engineer feels the issues this creates." ([source](https://newsletter.pragmaticengineer.com/p/building-pi-and-what-makes-self-modifying?t=5504s))
- Birgitta Böckeler: "develop team rituals to maintain a good understanding of the codebase and catch drift early; keep an eye on the trend of number of files touched per change, and number of" ([source](https://martinfowler.com/articles/exploring-gen-ai/tdd-in-the-agent-loop.html))
- OpenAI engineering: "This is the kind of architecture you usually postpone until you have hundreds of engineers. With coding agents, it’s an early prerequisite: the constraints are what allows speed without decay or architectural drift." ([source](https://web.archive.org/web/20261006122733id_/https://openai.com/index/harness-engineering/))
- Simon Willison: "If you’ve got a codebase with a bunch of patterns in, they will follow those patterns almost to a tee." ([source](https://simonwillison.net/2026/Mar/14/pragmatic-summit/))

### 9. Check that the team still understands its systems

The team regularly checks that engineers can explain and debug recently agent-changed critical services and pipelines without the agent. It encourages using agents to ask questions and get explanations rather than only to generate code, and it builds deliberate learning paths for juniors to replace the starter work agents now do.

Trust: People can only vouch for systems they understand, so keeping comprehension current keeps human judgment able to check what agents ship.

Status: established. Empirical support: measured. Experts: Thoughtworks, Addy Osmani, Anthropic engineering, Simon Willison, Unmesh Joshi, Andrej Karpathy, Kent Beck.

- Thoughtworks: "As AI takes on more execution work, human contribution increasingly shifts toward judgment: deciding what to delegate, evaluating outputs and determining when intervention is required." ([source](https://www.thoughtworks.com/insights/articles/path-to-ai-first-organization))
- Addy Osmani: "And within the AI group, the strong results came from those who asked conceptual questions and requested explanations rather than treating the model as a code vending machine." ([source](https://addyosmani.com/blog/agentic-skill-decay/))
- Anthropic engineering: "The largest gap in scores between the two groups was on debugging questions, suggesting that the ability to understand when code is incorrect and why it fails may be a particular area of concern if AI impedes coding development." ([source](https://www.anthropic.com/research/AI-assistance-coding-skills))
- Simon Willison: "It's so easy to let the codebase evolve outside of our abilities to reason clearly about it." ([source](https://simonwillison.net/2026/Mar/25/thoughts-on-slowing-the-fuck-down/))
- Unmesh Joshi: "The problem is not that the LLM generated code. The problem is that the code introduced vocabulary faster than the developers built understanding." ([source](https://martinfowler.com/articles/what-is-code.html))
- Andrej Karpathy: "But you still have to understand the fundamentals." ([source](https://karpathy.bearblog.dev/sequoia-ascent-2026/))
- Kent Beck: "So, one way to think about this is a junior programmer is, you know, senior programmer writes some tests and the junior programmer goes and makes 'em pass or whatever." ([source](https://www.heavybit.com/library/podcasts/o11ycast/ep-80-augmented-coding-with-kent-beck))

### 10. Version the agent's working context with the code

Conventions, business rules, check commands, known pitfalls and current API docs that agents need go into lean, reviewed, versioned instruction files in the repository, shared across the team and grown from observed failures rather than written up front. Each file has an owner and is pruned when models improve.

Trust: Reviewed, shared context makes agent output depend on the team's agreed standards rather than on who wrote the prompt, so quality stays consistent as more people direct agents.

Status: established. Empirical support: measured. Experts: OpenAI engineering, Thoughtworks, Charity Majors, METR, Steve Yegge, Andrej Karpathy, Addy Osmani, Birgitta Böckeler, Anthropic engineering.

- OpenAI engineering: "Add overrides in nested directories when specific teams need different rules." ([source](https://learn.chatgpt.com/docs/agent-configuration/agents-md))
- Thoughtworks: "Every team has senior developers who instinctively know when code is right—they spot architectural drift, security gaps, and convention violations that others miss." ([source](https://martinfowler.com/articles/reduce-friction-ai/))
- Charity Majors: "The knowledge in our heads is unavailable to AI until we encode it into the system, after all." ([source](https://charity.wtf/p/ai-demands-more-engineering-discipline))
- METR: "Our results also suggest that AI capabilities may be comparatively lower in settings with very high quality standards, or with many implicit requirements (e.g. relating to documentation, testing coverage, or linting/formatting) that take humans substantial time to learn." ([source](https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/))
- Steve Yegge: "Commit the instruction files (`AGENTS.md`, `CLAUDE.md`, `GEMINI.md`, as applicable) to git so all team members and AI tools get the same instructions." ([source](https://github.com/gastownhall/beads/blob/main/docs/getting-started/ide-setup.md))
- Andrej Karpathy: "Claude kept hallucinating deprecated APIs, model names, and input/output conventions that have all changed recently, which was confusing, but it resolved them after I copy pasted the docs back and forth for a while." ([source](https://karpathy.bearblog.dev/vibe-coding-menugen/))
- Addy Osmani: "Write the project rules file describing the real conventions, the ones in the code, not the ones in the wiki." ([source](https://github.com/addyosmani/agent-skills/blob/main/docs/adoption-guide.md))
- Birgitta Böckeler: "My recommendation would be to build context like rules files up gradually, and not pump too much stuff in there right from the start." ([source](https://martinfowler.com/articles/exploring-gen-ai/context-engineering-coding-agents.html))
- Anthropic engineering: "The highest-signal content in any skill is the Gotchas section. These sections should be built up from common failure points that Claude runs into when using your skill." ([source](https://claude.dev/blog/lessons-from-building-claude-code-how-we-use-skills/))

### 11. Make services drivable and observable by agents

The team prefers stacks and tooling that agents can operate and check: CLIs with self-describing help, local copies of a service an agent can start and query for structured results, configuration and infrastructure as text and commands rather than console clicks, strong typing and validated schemas, and wide structured telemetry agents can query.

Trust: When agents can exercise and observe the real system themselves, more of each change gets checked by machines before a human has to judge it.

Status: established. Empirical support: unmeasured. Experts: Andrej Karpathy, Simon Willison, Lauren Tan, Charity Majors, Birgitta Böckeler, Unmesh Joshi.

- Andrej Karpathy: "All of this work and state is not even accessible or manipulatable by an LLM - how are we supposed to be automating society by 2027 like this?" ([source](https://karpathy.bearblog.dev/vibe-coding-menugen/))
- Simon Willison: "I really like this pattern where the `--help` output for a command provides enough detail that a coding agent can use it—it works kind of like bundling a `SKILL.md` file directly inside the tool." ([source](https://simonwillison.net/2026/Jun/30/shot-scraper-video/))
- Lauren Tan: "The CLI lets an agent start the app, navigate it, inspect state, and read structured JSON results back. Each agent gets a complete copy of the application and can test a change end to end." ([source](https://thenewstack.io/agentic-verification-distributed-systems/))
- Charity Majors: "At agentic speed, that reconstruction becomes a bottleneck and a failure surface." ([source](https://charity.wtf/p/your-data-is-made-powerful-by-context))
- Birgitta Böckeler: "The harness described suggests that increasing trust and reliability required constraining the solution space: specific architectural patterns, enforced boundaries, standardized structures." ([source](https://martinfowler.com/articles/exploring-gen-ai/harness-engineering-memo.html))
- Unmesh Joshi: "The agent can generate a candidate, run it past the validator, and repair it from the error, all without a human in the loop." ([source](https://martinfowler.com/articles/llm-and-dsls.html))

### 12. Parallelize agents only along independent seams

Agents run in parallel only on work that splits cleanly into separate files, services or pipeline stages, each in its own isolated workspace. Coordination state such as task claims, dependencies and handoffs lives in durable, deterministic machinery rather than in an engineer's head or a chat session.

Trust: Independent, traceable streams of work can each be verified on their own, so adding agents does not create tangled changes no one can vouch for.

Status: established. Empirical support: measured. Experts: Anthropic engineering, Addy Osmani, Kent Beck, Thoughtworks, Simon Willison, Steve Yegge, Robert C. Martin.

- Anthropic engineering: "Split parallel tasks along file boundaries, merge the branches in a sensible order, and expect a session to report problems that another session is already fixing." ([source](https://claude.dev/blog/claude-code-in-the-cloud/))
- Addy Osmani: "Pick this only when **independent** investigations can run in parallel and produce reports that a single agent then merges." ([source](https://github.com/addyosmani/agent-skills/blob/main/docs/agents.md))
- Kent Beck: "I was managing it. Watching which agent was doing what. Wondering when to interrupt. Holding state in my head that the system should have been holding for me." ([source](https://newsletter.kentbeck.com/p/genie-lessons-nobody-wants-agents))
- Thoughtworks: "Tasks that need the same mental model should usually stay together." ([source](https://martinfowler.com/articles/orchestrator-tax.html))
- Simon Willison: "Carefully managing the context such that it fits within those limits is critical to getting great results out of a model." ([source](https://simonwillison.net/guides/agentic-engineering-patterns/subagents/))
- Steve Yegge: "wake an agent when something needs judgment. The rule is: crons watch, models act." ([source](https://yegge.ai/essays/the-shape-of-things-to-come/))
- Robert C. Martin: "SwarmForge coordinates AI agents in isolated git worktrees and tmux sessions." ([source](https://github.com/unclebob/swarm-forge/blob/main/README.md))

### 13. Test agent setups with repeated runs on real tasks

The team chooses models, effort levels, tools, prompts and rules by running them repeatedly against a fixed set of its own representative tasks and a baseline, not by reputation, folklore or vendor benchmarks. It sends work to the cheapest model that passes and reruns the evals when models change.

Trust: Setups proven on the team's own work behave predictably, so the team can rely on them instead of discovering their failures in production.

Status: established. Empirical support: measured. Experts: Kent Beck, Birgitta Böckeler, Thoughtworks, Andrej Karpathy, OpenAI engineering, METR, Anthropic engineering, Addy Osmani.

- Kent Beck: "That means I'm going to be doing the same thing over and over again with variations and seeing what of those variations really matter." ([source](https://newsletter.kentbeck.com/p/run-right-and-fast-for-the-adaptive?t=668s))
- Birgitta Böckeler: "So I also did a few runs of my automated setup with reasoning off - and lo and behold, it's not only faster (which was to be expected), but also performed the same to slightly better!" ([source](https://martinfowler.com/articles/exploring-gen-ai/local-models-for-coding-factors.html))
- Thoughtworks: "Teams should always evaluate these tools using evals; doing so not only helps us measure how good our agents are over time, it also helps us assess which agents perform better for specific use cases." ([source](https://www.thoughtworks.com/insights/articles/claude-code-cobol-modernization-reality))
- Andrej Karpathy: "You have to explore the model they give you. It has no manual. It works in some settings and not others." ([source](https://karpathy.bearblog.dev/sequoia-ascent-2026/))
- OpenAI engineering: "Try one change that should trigger the rule, one safe counterexample, and one unrelated change. Check that the first produces a useful finding and the others do not create noise, then refine the guidance from what you see." ([source](https://developers.openai.com/blog/custom-code-review-rules-for-codex/))
- METR: "benchmarks may overestimate model capabilities by only measuring performance on well-scoped, algorithmically scorable tasks." ([source](https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/))
- Anthropic engineering: "Sonnet 5.5 fits best when the task has a clear spec and a way to check the result." ([source](https://claude.dev/blog/building-with-claude-sonnet-5-5/))
- Addy Osmani: "Route the hard reasoning to a big model and the routine work, test generation, code review, CI checks, to a small cheap one. The quality holds and the bill comes down." ([source](https://addyosmani.com/blog/new-sdlc-vibe-coding/))

### 14. Build agent skill together, on scheduled real work

Whole teams, managers included, learn agentic engineering on their actual work during scheduled time, starting in low-risk areas. They keep pairing and shared practice, and enthusiasts and skeptics compare evidence together. A central enablement group supplies tooling and shared practices while individuals keep experimenting.

Trust: Skill in instructing and verifying agents is what makes a person's sign-off meaningful, and building it in the open spreads calibrated trust across the team instead of leaving it with a few people.

Status: established. Empirical support: measured. Experts: DORA, Gergely Orosz, Steve Yegge, Simon Willison, METR, Kent Beck, Charity Majors, Thoughtworks.

- DORA: "Build trust with AI technologies through hands-on experience in sandbox or low-risk environments." ([source](https://services.google.com/fh/files/misc/2024_final_dora_report.pdf#page=46))
- Gergely Orosz: "If you’re a manager in your workplace, make the case for every engineer to have access to the best models so they can complete their own “impossible project,” or at least see how far they can go." ([source](https://newsletter.pragmaticengineer.com/p/ai-first-makeover-craft))
- Steve Yegge: "The trainees must bring their actual work, and the instructor(s) will help them learn how to do it with agents." ([source](https://steve-yegge.medium.com/the-flat-curve-society-36c8b01eb33b?source=rss-c1ec701babb7------2))
- Simon Willison: "The key skill required to make productive use of coding agents is being able to confidently instruct them on how to make changes and then confidently verify that those changes have been applied in the correct way." ([source](https://simonwillison.net/2026/Aug/22/more-than-just-code-review/))
- METR: "It also may be the case that there are strong learning effects for AI tools like Cursor that only appear after several hundred hours of usage—our developers typically only use Cursor for a few dozen hours before and during the study." ([source](https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/))
- Kent Beck: "So while we're in this extremely murky regime, um, it behooves us to try a little bit of everything and be a part of communities that are trying everything that we're missing." ([source](https://newsletter.kentbeck.com/p/genie-lessons-nobody-wants-agents?t=2025s))
- Charity Majors: "Expect the company to provide you with resources like product subscriptions, tokens, and shared best practices, but know that your own continuous experimentation and learning will also be required." ([source](https://www.honeycomb.io/blog/ai-norms-values-part-2-ai-honeycomb-engineering))
- Thoughtworks: "at the core of the software engineering craft remains human collaboration and sharing." ([source](https://www.thoughtworks.com/insights/blog/agile-engineering-practices/why-ai-raising-stakes-software-engineering-craft))

### 15. Staff for domain judgment and breadth, not throughput

With agents supplying raw coding speed, the team hires and grows people for domain knowledge, systems judgment and product sense. It forms small cross-functional teams with broad engineers, and it keeps the senior infrastructure, data and security expertise needed to oversee agent output.

Trust: Trust in agent output rests on people who know what correct looks like in the domain, so staffing for judgment raises the team's ability to verify as fast as agents raise its ability to produce.

Status: established. Empirical support: measured. Experts: Anthropic engineering, Gergely Orosz, Martin Fowler, Charity Majors, Addy Osmani, Kent Beck.

- Anthropic engineering: "What I index on less, on the other hand, is raw throughput; the models handle that. The more important question is where you still need human expertise, and that’s where I’d focus." ([source](https://claude.com/resources/articles/running-an-ai-native-engineering-org))
- Gergely Orosz: "As engineers, I think it's pretty clear that an engineer becomes more valuable the more they take on the other parts of the business, the more empathy, the understanding." ([source](https://newsletter.pragmaticengineer.com/p/design-engineering-with-maggie-appleton?t=4971s))
- Martin Fowler: "Additionally this raises the importance of programmers understanding the domain they are working with, collaborating with users and customers to iteratively define and build their product." ([source](https://martinfowler.com/bliki/AgenticProgramming.html))
- Charity Majors: "Roles are blurring all over the place between eng and manager, eng and product, eng and business, eng and design, frontend eng and backend eng." ([source](https://www.honeycomb.io/blog/honeycomb-10-year-manifesto-part-1))
- Addy Osmani: "Developers with the deepest knowledge in one or two areas while maintaining broad literacy tend to deliver the best results." ([source](https://addyosmani.com/blog/earning-judgment/))
- Kent Beck: "The augmented development tools give us a chance to break down those silos. Now they also give us tools to enforce the silos more directly. And I hope we don't do that." ([source](https://newsletter.kentbeck.com/p/nobody-knows?t=1987s))

## Tensions

- **Does line-by-line human review stay?** (open): Should a human read every agent-written diff before it merges, or should human review move above the code and be planned away?
  - Gergely Orosz, Simon Willison, Martin Fowler, Andrej Karpathy: Keep an engaged human reviewer who reads agent code, with extra friction on critical services, because automation bias lets defects through once nobody reads.
  - Robert C. Martin, Steve Yegge, Charity Majors: Line-by-line review is slow and low value. Humans sign off on architecture, deployability and the running system, while machines and layered agent reviewers do the checking.
  - Settle it: For one quarter, randomly route low and medium risk agent PRs to either full human line review or architecture and behaviour sign-off plus agentic review, and compare escaped defects, rollbacks and review hours per tier.
- **How many agents should one engineer run?** (open): Should an engineer run one or two agents at a time, a handful in parallel, or a large crew?
  - Mitchell Hashimoto, Kent Beck, Robert C. Martin: Run one agent, two at most, because each extra agent adds cleanup and coordination that lands on the human.
  - Addy Osmani, Simon Willison: About three to five parallel agents per person is workable when the work splits into independent slices, and falling review quality marks the limit.
  - Gergely Orosz, Steve Yegge: Engineers should manage crews of five or more agents and grow the fleet until throughput stops rising.
  - Settle it: Have each engineer spend two-week periods at one, three and six concurrent agents on comparable work, recording merged-after-full-review output, rework, merge conflicts and self-reported fatigue.
- **Can one person replace a team?** (open): Should a leader staff components with single agent-directing individuals, or keep stable multi-person teams?
  - Robert C. Martin: One human directing agents can do a five or six person team's work, so organise around individuals owning large components behind narrow interfaces.
  - Thoughtworks, Simon Willison, Kent Beck, Steve Yegge: Teams shrink but not to one. A stable group must share the mental model and cognitive load, and people should keep working with people.
  - Settle it: Run comparable services with a solo owner and with a team of two or three for six months, tracking delivered functionality, incident recovery when the owner is away, and defects.
- **Perceived agent speedup versus measured slowdown** (leaning): Should a team reorganise around the large speedups practitioners report, or treat them as unproven until measured on its own work?
  - METR (measured): Self-reports and forecasts of AI speedup are unreliable and experienced developers on mature repos measured 19 percent slower, so measure with controlled trials before acting.
  - Lauren Tan, Steve Yegge, Thoughtworks: Agent-driven teams already deliver work estimated for far larger teams and hundreds of PRs or features per engineer, so the gain is real and teams should restructure for it now.
  - Settle it: Randomly assign pre-scoped backlog tasks to agent-allowed and agent-disallowed conditions for a month, collecting developer forecasts beforehand, and compare measured completion time with the forecasts.
- **Do experts gain most or least?** (open): Does AI help most in work the engineer already knows deeply, or in unfamiliar territory?
  - METR (measured): AI helps least where the developer is already expert and most on unfamiliar code and small greenfield work, so be sceptical of it in code you know well.
  - Anthropic engineering, Gergely Orosz, Simon Willison (measured): AI amplifies existing expertise, and the operator's domain knowledge multiplies what the agent accomplishes, so lean on experts and hire for depth.
  - Settle it: Tag each agent task with the engineer's self-rated familiarity and measure time to merge and rework against a no-agent baseline in each familiarity band.
- **Prescribe test-first process to agents?** (leaning): Should a team require agents to follow a test-first workflow, or only verify outcomes?
  - Birgitta Böckeler (measured): Prescribing TDD added cost without measurable quality gains, so enforce must-haves with hooks and invest in automated feedback on results instead.
  - Simon Willison, Kent Beck, Robert C. Martin (measured): Agents should work red/green test-first in small test-gated steps, and the chosen test discipline measurably changes the suite and the program.
  - Settle it: Run the same set of representative tasks several times with and without a TDD instruction, comparing mutation score, escaped defects, blind quality ranking and tokens per task.
- **Can agents verify their own work?** (open): Is agent self-verification enough to call work done, or must humans own the specification it is checked against?
  - Lauren Tan, Anthropic engineering: Agents that run and check their own work let humans step out of the slowest part of the loop, and that capability is critical infrastructure.
  - Birgitta Böckeler, Robert C. Martin, Unmesh Joshi: Agent-written tests and agent-confirmed failures prove little, so humans must write or approve the behavioural spec and mutation testing must show the tests bite.
  - Settle it: For a set of features, compare defects escaping a fully agent-written and agent-run test suite against defects escaping a human-approved acceptance suite on the same code, and run mutation testing on both.
- **Write intent down or ask the agent?** (open): Should a team record intent, decisions and tacit knowledge in documents, or keep code simple and ask the agent when questions come up?
  - Kent Beck: Agents weaken the case for docs and ADRs; keep code simple and ask the agent about the source rather than write documents that go stale.
  - Gergely Orosz, Charity Majors, OpenAI engineering, METR (measured): Intent, decisions and tacit rules are invisible to agents unless written into versioned artifacts in the repo, so preserve prompts, specs and decision records.
  - Settle it: Collect real questions about why the code is the way it is and time how accurately they get answered by asking an agent over code alone versus code plus decision records, and count agent mistakes traced to missing context.
- **Upfront spec or living prototype?** (open): Should agent work start from a human-approved spec, or from a shared prototype evolved in short cycles?
  - Addy Osmani, Thoughtworks: Run agent work through gated phases of spec, plan and tasks with human approval before code, because spec quality is the biggest lever.
  - Steve Yegge: Evolve a shared, visible prototype in short cycles instead of a big upfront spec.
  - Kent Beck: Spec-driven work suits one-off finish-line projects; long-lived systems need practices that keep paying for the next step, so decide which game first.
  - Settle it: Label projects as one-off or long-lived, assign spec-first or prototype-first, and compare idea-to-ship time, late intent rejections and rework over six months.
- **Validate before merge or in production?** (open): Should a team invest its validation effort in pre-merge gates or in observing changes in production?
  - Charity Majors: Pre-production checks quickly stop paying off at agent speed; replace merge-and-hope with flags, progressive rollout and telemetry-based validation in production.
  - Addy Osmani, Thoughtworks, OpenAI engineering: Deterministic checks in the agent loop and before merge decide when work is done, catching defects before humans or production see them.
  - Settle it: For a service, track where each agent defect was first caught (in-loop check, review, staged rollout, production) and the cost to fix at each stage, before and after adding progressive rollout.
- **Megabatch onto main or small batches?** (leaning): When agents commit faster than the build can verify, should a team land large batches and roll forward, or hold to small changes?
  - Steve Yegge: Once commits outrun build slots, land large batches onto main together and have agents diagnose and fix whatever breaks.
  - DORA, Addy Osmani, Andrej Karpathy (measured): Keep every change small and cheap to roll back, because larger changes are slower and less stable, and slow generation rather than outgrow review.
  - Settle it: On a high-commit-rate repo, alternate weeks of megabatch landing and small-batch queueing, recording main-red time, commit-to-landing time and production failures.
- **Separate role agents or one agent?** (open): Should a team split agent work into separate specialised roles such as implementer and verifier, or drive a single capable agent?
  - Addy Osmani, Steve Yegge, Anthropic engineering, Kent Beck (measured): The agent that writes a change should never grade it; use separate narrow-role agents for review, testing and merging.
  - Robert C. Martin, Simon Willison (measured): Drive one capable agent like a senior colleague, and use subagents only to protect context and cut cost, not as role swarms.
  - Settle it: Run the same tasks with a single agent and with an implementer plus independent verifier agent, comparing escaped defects, tokens per task and human orchestration time.
- **Review in the moment or monitor?** (open): Should humans review agent output as it arrives, or let agents run autonomously and step in only when needed?
  - Birgitta Böckeler: Deferring review on high-autonomy runs led to constant rework and late surprises, so understand output as it arrives.
  - Anthropic engineering, Mitchell Hashimoto (measured): Oversight means being able to see and intervene, not approving each step; agents can take more autonomy, and humans should check in on their own schedule.
  - Settle it: Assign comparable tasks to in-the-moment review and to autonomous runs with monitoring and handback points, then compare rework, late defects and human hours per task.
- **Count tokens or only outcomes?** (open): Should leaders track token spend per engineer as a sign of healthy agent adoption?
  - Steve Yegge (measured): Token spend shows real practice up to about 15M tokens a day, so track it on the way up, then switch to waste and outcomes per token.
  - Gergely Orosz, Charity Majors, DORA (measured): Activity metrics like tokens and AI lines reward looking busy and invite gaming, so judge AI only by delivery outcomes and set no individual usage targets.
  - Settle it: Correlate per-engineer token spend over a quarter with their change fail rate, rework and lead time, and see whether spend predicts outcomes below and above the threshold.
- **Should humans keep writing code?** (open): Should engineers keep hand-writing and reshaping code, or move entirely to specifying, judging and validating?
  - Unmesh Joshi, Mitchell Hashimoto: Reviewing generated code rarely forces design thinking, so developers should keep writing some code by hand to discover design and preserve skills.
  - Charity Majors, Anthropic engineering (measured): Engineers' work moves from typing code to writing specs, running experiments, interpreting production and deciding what to build.
  - Settle it: Give engineers periodic debugging and design-explanation checks, and compare scores and later change lead time for those who keep hand-authoring part of their work against those who fully delegate.

## Scoreboard

### DORA delivery

- **Change lead time** (`derivable`): The time from the first commit of a change to the production deploy that contains it.
  - How: First commit on the PR to the first successful production deploy_event whose commit contains the merge commit.
  - Definition from: [DORA's software delivery performance metrics](https://dora.dev/guides/dora-metrics/)
  - Note: DORA counts from the commit to version control; we take the PR's first commit as that commit. Median and p90, the deploy_event join and the exclusions are Expert Brain decision 0007. The stage metrics below decompose this total.
- **Deployment frequency** (`derivable`): The number of production deployments in a period.
  - How: Successful production deploy_events per service per week, written by the GitHub Actions, Jenkins or CloudBees CI adapter.
  - Definition from: [DORA's software delivery performance metrics](https://dora.dev/guides/dora-metrics/)
  - Note: The deploy_event record and its adapters are Expert Brain decision 0007.
- **Change fail rate** (`instrument`): The share of production deployments that need immediate intervention, such as a rollback or a hotfix.
  - How: A production deploy_event fails if its result is failed or rolled_back, or an incident names its commit. Revert commits and `hotfix` labels give a rough derivable floor until incidents are linked.
  - Definition from: [DORA's software delivery performance metrics](https://dora.dev/guides/dora-metrics/)
  - Note: The deploy_event result enum and the incident link are Expert Brain decision 0007.
- **Failed deployment recovery time** (`instrument`): The time from a failed deployment to recovery, for deployments that need immediate intervention.
  - How: Incident open and close timestamps, linked to the deploy by commit sha.
  - Definition from: [DORA's software delivery performance metrics](https://dora.dev/guides/dora-metrics/)
  - Note: Median and p90 and the incident record are Expert Brain decision 0007.
- **Rework rate** (`derivable`): The share of changed lines in a period that modify lines added within the previous 21 days.
  - How: The line_age_blame procedure on each merged PR, with a 21-day window.
  - Definition from: [DORA's software delivery performance metrics](https://dora.dev/guides/dora-metrics/)
  - Note: DORA's fifth metric, deployment rework rate, is the share of deployments that are unplanned and happen because of a production incident. Ours measures code rework instead, because it can be derived from git history without incident tagging. The procedure form and the exclusions are Expert Brain decision 0007.

### Lead time stages

- **Lead time stage: author working** (`derivable`): The time from the first commit to the PR being ready for review.
  - How: First commit author date to the ready_for_review event (or opened_at if opened non-draft).
  - Definition from: Expert Brain decision 0007: lead time split by who holds the PR
  - Note: Read next to PR count and size: time piling up here with many tiny PRs points to gaming; time piling up in the waiting-on-reviewer stage points to review capacity.
- **Lead time stage: waiting on reviewer** (`derivable`): The time from a review being requested to the first submitted review of any state.
  - How: First review_requested event (or ready_for_review if none) to the first submitted review.
  - Definition from: Expert Brain decision 0007: lead time split by who holds the PR
- **Lead time stage: back with author** (`derivable`): The time from changes being requested to the author's next push, summed over rounds.
  - How: Each changes_requested review paired with the next push to the branch; the intervals are summed per PR.
  - Definition from: Expert Brain decision 0007: lead time split by who holds the PR
- **Lead time stage: approved, not merged** (`derivable`): The time from the first approval to the merge.
  - How: First review with state approved to merged_at.
  - Definition from: Expert Brain decision 0007: lead time split by who holds the PR
- **Lead time stage: merged, not deployed** (`derivable`): The time from the merge to the first successful production deploy that contains it.
  - How: merged_at to the joined first_production_deploy_at from the deploy_event table.
  - Definition from: Expert Brain decision 0007: lead time split by who holds the PR
- **Lead time stage: blocked on a decision** (`instrument`): The time a PR carried the `blocked: decision` label, summed over the intervals it was applied.
  - How: Needs the `blocked: decision` label in every repo; the GitHub adapter reads the labeled and unlabeled events and pairs them into intervals.
  - Definition from: Expert Brain decision 0007: waits on business decisions are invisible to GitHub without a label

### Trust against code

- **Code volume** (`derivable`): Lines added and changed in merged PRs per week.
  - How: Sum of additions and deletions over merged PRs, by merge week.
  - Definition from: Expert Brain decision 0005: build trust as fast as code
  - Note: The denominator for the trust thesis: the trust metrics below are read against it, so a team can see whether trust keeps pace with code. Lockfiles, generated code and reverts are excluded (Expert Brain decision 0007).
- **Deterministically gated change share** (`derivable`): The share of merged changes whose merge required passing deterministic checks (tests, types, lint, mutation or coverage thresholds) rather than review alone.
  - How: Merged PRs whose required status checks all ran and passed and that were not merged with an admin bypass, over all merged PRs.
  - Definition from: Expert Brain decision 0005 and house principle: determinism for validation
  - Note: Admin-bypass merges count as ungated here rather than being excluded (Expert Brain decision 0007).
- **Review latency** (`derivable`): The time from a PR being ready for review to its first approving review.
  - How: PR ready-for-review event to the first review with state approved, from the GitHub API.
  - Definition from: Expert Brain decision 0005: build trust as fast as code
  - Note: v0 also counted ready-for-review to merge; that is now the sum of the lead time stages. Median and p90 are Expert Brain decision 0007.

### Maintenance cost

- **30-day churn on AI-authored changes** (`instrument`): The share of lines from AI-authored changes that are modified or deleted within 30 days of merge.
  - How: Needs AI-authored changes marked by the AI commit trailer or PR label; then the ai_line_survival procedure runs on git history.
  - Definition from: Expert Brain spec v0.4, section 5.7 (maintenance-cost proxy)
  - Note: The procedure form is Expert Brain decision 0007.
- **Unplanned work share** (`instrument`): The share of engineering time spent on unplanned work and defects.
  - How: Comes from the work tracker, not GitHub; each closed item carries its effort and a planned or unplanned flag.
  - Definition from: Expert Brain spec v0.4, section 5.7 (maintenance-cost proxy)
  - Note: The work_item record is Expert Brain decision 0007.

### Quality gates

- **Mutation score** (`instrument`): The share of generated mutants that the test suite kills.
  - How: A mutation-testing CI step per pilot repo, reporting killed and surviving mutants as a quality_gate_run.
  - Definition from: [clj-mutate README (Robert C. Martin)](https://github.com/unclebob/clj-mutate/blob/master/README.md)
  - Note: The quality_gate_run record is Expert Brain decision 0007.
- **CRAP score trend** (`instrument`): The trend of the worst CRAP scores, where CRAP(fn) = CC² × (1 - coverage)³ + CC, CC is cyclomatic complexity and coverage is the fraction covered by tests.
  - How: A CI step per pilot repo that records the CRAP scores of the riskiest functions as a quality_gate_run.
  - Definition from: [crap4clj README (Robert C. Martin)](https://github.com/unclebob/crap4clj/blob/master/README.md)
  - Note: The per-period value is the worst score in the latest run; the trend is read across periods (Expert Brain decision 0007).

### Adoption and trust

- **AI-assisted change share** (`instrument`): The share of merged changes that are AI-assisted.
  - How: The same commit trailer or PR label as the churn metric.
  - Definition from: Expert Brain spec v0.4, section 5.7 (adoption and trust)
- **Developer trust in AI-generated code** (`instrument`): A short recurring survey item: how much do you trust the quality of AI-generated code? (none, little, some, a lot), read next to AI usage.
  - How: A pulse survey, so results are correlated with usage rather than assumed; responses are anonymous and reported per team only.
  - Definition from: [DORA 2024 Accelerate State of DevOps report: trust in AI-generated code](https://services.google.com/fh/files/misc/2024_final_dora_report.pdf)
  - Note: The survey_response record and the team-only reporting are Expert Brain decision 0007.

### Data movement

- **Data-quality check pass rate** (`instrument`): The share of data-quality checks that pass, over the pipeline runs in a period.
  - How: The orchestrator writes a data_quality_run per pipeline run with the counts from the data-quality tooling (dbt tests, Great Expectations, Soda or equivalent). Not from GitHub.
  - Definition from: Expert Brain decision 0007: metrics for data-movement teams
- **Data incidents per period** (`instrument`): The number of late loads, bad rows reaching consumers, and reprocessing runs in a period.
  - How: The orchestrator writes an incident with kind late_load (an SLA missed), bad_rows_to_consumers (a downstream consumer received rows that failed a check) or reprocessing (a backfill or rerun of a completed load). Not from GitHub.
  - Definition from: Expert Brain decision 0007: metrics for data-movement teams

## Provenance

- Addy Osmani: [agent-skills: docs/adoption-guide.md](https://github.com/addyosmani/agent-skills/blob/main/docs/adoption-guide.md), undated
- Addy Osmani: [agent-skills: docs/agents.md](https://github.com/addyosmani/agent-skills/blob/main/docs/agents.md), undated
- Addy Osmani: [agent-skills: docs/copilot-setup.md](https://github.com/addyosmani/agent-skills/blob/main/docs/copilot-setup.md), undated
- Addy Osmani: [Agent Harness Engineering | AddyOsmani.com](https://addyosmani.com/blog/agent-harness-engineering/), 2026-04-19
- Addy Osmani: [Agent Skills | AddyOsmani.com](https://addyosmani.com/blog/agent-skills/), 2026-05-03
- Addy Osmani: [Agentic Code Review | AddyOsmani.com](https://addyosmani.com/blog/agentic-code-review/), 2026-06-15
- Addy Osmani: [The New Software Lifecycle | AddyOsmani.com](https://addyosmani.com/blog/new-sdlc-vibe-coding/), 2026-06-16
- Addy Osmani: [Agentic Autonomy Levels | AddyOsmani.com](https://addyosmani.com/blog/agentic-autonomy-levels/), 2026-07-02
- Addy Osmani: [Earning taste and judgment](https://addyosmani.com/blog/earning-judgment/), 2026-07-14
- Addy Osmani: [Agentic Skill Decay](https://addyosmani.com/blog/agentic-skill-decay/), 2026-08-31
- Andrej Karpathy: [Vibe coding MenuGen](https://karpathy.bearblog.dev/vibe-coding-menugen/), 2025-04-27
- Andrej Karpathy: [Andrej Karpathy: Software Is Changing (Again)](https://www.youtube.com/watch?v=LCEmiRjPEtQ), 2025-06-19
- Andrej Karpathy: [Andrej Karpathy — AGI is still a decade away](https://www.dwarkesh.com/p/andrej-karpathy), 2025-10-17
- Andrej Karpathy: [Sequoia Ascent 2026 summary](https://karpathy.bearblog.dev/sequoia-ascent-2026/), 2026-04-30
- Anthropic engineering: [How AI assistance impacts the formation of coding skills](https://www.anthropic.com/research/AI-assistance-coding-skills), 2026-01-29
- Anthropic engineering: [Measuring AI agent autonomy in practice](https://www.anthropic.com/research/measuring-agent-autonomy), 2026-02-18
- Anthropic engineering: [Building Claude Code with Boris Cherny](https://newsletter.pragmaticengineer.com/p/building-claude-code-with-boris-cherny), 2026-03-04
- Anthropic engineering: [Lessons from building Claude Code: How we use skills](https://claude.dev/blog/lessons-from-building-claude-code-how-we-use-skills/), 2026-06-03
- Anthropic engineering: [Running an AI-native engineering org](https://claude.com/resources/articles/running-an-ai-native-engineering-org), 2026-06-03
- Anthropic engineering: [How Claude Code is used in practice](https://www.anthropic.com/research/claude-code-expertise), 2026-06-16
- Anthropic engineering: [Building with Claude Sonnet 5.5](https://claude.dev/blog/building-with-claude-sonnet-5-5/), 2026-09-28
- Anthropic engineering: [Claude Code in the cloud: a field guide to cloud sessions](https://claude.dev/blog/claude-code-in-the-cloud/), 2026-10-06
- Birgitta Böckeler: [Context Engineering for Coding Agents](https://martinfowler.com/articles/exploring-gen-ai/context-engineering-coding-agents.html), 2026-02-05
- Birgitta Böckeler: [Harness Engineering - first thoughts](https://martinfowler.com/articles/exploring-gen-ai/harness-engineering-memo.html), 2026-02-17
- Birgitta Böckeler: [Viability of local models for coding](https://martinfowler.com/articles/exploring-gen-ai/local-models-for-coding-factors.html), 2026-07-07
- Birgitta Böckeler: [TDD inside the agent loop - theater or actual value?](https://martinfowler.com/articles/exploring-gen-ai/tdd-in-the-agent-loop.html), 2026-08-10
- Charity Majors: [Happy Birthday to Us: Honeycomb 10 Year Manifesto, Part 1](https://www.honeycomb.io/blog/honeycomb-10-year-manifesto-part-1), 2026-02-11
- Charity Majors: [Your Data Is Made Powerful By Context (so stop destroying it already)](https://charity.wtf/p/your-data-is-made-powerful-by-context), 2026-03-09
- Charity Majors: [AI enthusiasts are in a race against time, AI skeptics are in a race against entropy](https://charity.wtf/p/ai-enthusiasts-are-in-a-race-against), 2026-06-02
- Charity Majors: [AI demands more engineering discipline. Not less](https://charity.wtf/p/ai-demands-more-engineering-discipline), 2026-06-15
- Charity Majors: [Stop being skeptical about AI for development with Charity Majors](https://newsletter.pragmaticengineer.com/p/stop-being-skeptical-about-ai-for), 2026-08-12
- Charity Majors: [AI Norms & Values, Part 2 of 3: AI for Honeycomb Engineering](https://www.honeycomb.io/blog/ai-norms-values-part-2-ai-honeycomb-engineering), 2026-09-02
- DORA: [Accelerate](https://services.google.com/fh/files/misc/2024_final_dora_report.pdf), 2024-11-19
- DORA: [State of AI-assisted](https://services.google.com/fh/files/misc/2025_state_of_ai_assisted_software_development.pdf), 2025-10-15
- DORA: [DORA | DORA’s software delivery performance metrics](https://dora.dev/guides/dora-metrics/), 2026-01-05
- Gergely Orosz: [Inside a five-year-old startup’s rapid AI makeover](https://newsletter.pragmaticengineer.com/p/ai-first-makeover-craft), 2026-01-27
- Gergely Orosz: [Building Pi, and what makes self-modifying software so fascinating](https://newsletter.pragmaticengineer.com/p/building-pi-and-what-makes-self-modifying), 2026-04-29
- Gergely Orosz: [Design Engineering with Maggie Appleton](https://newsletter.pragmaticengineer.com/p/design-engineering-with-maggie-appleton), 2026-09-23
- Gergely Orosz: [Distributed databases with Peter Mattis](https://newsletter.pragmaticengineer.com/p/distributed-databases-with-peter), 2026-09-30
- Kent Beck: [Genie Session: Codex for Mac/GPUSortedMap](https://newsletter.kentbeck.com/p/genie-session-codex-for-macgpusortedmap), 2026-02-13
- Kent Beck: [Earn *And* Learn](https://newsletter.kentbeck.com/p/earn-and-learn), 2026-02-18
- Kent Beck: [Nobody Knows](https://newsletter.kentbeck.com/p/nobody-knows), 2026-03-25
- Kent Beck: [Genie Lessons: Nobody Wants Agents](https://newsletter.kentbeck.com/p/genie-lessons-nobody-wants-agents), 2026-04-23
- Kent Beck: [Genie Sessions: Run, Right, and Fast for the Adaptive Radix Tree](https://newsletter.kentbeck.com/p/run-right-and-fast-for-the-adaptive), 2026-05-02
- Kent Beck: [Trust Factory](https://newsletter.kentbeck.com/p/trust-factory), 2026-06-02
- Kent Beck: [How Do You Know That?](https://newsletter.kentbeck.com/p/how-do-you-know-that), 2026-07-22
- Kent Beck: [O11ycast | Ep. #80, Augmented Coding with Kent Beck | Heavybit](https://www.heavybit.com/library/podcasts/o11ycast/ep-80-augmented-coding-with-kent-beck), 2026-09-17
- Lauren Tan: [One engineer shipped 2,000 PRs a month to production. Verification is the key.](https://thenewstack.io/agentic-verification-distributed-systems/), 2026-09-19
- METR: [Measuring the Impact of Early-2025 AI on Experienced Open-Source Developer Productivity](https://arxiv.org/pdf/2507.09089), undated
- METR: [Measuring the Impact of Early-2025 AI on Experienced Open-Source Developer Productivity](https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/), 2025-07-10
- Martin Fowler: [Agentic Programming](https://martinfowler.com/bliki/AgenticProgramming.html), 2026-05-21
- Mitchell Hashimoto: [My AI Adoption Journey](https://mitchellh.com/writing/my-ai-adoption-journey), 2026-02-05
- Mitchell Hashimoto: [Mitchell Hashimoto’s new way of writing code](https://newsletter.pragmaticengineer.com/p/mitchell-hashimoto), 2026-02-25
- OpenAI engineering: [Best practices | ChatGPT Learn](https://learn.chatgpt.com/guides/best-practices), undated
- OpenAI engineering: [Custom Code Review rules for Codex | OpenAI Developers](https://developers.openai.com/blog/custom-code-review-rules-for-codex/), undated
- OpenAI engineering: [Custom instructions with AGENTS.md | ChatGPT Learn](https://learn.chatgpt.com/docs/agent-configuration/agents-md), undated
- OpenAI engineering: [Harness engineering: leveraging Codex in an agent-first world](https://web.archive.org/web/20261006122733id_/https://openai.com/index/harness-engineering/), 2026-02-11
- Robert C. Martin: [Acceptance-Pipeline-Specification: README.md](https://github.com/unclebob/Acceptance-Pipeline-Specification/blob/main/README.md), undated
- Robert C. Martin: [swarm-forge: README.md](https://github.com/unclebob/swarm-forge/blob/main/README.md), undated
- Robert C. Martin: [Uncle Bob: Why I Stopped Reading Code and Building Harnesses | Aviator](https://www.aviator.co/podcast/uncle-bob-martin-ai-clean-code), 2026-09-24
- Simon Willison: [Writing about Agentic Engineering Patterns](https://simonwillison.net/2026/Feb/23/agentic-engineering-patterns/), 2026-02-23
- Simon Willison: [My fireside chat about agentic engineering at the Pragmatic Summit](https://simonwillison.net/2026/Mar/14/pragmatic-summit/), 2026-03-14
- Simon Willison: [Subagents - Agentic Engineering Patterns](https://simonwillison.net/guides/agentic-engineering-patterns/subagents/), 2026-03-17
- Simon Willison: [Thoughts on slowing the fuck down](https://simonwillison.net/2026/Mar/25/thoughts-on-slowing-the-fuck-down/), 2026-03-25
- Simon Willison: [Highlights from my conversation about agentic engineering on Lenny's Podcast](https://simonwillison.net/2026/Apr/2/lennys-podcast/), 2026-04-02
- Simon Willison: [scan-for-secrets 0.1](https://simonwillison.net/2026/Apr/5/scan-for-secrets-3/), 2026-04-05
- Simon Willison: [Vibe coding and agentic engineering are getting closer than I'd like](https://simonwillison.net/2026/May/6/vibe-coding-and-agentic-engineering/), 2026-05-06
- Simon Willison: [Have your agent record video demos of its work with shot-scraper video](https://simonwillison.net/2026/Jun/30/shot-scraper-video/), 2026-06-30
- Simon Willison: [More than just code review](https://simonwillison.net/2026/Aug/22/more-than-just-code-review/), 2026-08-22
- Steve Yegge: [beads: docs/core-concepts/index.md](https://github.com/gastownhall/beads/blob/main/docs/core-concepts/index.md), undated
- Steve Yegge: [beads: docs/getting-started/ide-setup.md](https://github.com/gastownhall/beads/blob/main/docs/getting-started/ide-setup.md), undated
- Steve Yegge: [gastown: docs/concepts/identity.md](https://github.com/gastownhall/gastown/blob/main/docs/concepts/identity.md), undated
- Steve Yegge: [The Flat Curve Society](https://steve-yegge.medium.com/the-flat-curve-society-36c8b01eb33b?source=rss-c1ec701babb7------2), 2026-06-19
- Steve Yegge: [The Shape of Things to Come, Part 1: The Continuous Thunderdome](https://yegge.ai/essays/the-shape-of-things-to-come/), 2026-08-02
- Steve Yegge: [Fences, not Sandboxes](https://yegge.ai/essays/fences-not-sandboxes/), 2026-08-24
- Thoughtworks: [Reflections on the future of Software Engineering retreat](https://www.thoughtworks.com/insights/articles/reflections-future-software-engineering-retreat), 2026-02-25
- Thoughtworks: [Beyond the hype: A real-world guide to building enterprise-grade AI agents](https://www.thoughtworks.com/insights/articles/a-real-world-guide-to-building-enterprise-grade-ai-agents), 2026-02-26
- Thoughtworks: [Claude Code and COBOL modernization: What’s the reality?](https://www.thoughtworks.com/insights/articles/claude-code-cobol-modernization-reality), 2026-03-02
- Thoughtworks: [Humans and Agents in Software Engineering Loops](https://martinfowler.com/articles/exploring-gen-ai/humans-and-agents.html), 2026-03-04
- Thoughtworks: [Patterns for Reducing Friction in AI-Assisted Development](https://martinfowler.com/articles/reduce-friction-ai/), 2026-04-08
- Thoughtworks: [Why AI is raising the stakes of the software engineering craft](https://www.thoughtworks.com/insights/blog/agile-engineering-practices/why-ai-raising-stakes-software-engineering-craft), 2026-04-28
- Thoughtworks: [The Orchestrator's Tax](https://martinfowler.com/articles/orchestrator-tax.html), 2026-07-16
- Thoughtworks: [Path to AI-first organization](https://www.thoughtworks.com/insights/articles/path-to-ai-first-organization), 2026-09-23
- Thoughtworks: [Quality is speed: Where engineering discipline moves in the AI era](https://www.thoughtworks.com/insights/articles/quality-is-speed-AI-era), 2026-10-06
- Unmesh Joshi: [Conversation: LLMs and the what/how loop](https://martinfowler.com/articles/convo-what-how.html), 2026-01-21
- Unmesh Joshi: [What Is Code?](https://martinfowler.com/articles/what-is-code.html), 2026-05-12
- Unmesh Joshi: [DSLs Enable Reliable Use of LLMs](https://martinfowler.com/articles/llm-and-dsls.html), 2026-07-14
