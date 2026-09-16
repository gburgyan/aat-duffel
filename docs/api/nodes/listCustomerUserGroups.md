### listCustomerUserGroups

List customer user groups (GET /identity/customer/user_groups, 200).

**Adapter:** `listCustomerUserGroups`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| limit | integer | yes | 50 |  |
| after | string | no |  |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| groupCount | integer |  |
| nextCursor | string |  |

