+++
date = "2000-01-01T00:00:00+00:02"
title = "Album"
description = "Shows all available API Operatings for `album`"
toc = true
+++

## The Album Model

`copyright`: The copyright text.

`isComplete`: (Required) Indicates whether the album is complete.
        If true, the album is complete; otherwise, it is not. An album is complete if it contains all its tracks and songs.
        default is false

`isSingle`: (Required) Indicates whether the album contains a single song.
 default is false

 `name`: (Required) The localized name of the album.

 `recordLabel`: (Required) The name of the record label for the album.

`releaseDate`: (Required) The release date of the album in YYYY-MM-DD format.

`trackCount`: (Required) The number of tracks.

```go
type Album struct {
		ID          uuid.UUID      `json:"id"`
        Copyright   string         `json:"copyright"`                         
        IsComplete  bool           `json:"isComplete"`
        IsSingle    bool           `json:"isSingle"`
        Name        string         `json:"name"`
        RecordLabel string         `json:"recordLabel"`
        ReleaseDate time.Time      `json:"releaseDate"`
		TrackCount  int            `json:"trackCount"`
		CreatedAt   time.Time      `json:"createdAt"`
		UpdatedAt   time.Time      `json:"updatedAt"`
	}
```


## Create a new Album.

```
POST /api/albums
```

Example Body Params:
```json
{
    "copyright": "",
    "name": "One Hot Minute 2",
    "recordLabel": "Warner Bros.",
    "isComplete": false,
    "isSingle": false,
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
}
```

## Find one Album

  ```
  GET /api/albums/{id}
  ```

*Response*
```json
{
    "id": "7833d476-d89b-48d8-b232-dd3db7013391",
    "copyright": "",
    "isComplete": false,
    "isSingle": false,
    "name": "One Hot Minute",
    "recordLabel": "Warner Bros.",
    "releaseDate": "0001-01-01T00:00:00Z",
    "trackCount": 0,
}
```

## Lists all Albums

  ```
  GET /api/albums
  ```


*Response*

```json {linenos=table}
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
    },
    {
        "id": "b1af16e3-4cad-4a81-a35a-9c6208f57195",
        "copyright": "",
        "isComplete": false,
        "isSingle": false,
        "name": "One Hot Minute 2",
        "recordLabel": "Warner Bros.",
        "releaseDate": "0001-01-01T00:00:00Z",
        "trackCount": 0,
    }
]
```

## Delete one Album

  ```
  DELETE /api/albums/{id}
  ```

Returns `204 No Content`