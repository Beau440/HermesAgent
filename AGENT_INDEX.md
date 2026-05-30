Agent: Open Codex
# Hermes Agent Index

Use this as the first file to open when you want to understand or update the
agent.

## Current Agent

- Name: Hermes
- Owner: Beau
- Primary role: Personal AI assistant
- Main workspace: `C:\Users\BeauB\hermes-agent`
- VPS role: Runs the live Hermes agent and chat integrations
- Current provider: OpenAI Codex
- Current model: gpt-5.5

## Where Things Live

| Thing | Location |
| --- | --- |
| Agent identity | `soul/SOUL.md` |
| Stable personal context | `memory/about-me.md` |
| Project context | `memory/projects.md` |
| Decisions and rationale | `memory/decisions.md` |
| Skills | `skills/` |
| Scheduled jobs | `crons/` |
| Runtime settings | `config/` |
| VPS instructions | `deployment/` |

## Daily Operating Loop

1. Capture useful new facts in `memory/`.
2. Turn repeated procedures into `skills/<name>/SKILL.md`.
3. Register scheduled tasks in `crons/`.
4. Keep `deployment/` current after VPS changes.
5. Commit safe changes to GitHub.

## Core Personal Skills

- YouTube summaries: `skills/youtube-summarizer/`
- Web research: `skills/web-research/`
- X/Twitter post digests: `skills/x-post-digest/`
- Market briefings: `skills/market-brief/`
- Memory cleanup: `skills/memory-librarian/`
- Discord/chat operations: `skills/discord-operator/`
- VPS triage: `skills/vps-triage/`
- Safe GitHub backup: `skills/safe-github-backup/`

## Quick Health Check

```bash
hermes config show
hermes model
docker ps
git status
```

## Open Questions

- What is the exact VPS provider and dashboard URL?
- Is the live Hermes process Docker, host-level install, or managed one-click app?
- Which Discord bot/app owns the live agent?
- Where are credentials stored: 1Password, browser vault, VPS panel, or another vault?
- Should nightly GitHub backup be enabled?
