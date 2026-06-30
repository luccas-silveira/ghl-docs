---
title: "Update Recurring Task"
source_url: https://marketplace.gohighlevel.com/docs/ghl/locations/update-recurring-task
version: v3
method: PUT
endpoint: https://services.leadconnectorhq.com/locations/:locationId/recurring-tasks/:id
---
# Update Recurring Task

```
PUT https://services.leadconnectorhq.com/locations/:locationId/recurring-tasks/:id
```

Update Recurring Task

## Request

## Responses

- 200
- 400
- 401

Successful response

Bad Request

Unauthorized

#### Authorization: Authorization

```
name: Authorizationtype: httpscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L -X PUT 'https://services.leadconnectorhq.com/locations/:locationId/recurring-tasks/:id' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "title": "Task Name",
  "description": "Task Description",
  "contactIds": [\
    "sx6wyHhbFdRXh302Lunr"\
  ],
  "owners": [\
    "sx6wyHhbFdRXh302Lunr"\
  ],
  "rruleOptions": {
    "intervalType": "hourly",
    "interval": 1,
    "startDate": "2025-07-23T10:00:00.000Z",
    "dueAfterSeconds": 600
  },
  "ignoreTaskCreation": true
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

id — pathrequired

locationId — pathrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "title": "Task Name",
  "description": "Task Description",
  "contactIds": [\
    "sx6wyHhbFdRXh302Lunr"\
  ],
  "owners": [\
    "sx6wyHhbFdRXh302Lunr"\
  ],
  "rruleOptions": {
    "intervalType": "hourly",
    "interval": 1,
    "startDate": "2025-07-23T10:00:00.000Z",
    "dueAfterSeconds": 600
  },
  "ignoreTaskCreation": true
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!