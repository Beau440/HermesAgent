---
name: youtube-summarizer
description: Use when Beau shares a YouTube link or asks for a video, tutorial, podcast, interview, or livestream summary.
---

# YouTube Summarizer

## When To Use

Use this when Beau sends a YouTube URL, asks what a video says, wants notes from a
tutorial, or wants action items from a long video.

## Steps

1. Identify the video title, channel, length, and URL.
2. Get the transcript or captions when available. If transcript access fails, use
   the video page, description, chapters, comments, and web search as backup.
3. Summarize the video in Beau's style: direct, useful, and not bloated.
4. Separate facts, opinions, recommendations, and action items.
5. If it is a tutorial, produce a step-by-step checklist Beau can follow.
6. If it relates to Hermes, agents, VPS setup, GitHub, coding, or automation,
   suggest what should be saved into `memory/`, `skills/`, or `deployment/`.
7. Include the source URL and mention when transcript access was unavailable.

## Output Format

- Short answer: 3-6 bullets.
- Key ideas: concise bullets grouped by topic.
- Action items: concrete next steps.
- Save-worthy notes: only if useful for long-term memory.

## Rules

- Do not invent details if the transcript is unavailable.
- Do not quote long copyrighted passages.
- Prefer practical takeaways over a minute-by-minute recap unless Beau asks.
