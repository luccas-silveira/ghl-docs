---
title: "Agent/Ai-Bot is typing a message indicator for live chat"
source_url: https://marketplace.gohighlevel.com/docs/ghl/conversations/live-chat-agent-typing
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/conversations/providers/live-chat/typing
summary: "Agent/AI-Bot will call this when they are typing a message in live chat message"
---
# Agent/Ai-Bot is typing a message indicator for live chat

```
POST https://services.leadconnectorhq.com/conversations/providers/live-chat/typing
```


Agent/AI-Bot will call this when they are typing a message in live chat message

### Requirements

#### Scope(s)

`conversations/livechat.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

- application/json

### Body **required**

**locationId** stringrequired

Location Id

Example:`ve9EPM428h8vShlRW1KT`

**isTyping** stringrequired

Typing status

Example:`true`

**visitorId** stringrequired

visitorId is the Unique ID assigned to each Live chat visitor. visitorId will be added soon in [GET Contact API](https://marketplace.gohighlevel.com/docs/ghl/conversations/contacts/get-contact)

Example:`ve9EPM428h8vShlRW1KT`

**conversationId** stringrequired

Conversation Id

Example:`ve9EPM428h8vShlRW1KT`

## Responses

- 201
- 400
- 401
- 422

Show typing indicator for live chat

- application/json

- Schema
- Example (auto)

**Schema**

**success** booleanrequired

```json
{
  "success": true
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
name: Authorizationtype: httpscopes: conversations/livechat.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/conversations/providers/live-chat/typing' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "locationId": "ve9EPM428h8vShlRW1KT",
  "isTyping": true,
  "visitorId": "ve9EPM428h8vShlRW1KT",
  "conversationId": "ve9EPM428h8vShlRW1KT"
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

Body required

```json
{
  "locationId": "ve9EPM428h8vShlRW1KT",
  "isTyping": true,
  "visitorId": "ve9EPM428h8vShlRW1KT",
  "conversationId": "ve9EPM428h8vShlRW1KT"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!