---
title: "Update a knowledge base"
source_url: https://marketplace.gohighlevel.com/docs/ghl/knowledge-base/update-knowledge-base
version: v3
method: PUT
endpoint: https://services.leadconnectorhq.com/knowledge-bases/:id
---
# Update a knowledge base

```
PUT https://services.leadconnectorhq.com/knowledge-bases/:id
```


Update a knowledge base

### Requirements

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request

### Header Parameters

**Authorization** stringrequired

Access Token

Example: Bearer 9c48df2694a849b6089f9d0d3513efe

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**id** stringrequired

- application/json

### Body **required**

**name** string

field to update the name of the knowledge base

**description** string

field to update the description of the knowledge base

## Responses

- 200
- 400
- 401

Knowledge base updated successfully

- application/json

- Schema
- Example (auto)

**Schema**

**success** booleanrequired

```json
{
  "success": true
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

## Share your feedback

★★★★★

#### Authorization: Authorization

```
name: Authorizationtype: httpscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L -X PUT 'https://services.leadconnectorhq.com/knowledge-bases/:id' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "name": "string",
  "description": "string"
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

id — pathrequired

Authorization — headerrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "name": "string",
  "description": "string"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!