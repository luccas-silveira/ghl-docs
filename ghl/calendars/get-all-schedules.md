---
title: "List user availability schedule"
source_url: https://marketplace.gohighlevel.com/docs/ghl/calendars/get-all-schedules
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/calendars/schedules/search
---
# List user availability schedule

```
GET https://services.leadconnectorhq.com/calendars/schedules/search
```


Retrieve user availability schedules based on various filters including location, calendar, and user. Supports pagination.

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

### Query Parameters

**locationId** stringrequired

Location ID to filter schedules by

Example: IkqiJlXJ7o9h61tCHHod

**userId** stringrequired

User ID to filter schedules by specific user

Example: IkqiJlXJ7o9h61tCHHod

**calendarId** string

Calendar ID for filtering schedules by specific calendar

Example: WvVX9LpvlBO6K506xLbp

**skip** number

Number of items to skip for pagination

Default value:`0`

Example: 0

**limit** number

**Possible values:**`>= 1` and `<= 500`

Maximum number of items to return (max 500)

Default value:`50`

Example: 50

## Responses

- 200
- 400
- 401

Schedules retrieved successfully

- application/json

- Schema
- Example (auto)

**Schema**

**schedules** object\[\]required

Array of schedules

Array \[\
\
**id** stringrequired\
\
Unique identifier for the schedule\
\
Example:`IkqiJlXJ7o9h61tCHHod`\
\
**name** stringrequired\
\
Human-readable name for the schedule\
\
Example:`Business Hours Schedule`\
\
**locationId** stringrequired\
\
Location ID where this schedule applies\
\
Example:`IkqiJlXJ7o9h61tCHHod`\
\
**rules** object\[\]required\
\
Schedule rules defining when the schedule is active\
\
Array \[\
\
**type** stringrequired\
\
Type of schedule rule - weekday (recurring) or date (specific date)\
\
**Possible values:** \[`wday`, `date`\]\
\
Example:`wday`\
\
**intervals** object\[\]required\
\
Time intervals for the rule (e.g., 9 AM to 5 PM)\
\
Array \[\
\
**from** stringrequired\
\
Start time in HH:MM format (24-hour format)\
\
**Possible values:** Value must match regular expression `^([01]?[0-9]|2[0-3]):[0-5][0-9]$`\
\
Example:`09:00`\
\
**to** stringrequired\
\
End time in HH:MM format (24-hour format)\
\
**Possible values:** Value must match regular expression `^([01]?[0-9]|2[0-3]):[0-5][0-9]$`\
\
Example:`17:00`\
\
\]\
\
**date** string\
\
Specific date in YYYY-MM-DD format (only for date-type rules)\
\
**Possible values:** Value must match regular expression `^\d{4}-\d{2}-\d{2}$`\
\
Example:`2023-04-15`\
\
**day** string\
\
Day of week (only for weekday-type rules)\
\
**Possible values:** \[`sunday`, `monday`, `tuesday`, `wednesday`, `thursday`, `friday`, `saturday`\]\
\
Example:`monday`\
\
\]\
\
**timezone** stringrequired\
\
Timezone for the schedule (IANA timezone identifier)\
\
Example:`America/New_York`\
\
**dateAdded** stringrequired\
\
ISO date string when the schedule was created\
\
Example:`2023-01-15T10:30:00.000Z`\
\
**dateUpdated** stringrequired\
\
ISO date string when the schedule was last updated\
\
Example:`2023-01-20T14:45:00.000Z`\
\
**userId** stringrequired\
\
User ID associated with the schedule\
\
Example:`IkqiJlXJ7o9h61tCHHod`\
\
**calendarIds** string\[\]\
\
Calendar IDs associated with the schedule\
\
**deleted** booleanrequired\
\
Whether the schedule has been deleted\
\
Example:`false`\
\
\]

```json
{
  "schedules": [\
    {\
      "id": "IkqiJlXJ7o9h61tCHHod",\
      "name": "Business Hours Schedule",\
      "locationId": "IkqiJlXJ7o9h61tCHHod",\
      "rules": [\
        {\
          "type": "wday",\
          "intervals": [\
            {\
              "from": "09:00",\
              "to": "17:00"\
            }\
          ],\
          "date": "2023-04-15",\
          "day": "monday"\
        }\
      ],\
      "timezone": "America/New_York",\
      "dateAdded": "2023-01-15T10:30:00.000Z",\
      "dateUpdated": "2023-01-20T14:45:00.000Z",\
      "userId": "IkqiJlXJ7o9h61tCHHod",\
      "calendarIds": [\
        "string"\
      ],\
      "deleted": false\
    }\
  ]
}
```

Invalid request parameters

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
curl -L 'https://services.leadconnectorhq.com/calendars/schedules/search' \
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

locationId — queryrequired

userId — queryrequired

Version — headerrequired

\-\-\-v3

Show optional parameters

calendarId — query

skip — query

limit — query

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!