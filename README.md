# Hermes Agent — Config & Knowledge Store

This repo stores everything about my personal **Hermes Agent** (Nous Research) — its
identity, skills, memory, scheduled automations, deployment notes, and secrets *template*.

It mirrors Hermes' own concepts so it doubles as **version-controlled documentation** and a
**backup** of the agent's configuration. Real secrets are never committed (see `.gitignore`).

> Based on Nate Herk's "Hermes Agent: Zero to Personal AI Assistant" course
> and the Hermes docs at https://hermes-agent.nousresearch.com/docs/

## Layout

| Folder         | What lives here |
|----------------|-----------------|
| `soul/`        | The agent's identity & personality (`SOUL.md`) |
| `skills/`      | One folder per skill, each with a `SKILL.md` |
| `memory/`      | Durable, human-readable memory notes the agent reads/writes |
| `crons/`       | Scheduled automation definitions (what runs, when, why) |
| `config/`      | Model, channel (Telegram), and runtime settings |
| `deployment/`  | VPS setup, install steps, recovery notes |
| `logs/`        | Run logs / journals (gitignored by default) |

## Quick start

1. Copy `.env.example` to `.env` and fill in your real keys (`.env` is gitignored).
2. Edit `soul/SOUL.md` to define who Hermes is for you.
3. Add skills under `skills/<skill-name>/SKILL.md`.
4. Record automations in `crons/`.
5. Commit your changes: `git add . && git commit -m "..."`.

## Installing Hermes itself (reference)

```bash
pip install hermes-agent
hermes postinstall   # optionally installs Node.js, browser, ripgrep, ffmpeg
hermes setup
```

This repo does **not** contain Hermes' code — it stores *your* configuration of it.
