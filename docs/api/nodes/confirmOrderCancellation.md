### confirmOrderCancellation

Confirm a cancellation quote (POST /air/order_cancellations/{id}/actions/confirm, 200), which cancels the order and refunds it.

**Adapter:** `confirmOrderCancellation`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| orderCancellationId | string | yes | from: createOrderCancellation.orderCancellationId |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| orderCancellationId | string |  |
| confirmedAt | string |  |
| refundAmount | string |  |
| refundTo | string |  |

