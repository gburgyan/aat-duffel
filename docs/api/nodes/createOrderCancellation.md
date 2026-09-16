### createOrderCancellation

Quote an order's cancellation (POST /air/order_cancellations, 201): the refund, where it goes, and when the quote expires. Nothing is cancelled until confirmOrderCancellation, which cleanup runs next.

**Adapter:** `createOrderCancellation`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| orderId | string | yes | from: createOrder.orderId |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| orderCancellationId | string |  |
| refundAmount | string |  |
| refundCurrency | string |  |
| refundTo | string |  |
| expiresAt | string |  |
| airlineCreditCount | integer |  |

