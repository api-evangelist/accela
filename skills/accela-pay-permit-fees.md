---
name: accela-pay-permit-fees
description: Read the fees assessed against an Accela permit record, assemble them into a citizen shopping cart, take payment, and void it if the payment must be reversed.
api: Accela Construct API (V4)
generated: '2026-09-06'
method: generated
source: openapi/accela-payments-openapi.yml, openapi/accela-records-openapi.yml
base_url: https://apis.accela.com/v4
scopes: [records, shoppingcart, payments, invoices, trustaccounts]
operations:
  - v4.get.records.recordId.fees
  - v4.get.records.recordId.invoices
  - v4.post.shoppingCart
  - v4.put.shoppingCart.id
  - v4.post.payments.initialize
  - v4.put.payments.id
  - v4.put.payments.paymentId.void
  - v4.get.records.recordId.payments
  - v4.get.transaction.fees
safety: write — money movement, non-idempotent
---

# Pay permit fees

This is the only place in the Accela Construct contract that moves money, and the only place with a
first-class reversal operation. Both facts matter.

## Steps

1. **Read the fees.** `v4.get.records.recordId.fees` — `GET /v4/records/{recordId}/fees`. Invoiced amounts are
   at `v4.get.records.recordId.invoices`.
2. **Build the cart.** `v4.post.shoppingCart` — `POST /v4/shoppingCart`, then `v4.put.shoppingCart.id` to
   amend it. The cart is the citizen-facing basket; it is safe to build and discard.
3. **Initialize the payment.** `v4.post.payments.initialize` — `POST /v4/payments/initialize`. This is the
   two-phase boundary: nothing has been taken yet.
4. **Commit.** `v4.put.payments.id` — `PUT /v4/payments/{id}`. Money moves here.
   - **No idempotency key exists.** A retry after a timeout risks a double charge. Before retrying, call
     `v4.get.records.recordId.payments` and check whether the payment already landed.
5. **Confirm.** `v4.get.records.recordId.payments`, and `v4.get.transaction.fees` for the fee breakdown of a
   transaction.

## Reversal

`v4.put.payments.paymentId.void` — `PUT /v4/payments/{paymentId}/void` — voids a committed payment.

**Accela publishes no window for this.** Whether a given payment can still be voided depends on the agency's
configuration and its payment processor, neither of which is described in the contract. Do not tell a user
"you have N days" — this skill will not invent a number Accela has not published. Check with the agency.

Note that `v4.delete.records.recordId.partTransaction.ids` is summarised as "Void Record Part Transactions"
but is a DELETE with no reversal. Treat it as permanent.

## Compliance note

Accela states it is audited annually against PCI-DSS SAQ-D as a Service Provider
(https://www.accela.com/civic-platform/security/). Card data itself is not handled through these operations.
