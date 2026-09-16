### getPayment

Read one payment by its ID (GET /air/payments/{id}, 200).

**Adapter:** `getPayment`

**Inputs:**

| Name | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| paymentId | string | yes | from: createPayment.paymentId |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| paymentId | string |  |
| amount | string |  |
| currency | string |  |
| paymentType | string |  |
| paymentStatus | string |  |

