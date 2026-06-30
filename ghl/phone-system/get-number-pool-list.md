---
title: "List number pools"
source_url: https://marketplace.gohighlevel.com/docs/ghl/phone-system/get-number-pool-list
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/phone-system/number-pools
summary: "Returns number pools for the location. Requires locationId as a query parameter"
---
# List number pools

```
GET https://services.leadconnectorhq.com/phone-system/number-pools
```


Returns number pools for the location. Requires locationId as a query parameter.

### Requirements

#### Scope(s)

`numberpools.read`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request

### Query Parameters

**locationId** stringrequired

Location ID to scope the number pool list

Example: ve9EPM428h8vShlRW1KT

## Responses

- 200

List of number pools for the location.

## Share your feedback

★★★★★

#### Authorization: Authorization

```
name: Authorizationtype: httpscopes: numberpools.readscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/phone-system/number-pools' \
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

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!