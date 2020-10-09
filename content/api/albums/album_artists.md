+++
date = "2000-01-01T00:00:00+00:02"
title = "Album Artists"
description = "Handle, edit and manipulate a Artists of an Album"
toc = true
+++

## Create or Link Artist to Album

This endpoint allows you to Link an `Album -> Artist` relation or create a new Artist with Relation. If no `id` is provided a new Artist will be created.

```
POST /api/albums/{albumID}/artists
```

If the Artist you want to link exists you can *POST*

```json
{
    "id": "1607d150-861c-4782-8c1b-abe58254373b"
}
```

If you want to create a new Artist:

*Request*
```json
{
    "ipi": "withIpi",
    "isni": "withIsni",
    "sortName": "abca!",
    "name": "ultra performant artist!"
}
```

*Response*
```json
{
    "id": "572811a5-a202-470b-abd6-2e55ddc555e3",
    "ipi": "withIpi",
    "isni": "withIsni",
    "name": "ultra performant artist!",
    "sortName": "abca!",
    "createdAt": "2020-10-09T12:50:19.450452+02:00",
    "updatedAt": "2020-10-09T12:50:19.450452+02:00"
}
```

## List related Artists

```
GET /api/albums/{albumID}/artists
```

*Response*
```json
[
    {
        "id": "1607d150-861c-4782-8c1b-abe58254373b",
        "ipi": "",
        "isni": "",
        "name": "Red Hot Chili Peppers",
        "sortName": "",
        "createdAt": "2020-10-08T12:29:17.910156+02:00",
        "updatedAt": "2020-10-08T12:29:17.912486+02:00"
    },
    {
        "id": "50d872b8-a7a2-44ce-bdfa-514bc76bd960",
        "ipi": "",
        "isni": "",
        "name": "ultra performant artist!",
        "sortName": "ultra performant artist!",
        "createdAt": "2020-10-09T12:43:31.276382+02:00",
        "updatedAt": "2020-10-09T12:43:31.276382+02:00"
    },
    {
        "id": "572811a5-a202-470b-abd6-2e55ddc555e3",
        "ipi": "withIpi",
        "isni": "withIsni",
        "name": "ultra performant artist!",
        "sortName": "abca!",
        "createdAt": "2020-10-09T12:50:19.450452+02:00",
        "updatedAt": "2020-10-09T12:50:19.450452+02:00"
    },
    {
        "id": "b878ddf3-8c9e-42d5-8c73-bd7f2fd5e530",
        "ipi": "",
        "isni": "",
        "name": "Anthony Kiedis",
        "sortName": "",
        "createdAt": "2020-10-08T12:29:17.911585+02:00",
        "updatedAt": "2020-10-08T12:29:17.911585+02:00"
    }
]
```


## Delete Artist Relation

You are not allowed to `DELETE` the Artist at this endpoint.
This endpoint handles the Relationship between an existing Album and a Artist.

```
GET /api/albums/{albumID}/artists/{artistID}
```

*Response* is `204 No Content`