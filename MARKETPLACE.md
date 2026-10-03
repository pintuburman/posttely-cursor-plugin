# Cursor Marketplace submission

Posttely already hosts the MCP server and OAuth at `https://www.posttely.com/mcp`.
This repo is only the installable Cursor plugin wrapper.

## Checklist before submit

- [x] `.cursor-plugin/plugin.json` with unique kebab-case `name`: `posttely`
- [x] `mcp.json` points at `https://www.posttely.com/mcp`
- [x] README documents install + Authenticate flow
- [x] Logo committed at `assets/logo.svg` (1:1 plate)
- [x] Skills / rules / commands have valid frontmatter
- [x] MIT license
- [ ] Public GitHub repository created and pushed
- [ ] Local install tested via `~/.cursor/plugins/local/posttely`
- [ ] OAuth Authenticate completes in Cursor
- [ ] Publisher application submitted at https://cursor.com/marketplace/publish

## Create the public repo

This package currently lives inside the private Posttely Django monorepo at
`posttely-cursor-plugin/`. Marketplace review needs a **public** GitHub repo.

Suggested steps:

```bash
cd posttely-cursor-plugin
git init
git add .
git commit -m "Initial Posttely Cursor Marketplace plugin"
gh repo create pintuburman/posttely-cursor-plugin --public --source=. --remote=origin --push
```

If you prefer a different org/name, update:

- `.cursor-plugin/plugin.json` → `repository`
- this file’s example commands

## Submit to Cursor

1. Sign in at [cursor.com/marketplace/publish](https://cursor.com/marketplace/publish)
2. Fill publisher org / handle / contact email / logo URL
3. Paste the public repo URL: `https://github.com/pintuburman/posttely-cursor-plugin`
4. Submit Application (accepts Publisher Terms)
5. Wait for review email from `marketplace-publishing@cursor.com`

There is no published SLA. Listing exists only after Cursor approves it.

## After approval

- Users install from Marketplace and click Authenticate
- Every plugin update is re-reviewed, so keep `main` marketplace-ready

## Community listing (optional, faster)

You can also list on [cursor.directory](https://cursor.directory/plugins/new) while waiting for official review.
