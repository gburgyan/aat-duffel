### updateCustomerUser

Replace a customer user's details (PUT /identity/customer/users/{id}, 200); email and both names are required.

**Adapter:** `updateCustomerUser`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| customerUserId | string | yes | from: createCustomerUser.customerUserId |  |
| email | string | yes | from: createCustomerUser.email |  |
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

