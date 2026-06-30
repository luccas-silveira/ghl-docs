---
title: "Get Brand Boards"
source_url: https://marketplace.gohighlevel.com/docs/ghl/brand-boards/get-brand-boards-by-location
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/brand-boards/:locationId
---
# Get Brand Boards

```
GET https://services.leadconnectorhq.com/brand-boards/:locationId
```

Retrieves all Brand Boards for a specific location

### Requirements

#### Scope(s)

`brand-boards/design-kit.readonly`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/brand-boards/get-brand-boards-by-location/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

Example: v3

### Path Parameters

**locationId** stringrequired

Location ID where the brand boards exist

Example: ve9EPM428h8vShlRW1KT

### Query Parameters

**limit** number

Maximum number of brand boards to return

Default value:`10`

Example: 10

**offset** number

Number of brand boards to skip for pagination

Default value:`0`

Example: 0

**search** string

Search term to filter brand boards by name

Default value:``

Example: brandboard

**deleted** boolean

Include deleted brand boards in results

Default value:`false`

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/brand-boards/get-brand-boards-by-location/\#responses "Direct link to Responses")

- 200
- 400
- 401
- 403
- 422

Success

- application/json

- Schema
- Example (auto)

**Schema**

**brandBoards** object\[\]required

Array of brand boards for the location

Array \[\
\
**\_id** stringrequired\
\
Brand board ID\
\
Example:`507f1f77bcf86cd799439011`\
\
**name** stringrequired\
\
Brand board name\
\
Example:`My Brand Board`\
\
**updatedAt** stringrequired\
\
Last update timestamp\
\
Example:`2024-01-05T12:00:00.000Z`\
\
**default** boolean\
\
Whether this is the default brand board for the location\
\
Example:`false`\
\
**meta** object\
\
Metadata about the brand board\
\
**updatedBy** string\
\
User ID who last updated the brand board\
\
Example:`user_abc123`\
\
**lastAction** string\
\
Last action performed on the brand board\
\
Example:`UPDATE`\
\
**sourceId** string\
\
Source brand board ID if created from a template\
\
Example:`507f1f77bcf86cd799439011`\
\
**sourceType** string\
\
How the brand board was created\
\
**Possible values:** \[`template`, `blank`, `snapshot`, `url`\]\
\
Example:`blank`\
\
\]

**totalCount** numberrequired

Total number of brand boards matching the query

Example:`42`

```json
{
  "brandBoards": [\
    {\
      "_id": "507f1f77bcf86cd799439011",\
      "name": "My Brand Board",\
      "updatedAt": "2024-01-05T12:00:00.000Z",\
      "default": true,\
      "meta": {\
        "updatedBy": "user_abc123",\
        "lastAction": "UPDATE",\
        "sourceType": "blank"\
      }\
    }\
  ],
  "totalCount": 42
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

The token does not have access to this location

- application/json

- Schema
- Example (auto)

**Schema**

**statusCode** number

HTTP status code for invalid location access

Example:`403`

**message** string

Error message describing the location access failure

Example:`The token does not have access to this location`

```json
{
  "statusCode": 403,
  "message": "The token does not have access to this location"
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
name: Authorizationtype: httpscopes: brand-boards/design-kit.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/brand-boards/:locationId' \
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

limit — query

offset — query

search — query

deleted — query

\-\-\-truefalse

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!