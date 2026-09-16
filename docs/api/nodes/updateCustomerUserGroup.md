### updateCustomerUserGroup

Rename a customer user group or set its member (PATCH /identity/customer/user_groups/{id}, 200).

**Adapter:** `updateCustomerUserGroup`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| customerUserGroupId | string | yes | from: createCustomerUserGroup.customerUserGroupId |  |
| name | string | yes |  |  |
| userId | string | no |  |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| customerUserGroupId | string |  |
| name | string |  |
| userCount | integer |  |

