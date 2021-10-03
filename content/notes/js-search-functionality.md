---
title: "Implementing a frontend search functionality"

tags: ["javascript", "resources"]
categories: []
---

Let's say we have an online bookstore where we list all our available books. We want to be able to implement a search bar that can filter out results that match the title, author, publisher, etc. 

Solutions like [Algolia](https://www.algolia.com/), [Solr](https://solr.apache.org/), or [Elasticsearch](https://www.elastic.co/elasticsearch/) are non-trivial solutions that require quite a bit of configuration and resources. These solutions may also be overkill if you have a small to moderately large dataset. 

We can look at [Fuse.js](https://fusejs.io/) and [Lunr](https://lunrjs.com/) for a more lightweight solution. Fuse.js is what powers the [search engine](/search) for this site.
