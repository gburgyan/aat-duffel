### listOrders

Page through the account's orders (GET /air/orders, 200) with cursor pagination: limit is 1 to 200, and after takes the previous page's meta.after. Filters narrow the list to the orders booked from an offer, a booking reference, a customer user's orders, or orders by payment state. Orders this package books carry metadata.source "aat-duffel", and each page counts those, the ones of them still active (not cancelled), and active orders from anywhere else, apart.

**Adapter:** `listOrders`

**Inputs:**

| Name | Type | Required | Default | Description | Constraints |
|------|------|----------|---------|-------------|------------|
| limit | integer | yes | 200 | Orders per page, 1 to 200 | 1..200 |
| after | string | no |  | The cursor from the previous page's nextCursor |  |
| offerId | string | no |  | Only the orders booked from this offer |  |
| bookingReference | string | no |  | Only the order with this booking reference |  |
| userId | string | no |  | Only the orders a customer user (icu_) is attached to |  |
| awaitingPayment | boolean | no |  | true for orders still awaiting payment, false for the rest |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| orderCount | integer |  |
| ourOrderCount | integer | Orders on the page this package booked (metadata.source is aat-duffel) |
| ourActiveOrderCount | integer | Of the package's orders, those not cancelled |
| ourActiveOrders | activeOrder[] | The package's orders that are still active, when there are any |
|   └ id | string | elementField |
|   └ bookingReference | string | elementField |
|   └ createdAt | string | elementField |
| otherActiveOrderCount | integer | Active orders this package didn't book, such as those earlier projects left |
| liveModeOrderCount | integer | Orders booked in live mode; 0 on a test-mode account |
| nextCursor | string | The cursor for the next page; "" on the last page |

