---
title: "Update Note"
source_url: https://marketplace.gohighlevel.com/docs/ghl/contacts/update-note
version: v3
method: PUT
endpoint: https://services.leadconnectorhq.com/contacts/:contactId/notes/:id
summary: "User Id of the note author"
---
# Update Note

```
PUT https://services.leadconnectorhq.com/contacts/:contactId/notes/:id
```


Update Note

### Requirements

#### Scope(s)

`contacts.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

Example: v3

### Path Parameters

**contactId** stringrequired

Contact Id

Example: ve9EPM428h8vShlRW1KT

**id** stringrequired

Note Id

Example: ocQHyuzHvysMo5N5VsXc

- application/json

### Body **required**

**userId** string

User Id of the note author

Example:`GCs5KuzPqTls7vWclkEV`

**body** string

Body content of the note

Example:`lorem ipsum`

**title** string

Title of the note

Example:`Follow-up summary`

**color** string

Hex color code for the note

Example:`#FFAA00`

**pinned** boolean

Whether the note is pinned

Example:`false`

## Responses

- 200
- 400
- 401
- 422

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**note** object

Note details

**id** string

Unique identifier of the note

Example:`HGPcayliwcdoUFzvbTok`

**body** string

Body content of the note

Example:`lorem ipsum`

**userId** string

User Id of the note author

Example:`TUcmRxWrjqzJS8EjkxNK`

**dateAdded** string

Date the note was added (ISO 8601 format)

Example:`2021-07-08T12:02:11.285Z`

**contactId** string

Contact Id associated with the note

Example:`TUcmRxWrjqzJS8EjkxNK`

**title** string

Title of the note

Example:`Follow-up summary`

**color** string

Hex color code for the note

Example:`#FFAA00`

**pinned** boolean

Whether the note is pinned

Example:`false`

```json
{
  "note": {
    "id": "HGPcayliwcdoUFzvbTok",
    "body": "lorem ipsum",
    "userId": "TUcmRxWrjqzJS8EjkxNK",
    "dateAdded": "2021-07-08T12:02:11.285Z",
    "contactId": "TUcmRxWrjqzJS8EjkxNK"
  }
}
```

Bad Request

- application/json

- Schema
- Example (auto)

**Schema**

**statusCode** number

Example:`400`

**message** string

Example:`Bad Request`

```json
{
  "statusCode": 400,
  "message": "Bad Request"
}
```

Unauthorized

- application/json

- Schema
- Example (auto)

**Schema**

**statusCode** number

Example:`401`

**message** string

Example:`Invalid token: access token is invalid`

**error** string

Example:`Unauthorized`

```json
{
  "statusCode": 401,
  "message": "Invalid token: access token is invalid",
  "error": "Unauthorized"
}
```

Unprocessable Entity

- application/json

- Schema
- Example (auto)

**Schema**

**statusCode** number

Example:`422`

**message** string\[\]

Example:`["Unprocessable Entity"]`

**error** string

Example:`Unprocessable Entity`

```json
{
  "statusCode": 422,
  "message": [\
    "Unprocessable Entity"\
  ],
  "error": "Unprocessable Entity"
}
```

## Share your feedback

★★★★★

#### Authorization: Authorization

```
name: Authorizationtype: httpscopes: contacts.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
```

- curl
- nodejs
- python
- php
- java
- go
- ruby
- powershell

- CURL

```bash
curl -L -X PUT 'https://services.leadconnectorhq.com/contacts/:contactId/notes/:id' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "userId": "GCs5KuzPqTls7vWclkEV",
  "body": "lorem ipsum",
  "title": "Follow-up summary",
  "color": "#FFAA00",
  "pinned": false
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

contactId — pathrequired

id — pathrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "userId": "GCs5KuzPqTls7vWclkEV",
  "body": "lorem ipsum",
  "title": "Follow-up summary",
  "color": "#FFAA00",
  "pinned": false
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!