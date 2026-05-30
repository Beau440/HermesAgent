---
name: safe-github-backup
description: Use when backing up Hermes memory, skills, crons, soul, config notes, or deployment docs to GitHub.
---

# Safe GitHub Backup

## When To Use

Use this before committing or pushing this Hermes command center repo.

## Steps

1. Run `git status --short`.
2. Inspect changed files.
3. Refuse to continue if `.env`, keys, tokens, passwords, or secret-looking files
   are staged.
4. Run `git diff --stat` and summarize the intended backup.
5. Commit with a clear message.
6. Push to the configured remote.
7. Notify Beau with what changed and whether the push succeeded.

## Secret Checks

Stop and ask if any changed file matches:

- `.env`
- `*.key`
- `*.pem`
- `*secret*`
- `*private*`
- `credentials*.json`

## Notes

- The goal is to back up durable non-secret context, not runtime credentials.
- If there is no remote configured, document that in `deployment/backup-runbook.md`.
