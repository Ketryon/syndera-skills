# Syndera for your assistant

The Syndera plugin: Syndera's MCP server (your brands, posts, checks and results) and three skills that tell an assistant how to work with them:

- **`syndera-writer`** writes, rewrites and fixes posts: it reads the brand, studies its published posts, saves drafts and fixes failing checks.
- **`syndera-lead`** plans what to post, reviews how posts did and weighs boosts: from the brand's own results and your goals, saying how sure it is.
- **`syndera-strategist`** sits above both: it researches the brand's market and competitors (Syndera's Intel research, every claim sourced), decides what the brand can own that they can't, hands the angles to the lead and writer, and audits drafts against the market before they go out.

All three bring a way of working, not a style or a playbook. Your assistant uses its own judgement; the skills tell it what outranks what, how to read the evidence, and never to schedule, publish, render, boost or spend without your yes.

## Add it

| Where | How |
|---|---|
| Claude (web, desktop) | Customize → Plugins → Add marketplace → `Ketryon/syndera-skills`, then install **syndera**. |
| Claude Code | `/plugin marketplace add Ketryon/syndera-skills`, then `/plugin install syndera@syndera` |
| Codex, Cursor and other agents that read skills | `npx skills add Ketryon/syndera-skills`, and add `https://api.syndera.app/mcp` as an MCP server |
| The Syndera CLI | `syndera skill install` puts all three into `~/.claude/skills` (`--dir` for another agent's skills folder) |
| Your own agent on the REST API | `GET https://api.syndera.app/v1/skills` returns the skills' files; put them in your agent's context |
| Assistants that can't install skills | Nothing to do: Syndera's MCP server serves the same files as resources, and the `write`, `plan`, `strategy` and `audit` prompts start from them |

You sign in with Syndera the first time the assistant uses it. More: https://syndera.app/support/give-your-assistant-syndera-skills

## What's here

```
.claude-plugin/plugin.json        the plugin
.claude-plugin/marketplace.json   so this repo can be added as a marketplace
.mcp.json                         Syndera's MCP server
skills/syndera-writer/            writing posts: SKILL.md and three references
skills/syndera-lead/              planning, reviews and boosts: SKILL.md and three references
skills/syndera-strategist/        research, positioning and audits: SKILL.md and two references
evals/                            how each skill is tested (not installed)
```

This repo is published from `plugin/` in Syndera's own repository; changes are made there.

MIT licensed.
