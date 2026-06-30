---
title: "Get all categories"
source_url: https://marketplace.gohighlevel.com/docs/ghl/blogs/get-all-categories-by-location
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/blogs/categories
summary: "The 'Get all categories' Api return the blog categoies for a given location ID. Please use 'blogs/category.readonly'"
---
# Get all categories

```
GET https://services.leadconnectorhq.com/blogs/categories
```


The "Get all categories" Api return the blog categoies for a given location ID. Please use "blogs/category.readonly"

### Requirements

#### Scope(s)

`blogs/category.readonly`

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

Example: ve9EPM428h8vShlRW1KT

**limit** numberrequired

Number of categories to show in the listing

**offset** numberrequired

Number of categories to skip in listing

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

**categories** object\[\]required

Array of categories

Array \[\
\
**\_id** stringrequired\
\
Example:`lMOzIQZne5m6zQ528sT6`\
\
**label** string\
\
Example:`HighLevel`\
\
**locationId** stringrequired\
\
Example:`lMOzIQZne5m6zQ528sT6`\
\
**updatedAt** stringrequired\
\
Example:`2025-01-03T11:06:35.822Z`\
\
**canonicalLink** stringrequired\
\
Example:`https://tryghl.blog/doc/category/agency-growth`\
\
**urlSlug** stringrequired\
\
Example:`agency-growth`\
\
\]

```json
{
  "categories": [\
    {\
      "_id": "lMOzIQZne5m6zQ528sT6",\
      "label": "HighLevel",\
      "locationId": "lMOzIQZne5m6zQ528sT6",\
      "updatedAt": "2025-01-03T11:06:35.822Z",\
      "canonicalLink": "https://tryghl.blog/doc/category/agency-growth",\
      "urlSlug": "agency-growth"\
    }\
  ]
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
name: Authorizationtype: httpscopes: blogs/category.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/blogs/categories' \
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

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!