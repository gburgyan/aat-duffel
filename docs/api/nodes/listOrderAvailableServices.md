### listOrderAvailableServices

List the services a booked order can still add (GET /air/orders/{id}/available_services, 200).

**Adapter:** `listOrderAvailableServices`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| orderId | string | yes | from: createOrder.orderId |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| serviceCount | integer |  |

