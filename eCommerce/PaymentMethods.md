This was manually created based on Google searches.

There are two Slot types. The concept is that you first check for payment_method, then check for accepted_payment_method. If only payment_method is there, but not accepted_payment_method, then you can say that the specified method is *not* accepted by your site. If both are present, then the payment type *is accepted*.
