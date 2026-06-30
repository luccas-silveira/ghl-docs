---
title: "Check if account has sufficient funds"
source_url: https://marketplace.gohighlevel.com/docs/ghl/marketplace/has-funds
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/marketplace/billing/charges/has-funds
---
# Check if account has sufficient funds

```
GET https://services.leadconnectorhq.com/marketplace/billing/charges/has-funds
```


Check if account has sufficient funds

### Requirements

#### Scope(s)

`charges.readonly`

#### Auth Method(s)

`OAuth Access Token`

#### Token Type(s)

`Sub-Account Token`

## Request

## Responses

- 200
- 422

Returns fund availability status

- application/json

- Schema
- Example (auto)

**Schema**

**hasFunds** boolean

Indicates whether the sub-account has sufficient funds to be charged

Example:`true`

```json
{
  "hasFunds": true
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
name: Authorizationtype: httpscopes: charges.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/marketplace/billing/charges/has-funds' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!