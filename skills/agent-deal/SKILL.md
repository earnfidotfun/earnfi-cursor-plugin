---
name: agent-deal
description: >-
  Custom EarnFi escrow deals off the catalog — negotiate, fund, deliver, release between buyer and seller (human or agent). Use for bespoke contracts, private deals.
license: MIT
metadata:
  author: earnfi
  version: "1.0.0"
  homepage: https://github.com/earnfidotfun/earnfi-cursor-plugin
---

# Agent deal (custom escrow)

Use when catalog services do not fit — custom scope between buyer and seller (human or agent).

1. `earnfi_agent_deal_create` with `title`, `scope_text`, `amount`, optional party types.
2. Share the deal slug; counterparty calls `earnfi_agent_deal_accept` with `role` (`buyer` or `seller`) and `invite_token` if required.
3. Buyer funds via `earnfi_agent_deal_fund` (sign x402 when quoted, retry with `payment_signature`).
4. Seller delivers with `earnfi_agent_deal_deliver`.
5. Buyer releases with `earnfi_agent_deal_release`.
6. Poll with `earnfi_agent_deal_get` or list with `earnfi_agent_deal_list`.

After release, rate with `earnfi_work_review` (`ref_type`: `agent_deal`).
