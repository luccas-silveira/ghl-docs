---
title: "Get Duplicate Contact"
source_url: https://marketplace.gohighlevel.com/docs/ghl/contacts/get-duplicate-contact
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/contacts/search/duplicate
---
# Get Duplicate Contact

```
GET https://services.leadconnectorhq.com/contacts/search/duplicate
```


Get Duplicate Contact.

If `Allow Duplicate Contact` is disabled under Settings, the global unique identifier will be used for searching the contact. If the setting is enabled, first priority for search is `email` and the second priority will be `phone`.

### Requirements

#### Scope(s)

`contacts.readonly`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/contacts/get-duplicate-contact/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

Example: v3

### Query Parameters

**locationId** stringrequired

Location Id

Example: ve9EPM428h8vShlRW1KT

**number** string

Phone Number — URL-encoded. E.g. +1423164516 → %2B1423164516

Example: %2B1423164516

**email** string

Email — URL-encoded. E.g. test+abc@gmail.com → test%2Babc%40gmail.com

Example: test%2Babc%40gmail.com

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/contacts/get-duplicate-contact/\#responses "Direct link to Responses")

- 200
- 400
- 401

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
name: Authorizationtype: httpscopes: contacts.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/contacts/search/duplicate' \
-H 'Authorization: Bearer <TOKEN>'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

locationId — queryrequired

Version — headerrequired

\-\-\-v3

Show optional parameters

number — query

email — query

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!