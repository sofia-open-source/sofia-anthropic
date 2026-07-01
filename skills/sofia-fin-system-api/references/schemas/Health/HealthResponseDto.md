# HealthResponseDto

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `status` | string | Yes |  |
| `version` | string | Yes | Monorepo root package.json version. |
| `commitSha` | string | Yes | Git commit SHA from COMMIT_SHA when set at deploy. |
| `gitBranch` | string | Yes | Git branch from GIT_BRANCH or BRANCH_NAME when set at deploy. |
| `env` | string | Yes | Application environment (e.g. local, dev, preview, prod). |

