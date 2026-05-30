# Crons And Scheduled Automations

This is the human-readable registry of scheduled jobs. The actual scheduler may
live inside Hermes, Docker, the VPS panel, or another service.

## Format

```markdown
### task-name
- Status: active / paused / planned
- Schedule: every day at 08:00 America/New_York
- Surface: Hermes cron / VPS cron / Docker / GitHub Actions
- Does: one plain-English sentence
- Why: one plain-English sentence
- Notifies: Discord / Telegram / email / none
- Owner: Beau / Hermes
- Risk: low / medium / high
```

## Active Automations

No active automations documented yet.

## Planned Automations

### nightly-agent-backup
- Status: planned
- Schedule: every night after midnight
- Surface: Hermes cron
- Does: commits and pushes safe changes from this command center repo
- Why: preserve memory, skills, and setup notes if the VPS breaks
- Notifies: Discord or Telegram with success/failure
- Owner: Hermes
- Risk: medium
