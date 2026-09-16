### getBatchOfferRequest

Read the batches of a batch search that have arrived since the last read (GET /air/batch_offer_requests/{id}, 200). Each read returns only the new batches' offers, and remaining_batches counts what is still to come, so repeat it until remaining_batches is 0, collecting the offers. Batches come per supplier, so the count falls unevenly (6, 2, 1, 0 in one run), and Duffel Airways arrives in the first.

**Adapter:** `getBatchOfferRequest`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| batchOfferRequestId | string | yes | from: createBatchOfferRequest.batchOfferRequestId |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| remainingBatches | integer |  |
| totalBatches | integer |  |
| offerCount | integer | Offers in this read's batches |
| zzOffers | offer[] | The Duffel Airways offers in this read's batches |
|   └ id | string | elementField |
|   └ ownerCode | string | elementField |
|   └ totalAmount | string | elementField |
|   └ totalCurrency | string | elementField |
| zzOfferCount | integer |  |

