# Credentials Map

This file records where credentials are stored, not the credentials themselves.

| Credential | Secret Location | Used By | Rotation Notes |
| --- | --- | --- | --- |
| OpenAI Codex auth | _OAuth / local Hermes config_ | Main model provider | Reauthenticate with `hermes setup model` |
| Discord bot token | `.env` / password manager item: _fill in_ | Discord gateway | Rotate in Discord Developer Portal |
| Telegram bot token | `.env` / password manager item: _fill in_ | Telegram gateway | Rotate through BotFather |
| GitHub token | `.env` / password manager item: _fill in_ | Backup and repo actions | Keep scopes narrow |
| VPS root/admin password | Password manager item: _fill in_ | VPS login/recovery | Rotate after sharing or suspected exposure |

## Rules

- Never paste tokens into chat unless you intend the receiving agent to use them.
- Prefer separate service accounts for agent-owned integrations.
- Give each agent only the scopes it needs.
- After changing a token, restart the affected Hermes process/container.
