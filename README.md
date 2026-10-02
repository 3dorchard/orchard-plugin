# Orchard plugin

Connects your coding agent to [Orchard](https://3dorchard.com), a browser-based parametric CAD platform. Your agent plans a part, builds it in your own open Orchard editor tab while you watch, checks it against the plan, and saves it to your Orchard account.

The plugin contains one thing: the address of Orchard's hosted MCP server, `https://mcp.3dorchard.com/mcp`. It runs no code on your machine.

## Install

**Claude Code**

```
/plugin marketplace add 3dorchard/orchard-plugin
/plugin install orchard@3dorchard
```

Then run `/mcp`, choose `orchard`, and sign in with your Orchard account.

**Grok Build**

Install `orchard` from the plugin marketplace, then sign in when prompted.

**Any other MCP client**

Add a remote (Streamable HTTP) MCP server with the URL `https://mcp.3dorchard.com/mcp`. Sign-in is OAuth; the client registers itself.

## Use

1. Open an editor tab and keep it open: https://3dorchard.com/editor/new?connect=mcp
2. Ask your agent for a part, for example "a 60×40×5 mm mounting plate with four M3 holes, saved as a draft".

Your agent works only in your tab, under your account. By default its saves are private drafts you can publish from the editor; you can change that in Orchard's settings for your AI app.

## Network and data

- Endpoint: `https://mcp.3dorchard.com` (MCP + OAuth). Your editor tab connects to the same server.
- Credentials: an OAuth token issued by Orchard after you sign in. No API keys, nothing read from your machine.
- Privacy policy: https://3dorchard.com/privacy · Terms: https://3dorchard.com/terms
- Support: support@3dorchard.com

## License

MIT
