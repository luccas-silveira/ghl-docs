---
title: "Update Group"
source_url: https://marketplace.gohighlevel.com/docs/ghl/calendars/edit-group
version: v3
method: PUT
endpoint: https://services.leadconnectorhq.com/calendars/groups/:groupId
---
# Update Group

```
PUT https://services.leadconnectorhq.com/calendars/groups/:groupId
```


Update Group by group ID

### Requirements

#### Scope(s)

`calendars/groups.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/calendars/edit-group/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**groupId** stringrequired

Group Id

Example: ocQHyuzHvysMo5N5VsXc

- application/json

### Body **required**

**name** stringrequired

Example:`group a`

**description** stringrequired

Example:`group description`

**slug** stringrequired

Example:`15-mins`

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/calendars/edit-group/\#responses "Direct link to Responses")

- 200
- 400
- 401

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**group** object

**locationId** stringrequired

Example:`ocQHyuzHvysMo5N5VsXc`

**name** stringrequired

Example:`group a`

**description** stringrequired

Example:`group description`

**slug** stringrequired

Example:`15-mins`

**isActive** boolean

Example:`true`

**id** string

Example:`ocQHyuzHvysMo5N5VsXc`

```json
{
  "group": {
    "locationId": "ocQHyuzHvysMo5N5VsXc",
    "name": "group a",
    "description": "group description",
    "slug": "15-mins",
    "isActive": true,
    "id": "ocQHyuzHvysMo5N5VsXc"
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
name: Authorizationtype: httpscopes: calendars/groups.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L -X PUT 'https://services.leadconnectorhq.com/calendars/groups/:groupId' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "name": "group a",
  "description": "group description",
  "slug": "15-mins"
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

groupId — pathrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "name": "group a",
  "description": "group description",
  "slug": "15-mins"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!