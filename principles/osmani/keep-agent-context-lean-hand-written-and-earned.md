# Keep agent context lean, hand-written and earned

Verified: 8 verbatim quotes from 10 sources

Dimension: Techniques (techniques)

Evidence: measurement

How to measure: Run the same tasks with the current context file, a trimmed hand-written one and none, and compare task success, token cost and how accurately skills trigger.

Context files should hold only what the agent cannot find in the code: real conventions, intent, check commands and landmines. Humans write them, not /init or an agent, and they are kept current. Generated or bloated files lower success and raise cost. Keep always-on rules to a few essentials and load longer workflows as skills on demand, using descriptions that say what each skill does and when to use it.

## Quotes

> Write the project rules file describing the real conventions, the ones in the code, not the ones in the wiki.
>
> [agent-skills: docs/adoption-guide.md](https://github.com/addyosmani/agent-skills/blob/main/docs/adoption-guide.md)

> Do not also paste `using-agent-skills/SKILL.md` into `AGENTS.md`, a system prompt, or other always-on context: that stacks the pack's meta-router on Codex's native router and adds unnecessary routing work.
>
> [agent-skills: docs/codex-setup.md](https://github.com/addyosmani/agent-skills/blob/main/docs/codex-setup.md)

> **Do not** copy entire `SKILL.md` bodies into rules; that duplicates `.cursor/skills/` and wastes context.
>
> [agent-skills: docs/cursor-setup.md](https://github.com/addyosmani/agent-skills/blob/main/docs/cursor-setup.md)

> Skills are on-demand expertise that activate only when relevant, keeping your context window clean.
>
> [agent-skills: docs/gemini-cli-setup.md](https://github.com/addyosmani/agent-skills/blob/main/docs/gemini-cli-setup.md)

> Skills load on demand: only the skill name and description sit in context at startup. The full `SKILL.md` loads only when an agent decides the skill is relevant.
>
> [agent-skills: docs/skill-anatomy.md](https://github.com/addyosmani/agent-skills/blob/main/docs/skill-anatomy.md)

> Keep `.windsurfrules` focused on 2-3 essential skills to stay within context limits:
>
> [agent-skills: docs/windsurf-setup.md](https://github.com/addyosmani/agent-skills/blob/main/docs/windsurf-setup.md)

> The practical filter is simple: can the agent discover this on its own by reading your code? If yes, delete it. Every line should represent information that isn’t already in the repo.
>
> [Stop Using /init for AGENTS.md | AddyOsmani.com](https://addyosmani.com/blog/agents-md/)

> Across 288 runs on 17 real tasks, they didn’t make a clear difference to correctness.
>
> [Audit your Agent files](https://addyosmani.com/blog/audit-your-agent-files/)

## Support

Established: 10 independent sources support this principle.

Expert: Addy Osmani

Topics: metrics, techniques, tools

## Related principles

- [Addy Osmani: Encode team process as shared, tested skill workflows](encode-team-process-as-shared-tested-skill-workflows.md)
- [Addy Osmani: Grow the harness from real failures and prune it](grow-the-harness-from-real-failures-and-prune-it.md)
