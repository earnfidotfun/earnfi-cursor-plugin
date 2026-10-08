---
name: mcp-connect
description: >-
  Connect and troubleshoot EarnFi MCP (~135 tools). Use for setup, endpoint, stale tool list, smoke test, or "is EarnFi connected".
license: MIT
metadata:
  author: earnfi
  version: "1.1.0"
  homepage: https://github.com/earnfidotfun/earnfi-cursor-plugin
---

# EarnFi MCP

**Endpoint:** `https://app.earnfi.fun/mcp` (Streamable HTTP)

This plugin ships `.mcp.json` pointing at that URL. For a manual MCP config:

```json
{
  "mcpServers": {
    "earnfi": {
      "url": "https://app.earnfi.fun/mcp"
    }
  }
}
```

Prefer **MCP tools** over inventing REST paths. For intent → tool mapping, load the **mcp-router** skill.

Coverage includes: register/profile, pay-first job creates, marketplace hire (create+fund), orders, deals, open work, threads, reviews, receipts, OKX rail, and Equity Guard.

## Tool list out of date?

**Reload Plugin** does not always refresh the MCP session. After a server update:

1. **Settings → MCP → EarnFi → Restart** (or toggle off/on).
2. **Developer: Reload Window** if the UI still shows an old tool count.
3. Confirm in **MCP Logs** that a new `tools/list` ran.

Expect ~**135** tools, aligned with [server-card.json](https://app.earnfi.fun/.well-known/mcp/server-card.json).

## Verify connectivity

Use the **earnfi-smoke-test** command or ask the agent to call `earnfi_agent_catalog` and `earnfi_marketplace_stats` (free reads, no payment).
