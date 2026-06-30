---
title: "Validate group slug"
source_url: https://marketplace.gohighlevel.com/docs/ghl/calendars/validate-groups-slug
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/calendars/groups/validate-slug
summary: "Validate if group slug is available or not"
---
# Validate group slug

```
POST https://services.leadconnectorhq.com/calendars/groups/validate-slug
```


Validate if group slug is available or not.

### Requirements

#### Scope(s)

`calendars/groups.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

- application/json

### Body **required**

**locationId** stringrequired

Location Id

Example:`ve9EPM428h8vShlRW1KT`

**slug** stringrequired

Slug

Example:`calendar-1`

## Responses

- 200
- 400
- 401

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**available** booleanrequired

```json
{
  "available": true
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
name: Authorizationtype: httpscopes: calendars/groups.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/calendars/groups/validate-slug' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "locationId": "ve9EPM428h8vShlRW1KT",
  "slug": "calendar-1"
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "locationId": "ve9EPM428h8vShlRW1KT",
  "slug": "calendar-1"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!