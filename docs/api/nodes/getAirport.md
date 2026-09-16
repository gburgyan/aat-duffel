### getAirport

Read one airport by its arp_ ID (GET /air/airports/{id}, 200; an unknown ID is 404). Carries IATA and ICAO codes, the IATA code of its city, the country, coordinates, and the IANA time zone that departure and arrival times are local to.

**Adapter:** `getAirport`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| airportId | string | yes | from: listAirports.airports | The airport's arp_ ID |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| id | string |  |
| iataCode | string |  |
| icaoCode | string | The ICAO code; "" when Duffel has none |
| name | string |  |
| cityCode | string | The IATA code of the airport's city, such as LON for Heathrow; "" when it has none |
| countryCode | string |  |
| timeZone | string |  |
| latitude | float |  |
| longitude | float |  |

