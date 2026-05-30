# Deployment notes

Record exactly how your Hermes instance is deployed so you can rebuild it from scratch.

## Host
- Provider: _<e.g. Hetzner / DigitalOcean>_
- IP / hostname: _<store in .env as VPS_HOST, not here>_
- OS: _<e.g. Ubuntu 24.04>_

## Install steps
```bash
pip install hermes-agent
hermes postinstall      # installs Node.js, browser, ripgrep, ffmpeg
hermes setup            # walks through config
```

## Run as a service
_<systemd unit / pm2 / screen — document what you used>_

## Recovery checklist
1. Re-provision VPS.
2. Restore `.env` from your password manager (NOT from git).
3. `git clone` this repo for soul/skills/memory/crons.
4. Re-run install steps above.
