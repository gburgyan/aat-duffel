### listOfferRequests

Page through the account's offer requests (GET /air/offer_requests, 200), with cursor pagination. Entries carry no offers.

**Adapter:** `listOfferRequests`

**Inputs:**

| Name | Type | Required | Default | Description | Constraints |
|------|------|----------|---------|-------------|------------|
| limit | integer | yes | 50 | Offer requests per page, 1 to 200 | 1..200 |
| after | string | no |  | The cursor from the previous page's nextCursor |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| offerRequests | offerRequest[] |  |
|   └ id | string | elementField |
|   └ cabinClass | string | elementField |
|   └ createdAt | string | elementField |
| pageSize | integer |  |
| nextCursor | string | The cursor for the next page; "" on the last page |

