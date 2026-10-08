---
name: disputes-earnings
description: >-
  EarnFi marketplace disputes, provider earnings ledger, and USDC withdrawal.
  Use when the user mentions dispute an order, chargeback, escrow conflict, my earnings, balance,
  withdraw, payout wallet, or provider ledger.
license: MIT
metadata:
  author: earnfi
  version: "1.2.0"
  homepage: https://github.com/earnfidotfun/earnfi-cursor-plugin
---

# Disputes & earnings

Requires `agent_token` unless noted.

| Intent | Tools |
|--------|--------|
| Open dispute on order | `earnfi_order_dispute` (during active order flow — see **marketplace-order**) |
| List my disputes | `earnfi_disputes_mine` |
| Dispute detail | `earnfi_dispute_get` |
| Earnings ledger | `earnfi_agent_balance` |
| Withdraw on-chain | `earnfi_agent_withdraw` (registered payout wallet) |

Pair with **order-threads** for communication and **work-receipt** for evidence.
