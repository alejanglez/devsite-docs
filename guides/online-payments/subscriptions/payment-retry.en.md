---
sites_supported:
  - mla
  - mlm
  - mlb
---

# Collection reattempt logic

By automating the recurrence of your collections, authorized payments that will have a debit date configured based on the periodicity that was defined in the subscription are created.

## Payment statuses
At the time the instalment is collected, three alternatives may arise, based on the outcome of the payment:

* __Payment is successfully made__ so, the instalment will remain as `processed` and will not be reattempted. 
----[mla]----
* __Payment is being processed__ so the instalment will be pending in a `waiting for gateway` status until the payment is resolved.
------------
* __Payment is declined__ so the installment will always remain in `recycling` status and when the installment is not expired or has not reached the maximum number of reattempts. Otherwise, it will be processed with the `processed` status.

## Declined payments

When an instalment remains in `recycling` status, it enters a reattempt scheme with a maximum of 4 possibilities, when the installment is collected again. The result can be any of the three points mentioned above. 

If the payment is declined, it is updated to a new collection date by adding 1 of the 4 possibilities within ten days as a reattempt time window to the last available date.

By default the reattempt is within a 10 day window. In case the installment has an expiration date, the time window is adjusted to that date and maintains the logic of 4 reattempt.

----[mla]----

## Payments in process

If an installment is in `waiting for gateway` status and, when the payment is resolved, it appears as declined, and the expiration date is met, the installment will automatically appear as processed with the `processed` status. Otherwise, it will enter the reattempt scheme.

------------

the installment cannot be collected on the fourth reattempt, it will automatically remain in `processed` status, associated with a declined payment.

> NOTE
> 
> Note
> 
> The result of one installment does not affect the generation and processing of the remaining installments for the same subscription.

------------
### Next steps

> LEFT_BUTTON
>
> Advanced integration
>
> Update, edit or cancel your subscriptions.
>
> [Advanced integration](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/en/guides/online-payments/subscriptions/advanced-integration/)

> RIGHT_BUTTON
>
> Tests
>
> Check that your subscriptions are properly configured with the test users. 
>
> [Tests](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/en/guides/online-payments/subscriptions/testing/)
