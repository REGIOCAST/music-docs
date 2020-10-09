+++
date = "2000-01-01T00:00:00+00:02"
title = "Song"
description = "Shows all available API Operatings for `song`"
toc = true
+++

Shows all available API Operatings for `song`

## Create a new Song

```
POST /api/songs
```

*Request*
```json
{
    "composerName": "Red Hot Chili Peppers",
    "discNumber": 1,
    "durationInMillis": 20000,
    "isrc": "USQY51021557",
    "name": "Aeroplane",
    "releaseDate": "1996-03-14T10:27:31+00:00",
    "trackNumber": 1
}
```


*Response*
```json
{
    "id": "b38db132-c4b7-4123-8107-abbb88b7d921",
    "composerName": "Red Hot Chili Peppers",
    "discNumber": 1,
    "durationInMillis": 20000,
    "isrc": "USQY51021557",
    "name": "Aeroplane",
    "releaseDate": "1996-03-14T10:27:31Z",
    "trackNumber": 1,
    "albumId": "00000000-0000-0000-0000-000000000000",
    "album": null,
    "createdAt": "2020-10-06T12:32:58.473323+02:00",
    "updatedAt": "2020-10-06T12:32:58.473323+02:00"
}
```

## Find Song by ID

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

## Lists all Songs

```
GET /api/songs
```

```json
[
    {
        "id": "b38db132-c4b7-4123-8107-abbb88b7d921",
        "composerName": "Red Hot Chili Peppers",
        "discNumber": 1,
        "durationInMillis": 20000,
        "isrc": "USQY51021557",
        "name": "Aeroplane",
        "releaseDate": "1996-03-14T10:27:31Z",
        "trackNumber": 1,
        "albumId": "00000000-0000-0000-0000-000000000000",
        "album": null,
        "createdAt": "2020-10-06T12:32:58.473323+02:00",
        "updatedAt": "2020-10-06T12:32:58.473323+02:00"
    }
]
```

## Update a Song

```
   PATCH /api/songs/{id}
```

*Request*
```json
{
    "composerName": "updated ComposerName"
}
```

*Response*
```json
{
    "id": "b38db132-c4b7-4123-8107-abbb88b7d921",
    "composerName": "updated ComposerName",
    "discNumber": 1,
    "durationInMillis": 20000,
    "isrc": "USQY51021557",
    "name": "Aeroplane",
    "releaseDate": "1996-03-14T10:27:31Z",
    "trackNumber": 1,
    "albumId": "00000000-0000-0000-0000-000000000000",
    "album": null,
    "createdAt": "2020-10-06T12:32:58.473323+02:00",
    "updatedAt": "2020-10-06T12:35:17.546596+02:00"
}
```

## Deletes a song by its ID

```
DELETE /api/songs/{id}
```

Returns `204 No Content`