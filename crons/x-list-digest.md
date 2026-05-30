# X List Digest

## Goal

Every couple of hours, scan Beau's X list for interesting public posts and send a
short breakdown.

## Source

- X list: `https://x.com/i/lists/1983435862911103455`
- Preferred tools: browser automation, Firecrawl/web extract, DuckDuckGo/web
  search.
- X API: not required.

## Cadence

- Planned schedule: every 2 hours while Beau wants it active.
- Timezone: America/New_York.

## Draft Prompt

Use `x-list-digest`, `x-post-digest`, `web-research`, and `discord-operator`.
Scan the public X list at `https://x.com/i/lists/1983435862911103455` for recent
interesting posts. Use browser/public web/Firecrawl sources only; do not require
X API access. Select only high-signal posts, group them by theme, include source
links when available, and send Beau a concise Discord-friendly breakdown. If
nothing interesting is found, send nothing unless there has been no status update
today.

## Output

- One-sentence headline.
- 3-7 top posts or themes.
- Why each matters.
- Source links or source caveat.
- One suggested follow-up.

## Safety

- Do not engage with X posts.
- Do not ask for X credentials.
- Do not present X claims as verified facts without corroboration.
