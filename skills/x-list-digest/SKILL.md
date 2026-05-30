---
name: x-list-digest
description: Use when Beau wants recurring digests of public posts from an X/Twitter list or selected people, without requiring X API access.
---

# X List Digest

## When To Use

Use this when Beau provides an X list URL, a group of handles, or asks for an
ongoing digest of posts from specific people. If the X list URL is blocked, use
the handle watchlist at `/opt/data/HermesAgent/config/x-watchlist.md`.

Primary list:

- `https://x.com/i/lists/1983435862911103455`

Fallback watchlist:

- `/opt/data/HermesAgent/config/x-watchlist.md`

## Source Strategy

Do not require X API access. Use the best available public path:

1. Firecrawl/web extraction for accessible post pages, list pages, embeds, or
   mirrors.
2. Browser automation for the public X list page, if available.
3. DuckDuckGo/web search for recent posts by handles in `config/x-watchlist.md`.
4. Public mirrors, article embeds, newsletters, or search snippets.
5. Ask Beau for the post text if X blocks access.

If Firecrawl fails, times out, rate-limits, or appears to be out of credits,
fall back to DuckDuckGo/public web search and browser-accessible pages. Mention
the fallback briefly in the digest only when it affects confidence or coverage.

## Steps

1. Try the list URL first. If it is blocked or empty, read
   `/opt/data/HermesAgent/config/x-watchlist.md`.
2. Collect recent public posts from the list or watchlist since the last digest
   window.
3. Select only the most interesting posts. Favor:
   - concrete news
   - unusual claims
   - useful tools or launches
   - market-moving information
   - strong arguments from credible people
   - repeated themes across multiple people
4. Group posts by theme rather than account-by-account when possible.
5. For each selected post, include:
   - person/handle
   - short paraphrase
   - why it matters
   - link or source trail
   - confidence level if source access is partial
6. Cross-check important claims with non-X sources before presenting them as
   facts.
7. Keep the digest concise enough to read in Discord.

## Output Format

- Headline: one sentence on what the list is talking about.
- Top posts: 3-7 items with handle, takeaway, why it matters, and link.
- Themes: 2-5 bullets.
- Claims to verify: only if needed.
- Suggested follow-up: one useful next action.

## Recurring Behavior

For scheduled digests:

- Default cadence: every 2 hours.
- Send only if there is something worth reading.
- If no interesting posts are found, send a short "quiet window" note at most
  once per day.
- Avoid repeating posts already included in the previous digest when possible.

## Safety

- Never ask Beau for X API credentials in chat.
- Never post, like, repost, follow, DM, or engage without explicit approval.
- Treat X as signal, not ground truth.
- Do not spam Beau with low-value posts just because the cron ran.
- Do not keep retrying Firecrawl after a credit/rate-limit failure during the
  same digest run.
