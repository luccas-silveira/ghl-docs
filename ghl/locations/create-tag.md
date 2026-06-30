---
title: "Create Tag"
source_url: https://marketplace.gohighlevel.com/docs/ghl/locations/create-tag
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/locations/:locationId/tags
---
# Create Tag

```
POST https://services.leadconnectorhq.com/locations/:locationId/tags
```

Create tag

### Requirements

#### Scope(s)

`locations/tags.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**locationId** stringrequired

Location Id

Example: ve9EPM428h8vShlRW1KT

- application/json

### Body **required**

**name** stringrequired

Tag name

Example:`Tag`

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

**tag** object

**name** string

Example:`minim aliquip anim`

**locationId** string

Example:`ve9EPM428h8vShlRW1KT`

**id** string

Example:`flGwEuzsfJOia1i1ikRN`

```json
{
  "tag": {
    "name": "minim aliquip anim",
    "locationId": "ve9EPM428h8vShlRW1KT",
    "id": "flGwEuzsfJOia1i1ikRN"
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
name: Authorizationtype: httpscopes: locations/tags.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/locations/:locationId/tags' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "name": "Tag"
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

locationId — pathrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "name": "Tag"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!