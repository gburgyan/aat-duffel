### getOrderCancellation

Read a cancellation, quoted or confirmed (GET /air/order_cancellations/{id}, 200).

**Adapter:** `getOrderCancellation`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| orderCancellationId | string | yes | from: createOrderCancellation.orderCancellationId |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| orderCancellationId | string |  |
| refundAmount | string |  |
| refundTo | string |  |
| expiresAt | string |  |
| confirmedAt | string |  |

