---
title: "Get Last Snapshot Push"
source_url: https://marketplace.gohighlevel.com/docs/ghl/snapshots/get-latest-snapshot-push
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/snapshots/snapshot-status/:snapshotId/location/:locationId
---
# Get Last Snapshot Push

```
GET https://services.leadconnectorhq.com/snapshots/snapshot-status/:snapshotId/location/:locationId
```


Get Latest Snapshot Push Status for a location id

### Requirements

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

**snapshotId** stringrequired

Example: 39It2BFz7EkNaNBALPif

**locationId** stringrequired

Example: IIRGHCgxSINdPT79M75P

### Query Parameters

**companyId** stringrequired

Example: 5D112kQsiKESj6rash

## Responses

- 200
- 400
- 401

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**data** object

**id** string

Document id

Example:`1eM2UgkfaECOYyUdCo9Pa`

**locationId** string

Sub-account id

Example:`BrKClvyvdxhJ9Mxz2pzQ`

**status** string

Status of snapshot push

Example:`processing`

**completed** string\[\]

List of completed assets

Example:`['forms', 'surveys', 'funnels', 'workflows']`

**pending** string\[\]

List of pending assets

Example:`['custom_fields','custom_values','tags']`

```json
{
  "data": {
    "id": "1eM2UgkfaECOYyUdCo9Pa",
    "locationId": "BrKClvyvdxhJ9Mxz2pzQ",
    "status": "processing",
    "completed": "['forms', 'surveys', 'funnels', 'workflows']",
    "pending": "['custom_fields','custom_values','tags']"
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

## Share your feedback

★★★★★

#### Authorization: Authorization

```
name: Authorizationtype: httpscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Agency (OR) Personal Integration Token from Agency.
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
curl -L 'https://services.leadconnectorhq.com/snapshots/snapshot-status/:snapshotId/location/:locationId' \
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

snapshotId — pathrequired

locationId — pathrequired

companyId — queryrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!