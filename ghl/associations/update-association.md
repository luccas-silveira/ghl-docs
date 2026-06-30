---
title: "Update Association By Id"
source_url: https://marketplace.gohighlevel.com/docs/ghl/associations/update-association
version: v3
method: PUT
endpoint: https://services.leadconnectorhq.com/associations/:associationId
---
# Update Association By Id

```
PUT https://services.leadconnectorhq.com/associations/:associationId
```


Update Association , Allows you to update labels of an associations. Documentation Link - [https://doc.clickup.com/8631005/d/h/87cpx-293776/cd0f4122abc04d3](https://doc.clickup.com/8631005/d/h/87cpx-293776/cd0f4122abc04d3)

### Requirements

#### Scope(s)

`associations.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/associations/update-association/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

### Path Parameters

**associationId** stringrequired

- application/json

### Body **required**

**firstObjectLabel** objectrequired

Example:`student`

**secondObjectLabel** objectrequired

Example:`tutor`

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/associations/update-association/\#responses "Direct link to Responses")

- 200
- 400
- 401
- 422

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**locationId** stringrequired

Example:`string`

**id** stringrequired

Example:`ve9EPM428h8vShlRW1KT`

**key** stringrequired

First Objects Association Label (custom\_objects.children)

Example:`student`

**firstObjectLabel** objectrequired

First Objects Association Label (custom\_objects.children)

Example:`student`

**firstObjectKey** objectrequired

First Objects Key

Example:`custom_objects.children`

**secondObjectLabel** objectrequired

Second Object Association Label (contact)

Example:`Teacher`

**secondObjectKey** objectrequired

Second Objects Key

Example:`contact`

**associationType** objectrequired

Association Type can be USER\_DEFINED or SYSTEM\_DEFINED

Example:`USER_DEFINED`

```json
{
  "locationId": "string",
  "id": "ve9EPM428h8vShlRW1KT",
  "key": "student",
  "firstObjectLabel": "student",
  "firstObjectKey": "custom_objects.children",
  "secondObjectLabel": "Teacher",
  "secondObjectKey": "contact",
  "associationType": "USER_DEFINED"
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

Unprocessable Entity

- application/json

- Schema
- Example (auto)

**Schema**

**statusCode** number

Example:`422`

**message** string\[\]

Example:`["Unprocessable Entity"]`

**error** string

Example:`Unprocessable Entity`

```json
{
  "statusCode": 422,
  "message": [\
    "Unprocessable Entity"\
  ],
  "error": "Unprocessable Entity"
}
```

## Share your feedback

★★★★★

#### Authorization: Authorization

```
name: Authorizationtype: httpscopes: associations.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L -X PUT 'https://services.leadconnectorhq.com/associations/:associationId' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "firstObjectLabel": "student",
  "secondObjectLabel": "tutor"
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

associationId — pathrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "firstObjectLabel": "student",
  "secondObjectLabel": "tutor"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!