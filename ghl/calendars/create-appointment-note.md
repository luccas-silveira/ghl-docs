---
title: "Create Note"
source_url: https://marketplace.gohighlevel.com/docs/ghl/calendars/create-appointment-note
version: v3
method: POST
endpoint: https://services.leadconnectorhq.com/calendars/appointments/:appointmentId/notes
---
# Create Note

```
POST https://services.leadconnectorhq.com/calendars/appointments/:appointmentId/notes
```


Create Note

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

**appointmentId** stringrequired

Appointment ID

- application/json

### Body **required**

**userId** string

Example:`GCs5KuzPqTls7vWclkEV`

**body** stringrequired

Note body

**Possible values:**`<= 5000 characters`

Example:`lorem ipsum`

## Responses

- 201
- 400
- 401

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**note** object

**id** string

Example:`HGPcayliwcdoUFzvbTok`

**body** string

Example:`lorem ipsum`

**userId** string

Example:`TUcmRxWrjqzJS8EjkxNK`

**dateAdded** string

Example:`2021-07-08T12:02:11.285Z`

**contactId** string

Example:`TUcmRxWrjqzJS8EjkxNK`

**createdBy** object

**id** string

Example:`TUcmRxWr`

**name** string

Example:`John Doe`

```json
{
  "note": {
    "id": "HGPcayliwcdoUFzvbTok",
    "body": "lorem ipsum",
    "userId": "TUcmRxWrjqzJS8EjkxNK",
    "dateAdded": "2021-07-08T12:02:11.285Z",
    "contactId": "TUcmRxWrjqzJS8EjkxNK",
    "createdBy": {
      "id": "TUcmRxWr",
      "name": "John Doe"
    }
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
curl -L 'https://services.leadconnectorhq.com/calendars/appointments/:appointmentId/notes' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "userId": "GCs5KuzPqTls7vWclkEV",
  "body": "lorem ipsum"
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

appointmentId — pathrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "userId": "GCs5KuzPqTls7vWclkEV",
  "body": "lorem ipsum"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!