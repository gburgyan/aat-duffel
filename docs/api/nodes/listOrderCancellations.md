### listOrderCancellations

List an order's cancellations (GET /air/order_cancellations?order_id=, 200).

**Adapter:** `listOrderCancellations`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| orderId | string | yes | from: createOrder.orderId |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| cancellationCount | integer |  |
| confirmedCancellationCount | integer |  |

