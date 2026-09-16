### getLoyaltyProgramme

Read one loyalty programme by its loy_ ID (GET /air/loyalty_programmes/{id}, 200), with the arl_ ID of the airline that runs it and its alliance, if any.

**Adapter:** `getLoyaltyProgramme`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| loyaltyProgrammeId | string | yes | from: listLoyaltyProgrammes.loyaltyProgrammes | The programme's loy_ ID |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| id | string |  |
| name | string |  |
| ownerAirlineId | string | The arl_ ID of the airline that runs the programme |
| alliance | string | The alliance the programme belongs to; "" when none |

