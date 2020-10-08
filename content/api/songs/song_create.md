+++
date = "2000-01-01T00:00:00+00:02"
title = "Song Create"
description = "Endpoint to create a new Song"
+++

Create a new Song.

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