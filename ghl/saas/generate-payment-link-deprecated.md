---
title: "Update SaaS subscription"
source_url: https://marketplace.gohighlevel.com/docs/ghl/saas/generate-payment-link-deprecated
version: v3
method: PUT
endpoint: https://services.leadconnectorhq.com/saas-api/public-api/update-saas-subscription/:locationId
summary: "This endpoint has been deprecated and may be replaced or removed in future versions of the API"
---
# Update SaaS subscription

```
PUT https://services.leadconnectorhq.com/saas-api/public-api/update-saas-subscription/:locationId
```


deprecated

This endpoint has been deprecated and may be replaced or removed in future versions of the API.

Update SaaS subscription for given locationId and customerId

### Requirements

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Agency Token`

## Request

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**locationId** stringrequired

Location ID to update subscription for

Example: AUKAtFVo0lWezBsBQ3FE

- application/json

### Body **required**

**subscriptionId** stringrequired

Subscription ID

Example:`sub_1QDPY5FpU9DlKp7RQ8BXfywx`

**customerId** stringrequired

Customer ID

Example:`cus_1QDPY5FpU9DlKp7RQ8BXfywx`

**companyId** stringrequired

Company ID

Example:`companyId1`

## Responses

- 200
- 400
- 401
- 404
- 500

SaaS subscription updated successfully

- application/json

- Schema
- Example (auto)

**Schema**

**string** string

```json
"string"
```

Bad Request

- application/json

- Schema
- Example (auto)

**Schema**

**statusCode** number

Status code

Example:`400`

**message** string

Error message

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

Status code

Example:`401`

**message** string

Error message

Example:`Invalid token: access token is invalid`

**error** string

Error message

Example:`Unauthorized`

```json
{
  "statusCode": 401,
  "message": "Invalid token: access token is invalid",
  "error": "Unauthorized"
}
```

Resource not found

- application/json

- Schema
- Example (auto)

**Schema**

**statusCode** number

Status code

Example:`404`

**message** string

Error message

Example:`["Contact not found","User not found","Group not found","Channel not found"]`

```json
{
  "statusCode": 404,
  "message": [\
    "Contact not found",\
    "User not found",\
    "Group not found",\
    "Channel not found"\
  ]
}
```

Internal server error

- application/json

- Schema
- Example (auto)

**Schema**

**statusCode** number

Status code

Example:`500`

**message** string

Error message

Example:`Internal Server Error`

```json
{
  "statusCode": 500,
  "message": "Internal Server Error"
}
```

## Share your feedback

★★★★★

#### Authorization: Authorization

```
name: Authorizationtype: httpscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Company
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
curl -L -X PUT 'https://services.leadconnectorhq.com/saas-api/public-api/update-saas-subscription/:locationId' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "subscriptionId": "sub_1QDPY5FpU9DlKp7RQ8BXfywx",
  "customerId": "cus_1QDPY5FpU9DlKp7RQ8BXfywx",
  "companyId": "companyId1"
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

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "subscriptionId": "sub_1QDPY5FpU9DlKp7RQ8BXfywx",
  "customerId": "cus_1QDPY5FpU9DlKp7RQ8BXfywx",
  "companyId": "companyId1"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!