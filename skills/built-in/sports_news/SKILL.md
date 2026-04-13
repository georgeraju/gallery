---
name: sports_news
description: Fetch and summarize the latest sports news headlines by category using the newsdata.io API.
---

# Sports News Summary

Fetches the latest sports news from newsdata.io and presents them organized by sport category so you can summarize them into bullet points.

## Categories

- **Football**
- **Basketball**
- **Tennis**
- **Cricket**
- **Other Sports**

## Setup

1. Obtain a free API key from [newsdata.io](https://newsdata.io/).
2. Replace the placeholder in `scripts/key.txt` with your API key.

## Examples

- "What are the latest sports news headlines?"
- "Summarize today's top sports stories"
- "Give me a quick update on football news"
- "What's happening in cricket today?"

## Instructions

Call the `run_js` tool with `index.html`. No additional `data` fields are required — the skill will automatically fetch the latest sports news.

Summarize the returned news articles into concise bullet points organized under each sport category heading. Keep each bullet point to one short sentence.