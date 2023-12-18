# Sitemap Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Sitemap Scraper](https://oxylabs.io/products/scraper-api/web/sitemap-scraper?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from any sitemap effortlessly. This brief guide explains how a Sitemap Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get sitemap results by providing your own URLs to our service. We can return the HTML for any sitemap you like.

#### Python code example

The example below illustrates how you can get sitemap of [oxylabs.io](https://oxylabs.io/)

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://oxylabs.io/sitemap.xml'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/sitemap-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<?xml version=\"1.0\" encoding=\"UTF-8\"?>\n  <urlset xmlns=\"http://www.sitemaps.org/schemas/sitemap/0.9\" ... </html>",
      "created_at": "2023-12-18 11:31:31",
      "updated_at": "2023-12-18 11:31:32",
      "page": 1,
      "url": "https://oxylabs.io/sitemap.xml",
      "job_id": "7142476472547084289",
      "status_code": 200
    }
  ]
}
```
Using our Sitemap Scraper, you can easily extract website data from any sitemap. If you need further assistance, feel free to reach out to our support team via live chat or drop us an email at hello@oxylabs.io.
