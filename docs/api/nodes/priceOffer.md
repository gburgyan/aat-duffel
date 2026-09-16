### priceOffer

Price an offer with the services and payment method an order will use (POST /air/offers/{id}/actions/price, 200). The response is the offer at that price; an instant order pays exactly its total_amount. A balance payment adds no surcharge. On the LHR to STN test route each call raises the price again.

**Adapter:** `priceOffer`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| offerId | string | yes | from: getOffer.offerId |  |
| services | serviceSelection[] | no |  | Services the order will buy, as a list of {id, quantity} |
| seatServices | serviceSelection[] | no |  | Seats the order will buy, each {id}, as getSeatMaps picks them |
| bagServices | serviceSelection[] | no |  | Checked bags the order will buy, each {id}, as getOfferBags lists them |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| offerId | string |  |
| totalAmount | string |  |
| totalCurrency | string |  |
| intendedServiceCount | integer |  |
| intendedServices | serviceSelection[] | The services priced, each {id, quantity}, which createOrder books as they are |
|   └ id | string | elementField |
|   └ quantity | integer | elementField |

