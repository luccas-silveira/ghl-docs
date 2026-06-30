---
title: "Get all Tasks"
source_url: https://marketplace.gohighlevel.com/docs/ghl/contacts/get-all-tasks
version: v3
method: GET
endpoint: https://services.leadconnectorhq.com/contacts/:contactId/tasks
---
# Get all Tasks

```
GET https://services.leadconnectorhq.com/contacts/:contactId/tasks
```


Get all Tasks

### Requirements

#### Scope(s)

`contacts.readonly`

#### Auth Method(s)

`OAuth Access Token``Private Integration Token`

#### Token Type(s)

`Sub-Account Token`

## Request [​](https://marketplace.gohighlevel.com/docs/ghl/contacts/get-all-tasks/\#request "Direct link to Request")

### Header Parameters

**Version** stringrequired

**Possible values:** \[`v3`\]

API Version

Example: v3

### Path Parameters

**contactId** stringrequired

Contact Id

Example: ve9EPM428h8vShlRW1KT

## Responses [​](https://marketplace.gohighlevel.com/docs/ghl/contacts/get-all-tasks/\#responses "Direct link to Responses")

- 200
- 400
- 401

Successful response

- application/json

- Schema
- Example (auto)

**Schema**

**tasks** object\[\]

List of tasks

Array \[\
\
**id** string\
\
Unique identifier of the task\
\
Example:`lJpzYrWdpkC2hX6t2yue`\
\
**title** string\
\
Title of the task\
\
Example:`test`\
\
**body** string\
\
Body or description of the task\
\
Example:`testing`\
\
**assignedTo** string\
\
User Id to whom the task is assigned\
\
Example:`tesTUcmRxWrjqzJS8EjkxNKting`\
\
**dueDate** string\
\
Due date of the task (ISO 8601 format)\
\
Example:`2021-07-08T02:30:00.000Z`\
\
**completed** boolean\
\
Whether the task is completed\
\
Example:`true`\
\
**contactId** string\
\
Contact Id associated with the task\
\
Example:`lJpzYrWdpkC2hX6t2yue`\
\
\]

```json
{
  "tasks": [\
    {\
      "id": "lJpzYrWdpkC2hX6t2yue",\
      "title": "test",\
      "body": "testing",\
      "assignedTo": "tesTUcmRxWrjqzJS8EjkxNK",\
      "dueDate": "2021-07-08T02:30:00.000Z",\
      "completed": true,\
      "contactId": "lJpzYrWdpkC2hX6t2yue"\
    }\
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
name: Authorizationtype: httpscopes: contacts.readonlyscheme: bearerbearerFormat: JWTin: headerdescription: Use the Access Token generated with user type as Sub-Account (OR) Private Integration Token of Sub-Account.
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
curl -L 'https://services.leadconnectorhq.com/contacts/:contactId/tasks' \
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

contactId — pathrequired

Version — headerrequired

\-\-\-v3

Send API Request

ResponseClear

Click the `Send API Request` button above and see the response here!