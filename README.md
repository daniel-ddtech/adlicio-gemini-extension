# Adlicio extension for Gemini CLI

Connects Gemini CLI to [Adlicio](https://tryadlicio.com), a customer-voice
research tool for marketers and ad operators.

Adlicio gives agents real customer language. Scrape comments and reviews from
Reddit, YouTube, Amazon, TikTok, Instagram, Trustpilot, the app stores and more
(30+ sources), search Reddit and YouTube, pull top-performing TikTok and Instagram
videos with their hooks, find competitor ads from the Meta Ad Library, and build
brand and voice-of-customer reports.

## Install

```bash
gemini extensions install https://github.com/daniel-ddtech/adlicio-gemini-extension
```

## What it adds

One MCP server, `adlicio`, pointing at the hosted endpoint:

```
https://mcp.tryadlicio.com/mcp
```

Transport is streamable HTTP. Auth is OAuth 2.1 with dynamic client
registration, so there is nothing to configure and no API key to set. The first
tool call opens a browser sign-in for your Adlicio account.

`GEMINI.md` ships alongside it and tells the model how to run a research pass
and how to report the result with sources.

## Tools

Scraping and search: `scrape_url`, `search_reddit`, `search_youtube`,
`search_blind`, `research_topic`, `start_deep_scrape`, `get_deep_scrape`.

Ad and creator research: `find_scroll_stoppers`, `find_creators`,
`find_competitor_ads`, `find_products`, `find_early_products`, `save_script`.

Reports: `start_brand_research`, `get_brand_research`, `start_voc_report`,
`get_voc_report`, `get_audience`.

Listening and history: `create_brand`, `add_tracked_source`,
`list_tracked_sources`, `list_history`, `search_history`, `get_history_item`,
`scrape_facebook_group`, `get_extension_job`, `whoami`.

`scrape_url` supports Reddit, YouTube, Amazon, the Apple App Store, Google Play,
Steam, Trustpilot, Reviews.io, Etsy, Walmart, Sephora, Ulta, eBay, Better
Business Bureau, G2, AliExpress, TripAdvisor, Stack Exchange, Discourse, phpBB,
XenForo, vBulletin, Invision Community, Hacker News, Quora, Product Hunt,
Shopify and DTC product pages including Yotpo and Loox, Disqus comments, public
Facebook posts, public LinkedIn posts, public Blind posts, public Instagram
posts and reels, TikTok videos, and Notion pages.

## Access and credits

The MCP server works with the Starter, Growth and Scale plans (from $49 a
month). The Pro plan covers the Chrome extension only. A free account can connect and see the tools, but most tools
spend research credits. `search_reddit` and `search_youtube` cost no credits.

Plans and setup: <https://tryadlicio.com/mcp>

## Related

- CLI and MCP docs: <https://github.com/daniel-ddtech/commentscraper-cli>
- Agent plugin for Claude Code, Copilot, Codex, Cursor and Grok:
  <https://github.com/daniel-ddtech/adlicio-plugin>
- MCP Registry entry: `com.tryadlicio/adlicio`

## License

MIT. Contact: daniel@tryadlicio.com
