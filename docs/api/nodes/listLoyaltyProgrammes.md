### listLoyaltyProgrammes

Page through the airline loyalty programmes a passenger can book with (GET /air/loyalty_programmes, 200), with cursor pagination. Each names the airline that runs it.

**Adapter:** `listLoyaltyProgrammes`

**Inputs:**

| Name | Type | Required | Default | Description | Constraints |
|------|------|----------|---------|-------------|------------|
| limit | integer | yes | 50 | Programmes per page, 1 to 200 | 1..200 |
| after | string | no |  | The cursor from the previous page's nextCursor |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| loyaltyProgrammes | loyaltyProgramme[] |  |
|   └ id | string | elementField |
|   └ name | string | elementField |
|   └ ownerAirlineId | string | elementField |
| pageSize | integer |  |
| nextCursor | string | The cursor for the next page; "" on the last page |

