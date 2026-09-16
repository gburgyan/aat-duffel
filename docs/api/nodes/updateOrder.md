### updateOrder

Replace an order's metadata (PATCH /air/orders/{id}, 200), the only thing it updates. The request sends the source tag again with the new reference.

**Adapter:** `updateOrder`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| orderId | string | yes | from: createOrder.orderId |  |
| reference | string | yes |  |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| orderId | string |  |
| metadataSource | string |  |
| metadataReference | string |  |

