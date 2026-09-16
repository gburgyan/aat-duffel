### createOrder

Book an offer (POST /air/orders, 201). An instant order pays from the balance, with amount and currency exactly the priced total, services included; a hold order sends no payment and is paid later with createPayment. Each passenger is named with the offer's pas_ ID, a title, gender, names, and a birth date that fits the age searched, and an adult who carries an infant names that infant. Every order carries metadata.source "aat-duffel". Its cleanup cancels the order.

**Adapter:** `createOrder`

**Inputs:**

| Name | Type | Required | Default | Description | Examples |
|------|------|----------|---------|-------------|----------|
| orderType | enum[instant, hold] | yes | instant |  | instant, hold |
| offerId | string | yes | from: getOffer.offerId |  |  |
| bookingPassengers | bookingPassenger[] | yes | from: getOffer.bookingPassengers |  |  |
| infantCarers | bookingPassenger[] | no |  | Adults who carry an infant, from getOffer.infantCarers |  |
| services | serviceSelection[] | no |  | Services to buy, as priceOffer.intendedServices lists them |  |
| amount | string | no |  | The payment, exactly the priced total; leave it out for a hold order |  |
| currency | string | no |  |  |  |
| email | string | yes | {{env.contactEmail}} |  |  |
| phoneNumber | string | yes | {{env.contactPhone}} |  |  |
| userId | string | no |  | A customer user (icu_) to attach to the order |  |
| reference | string | no |  | A reference stored in the order's metadata next to its source |  |

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
| lastChangeTotalAmount | string |  |
| refundAmount | string |  |
| refundTo | string |  |
| airlineInitiatedChangeCount | integer |  |
| firstSliceOrigin | string |  |
| firstSliceDestination | string |  |
| seatsPerSlice | string |  |
| bagsPerSlice | string |  |
| totalBeforeChanges | string |  |
| secondSliceDepartureDate | string |  |
| cabinClasses | string |  |

