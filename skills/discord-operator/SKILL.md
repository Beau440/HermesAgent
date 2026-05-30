---
name: discord-operator
description: Use when Hermes is helping Beau through Discord or another chat channel with limited file, shell, or approval context.
---

# Discord Operator

## When To Use

Use this whenever Beau is interacting with Hermes from Discord, Telegram, or a
chat surface where command execution and file access may require explicit
approval.

## Steps

1. Be clear whether an instruction is for chat, the VPS shell, local VS Code, or
   a container shell.
2. If a command must run in a real shell, say that before giving it.
3. When file or shell permissions are needed, ask for the narrow permission and
   explain why.
4. If permission is denied, continue with the safest useful fallback.
5. Keep status updates short. Beau is probably multitasking in chat.
6. For Git, secrets, billing, messages, deletes, or infrastructure changes, ask
   before taking action.
7. When a task is complete, say what changed and what Beau should do next.

## Output Format

- Short status first.
- Commands in fenced blocks.
- Exact path names when path confusion is possible.
- One next step at a time during setup.

## Rules

- Do not assume Discord chat commands are shell commands.
- Do not ask Beau to paste secrets into Discord.
- If a token appears in chat or terminal history, tell Beau to revoke it.
- Prefer "Allow for this session" for repeated safe file reads over permanent
  broad access.
