# Add Book

This is for adding book data in the `Publisher` site.

**URL** : `/api/v1/books/book/:id`

**Url Parameter**: 

| Url Parameter    | Description |
| -------- | ------- |
| id  | For adding a book data by id.  |

**Method** : `POST`

**Auth required** : YES

**Permissions required** : None

**Data constraints**

Note that ((`content` and `explainTypes`) or `problem`) are **required**.

**Data examples**

Partial data is allowed.

```json
{
    "content": {
        "length": 3,
        "technic": 2,
        "explain": 3,
        "example": 3,
    },
    "explainTypes": {
        "T": 12,
        "D": 28,
        "P": 60
    },
    "problem": {
        "analyze": true,
        "applied": false,
        "knowledgeTest": false,
        "answer": 2,
        "complexNumber": 3,
        "step": 2,
        "analyzeHardness": 2,
        "technicalTermDifficulty": 2,
    }
}
```

## Success Responses

**Condition** : Id provided is valid.

**Code** : `200 OK`

**Content example** : Response will reflect back that the book is added:

```json
{
    "message": [
        "Book Added"
    ]
}
```

## Error Response

**Condition** : If not provide `id` have `bookType` does not match with `content` and `problem`:

**Code** : `400 BAD REQUEST`

**Content example** :

```json
{
    "message": [
        "Please provide matched data with bookType",
    ]
}
```

### Or

**Condition** : Authorized User is not have `Publisher` permission.

**Code** : `403 FORBIDDEN`

**Content** : `{}`

## Notes

* All field can get more infomation in [Books Database](../../../database/README.md)

