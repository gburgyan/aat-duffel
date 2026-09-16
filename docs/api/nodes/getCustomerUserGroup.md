### getCustomerUserGroup

Read a customer user group (GET /identity/customer/user_groups/{id}, 200).

**Adapter:** `getCustomerUserGroup`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| customerUserGroupId | string | yes | from: createCustomerUserGroup.customerUserGroupId |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| customerUserGroupId | string |  |
| name | string |  |
| userCount | integer |  |

