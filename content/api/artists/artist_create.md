+++
date = "2000-01-01T00:00:00+00:02"
title = "Artist Create"
description = "Endpoint to create a new Artist"
+++

Create a new Artist with Sub-Artists.

```
POST /api/artists
```

As you see, you are able to nest sub-artists on this Endpoint. The API will create all nested relations by itself.

```json
{
    "name": "Red Hot Chili Peppers",
    "members": [
        {
            "name": "Anthony Kiedis"
        },
        {
            "name": "Michael „Flea“ Balzary"
        },
        {
            "name": "Chad Smith"
        },
        {
            "name": "John Frusciante"
        }
    ]
}
```

Example Response Body:

```json {linenos=table}
{
    "id": "1607d150-861c-4782-8c1b-abe58254373b",
    "members": [
        {
            "id": "b878ddf3-8c9e-42d5-8c73-bd7f2fd5e530",
            "members": null,
            "albums": null,
            "ipi": "",
            "isni": "",
            "name": "Anthony Kiedis",
            "sortName": "",
            "createdAt": "2020-10-08T12:29:17.911585+02:00",
            "updatedAt": "2020-10-08T12:29:17.911585+02:00"
        },
        {
            "id": "22188e6c-371f-4a83-bbaa-4d0ff1e1aeb3",
            "members": null,
            "albums": null,
            "ipi": "",
            "isni": "",
            "name": "Michael „Flea“ Balzary",
            "sortName": "",
            "createdAt": "2020-10-08T12:29:17.911585+02:00",
            "updatedAt": "2020-10-08T12:29:17.911585+02:00"
        },
        {
            "id": "e1e84cbd-017b-4fb8-b1e0-b698cdfb5341",
            "members": null,
            "albums": null,
            "ipi": "",
            "isni": "",
            "name": "Chad Smith",
            "sortName": "",
            "createdAt": "2020-10-08T12:29:17.911585+02:00",
            "updatedAt": "2020-10-08T12:29:17.911585+02:00"
        },
        {
            "id": "40e0b6e2-df93-4e77-8486-59a2c5d2e376",
            "members": null,
            "albums": null,
            "ipi": "",
            "isni": "",
            "name": "John Frusciante",
            "sortName": "",
            "createdAt": "2020-10-08T12:29:17.911585+02:00",
            "updatedAt": "2020-10-08T12:29:17.911585+02:00"
        }
    ],
    "albums": null,
    "ipi": "",
    "isni": "",
    "name": "Red Hot Chili Peppers",
    "sortName": "",
    "createdAt": "2020-10-08T12:29:17.910156+02:00",
    "updatedAt": "2020-10-08T12:29:17.912486+02:00"
}
```