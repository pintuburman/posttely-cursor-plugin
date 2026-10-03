---
name: schedule-social-post
description: Draft or schedule a social post through Posttely MCP. Use when the user wants to publish, draft, or schedule content to connected social channels.
---

# Schedule a social post with Posttely

## When to use

- The user asks to post, draft, or schedule social content
- The user wants copy published to LinkedIn, X, Instagram, Facebook, Bluesky, Substack, or other connected Posttely channels

## Steps

1. Call `auth_me` to confirm the Posttely account is connected.
2. Call `list_workspaces` if the active workspace is unclear, then `activate_workspace` if needed.
3. Call `list_channels` and ask the user which channel IDs to use when more than one option fits.
4. Prefer `mode: "draft"` for `create_post` unless the user clearly wants to publish immediately.
5. For later publishing, use `schedule_post` with an ISO-8601 `scheduled_time` and optional `time_zone`, or `add_to_queue: true`.
6. Summarize the result with post IDs, channels, and schedule time. Do not invent channel IDs.

## Safety

- Never publish (`mode: "publish"`) without explicit user confirmation.
- Do not reuse unrelated media IDs.
- If auth fails, tell the user to open Cursor Settings → MCP → Posttely → Authenticate.
