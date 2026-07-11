# Reports API Reference

*(Sample API reference demonstrating structured, developer-facing documentation.)*

## `GET /v1/reports/{report_id}`

Retrieve a single report by ID.

### Authentication

Bearer token in the `Authorization` header.

### Path parameters

| Parameter | Type | Required | Description |
| --- | --- | --- | --- |
| `report_id` | string | Yes | The unique identifier of the report, e.g. `rep_12345`. |

### Query parameters

| Parameter | Type | Required | Description |
| --- | --- | --- | --- |
| `format` | string | No | Response format: `json` (default) or `csv`. |

### Example request

```bash
curl https://api.example.com/v1/reports/rep_12345 \
  -H "Authorization: Bearer YOUR_API_KEY"
```

### Example response

```json
{
  "report_id": "rep_12345",
  "status": "complete",
  "metric": "impressions",
  "start_date": "2026-01-01",
  "end_date": "2026-01-31",
  "total": 1840233
}
```

### Response fields

| Field | Type | Description |
| --- | --- | --- |
| `report_id` | string | Unique identifier of the report. |
| `status` | string | `pending`, `processing`, or `complete`. |
| `total` | integer | Aggregated value for the requested metric. |

### Status codes

| Code | Meaning |
| --- | --- |
| `200` | Success. |
| `401` | Missing or invalid API key. |
| `404` | Report not found. |
