+++
date = "2000-01-01T00:00:00+00:02"
title = "Album Tracks"
description = "Handle, edit and manipulate a Tracks of a Album"
toc = true
+++

**Alert** Albums are working with `Tracks` not with `Songs`. Under the hood it's the same entity.

## Create or Link Track with Album

This endpoint allows you to Link an `Album -> Song` relation or create a new Artist with Relation. If no `id` is provided a new Album will be created.

```
POST /api/albums/{albumID}/tracks
```

If the Track you want to link exists you can *POST*

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

## List related Tracks

```
GET /api/albums/{albumID}/tracks
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
