+++
date = "2000-01-01T00:00:00+00:02"
title = "Artist Albums"
description = "Handle, edit and manipulate a Artist Albums"
toc = true
+++

## Create or Link Album with Artist

This endpoint allows you to Link an `Artist -> Album` relation or create a new Artist with Relation. If no `id` is provided a new Album will be created.

```
POST /api/artists/{artistID}/albums
```

If the Album you want to link exists you can *POST*

```json
{
    "id": "1607d150-861c-4782-8c1b-abe58254373b"
}
```

If you want to create a new Album:

*Request*
```json
{
    "composerName": "Red Hot Chili Peppers",
    "discNumber": 1,
    "durationInMillis": 20000,
    "isrc": "USQY51021557",
    "name": "Another World",
    "releaseDate": "1996-03-14T10:27:31+00:00",
    "trackNumber": 1
}
```

*Response*
```json
{
    "id": "14c58899-b0f6-45f2-a7d0-ce18e2db61e6",
    "artworkId": "00000000-0000-0000-0000-000000000000",
    "composerName": "Red Hot Chili Peppers",
    "discNumber": 1,
    "durationInMillis": 20000,
    "isrc": "USQY51021557",
    "name": "Another World",
    "releaseDate": "1996-03-14T10:27:31Z",
    "trackNumber": 1,
    "scheduleInfo": null,
    "libraryInfo": null,
    "createdAt": "2020-10-09T12:23:38.011049+02:00",
    "updatedAt": "2020-10-09T12:23:38.011049+02:00"
}
```

## List related Albums

```
GET /api/artists/{artistID}/albums
```

*Response*
```json
[
    {
        "id": "7833d476-d89b-48d8-b232-dd3db7013391",
        "copyright": "",
        "isComplete": false,
        "isSingle": false,
        "name": "One Hot Minute",
        "recordLabel": "Warner Bros.",
        "releaseDate": "0001-01-01T00:00:00Z",
        "trackCount": 0,
        "createdAt": "2020-10-09T11:23:12.888452+02:00",
        "updatedAt": "2020-10-09T11:23:12.888452+02:00"
    }
]
```