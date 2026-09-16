### getCustomerUser

Read a customer user (GET /identity/customer/users/{id}, 200).

**Adapter:** `getCustomerUser`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| customerUserId | string | yes | from: createCustomerUser.customerUserId |  |

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

