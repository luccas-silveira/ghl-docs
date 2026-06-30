---
title: "Get locations by stripeId with companyId"
source_url: https://marketplace.gohighlevel.com/docs/ghl/saas/locations
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/saas/locations
---
# Get locations by stripeId with companyId

```
GET https://services.leadconnectorhq.com/saas/locations
```


Get locations by stripeCustomerId or stripeSubscriptionId with companyId

### Requirements

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Agency Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/saas/locations/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Query Parameters

**customerId** stringrequired

**subscriptionId** stringrequired

**companyId** stringrequired

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/saas/locations/\#responses "Direct link to Responses")

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
curl -L 'https://services.leadconnectorhq.com/saas/locations' \
-H 'Authorization: Bearer <TOKEN>'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

customerId — queryrequired

subscriptionId — queryrequired

companyId — queryrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!