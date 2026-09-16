### createWebhook

Register a webhook (POST /air/webhooks, 201). Duffel allows one per live mode, and the signing secret comes back only here; no output holds it. Cleanup deletes the webhook.

**Adapter:** `createWebhook`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| url | string | yes | https://example.com/aat-duffel/webhooks |  |
| events | string[] | yes | [order.created] |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| webhookId | string |  |
| url | string |  |
| active | boolean |  |
| liveMode | boolean |  |
| events | string | The subscribed events, sorted and joined by commas |
| secretIssued | boolean |  |

