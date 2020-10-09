+++
date = "2000-01-01T00:00:00+00:02"
title = "Artist Songs"
description = "Handle, edit and manipulate a Artist Songs"
toc = true
+++

## List related Songs

```
GET /api/artists/{artistID}/songs
```

*Response*
```json
[
    {
        "id": "68a27f48-4394-4edd-99f6-8f467013166b",
        "artworkId": "93713831-8116-47cc-895a-e325a4d96911",
        "composerName": "Red Hot Chili Peppers",
        "discNumber": 1,
        "durationInMillis": 20000,
        "isrc": "USQY51021557",
        "name": "Aeroplane",
        "releaseDate": "1996-03-14T10:27:31Z",
        "trackNumber": 1,
        "scheduleInfo": null,
        "libraryInfo": null,
        "createdAt": "2020-10-09T08:42:40.897687+02:00",
        "updatedAt": "2020-10-09T08:42:40.897687+02:00"
    }
]
```