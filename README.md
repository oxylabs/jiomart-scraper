# Jiomart Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Jiomart Scraper](https://oxylabs.io/products/scraper-api/ecommerce/jiomart?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Jiomart website effortlessly. This brief guide explains how an Jiomart Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Jiomart results by providing your own URLs to our service. We can return the HTML for any Jiomart page you like.

#### Python code example

The example below illustrates how you can get HTML of Jiomart page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.jiomart.com/groceries'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/jiomart-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!doctype html> <html lang=\"en-US\"> <head> <title>Jiomart - Groceries</title> <meta charset=\"utf-8\"> ... </html>",
      "created_at": "2023-12-18 10:28:42",
      "updated_at": "2023-12-18 10:28:45",
      "page": 1,
      "url": "https://www.jiomart.com/groceries",
      "job_id": "7142460660729798657",
      "status_code": 200
    }
  ]
}
```
With our Jiomart Scraper, you can easily pull public information from any Jiomart web page. Gather vital grocery details such as price, customer reviews, or product descriptions, to understand market trends and supersede your business rivals. If you encounter any uncertainties, our support team is ready to answer via live chat or you can drop us an email at hello@oxylabs.io.