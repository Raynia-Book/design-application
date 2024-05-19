# API Response Documentation

This documentation provides a list of possible API response codes, their meanings, and specific codes for different API endpoints.

## General Response Codes

### 1xx: Informational

- **100 Invalid Field**
  - Description: Invalid field provided. Please specify which field is invalid. (tell which field is invalid in description)

### 2xx: Success

- **200 Success**
  - Description: The request was successful.

### 3xx: Token Issues

- **300 Token Invalid**
  - Description: The provided token is invalid.
- **301 Token Expire**
  - Description: The token has expired.
- **302 No Permission**
  - Description: The user does not have permission to perform this action.

### 4xx: Client Errors

- **400 Not Found**
  - Description: The requested resource was not found. Please specify what was not found. (description บอกว่าอะไรnotfound)
- **500 Username Used**
  - Description: The username is already in use.
- **501 Email Used**
  - Description: The email is already in use.

### 5xx: Server Errors

- **600 Username and Password Incorrect**
  - Description: The username and password combination is incorrect.
- **700 Database Failed**
  - Description: There was a database error.
- **701 Call Service Failed**
  - Description: Failed to call the external service.

## Endpoint Specific Response Codes

### Show Books

- **Invalid Field (return field name, length, etc.)**
  - Description: One or more fields are invalid.
- **Success Send Books Data**
  - Description: Successfully sent books data.

### Show Book

- **Id Not Found**
  - Description: The specified book ID was not found.
- **Success Send Book Data**
  - Description: Successfully sent book data.

### Put Book

- **Token Invalid**
  - Description: The provided token is invalid.
- **Token Expire**
  - Description: The token has expired.
- **Invalid Field (return field name, length, etc.)**
  - Description: One or more fields are invalid.
- **Data Added Success**
  - Description: Data added successfully.

### Add Book

- **Invalid Field (return field name, length, etc.)**
  - Description: One or more fields are invalid.
- **Token Invalid**
  - Description: The provided token is invalid.
- **Token Expire**
  - Description: The token has expired.
- **No Permission**
  - Description: The user does not have permission to perform this action.
- **Book Added Return Id**
  - Description: Book added successfully, returning the book ID.

### Sign In

- **Success Return a Token**
  - Description: Successfully signed in, returning a token.
- **Username Password Incorrect**
  - Description: The username and password combination is incorrect.
- **Invalid Field**
  - Description: One or more fields are invalid.

### Show Info

- **Token Invalid**
  - Description: The provided token is invalid.
- **Token Expire**
  - Description: The token has expired.
- **Success Return Account Data**
  - Description: Successfully returned account data.

### Send File

- **Filename Not Found**
  - Description: The specified filename was not found.
- **Success File Sent**
  - Description: Successfully sent the file.

### Sign Up

- **Invalid Field (email invalid format)**
  - Description: One or more fields are invalid (e.g., email format).
- **Created Return a Token**
  - Description: Account created successfully, returning a token.
- **Email Used**
  - Description: The email is already in use.
- **Username Used**
  - Description: The username is already in use.

### Delete Book

- **Token Invalid**
  - Description: The provided token is invalid.
- **Token Expire**
  - Description: The token has expired.
- **No Permission**
  - Description: The user does not have permission to perform this action.
- **Delete Success**
  - Description: Book deleted successfully.

### Update Info

- **Token Invalid**
  - Description: The provided token is invalid.
- **Token Expire**
  - Description: The token has expired.
- **Invalid Field**
  - Description: One or more fields are invalid.
- **Update Success**
  - Description: Information updated successfully.
