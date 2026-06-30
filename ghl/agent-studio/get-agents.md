---
title: "List Agents"
source_url: https://marketplace.gohighlevel.com/docs/ghl/agent-studio/get-agents
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/agent-studio/agent
---
# List Agents

```
GET https://services.leadconnectorhq.com/agent-studio/agent
```


Lists all active agents for the specified location. locationId is required parameter to ensure optimal performance. Supports pagination using limit and offset. Optionally filter by isPublished=true to return only agents with a published production version.

### Requirements

#### Scope(s)

`agent-studio.readonly`

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

Example: C2QujeCh8ZnC7al2InWR

**isPublished** string

Optional filter to return only agents with a published production version

Example: true

**limit** stringrequired

Example: 20

**offset** stringrequired

Example: 0

**source** string

Example: api

## Responses

- 200
- 400
- 401
- 422
- 500

Agents retrieved successfully

- application/json

- Schema
- Example (auto)

**Schema**

**success** booleanrequired

Success status

Example:`true`

**message** stringrequired

Response message

Example:`Agents retrieved successfully`

**agents** object\[\]required

List of agents with metadata

Array \[\
\
**agentId** string\
\
Agent ID\
\
**name** string\
\
Agent name\
\
**description** string\
\
Agent description\
\
**locationId** string\
\
Location ID\
\
**status** string\
\
Agent status (always "active")\
\
**createdAt** string\
\
Creation timestamp\
\
**updatedAt** string\
\
Last update timestamp\
\
\]

**pagination** objectrequired

Pagination metadata

**total** number

Total number of agents

**limit** number

Number of agents per page

**offset** number

Starting position

**hasMore** boolean

Whether more agents exist

```json
{
  "success": true,
  "message": "Agents retrieved successfully",
  "agents": [\
    {\
      "agentId": "p1q2r3s4t5u6v7w8x9y0z1a2",\
      "name": "Marketing Assistant",\
      "description": "AI agent specialized in marketing strategy and content creation",\
      "locationId": "C2QujeCh8ZnC7al2InWR",\
      "status": "active",\
      "createdAt": "2024-01-15T10:30:00.000Z",\
      "updatedAt": "2024-02-20T14:45:00.000Z"\
    },\
    {\
      "agentId": "b3c4d5e6f7g8h9i0j1k2l3m4",\
      "name": "Customer Support Bot",\
      "description": "AI agent for handling customer inquiries and support tickets",\
      "locationId": "C2QujeCh8ZnC7al2InWR",\
      "status": "active",\
      "createdAt": "2024-01-10T09:15:00.000Z",\
      "updatedAt": "2024-02-18T16:20:00.000Z"\
    }\
  ],
  "pagination": {
    "total": 25,
    "limit": 20,
    "offset": 0,
    "hasMore": true
  }
}
```

Bad Request - locationId is required

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

Internal Server Error

- application/json

- Schema
- Example (auto)

**Schema**

**statusCode** number

Example:`500`

**message** string

Example:`Internal Server Error`

```json
{
  "statusCode": 500,
  "message": "Internal Server Error"
}
```

## Share your feedback

★★★★★

#### Authorization: Authorization

```
name: Authorizationtype: httpscopes: agent-studio.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/agent-studio/agent' \
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

isPublished — query

source — query

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!