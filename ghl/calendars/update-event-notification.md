---
title: "Update notification"
source_url: https://marketplace.gohighlevel.com/docs/ghl/calendars/update-event-notification
version: v3
method: PUT
endpoint: https://services.leadconnectorhq.com/calendars/:calendarId/notifications/:notificationId
summary: "Update Event notification by id"
---
# Update notification

```
PUT https://services.leadconnectorhq.com/calendars/:calendarId/notifications/:notificationId
```


Update Event notification by id

### Requirements

#### Scope(s)

`calendars/events.write`

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

**notificationId** stringrequired

- application/json

### Body **required**

**receiverType** string

Notification recipient type

**Possible values:** \[`contact`, `guest`, `assignedUser`, `emails`, `phoneNumbers`, `business`\]

**additionalEmailIds** string\[\]

Additional email addresses to receive notifications.

Example:`["example1@email.com","example2@email.com"]`

**additionalPhoneNumbers** string\[\]

Additional phone numbers to receive notifications.

Example:`["+919876744444","+919876744445"]`

**selectedUsers** string\[\]

Selected users for in-App and business email notifications. Supports user IDs and special keyword "sub\_account\_admin"

Example:`["userId1","userId2","sub_account_admin"]`

**channel** string

Notification channel

**Possible values:** \[`email`, `inApp`, `sms`, `whatsapp`\]

**notificationType** string

Notification type

**Possible values:** \[`booked`, `confirmation`, `cancellation`, `reminder`, `followup`, `reschedule`\]

**isActive** boolean

Is the notification active

**Default value:** `true`

**deleted** boolean

Marks the notification as deleted (soft delete)

**Default value:** `false`

**templateId** string

Template ID for email notification

**body** string

Body for email notification. Not necessary for in-App notification

**subject** string

Subject for email notification. Not necessary for in-App notification

**afterTime** object\[\]

Specifies the time after which the follow-up notification should be sent. This is not required for other notification types.

Array \[\
\
**timeOffset** number\
\
**unit** string\
\
\]

**beforeTime** object\[\]

Specifies the time before which the reminder notification should be sent. This is not required for other notification types.

Array \[\
\
**timeOffset** number\
\
**unit** string\
\
\]

**fromAddress** string

From address for email notification

**fromNumber** string

from number for sms notification

**fromName** string

From name for email/sms notification

## Responses

- 200
- 400
- 401

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**message** stringrequired

Result of delete/update operation

```json
{
  "message": "string"
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
name: Authorizationtype: httpscopes: calendars/events.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L -X PUT 'https://services.leadconnectorhq.com/calendars/:calendarId/notifications/:notificationId' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
--data-raw '{
  "receiverType": "contact",
  "additionalEmailIds": [\
    "example1@email.com",\
    "example2@email.com"\
  ],
  "additionalPhoneNumbers": [\
    "+919876744444",\
    "+919876744445"\
  ],
  "selectedUsers": [\
    "userId1",\
    "userId2",\
    "sub_account_admin"\
  ],
  "channel": "email",
  "notificationType": "booked",
  "isActive": true,
  "deleted": false,
  "templateId": "string",
  "body": "string",
  "subject": "string",
  "afterTime": [\
    {\
      "timeOffset": 1,\
      "unit": "hours"\
    }\
  ],
  "beforeTime": [\
    {\
      "timeOffset": 1,\
      "unit": "hours"\
    }\
  ],
  "fromAddress": "string",
  "fromNumber": "string",
  "fromName": "string"
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

calendarId — pathrequired

notificationId — pathrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "receiverType": "contact",
  "additionalEmailIds": [\
    "example1@email.com",\
    "example2@email.com"\
  ],
  "additionalPhoneNumbers": [\
    "+919876744444",\
    "+919876744445"\
  ],
  "selectedUsers": [\
    "userId1",\
    "userId2",\
    "sub_account_admin"\
  ],
  "channel": "email",
  "notificationType": "booked",
  "isActive": true,
  "deleted": false,
  "templateId": "string",
  "body": "string",
  "subject": "string",
  "afterTime": [\
    {\
      "timeOffset": 1,\
      "unit": "hours"\
    }\
  ],
  "beforeTime": [\
    {\
      "timeOffset": 1,\
      "unit": "hours"\
    }\
  ],
  "fromAddress": "string",
  "fromNumber": "string",
  "fromName": "string"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!