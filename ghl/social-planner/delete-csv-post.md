---
title: "Delete CSV Post"
source_url: https://marketplace.gohighlevel.com/docs/ghl/social-planner/delete-csv-post
version: v3
method: DELETE
endpoint: https://services.leadconnectorhq.com/social-media-posting/:locationId/csv/:csvId/post/:postId
---
# Delete CSV Post

```
DELETE https://services.leadconnectorhq.com/social-media-posting/:locationId/csv/:csvId/post/:postId
```


Delete a specific post from a CSV import

### Requirements

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

**locationId** stringrequired

Location Id

Example: ve9EPM428h8vShlRW1KT

**postId** stringrequired

CSV Post Id

Example: 65f92e55cc884f0d0845e447

**csvId** stringrequired

CSV Id

Example: 65f92e55cc884f0d0845e447

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

**success** booleanrequired

Success or Failure

Example:`true`

**statusCode** numberrequired

Status Code

Example:`200`

**message** stringrequired

Message

Example:`Deleted CSV Post`

**results** object

Requested Results

**postId** stringrequired

Post Id

Example:`65f92e55cc884f0d0845e447`

**csv** object

CSV Data

**\_id** string

CSV Id

Example:`65f92e55cc884f0d0845e447`

**csvFileType** string

CSV file type

**Possible values:** \[`basic`, `advance`\]

Example:`basic`

**mediaOptimization** boolean

Media optimization flag

Example:`true`

**applyWatermark** boolean

Apply watermark flag

Example:`false`

**status** string

CSV import status

**Possible values:** \[`pending`, `in_progress`, `completed`, `failed`, `in_review`, `importing`, `deleted`\]

Example:`completed`

**updatedAt** date-time

Date Updated

Example:`2023-08-02T00:00:00.000Z`

```json
{
  "success": true,
  "statusCode": 200,
  "message": "Deleted CSV Post",
  "results": {
    "postId": "65f92e55cc884f0d0845e447",
    "csv": {
      "_id": "65f92e55cc884f0d0845e447",
      "status": "completed"
    }
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
curl -L -X DELETE 'https://services.leadconnectorhq.com/social-media-posting/:locationId/csv/:csvId/post/:postId' \
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

locationId — pathrequired

postId — pathrequired

csvId — pathrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!