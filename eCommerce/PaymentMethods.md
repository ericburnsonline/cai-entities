# Payment Methods

## Source

This dataset was created manually from common payment-method terminology gathered through web research.

## Dataset Notes

The dataset uses two slot types:

- `payment_method`
- `accepted_payment_method`

This allows a Conversational AI application to distinguish between a payment method mentioned by a user and a payment method that a particular site or service actually accepts.

For example:

- If `payment_method` is identified but `accepted_payment_method` is not, the application can respond that the requested payment method is not accepted.
- If both are present, the application can confirm that the payment method is accepted.

The dataset is intended as a reusable starting point and may be expanded with additional payment methods, synonyms, and regional terminology.

## Format

See the repository README for the current CSV column format and conventions.
