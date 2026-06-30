---
title: "Delete Event"
source_url: https://marketplace.gohighlevel.com/docs/ghl/calendars/delete-event
version: v3
method: DELETE
endpoint: https://services.leadconnectorhq.com/calendars/events/:eventId
---
# Delete Event

```
DELETE https://services.leadconnectorhq.com/calendars/events/:eventId
```


Delete event by ID

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

**eventId** stringrequired

Event Id or Instance id. For recurring appointments send masterEventId to modify original series.

Examples:

- example1
- example2

Event ID

Example:`ocQHyuzHvysMo5N5VsXc`

Recurring Instance ID

Example:`ocQHyuzHvysMo5N5VsXc_1729821600000_1800`

- application/json

### Body **required**

object

## Responses

- 201
- 400
- 401

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**succeeded** boolean

Example:`true`

```json
{
  "succeeded": true
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
curl -L -X DELETE 'https://services.leadconnectorhq.com/calendars/events/:eventId' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{}'
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

Body required

```json
{}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!