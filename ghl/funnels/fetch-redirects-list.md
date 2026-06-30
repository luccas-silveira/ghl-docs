---
title: "Fetch List of Redirects"
source_url: https://marketplace.gohighlevel.com/docs/ghl/funnels/fetch-redirects-list
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/funnels/lookup/redirect/list
summary: "Retrieves a list of all URL redirects based on the given query parameters"
---
# Fetch List of Redirects

```
GET https://services.leadconnectorhq.com/funnels/lookup/redirect/list
```


Retrieves a list of all URL redirects based on the given query parameters.

### Requirements

#### Scope(s)

`funnels/redirect.readonly`

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

Example: 6p2RxpgtMKQwO3E6IUaT

**limit** numberrequired

Example: 20

**offset** numberrequired

Example: 10

**search** string

Example: example.com/test

## Responses

- 200
- 422

Successful response - List of URL redirects returned

- application/json

- Schema
- Example (auto)

**Schema**

**data** objectrequired

Object containing the count of redirects and an array of redirect data

Example:`{"count":42,"data":[]}`

```json
{
  "data": {
    "count": 42,
    "data": []
  }
}
```

Unprocessable Entity - The provided data is invalid or incomplete

## Share your feedback

★★★★★

#### Authorization: Authorization

```
name: Authorizationtype: httpscopes: funnels/redirect.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/funnels/lookup/redirect/list' \
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

limit — queryrequired

offset — queryrequired

Version — headerrequired

\-\-\-v3

Show optional parameters

search — query

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!