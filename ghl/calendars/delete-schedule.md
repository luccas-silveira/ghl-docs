---
title: "Delete user availability schedule"
source_url: https://marketplace.gohighlevel.com/docs/ghl/calendars/delete-schedule
version: v3
method: DELETE
endpoint: https://services.leadconnectorhq.com/calendars/schedules/:id
---
# Delete user availability schedule

```
DELETE https://services.leadconnectorhq.com/calendars/schedules/:id
```


Permanently remove a schedule and all its associated rules. This action cannot be undone.

### Requirements

#### Scope(s)

`calendars.write`

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

**id** stringrequired

Unique identifier of the schedule to delete

Example: sch123def456ghi789

## Responses

- 200
- 400
- 401
- 404

Schedule deleted successfully

- application/json

- Schema
- Example (auto)

**Schema**

**success** boolean

Whether the deletion was successful

Example:`true`

```json
{
  "success": true
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

Schedule with the specified ID was not found

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
curl -L -X DELETE 'https://services.leadconnectorhq.com/calendars/schedules/:id' \
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

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!