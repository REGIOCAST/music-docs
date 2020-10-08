---
date: 2000-01-01T00:00:00+00:00
title: Headers
author: juliankoehn
weight: 21
description: |
  Configure server headers.
---

Music provides a number of configuration options that can be used to secure http requests. Here is a list of available parameters:

```
MUSIC_HTTP_ALLOWED_HOSTS
MUSIC_HTTP_PROXY_HEADERS
MUSIC_HTTP_SSL_REDIRECT
MUSIC_HTTP_SSL_TEMPORARY_REDIRECT
MUSIC_HTTP_SSL_HOST
MUSIC_HTTP_SSL_PROXY_HEADERS
MUSIC_HTTP_STS_SECONDS
MUSIC_HTTP_STS_INCLUDE_SUBDOMAINS
MUSIC_HTTP_STS_PRELOAD
MUSIC_HTTP_STS_FORCE_HEADER
MUSIC_HTTP_BROWSER_XSS_FILTER
MUSIC_HTTP_FRAME_DENY
MUSIC_HTTP_CONTENT_TYPE_NO_SNIFF
MUSIC_HTTP_CONTENT_SECURITY_POLICY
MUSIC_HTTP_REFERRER_POLICY
```

_This document is still a work-in-progress. You can read more about each of these parameters at [github.com/unrolled/secure](https://github.com/unrolled/secure)._

# Recommended Headers

We recommend setting these configuration parameters. _Please note these parameters should only be used when SSL is enabled._

```
MUSIC_HTTP_SSL_REDIRECT=true
MUSIC_HTTP_SSL_TEMPORARY_REDIRECT=true
MUSIC_HTTP_SSL_HOST=music.company.com
MUSIC_HTTP_STS_SECONDS=315360000
```