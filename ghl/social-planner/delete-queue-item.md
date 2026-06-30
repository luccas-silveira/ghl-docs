---
title: "Delete an item from a queue"
source_url: https://marketplace.gohighlevel.com/docs/ghl/social-planner/delete-queue-item
version: v3
method: DELETE
endpoint: https://services.leadconnectorhq.com/social-media-posting/category/queues/:queueId/items/:itemId
summary: "Deletes an item from a specific category queue"
---
# Delete an item from a queue

```
DELETE https://services.leadconnectorhq.com/social-media-posting/category/queues/:queueId/items/:itemId
```


Deletes an item from a specific category queue.

### Requirements

#### Scope(s)

`socialplanner/category.write`

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

### Path Parameters

**queueId** stringrequired

**itemId** stringrequired

### Query Parameters

**locationId** stringrequired

Location ID

Example: 609e126a1c4ae1001291e1b5

**sessionId** string

Edit session ID

Example: 60af88475f1b2c001f5d5f4b

## Responses

- 200
- 400
- 401
- 422

The queue item has been successfully deleted.

- application/json

- Schema
- Example (auto)

**Schema**

**success** booleanrequired

Example:`true`

**statusCode** numberrequired

Example:`200`

**results** objectrequired

**message** string

A message indicating the result of the operation.

Example:`The queue item has been successfully deleted.`

**updatedSlots** object\[\]

Updated slot information for items affected by the operation

Array \[\
\
**itemId** string\
\
The ID of the queue item\
\
Example:`60af88475f1b2c001f5d5f4b`\
\
**scheduledDateTime** date-timenullable\
\
The updated scheduled date/time for this item\
\
Example:`2023-10-15T10:00:00.000Z`\
\
**isSkipped** boolean\
\
Indicates if this time slot is skipped\
\
Example:`false`\
\
\]

**totalPostsChanged** number

Number of unique posts that had their slots changed

Example:`5`

**traceId** string

```json
{
  "success": true,
  "statusCode": 200,
  "results": {
    "message": "The queue item has been successfully deleted.",
    "updatedSlots": [\
      {\
        "itemId": "60af88475f1b2c001f5d5f4b",\
        "scheduledDateTime": "2023-10-15T10:00:00.000Z",\
        "isSkipped": false\
      }\
    ],
    "totalPostsChanged": 5
  },
  "traceId": "string"
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
curl -L -X DELETE 'https://services.leadconnectorhq.com/social-media-posting/category/queues/:queueId/items/:itemId' \
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

queueId — pathrequired

itemId — pathrequired

locationId — queryrequired

Version — headerrequired

\-\-\-v3

Show optional parameters

sessionId — query

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!