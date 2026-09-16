### getCity

Read one city by its cit_ ID (GET /air/cities/{id}, 200), with the airports that serve it.

**Adapter:** `getCity`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| cityId | string | yes | from: listCities.cities | The city's cit_ ID |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| id | string |  |
| iataCode | string |  |
| name | string |  |
| countryCode | string |  |
| airportCodes | string[] | The IATA codes of the city's airports |
| airportCount | integer |  |

