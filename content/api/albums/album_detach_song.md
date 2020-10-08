+++
date = "2000-01-01T00:00:00+00:02"
title = "Album Detach Song"
description = "Endpoint to detach song from Album"
+++

Detach a Song from given Album.

  ```
  DELETE /api/albums/{albumid}/songs
  ```

Example Body Params:
```json
{
    "songs": [
        "1607d150-861c-4782-8c1b-abe58254373b"
    ] 
}
```

Response is `204 NoContent`