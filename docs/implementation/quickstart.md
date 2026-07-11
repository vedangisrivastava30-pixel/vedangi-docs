# Quickstart

Get your first report from the Reports API in under five minutes. *(Sample documentation
written to demonstrate developer-facing, docs-as-code technical writing.)*

## Prerequisites

- An API key (Settings → API Keys)
- A terminal with `curl`, or Postman

## 1. Authenticate

All requests use a bearer token in the `Authorization` header:

```bash
curl https://api.example.com/v1/reports \
  -H "Authorization: Bearer YOUR_API_KEY"
```

## 2. Request a report

```bash
curl -X POST https://api.example.com/v1/reports \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{ "metric": "impressions", "start_date": "2026-01-01", "end_date": "2026-01-31" }'
```

## 3. Read the response

```json
{
  "report_id": "rep_12345",
  "status": "complete",
  "metric": "impressions",
  "total": 1840233
}
```

!!! tip "REST vs GraphQL"
    This endpoint is REST: one URL per resource, fixed response shape. The same data is also
    available via our GraphQL endpoint, where you request exactly the fields you need in a
    single query. Choose REST for simple, cacheable reads; choose GraphQL to avoid
    over-fetching across related resources.
