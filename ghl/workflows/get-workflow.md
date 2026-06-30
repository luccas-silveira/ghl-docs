---
title: "Get Workflow"
source_url: https://marketplace.gohighlevel.com/docs/ghl/workflows/get-workflow
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/workflows
---
# Get Workflow

```
GET https://services.leadconnectorhq.com/workflows/
```


Get Workflow

### Requirements

#### Scope(s)

`workflows.readonly`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Query Parameters

**locationId** stringrequired

Example: ve9EPM428h8vShlRW1KT

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

**workflows** object\[\]

Array \[\
\
**id** string\
\
Example:`78559bb3-b920-461e-b010-7b2a2816d2a9`\
\
**name** string\
\
Example:`First Workflow`\
\
**status** string\
\
Example:`draft`\
\
**version** number\
\
Example:`2`\
\
**createdAt** string\
\
Example:`2021-05-26T11:33:49.000Z`\
\
**updatedAt** string\
\
Example:`2021-05-26T11:33:49.000Z`\
\
**locationId** string\
\
Example:`eBG6WapS3v4ZqwA45MTxtYJ`\
\
\]

```json
{
  "workflows": [\
    {\
      "id": "78559bb3-b920-461e-b010-7b2a2816d2a9",\
      "name": "First Workflow",\
      "status": "draft",\
      "version": 2,\
      "createdAt": "2021-05-26T11:33:49.000Z",\
      "updatedAt": "2021-05-26T11:33:49.000Z",\
      "locationId": "eBG6WapS3v4ZqwA45MTxtYJ"\
    }\
  ]
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
name: Authorizationtype: httpscopes: workflows.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/workflows/' \
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

locationId — queryrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!