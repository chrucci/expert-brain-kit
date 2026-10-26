# Principles v0: building trust as fast as code

## Purpose and how to read it

This is version 0 of a set of principles for building efficient teams of humans and AI agents. It is meant to be tested, not obeyed: each principle is a hypothesis drawn from what leading practitioners and researchers have published, and the scoreboard says what a pilot team would measure to find out whether it holds. Each principle names the experts behind it with one short verified quote each. Its status is established when two or more experts back it with a verified quote, candidate when one does and inferred when none does; empirical support says whether any of the evidence is a measurement rather than opinion or experience. Where the experts disagree, the question is listed under Tensions with the experiment that would settle it.

## The thesis

Agents let teams produce code faster than they produce trust, so a team must build a system of trust that keeps up with the rate at which it builds code. Every principle below is read through that question: does it let trust keep pace with code? Repeatable, deterministic checks are one mechanism, because evidence is what trust is built on. The scoreboard sets the rate at which a team builds trust next to the rate at which it builds code.

> "We're accumulating code faster than we are accumulating trust."
> - quoted by Kent Beck in ["Trust Factory"](https://newsletter.kentbeck.com/p/trust-factory)

## Principles

### 1. Prove work is done independently of its author

A change counts as done only when something other than the agent that wrote it says so: tests, contract checks, builds, a real call to the endpoint or a pipeline run on sample data, in an environment the agent can run itself. Review comes from a separate fresh-context agent or a human, never from the authoring agent's own summary.

Trust: Trust comes from repeatable evidence that anyone can rerun, so it grows as fast as the checks run instead of as fast as people can read agent claims.

Status: established. Empirical support: measured. Experts: Anthropic engineering, OpenAI engineering, Addy Osmani, Thoughtworks, METR, Kent Beck, Simon Willison, Steve Yegge, Gergely Orosz.

- Anthropic engineering: "Software is comparatively easy to test and review—you can run code and see if it works—which makes it easier to trust an agent and catch its mistakes." ([source](https://www.anthropic.com/research/measuring-agent-autonomy))
- OpenAI engineering: "Codex can do this loop for you, but only if it knows what “good” looks like. That guidance can come from either the prompt or `AGENTS.md`." ([source](https://learn.chatgpt.com/guides/best-practices))
- Addy Osmani: "Every PR must pass: lint, type check, tests, build" ([source](https://github.com/addyosmani/agent-skills/blob/main/docs/copilot-setup.md))
- Thoughtworks: "Agents produce better code when they can gauge the quality of the code they produce themselves rather than relying on us to check it for them." ([source](https://martinfowler.com/articles/exploring-gen-ai/humans-and-agents.html))
- METR: "fully autonomous AI agents using Claude 3.7 Sonnet can often correctly implement the core functionality of issues on several repositories that are included in our study, although they fail to fully satisfy all requirements (typically leaving out important documentation, failing linting/styling rules, and leaving out key unit or integration tests)." ([source](https://arxiv.org/pdf/2507.09089#page=12))
- Kent Beck: "So it looks like we have an implementer and a verifier, which like informally, that's my kind of, that's my kind of division of labor." ([source](https://newsletter.kentbeck.com/p/genie-lessons-nobody-wants-agents?t=1594s))
- Simon Willison: "allowing them to test that code and iterate on it independently of turn-by-turn guidance from their human supervisor." ([source](https://simonwillison.net/2026/Feb/23/agentic-engineering-patterns/))
- Steve Yegge: "Do not commit, push, or run Dolt remote sync without explicit user or orchestrator approval." ([source](https://github.com/gastownhall/beads/blob/main/docs/getting-started/ide-setup.md))
- Gergely Orosz: "I really like this point Armin made just a few seconds ago that AI works best when the engineer stays in the loop and the system can actually validate what changed." ([source](https://newsletter.pragmaticengineer.com/p/building-pi-and-what-makes-self-modifying?t=2553s))

### 2. Name an accountable human for every change

Every agent-produced change, and every service or pipeline it touches, has a named human owner who answers for its quality and decides whether it ships. Commits and tickets record both the agent that did the work and the human who owns it, and the engineers who run a system in production help set the conditions under which agent changes enter it.

Trust: Trust needs someone who can be asked and held to account, and a named owner keeps accountability from disappearing as the volume of agent code grows.

Status: established. Empirical support: unmeasured. Experts: Kent Beck, Addy Osmani, Simon Willison, Andrej Karpathy, Martin Fowler, Gergely Orosz, Robert C. Martin, Steve Yegge, Charity Majors.

- Kent Beck: "This one is about what stays with us. Who cares whether the work is good? Who is accountable when it goes wrong?" ([source](https://newsletter.kentbeck.com/p/how-do-you-know-that))
- Addy Osmani: "A model cannot be paged and cannot be held responsible for what it shipped, so whoever clicks merge owns it." ([source](https://addyosmani.com/blog/agentic-code-review/))
- Simon Willison: "The moment you ship your vibe coding code for other people to use, where your bugs might actually harm somebody else, that’s when you need to take a step back." ([source](https://simonwillison.net/2026/Apr/2/lennys-podcast/))
- Andrej Karpathy: "Agentic engineering is about preserving the quality bar of professional software. You are not allowed to introduce vulnerabilities because of vibe coding. You are still responsible for your software, just as before." ([source](https://karpathy.bearblog.dev/sequoia-ascent-2026/))
- Martin Fowler: "This is a profound change to the nature of programming, where humans oversee LLM agents who generate the code. Humans are still responsible for what the software does and how it works, but use different skills to create their products." ([source](https://martinfowler.com/bliki/AgenticProgramming.html))
- Gergely Orosz: "AI handles much of the implementation, but engineers are setting the direction, and make continuous course corrections." ([source](https://newsletter.pragmaticengineer.com/p/ai-first-makeover-craft))
- Robert C. Martin: "The agents are not responsible for anything. They're entirely irresponsible. Only humans can be responsible, at the moment and probably over the next several years." ([source](https://www.aviator.co/podcast/uncle-bob-martin-ai-clean-code))
- Steve Yegge: "When you deploy AI agents at scale, anonymous work creates real problems:" ([source](https://github.com/gastownhall/gastown/blob/main/docs/concepts/identity.md))
- Charity Majors: "Which means software engineers who own the code should be, at minimum, *extremely involved* in defining the conditions for the code they agree to support." ([source](https://charity.wtf/p/ai-enthusiasts-are-in-a-race-against))

### 3. Turn every recurring agent mistake into a check

When an agent gets something wrong, or a reviewer makes the same comment twice, the team fixes the environment rather than the diff: rules that must always hold move out of prompts and into lint rules, tests, hooks or permissions, with error messages that tell the agent how to fix the problem. The team audits these checks regularly and prunes the ones newer models no longer need.

Trust: Each lesson becomes a check that runs on every future change, so trust builds up over time instead of depending on someone remembering the problem.

Status: established. Empirical support: unmeasured. Experts: Mitchell Hashimoto, Addy Osmani, OpenAI engineering, Thoughtworks, Birgitta Böckeler, Anthropic engineering, Steve Yegge.

- Mitchell Hashimoto: "It is the idea that anytime you find an agent makes a mistake, you take the time to engineer a solution such that the agent never makes that mistake again." ([source](https://mitchellh.com/writing/my-ai-adoption-journey))
- Addy Osmani: "The most important habit in harness engineering is treating agent mistakes as permanent signals." ([source](https://addyosmani.com/blog/agent-harness-engineering/))
- OpenAI engineering: "When Codex makes the same mistake twice, ask it for a retrospective and update `AGENTS.md`. Guidance stays practical and based on real friction." ([source](https://learn.chatgpt.com/guides/best-practices))
- Thoughtworks: "The orchestrator can grade its own session and surface clues, as it did here, but it cannot make that judgment call itself. The choice of what to codify, what to leave alone, and what might be an overreaction is still mine." ([source](https://martinfowler.com/articles/orchestrator-tax.html))
- Birgitta Böckeler: "A good harness should not necessarily aim to fully eliminate human input, but to direct it to where our input is most important." ([source](https://martinfowler.com/articles/exploring-gen-ai/harness-engineering-memo.html))
- Anthropic engineering: "when a coworker puts up a pull request and I'm like, this is lintable. I'll just be at Claude. Please write a lint rule for this in that PR on their PR." ([source](https://newsletter.pragmaticengineer.com/p/building-claude-code-with-boris-cherny?t=2656s))
- Steve Yegge: "Now rules go through a lifecycle, tightening each time they're re-violated: first custom, then advisories/warnings, then written law in the constitution that all agents must obey, and finally, mechanical enforcement: programs that refuse by policy, or observe and alert loudly." ([source](https://yegge.ai/essays/fences-not-sandboxes/))

### 4. Prove the tests catch broken behaviour

Humans write or approve the tests that encode intent, such as API contract tests, acceptance scenarios, data-quality checks and replayed production traffic, and the team uses mutation testing or a trusted reference implementation to confirm those tests fail when behaviour breaks. A green suite written by the agent, or high coverage, is not treated as proof that the behaviour is right or that the design is good.

Trust: Checks earn trust only when they are shown to fail on broken code, so proving the tests stops a passing suite from giving false confidence as agent output grows.

Status: established. Empirical support: unmeasured. Experts: Birgitta Böckeler, Unmesh Joshi, Robert C. Martin, Kent Beck, Simon Willison, Andrej Karpathy, Charity Majors.

- Birgitta Böckeler: "When the agent both writes the test and confirms it failed, a red test tells you the agent ran it and saw failure, not that the failure was for the right reason." ([source](https://martinfowler.com/articles/exploring-gen-ai/tdd-in-the-agent-loop.html))
- Unmesh Joshi: "This is also why generating test cases with LLMs to improve “test coverage” is not something I find very useful." ([source](https://martinfowler.com/articles/convo-what-how.html))
- Robert C. Martin: "Runs `bb gherkin-mutator` and improves scenarios or handlers until important mutations are killed." ([source](https://github.com/unclebob/Acceptance-Pipeline-Specification/blob/main/README.md))
- Kent Beck: "Exactly what she told it. Not at all what she wanted. Anyone working with agents today knows the feeling." ([source](https://newsletter.kentbeck.com/p/how-do-you-know-that))
- Simon Willison: "Having an existing conformance testing suite of the quality of `test262` is a huge unlock for projects of this magnitude, and the ability to compare output with an existing trusted implementation makes agentic engineering much more of a safe bet." ([source](https://simonwillison.net/2026/Feb/23/ladybird-adopts-rust/))
- Andrej Karpathy: "But I had a Python implementation that I fully understand, and I’m just making sure I’m making a more efficient version of it, and I have tests so I feel safer doing that stuff." ([source](https://www.dwarkesh.com/p/andrej-karpathy))
- Charity Majors: "Those tests and techniques are not about testing for correctness or what *ought* to be happening, they are about observing and encoding what *is* happening." ([source](https://charity.wtf/p/ai-demands-more-engineering-discipline))

### 5. Invest in verification, the real delivery bottleneck

The team measures where work waits and treats human verification capacity as the constraint, putting effort there instead of into generating more code. That means scoping agent tasks tightly, letting agents do a first review pass, and having them present legible evidence such as run logs, sample requests and responses, or before-and-after data diffs.

Trust: Trust is limited by how fast people can verify, so making verification faster is the most direct way to let trust keep up with code.

Status: established. Empirical support: measured. Experts: Thoughtworks, Addy Osmani, OpenAI engineering, DORA, Simon Willison, Andrej Karpathy, Anthropic engineering.

- Thoughtworks: "If extraction runs in parallel but SME capacity doesn't, review becomes the pacing function and timelines stretch." ([source](https://www.thoughtworks.com/insights/articles/ai-assisted-migration-lessons))
- Addy Osmani: "Scope discipline is the single biggest determinant of whether an agent’s PR is mergeable or has to be unwound." ([source](https://addyosmani.com/blog/agent-skills/))
- OpenAI engineering: "It also means more pull requests waiting for someone who knows what to look for, and code review can quickly become the bottleneck." ([source](https://developers.openai.com/blog/custom-code-review-rules-for-codex/))
- DORA: "With this insight, they can decide to apply AI to improve the code review process, rather than using AI to simply generate more code that will only exacerbate the bottleneck." ([source](https://services.google.com/fh/files/misc/2025_state_of_ai_assisted_software_development.pdf#page=76))
- Simon Willison: "Anyone who’s done any product work knows that your initial ideas are always wrong. What matters is proving them, and testing them." ([source](https://simonwillison.net/2026/Apr/2/lennys-podcast/))
- Andrej Karpathy: "we we're now kind of like cooperating with AIS and usually they are doing the generation and we as humans are doing the verification. It is in our interest to make this loop go as fast as possible." ([source](https://www.youtube.com/watch?v=LCEmiRjPEtQ&t=1320s))
- Anthropic engineering: "As Claude takes on more, I'd noticed I was reading plans less closely, and I wanted a way to stay engaged with its choices rather than just hand them off." ([source](https://claude.dev/blog/using-claude-code-the-unreasonable-effectiveness-of-html/))

### 6. Set agent autonomy by blast radius, widen with evidence

The team sorts work into explicit risk tiers by blast radius and reversibility, for example schema changes, auth and production data movement versus internal tooling, and gives each tier its own level of agent freedom, human gating and least-privilege access, with secrets kept out of the agent's reach. Autonomy widens only as logged intervention and failure rates stay low, and agents must stop and escalate when they hit those limits instead of working around them.

Trust: Autonomy grows only where evidence has already built trust, so the team never hands agents more freedom than its checks can back.

Status: established. Empirical support: measured. Experts: Thoughtworks, Charity Majors, Addy Osmani, OpenAI engineering, Andrej Karpathy, Mitchell Hashimoto, Gergely Orosz, Anthropic engineering, Steve Yegge, Simon Willison.

- Thoughtworks: "The final step is to package the code, test results, and my reasoning log, then notify the compliance manager for final approval." ([source](https://www.thoughtworks.com/insights/articles/a-real-world-guide-to-building-enterprise-grade-ai-agents))
- Charity Majors: "Better evals? Better tests? Better feature flags, guardrails, observability? Work on decoupling dependencies and reducing blast radius? Start with something small and out of the critical path?" ([source](https://charity.wtf/p/ai-enthusiasts-are-in-a-race-against))
- Addy Osmani: "You can use the `--dangerously-skip-permissions` flag only in trusted local projects where you want to bypass manual tool approval prompts." ([source](https://github.com/addyosmani/agent-skills/blob/main/docs/antigravity-setup.md))
- OpenAI engineering: "Keep approval and sandboxing tight by default, then loosen permissions only for trusted repos or specific workflows once the need is clear." ([source](https://learn.chatgpt.com/guides/best-practices))
- Andrej Karpathy: "you are in charge of the autonomy slider and depending on the complexity of the task at hand you can uh tune the amount of autonomy that you're willing to give up uh for that task" ([source](https://www.youtube.com/watch?v=LCEmiRjPEtQ&t=1229s))
- Mitchell Hashimoto: "If it's ghosty, I'm reviewing everything that's going into it." ([source](https://newsletter.pragmaticengineer.com/p/mitchell-hashimoto?t=4848s))
- Gergely Orosz: "you have services based on tier based on criticality, the highest tier software. now needs to have let's say two or three code reviews or an approval from a director to do a configuration change which again all slows down but it's kind of like we know that this is on purpose" ([source](https://newsletter.pragmaticengineer.com/p/building-pi-and-what-makes-self-modifying?t=4035s))
- Anthropic engineering: "effective oversight doesn’t require approving every action but being in a position to intervene when it matters." ([source](https://www.anthropic.com/research/measuring-agent-autonomy))
- Steve Yegge: "A **gate** parks a step until something external happens: a human sign-off, a timer, or a GitHub run or PR" ([source](https://github.com/gastownhall/beads/blob/main/docs/core-concepts/index.md))
- Simon Willison: "I'm often paranoid that one of my API keys or similar secrets might inadvertently be revealed in the detailed log files." ([source](https://simonwillison.net/2026/Apr/5/scan-for-secrets-3/))

### 7. Humans own intent, design and structural health

Humans decide what gets built and make the consequential design calls, such as identity and authorization, data models, service contracts and pipeline boundaries, while agents decide how to implement them. A named person watches the system's long-term structure and runs regular reviews to catch design drift and hidden tech debt.

Trust: Checks can confirm that code does what was asked, but only human-owned design keeps what was asked coherent, so trust holds at the system level as well as the change level.

Status: established. Empirical support: measured. Experts: Andrej Karpathy, Kent Beck, Thoughtworks, Simon Willison, Steve Yegge, Unmesh Joshi, Gergely Orosz, Birgitta Böckeler, Anthropic engineering.

- Andrej Karpathy: "Right now the agents are like interns. You still have to be in charge of aesthetics, judgment, taste, and oversight." ([source](https://karpathy.bearblog.dev/sequoia-ascent-2026/))
- Kent Beck: "At some point the complexity will exceed the genie’s capacity & it’s game over with lots of dollar signs left to play for." ([source](https://newsletter.kentbeck.com/p/earn-and-learn))
- Thoughtworks: "I think this is a clear example where an AI agent left to their own would have changed the codebase for the worse, and it took a developer with experience to notice the issue and to direct the agent to the correct implementation." ([source](https://martinfowler.com/articles/exploring-gen-ai/ccmenu-quality.html))
- Simon Willison: "AI worked great for the low level details but did not produce a coherent high-level architecture" ([source](https://simonwillison.net/2026/Apr/5/building-with-ai/))
- Steve Yegge: "The problem is, that is *thousands* of little decisions, many of which conflict and need a human to reconcile them." ([source](https://yegge.ai/essays/fences-not-sandboxes/))
- Unmesh Joshi: "They are a great help while we shape the design and its vocabulary, acting as brainstorming partners to help us explore the design space and discover the right abstractions. Once the vocabulary is established, LLMs work as an excellent natural language interface to it." ([source](https://martinfowler.com/articles/llm-and-dsls.html))
- Gergely Orosz: "When a codebase gets too complex, the human engineer feels the issues this creates." ([source](https://newsletter.pragmaticengineer.com/p/building-pi-and-what-makes-self-modifying?t=5504s))
- Birgitta Böckeler: "develop team rituals to maintain a good understanding of the codebase and catch drift early; keep an eye on the trend of number of files touched per change, and number of" ([source](https://martinfowler.com/articles/exploring-gen-ai/tdd-in-the-agent-loop.html))
- Anthropic engineering: "In practice, there is a clear division of labor in agentic coding––people decide what to build, and the agent decides how to build it." ([source](https://www.anthropic.com/research/claude-code-expertise))

### 8. Keep the team's understanding level with the code

The team regularly checks whether engineers can explain and debug recently agent-changed critical services without agent help, and encourages using agents to explain and teach rather than only to generate. It deliberately creates new learning paths for juniors to replace the starter work agents now take.

Trust: People can only vouch for systems they understand, so keeping understanding level with the code keeps human oversight meaningful.

Status: established. Empirical support: measured. Experts: Unmesh Joshi, Simon Willison, Thoughtworks, Addy Osmani, Anthropic engineering, Andrej Karpathy, Gergely Orosz, Kent Beck.

- Unmesh Joshi: "The problem is not that the LLM generated code. The problem is that the code introduced vocabulary faster than the developers built understanding." ([source](https://martinfowler.com/articles/what-is-code.html))
- Simon Willison: "It's so easy to let the codebase evolve outside of our abilities to reason clearly about it." ([source](https://simonwillison.net/2026/Mar/25/thoughts-on-slowing-the-fuck-down/))
- Thoughtworks: "As AI takes on more execution work, human contribution increasingly shifts toward judgment: deciding what to delegate, evaluating outputs and determining when intervention is required." ([source](https://www.thoughtworks.com/insights/articles/path-to-ai-first-organization))
- Addy Osmani: "And within the AI group, the strong results came from those who asked conceptual questions and requested explanations rather than treating the model as a code vending machine." ([source](https://addyosmani.com/blog/agentic-skill-decay/))
- Anthropic engineering: "The largest gap in scores between the two groups was on debugging questions, suggesting that the ability to understand when code is incorrect and why it fails may be a particular area of concern if AI impedes coding development." ([source](https://www.anthropic.com/research/AI-assistance-coding-skills))
- Andrej Karpathy: "But you still have to understand the fundamentals." ([source](https://karpathy.bearblog.dev/sequoia-ascent-2026/))
- Gergely Orosz: "And I do have this belief that when you're working with AI, like as long as we're learning, I think we're fine. As long as we stop learning and outsource the learning to this thing, trouble will be brewing maybe, you know, months or years down the road." ([source](https://newsletter.pragmaticengineer.com/p/ai-skills-with-matt-pocock?t=2133s))
- Kent Beck: "So, one way to think about this is a junior programmer is, you know, senior programmer writes some tests and the junior programmer goes and makes 'em pass or whatever." ([source](https://www.heavybit.com/library/podcasts/o11ycast/ep-80-augmented-coding-with-kent-beck))

### 9. Measure stability and rework alongside throughput, per service

For each service or pipeline, the team tracks throughput together with change failure rate, rework, escaped defects and data incidents against a pre-agent baseline, with the unit of work defined before measuring. AI wins are reported in the same forum as their downstream cleanup costs, and metrics serve the team's own improvement rather than per-person targets.

Trust: Paired outcome metrics show directly whether trust is keeping pace with code, and they expose the gap as soon as speed starts to outrun stability.

Status: established. Empirical support: measured. Experts: DORA, Thoughtworks, Gergely Orosz, Addy Osmani, Charity Majors, METR, Anthropic engineering, Simon Willison.

- DORA: "DORA’s research has repeatedly demonstrated that speed and stability are not tradeoffs. In fact, we see that the metrics are correlated for most teams." ([source](https://dora.dev/guides/dora-metrics/))
- Thoughtworks: "If an AI generates 200 lines of code in seconds, but a developer spends 30 minutes reviewing, debugging, and refactoring to fit team patterns, the net productivity gain is questionable." ([source](https://martinfowler.com/articles/reduce-friction-ai/))
- Gergely Orosz: "This is an observed thing that when you start to have more output, you increase your deployment frequency. You often, not always, but you often have more regressions." ([source](https://newsletter.pragmaticengineer.com/p/distributed-databases-with-peter?t=4967s))
- Addy Osmani: "Deciding on metric after-the-fact is probably not enough. Metrics can be put in place in advance, in a concise doc." ([source](https://addyosmani.com/blog/agentic-autonomy-levels/))
- Charity Majors: "The share of software engineering teams that work in short, fast feedback loops (the cardinal sign of discipline in my book) is, and always has been, appallingly small." ([source](https://charity.wtf/p/ai-demands-more-engineering-discipline))
- METR: "It’s possible for AI assistance to affect the outcomes without actually increasing productivity, e.g. by causing developers to write more verbose but functionally equivalent code, or causing them to break up pull requests into smaller chunks of work." ([source](https://arxiv.org/pdf/2507.09089#page=3))
- Anthropic engineering: "On the third bullet, don't confuse throughput with success. Throughput is one metric, but the real metric is measuring the thing you're trying to solve." ([source](https://claude.com/resources/articles/running-an-ai-native-engineering-org))
- Simon Willison: "Designing feedback loops to help "mend the gap in shared reality" between the two groups is a fascinating organizational design problem." ([source](https://simonwillison.net/2026/Jun/4/ai-enthusiasts-ai-skeptics/))

### 10. Put team knowledge where agents can read it

Conventions, invariants, business rules and operational steps go into short, versioned, reviewed files in the repository, and into CLIs and config-as-code instead of console click-throughs, so agents get the same context whoever is prompting. These files have owners, start small, grow only from observed failures, and are shared among teams with similar stacks.

Trust: When the standards agents work to are written down and reviewed like code, output quality stops depending on tacit knowledge, and the team can trust it consistently across people and services.

Status: established. Empirical support: measured. Experts: OpenAI engineering, Thoughtworks, Charity Majors, Anthropic engineering, Addy Osmani, Birgitta Böckeler, Steve Yegge, METR, Andrej Karpathy, Simon Willison.

- OpenAI engineering: "Create persistent defaults in your Codex home directory so every repository inherits your working agreements." ([source](https://learn.chatgpt.com/docs/agent-configuration/agents-md))
- Thoughtworks: "Every team has senior developers who instinctively know when code is right—they spot architectural drift, security gaps, and convention violations that others miss." ([source](https://martinfowler.com/articles/reduce-friction-ai/))
- Charity Majors: "The knowledge in our heads is unavailable to AI until we encode it into the system, after all." ([source](https://charity.wtf/p/ai-demands-more-engineering-discipline))
- Anthropic engineering: "The highest-signal content in any skill is the Gotchas section. These sections should be built up from common failure points that Claude runs into when using your skill." ([source](https://claude.dev/blog/lessons-from-building-claude-code-how-we-use-skills/))
- Addy Osmani: "Write the project rules file describing the real conventions, the ones in the code, not the ones in the wiki." ([source](https://github.com/addyosmani/agent-skills/blob/main/docs/adoption-guide.md))
- Birgitta Böckeler: "My recommendation would be to build context like rules files up gradually, and not pump too much stuff in there right from the start." ([source](https://martinfowler.com/articles/exploring-gen-ai/context-engineering-coding-agents.html))
- Steve Yegge: "Commit the instruction files (`AGENTS.md`, `CLAUDE.md`, `GEMINI.md`, as applicable) to git so all team members and AI tools get the same instructions." ([source](https://github.com/gastownhall/beads/blob/main/docs/getting-started/ide-setup.md))
- METR: "Our results also suggest that AI capabilities may be comparatively lower in settings with very high quality standards, or with many implicit requirements (e.g. relating to documentation, testing coverage, or linting/formatting) that take humans substantial time to learn." ([source](https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/))
- Andrej Karpathy: "All of this work and state is not even accessible or manipulatable by an LLM - how are we supposed to be automating society by 2027 like this?" ([source](https://karpathy.bearblog.dev/vibe-coding-menugen/))
- Simon Willison: "I really like this pattern where the `--help` output for a command provides enough detail that a coding agent can use it—it works kind of like bundling a `SKILL.md` file directly inside the tool." ([source](https://simonwillison.net/2026/Jun/30/shot-scraper-video/))

### 11. Treat code structure as agent infrastructure

The team invests in stable abstractions, enforced module and service boundaries, strong typing, schemas and small validated DSLs for things like pipeline definitions, because agents copy whatever patterns they find. It benchmarks a fixed change at checkpoints to see how structure affects agent cost and success.

Trust: A constrained, well-factored codebase narrows what agents can get wrong and lets machines validate more of their output, so each change needs less human trust.

Status: established. Empirical support: measured. Experts: Thoughtworks, Unmesh Joshi, Simon Willison, Birgitta Böckeler, Gergely Orosz, Kent Beck.

- Thoughtworks: "the same traits making high-quality software understandable to humans also allow AIs to understand it more quickly. Therefore, building high-quality software enables the AI to move faster as well." ([source](https://www.thoughtworks.com/insights/articles/quality-is-speed-AI-era))
- Unmesh Joshi: "Because abstractions form the essential vocabulary for the prompts, the generated program is more predictable and easier to review." ([source](https://martinfowler.com/articles/convo-what-how.html))
- Simon Willison: "If you’ve got a codebase with a bunch of patterns in, they will follow those patterns almost to a tee." ([source](https://simonwillison.net/2026/Mar/14/pragmatic-summit/))
- Birgitta Böckeler: "The harness described suggests that increasing trust and reliability required constraining the solution space: specific architectural patterns, enforced boundaries, standardized structures." ([source](https://martinfowler.com/articles/exploring-gen-ai/harness-engineering-memo.html))
- Gergely Orosz: "Old “enterprise” patterns are coming back in fashion for writing quality software, as agents are the new junior engineers" ([source](https://newsletter.pragmaticengineer.com/p/opencode))
- Kent Beck: "the genie only has to operate on a single file at a time, then it seems to operate much better. If I break it out into two files and now the genie has to make some change that spans two files, then it gets stupid again." ([source](https://newsletter.kentbeck.com/p/genie-sessions-optionality?t=3120s))

### 12. Parallelize only independent work, coordinated by deterministic machinery

Agents run in parallel only on work that splits cleanly, such as separate services, files or pipeline stages in their own worktrees, and each engineer finds their own limit from data on review quality and rework. Work state, claims, dependencies and handoffs live in a durable, version-controlled tracker or queue, not in agent sessions or a human's head.

Trust: Deterministic coordination keeps parallel work auditable and collision-free, so adding agents adds output without adding untracked risk.

Status: established. Empirical support: measured. Experts: Anthropic engineering, Addy Osmani, Kent Beck, Thoughtworks, Simon Willison, Steve Yegge, Robert C. Martin, Charity Majors.

- Anthropic engineering: "Split parallel tasks along file boundaries, merge the branches in a sensible order, and expect a session to report problems that another session is already fixing." ([source](https://claude.dev/blog/claude-code-in-the-cloud/))
- Addy Osmani: "The biggest bottleneck at this level is decomposition: defining the right slices to delegate." ([source](https://addyosmani.com/blog/agentic-autonomy-levels/))
- Kent Beck: "I was managing it. Watching which agent was doing what. Wondering when to interrupt. Holding state in my head that the system should have been holding for me." ([source](https://newsletter.kentbeck.com/p/genie-lessons-nobody-wants-agents))
- Thoughtworks: "Tasks that need the same mental model should usually stay together." ([source](https://martinfowler.com/articles/orchestrator-tax.html))
- Simon Willison: "I can fire up four agents in parallel and have them work on four different problems. And by like 11 AM, I am wiped out for the day." ([source](https://simonwillison.net/2026/Apr/2/lennys-podcast/))
- Steve Yegge: "I arrived at 18 by slowly adding them, as needed, until I found equilibrium: I don't really need any more than this, or it overwhelms the fleet." ([source](https://yegge.ai/essays/the-shape-of-things-to-come/))
- Robert C. Martin: "SwarmForge coordinates AI agents in isolated git worktrees and tmux sessions." ([source](https://github.com/unclebob/swarm-forge/blob/main/README.md))
- Charity Majors: "Ultimately, the answer to this question is you should run the number of agents that allows you to deliver impact most effectively, and you should do the work of generating the data to answer that question for yourself." ([source](https://www.honeycomb.io/blog/ai-norms-values-part-2-ai-honeycomb-engineering))

### 13. Choose models, tools and instructions by your own evals

The team keeps a small eval suite of its own representative tasks and reruns it whenever it changes a model, tool, prompt or rules file, comparing pass rate, cost, time and review effort instead of relying on benchmarks or folklore. It routes routine, checkable work to cheaper models and saves stronger models for design, review and hard debugging, letting the evals confirm that quality holds.

Trust: Evals turn the agent setup itself into something measured and repeatable, so the team can trust a change to its tooling for the same reason it trusts a code change.

Status: established. Empirical support: measured. Experts: Birgitta Böckeler, Thoughtworks, Andrej Karpathy, Kent Beck, OpenAI engineering, METR, Anthropic engineering, Addy Osmani, Steve Yegge.

- Birgitta Böckeler: "So I also did a few runs of my automated setup with reasoning off - and lo and behold, it's not only faster (which was to be expected), but also performed the same to slightly better!" ([source](https://martinfowler.com/articles/exploring-gen-ai/local-models-for-coding-factors.html))
- Thoughtworks: "Teams should always evaluate these tools using evals; doing so not only helps us measure how good our agents are over time, it also helps us assess which agents perform better for specific use cases." ([source](https://www.thoughtworks.com/insights/articles/claude-code-cobol-modernization-reality))
- Andrej Karpathy: "You have to explore the model they give you. It has no manual. It works in some settings and not others." ([source](https://karpathy.bearblog.dev/sequoia-ascent-2026/))
- Kent Beck: "I want to find out what augmented development is sensitive to. Does it matter what order we implement the tests in? Does it matter what priority we put on readability versus the next feature?" ([source](https://newsletter.kentbeck.com/p/run-right-and-fast-for-the-adaptive?t=668s))
- OpenAI engineering: "Try one change that should trigger the rule, one safe counterexample, and one unrelated change. Check that the first produces a useful finding and the others do not create noise, then refine the guidance from what you see." ([source](https://developers.openai.com/blog/custom-code-review-rules-for-codex/))
- METR: "benchmarks may overestimate model capabilities by only measuring performance on well-scoped, algorithmically scorable tasks." ([source](https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/))
- Anthropic engineering: "Sonnet 5.5 fits best when the task has a clear spec and a way to check the result." ([source](https://claude.dev/blog/building-with-claude-sonnet-5-5/))
- Addy Osmani: "Route the hard reasoning to a big model and the routine work, test generation, code review, CI checks, to a small cheap one. The quality holds and the bill comes down." ([source](https://addyosmani.com/blog/new-sdlc-vibe-coding/))
- Steve Yegge: "have agents hand off earlier in context (price is quadratic-ish in context length)" ([source](https://yegge.ai/essays/seats-and-sunsets/))

### 14. Build agent skill together, on real work

The team builds agentic skill hands-on in scheduled time, training whole teams together, managers included, on their actual services and pipelines and keeping pairing and peer review in the loop. It shares what works in visible channels and expects a productivity dip before the gains arrive.

Trust: Skill built together spreads calibrated judgment about when to trust agent output across the whole team instead of leaving it with a few enthusiasts.

Status: established. Empirical support: measured. Experts: DORA, Gergely Orosz, Steve Yegge, Simon Willison, METR, Kent Beck, Charity Majors, Thoughtworks.

- DORA: "Build trust with AI technologies through hands-on experience in sandbox or low-risk environments." ([source](https://services.google.com/fh/files/misc/2024_final_dora_report.pdf#page=46))
- Gergely Orosz: "If you’re a manager in your workplace, make the case for every engineer to have access to the best models so they can complete their own “impossible project,” or at least see how far they can go." ([source](https://newsletter.pragmaticengineer.com/p/ai-first-makeover-craft))
- Steve Yegge: "The trainees must bring their actual work, and the instructor(s) will help them learn how to do it with agents." ([source](https://steve-yegge.medium.com/the-flat-curve-society-36c8b01eb33b?source=rss-c1ec701babb7------2))
- Simon Willison: "The key skill required to make productive use of coding agents is being able to confidently instruct them on how to make changes and then confidently verify that those changes have been applied in the correct way." ([source](https://simonwillison.net/2026/Aug/22/more-than-just-code-review/))
- METR: "It also may be the case that there are strong learning effects for AI tools like Cursor that only appear after several hundred hours of usage—our developers typically only use Cursor for a few dozen hours before and during the study." ([source](https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/))
- Kent Beck: "So while we're in this extremely murky regime, um, it behooves us to try a little bit of everything and be a part of communities that are trying everything that we're missing." ([source](https://newsletter.kentbeck.com/p/genie-lessons-nobody-wants-agents?t=2025s))
- Charity Majors: "I want people who understand what we're trying to do. Understand how we're trying to do it or who are there to help us figure out how we're going to do it." ([source](https://newsletter.pragmaticengineer.com/p/stop-being-skeptical-about-ai-for?t=4284s))
- Thoughtworks: "Thoughtworks combined established agile practices, including agile pairing, shared ownership and peer review, with 18 AI skills and 12 reusable prompts." ([source](https://www.thoughtworks.com/insights/articles/strategic-ai-delivery-platform-modernization))

### 15. Staff for domain depth, breadth and senior oversight

The team staffs for domain and product knowledge and cross-functional breadth rather than raw coding throughput, and keeps the senior infrastructure, data and security people who can judge agent output. Product, operations and other non-engineers can make changes with agents, going through the same gates as engineers.

Trust: People who know the domain and the risky parts of the system can tell plausible agent output from correct output, so their judgment is what lets trust keep up as each person covers more ground.

Status: established. Empirical support: measured. Experts: Charity Majors, Addy Osmani, Kent Beck, Gergely Orosz, Anthropic engineering, Martin Fowler.

- Charity Majors: "Roles are blurring all over the place between eng and manager, eng and product, eng and business, eng and design, frontend eng and backend eng." ([source](https://www.honeycomb.io/blog/honeycomb-10-year-manifesto-part-1))
- Addy Osmani: "Developers with the deepest knowledge in one or two areas while maintaining broad literacy tend to deliver the best results." ([source](https://addyosmani.com/blog/earning-judgment/))
- Kent Beck: "The augmented development tools give us a chance to break down those silos. Now they also give us tools to enforce the silos more directly. And I hope we don't do that." ([source](https://newsletter.kentbeck.com/p/nobody-knows?t=1987s))
- Gergely Orosz: "Small teams that have the right skill set or see the right business opportunity or have advantages can do way more." ([source](https://newsletter.pragmaticengineer.com/p/from-ides-to-ai-agents-with-steve?t=1164s))
- Anthropic engineering: "What I index on less, on the other hand, is raw throughput; the models handle that. The more important question is where you still need human expertise, and that’s where I’d focus." ([source](https://claude.com/resources/articles/running-an-ai-native-engineering-org))
- Martin Fowler: "Additionally this raises the importance of programmers understanding the domain they are working with, collaborating with users and customers to iteratively define and build their product." ([source](https://martinfowler.com/bliki/AgenticProgramming.html))

## Tensions

- **Must humans read every agent diff?** (open): Should a human read and approve agent code line by line, or move human attention to intent and design while automated and agentic checks validate the code?
  - Gergely Orosz, Martin Fowler, Simon Willison: Keep an engaged human reviewer on agent changes, with extra friction on critical services, because people stop reading once output looks fine a few times.
  - Robert C. Martin, Charity Majors, Steve Yegge, Thoughtworks: Line-by-line review is slow and humans are poor validators. Check architecture, deployability and running behaviour, and let machines and layered agent review catch bugs.
  - Settle it: Within one service tier, randomly route agent PRs either to full line-by-line human review or to deterministic gates plus agent review plus a human design check, and compare escaped defects, incidents and review hours over a quarter.
- **How many agents should one engineer run?** (open): Should an engineer run one or two agents at a time, or scale to many parallel agents with coordination machinery?
  - Mitchell Hashimoto, Kent Beck, Robert C. Martin: Run one agent, two at most. Extra agents add cleanup and coordination work for the human.
  - Steve Yegge, Gergely Orosz, Addy Osmani: Run many agents in parallel, adding one at a time until throughput stops rising, with deterministic dispatch and owned areas to keep them apart.
  - Charity Majors: There is no team-wide answer. Each engineer finds their own count from their own data.
  - Settle it: Have engineers rotate through two-week periods at one, two, four and eight concurrent agents on comparable backlog work, recording merged changes after full review, human cleanup hours, rework and defects per period.
- **Can one person replace a team?** (open): Should a leader restructure toward individuals each owning large components with agents, or keep small multi-person teams that share the mental model?
  - Robert C. Martin: One human directing agents can do the work of five or six developers, so teams become individuals owning components behind narrow interfaces.
  - Thoughtworks, Simon Willison, Kent Beck: Teams shrink but not to one. Several people are needed to share the cognitive load, hold the mental model and build trust through daily collaboration.
  - Settle it: Run comparable components with one owner plus agents against a team of two or three plus agents for six months, tracking functionality delivered, incident response time, defects and what happens when the solo owner is away.
- **Trust reported speedups or measure them?** (leaning): Should a leader resize and restructure teams on practitioner reports of large agent speedups, or only on controlled measurement of real work?
  - METR, Gergely Orosz (measured): Self-reports and forecasts are unreliable, even about direction; experienced developers on mature repos were measured 19% slower while believing they were faster.
  - Thoughtworks, Steve Yegge: Small agent-assisted teams have delivered work estimated for far larger teams, so projects can be staffed with fewer people now.
  - Settle it: Randomly assign scoped backlog tasks to AI-allowed and AI-disallowed conditions on the team's own codebase, record completion time, and compare with the developers' forecasts and estimates.
- **Does AI help novices or experts more?** (open): Should a team point agents mainly at unfamiliar code and tasks, or at its deepest domain experts working in their own areas?
  - METR (measured): AI help is worth most on unfamiliar tasks and small greenfield work and least where the developer is already an expert.
  - Anthropic engineering, Gergely Orosz, Simon Willison (measured): Agents amplify existing expertise, so domain and systems experts get the most out of them and should be staffed and hired for.
  - Settle it: Break down agent-assisted task time and verified success by the engineer's prior exposure to the code, separating speed (METR's measure) from quality of outcome (Anthropic's measure).
- **Is token spend a useful team metric?** (leaning): Should a leader track and encourage per-engineer token spend during adoption, or ignore activity measures in favour of outcomes?
  - Steve Yegge (measured): Token spend shows real practice and is worth pushing up to around 15M tokens a day before switching to waste and outcomes per token.
  - DORA, Gergely Orosz, Charity Majors (measured): Usage and token counts reward looking busy and invite gaming; judge AI only by delivery outcomes and never set individual usage targets.
  - Settle it: Over two quarters, correlate each engineer's token spend with their change fail rate, rework and lead time, and check whether teams told to raise spend improve outcomes more than teams given only outcome goals.
- **Should teams prescribe test-first to agents?** (leaning): Should the team instruct agents to follow a test-first process such as TDD, or only verify outcomes and leave the process to the agent?
  - Birgitta Böckeler (measured): Prescribing TDD added cost with no measured quality gain; enforce what must happen with hooks and invest in feedback on results.
  - Simon Willison, Kent Beck, Robert C. Martin: Agents should work test-first in small test-gated steps, because without it they drift, skip tests or delete assertions.
  - Settle it: Run the same set of tasks with and without TDD instructions, several runs each, and compare blind quality rankings, mutation scores, defects and tokens per task.
- **Write docs or just ask the agent?** (open): Should a team write and maintain documents recording intent and decisions, or keep code simple and ask the agent when questions arise?
  - Kent Beck: Agents weaken the case for docs and ADRs; ask the agent about the source instead of writing documents that go stale.
  - Gergely Orosz, OpenAI engineering, Charity Majors: Intent, decisions and tacit rules are not in the code, so record them in versioned files beside it or they are lost to people and agents.
  - Settle it: Collect real questions engineers ask about a service, answer half by asking an agent of the code alone and half with linked specs and decision logs, and score accuracy and time, especially for why-questions.
- **Spec up front or evolve a prototype?** (open): Should agent work start from a human-approved spec and plan, or from a shared prototype evolved in short visible cycles?
  - Addy Osmani, Thoughtworks, Gergely Orosz: Agents should build from a precise, approved spec and staged design checkpoints, because ambiguity multiplies across agents.
  - Steve Yegge: At agent speed, evolve a living prototype in the open instead of writing a big upfront spec.
  - Kent Beck: Whether spec-first fits depends on whether the software is a one-off or must keep paying for its next step, so decide that first.
  - Settle it: Label features as one-off or long-lived, run comparable features spec-first and prototype-first, and compare idea-to-ship time, rework and later rewrite rates.
- **Should engineers keep writing code by hand?** (open): Should engineers keep hand-writing and reshaping a meaningful share of code, or move almost entirely to directing, specifying and harness work?
  - Unmesh Joshi, Mitchell Hashimoto: Humans should keep writing and reshaping code, because design is discovered by writing it and skills only grow in work not delegated.
  - Charity Majors, Anthropic engineering, OpenAI engineering (measured): The human job moves from typing code to deciding what to build, writing specs, interpreting production and improving the harness.
  - Settle it: Compare modules where humans authored or refactored the structure with modules merged as generated, on later change lead time and readability, and run periodic debugging checks on engineers by how much they hand-code.
- **Small batches or megabatches onto main?** (leaning): When agents commit faster than the build can verify, should a team hold to small verified changes or land large batches and roll forward?
  - Steve Yegge: Land large batches onto main together and have agents diagnose and fix breakage, since one green build per commit becomes impossible.
  - DORA, Addy Osmani (measured): Keep each change small and rollback cheap; larger changes are slower and less stable, and AI makes holding this discipline more important.
  - Settle it: On a high-commit-rate repo, alternate periods of batched bisection with small changes and megabatch landing, comparing time main stays red, commit-to-landing time and production failures.
- **Validate before merge or in production?** (open): Should a team put its validation effort into pre-merge deterministic gates or into fast production observation with flags and progressive rollout?
  - Charity Majors: Pre-production checks quickly stop paying off; replace merge-and-hope with deploy, observe and learn using flags, rollouts and traces.
  - Addy Osmani, Thoughtworks, Anthropic engineering: Work is done only when deterministic checks in the loop prove it before merge, so failures are caught before a human or user sees them.
  - Settle it: For a set of services, shift spend toward either stronger pre-merge gates or production telemetry and progressive rollout, and track where defects are caught and how fast failures are found and fixed.
- **Specialist role pipelines or lean subagents?** (open): Should a team split agent work into a fixed pipeline of specialist roles, or keep one main agent and use subagents only to protect context and cut cost?
  - Robert C. Martin, Steve Yegge: Divide work into distinct agent roles (specifier, coder, cleaner, architect, QA, or worker, supervisor, merger) each owning one concern.
  - Simon Willison, Kent Beck (measured): Role swarms add coordination cost without matching benefit; use subagents for context isolation and cheaper models only.
  - Settle it: Run the same features through a role pipeline and through a single agent with subagents, comparing escaped defects, rework, tokens per task and human coordination time.
- **Slow down, or speed is safety?** (open): Should a team deliberately slow agent-driven delivery until trust catches up, or push throughput on the basis that speed and stability rise together?
  - Kent Beck, Birgitta Böckeler: Agents produce code faster than trust; slow down so it really works and lean on trust-building practices.
  - DORA (measured): Throughput and stability improve together and going slower does not make delivery safer; measure both and fix instability directly.
  - Settle it: Track deployment frequency, lead time, change fail rate and rework per service as AI adoption grows, and test whether services that throttled agent output saw lower instability than those that did not.

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
- Addy Osmani: [agent-skills: docs/antigravity-setup.md](https://github.com/addyosmani/agent-skills/blob/main/docs/antigravity-setup.md), undated
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
- Anthropic engineering: [Using Claude Code: The unreasonable effectiveness of HTML](https://claude.dev/blog/using-claude-code-the-unreasonable-effectiveness-of-html/), 2026-05-20
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
- Charity Majors: [AI enthusiasts are in a race against time, AI skeptics are in a race against entropy](https://charity.wtf/p/ai-enthusiasts-are-in-a-race-against), 2026-06-02
- Charity Majors: [AI demands more engineering discipline. Not less](https://charity.wtf/p/ai-demands-more-engineering-discipline), 2026-06-15
- Charity Majors: [Stop being skeptical about AI for development with Charity Majors](https://newsletter.pragmaticengineer.com/p/stop-being-skeptical-about-ai-for), 2026-08-12
- Charity Majors: [AI Norms & Values, Part 2 of 3: AI for Honeycomb Engineering](https://www.honeycomb.io/blog/ai-norms-values-part-2-ai-honeycomb-engineering), 2026-09-02
- DORA: [Accelerate](https://services.google.com/fh/files/misc/2024_final_dora_report.pdf), 2024-11-19
- DORA: [State of AI-assisted](https://services.google.com/fh/files/misc/2025_state_of_ai_assisted_software_development.pdf), 2025-10-15
- DORA: [DORA | DORA’s software delivery performance metrics](https://dora.dev/guides/dora-metrics/), 2026-01-05
- Gergely Orosz: [Inside a five-year-old startup’s rapid AI makeover](https://newsletter.pragmaticengineer.com/p/ai-first-makeover-craft), 2026-01-27
- Gergely Orosz: [From IDEs to AI Agents with Steve Yegge](https://newsletter.pragmaticengineer.com/p/from-ides-to-ai-agents-with-steve), 2026-03-11
- Gergely Orosz: [Building Pi, and what makes self-modifying software so fascinating](https://newsletter.pragmaticengineer.com/p/building-pi-and-what-makes-self-modifying), 2026-04-29
- Gergely Orosz: [Building OpenCode with Dax Raad](https://newsletter.pragmaticengineer.com/p/opencode), 2026-05-27
- Gergely Orosz: [AI Skills with Matt Pocock](https://newsletter.pragmaticengineer.com/p/ai-skills-with-matt-pocock), 2026-09-17
- Gergely Orosz: [Distributed databases with Peter Mattis](https://newsletter.pragmaticengineer.com/p/distributed-databases-with-peter), 2026-09-30
- Kent Beck: [Genie Sessions: Optionality](https://newsletter.kentbeck.com/p/genie-sessions-optionality), 2026-01-30
- Kent Beck: [Earn *And* Learn](https://newsletter.kentbeck.com/p/earn-and-learn), 2026-02-18
- Kent Beck: [Nobody Knows](https://newsletter.kentbeck.com/p/nobody-knows), 2026-03-25
- Kent Beck: [Genie Lessons: Nobody Wants Agents](https://newsletter.kentbeck.com/p/genie-lessons-nobody-wants-agents), 2026-04-23
- Kent Beck: [Genie Sessions: Run, Right, and Fast for the Adaptive Radix Tree](https://newsletter.kentbeck.com/p/run-right-and-fast-for-the-adaptive), 2026-05-02
- Kent Beck: [Trust Factory](https://newsletter.kentbeck.com/p/trust-factory), 2026-06-02
- Kent Beck: [How Do You Know That?](https://newsletter.kentbeck.com/p/how-do-you-know-that), 2026-07-22
- Kent Beck: [O11ycast | Ep. #80, Augmented Coding with Kent Beck | Heavybit](https://www.heavybit.com/library/podcasts/o11ycast/ep-80-augmented-coding-with-kent-beck), 2026-09-17
- METR: [Measuring the Impact of Early-2025 AI on Experienced Open-Source Developer Productivity](https://arxiv.org/pdf/2507.09089), undated
- METR: [Measuring the Impact of Early-2025 AI on Experienced Open-Source Developer Productivity](https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/), 2025-07-10
- Martin Fowler: [Agentic Programming](https://martinfowler.com/bliki/AgenticProgramming.html), 2026-05-21
- Mitchell Hashimoto: [My AI Adoption Journey](https://mitchellh.com/writing/my-ai-adoption-journey), 2026-02-05
- Mitchell Hashimoto: [Mitchell Hashimoto’s new way of writing code](https://newsletter.pragmaticengineer.com/p/mitchell-hashimoto), 2026-02-25
- OpenAI engineering: [Best practices | ChatGPT Learn](https://learn.chatgpt.com/guides/best-practices), undated
- OpenAI engineering: [Custom Code Review rules for Codex | OpenAI Developers](https://developers.openai.com/blog/custom-code-review-rules-for-codex/), undated
- OpenAI engineering: [Custom instructions with AGENTS.md | ChatGPT Learn](https://learn.chatgpt.com/docs/agent-configuration/agents-md), undated
- Robert C. Martin: [Acceptance-Pipeline-Specification: README.md](https://github.com/unclebob/Acceptance-Pipeline-Specification/blob/main/README.md), undated
- Robert C. Martin: [swarm-forge: README.md](https://github.com/unclebob/swarm-forge/blob/main/README.md), undated
- Robert C. Martin: [Uncle Bob: Why I Stopped Reading Code and Building Harnesses | Aviator](https://www.aviator.co/podcast/uncle-bob-martin-ai-clean-code), 2026-09-24
- Simon Willison: [Ladybird adopts Rust, with help from AI](https://simonwillison.net/2026/Feb/23/ladybird-adopts-rust/), 2026-02-23
- Simon Willison: [Writing about Agentic Engineering Patterns](https://simonwillison.net/2026/Feb/23/agentic-engineering-patterns/), 2026-02-23
- Simon Willison: [My fireside chat about agentic engineering at the Pragmatic Summit](https://simonwillison.net/2026/Mar/14/pragmatic-summit/), 2026-03-14
- Simon Willison: [Thoughts on slowing the fuck down](https://simonwillison.net/2026/Mar/25/thoughts-on-slowing-the-fuck-down/), 2026-03-25
- Simon Willison: [Highlights from my conversation about agentic engineering on Lenny's Podcast](https://simonwillison.net/2026/Apr/2/lennys-podcast/), 2026-04-02
- Simon Willison: [Eight years of wanting, three months of building with AI](https://simonwillison.net/2026/Apr/5/building-with-ai/), 2026-04-05
- Simon Willison: [scan-for-secrets 0.1](https://simonwillison.net/2026/Apr/5/scan-for-secrets-3/), 2026-04-05
- Simon Willison: [AI enthusiasts are in a race against time, AI skeptics are in a race against entropy](https://simonwillison.net/2026/Jun/4/ai-enthusiasts-ai-skeptics/), 2026-06-04
- Simon Willison: [Have your agent record video demos of its work with shot-scraper video](https://simonwillison.net/2026/Jun/30/shot-scraper-video/), 2026-06-30
- Simon Willison: [More than just code review](https://simonwillison.net/2026/Aug/22/more-than-just-code-review/), 2026-08-22
- Steve Yegge: [beads: docs/core-concepts/index.md](https://github.com/gastownhall/beads/blob/main/docs/core-concepts/index.md), undated
- Steve Yegge: [beads: docs/getting-started/ide-setup.md](https://github.com/gastownhall/beads/blob/main/docs/getting-started/ide-setup.md), undated
- Steve Yegge: [gastown: docs/concepts/identity.md](https://github.com/gastownhall/gastown/blob/main/docs/concepts/identity.md), undated
- Steve Yegge: [The Flat Curve Society](https://steve-yegge.medium.com/the-flat-curve-society-36c8b01eb33b?source=rss-c1ec701babb7------2), 2026-06-19
- Steve Yegge: [The Shape of Things to Come, Part 1: The Continuous Thunderdome](https://yegge.ai/essays/the-shape-of-things-to-come/), 2026-08-02
- Steve Yegge: [Fences, not Sandboxes](https://yegge.ai/essays/fences-not-sandboxes/), 2026-08-24
- Steve Yegge: [Seats and Sunsets](https://yegge.ai/essays/seats-and-sunsets/), 2026-09-15
- Thoughtworks: [Assessing internal quality while coding with an agent](https://martinfowler.com/articles/exploring-gen-ai/ccmenu-quality.html), 2026-01-27
- Thoughtworks: [Beyond the hype: A real-world guide to building enterprise-grade AI agents](https://www.thoughtworks.com/insights/articles/a-real-world-guide-to-building-enterprise-grade-ai-agents), 2026-02-26
- Thoughtworks: [Claude Code and COBOL modernization: What’s the reality?](https://www.thoughtworks.com/insights/articles/claude-code-cobol-modernization-reality), 2026-03-02
- Thoughtworks: [Humans and Agents in Software Engineering Loops](https://martinfowler.com/articles/exploring-gen-ai/humans-and-agents.html), 2026-03-04
- Thoughtworks: [Patterns for Reducing Friction in AI-Assisted Development](https://martinfowler.com/articles/reduce-friction-ai/), 2026-04-08
- Thoughtworks: [AI-assisted migration: Critical lessons from the modernization frontlines](https://www.thoughtworks.com/insights/articles/ai-assisted-migration-lessons), 2026-07-13
- Thoughtworks: [The Orchestrator's Tax](https://martinfowler.com/articles/orchestrator-tax.html), 2026-07-16
- Thoughtworks: [Lessons from platform modernization that every AI program needs](https://www.thoughtworks.com/insights/articles/strategic-ai-delivery-platform-modernization), 2026-09-04
- Thoughtworks: [Path to AI-first organization](https://www.thoughtworks.com/insights/articles/path-to-ai-first-organization), 2026-09-23
- Thoughtworks: [Quality is speed: Where engineering discipline moves in the AI era](https://www.thoughtworks.com/insights/articles/quality-is-speed-AI-era), 2026-10-06
- Unmesh Joshi: [Conversation: LLMs and the what/how loop](https://martinfowler.com/articles/convo-what-how.html), 2026-01-21
- Unmesh Joshi: [What Is Code?](https://martinfowler.com/articles/what-is-code.html), 2026-05-12
- Unmesh Joshi: [DSLs Enable Reliable Use of LLMs](https://martinfowler.com/articles/llm-and-dsls.html), 2026-07-14
