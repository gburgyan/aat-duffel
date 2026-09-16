### createOrderChangeRequest

Ask what it costs to replace an order's slice with another (POST /air/order_change_requests, 201). The request removes one slice and adds a journey on a new date in a requested cabin, and answers with change offers, each with its added flight, what it costs, and the order's new total.

**Adapter:** `createOrderChangeRequest`

**Inputs:**

| Name | Type | Required | Default | Description | Examples |
|------|------|----------|---------|-------------|----------|
| orderId | string | yes | from: createOrder.orderId |  |  |
| sliceId | string | yes | from: createOrder.firstSliceId |  |  |
| origin | string | yes |  |  |  |
| destination | string | yes |  |  |  |
| departureDate | date | yes | {{today + 37 days}} |  |  |
| cabinClass | enum[economy, premium_economy, business, first] | yes | economy |  | economy, premium_economy, business, first |

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
| cabins | string | The distinct cabins offered, sorted and joined by commas |
| departureTimes | string | The distinct departure times offered, sorted and joined by commas |
| changeTotals | string | The distinct change totals, sorted and joined by commas |
| businessOfferCount | integer |  |

