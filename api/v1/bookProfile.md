# RESTAPIDocs For Book Profile Version 1

This is an api specification for Book Profile Version 1.

## Open Endpoints

Open endpoints require no Authentication.

* [Show Books](books/showBooks.md) : `POST /api/v1/books`
* [Show Book](books/showBook.md) : `GET /api/v1/books/book/:id`

## Endpoints that require Authentication

Closed endpoints require a valid Token to be included in the header of the
request. A Token can be acquired from Sign In and Sign Up.

### Regular User

Each endpoint manipulates information of the book:

* [Put Book](books/putBook.md) : `PUT /api/v1/books/book/put/:id`

### Publisher User

Endpoints for deleteing and manipulating the Accounts that the Authenticated User
has permissions to access.

* [Add Book](books/addBook.md) : `POST /api/v1/books/book/add`
* [Delete Book](books/deleteBook.md) : `DELETE /api/v1/books/book/delete/:id`