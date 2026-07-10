# Inliner.ai agent integration

The official cross-agent skill and plugin for generating, editing, hosting, and managing visual assets with [Inliner.ai](https://inliner.ai).

The package combines an open-standard `inliner-ai` skill with the `@inliner/mcp-server` tools. The skill teaches agents when to use Inliner; MCP generates or edits the actual hosted asset.

## Behavior

- New asset to insert or ship: call `generate_image` and wait for the completed CDN URL.
- Existing asset to change: call `edit_image` with an explicit source.
- URL naming only: call `recommend_image_url`, which does not generate an asset.
- Existing generated URL: reuse it directly.
- Project selection: explicit project, configured default, account default, then first project.
- Project creation: only with explicit user intent.

`generate_image_url` and `create_image` remain deprecated MCP aliases for compatibility.

## Requirements

1. Create an account at [app.inliner.ai](https://app.inliner.ai).
2. Create an API key under **Account > API Keys**.
3. Set `INLINER_API_KEY`. Optionally set `INLINER_DEFAULT_PROJECT`.
4. Ensure Node.js 18 or newer and `npx` are available for the local MCP server.

## Install

### Gemini CLI extension

The extension bundles the skill and MCP configuration:

```bash
gemini extensions install https://github.com/inliner-ai/agent-skill
```

For the skill without bundled MCP configuration:

```bash
gemini skills install https://github.com/inliner-ai/agent-skill --path skills/inliner-ai
```

### Claude Code skill

Copy or link `skills/inliner-ai` to either:

- `.claude/skills/inliner-ai` for one project
- `~/.claude/skills/inliner-ai` for all projects

Configure `.mcp.json` from this repository, or add the server directly:

```bash
claude mcp add --transport stdio inliner -- npx -y @inliner/mcp-server
```

### Codex plugin

Install the versioned plugin, which bundles both the skill and MCP configuration:

```bash
codex plugin marketplace add inliner-ai/agent-skill --ref v1.3.0
codex plugin add inliner-ai@inliner-ai
```

For the skill without bundled MCP configuration:

Copy or link `skills/inliner-ai` to either:

- `.agents/skills/inliner-ai` for one repository
- `~/.agents/skills/inliner-ai` for all repositories

The repository also contains `.agents/plugins/marketplace.json` for Codex marketplace discovery.

### Cursor

Install the separate [Inliner Cursor plugin](https://github.com/inliner-ai/cursor-plugin). Its skill is synchronized from this canonical package.

## Included files

- `skills/inliner-ai/SKILL.md`: canonical activation and workflow guidance
- `skills/inliner-ai/references/`: URL, dimensions, format, and MCP reference
- `.codex-plugin/plugin.json`: Codex plugin manifest
- `.agents/plugins/marketplace.json`: version-pinned Codex marketplace catalog
- `.claude-plugin/plugin.json`: Claude plugin manifest
- `gemini-extension.json`: Gemini extension manifest and secret settings
- `.mcp.json`: shared local MCP configuration
- `evals/evals.json`: positive and negative activation cases

## Validate

```bash
npx -y skills-ref validate skills/inliner-ai
node -e "JSON.parse(require('fs').readFileSync('gemini-extension.json'))"
```

## Links

- [Inliner.ai](https://inliner.ai)
- [Dashboard](https://app.inliner.ai)
- [MCP server](https://github.com/inliner-ai/mcp-server)
- [MCP setup guide](https://inliner.ai/use-case/mcp-server-ai-coding-agents)
- [CLI](https://github.com/inliner-ai/cli)
