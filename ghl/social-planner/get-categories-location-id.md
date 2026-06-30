---
title: "Get categories by location id"
source_url: https://marketplace.gohighlevel.com/docs/ghl/social-planner/get-categories-location-id
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/social-media-posting/:locationId/categories
---
# Get categories by location id

```
GET https://services.leadconnectorhq.com/social-media-posting/:locationId/categories
```


Retrieve all categories for a specific location with optional search and pagination

### Requirements

#### Scope(s)

`socialplanner/category.readonly`

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

### Path Parameters

**locationId** stringrequired

Location Id

Example: ve9EPM428h8vShlRW1KT

### Query Parameters

**searchText** string

Search text string

Example: test

**limit** string

Limit

Example: 10

**skip** string

Skip

Example: 0

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

**success** booleanrequired

Success or Failure

Example:`true`

**statusCode** numberrequired

Status Code

Example:`200`

**message** stringrequired

Message

Example:`Fetched Categories by Location ID`

**results** object

Requested Results

**count** numberrequired

Count

Example:`3`

**categories** object\[\]required

Meta Data

Array \[\
\
**name** string\
\
Category Name\
\
Example:`Primary`\
\
**primaryColor** string\
\
Color For Category\
\
Example:`#FFFFFF`\
\
**secondaryColor** string\
\
Secondary Color\
\
Example:`#FFFFFF`\
\
**locationId** string\
\
Location ID\
\
Example:`Lx1EI6YIgQYMQi0ytFXv`\
\
**\_id** string\
\
ID\
\
Example:`Lx1EI6YIgQYMQi0ytFXv`\
\
**createdBy** string\
\
Created By User\
\
Example:`Lx1EI6YIgQYMQi0ytFXv`\
\
**deleted** booleanrequired\
\
Deleted Value\
\
Example:`false`\
\
**createdAt** date-time\
\
Example:`2023-08-02T00:00:00.000Z`\
\
**updatedAt** date-time\
\
Example:`2023-08-02T00:00:00.000Z`\
\
\]

```json
{
  "success": true,
  "statusCode": 200,
  "message": "Fetched Categories by Location ID",
  "results": {
    "count": 3,
    "categories": [\
      {\
        "name": "Primary",\
        "primaryColor": "#FFFFFF",\
        "secondaryColor": "#FFFFFF",\
        "locationId": "Lx1EI6YIgQYMQi0ytFXv",\
        "_id": "Lx1EI6YIgQYMQi0ytFXv",\
        "createdBy": "Lx1EI6YIgQYMQi0ytFXv",\
        "deleted": false,\
        "createdAt": "2023-08-02T00:00:00.000Z",\
        "updatedAt": "2023-08-02T00:00:00.000Z"\
      }\
    ]
  }
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
name: Authorizationtype: httpscopes: socialplanner/category.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/social-media-posting/:locationId/categories' \
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

locationId — pathrequired

Version — headerrequired

\-\-\-v3

Show optional parameters

searchText — query

limit — query

skip — query

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!