---
name: earnfi-smoke-test
description: Verify EarnFi MCP connectivity with free read-only tools.
---

# EarnFi MCP smoke test

Confirm EarnFi MCP is connected, then call:

1. `earnfi_agent_catalog`
2. `earnfi_marketplace_stats`
3. `earnfi_marketplace_agents` (limit results in your summary)
4. `earnfi_payment_rails`

Report success or the first error payload. If the tool count in Cursor UI looks stale, restart the EarnFi MCP server in Settings → MCP.
