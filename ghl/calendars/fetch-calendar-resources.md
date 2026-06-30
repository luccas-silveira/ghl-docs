---
title: "List Calendar Resources"
source_url: https://marketplace.gohighlevel.com/docs/ghl/calendars/fetch-calendar-resources
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/calendars/resources/:resourceType
summary: "This endpoint has been deprecated and may be replaced or removed in future versions of the API"
---
# List Calendar Resources

```
GET https://services.leadconnectorhq.com/calendars/resources/:resourceType
```


deprecated

This endpoint has been deprecated and may be replaced or removed in future versions of the API.

List calendar resources by resource type and location ID (Services V1)

### Requirements

#### Scope(s)

`calendars/resources.readonly`

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

**resourceType** stringrequired

**Possible values:** \[`equipments`, `rooms`\]

Calendar Resource Type

### Query Parameters

**locationId** stringrequired

**limit** numberrequired

**skip** numberrequired

## Responses

- 200
- 400
- 401

Calendar resources listed

- application/json

- Schema
- Example (auto)

**Schema**

Array \[\
\
**locationId** stringrequired\
\
Location ID of the resource\
\
**name** stringrequired\
\
Name of the resource\
\
Example:`yoga room`\
\
**resourceType** stringrequired\
\
**Possible values:** \[`equipments`, `rooms`\]\
\
**isActive** booleanrequired\
\
Whether the resource is active\
\
**description** string\
\
Description of the resource\
\
**quantity** number\
\
Quantity of the resource\
\
**outOfService** number\
\
Indicates if the resource is out of service\
\
Example:`0`\
\
**capacity** number\
\
Capacity of the resource\
\
Example:`85`\
\
**calendarIds** string\[\]required\
\
Calendar IDs\
\
Example:`["Jsj0xnlDDjw0SuvX1J13","oCM5feFC86FAAbcO7lJK"]`\
\
\]

```json
[\
  {\
    "locationId": "string",\
    "name": "yoga room",\
    "resourceType": "equipments",\
    "isActive": true,\
    "description": "string",\
    "quantity": 0,\
    "outOfService": 0,\
    "capacity": 85,\
    "calendarIds": [\
      "Jsj0xnlDDjw0SuvX1J13",\
      "oCM5feFC86FAAbcO7lJK"\
    ]\
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
name: Authorizationtype: httpscopes: calendars/resources.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/calendars/resources/:resourceType' \
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

locationId — queryrequired

limit — queryrequired

skip — queryrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!