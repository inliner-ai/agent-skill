# @inliner/agent-skill

**The Official Agent Skill for [Inliner.ai](https://inliner.ai)**

Generate, edit, and manage AI images directly within your development workflow. This skill empowers AI coding assistants (like Gemini CLI, Cursor, and Claude Code) to handle visual assets as naturally as they handle code.

[![Inliner Website](https://img.shields.io/badge/website-inliner.ai-blue)](https://inliner.ai)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)

## Why Inliner.ai?

Inliner.ai is the simplest way to generate and serve images for modern web applications.

- **URL-Native Architecture**: Generate images by simply defining a URL path. No complex SDKs or API integrations required—if you can write an `<img>` tag, you can use Inliner.
- **Built for AI Workflows**: Designed specifically for developers using AI coding assistants. This skill bridges the gap between your code and visual assets.
- **Global Edge Performance**: Every image is served via a global CDN with 320+ edge locations, ensuring fast delivery and permanent caching.
- **Professional Results at Scale**: Perfect for landing pages, SaaS dashboards, blog headers, and marketing materials at 90%+ savings compared to stock photography.
- **Multi-Model Intelligence**: Leverages the best AI models (GPT-4o, Gemini, Flux, Imagen) to deliver the right aesthetic for every request.

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

- **[Official Website](https://inliner.ai)**
- [Web Application (Dashboard)](https://app.inliner.ai)
- [Documentation & Tutorials](https://inliner.ai/tutorial)
- [Inliner MCP Server](https://github.com/inliner-ai/agent-skill)
- [Inliner CLI](https://github.com/inliner-ai/cli)
