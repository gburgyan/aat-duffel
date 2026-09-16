### suggestPlaces

Look up airports and cities by name or near a point (GET /places/suggestions), answering 200 with a list, empty when nothing matches. Send query for a name or code, or lat, lng, and rad (metres) for a point. An airport (arp_, type airport) carries its city under city; a city (cit_, type city) lists its airports.

**Adapter:** `suggestPlaces`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| query | string | no |  | A city, airport, or IATA code to match, such as Heathrow or JFK |
| lat | float | no |  | Latitude of the point to search near; send lng and rad with it |
| lng | float | no |  | Longitude of the point to search near |
| rad | integer | no |  | Search radius around the point, in metres |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| placeCount | integer | How many airports and cities matched |
| places | place[] | The matches in Duffel's order, airports and cities mixed |
|   └ id | string | elementField |
|   └ type | enum[airport, city] | elementField |
|   └ iataCode | string | elementField |
|   └ name | string | elementField |
|   └ cityId | string | elementField |
|   └ cityCode | string | elementField |
|   └ countryCode | string | elementField |
| airportCodes | string[] | The IATA codes of the matched airports, in order |
| cityCodes | string[] | The IATA codes of the matched cities, in order |
| firstAirportCode | string | The first matched airport's IATA code; "" when no airport matched |
| firstCityAirportCode | string | The first airport of the first matched city; "" when no city matched |

