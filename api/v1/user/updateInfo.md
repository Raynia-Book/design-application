# Updaet Info

Update an Account for the user.

**URL** : `/api/v1/user/`

**Method** : `PUT`

**Auth required** : Yes

**Permissions required** : User is a owner of the account

**Data constraints**

```json
{
    "imagePath": "[Url format]",
    "email": "[email format]",
    "name": "[unicode 64 chars max]",
    "password": "[password constraint]",
}
```

**Data example** Partial field allow.

```json
{
    "imagePath": "https://google.com",
    "name": "name",
    "password": "pAs#@woR094",
}
```

## Success Responses

**Condition** : Data provided is valid and User is Authenticated.

**Code** : `200 OK`

**Content example** : Response will reflect back the updated information.

```json
{
    "id": 1234,
    "imagePath": "https://google.com",
    "email": "test@gmail.com",
    "name": "name",
    "password": "pAs#@woR094",
}
```

## Error Response

**Condition** : If provided data is invalid, e.g. a name field is too long.

**Code** : `400 BAD REQUEST`

**Content example** :

```json
{
    "first_name": [
        "Please provide valid data.",
    ]
}
```

## Notes

* Endpoint will ignore irrelevant and read-only data such as parameters that
  don't exist, or fields that are not editable like `id` or `email`.