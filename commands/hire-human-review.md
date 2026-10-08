---
name: hire-human-review
description: Request a paid human review Human Action on EarnFi (quote then x402 pay).
---

# Hire a human review

1. Load **find-human-worker** and **mcp-router** skills if needed.
2. Call `earnfi_human_review` (or `earnfi_human_action_create` with `action_type: review`) **without** `payment_signature` to receive a 402 quote.
3. Sign x402 USDC on the **Solana** rail for the quoted amount.
4. Retry the **same** tool with `payment_signature`.
5. Poll with `earnfi_human_action_result` using the returned `action_id` and `secret`.

Never mix OKX payment proofs into Solana Human Action tools.
