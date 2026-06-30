---
title: "Get Agency Plans"
source_url: https://marketplace.gohighlevel.com/docs/ghl/saas/get-agency-plans
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/saas/agency-plans/:companyId
---
# Get Agency Plans

```
GET https://services.leadconnectorhq.com/saas/agency-plans/:companyId
```


Fetch all agency subscription plans for a given company ID

### Requirements

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Agency Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/saas/get-agency-plans/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**companyId** stringrequired

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/saas/get-agency-plans/\#responses "Direct link to Responses")

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
curl -L 'https://services.leadconnectorhq.com/saas/agency-plans/:companyId' \
-H 'Authorization: Bearer <TOKEN>'
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

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!