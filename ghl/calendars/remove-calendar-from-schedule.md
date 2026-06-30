---
title: "Remove user availability schedule from a calendar"
source_url: https://marketplace.gohighlevel.com/docs/ghl/calendars/remove-calendar-from-schedule
version: v3
method: DELETE
endpoint: https://services.leadconnectorhq.com/calendars/schedules/:id/associations/:calendarId
---
# Remove user availability schedule from a calendar

```
DELETE https://services.leadconnectorhq.com/calendars/schedules/:id/associations/:calendarId
```


Removes the association between a team calendar and the given schedule by removing the calendarId from the schedule

### Requirements

#### Scope(s)

`calendars.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/calendars/remove-calendar-from-schedule/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**id** stringrequired

Unique identifier of the schedule

Example: IkqiJlXJ7o9h61tCHHod

**calendarId** stringrequired

Unique identifier of the calendar to remove from the schedule

Example: WvVX9LpvlBO6K506xLbp

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/calendars/remove-calendar-from-schedule/\#responses "Direct link to Responses")

- 200
- 400
- 401
- 404

Calendar successfully removed from schedule

- application/json

- Schema
- Example (auto)

**Schema**

**success** boolean

Example:`true`

```json
{
  "success": true
}
```

Schedule and calendar must belong to the same location

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

User not authenticated

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

Schedule or calendar not found

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

## Share your feedback

★★★★★

#### Authorization: Authorization

```
name: Authorizationtype: httpscopes: calendars.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L -X DELETE 'https://services.leadconnectorhq.com/calendars/schedules/:id/associations/:calendarId' \
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

id — pathrequired

calendarId — pathrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!