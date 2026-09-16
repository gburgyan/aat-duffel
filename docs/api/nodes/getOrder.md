### getOrder

Read an order (GET /air/orders/{id}, 200): its payment state, the actions it allows, its passengers by type, slices with their cabin, services, and metadata.

**Adapter:** `getOrder`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| orderId | string | yes | from: createOrder.orderId |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| orderId | string |  |
| bookingReference | string |  |
| liveMode | boolean |  |
| orderType | string |  |
| totalAmount | string |  |
| totalCurrency | string |  |
| totalAmountCents | integer |  |
| awaitingPayment | boolean |  |
| paymentRequiredBy | string |  |
| priceGuaranteeExpiresAt | string |  |
| paidAt | string |  |
| cancelledAt | string |  |
| availableActions | string | The actions the order allows, sorted and joined by commas, such as cancel,change,update |
| cancellable | boolean |  |
| passengerCount | integer |  |
| adultCount | integer |  |
| childCount | integer |  |
| infantCount | integer |  |
| loyaltyAccountCount | integer |  |
| sliceCount | integer |  |
| slices | orderSlice[] |  |
|   └ id | string | elementField |
|   └ origin | string | elementField |
|   └ destination | string | elementField |
|   └ departureDate | string | elementField |
|   └ cabinClass | string | elementField |
| firstSliceId | string |  |
| serviceCount | integer |  |
| seatCount | integer |  |
| bagCount | integer |  |
| metadataSource | string |  |
| metadataReference | string |  |
| userCount | integer |  |
| firstSliceCabin | string |  |
| firstSliceDepartureDate | string |  |
| firstSliceDepartureTime | string | The first slice's departure time, HH:MM local to its airport |
| changeCount | integer |  |
| confirmedChangeCount | integer |  |
| lastChangeTotalAmount | string | What the latest confirmed change cost; "" before any |
| refundAmount | string | The refund of a confirmed cancellation; "" when the order isn't cancelled |
| refundTo | string |  |
| airlineInitiatedChangeCount | integer |  |
| firstSliceOrigin | string |  |
| firstSliceDestination | string |  |
| seatsPerSlice | string | Seat services on each slice, in slice order, such as "2,2" |
| bagsPerSlice | string | Extra bag services on each slice, in slice order, such as "1,0" |
| totalBeforeChanges | string | The total less every confirmed change's change_total_amount |
| secondSliceDepartureDate | string | The second slice's local departure date; "" for one slice |
| cabinClasses | string | Every flight's cabin, distinct and sorted, joined by commas |

