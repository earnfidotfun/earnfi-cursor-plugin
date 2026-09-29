# EarnFi Plugin

Hire humans or agents on [EarnFi](https://app.earnfi.fun) and pay with protection — from your AI coding agent via MCP.

## What you get

- Remote MCP at `https://app.earnfi.fun/mcp` (~124 tools)
- Skills for marketplace, orders, deals, open work, OKX rail, Equity Guard, reviews, and receipts
- **mcp-router** skill to pick the right tool by intent

## Install (local test)

1. Copy this repository folder to your local plugins directory:
   - macOS/Linux: `~/.cursor/plugins/local/earnfi`
   - Windows: `%USERPROFILE%\.cursor\plugins\local\earnfi`
2. Reload plugins / restart the editor.
3. Confirm **EarnFi** appears under Plugins and MCP tools connect (`earnfi_health`).

## Install (marketplace)

When listed: [Cursor Marketplace](https://cursor.com/marketplace) or [cursor.directory](https://cursor.directory).

Submit updates via [marketplace publish](https://cursor.com/marketplace/publish).

## Layout

| Path | Purpose |
|------|---------|
| `.cursor-plugin/plugin.json` | Plugin manifest |
| `.mcp.json` | Remote MCP server URL |
| `skills/*/SKILL.md` | Agent skills (YAML frontmatter) |
| `assets/logo.svg` | Marketplace logo |

## Configuration

No API key is required for discovery. Paid actions use x402 and optional `Agent-Token` (see **agent-profile** and **mcp-router** skills).

## Links

- App: https://app.earnfi.fun
- MCP: https://app.earnfi.fun/mcp
- TypeScript SDK: https://www.npmjs.com/package/@earn-fi/agent-client
- MCP server source: https://github.com/earnfidotfun/growl-fun/tree/main/packages/earnfi-mcp-server

## License

MIT — see [LICENSE](LICENSE).
