---
title: "Delete Recurring Task"
source_url: https://marketplace.gohighlevel.com/docs/ghl/locations/delete-recurring-task
version: v3
method: DELETE
endpoint: https://services.leadconnectorhq.com/locations/:locationId/recurring-tasks/:id
---
# Delete Recurring Task

```
DELETE https://services.leadconnectorhq.com/locations/:locationId/recurring-tasks/:id
```


Delete Recurring Task

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

### Path Parameters

**id** stringrequired

Recurring Task Id

Example: sx6wyHhbFdRXh302Lunr

**locationId** stringrequired

Location Id

Example: sx6wyHhbFdRXh302Lunr

## Responses

- 200
- 400
- 401

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**id** stringrequired

Recurring Task Id

Example:`sx6wyHhbFdRXh302Lunr`

**success** booleanrequired

Success

Example:`true`

```json
{
  "id": "sx6wyHhbFdRXh302Lunr",
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
curl -L -X DELETE 'https://services.leadconnectorhq.com/locations/:locationId/recurring-tasks/:id' \
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

id — pathrequired

locationId — pathrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!