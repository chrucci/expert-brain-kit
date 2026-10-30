# House principles

Chris's own principles for his teams, kept in `house-principles.yaml` in chrucci/expert-brain.
They are hypotheses, not findings: the home pipeline tests each one against every expert principle and lists the experts who support it and the experts who argue against it.

## The thesis

Agents let teams produce code faster than they produce trust, so a team must build a system of trust that keeps up with the rate at which it builds code. Every principle below is read through that question: does it let trust keep pace with code? Repeatable, deterministic checks are one mechanism, because evidence is what trust is built on. The scoreboard sets the rate at which a team builds trust next to the rate at which it builds code.

> "We're accumulating code faster than we are accumulating trust."
> - quoted by Kent Beck in ["Trust Factory"](https://newsletter.kentbeck.com/p/trust-factory)

The thesis is Chris's framing, not a principle the pipeline tests.

## Lean on determinism for validation, testing and verification

House principle by Chris, 2026-10-10

Prefer deterministic processes to non-deterministic ones wherever they can do the job, above all for validation, testing and verification. LLMs have solid uses, such as generating code, writing tests and writing static-analysis rules, but the checks that validate the work must be repeatable processes that run the same way every time, not an agent judging whether the code is right, well styled or secure.

Anti-pattern: The agentic golden hammer: doing everything agentically, for example having the agent say whether the code is right instead of writing a unit test in an ordinary language.

Dimension: Deterministic guardrails
Metric: Share of merge-blocking checks that are deterministic (tests, static analysis, CI rules) versus model-judged, and how often model-judged checks change their verdict when re-run on the same change.

### Supported by
- Thoughtworks: Enforce agent work with deterministic sensors in the loop (probability 0.97, [principles/thoughtworks/enforce-agent-work-with-deterministic-sensors-in-the-loop.md](principles/thoughtworks/enforce-agent-work-with-deterministic-sensors-in-the-loop.md))
  - "Agents produce better code when they can gauge the quality of the code they produce themselves rather than relying on us to check it for them."
- Addy Osmani: Deterministic checks, not the agent, decide when work is done (probability 0.97, [principles/osmani/deterministic-checks-not-the-agent-decide-when-work-is-done.md](principles/osmani/deterministic-checks-not-the-agent-decide-when-work-is-done.md))
  - "Goal: every area the agent will touch gets a safety net first."
- Charity Majors: Move trust from authorship to deterministic validation (probability 0.96, [principles/majors/move-trust-from-authorship-to-deterministic-validation.md](principles/majors/move-trust-from-authorship-to-deterministic-validation.md))
  - "If you're debiting from this trust account and the creation of the code, it has to get built up somewhere else."
- Gergely Orosz: Close the loop with mechanical validation (probability 0.96, [principles/orosz/close-the-loop-with-mechanical-validation.md](principles/orosz/close-the-loop-with-mechanical-validation.md))
  - "Tools that help agents get feedback – CLIs like Claude Code, Codex, and similar – have been a big boost."
- Anthropic engineering: Done means a check the agent can run (probability 0.96, [principles/anthropic/done-means-a-check-the-agent-can-run.md](principles/anthropic/done-means-a-check-the-agent-can-run.md))
  - "Software is comparatively easy to test and review—you can run code and see if it works—which makes it easier to trust an agent and catch its mistakes."
- OpenAI engineering: A checkable definition of done, proven by fast execution (probability 0.96, [principles/openai/a-checkable-definition-of-done-proven-by-fast-execution.md](principles/openai/a-checkable-definition-of-done-proven-by-fast-execution.md))
  - "Codex can do this loop for you, but only if it knows what “good” looks like. That guidance can come from either the prompt or `AGENTS.md`."
- OpenAI engineering: Deterministic checks in CI, model review only for judgment (probability 0.96, [principles/openai/deterministic-checks-in-ci-model-review-only-for-judgment.md](principles/openai/deterministic-checks-in-ci-model-review-only-for-judgment.md))
  - "Keep rules concise, explain the behavior to flag and any safe path or exception, and reserve formatting and lint checks for CI."
- METR: Use deterministic gates to finish agent work (probability 0.95, [principles/metr/use-deterministic-gates-to-finish-agent-work.md](principles/metr/use-deterministic-gates-to-finish-agent-work.md))
  - "fully autonomous AI agents using Claude 3.7 Sonnet can often correctly implement the core functionality of issues on several repositories that are included in our study, although they fail to fully satisfy all requirements (typically leaving out important documentation, failing linting/styling rules, and leaving out key unit or integration tests)."
- Steve Yegge: Agents never land their own work: a gated merge queue decides (probability 0.95, [principles/yegge/agents-never-land-their-own-work-a-gated-merge-queue-decides.md](principles/yegge/agents-never-land-their-own-work-a-gated-merge-queue-decides.md))
  - "Do not commit, push, or run Dolt remote sync without explicit user or orchestrator approval."
- Simon Willison: Automated tests are mandatory, and agents work test-first (probability 0.95, [principles/willison/automated-tests-are-mandatory-and-agents-work-test-first.md](principles/willison/automated-tests-are-mandatory-and-agents-work-test-first.md))
  - "When you implement this use playwright and red/green TDD, plan that too"
- Anthropic engineering: Move rules out of prompts and into deterministic gates (probability 0.95, [principles/anthropic/move-rules-out-of-prompts-and-into-deterministic-gates.md](principles/anthropic/move-rules-out-of-prompts-and-into-deterministic-gates.md))
  - "We have type checkers. We have linters. We run the build. Claude is actually so good at writing lint rules."
- Robert C. Martin: Agree on shared deterministic gates and loosen thresholds only as agents improve (probability 0.95, [principles/unclebob/agree-on-shared-deterministic-gates-and-loosen-thresholds-only-as-agents-improve.md](principles/unclebob/agree-on-shared-deterministic-gates-and-loosen-thresholds-only-as-agents-improve.md))
  - "If you don't have agents write unit tests, so far as I have seen, they will go off into Wonderland."
- Andrej Karpathy: Gate agent rewrites with tests and a trusted reference (probability 0.94, [principles/karpathy/gate-agent-rewrites-with-tests-and-a-trusted-reference.md](principles/karpathy/gate-agent-rewrites-with-tests-and-a-trusted-reference.md))
  - "But I had a Python implementation that I fully understand, and I’m just making sure I’m making a more efficient version of it, and I have tests so I feel safer doing that stuff."
- Charity Majors: Humans judge what to build; machines are the quality gate (probability 0.94, [principles/majors/humans-judge-what-to-build-machines-are-the-quality-gate.md](principles/majors/humans-judge-what-to-build-machines-are-the-quality-gate.md))
  - "Human brains are *not good* at validation. The nitpickiness, the repetition. This is the worst thing to be clinging to, y’all."
- Addy Osmani: Grow the harness from real failures and prune it (probability 0.94, [principles/osmani/grow-the-harness-from-real-failures-and-prune-it.md](principles/osmani/grow-the-harness-from-real-failures-and-prune-it.md))
  - "Adoption should make quality monotonically better: each phase adds a gate that doesn't come back off. If a month in you can't name what's now enforced that wasn't before, the rollout has stalled."
- Robert C. Martin: Deterministic plumbing owns coordination, agents own adaptation (probability 0.94, [principles/unclebob/deterministic-plumbing-owns-coordination-agents-own-adaptation.md](principles/unclebob/deterministic-plumbing-owns-coordination-agents-own-adaptation.md))
  - "Some pipeline tools are pre-supplied Go commands from this repository. Other components are project-dependent and are written by the agents responsible for installing and maintaining acceptance testing in the target project."
- Kent Beck: Rein in the agent with small, test-gated steps (probability 0.93, [principles/beck/rein-in-the-agent-with-small-test-gated-steps.md](principles/beck/rein-in-the-agent-with-small-test-gated-steps.md))
  - "So I'm gonna keep using tests because it makes sense to me to use tests. And I've had really bad experiences with the genie not using tests. or deleting tests or taking assertions out of tests."
- Charity Majors: Encode the team's knowledge into the system (probability 0.93, [principles/majors/encode-the-team-s-knowledge-into-the-system.md](principles/majors/encode-the-team-s-knowledge-into-the-system.md))
  - "Those tests and techniques are not about testing for correctness or what *ought* to be happening, they are about observing and encoding what *is* happening."
- Addy Osmani: Encode team process as shared, tested skill workflows (probability 0.93, [principles/osmani/encode-team-process-as-shared-tested-skill-workflows.md](principles/osmani/encode-team-process-as-shared-tested-skill-workflows.md))
  - "Maintaining per-agent metadata by hand across every skill is repetitive, drifts out of sync, and is easy to get wrong. A better approach is to keep a single source of truth and generate the agent-specific output:"
- Anthropic engineering: Measure verified outcomes with noise-aware evals (probability 0.93, [principles/anthropic/measure-verified-outcomes-with-noise-aware-evals.md](principles/anthropic/measure-verified-outcomes-with-noise-aware-evals.md))
  - "This one's interesting to dig into because it might help you identify where your pipeline is struggling to scale. As we’re generating so much more code, sometimes build systems and continuous integration (CI) may struggle to keep up."
- Thoughtworks: Verification is the bottleneck; spend human review by risk (probability 0.92, [principles/thoughtworks/verification-is-the-bottleneck-spend-human-review-by-risk.md](principles/thoughtworks/verification-is-the-bottleneck-spend-human-review-by-risk.md))
  - "If extraction runs in parallel but SME capacity doesn't, review becomes the pacing function and timelines stretch."
- OpenAI engineering: Evaluate agent instructions like code (probability 0.92, [principles/openai/evaluate-agent-instructions-like-code.md](principles/openai/evaluate-agent-instructions-like-code.md))
  - "Codex could find and cite local guidance that a default review might miss, but broad instructions could easily create noise."
- Robert C. Martin: Prove acceptance tests are wired to the application (probability 0.92, [principles/unclebob/prove-acceptance-tests-are-wired-to-the-application.md](principles/unclebob/prove-acceptance-tests-are-wired-to-the-application.md))
  - "The normal run proves that the project satisfies the feature. The mutation run checks whether the acceptance tests fail when important example values change."
- Birgitta Böckeler: Agent-written tests are not proof of correctness (probability 0.91, [principles/bockeler/agent-written-tests-are-not-proof-of-correctness.md](principles/bockeler/agent-written-tests-are-not-proof-of-correctness.md))
  - "When the agent both writes the test and confirms it failed, a red test tells you the agent ran it and saw failure, not that the failure was for the right reason."
- Birgitta Böckeler: Pair guides with fast, self-correcting sensors (probability 0.91, [principles/bockeler/pair-guides-with-fast-self-correcting-sensors.md](principles/bockeler/pair-guides-with-fast-self-correcting-sensors.md))
  - "Separately, you get either an agent that keeps repeating the same mistakes (feedback-only) or an agent that encodes rules but never finds out whether they worked (feed-forward-only)."
- OpenAI engineering: Engineers own the harness and turn each agent failure into a lasting fix (probability 0.91, [principles/openai/engineers-own-the-harness-and-turn-each-agent-failure-into-a-lasting-fix.md](principles/openai/engineers-own-the-harness-and-turn-each-agent-failure-into-a-lasting-fix.md))
  - "Keep it practical. A short, accurate `AGENTS.md` is more useful than a long file full of vague rules. Start with the basics, then add new rules only after you notice repeated mistakes."
- Kent Beck: Slow down until trust catches up with code (probability 0.90, [principles/beck/slow-down-until-trust-catches-up-with-code.md](principles/beck/slow-down-until-trust-catches-up-with-code.md))
  - "Slow development to ensure that the damn stuff actually works."
- Kent Beck: Verify what the agent did, not what it claims (probability 0.90, [principles/beck/verify-what-the-agent-did-not-what-it-claims.md](principles/beck/verify-what-the-agent-did-not-what-it-claims.md))
  - "So it looks like we have an implementer and a verifier, which like informally, that's my kind of, that's my kind of division of labor."
- Steve Yegge: Deterministic machinery dispatches work; models act on judgment (probability 0.90, [principles/yegge/deterministic-machinery-dispatches-work-models-act-on-judgment.md](principles/yegge/deterministic-machinery-dispatches-work-models-act-on-judgment.md))
  - "wake an agent when something needs judgment. The rule is: crons watch, models act."
- Anthropic engineering: Agree the plan and testable criteria before agents build (probability 0.90, [principles/anthropic/agree-the-plan-and-testable-criteria-before-agents-build.md](principles/anthropic/agree-the-plan-and-testable-criteria-before-agents-build.md))
  - "When I first joined the Claude Code team, we wrote a pretty good six month roadmap, and then *because* of Claude Code, so many things changed that it was out of date by month three."
- Kent Beck: Make expectations explicit and let the agent observe real behaviour (probability 0.89, [principles/beck/make-expectations-explicit-and-let-the-agent-observe-real-behaviour.md](principles/beck/make-expectations-explicit-and-let-the-agent-observe-real-behaviour.md))
  - "Exactly what she told it. Not at all what she wanted. Anyone working with agents today knows the feeling."
- Mitchell Hashimoto: Turn every agent mistake into a permanent guardrail (probability 0.89, [principles/hashimoto/turn-every-agent-mistake-into-a-permanent-guardrail.md](principles/hashimoto/turn-every-agent-mistake-into-a-permanent-guardrail.md))
  - "It is the idea that anytime you find an agent makes a mistake, you take the time to engineer a solution such that the agent never makes that mistake again."
- Birgitta Böckeler: Choose stacks and architecture for harnessability (probability 0.88, [principles/bockeler/choose-stacks-and-architecture-for-harnessability.md](principles/bockeler/choose-stacks-and-architecture-for-harnessability.md))
  - "But for maintainable, AI-generated code at scale that we can trust, something has to give."
- Birgitta Böckeler: Measure the harness and agent setup with data (probability 0.88, [principles/bockeler/measure-the-harness-and-agent-setup-with-data.md](principles/bockeler/measure-the-harness-and-agent-setup-with-data.md))
  - "So I also did a few runs of my automated setup with reasoning off - and lo and behold, it's not only faster (which was to be expected), but also performed the same to slightly better!"
- Birgitta Böckeler: Verify outcomes instead of prescribing the agent's process (probability 0.88, [principles/bockeler/verify-outcomes-instead-of-prescribing-the-agent-s-process.md](principles/bockeler/verify-outcomes-instead-of-prescribing-the-agent-s-process.md))
  - "Once the agent gets all these instructions and guidance, execution still depends on how well the LLM interprets them!"
- Addy Osmani: Let verification and risk set agent autonomy (probability 0.88, [principles/osmani/let-verification-and-risk-set-agent-autonomy.md](principles/osmani/let-verification-and-risk-set-agent-autonomy.md))
  - "You can use the `--dangerously-skip-permissions` flag only in trusted local projects where you want to bypass manual tool approval prompts."
- Lauren Tan: Give agents a drivable interface and feature map of the system (probability 0.88, [principles/tan/give-agents-a-drivable-interface-and-feature-map-of-the-system.md](principles/tan/give-agents-a-drivable-interface-and-feature-map-of-the-system.md))
  - "The verification skill she describes generates a command line interface (CLI) and a feature map for the application."
- DORA: Trust but verify AI output (probability 0.87, [principles/dora/trust-but-verify-ai-output.md](principles/dora/trust-but-verify-ai-output.md))
  - "Of course, faster code reviews and approvals do not equate to better and more thorough code review processes and approval processes."
- Charity Majors: Earn agent autonomy over merging with guardrails and evidence (probability 0.87, [principles/majors/earn-agent-autonomy-over-merging-with-guardrails-and-evidence.md](principles/majors/earn-agent-autonomy-over-merging-with-guardrails-and-evidence.md))
  - "Yes, it may be absolutely unthinkable to start auto-accepting diffs given the current state of your codebase and guardrails."
- OpenAI engineering: Enforce architecture and taste mechanically and continuously (probability 0.87, [principles/openai/enforce-architecture-and-taste-mechanically-and-continuously.md](principles/openai/enforce-architecture-and-taste-mechanically-and-continuously.md))
  - "This is the kind of architecture you usually postpone until you have hundreds of engineers. With coding agents, it’s an early prerequisite: the constraints are what allows speed without decay or architectural drift."
- Andrej Karpathy: Stay responsible for agent-written software (probability 0.86, [principles/karpathy/stay-responsible-for-agent-written-software.md](principles/karpathy/stay-responsible-for-agent-written-software.md))
  - "Agentic engineering is about preserving the quality bar of professional software. You are not allowed to introduce vulnerabilities because of vibe coding. You are still responsible for your software, just as before."
- Unmesh Joshi: Constrained DSLs with validators let agents self-correct (probability 0.86, [principles/joshi/constrained-dsls-with-validators-let-agents-self-correct.md](principles/joshi/constrained-dsls-with-validators-let-agents-self-correct.md))
  - "The agent can generate a candidate, run it past the validator, and repair it from the error, all without a human in the loop."
- Addy Osmani: Humans own the outer loop: intent, judgment and the ship decision (probability 0.86, [principles/osmani/humans-own-the-outer-loop-intent-judgment-and-the-ship-decision.md](principles/osmani/humans-own-the-outer-loop-intent-judgment-and-the-ship-decision.md))
  - "If you put a human check into a system that otherwise moves at machine speed, don’t be surprised if that impacts productivity."
- Simon Willison: Agents must run their work and show evidence it works (probability 0.86, [principles/willison/agents-must-run-their-work-and-show-evidence-it-works.md](principles/willison/agents-must-run-their-work-and-show-evidence-it-works.md))
  - "allowing them to test that code and iterate on it independently of turn-by-turn guidance from their human supervisor."
- Simon Willison: Delegate tedious, well-bounded and trial-and-error work to agents (probability 0.86, [principles/willison/delegate-tedious-well-bounded-and-trial-and-error-work-to-agents.md](principles/willison/delegate-tedious-well-bounded-and-trial-and-error-work-to-agents.md))
  - "That's exactly the kind of tedious work that coding agents excel at!"
- Robert C. Martin: Humans own the behavioural specification (probability 0.86, [principles/unclebob/humans-own-the-behavioural-specification.md](principles/unclebob/humans-own-the-behavioural-specification.md))
  - "If you've got a fairly elaborate system that requires a lot of behavioral specification, it is wise to have humans produce that, and I like Gherkin, the old behavior-driven development language, for it."
- Martin Fowler: Humans own and evaluate what agents build (probability 0.85, [principles/fowler/humans-own-and-evaluate-what-agents-build.md](principles/fowler/humans-own-and-evaluate-what-agents-build.md))
  - "This is a profound change to the nature of programming, where humans oversee LLM agents who generate the code. Humans are still responsible for what the software does and how it works, but use different skills to create their products."
- Steve Yegge: Enforce critical rules mechanically, and curate the fences (probability 0.85, [principles/yegge/enforce-critical-rules-mechanically-and-curate-the-fences.md](principles/yegge/enforce-critical-rules-mechanically-and-curate-the-fences.md))
  - "Now rules go through a lifecycle, tightening each time they're re-violated: first custom, then advisories/warnings, then written law in the constitution that all agents must obey, and finally, mechanical enforcement: programs that refuse by policy, or observe and alert loudly."
- OpenAI engineering: Plan, size and bound each agent run (probability 0.85, [principles/openai/plan-size-and-bound-each-agent-run.md](principles/openai/plan-size-and-bound-each-agent-run.md))
  - "A good loop usually stops for one of four reasons: validation passes, the loop reaches a maximum number of attempts, the remaining delta stops changing, or the next decision needs human review. Those stop conditions are just as important as the repair prompt."
- Andrej Karpathy: Write concrete prompts that state the goal (probability 0.84, [principles/karpathy/write-concrete-prompts-that-state-the-goal.md](principles/karpathy/write-concrete-prompts-that-state-the-goal.md))
  - "if your prompt is vague, then uh the AI might not do exactly what you wanted and in that case, verification will fail."
- Unmesh Joshi: Well-designed code is the primary harness (probability 0.84, [principles/joshi/well-designed-code-is-the-primary-harness.md](principles/joshi/well-designed-code-is-the-primary-harness.md))
  - "Because abstractions form the essential vocabulary for the prompts, the generated program is more predictable and easier to review."
- Simon Willison: Conformance suites make agent-driven ports and rewrites viable (probability 0.84, [principles/willison/conformance-suites-make-agent-driven-ports-and-rewrites-viable.md](principles/willison/conformance-suites-make-agent-driven-ports-and-rewrites-viable.md))
  - "Having an existing conformance testing suite of the quality of `test262` is a huge unlock for projects of this magnitude, and the ability to compare output with an existing trusted implementation makes agentic engineering much more of a safe bet."
- Robert C. Martin: Quality gates buy test strength, not design (probability 0.84, [principles/unclebob/quality-gates-buy-test-strength-not-design.md](principles/unclebob/quality-gates-buy-test-strength-not-design.md))
  - "CRAP buys coverage and spends cleanliness. It does not improve design."
- Lauren Tan: Pick tools and stack for how well agents can verify with them (probability 0.84, [principles/tan/pick-tools-and-stack-for-how-well-agents-can-verify-with-them.md](principles/tan/pick-tools-and-stack-for-how-well-agents-can-verify-with-them.md))
  - "I personally feel that agentic verification is so important that I would unironically suggest building your own rich debugging tools, or even choosing a different tech stack, in order to have unfair advantages and extreme productivity in building software."
- Andrej Karpathy: Map a model's jagged capabilities empirically (probability 0.83, [principles/karpathy/map-a-model-s-jagged-capabilities-empirically.md](principles/karpathy/map-a-model-s-jagged-capabilities-empirically.md))
  - "It is about getting the most out of the tools available, using their features, and investing in your own setup."
- Andrej Karpathy: The human owns the spec, design and taste (probability 0.83, [principles/karpathy/the-human-owns-the-spec-design-and-taste.md](principles/karpathy/the-human-owns-the-spec-design-and-taste.md))
  - "Right now the agents are like interns. You still have to be in charge of aesthetics, judgment, taste, and oversight."
- Steve Yegge: Agents stay in scope and escalate instead of bypassing (probability 0.83, [principles/yegge/agents-stay-in-scope-and-escalate-instead-of-bypassing.md](principles/yegge/agents-stay-in-scope-and-escalate-instead-of-bypassing.md))
  - "A **gate** parks a step until something external happens: a human sign-off, a timer, or a GitHub run or PR"
- Gergely Orosz: Steer agents with classic structure and organisational context (probability 0.82, [principles/orosz/steer-agents-with-classic-structure-and-organisational-context.md](principles/orosz/steer-agents-with-classic-structure-and-organisational-context.md))
  - "But what they found is they built a bunch of internal systems, a lot of it, to help to feed NCD's agent harnesses, and now they're working better."
- Addy Osmani: Keep agent context lean, hand-written and earned (probability 0.82, [principles/osmani/keep-agent-context-lean-hand-written-and-earned.md](principles/osmani/keep-agent-context-lean-hand-written-and-earned.md))
  - "Write the project rules file describing the real conventions, the ones in the code, not the ones in the wiki."
- Simon Willison: Keep secrets out of agents' reach and out of their transcripts (probability 0.82, [principles/willison/keep-secrets-out-of-agents-reach-and-out-of-their-transcripts.md](principles/willison/keep-secrets-out-of-agents-reach-and-out-of-their-transcripts.md))
  - "I'm often paranoid that one of my API keys or similar secrets might inadvertently be revealed in the detailed log files."
- OpenAI engineering: Earn agent autonomy gradually within fixed boundaries (probability 0.82, [principles/openai/earn-agent-autonomy-gradually-within-fixed-boundaries.md](principles/openai/earn-agent-autonomy-gradually-within-fixed-boundaries.md))
  - "Keep approval and sandboxing tight by default, then loosen permissions only for trusted repos or specific workflows once the need is clear."
- Andrej Karpathy: Keep agent changes small so verification stays fast (probability 0.81, [principles/karpathy/keep-agent-changes-small-so-verification-stays-fast.md](principles/karpathy/keep-agent-changes-small-so-verification-stays-fast.md))
  - "we we're now kind of like cooperating with AIS and usually they are doing the generation and we as humans are doing the verification. It is in our interest to make this loop go as fast as possible."
- Thoughtworks: Developer value shifts to thinking, and understanding must keep pace (probability 0.81, [principles/thoughtworks/developer-value-shifts-to-thinking-and-understanding-must-keep-pace.md](principles/thoughtworks/developer-value-shifts-to-thinking-and-understanding-must-keep-pace.md))
  - "In our work we have identified three core skills that they need in order to do their work effectively. These skills reflect where the value of developers is shifting in an AI-assisted world."
- Thoughtworks: Humans on the loop: fix the harness, not the artefact (probability 0.81, [principles/thoughtworks/humans-on-the-loop-fix-the-harness-not-the-artefact.md](principles/thoughtworks/humans-on-the-loop-fix-the-harness-not-the-artefact.md))
  - "The right place for us humans is to build and manage the working loop rather than either leaving the agents to it or micromanaging what they produce. Let’s call this “on the loop.”"
- Thoughtworks: Measure internal quality and rework, not generation speed (probability 0.81, [principles/thoughtworks/measure-internal-quality-and-rework-not-generation-speed.md](principles/thoughtworks/measure-internal-quality-and-rework-not-generation-speed.md))
  - "And it’s even rarer that people assess the quality of the code generated by the agent. I’d argue, though, that internal quality is crucial for development to continue at a sustainable pace over years, rather than collapse under its own weight."
- Steve Yegge: Humans keep judgment, taste and the final say (probability 0.81, [principles/yegge/humans-keep-judgment-taste-and-the-final-say.md](principles/yegge/humans-keep-judgment-taste-and-the-final-say.md))
  - "Wheelhouse was built entirely through a process of clarification. I would ask for something, Fable would ask clarifying questions and collect verdicts, and they would be recorded as law."
- Steve Yegge: Version-controlled, layered agent instructions and workflow templates (probability 0.81, [principles/yegge/version-controlled-layered-agent-instructions-and-workflow-templates.md](principles/yegge/version-controlled-layered-agent-instructions-and-workflow-templates.md))
  - "Commit the instruction files (`AGENTS.md`, `CLAUDE.md`, `GEMINI.md`, as applicable) to git so all team members and AI tools get the same instructions."
- Anthropic engineering: Treat shared agent context as owned, pruned code (probability 0.81, [principles/anthropic/treat-shared-agent-context-as-owned-pruned-code.md](principles/anthropic/treat-shared-agent-context-as-owned-pruned-code.md))
  - "If your prompts carry workarounds such as refusal steering, tool-call retry shims, or "do not be lazy," remove them and re-run your evals before tuning anything else."
- Robert C. Martin: Agents escalate ambiguity to a human operator (probability 0.81, [principles/unclebob/agents-escalate-ambiguity-to-a-human-operator.md](principles/unclebob/agents-escalate-ambiguity-to-a-human-operator.md))
  - "Agents exchange committed work through durable handoffs, while the operator uses a local dashboard to start work, inspect agents, handle approval gates, answer clarifications, and stop the swarm."
- Thoughtworks: Experienced humans own design quality, intent and strategy (probability 0.80, [principles/thoughtworks/experienced-humans-own-design-quality-intent-and-strategy.md](principles/thoughtworks/experienced-humans-own-design-quality-intent-and-strategy.md))
  - "I think this is a clear example where an AI agent left to their own would have changed the codebase for the worse, and it took a developer with experience to notice the issue and to direct the agent to the correct implementation."

### Contradicted by
No contradicting principle found among 222 expert principles yet.

## Proposing a change

Open a pull request on chrucci/expert-brain that edits `house-principles.yaml`.
The home pipeline tests the new wording against the experts, and the next kit shows what supports and contradicts it.
Never edit this file by hand: it is generated.
