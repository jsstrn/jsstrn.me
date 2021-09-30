---
title: "How to download online videos"

tags: ["productivity"]
categories: ["technology"]
---

Download the [`youtube-dl`](https://github.com/ytdl-org/youtube-dl) command line tool from `brew`

```sh
brew install youtube-dl
```

`youtube-dl` supports a huge list of extractors, including popular sites like YouTube and Vimeo.

List all extractors and pipe it into `grep` to search for an extractor

```sh
youtube-dl --list-extractors | grep "udemy"
```

To download a video

```sh
youtube-dl "video-url"
```

Simply pass in the cookie file to download videos that require login credentials

```sh
youtube-dl --cookies <path-to-cookie-file> "video-url"
```

You can use a browser extension like [cookie.txt](https://addons.mozilla.org/en-US/firefox/addon/cookies-txt/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search) to extract your cookie file.
