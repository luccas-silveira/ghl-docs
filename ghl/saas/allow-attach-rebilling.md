---
title: "Allow Attach Rebilling"
source_url: https://marketplace.gohighlevel.com/docs/ghl/saas/allow-attach-rebilling
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/saas/allow-attach-rebilling/:locationId
---
# Allow Attach Rebilling

```
POST https://services.leadconnectorhq.com/saas/allow-attach-rebilling/:locationId
```


Marks a SaaS sub-account as awaiting rebilling attach and optionally stores the rebilling configuration that should be applied when the rebilling config is created. Sets payment\_pending on the sub-account. Only allowed when the sub-account is in setup\_pending state.

### Requirements

#### Scope(s)

`saas/company.read`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Agency Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/saas/allow-attach-rebilling/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**locationId** stringrequired

Location ID (Sub-account) to allow attach rebilling for

Example: AUKAtFVo0lWezBsBQ3FE

- application/json

### Body **required**

**companyId** stringrequired

Company ID owning the location

Example:`5DP4iH6HLkQsiKESj6rh`

**attachedRebillingConfig** object

Map of rebilling product code to its config. When provided, this gets stored on the sub-account so it can be applied when the rebilling config is created. Omit to only mark the sub-account as awaiting rebilling attach without any pre-configured products. Possible product keys: `contentAI`, `workflow_premium_actions`, `workflow_ai`, `conversationAI`, `whatsApp`, `reviewsAI`, `EmailVerification`, `funnelAI`, `domainPurchase`, `Phone`, `Email`, `agentStudio`, `askai`, `aiStudio`.

**property name\*** AttachedRebillingProductConfigDto

**enabled** booleanrequired

Enable rebilling for the product

Example:`true`

**markup** numberrequired

Additional value to be added in terms of percentage

Example:`300`

**price** number

Product price override

Example:`0.0025`

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/saas/allow-attach-rebilling/\#responses "Direct link to Responses")

- 200
- 400
- 401
- 404
- 422
- 500

Allow attach rebilling completed successfully

- application/json

- Schema
- Example (auto)

**Schema**

**success** booleanrequired

Indicates if the allow attach rebilling operation succeeded

Example:`true`

**locationId** stringrequired

Location ID the rebilling config was attached to

Example:`AUKAtFVo0lWezBsBQ3FE`

**attachedRebillingConfig** objectrequired

Stored rebilling configuration on the location. Markup is the internal percentage value converted from the request multiplier (e.g. 4 -> 300%, 3 -> 200%).

Example:`{"EmailVerification":{"enabled":true,"markup":300,"price":0.0025},"Phone":{"enabled":true,"markup":200}}`

```json
{
  "success": true,
  "locationId": "AUKAtFVo0lWezBsBQ3FE",
  "attachedRebillingConfig": {
    "EmailVerification": {
      "enabled": true,
      "markup": 300,
      "price": 0.0025
    },
    "Phone": {
      "enabled": true,
      "markup": 200
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

Unprocessable entity (e.g. sub-account already in saas mode activated, or not in setup\_pending state)

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
name: Authorizationtype: httpscopes: saas/company.readscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Company
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
curl -L 'https://services.leadconnectorhq.com/saas/allow-attach-rebilling/:locationId' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "companyId": "5DP4iH6HLkQsiKESj6rh",
  "attachedRebillingConfig": {
    "EmailVerification": {
      "enabled": true,
      "markup": 4,
      "price": 0.0025
    },
    "Phone": {
      "enabled": true,
      "markup": 3
    },
    "agentStudio": {
      "enabled": true,
      "markup": 8,
      "price": 0.25
    },
    "contentAI": {
      "enabled": true,
      "markup": 5,
      "price": 0.09
    },
    "domainPurchase": {
      "enabled": true,
      "markup": 3
    }
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

locationId — pathrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "companyId": "5DP4iH6HLkQsiKESj6rh",
  "attachedRebillingConfig": {
    "EmailVerification": {
      "enabled": true,
      "markup": 4,
      "price": 0.0025
    },
    "Phone": {
      "enabled": true,
      "markup": 3
    },
    "agentStudio": {
      "enabled": true,
      "markup": 8,
      "price": 0.25
    },
    "contentAI": {
      "enabled": true,
      "markup": 5,
      "price": 0.09
    },
    "domainPurchase": {
      "enabled": true,
      "markup": 3
    }
  }
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!