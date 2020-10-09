+++
date = "2000-01-01T00:00:00+00:02"
title = "Artist Albums"
description = "Handle, edit and manipulate a Artist Albums"
toc = true
+++


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