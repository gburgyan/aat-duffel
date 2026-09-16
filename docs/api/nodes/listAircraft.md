### listAircraft

Page through the aircraft types segments are flown on (GET /air/aircraft, 200), with cursor pagination.

**Adapter:** `listAircraft`

**Inputs:**

| Name | Type | Required | Default | Description | Constraints |
|------|------|----------|---------|-------------|------------|
| limit | integer | yes | 50 | Aircraft per page, 1 to 200 | 1..200 |
| after | string | no |  | The cursor from the previous page's nextCursor |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| aircraft | aircraftType[] |  |
|   └ id | string | elementField |
|   └ iataCode | string | elementField |
|   └ name | string | elementField |
| pageSize | integer |  |
| nextCursor | string | The cursor for the next page; "" on the last page |

