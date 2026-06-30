---
title: "Get Campaigns"
source_url: https://marketplace.gohighlevel.com/docs/ghl/campaigns/get-campaigns
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/campaigns
---
# Get Campaigns

```
GET https://services.leadconnectorhq.com/campaigns/
```


Get Campaigns

### Requirements

#### Scope(s)

`campaigns.readonly`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Query Parameters

**locationId** stringrequired

Example: ve9EPM428h8vShlRW1KT

**status** string

Example: draft

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

**campaigns** object\[\]

Array \[\
\
**id** string\
\
Example:`mIVALPYuTD7YjUHnFEx4`\
\
**name** string\
\
Example:`test`\
\
**status** string\
\
Example:`published`\
\
**locationId** string\
\
Example:`ve9EPM428h8vShlRW1KT`\
\
\]

```json
{
  "campaigns": [\
    {\
      "id": "mIVALPYuTD7YjUHnFEx4",\
      "name": "test",\
      "status": "published",\
      "locationId": "ve9EPM428h8vShlRW1KT"\
    }\
  ]
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
name: Authorizationtype: httpscopes: campaigns.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/campaigns/' \
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

locationId — queryrequired

Version — headerrequired

\-\-\-v3

Show optional parameters

status — query

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!