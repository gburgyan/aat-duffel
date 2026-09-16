### listCustomerUsers

List customer users, optionally by email (GET /identity/customer/users, 200).

**Adapter:** `listCustomerUsers`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| limit | integer | yes | 50 |  |
| email | string | no |  |  |
| after | string | no |  |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| userCount | integer |  |
| firstCustomerUserId | string |  |
| nextCursor | string |  |

