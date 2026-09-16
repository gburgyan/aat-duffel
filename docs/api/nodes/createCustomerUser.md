### createCustomerUser

Create a customer user (POST /identity/customer/users, 201). Duffel's API reference lists no way to delete one, so each run's user stays on the account, with an email unique to the run.

**Adapter:** `createCustomerUser`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| email | string | yes | aat-duffel-{{random 10}}@example.com |  |
| givenName | string | yes | Amelia |  |
| familyName | string | yes | Earhart |  |
| phoneNumber | string | no |  |  |
| groupId | string | no |  |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| customerUserId | string |  |
| email | string |  |
| givenName | string |  |
| familyName | string |  |
| phoneNumber | string |  |
| groupId | string |  |
| liveMode | boolean |  |

