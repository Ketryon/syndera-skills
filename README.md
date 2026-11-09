# Syndera for your assistant

One plugin: Syndera's MCP server (your brands, posts, checks and results) plus one skill, `syndera-writer`, that tells an assistant how to write posts with them. The skill brings a way of working, not a style: voice, angle and format come from the brand and from you.

## Install

- **Claude** (web, desktop, Claude Code): Customize → Plugins → Add marketplace → this repo. Or `/plugin marketplace add <this repo>` then `/plugin install syndera` in Claude Code.
- **Any agent that reads skills** (Codex, Cursor and others): `npx skills add <this repo>`, and add `https://api.syndera.app/mcp` as an MCP server.
- **Just the skill:** copy `skills/syndera-writer/` into your agent's skills folder.

You sign in with Syndera the first time the assistant uses it.

## What's here

```
.claude-plugin/plugin.json   the plugin
.mcp.json                    Syndera's MCP server
skills/syndera-writer/       the skill: SKILL.md and three references
evals/syndera-writer/        how the skill is tested (not installed)
```

MIT licensed.
