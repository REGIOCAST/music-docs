+++
date = "2000-01-01T00:00:00+00:02"
title = "Artist Find"
description = "Endpoint to find an Artists"
+++

Find Artist by ID

```
GET /api/artists/{id}
```

By default all members of an artist are preloaded.

```json
{
    "id": "33244a4b-dfc5-4317-9039-d2cebfb12782",
    "members": [
        {
            "id": "0ba86437-61bf-4f25-905a-526a76cb09a4",
            "name": "Michael „Flea“ Balzary",
            "createdAt": "2020-10-06T13:32:24.213784+02:00",
            "updatedAt": "2020-10-06T13:32:24.213784+02:00"
        },
        {
            "id": "13d2f8a6-4f5d-45c6-b10c-3309f26fdf63",
            "name": "Chad Smith",
            "createdAt": "2020-10-06T13:32:24.213784+02:00",
            "updatedAt": "2020-10-06T13:32:24.213784+02:00"
        },
        {
            "id": "1d1809df-cf05-4604-97e8-6ff3de542f6a",
            "name": "Michael „Flea“ Balzary",
            "createdAt": "2020-10-06T13:32:24.213784+02:00",
            "updatedAt": "2020-10-06T13:32:24.213784+02:00"
        },
        {
            "id": "3a456127-df78-4d7d-902f-b66b86fb9c44",
            "name": "Anthony Kiedis",
            "createdAt": "2020-10-06T13:32:24.213784+02:00",
            "updatedAt": "2020-10-06T13:32:24.213784+02:00"
        },
        {
            "id": "609daad8-4052-4173-840c-1e72cc87d180",
            "name": "Chad Smith",
            "createdAt": "2020-10-06T13:32:24.213784+02:00",
            "updatedAt": "2020-10-06T13:32:24.213784+02:00"
        },
        {
            "id": "836de2fb-cb0c-4299-8cc8-e13a074d196e",
            "name": "Anthony Kiedis",
            "createdAt": "2020-10-06T13:32:24.213784+02:00",
            "updatedAt": "2020-10-06T13:32:24.213784+02:00"
        },
        {
            "id": "8efff465-78ca-45ee-b407-f00949da0032",
            "name": "John Frusciante",
            "createdAt": "2020-10-06T13:32:24.213784+02:00",
            "updatedAt": "2020-10-06T13:32:24.213784+02:00"
        },
        {
            "id": "cd9c7e6a-806e-4d1a-b0f4-bdae9552effd",
            "name": "John Frusciante",
            "createdAt": "2020-10-06T13:32:24.213784+02:00",
            "updatedAt": "2020-10-06T13:32:24.213784+02:00"
        }
    ],
    "albums": [],
    "name": "Red Hot Chili Peppers",
    "createdAt": "2020-10-06T13:32:24.213112+02:00",
    "updatedAt": "2020-10-06T13:32:24.214982+02:00"
}
```