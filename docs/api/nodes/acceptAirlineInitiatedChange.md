### acceptAirlineInitiatedChange

Accept an airline-initiated change (POST /air/airline_initiated_changes/{id}/actions/accept). Only the order's latest change can be accepted; an older one gets 422 stale_airline_initiated_change_accept.

**Adapter:** `acceptAirlineInitiatedChange`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| airlineInitiatedChangeId | string | yes | from: listAirlineInitiatedChanges.latestAirlineInitiatedChangeId |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| airlineInitiatedChangeId | string |  |
| actionTaken | string |  |

