---
title: "Create Agent"
source_url: https://marketplace.gohighlevel.com/docs/ghl/agent-studio/create-agent
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/agent-studio/agent
---
# Create Agent

```
POST https://services.leadconnectorhq.com/agent-studio/agent
```


Creates a new agent with staging version. The agent will be created with an initial staging version that can later be promoted to production.

### Requirements

#### Scope(s)

`agent-studio.write`

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

**source** string

Example: api

- application/json

### Body **required**

**locationId** stringrequired

Location ID

Example:`C2QujeCh8ZnC7al2InWR`

**name** string

Name of the agent

Example:`Customer Support Agent`

**description** string

Description of the agent

Example:`AI agent specialized in handling customer inquiries and support tickets`

**agencyId** string

Agency ID

Example:`gjL2sFNXJfJYa3d2OYSN`

**authorId** string

Author ID

Example:`usr_abc123def456`

**authorName** string

Author name

Example:`John Doe`

**authorEmail** string

Author email

Example:`john@example.com`

**status** stringrequired

Status of the agent

**Possible values:** \[`active`, `inactive`, `archived`\]

Example:`active`

**version** objectrequired

Version data for the agent including nodes, edges, and configuration

Example:`{"versionName":"Version 1","description":"Initial version","nodes":[],"edges":[],"uiNodes":[],"uiEdges":[],"globalVariables":[],"inputVariables":[],"runtimeVariables":[],"scopes":[]}`

**nodes** string\[\]

Nodes array (deprecated, prefer using version.nodes)

Example:`[]`

**edges** string\[\]

Edges array (deprecated, prefer using version.edges)

Example:`[]`

## Responses

- 201
- 400
- 401
- 422
- 500

Agent created successfully

- application/json

- Schema
- Example (auto)

**Schema**

**success** booleanrequired

Success status

Example:`true`

**message** stringrequired

Response message

Example:`Agent created successfully with staging version.`

**agent** objectrequired

Created agent data with metadata

Example:`{"agentId":"p1q2r3s4t5u6v7w8x9y0z1a2","name":"Customer Support Agent","description":"AI agent specialized in handling customer inquiries and support tickets","locationId":"C2QujeCh8ZnC7al2InWR","agencyId":"gjL2sFNXJfJYa3d2OYSN","status":"active","authorId":"usr_abc123def456","folderId":"C2QujeCh8ZnC7al2InWR","folderName":null,"createdAt":"2024-02-27T10:30:00.000Z","updatedAt":"2024-02-27T10:30:00.000Z"}`

**versions** arrayrequired

Created versions array (initial staging version)

Example:`[{"versionId":"v1a2b3c4d5e6f7g8h9i0","agentId":"p1q2r3s4t5u6v7w8x9y0z1a2","versionName":"Customer Support Agent v1","state":"staging","isPublished":false,"version":1,"createdAt":"2024-02-27T10:30:00.000Z"}]`

```json
{
  "success": true,
  "message": "Agent created successfully with staging version.",
  "agent": {
    "agentId": "p1q2r3s4t5u6v7w8x9y0z1a2",
    "name": "Customer Support Agent",
    "description": "AI agent specialized in handling customer inquiries and support tickets",
    "locationId": "C2QujeCh8ZnC7al2InWR",
    "agencyId": "gjL2sFNXJfJYa3d2OYSN",
    "status": "active",
    "authorId": "usr_abc123def456",
    "folderId": "C2QujeCh8ZnC7al2InWR",
    "folderName": null,
    "createdAt": "2024-02-27T10:30:00.000Z",
    "updatedAt": "2024-02-27T10:30:00.000Z"
  },
  "versions": [\
    {\
      "versionId": "v1a2b3c4d5e6f7g8h9i0",\
      "agentId": "p1q2r3s4t5u6v7w8x9y0z1a2",\
      "versionName": "Customer Support Agent v1",\
      "state": "staging",\
      "isPublished": false,\
      "version": 1,\
      "createdAt": "2024-02-27T10:30:00.000Z"\
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
name: Authorizationtype: httpscopes: agent-studio.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
--data-raw '{
  "locationId": "C2QujeCh8ZnC7al2InWR",
  "name": "Customer Support Agent",
  "description": "AI agent specialized in handling customer inquiries and support tickets",
  "agencyId": "gjL2sFNXJfJYa3d2OYSN",
  "authorId": "usr_abc123def456",
  "authorName": "John Doe",
  "authorEmail": "john@example.com",
  "status": "active",
  "version": {
    "versionName": "Version 1",
    "description": "Initial version",
    "nodes": [],
    "edges": [],
    "uiNodes": [],
    "uiEdges": [],
    "globalVariables": [],
    "inputVariables": [],
    "runtimeVariables": [],
    "scopes": []
  },
  "nodes": [],
  "edges": []
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

Version — headerrequired

\-\-\-v3

Show optional parameters

source — query

Body required

```json
{
  "locationId": "C2QujeCh8ZnC7al2InWR",
  "name": "Customer Support Agent",
  "description": "AI agent specialized in handling customer inquiries and support tickets",
  "agencyId": "gjL2sFNXJfJYa3d2OYSN",
  "authorId": "usr_abc123def456",
  "authorName": "John Doe",
  "authorEmail": "john@example.com",
  "status": "active",
  "version": {
    "versionName": "Version 1",
    "description": "Initial version",
    "nodes": [],
    "edges": [],
    "uiNodes": [],
    "uiEdges": [],
    "globalVariables": [],
    "inputVariables": [],
    "runtimeVariables": [],
    "scopes": []
  },
  "nodes": [],
  "edges": []
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!