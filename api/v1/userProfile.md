# RESTAPIDocs For User Profile Version 1

This is an api specification for User Profile Version 1.

## Open Endpoints

Open endpoints require no Authentication.

* [Sign In](user/signIn.md) : `POST /api/v1/user/sign-in`
* [Sign Up](user/signUp.md) : `POST /api/v1/user/sign-up`

## Endpoints that require Authentication

Closed endpoints require a valid Token to be included in the header of the
request. A Token can be acquired from the Sign In and Sign Up view above.

### Current User related

Each endpoint manipulates or displays information related to the User whose
Token is provided with the request:

* [Show Info](user/showInfo.md) : `GET /api/v1/user/showinfo`
* [Update Info](user/updateInfo.md) : `PUT /api/v1/user/updateinfo`
* [Delete Account](user/deleteAccount.md) : `DELETE /api/v1/user/delete`