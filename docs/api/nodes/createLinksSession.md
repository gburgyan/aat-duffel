### createLinksSession

Start a Duffel Links checkout session (POST /links/sessions). The session URL books on the account, so no output holds it: only whether one came back and its host.

**Adapter:** `createLinksSession`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| reference | string | no |  | Required by Duffel; optional here so a plan can see the refusal |
| successUrl | string | no |  | Required by Duffel |
| failureUrl | string | no |  | Required by Duffel |
| abandonmentUrl | string | no |  | Required by Duffel |
| travellerCurrency | string | no |  |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| urlIssued | boolean |  |
| urlHost | string |  |

