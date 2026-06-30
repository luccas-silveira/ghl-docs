---
title: "Delete Custom Field By Id"
source_url: https://marketplace.gohighlevel.com/docs/ghl/custom-fields/delete-custom-field
version: v3
method: DELETE
endpoint: https://services.leadconnectorhq.com/custom-fields/:id
---
# Delete Custom Field By Id

```
DELETE https://services.leadconnectorhq.com/custom-fields/:id
```


Delete Custom Field By Id

info

Only supports Custom Objects and Company (Business) today. Will be extended to other Standard Objects in the future.

### Requirements

#### Scope(s)

`locations/customFields.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/custom-fields/delete-custom-field/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**id** stringrequired

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/custom-fields/delete-custom-field/\#responses "Direct link to Responses")

- 200
- 400
- 401

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**succeded** booleanrequired

Example:`true`

**id** stringrequired

Example:`3v34PM428h8vShlRW1KT`

**key** stringrequired

Example:`custom_object.pet.name`

```json
{
  "succeded": true,
  "id": "3v34PM428h8vShlRW1KT",
  "key": "custom_object.pet.name"
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
name: Authorizationtype: httpscopes: locations/customFields.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L -X DELETE 'https://services.leadconnectorhq.com/custom-fields/:id' \
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

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!