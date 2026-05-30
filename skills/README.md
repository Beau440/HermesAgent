# Skills

Each skill is a reusable playbook. Create a new folder for each skill and put the
instructions in `SKILL.md`.

```text
skills/
  nightly-backup/
    SKILL.md
  vps-triage/
    SKILL.md
```

Use skills when Hermes repeats the same workflow more than once. Keep them
specific enough that Hermes knows when to trigger them.

Start from `skills/_template/SKILL.md`.

## Personal Skills

- `youtube-summarizer`: video summaries, tutorials, and action items.
- `web-research`: current web research with source links.
- `x-post-digest`: X/Twitter post, thread, profile, and person digests.
- `market-brief`: stocks, crypto, macro, earnings, and watchlists.
- `memory-librarian`: durable memory and project state cleanup.
- `discord-operator`: safer help through Discord/chat surfaces.
- `vps-triage`: live Hermes VPS/container debugging.
- `safe-github-backup`: safe GitHub commits and pushes without secrets.
