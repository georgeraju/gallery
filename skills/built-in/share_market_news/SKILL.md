---
name: share_market_news
description: Fetch and summarize the latest share market news for a given country using the newsdata.io API.
---

# Share Market News Summary

Fetches the latest share market and financial news from newsdata.io for a country specified in the user prompt, then summarizes them as concise bullet points.

## Setup

1. Obtain a free API key from [newsdata.io](https://newsdata.io/).
2. Replace the placeholder in `scripts/key.txt` with your API key.

## Examples

- "Fetch current market news from USA"
- "Get share market news from India"
- "What is the latest stock market news from Japan?"
- "Summarize NASDAQ news from the US"
- "Give me today's market news from UK"

## Instructions

Call the `run_js` tool with `index.html`. Pass the user's message (which contains the country name or market name) as the `data.prompt` field.

The skill will fetch the latest English-language business/finance news for that country and return the headlines. Summarize the returned headlines into concise bullet points. Keep each bullet to one short sentence. If no country is mentioned, default to the United States.