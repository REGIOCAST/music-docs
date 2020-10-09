+++
date = "2000-01-01T00:00:00+00:02"
title = "Song Artists"
description = "Handle, edit and manipulate a Songs Artists"
toc = true
+++

## Create or Link Artist with Song

This endpoint allows you to Link an `Artist -> Song` relation or create a new Artist with Relation. If no `id` is provided a new Artist will be created.

```
POST /api/songs/{songID}/artists
```

If the Artist you want to link you can *POST*

```
{
    "id": "1607d150-861c-4782-8c1b-abe58254373b"
}
```

If you want to create a new Artist:

*Request*
```
{
    "ipi": "",
    "isni": "",
    "name": "Red Hot Chili Peppers",
    "sortName": ""
}
```

*Response*
```
{
    "id": "1607d150-861c-4782-8c1b-abe58254373b",
    "members": null,
    "albums": null,
    "ipi": "",
    "isni": "",
    "name": "Red Hot Chili Peppers",
    "sortName": "",
    "createdAt": "2020-10-08T12:29:17.910156+02:00",
    "updatedAt": "2020-10-08T12:29:17.912486+02:00"
}
```

## List related Artists

```
GET /api/songs/{songID}/artists
```

*Response*
```json
[
    {
        "id": "1607d150-861c-4782-8c1b-abe58254373b",
        "members": null,
        "albums": null,
        "ipi": "",
        "isni": "",
        "name": "Red Hot Chili Peppers",
        "sortName": "",
        "createdAt": "2020-10-08T12:29:17.910156+02:00",
        "updatedAt": "2020-10-08T12:29:17.912486+02:00"
    }
]
```


## Delete Artist Relation

You are not allowed to `DELETE` the Artist on this endpoint.
This endpoint handles the Relationship between an existing Artist and a Song.

```
GET /api/songs/{songID}/artists/{artistID}
```

*Response* is `204 No Content`