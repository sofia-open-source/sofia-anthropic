# GET /core/activity-history

**Resource:** [Core - Activity History](../resources/Core-Activity-History.md)
**Lists sanitized organization activity history.**
**Operation ID:** `coreFindAllActivityHistory`

## Parameters

| Name | In | Type | Required | Description |
|------|------|------|----------|-------------|
| `pageIndex` | query | number | No |  |
| `pageSize` | query | number | No |  |
| `requesterUserId` | query | string | No | Identifier of the user who performed the action. |
| `fromDate` | query | any | No | Minimum activity creation date. |
| `toDate` | query | any | No | Maximum activity creation date. |
| `action` | query | string[] | No | Activity actions to filter by. |
| `channel` | query | string[] | No | Activity channels to filter by. |
| `resource` | query | string[] | No | Activity resources to filter by. |

## Responses

| Status | Description |
|--------|-------------|
| 200 |  |
| default |  |

**Success Response Schema:**

[ActivityHistoryPageResponseDto](../schemas/Activity/ActivityHistoryPageResponseDto.md)

