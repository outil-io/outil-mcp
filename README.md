# Outil.io MCP server

[Outil.io](https://outil.io) is an all-in-one marketing platform for entrepreneurs: website builder, sales funnels, CRM, email campaigns, SMS, WhatsApp, Telegram, automations, online courses, shop and payments, bookings, webinars and affiliation.

Its remote MCP server lets an AI assistant operate your project with the same actions and controls as the interface.

- **URL:** `https://outil.io/mcp` (Streamable HTTP). Smaller tool sets: `/mcp/crm`, `/mcp/marketing`, `/mcp/commerce`, `/mcp/content`, `/mcp/learning`, `/mcp/automation`.
- **Authentication:** OAuth 2.1 (sign in to Outil, choose the project and access level), or an API key `Authorization: Bearer outil_…` created in Paramètres → API & MCP.
- **Guide (French):** https://outil.io/serveur-mcp

## Install

| Client | How |
| --- | --- |
| Claude (claude.ai, Desktop) | Settings → Connectors → Add custom connector → `https://outil.io/mcp` |
| Claude Code | `claude mcp add --transport http outil https://outil.io/mcp`, or `/plugin marketplace add outil-io/outil-mcp` then `/plugin install outil@outil` |
| ChatGPT | Settings → Apps & Connectors → Create (developer mode) → `https://outil.io/mcp`, OAuth |
| Gemini CLI | `gemini extensions install https://github.com/outil-io/outil-mcp` |
| Cursor / VS Code | Add `{"url": "https://outil.io/mcp"}` as an MCP server |
| API key clients | `{"type": "http", "url": "https://outil.io/mcp", "headers": {"Authorization": "Bearer outil_…"}}` |

## Safety

Every tool respects the role granted (viewer, editor, admin, owner), consent per channel (email, SMS, WhatsApp, Telegram) and record versions. Read-only tools are annotated `readOnlyHint`; deletions `destructiveHint`; tools that send messages or charge payments `openWorldHint`. Access can be revoked at any time in Paramètres → API & MCP.

## Legal

Published by REPHI CONSULTING SAS — [legal notice](https://outil.io/mentions-legales), [privacy](https://outil.io/confidentialite), [terms](https://outil.io/conditions). Contact: contact@outil.io. The files in this repository are MIT-licensed; the Outil.io service is subject to its terms.
