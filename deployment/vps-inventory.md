# VPS Inventory

Use one section per server or container. Keep passwords and tokens out of this
file.

## Hermes Main VPS

- Provider: _fill in_
- Dashboard label: _fill in_
- Hostname/IP: stored in `.env`
- SSH user: stored in `.env`
- Purpose: Live Hermes agent
- Deployment style: _Docker / one-click Docker / host install_
- Restart method: _fill in after confirmed_
- Backup repo: _fill in GitHub URL_
- Notes:
  - Current model: gpt-5.5
  - Current provider: OpenAI Codex

## Additional Agents

Add separate sections for each future agent. Use separate credentials and memory
when the role is meaningfully different.
