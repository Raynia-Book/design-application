# Show Info

Get the details of the currently Authenticated User.

**URL** : `/api/v1/user/`

**Method** : `GET`

**Auth required** : YES

**Permissions required** : None

## Success Response

**Code** : `200 OK`

**Content examples**

```json
{
    "imagePath": "https://google.com",
    "name": "Joe",
    "username": "Bloggs",
    "isPublisher": true,
    "email": "thisisan@example.com"
}
```

## Error Responses

**Condition** : If there was no Account available to delete.

**Code** : `404 NOT FOUND`

**Content** : `{}`