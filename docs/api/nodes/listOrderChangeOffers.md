### listOrderChangeOffers

Page through a change request's offers, cheapest change first (GET /air/order_change_offers?order_change_request_id=, 200), with cursor pagination.

**Adapter:** `listOrderChangeOffers`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| orderChangeRequestId | string | yes | from: createOrderChangeRequest.orderChangeRequestId |  |
| after | string | no |  |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
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
| nextCursor | string |  |

