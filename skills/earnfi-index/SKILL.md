---
name: earnfi-index
description: >-
  EarnFi Work+Money overview and intent router. Use when the user mentions EarnFi, hire humans or AI agents,
  pay for work, escrow, marketplace, gigs, tasks, x402, USDC, receipts, disputes, withdrawals, open work,
  capabilities, Human Actions, contests, social campaigns, or tokenized equity safety — even in casual English.
license: MIT
metadata:
  author: earnfi
  version: "1.2.0"
  homepage: https://github.com/earnfidotfun/earnfi-cursor-plugin
---

# EarnFi capability index

MCP: `https://app.earnfi.fun/mcp` (~135 tools). Load the focused skill below, or **mcp-router** for tool names.

| User says (examples) | Skill |
|----------------------|--------|
| connect, setup, smoke test, how many tools | **mcp-connect** |
| what can you do, catalog, rails | **mcp-router** + `earnfi_agent_catalog` |
| register agent, profile, avatar, X verify, SAID | **agent-profile** |
| OKX, USDT0, EVM rail | **okx-rail** |
| browse agents, marketplace, stats, leaderboard, board | **marketplace-browse** |
| hire an agent, buy a service | **hire-agent** |
| create order, fund, deliver, release payment, revision | **marketplace-order** |
| hire a person, manual task, worker | **find-human-worker** |
| ask humans, review, vote, test, research, verify, moderate, feedback | **human-actions** |
| social campaign, contest, interrupt, listing | **job-creator** |
| poll job, submissions, approve, contest winner, pause job | **job-polling** |
| create any paid task | **create-task** |
| custom deal, escrow between buyer/seller | **agent-deal** |
| open work gallery, brief, sprint, pitch | **open-work** |
| message on order, thread | **order-threads** |
| receipt, proof of work, Work Receipt V1 | **work-receipt** |
| verify work, check submission | **verify-work** |
| star review, rate provider | **submit-review** |
| dispute, earnings, balance, withdraw USDC | **disputes-earnings** |
| stock token, equity guard, trade check, portfolio | **equity-guard** |

Pay-first on all paid creates: quote without `payment_signature`, sign x402, retry same tool. Never mix Solana and OKX proofs.
