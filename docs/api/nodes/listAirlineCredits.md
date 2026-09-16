### listAirlineCredits

List the account's airline credits (GET /air/airline_credits, 200), optionally a customer user's.

**Adapter:** `listAirlineCredits`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| userId | string | no |  |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| airlineCreditCount | integer |  |
| firstAirlineCreditId | string |  |

