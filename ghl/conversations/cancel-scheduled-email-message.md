---
title: "Cancel a scheduled email message."
source_url: https://marketplace.gohighlevel.com/docs/ghl/conversations/cancel-scheduled-email-message
version: v3
method: DELETE
endpoint: https://services.leadconnectorhq.com/conversations/messages/email/:emailMessageId/schedule
---
# Cancel a scheduled email message.

```
DELETE https://services.leadconnectorhq.com/conversations/messages/email/:emailMessageId/schedule
```


Post the messageId for the API to delete a scheduled email message.

### Requirements

#### Scope(s)

`conversations/message.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request

### Path Parameters

**emailMessageId** stringrequired

Email Message Id

Example: ve9EPM428h8vShlRW1KT

## Responses

- 200

The scheduled email message was cancelled successfully

- application/json

- Schema
- Example (auto)

**Schema**

**status** numberrequired

HTTP Status code of the request

Example:`404`

**message** stringrequired

Error message of the request

Example:`Failed cancel the scheduled message`

```json
{
  "status": 404,
  "message": "Failed cancel the scheduled message"
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
curl -L -X DELETE 'https://services.leadconnectorhq.com/conversations/messages/email/:emailMessageId/schedule' \
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

emailMessageId — pathrequired

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!