---
title: "Pause location"
source_url: https://marketplace.gohighlevel.com/docs/ghl/saas/pause-location
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/saas/pause/:locationId
---
# Pause location

```
POST https://services.leadconnectorhq.com/saas/pause/:locationId
```


Pause Sub account for given locationId

### Requirements

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Agency Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/saas/pause-location/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**locationId** stringrequired

- application/json

### Body **required**

**paused** booleanrequired

Paused

Example:`true`

**companyId** stringrequired

Company ID

Example:`companyId1`

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/saas/pause-location/\#responses "Direct link to Responses")

- 201

## Share your feedback

★★★★★

#### Authorization: Authorization

```
name: Authorizationtype: httpscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Company
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
curl -L 'https://services.leadconnectorhq.com/saas/pause/:locationId' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "paused": true,
  "companyId": "companyId1"
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

locationId — pathrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "paused": true,
  "companyId": "companyId1"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!