---
name: url-content-summarizer
description: Read and summarize the main content of a user provided URL in one paragraph.
---

# URL Content Summarizer

## Examples

- "Summarize the content of [URL]"
- "What's the main content of [URL]?"
- "Give me a summary of [URL]"

## Instructions

Call the `run_js` tool with the following exact parameters:

- data: A JSON string with the following field
  - url: The URL to fetch and summarize content from.
