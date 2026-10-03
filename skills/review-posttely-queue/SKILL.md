---
name: review-posttely-queue
description: Review upcoming and recent Posttely posts. Use when the user asks what is scheduled, queued, or recently published.
---

# Review Posttely queue and recent posts

## When to use

- The user asks what posts are scheduled or upcoming
- The user wants a calendar view or recent publish history

## Steps

1. Confirm auth with `auth_me`.
2. Use `list_queue` for the next scheduled or queued items.
3. Use `list_calendar` with `YYYY-MM` when the user asks about a specific month.
4. Use `list_recent_posts` for publish history.
5. Summarize clearly: content preview, channels, status, and times.

## Notes

- Prefer the active workspace channels unless the user asks for all workspaces.
- If the queue is empty, say so and offer to draft or schedule a new post.
