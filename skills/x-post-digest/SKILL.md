---
name: x-post-digest
description: Use when Beau wants Hermes to summarize X/Twitter posts, threads, profiles, or posts from specific people.
---

# X Post Digest

## When To Use

Use this when Beau asks for:

- a summary of an X/Twitter post or thread
- a digest of recent posts from a person or handle
- reactions to a topic on X
- a watchlist-style summary of what certain people are saying
- a comparison between X discussion and broader web/news sources

## Preferred Sources

Use the best available source in this order:

1. Public web search results that include X posts, quoted text, mirrors, or
   embedded pages.
2. Firecrawl or browser extraction for public X pages, if configured.
3. Nitter-like mirrors, archive/search snippets, RSS, newsletters, or article
   pages that quote the posts.
4. Ask Beau to paste the post/thread text if public access is blocked.
5. Optional later: Hermes `x_search` or `xurl` if Beau sets up X/xAI API access.

## Steps

1. Identify the target: handle, post URL, topic, timeframe, and desired depth.
2. Read only public post content. Do not require X API credentials.
3. For a person digest, group posts by theme instead of listing every post.
4. Separate:
   - what the person actually said
   - context from replies or quote posts
   - your interpretation
   - uncertainty or missing context
5. Include links or post IDs when available.
6. For market, politics, medical, legal, or breaking-news topics, cross-check
   against non-X sources before presenting claims as facts.
7. Save durable preferences or watchlists only if Beau asks.

## Output Format

- One-line takeaway.
- Key posts/themes.
- Notable quotes or claims, paraphrased unless short.
- What changed since the last digest, if known.
- Open questions or claims to verify.
- Source links/post IDs.

## Safety

- Never ask Beau to paste X API secrets or tokens into chat.
- Do not require X API access for the normal digest workflow.
- Never read, print, summarize, or expose `~/.xurl`.
- Before posting, liking, reposting, following, blocking, muting, or sending DMs,
  ask Beau for explicit confirmation.
- Do not treat X discourse as verified fact without corroboration.
- If X access is blocked, say so plainly and use public search/web fallback.
