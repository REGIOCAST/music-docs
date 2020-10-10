+++
date = "2000-01-01T00:00:00+00:02"
title = "Artist Songs"
description = "Handle, edit and manipulate a Artist Songs"
toc = true
+++

## Create or Link Song with Artist

This endpoint allows you to Link a `Song -> Album` relation or create a new Artist with Relation. If no `id` is provided a new Song will be created.

```
POST /api/artists/{artistID}/songs
```

If the Song you want to link exists you can *POST*

```json
{
    "id": "1607d150-861c-4782-8c1b-abe58254373b"
}
```

If you want to create a new Song:

*Request*
```json
    {
        "composerName": "Red Hot Chili Peppers",
        "discNumber": 1,
        "durationInMillis": 20000,
        "isrc": "USQY51021557",
        "name": "Aeroplane",
        "releaseDate": "1996-03-14T10:27:31Z"
    }
```

*Response*
```json
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
```


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

## Delete Song Relation

You are not allowed to `DELETE` the Song at this endpoint.
This endpoint handles the Relationship between an existing Song and an Artist.

```
GET /api/artists/{artistID}/songs/{songID}
```

*Response* is `204 No Content`