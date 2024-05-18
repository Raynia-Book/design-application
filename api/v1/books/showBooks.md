# Show Books

This is for showing books in the Home Page.

**URL** : `/api/v1/books/`

**Method** : `POST`

**Auth required** : NO

**Permissions required** : None

**Data constraints**

```json
{
    "q": "google",
    "sort": "asc",
    "subject": ["คณิตศาสตร์"],
    "level": [1, 2, 3],
    "bookType": ["เนื้อหา", "โจทย์"],
    "contentQuadrant": 2,
    "problemQuadrant": 1,
    "pageNumber": 0,
    "size": 5
}
```

Note that `size` and `pageNumber` are **required** for pagination.

**Data examples**

Partial data is allowed.

```json
{
    "bookType": ["เนื้อหา"],
    "contentQuadrant": 2,
    "pageNumber": 0,
    "size": 3
}
```

## Success Responses

**Condition** : Data provided is valid.

**Code** : `200 OK`

**Content example** : Response will send back a data of books that required for Home Page:

```json
[
    {
        "coverPath": "https://google.com",
        "bookType": ["เนื้อหา"],
        "name": "Biology",
        "price": 123,
        "minLevel": 4,
        "pageNumber": 0
    },
    {
        "coverPath": "https://facebook.com",
        "bookType": ["เนื้อหา"],
        "name": "Chemistry",
        "price": 133,
        "minLevel": 4,
        "pageNumber": 1
    },
    {
        "coverPath": "https://x.com",
        "bookType": ["เนื้อหา"],
        "name": "Science",
        "price": 143,
        "minLevel": 1,
        "pageNumber": 2
    }
]
```

## Error Response

**Condition** : If not provide `pageNumber` or `size`:

**Code** : `400 BAD REQUEST`

**Content example** :

```json
{
    "message": [
        "Please provide pageNumber and size",
    ]
}
```
### Or

**Condition** : If not provide `bookType` does not match with `contentQuadrant` and `problemQuadrant`:

**Code** : `400 BAD REQUEST`

**Content example** :

```json
{
    "message": [
        "Please provide matched bookType",
    ]
}
```

## Notes

* All field can get more infomation in [Books Database](../../../database/README.md)

