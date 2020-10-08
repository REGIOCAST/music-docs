+++
date = "2000-01-01T00:00:00+00:02"
title = "Album Find"
description = "Endpoint to find Album"
+++

Find one Album

  ```
  GET /api/albums/{id}
  ```

Response
```json
{
    "id": "7833d476-d89b-48d8-b232-dd3db7013391",
    "copyright": "",
    "isComplete": false,
    "isSingle": false,
    "name": "One Hot Minute",
    "recordLabel": "Warner Bros.",
    "releaseDate": "0001-01-01T00:00:00Z",
    "trackCount": 0,
    "tracks": [
        {
            "id": "823a18d1-6203-4e64-b16a-de2ae6876d62",
            "composerName": "Red Hot Chili Peppers",
            "discNumber": 1,
            "durationInMillis": 20000,
            "isrc": "USQY51021557",
            "name": "Aeroplane",
            "releaseDate": "1996-03-14T10:27:31Z",
            "trackNumber": 1,
            "albumId": "7833d476-d89b-48d8-b232-dd3db7013391",
            "album": null,
            "scheduleInfo": null,
            "libraryInfo": null,
            "createdAt": "2020-10-07T16:40:05.53642+02:00",
            "updatedAt": "2020-10-07T16:40:05.53642+02:00"
        }
    ]
}
```