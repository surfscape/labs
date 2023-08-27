---
title: NeoSearch
track_code: SPTC250823NS
date: 2023-08-25T00:00
summary: Neocities search engine
status: Planing
---

A Neocities search engine that would search any page and link inside the `neocities.org` domain.

## Implementation, Roadblocks & Alternatives

This could be done using a search API like the [Bing Web Search API](https://www.microsoft.com/en-us/bing/apis/bing-web-search-api), however, since NeoSearch runs on the client side this would expose the API key to anyone and since serverless functions are paid and we do not have any funds this is not an option.

There's also the possibility to use the [DuckDuckGo API](http://api.duckduckgo.com/?q=x&format=json) since it does not need an API key, however, this is not a complete API and after some tests, it's not capable to search a lot of complex terms including links and words in the `neocities.org` domain.

Another possiblity is to screen scrape DuckDuckGo for links. We would use the HTML or Lite version of DDG since it's lighter on the client side, however DDG does not include the [CORS header](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS) meaning a domain (NeoSearch) can't access the content of another domain (DuckDuckGo HTML/Lite) unless allowed.

We could also use [Google CSE](https://programmablesearchengine.google.com/about/) which is what all Neocities search engines use but this goes againts our mission of not tracking users since Google is pretty much an advertising company. We have the resources to at least block the ads on CSE but that does not help with the tracking issue.

The last possibility we have is to create a in-house CORS proxy to add the CORS header to DuckDuckGo and then screen scrape DuckDuckGo (or any other search engine) using JS on the client side, this will allows us to use DuckDuckGo as our provider and we do not need to use any API, however, the CORS proxy needs to be hosted on a server or use a serverless function and that would probably cost us some money monthly and since we don't have any funds this is mostly unlikely to happen.
