# Runtime configuration (reference)

Document the non-secret settings of your Hermes deployment here. Real secrets go in `.env`.

## Model
- Provider: _<anthropic / openai / openrouter>_
- Model: _<e.g. claude-opus-4-8>_
- Fallback model: _<optional>_

## Channels
- Telegram: enabled? _<yes/no>_  — token in `.env` as `TELEGRAM_BOT_TOKEN`
- Allowed users: _<who can message the agent>_

## Behavior toggles
- Self-improvement: _<on/off>_
- Auto-run skills without confirmation: _<off recommended>_
