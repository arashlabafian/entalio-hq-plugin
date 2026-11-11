---
name: hq
description: How to work in Entalio HQ through its MCP tools (hq_*). Use whenever a task reads or changes HQ - work items, decisions, pages, the CRM, files, therapists, clients or Messages - or when someone asks what's going on at Entalio.
---

# Working in Entalio HQ

HQ is Entalio's internal app: work items (tasks, issues, risks and decisions), pages, the CRM, files, costs, therapists and client codes. Its MCP server is `hq`; the first time, run `/mcp`, pick hq, and sign in with your HQ login. You choose there what the connection may do (read only, or read and write; clients and private files only from an app on your own computer).

## You act as the person who connected
Everything you change shows under their name, is logged in Activity and can be undone (`hq_feed`, `hq_undo`). Never write "Claude did..." in a comment, and never assign work to Claude: owners and delegates are people (`hq_people`).

## Rules
- **Ask before creating a work item.** Show the person its exact title, description and owner, and call `hq_create` only after their yes. Status changes and comments on existing items don't need asking.
- **Messages are the person's own words.** Post, reply, react or start a topic only when they tell you to, or after they approved the exact text. Something needed from someone else is a task they own, not a message.
- **Comments are not messages.** Progress on an item goes on the item (`hq_comment`); `hq_message_post` is for talking to someone.
- **Decisions** are work items of kind `decision`: the question and the choices in plain short text, the recommended one first. Record the owner's answer with `hq_decide` only when they said it.
- **Clients** have codes (CL-n). Their questionnaire answers are for matching only: never change them, and never write notes about a client's wellbeing anywhere. No client names in pages or messages.
- **Links:** every record in a result has `url`. Give that link when you mention an item.
- You can't delete, send email or undo someone else's create through MCP.

## Where to start
- Find things: `hq_search` (filters by type, status, owner, project, due), then `hq_get` for one record with its links and comments.
- Change things: `hq_update` (status: Backlog, Todo, In progress, In review, Done), `hq_comment`, `hq_link`.
- What happened: `hq_feed`. Who's who and the project keys: `hq_people`.
- Pages: see the `hq-pages` skill. What needs attention: the `hq-status` skill.
