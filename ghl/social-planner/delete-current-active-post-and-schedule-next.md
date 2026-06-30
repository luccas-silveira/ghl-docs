---
title: "Delete an active post and schedule the next one"
source_url: https://marketplace.gohighlevel.com/docs/ghl/social-planner/delete-current-active-post-and-schedule-next
version: v3
method: DELETE
endpoint: https://services.leadconnectorhq.com/social-media-posting/category/queues/:postId/active-post
summary: "Deletes a post that is currently scheduled and automatically triggers the scheduling of the next available post in the queue"
---
# Delete an active post and schedule the next one

```
DELETE https://services.leadconnectorhq.com/social-media-posting/category/queues/:postId/active-post
```


Deletes a post that is currently scheduled and automatically triggers the scheduling of the next available post in the queue.

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

**postId** stringrequired

### Query Parameters

**locationId** stringrequired

Location ID

Example: 609e126a1c4ae1001291e1b5

## Responses

- 200
- 400
- 401
- 422

Successfully deleted the active post and scheduled the next one.

- application/json

- Schema
- Example (auto)

**Schema**

**success** booleanrequired

Example:`true`

**statusCode** numberrequired

Example:`200`

**results** objectrequired

**message** string

A message indicating the result of the operation.

Example:`Current post deleted and next post scheduled successfully`

**traceId** string

```json
{
  "success": true,
  "statusCode": 200,
  "results": {
    "message": "Current post deleted and next post scheduled successfully"
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
curl -L -X DELETE 'https://services.leadconnectorhq.com/social-media-posting/category/queues/:postId/active-post' \
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

postId — pathrequired

locationId — queryrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!