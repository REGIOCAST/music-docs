+++
date = "2000-01-01T00:00:00+00:02"
title = "Artist Members"
description = "Handle, edit and manipulate a Artists Members"
toc = true
+++

## Create or Link Member with Artist

This endpoint allows you to Link an `Member -> Album` relation or create a new Artist with Relation. If no `id` is provided a new Member/Artist will be created.

```
POST /api/artists/{artistID}/members
```

If the Member you want to link exists you can *POST*

```json
{
    "id": "1607d150-861c-4782-8c1b-abe58254373b"
}
```

If you want to create a new Member:

*Request*
```json
{
        "ipi": "",
        "isni": "",
        "name": "Awesome brady",
        "sortName": "Awesome brady"
    }
```

*Response*
```json
{
        "id": "6c3674d9-9b69-405a-bdfc-b1d6494803c3",
        "ipi": "",
        "isni": "",
        "name": "Awesome brady",
        "sortName": "Awesome brady",
        "createdAt": "2020-10-08T16:56:47.726192+02:00",
        "updatedAt": "2020-10-08T16:56:47.727517+02:00"
}
```

## List related Members

```
GET /api/artists/{artistID}/members
```

*Response*
```json
[
    {
        "id": "6c3674d9-9b69-405a-bdfc-b1d6494803c3",
        "ipi": "",
        "isni": "",
        "name": "Awesome brady",
        "sortName": "Awesome brady",
        "createdAt": "2020-10-08T16:56:47.726192+02:00",
        "updatedAt": "2020-10-08T16:56:47.727517+02:00"
    }
]
```