---
title: "Get Appointment"
source_url: https://marketplace.gohighlevel.com/docs/ghl/calendars/get-appointment
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/calendars/events/appointments/:eventId
---
# Get Appointment

```
GET https://services.leadconnectorhq.com/calendars/events/appointments/:eventId
```


Get appointment by ID

### Requirements

#### Scope(s)

`calendars/events.readonly`

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

**eventId** stringrequired

Event Id or Instance id. For recurring appointments send masterEventId to modify original series.

Examples:

- example1
- example2

Event ID

Example:`ocQHyuzHvysMo5N5VsXc`

Recurring Instance ID

Example:`ocQHyuzHvysMo5N5VsXc_1729821600000_1800`

## Responses

- 200
- 400
- 401

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**event** object

**id** stringrequired

Event Id or Instance id for a recurring event

**address** string

Calendar Event address

Example:`https://meet.google.com/yqp-gogr-wve`

**title** stringrequired

Calendar Event title

Example:`Appointment with GHL Dev team`

**calendarId** stringrequired

Calendar ID

Example:`BqTwX8QFwXzpegMve9EQ`

**locationId** stringrequired

Location ID

Example:`0007BWpSzSwfiuSl0tR2`

**contactId** stringrequired

Contact ID

Example:`9NkT25Vor1v4aQatFsv2`

**groupId** stringrequired

Group ID

Example:`9NkT25Vor1v4aQatFsv2`

**appointmentStatus** stringrequired

Appointment Status

Example:`confirmed`

**assignedUserId** stringrequired

AssignedUser - the primary owner of an appointment

Example:`YlWd2wuCAZQzh2cH1fVZ`

**users** string\[\]required

Users - the secondary owners of an appointment.

Example:`["YlWd2wuCAZQzh2cH1fVZ","9NkT25Vor1v4aQatFsv2"]`

**notes** string

Notes

Example:`Some dummy note`

**description** string

Description

Example:`Some dummy description`

**isRecurring** boolean

true if the event is recurring otherwise false

Example:`true`

**rrule** string

RRULE as per the iCalendar (RFC 5545) specification for recurring events. DTSTART is not required, instance ids are calculated on the basis of startTime of the event.

**deleted** boolean

Tells if a calendar event has been deleted

Example:`false`

**startTime** objectrequired

Start Time

Example:`2023-09-25T16:00:00+05:30`

**endTime** objectrequired

End Time

Example:`2023-09-25T16:00:00+05:30`

**dateAdded** objectrequired

Date Added

Example:`2023-09-25T16:00:00+05:30`

**dateUpdated** objectrequired

Date Updated

Example:`2023-09-25T16:00:00+05:30`

**assignedResources** string\[\]

Ids of associated resources rooms and/or equipments

**createdBy** object

Appointment booked by metadata

**userId** string

The ID of the user who created or updated the appointment

**source** stringrequired

The source of the appointment

**masterEventId** string

Master event id for a recurring instance

Example:`ocWd2wuBGAQzh2cH1fSZ`

```json
{
  "event": {
    "id": "string",
    "address": "https://meet.google.com/yqp-gogr-wve",
    "title": "Appointment with GHL Dev team",
    "calendarId": "BqTwX8QFwXzpegMve9EQ",
    "locationId": "0007BWpSzSwfiuSl0tR2",
    "contactId": "9NkT25Vor1v4aQatFsv2",
    "groupId": "9NkT25Vor1v4aQatFsv2",
    "appointmentStatus": "confirmed",
    "assignedUserId": "YlWd2wuCAZQzh2cH1fVZ",
    "users": [\
      "YlWd2wuCAZQzh2cH1fVZ",\
      "9NkT25Vor1v4aQatFsv2"\
    ],
    "notes": "Some dummy note",
    "description": "Some dummy description",
    "isRecurring": "true",
    "rrule": "string",
    "deleted": false,
    "startTime": "2023-09-25T16:00:00+05:30",
    "endTime": "2023-09-25T16:00:00+05:30",
    "dateAdded": "2023-09-25T16:00:00+05:30",
    "dateUpdated": "2023-09-25T16:00:00+05:30",
    "assignedResources": [\
      "string"\
    ],
    "createdBy": {
      "userId": "string",
      "source": "string"
    },
    "masterEventId": "ocWd2wuBGAQzh2cH1fSZ"
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
name: Authorizationtype: httpscopes: calendars/events.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/calendars/events/appointments/:eventId' \
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

eventId — pathrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!