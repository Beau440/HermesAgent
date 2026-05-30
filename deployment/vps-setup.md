# VPS Setup And Recovery

Record enough detail here that you can rebuild the agent without guessing.

## Host

- Provider: _fill in_
- Dashboard URL: store in `.env` as `VPS_DASHBOARD_URL`
- IP / hostname: store in `.env` as `VPS_HOST`
- Login user: store in `.env` as `VPS_USER`
- OS/image: _fill in_
- Install style: _Docker / one-click app / host-level Python install_

## First Login

```bash
ssh <user>@<host>
```

If you land at a short prompt like a container ID and common commands such as
`sudo` or `systemctl` are missing, you are likely inside a container rather than
the host OS.

## Hermes Setup

```bash
hermes setup
hermes setup model
hermes model
```

## Restart Patterns

Docker:

```bash
docker ps
docker restart <container>
docker logs -f <container>
```

Docker Compose:

```bash
docker compose restart
docker compose logs -f
```

System service:

```bash
systemctl restart hermes
systemctl status hermes
journalctl -u hermes -f
```

Managed VPS panel:

1. Open the VPS provider dashboard.
2. Find the Docker/app/container manager.
3. Restart the Hermes container or app.
4. Reopen the Hermes CLI/chat and verify the model/status.

## Recovery Checklist

1. Re-provision the VPS/container.
2. Restore secrets from the password manager into `.env`.
3. Clone this repo.
4. Restore `soul/`, `memory/`, `skills/`, `crons/`, and `config/` notes.
5. Run `hermes setup`.
6. Run `hermes setup model`.
7. Reconnect Discord/Telegram.
8. Verify with a harmless test message.
9. Commit any updated docs back to GitHub.
