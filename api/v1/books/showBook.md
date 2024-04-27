# Show Book

This is for showing book data in the specify book page.

**URL** : `/api/v1/books/book/:id/`

**Url Parameter**: 

| Url Parameter    | Description |
| -------- | ------- |
| id  | For quering a book data by id.  |


**Method** : `GET`

**Auth required** : NO

**Permissions required** : None

## Success Responses

**Condition** : Id provided is valid.

**Code** : `200 OK`

**Content example** : Response will send back a data of books that required for Book Page:

```json
{
    "imagePath": ["https://google.com"],
    "bookType": ["เนื้อหา", "โจทย์"],
    "name": "Biology",
    "price": 123,
    "minLevel": 4,
    "subject": ["ชีวะวิทยา", "วิทยศาสตร์"],
    "publisher": "Cid Choky",
    "author": "Cid Choky",
    "description": "abc",
    "sourceUrl": "http://lazada.com",
    "content": {
        "explainTypes": {
            "T": 12,
            "D": 28,
            "P": 60
        },
        "completeScore": 2,
        "deptScore": 3,
        "contentQuadrant": 2
    },
    "problem": {
        "manyScore": 2,
        "answerScore": 2,
        "hardnessScore": 2,
        "problemQuadrant": 2
    },
    "physical": {
        "easyToReadScore": 3,
        "easyToUseScore": 2
    }
}
```

## Error Response

**Condition** : If there was no book available.

**Code** : `404 NOT FOUND`

**Content** : `{}`

## Notes

* All field can get more infomation in [Books Database](../../../database/README.md)

