### updateOfferPassenger

Name an offer's passenger and attach loyalty programme accounts before booking (PATCH /air/offers/{offer_id}/passengers/{id}, 200). Read the offer again for its new price: Duffel's test loyalty account (Amelia Earhart, ZZ, 1234567890) takes 10% off a Duffel Airways offer.

**Adapter:** `updateOfferPassenger`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| offerId | string | yes | from: getOffer.offerId |  |
| passengerId | string | yes | from: getOffer.passengers |  |
| givenName | string | yes | Amelia |  |
| familyName | string | yes | Earhart |  |
| loyaltyAirline | string | yes | ZZ | IATA code of the airline whose programme the account belongs to |
| loyaltyAccountNumber | string | no |  | The loyalty account to attach; leave out to set only the name |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| passengerId | string |  |
| givenName | string |  |
| familyName | string |  |
| loyaltyAccountCount | integer |  |
| loyaltyAccountNumber | string | The first attached account; "" when none is attached |

