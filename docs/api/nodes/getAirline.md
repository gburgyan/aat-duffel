### getAirline

Read one airline by its arl_ ID (GET /air/airlines/{id}, 200), with its logos and its conditions of carriage when Duffel has them.

**Adapter:** `getAirline`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| airlineId | string | yes | from: listAirlines.airlines | The airline's arl_ ID |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| id | string |  |
| iataCode | string | The IATA code; "" when the airline has none |
| name | string |  |
| logoSymbolUrl | string | The square logo's URL; "" when Duffel has none |
| conditionsOfCarriageUrl | string | The airline's conditions of carriage; "" when Duffel has none |

