---
title: "Get locations by stripeId with companyId"
source_url: https://marketplace.gohighlevel.com/docs/ghl/saas/locations-deprecated
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/saas-api/public-api/locations
---
# Get locations by stripeId with companyId

```
GET https://services.leadconnectorhq.com/saas-api/public-api/locations
```


deprecated

This endpoint has been deprecated and may be replaced or removed in future versions of the API.

Get locations by stripeCustomerId or stripeSubscriptionId with companyId

### Requirements

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Agency Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/saas/locations-deprecated/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Query Parameters

**customerId** string

Stripe customer ID to find locations for

Example: cus\_OD2oBjRfKEF6FV

**subscriptionId** string

Stripe subscription ID to find locations for

Example: sub\_1NVqlLByVlfITvRXgirIdpyc

**companyId** stringrequired

Company ID to filter locations

Example: 5DP4iH6HLkQsiKESj6rh

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/saas/locations-deprecated/\#responses "Direct link to Responses")

- 200
- 400
- 401
- 404
- 500

Locations retrieved successfully

- application/json

- Schema
- Example (auto)

**Schema**

Array \[\
\
string\
\
\]

```json
[\
  "string"\
]
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
curl -L 'https://services.leadconnectorhq.com/saas-api/public-api/locations' \
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

companyId — queryrequired

Version — headerrequired

\-\-\-v3

Show optional parameters

customerId — query

subscriptionId — query

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!