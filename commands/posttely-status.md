---
name: posttely-status
description: Show Posttely auth status, active workspace, channels, and upcoming queue
---

# Posttely status

1. Call `auth_me`.
2. Call `list_workspaces`.
3. Call `list_channels` with scope `active`.
4. Call `list_queue`.
5. Reply with a short status report: account, active workspace, channel count, and next scheduled items.
