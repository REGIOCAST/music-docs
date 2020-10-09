+++
date = "2000-01-01T00:00:00+00:02"
title = "Song Artwork"
description = "Handle, edit and manipulate a Songs Artwork"
+++

# List related Artwork

To keep the API consistent. This endpoint is returning `Array<Artwork>`. The max length is 1.

```
GET /api/songs/{songID}/artwork
```

*Response*
```json
[
    {
        "id": "db457d3c-4610-484c-8ac0-e59041bf547c",
        "name": "iris-refactor.jpg",
        "mimeType": "image/jpeg",
        "size": 62854,
        "bucket": "your.s3bucket.tld",
        "publicPath": "https://s3-eu-west-1.amazonaws.com/your.s3bucket.tld/1id8BSnrT51nZ0itggEocutlHWN/iris-refactor.jpg",
        "alt": "",
        "width": 1031,
        "height": 506,
        "isAnimated": false,
        "duration": 0,
        "createdAt": "2020-10-09T08:46:13.233113+02:00",
        "updatedAt": "2020-10-09T08:46:13.233113+02:00"
    }
]
```


# Upload a new Artwork for given Song

Request must be of type `form-data` and must contain `file`. You can append your Form with `alt` to create a alt-tag for the Artwork on-the-fly.

```
POST /api/songs/{songID}/artwork
```

Attributes like `mimeType`, `size`, `width` and `height` are extracted from the buffer.

*Response*
```json
{
    "id": "db457d3c-4610-484c-8ac0-e59041bf547c",
    "name": "iris-refactor.jpg",
    "mimeType": "image/jpeg",
    "size": 62854,
    "bucket": "your.s3bucket.tld",
    "publicPath": "https://s3-eu-west-1.amazonaws.com/your.s3bucket.tld/1id8BSnrT51nZ0itggEocutlHWN/iris-refactor.jpg",
    "alt": "",
    "width": 1031,
    "height": 506,
    "isAnimated": false,
    "duration": 0,
    "createdAt": "2020-10-09T08:46:13.233113+02:00",
    "updatedAt": "2020-10-09T08:46:13.233113+02:00"
}
```