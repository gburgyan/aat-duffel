### listAirlineInitiatedChanges

List an order's airline-initiated changes (GET /air/airline_initiated_changes?order_id=, 200).

**Adapter:** `listAirlineInitiatedChanges`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| orderId | string | yes | from: createOrder.orderId |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| airlineInitiatedChangeCount | integer |  |
| latestAirlineInitiatedChangeId | string | The newest change, the only one that can be accepted; "" when there is none |
| latestActionTaken | string |  |
| latestAvailableActions | string | The newest change's available actions, sorted and joined by commas |

