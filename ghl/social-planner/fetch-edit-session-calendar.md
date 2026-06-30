---
title: "Fetch calendar view for an edit session"
source_url: https://marketplace.gohighlevel.com/docs/ghl/social-planner/fetch-edit-session-calendar
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/social-media-posting/category/queues/:queueId/edit/calendar
---
# Fetch calendar view for an edit session

```
POST https://services.leadconnectorhq.com/social-media-posting/category/queues/:queueId/edit/calendar
```

Retrieves a calendar preview of scheduled posts based on draft items within an edit session. This shows how posts would be scheduled if changes were saved.

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/social-planner/fetch-edit-session-calendar/\#request "Direct link to Request")

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/social-planner/fetch-edit-session-calendar/\#responses "Direct link to Responses")

- 201
- 400
- 401
- 422

Edit session calendar fetched successfully.

Bad Request

Unauthorized

Unprocessable Entity

#### Authorization: Authorization

```
name: Authorizationtype: httpscopes: socialplanner/category.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/social-media-posting/category/queues/:queueId/edit/calendar' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "locationId": "609e126a1c4ae1001291e1b5",
  "sessionId": "60af88475f1b2c001f5d5f4b",
  "startDate": "2023-10-01T00:00:00.000Z",
  "endDate": "2023-10-31T23:59:59.999Z",
  "accountIds": [\
    "aF3KhyL8JIuBwzK3m7Ly_iVrVJ2uoXNF0wzcBzgl5_12554616564525983496"\
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

queueId — pathrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "locationId": "609e126a1c4ae1001291e1b5",
  "sessionId": "60af88475f1b2c001f5d5f4b",
  "startDate": "2023-10-01T00:00:00.000Z",
  "endDate": "2023-10-31T23:59:59.999Z",
  "accountIds": [\
    "aF3KhyL8JIuBwzK3m7Ly_iVrVJ2uoXNF0wzcBzgl5_12554616564525983496"\
  ]
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!