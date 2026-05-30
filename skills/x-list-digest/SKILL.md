---
name: x-list-digest
description: Use when Beau wants recurring digests of public posts from an X/Twitter list or selected people, without requiring X API access.
---

# X List Digest

## When To Use

Use this when Beau provides an X list URL, a group of handles, or asks for an
ongoing digest of posts from specific people.

Primary list:

- `https://x.com/i/lists/1983435862911103455`

## Source Strategy

Do not require X API access. Use the best available public path:

1. Browser automation for the public X list page, if available.
2. Firecrawl/web extraction for accessible post pages or mirrors.
3. DuckDuckGo/web search for `site:x.com` posts from list members or quoted
   pages.
4. Public mirrors, article embeds, newsletters, or search snippets.
5. Ask Beau for the post text if X blocks access.

## Steps

1. Collect recent public posts from the list since the last digest window.
2. Select only the most interesting posts. Favor:
   - concrete news
   - unusual claims
   - useful tools or launches
   - market-moving information
   - strong arguments from credible people
   - repeated themes across multiple people
3. Group posts by theme rather than account-by-account when possible.
4. For each selected post, include:
   - person/handle
   - short paraphrase
   - why it matters
   - link or source trail
   - confidence level if source access is partial
5. Cross-check important claims with non-X sources before presenting them as
   facts.
6. Keep the digest concise enough to read in Discord.

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
