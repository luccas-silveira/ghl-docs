---
title: "Update Rebilling"
source_url: https://marketplace.gohighlevel.com/docs/ghl/saas/update-rebilling-deprecated
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/saas-api/public-api/update-rebilling/:companyId
---
# Update Rebilling

```
POST https://services.leadconnectorhq.com/saas-api/public-api/update-rebilling/:companyId
```


deprecated

This endpoint has been deprecated and may be replaced or removed in future versions of the API.

Bulk update rebilling for given locationIds

### Requirements

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Agency Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/saas/update-rebilling-deprecated/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**companyId** stringrequired

Company ID to update rebilling for

Example: 5DP4iH6HLkQsiKESj6rh

- application/json

### Body **required**

**product** stringrequired

The product to update rebilling for

**Possible values:** \[`contentAI`, `workflow_premium_actions`, `workflow_ai`, `conversationAI`, `EmailNotification`, `whatsApp`, `reviewsAI`, `VERIFIED_CALLER_ID`, `WALLET_SALES_TAX`, `NOTIFICATION_SMS`, `EmailSmtp`, `EmailVerification`, `autoCompleteAddress`, `funnelAI`, `domainPurchase`, `Phone`, `Email`\]

Example:`contentAI`

**locationIds** string\[\]required

Array of location IDs to update rebilling for

Example:`["zzyG7A4x6bRJl5SlhQhH","Vygq7VgXCDfg3xnl8TBR"]`

**config** objectrequired

Configuration for rebilling settings

**optIn** boolean

Enable the product for the locations

Example:`true`

**enabled** boolean

Enable the rebilling for the locations

Example:`true`

**markup** number

Additional value to be added in terms of percentage. For example, if the product price is $100 and the markup is 5, the amount charged to will be $105.

Example:`5`

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/saas/update-rebilling-deprecated/\#responses "Direct link to Responses")

- 200
- 400
- 401
- 404
- 500

Rebilling updated successfully

- application/json

- Schema
- Example (auto)

**Schema**

**success** booleanrequired

Indicates if the rebilling update was successful

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
curl -L 'https://services.leadconnectorhq.com/saas-api/public-api/update-rebilling/:companyId' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "product": "contentAI",
  "locationIds": [\
    "zzyG7A4x6bRJl5SlhQhH",\
    "Vygq7VgXCDfg3xnl8TBR"\
  ],
  "config": {
    "optIn": true,
    "enabled": true,
    "markup": 5
  }
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

companyId — pathrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "product": "contentAI",
  "locationIds": [\
    "zzyG7A4x6bRJl5SlhQhH",\
    "Vygq7VgXCDfg3xnl8TBR"\
  ],
  "config": {
    "optIn": true,
    "enabled": true,
    "markup": 5
  }
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!