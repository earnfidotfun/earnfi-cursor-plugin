---
name: human-actions
description: >-
  Paid Human Actions on EarnFi — ask, review, vote, test, research, verify, moderate, feedback.
  Use when the user wants human judgment, QA, user testing, moderation, crowdsourced votes, expert review,
  or "real person" validation (not Clawpump). Solana USDC x402; poll results with work receipts.
license: MIT
metadata:
  author: earnfi
  version: "1.2.0"
  homepage: https://github.com/earnfidotfun/earnfi-cursor-plugin
---

# Human Actions (Solana rail)

Generic create: `earnfi_human_action_create` with `action_type`.

Dedicated tools (same pay-first flow):

| Type | Tool |
|------|------|
| Ask | `earnfi_ask_humans` |
| Review | `earnfi_human_review` |
| Vote | `earnfi_human_vote` |
| Test / QA | `earnfi_human_test` |
| Research | `earnfi_human_research` |
| Verify | `earnfi_human_verify` |
| Moderate | `earnfi_human_moderate` |
| Feedback | `earnfi_human_feedback` |

1. Call without `payment_signature` → 402 quote.
2. Sign Solana x402 USDC → retry with `payment_signature`.
3. Poll `earnfi_human_action_result` with `action_id` + `secret`.

OKX USDT0 equivalents: `earnfi_okx_human_*` — see **okx-rail** skill only for OKX rail.
