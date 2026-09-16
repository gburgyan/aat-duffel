### listOffers

Page through an offer request's offers (GET /air/offers, 200), cheapest first with sort=total_amount; maxConnections 0 keeps direct flights only. Every offer prices all the passengers searched for and is owned by the airline that sells it. In test mode only Duffel Airways, owner ZZ, books reliably, so plans take the offer whose ownerCode is ZZ. A route with no flights, such as the PVD to RAI test route, gives an empty page.

**Adapter:** `listOffers`

**Inputs:**

| Name | Type | Required | Default | Description | Constraints | Examples |
|------|------|----------|---------|-------------|------------|----------|
| offerRequestId | string | yes | from: createOfferRequest.offerRequestId |  |  |  |
| sort | enum[total_amount, total_duration] | yes | total_amount |  |  | total_amount, total_duration |
| limit | integer | yes | 50 | Offers per page, 1 to 200 | 1..200 |  |
| maxConnections | integer | no |  | The most connections a slice may have; 0 for direct flights only |  |  |
| after | string | no |  | The cursor from the previous page's nextCursor |  |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| offers | offer[] |  |
|   └ id | string | elementField |
|   └ ownerCode | string | elementField |
|   └ totalAmount | string | elementField |
|   └ totalCurrency | string | elementField |
|   └ requiresInstantPayment | boolean | elementField |
| pageSize | integer |  |
| nextCursor | string | The cursor for the next page; "" on the last page |
| zzOfferCount | integer | How many offers on this page Duffel Airways owns |
| instantPaymentCount | integer | How many offers on this page must be paid as they are booked, rather than held |
| cheapestTotalAmount | string | The first offer's total; the cheapest when sorted by total_amount; "" on an empty page |

