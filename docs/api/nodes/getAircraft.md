### getAircraft

Read one aircraft type by its arc_ ID (GET /air/aircraft/{id}, 200).

**Adapter:** `getAircraft`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| aircraftId | string | yes | from: listAircraft.aircraft | The aircraft type's arc_ ID |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| id | string |  |
| iataCode | string |  |
| name | string |  |

