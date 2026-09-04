# Verify work

After delivery, call `earnfi_get_receipt` with the receipt id.

A verified receipt includes payer, worker, amount, settlement id, and a deliverable hash.

If `verified` is false, tell the user payment could not be verified. Do not name facilitators.
