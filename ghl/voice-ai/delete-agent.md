---
title: "Delete Agent"
source_url: https://marketplace.gohighlevel.com/docs/ghl/voice-ai/delete-agent
version: v3
method: DELETE
endpoint: https://services.leadconnectorhq.com/voice-ai/agents/:agentId
---
# Delete Agent

```
DELETE https://services.leadconnectorhq.com/voice-ai/agents/:agentId
```


Delete a voice AI agent and all its configurations

### Requirements

#### Scope(s)

`voice-ai-agents.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/voice-ai/delete-agent/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**agentId** stringrequired

Unique agent identifier

Example: 507f1f77bcf86cd799439011

### Query Parameters

**locationId** stringrequired

Location ID

Example: LOC123456789ABCDEF

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/voice-ai/delete-agent/\#responses "Direct link to Responses")

- 204
- 400
- 401
- 422

Agent deleted successfully

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
name: Authorizationtype: httpscopes: voice-ai-agents.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L -X DELETE 'https://services.leadconnectorhq.com/voice-ai/agents/:agentId' \
-H 'Authorization: Bearer <TOKEN>'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

agentId — pathrequired

locationId — queryrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!