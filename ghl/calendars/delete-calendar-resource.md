---
title: "Delete Calendar Resource"
source_url: https://marketplace.gohighlevel.com/docs/ghl/calendars/delete-calendar-resource
version: v3
method: DELETE
endpoint: https://services.leadconnectorhq.com/calendars/resources/:resourceType/:id
---
# Delete Calendar Resource

```
DELETE https://services.leadconnectorhq.com/calendars/resources/:resourceType/:id
```


deprecated

This endpoint has been deprecated and may be replaced or removed in future versions of the API.

Delete calendar resource by ID (Services V1)

### Requirements

#### Scope(s)

`calendars/resources.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/calendars/delete-calendar-resource/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**resourceType** stringrequired

**Possible values:** \[`equipments`, `rooms`\]

Calendar Resource Type

**id** stringrequired

Calendar Resource ID

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/calendars/delete-calendar-resource/\#responses "Direct link to Responses")

- 200
- 400
- 401

Calendar resource deleted

- application/json

- Schema
- Example (auto)

**Schema**

**success** boolean

Success

Example:`true`

```json
{
  "success": "true"
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
name: Authorizationtype: httpscopes: calendars/resources.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L -X DELETE 'https://services.leadconnectorhq.com/calendars/resources/:resourceType/:id' \
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

resourceType — pathrequired

\-\-\-equipmentsrooms

id — pathrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!