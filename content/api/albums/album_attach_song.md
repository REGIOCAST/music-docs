+++
date = "2000-01-01T00:00:00+00:02"
title = "Album Attach Song"
description = "Endpoint to attach song to Album"
+++

Attach a Song to given Album.

  ```
  POST /api/albums/{albumid}/songs
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