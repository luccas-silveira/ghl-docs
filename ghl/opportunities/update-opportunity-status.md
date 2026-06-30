---
title: "Update Opportunity Status"
source_url: https://marketplace.gohighlevel.com/docs/ghl/opportunities/update-opportunity-status
version: v3
method: PUT
endpoint: https://services.leadconnectorhq.com/opportunities/:id/status
summary: "Update Opportunity Status"
---
# Update Opportunity Status

```
PUT https://services.leadconnectorhq.com/opportunities/:id/status
```


Update Opportunity Status

### Requirements

#### Scope(s)

`opportunities.write`

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

**id** stringrequired

Opportunity Id

Example: yWQobCRIhRguQtD2llvk

- application/json

### Body **required**

**status** stringrequired

New status for the opportunity

**Possible values:** \[`open`, `won`, `lost`, `abandoned`, `all`\]

Example:`open`

**lostReasonId** string

lost reason Id

Example:`CLu7BaljjqrEjBGKTNNe`

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

**succeded** booleandeprecated

Indicates whether the operation was successful. Deprecated — use `success` instead.

Example:`true`

**success** boolean

Indicates whether the operation was successful

Example:`true`

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
name: Authorizationtype: httpscopes: opportunities.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L -X PUT 'https://services.leadconnectorhq.com/opportunities/:id/status' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "status": "open",
  "lostReasonId": "CLu7BaljjqrEjBGKTNNe"
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

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "status": "open",
  "lostReasonId": "CLu7BaljjqrEjBGKTNNe"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!