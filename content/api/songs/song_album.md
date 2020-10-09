+++
date = "2000-01-01T00:00:00+00:02"
title = "Song Albums"
description = "Handle, edit and manipulate a Songs Albums"
toc = true
+++

## Create or Link Album with Song

This endpoint allows you to Link an `Album -> Song` relation or create a new Artist with Relation. If no `id` is provided a new Album will be created.

```
POST /api/songs/{songID}/albums
```

If the Album you want to link you can *POST*

```
{
    "id": "1607d150-861c-4782-8c1b-abe58254373b"
}
```

If you want to create a new Album:

*Request*
```
{
    "copyright": "",
    "isComplete": false,
    "isSingle": true,
    "name": "i am a single",
    "recordLabel": "",
    "releaseDate": "0001-01-01T00:00:00Z",
    "trackCount": 0,
}
```

*Response*
```
{
    "id": "132327e7-8613-425a-8500-3bbf7792f7c1",
    "copyright": "",
    "isComplete": false,
    "isSingle": true,
    "name": "i am a single",
    "recordLabel": "",
    "releaseDate": "0001-01-01T00:00:00Z",
    "trackCount": 0,
    "createdAt": "2020-10-09T11:23:12.888452+02:00",
    "updatedAt": "2020-10-09T11:23:12.888452+02:00"
}
```


## List related Albums

```
GET /api/songs/{songID}/albums
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
    },
    {
        "id": "132327e7-8613-425a-8500-3bbf7792f7c1",
        "copyright": "",
        "isComplete": false,
        "isSingle": true,
        "name": "i am a single",
        "recordLabel": "",
        "releaseDate": "0001-01-01T00:00:00Z",
        "trackCount": 0,
        "createdAt": "2020-10-09T11:23:12.888452+02:00",
        "updatedAt": "2020-10-09T11:23:12.888452+02:00"
    }
]
```


## Delete Album Relation

You are not allowed to `DELETE` the Album on this endpoint.
This endpoint handles the Relationship between an existing Album and a Song.

```
GET /api/songs/{songID}/albums/{albumID}
```

*Response* is `204 No Content`