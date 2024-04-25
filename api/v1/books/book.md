# Instruction For Book Api Version 1
```
BASE /api/v1/books
```
## POST /?q=text

### request
q is search for author publisher and bookName

```
{
    subject: string[],
    level: string[],
    bookContentType: number,
    bookProblemType: number,
    pageNumber: number Example: 0,
    size: number Example: 5
}
```

### process
SELECT * FROM 

### response
```
{
    imagePath: string,
    bookType: string[],
    name: string,
    price: number,
    minLevel: number,
    pageNumber: number Example: 5
}
```

| Attribute    | Description |
| -------- | ------- |
| imagePath  | An url of image for fetching image.  |
| bookType |   An array of types of book. Examples: ['เนื้อหา', 'โจทย์']. |
| name    | A name of a book.    |
| price    | A price of a book.    |
| minLevel    | A min level required for the book.    |
| pageNumber    |  A number of last limit for pagination purpose.  |

## GET s/book/:id
{

}