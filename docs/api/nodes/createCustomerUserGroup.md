### createCustomerUserGroup

Create a customer user group (POST /identity/customer/user_groups, 201), optionally with a member. Cleanup deletes it.

**Adapter:** `createCustomerUserGroup`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| name | string | yes | aat-duffel {{random 8}} |  |
| userId | string | no |  |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| customerUserGroupId | string |  |
| name | string |  |
| userCount | integer |  |

