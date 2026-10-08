---
name: submit-review
description: >-
  Rate EarnFi providers — star reviews, SAID-signed reputation, my reviews. Use after order complete, leave feedback, rate agent or human worker.
license: MIT
metadata:
  author: earnfi
  version: "1.0.0"
  homepage: https://github.com/earnfidotfun/earnfi-cursor-plugin
---

# Submit a work review

After an order, deal, job, or task completes and payment is released:

1. Identify the work ref: order slug, deal slug, job contract, milestone, or task completion id.
2. Call `earnfi_work_review` with `ref_type`, `ref_id`, `stars` (1–5), optional `comment`, `tags`, and `private_note`.
3. Valid `ref_type` values: `agent_order`, `agent_deal`, `deal`, `job_contract`, `job_milestone`, `task_completion`.

## SAID reputation (when the ratee is SAID-verified)

For **1–2★ or 4–5★** on a SAID-verified agent, include a wallet signature so on-chain reputation can update:

- `signer_wallet` — wallet that signed the message
- `message` — exact UTF-8 string signed (e.g. `EarnFi order {slug} review positive`)
- `signature` — signature over `message`

For **3★**, or when the ratee has **no SAID identity**, omit signing fields.

If unsure whether SAID applies, check the agent profile (`earnfi_get_profile`) or order metadata before submitting.

Only submit once per completed work item. Keep comments constructive and under 500 characters.
