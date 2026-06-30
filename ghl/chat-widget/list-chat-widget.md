---
title: "List Chat Widgets"
source_url: https://marketplace.gohighlevel.com/docs/ghl/chat-widget/list-chat-widget
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/chat-widget/list
---
# List Chat Widgets

```
GET https://services.leadconnectorhq.com/chat-widget/list
```


Returns chat widgets for the sub-account with pagination and optional filters.

### Requirements

#### Scope(s)

`chat-widget.readonly`

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

The location ID

Example: ve9EPM428h8vShlRWsss

**offset** stringrequired

Offset

Example: 10

**limit** stringrequired

Limit

Example: 0

**chatType** string

**Possible values:** \[`liveChat`, `waChat`, `emailChat`, `allInOneChat`, `voiceAiChat`, `facebookChat`, `instagramChat`, `webChat`\]

The type of chat widget. Supports normal ChatType values, plus the virtual umbrella "webChat" (maps to facebookChat/emailChat/instagramChat/waChat).

Example: emailChat

**excludeChatType** string

**Possible values:** \[`liveChat`, `waChat`, `emailChat`, `allInOneChat`, `voiceAiChat`, `facebookChat`, `instagramChat`\]

The type of chat widget

Example: voiceAiChat

**voiceAiAgentId** string

The voice AI agent ID

Example: 66597c9a41106ba6eb4eac3c

**allInOneChatTypes** string

**Possible values:** \[`liveChat`, `waChat`, `emailChat`, `allInOneChat`, `voiceAiChat`, `facebookChat`, `instagramChat`, `webChat`\]

All-in-one chat type to filter by. Only applies when chatType is "allInOneChat". Supports normal ChatType values plus the virtual umbrella "webChat" (maps to facebookChat/emailChat/instagramChat/waChat).

Example: emailChat

## Responses

- 200
- 400
- 401
- 403
- 404
- 422

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

Example:`403`

**message** string

Example:`You do not have permission to access this resource`

**error** string

Example:`Forbidden`

```json
{
  "statusCode": 403,
  "message": "You do not have permission to access this resource",
  "error": "Forbidden"
}
```

Not Found

- application/json

- Schema
- Example (auto)

**Schema**

**statusCode** number

Example:`404`

**message** string

Example:`Conversation id, contact id, workflow id, or campaign id not given`

```json
{
  "statusCode": 404,
  "message": "Conversation id, contact id, workflow id, or campaign id not given"
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
name: Authorizationtype: httpscopes: chat-widget.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/chat-widget/list' \
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

offset — queryrequired

limit — queryrequired

Version — headerrequired

\-\-\-v3

Show optional parameters

chatType — query

\-\-\-liveChatwaChatemailChatallInOneChatvoiceAiChatfacebookChatinstagramChatwebChat

excludeChatType — query

\-\-\-liveChatwaChatemailChatallInOneChatvoiceAiChatfacebookChatinstagramChat

voiceAiAgentId — query

allInOneChatTypes — query

\-\-\-liveChatwaChatemailChatallInOneChatvoiceAiChatfacebookChatinstagramChatwebChat

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!