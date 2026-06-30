---
title: "Get SaaS Plan"
source_url: https://marketplace.gohighlevel.com/docs/ghl/saas/get-saas-plan
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/saas/saas-plan/:planId
summary: "Fetch a specific SaaS plan by plan ID"
---
# Get SaaS Plan

```
GET https://services.leadconnectorhq.com/saas/saas-plan/:planId
```


Fetch a specific SaaS plan by plan ID

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

**planId** stringrequired

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
curl -L 'https://services.leadconnectorhq.com/saas/saas-plan/:planId' \
-H 'Authorization: Bearer <TOKEN>'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

planId — pathrequired

companyId — queryrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!