---
title: "Get Widget Config"
source_url: https://marketplace.gohighlevel.com/docs/ghl/chat-widget/get-widget
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/chat-widget/public/config/:id
---
# Get Widget Config

```
GET https://services.leadconnectorhq.com/chat-widget/public/config/:id
```


Returns widget configuration by ID.

## Request

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

Example: v3

### Path Parameters

**id** stringrequired

The chat widget ID

Example: ve9EPM428h8vShlRWsss

### Query Parameters

**version** string

Default value:`2`

Example: 3

## Responses

- 200
- 400
- 401
- 403
- 404
- 422

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

The token does not have access to this location

- application/json

- Schema
- Example (auto)

**Schema**

**statusCode** number

Example:`403`

**message** string

Example:`You do not have permission to access this resource`

**error** string

Example:`Forbidden`

```json
{
  "statusCode": 403,
  "message": "You do not have permission to access this resource",
  "error": "Forbidden"
}
```

Not Found

- application/json

- Schema
- Example (auto)

**Schema**

**statusCode** number

Example:`404`

**message** string

Example:`Conversation id, contact id, workflow id, or campaign id not given`

```json
{
  "statusCode": 404,
  "message": "Conversation id, contact id, workflow id, or campaign id not given"
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
curl -L 'https://services.leadconnectorhq.com/chat-widget/public/config/:id'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Parameters

id — pathrequired

Version — headerrequired

\-\-\-v3

Show optional parameters

version — query

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!