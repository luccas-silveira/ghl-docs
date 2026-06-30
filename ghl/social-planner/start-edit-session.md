---
title: "Start or resume an edit session"
source_url: https://marketplace.gohighlevel.com/docs/ghl/social-planner/start-edit-session
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/social-media-posting/category/queues/:queueId/edit/start
---
# Start or resume an edit session

```
POST https://services.leadconnectorhq.com/social-media-posting/category/queues/:queueId/edit/start
```


Creates a draft copy of queue items for editing. Changes are staged until saved or discarded.

### Requirements

#### Scope(s)

`socialplanner/category.write`

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

**queueId** stringrequired

- application/json

### Body **required**

**locationId** stringrequired

Location ID

Example:`609e126a1c4ae1001291e1b5`

## Responses

- 201
- 400
- 401
- 422

Edit session started successfully.

- application/json

- Schema
- Example (auto)

**Schema**

**success** booleanrequired

Example:`true`

**statusCode** numberrequired

Example:`201`

**results** objectrequired

**message** string

A message indicating the result of the operation.

Example:`Edit session started successfully`

**sessionId** string

The ID of the edit session.

Example:`60af88475f1b2c001f5d5f4b`

**itemCount** number

Number of items staged for editing.

Example:`25`

**traceId** string

```json
{
  "success": true,
  "statusCode": 201,
  "results": {
    "message": "Edit session started successfully",
    "sessionId": "60af88475f1b2c001f5d5f4b",
    "itemCount": 25
  },
  "traceId": "string"
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
name: Authorizationtype: httpscopes: socialplanner/category.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/social-media-posting/category/queues/:queueId/edit/start' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "locationId": "609e126a1c4ae1001291e1b5"
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

queueId — pathrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "locationId": "609e126a1c4ae1001291e1b5"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!