---
title: "Delete a knowledge base"
source_url: https://marketplace.gohighlevel.com/docs/ghl/knowledge-base/delete-knowledge-base
version: v3
method: DELETE
endpoint: https://services.leadconnectorhq.com/knowledge-bases/:knowledgeBaseId
---
# Delete a knowledge base

```
DELETE https://services.leadconnectorhq.com/knowledge-bases/:knowledgeBaseId
```


Delete a knowledge base

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

**knowledgeBaseId** stringrequired

## Responses

- 200
- 400
- 401

Knowledge base deleted successfully

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
curl -L -X DELETE 'https://services.leadconnectorhq.com/knowledge-bases/:knowledgeBaseId' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

knowledgeBaseId — pathrequired

Authorization — headerrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!