# Gregale plugin for Claude Code

Deploy, diagnose and roll back Gregale apps from Claude Code. The plugin adds:

- Gregale's hosted MCP server (`https://api.gregale.dev/mcp`) via
  [`.mcp.json`](./.mcp.json). When Claude Code connects, authorize via OAuth in
  your browser, choose what the agent may do and which apps it may use;
- the `deploy` skill, which deploys the current project, verifies an application
  response and rolls back a broken release with your approval;
- the `diagnose` skill, which finds why an app is failing or slow from health,
  error groups, logs, and request timelines;
- `CLAUDE.md` with the safe operational defaults both skills follow.

## Install in Claude Code

```sh
/plugin marketplace add gregale-dev/gregale-claude-code-plugin
/plugin install gregale@gregale-dev
```

Or connect just the hosted MCP server directly:

```sh
claude mcp add --transport http gregale https://api.gregale.dev/mcp
```

The skills can also deploy with the `gregale` CLI; install it and log in (or set
`GREGALE_TOKEN`): https://gregale.dev/docs/install

## Links

- [Gregale agent guide](https://gregale.dev/docs/agents)
- [CLI & MCP setup](https://gregale.dev/docs/cli)
- [llms.txt](https://gregale.dev/llms.txt)

## License

Apache-2.0 — see [LICENSE](./LICENSE).
