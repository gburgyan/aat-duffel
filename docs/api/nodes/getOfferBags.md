### getOfferBags

Read an offer's extra checked bags (GET /air/offers/{id}?return_available_services=true, 200), one service per passenger and segment. A step of its own names the bags an order buys, so getOffer's outputs don't wire bags into every order.

**Adapter:** `getOfferBags`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| offerId | string | yes | from: getOffer.offerId |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| bagServices | bagService[] |  |
|   └ id | string | elementField |
|   └ passengerId | string | elementField |
|   └ segmentId | string | elementField |
|   └ amount | string | elementField |
| bagServiceCount | integer |  |

