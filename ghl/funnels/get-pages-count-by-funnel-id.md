---
title: "Fetch count of funnel pages"
source_url: https://marketplace.gohighlevel.com/docs/ghl/funnels/get-pages-count-by-funnel-id
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/funnels/page/count
---
# Fetch count of funnel pages

```
GET https://services.leadconnectorhq.com/funnels/page/count
```


Retrieves count of all funnel pages based on the given query parameters.

### Requirements

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request

### Query Parameters

**locationId** stringrequired

**funnelId** stringrequired

**name** string

## Responses

- 200

Successful response - Count of funnel pages returned

- application/json

- Schema
- Example (auto)

**Schema**

**count** numberrequired

Example:`20`

```json
{
  "count": 20
}
```

## Share your feedback

★★★★★

#### Authorization: Authorization

```
name: Authorizationtype: httpscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/funnels/page/count' \
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

funnelId — queryrequired

Show optional parameters

name — query

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!