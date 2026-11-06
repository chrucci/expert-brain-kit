# Expert brain work kit

What the leading practitioners and researchers say about building efficient engineering teams of humans and AI agents, as plain Markdown.
It is the finished output of the expert brain that Chris runs at home: the principles, where the experts agree and disagree, what would settle each disagreement, and the scoreboard to measure it.
Use it to build material for the engineering teams: talk outlines, team standards, one-pagers and FAQs.

## Freshness

- Generated on 2026-10-26 from chrucci/expert-brain at commit `f93fb4fa520d`.
- Newest source document quoted: 2026-10-09.
- 219 expert principles from 17 experts, 11 dimension pages, 14 tensions (10 open, 4 leaning, 0 settled), 1 house principle.

A new kit arrives as a pull request on this repository after the weekly refresh at home; read the diff before you merge it.

## Sourcing

- Every input is public: blogs, newsletters, talks, papers and reports by the experts listed below.
No company data went in, and none may be added here.
- Every quote is verbatim.
Code checked each one word for word against a saved copy of its source; no model wrote or repaired a quote.
- Quotes are short and attributed, and each links to its public source.
The full source texts stay at home and are not in this kit.
- Statements, positions and summaries are in our words, written by a model from the verified principles; only the quoted text is the expert's.
- Review anything you take from here before you use it at work.

## What is in it

| Path | What |
|---|---|
| `principles-v0.md` | Principles v0: the thesis, the principles two or more experts back, the open tensions, the scoreboard and the provenance. Start here. |
| `dimensions/` | 11 pages, one per dimension of team design, plus an index. |
| `tensions/` | 14 pages, one per disagreement, plus an index. |
| `principles/` | 219 verified expert principles, one file each, by expert, plus an index. |
| `house-principles.md` | Chris's own principles and the trust thesis. |
| `AGENTS.md` | Instructions for Codex; `CLAUDE.md` points Claude Code at the same file. |

## Using it with an agent

Open this directory in Codex or Claude Code and ask in plain words, for example:

- "Draft a 20-minute talk outline on the trust thesis for the engineering org, with every claim cited."
- "Write a one-page team standard for reviewing agent-written changes."
- "Build an FAQ on how many agents a team should run."

The agent follows `AGENTS.md`: it uses only this kit as evidence, cites the kit file and the public source behind every claim, and quotes exactly.

## Proposing a change

- To change Chris's own principles, open a pull request on chrucci/expert-brain that edits `house-principles.yaml`.
The home pipeline tests the new wording against the experts, and the next kit carries the result.
- To suggest an expert or a source, open an issue on chrucci/expert-brain.
- Never edit the files in this kit by hand: each one is generated, and the next refresh overwrites it.

## Experts

- **Andrej Karpathy** (`karpathy`, 15 principles): Former Tesla AI lead and OpenAI researcher who explains how LLMs work from first principles and framed "software 2.0" and the 2025 shift toward agentic coding.
- **Kent Beck** (`beck`, 21 principles): Creator of Extreme Programming and TDD, now working on "augmented coding" with AI agents, which tests whether test-first and simple design still hold up when an agent writes the code.
- **Martin Fowler** (`fowler`, 6 principles): Long-running writer on software design and refactoring at martinfowler.com, whose 2023-2026 pieces on LLMs and abstraction test what changes in software development with agentic tools.
- **Birgitta Böckeler** (`bockeler`, 12 principles): Thoughtworks engineer whose "Exploring Gen AI" memos and harness and sensor articles give the most concrete practice guidance on controlling coding agents.
- **Unmesh Joshi** (`joshi`, 8 principles): Thoughtworks engineer and frequent Fowler co-author whose articles on the learning loop, what code is, and DSLs argue for constraints that make LLM output reliable.
- **Thoughtworks** (`thoughtworks`, 16 principles): Thoughtworks as a collective, covering the many one-off martinfowler.com authors and the Technology Radar, which records how the firm's teams adopt and drop AI-assisted delivery practices.
- **METR** (`metr`, 7 principles): Independent evaluator whose July 2025 randomized controlled trial found experienced open-source developers were slower with early-2025 AI tools, a counterweight every tension needs with its scope stated.
- **DORA** (`dora`, 9 principles): Google Cloud's DevOps Research and Assessment program, whose yearly reports and four-key metrics are the empirical baseline for whether AI-assisted development changes delivery outcomes.
- **Mitchell Hashimoto** (`hashimoto`, 7 principles): HashiCorp co-founder (Vagrant, Terraform) who now runs the Ghostty terminal project and writes first-hand accounts of adopting coding agents on a real codebase, plus the AI contribution rules his open source team enforces.
- **Charity Majors** (`majors`, 16 principles): Honeycomb co-founder and CTO whose 2025-2026 writing argues that AI demands more engineering discipline, not less - production ownership, observability and fast feedback loops as the guardrails for teams shipping agent-written code.
- **Gergely Orosz** (`orosz`, 13 principles): Author of The Pragmatic Engineer, whose industry surveys and interviews with the builders of Claude Code, Codex and in-house agents report how real engineering teams adopt AI tools and how roles, team size and code review change as a result.
- **Addy Osmani** (`osmani`, 14 principles): Long-time Google engineering leader (Chrome, then Google Cloud AI) and author of "Beyond Vibe Coding" whose 2025-2026 writing on the 70% and 80% problems, specs, loop engineering, agent orchestration and agentic code review maps directly onto how human-agent teams should split work and verify it.
- **Steve Yegge** (`yegge`, 19 principles): Ex-Amazon and Google engineer, co-author of "Vibe Coding" with Gene Kim and builder of the Gas Town agent orchestrator and Beads, who writes first-hand about running fleets of 50+ coding agents, the changing role of human engineers, and the guardrails agent teams need.
- **Simon Willison** (`willison`, 18 principles): Django co-creator and coiner of "prompt injection" who documents agentic coding practice almost daily and is writing the "Agentic Engineering Patterns" guide (tests first, subagents, git with agents, anti-patterns).
- **Anthropic engineering** (`anthropic`, 14 principles): Anthropic's own teams writing first-hand about how they build with Claude Code and agents, covering harnesses, context engineering, tool design, skills, verification loops and how engineering roles change.
- **OpenAI engineering** (`openai`, 12 principles): OpenAI's own teams writing about how they build software with Codex agents, including the harness-engineering account of a seven-engineer team shipping a million-line product with agent-written code, per-worktree observability and mechanically enforced architecture.
- **Robert C. Martin** (`unclebob`, 12 principles): Author of Clean Code and Agile Manifesto signatory who in 2026 moved to agent-only coding, replacing human code reading with deterministic constraints (TDD, Gherkin acceptance tests, CRAP scores, mutation testing) and published SwarmForge, a multi-agent role pipeline, plus controlled experiments on those disciplines.

## Licence

Chris's own text is CC BY 4.0 (see `LICENSE` and `NOTICE.md`): reuse and adapt it with credit.
Quoted passages stay with their authors and are cited inline.
