+++
date = "2000-01-01T00:00:00+00:02"
title = "Album Attach Artist"
description = "Endpoint to attach artist to Album"
+++

Attach an Artist to given Album.

  ```
  POST /api/albums/{albumid}/artists
  ```

Example Body Params:
```json
{
    "artists": [
        "1607d150-861c-4782-8c1b-abe58254373b"
    ] 
}
```

Response is `204 NoContent`