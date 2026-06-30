---
title: "Get Agent"
source_url: https://marketplace.gohighlevel.com/docs/ghl/conversation-ai/get-agent
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/conversation-ai/agents/:agentId
summary: "Retrieves a specific AI agent by its ID. Returns the complete agent configuration including name, status, actions, and settings"
---
# Get Agent

```
GET https://services.leadconnectorhq.com/conversation-ai/agents/:agentId
```

Retrieves a specific AI agent by its ID. Returns the complete agent configuration including name, status, actions, and settings.

### Requirements

#### Scope(s)

`conversation-ai.readonly`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**agentId** stringrequired

Conversations AI agent id

Example: EmployeeId123

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

**id** stringrequired

Unique identifier for the agent.

Example:`emp_123`

**name** stringrequired

Name of the agent.

Example:`John Doe`

**businessName** string

Name of the business the agent represents.

Example:`Tech Corp`

**mode** stringrequired

Current operating mode of the agent.

**Possible values:** \[`off`, `suggestive`, `auto-pilot`\]

Example:`auto-pilot`

**channels** string\[\]required

Communication channels the agent operates on.

**Possible values:** \[`IG`, `FB`, `SMS`, `WebChat`, `WhatsApp`, `Live_Chat`\]

Example:`["SMS","Live_Chat"]`

**waitTime** numberrequired

Wait time before agent responds.

Example:`30`

**waitTimeUnit** stringrequired

Unit for wait time.

**Possible values:** \[`minutes`, `seconds`\]

Example:`seconds`

**sleepEnabled** booleanrequireddeprecated

Indicates if sleep functionality is enabled.

Example:`false`

**sleepTime** number

Duration of sleep period.

Example:`2`

**sleepTimeUnit** string

Unit of sleep time.

**Possible values:** \[`hours`, `minutes`, `seconds`\]

Example:`hours`

**actions** object\[\]required

List of actions associated with this agent.

Array \[\
\
**id** stringrequired\
\
Unique identifier for the action.\
\
Example:`actionId123`\
\
**type** stringrequired\
\
type of action.\
\
**Possible values:** \[`triggerWorkflow`, `updateContactField`, `appointmentBooking`, `stopBot`, `humanHandOver`, `advancedFollowup`, `transferBot`\]\
\
Example:`triggerWorkflow`\
\
\]

**isPrimary** booleanrequired

Indicates if this agent is a primary agent.

Example:`false`

**autoPilotMaxMessages** numberrequired

Maximum number of messages in auto-pilot mode before requiring human intervention.

Example:`25`

**goal** string

The goal of the agent.

Example:`Assist customers with inquiries`

**personality** string

Personality traits of the agent.

Example:`Friendly and helpful`

**instructions** string

Instructions for the agent.

Example:`Provide excellent customer service`

**knowledgeBaseIds** string\[\]

Array of knowledge base IDs associated with this agent.

Example:`["kb_123","kb_456"]`

**sleepOnManualMessage** boolean

Whether the bot sleeps on manual outbound messages.

Example:`false`

**sleepOnWorkflowMessage** boolean

Whether the bot sleeps on workflow outbound messages.

Example:`false`

```json
{
  "id": "emp_123",
  "name": "John Doe",
  "businessName": "Tech Corp",
  "mode": "auto-pilot",
  "channels": [\
    "SMS",\
    "Live_Chat"\
  ],
  "waitTime": 30,
  "waitTimeUnit": "seconds",
  "sleepTime": 2,
  "sleepTimeUnit": "hours",
  "actions": [\
    {\
      "id": "actionId123",\
      "type": "triggerWorkflow"\
    }\
  ],
  "isPrimary": false,
  "autoPilotMaxMessages": 25,
  "goal": "Assist customers with inquiries",
  "personality": "Friendly and helpful",
  "instructions": "Provide excellent customer service",
  "knowledgeBaseIds": [\
    "kb_123",\
    "kb_456"\
  ],
  "sleepOnManualMessage": false,
  "sleepOnWorkflowMessage": false
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
name: Authorizationtype: httpscopes: conversation-ai.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/conversation-ai/agents/:agentId' \
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

agentId — pathrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!