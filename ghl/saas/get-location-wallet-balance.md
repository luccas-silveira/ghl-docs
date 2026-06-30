---
title: "Get Location Wallet Balance"
source_url: https://marketplace.gohighlevel.com/docs/ghl/saas/get-location-wallet-balance
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/saas-api/public-api/companies/:companyId/locations/:locationId/wallet-balance
---
# Get Location Wallet Balance

```
GET https://services.leadconnectorhq.com/saas-api/public-api/companies/:companyId/locations/:locationId/wallet-balance
```


Fetch the wallet balance for a specific location. Returns a resource object with balance details.

### Requirements

#### Scope(s)

`saas/company.read`

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

**companyId** stringrequired

Company ID that owns the location

Example: 5DP4iH6HLkQsiKESj6rh

**locationId** stringrequired

Location ID to get wallet balance for

Example: AUKAtFVo0lWezBsBQ3FE

## Responses

- 200
- 400
- 401
- 404
- 500

Location wallet balance retrieved successfully

- application/json

- Schema
- Example (auto)

**Schema**

**walletId** stringrequired

Wallet Id

Example:`xyz789`

**balance** numberrequired

Current wallet balance

Example:`1500.5`

**complimentaryCredits** numberrequired

Complimentary credits amount

Example:`100`

```json
{
  "walletId": "xyz789",
  "balance": 1500.5,
  "complimentaryCredits": 100
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
curl -L 'https://services.leadconnectorhq.com/saas-api/public-api/companies/:companyId/locations/:locationId/wallet-balance' \
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

companyId — pathrequired

locationId — pathrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!