# Posttely for Cursor

Connect Cursor to [Posttely](https://www.posttely.com) so the agent can draft, schedule, and review social posts through the official hosted MCP server.

This repository is the **Cursor Marketplace plugin package**. The MCP API itself is hosted at:

```text
https://www.posttely.com/mcp
```

Auth uses Posttely OAuth 2.1 (PKCE). No API key is stored in the plugin.

## What you get

After install + Authenticate, Cursor can use Posttely tools such as:

- `auth_me` / `auth_logout`
- `list_workspaces` / `activate_workspace`
- `list_channels`
- `create_post` (draft or publish)
- `schedule_post`
- `list_queue` / `list_recent_posts` / `list_calendar`
- `generate_caption`

The plugin also ships skills, a rule, and a `/posttely-status` command.

## Install from Marketplace (after approval)

1. Open Cursor → **Customize** / Marketplace
2. Search for **Posttely**
3. Install the plugin
4. Open **Settings → MCP → Posttely → Authenticate**
5. Sign in to Posttely in the browser and allow access

Setup guide: [https://www.posttely.com/mcp-setup/](https://www.posttely.com/mcp-setup/)

## Local test (before Marketplace)

From this plugin directory:

```bash
mkdir -p ~/.cursor/plugins/local
ln -sfn "$(pwd)" ~/.cursor/plugins/local/posttely
```

Then restart Cursor, open **Settings → MCP**, find **posttely**, and click **Authenticate**.

Or add the same URL-only MCP config manually:

```json
{
  "mcpServers": {
    "posttely": {
      "url": "https://www.posttely.com/mcp"
    }
  }
}
```

## Package layout

```text
posttely-cursor-plugin/
├── .cursor-plugin/plugin.json
├── mcp.json
├── assets/logo.svg
├── skills/
├── rules/
├── commands/
├── LICENSE
└── README.md
```

## Marketplace submission

See [MARKETPLACE.md](./MARKETPLACE.md).

## Support

- Product: [https://www.posttely.com](https://www.posttely.com)
- MCP setup: [https://www.posttely.com/mcp-setup/](https://www.posttely.com/mcp-setup/)
- Email: support@posttely.com

## License

MIT
