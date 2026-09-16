### getOfferRequest

Read an offer request (GET /air/offer_requests/{id}, 200). It inlines every offer the search produced, so the response is as large as return_offers=true would have made the search's; listOffers pages them instead.

**Adapter:** `getOfferRequest`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| offerRequestId | string | yes | from: createOfferRequest.offerRequestId |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| offerRequestId | string |  |
| cabinClass | string |  |
| sliceCount | integer |  |
| passengerCount | integer |  |
| offerCount | integer |  |

