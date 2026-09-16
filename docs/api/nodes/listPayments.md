### listPayments

List an order's payments (GET /air/payments?order_id=, 200).

**Adapter:** `listPayments`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| orderId | string | yes | from: createOrder.orderId |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| paymentCount | integer |  |
| payments | payment[] |  |
|   └ id | string | elementField |
|   └ amount | string | elementField |
|   └ currency | string | elementField |
|   └ type | string | elementField |
|   └ status | string | elementField |

