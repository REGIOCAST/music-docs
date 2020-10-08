+++
date = "2000-01-01T00:00:00+00:02"
title = "Artist Create"
description = "Endpoint to create a new Artist"
+++

Create a new Artist.

```
POST /api/artists
```

*Request*
```json
{
    "name": "Red Hot Chili Peppers",
}
```

*Response*
```json
{
    "id": "33244a4b-dfc5-4317-9039-d2cebfb12782",
    "name": "Red Hot Chili Peppers",
    "createdAt": "2020-10-06T13:32:24.213112+02:00",
    "updatedAt": "2020-10-06T13:32:24.214982+02:00"
}
```

This Query will just create a new Artist (Band), but sometimes you want to create the entire band at once. You can use `Upsert` for this.

All Band members will be created and the relations will be auto-generated. Example:

*Request*
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

*Response* 
```json
{
    "id": "33244a4b-dfc5-4317-9039-d2cebfb12782",
    "members": [
        {
            "id": "836de2fb-cb0c-4299-8cc8-e13a074d196e",
            "name": "Anthony Kiedis",
            "createdAt": "2020-10-06T13:32:24.213784+02:00",
            "updatedAt": "2020-10-06T13:32:24.213784+02:00"
        },
        {
            "id": "0ba86437-61bf-4f25-905a-526a76cb09a4",
            "name": "Michael „Flea“ Balzary",
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
            "id": "cd9c7e6a-806e-4d1a-b0f4-bdae9552effd",
            "name": "John Frusciante",
            "createdAt": "2020-10-06T13:32:24.213784+02:00",
            "updatedAt": "2020-10-06T13:32:24.213784+02:00"
        }
    ],
    "name": "Red Hot Chili Peppers",
    "createdAt": "2020-10-06T13:32:24.213112+02:00",
    "updatedAt": "2020-10-06T13:32:24.214982+02:00"
}
```