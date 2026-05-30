# Backup Runbook

Use this to keep the safe parts of Hermes backed up to GitHub.

## What To Back Up

- `soul/`
- `memory/`
- `skills/`
- `crons/`
- `config/`
- `deployment/`
- `README.md`
- `AGENT_INDEX.md`

## What Not To Back Up

- `.env`
- API keys
- OAuth tokens
- Bot tokens
- Private SSH keys
- VPS passwords
- Raw logs containing secrets

## Manual Backup

```bash
git status
git diff
git add .
git status --short
git commit -m "Update Hermes agent notes"
git push
```

Before committing, verify `.env` is not staged.

## Nightly Backup Idea

Create a Hermes cron that checks for safe changes and pushes them once per night.
The cron should refuse to run if `.env` or secret-looking files are staged.
