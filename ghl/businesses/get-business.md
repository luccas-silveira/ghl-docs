---
title: "Get Business"
source_url: https://marketplace.gohighlevel.com/docs/ghl/businesses/get-business
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/businesses/:businessId
---
# Get Business

```
GET https://services.leadconnectorhq.com/businesses/:businessId
```


Get Business

### Requirements

#### Scope(s)

`businesses.readonly`

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

**businessId** stringrequired

Example: 5DP4iH6HLkQsiKESj6rh

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

**business** object

Business Response

**id** stringrequired

Business Id

Example:`63771dcac1116f0e21de8e12`

**name** stringrequired

Business Name

Example:`Microsoft`

**phone** string

phone number

**email** string

email

Example:`abc@microsoft.com`

**website** string

website

Example:`microsoft.com`

**address** string

address

**city** string

city

**description** string

description

**state** string

state

**postalCode** string

postal code

**country** string

country

Example:`united states`

**updatedBy** object

updated By

**locationId** stringrequired

locaitonId

**createdBy** object

Created By

**createdAt** date-time

Creation Time

**updatedAt** date-time

Last updation time

```json
{
  "business": {
    "id": "63771dcac1116f0e21de8e12",
    "name": "Microsoft",
    "phone": "string",
    "email": "abc@microsoft.com",
    "website": "microsoft.com",
    "address": "string",
    "city": "string",
    "description": "string",
    "state": "string",
    "postalCode": "string",
    "country": "united states",
    "updatedBy": {},
    "locationId": "string",
    "createdBy": {},
    "createdAt": "2024-07-29T15:51:28.071Z",
    "updatedAt": "2024-07-29T15:51:28.071Z"
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
name: Authorizationtype: httpscopes: businesses.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/businesses/:businessId' \
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

businessId — pathrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!