---
name: memory-librarian
description: Use when Beau wants Hermes to remember something, clean up memory, update project status, or organize long-term agent context.
---

# Memory Librarian

## When To Use

Use this when Beau says to remember something, when a project changes status, or
when repeated context should become durable memory.

## Steps

1. Decide whether the information is durable. Do not save temporary chatter.
2. Choose the right file:
   - `memory/about-me.md` for stable facts about Beau.
   - `memory/preferences.md` for how Beau likes work handled.
   - `memory/projects.md` for active project state.
   - `memory/decisions.md` for decisions and rationale.
3. Keep entries short, dated when useful, and easy to prune later.
4. Do not store secrets, tokens, passwords, private keys, or sensitive personal
   details unless Beau explicitly asks and the storage location is safe.
5. When memory conflicts, ask Beau which version is current.
6. After editing memory, summarize exactly what changed.

## Output Format

- What was saved.
- Where it was saved.
- Anything intentionally not saved.

## Rules

- Prefer fewer, higher-quality memory entries.
- Keep memory useful for future action, not archival noise.
- Never commit secrets into memory files.
