### listUpsellOffers

Ask for the same journey in higher fare brands (POST /air/offers/{id}/upsell_offers). Duffel Airways sells no upsells: the answer is 422 unsupported_action, an airline_error, and the JS client's /upsell path answers the same.

**Adapter:** `listUpsellOffers`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| offerId | string | yes | from: getOffer.offerId |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| upsellOfferCount | integer | How many upsell offers came back, from an airline that sells them |

