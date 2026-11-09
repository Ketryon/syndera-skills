# The same steps on MCP, the CLI and the REST API

SKILL.md names the MCP tools. On the `syndera` CLI or the REST API (`https://api.syndera.app/v1`, `Authorization: Bearer <key>`, an `Idempotency-Key` on every write; reference at https://api.syndera.app), these are the equivalents.

| Step | MCP tool | CLI | REST |
|---|---|---|---|
| Read a brand | `get_brand` | `syndera brands show <id>` | `GET /brands/{id}` |
| Its channels | `list_channels` | `syndera channels ls --brand <id>` | `GET /channels?brandId=<id>` |
| The calendar | `list_posts` (status `scheduled`, from/to) | `syndera posts ls --brand <id> --status scheduled --from <iso> --to <iso>` | `GET /posts?brandId=<id>&status=scheduled&from=…&to=…` |
| Published posts and results | `list_posts` (status `published`) | `syndera posts ls --brand <id> --status published --json` | `GET /posts?brandId=<id>&status=published` |
| Drafts | `list_posts` (status `draft`) | `syndera posts ls --brand <id> --status draft` | `GET /posts?brandId=<id>&status=draft` |
| Renders left | `get_plan` | `syndera plan` | `GET /billing` |
| Ads access on X / TikTok | `x_boost_state` / `tiktok_boost_state` | `syndera boost x <post>` / `syndera boost tiktok <post>` | `GET /posts/{id}/boost/x` / `…/tiktok` |
| X reach estimate | `x_estimate` | (not in the CLI) | `POST /posts/{id}/boost/x/estimate` |
| A boost's results | `x_boost_stats` / `tiktok_boost_stats` | `syndera boost x <post> stats` | `GET /posts/{id}/boost/x/stats` / `…/tiktok/stats` |
| Pause or stop a boost | `pause_boost` / `stop_boost` | `syndera boost pause <post>` / `stop` | `POST /posts/{id}/boost/pause` / `stop` |

Starting a boost (`start_x_boost`, `start_tiktok_boost`, `syndera boost x <post> --account … --goal … --budget … --days …`, `POST /posts/{id}/boost/x`) spends money: ask first, every time.
