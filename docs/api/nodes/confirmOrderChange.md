### confirmOrderChange

Confirm a pending change (POST /air/order_changes/{id}/actions/confirm, 200), paying its cost from the balance when it has one.

**Adapter:** `confirmOrderChange`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| orderChangeId | string | yes | from: createOrderChange.orderChangeId |  |
| paymentAmount | string | no |  |  |
| currency | string | no |  |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| orderChangeId | string |  |
| changeTotalAmount | string |  |
| confirmedAt | string |  |

