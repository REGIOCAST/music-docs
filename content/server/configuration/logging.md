---
date: 2000-01-01T00:00:00+00:00
title: Logging
author: juliankoehn
weight: 21
aliases:
- /installation/logging/
- /administration/server/logging
description: |
  Configure server logging.
---

The server logs are written to stderr and are captured by the Docker daemon. You can access the server logs by running the following Docker command:

```
$ docker logs <container name>
```

The default log level is `INFO`. You can enable more detailed debug logging with the following configuration parameter:

```
MUSIC_LOGS_DEBUG=true
```

Logs are written to stderr in json-format. You can change the default log format to something more human-readable with the following configuration parameters:

```
MUSIC_LOGS_TEXT=true
MUSIC_LOGS_PRETTY=true
MUSIC_LOGS_COLOR=true
```