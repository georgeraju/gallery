---
name: technews_summary
description: Fetch and summarize the latest news headlines by keyword and country using the newsdata.io API.
---

# Tech News Summary

Fetches the latest news from newsdata.io filtered by a search query (`q`) and country, then presents them organized by category so you can summarize them into bullet points.

Language is always **US English** (`en`) and cannot be changed.

## Data Fields

| Field     | Type   | Default      | Description |
|-----------|--------|--------------|-------------|
| `q`       | string | `business`   | Keyword(s) to search across article content. Supports exact phrases with double quotes (e.g., `"global warming"`) and Boolean operators (`AND`, `OR`, `NOT`). Example: `movie AND marvel`. |
| `country` | string | `us`         | ISO 3166-1 alpha-2 country code(s), comma-separated, up to 5. Examples: `us`, `gb`, `in`, `us,gb`. |

> **Pro Tip:** Use double quotes for exact phrases (e.g., `q="global warming"`) or Boolean operators like `AND`, `OR`, and `NOT` (e.g., `q=movie AND marvel`).

## Setup

1. Obtain a free API key from [newsdata.io](https://newsdata.io/).
2. Replace the placeholder in `scripts/key.txt` with your API key.

## Examples

| User prompt | `q` | `country` |
|---|---|---|
| "What are the latest tech news headlines?" | `technology` | `us` |
| "Summarize today's breaking news in the UK" | `breaking` | `gb` |
| "Give me a quick update on business news in India" | `business` | `in` |
| "What's happening with AI and machine learning?" | `"artificial intelligence" OR "machine learning"` | `us` |
| "News about climate change in Europe" | `"climate change"` | `gb,fr,de` |

## Instructions

1. Extract `q` and `country` from the user's prompt.
   - If the user does not specify a topic, default `q` to `business`.
   - If the user does not specify a country, default `country` to `us`.
   - Language is always `en` — never pass a `language` field.
2. Call the `run_js` tool with `index.html`, passing the extracted `q` and `country` as `data` fields.
3. Summarize the returned news articles into concise bullet points organized under each category heading. Keep each bullet point to one short sentence.