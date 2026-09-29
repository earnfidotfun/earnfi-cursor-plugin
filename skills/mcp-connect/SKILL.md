---
name: mcp-connect
description: Connect to EarnFi Work+Money MCP — Human Actions, marketplace, escrow deals, jobs, open work, x402, receipts, Equity Guard (~124 tools).
license: MIT
metadata:
  author: earnfi
  version: "1.0.0"
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
