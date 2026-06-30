---
title: "Get Free Slots"
source_url: https://marketplace.gohighlevel.com/docs/ghl/calendars/get-slots
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/calendars/:calendarId/free-slots
---
# Get Free Slots

```
GET https://services.leadconnectorhq.com/calendars/:calendarId/free-slots
```


Get free slots for a calendar between a date range. Optionally a consumer can also request free slots in a particular timezone and also for a particular user.

### Requirements

#### Scope(s)

`calendars.readonly`

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

**calendarId** stringrequired

Calendar Id

Example: ocQHyuzHvysMo5N5VsXc

### Query Parameters

**startDate** numberrequired

Start Date ( **⚠️ Important:** Date range cannot be more than 31 days)

Example: 1548898600000

**endDate** numberrequired

End Date ( **⚠️ Important:** Date range cannot be more than 31 days)

Example: 1601490599999

**timezone** string

The timezone in which the free slots are returned

Example: America/Chihuahua

**userId** string

The user for whom the free slots are returned

Example: 082goXVW3lIExEQPOnd3

**userIds** string\[\]

The users for whom the free slots are returned

## Responses

- 200
- 400
- 401

Availability map keyed by date (YYYY-MM-DD)

- application/json

- Schema
- Example (auto)

**Schema**

**property name\*** SlotsSchema

**slots** string\[\]required

Example:`["2024-10-28T10:00:00-05:00","2024-10-28T11:00:00-05:00"]`

```json
{
  "2024-10-28": {
    "slots": [\
      "2024-10-28T10:00:00-05:00",\
      "2024-10-28T11:00:00-05:00"\
    ]
  },
  "2024-10-29": {
    "slots": [\
      "2024-10-29T10:00:00-05:00",\
      "2024-10-29T14:30:00-05:00"\
    ]
  }
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

## Share your feedback

★★★★★

#### Authorization: Authorization

```
name: Authorizationtype: httpscopes: calendars.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/calendars/:calendarId/free-slots' \
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

calendarId — pathrequired

startDate — queryrequired

endDate — queryrequired

Version — headerrequired

\-\-\-v3

Show optional parameters

timezone — query

userId — query

userIds — query

Add item

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!