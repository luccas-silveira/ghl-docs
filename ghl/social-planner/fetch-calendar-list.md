---
title: "Get scheduled posts calendar view"
source_url: https://marketplace.gohighlevel.com/docs/ghl/social-planner/fetch-calendar-list
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/social-media-posting/category/queues/list/calendar
---
# Get scheduled posts calendar view

```
POST https://services.leadconnectorhq.com/social-media-posting/category/queues/list/calendar
```

Returns scheduled posts from active queues within a date range. Supports filtering by categories and accounts.

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/social-planner/fetch-calendar-list/\#request "Direct link to Request")

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/social-planner/fetch-calendar-list/\#responses "Direct link to Responses")

- 201
- 400
- 401
- 422

Calendar list fetched successfully.

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
curl -L 'https://services.leadconnectorhq.com/social-media-posting/category/queues/list/calendar' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "locationId": "609e126a1c4ae1001291e1b5",
  "startDate": "2023-10-01T00:00:00.000Z",
  "endDate": "2023-10-31T23:59:59.999Z",
  "categoryIds": [\
    "64e431dcaf507c4b26dbdf8b"\
  ],
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

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "locationId": "609e126a1c4ae1001291e1b5",
  "startDate": "2023-10-01T00:00:00.000Z",
  "endDate": "2023-10-31T23:59:59.999Z",
  "categoryIds": [\
    "64e431dcaf507c4b26dbdf8b"\
  ],
  "accountIds": [\
    "aF3KhyL8JIuBwzK3m7Ly_iVrVJ2uoXNF0wzcBzgl5_12554616564525983496"\
  ]
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!