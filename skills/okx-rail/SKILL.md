---
name: okx-rail
description: >-
  EarnFi OKX X Layer USDT0 rail — register EVM wallet, okx human actions, okx job creates. Use for USDT0, X Layer, EVM x402 — never mix with Solana proofs.
license: MIT
metadata:
  author: earnfi
  version: "1.0.0"
  homepage: https://github.com/earnfidotfun/earnfi-cursor-plugin
---

# OKX rail (USDT0)

Rails are **URL-bound**. Never send Solana `signed_tx` to OKX tools or EVM payment payloads to Solana tools.

## Discovery

- `earnfi_payment_rails` — lists `okx-xlayer-usdt0` vs default Solana rail
- `earnfi_okx_catalog`, `earnfi_okx_info`, `earnfi_okx_health` — OKX rail discovery (see `earnfi_payment_rails` for base URLs)

## Registration (optional before pay)

1. `earnfi_okx_register_challenge` — EVM `0x` address
2. Sign EIP-191 message
3. `earnfi_okx_register` → `agent_token`

Pay-first still works: first paid OKX create can bind identity from the paying wallet.

## Paid creates (two-step)

Same pattern as Solana: omit `payment_signature` → 402 quote → sign **EVM x402 (EIP-3009 USDT0)** → retry **same tool** with `payment_signature`.

Tools include:

- `earnfi_okx_social_create`, `earnfi_okx_manual_create`, `earnfi_okx_contest_create`, `earnfi_okx_interrupt_create`
- `earnfi_okx_ask_humans`, `earnfi_okx_human_action_create`
- Convenience: `earnfi_okx_human_review`, `_vote`, `_test`, `_research`, `_verify`, `_moderate`, `_feedback`

Poll human actions with `earnfi_human_action_result` (Solana path) only when the action id is on the default rail — for OKX-created actions, use the action id returned on the OKX create response and the OKX result route documented in `earnfi_okx_info`.
