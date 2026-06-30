---
title: "Add message attachments"
source_url: https://marketplace.gohighlevel.com/docs/ghl/conversations/add-message-attachments
version: v3
method: PUT
endpoint: https://services.leadconnectorhq.com/conversations/messages/:messageId/attachments
summary: "Set attachments on an existing message (replaces existing). Maximum 5 URLs. Supported for Custom Call message type"
---
# Add message attachments

```
PUT https://services.leadconnectorhq.com/conversations/messages/:messageId/attachments
```


Set attachments on an existing message (replaces existing). Maximum 5 URLs. Supported for Custom Call message type.

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

**attachments** string\[\]required

Array of attachment URLs to set on the message (replaces existing). Maximum 5 URLs.

Example:`["https://provider.com/recordings/call-123.mp3"]`

## Responses

- 200
- 400
- 401
- 403

Successfully set message attachments

- application/json

- Schema
- Example (auto)

**Schema**

**success** booleanrequired

Indicates whether the operation was successful.

Example:`true`

**messageId** stringrequired

The ID of the message that was updated.

Example:`ve9EPM428h8vShlRW1KT`

**attachments** string\[\]required

The updated list of attachment URLs on the message.

Example:`["https://provider.com/recordings/call-123.mp3"]`

```json
{
  "success": true,
  "messageId": "ve9EPM428h8vShlRW1KT",
  "attachments": [\
    "https://provider.com/recordings/call-123.mp3"\
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
curl -L -X PUT 'https://services.leadconnectorhq.com/conversations/messages/:messageId/attachments' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "attachments": [\
    "https://provider.com/recordings/call-123.mp3"\
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
  "attachments": [\
    "https://provider.com/recordings/call-123.mp3"\
  ]
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!