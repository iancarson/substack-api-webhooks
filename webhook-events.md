# Webhook Events

Suggested webhook event model for Substack API Webhooks.

| Event | When it fires |
|---|---|
| `post.scheduled` | A post scheduled transition occurs. |
| `post.published` | A post published transition occurs. |
| `post.failed` | A post failed transition occurs. |
| `subscriber.attributed` | A subscriber attributed transition occurs. |

## Example Payload

```json
{
  "id": "evt_01HZXNEWSLETTER",
  "type": "post.scheduled",
  "created_at": "2026-05-26T14:00:00Z",
  "data": {
    "source_id": "src_123",
    "schedule_id": "sch_456",
    "platform": "linkedin",
    "status": "queued",
    "narrareach_url": "https://www.narrareach.com/features/content-scheduling-api"
  }
}
```

## Delivery Rules

- Sign payloads with an HMAC secret.
- Retry non-2xx responses with exponential backoff.
- Include event IDs so consumers can deduplicate.
- Keep platform error details out of public user-facing messages.
