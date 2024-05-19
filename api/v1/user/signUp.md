# Sign Up

Create an Account for the user.

**URL** : `/api/v1/user/`

**Method** : `POST`

**Auth required** : No

**Permissions required** : None

**Data constraints**

```json
{
    "email": "[email format]",
    "username": "[unicode 64 chars max]",
    "name": "[unicode 64 chars max]",
    "password": "[password constraint]",
}
```

**Data example** All fields must be sent.

```json
{
    "email": "test@gmail.com",
    "username": "username",
    "name": "name",
    "password": "pAs#@woR094",
}
```

## Success Response

**Condition** : If everything is OK and an Account didn't exist for this User.

**Code** : `201 CREATED`

**Content example**

```json
{
    "token": "93144b288eb1fdccbe46d6fc0f241a51766ecd3d"
}
```

## Error Responses

**Condition** : If Username already exists for User.

**Code** : `303 SEE OTHER`

**Content** : `{}`

### Or

**Condition** : If fields are missed.

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "name": [
        "This field is required."
    ]
}
```