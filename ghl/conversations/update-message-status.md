---
title: "Update message status"
source_url: https://marketplace.gohighlevel.com/docs/ghl/conversations/update-message-status
version: v3
method: PUT
endpoint: https://services.leadconnectorhq.com/conversations/messages/:messageId/status
summary: "Post the necessary fields for the API to update message status"
---
# Update message status

```
PUT https://services.leadconnectorhq.com/conversations/messages/:messageId/status
```


Post the necessary fields for the API to update message status.

### Requirements

#### Scope(s)

`conversations/message.write`

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

**messageId** stringrequired

Message Id

Example: ve9EPM428h8vShlRW1KT

- application/json

### Body **required**

**status** stringrequired

Message status

**Possible values:** \[`delivered`, `failed`, `pending`, `read`\]

Example:`read`

**error** object

Error object from the conversation provider

**code** stringrequired

Error Code

Example:`1`

**type** stringrequired

Error Type

Example:`saas`

**message** stringrequired

Error Message

Example:`There was an error from the provider`

**emailMessageId** string

Email message Id

Example:`ve9EPM428h8vShlRW1KT`

**recipients** string\[\]

Email delivery status for additional email recipients.

## Responses

- 200
- 400
- 401
- 403

Created the message

- application/json

- Schema
- Example (auto)

**Schema**

**conversationId** stringrequired

Conversation ID.

Example:`ABC12h2F6uBrIkfXYazb`

**emailMessageId** string

This contains the email message id (only for Email type). Use this ID to send inbound replies to CRM to create a threaded email.

Example:`rnGyqh2F6uBrIkfhFo9A`

**messageId** stringrequired

This is the main Message ID

Example:`t22c6DQcTDf3MjRhwf77`

**messageIds** string\[\]

When sending via the GMB channel, we will be returning list of `messageIds` instead of single `messageId`.

**msg** string

Additional response message when sending a workflow message

Example:`Message queued successfully.`

```json
{
  "conversationId": "ABC12h2F6uBrIkfXYazb",
  "emailMessageId": "rnGyqh2F6uBrIkfhFo9A",
  "messageId": "t22c6DQcTDf3MjRhwf77",
  "messageIds": [\
    "string"\
  ],
  "msg": "Message queued successfully."
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

Forbidden

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

## Share your feedback

★★★★★

#### Authorization: Authorization

```
name: Authorizationtype: httpscopes: conversations/message.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L -X PUT 'https://services.leadconnectorhq.com/conversations/messages/:messageId/status' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "status": "read",
  "error": {
    "code": "1",
    "type": "saas",
    "message": "There was an error from the provider"
  },
  "emailMessageId": "ve9EPM428h8vShlRW1KT",
  "recipients": [\
    "string"\
  ]
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

messageId — pathrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "status": "read",
  "error": {
    "code": "1",
    "type": "saas",
    "message": "There was an error from the provider"
  },
  "emailMessageId": "ve9EPM428h8vShlRW1KT",
  "recipients": [\
    "string"\
  ]
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!