# Nightly Agent Backup

## Goal

Back up safe Hermes command center changes to GitHub every night.

## Schedule

- Planned time: _fill in_
- Timezone: America/New_York

## Safety Checks

The job should stop if any of these are true:

- `.env` is staged or modified for commit
- files matching `*.key`, `*.pem`, `*secret*`, or `*private*` are staged
- `git diff` contains obvious token names
- remote GitHub repository is not configured

## Draft Prompt For Hermes

Check the Hermes command center repo for safe documentation changes. If there are
changes, verify no secrets are staged, commit them with a clear message, push to
GitHub, and notify Beau with the result. If anything looks risky, stop and ask.
