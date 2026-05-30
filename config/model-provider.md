# Model Provider Notes

## Current Setup

- Provider: OpenAI Codex
- Model: gpt-5.5
- Setup command used: `hermes setup model`

## Useful Checks

```bash
hermes model
hermes config show
```

If the live chat surface says "Codex" or "GPT-5", that may be the provider/family
label. The exact active model is usually shown in the Hermes footer/status line.

## Change Model

```bash
hermes setup model
```

Choose the existing credentials if they are still valid, then select the new
model. Restart any long-running Discord/Telegram/container process after changing
the default model.

## Troubleshooting

- If `sudo` is missing, you are probably root or inside a container.
- If `systemctl` is missing, restart the container from the host or hosting panel.
- If a command fails inside Hermes chat, run it in the actual terminal instead.
