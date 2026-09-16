### createBatchOfferRequest

Start a search whose offers arrive in batches (POST /air/batch_offer_requests, 201), to show results as each supplier answers. The response has the ID, total_batches, and remaining_batches, and no offers. Read the batches with getBatchOfferRequest within a minute, after which the search expires.

**Adapter:** `createBatchOfferRequest`

**Inputs:**

| Name | Type | Required | Default | Description | Examples |
|------|------|----------|---------|-------------|----------|
| origin | string | yes | LHR |  |  |
| destination | string | yes | JFK |  |  |
| departureDate | date | yes | {{today + 30 days}} |  |  |
| returnDate | date | no |  |  |  |
| passengerAges | integer[] | yes | [35] |  |  |
| cabinClass | enum[economy, premium_economy, business, first] | yes | economy |  | economy, premium_economy, business, first |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| batchOfferRequestId | string |  |
| liveMode | boolean |  |
| totalBatches | integer |  |
| remainingBatches | integer |  |

