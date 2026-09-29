---
name: verify-work
description: Verify completed work using EarnFi Work Receipt V1.
license: MIT
metadata:
  author: earnfi
  version: "1.0.0"
  homepage: https://github.com/earnfidotfun/earnfi-cursor-plugin
---

# Verify work

After delivery, call `earnfi_get_receipt` with the receipt id (or `earnfi_get_work_receipt` by ref).

A verified receipt includes payer, worker, amount, settlement id, and a deliverable hash.

If `verified` is false, tell the user payment could not be verified. Do not name facilitators.

See **work-receipt** for ref_type lookup table.
