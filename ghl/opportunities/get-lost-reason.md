---
title: "Get lost reason"
source_url: https://marketplace.gohighlevel.com/docs/ghl/opportunities/get-lost-reason
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/opportunities/lost-reason
summary: "Get lost reason"
---
# Get lost reason

```
GET https://services.leadconnectorhq.com/opportunities/lost-reason
```


Get lost reason

### Requirements

#### Scope(s)

`opportunities.readonly`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

Example: v3

### Query Parameters

**locationId** stringrequired

Identifier of the location (sub-account)

Example: ve9EPM428h8vShlRW1KT

**name** string

lost reason name

Example: lost reason

**deleted** boolean

deleted

Default value:`false`

**query** string

search query

Example: dentist

**skip** number

skip

Default value:`0`

Example: 1

**limit** number

limit

Default value:`100`

Example: 10

**getCount** boolean

get count

Example: field

## Responses

- 200
- 400
- 401
- 422

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**lostReasons** object\[\]

List of lost reasons for the location

Array \[\
\
**id** string\
\
lost reason id\
\
Example:`ve9EPM428h8vShlRW1KT`\
\
**name** string\
\
lost reason name\
\
Example:`lost reason`\
\
**locationId** string\
\
location id\
\
Example:`location_id`\
\
**updatedAt** date-time\
\
updated at\
\
Example:`2023-06-19T12:04:22.488Z`\
\
**createdAt** date-time\
\
created at\
\
Example:`2023-06-19T12:04:22.488Z`\
\
\]

**total** number

Total number of lost reasons matching the query

Example:`100`

```json
{
  "lostReasons": [],
  "total": 100
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
name: Authorizationtype: httpscopes: opportunities.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/opportunities/lost-reason' \
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

Version — headerrequired

\-\-\-v3

Show optional parameters

name — query

deleted — query

\-\-\-truefalse

query — query

skip — query

limit — query

getCount — query

\-\-\-truefalse

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!