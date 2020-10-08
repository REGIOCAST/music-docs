+++
date = "2000-01-01T00:00:00+00:02"
title = "Song Find"
description = "Endpoint to find a Song"
+++

Find Song by ID

```
GET /api/songs/{id}
```

Finds a song by it's ID. Album is always eager loaded.

```json
{
    "id": "701fedca-2754-45d9-97d1-74e8bdaee383",
    "composerName": "Red Hot Chili Peppers",
    "discNumber": 1,
    "durationInMillis": 20000,
    "isrc": "USQY51021557",
    "name": "Aeroplane",
    "releaseDate": "1996-03-14T10:27:31Z",
    "trackNumber": 1,
    "albumId": "8d59b381-484e-421e-99d0-1e331f1f810f",
    "album": {
        "id": "8d59b381-484e-421e-99d0-1e331f1f810f",
        "copyright": "",
        "isComplete": false,
        "isSingle": false,
        "name": "One Hot Minute",
        "recordLabel": "Warner Bros.",
        "releaseDate": "0001-01-01T00:00:00Z",
        "trackCount": 0,
        "tracks": null
    },
    "createdAt": "2020-10-06T12:41:06.709927+02:00",
    "updatedAt": "2020-10-06T12:41:06.709927+02:00"
}
```