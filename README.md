# @inliner/agent-skill

The official Agent Skill for [Inliner.ai](https://inliner.ai). This skill empowers AI coding agents (like Gemini CLI, Cursor, and Claude Code) to generate, edit, and manage AI images directly within your development workflow.

## Features

- **Zero-Config URLs**: Generate images by simply constructing a URL.
- **Smart Slugging**: Automatic SEO-friendly URL optimization.
- **AI Editing**: Modify existing images with natural language instructions.
- **MCP Integration**: Deep integration with the Inliner MCP server for advanced project management.
- **Built-in Reference**: Expert guidance on image dimensions and styles.

## Installation

### Gemini CLI
```bash
gemini skills install https://github.com/inliner-ai/agent-skill
```

### Claude Code
```bash
claude skill install @inliner/agent-skill
```

### Cursor
Add to `.cursor/skills/inliner-images/SKILL.md` or install via the upcoming gallery.

## Usage

Once enabled, your AI agent can handle requests like:

- *"Add a photorealistic hero image of a modern office to the landing page"*
- *"Generate a 400x400 profile avatar for the user card"*
- *"Edit the hero image to make the background blue"*
- *"List my Inliner projects"*

## What's Included

- `SKILL.md`: The core instruction set for the AI agent.
- `references/dimensions.md`: A detailed guide on recommended image sizes for various UI components.
- `gemini-extension.json`: Manifest for Gemini CLI discovery.

## Links

- [Inliner.ai Dashboard](https://inliner.ai)
- [Documentation & Tutorials](https://inliner.ai/tutorial)
- [Inliner MCP Server](https://github.com/inliner-ai/inliner/tree/master/packages/mcp-server)
