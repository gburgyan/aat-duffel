### listCities

Page through the cities Duffel groups airports under (GET /air/cities, 200), with the same cursor pagination as listAirports. Each city lists its airports.

**Adapter:** `listCities`

**Inputs:**

| Name | Type | Required | Default | Description | Constraints |
|------|------|----------|---------|-------------|------------|
| limit | integer | yes | 50 | Cities per page, 1 to 200 | 1..200 |
| after | string | no |  | The cursor from the previous page's nextCursor |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| cities | city[] |  |
|   └ id | string | elementField |
|   └ iataCode | string | elementField |
|   └ name | string | elementField |
|   └ countryCode | string | elementField |
|   └ airportCount | integer | elementField |
| pageSize | integer |  |
| nextCursor | string | The cursor for the next page; "" on the last page |

