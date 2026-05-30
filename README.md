# Hermes Agent Command Center

This repo is the control room for Beau's Hermes agent: identity, memory, skills,
cron registry, VPS notes, model/provider settings, and recovery steps.

It is meant to work like the project shown in the Hermes setup video: one VS Code
workspace where you can see the agent's long-term context, document how it is
deployed, track scheduled jobs, and keep a safe GitHub backup without committing
secrets.

Real credentials belong in `.env` or a password manager. Do not commit them.

## Start Here

1. Open `hermes-agent.code-workspace` in VS Code.
2. Fill in non-secret details in `AGENT_INDEX.md`.
3. Copy `.env.example` to `.env` and fill secrets locally only.
4. Update `soul/SOUL.md` with the agent's identity and boundaries.
5. Record durable facts in `memory/`.
6. Add reusable procedures in `skills/`.
7. Register scheduled tasks in `crons/`.
8. Keep deployment/recovery notes in `deployment/`.

## Layout

| Path | Purpose |
| --- | --- |
| `AGENT_INDEX.md` | One-page dashboard for the agent and VPS |
| `soul/SOUL.md` | Hermes' identity, voice, rules, and boundaries |
| `memory/` | Long-term context the agent should preserve |
| `skills/` | Reusable playbooks and procedures |
| `crons/` | Human-readable registry of scheduled automations |
| `config/` | Provider, model, channel, and integration notes |
| `deployment/` | VPS, Docker, service, backup, and recovery notes |
| `logs/` | Local run notes and troubleshooting logs, gitignored |

## Common Commands

Run these in a normal terminal, not inside a Hermes chat message.

```bash
hermes setup
hermes setup model
hermes model
hermes config show
hermes acp --check
```

If the agent runs in Docker on the VPS:

```bash
docker ps
docker compose restart
docker logs -f <container>
```

If it runs as a regular service on the VPS:

```bash
systemctl status hermes
systemctl restart hermes
journalctl -u hermes -f
```

Some hosted containers do not include `sudo` or `systemctl`. In that case, restart
the container from the VPS host panel or with `docker restart <container>`.

## Safety Rules

- Never commit `.env`, API keys, passwords, OAuth tokens, private keys, or bot tokens.
- Store only references to credentials here, such as "1Password item: Hermes VPS".
- Confirm before spending money, sending messages, deleting data, or changing DNS.
- Keep GitHub tokens scoped as narrowly as possible.
- Prefer one Hermes agent per role/container when the memory, tools, or secrets differ.

## Backup Flow

Use GitHub for the safe parts of the agent:

```bash
git status
git add .
git commit -m "Update Hermes agent command center"
git push
```

Before pushing, inspect changes and verify `.env` is not staged:

```bash
git diff --cached --stat
git status --short
```
