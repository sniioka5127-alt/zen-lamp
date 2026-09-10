# ENTITY-04 | Google verification notes

Google Search Console separates indexed data from Live Test data. After deploying identity changes, use both:

- Indexed result: what Google currently knows about the URL.
- Live Test: whether the currently deployed URL can be crawled and indexed.

A successful Live Test does not mean the indexed result has already refreshed. Request indexing only after the live page is correct.

For bulk changed URLs, keep the sitemap current and use Search Console's sitemap reporting in addition to single-URL requests.

ENTITY-04 does not assume that a structured-data relationship will create a Knowledge Panel or improve ranking by itself.
