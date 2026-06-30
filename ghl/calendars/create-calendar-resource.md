---
title: "Create Calendar Resource"
source_url: https://marketplace.gohighlevel.com/docs/ghl/calendars/create-calendar-resource
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/calendars/resources/:resourceType
summary: "This endpoint has been deprecated and may be replaced or removed in future versions of the API"
---
# Create Calendar Resource

```
POST https://services.leadconnectorhq.com/calendars/resources/:resourceType
```


deprecated

This endpoint has been deprecated and may be replaced or removed in future versions of the API.

Create calendar resource by resource type (Services V1)

### Requirements

#### Scope(s)

`calendars/resources.write`

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

- application/json

### Body **required**

**locationId** stringrequired

**name** stringrequired

**description** stringrequired

**quantity** numberrequired

Quantity of the equipment.

**outOfService** numberrequired

Quantity of the out of service equipment.

**capacity** numberrequired

Capacity of the room.

**calendarIds** string\[\]required

Service calendar IDs to be mapped with the resource.

```text
One equipment can only be mapped with one service calendar.
```

One room can be mapped with multiple service calendars.

**Possible values:**`<= 100`

## Responses

- 201
- 400
- 401

Calendar resource created

- application/json

- Schema
- Example (auto)

**Schema**

**locationId** stringrequired

Location ID of the resource

**name** stringrequired

Name of the resource

Example:`yoga room`

**resourceType** stringrequired

**Possible values:** \[`equipments`, `rooms`\]

**isActive** booleanrequired

Whether the resource is active

**description** string

Description of the resource

**quantity** number

Quantity of the resource

**outOfService** number

Indicates if the resource is out of service

Example:`0`

**capacity** number

Capacity of the resource

Example:`85`

**calendarIds** string\[\]required

Calendar IDs

Example:`["Jsj0xnlDDjw0SuvX1J13","oCM5feFC86FAAbcO7lJK"]`

```json
{
  "locationId": "string",
  "name": "yoga room",
  "resourceType": "equipments",
  "isActive": true,
  "description": "string",
  "quantity": 0,
  "outOfService": 0,
  "capacity": 85,
  "calendarIds": [\
    "Jsj0xnlDDjw0SuvX1J13",\
    "oCM5feFC86FAAbcO7lJK"\
  ]
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
curl -L 'https://services.leadconnectorhq.com/calendars/resources/:resourceType' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "locationId": "string",
  "name": "string",
  "description": "string",
  "quantity": 0,
  "outOfService": 0,
  "capacity": 0,
  "calendarIds": [\
    "string"\
  ]
}'
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

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "locationId": "string",
  "name": "string",
  "description": "string",
  "quantity": 0,
  "outOfService": 0,
  "capacity": 0,
  "calendarIds": [\
    "string"\
  ]
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!