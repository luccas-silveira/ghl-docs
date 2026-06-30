---
title: "Start CSV Finalize"
source_url: https://marketplace.gohighlevel.com/docs/ghl/social-planner/start-csv-finalize
version: v3
method: PATCH
endpoint: https://services.leadconnectorhq.com/social-media-posting/:locationId/csv/:id
---
# Start CSV Finalize

```
PATCH https://services.leadconnectorhq.com/social-media-posting/:locationId/csv/:id
```


Finalize a CSV import and schedule all posts for publishing

### Requirements

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/social-planner/start-csv-finalize/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

Example: v3

### Path Parameters

**locationId** stringrequired

Location Id

Example: ve9EPM428h8vShlRW1KT

**id** stringrequired

CSV Id

Example: 65f92e55cc884f0d0845e447

- application/json

### Body **required**

**userId** stringrequired

User ID

Example:`sdfdsfdsfEWEsdfsdsW32dd`

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/social-planner/start-csv-finalize/\#responses "Direct link to Responses")

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

Example:`Updated Successfully`

```json
{
  "success": true,
  "statusCode": 200,
  "message": "Updated Successfully"
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
curl -L -X PATCH 'https://services.leadconnectorhq.com/social-media-posting/:locationId/csv/:id' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "userId": "sdfdsfdsfEWEsdfsdsW32dd"
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

id — pathrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "userId": "sdfdsfdsfEWEsdfsdsW32dd"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!