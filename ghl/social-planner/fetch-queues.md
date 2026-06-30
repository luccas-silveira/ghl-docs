---
title: "Fetch category queues for a location"
source_url: https://marketplace.gohighlevel.com/docs/ghl/social-planner/fetch-queues
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/social-media-posting/category/queues/list
---
# Fetch category queues for a location

```
POST https://services.leadconnectorhq.com/social-media-posting/category/queues/list
```


Retrieves a paginated list of all category queues for a given location, excluding any that have been marked as deleted.

### Requirements

#### Scope(s)

`socialplanner/category.readonly`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/social-planner/fetch-queues/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

Example: v3

- application/json

### Body **required**

**locationId** stringrequired

Location ID

Example:`609e126a1c4ae1001291e1b5`

**skip** number

Number of items to skip

Example:`0`

**limit** number

Maximum number of items to return

Example:`10`

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/social-planner/fetch-queues/\#responses "Direct link to Responses")

- 201
- 400
- 401
- 422

Successfully retrieved category queues.

- application/json

- Schema
- Example (auto)

**Schema**

**success** booleanrequired

Example:`true`

**statusCode** numberrequired

Example:`201`

**results** objectrequired

**message** string

Example:`Queues fetched successfully`

**queues** object\[\]

Array \[\
\
**\_id** string\
\
Queue ID\
\
Example:`60af88475f1b2c001f5d5f4b`\
\
**locationId** string\
\
Location ID\
\
Example:`location-123`\
\
**categoryId** string\
\
Category ID\
\
Example:`60af88475f1b2c001f5d5f4b`\
\
**timeSlots** object\[\]\
\
Time slots for scheduling posts\
\
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
\]\
\
**enableFuturePosts** boolean\
\
Enable posting future content\
\
Example:`false`\
\
**prioritizeNewContent** boolean\
\
Prioritize new content over older content\
\
Example:`false`\
\
**currentOrder** number\
\
Current order number in the queue\
\
Example:`1000`\
\
**status** string\
\
Status of the queue. Possible values: active, paused, draft.\
\
**Possible values:** \[`active`, `paused`, `draft`\]\
\
Example:`active`\
\
**startDate** date-time\
\
Start date of the queue\
\
Example:`2023-01-01T12:00:00Z`\
\
**skipDateTime** date-time\[\]\
\
Dates/times to skip posting\
\
Example:`["2023-01-02T12:00:00Z"]`\
\
**currentPostId** stringnullable\
\
ID of the currently scheduled post\
\
Example:`60af88475f1b2c001f5d5f4b`\
\
**totalPosts** number\
\
Total number of posts in the queue\
\
Example:`10`\
\
**lastScheduledTime** date-timenullable\
\
Timestamp of the last scheduled post\
\
Example:`2023-01-01T12:00:00Z`\
\
**createdBy** string\
\
ID of the user who created the queue\
\
Example:`user-123`\
\
**createdAt** date-time\
\
Creation timestamp\
\
Example:`2023-01-01T00:00:00Z`\
\
**updatedAt** date-time\
\
Last update timestamp\
\
Example:`2023-01-01T00:00:00Z`\
\
**category** object\
\
The category associated with the queue.\
\
**\_id** string\
\
Category ID\
\
Example:`6756f381be2553245b08d30c`\
\
**name** string\
\
Name of the category\
\
Example:`Category Name`\
\
**primaryColor** string\
\
Primary color of the category\
\
Example:`#FFFFFF`\
\
**secondaryColor** string\
\
Secondary color of the category\
\
Example:`#000000`\
\
**deleted** boolean\
\
Indicates if the category is deleted\
\
Example:`false`\
\
**locationId** string\
\
Location ID\
\
Example:`fvg1TXIiVxGcdOaL0riG`\
\
**createdBy** string\
\
ID of the user who created the category\
\
Example:`SQ6d63Va2PUbWEZ9k0TD`\
\
**createdAt** string\
\
Creation timestamp\
\
Example:`2024-12-09T13:41:21.385Z`\
\
**updatedAt** string\
\
Last update timestamp\
\
Example:`2024-12-09T13:41:21.385Z`\
\
\]

**meta** object

**count** string

Total count of items

Example:`100`

**traceId** string

```json
{
  "success": true,
  "statusCode": 201,
  "results": {
    "message": "Queues fetched successfully",
    "queues": [\
      {\
        "_id": "60af88475f1b2c001f5d5f4b",\
        "locationId": "location-123",\
        "categoryId": "60af88475f1b2c001f5d5f4b",\
        "timeSlots": [\
          {\
            "dayOfWeek": 0,\
            "time": "09:00"\
          }\
        ],\
        "enableFuturePosts": false,\
        "prioritizeNewContent": false,\
        "currentOrder": 1000,\
        "status": "active",\
        "startDate": "2023-01-01T12:00:00Z",\
        "skipDateTime": [\
          "2023-01-02T12:00:00Z"\
        ],\
        "currentPostId": "60af88475f1b2c001f5d5f4b",\
        "totalPosts": 10,\
        "lastScheduledTime": "2023-01-01T12:00:00Z",\
        "createdBy": "user-123",\
        "createdAt": "2023-01-01T00:00:00Z",\
        "updatedAt": "2023-01-01T00:00:00Z",\
        "category": {\
          "_id": "6756f381be2553245b08d30c",\
          "name": "Category Name",\
          "primaryColor": "#FFFFFF",\
          "secondaryColor": "#000000",\
          "deleted": false,\
          "locationId": "fvg1TXIiVxGcdOaL0riG",\
          "createdBy": "SQ6d63Va2PUbWEZ9k0TD",\
          "createdAt": "2024-12-09T13:41:21.385Z",\
          "updatedAt": "2024-12-09T13:41:21.385Z"\
        }\
      }\
    ],
    "meta": {
      "count": "100"
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
curl -L 'https://services.leadconnectorhq.com/social-media-posting/category/queues/list' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "locationId": "609e126a1c4ae1001291e1b5",
  "skip": 0,
  "limit": 10
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
  "skip": 0,
  "limit": 10
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!