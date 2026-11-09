# Syndera for your assistant

The Syndera plugin: Syndera's MCP server (your brands, posts, checks and results) and one skill, `syndera-writer`, that tells an assistant how to write posts with them.

The skill brings a way of working, not a style. Your assistant does the writing with its own judgement; the skill tells it what outranks what (the post's checks, then the brand's never-rules, then your request, then the brand's own posts), to read the brand before writing, to save drafts and fix failing checks, and never to schedule, publish, render or boost without your yes. Voice, angle and format come from the brand and from you.

## Add it

| Where | How |
|---|---|
| Claude (web, desktop) | Customize → Plugins → Add marketplace → `Ketryon/syndera-skills`, then install **syndera**. |
| Claude Code | `/plugin marketplace add Ketryon/syndera-skills`, then `/plugin install syndera@syndera` |
| Codex, Cursor and other agents that read skills | `npx skills add Ketryon/syndera-skills`, and add `https://api.syndera.app/mcp` as an MCP server |
| The Syndera CLI | `syndera skill install` (into `~/.claude/skills`; `--dir` for another agent's skills folder) |
| Your own agent on the REST API | `GET https://api.syndera.app/v1/skill` returns the skill's files; put them in your agent's context |
| Assistants that can't install skills | Nothing to do: Syndera's MCP server serves the same files as resources and as a `write` prompt |

You sign in with Syndera the first time the assistant uses it. More: https://syndera.app/support/give-your-assistant-the-writer-skill

## What's here

```
.claude-plugin/plugin.json        the plugin
.claude-plugin/marketplace.json   so this repo can be added as a marketplace
.mcp.json                         Syndera's MCP server
skills/syndera-writer/            the skill: SKILL.md and three references
evals/syndera-writer/             how the skill is tested (not installed)
```

This repo is published from `plugin/` in Syndera's own repository; changes are made there.

MIT licensed.
