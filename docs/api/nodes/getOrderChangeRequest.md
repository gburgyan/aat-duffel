### getOrderChangeRequest

Read an order change request with its change offers (GET /air/order_change_requests/{id}, 200).

**Adapter:** `getOrderChangeRequest`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| orderChangeRequestId | string | yes | from: createOrderChangeRequest.orderChangeRequestId |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| orderChangeRequestId | string |  |
| changeOfferCount | integer |  |
| changeOffers | changeOffer[] |  |
|   └ id | string | elementField |
|   └ cabinClass | string | elementField |
|   └ departureTime | string | elementField |
|   └ departureDate | string | elementField |
|   └ changeTotalAmount | string | elementField |
|   └ penaltyTotalAmount | string | elementField |
|   └ newTotalAmount | string | elementField |
| cabins | string |  |
| departureTimes | string |  |
| changeTotals | string |  |
| businessOfferCount | integer |  |

