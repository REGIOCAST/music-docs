+++
date = "2000-01-01T00:00:00+00:02"
title = "Album Create"
description = "Endpoint to create a new Album"
+++

Create a new Album.

* Creates a album:
  ```
  POST /api/albums
  ```

Example Body Params:
```json
{
    "name": "One Hot Minute 2",
    "recordLabel": "Warner Bros."
} 
```

Example Response Body:

```json {linenos=table}
{
    "id": "b1af16e3-4cad-4a81-a35a-9c6208f57195",
    "copyright": "",
    "isComplete": false,
    "isSingle": false,
    "name": "One Hot Minute 2",
    "recordLabel": "Warner Bros.",
    "releaseDate": "0001-01-01T00:00:00Z",
    "trackCount": 0,
    "tracks": null
}
```