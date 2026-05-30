# Default Hermes Skill Loadout

This is Beau's preferred broad startup set. Use it when starting Hermes for a
general-purpose session.

```zsh
hermes --skills youtube-content,youtube-summarizer,x-post-digest,web-research,duckduckgo-search,market-brief,stocks,memory-librarian,discord-operator,vps-triage,safe-github-backup,github-auth,github-issues,github-repo-management,github-pr-workflow,github-code-review,codebase-inspection,systematic-debugging,test-driven-development,python-debugpy,hermes-agent,hermes-agent-skill-authoring,codex,claude-code,kanban-codex-lane,webhook-subscriptions,native-mcp,google-workspace,airtable,linear,notion,maps,nano-pdf,ocr-and-documents,powerpoint,arxiv,blogwatcher,llm-wiki,polymarket,research-paper-writing
```

## Add When Configured

Add these once the provider/API is set up:

- Firecrawl/web extraction tool
- Browser automation / Browserbase / Browser Use
- `searxng-search` or `scrapling` if installed and working
- `xurl` or `x_search` only if Beau later configures X/xAI API access

## Notes

- Browser and Firecrawl usually show up as tools/toolsets or provider settings,
  not necessarily as preloadable `--skills` names.
- `x-post-digest` should work from public web/browser/Firecrawl sources first.
- `xurl` and `x_search` are optional API-based upgrades, not required defaults.
- Keep risky skills like pentesting, 1Password, or godmode out of the default
  loadout unless Beau explicitly needs them.
