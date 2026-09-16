### updateWebhook

Activate or deactivate a webhook, or change its events (PATCH /air/webhooks/{id}, 200).

**Adapter:** `updateWebhook`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| webhookId | string | yes | from: createWebhook.webhookId |  |
| active | boolean | yes | true |  |
| events | string[] | no |  |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| webhookId | string |  |
| active | boolean |  |
| events | string |  |

