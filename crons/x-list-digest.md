# X List Digest

## Goal

Every couple of hours, scan Beau's X list for interesting public posts and send a
short breakdown.

## Source

- X list: `https://x.com/i/lists/1983435862911103455`
- Fallback watchlist: `/opt/data/HermesAgent/config/x-watchlist.md`
- Preferred tools: Firecrawl/web extract, browser automation, DuckDuckGo/web
  search.
- Fallback: if Firecrawl fails, times out, rate-limits, or runs out of credits,
  use DuckDuckGo/public web search and browser-accessible pages instead.
- X API: not required.

## Cadence

- Planned schedule: every 2 hours while Beau wants it active.
- Timezone: America/New_York.

## Draft Prompt

Use `x-list-digest`, `x-post-digest`, `web-research`, and `discord-operator`.
Scan the public X list at `https://x.com/i/lists/1983435862911103455` for recent
interesting posts. Use Firecrawl first for web extraction; if Firecrawl fails,
times out, rate-limits, or runs out of credits, fall back to DuckDuckGo/public
web search and browser-accessible pages. If the X list URL is blocked, read
`/opt/data/HermesAgent/config/x-watchlist.md` and search recent public posts from
those handles instead. Do not require X API access. Select only high-signal
posts, group them by theme, include source links when available, and send Beau a
concise Discord-friendly breakdown. If nothing interesting is found, send nothing
unless there has been no status update today.

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
