### listAirports

Page through every airport Duffel knows, in name order (GET /air/airports, 200). Pages use cursors: limit is 1 to 200, and after takes the previous page's meta.after, which is null on the last page. Every response reports the token's rate limit in ratelimit-* headers.

**Adapter:** `listAirports`

**Inputs:**

| Name | Type | Required | Default | Description | Constraints |
|------|------|----------|---------|-------------|------------|
| limit | integer | yes | 50 | Airports per page, 1 to 200 | 1..200 |
| after | string | no |  | The cursor from the previous page's nextCursor; leave out for the first page |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| airports | airport[] | This page's airports |
|   └ id | string | elementField |
|   └ iataCode | string | elementField |
|   └ icaoCode | string | elementField |
|   └ name | string | elementField |
|   └ cityCode | string | elementField |
|   └ countryCode | string | elementField |
|   └ timeZone | string | elementField |
| pageSize | integer | How many airports this page holds |
| nextCursor | string | The cursor for the next page, from meta.after; "" on the last page |
| rateLimitLimit | integer | Requests the token may make per minute, from the ratelimit-limit header |
| rateLimitRemaining | integer | Requests the token has left this minute, from the ratelimit-remaining header |

