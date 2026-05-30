# Channels

Document the surfaces where Hermes can talk to you. Keep actual tokens in `.env`
or a password manager.

## Discord

- Status: active
- Bot/app name: _fill in_
- Server/guild: _fill in_
- Allowed users/roles: _fill in_
- Token location: `.env` as `DISCORD_BOT_TOKEN`
- Notes:
  - If Discord says "I am Codex based on GPT-5", that can be normal provider
    identity text. Check the Hermes session footer or config for the exact model.

## Telegram

- Status: optional
- Bot username: _fill in_
- Allowed user IDs: `.env` as `TELEGRAM_ALLOWED_USER_IDS`
- Token location: `.env` as `TELEGRAM_BOT_TOKEN`

## CLI / Terminal

- Best for setup, model switching, config checks, and deep debugging.
- Shell commands must be run in the terminal, not typed as normal chat messages.

## VS Code

- Best for editing this repo, reviewing diffs, and using an ACP agent panel.
- Health check:

```bash
hermes acp --check
```

Manual ACP command if needed:

```bash
hermes acp
```
