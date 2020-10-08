+++
date = "2000-01-01T00:00:00+00:02"
title = "Artwork Create"
description = "Endpoint to create a new Artwork"
+++

Create a new Artwork.
```
*POST* /api/artworks
```

Allows to Upload a `Artwork` to the Service. Request has to be a `multipart/form-data` req.

`form-data`:
- file **the actual file**
- alt **alt name of the file**

**Note:** Filenames are URI encoded by default, to reduce possible user mistakes.

*Response*
```json
{
    "id": "f7640b4e-7391-43cc-ae86-716c04d15b01",
    "name": "Screenshot 2020-10-07 at 09.23.53.png",
    "mimeType": "image/png",
    "size": 4759480,
    "bucket": "storage.delivc.com",
    "publicPath": "https://s3-eu-west-1.amazonaws.com/storage.delivc.com/1iYCDvVAta4SHdQlgi9Ty1nyqoR/Screenshot_2020-10-07_at_09.23.53.png",
    "alt": "lalaland",
    "width": 2880,
    "height": 1800,
    "isAnimated": false,
    "duration": 0,
    "createdAt": "2020-10-07T14:50:23.269502+02:00",
    "updatedAt": "2020-10-07T14:50:23.269502+02:00"
}
```
