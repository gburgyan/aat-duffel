### getOffer

Read one offer at its latest price, with the extra services it sells (GET /air/offers/{id}?return_available_services=true, 200). An offer expires about 30 minutes after the search; a stale one, as on the LGW to LHR test route, is 422 offer_no_longer_available. The price can move after the search: on the LHR to STN test route every read costs 10.00 more. A Duffel Airways offer can always be held, with payment due about three days later, and sells one extra 23 kg checked bag per passenger and segment. Whether it allows a change or a refund varies from search to search; an allowed one states its penalty.

**Adapter:** `getOffer`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| offerId | string | yes | from: listOffers.offers |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| offerId | string |  |
| ownerCode | string |  |
| liveMode | boolean |  |
| totalAmount | string | What the offer costs for every passenger, as a decimal string |
| totalCurrency | string |  |
| baseAmount | string |  |
| taxAmount | string |  |
| expiresAt | string |  |
| requiresInstantPayment | boolean | true when the offer can't be held and must be paid as it's booked |
| paymentRequiredBy | string | When a held order of this offer must be paid; "" when it can't be held |
| fareBrand | string | The first slice's fare brand, such as Basic; "" when the airline names none |
| changeAllowed | boolean |  |
| changePenalty | string | The penalty for a change before departure; "" when none is stated |
| refundAllowed | boolean |  |
| refundPenalty | string | The penalty for a refund before departure; "" when none is stated |
| sliceCount | integer |  |
| firstSliceSegmentCount | integer | Flights in the first slice; 2 or more means a connection |
| firstSegmentStopCount | integer | Stops within the first flight, where the aircraft lands without a change of flight number |
| firstSegmentBaggageCount | integer | Kinds of baggage included for the first passenger on the first flight |
| passengers | offerPassenger[] |  |
|   └ id | string | elementField |
|   └ type | string | elementField |
|   └ age | integer | elementField |
|   └ loyaltyAccountCount | integer | elementField |
| services | service[] | The extra services the offer sells, each for one passenger on one segment |
|   └ id | string | elementField |
|   └ type | string | elementField |
|   └ amount | string | elementField |
|   └ currency | string | elementField |
|   └ maxQuantity | integer | elementField |
|   └ bagType | string | elementField |
|   └ maxWeightKg | integer | elementField |
|   └ passengerId | string | elementField |
|   └ segmentId | string | elementField |
| serviceCount | integer |  |
| checkedBagServiceId | string | The first extra checked bag for sale; "" when the offer sells none |
| checkedBagAmount | string | That bag's price; "" when the offer sells none |
| totalAmountCents | integer | totalAmount in cents, to compare prices as whole numbers |
| bookingPassengers | bookingPassenger[] | The passengers as createOrder names them, each with a title, gender, names, and a birth date that fits the age searched; adults who carry an infant are in infantCarers instead |
|   └ id | string | elementField |
|   └ type | string | elementField |
|   └ age | integer | elementField |
|   └ title | string | elementField |
|   └ gender | string | elementField |
|   └ givenName | string | elementField |
|   └ familyName | string | elementField |
|   └ bornOn | string | elementField |
| infantCarers | bookingPassenger[] | Adults who carry an infant, each with the infant's pas_ ID as infantPassengerId; absent without infants |
|   └ id | string | elementField |
|   └ type | string | elementField |
|   └ age | integer | elementField |
|   └ title | string | elementField |
|   └ gender | string | elementField |
|   └ givenName | string | elementField |
|   └ familyName | string | elementField |
|   └ bornOn | string | elementField |
|   └ infantPassengerId | string | elementField |
| passengerCount | integer |  |
| firstSliceOrigin | string |  |
| firstSliceDestination | string |  |
| firstSliceDepartureDate | string | The first flight's local departure date |
| secondSliceDepartureDate | string | The second slice's first flight's local departure date; "" for one slice |
| cabinClasses | string | Every flight's cabin, distinct and sorted, joined by commas |

