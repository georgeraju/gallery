---
name: share_market_news
description: Fetch and summarize the latest share market news for a given market or country using the newsdata.io API.
---

# Share Market News Summary

Fetches the latest share market and financial news from newsdata.io for a market or country specified in the user prompt, then summarizes them as concise bullet points organized by sub-section.

## Supported Markets

| Market / Exchange | Examples you can say |
|---|---|
| 🇺🇸 US (NASDAQ, NYSE, S&P 500, Dow Jones) | "NASDAQ news", "S&P 500 update" |
| 🇬🇧 UK (FTSE, LSE) | "FTSE 100 news", "London market update" |
| 🇮🇳 India (Sensex, Nifty, BSE, NSE) | "Sensex today", "Nifty news" |
| 🇯🇵 Japan (Nikkei, TSE) | "Nikkei news", "Tokyo market update" |
| 🇩🇪 Germany (DAX) | "DAX news", "Frankfurt market" |
| 🇫🇷 France (CAC 40) | "CAC 40 update", "Paris market" |
| 🇨🇳 China (Shanghai, SSE) | "Shanghai market news" |
| 🇭🇰 Hong Kong (Hang Seng, HSI) | "Hang Seng news", "Hong Kong market" |
| 🇦🇺 Australia (ASX) | "ASX news", "Australian market" |
| 🇨🇦 Canada (TSX) | "TSX update", "Toronto market" |
| 🇸🇬 Singapore (SGX) | "Singapore market news" |
| 🇰🇷 South Korea (KOSPI, KOSDAQ) | "KOSPI news", "Seoul market" |
| 🇧🇷 Brazil (Bovespa, B3) | "Bovespa news", "Brazilian market" |

Defaults to **US** if no market or country is recognized in the prompt.

## Setup

1. Obtain a free API key from [newsdata.io](https://newsdata.io/).
2. Replace the placeholder in `scripts/key.txt` with your API key.

## Examples

- "Fetch current market news from USA"
- "Get share market news from India"
- "What is the latest Nikkei news from Japan?"
- "Summarize NASDAQ news from the US"
- "Give me today's Hang Seng market news"
- "What's happening with the Shanghai stock exchange?"
- "Show me the latest Hong Kong market headlines"

## Instructions

Call the `run_js` tool with `index.html`. Pass the user's message (which contains the country name or market name) as the `data.prompt` field.

The skill will:
1. Parse the prompt to detect the target market or country.
2. Fetch the latest English-language business/finance news for that country via newsdata.io.
3. Return the headlines organized under sub-sections: **Stocks & Equities**, **Bonds & Fixed Income**, **Commodities**, **Currencies & Forex**, **Crypto & Digital Assets**, **Market News**.

Summarize the returned headlines into concise bullet points under each sub-section heading. Keep each bullet to one short sentence.