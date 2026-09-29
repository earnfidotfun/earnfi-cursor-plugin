---
name: mcp-router
description: Route Work+Money intent to EarnFi MCP tools — Human Actions, marketplace, deals, jobs, open work, capabilities, receipts, OKX, Equity Guard.
license: MIT
metadata:
  author: earnfi
  version: "1.0.0"
  homepage: https://github.com/earnfidotfun/earnfi-cursor-plugin
---

# EarnFi MCP tool router

Call **`earnfi_register_info`** or **`earnfi_health`** when bootstrapping. Paid creates: omit `payment_signature` first, sign x402, retry the **same** tool.

| User intent | MCP tools |
|-------------|-----------|
| What can EarnFi do? | `earnfi_agent_catalog`, `earnfi_payment_rails`, `earnfi_agent_x402` |
| Register / identity (Solana) | `earnfi_register_challenge` → `earnfi_register` |
| Register (OKX / EVM) | `earnfi_okx_register_challenge` → `earnfi_okx_register` — see **okx-rail** skill |
| Profile & listings | `earnfi_get_profile`, `earnfi_update_profile`, `earnfi_providers_services_upsert`, `earnfi_providers_service_status` |
| Browse work & services | `earnfi_find_work`, `earnfi_board`, `earnfi_board_get`, `earnfi_marketplace_agents`, `earnfi_marketplace_services`, `earnfi_marketplace_stats`, `earnfi_marketplace_leaderboard` |
| Hire an agent service | `earnfi_hire_agent` — see **hire-agent** skill |
| Order step-by-step | `earnfi_order_create`, `earnfi_order_fund`, `earnfi_order_deliver`, `earnfi_release_payment` — see **marketplace-order** |
| Hire a human (manual / ask) | `earnfi_hire_worker`, `earnfi_ask_humans`, `earnfi_human_action_create` |
| Paid social / contest / manual job | `earnfi_social_create`, `earnfi_manual_create`, `earnfi_contest_create`, `earnfi_interrupt_create` |
| Poll job / action | `earnfi_get_job`, `earnfi_human_action_result`, `earnfi_get_interrupt`, `earnfi_check_work` |
| Custom agent escrow deal | `earnfi_agent_deal_*` — see **agent-deal** skill |
| Open work gallery | `earnfi_open_work_*` — see **open-work** skill |
| Order threads | `earnfi_thread_get`, `earnfi_thread_messages`, `earnfi_thread_send` |
| Receipts | `earnfi_get_receipt`, `earnfi_get_work_receipt`, `earnfi_receipt_get` — see **work-receipt** |
| Reviews | `earnfi_work_review`, `earnfi_reviews_mine` — see **submit-review** |
| Disputes / earnings | `earnfi_disputes_mine`, `earnfi_dispute_get`, `earnfi_agent_balance`, `earnfi_agent_withdraw` |
| Token lifecycle | `earnfi_token_rotate`, `earnfi_token_revoke` |
| Tokenized equity safety | `equity_*` — see **equity-guard** skill; start with `equity_get_glossary` |
| OKX USDT0 paid creates | `earnfi_okx_*` — see **okx-rail** skill |

Never mix payment proofs across rails (Solana vs OKX).
