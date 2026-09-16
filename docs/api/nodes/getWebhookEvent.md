### getWebhookEvent

Read a webhook event (GET /air/webhooks/events/{id}, 200).

**Adapter:** `getWebhookEvent`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| eventId | string | yes | from: listWebhookDeliveries.latestEventId |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| eventId | string |  |
| eventType | string |  |
| liveMode | boolean |  |

