### getOrderChangeOffer

Read one change offer (GET /air/order_change_offers/{id}, 200) with the flight it adds and its cost.

**Adapter:** `getOrderChangeOffer`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| orderChangeOfferId | string | yes |  |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| orderChangeOfferId | string |  |
| changeTotalAmount | string |  |
| changeTotalCurrency | string |  |
| penaltyTotalAmount | string |  |
| newTotalAmount | string |  |
| cabinClass | string |  |
| departureTime | string |  |
| departureDate | string |  |

