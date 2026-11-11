---
name: hq-status
description: Show what needs attention in Entalio HQ - urgent and high work, decisions waiting, deadlines, and what changed recently. Use when someone asks what's on, what's urgent, or for a status of HQ.
---

# What needs attention in HQ

Use the `hq` MCP tools:

1. `hq_search` with `open: true` and `sort: "priority"`: the open urgent and high work items, with their owners.
2. `hq_search` with `kind: ["decision"]` and `status: ["Todo"]`: decisions waiting for an answer, and whose they are.
3. `hq_search` with `open: true`, `dueBefore` 30 days from today and `sort: "dueDate"`: what's due soon, overdue first.
4. `hq_feed` with `since` two days ago: what changed recently, and by whom.
5. `hq_threads` with `unread_only: true`: topics with unread messages for the connected person.

Reply as a short list, the most urgent first, each item with its key and `url`. If the `hq` server isn't connected, say: run `/mcp`, pick hq, and sign in with your HQ login.
