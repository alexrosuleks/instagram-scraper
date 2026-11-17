# Instagram Scraper: Instagram Scraper API for Python & Node.js (2026)

Scrape public Instagram profiles, posts, reels, comments, hashtags, and places. Get captions, likes, comments, media URLs, and owner details without logging in.

**[▶ Try the Instagram Scraper free on Scrapely](https://scrape.ly/store/echofield/instagram-scraper)** · [Compare Scrapely vs other scraping tools](https://scrape.ly/compare)

This repository shows how to scrape Instagram data with the [Instagram Scraper](https://scrape.ly/store/echofield/instagram-scraper) using the official
**Scrapely SDKs for JavaScript and Python**. You pass the input, Scrapely runs the instagram scraper in the cloud
(proxies, retries, browser and scaling included) and returns clean, structured data as JSON, CSV or Excel.
No scraper code to maintain and no blocked requests to debug.

## Why use this Instagram scraper

- **No-code or API:** run it from the [Scrapely Store](https://scrape.ly/store/echofield/instagram-scraper) or from your code with the SDK.
- **Structured instagram data:** ready-to-use fields instead of raw HTML.
- **Pay per result:** $2.29 per 1,000 result results, no monthly subscription required.
- **Maintained and monitored:** scrapers are tested around the clock and fixed fast when Instagram changes.
- **Integrations:** n8n, Make, Zapier, LangChain, LlamaIndex, MCP (Claude, Cursor) and webhooks.

## What Instagram data can you extract?

Scrape public Instagram profiles, posts, reels, comments, hashtags, and places. Get captions, likes, comments, media URLs, and owner details without logging in.

## Quick start

1. [Sign up for Scrapely](https://scrape.ly) (free plan available) and copy your API token from
   **Settings → API & Integrations**.
2. Clone this repo and set your token:

```bash
export SCRAPELY_TOKEN=your_token
```

### Node.js (JavaScript SDK)

```bash
npm install
node example.js
```

```js
const { ScrapelyClient } = require('scrapely-client');
const client = new ScrapelyClient({ token: process.env.SCRAPELY_TOKEN });

const run = await client.actor('echofield/instagram-scraper').call({"resultsType": "posts", "directUrls": ["https://www.instagram.com/humansofny/"], "resultsLimit": 20, "searchType": "hashtag", "searchLimit": 10, "commentsPostsLimit": 10});
const { items } = await client.dataset(run.defaultDatasetId).listItems();
```

### Python (Python SDK)

```bash
pip install -r requirements.txt
python example.py
```

```python
from scrapely_client import ScrapelyClient
client = ScrapelyClient(os.environ['SCRAPELY_TOKEN'])

run = client.actor('echofield/instagram-scraper').call(run_input={ "resultsType": "posts", "directUrls": [ "https://www.instagram.com/humansofny/" ], "resultsLimit": 20, "searchType": "hashtag", "searchLimit": 10, "commentsPostsLimit": 10 })
items = list(client.dataset(run.default_dataset_id).iterate_items())
```

### REST API / cURL

```bash
curl -X POST "https://api.scrape.ly/v2/acts/echofield~instagram-scraper/run-sync-get-dataset-items?token=$SCRAPELY_TOKEN" \
  -H "Content-Type: application/json" \
  -d @input.json
```

## Example input

```json
{
  "resultsType": "posts",
  "directUrls": [
    "https://www.instagram.com/humansofny/"
  ],
  "resultsLimit": 20,
  "searchType": "hashtag",
  "searchLimit": 10,
  "commentsPostsLimit": 10
}
```

See every input option on the [Instagram Scraper page](https://scrape.ly/store/echofield/instagram-scraper).

## Pricing

**$2.29 per 1,000 result results.** Free plan available, no credit card needed to start. Check current pricing on the
[Store page](https://scrape.ly/store/echofield/instagram-scraper) and see how Scrapely compares with other tools on [scrape.ly/compare](https://scrape.ly/compare).

## FAQ

**How do I scrape Instagram with Python?** Install `scrapely-client-python`, set `SCRAPELY_TOKEN` and run
`example.py`. The scraper runs on Scrapely and you read the results from the dataset.

**How do I scrape Instagram with Node.js?** Install `scrapely-client`, set `SCRAPELY_TOKEN` and run `example.js`.

**Is there a instagram scraper API?** Yes. Call `POST https://api.scrape.ly/v2/acts/echofield~instagram-scraper/runs`
or use `run-sync-get-dataset-items` to get results in one request.

**Do I need proxies?** No. Proxies, retries and browsers are handled by Scrapely.

**Is scraping Instagram legal?** This scraper collects publicly available data. Check Instagram's terms and the
laws that apply to you, especially for personal data (GDPR, CCPA).

**Can I schedule it or get results by webhook?** Yes. Use Scrapely schedules and webhooks, or n8n, Make and Zapier.

## Related Instagram scrapers

- [Instagram Profile Scraper](https://github.com/alexrosuleks/instagram-profile-scraper): Scrape public Instagram profile details from usernames, IDs, or URLs: bio, follower and following counts, posts count,…
- [Instagram Reel Scraper](https://github.com/alexrosuleks/instagram-reel-scraper): Scrape public Instagram reels from a profile or reel URL. Get captions, play and like counts, comment counts, video…
- [Instagram Post Scraper](https://github.com/alexrosuleks/instagram-post-scraper): Scrape public Instagram posts from usernames, profile URLs, or post URLs. Get captions, hashtags, likes, comments…
- [Instagram Hashtag Scraper](https://github.com/alexrosuleks/instagram-hashtag-scraper): Scrape public Instagram posts and reels for one or more hashtags. Get captions, likes, comment counts, media URLs,…

## Looking for an alternative?

Scrapely is an alternative to Apify, Bright Data, ScraperAPI, Firecrawl, Octoparse, PhantomBuster, SerpApi,
Zyte and others. See the side-by-side pricing on [scrape.ly/compare](https://scrape.ly/compare).

---

**Keywords:** instagram scraper, instagram scraper, instagram scraper api, instagram scraper python, instagram scraper node.js,
scrape instagram, instagram data extraction, instagram crawler, instagram api, export instagram data to csv, instagram-scraper

License: MIT. Example code only; the scraper runs on [Scrapely](https://scrape.ly/store/echofield/instagram-scraper).
