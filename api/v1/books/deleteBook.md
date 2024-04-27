# Delete Book

This is for showing book data.

**URL** : `/api/v1/books/book/:id/`

**Url Parameter**:

| Url Parameter    | Description |
| -------- | ------- |
| id  | For deleting a book data by id.  |


**Method** : `DELETE`

**Auth required** : YES

**Permissions required** : User is a Publisher of the book.

## Success Responses

**Condition** : Id provided is valid.

**Code** : `200 OK`

**Content example** : Response will reflect back that the book is deleted:

```json
{
    "message": [
        "Book Deleted"
    ]
}
```

## Error Response

**Condition** : If there was no Account available to delete.

**Code** : `404 NOT FOUND`

**Content** : `{}`

### Or

**Condition** : Authorized User is not Owner of book at URL.

**Code** : `403 FORBIDDEN`

**Content** : `{}`