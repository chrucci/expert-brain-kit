# Keep agent work state in a durable work graph, not the session

Verified: 8 verbatim quotes from 16 sources

Dimension: Techniques (techniques)

Evidence: experience

How to measure: Count tasks that are redone, dropped or re-planned after an agent crash, restart, compaction or handoff, before and after work state moves into a persistent issue graph.

Agents lose their context when a session ends, crashes or compacts, so markdown plans, TODOs and chat history are unreliable places to keep track of work. Record every unit of work, every handoff and all newly discovered work as version-controlled, linked items in a persistent graph, kept apart from the agent's identity and sandbox. Then any fresh session can pick up exactly where the last one stopped.

## Quotes

> Coding agents lose their memory every time a session ends. Markdown plans rot,
> TODO comments scatter, and a crashed agent takes its context with it.
>
> [beads: docs/core-concepts/index.md](https://github.com/gastownhall/beads/blob/main/docs/core-concepts/index.md)

> Traditional issue trackers (Jira, GitHub Issues) weren't designed for AI agents.
>
> [beads: docs/index.md](https://github.com/gastownhall/beads/blob/main/docs/index.md)

> `.aider/BEADS.md` holds the workflow rules the AI follows: track all work in bd (never markdown TODOs), suggest `bd ready` to find work, suggest `bd create` for new issues, suggest `bd dolt push` at end of session — and always *suggest* commands for you to run via `/run`.
>
> [beads: docs/integrations/aider.md](https://github.com/gastownhall/beads/blob/main/docs/integrations/aider.md)

> Beads (`bd`) is an issue tracker designed specifically for AI-supervised coding workflows. It helps AI agents and developers:
>
> [beads: docs/integrations/claude-code-plugin.md](https://github.com/gastownhall/beads/blob/main/docs/integrations/claude-code-plugin.md)

> Beads gives Copilot a persistent, structured memory for tracking work: with the MCP server configured, you create, update, and track issues in natural language without leaving the editor.
>
> [beads: docs/integrations/github-copilot.md](https://github.com/gastownhall/beads/blob/main/docs/integrations/github-copilot.md)

> Document handoffs** - Use comments to explain context
>
> [beads: docs/multi-agent/coordination.md](https://github.com/gastownhall/beads/blob/main/docs/multi-agent/coordination.md)

> What you want is to plan freely *about* the project without planning *in* the project.
>
> [beads: docs/multi-agent/routing.md](https://github.com/gastownhall/beads/blob/main/docs/multi-agent/routing.md)

> GitHub Issues plus the `gh` CLI can approximate some features, but hosted trackers fundamentally cannot replicate what AI agents need:
>
> [beads: docs/reference/faq.md](https://github.com/gastownhall/beads/blob/main/docs/reference/faq.md)

## Support

Established: 16 independent sources support this principle.

Expert: Steve Yegge

Topics: agent-roles, techniques, tools

## Related principles

- [Steve Yegge: Deterministic machinery dispatches work; models act on judgment](deterministic-machinery-dispatches-work-models-act-on-judgment.md)
- [Steve Yegge: Keep agent context lean and re-inject it automatically](keep-agent-context-lean-and-re-inject-it-automatically.md)
