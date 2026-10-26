# Keep agent context lean and re-inject it automatically

Verified: 8 verbatim quotes from 12 sources

Dimension: Techniques (techniques)

Evidence: experience

How to measure: Compare tokens injected per session, cost and task success, and how often agents lose track of the workflow after compaction, between MCP or full-file setups and CLI-plus-hook priming.

Connect agents to tools through a CLI plus a short priming hook rather than MCP schemas wherever a shell exists, because schemas can cost tens of thousands of tokens and dilute attention. Use deterministic harness hooks to reload a compact workflow primer at session start and after compaction. Hand off to a fresh session before the context window degrades, so nobody has to remember to reload context.

## Quotes

> Hook-enabled agents use the `minimal` profile because `bd prime` injects full context at session start.
>
> [beads: docs/getting-started/ide-setup.md](https://github.com/gastownhall/beads/blob/main/docs/getting-started/ide-setup.md)

> MCP tool schemas can add 10-50k tokens to every request; `bd prime` adds ~1-2k tokens of workflow context - 10-50x less overhead, which means lower cost, lower latency, and better model attention.
>
> [beads: docs/integrations/claude-code.md](https://github.com/gastownhall/beads/blob/main/docs/integrations/claude-code.md)

> The plugin does not bundle an MCP server — it works through the bd CLI,
> which Claude Code drives directly (lower token overhead than MCP tool
> schemas).
>
> [beads: docs/integrations/claude-code-plugin.md](https://github.com/gastownhall/beads/blob/main/docs/integrations/claude-code-plugin.md)

> Beads uses that lifecycle to inject `bd prime` on session start and recover context after compaction.
>
> [beads: docs/integrations/codex.md](https://github.com/gastownhall/beads/blob/main/docs/integrations/codex.md)

> **Context efficiency still matters**, even with large context windows:
>
> [beads: docs/integrations/copilot-cli.md](https://github.com/gastownhall/beads/blob/main/docs/integrations/copilot-cli.md)

> Cursor agent hooks that load `bd prime` on session
> start and recover it after a context compaction.
>
> [beads: docs/integrations/cursor.md](https://github.com/gastownhall/beads/blob/main/docs/integrations/cursor.md)

> Both work against the same database - use MCP for conversational work, the CLI for quick commands.
>
> [beads: docs/integrations/github-copilot.md](https://github.com/gastownhall/beads/blob/main/docs/integrations/github-copilot.md)

> **Prefer CLI + hooks** when shell is available - it's more context efficient.
>
> [beads: docs/integrations/mcp-server.md](https://github.com/gastownhall/beads/blob/main/docs/integrations/mcp-server.md)

## Support

Established: 12 independent sources support this principle.

Expert: Steve Yegge

Topics: techniques, tools

## Related principles

- [Steve Yegge: Version-controlled, layered agent instructions and workflow templates](version-controlled-layered-agent-instructions-and-workflow-templates.md)
- [Steve Yegge: Keep agent work state in a durable work graph, not the session](keep-agent-work-state-in-a-durable-work-graph-not-the-session.md)
