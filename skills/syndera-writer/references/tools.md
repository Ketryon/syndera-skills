# The same steps on MCP, the CLI and the REST API

SKILL.md names the MCP tools. If you're working through the `syndera` CLI or the REST API instead, these are the equivalents. The REST API lives at `https://api.syndera.app/v1`; send `Authorization: Bearer <key>` and an `Idempotency-Key` header on every write. The full reference is at https://api.syndera.app.

| Step | MCP tool | CLI | REST |
|---|---|---|---|
| List brands | `list_brands` | `syndera brands ls` | `GET /brands` |
| Read a brand | `get_brand` | `syndera brands show <id>` | `GET /brands/{id}` |
| A brand's channels | `list_channels` | `syndera channels ls --brand <id>` | `GET /channels?brandId=<id>` |
| Published posts (with results) | `list_posts` (status `published`) | `syndera posts ls --brand <id> --status published --json` | `GET /posts?brandId=<id>&status=published` |
| One post | `get_post` | `syndera posts show <id> --json` | `GET /posts/{id}` |
| Create a draft | `create_post` | `syndera posts create --brand <id> --title "…" --caption "…" [--channel <id> …]` | `POST /posts` |
| Edit a draft | `update_post` | `syndera posts edit <id> --caption "…"` | `PATCH /posts/{id}` |
| What TikTok allows for an account | `get_tiktok_creator` | `syndera channels tiktok <id>` | `GET /channels/{id}/tiktok-creator` |
| The media library | `list_media` | `syndera media ls --brand <id>` | `GET /media?brandId=<id>` |
| Alt text on an image | `update_media` | `syndera media edit <id> --alt "…"` | `PATCH /media/{id}` |

The CLI's `posts create --caption` sets the same caption on every channel; to give each network its own caption, send all the variants at once with `syndera api PATCH /posts/<id> --data '{"variants":[…]}'` (the same body as `PATCH /posts/{id}`; it replaces every variant).

Anything that needs the person's yes (schedule, publish, render, boost, delete) has CLI and REST equivalents too (`syndera posts schedule`, `POST /posts/{id}/schedule`, …). The rule in SKILL.md applies the same way: ask first.
