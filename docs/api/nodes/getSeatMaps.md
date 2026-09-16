### getSeatMaps

Read an offer's seat maps (GET /air/seat_maps?offer_id=, 200): one map per segment, each with cabins of rows, sections, and elements. A seat is for sale when its available_services price it for a passenger, and some seats carry disclosures, such as "Passenger must be an adult". The Duffel Airways economy cabin has 192 seats, 76 of them for sale at 20.00. Seats are bought only with the order.

**Adapter:** `getSeatMaps`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| offerId | string | yes | from: getOffer.offerId |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| seatMapCount | integer |  |
| seats | seat[] | One entry per seat for sale per passenger, across every map |
|   └ designator | string | elementField |
|   └ segmentId | string | elementField |
|   └ passengerId | string | elementField |
|   └ serviceId | string | elementField |
|   └ amount | string | elementField |
|   └ currency | string | elementField |
|   └ restricted | boolean | elementField |
| availableSeatCount | integer |  |
| restrictedSeatCount | integer | Seats for sale that carry a disclosure |
| seatServices | seatPick[] | The seats an order buys: for each passenger on each segment, the first seat for sale with no disclosure that no one else has; absent when there are none |
|   └ id | string | elementField |
|   └ designator | string | elementField |
|   └ passengerId | string | elementField |
|   └ segmentId | string | elementField |
|   └ amount | string | elementField |
| seatablePairCount | integer | Passenger and segment pairs with any seat for sale |

