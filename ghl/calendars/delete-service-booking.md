---
title: "Delete Service Booking"
source_url: https://marketplace.gohighlevel.com/docs/ghl/calendars/delete-service-booking
version: v3
method: DELETE
endpoint: https://services.leadconnectorhq.com/calendars/services/bookings/:bookingId
---
# Delete Service Booking

```
DELETE https://services.leadconnectorhq.com/calendars/services/bookings/:bookingId
```


Delete a service booking by ID

### Requirements

#### Scope(s)

`calendars/events.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/calendars/delete-service-booking/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**bookingId** stringrequired

Unique Service Booking ID

Example: IkqiJlXJ7o9h61tCHHod

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/calendars/delete-service-booking/\#responses "Direct link to Responses")

- 200
- 400
- 401

Booking deleted successfully

- application/json

- Schema
- Example (auto)

**Schema**

**success** booleanrequired

Indicates if the deletion was successful

Example:`true`

**message** stringrequired

Response message

Example:`Service booking deleted successfully`

```json
{
  "success": true,
  "message": "Service booking deleted successfully"
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
curl -L -X DELETE 'https://services.leadconnectorhq.com/calendars/services/bookings/:bookingId' \
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

bookingId — pathrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!