---
title: "Fetch slot information for queue items"
source_url: https://marketplace.gohighlevel.com/docs/ghl/social-planner/fetch-slots
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/social-media-posting/category/queues/:queueId/slots
---
# Fetch slot information for queue items

```
POST https://services.leadconnectorhq.com/social-media-posting/category/queues/:queueId/slots
```


Returns paginated slot information (scheduledDateTime, isSkipped) for queue items. Pass sessionId to get slots for draft items, or omit for live items. Call this after mutations to refresh slot data.

### Requirements

#### Scope(s)

`socialplanner/category.readonly`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/social-planner/fetch-slots/\#request "Direct link to Request")

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

The location ID

Example:`abc123`

**sessionId** string

Session ID for edit mode. If not provided, calculates slots for live items.

Example:`507f1f77bcf86cd799439011`

**skip** number

Number of items to skip

**Default value:** `0`

Example:`0`

**limit** number

Number of items to return

**Default value:** `20`

Example:`20`

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/social-planner/fetch-slots/\#responses "Direct link to Responses")

- 201
- 400
- 401
- 422

Slots fetched successfully.

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

Example:`Slots fetched successfully`

**slots** object\[\]

Slot information for items in the requested range

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

**total** number

Total number of items in the queue

Example:`100`

**skip** number

Number of items skipped

Example:`0`

**limit** number

Number of items returned

Example:`20`

**timezone** string

Timezone used for slot calculations

Example:`America/New_York`

**traceId** string

```json
{
  "success": true,
  "statusCode": 200,
  "results": {
    "message": "Slots fetched successfully",
    "slots": [\
      {\
        "itemId": "60af88475f1b2c001f5d5f4b",\
        "scheduledDateTime": "2023-10-15T10:00:00.000Z",\
        "isSkipped": false\
      }\
    ],
    "total": 100,
    "skip": 0,
    "limit": 20,
    "timezone": "America/New_York"
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
curl -L 'https://services.leadconnectorhq.com/social-media-posting/category/queues/:queueId/slots' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "locationId": "abc123",
  "sessionId": "507f1f77bcf86cd799439011",
  "skip": 0,
  "limit": 20
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
  "locationId": "abc123",
  "sessionId": "507f1f77bcf86cd799439011",
  "skip": 0,
  "limit": 20
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!