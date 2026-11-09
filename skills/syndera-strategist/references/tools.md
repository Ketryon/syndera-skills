# The same steps on MCP, the CLI and the REST API

SKILL.md names the MCP tools. On the `syndera` CLI or the REST API (`https://api.syndera.app/v1`, `Authorization: Bearer <key>`, an `Idempotency-Key` on every write; reference at https://api.syndera.app), these are the equivalents.

| Step | MCP tool | CLI | REST |
|---|---|---|---|
| Read a brand and its competitors | `get_brand` | `syndera brands show <id>` | `GET /brands/{id}` |
| Set its competitors (with a yes) | `update_brand` (`competitors`) | `syndera brands edit <id> --competitor "Acme acme.com" …` | `PATCH /brands/{id}` with `competitors` |
| Read the Intel brief | `get_intel` | `syndera intel <brand>` | `GET /brands/{id}/intel` |
| Run research (with a yes) | `start_research` | `syndera intel <brand> run [--focus "…"]` | `POST /brands/{id}/research` |
| A run's progress | `get_research` | (the CLI waits and shows it) | `GET /research/{id}` |
| Research runs left | `get_plan` | `syndera plan` | `GET /billing` (`researchIncluded`, `researchUsed`, `researchRate`) |
| Drafts | `list_posts` (status `draft`) | `syndera posts ls --brand <id> --status draft` | `GET /posts?brandId=<id>&status=draft` |
| A post's latest audit | `get_audit` | `syndera posts audit <id> --last` | `GET /posts/{id}/audit` |
| Audit a post (one AI call) | `audit_post` | `syndera posts audit <id>` | `POST /posts/{id}/audit` |
| Dismiss a finding | `dismiss_finding` | `syndera posts audit <id> --dismiss f1` | `PATCH /posts/{id}/audit/findings/{findingId}` with `{"dismissed": true}` |
| Edit a post (with a yes) | `update_post` | `syndera posts edit <id> --caption "…"` | `PATCH /posts/{id}` |

Add `--json` to any CLI command for the full answer, including every source URL.
