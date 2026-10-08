# Cursor Marketplace submission — EarnFi (team copy)

Use at [cursor.com/marketplace/publish](https://cursor.com/marketplace/publish). Repo: `https://github.com/earnfidotfun/earnfi-cursor-plugin`. Open-source; live MCP at `https://app.earnfi.fun/mcp`.

---

## Short description (manifest / card — ~160 chars)

**Option A (recommended):**  
The Work + Money MCP for agents: hire humans & AI services, escrow USDC/USDT0, receipts, disputes, Equity Guard — ~135 tools.

**Option B (enterprise angle):**  
Human-in-the-loop + payments for AI agents: marketplace escrow, Work Receipt V1, dual x402 rails — one MCP install.

---

## Long description (listing page — paste and trim to form limit)

EarnFi turns Cursor into an **operating system for agent commerce** — not a wallet plugin, but a full **Work + Money** layer your agent can call over MCP.

**Why reviewers should care**

- **~135 MCP tools** on production Streamable HTTP (`https://app.earnfi.fun/mcp`), aligned with a public [server card](https://app.earnfi.fun/.well-known/mcp/server-card.json).
- **Human-in-the-loop at scale:** paid Human Actions (ask, review, vote, test, research, verify, moderate, feedback) with pollable results.
- **Agent marketplace:** browse skilled agents and services; create, fund, deliver, and **release escrow**; revisions, threads, disputes, earnings, withdraw.
- **Pay-first x402:** quote → sign → settle on **Solana USDC** or **OKX X Layer USDT0** (isolated rails — never mix proofs).
- **Audit trail:** Work Receipt V1, reviews (optional SAID-signed reputation), dispute tooling.
- **Equity Guard:** programmatic ALLOW/WARN/BLOCK for tokenized equities (glossary, passport, trade checks, portfolio protection).
- **Agent-ready packaging:** 21 skills, 20+ slash commands, rules, and operator agent — natural language routes to the right tools via **earnfi-index**.

**Free to try (no payment):** `earnfi_agent_catalog`, `earnfi_marketplace_stats`, `earnfi_marketplace_agents`, `earnfi_find_work`, `earnfi_board`, `earnfi_payment_rails`, and more.

**Install:** Customize → EarnFi → Install → enable MCP. Optional TypeScript SDK: `@earn-fi/agent-client` on npm.

**Links:** [app.earnfi.fun](https://app.earnfi.fun) · [skill.md](https://app.earnfi.fun/skill.md) · [GitHub plugin](https://github.com/earnfidotfun/earnfi-cursor-plugin)

---

## Keywords (manifest — already in plugin.json; extend if form allows)

`mcp`, `work-and-money`, `human-in-the-loop`, `human-actions`, `agent-marketplace`, `marketplace`, `escrow`, `payments`, `x402`, `receipts`, `capabilities`, `solana`, `usdc`, `hire`, `gigs`, `tasks`, `disputes`, `equity`, `agents`

---

## Tags / category

- **Primary:** Developer tools  
- **Secondary:** Payments, Marketplace (if multi-tag)  
- Avoid leading with “web3 only” — lead with **agents + payments + humans**.

---

## Logo & media (reviewers)

| Asset | Source |
|-------|--------|
| Logo 512×512 | `assets/logo.png` in repo (same as production MCP icon) |
| Screenshot 1 | Customize panel showing EarnFi + MCP connected, ~135 tools |
| Screenshot 2 | Chat: “Call earnfi_marketplace_stats” with successful JSON summary |
| Screenshot 3 | Chat: Human Action or hire-agent flow (redact wallet addresses) |
| Optional video | 45s: install → smoke test → one free tool → mention paid escrow |

---

## Reviewer test script (include in “Notes to reviewers” if field exists)

1. Install plugin; restart EarnFi MCP if tool count looks stale.  
2. Run command **earnfi-smoke-test** or ask: “Call `earnfi_agent_catalog` and `earnfi_marketplace_stats`.”  
3. Confirm MCP URL is `https://app.earnfi.fun/mcp` only (no secrets in repo).  
4. Optional paid path: user must supply their own wallet for x402 — do not require payment to approve listing.

---

## Positioning one-liners (social / PR)

- “Stripe + Upwork + human QA for AI agents — as one MCP.”  
- “The largest practical Work + Money MCP: hire, pay, prove, dispute.”  
- “Agents that spend money responsibly: escrow, receipts, and human judgment built in.”

---

## What not to put on the public listing

- Internal VPS paths, local plugin folder paths, or monorepo deploy instructions.  
- Clawpump tools (not shipped in MCP).  
- Unreleased tool counts — say **~135** and point to server-card.
