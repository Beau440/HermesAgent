# Crons — scheduled automations

Document each scheduled task Hermes runs: what it does, when, and why. This is your
human-readable registry (the actual schedule is configured inside Hermes).

## Format

```
### <task name>
- Schedule: <cron expression or plain English, e.g. "every day 8am">
- Does: <what it does>
- Why: <why it exists>
- Notifies: <where output goes, e.g. Telegram>
```

## Active automations

### example-morning-brief
- Schedule: every day 08:00
- Does: summarizes overnight emails/news into a short brief
- Why: start the day informed without digging
- Notifies: Telegram
