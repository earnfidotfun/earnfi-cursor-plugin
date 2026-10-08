---
name: equity-guard
description: Tokenized equity safety — search assets, ALLOW/WARN/BLOCK trades, portfolio protection via equity_* MCP tools.
license: MIT
metadata:
  author: earnfi
  version: "1.0.0"
  homepage: https://github.com/earnfidotfun/earnfi-cursor-plugin
---

# Equity Guard

Programmable safety for tokenized equities on Solana. MCP tools call the Growl equity-guard API (free reads; trade checks persist receipts).

## Start here

1. **`equity_get_glossary`** — badge meanings, breaker states, decision labels, reason codes. Explain these to users before trading advice.
2. **`equity_search`** — registry; trust `guard_signal`, `price_confidence`, `onchain_price_trusted` for decisions (not raw diagnostic prices alone).

## Due diligence

- `equity_get_passport` — attested ticker → mint → issuer
- `equity_get_market_state` — NYSE session vs on-chain hours
- `equity_get_liquidity` — impact snapshot
- `equity_get_peg`, `equity_get_circuit_breaker`
- `equity_list_corporate_actions`

## Trade flow

1. `equity_preview_trade` or `equity_simulate_trade` — non-persisted what-if
2. `equity_authorize_trade` / `equity_check_trade` — ALLOW / WARN / BLOCK + `receipt_id`
3. Optional execution: `equity_prepare_execution` → user signs tx → `equity_confirm_execution`
4. `equity_verify_receipt`, `equity_export_receipt`

## Portfolio

- `equity_get_portfolio` — map wallet holdings to registry
- `equity_protect_portfolio` — exit check plan per holding

## Liquidity (advanced)

- `equity_meteora_pools`, `equity_meteora_claw_pools`, `equity_meteora_stock_pairs`

Agent API alias (SDK): `client.equity.*` on `@earn-fi/agent-client`. Prefer MCP tools when already connected.
