---
title: "Generate Invoice Number"
source_url: https://marketplace.gohighlevel.com/docs/ghl/invoices/generate-invoice-number
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/invoices/generate-invoice-number
---
# Generate Invoice Number

```
GET https://services.leadconnectorhq.com/invoices/generate-invoice-number
```


Get the next invoice number for the given location

### Requirements

#### Scope(s)

`invoices.readonly`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token``Agency Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/invoices/generate-invoice-number/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Query Parameters

**altId** stringrequired

Location Id

**altType** stringrequired

**Possible values:** \[`location`\]

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/invoices/generate-invoice-number/\#responses "Direct link to Responses")

- 200
- 400
- 401
- 422

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**invoiceNumber** number

Invoice Number

Example:`19`

```json
{
  "invoiceNumber": "19"
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
name: Authorizationtype: httpscopes: invoices.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/invoices/generate-invoice-number' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Security Scheme

Location-AccessAgency-Access

Bearer Token

Parameters

altId — queryrequired

altType — queryrequired

\-\-\-location

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!