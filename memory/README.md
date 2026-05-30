# Memory

Memory is durable context for Hermes. Keep it specific, current, and safe.

## Files

| File | Purpose |
| --- | --- |
| `about-me.md` | Stable facts about Beau |
| `projects.md` | Active projects and status |
| `decisions.md` | Decisions made and why |
| `preferences.md` | How Beau likes work handled |

## Rules

- Do not store secrets here.
- Prefer stable facts over temporary chat context.
- Date decisions so old context can be pruned later.
- Keep one idea per bullet when possible.

## Maintenance

Review memory regularly. Stale memory can make an agent behave strangely because
it confidently follows outdated assumptions.
