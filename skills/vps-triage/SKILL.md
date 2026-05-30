---
name: vps-triage
description: Use when Beau needs to understand or fix the live Hermes VPS, container, service, model, or chat gateway.
---

# VPS Triage

## When To Use

Use this when Beau says the VPS, Discord bot, Telegram bot, Hermes model, Docker
container, or live agent is not behaving as expected.

## Steps

1. Identify where the command should run: local Windows machine, VPS host,
   container shell, or Hermes chat.
2. Check whether Beau is inside a container. Missing `sudo` and `systemctl` often
   means container shell.
3. Check the active model/provider with `hermes model` or `hermes config show`.
4. Check the running process or container with `ps aux`, `docker ps`, or the VPS
   dashboard.
5. Restart the smallest affected component first.
6. Verify with a harmless test message.
7. Update `deployment/vps-setup.md` or `deployment/vps-inventory.md` with anything
   newly learned.

## Notes

- Do not ask Beau to paste secrets.
- If a command fails inside Hermes chat, tell Beau to run it in the actual shell.
- If the host is managed by a VPS panel, the correct restart path may be the panel
  rather than terminal commands.
