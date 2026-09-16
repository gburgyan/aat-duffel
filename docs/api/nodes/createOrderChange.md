### createOrderChange

Choose a change offer (POST /air/order_changes, 201), which makes a pending change with its cost. Nothing changes on the order until confirmOrderChange.

**Adapter:** `createOrderChange`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| orderChangeOfferId | string | yes | from: getOrderChangeOffer.orderChangeOfferId |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| orderChangeId | string |  |
| changeTotalAmount | string |  |
| changeTotalCurrency | string |  |
| penaltyTotalAmount | string |  |
| newTotalAmount | string |  |
| confirmedAt | string |  |
| paymentAmount | string | The payment the confirmation sends; absent when the change costs nothing |
| addedCabinClass | string |  |
| addedDepartureTime | string |  |

