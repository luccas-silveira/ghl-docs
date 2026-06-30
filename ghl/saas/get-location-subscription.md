---
title: "Get Location Subscription Details"
source_url: https://marketplace.gohighlevel.com/docs/ghl/saas/get-location-subscription
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/saas/get-saas-subscription/:locationId
---
# Get Location Subscription Details

```
GET https://services.leadconnectorhq.com/saas/get-saas-subscription/:locationId
```


Fetch subscription details for a specific location from location metadata

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

**locationId** stringrequired

### Query Parameters

**companyId** stringrequired

## Responses

- 200

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
curl -L 'https://services.leadconnectorhq.com/saas/get-saas-subscription/:locationId' \
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

companyId — queryrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!