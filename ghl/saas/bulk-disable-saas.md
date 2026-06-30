---
title: "Disable SaaS for locations"
source_url: https://marketplace.gohighlevel.com/docs/ghl/saas/bulk-disable-saas
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/saas/bulk-disable-saas/:companyId
---
# Disable SaaS for locations

```
POST https://services.leadconnectorhq.com/saas/bulk-disable-saas/:companyId
```


Disable SaaS for locations for given locationIds

### Requirements

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Agency Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/saas/bulk-disable-saas/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**companyId** stringrequired

- application/json

### Body **required**

**locationIds** string\[\]required

Location IDs

Example:`["locationId1","locationId2"]`

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/saas/bulk-disable-saas/\#responses "Direct link to Responses")

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
curl -L 'https://services.leadconnectorhq.com/saas/bulk-disable-saas/:companyId' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "locationIds": [\
    "locationId1",\
    "locationId2"\
  ]
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

companyId — pathrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "locationIds": [\
    "locationId1",\
    "locationId2"\
  ]
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!