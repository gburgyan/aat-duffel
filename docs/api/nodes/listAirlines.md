### listAirlines

Page through the airlines Duffel sells (GET /air/airlines, 200), with cursor pagination. Test mode's own airline, Duffel Airways, has IATA code ZZ.

**Adapter:** `listAirlines`

**Inputs:**

| Name | Type | Required | Default | Description | Constraints |
|------|------|----------|---------|-------------|------------|
| limit | integer | yes | 50 | Airlines per page, 1 to 200 | 1..200 |
| after | string | no |  | The cursor from the previous page's nextCursor |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| airlines | airline[] |  |
|   └ id | string | elementField |
|   └ iataCode | string | elementField |
|   └ name | string | elementField |
| pageSize | integer |  |
| nextCursor | string | The cursor for the next page; "" on the last page |

