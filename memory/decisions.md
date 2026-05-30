# Decisions

## 2026-05-29: Use VS Code Repo As Hermes Command Center

- Decision: Keep Hermes identity, memory, skills, cron registry, VPS notes, and
  safe configuration docs in `C:\Users\BeauB\hermes-agent`.
- Why: It creates one organized place to manage the agent and back up non-secret
  state to GitHub.
- Tradeoff: Secrets must stay outside Git, so the repo tracks references to
  credentials rather than the values.

## 2026-05-29: Use OpenAI Codex Provider With gpt-5.5

- Decision: Hermes was configured with `hermes setup model` to use `gpt-5.5`.
- Why: The setup wizard was easier and less error-prone than manual config edits.
- Note: Chat surfaces may still describe the provider as Codex or GPT-5 family.
