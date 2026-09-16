### getOrderChange

Read an order change (GET /air/order_changes/{id}, 200), pending or confirmed.

**Adapter:** `getOrderChange`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| orderChangeId | string | yes | from: createOrderChange.orderChangeId |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| orderChangeId | string |  |
| changeTotalAmount | string |  |
| confirmedAt | string |  |

