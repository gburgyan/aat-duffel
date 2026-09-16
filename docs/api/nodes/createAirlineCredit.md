### createAirlineCredit

Record an airline credit the account holds (POST /air/airline_credits).

**Adapter:** `createAirlineCredit`

**Inputs:**

| Name | Type | Required | Default | Description | Examples |
|------|------|----------|---------|-------------|----------|
| airlineCode | string | yes | ZZ |  |  |
| amount | string | yes | 25.00 |  |  |
| currency | string | yes | USD |  |  |
| code | string | yes | {{unixtime}}000 | A 13-digit ticket number; Duffel refuses letters with 422 validation_format |  |
| issuedOn | date | yes | {{today}} |  |  |
| expiresAt | string | yes | {{now + 365 days}} |  |  |
| creditType | enum[eticket, mco, emd] | yes | mco |  | eticket, mco, emd |
| givenName | string | yes | Amelia |  |  |
| familyName | string | yes | Earhart |  |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| airlineCreditId | string |  |
| amount | string |  |
| code | string |  |

