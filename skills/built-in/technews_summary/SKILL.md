---
name: technews_summary
description: Fetch and summarize the latest news headlines by category using the newsdata.io API.
---

# Tech News Summary

Fetches the latest news from newsdata.io and presents them organized by category so you can summarize them into bullet points.

## Categories

- **Breaking News**
- **Business**
- **Entertainment**
- **Technology**
- **Environment**

## Setup

1. Obtain a free API key from [newsdata.io](https://newsdata.io/).
2. Replace the placeholder in `scripts/key.txt` with your API key.

## Examples

- "What are the latest tech news headlines?"
- "Summarize today's breaking news"
- "Give me a quick update on business news"

## Instructions

Call the `run_js` tool with `index.html`. No additional `data` fields are required — the skill will automatically fetch the latest news.

Summarize the returned news articles into concise bullet points organized under each category heading. Keep each bullet point to one short sentence.