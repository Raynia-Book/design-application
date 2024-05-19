# Get Pdf

This is for downloading pdf.

**URL** : `/api/v1/file/:filename/`

**Url Parameter**:

| Url Parameter    | Description |
| -------- | ------- |
| filename  | For downloading a file by filename.  |


**Method** : `GET`

**Auth required** : NO

**Permissions required** : None

## Success Responses

**Condition** : Data provided is valid.

**Code** : `200 OK`

**Header example**: Content-Disposition attachment; filename="2024-04-27T17:50:04.811Z"

**Content example** : Response will send back an `Blob` of file:

## Error Response

**Condition** : If there was no filename available.

**Code** : `404 NOT FOUND`

**Content** : `{}`