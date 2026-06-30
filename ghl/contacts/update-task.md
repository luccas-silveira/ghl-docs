---
title: "Update Task"
source_url: https://marketplace.gohighlevel.com/docs/ghl/contacts/update-task
version: v3
method: PUT
endpoint: https://services.leadconnectorhq.com/contacts/:contactId/tasks/:taskId
summary: "Title of the task"
---
# Update Task

```
PUT https://services.leadconnectorhq.com/contacts/:contactId/tasks/:taskId
```

Update Task

### Requirements

#### Scope(s)

`contacts.write`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

Example: v3

### Path Parameters

**contactId** stringrequired

Contact Id

Example: ve9EPM428h8vShlRW1KT

**taskId** stringrequired

Task Id

Example: ocQHyuzHvysMo5N5VsXc

- application/json

### Body **required**

**title** string

Title of the task

Example:`First Task`

**body** string

Body or description of the task

Example:`loram ipsum`

**dueDate** string

Due date of the task (ISO 8601 format)

Example:`2020-10-25T11:00:00Z`

**completed** boolean

Whether the task is completed

Example:`true`

**assignedTo** string

User Id to whom the task is assigned

Example:`hxHGVRb1YJUscrCB8eXK`

## Responses

- 200
- 400
- 401
- 422

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**task** object

Task details

**id** string

Unique identifier of the task

Example:`lJpzYrWdpkC2hX6t2yue`

**title** string

Title of the task

Example:`test`

**body** string

Body or description of the task

Example:`testing`

**assignedTo** string

User Id to whom the task is assigned

Example:`tesTUcmRxWrjqzJS8EjkxNKting`

**dueDate** string

Due date of the task (ISO 8601 format)

Example:`2021-07-08T02:30:00.000Z`

**completed** boolean

Whether the task is completed

Example:`true`

**contactId** string

Contact Id associated with the task

Example:`lJpzYrWdpkC2hX6t2yue`

```json
{
  "task": {
    "id": "lJpzYrWdpkC2hX6t2yue",
    "title": "test",
    "body": "testing",
    "assignedTo": "tesTUcmRxWrjqzJS8EjkxNK",
    "dueDate": "2021-07-08T02:30:00.000Z",
    "completed": true,
    "contactId": "lJpzYrWdpkC2hX6t2yue"
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
name: Authorizationtype: httpscopes: contacts.writescheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L -X PUT 'https://services.leadconnectorhq.com/contacts/:contactId/tasks/:taskId' \
-H 'Content-Type: application/json' \
-H 'Accept: application/json' \
-H 'Authorization: Bearer <TOKEN>' \
-d '{
  "title": "First Task",
  "body": "loram ipsum",
  "dueDate": "2020-10-25T11:00:00Z",
  "completed": true,
  "assignedTo": "hxHGVRb1YJUscrCB8eXK"
}'
```

Request Collapse all

Base URL

Edit

https://services.leadconnectorhq.com

Auth

Bearer Token

Parameters

contactId — pathrequired

taskId — pathrequired

Version — headerrequired

\-\-\-v3

Body required

```json
{
  "title": "First Task",
  "body": "loram ipsum",
  "dueDate": "2020-10-25T11:00:00Z",
  "completed": true,
  "assignedTo": "hxHGVRb1YJUscrCB8eXK"
}
```

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!