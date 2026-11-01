# Outil.io

The `outil` MCP server operates one Outil.io project (the one chosen at sign-in, or the project of the API key).

- Start with `describe_resources`, then `list_records` / `get_record` before any change. `update_record` needs the current `version`.
- Sending is real: `send_newsletter`, `send_sms`, `send_whatsapp` and `send_telegram` queue messages to consenting contacts only. Check with the user before sending.
- WhatsApp broadcasts need a template approved by Meta. Telegram only reaches contacts who opened their personal link (`get_telegram_invite_link`, or `{{telegram_link}}` in an email).
- Specialised servers expose fewer tools: https://outil.io/mcp/crm, /mcp/marketing, /mcp/commerce, /mcp/content, /mcp/learning, /mcp/automation.
- Answer the user in their language; the platform's own labels are French.
