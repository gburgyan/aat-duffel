### createComponentClientKey

Issue a component client key for Duffel's UI components (POST /identity/component_client_keys), with no claims, a user, or a user and an order. The key is a credential, so no output holds it.

**Adapter:** `createComponentClientKey`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| userId | string | no |  |  |
| orderId | string | no |  |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| keyIssued | boolean |  |
| keyPartCount | integer | The key's dot-separated parts; a JWT has three |

