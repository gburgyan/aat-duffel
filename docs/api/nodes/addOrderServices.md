### addOrderServices

Add a service to a booked order (POST /air/orders/{id}/services), paying for it from the balance when an amount is given; a held order takes no payment.

**Adapter:** `addOrderServices`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| orderId | string | yes | from: createOrder.orderId |  |
| serviceId | string | yes |  |  |
| amount | string | no |  |  |
| currency | string | no |  |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| serviceCount | integer |  |

