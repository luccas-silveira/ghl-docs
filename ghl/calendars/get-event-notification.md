---
title: "Get notifications"
source_url: https://marketplace.gohighlevel.com/docs/ghl/calendars/get-event-notification
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/calendars/:calendarId/notifications
---
# Get notifications

```
GET https://services.leadconnectorhq.com/calendars/:calendarId/notifications
```


Get calendar notifications based on query

### Requirements

#### Scope(s)

`calendars/events.readonly`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/calendars/get-event-notification/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**calendarId** stringrequired

### Query Parameters

**isActive** boolean

**deleted** boolean

**limit** number

Number of records to return

Default value:`100`

**skip** number

Number of records to skip

Default value:`0`

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/calendars/get-event-notification/\#responses "Direct link to Responses")

- 200
- 400
- 401

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

Array \[\
\
**\_id** string\
\
Notification ID\
\
**receiverType** string\
\
**Possible values:** \[`contact`, `guest`, `assignedUser`, `emails`, `phoneNumbers`, `business`\]\
\
Example:`contact`\
\
**additionalEmailIds** string\[\]\
\
Example:`["example1@email.com","example2@email.com"]`\
\
**additionalPhoneNumbers** string\[\]\
\
Example:`["+919876744444","+919876744445"]`\
\
**channel** string\
\
**Possible values:** \[`email`, `inApp`, `sms`, `whatsapp`\]\
\
Example:`email`\
\
**notificationType** string\
\
**Possible values:** \[`booked`, `confirmation`, `cancellation`, `reminder`, `followup`, `reschedule`\]\
\
Example:`confirmation`\
\
**isActive** boolean\
\
Example:`true`\
\
**additionalWhatsappNumbers** string\[\]\
\
Example:`["+919876744444","+919876744445"]`\
\
**templateId** string\
\
Example:`0as9d8as0d`\
\
**body** string\
\
Example:`This is a test notification`\
\
**subject** string\
\
Example:`Test Notification`\
\
**afterTime** object\[\]\
\
Array \[\
\
**timeOffset** number\
\
**unit** string\
\
\]\
\
**beforeTime** object\[\]\
\
Array \[\
\
**timeOffset** number\
\
**unit** string\
\
\]\
\
**selectedUsers** string\[\]\
\
Example:`["user1","user2"]`\
\
**deleted** boolean\
\
Example:`false`\
\
\]

```json
[\
  {\
    "_id": "string",\
    "receiverType": "contact",\
    "additionalEmailIds": [\
      "example1@email.com",\
      "example2@email.com"\
    ],\
    "additionalPhoneNumbers": [\
      "+919876744444",\
      "+919876744445"\
    ],\
    "channel": "email",\
    "notificationType": "confirmation",\
    "isActive": true,\
    "additionalWhatsappNumbers": [\
      "+919876744444",\
      "+919876744445"\
    ],\
    "templateId": "0as9d8as0d",\
    "body": "This is a test notification",\
    "subject": "Test Notification",\
    "afterTime": [\
      {\
        "timeOffset": 1,\
        "unit": "hours"\
      }\
    ],\
    "beforeTime": [\
      {\
        "timeOffset": 1,\
        "unit": "hours"\
      }\
    ],\
    "selectedUsers": [\
      "user1",\
      "user2"\
    ],\
    "deleted": false\
  }\
]
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
curl -L 'https://services.leadconnectorhq.com/calendars/:calendarId/notifications' \
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

Version — headerrequired

\-\-\-v3

Show optional parameters

isActive — query

\-\-\-truefalse

deleted — query

\-\-\-truefalse

limit — query

skip — query

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!