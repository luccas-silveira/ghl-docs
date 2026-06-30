---
title: "Delete Sub-Account (Formerly Location)"
source_url: https://marketplace.gohighlevel.com/docs/ghl/locations/delete-location
version: v3
method: DELETE
endpoint: https://services.leadconnectorhq.com/locations/:locationId
---
# Delete Sub-Account (Formerly Location)

```
DELETE https://services.leadconnectorhq.com/locations/:locationId
```


Delete a Sub-Account (Formerly Location) from the Agency

### Requirements

#### Scope(s)

`locations.internal-access-only`

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

Location Id

Example: ve9EPM428h8vShlRW1KT

### Query Parameters

**deleteTwilioAccount** booleanrequired

Boolean value to indicate whether to delete Twilio Account or not

## Responses

- 200
- 400
- 401

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**success** booleanrequired

Success status of the API

Example:`true`

**message** stringrequired

Success message of the API

Example:`Deleted location with id: ve9EPM428h8vShlRW1KT`

```json
{
  "success": true,
  "message": "Deleted location with id: ve9EPM428h8vShlRW1KT"
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
name: Authorizationtype: httpscopes: locations.internal-access-onlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Agency (OR) Private Integration Token of Agency.
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
curl -L -X DELETE 'https://services.leadconnectorhq.com/locations/:locationId' \
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

locationId — pathrequired

deleteTwilioAccount — queryrequired

\-\-\-truefalse

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!