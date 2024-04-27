# Add Book

This is for adding book data in the `Publisher` site.

**URL** : `/api/v1/books/book/`

**Method** : `POST`

**Auth required** : YES

**Permissions required** : User is a `Publisher`.

**Data constraints**

Note that ((`content` and `explainTypes`) or `problem`), `simpleBookData`and `physical` are **required**.

**Data examples**

Partial data is allowed.

```json
{
    "simpleBookData": {
        "name": "Biology",
        "author": "Cid Choky",
        "price": 12,
        "subject": ["วิทยาศาสตร์"],
        "minLevel": 1,
        "minTerm": 2,
        "maxLevel": 3,
        "maxTerm": 1,
        "imagePath": ["https://google.com"],
        "bookTypes": ["เนื้อหา", "โจทย์"],
        "description": "abc",
        "sourceUrl": "http://lazada.com"
    },
    "content": {
        "complete": 3,
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

    },
    "physical": {
        "surfaceCmW": 2.3,
        "surfaceCmH": 2.3,
        "weightG": 2.3,
        "deepCm": 2.3,
        "threadSewing": true,
        "glue": true,
        "flexibleRidge": true,
        "cover": 12,
        "gram": 12,
        "fontTyped": true,
        "fontSize": 21.2,
        "eyeCare": true,
        "blackWhite": true,
        "oneCharLineSpacing": true,
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

**Condition** : If not provide `bookType` does not match with `content` and `problem`:

**Code** : `400 BAD REQUEST`

**Content example** :

```json
{
    "message": [
        "Please provide matched bookType",
    ]
}
```

### Or

**Condition** : Authorized User is not have `Publisher` permission.

**Code** : `403 FORBIDDEN`

**Content** : `{}`

## Notes

* All field can get more infomation in [Books Database](../../../database/README.md)

