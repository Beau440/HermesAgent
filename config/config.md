# Runtime Configuration

This file documents non-secret runtime settings. Keep tokens and passwords in
`.env` or your password manager.

## Main Model

- Active provider: OpenAI Codex
- Default model: gpt-5.5
- Previous model seen: gpt-5.3-codex
- Notes: The provider can still display as "OpenAI Codex" while the footer/status
  shows the actual active model, such as `gpt-5.5`.

## Model Commands

Run from a real terminal:

```bash
hermes setup model
hermes model
hermes config show
```

Do not type shell commands into a Hermes/Discord chat unless you are asking Hermes
to run them as a task.

## Channels

- Discord: enabled, confirm exact bot/app details in `config/channels.md`
- Telegram: optional, token goes in `.env` as `TELEGRAM_BOT_TOKEN`
- CLI/TUI: useful for deep work and debugging
- VS Code ACP: useful for repo work with diffs and approvals

## Behavior Toggles

- Self-improvement: document current setting here when confirmed
- Auto-run skills: keep conservative until the agent is trusted
- Permission mode: document whether the active surface asks, accepts edits, or runs
  unattended

## Integrations

Track integration setup in separate files:

- `config/channels.md`
- `config/credentials-map.md`
- `config/model-provider.md`
