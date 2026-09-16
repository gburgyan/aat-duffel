### createPayment

Pay a held order (POST /air/payments, 201), from the balance or with an airline credit, with amount and currency exactly the order's total.

**Adapter:** `createPayment`

**Inputs:**

| Name | Type | Required | Default | Description | Examples |
|------|------|----------|---------|-------------|----------|
| orderId | string | yes | from: createOrder.orderId |  |  |
| amount | string | yes |  |  |  |
| currency | string | yes |  |  |  |
| paymentType | enum[balance, airline_credit] | yes | balance |  | balance, airline_credit |
| airlineCreditId | string | no |  | The credit a payment of type airline_credit spends |  |

**Outputs:**

| Name | Type | Description |
|------|------|-------------|
| paymentId | string |  |
| amount | string |  |
| currency | string |  |
| paymentType | string |  |
| paymentStatus | string |  |

