+++
date = "2000-01-01T00:00:00+00:02"
title = "Album List"
description = "Endpoint to list all Albums"
+++

Lists all Albums

  ```
  GET /api/albums
  ```


Example Response Body:

```json {linenos=table}
[
    {
        "id": "7833d476-d89b-48d8-b232-dd3db7013391",
        "artists": [
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
        ],
        "copyright": "",
        "isComplete": false,
        "isSingle": false,
        "name": "One Hot Minute",
        "recordLabel": "Warner Bros.",
        "releaseDate": "0001-01-01T00:00:00Z",
        "trackCount": 0,
        "tracks": []
    },
    {
        "id": "b1af16e3-4cad-4a81-a35a-9c6208f57195",
        "artists": [],
        "copyright": "",
        "isComplete": false,
        "isSingle": false,
        "name": "One Hot Minute 2",
        "recordLabel": "Warner Bros.",
        "releaseDate": "0001-01-01T00:00:00Z",
        "trackCount": 0,
        "tracks": []
    }
]
```