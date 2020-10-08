+++
date = "2000-01-01T00:00:00+00:02"
title = "Album Attach Song"
description = "Endpoint to attach song to Album"
+++

Attach a Song to given Album.

  ```
  POST /api/albums/{albumid}/songs
  ```

You can use `SongId` to attach a single song or `songs` to attach many songs.

```json
{
    "songId": "823a18d1-6203-4e64-b16a-de2ae6876d62",
    "songs": ["823a18d1-6203-4e64-b16a-de2ae6876d62"]
}
```

Response is `204 NoContent`