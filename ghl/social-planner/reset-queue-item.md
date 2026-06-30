---
title: "Reset an item in a queue"
source_url: https://marketplace.gohighlevel.com/docs/ghl/social-planner/reset-queue-item
version: v3
method: PUT
endpoint: https://services.leadconnectorhq.com/social-media-posting/category/queues/:queueId/items/:itemId/reset
summary: "Resets a specific queue item to its original state, discarding any modifications made"
---
# Reset an item in a queue

```
PUT https://services.leadconnectorhq.com/social-media-posting/category/queues/:queueId/items/:itemId/reset
```

Resets a specific queue item to its original state, discarding any modifications made.

## Request

## Responses

- 200
- 400
- 401
- 422

The queue item has been successfully reset.

Bad Request

Unauthorized

Unprocessable Entity

#### Authorization: Authorization

```
name: Authorizationtype: httpscopes: socialplanner/category.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L -X PUT 'https://services.leadconnectorhq.com/social-media-posting/category/queues/:queueId/items/:itemId/reset' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "locationId": "609e126a1c4ae1001291e1b5",
  "sessionId": "60af88475f1b2c001f5d5f4b"
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

queueId — pathrequired

itemId — pathrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "locationId": "609e126a1c4ae1001291e1b5",
  "sessionId": "60af88475f1b2c001f5d5f4b"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!