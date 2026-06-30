---
title: "Update queue settings or status"
source_url: https://marketplace.gohighlevel.com/docs/ghl/social-planner/update-queue
version: v3
method: PUT
endpoint: https://services.leadconnectorhq.com/social-media-posting/category/queues/:queueId
---
# Update queue settings or status

```
PUT https://services.leadconnectorhq.com/social-media-posting/category/queues/:queueId
```


Updates queue status (active/paused/deleted), time slots, or skip dates.

### Requirements

#### Scope(s)

`socialplanner/category.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/social-planner/update-queue/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

Example: v3

### Path Parameters

**queueId** stringrequired

- application/json

### Body **required**

**locationId** stringrequired

Location ID

Example:`609e126a1c4ae1001291e1b5`

**skipLegacyWatermark** boolean

Skip legacy watermark cleanup when rescheduling posts

Example:`false`

**status** object

Status of the Queue

Example:`paused`

**skipDateTime** string

Skip Date Time in ISO format

Example:`2023-10-05T14:48:00.000Z`

**timeSlots** object\[\]

Array \[\
\
**dayOfWeek** numberrequired\
\
Day of the week (0-6)\
\
Example:`0`\
\
**time** stringrequired\
\
Time in HH:mm format\
\
Example:`09:00`\
\
\]

**enableFuturePosts** boolean

Enable posting future content. Automatically Queue any New Posts Created in this Category.

Example:`true`

**prioritizeNewContent** boolean

Prioritize new content over older content. When true, new items added via directToQueue will be placed at the top of the queue.

Example:`false`

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/social-planner/update-queue/\#responses "Direct link to Responses")

- 200
- 400
- 401
- 422

Queue updated successfully.

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

A message indicating the result of the operation. Examples: "Queue updated successfully.", "Queue paused successfully.", "Queue activated successfully.", "Queue deleted successfully."

Example:`Queue paused successfully.`

**queue** object

The updated queue.

**\_id** string

Queue ID

Example:`60af88475f1b2c001f5d5f4b`

**locationId** string

Location ID

Example:`location-123`

**categoryId** string

Category ID

Example:`60af88475f1b2c001f5d5f4b`

**timeSlots** object\[\]

Time slots for scheduling posts

Array \[\
\
**dayOfWeek** numberrequired\
\
Day of the week (0-6)\
\
Example:`0`\
\
**time** stringrequired\
\
Time in HH:mm format\
\
Example:`09:00`\
\
\]

**enableFuturePosts** boolean

Enable posting future content

Example:`false`

**prioritizeNewContent** boolean

Prioritize new content over older content

Example:`false`

**currentOrder** number

Current order number in the queue

Example:`1000`

**status** string

Status of the queue. Possible values: active, paused, draft.

**Possible values:** \[`active`, `paused`, `draft`\]

Example:`active`

**startDate** date-time

Start date of the queue

Example:`2023-01-01T12:00:00Z`

**skipDateTime** date-time\[\]

Dates/times to skip posting

Example:`["2023-01-02T12:00:00Z"]`

**currentPostId** stringnullable

ID of the currently scheduled post

Example:`60af88475f1b2c001f5d5f4b`

**totalPosts** number

Total number of posts in the queue

Example:`10`

**lastScheduledTime** date-timenullable

Timestamp of the last scheduled post

Example:`2023-01-01T12:00:00Z`

**createdBy** string

ID of the user who created the queue

Example:`user-123`

**createdAt** date-time

Creation timestamp

Example:`2023-01-01T00:00:00Z`

**updatedAt** date-time

Last update timestamp

Example:`2023-01-01T00:00:00Z`

**traceId** string

```json
{
  "success": true,
  "statusCode": 200,
  "results": {
    "message": "Queue paused successfully.",
    "queue": {
      "_id": "60af88475f1b2c001f5d5f4b",
      "locationId": "location-123",
      "categoryId": "60af88475f1b2c001f5d5f4b",
      "timeSlots": [\
        {\
          "dayOfWeek": 0,\
          "time": "09:00"\
        }\
      ],
      "enableFuturePosts": false,
      "prioritizeNewContent": false,
      "currentOrder": 1000,
      "status": "active",
      "startDate": "2023-01-01T12:00:00Z",
      "skipDateTime": [\
        "2023-01-02T12:00:00Z"\
      ],
      "currentPostId": "60af88475f1b2c001f5d5f4b",
      "totalPosts": 10,
      "lastScheduledTime": "2023-01-01T12:00:00Z",
      "createdBy": "user-123",
      "createdAt": "2023-01-01T00:00:00Z",
      "updatedAt": "2023-01-01T00:00:00Z"
    }
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
curl -L -X PUT 'https://services.leadconnectorhq.com/social-media-posting/category/queues/:queueId' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "locationId": "609e126a1c4ae1001291e1b5",
  "skipLegacyWatermark": false,
  "status": "paused",
  "skipDateTime": "2023-10-05T14:48:00.000Z",
  "timeSlots": [\
    {\
      "dayOfWeek": 0,\
      "time": "09:00"\
    }\
  ],
  "enableFuturePosts": true,
  "prioritizeNewContent": false
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
  "skipLegacyWatermark": false,
  "status": "paused",
  "skipDateTime": "2023-10-05T14:48:00.000Z",
  "timeSlots": [\
    {\
      "dayOfWeek": 0,\
      "time": "09:00"\
    }\
  ],
  "enableFuturePosts": true,
  "prioritizeNewContent": false
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!