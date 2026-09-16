### createOfferRequest

Search for flights (POST /air/offer_requests?return_offers=false, 201). The response has the offer request's orq_ ID, its passengers with their pas_ IDs, and the slices searched, but no offers: listOffers pages them, where return_offers=true would put every offer in this response (1.5 MB for 229 offers from LHR to JFK). One slice is a one-way search; returnDate adds the way back, and stopover with onwardDate adds an open-jaw leg from destination to stopover instead. Passengers are given by age. live_mode is false for a test token. A supplier slower than supplierTimeout milliseconds is left out; Duffel's STN to LHR test route answers 504 gateway_timeout_error.

**Adapter:** `createOfferRequest`

**Inputs:**

| Name | Type | Required | Default | Description | Examples |
|------|------|----------|---------|-------------|----------|
| origin | string | yes | LHR | IATA code of the airport or city to fly from |  |
| destination | string | yes | JFK | IATA code of the airport or city to fly to |  |
| departureDate | date | yes | {{today + 30 days}} | The outbound departure date |  |
| returnDate | date | no |  | Adds a slice back from destination to origin on this date |  |
| stopover | string | no |  | Adds an open-jaw slice from destination to this airport, departing onwardDate |  |
| onwardDate | date | no |  | The departure date of the open-jaw slice; send with stopover |  |
| passengerAges | integer[] | yes | [35] | One age per passenger; 18 and over flies as an adult, under 2 as an infant |  |
| cabinClass | enum[economy, premium_economy, business, first] | yes | economy |  | economy, premium_economy, business, first |
| maxConnections | integer | no |  | The most connections a slice may have; 0 for direct flights only |  |
| supplierTimeout | integer | yes | 20000 | Milliseconds to wait for each supplier, 2000 to 60000 |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| offerRequestId | string |  |
| liveMode | boolean | false for a test token; plans assert it before anything is booked |
| cabinClass | string |  |
| sliceCount | integer |  |
| passengerCount | integer |  |
| passengers | searchPassenger[] | The passengers searched for, with the pas_ IDs an order names |
|   └ id | string | elementField |
|   └ type | string | elementField |
|   └ age | integer | elementField |
| firstSliceOrigin | string | The first slice's origin as Duffel echoes the search |
| firstSliceDestination | string |  |
| firstSliceDepartureDate | string |  |
| secondSliceDepartureDate | string | The second slice's departure date; "" for a one-way search |

