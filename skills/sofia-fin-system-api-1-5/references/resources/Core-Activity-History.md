# Core - Activity History

Organization activity history built from core events. Lists who changed tracked resources, when, through which channel, and a sanitized summary of changed fields.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/core/activity-history` | Lists sanitized organization activity history. | [View](../operations/coreFindAllActivityHistory.md) |
| GET | `/core/activity-history/requesters` | Lists distinct users who appear in the organization activity history. | [View](../operations/coreFindAllActivityHistoryRequesters.md) |
