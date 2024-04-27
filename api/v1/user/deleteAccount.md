# Delete Account

Delete the Account of the Authenticated User if they are Owner.

**URL** : `/api/v1/user/`

**Method** : `DELETE`

**Auth required** : YES

**Permissions required** : User is Account Owner

**Data** : `{}`

## Success Response

**Condition** : If the Account exists.

**Code** : `204 NO CONTENT`

**Content** : `{}`

## Error Responses

**Condition** : If there was no Account available to delete.

**Code** : `404 NOT FOUND`

**Content** : `{}`

### Or

**Condition** : Authorized User is not Owner of Account at URL.

**Code** : `403 FORBIDDEN`

**Content** : `{}`