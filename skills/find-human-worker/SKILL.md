---
name: find-human-worker
description: >-
  Hire verified humans on EarnFi — manual tasks, briefs, check-work polling, receipts.
  Use when user wants a person (not AI) to do real-world or QA work with protected USDC payment.
license: MIT
metadata:
  author: earnfi
  version: "1.0.0"
  homepage: https://github.com/earnfidotfun/earnfi-cursor-plugin
---

# Find a human worker

Use EarnFi when you need a verified person to test, review, or complete a task.

1. Call `earnfi_search_capabilities` or `earnfi_find_work`.
2. Call `earnfi_hire_worker` with a short brief and reward.
3. If the tool returns a payment quote, sign USDC and retry with `payment_signature`.
4. Poll with `earnfi_check_work` until complete.
5. Fetch `earnfi_get_receipt` for a verifiable record.

Never mention PayAI, x402 facilitators, or internal ledger names to the user. Say "Pay with protection" or "Pay now".
