---
title: "List Estimate Templates"
source_url: https://marketplace.gohighlevel.com/docs/ghl/invoices/list-estimate-templates
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/invoices/estimate/template
---
# List Estimate Templates

```
GET https://services.leadconnectorhq.com/invoices/estimate/template
```


Get a list of estimate templates or a specific template by ID

### Requirements

#### Scope(s)

`invoices/estimate.readonly`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token``Agency Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/invoices/list-estimate-templates/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Query Parameters

**altId** stringrequired

Location Id or Agency Id

Example: 6578278e879ad2646715ba9c

**altType** stringrequired

**Possible values:** \[`location`\]

**search** string

To search for an estimate template by id / name

Example: Alex

**limit** stringrequired

Limit the number of items to return

Example: 10

**offset** stringrequired

Number of items to skip

Example: 10

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/invoices/list-estimate-templates/\#responses "Direct link to Responses")

- 200
- 400
- 401
- 422

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**data** string\[\]required

List of estimate templates

**totalCount** numberrequired

Total number of estimate templates available

**traceId** stringrequired

Unique identifier for tracing the request

```json
{
  "data": [\
    "string"\
  ],
  "totalCount": 0,
  "traceId": "string"
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
name: Authorizationtype: httpscopes: invoices/estimate.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/invoices/estimate/template' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Security Scheme

Location-AccessAgency-Access

Bearer Token

Parameters

altId — queryrequired

altType — queryrequired

\-\-\-location

limit — queryrequired

offset — queryrequired

Version — headerrequired

\-\-\-v3

Show optional parameters

search — query

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!