# Shade MCP

Shade MCP connects AI assistants to the creative assets in your Shade workspace.
It can search and browse drives, inspect assets and transcripts, manage files and
metadata, curate collections and views, add comments, create share links, work
with custom objects, and manage automations.

## Connect

The production Streamable HTTP endpoint is:

```text
https://mcp.shade.inc/mcp
```

Shade uses OAuth. Your MCP client opens Shade sign-in when you connect.

Watch the [production MCP reviewer walkthrough](https://github.com/shade-labs/shade-mcp/releases/download/reviewer-demo-2026-07-13/shade-mcp-reviewer-demo.mp4) for a concise connection, search, asset-inspection, preview, and safety demo.

### Cursor

Install the Shade plugin from the Cursor Marketplace, or add this to
`~/.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "shade": {
      "url": "https://mcp.shade.inc/mcp"
    }
  }
}
```

### Codex

The marketplace-ready Codex package is in [`plugins/shade`](./plugins/shade) and depends on the reviewed Shade app. For a direct custom connection, add this to `~/.codex/config.toml`:

```toml
[mcp_servers.shade]
url = "https://mcp.shade.inc/mcp"
```

Then run:

```sh
codex mcp login shade
```

### Claude

Open **Settings → Connectors → Add custom connector**, name it **Shade**, and
enter `https://mcp.shade.inc/mcp`.

### GitHub Copilot CLI

```sh
copilot mcp add --transport http shade https://mcp.shade.inc/mcp
```

### ChatGPT

In ChatGPT settings, enable Developer mode under Connectors, create a connector
named **Shade**, and use `https://mcp.shade.inc/mcp`.

## Example prompts

- “Find five clips showing a person eating pizza.”
- “Summarize this video and show representative preview frames.”
- “Browse the project folder and identify the latest graded exports.”
- “Show the configured approval metadata and the value on this asset.”
- “Create a review collection and add these selected assets.”

## Security and privacy

Shade MCP only accesses workspaces and drives available to the authenticated
Shade user. Mutating tools require the host's normal approval flow. See the
[Shade Privacy Policy](https://shade.inc/legal/privacy-policy),
[Terms of Service](https://shade.inc/legal/terms-of-service), and
[security and legal overview](https://shade.inc/legal).

For help, visit the [Shade Help Center](https://academy.shade.inc/help-center).
