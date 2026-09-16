### listWebhookDeliveries

List the attempts Duffel made to deliver webhook events (GET /air/webhooks/deliveries, 200), for one webhook or event type.

**Adapter:** `listWebhookDeliveries`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| webhookId | string | no |  |  |
| eventType | string | no |  |  |
| after | string | no |  |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| deliveryCount | integer |  |
| latestDeliveryId | string |  |
| latestEventId | string |  |
| latestEventType | string |  |
| latestResponseStatusCode | integer |  |
| nextCursor | string |  |

